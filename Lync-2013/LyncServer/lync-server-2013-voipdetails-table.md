---
title: Lync Server 2013：VoipDetails 表
description: Lync Server 2013： VoipDetails 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f23d991c1d577a15717de2572d744e1b65ba6bab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391731"
---
# <a name="voipdetails-table-in-lync-server-2013"></a><span data-ttu-id="c595b-103">Lync Server 2013 中的 VoipDetails 表</span><span class="sxs-lookup"><span data-stu-id="c595b-103">VoipDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c595b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c595b-104">

<span> </span></span></span>

<span data-ttu-id="c595b-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="c595b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="c595b-106">每条记录表示至少有一位用户是 VoIP 用户的 1 2 方呼叫。</span><span class="sxs-lookup"><span data-stu-id="c595b-106">Each record represents one two-party call in which at least one user is a VoIP user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c595b-107">列</span><span class="sxs-lookup"><span data-stu-id="c595b-107">Column</span></span></th>
<th><span data-ttu-id="c595b-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="c595b-108">Data Type</span></span></th>
<th><span data-ttu-id="c595b-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="c595b-109">Key/Index</span></span></th>
<th><span data-ttu-id="c595b-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="c595b-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c595b-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-112">datetime</span><span class="sxs-lookup"><span data-stu-id="c595b-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="c595b-113">Primary</span><span class="sxs-lookup"><span data-stu-id="c595b-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="c595b-114">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="c595b-114">Time of session request.</span></span> <span data-ttu-id="c595b-115">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="c595b-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="c595b-116">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c595b-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-118">int</span><span class="sxs-lookup"><span data-stu-id="c595b-118">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-119">Primary</span><span class="sxs-lookup"><span data-stu-id="c595b-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="c595b-120">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="c595b-120">ID number to identify the session.</span></span> <span data-ttu-id="c595b-121">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="c595b-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="c595b-122">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c595b-123"><strong>FromNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-123"><strong>FromNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-124">int</span><span class="sxs-lookup"><span data-stu-id="c595b-124">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-125">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-126">呼叫方的<strong>PhoneId</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-126"><strong>PhoneId</strong> of the caller.</span></span> <span data-ttu-id="c595b-127">有关详细信息，请参阅 <a href="lync-server-2013-phones-table.md">Lync Server 2013 中</a> 的 "电话" 表。</span><span class="sxs-lookup"><span data-stu-id="c595b-127">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="c595b-128">如果 not NULL 且 <strong>FromGatewayId</strong> 不为 null，则呼叫方是 PSTN 用户。</span><span class="sxs-lookup"><span data-stu-id="c595b-128">If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c595b-129"><strong>ConnectedNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-129"><strong>ConnectedNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-130">int</span><span class="sxs-lookup"><span data-stu-id="c595b-130">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-131">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-131">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-132">呼叫接收器的<strong>PhoneId</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-132"><strong>PhoneId</strong> of the call receiver.</span></span> <span data-ttu-id="c595b-133">有关详细信息，请参阅 <a href="lync-server-2013-phones-table.md">Lync Server 2013 中</a> 的 "电话" 表。</span><span class="sxs-lookup"><span data-stu-id="c595b-133">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="c595b-134">如果 not NULL 且 <strong>ToGatewayId</strong> 不为 null，则呼叫接收器是 PSTN 用户。</span><span class="sxs-lookup"><span data-stu-id="c595b-134">If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c595b-135"><strong>FromMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-135"><strong>FromMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-136">int</span><span class="sxs-lookup"><span data-stu-id="c595b-136">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-137">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-138">呼叫来自的中介服务器。</span><span class="sxs-lookup"><span data-stu-id="c595b-138">The Mediation Server the call is coming from.</span></span> <span data-ttu-id="c595b-139">有关详细信息，请参阅 <a href="lync-server-2013-mediationservers-table.md">Lync Server 2013 中的 MediationServers 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-139">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c595b-140"><strong>ToMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-140"><strong>ToMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-141">int</span><span class="sxs-lookup"><span data-stu-id="c595b-141">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-142">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-143">将调用的中介服务器将转到。</span><span class="sxs-lookup"><span data-stu-id="c595b-143">The Mediation Server called is going to.</span></span> <span data-ttu-id="c595b-144">有关详细信息，请参阅 <a href="lync-server-2013-mediationservers-table.md">Lync Server 2013 中的 MediationServers 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-144">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c595b-145"><strong>FromGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-145"><strong>FromGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-146">int</span><span class="sxs-lookup"><span data-stu-id="c595b-146">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-147">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-148">呼叫的网关来自。</span><span class="sxs-lookup"><span data-stu-id="c595b-148">Gateway the call is coming from.</span></span> <span data-ttu-id="c595b-149">有关详细信息，请参阅 <a href="lync-server-2013-gateways-table.md">Lync Server 2013 中的网关表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-149">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c595b-150"><strong>ToGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-150"><strong>ToGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-151">int</span><span class="sxs-lookup"><span data-stu-id="c595b-151">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-152">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-152">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-153">呼叫将转网网关。</span><span class="sxs-lookup"><span data-stu-id="c595b-153">Gateway the call is going to.</span></span> <span data-ttu-id="c595b-154">有关详细信息，请参阅 <a href="lync-server-2013-gateways-table.md">Lync Server 2013 中的网关表</a> 。</span><span class="sxs-lookup"><span data-stu-id="c595b-154">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c595b-155"><strong>DisconnectedbyURIId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-155"><strong>DisconnectedbyURIId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-156">int</span><span class="sxs-lookup"><span data-stu-id="c595b-156">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-157">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-158">断开呼叫的用户的 URI （如果用户具有 URI）。</span><span class="sxs-lookup"><span data-stu-id="c595b-158">URI of the user who disconnected the call, if the user has a URI.</span></span> <span data-ttu-id="c595b-159">有关详细信息，请参阅 <a href="lync-server-2013-users-table.md">Lync Server 2013 中</a> 的 "用户" 表。</span><span class="sxs-lookup"><span data-stu-id="c595b-159">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c595b-160"><strong>DisconnectedbyPhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="c595b-160"><strong>DisconnectedbyPhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="c595b-161">int</span><span class="sxs-lookup"><span data-stu-id="c595b-161">int</span></span></p></td>
<td><p><span data-ttu-id="c595b-162">外表</span><span class="sxs-lookup"><span data-stu-id="c595b-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c595b-163">断开通话的电话的 ID 已断开与电话的连接。</span><span class="sxs-lookup"><span data-stu-id="c595b-163">ID of the phone that disconnected the call was disconnected from a phone.</span></span> <span data-ttu-id="c595b-164">有关详细信息，请参阅 <a href="lync-server-2013-phones-table.md">Lync Server 2013 中</a> 的 "电话" 表。</span><span class="sxs-lookup"><span data-stu-id="c595b-164">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c595b-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c595b-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

