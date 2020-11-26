---
title: Lync Server 2013：ConferenceSessionDetails 表
description: Lync Server 2013： ConferenceSessionDetails 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails table
ms:assetid: 9eae6a54-69fd-4966-aa17-7ecee1297ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412741(v=OCS.15)
ms:contentKeyID: 48184925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d101eb1607e366ab814e60acaeee80820fe87c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434415"
---
# <a name="conferencesessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="ebf62-103">Lync Server 2013 中的 ConferenceSessionDetails 表</span><span class="sxs-lookup"><span data-stu-id="ebf62-103">ConferenceSessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ebf62-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ebf62-104">

<span> </span></span></span>

<span data-ttu-id="ebf62-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="ebf62-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="ebf62-106">每个记录表示一个会议会话，该会话可以是与焦点的会话，也可以是与特定的会议服务器的会话。</span><span class="sxs-lookup"><span data-stu-id="ebf62-106">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebf62-107">列</span><span class="sxs-lookup"><span data-stu-id="ebf62-107">Column</span></span></th>
<th><span data-ttu-id="ebf62-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="ebf62-108">Data Type</span></span></th>
<th><span data-ttu-id="ebf62-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="ebf62-109">Key/Index</span></span></th>
<th><span data-ttu-id="ebf62-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="ebf62-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-112">从中</span><span class="sxs-lookup"><span data-stu-id="ebf62-112">Datetime</span></span></p></td>
<td><p><span data-ttu-id="ebf62-113">主、外部</span><span class="sxs-lookup"><span data-stu-id="ebf62-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-114">会话请求的时间;与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会议会话。</span><span class="sxs-lookup"><span data-stu-id="ebf62-114">Time of session request; used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="ebf62-115">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-117">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-117">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-118">主、外部</span><span class="sxs-lookup"><span data-stu-id="ebf62-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-119">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="ebf62-119">ID number to identify the session.</span></span> <span data-ttu-id="ebf62-120">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会议会话。</span><span class="sxs-lookup"><span data-stu-id="ebf62-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="ebf62-121">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-122"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-122"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-123">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-123">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-124">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-125">与此会话相关的焦点会议 URI。</span><span class="sxs-lookup"><span data-stu-id="ebf62-125">Focus conference URI related to this session.</span></span> <span data-ttu-id="ebf62-126">有关详细信息，请参阅 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 中的 ConferenceUris 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-126">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="ebf62-127">此 URI 是基于焦点的会议 URI。</span><span class="sxs-lookup"><span data-stu-id="ebf62-127">This URI is a Focus-based conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-129">标识符</span><span class="sxs-lookup"><span data-stu-id="ebf62-129">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-130">区分定期会议的实例的标识符。</span><span class="sxs-lookup"><span data-stu-id="ebf62-130">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="ebf62-131">每个定期会议实例具有相同的 ConferenceURI，但具有不同的 ConfInstance 值。</span><span class="sxs-lookup"><span data-stu-id="ebf62-131">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p>
<p><span data-ttu-id="ebf62-132">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="ebf62-132">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-133"><strong>McuConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-133"><strong>McuConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-134">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-134">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-135">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-135">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-136">与此会话相关的会议服务器会议 URI。</span><span class="sxs-lookup"><span data-stu-id="ebf62-136">Conferencing server conference URI related to this session.</span></span> <span data-ttu-id="ebf62-137">有关详细信息，请参阅 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 中的 ConferenceUris 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-137">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="ebf62-138">此 URI 是基于会议服务器的会议 URI。</span><span class="sxs-lookup"><span data-stu-id="ebf62-138">This URI is the conferencing server-based conference URI.</span></span> <span data-ttu-id="ebf62-139">对于聚焦会议会话，此列将为 null。</span><span class="sxs-lookup"><span data-stu-id="ebf62-139">For Focus conference sessions, this column will be null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-140"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-140"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-141">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-141">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-142">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-143">会议会话中一个用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-143">ID of one user in the conference session.</span></span> <span data-ttu-id="ebf62-144">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="ebf62-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-145"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-145"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-146">标识符</span><span class="sxs-lookup"><span data-stu-id="ebf62-146">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-147">标识终结点实例的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-147">A GUID to identify the instance of endpoint.</span></span> <span data-ttu-id="ebf62-148">例如，如果一个用户使用同一帐户登录到不同的计算机，则每台计算机都将具有不同的终结点 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-148">For example, if one user logs on to different machines with the same account, then each machine will have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-149"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-149"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-150">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-150">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-151">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-151">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-152">指明呼叫者代表的用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-152">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="ebf62-153">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="ebf62-153">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-154"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-154"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-155">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-155">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-156">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-157">按呼叫者引用的用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-157">ID of the user by who the call is referred.</span></span> <span data-ttu-id="ebf62-158">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="ebf62-158">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-159"><strong>UserClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-159"><strong>UserClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-160">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-160">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-161">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-162">会议用户使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="ebf62-162">Client version used by the conference user.</span></span> <span data-ttu-id="ebf62-163">有关详细信息，请参阅 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-164"><strong>ConfClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-164"><strong>ConfClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-165">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-165">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-166">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-166">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-167">会议服务器使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="ebf62-167">Client version used by the conference server.</span></span> <span data-ttu-id="ebf62-168">有关详细信息，请参阅 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-168">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-169"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-169"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-170">datetime</span><span class="sxs-lookup"><span data-stu-id="ebf62-170">datetime</span></span></p></td>
<td><p><span data-ttu-id="ebf62-171">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-171">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-172">标识由当前会话替换的对话框的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="ebf62-172">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="ebf62-173">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-173">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-174"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-174"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-175">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-175">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-176">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-176">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-177">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="ebf62-177">ID number to identify the session.</span></span> <span data-ttu-id="ebf62-178">与 <strong>ReplacesDialogIdTime</strong> 结合使用以唯一标识此会话替换的会话。</span><span class="sxs-lookup"><span data-stu-id="ebf62-178">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="ebf62-179">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-179">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-180"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-180"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-181">bit</span><span class="sxs-lookup"><span data-stu-id="ebf62-181">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-182">指示会议服务器是否已启动会话。</span><span class="sxs-lookup"><span data-stu-id="ebf62-182">Indicates if the session started by the conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-183"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-183"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-184">bit</span><span class="sxs-lookup"><span data-stu-id="ebf62-184">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-185">指示会议服务器是否已结束会话。</span><span class="sxs-lookup"><span data-stu-id="ebf62-185">Indicates if the session ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-186"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-186"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-187">bit</span><span class="sxs-lookup"><span data-stu-id="ebf62-187">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-188">用户是否从内部登录。</span><span class="sxs-lookup"><span data-stu-id="ebf62-188">Whether user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-189"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-189"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-190">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-190">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-191">会话初始协议 (SIP) 响应代码回复到会话邀请。</span><span class="sxs-lookup"><span data-stu-id="ebf62-191">Session Initiation Protocol (SIP) response code to the session invitation.</span></span> <span data-ttu-id="ebf62-192">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="ebf62-192">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="ebf62-193">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-193">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-194"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-194"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-195">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-195">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-196">从 SIP 标题捕获的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-196">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-197"><strong>ServerId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-197"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-198">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-198">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-199">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-200">用于此会话的前端服务器的 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-200">ID of the front-end server used for this session.</span></span> <span data-ttu-id="ebf62-201">有关详细信息，请参阅 <a href="lync-server-2013-servers-table.md">Lync Server 2013 中</a> 的 "服务器" 表。</span><span class="sxs-lookup"><span data-stu-id="ebf62-201">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-202"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-202"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-203">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-203">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-204">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-204">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-205">捕获会话的池的 ID。</span><span class="sxs-lookup"><span data-stu-id="ebf62-205">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="ebf62-206">有关详细信息，请参阅 <a href="lync-server-2013-pools-table.md">Lync Server 2013 中的 pool 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-206">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-207"><strong>MediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-207"><strong>MediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-208">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-208">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-209">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-209">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-210">通话所使用的中介服务器。</span><span class="sxs-lookup"><span data-stu-id="ebf62-210">The Mediation Server the call is using.</span></span> <span data-ttu-id="ebf62-211">有关详细信息，请参阅 <a href="lync-server-2013-mediationservers-table.md">Lync Server 2013 中的 MediationServers 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-211">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-212"><strong>GatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-212"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-213">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-213">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-214">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-214">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-215">呼叫使用的网关。</span><span class="sxs-lookup"><span data-stu-id="ebf62-215">The gateway the call is using.</span></span> <span data-ttu-id="ebf62-216">有关详细信息，请参阅 <a href="lync-server-2013-gateways-table.md">Lync Server 2013 中的网关表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-216">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-217"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-217"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-218">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-218">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-219">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-220">通话所使用的边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="ebf62-220">The Edge Server the call is using.</span></span> <span data-ttu-id="ebf62-221">有关详细信息，请参阅 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013 中的 EdgeServers 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-221">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-222"><strong>ContentTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-222"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-223">int</span><span class="sxs-lookup"><span data-stu-id="ebf62-223">int</span></span></p></td>
<td><p><span data-ttu-id="ebf62-224">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-224">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-225">会话中使用的内容类型。</span><span class="sxs-lookup"><span data-stu-id="ebf62-225">Content type used in the session.</span></span> <span data-ttu-id="ebf62-226">有关详细信息，请参阅 <a href="lync-server-2013-contenttypes-table.md">Lync Server 2013 中的 ContentTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-226">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-227"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-227"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-228">datetime</span><span class="sxs-lookup"><span data-stu-id="ebf62-228">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-229">第一次邀请请求的时间。</span><span class="sxs-lookup"><span data-stu-id="ebf62-229">The time of the first INVITE request.</span></span> <span data-ttu-id="ebf62-230">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="ebf62-230">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="ebf62-231">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-231">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-232"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-233">datetime</span><span class="sxs-lookup"><span data-stu-id="ebf62-233">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-234">第一次 SIP 响应的时间。</span><span class="sxs-lookup"><span data-stu-id="ebf62-234">Time of the first SIP RESPONSE.</span></span> <span data-ttu-id="ebf62-235">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="ebf62-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="ebf62-236">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="ebf62-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-237"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-237"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-238">datetime</span><span class="sxs-lookup"><span data-stu-id="ebf62-238">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-239">会话结束的时间。</span><span class="sxs-lookup"><span data-stu-id="ebf62-239">The time when the session is ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-240"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-240"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-241">tinyint</span><span class="sxs-lookup"><span data-stu-id="ebf62-241">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ebf62-242">外表</span><span class="sxs-lookup"><span data-stu-id="ebf62-242">Foreign</span></span></p></td>
<td><p><span data-ttu-id="ebf62-243"><a href="lync-server-2013-uritypes-table.md">在 Lync Server 2013 中的 UriTypes 表中</a>包含 MCU URI 类型值。</span><span class="sxs-lookup"><span data-stu-id="ebf62-243">Contains the MCU URI type value from the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a>.</span></span> <span data-ttu-id="ebf62-244">此字段用于提高查询性能。</span><span class="sxs-lookup"><span data-stu-id="ebf62-244">This field is used for improving query performance.</span></span></p>
<p><span data-ttu-id="ebf62-245">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="ebf62-245">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebf62-246"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-246"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-247">smallint</span><span class="sxs-lookup"><span data-stu-id="ebf62-247">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-248">指示用户属性的位集。</span><span class="sxs-lookup"><span data-stu-id="ebf62-248">A bit set that indicates the user attributes.</span></span> <span data-ttu-id="ebf62-249">列出了以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="ebf62-249">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="ebf62-250">与桌面电话集成-1</span><span class="sxs-lookup"><span data-stu-id="ebf62-250">Integrated with desktop phone - 1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebf62-251"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="ebf62-251"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="ebf62-252">smallint</span><span class="sxs-lookup"><span data-stu-id="ebf62-252">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ebf62-253">指示通话属性的位集。</span><span class="sxs-lookup"><span data-stu-id="ebf62-253">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="ebf62-254">列出了以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="ebf62-254">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="ebf62-255">重试会话-1</span><span class="sxs-lookup"><span data-stu-id="ebf62-255">Retried Session - 1</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ebf62-256">\* 对于大多数会话，SessionIdSeq 将具有值1。</span><span class="sxs-lookup"><span data-stu-id="ebf62-256">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="ebf62-257">如果多个会话的开始时间完全相同，则一个会话的 SessionIdSeq 将为1，而另一个会话将为2，依此类推。</span><span class="sxs-lookup"><span data-stu-id="ebf62-257">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="ebf62-258"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ebf62-258"></div>

<span> </span>

</div>

</div>

</span></span></div>

