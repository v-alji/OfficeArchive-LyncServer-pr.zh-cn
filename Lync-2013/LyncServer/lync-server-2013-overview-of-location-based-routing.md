---
title: Lync Server 2013： Location-Based 路由概述
description: Lync Server 2013： Location-Based 路由的概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392328"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="bdbe8-103">Lync Server 2013 中的 Location-Based 路由概述</span><span class="sxs-lookup"><span data-stu-id="bdbe8-103">Overview of Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bdbe8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bdbe8-104">

<span> </span></span></span>

<span data-ttu-id="bdbe8-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="bdbe8-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="bdbe8-p101">基于位置的路由引入了一组新规则，它们可修改国内和国际 PSTN 呼叫的路由以防止收费绕路情形。使用基于位置的路由可灵活地将这些规则限定为仅特定区域、特定网关或特定用户集。</span><span class="sxs-lookup"><span data-stu-id="bdbe8-p101">Location-Based Routing introduces a new set of rules that modifies the routing of national and international PSTN calls to prevent toll bypass. Location-Based Routing provides the flexibility to scope these rules to specific regions, specific gateways or to specific set of users only.</span></span>

<span data-ttu-id="bdbe8-108">以下方案说明了 Location-Based 路由可以强制使用的主要限制类型：</span><span class="sxs-lookup"><span data-stu-id="bdbe8-108">The following scenarios illustrate the main types of restrictions Location-Based Routing can enforce:</span></span>

  - <span data-ttu-id="bdbe8-109">外出呼叫-Location-Based 路由可以强制传出调用来自与呼叫者在同一区域的 PSTN 网关的传出呼叫，该网关与呼叫者阻止 PSTN 免绕过，防止呼叫来自另一个地区的 PSTN 网关的外出。</span><span class="sxs-lookup"><span data-stu-id="bdbe8-109">Egress calls – Location-Based Routing can enforce outgoing calls to egress from a PSTN gateway that is located in the same region as where the caller is to prevent PSTN toll bypass, which prevents calls to egress from a PSTN gateway located in a different region as the caller.</span></span>

  - <span data-ttu-id="bdbe8-110">入站呼叫-如果 PSTN 网关路由传入呼叫与被呼叫的 Lync 用户不在同一地区，则 Location-Based 路由可以阻止传入的 PSTN 呼叫拨打 Lync 终结点。</span><span class="sxs-lookup"><span data-stu-id="bdbe8-110">Ingress calls – Location-Based Routing can prevent incoming PSTN calls to ring Lync endpoints if the PSTN gateway routing the incoming call is not located in the same region as the called Lync user.</span></span>

  - <span data-ttu-id="bdbe8-111">未知区域-Location-Based 路由对位于不确定 (位置的用户（即从 Internet 连接或位于未知区域) 的远程用户）限制传入和传出 PSTN 呼叫。</span><span class="sxs-lookup"><span data-stu-id="bdbe8-111">Unknown regions – Location-Based Routing restricts incoming and outgoing PSTN calls to and from users that are located in undetermined locations (i.e. remote users connecting from the Internet or located in unknown regions).</span></span>

  - <span data-ttu-id="bdbe8-112">国际区域-如果找不到用户所在位置的网关，Location-Based 路由通过国际 PSTN 网关对传出呼叫进行路由。</span><span class="sxs-lookup"><span data-stu-id="bdbe8-112">International regions – Location-Based Routing enforces routing of outgoing calls through international PSTN gateways if a gateway local to the user’s location cannot be found.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="bdbe8-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bdbe8-113">See Also</span></span>


[<span data-ttu-id="bdbe8-114">在 Lync Server 2013 中规划基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="bdbe8-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="bdbe8-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bdbe8-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

