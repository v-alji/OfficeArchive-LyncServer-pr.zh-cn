---
title: Lync Server 2013：FocusJoinsAndLeaves 表
description: Lync Server 2013： FocusJoinsAndLeaves 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves table
ms:assetid: e6f0212c-67e9-4061-8720-d0296e855991
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399026(v=OCS.15)
ms:contentKeyID: 48185690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5796de16ed204ce4f33935d937cbaa425d63a67f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428103"
---
# <a name="focusjoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="28646-103">Lync Server 2013 中的 FocusJoinsAndLeaves 表</span><span class="sxs-lookup"><span data-stu-id="28646-103">FocusJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28646-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28646-104">

<span> </span></span></span>

<span data-ttu-id="28646-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="28646-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="28646-106">此表中的每条记录包含有关一个用户的加入的 CDR 信息，并为一个会议留下信息。</span><span class="sxs-lookup"><span data-stu-id="28646-106">Each record in this table contains the CDR information about one user’s join and leave information for one conference.</span></span> <span data-ttu-id="28646-107">每次用户加入和离开会议时，每个会议都将在此表中由一条记录表示。</span><span class="sxs-lookup"><span data-stu-id="28646-107">Each conference is represented in this table by one record for each time a user joins and leaves the conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28646-108">列</span><span class="sxs-lookup"><span data-stu-id="28646-108">Column</span></span></th>
<th><span data-ttu-id="28646-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="28646-109">Data Type</span></span></th>
<th><span data-ttu-id="28646-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="28646-110">Key/Index</span></span></th>
<th><span data-ttu-id="28646-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="28646-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28646-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="28646-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-113">datetime</span><span class="sxs-lookup"><span data-stu-id="28646-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="28646-114">主、外部</span><span class="sxs-lookup"><span data-stu-id="28646-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="28646-115">会议实例的时间。</span><span class="sxs-lookup"><span data-stu-id="28646-115">Time of conference instance.</span></span> <span data-ttu-id="28646-116">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="28646-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="28646-117">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="28646-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28646-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="28646-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-119">int</span><span class="sxs-lookup"><span data-stu-id="28646-119">int</span></span></p></td>
<td><p><span data-ttu-id="28646-120">主、外部</span><span class="sxs-lookup"><span data-stu-id="28646-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="28646-121">标识会议实例的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="28646-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="28646-122">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="28646-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="28646-123">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="28646-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28646-124"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="28646-124"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-125">datetime</span><span class="sxs-lookup"><span data-stu-id="28646-125">datetime</span></span></p></td>
<td><p><span data-ttu-id="28646-126">主、外部</span><span class="sxs-lookup"><span data-stu-id="28646-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="28646-127">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="28646-127">Time of session request.</span></span> <span data-ttu-id="28646-128">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="28646-128">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="28646-129">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="28646-129">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28646-130"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="28646-130"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-131">int</span><span class="sxs-lookup"><span data-stu-id="28646-131">int</span></span></p></td>
<td><p><span data-ttu-id="28646-132">主、外部</span><span class="sxs-lookup"><span data-stu-id="28646-132">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="28646-133">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="28646-133">ID number to identify the session.</span></span> <span data-ttu-id="28646-134">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="28646-134">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="28646-135">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="28646-135">see the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28646-136"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="28646-136"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-137">int</span><span class="sxs-lookup"><span data-stu-id="28646-137">int</span></span></p></td>
<td><p><span data-ttu-id="28646-138">外表</span><span class="sxs-lookup"><span data-stu-id="28646-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="28646-139">标识此用户的唯一号码，从 <a href="lync-server-2013-users-table.md">Lync Server 2013 的 "用户" 表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="28646-139">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28646-140"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="28646-140"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-141">int</span><span class="sxs-lookup"><span data-stu-id="28646-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="28646-142">如果用户同时在多台计算机或设备上登录，则 <strong>UserInstance</strong> 用于唯一标识用户/设备组合。</span><span class="sxs-lookup"><span data-stu-id="28646-142">If a user is logged on at multiple computers or devices at the same time, <strong>UserInstance</strong> is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28646-143"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="28646-143"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-144">bit</span><span class="sxs-lookup"><span data-stu-id="28646-144">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="28646-145">用户是否已从内部登录。</span><span class="sxs-lookup"><span data-stu-id="28646-145">Whether the user logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28646-146"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="28646-146"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-147">int</span><span class="sxs-lookup"><span data-stu-id="28646-147">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="28646-148">此用户在会议中的角色，如 "演示者" 或 "与会者"。</span><span class="sxs-lookup"><span data-stu-id="28646-148">This user’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28646-149"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="28646-149"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-150">datetime</span><span class="sxs-lookup"><span data-stu-id="28646-150">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="28646-151">此用户加入会议的时间。</span><span class="sxs-lookup"><span data-stu-id="28646-151">The time this user joins the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28646-152"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="28646-152"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-153">datetime</span><span class="sxs-lookup"><span data-stu-id="28646-153">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="28646-154">此用户离开会议的时间。</span><span class="sxs-lookup"><span data-stu-id="28646-154">The time this user leaves the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28646-155"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="28646-155"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-156">int</span><span class="sxs-lookup"><span data-stu-id="28646-156">int</span></span></p></td>
<td><p><span data-ttu-id="28646-157">外表</span><span class="sxs-lookup"><span data-stu-id="28646-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="28646-158">用户的客户端软件版本， <a href="lync-server-2013-clientversions-table.md">在 Lync Server 2013 中引用 ClientVersions 表</a>。</span><span class="sxs-lookup"><span data-stu-id="28646-158">Version of the user’s client software, referenced to the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28646-159"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="28646-159"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="28646-160">标识符</span><span class="sxs-lookup"><span data-stu-id="28646-160">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="28646-161">会议中使用的终结点 (GUID) 的全局唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="28646-161">Globally unique identifier (GUID) of the endpoint used in the conference.</span></span></p>
<p><span data-ttu-id="28646-162">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="28646-162">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="28646-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28646-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

