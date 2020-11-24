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
# <a name="pstn-gateways-location-in-lync-server-2013"></a><span data-ttu-id="293c4-103">Lync Server 2013 中 PSTN 网关的位置</span><span class="sxs-lookup"><span data-stu-id="293c4-103">PSTN gateway's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="293c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="293c4-104">

<span> </span></span></span>

<span data-ttu-id="293c4-105">_**主题上次修改时间：** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="293c4-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="293c4-106">通过 PSTN 网关路由的呼叫以及 Pbx 可能需要 Location-Based 路由限制，具体取决于此类系统的位置。</span><span class="sxs-lookup"><span data-stu-id="293c4-106">Calls routed via PSTN gateways and PBXs might require Location-Based Routing restrictions depending on the location of such systems.</span></span> <span data-ttu-id="293c4-107">可以按每个干线的粒度为单位启用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="293c4-107">Location-Based Routing can be enabled at the granularity on a per trunk basis.</span></span>

<span data-ttu-id="293c4-108">当在主干上启用时，Location-Based 路由会引入以下一组规则：</span><span class="sxs-lookup"><span data-stu-id="293c4-108">Location-Based Routing introduces the following set of rules when enabled on a trunk:</span></span>

  - <span data-ttu-id="293c4-109">在每个干线基础上启用 Location-Based 路由时，该主干上定义的规则将仅应用于通过该主干路由的呼叫。</span><span class="sxs-lookup"><span data-stu-id="293c4-109">When Location-Based Routing is enabled on a per trunk basis, the rules define on that trunk will be applied only to calls routed through that trunk.</span></span>

  - <span data-ttu-id="293c4-110">若要防止 PSTN tolls 绕过从网络站点（PSTN 网关所在的网络站点不同）调用的位置，请 Location-Based 路由引入了网络站点与给定主干的关联。</span><span class="sxs-lookup"><span data-stu-id="293c4-110">To prevent PSTN tolls bypass where calls originate from a network site different that the network site where the PSTN gateway is located, Location-Based Routing introduces the association of a network site to a given trunk.</span></span> <span data-ttu-id="293c4-111">这定义了允许呼叫路由到给定中继的网络站点。</span><span class="sxs-lookup"><span data-stu-id="293c4-111">This defines the network site that allows calls to be routed to a given trunk.</span></span>

<span data-ttu-id="293c4-112">可以通过以下两种方式为 Location-Based 路由启用中继：</span><span class="sxs-lookup"><span data-stu-id="293c4-112">Trunks can be enabled for Location-Based Routing in two ways:</span></span>

  - <span data-ttu-id="293c4-p103">为中继定义将呼叫发出到 PSTN 的 PSTN 网关。此类型的中继路由的传入呼叫只能路由到位于与中继相同的网络站点中的终结点。</span><span class="sxs-lookup"><span data-stu-id="293c4-p103">The trunk is defined for a PSTN gateway that egresses calls to the PSTN. Incoming calls routed by a trunk of this type will be routed only to endpoints located within the same network site as the trunk.</span></span>

  - <span data-ttu-id="293c4-115">主干是针对中介服务器对等方定义的，它不会向在静态位置 (（即 PBX 电话) ）的 PSTN 和服务用户传出呼叫。</span><span class="sxs-lookup"><span data-stu-id="293c4-115">The trunk is defined for a Mediation Server peer that doesn’t egress calls to the PSTN and services users with legacy phones in a static locations (i.e. PBX phones).</span></span> <span data-ttu-id="293c4-116">对于此特殊配置，此类型的中继路由的传入呼叫将视为来自与中继相同的网络站点。</span><span class="sxs-lookup"><span data-stu-id="293c4-116">For this particular configuration, all incoming calls routed by a trunk of this type will be considered to be originating from the same network site as the trunk.</span></span> <span data-ttu-id="293c4-117">来自 PBX 用户的呼叫将具有与与主干相同的网络站点中的 Lync 用户的相同 Location-Based 路由强制。</span><span class="sxs-lookup"><span data-stu-id="293c4-117">Calls from PBX users will have the same Location-Based Routing enforcement as Lync users who are located in the same network site as the trunk.</span></span> <span data-ttu-id="293c4-118">如果位于单独网络站点的两个 PBX 系统通过 Lync Server 连接，Location-Based 路由将允许从一个网络站点中的一个 PBX 终结点路由到另一个网络站点中的另一个 PBX 终结点。</span><span class="sxs-lookup"><span data-stu-id="293c4-118">If two PBX systems located in separate network sites are connected through Lync Server, Location-Based Routing will allow routing from one PBX endpoint in one network site to another PBX endpoint in the other network site.</span></span> <span data-ttu-id="293c4-119">Location-Based 路由不会阻止此方案。</span><span class="sxs-lookup"><span data-stu-id="293c4-119">This scenario will not be blocked by Location-Based Routing.</span></span> <span data-ttu-id="293c4-120">除了此方案以及与同一位置的 Lync 用户类似的情况下，连接到具有此配置的中介服务器对等的终结点将能够在不将调用路由)  (到其他中介服务器对等的情况下发出或接收来自其他中介服务器对等的呼叫，而不考虑与中介服务器对等关联的网络站点。</span><span class="sxs-lookup"><span data-stu-id="293c4-120">In addition to this scenario and in a similar way as a Lync user in the same location, endpoints connected to a Mediation Server peer with this configuration will be able to make or receive calls to and from other Mediation Server peer that do not route calls to the PSTN (i.e. an endpoint connected to a different PBX) regardless of the network site to which the Mediation Server peer is associated.</span></span> <span data-ttu-id="293c4-121">所有入站呼叫、出站呼叫、呼叫转接和涉及 PSTN 终结点的转接将根据基于位置的路由，仅使用定义为本中介服务器对等的本地的 PSTN 网关。</span><span class="sxs-lookup"><span data-stu-id="293c4-121">All inbound calls, outbound calls, call transfers and call forwards involving PSTN endpoints will be subject to Location Based Routing to use only PSTN gateways that are defined as local to such Mediation Server peer.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="293c4-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="293c4-122">See Also</span></span>


[<span data-ttu-id="293c4-123">Lync Server 2013 中基于位置的路由指南</span><span class="sxs-lookup"><span data-stu-id="293c4-123">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="293c4-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="293c4-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

