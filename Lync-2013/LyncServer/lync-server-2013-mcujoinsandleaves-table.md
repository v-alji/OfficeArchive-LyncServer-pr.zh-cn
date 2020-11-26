---
title: Lync Server 2013：McuJoinsAndLeaves 表
description: Lync Server 2013： McuJoinsAndLeaves 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves table
ms:assetid: 4e073366-0b5d-45b4-a3f6-d63dd5fd9f25
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398316(v=OCS.15)
ms:contentKeyID: 48184115
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee7d9473892ac357dcefd80b0d52382c5dd7d930
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425750"
---
# <a name="mcujoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="20aa9-103">Lync Server 2013 中的 McuJoinsAndLeaves 表</span><span class="sxs-lookup"><span data-stu-id="20aa9-103">McuJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20aa9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20aa9-104">

<span> </span></span></span>

<span data-ttu-id="20aa9-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="20aa9-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="20aa9-106">此表中的每条记录包含有关用户加入或离开和会议服务器的一个组合的调用详细信息。</span><span class="sxs-lookup"><span data-stu-id="20aa9-106">Each record in this table contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="20aa9-107">例如，如果用户加入包含 web 会议和音频/视频元素的会议，将为该用户的网络会议加入创建一条记录，并且将为用户的音频/视频会议加入创建另一条记录。</span><span class="sxs-lookup"><span data-stu-id="20aa9-107">For example, if a user joins a conference that includes web conferencing and audio/video elements, one record would be created for that user’s web conferencing join, and another record would be created for the user’s audio/video conferencing join.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20aa9-108">列</span><span class="sxs-lookup"><span data-stu-id="20aa9-108">Column</span></span></th>
<th><span data-ttu-id="20aa9-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="20aa9-109">Data Type</span></span></th>
<th><span data-ttu-id="20aa9-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="20aa9-110">Key/Index</span></span></th>
<th><span data-ttu-id="20aa9-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="20aa9-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20aa9-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-113">datetime</span><span class="sxs-lookup"><span data-stu-id="20aa9-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="20aa9-114">主、外部</span><span class="sxs-lookup"><span data-stu-id="20aa9-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="20aa9-115">会议实例的时间。</span><span class="sxs-lookup"><span data-stu-id="20aa9-115">Time of conference instance.</span></span> <span data-ttu-id="20aa9-116">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="20aa9-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="20aa9-117">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="20aa9-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20aa9-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-119">int</span><span class="sxs-lookup"><span data-stu-id="20aa9-119">int</span></span></p></td>
<td><p><span data-ttu-id="20aa9-120">主、外部</span><span class="sxs-lookup"><span data-stu-id="20aa9-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="20aa9-121">标识会议实例的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="20aa9-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="20aa9-122">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="20aa9-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="20aa9-123">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="20aa9-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20aa9-124"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-125">int</span><span class="sxs-lookup"><span data-stu-id="20aa9-125">int</span></span></p></td>
<td><p><span data-ttu-id="20aa9-126">主、外部</span><span class="sxs-lookup"><span data-stu-id="20aa9-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="20aa9-127">标识此用户的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="20aa9-127">Unique number identifying this user.</span></span> <span data-ttu-id="20aa9-128">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="20aa9-128">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20aa9-129"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-129"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-130">int</span><span class="sxs-lookup"><span data-stu-id="20aa9-130">int</span></span></p></td>
<td><p><span data-ttu-id="20aa9-131">Primary</span><span class="sxs-lookup"><span data-stu-id="20aa9-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="20aa9-132">如果一次用户在多台计算机或设备上登录，McuUserInstance 将唯一标识用户/设备组合。</span><span class="sxs-lookup"><span data-stu-id="20aa9-132">If a user is logged on at multiple computers or devices at once, McuUserInstance uniquely identifies the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20aa9-133"><strong>IsFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-133"><strong>IsFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-134">bit</span><span class="sxs-lookup"><span data-stu-id="20aa9-134">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="20aa9-135">用户是否从 PSTN 进行联接。</span><span class="sxs-lookup"><span data-stu-id="20aa9-135">Whether the user is joining from a PSTN or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20aa9-136"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-136"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-137">int</span><span class="sxs-lookup"><span data-stu-id="20aa9-137">int</span></span></p></td>
<td><p><span data-ttu-id="20aa9-138">主、外部</span><span class="sxs-lookup"><span data-stu-id="20aa9-138">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="20aa9-139">标识此会议服务器的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="20aa9-139">Unique number identifying this conferencing server.</span></span> <span data-ttu-id="20aa9-140">有关详细信息，请参阅 <a href="lync-server-2013-mcus-table.md">Lync Server 2013 中的 Mcus 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="20aa9-140">See the <a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20aa9-141"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-141"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-142">datetime</span><span class="sxs-lookup"><span data-stu-id="20aa9-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="20aa9-143">外表</span><span class="sxs-lookup"><span data-stu-id="20aa9-143">Foreign</span></span></p></td>
<td><p><span data-ttu-id="20aa9-144">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="20aa9-144">Time of session request.</span></span> <span data-ttu-id="20aa9-145">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="20aa9-145">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="20aa9-146">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="20aa9-146">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20aa9-147"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-147"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-148">int</span><span class="sxs-lookup"><span data-stu-id="20aa9-148">int</span></span></p></td>
<td><p><span data-ttu-id="20aa9-149">外表</span><span class="sxs-lookup"><span data-stu-id="20aa9-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="20aa9-150">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="20aa9-150">ID number to identify the session.</span></span> <span data-ttu-id="20aa9-151">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="20aa9-151">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="20aa9-152">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="20aa9-152">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20aa9-153"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-153"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-154">datetime</span><span class="sxs-lookup"><span data-stu-id="20aa9-154">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="20aa9-155">此用户加入此会议服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="20aa9-155">The time this user joins this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20aa9-156"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-156"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-157">datetime</span><span class="sxs-lookup"><span data-stu-id="20aa9-157">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="20aa9-158">此用户离开此会议服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="20aa9-158">The time this user leaves this conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20aa9-159"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="20aa9-159"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="20aa9-160">int</span><span class="sxs-lookup"><span data-stu-id="20aa9-160">int</span></span></p></td>
<td><p><span data-ttu-id="20aa9-161">外表</span><span class="sxs-lookup"><span data-stu-id="20aa9-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="20aa9-162">用于指定会议中客户端软件使用的版本号的标识符。</span><span class="sxs-lookup"><span data-stu-id="20aa9-162">Identifier that specifies the version number of the client software use in the conference.</span></span> <span data-ttu-id="20aa9-163">有关详细信息，请参阅 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013 中的 ClientVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="20aa9-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="20aa9-164">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="20aa9-164">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="20aa9-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20aa9-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

