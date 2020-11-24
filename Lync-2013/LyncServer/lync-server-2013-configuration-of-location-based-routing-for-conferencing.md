---
title: Lync Server 2013：会议的基于位置的路由的配置
description: Lync Server 2013：为会议 Location-Based 路由的配置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392418"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Lync Server 2013 中会议的基于位置的路由的配置

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-09-11_

Location-Based 路由会议应用程序依赖于 Lync Server 2013 的配置 Location-Based 路由。 主要配置如下：

  - 加入会议的参与者的位置基于其网络站点进行确定。 必须在 Lync Server 中定义网络网站及其关联的网络子网，才能强制 Location-Based 路由。

  - 若要强制 Location-Based 路由会议，必须为 Lync 参与者启用 Location-Based 路由。

  - 若要强制 Location-Based 路由 PSTN 终结点加入会议，必须为 Location-Based 路由配置用于连接 PSTN 终结点的 SIP 中继。

有关部署和配置 Lync Server 2013 Location-Based 路由的其他信息，请参阅配置 [基于位置的路由](lync-server-2013-configuring-location-based-routing.md)。

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a>启用 Location-Based 路由会议应用程序

默认情况下，Location-Based "路由会议" 应用程序处于禁用状态。 在启用此应用程序之前，您需要确定要为该应用程序分配的适当优先级。 若要确定此优先级，请在 Lync Server 命令行管理程序中运行以下 cmdlet：

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

在此 cmdlet 中， \<Pool FQDN\> 是要启用 Location-Based 路由会议应用程序的池。

此 cmdlet 将返回由 Lync Server 托管的应用程序的列表及其每个应用程序的优先级值。 需要为 Location-Based 路由会议应用程序分配比 "UdcAgent" 应用程序更大的优先级值，并小于 "DefaultRouting"、"ExumRouting" 和 "OutboundRouting" 应用程序。 我们建议你为 Location-Based 路由会议应用程序分配一个比 "UdcAgent" 应用程序优先级值更高的优先级值。

例如，如果 "UdcAgent" 应用程序的优先级值为 "2"，"DefaultRouting" 应用程序的优先级值为 "8"，"ExumRouting" 应用程序的优先级值为 "9"，"OutboundRouting" 应用程序的优先级值为 "10"，则你应该为 Location-Based 路由会议应用程序分配优先级值 "3"。 这样做将按以下顺序设定应用程序的优先级：其他应用程序（优先级：0 到 1）、“UdcAgent”（优先级：2）、基于位置的路由会议应用程序（优先级：3）、其他应用程序（优先级：4 到 8）、“DefaultRouting”（优先级：9）、“ExumRouting”（优先级：10）和“OutboundRouting”（优先级：11）。

找到 Location-Based 路由会议应用程序的正确优先级值后，为每个 Front-End 池或标准版服务器键入以下 cmdlet，以便为 Location-Based 路由启用的家庭用户：

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

例如：

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

使用此 cmdlet 后，重启池中的所有前端服务器或 Location-Based 路由会议应用程序已启用的标准版服务器。

<div>


> [!IMPORTANT]  
> Location-Based 路由 enforcements 到会议或咨询式传输，直到适用的池中的所有前端服务器或标准版服务器重新启动后才会强制执行。



</div>

一旦已成功启用 Location-Based 路由会议应用程序并重新启动所有适用的 Lync 服务器，将监视所有已启用了 Location-Based 路由的 Lync 用户组织的会议，以防止 PSTN 免绕过

</div>

</div>

<span> </span>

</div>

</div>

</div>

