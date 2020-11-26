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
# <a name="users-location-in-lync-server-2013"></a><span data-ttu-id="988b2-103">Lync Server 2013 中用户的位置</span><span class="sxs-lookup"><span data-stu-id="988b2-103">User's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="988b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="988b2-104">

<span> </span></span></span>

<span data-ttu-id="988b2-105">_**主题上次修改时间：** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="988b2-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="988b2-106">Location-Based 路由利用在 Lync Server 中定义的相同网络区域、网站和子网，E9 在 Lync Server 中使用，它是由 CAC 和媒体旁路以应用呼叫路由限制来防止 PSTN 免绕过。</span><span class="sxs-lookup"><span data-stu-id="988b2-106">Location-Based Routing leverages the same network regions, sites and subnets as defined in Lync Server used by E9-1-1, CAC and Media Bypass to apply call routing restrictions to prevent PSTN toll bypass.</span></span> <span data-ttu-id="988b2-107">用户的位置由连接 (s) 的用户 Lync 终结点的 IP 子网确定。</span><span class="sxs-lookup"><span data-stu-id="988b2-107">A user’s location is determined by the IP subnet of the user’s Lync endpoint(s) are connected from.</span></span> <span data-ttu-id="988b2-108">每个 IP 子网都与一个网络站点相关联，它们将聚合到由管理员确定的网络区域中。</span><span class="sxs-lookup"><span data-stu-id="988b2-108">Each IP subnet is associated to a network site, which are aggregated into network regions defined by the administrator.</span></span> <span data-ttu-id="988b2-109">基于位置的路由基于用户的网络站点强制实施。</span><span class="sxs-lookup"><span data-stu-id="988b2-109">Location-Based Routing is enforced based on the user’s network site.</span></span>

<span data-ttu-id="988b2-110">Location-Based 路由规则针对每个网络站点应用，这意味着给定的一组规则将应用于为位于同一网络站点内的 Location-Based 路由启用的所有终结点。</span><span class="sxs-lookup"><span data-stu-id="988b2-110">Location-Based Routing rules are applied on a per network site basis, meaning that a given set of rules will be applied to all endpoints enabled for Location-Based Routing that are located within the same network site.</span></span> <span data-ttu-id="988b2-111">管理员可以将基于位置的路由应用于需要它的网络站点。</span><span class="sxs-lookup"><span data-stu-id="988b2-111">Administrators can apply Location-Based Routing to network sites that require it.</span></span>

<span data-ttu-id="988b2-112">可以在每个网络站点上定义语音路由策略，以定义应由网络站点内的所有用户用于呼叫 PSTN 号码的特殊 PSTN 网关。</span><span class="sxs-lookup"><span data-stu-id="988b2-112">Voice routing policies can be defined on a per network site basis to define a particular PSTN gateway that should be used by all users located in the network site to call PSTN phone numbers.</span></span> <span data-ttu-id="988b2-113">当用户位于为 Location-Based 路由启用的网络网站时，此类语音路由策略将优先于用户的语音策略所定义的路由，并且将阻止通过已启用 Location-Based 路由的其他 PSTN 网关路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="988b2-113">Such voice routing policies will take precedence over the routing defined by the user’s voice policy when the user is located in a network site enabled for Location-Based Routing, and it will prevent the routing of calls via other PSTN gateways that are enabled for Location-Based Routing.</span></span> <span data-ttu-id="988b2-114">当 Lync 用户发出 PSTN 呼叫时，用户的语音策略确定是否可以授权用户进行呼叫。</span><span class="sxs-lookup"><span data-stu-id="988b2-114">When a Lync user places a PSTN call, the user’s voice policy determines whether the user can be authorized to place the call.</span></span> <span data-ttu-id="988b2-115">如果用户的语音策略允许用户进行呼叫，Location-Based 路由确定呼叫应传出的 PSTN 网关。</span><span class="sxs-lookup"><span data-stu-id="988b2-115">If the user’s voice policy allows the user to place the call, Location-Based Routing determines which PSTN gateway the call should egress from.</span></span> <span data-ttu-id="988b2-116">Location-Based 路由根据用户的位置进行此确定。</span><span class="sxs-lookup"><span data-stu-id="988b2-116">Location-Based Routing makes this determination based on the user’s location.</span></span>

<span data-ttu-id="988b2-117">用户位置可以通过以下方式进行分类：</span><span class="sxs-lookup"><span data-stu-id="988b2-117">A user location can be categorized in the following ways:</span></span>

  - <span data-ttu-id="988b2-118">用户位于为 Location-Based 路由启用的已知网络网站，并且其 (直接拨入式拨号) 号码将在放置在同一网络站点 (（即 office) ）的 PSTN 网关上终止。</span><span class="sxs-lookup"><span data-stu-id="988b2-118">The user is located in a known network site enabled for Location-Based Routing and his DID (Direct Inward Dial) number terminates on a PSTN gateway placed in the same network site (i.e. office).</span></span> <span data-ttu-id="988b2-119">出站呼叫通过用户所在的网络站点的语音路由策略进行路由。</span><span class="sxs-lookup"><span data-stu-id="988b2-119">The routing of outbound calls will be through the voice routing policy of the network site in which the user is located.</span></span> <span data-ttu-id="988b2-120">发往用户的传入 PSTN 呼叫将路由到与 PSTN 网关位于相同网络站点中的终结点。</span><span class="sxs-lookup"><span data-stu-id="988b2-120">Incoming PSTN calls to the user are routed to endpoints that are located in the same network site as the PSTN gateway.</span></span>

  - <span data-ttu-id="988b2-p105">用户所在的已知网络站点不同于 PSTN 网关所在的网络站点。（例如，用户前往另一公司办事处出差。）出站呼叫使用用户所在的网络站点的语音路由策略进行路由。发往用户的传入 PSTN 呼叫不会路由到所在站点与 PSTN 网关不同的终结点，从而防止 PSTN 收费绕路情形。</span><span class="sxs-lookup"><span data-stu-id="988b2-p105">The user is located in a known network site that is in different from the network site where the PSTN gateway is located. (i.e. the user traveled to another corporate office). The routing of outbound calls will be using the voice routing policy of the network site in which the user is located. Incoming PSTN calls to the user will not be routed to endpoints that are located in different sites than the PSTN gateway to prevent PSTN toll bypassing.</span></span>

  - <span data-ttu-id="988b2-125">当用户位于 Lync Server 部署未知的网络网站中时，出站呼叫的路由将基于为用户分配给未绑定到 Location-Based 路由限制的 PSTN 网关的语音策略。</span><span class="sxs-lookup"><span data-stu-id="988b2-125">When a user is located in a network site that is unknown to the Lync Server deployment, the routing of outbound calls will be based on the voice policy assigned to the user to PSTN gateways not bound to Location-Based Routing restrictions.</span></span> <span data-ttu-id="988b2-126">传入 PSTN 呼叫不会路由到位于未知网络站点内的终结点，从而防止 PSTN 收费绕路情形。</span><span class="sxs-lookup"><span data-stu-id="988b2-126">Incoming PSTN calls will not be routed to endpoints that are located in unknown network sites to prevent PSTN toll bypassing.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="988b2-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="988b2-127">See Also</span></span>


[<span data-ttu-id="988b2-128">Lync Server 2013 中基于位置的路由指南</span><span class="sxs-lookup"><span data-stu-id="988b2-128">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="988b2-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="988b2-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

