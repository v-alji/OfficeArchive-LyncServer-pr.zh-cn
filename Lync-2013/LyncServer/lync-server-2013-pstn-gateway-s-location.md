---
title: Lync Server 2013：PSTN 网关的位置
description: Lync Server 2013： PSTN 网关的位置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392133"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a>Lync Server 2013 中 PSTN 网关的位置

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-03-09_

通过 PSTN 网关路由的呼叫以及 Pbx 可能需要 Location-Based 路由限制，具体取决于此类系统的位置。 可以按每个干线的粒度为单位启用 Location-Based 路由。

当在主干上启用时，Location-Based 路由会引入以下一组规则：

  - 在每个干线基础上启用 Location-Based 路由时，该主干上定义的规则将仅应用于通过该主干路由的呼叫。

  - 若要防止 PSTN tolls 绕过从网络站点（PSTN 网关所在的网络站点不同）调用的位置，请 Location-Based 路由引入了网络站点与给定主干的关联。 这定义了允许呼叫路由到给定中继的网络站点。

可以通过以下两种方式为 Location-Based 路由启用中继：

  - 为中继定义将呼叫发出到 PSTN 的 PSTN 网关。此类型的中继路由的传入呼叫只能路由到位于与中继相同的网络站点中的终结点。

  - 主干是针对中介服务器对等方定义的，它不会向在静态位置 (（即 PBX 电话) ）的 PSTN 和服务用户传出呼叫。 对于此特殊配置，此类型的中继路由的传入呼叫将视为来自与中继相同的网络站点。 来自 PBX 用户的呼叫将具有与与主干相同的网络站点中的 Lync 用户的相同 Location-Based 路由强制。 如果位于单独网络站点的两个 PBX 系统通过 Lync Server 连接，Location-Based 路由将允许从一个网络站点中的一个 PBX 终结点路由到另一个网络站点中的另一个 PBX 终结点。 Location-Based 路由不会阻止此方案。 除了此方案以及与同一位置的 Lync 用户类似的情况下，连接到具有此配置的中介服务器对等的终结点将能够在不将调用路由)  (到其他中介服务器对等的情况下发出或接收来自其他中介服务器对等的呼叫，而不考虑与中介服务器对等关联的网络站点。 所有入站呼叫、出站呼叫、呼叫转接和涉及 PSTN 终结点的转接将根据基于位置的路由，仅使用定义为本中介服务器对等的本地的 PSTN 网关。

<div>

## <a name="see-also"></a>另请参阅


[Lync Server 2013 中基于位置的路由指南](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

