---
title: Lync Server 2013：同时响铃
description: Lync 服务器2013：同时拨打。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Simultaneous ringing
ms:assetid: df02f919-4d50-4832-9300-6c51f8b4fc56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994079(v=OCS.15)
ms:contentKeyID: 51803990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 595c8c1d4ce105e2189002f18733ffae92cff8bf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423818"
---
# <a name="simultaneous-ringing-in-lync-server-2013"></a><span data-ttu-id="00749-103">Lync Server 2013 中的同时响铃</span><span class="sxs-lookup"><span data-stu-id="00749-103">Simultaneous ringing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00749-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00749-104">

<span> </span></span></span>

<span data-ttu-id="00749-105">_**主题上次修改时间：** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="00749-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="00749-106">当被呼叫方启用同时拨打时，Location-Based 路由将分析呼叫方的位置和被呼叫方的终结点，以确定是否应路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="00749-106">When the called party has simultaneous ringing enabled, Location-Based Routing analyzes the location of the calling party and the endpoints of the called parties to determine whether the call should be routed.</span></span>

<span data-ttu-id="00749-107">下表说明配置了同时响铃的用户，同时响铃目标是位于相同网络站点中的用户、位于不同网络站点中的用户或者位于未知网络站点中的用户。</span><span class="sxs-lookup"><span data-stu-id="00749-107">The following table illustrates a user configured with simultaneous ringing, and the simultaneous ringing target is a user in the same network site, in a different network site, or in an unknown network site.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00749-108">传入 PSTN 呼叫</span><span class="sxs-lookup"><span data-stu-id="00749-108">Incoming PSTN call for</span></span></th>
<th><span data-ttu-id="00749-109">位于与被呼叫者相同的网络站点中</span><span class="sxs-lookup"><span data-stu-id="00749-109">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="00749-110">位于与被呼叫者不同的网络站点中</span><span class="sxs-lookup"><span data-stu-id="00749-110">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="00749-111">位于未知的网络网站中，或者未启用 Location-Based 路由</span><span class="sxs-lookup"><span data-stu-id="00749-111">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00749-112">Lync 用户</span><span class="sxs-lookup"><span data-stu-id="00749-112">Lync user</span></span></p></td>
<td><p><span data-ttu-id="00749-113">允许同时响铃</span><span class="sxs-lookup"><span data-stu-id="00749-113">Simultaneous ring allowed</span></span></p></td>
<td><p><span data-ttu-id="00749-114">不允许同时响铃</span><span class="sxs-lookup"><span data-stu-id="00749-114">Simultaneous ring not allowed</span></span></p></td>
<td><p><span data-ttu-id="00749-115">不允许同时响铃</span><span class="sxs-lookup"><span data-stu-id="00749-115">Simultaneous ring not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="00749-116">下表说明了来自 Lync 用户的呼叫 (即 Lync 呼叫者) 在同一网络站点、不同网络站点或未知网络站点中。</span><span class="sxs-lookup"><span data-stu-id="00749-116">The following table illustrates a call from a Lync user (i.e. Lync caller) in the same network site, in a different network site, or from an unknown network site.</span></span> <span data-ttu-id="00749-117">被呼叫者将 PSTN 终结点（如移动电话）配置为同时响铃目标。</span><span class="sxs-lookup"><span data-stu-id="00749-117">The callee has a PSTN endpoint (i.e. cellphone) configured as a simultaneous ring target.</span></span> <span data-ttu-id="00749-118">在这种情况下，Location-Based 路由将确定是否应将呼叫路由到同时拨打的目标 (（即被调用方的手机) ）。</span><span class="sxs-lookup"><span data-stu-id="00749-118">In this scenario, Location-Based Routing will determine whether the call should be routed to the simultaneous ring target (i.e. cellphone) of the callee or not.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00749-119">同时响铃目标</span><span class="sxs-lookup"><span data-stu-id="00749-119">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="00749-120">位于与被呼叫者相同的网络站点中</span><span class="sxs-lookup"><span data-stu-id="00749-120">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="00749-121">位于与被呼叫者不同的网络站点中</span><span class="sxs-lookup"><span data-stu-id="00749-121">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="00749-122">位于未知的网络网站中，或者未启用 Location-Based 路由</span><span class="sxs-lookup"><span data-stu-id="00749-122">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00749-123">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="00749-123">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="00749-124">允许通过呼叫者的站点语音路由策略同时响铃</span><span class="sxs-lookup"><span data-stu-id="00749-124">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="00749-125">允许通过呼叫者的站点语音路由策略同时响铃</span><span class="sxs-lookup"><span data-stu-id="00749-125">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="00749-126">允许通过呼叫者的语音策略向未启用基于位置的路由的中继同时响铃</span><span class="sxs-lookup"><span data-stu-id="00749-126">Simultaneous ring allowed through the caller’s voice policy to trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="00749-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00749-127">See Also</span></span>


[<span data-ttu-id="00749-128">Lync Server 2013 中基于位置的路由的方案</span><span class="sxs-lookup"><span data-stu-id="00749-128">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="00749-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00749-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

