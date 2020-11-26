---
title: Lync Server 2013： Location-Based 路由和咨询式呼叫转移
description: Lync Server 2013： Location-Based 路由和咨询式呼叫传输。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426552"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a><span data-ttu-id="42e51-103">Lync Server 2013 中的 Location-Based 路由和咨询式呼叫转移</span><span class="sxs-lookup"><span data-stu-id="42e51-103">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42e51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42e51-104">

<span> </span></span></span>

<span data-ttu-id="42e51-105">_**主题上次修改时间：** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="42e51-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="42e51-106">除了强制 Location-Based 路由到 Lync 会议之外，Location-Based 路由会议应用程序在向 PSTN 终结点传出的咨询式呼叫传输上强制 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="42e51-106">In addition to enforcing Location-Based Routing to Lync meetings, the Location-Based Routing Conferencing application enforces Location-Based Routing restrictions on consultative call transfers that egress to PSTN endpoints.</span></span> <span data-ttu-id="42e51-107">咨询式呼叫转移是在双方将呼叫转移到新用户之间建立的呼叫。</span><span class="sxs-lookup"><span data-stu-id="42e51-107">A consultative call transfer is a call established between two parties where one of the parties transfers the call to a new user.</span></span> <span data-ttu-id="42e51-108">例如，PSTN 终结点调用 (Lync 被呼叫方) 的用户。</span><span class="sxs-lookup"><span data-stu-id="42e51-108">For example, a PSTN endpoint calls user A (Lync callee).</span></span> <span data-ttu-id="42e51-109">用户 A 确定应将 PSTN 用户转发给用户 B (Lync 用户) 。</span><span class="sxs-lookup"><span data-stu-id="42e51-109">User A determines the PSTN user should be forwarded to user B (Lync user).</span></span> <span data-ttu-id="42e51-110">用户 A 将呼叫与 PSTN 用户保持通话状态，然后呼叫用户 B。用户 B 同意与 PSTN 用户交谈。</span><span class="sxs-lookup"><span data-stu-id="42e51-110">User A places the call with the PSTN user on hold, and calls user B. User B agrees to talk to the PSTN user.</span></span> <span data-ttu-id="42e51-111">用户 A 将呼叫转接至用户 B。</span><span class="sxs-lookup"><span data-stu-id="42e51-111">User A transfers the call on-hold to user B.</span></span>

<span data-ttu-id="42e51-112">**咨询呼叫转接呼叫流**</span><span class="sxs-lookup"><span data-stu-id="42e51-112">**Consultative call transfer call flow**</span></span>

