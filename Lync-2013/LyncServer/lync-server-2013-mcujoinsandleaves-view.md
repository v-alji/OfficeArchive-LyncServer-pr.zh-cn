---
title: Lync Server 2013： McuJoinsAndLeaves 视图
description: Lync Server 2013： McuJoinsAndLeaves 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves view
ms:assetid: 6f00b8e7-b8b6-4657-ac5e-d8a571806ae2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688088(v=OCS.15)
ms:contentKeyID: 49733687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7f2f51c340d5bd4824a6e8eff1a0da172a758c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425729"
---
# <a name="mcujoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="f849c-103">Lync Server 2013 中的 McuJoinsAndLeaves 视图</span><span class="sxs-lookup"><span data-stu-id="f849c-103">McuJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f849c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f849c-104">

<span> </span></span></span>

<span data-ttu-id="f849c-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="f849c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="f849c-106">McuJoinsAndLeaves 视图存储有关用户为一个会议服务器加入和离开信息的信息。</span><span class="sxs-lookup"><span data-stu-id="f849c-106">The McuJoinsAndLeaves view stores information about users join and leave information for one conference server.</span></span> <span data-ttu-id="f849c-107">此视图中的每条记录包含有关用户加入或离开和会议服务器的一个组合的调用详细信息。</span><span class="sxs-lookup"><span data-stu-id="f849c-107">Each record in this view contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="f849c-108">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="f849c-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f849c-109">列</span><span class="sxs-lookup"><span data-stu-id="f849c-109">Column</span></span></th>
<th><span data-ttu-id="f849c-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="f849c-110">Data Type</span></span></th>
<th><span data-ttu-id="f849c-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="f849c-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f849c-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-113">datetime</span><span class="sxs-lookup"><span data-stu-id="f849c-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="f849c-114">会议实例的时间。</span><span class="sxs-lookup"><span data-stu-id="f849c-114">Time of conference instance.</span></span> <span data-ttu-id="f849c-115">与 SessionIdSeq 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="f849c-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="f849c-116">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="f849c-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-118">int</span><span class="sxs-lookup"><span data-stu-id="f849c-118">int</span></span></p></td>
<td><p><span data-ttu-id="f849c-119">标识会议实例的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="f849c-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="f849c-120">与 SessionIdTime 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="f849c-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="f849c-121">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="f849c-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-122"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-122"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-123">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f849c-123">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f849c-124">用户连接到的会议服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="f849c-124">The URI of the conferencing server that the user connected to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-125"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-125"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f849c-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f849c-127">用户连接到的会议服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="f849c-127">The URI of the conferencing server that the user connected to.</span></span> <span data-ttu-id="f849c-128">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f849c-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-129"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-129"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-130">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="f849c-130">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="f849c-131">已捕获其会议服务器加入/离开信息的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="f849c-131">The URI of the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-132"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-132"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f849c-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f849c-134">已捕获其会议服务器加入/离开信息的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="f849c-134">The type of URI of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="f849c-135">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f849c-135">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-136"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-136"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f849c-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f849c-138">已捕获其会议服务器加入/离开信息的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="f849c-138">The tenant of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="f849c-139">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f849c-139">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-140"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-140"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f849c-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f849c-142">已捕获会议服务器加入/离开信息的用户所使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="f849c-142">The version of client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-143"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-143"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-144">int</span><span class="sxs-lookup"><span data-stu-id="f849c-144">int</span></span></p></td>
<td><p><span data-ttu-id="f849c-145">已捕获会议服务器加入/离开信息的用户所使用的客户端。</span><span class="sxs-lookup"><span data-stu-id="f849c-145">The client used by the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="f849c-146">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f849c-146">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-147"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-147"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-148">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="f849c-148">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="f849c-149">已捕获其会议服务器加入/离开信息的用户所使用的客户端类别的名称。</span><span class="sxs-lookup"><span data-stu-id="f849c-149">The name of the category of the client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-150"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-150"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-151">int</span><span class="sxs-lookup"><span data-stu-id="f849c-151">int</span></span></p></td>
<td><p><span data-ttu-id="f849c-152">为同时登录到多台设备的用户唯一标识用户/设备组合。</span><span class="sxs-lookup"><span data-stu-id="f849c-152">Uniquely identifies the user/device combination for users simultaneously logged on to multiple devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-153"><strong>IsUserFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-153"><strong>IsUserFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-154">bit</span><span class="sxs-lookup"><span data-stu-id="f849c-154">bit</span></span></p></td>
<td><p><span data-ttu-id="f849c-155">表示用户是否为内部用户的位。</span><span class="sxs-lookup"><span data-stu-id="f849c-155">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-156"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-156"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-157">datetime</span><span class="sxs-lookup"><span data-stu-id="f849c-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="f849c-158">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="f849c-158">Time of session request.</span></span> <span data-ttu-id="f849c-159">与 SessionIdSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="f849c-159">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="f849c-160">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f849c-160">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-161"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-161"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-162">int</span><span class="sxs-lookup"><span data-stu-id="f849c-162">int</span></span></p></td>
<td><p><span data-ttu-id="f849c-163">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="f849c-163">ID number to identify the session.</span></span> <span data-ttu-id="f849c-164">与 SessionIdTime 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="f849c-164">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="f849c-165">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="f849c-165">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-166"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-166"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-167">varchar (775) </span><span class="sxs-lookup"><span data-stu-id="f849c-167">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="f849c-168">会话的 SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="f849c-168">SIP dialog ID of the session.</span></span> <span data-ttu-id="f849c-169">格式为：对话框; 从-标签; 到-标记。</span><span class="sxs-lookup"><span data-stu-id="f849c-169">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f849c-170"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-170"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-171">datetime</span><span class="sxs-lookup"><span data-stu-id="f849c-171">datetime</span></span></p></td>
<td><p><span data-ttu-id="f849c-172">用户加入会议服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="f849c-172">Time the user joined the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f849c-173"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="f849c-173"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f849c-174">datetime</span><span class="sxs-lookup"><span data-stu-id="f849c-174">datetime</span></span></p></td>
<td><p><span data-ttu-id="f849c-175">用户离开会议服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="f849c-175">Time the user left the conferencing server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f849c-176">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f849c-176">


</div>

<span> </span>

</div>

</div>

</span></span></div>

