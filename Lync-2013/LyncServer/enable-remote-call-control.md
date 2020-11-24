---
title: 启用远程呼叫控制
description: 启用远程呼叫控制。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Enable remote call control
ms:assetid: 0b91d418-e6ed-4556-97af-e8523e01f249
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204664(v=OCS.15)
ms:contentKeyID: 48183380
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8009ffc927ad3f7a4f83ad3505100f3a9d4e82d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392029"
---
# <a name="enable-remote-call-control"></a>启用远程呼叫控制

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-02_

通过 "远程呼叫控制"，用户可以通过使用 Lync Server 2013 来控制其桌面专用分支 exchange (PBX) 电话。 如果你在旧环境中部署了远程呼叫控制，并且希望迁移到 Lync Server 2013，则需要执行以下任务：

1.  安装 SIP/CSTA 网关并将其配置为与你的 PBX 通信。 当您部署 Lync Server 2013 试验池时，您需要执行此步骤。

2.  合并拓扑并迁移策略和设置后，将 Lync Server 2013 配置为将 CSTA 请求路由到 SIP/CSTA 网关。 此步骤是遵循自动迁移的手动步骤。 若要为 CSTA 请求配置路由，请执行下列操作：
    
      - 删除旧版授权主机条目 (在 Lync Server 2013) 中称为 " *受信任服务器" 条目* 。 如果你要从旧部署迁移用户，请确保删除你为 SIP/CSTA 网关创建的所有现有授权主机条目，然后再在 Lync Server 2013 试验池上配置新的受信任的应用程序条目。 有关如何删除以前授权的主机条目的详细信息，请参阅 [删除授权主机条目](remove-an-authorized-host-entry.md)。
    
      - 为远程呼叫控制配置静态路由。 你可以为希望支持远程呼叫控制的单个池配置静态路由，也可以配置全局静态路由，以便未使用池级别的静态路由配置的每个池都使用全局静态路由。 有关如何配置静态路由的详细信息，请参阅部署文档中 [Lync Server 2013 中的 "为远程呼叫控制配置静态路由](lync-server-2013-configure-a-static-route-for-remote-call-control.md) "。
    
      - 在要支持远程呼叫控制的每个池上配置 "远程呼叫控制" 的受信任应用程序条目。 有关如何配置受信任的应用程序条目的详细信息，请参阅部署文档中的 [Lync Server 2013 中的 "配置受信任的应用程序项](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) "。

3.  如果你部署了使用传输控制协议 (TCP) 连接到 Lync Server 2013 的 SIP/CSTA 网关，请在拓扑生成器中定义网关的 IP 地址。 有关定义 IP 地址的详细信息，请参阅部署文档中 [Lync Server 2013 中的 "定义 SIP/CSTA 网关 IP 地址](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) "。

4.  通过启用远程呼叫控制并分配一行服务器统一资源标识符 (URI) 和行 URI，为远程呼叫控制配置 Lync 2013 用户。 将用户从旧版部署迁移到 Lync Server 2013 时，将迁移远程呼叫控制设置和其他用户设置。

5.  如果你在旧部署中自定义了通讯录电话号码规范化规则，则需要在完成策略和设置的自动迁移后执行一些手动任务以迁移自定义的规范化规则。 如果您没有自定义规范化规则，通讯簿将随拓扑的其余部分一起迁移。 有关手动迁移自定义规范化规则的详细信息，请参阅 [迁移通讯簿](migrate-address-book.md)。

</div>

<span> </span>

</div>

</div>

</div>

