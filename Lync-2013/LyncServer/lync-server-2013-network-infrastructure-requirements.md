---
title: Lync Server 2013 网络基础结构要求
description: Lync Server 2013 网络基础结构要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network infrastructure requirements
ms:assetid: 35c7bb3f-8e0f-48b7-8a2c-857d4b42a4c4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425841(v=OCS.15)
ms:contentKeyID: 48183804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f7ff21c2f936ef8e048f6831d55408994055400
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425190"
---
# <a name="network-infrastructure-requirements-for-lync-server-2013"></a>Lync Server 2013 的网络基础结构要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-18_

Lync Server 2013 拓扑中每台服务器的网络适配器卡必须至少支持1千兆位/秒 (Gbps) 。 通常，你应使用低延迟和高带宽局域网 (局域网) 连接 Lync Server 拓扑中的所有服务器角色。 LAN 的大小取决于拓扑的大小：

  - 在标准版拓扑中，服务器应位于支持 1 Gbps 以太网或等效的网络中。

  - 在前端池拓扑中，大多数服务器应位于支持超过 1 Gbps 的网络中，尤其是支持音频/视频 (A/V) 会议和应用程序共享时。

对于公用电话交换网 (PSTN) 集成，可以使用 T1/E1 线路或 SIP 中继进行集成。

<div>

## <a name="audiovideo-network-requirements"></a>音频/视频网络要求

在 Lync Server 部署中，音频/视频 (A/V) 的网络要求包括以下内容：

  - 如果您使用 DNS 负载平衡部署单个边缘服务器或边缘池，则可以将外部防火墙配置为 NAT。 不能将内部防火墙配置为 NAT。 有关这些要求的详细信息，请参阅在规划文档中 [确定 Lync Server 2013 的外部 A/V 防火墙和端口要求](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md) 。
    
    <div>
    

    > [!IMPORTANT]  
    > 如果你有一个 Edge 池，并且使用的是硬件负载平衡器，则必须在每个边缘服务器上使用公共 IP 地址，并且不能在 NAT 设备上使用 NAT 来 (nat 入站或出站通信) 的其他基础结构设备。 有关详细信息，请参阅在规划外部用户访问文档中的 <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Lync Server 2013 中具有硬件负载平衡器的 "端口摘要-缩放的合并边缘</A> "。

    
    </div>

  - 如果您的组织使用了服务质量 (QoS) 基础结构，则媒体子系统应设计为在此现有基础结构中工作。

  - 如果使用 Internet 协议安全性 (IPsec)，建议在用于 A/V 流量的端口范围内禁用 IPsec。 有关详细信息，请参阅规划文档中的 [Lync Server 2013 中的 IPsec 异常](lync-server-2013-ipsec-exceptions.md) 。

若要确保最佳的媒体质量，请执行下列操作：

  - 将您的网络链接设置为支持每秒 65 kb 的吞吐量，每秒 kbps，每个视频流 kbps，在高峰使用期内启用 (500) Kbps。 双向音频或视频会话由两个流组成。

  - 为了处理此级别以上流量中的意外峰值和延长使用时间，Lync Server 媒体终结点可以适应不同的网络条件，并支持加载三倍的网络条件 (查看音频和视频的以前段落) ，同时仍保持可接受的质量。 但是，不要假定此适应性将支持未预配的网络。 在预配网络中，Lync 服务器媒体终结点能够动态处理不同网络条件的能力 (例如，降低了临时数据包丢失) 。

  - 对于预配成本极其昂贵且非常困难的网络链接，你可能需要考虑为较低的流量量进行预配。 在这种情况下，让 Lync Server 媒体终结点的 elasticity 能够吸收流量音量与峰值流量级别之间的差异，降低语音质量的成本。 此外，还会减少余地的余地，但仍可吸收通信量突然出现高峰的情况。

  - 对于在短期内无法正确设置的链接 (例如，具有非常差的 WAN 链接) 的网站，请考虑为某些用户禁用视频。

  - 设置您的网络以确保最大的端到端延迟 (延迟) 150 毫秒 (ms) 在 "高峰负载" 下。 延迟是 Lync Server 媒体组件无法减少的网络问题，查找和消除薄弱点非常重要。

  - 对于运行防病毒软件的服务器，请在例外列表中包括运行 Lync Server 的所有服务器，以便提供最佳性能和音频质量。

</div>

<div>

## <a name="conferencing-network-requirements"></a>会议网络要求

从 Internet 信息服务 (IIS) 服务器下载会议内容所使用的带宽取决于上载的内容的大小。

</div>

</div>

<span> </span>

</div>

</div>

</div>

