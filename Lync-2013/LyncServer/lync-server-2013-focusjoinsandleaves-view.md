---
title: Lync Server 2013： FocusJoinsAndLeaves 视图
description: Lync Server 2013： FocusJoinsAndLeaves 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves view
ms:assetid: 226460ef-766f-4d61-80cb-f332b65a210d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687992(v=OCS.15)
ms:contentKeyID: 49733582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6f68c44461e378e9ebedce1305ee6b384a7a8a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428104"
---
# <a name="focusjoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="fb86f-103">Lync Server 2013 中的 FocusJoinsAndLeaves 视图</span><span class="sxs-lookup"><span data-stu-id="fb86f-103">FocusJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb86f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb86f-104">

<span> </span></span></span>

<span data-ttu-id="fb86f-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="fb86f-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="fb86f-106">FocusJoinsAndLeaves 视图存储有关加入和离开一次会议的信息的信息。</span><span class="sxs-lookup"><span data-stu-id="fb86f-106">The FocusJoinsAndLeaves view stores information about join and leave information for one conference.</span></span> <span data-ttu-id="fb86f-107">每个会议在用户加入和离开会议时编写的记录在此视图中表示。</span><span class="sxs-lookup"><span data-stu-id="fb86f-107">Each conference is represented in this view by a record written each time a user joins and leaves the conference.</span></span> <span data-ttu-id="fb86f-108">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="fb86f-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb86f-109">列</span><span class="sxs-lookup"><span data-stu-id="fb86f-109">Column</span></span></th>
<th><span data-ttu-id="fb86f-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="fb86f-110">Data Type</span></span></th>
<th><span data-ttu-id="fb86f-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="fb86f-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-113">datetime</span><span class="sxs-lookup"><span data-stu-id="fb86f-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="fb86f-114">会议实例的时间。</span><span class="sxs-lookup"><span data-stu-id="fb86f-114">Time of conference instance.</span></span> <span data-ttu-id="fb86f-115">与 SessionIdSeq 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="fb86f-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="fb86f-116">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="fb86f-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-118">int</span><span class="sxs-lookup"><span data-stu-id="fb86f-118">int</span></span></p></td>
<td><p><span data-ttu-id="fb86f-119">标识会议实例的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="fb86f-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="fb86f-120">与 SessionIdTime 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="fb86f-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="fb86f-121">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="fb86f-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-122"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-122"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-123">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="fb86f-123">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="fb86f-124">已捕获其会议加入/离开信息的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="fb86f-124">URI of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-125"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-125"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="fb86f-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="fb86f-127">已捕获其会议加入/离开信息的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="fb86f-127">Type of URI of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="fb86f-128">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="fb86f-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-129"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-129"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-130">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="fb86f-130">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="fb86f-131">已捕获其会议加入/离开信息的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="fb86f-131">Tenant of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="fb86f-132">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="fb86f-132">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-133"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-133"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-134">标识符</span><span class="sxs-lookup"><span data-stu-id="fb86f-134">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="fb86f-135">已捕获其会议加入/离开信息的用户的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="fb86f-135">Unique identifier of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-136"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-136"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="fb86f-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="fb86f-138">已捕获其会议加入/离开信息的用户使用的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="fb86f-138">Version of client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-139"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-139"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-140">int</span><span class="sxs-lookup"><span data-stu-id="fb86f-140">int</span></span></p></td>
<td><p><span data-ttu-id="fb86f-141">已捕获会议加入/离开信息的用户使用的客户端。</span><span class="sxs-lookup"><span data-stu-id="fb86f-141">Client used by the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="fb86f-142">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 中的 UserAgentDef 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="fb86f-142">See <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-143"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-143"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-144">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="fb86f-144">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="fb86f-145">已捕获会议加入/离开信息的用户所使用的客户端类别的名称。</span><span class="sxs-lookup"><span data-stu-id="fb86f-145">Name of the category of the client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-146"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-146"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-147">int</span><span class="sxs-lookup"><span data-stu-id="fb86f-147">int</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-148"><strong>IsuserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-148"><strong>IsuserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-149">bit</span><span class="sxs-lookup"><span data-stu-id="fb86f-149">bit</span></span></p></td>
<td><p><span data-ttu-id="fb86f-150">表示用户是否为内部用户的位。</span><span class="sxs-lookup"><span data-stu-id="fb86f-150">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-151"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-151"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-152">datetime</span><span class="sxs-lookup"><span data-stu-id="fb86f-152">datetime</span></span></p></td>
<td><p><span data-ttu-id="fb86f-153">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="fb86f-153">Time of session request.</span></span> <span data-ttu-id="fb86f-154">与 SessionIdSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="fb86f-154">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="fb86f-155">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="fb86f-155">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-156"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-156"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-157">int</span><span class="sxs-lookup"><span data-stu-id="fb86f-157">int</span></span></p></td>
<td><p><span data-ttu-id="fb86f-158">如果用户同时在多台计算机或设备上登录，则 UserInstance 用于唯一标识用户/设备组合。</span><span class="sxs-lookup"><span data-stu-id="fb86f-158">If a user is logged on at multiple computers or devices at the same time, UserInstance is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-159"><strong>DialogId</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-159"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-160">varchar (775) </span><span class="sxs-lookup"><span data-stu-id="fb86f-160">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="fb86f-161">会话的 SIP 对话框 ID。</span><span class="sxs-lookup"><span data-stu-id="fb86f-161">SIP dialog ID of the session.</span></span> <span data-ttu-id="fb86f-162">格式为：对话框; 从-标签; 到-标记。</span><span class="sxs-lookup"><span data-stu-id="fb86f-162">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-163"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-163"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-164">datetime</span><span class="sxs-lookup"><span data-stu-id="fb86f-164">datetime</span></span></p></td>
<td><p><span data-ttu-id="fb86f-165">用户加入会议的时间。</span><span class="sxs-lookup"><span data-stu-id="fb86f-165">Time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb86f-166"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-166"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-167">datetime</span><span class="sxs-lookup"><span data-stu-id="fb86f-167">datetime</span></span></p></td>
<td><p><span data-ttu-id="fb86f-168">用户离开会议的时间。</span><span class="sxs-lookup"><span data-stu-id="fb86f-168">Time that the user left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb86f-169"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="fb86f-169"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="fb86f-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="fb86f-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="fb86f-171">用户在会议中的角色，如 "演示者" 或 "与会者"。</span><span class="sxs-lookup"><span data-stu-id="fb86f-171">User’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fb86f-172">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb86f-172">


</div>

<span> </span>

</div>

</div>

</span></span></div>

