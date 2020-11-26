---
title: Lync Server 2013：SIP 中继部署清单
description: Lync Server 2013： SIP 中继部署清单。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIP trunk deployment checklist
ms:assetid: 94f4f03e-19d5-4198-92be-e4076dbb959a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398755(v=OCS.15)
ms:contentKeyID: 48184891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbab9647a7146b2478317ab6c020969506f9c0ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423811"
---
# <a name="sip-trunk-deployment-checklist-for-lync-server-2013"></a><span data-ttu-id="abe5a-103">Lync Server 2013 的 SIP 中继部署清单</span><span class="sxs-lookup"><span data-stu-id="abe5a-103">SIP trunk deployment checklist for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abe5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abe5a-104">

<span> </span></span></span>

<span data-ttu-id="abe5a-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="abe5a-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="abe5a-106">你和你的服务提供商必须交换有关你的各个 SIP 中继终结点的一些基本连接信息，你才能部署 SIP 主干。</span><span class="sxs-lookup"><span data-stu-id="abe5a-106">Before you can deploy a SIP trunk, you and your service provider must exchange some basic connection information about your respective SIP trunk endpoints.</span></span>

<span data-ttu-id="abe5a-107">获取将连接到的每个 ITSP 网关的以下信息：</span><span class="sxs-lookup"><span data-stu-id="abe5a-107">Get the following information for each ITSP gateway that you will connect to:</span></span>

  - <span data-ttu-id="abe5a-108">IP 地址</span><span class="sxs-lookup"><span data-stu-id="abe5a-108">IP address</span></span>

  - <span data-ttu-id="abe5a-109"> (FQDN) 的完全限定的域名</span><span class="sxs-lookup"><span data-stu-id="abe5a-109">Fully qualified domain name (FQDN)</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="abe5a-110">服务提供商可能要求您连接到多个 ITSP 网关。</span><span class="sxs-lookup"><span data-stu-id="abe5a-110">The service provider may ask you to connect to more than one ITSP gateway.</span></span> <span data-ttu-id="abe5a-111">在这种情况下，必须在池中的每个 ITSP 网关和每个中介服务器之间配置连接。</span><span class="sxs-lookup"><span data-stu-id="abe5a-111">In that case, you must configure a connection between each ITSP gateway and each Mediation Server in your pool.</span></span>



</div>

<span data-ttu-id="abe5a-112">您提供给服务提供商的信息取决于 SIP 中继连接类型：</span><span class="sxs-lookup"><span data-stu-id="abe5a-112">The information you give to your service provider depends on your SIP trunk connection type:</span></span>

  - <span data-ttu-id="abe5a-113">对于多协议标签切换 (MPLS) 或专用网络连接，请为 ITSP 提供你的外围网络中的路由器的公共可路由 IP 地址 (也称为 DMZ、隔离区域和屏蔽子网) 。</span><span class="sxs-lookup"><span data-stu-id="abe5a-113">For Multiprotocol Label Switching (MPLS) or private network connections, give the ITSP the publicly routable IP Address of the router in your perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span> <span data-ttu-id="abe5a-114">验证 ITSP 上的网关或会话边界控制器 (SBC) 是否可以联系到此地址。</span><span class="sxs-lookup"><span data-stu-id="abe5a-114">Verify that the gateway or Session Border Controller (SBC) at the ITSP can reach this address.</span></span> <span data-ttu-id="abe5a-115">还为 ITSP 提供中介服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="abe5a-115">Also give the ITSP the FQDN of your Mediation Server.</span></span>

  - <span data-ttu-id="abe5a-116">对于虚拟专用网络 (VPN) 连接，为 ITSP 提供 VPN 服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="abe5a-116">For virtual private network (VPN) connections, give the ITSP the IP address of your VPN server.</span></span>

<div>

## <a name="certificate-considerations"></a><span data-ttu-id="abe5a-117">证书注意事项</span><span class="sxs-lookup"><span data-stu-id="abe5a-117">Certificate Considerations</span></span>

<span data-ttu-id="abe5a-118">若要确定是否需要用于 SIP 中继的证书，请查看有关协议支持的 ITSP：</span><span class="sxs-lookup"><span data-stu-id="abe5a-118">To determine whether you need a certificate for SIP trunking, check with your ITSP about protocol support:</span></span>

1.  <span data-ttu-id="abe5a-119">如果 ITSP 支持仅 (TCP) 传输控制协议，则不需要证书。</span><span class="sxs-lookup"><span data-stu-id="abe5a-119">If your ITSP supports Transmission Control Protocol (TCP) only, you do not need a certificate.</span></span>

2.  <span data-ttu-id="abe5a-120">如果你的 ITSP 支持 (TLS) 的传输层安全，则 ITSP 必须为你提供证书。</span><span class="sxs-lookup"><span data-stu-id="abe5a-120">If your ITSP supports Transport Layer Security (TLS), the ITSP must provide you with a certificate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="abe5a-121">SIP 与实时传输协议协同工作 (RTP) 或安全实时传输协议 (SRTP) ，通过 Internet 协议管理实际语音数据的协议 (VoIP) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="abe5a-121">SIP works in conjunction with real-time transport protocol (RTP) or secure real-time transport protocol (SRTP), the protocols that manage the actual voice data in Voice over Internet Protocol (VoIP) calls.</span></span>



</div>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="abe5a-122">部署过程</span><span class="sxs-lookup"><span data-stu-id="abe5a-122">Deployment Process</span></span>

<span data-ttu-id="abe5a-123">若要实现 SIP 中继连接的 Lync Server 一方，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="abe5a-123">To implement the Lync Server side of the SIP trunk connection, follow these steps:</span></span>

1.  <span data-ttu-id="abe5a-124">使用 Lync Server 拓扑生成器创建和配置 SIP 域拓扑。</span><span class="sxs-lookup"><span data-stu-id="abe5a-124">Using the Lync Server Topology Builder, create and configure the SIP domain topology.</span></span> <span data-ttu-id="abe5a-125">有关详细信息，请参阅在部署文档中的 [Lync Server 2013 的拓扑生成器中定义和配置拓扑](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md) 。</span><span class="sxs-lookup"><span data-stu-id="abe5a-125">For details, see [Define and configure a topology in Topology Builder for Lync Server 2013](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md) in the Deployment documentation.</span></span>

2.  <span data-ttu-id="abe5a-126">使用 Lync Server "控制面板" 为新的 SIP 域配置语音路由。</span><span class="sxs-lookup"><span data-stu-id="abe5a-126">Using the Lync Server Control Panel, configure voice routing for the new SIP domain.</span></span> <span data-ttu-id="abe5a-127">有关详细信息，请参阅部署文档中 [Lync Server 2013 中的 "配置中继](lync-server-2013-configuring-trunks.md) "。</span><span class="sxs-lookup"><span data-stu-id="abe5a-127">For details, see [Configuring trunks in Lync Server 2013](lync-server-2013-configuring-trunks.md) in the Deployment documentation.</span></span>

3.  <span data-ttu-id="abe5a-128">使用 **CsPstnOutboundCall** cmdlet 测试连接性。</span><span class="sxs-lookup"><span data-stu-id="abe5a-128">Test connectivity by using the **Test-CsPstnOutboundCall** cmdlet.</span></span> <span data-ttu-id="abe5a-129">有关详细信息，请参阅 lync server Management Shell 文档或 Lync Server 命令行管理程序的帮助。</span><span class="sxs-lookup"><span data-stu-id="abe5a-129">For details, see the Lync Server Management Shell documentation or Help for Lync Server Management Shell.</span></span>

<span data-ttu-id="abe5a-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abe5a-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

