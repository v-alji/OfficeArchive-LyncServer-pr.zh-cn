---
title: Lync Server 2013：用户的位置
description: Lync Server 2013：用户的位置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User's location
ms:assetid: ce57941d-086b-448e-8ada-c7d636a2a1c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994073(v=OCS.15)
ms:contentKeyID: 51803984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a92ec780809cdb3e1ee582ce6c348c884bbb5890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439168"
---
# <a name="users-location-in-lync-server-2013"></a>Lync Server 2013 中用户的位置

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-03-09_

Location-Based 路由利用在 Lync Server 中定义的相同网络区域、网站和子网，E9 在 Lync Server 中使用，它是由 CAC 和媒体旁路以应用呼叫路由限制来防止 PSTN 免绕过。 用户的位置由连接 (s) 的用户 Lync 终结点的 IP 子网确定。 每个 IP 子网都与一个网络站点相关联，它们将聚合到由管理员确定的网络区域中。 基于位置的路由基于用户的网络站点强制实施。

Location-Based 路由规则针对每个网络站点应用，这意味着给定的一组规则将应用于为位于同一网络站点内的 Location-Based 路由启用的所有终结点。 管理员可以将基于位置的路由应用于需要它的网络站点。

可以在每个网络站点上定义语音路由策略，以定义应由网络站点内的所有用户用于呼叫 PSTN 号码的特殊 PSTN 网关。 当用户位于为 Location-Based 路由启用的网络网站时，此类语音路由策略将优先于用户的语音策略所定义的路由，并且将阻止通过已启用 Location-Based 路由的其他 PSTN 网关路由呼叫。 当 Lync 用户发出 PSTN 呼叫时，用户的语音策略确定是否可以授权用户进行呼叫。 如果用户的语音策略允许用户进行呼叫，Location-Based 路由确定呼叫应传出的 PSTN 网关。 Location-Based 路由根据用户的位置进行此确定。

用户位置可以通过以下方式进行分类：

  - 用户位于为 Location-Based 路由启用的已知网络网站，并且其 (直接拨入式拨号) 号码将在放置在同一网络站点 (（即 office) ）的 PSTN 网关上终止。 出站呼叫通过用户所在的网络站点的语音路由策略进行路由。 发往用户的传入 PSTN 呼叫将路由到与 PSTN 网关位于相同网络站点中的终结点。

  - 用户所在的已知网络站点不同于 PSTN 网关所在的网络站点。（例如，用户前往另一公司办事处出差。）出站呼叫使用用户所在的网络站点的语音路由策略进行路由。发往用户的传入 PSTN 呼叫不会路由到所在站点与 PSTN 网关不同的终结点，从而防止 PSTN 收费绕路情形。

  - 当用户位于 Lync Server 部署未知的网络网站中时，出站呼叫的路由将基于为用户分配给未绑定到 Location-Based 路由限制的 PSTN 网关的语音策略。 传入 PSTN 呼叫不会路由到位于未知网络站点内的终结点，从而防止 PSTN 收费绕路情形。

<div>

## <a name="see-also"></a>另请参阅


[Lync Server 2013 中基于位置的路由指南](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