<span data-ttu-id="42e51-113">![会议的基于位置的路由图示](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "会议的基于位置的路由图示")</span><span class="sxs-lookup"><span data-stu-id="42e51-113">![Location-based routing for conferencing diagram](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Location-based routing for conferencing diagram")</span></span>

<span data-ttu-id="42e51-114">当启用 Location-Based 路由的用户启动 PSTN 终结点的咨询式呼叫转移时 (如前面的图所示) 所示，这将创建两个活动呼叫、PSTN 用户 A 和 Lync 用户 A 之间的一个通话以及 Lync 用户 A 和 Lync 用户 B 之间的另一个通话。以下行为由 Location-Based 路由会议应用程序强制执行：</span><span class="sxs-lookup"><span data-stu-id="42e51-114">When a user enabled for Location-Based Routing initiates a consultative call transfer of a PSTN endpoint (as shown in the preceding figure), this creates two active calls, one call between the PSTN user and Lync user A, and the other between Lync user A and Lync user B. the following behavior is enforced by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="42e51-115">如果您有权将 pstn 呼叫路由到 PSTN 呼叫以将 PSTN 呼叫重新路由到网络站点（Lync 用户 B (即 "转移目标) "，则将允许呼叫转移;否则，将阻止咨询呼叫转接。</span><span class="sxs-lookup"><span data-stu-id="42e51-115">If the SIP trunk routing the PSTN call is authorized to re-route the PSTN call to the network site where Lync user B (i.e. transfer target) is located,, then the call transfer will be allowed; otherwise, the consultative call transfer will be blocked.</span></span> <span data-ttu-id="42e51-116">此授权的依据是转接方的位置与负责将活动呼叫路由到 PSTN 终结点的 SIP 中继位于相同网络站点。</span><span class="sxs-lookup"><span data-stu-id="42e51-116">This authorization is performed based on the transferred party’s location being in the same network site as the SIP trunk that is routing the active call to the PSTN endpoint.</span></span>

  - <span data-ttu-id="42e51-117">如果 SIP 中继路由入站 PSTN 呼叫没有授权将呼叫路由到 (Lync 用户 B) 的已传送方或已转移的当事方位于未知的网络站点，则向 PSTN 终结点进行咨询性呼叫转移 (例如将阻止呼叫转移目标) 。</span><span class="sxs-lookup"><span data-stu-id="42e51-117">If the SIP trunk routing the inbound PSTN call is not authorized to route calls to the network site where the transferred party (Lync user B) is located or the transferred party is located in an unknown network site, then the consultative call transfer to the PSTN endpoint (i.e. call transfer target) will be blocked.</span></span>

<span data-ttu-id="42e51-118">下表介绍了 Location-Based 路由会议应用程序如何为咨询式呼叫传送应用 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="42e51-118">The following table describes how Location-Based Routing restrictions are applied by the Location-Based Routing Conferencing application for consultative call transfers.</span></span> <span data-ttu-id="42e51-119">尽管 PBX 终结点并非直接与某个网络站点关联，但可以为 PBX 连接到的 SIP 中继分配一个网络站点。</span><span class="sxs-lookup"><span data-stu-id="42e51-119">Although PBX endpoints are not directly associated with a network site, the SIP trunk the PBX is connected to can be assigned a network site.</span></span> <span data-ttu-id="42e51-120">因此，PBX 终结点可以间接与网络站点关联。</span><span class="sxs-lookup"><span data-stu-id="42e51-120">Therefore, the PBX endpoint can be indirectly associated with a network site.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42e51-121">呼叫被转接方的网络站点</span><span class="sxs-lookup"><span data-stu-id="42e51-121">Network site of call transferred party</span></span></p></td>
<td><p><span data-ttu-id="42e51-122">呼叫转接目标的网络站点</span><span class="sxs-lookup"><span data-stu-id="42e51-122">Network site of call transfer target</span></span></p></td>
<td><p><span data-ttu-id="42e51-123">行为</span><span class="sxs-lookup"><span data-stu-id="42e51-123">Behavior</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42e51-124">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-124">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-125">同一网络网站中的 Lync 用户 (亦即站点 1) </span><span class="sxs-lookup"><span data-stu-id="42e51-125">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="42e51-126">咨询转接将被允许</span><span class="sxs-lookup"><span data-stu-id="42e51-126">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42e51-127">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-127">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-128">不同网络站点中的 Lync 用户 (亦即站点 2) </span><span class="sxs-lookup"><span data-stu-id="42e51-128">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="42e51-129">咨询转接将被禁止</span><span class="sxs-lookup"><span data-stu-id="42e51-129">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42e51-130">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-130">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-131">未知网络网站中的 Lync 用户</span><span class="sxs-lookup"><span data-stu-id="42e51-131">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="42e51-132">咨询转接将被禁止</span><span class="sxs-lookup"><span data-stu-id="42e51-132">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42e51-133">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-133">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-134">联合 Lync 用户</span><span class="sxs-lookup"><span data-stu-id="42e51-134">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="42e51-135">咨询转接将被禁止</span><span class="sxs-lookup"><span data-stu-id="42e51-135">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42e51-136">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-136">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-137">PBX 终结点位于相同站点（即站点 1）</span><span class="sxs-lookup"><span data-stu-id="42e51-137">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="42e51-138">咨询转接将被允许</span><span class="sxs-lookup"><span data-stu-id="42e51-138">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42e51-139">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-139">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-140">PBX 终结点位于不同站点（即站点 2）</span><span class="sxs-lookup"><span data-stu-id="42e51-140">PBX endpoint in a different sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="42e51-141">咨询转接将被禁止</span><span class="sxs-lookup"><span data-stu-id="42e51-141">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42e51-142">PBX 终结点位于相同站点（即站点 1）</span><span class="sxs-lookup"><span data-stu-id="42e51-142">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="42e51-143">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-143">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-144">咨询转接将被允许</span><span class="sxs-lookup"><span data-stu-id="42e51-144">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42e51-145">PBX 终结点位于不同站点（即站点 2）</span><span class="sxs-lookup"><span data-stu-id="42e51-145">PBX endpoint in a different site (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="42e51-146">PSTN 终结点</span><span class="sxs-lookup"><span data-stu-id="42e51-146">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="42e51-147">咨询转接将被禁止</span><span class="sxs-lookup"><span data-stu-id="42e51-147">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42e51-148">PBX 终结点位于任意站点</span><span class="sxs-lookup"><span data-stu-id="42e51-148">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="42e51-149">同一网络网站中的 Lync 用户 (亦即站点 1) </span><span class="sxs-lookup"><span data-stu-id="42e51-149">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="42e51-150">咨询转接将被允许</span><span class="sxs-lookup"><span data-stu-id="42e51-150">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42e51-151">PBX 终结点位于任意站点</span><span class="sxs-lookup"><span data-stu-id="42e51-151">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="42e51-152">不同网络站点中的 Lync 用户 (亦即站点 2) </span><span class="sxs-lookup"><span data-stu-id="42e51-152">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="42e51-153">咨询转接将被允许</span><span class="sxs-lookup"><span data-stu-id="42e51-153">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42e51-154">PBX 终结点位于任意站点</span><span class="sxs-lookup"><span data-stu-id="42e51-154">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="42e51-155">未知网络网站中的 Lync 用户</span><span class="sxs-lookup"><span data-stu-id="42e51-155">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="42e51-156">咨询转接将被允许</span><span class="sxs-lookup"><span data-stu-id="42e51-156">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42e51-157">PBX 终结点位于任意站点</span><span class="sxs-lookup"><span data-stu-id="42e51-157">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="42e51-158">联合 Lync 用户</span><span class="sxs-lookup"><span data-stu-id="42e51-158">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="42e51-159">咨询转接将被允许</span><span class="sxs-lookup"><span data-stu-id="42e51-159">Consultative transfer will be allowed</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="42e51-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42e51-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

