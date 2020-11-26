---
title: Lync Server 2013：传入呼叫
description: Lync Server 2013：传入呼叫。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Incoming calls
ms:assetid: 65b9c1b4-6af7-4527-8c33-22c4442bd209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994038(v=OCS.15)
ms:contentKeyID: 51803948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a72c7fc378240f9751eae8e6c24e9cc601b08d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427297"
---
# <a name="incoming-calls-in-lync-server-2013"></a><span data-ttu-id="b98c0-103">Lync Server 2013 中的传入呼叫</span><span class="sxs-lookup"><span data-stu-id="b98c0-103">Incoming calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b98c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b98c0-104">

<span> </span></span></span>

<span data-ttu-id="b98c0-105">_**主题上次修改时间：** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="b98c0-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="b98c0-106">为 Location-Based 路由启用的用户传入呼叫的路由取决于用户终结点的位置。</span><span class="sxs-lookup"><span data-stu-id="b98c0-106">The routing of incoming calls to users enabled for Location-Based Routing depends on the location of the user’s endpoint.</span></span> <span data-ttu-id="b98c0-107">传入呼叫的路由通过以下方式受到影响。</span><span class="sxs-lookup"><span data-stu-id="b98c0-107">The routing of incoming calls is affected in the following way.</span></span> <span data-ttu-id="b98c0-108">如果用户对位于启用的 Location-Based 路由网络站点中的终结点进行传入呼叫，并且终结点与 PSTN 网关位于同一网络站点，则将路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="b98c0-108">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in the same network site as the PSTN gateway, the call will be routed.</span></span> <span data-ttu-id="b98c0-109">如果用户对位于启用的支持路由的网络站点 Location-Based 中的终结点进行传入呼叫，并且终结点所在的网络站点与 PSTN 网关不同，则不会路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="b98c0-109">If a user has an incoming call to an endpoint located in a Location-Based Routing enabled network site, and the endpoint is located in a different network site than the PSTN gateway, the call will not be routed.</span></span> <span data-ttu-id="b98c0-110">当用户没有终结点位于与发出传入呼叫的 PSTN 网关相同的网络站点中时，则传入呼叫将直接路由到用户的语音邮件，并且将向被呼叫方发送错过的呼叫通知。</span><span class="sxs-lookup"><span data-stu-id="b98c0-110">When a user has no endpoints located in the same network site as the PSTN gateway where the incoming call is originating from, the incoming call will be routed directly to the user’s voicemail and a missed call notification will be sent to the called party.</span></span>

<span data-ttu-id="b98c0-111">已启用 Location-Based 路由的用户的呼叫转接设置将继续强制执行，但转发的呼叫将受到用户 Location-Based 路由限制的约束。</span><span class="sxs-lookup"><span data-stu-id="b98c0-111">The call forwarding settings of a user that is enabled for Location-Based Routing will continue to be enforced, however, calls forwarded will be subject to Location-Based Routing restrictions of the user.</span></span>

<span data-ttu-id="b98c0-112">下表说明了 Location-Based 路由如何影响传入呼叫的路由，具体取决于被呼叫方终结点的位置。</span><span class="sxs-lookup"><span data-stu-id="b98c0-112">The following table illustrates how Location-Based Routing affects the routing of inbound calls depending on the location of the callee’s endpoint.</span></span> <span data-ttu-id="b98c0-113">PSTN 网关的网络站点已启用 Location-Based 路由，Location-Based 路由只允许将 PSTN 呼叫路由到同一网络站点内的终结点。</span><span class="sxs-lookup"><span data-stu-id="b98c0-113">The network site of the PSTN gateway is enabled for Location-Based Routing, and Location-Based Routing only permits routing of PSTN calls to endpoints within the same network site.</span></span>

### <a name="callee-receiving-an-inbound-call-from-the-pstn"></a><span data-ttu-id="b98c0-114">从 PSTN 接收入站呼叫的被呼叫者</span><span class="sxs-lookup"><span data-stu-id="b98c0-114">Callee receiving an inbound call from the PSTN</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b98c0-115">位于与 PSTN 网关相同的网络站点中的被呼叫者终结点</span><span class="sxs-lookup"><span data-stu-id="b98c0-115">Callee’s endpoint located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="b98c0-116">不位于与 PSTN 网关相同的网络站点中的被呼叫者终结点</span><span class="sxs-lookup"><span data-stu-id="b98c0-116">Callee’s endpoint not located in the same network site as PSTN gateway</span></span></th>
<th><span data-ttu-id="b98c0-117">位于未知网络站点中或者没有启用基于位置的路由的被呼叫者终结点</span><span class="sxs-lookup"><span data-stu-id="b98c0-117">Callee’s endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b98c0-118">入站 PSTN 呼叫的路由</span><span class="sxs-lookup"><span data-stu-id="b98c0-118">Routing of inbound PSTN call</span></span></p></td>
<td><p><span data-ttu-id="b98c0-119">传入呼叫会路由到被呼叫者的终结点</span><span class="sxs-lookup"><span data-stu-id="b98c0-119">Incoming call is routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="b98c0-120">传入呼叫不会路由到被呼叫者的终结点</span><span class="sxs-lookup"><span data-stu-id="b98c0-120">Incoming call is not routed to callee’s endpoints</span></span></p></td>
<td><p><span data-ttu-id="b98c0-121">传入呼叫不会路由到被呼叫者的终结点</span><span class="sxs-lookup"><span data-stu-id="b98c0-121">Incoming call is not routed to callee’s endpoints</span></span></p></td>
</tr>
</tbody>
</table>

  

<div>

## <a name="see-also"></a><span data-ttu-id="b98c0-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b98c0-122">See Also</span></span>


[<span data-ttu-id="b98c0-123">Lync Server 2013 中基于位置的路由的方案</span><span class="sxs-lookup"><span data-stu-id="b98c0-123">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="b98c0-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b98c0-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

