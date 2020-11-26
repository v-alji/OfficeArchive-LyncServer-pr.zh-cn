---
title: Lync Server 2013：SessionDetails 表
description: Lync Server 2013： SessionDetails 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails table
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398589(v=OCS.15)
ms:contentKeyID: 48184559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd927f784fb0f2a835c896824105fe8bb112c7a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444775"
---
# <a name="sessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="a082f-103">Lync Server 2013 中的 SessionDetails 表</span><span class="sxs-lookup"><span data-stu-id="a082f-103">SessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a082f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a082f-104">

<span> </span></span></span>

<span data-ttu-id="a082f-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a082f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a082f-106">每条记录表示一个对等会话，可以是 VoIP-VoIP 的电话呼叫、两方 IM 会话或其他类型的会话。</span><span class="sxs-lookup"><span data-stu-id="a082f-106">Each record represents one peer-to-peer session, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="a082f-107">你可以使用 [Lync Server 2013 中的 media 表](lync-server-2013-media-table.md) 执行表联接，以查找此会话中涉及的每个媒体的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a082f-107">You can perform a table join with the [Media table in Lync Server 2013](lync-server-2013-media-table.md) to find the details of each media involved in this session.</span></span>

<span data-ttu-id="a082f-108">请注意，IsUser1IntegratedWithDeskPhone 和 IsUser2IntegratedWithDeskPhone 字段已从 Microsoft Lync Server 2013 中使用的 SessionDetails 表中删除。</span><span class="sxs-lookup"><span data-stu-id="a082f-108">Note that the IsUser1IntegratedWithDeskPhone and the IsUser2IntegratedWithDeskPhone fields have been dropped from the SessionDetails table used in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a082f-109">列</span><span class="sxs-lookup"><span data-stu-id="a082f-109">Column</span></span></th>
<th><span data-ttu-id="a082f-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="a082f-110">Data Type</span></span></th>
<th><span data-ttu-id="a082f-111">键/索引</span><span class="sxs-lookup"><span data-stu-id="a082f-111">Key/Index</span></span></th>
<th><span data-ttu-id="a082f-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="a082f-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a082f-113"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-113"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-114">datetime</span><span class="sxs-lookup"><span data-stu-id="a082f-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="a082f-115">主、外部</span><span class="sxs-lookup"><span data-stu-id="a082f-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-116">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="a082f-116">Time of session request.</span></span> <span data-ttu-id="a082f-117">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="a082f-117">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="a082f-118">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-118">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-119"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-119"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-120">int</span><span class="sxs-lookup"><span data-stu-id="a082f-120">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-121">主、外部</span><span class="sxs-lookup"><span data-stu-id="a082f-121">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-122">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="a082f-122">ID number to identify the session.</span></span> <span data-ttu-id="a082f-123">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。 \* 有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-123">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.\* See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-124"><strong>True&correlationid</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-124"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-125">标识符</span><span class="sxs-lookup"><span data-stu-id="a082f-125">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-126">用于关联多个会话的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a082f-126">A GUID to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-127"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-127"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-128">datetime</span><span class="sxs-lookup"><span data-stu-id="a082f-128">datetime</span></span></p></td>
<td><p><span data-ttu-id="a082f-129">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-130">标识由当前会话替换的对话框的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="a082f-130">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="a082f-131">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-131">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-132"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-132"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-133">int</span><span class="sxs-lookup"><span data-stu-id="a082f-133">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-134">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-135">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="a082f-135">ID number to identify the session.</span></span> <span data-ttu-id="a082f-136">与 <strong>ReplacesDialogIdTime</strong> 结合使用以唯一标识此会话替换的会话。</span><span class="sxs-lookup"><span data-stu-id="a082f-136">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="a082f-137">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-137">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-138"><strong>User1Id</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-138"><strong>User1Id</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-139">int</span><span class="sxs-lookup"><span data-stu-id="a082f-139">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-140">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-140">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-141">会话中一个用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-141">ID of one user in the session.</span></span> <span data-ttu-id="a082f-142">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="a082f-142">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-143"><strong>User2Id</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-143"><strong>User2Id</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-144">int</span><span class="sxs-lookup"><span data-stu-id="a082f-144">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-145">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-146">会话中其他用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-146">ID of the other user in the session.</span></span> <span data-ttu-id="a082f-147">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="a082f-147">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-148"><strong>User1EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-148"><strong>User1EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-149">标识符</span><span class="sxs-lookup"><span data-stu-id="a082f-149">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-150">标识会话中第一个用户使用的终结点的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a082f-150">GUID that identifies the endpoint used by the first user in the session.</span></span></p>
<p><span data-ttu-id="a082f-151">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="a082f-151">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-152"><strong>User2EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-152"><strong>User2EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-153">标识符</span><span class="sxs-lookup"><span data-stu-id="a082f-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-154">标识会话中第二用户使用的终结点的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a082f-154">GUID that identifies the endpoint used by the second user in the session.</span></span></p>
<p><span data-ttu-id="a082f-155">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="a082f-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-156"><strong>TargetUserId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-156"><strong>TargetUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-157">int</span><span class="sxs-lookup"><span data-stu-id="a082f-157">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-158">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-158">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-159">SIP 请求中的原始用户 URI。</span><span class="sxs-lookup"><span data-stu-id="a082f-159">The original To user URI in the SIP request.</span></span> <span data-ttu-id="a082f-160">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="a082f-160">see the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-161"><strong>SessionStartedById</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-161"><strong>SessionStartedById</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-162">int</span><span class="sxs-lookup"><span data-stu-id="a082f-162">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-163">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-164">启动会话的用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-164">ID of the user who started the session.</span></span> <span data-ttu-id="a082f-165">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="a082f-165">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-166"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-166"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-167">int</span><span class="sxs-lookup"><span data-stu-id="a082f-167">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-168">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-168">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-169">指明呼叫者代表的用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-169">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="a082f-170">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="a082f-170">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-171"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-171"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-172">int</span><span class="sxs-lookup"><span data-stu-id="a082f-172">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-173">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-173">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-174">按呼叫者引用的用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-174">ID of the user by who the call is referred.</span></span> <span data-ttu-id="a082f-175">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="a082f-175">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-176"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-176"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-177">int</span><span class="sxs-lookup"><span data-stu-id="a082f-177">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-178">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-178">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-179">用于此会话的前端服务器的 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-179">ID of the front-end server used for this session.</span></span> <span data-ttu-id="a082f-180">有关详细信息，请参阅 <a href="lync-server-2013-servers-table.md">Lync Server 2013 中</a> 的 "服务器" 表。</span><span class="sxs-lookup"><span data-stu-id="a082f-180">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-181"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-181"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-182">int</span><span class="sxs-lookup"><span data-stu-id="a082f-182">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-183">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-183">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-184">捕获会话的池的 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-184">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="a082f-185">有关详细信息，请参阅 <a href="lync-server-2013-pools-table.md">Lync Server 2013 中的 pool 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-185">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-186"><strong>ContentTypeID</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-186"><strong>ContentTypeID</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-187">int</span><span class="sxs-lookup"><span data-stu-id="a082f-187">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-188">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-189">会话中使用的内容类型。</span><span class="sxs-lookup"><span data-stu-id="a082f-189">Content type used in the session.</span></span> <span data-ttu-id="a082f-190">有关详细信息，请参阅 <a href="lync-server-2013-contenttypes-table.md">Lync Server 2013 中的 ContentTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-190">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-191"><strong>User1ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-191"><strong>User1ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-192">int</span><span class="sxs-lookup"><span data-stu-id="a082f-192">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-193">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-194">User1 使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="a082f-194">Client version used by User1.</span></span> <span data-ttu-id="a082f-195">有关详细信息，请参阅 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-195">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-196"><strong>User2ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-196"><strong>User2ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-197">int</span><span class="sxs-lookup"><span data-stu-id="a082f-197">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-198">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-198">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-199">用户2使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="a082f-199">Client version used by User2.</span></span> <span data-ttu-id="a082f-200">有关详细信息，请参阅 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-200">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-201"><strong>User1EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-201"><strong>User1EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-202">int</span><span class="sxs-lookup"><span data-stu-id="a082f-202">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-203">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-203">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-204">由 User1 使用的边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="a082f-204">Edge Server used by User1.</span></span> <span data-ttu-id="a082f-205">有关详细信息，请参阅 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 中的 EdgeServers 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-205">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-206"><strong>User2EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-206"><strong>User2EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-207">int</span><span class="sxs-lookup"><span data-stu-id="a082f-207">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-208">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-208">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-209">由服务者使用的边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="a082f-209">Edge Server used by User2.</span></span> <span data-ttu-id="a082f-210">有关详细信息，请参阅 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 中的 EdgeServers 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-210">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-211"><strong>IsUser1Internal</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-211"><strong>IsUser1Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-212">bit</span><span class="sxs-lookup"><span data-stu-id="a082f-212">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-213">User1 是否从内部登录。</span><span class="sxs-lookup"><span data-stu-id="a082f-213">Whether User1 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-214"><strong>IsUser2Internal</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-214"><strong>IsUser2Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-215">bit</span><span class="sxs-lookup"><span data-stu-id="a082f-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-216">2/2 是否已从内部登录。</span><span class="sxs-lookup"><span data-stu-id="a082f-216">Whether User2 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-217"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-217"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-218">datetime</span><span class="sxs-lookup"><span data-stu-id="a082f-218">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-219">第一次邀请请求的时间。</span><span class="sxs-lookup"><span data-stu-id="a082f-219">The time of the first INVITE request.</span></span> <span data-ttu-id="a082f-220">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="a082f-220">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="a082f-221">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="a082f-221">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="a082f-222">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="a082f-222">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="a082f-223">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="a082f-223">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-224"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-224"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-225">datetime</span><span class="sxs-lookup"><span data-stu-id="a082f-225">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-226">对第一个邀请消息的答复时间。</span><span class="sxs-lookup"><span data-stu-id="a082f-226">The time of the response to the first INVITE message.</span></span> <span data-ttu-id="a082f-227">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="a082f-227">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="a082f-228">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="a082f-228">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-229"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-229"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-230">int</span><span class="sxs-lookup"><span data-stu-id="a082f-230">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-231">会议邀请的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="a082f-231">SIP response code to the session invitation.</span></span> <span data-ttu-id="a082f-232">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="a082f-232">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="a082f-233">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="a082f-233">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-234"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-234"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-235">int</span><span class="sxs-lookup"><span data-stu-id="a082f-235">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-236">从 SIP 标题捕获的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="a082f-236">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-237"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-237"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-238">int</span><span class="sxs-lookup"><span data-stu-id="a082f-238">int</span></span></p></td>
<td><p><span data-ttu-id="a082f-239">外表</span><span class="sxs-lookup"><span data-stu-id="a082f-239">Foreign</span></span></p></td>
<td><p><span data-ttu-id="a082f-240">通话优先级。</span><span class="sxs-lookup"><span data-stu-id="a082f-240">Call priority.</span></span> <span data-ttu-id="a082f-241">有关详细信息，请参阅 <a href="lync-server-2013-callpriorities-table.md">Lync Server 2013 中的 CallPriorities 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a082f-241">See the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-242"><strong>User1MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-242"><strong>User1MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-243">int</span><span class="sxs-lookup"><span data-stu-id="a082f-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-244">在会话期间由 User1 发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="a082f-244">Number of messages sent by User1 during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-245"><strong>User2MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-245"><strong>User2MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-246">int</span><span class="sxs-lookup"><span data-stu-id="a082f-246">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-247">会话期间由操作者发送的邮件数。</span><span class="sxs-lookup"><span data-stu-id="a082f-247">Number of messages sent by User2 during the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-248"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-248"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-249">datetime</span><span class="sxs-lookup"><span data-stu-id="a082f-249">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-250">会话结束时的时间。</span><span class="sxs-lookup"><span data-stu-id="a082f-250">Time at the end of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-251"><strong>MediaTypes</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-251"><strong>MediaTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-252">int</span><span class="sxs-lookup"><span data-stu-id="a082f-252">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-253">指示此会话的媒体类型的位集。</span><span class="sxs-lookup"><span data-stu-id="a082f-253">A bit set that indicates the media type of this session.</span></span> <span data-ttu-id="a082f-254">列出的是以下类型的定义：</span><span class="sxs-lookup"><span data-stu-id="a082f-254">Listed are the definitions of the types:</span></span></p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a082f-255">即时消息</span><span class="sxs-lookup"><span data-stu-id="a082f-255">IM</span></span></p></td>
<td><p><span data-ttu-id="a082f-256">1</span><span class="sxs-lookup"><span data-stu-id="a082f-256">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-257">FILE_TRANSFER</span><span class="sxs-lookup"><span data-stu-id="a082f-257">FILE_TRANSFER</span></span></p></td>
<td><p><span data-ttu-id="a082f-258">2</span><span class="sxs-lookup"><span data-stu-id="a082f-258">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-259">REMOTE_ASSISTANCE</span><span class="sxs-lookup"><span data-stu-id="a082f-259">REMOTE_ASSISTANCE</span></span></p></td>
<td><p><span data-ttu-id="a082f-260">4</span><span class="sxs-lookup"><span data-stu-id="a082f-260">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-261">APP_SHARING</span><span class="sxs-lookup"><span data-stu-id="a082f-261">APP_SHARING</span></span></p></td>
<td><p><span data-ttu-id="a082f-262">个</span><span class="sxs-lookup"><span data-stu-id="a082f-262">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-263">视听</span><span class="sxs-lookup"><span data-stu-id="a082f-263">AUDIO</span></span></p></td>
<td><p><span data-ttu-id="a082f-264">utf-16</span><span class="sxs-lookup"><span data-stu-id="a082f-264">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-265">VIDEO</span><span class="sxs-lookup"><span data-stu-id="a082f-265">VIDEO</span></span></p></td>
<td><p><span data-ttu-id="a082f-266">32</span><span class="sxs-lookup"><span data-stu-id="a082f-266">32</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-267">APP_INVITE</span><span class="sxs-lookup"><span data-stu-id="a082f-267">APP_INVITE</span></span></p></td>
<td><p><span data-ttu-id="a082f-268">64</span><span class="sxs-lookup"><span data-stu-id="a082f-268">64</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-269"><strong>User1Flag</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-269"><strong>User1Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-270">smallint</span><span class="sxs-lookup"><span data-stu-id="a082f-270">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-271">指示 User1 属性的位集。</span><span class="sxs-lookup"><span data-stu-id="a082f-271">A bit set that indicates the User1 attributes.</span></span> <span data-ttu-id="a082f-272">列出了以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="a082f-272">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="a082f-273">0x01-与桌面电话集成</span><span class="sxs-lookup"><span data-stu-id="a082f-273">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-274"><strong>User2Flag</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-274"><strong>User2Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-275">smallint</span><span class="sxs-lookup"><span data-stu-id="a082f-275">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-276">指示 "工作 2" 属性的位集。</span><span class="sxs-lookup"><span data-stu-id="a082f-276">A bit set that indicates the User2 attributes.</span></span> <span data-ttu-id="a082f-277">列出了以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="a082f-277">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="a082f-278">0x01-与桌面电话集成</span><span class="sxs-lookup"><span data-stu-id="a082f-278">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a082f-279"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-279"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-280">smallint</span><span class="sxs-lookup"><span data-stu-id="a082f-280">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-281">指示通话属性的位集。</span><span class="sxs-lookup"><span data-stu-id="a082f-281">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="a082f-282">列出了以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="a082f-282">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="a082f-283">0x01-重试会话</span><span class="sxs-lookup"><span data-stu-id="a082f-283">0x01 - Retried Session</span></span></p></li>
<li><p><span data-ttu-id="a082f-284">0x02-代表响应组的代理发出的呼叫</span><span class="sxs-lookup"><span data-stu-id="a082f-284">0x02 - A call made by agent on behalf of a response group</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a082f-285"><strong>过</strong></span><span class="sxs-lookup"><span data-stu-id="a082f-285"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="a082f-286">bit</span><span class="sxs-lookup"><span data-stu-id="a082f-286">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="a082f-287">供监视服务内部使用。</span><span class="sxs-lookup"><span data-stu-id="a082f-287">For internal use by the Monitoring service.</span></span></p>
<p><span data-ttu-id="a082f-288">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="a082f-288">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a082f-289">\* 对于大多数会话，SessionIdSeq 将具有值1。</span><span class="sxs-lookup"><span data-stu-id="a082f-289">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="a082f-290">如果多个会话的开始时间完全相同，则一个会话的 SessionIdSeq 将为1，而另一个会话将为2，依此类推。</span><span class="sxs-lookup"><span data-stu-id="a082f-290">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="a082f-291"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a082f-291"></div>

<span> </span>

</div>

</div>

</span></span></div>

