---
title: Lync Server 2013：Conferences 表
description: Lync Server 2013： "会议" 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences table
ms:assetid: c3da6271-b3c6-4898-894f-10456ec794d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412964(v=OCS.15)
ms:contentKeyID: 48185340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e0d8c61e795dc0c8f9843b871d7e4efd1bec571
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392229"
---
# <a name="conferences-table-in-lync-server-2013"></a><span data-ttu-id="79e2d-103">Lync Server 2013 中的 Conferences 表</span><span class="sxs-lookup"><span data-stu-id="79e2d-103">Conferences table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79e2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79e2d-104">

<span> </span></span></span>

<span data-ttu-id="79e2d-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="79e2d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="79e2d-106">此表中的每条记录包含有关一次会议的通话详细信息。</span><span class="sxs-lookup"><span data-stu-id="79e2d-106">Each record in this table contains call details about one conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79e2d-107">列</span><span class="sxs-lookup"><span data-stu-id="79e2d-107">Column</span></span></th>
<th><span data-ttu-id="79e2d-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="79e2d-108">Data Type</span></span></th>
<th><span data-ttu-id="79e2d-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="79e2d-109">Key/Index</span></span></th>
<th><span data-ttu-id="79e2d-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="79e2d-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79e2d-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-112">datetime</span><span class="sxs-lookup"><span data-stu-id="79e2d-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="79e2d-113">Primary</span><span class="sxs-lookup"><span data-stu-id="79e2d-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="79e2d-114">由 CDR 代理捕获会议请求的时间。</span><span class="sxs-lookup"><span data-stu-id="79e2d-114">Time that the conference request was captured by the CDR agent.</span></span> <span data-ttu-id="79e2d-115">仅用作主键以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="79e2d-115">Used only as a primary key to uniquely identify a conference instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e2d-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-117">int</span><span class="sxs-lookup"><span data-stu-id="79e2d-117">int</span></span></p></td>
<td><p><span data-ttu-id="79e2d-118">Primary</span><span class="sxs-lookup"><span data-stu-id="79e2d-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="79e2d-119">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="79e2d-119">ID number to identify the session.</span></span> <span data-ttu-id="79e2d-120">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="79e2d-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79e2d-121"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-121"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-122">int</span><span class="sxs-lookup"><span data-stu-id="79e2d-122">int</span></span></p></td>
<td><p><span data-ttu-id="79e2d-123">外表</span><span class="sxs-lookup"><span data-stu-id="79e2d-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="79e2d-124">会议 URI。</span><span class="sxs-lookup"><span data-stu-id="79e2d-124">Conference URI.</span></span> <span data-ttu-id="79e2d-125">有关详细信息，请参阅 <a href="lync-server-2013-conferenceuris-table.md">Lync Server 2013 中的 ConferenceUris 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="79e2d-125">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e2d-126"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-126"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-127">标识符</span><span class="sxs-lookup"><span data-stu-id="79e2d-127">uniqueidentifier</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="79e2d-128">适用于定期会议;定期会议的每个实例都具有相同的 <strong>ConferenceUri</strong>，但将具有不同的 <strong>ConfInstance</strong>。</span><span class="sxs-lookup"><span data-stu-id="79e2d-128">Useful for recurring conferences; each instance of a recurring conference has the same <strong>ConferenceUri</strong>, but will have a different <strong>ConfInstance</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79e2d-129"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-129"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-130">datetime</span><span class="sxs-lookup"><span data-stu-id="79e2d-130">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="79e2d-131">会议开始时间。</span><span class="sxs-lookup"><span data-stu-id="79e2d-131">Conference start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e2d-132"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-132"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-133">datetime</span><span class="sxs-lookup"><span data-stu-id="79e2d-133">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="79e2d-134">会议开始时间。</span><span class="sxs-lookup"><span data-stu-id="79e2d-134">Conference start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79e2d-135"><strong>PoolId</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-135"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-136">int</span><span class="sxs-lookup"><span data-stu-id="79e2d-136">int</span></span></p></td>
<td><p><span data-ttu-id="79e2d-137">外表</span><span class="sxs-lookup"><span data-stu-id="79e2d-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="79e2d-138">标识在其中捕获会议的池的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="79e2d-138">ID number to identify the pool in which the conference was captured.</span></span> <span data-ttu-id="79e2d-139">有关详细信息，请参阅 <a href="lync-server-2013-pools-table.md">Lync Server 2013 中的 pool 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="79e2d-139">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e2d-140"><strong>OrganizerId</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-140"><strong>OrganizerId</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-141">整形</span><span class="sxs-lookup"><span data-stu-id="79e2d-141">Int</span></span></p></td>
<td><p><span data-ttu-id="79e2d-142">外表</span><span class="sxs-lookup"><span data-stu-id="79e2d-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="79e2d-143">标识此会议的组织者 URI 的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="79e2d-143">ID number to identify the organizer URI of this conference.</span></span> <span data-ttu-id="79e2d-144">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="79e2d-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79e2d-145"><strong>旗</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-145"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-146">smallint</span><span class="sxs-lookup"><span data-stu-id="79e2d-146">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="79e2d-147">包含会议属性的位掩码。</span><span class="sxs-lookup"><span data-stu-id="79e2d-147">A bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="79e2d-148">可能的值：</span><span class="sxs-lookup"><span data-stu-id="79e2d-148">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="79e2d-149">0X01</span><span class="sxs-lookup"><span data-stu-id="79e2d-149">0X01</span></span></p></li>
<li><p><span data-ttu-id="79e2d-150">合成</span><span class="sxs-lookup"><span data-stu-id="79e2d-150">Synthetic</span></span></p></li>
<li><p><span data-ttu-id="79e2d-151">事务</span><span class="sxs-lookup"><span data-stu-id="79e2d-151">Transaction</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e2d-152"><strong>过</strong></span><span class="sxs-lookup"><span data-stu-id="79e2d-152"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="79e2d-153">bit</span><span class="sxs-lookup"><span data-stu-id="79e2d-153">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="79e2d-154">监视服务使用的内部字段。</span><span class="sxs-lookup"><span data-stu-id="79e2d-154">Internal field used by the Monitoring service.</span></span></p>
<p><span data-ttu-id="79e2d-155">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="79e2d-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="79e2d-156">\* 对于大多数会话，SessionIdSeq 将具有值1。</span><span class="sxs-lookup"><span data-stu-id="79e2d-156">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="79e2d-157">如果两个会话的开始时间完全相同，则一个会话的 SessionIdSeq 将为1，而另一个会话将为2，依此类推。</span><span class="sxs-lookup"><span data-stu-id="79e2d-157">If two sessions start at exactly the same time, the SessionIdSeq for one will be 1, and for the other will be 2, and so on.</span></span>

<span data-ttu-id="79e2d-158"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79e2d-158"></div>

<span> </span>

</div>

</div>

</span></span></div>

