---
title: Lync Server 2013：会话视图
description: Lync Server 2013：会话视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session view
ms:assetid: 49e33f5b-45d0-4146-a5a4-76954d895a98
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688048(v=OCS.15)
ms:contentKeyID: 49733641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff4bc4abbd55e073006693d28f092f077698ef75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444789"
---
# <a name="session-view-in-lync-server-2013"></a><span data-ttu-id="75bbb-103">Lync Server 2013 中的 "会话" 视图</span><span class="sxs-lookup"><span data-stu-id="75bbb-103">Session view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75bbb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75bbb-104">

<span> </span></span></span>

<span data-ttu-id="75bbb-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="75bbb-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="75bbb-106">"会话" 视图存储有关具有数据库中的记录的会话的信息。</span><span class="sxs-lookup"><span data-stu-id="75bbb-106">The Session View stores information about sessions that have records in the database.</span></span> <span data-ttu-id="75bbb-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="75bbb-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75bbb-108">列</span><span class="sxs-lookup"><span data-stu-id="75bbb-108">Column</span></span></th>
<th><span data-ttu-id="75bbb-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="75bbb-109">Data Type</span></span></th>
<th><span data-ttu-id="75bbb-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="75bbb-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-111">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="75bbb-111">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="75bbb-112">datetime</span><span class="sxs-lookup"><span data-stu-id="75bbb-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="75bbb-113">从 MediaLine 表中引用。</span><span class="sxs-lookup"><span data-stu-id="75bbb-113">Referenced from the MediaLine Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-114">ConferenceURI</span><span class="sxs-lookup"><span data-stu-id="75bbb-114">ConferenceURI</span></span></p></td>
<td><p><span data-ttu-id="75bbb-115">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="75bbb-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-116">会议 URI （如果这是会议）或 DialogID （如果这是对等会话）。</span><span class="sxs-lookup"><span data-stu-id="75bbb-116">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-117">关系</span><span class="sxs-lookup"><span data-stu-id="75bbb-117">Correlation</span></span></p></td>
<td><p><span data-ttu-id="75bbb-118">varchar (max) </span><span class="sxs-lookup"><span data-stu-id="75bbb-118">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-119">会话的相关 ID。</span><span class="sxs-lookup"><span data-stu-id="75bbb-119">Correlation ID of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-120">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="75bbb-120">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="75bbb-121">bit</span><span class="sxs-lookup"><span data-stu-id="75bbb-121">bit</span></span></p></td>
<td><p><span data-ttu-id="75bbb-122">对话框类别;0是 Lync 服务器以中介服务器腿;1是中介服务器到 PSTN 网关腿。</span><span class="sxs-lookup"><span data-stu-id="75bbb-122">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-123">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="75bbb-123">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="75bbb-124">bit</span><span class="sxs-lookup"><span data-stu-id="75bbb-124">bit</span></span></p></td>
<td><p><span data-ttu-id="75bbb-125">指示是否跳过呼叫。</span><span class="sxs-lookup"><span data-stu-id="75bbb-125">Indicates whether or not the call was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-126">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="75bbb-126">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="75bbb-127">int</span><span class="sxs-lookup"><span data-stu-id="75bbb-127">int</span></span></p></td>
<td><p><span data-ttu-id="75bbb-128">此字段（如果存在）指示无法跳过呼叫的原因，即使旁路 Id 匹配也是如此。</span><span class="sxs-lookup"><span data-stu-id="75bbb-128">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="75bbb-129">对于 Lync Server，只定义一个值：</span><span class="sxs-lookup"><span data-stu-id="75bbb-129">For Lync Server, only one value is defined:</span></span></p>
<p><span data-ttu-id="75bbb-130">0x0001-默认网络适配器的未知旁路 ID</span><span class="sxs-lookup"><span data-stu-id="75bbb-130">0x0001 – Unknown bypass ID for Default network adapter</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="75bbb-131">StartTime</span></span></p></td>
<td><p><span data-ttu-id="75bbb-132">datetime</span><span class="sxs-lookup"><span data-stu-id="75bbb-132">datetime</span></span></p></td>
<td><p><span data-ttu-id="75bbb-133">通话开始时间。</span><span class="sxs-lookup"><span data-stu-id="75bbb-133">Call start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-134">EndTime</span><span class="sxs-lookup"><span data-stu-id="75bbb-134">EndTime</span></span></p></td>
<td><p><span data-ttu-id="75bbb-135">datetime</span><span class="sxs-lookup"><span data-stu-id="75bbb-135">datetime</span></span></p></td>
<td><p><span data-ttu-id="75bbb-136">通话结束时间。</span><span class="sxs-lookup"><span data-stu-id="75bbb-136">Call end time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-137">CallerPool</span><span class="sxs-lookup"><span data-stu-id="75bbb-137">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="75bbb-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="75bbb-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-139">呼叫方池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="75bbb-139">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-140">CalleePool</span><span class="sxs-lookup"><span data-stu-id="75bbb-140">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="75bbb-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="75bbb-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-142">被调用池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="75bbb-142">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-143">CallerPAI</span><span class="sxs-lookup"><span data-stu-id="75bbb-143">CallerPAI</span></span></p></td>
<td><p><span data-ttu-id="75bbb-144">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="75bbb-144">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-145">调用方的 p 声明标识 URI。</span><span class="sxs-lookup"><span data-stu-id="75bbb-145">Caller’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-146">CalleePAI</span><span class="sxs-lookup"><span data-stu-id="75bbb-146">CalleePAI</span></span></p></td>
<td><p><span data-ttu-id="75bbb-147">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="75bbb-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-148">被调用方的 p 声明标识 URI。</span><span class="sxs-lookup"><span data-stu-id="75bbb-148">Callee’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-149">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="75bbb-149">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="75bbb-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="75bbb-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-151">调用方的终结点名称。</span><span class="sxs-lookup"><span data-stu-id="75bbb-151">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-152">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="75bbb-152">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="75bbb-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="75bbb-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-154">调用方的终结点名称。</span><span class="sxs-lookup"><span data-stu-id="75bbb-154">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-155">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="75bbb-155">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="75bbb-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="75bbb-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-157">呼叫方的用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="75bbb-157">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-158">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="75bbb-158">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="75bbb-159">smallint</span><span class="sxs-lookup"><span data-stu-id="75bbb-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="75bbb-160">呼叫方的用户代理的类型。</span><span class="sxs-lookup"><span data-stu-id="75bbb-160">Type of caller’s user agent.</span></span> <span data-ttu-id="75bbb-161">有关详细信息，请参阅 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="75bbb-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-162">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="75bbb-162">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="75bbb-163">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="75bbb-163">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-164">呼叫者的用户代理类别。</span><span class="sxs-lookup"><span data-stu-id="75bbb-164">Category of caller’s user agent.</span></span> <span data-ttu-id="75bbb-165">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 中的 UserAgentDef 表 (QoE) </a> 。</span><span class="sxs-lookup"><span data-stu-id="75bbb-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-166">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="75bbb-166">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="75bbb-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="75bbb-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-168">被呼叫方的用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="75bbb-168">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-169">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="75bbb-169">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="75bbb-170">smallint</span><span class="sxs-lookup"><span data-stu-id="75bbb-170">smallint</span></span></p></td>
<td><p><span data-ttu-id="75bbb-171">被呼叫方的用户代理类型。</span><span class="sxs-lookup"><span data-stu-id="75bbb-171">Type of user agent for the callee.</span></span> <span data-ttu-id="75bbb-172">有关详细信息，请参阅 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="75bbb-172">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-173">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="75bbb-173">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="75bbb-174">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="75bbb-174">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-175">被呼叫方的用户代理类别。</span><span class="sxs-lookup"><span data-stu-id="75bbb-175">User agent category for the callee.</span></span> <span data-ttu-id="75bbb-176">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 中的 UserAgentDef 表 (QoE) </a> 。</span><span class="sxs-lookup"><span data-stu-id="75bbb-176">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-177">CallerURI</span><span class="sxs-lookup"><span data-stu-id="75bbb-177">CallerURI</span></span></p></td>
<td><p><span data-ttu-id="75bbb-178">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="75bbb-178">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-179">调用方的 URI。</span><span class="sxs-lookup"><span data-stu-id="75bbb-179">Caller’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75bbb-180">CalleeURI</span><span class="sxs-lookup"><span data-stu-id="75bbb-180">CalleeURI</span></span></p></td>
<td><p><span data-ttu-id="75bbb-181">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="75bbb-181">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="75bbb-182">被调用方的 URI。</span><span class="sxs-lookup"><span data-stu-id="75bbb-182">Callee’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75bbb-183">CallPrioirty</span><span class="sxs-lookup"><span data-stu-id="75bbb-183">CallPrioirty</span></span></p></td>
<td><p><span data-ttu-id="75bbb-184">int</span><span class="sxs-lookup"><span data-stu-id="75bbb-184">int</span></span></p></td>
<td><p><span data-ttu-id="75bbb-185">通话的优先级。</span><span class="sxs-lookup"><span data-stu-id="75bbb-185">Priority of the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="75bbb-186">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75bbb-186">


</div>

<span> </span>

</div>

</div>

</span></span></div>

