---
title: Lync Server 2013：会议 Location-Based 路由概述
description: Lync Server 2013：会议 Location-Based 路由概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing for conferencing
ms:assetid: 8b86740e-db95-4304-bb83-64d0cbb91d47
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362815(v=OCS.15)
ms:contentKeyID: 56335084
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a8fe9cdf4a797243c3ec04b3466011f374fb0d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392329"
---
# <a name="overview-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="0fbc1-103">Lync Server 2013 中的会议 Location-Based 路由概述</span><span class="sxs-lookup"><span data-stu-id="0fbc1-103">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0fbc1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0fbc1-104">

<span> </span></span></span>

<span data-ttu-id="0fbc1-105">_**主题上次修改时间：** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="0fbc1-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="0fbc1-106">Location-Based 路由会议应用程序向 Lync 会议提供阻止 PSTN 免绕过的机制。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-106">The Location-Based Routing Conferencing application provides to Lync Conferences a mechanism for the prevention of PSTN toll bypass.</span></span> <span data-ttu-id="0fbc1-107">应用程序监控活动会议，并根据参与的 Lync 用户的位置强制执行 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-107">The application monitors active conferences and enforces Location-Based Routing restrictions based on the location of the Lync users participating.</span></span>

<span data-ttu-id="0fbc1-108">Location-Based 路由会议应用程序确定如果满足以下条件，是否会在 Lync 会议上执行 Location-Based 路由：</span><span class="sxs-lookup"><span data-stu-id="0fbc1-108">The Location-Based Routing Conferencing application determines whether Location-Based Routing is to be enforced on a Lync meeting if the following criteria are met:</span></span>

  - <span data-ttu-id="0fbc1-109">会议组织者已启用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-109">The meeting organizer is enabled for Location-Based Routing.</span></span> <span data-ttu-id="0fbc1-110">Location-Based 路由限制将仅应用于已启用 Location-Based 路由的用户组织的会议。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-110">Location-Based Routing restrictions will be applied only to conferences that are organized by users who are enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="0fbc1-111">PSTN 终结点中至少有一名会议参与者。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-111">At least one meeting participant is a PSTN endpoint.</span></span> <span data-ttu-id="0fbc1-112">Location-Based 路由限制仅适用于包含 PSTN 终结点的会议。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-112">Location-Based Routing restrictions are applicable only for conferences that include PSTN endpoints.</span></span>

  - <span data-ttu-id="0fbc1-113">用于将会议桥接到 PSTN 的 PSTN 网关所在的网络站点以及组织者和参与者用于从中连接的网络站点。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-113">The network site where the PSTN gateway used to bridge the conference to the PSTN is located as well as the network sites where the organizers and participants are connecting from.</span></span>

<span data-ttu-id="0fbc1-114">Location-Based 路由会议应用程序阻止 Lync 用户和 PSTN 终结点从不同网络站点加入同一会议。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-114">The Location-Based Routing Conferencing application prevents the participation of Lync users and PSTN endpoints from different network sites to the same conference.</span></span> <span data-ttu-id="0fbc1-115">如果为 Location-Based 的路由启用了会议组织者，则会议应用程序会强制执行以下限制：</span><span class="sxs-lookup"><span data-stu-id="0fbc1-115">If the organizer of a meeting is enabled for Location-Based Routing, the Conferencing application enforces the following restrictions:</span></span>

  - <span data-ttu-id="0fbc1-116">可以加入 Lync 会议的终结点取决于已加入会议的终结点，并且此限制会调整为联接终结点，并将新终结点加入会议。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-116">The endpoints that can join a Lync meeting depend on the endpoints that already joined the conference, and this restriction adjusts as joined endpoints leave and new endpoints join the conference.</span></span> <span data-ttu-id="0fbc1-117">如果组织者和参与者从同一网络网站加入 Lync 会议，则 PSTN 终结点、同一网络网站中的另一个参与者、来自不同网络网站的另一个参与者或来自未知网络网站的参与者允许加入。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-117">If organizers and participants are joining a Lync meeting from the same network site, then a PSTN endpoint, another participant from the same network site, another participant from a different network site or a participant from an unknown network site are allowed to join.</span></span>

  - <span data-ttu-id="0fbc1-118">如果组织者和参与者从不同或未知的网络站点加入会议，则如果 PSTN 呼叫从启用了基于位置的路由的 SIP 中继传入，将不允许 PSTN 终结点加入会议。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-118">If organizers and participants are joining the meeting from different or unknown network sites, a PSTN endpoint is not allowed to join the meeting if the PSTN call ingresses from a SIP trunk enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="0fbc1-119">如果组织者和参与者都从同一网络网站加入会议，并且有参与者加入来自 PSTN 的同一会议，则不允许来自其他网络网站的 Lync 终结点加入会议。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-119">If organizers and participants are all joining the meeting from the same network site and there are participants joining the same meeting from the PSTN, a Lync endpoint from a different network site is not allowed to join the meeting.</span></span>

