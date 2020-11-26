---
title: Lync Server 2013： SessionDetails 视图
description: Lync Server 2013： SessionDetails 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails view
ms:assetid: ea328c6f-cf22-48dd-8f7f-f1666c9148c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721924(v=OCS.15)
ms:contentKeyID: 49733859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c9f657257e54389defb805919be61adbdecad74
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424028"
---
# <a name="sessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="c3e27-103">Lync Server 2013 中的 SessionDetails 视图</span><span class="sxs-lookup"><span data-stu-id="c3e27-103">SessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3e27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3e27-104">

<span> </span></span></span>

<span data-ttu-id="c3e27-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="c3e27-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="c3e27-106">SessionDetails 视图存储有关对等会话的信息，这些会话可以是 VoIP-VoIP 电话呼叫、两方 IM 会话或其他类型的会话。</span><span class="sxs-lookup"><span data-stu-id="c3e27-106">The SessionDetails view stores information about peer-to-peer sessions, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="c3e27-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="c3e27-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3e27-108">列</span><span class="sxs-lookup"><span data-stu-id="c3e27-108">Column</span></span></th>
<th><span data-ttu-id="c3e27-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="c3e27-109">Data Type</span></span></th>
<th><span data-ttu-id="c3e27-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="c3e27-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-112">datetime</span><span class="sxs-lookup"><span data-stu-id="c3e27-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3e27-113">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="c3e27-113">Time of session request.</span></span> <span data-ttu-id="c3e27-114">与 SessionIdSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="c3e27-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="c3e27-115">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 表中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-117">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-117">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-118">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="c3e27-118">ID number to identify the session.</span></span> <span data-ttu-id="c3e27-119">与 SessionIdTime 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="c3e27-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="c3e27-120">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-121"><strong>InviteTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-121"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-122">datetime</span><span class="sxs-lookup"><span data-stu-id="c3e27-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3e27-123">第一次邀请请求的时间。</span><span class="sxs-lookup"><span data-stu-id="c3e27-123">Time of the first INVITE request.</span></span> <span data-ttu-id="c3e27-124">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="c3e27-124">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="c3e27-125">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-125">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="c3e27-126">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="c3e27-126">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="c3e27-127">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-127">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-128"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-128"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-129">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="c3e27-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-130">启动会话的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="c3e27-130">URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-131"><strong>ToUri</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-131"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-132">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="c3e27-132">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-133">加入会话的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="c3e27-133">URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-134"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-134"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-136">启动会话的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="c3e27-136">Type of URI of the user who started the session.</span></span> <span data-ttu-id="c3e27-137">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-137">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-140">加入会话的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="c3e27-140">Type of URI of the user who joined the session.</span></span> <span data-ttu-id="c3e27-141">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-141">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-142"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-142"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-143">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="c3e27-143">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-144">启动会话的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="c3e27-144">Tenant of the user who started the session.</span></span> <span data-ttu-id="c3e27-145">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-146"><strong>ToTenant</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-146"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-147">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-147">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-148">加入会话的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="c3e27-148">The tenant of the user who joined the session.</span></span> <span data-ttu-id="c3e27-149">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-149">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-150"><strong>FromEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-150"><strong>FromEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-151">标识符</span><span class="sxs-lookup"><span data-stu-id="c3e27-151">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="c3e27-152">启动会话的用户的终结点的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="c3e27-152">Unique identifier of the endpoint of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-153"><strong>ToEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-153"><strong>ToEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-154">标识符</span><span class="sxs-lookup"><span data-stu-id="c3e27-154">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="c3e27-155">加入会话的用户的终结点的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="c3e27-155">Unique identifier of the endpoint of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-156"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-156"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-157">datetime</span><span class="sxs-lookup"><span data-stu-id="c3e27-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3e27-158">会话的结束时间。</span><span class="sxs-lookup"><span data-stu-id="c3e27-158">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-159"><strong>FromMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-159"><strong>FromMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-160">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-160">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-161">启动会话的用户发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="c3e27-161">Number of messages sent by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-162"><strong>ToMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-162"><strong>ToMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-163">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-163">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-164">加入会话的用户发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="c3e27-164">Number of messages sent by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-165"><strong>FromClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-165"><strong>FromClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-166">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-166">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-167">启动会话的用户所使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="c3e27-167">Version of client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-168"><strong>FromClientType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-168"><strong>FromClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-169">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-169">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-170">启动会话的用户所使用的客户端。</span><span class="sxs-lookup"><span data-stu-id="c3e27-170">Client used by the user who started the session.</span></span> <span data-ttu-id="c3e27-171">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-171">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-172"><strong>FromClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-172"><strong>FromClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-173">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="c3e27-173">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-174">启动会话的用户所使用的客户端类别的名称。</span><span class="sxs-lookup"><span data-stu-id="c3e27-174">Name of the category of the client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-175"><strong>ToClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-175"><strong>ToClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-176">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-176">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-177">加入会话的用户使用的客户端版本</span><span class="sxs-lookup"><span data-stu-id="c3e27-177">Version of client used by the user who joined the session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-178"><strong>ToClientType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-178"><strong>ToClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-179">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-179">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-180">加入会话的用户所使用的客户端。</span><span class="sxs-lookup"><span data-stu-id="c3e27-180">Client used by the user who joined the session.</span></span> <span data-ttu-id="c3e27-181">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-181">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-182"><strong>ToClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-182"><strong>ToClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-183">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="c3e27-183">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-184">加入会话的用户所使用的客户端类别的名称。</span><span class="sxs-lookup"><span data-stu-id="c3e27-184">Name of the category of the client used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-185"><strong>TargetUri</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-185"><strong>TargetUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-186">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="c3e27-186">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-187">会话的目标用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="c3e27-187">URI of the target user of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-188"><strong>TargetUriType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-188"><strong>TargetUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-189">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="c3e27-189">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-190">会话的目标用户的 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="c3e27-190">Type of URI of the target user for the session.</span></span> <span data-ttu-id="c3e27-191">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-191">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-192"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-192"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-193">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="c3e27-193">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-194">已代表其启动会话的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="c3e27-194">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-195"><strong>OnnnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-195"><strong>OnnnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-197">已代表其启动会话的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="c3e27-197">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="c3e27-198">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-198">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-199"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-199"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-201">其代表启动会话的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="c3e27-201">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="c3e27-202">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-202">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-203"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-203"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-204">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="c3e27-204">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-205">引用会话的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="c3e27-205">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-206"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-206"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-207">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-207">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-208">引用会话的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="c3e27-208">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="c3e27-209">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-209">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-210"><strong>ReferredByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-210"><strong>ReferredByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-211">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-211">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-212">引用会话的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="c3e27-212">Tenant of the user who referred the session.</span></span> <span data-ttu-id="c3e27-213">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-213">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-214"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-214"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-215">varchar (775) </span><span class="sxs-lookup"><span data-stu-id="c3e27-215">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-216">SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="c3e27-216">SIP dialog ID.</span></span> <span data-ttu-id="c3e27-217">格式为：</span><span class="sxs-lookup"><span data-stu-id="c3e27-217">The format is:</span></span></p>
<p><span data-ttu-id="c3e27-218">对话框; 从-标签; 到-标记</span><span class="sxs-lookup"><span data-stu-id="c3e27-218">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-219"><strong>True&correlationid</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-219"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-220">标识符</span><span class="sxs-lookup"><span data-stu-id="c3e27-220">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="c3e27-221">用于关联多个会话的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c3e27-221">GUID used to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-222"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-222"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-223">datetime</span><span class="sxs-lookup"><span data-stu-id="c3e27-223">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3e27-224">会话替换的对话的时间。</span><span class="sxs-lookup"><span data-stu-id="c3e27-224">Time of the dialog which was replaced by the session.</span></span> <span data-ttu-id="c3e27-225">与 ReplaceDialogIdSeq 结合使用以唯一标识由会话替换的对话框。</span><span class="sxs-lookup"><span data-stu-id="c3e27-225">Used in conjunction with ReplaceDialogIdSeq to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="c3e27-226">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-226">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-227"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-227"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-228">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-228">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-229">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="c3e27-229">ID number to identify the session.</span></span> <span data-ttu-id="c3e27-230">与 ReplaceDialogIdTime 结合使用以唯一标识由会话替换的对话框。</span><span class="sxs-lookup"><span data-stu-id="c3e27-230">Used in conjunction with ReplaceDialogIdTime to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="c3e27-231">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-231">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-232"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-232"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-233">varchar (775) </span><span class="sxs-lookup"><span data-stu-id="c3e27-233">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-234">会话将替换的 SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="c3e27-234">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="c3e27-235">格式为：</span><span class="sxs-lookup"><span data-stu-id="c3e27-235">The format is:</span></span></p>
<p><span data-ttu-id="c3e27-236">对话框; 从-标签; 到-标记</span><span class="sxs-lookup"><span data-stu-id="c3e27-236">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-237"><strong>ResponseTime</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-237"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-238">datetime</span><span class="sxs-lookup"><span data-stu-id="c3e27-238">datetime</span></span></p></td>
<td><p><span data-ttu-id="c3e27-239">对第一个邀请消息的答复时间。</span><span class="sxs-lookup"><span data-stu-id="c3e27-239">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="c3e27-240">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="c3e27-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="c3e27-241">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-242"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-242"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-243">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-243">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-244">会议邀请的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="c3e27-244">SIP response code to the session invitation.</span></span> <span data-ttu-id="c3e27-245">此字段通常由会话中的初始邀请消息所生成的数据填充。</span><span class="sxs-lookup"><span data-stu-id="c3e27-245">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="c3e27-246">如果没有邀请消息，则该字段将填充第一条相关 SIP 消息的日期和时间， (再见、取消、消息或信息) 。</span><span class="sxs-lookup"><span data-stu-id="c3e27-246">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-247"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-247"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-248">int</span><span class="sxs-lookup"><span data-stu-id="c3e27-248">int</span></span></p></td>
<td><p><span data-ttu-id="c3e27-249">从 SIP 标题捕获的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="c3e27-249">Diagnostic ID captured from SIP headers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-250"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-250"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-251">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-251">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-252">会话的内容类型。</span><span class="sxs-lookup"><span data-stu-id="c3e27-252">Type of content for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-253"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-253"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-254">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-254">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-255">捕获会话的数据的前端服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c3e27-255">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-256"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-256"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-257">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-257">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-258">捕获会话的数据的池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c3e27-258">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-259"><strong>FromEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-259"><strong>FromEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-260">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-260">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-261">启动会话的用户所使用的边缘服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c3e27-261">FQDN of the Edge server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-262"><strong>ToEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-262"><strong>ToEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-263">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-263">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-264">启动会话的用户所使用的边缘服务器的 FQDN</span><span class="sxs-lookup"><span data-stu-id="c3e27-264">FQDN of the Edge server used by the user who started the session</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-265"><strong>IsFromInternal</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-265"><strong>IsFromInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-266">bit</span><span class="sxs-lookup"><span data-stu-id="c3e27-266">bit</span></span></p></td>
<td><p><span data-ttu-id="c3e27-267">指示启动会话的用户是否从内部网络登录。</span><span class="sxs-lookup"><span data-stu-id="c3e27-267">Indicates whether the user who started the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-268"><strong>IsToInternal</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-268"><strong>IsToInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-269">bit</span><span class="sxs-lookup"><span data-stu-id="c3e27-269">bit</span></span></p></td>
<td><p><span data-ttu-id="c3e27-270">指示加入会话的用户是否从内部网络登录。</span><span class="sxs-lookup"><span data-stu-id="c3e27-270">Indicates whether the user who joined the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-271"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-271"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-272">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="c3e27-272">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-273">会话的调用优先级。</span><span class="sxs-lookup"><span data-stu-id="c3e27-273">Call priority of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-274"><strong>FromUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-274"><strong>FromUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-275">smallint</span><span class="sxs-lookup"><span data-stu-id="c3e27-275">smallint</span></span></p></td>
<td><p><span data-ttu-id="c3e27-276">指示启动会话的用户的属性。</span><span class="sxs-lookup"><span data-stu-id="c3e27-276">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="c3e27-277">允许以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="c3e27-277">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="c3e27-278">0x01-与桌面电话集成</span><span class="sxs-lookup"><span data-stu-id="c3e27-278">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-279"><strong>ToUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-279"><strong>ToUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-280">smallint</span><span class="sxs-lookup"><span data-stu-id="c3e27-280">smallint</span></span></p></td>
<td><p><span data-ttu-id="c3e27-281">指示启动会话的用户的属性。</span><span class="sxs-lookup"><span data-stu-id="c3e27-281">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="c3e27-282">允许以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="c3e27-282">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="c3e27-283">0x01-与桌面电话集成</span><span class="sxs-lookup"><span data-stu-id="c3e27-283">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e27-284"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-284"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-285">smallint</span><span class="sxs-lookup"><span data-stu-id="c3e27-285">smallint</span></span></p></td>
<td><p><span data-ttu-id="c3e27-286">指示通话属性。</span><span class="sxs-lookup"><span data-stu-id="c3e27-286">Indicates the call attributes.</span></span> <span data-ttu-id="c3e27-287">允许以下属性定义：</span><span class="sxs-lookup"><span data-stu-id="c3e27-287">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="c3e27-288">0x01-重试会话</span><span class="sxs-lookup"><span data-stu-id="c3e27-288">0x01 - Retried Session</span></span></p>
<p><span data-ttu-id="c3e27-289">0x02-代表响应组的代理发出的呼叫</span><span class="sxs-lookup"><span data-stu-id="c3e27-289">0x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e27-290"><strong>位置</strong></span><span class="sxs-lookup"><span data-stu-id="c3e27-290"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e27-291">varchar (max) </span><span class="sxs-lookup"><span data-stu-id="c3e27-291">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="c3e27-292">紧急电话的位置。</span><span class="sxs-lookup"><span data-stu-id="c3e27-292">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c3e27-293">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3e27-293">


</div>

<span> </span>

</div>

</div>

</span></span></div>