<span data-ttu-id="0fbc1-120">下表汇总了这些会议 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-120">These conferencing Location-Based Routing restrictions are summarized in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fbc1-121">任意时间点处于会议中的用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-121">User(s) in a conference at any given point</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-122">允许加入会议的用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-122">User(s) allowed to join the conference</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-123">不允许加入会议的用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-123">User(s) not allowed to join the conference</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fbc1-124">Lync VoIP 客户端用户 (s) 来自单个网络网站</span><span class="sxs-lookup"><span data-stu-id="0fbc1-124">Lync VoIP client user(s) from a single network site</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-125">来自同一网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-125">Lync VoIP client user from the same network site</span></span></p>
<p><span data-ttu-id="0fbc1-126">来自不同网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-126">Lync VoIP client user from a different network site</span></span></p>
<p><span data-ttu-id="0fbc1-127">来自未知网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-127">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="0fbc1-128">联合 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-128">Federated Lync VoIP client user</span></span></p>
<p><span data-ttu-id="0fbc1-129">从 PSTN 终结点加入的用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-129">User joining from a PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-130">无</span><span class="sxs-lookup"><span data-stu-id="0fbc1-130">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fbc1-131">Lync VoIP 客户端用户 (s) 来自未知网络网站</span><span class="sxs-lookup"><span data-stu-id="0fbc1-131">Lync VoIP client user(s) from an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-132">任何网站中的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-132">Lync VoIP client user from any site</span></span></p>
<p><span data-ttu-id="0fbc1-133">来自未知网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-133">Lync VoIP client user from an unknown site</span></span></p>
<p><span data-ttu-id="0fbc1-134">联合 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-134">Federated Lync VoIP client user</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-135">通过 PSTN 终结点加入的用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-135">User joining via a PSTN endpoint</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fbc1-136">来自不同网络站点的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-136">Lync VoIP client users from different network sites</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-137">来自任何网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-137">Lync VoIP client user from any network site</span></span></p>
<p><span data-ttu-id="0fbc1-138">来自未知网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-138">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="0fbc1-139">联合 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-139">Federated Lync VoIP client user</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-140">通过 PSTN 终结点加入的用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-140">User joining via a PSTN endpoint</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fbc1-141">Lync VoIP 客户端用户 (s) 从单个网络站点和从 PSTN 终结点加入的用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-141">Lync VoIP client user(s) from a single network site and users joining from a PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-142">来自同一网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-142">Lync VoIP client user from the same network site</span></span></p></td>
<td><p><span data-ttu-id="0fbc1-143">来自不同网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-143">Lync VoIP client user from a different network site</span></span></p>
<p><span data-ttu-id="0fbc1-144">来自未知网络网站的 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-144">Lync VoIP client user from an unknown network site</span></span></p>
<p><span data-ttu-id="0fbc1-145">联合 Lync VoIP 客户端用户</span><span class="sxs-lookup"><span data-stu-id="0fbc1-145">Federated Lync VoIP client user</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0fbc1-146">以下是 Location-Based 路由会议应用程序的其他特征：</span><span class="sxs-lookup"><span data-stu-id="0fbc1-146">The following are additional characteristics of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="0fbc1-147">当不允许用户在给定 Location-Based 路由限制的情况下加入会议时，对会议的用户呼叫将被拒绝，并且他的 Lync 客户端将报告呼叫未完成或已结束。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-147">When a user is not allowed to join a conference given Location-Based Routing restrictions, the users call to the conference will be rejected and his Lync Client will report that the call was not completed or has ended.</span></span>

  - <span data-ttu-id="0fbc1-148">使用 Location-Based 路由 enforcements 加入会议的 PSTN 终结点不会被限制为加入会议（如果终结点通过未启用 Location-Based 路由的干线连接）。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-148">A PSTN endpoint joining a conference with Location-Based Routing enforcements will not be restricted to join the conference regardless of its state if the endpoint joins via a trunk that is not enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="0fbc1-149">通过 SIP 主干连接到 Mediations 服务器的 PBX 系统不会对 PSTN 进行传出调用，其 enforcements 与在定义 SIP 主干的同一网络站点中的 Lync 用户具有相同的。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-149">A PBX system connected to a Mediations Server over a SIP trunk that does not egress calls to the PSTN will have the same enforcements as Lync users located in the same network site where the SIP trunk is defined.</span></span> <span data-ttu-id="0fbc1-150">例如，PSTN 终结点将能够使用 PBX 用户和 Lync 用户加入会议（如果它们位于同一网络网站中）;否则，如果 PBX 用户与 Lync 用户位于不同的网络站点，则不允许 PSTN 终结点加入会议。</span><span class="sxs-lookup"><span data-stu-id="0fbc1-150">For example, a PSTN endpoint will be able to join a conference with a PBX user and a Lync user if they are located in the same network site; otherwise, the PSTN endpoint will not be allowed to join the conference if the PBX user is in a different network site than the Lync user.</span></span>

<span data-ttu-id="0fbc1-151"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0fbc1-151"></div>

<span> </span>

</div>

</div>

</span></span></div>

