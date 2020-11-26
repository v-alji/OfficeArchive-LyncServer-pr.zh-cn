---
title: Lync Server 2013： AudioStreamDetail 视图
description: Lync Server 2013： AudioStreamDetail 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438160"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="7a0d4-103">Lync Server 2013 中的 AudioStreamDetail 视图</span><span class="sxs-lookup"><span data-stu-id="7a0d4-103">AudioStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a0d4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a0d4-104">

<span> </span></span></span>

<span data-ttu-id="7a0d4-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="7a0d4-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="7a0d4-106">AudioStreamDetail 视图存储有关数据库中每个音频流的信息。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-106">The AudioStreamDetail View stores information about each audio stream in the database.</span></span> <span data-ttu-id="7a0d4-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a0d4-108">列</span><span class="sxs-lookup"><span data-stu-id="7a0d4-108">Column</span></span></th>
<th><span data-ttu-id="7a0d4-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="7a0d4-109">Data Type</span></span></th>
<th><span data-ttu-id="7a0d4-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="7a0d4-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="7a0d4-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-112">datetime</span><span class="sxs-lookup"><span data-stu-id="7a0d4-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-113">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="7a0d4-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-115">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-115">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-116">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-117">StreamId</span><span class="sxs-lookup"><span data-stu-id="7a0d4-117">StreamId</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-118">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-118">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-119">媒体行内的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-119">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-120">StartTime</span><span class="sxs-lookup"><span data-stu-id="7a0d4-120">StartTime</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-121">datetime</span><span class="sxs-lookup"><span data-stu-id="7a0d4-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-122">会话的开始时间。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-122">Start time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-123">EndTime</span><span class="sxs-lookup"><span data-stu-id="7a0d4-123">EndTime</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-124">datetime</span><span class="sxs-lookup"><span data-stu-id="7a0d4-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-125">会话的结束时间。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-125">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-126">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="7a0d4-126">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-127">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-127">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-128">对话框类别：0是 Lync 服务器，用于采集服务器腿;1是中介服务器到 PSTN 网关腿。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-128">Dialog category: 0 is the Lync Server to Mediation Server leg; 1 is the Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-129">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="7a0d4-129">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-130">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-130">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-131">指示是否已绕过呼叫的标志。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-131">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-132">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="7a0d4-132">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-133">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-133">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-134">如果存在，则指示未跳过呼叫的原因，即使旁路 Id 匹配也是如此。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-134">If present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="7a0d4-135">仅定义了一个值：</span><span class="sxs-lookup"><span data-stu-id="7a0d4-135">Only one value is defined:</span></span></p>
<p><span data-ttu-id="7a0d4-136">0x0001-默认网络适配器的旁路 ID 未知。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-136">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-137">CallPriority</span><span class="sxs-lookup"><span data-stu-id="7a0d4-137">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-138">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-138">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-139">通话的优先级。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-139">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-140">CallerPool</span><span class="sxs-lookup"><span data-stu-id="7a0d4-140">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a0d4-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-142">呼叫方池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-142">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-143">CalleePool</span><span class="sxs-lookup"><span data-stu-id="7a0d4-143">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-144">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a0d4-144">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-145">被调用池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-145">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-146">呼叫者</span><span class="sxs-lookup"><span data-stu-id="7a0d4-146">Caller</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-147">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-148">调用方的 URI。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-148">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-149">被叫方</span><span class="sxs-lookup"><span data-stu-id="7a0d4-149">Callee</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-150">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-150">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-151">被调用方的 URI。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-151">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-152">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="7a0d4-152">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a0d4-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-154">呼叫方的用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-154">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-155">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="7a0d4-155">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-156">smallint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-156">smallint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-157">呼叫方的用户代理的类型。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-157">Type of the caller’s user agent.</span></span> <span data-ttu-id="7a0d4-158">有关详细信息，请参阅 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-158">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-159">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="7a0d4-159">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-160">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-160">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-161">呼叫方的用户代理类别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-161">Category of the caller’s user agent.</span></span> <span data-ttu-id="7a0d4-162">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 中的 UserAgentDef 表 (QoE) </a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-162">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-163">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="7a0d4-163">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-164">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a0d4-164">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-165">被呼叫方的用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-165">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-166">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="7a0d4-166">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-167">smallint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-167">smallint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-168">被调用方的用户代理的类型。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-168">Type of callee’s user agent.</span></span> <span data-ttu-id="7a0d4-169">有关信息，请参阅 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-169">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-170">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="7a0d4-170">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-171">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-171">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-172">被呼叫方的用户代理类别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-172">Category of callee’s user agent.</span></span> <span data-ttu-id="7a0d4-173">有关信息，请参阅 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 中的 UserAgentDef 表 (QoE) </a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-173">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-174">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-174">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a0d4-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-176">调用方的终结点名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-176">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-177">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-177">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7a0d4-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-179">被调用方的终结点名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-179">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-180">CallerOS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-180">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-181">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-181">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-182">呼叫方终结点 (操作系统) 的操作系统。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-182">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-183">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-183">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-184">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-184">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-185">被调用方终结点的操作系统 (操作系统) 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-185">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-186">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="7a0d4-186">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-187">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-187">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-188">呼叫方终结点的 CPU 名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-188">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-189">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="7a0d4-189">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-190">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-190">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-191">被调用方终结点的 CPU 名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-191">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-192">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="7a0d4-192">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-193">smallint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-193">smallint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-194">呼叫方终结点中的 CPU 内核数。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-194">Number of CPU cores in the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-195">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="7a0d4-195">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-196">smallint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-196">smallint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-197">被调用方的终结点中的 CPU 内核数。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-197">Number of CPU cores in the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-198">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7a0d4-198">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-199">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-199">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-200">呼叫方终结点的 CPU 处理器速度。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-200">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-201">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7a0d4-201">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-202">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-202">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-203">被调用方终结点的 CPU 处理器速度。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-203">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-204">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="7a0d4-204">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-206">指示呼叫者的系统是否在虚拟化环境中运行。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-206">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="7a0d4-207">有关详细信息，请参阅 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 中的终结点表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-207">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-208">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="7a0d4-208">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-209">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-209">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-210">指示被调用方的系统是否在虚拟化环境中运行。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-210">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="7a0d4-211">有关详细信息，请参阅 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 中的终结点表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-211">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-212">CorrelationKey</span><span class="sxs-lookup"><span data-stu-id="7a0d4-212">CorrelationKey</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7a0d4-213">相关密钥。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-213">Correlation key.</span></span> <span data-ttu-id="7a0d4-214">从 <a href="lync-server-2013-sessioncorrelation-table.md">Lync Server 2013 中的 SessionCorrelation 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-214">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-215">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="7a0d4-215">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-216">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-216">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-217">有关媒体路径（如直接或中继）的信息。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-217">Information about the media path, such as direct or relayed.</span></span> <span data-ttu-id="7a0d4-218">有关详细信息，请参阅 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-218">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-219">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="7a0d4-219">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-220">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-220">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-221">有关交互式连接的信息 (冰) 过程（在调用方的位标志中描述）。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-221">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="7a0d4-222">有关详细信息，请参阅体验质量监视服务器协议规范。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-222">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-223">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="7a0d4-223">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-224">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-224">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-225">有关交互式连接的信息 (冰) 进程（在被呼叫方的位标志中描述）。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-225">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="7a0d4-226">有关详细信息，请参阅体验质量监视服务器协议规范。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-226">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-227">Transport</span><span class="sxs-lookup"><span data-stu-id="7a0d4-227">Transport</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-228">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-228">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-229">传输类型：0是 UDP，1是 TCP。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-229">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-230">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="7a0d4-230">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-231">var (50) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-232">呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-232">IP address of the caller.</span></span> <span data-ttu-id="7a0d4-233">这可能是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-234">CallerPort</span><span class="sxs-lookup"><span data-stu-id="7a0d4-234">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-235">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-235">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-236">呼叫方使用的端口。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-236">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-237">CallerInside</span><span class="sxs-lookup"><span data-stu-id="7a0d4-237">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-238">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-238">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-239">指示呼叫者是否在间隔网络内：1表示呼叫方位于企业网络内，0表示呼叫方位于网络外部。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-239">Indicates whether the caller is inside the interval network: 1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-240">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="7a0d4-240">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-241">var (50) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-241">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-242">被呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-242">IP address of the callee.</span></span> <span data-ttu-id="7a0d4-243">这可能是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-243">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-244">CalleePort</span><span class="sxs-lookup"><span data-stu-id="7a0d4-244">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-245">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-245">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-246">被呼叫方使用的端口。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-246">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-247">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="7a0d4-247">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-248">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-248">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-249">指示被调用方是否在间隔网络内：1表示被呼叫方位于企业网络内，0表示被呼叫方位于网络外部。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-249">Indicates whether the callee is inside the interval network: 1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-250">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="7a0d4-250">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-251">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-251">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-252">呼叫者站点的名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-252">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-253">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="7a0d4-253">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-254">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-254">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-255">呼叫方网站的国家/地区的名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-255">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-256">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="7a0d4-256">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-257">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-257">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-258">被调用方的网站的名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-258">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-259">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="7a0d4-259">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-260">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-260">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-261">被呼叫方网站的国家/地区的名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-261">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-262">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="7a0d4-262">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-263">var (50) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-263">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-264">呼叫方使用的 A/V 边缘服务的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-264">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="7a0d4-265">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-265">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-266">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="7a0d4-266">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-267">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-267">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-268">由呼叫方使用的 A/V 边缘服务使用的端口。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-268">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-269">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="7a0d4-269">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-270">var (50) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-270">var(50)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-271">被呼叫方使用的 A/V 边缘服务的 IP 地址密钥。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-271">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="7a0d4-272">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-272">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-273">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="7a0d4-273">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-274">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-274">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-275">用于由被呼叫方使用的 A/V 边缘服务的端口。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-275">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-276">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="7a0d4-276">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-277">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-277">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-278">呼叫方的捕获设备名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-278">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-279">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="7a0d4-279">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-280">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-280">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-281">调用方的呈现设备名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-281">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-282">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="7a0d4-282">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-283">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-283">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-284">呼叫方的捕获设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-284">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-285">CallerRenderDriver</span><span class="sxs-lookup"><span data-stu-id="7a0d4-285">CallerRenderDriver</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-286">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-286">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-287">呼叫方的呈现设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-287">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-288">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="7a0d4-288">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-289">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-289">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-290">被调用方的捕获设备名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-290">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-291">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="7a0d4-291">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-292">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-292">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-293">被调用方的呈现设备名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-293">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-294">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="7a0d4-294">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-295">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-295">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-296">被调用方的捕获设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-296">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-297">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="7a0d4-297">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-298">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-298">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-299">被调用方的呈现设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-299">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-300">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="7a0d4-300">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-302">呼叫者的网络连接类型：0是 "有线"，1是 "无线"。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-302">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-303">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="7a0d4-303">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-304">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-304">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-305">指示呼叫者是否通过虚拟专用网络连接：1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-305">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-306">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="7a0d4-306">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-307">十进制 (18，0) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-307">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-308">呼叫方终结点的网络链接速度（以 bps 为实现）。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-308">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-309">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="7a0d4-309">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-310">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-310">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-311">被呼叫方的网络连接类型：0是 "有线"，1是 "无线"。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-311">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-312">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="7a0d4-312">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-313">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-313">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-314">指示呼叫者是否通过虚拟专用网络连接：1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-314">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-315">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="7a0d4-315">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-316">十进制 (18，0) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-316">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-317">被呼叫方终结点的网络链接速度，以 bps 为限。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-317">Network link speed for the callee's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-318">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-318">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-319">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-319">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-320">Narrowband) 的音频 (会话的会话 MOS。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-320">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-321">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-321">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-322">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-322">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-323">在给定各种策略设置 (、API、SDP、策略服务器等) 的情况下，应用到给定发送方流的实际带宽。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-323">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="7a0d4-324">此操作不会与有效的带宽混淆，因为根据带宽估计，可能会有较低的有效带宽。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-324">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="7a0d4-325">这基本上是发送流对带宽估计所施加限制限制的最大带宽</span><span class="sxs-lookup"><span data-stu-id="7a0d4-325">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-326">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="7a0d4-326">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-327">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-327">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-328">实时控制协议 (RTCP) 统计信息的平均网络抖动。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-328">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-329">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="7a0d4-329">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-330">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-330">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-331">通话期间网络抖动的最大值。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-331">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-332">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="7a0d4-332">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-333">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-333">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-334">通话期间平均数据包丢失速率。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-334">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-335">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="7a0d4-335">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-336">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-336">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-337">通话过程中观察到的最大数据包丢失。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-337">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-338">BurstDensity</span><span class="sxs-lookup"><span data-stu-id="7a0d4-338">BurstDensity</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-339">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-339">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-340">通话期间出现猝发损失期间的数据包丢失的平均密度。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-340">Average density of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-341">BurstDuration</span><span class="sxs-lookup"><span data-stu-id="7a0d4-341">BurstDuration</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-342">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-342">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-343">通话期间出现猝发损失期间的数据包丢失的平均持续时间。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-343">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-344">BurstGapDensity</span><span class="sxs-lookup"><span data-stu-id="7a0d4-344">BurstGapDensity</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-345">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-345">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-346">出现猝发数据包丢失之间的平均数据包损失的平均密度。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-346">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-347">BurstGapDuration</span><span class="sxs-lookup"><span data-stu-id="7a0d4-347">BurstGapDuration</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-348">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-348">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-349">爆发数据包损失之间的平均持续时间。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-349">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-350">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="7a0d4-350">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-351">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-351">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-352">音频流的数据包计数。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-352">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-353">BandwidthEst</span><span class="sxs-lookup"><span data-stu-id="7a0d4-353">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-354">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-354">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-355">音频流的带宽估计。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-355">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-356">DegradationAvg</span><span class="sxs-lookup"><span data-stu-id="7a0d4-356">DegradationAvg</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-357">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-357">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-358">整个通话的网络 MOS 降级。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-358">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="7a0d4-359">范围为0.0 到5.0。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-359">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="7a0d4-360">此指标显示由于抖动和数据包丢失，网络 MOS 的减少量。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-360">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="7a0d4-361">对于可接受的质量，它应小于0.5。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-361">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-362">DegradationMax</span><span class="sxs-lookup"><span data-stu-id="7a0d4-362">DegradationMax</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-363">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-363">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-364">通话期间最大网络 MOS 性能下降。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-364">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-365">DegradationJitterAvg</span><span class="sxs-lookup"><span data-stu-id="7a0d4-365">DegradationJitterAvg</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-366">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-366">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-367">由抖动导致的网络 MOS 性能下降。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-367">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-368">DegradationPacketLossAvg</span><span class="sxs-lookup"><span data-stu-id="7a0d4-368">DegradationPacketLossAvg</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-369">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-369">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-370">由于数据包丢失导致网络 MOS 性能下降。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-370">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-371">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="7a0d4-371">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-372">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-372">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-373">用于呼叫的音频编解码器，从 <a href="lync-server-2013-payloaddescription-table.md">Lync Server 2013 中的 PayloadDescription 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-373">The audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-374">AudioSampleRate</span><span class="sxs-lookup"><span data-stu-id="7a0d4-374">AudioSampleRate</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-375">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-375">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-376">音频流的采样率。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-376">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-377">CallerSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-377">CallerSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-378">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-378">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-379">呼叫者发送的音频的模拟增益控制音频信号级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-379">Post-Analog Gain Control audio signal level for the audio the caller sent.</span></span> <span data-ttu-id="7a0d4-380">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-380">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-381">为获得可接受的质量，它至少应为 30 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-381">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="7a0d4-382">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-382">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-383">CallerRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-383">CallerRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-384">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-384">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-385">呼叫者收到的音频的音频信号级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-385">Audio signal level for the audio the caller received.</span></span> <span data-ttu-id="7a0d4-386">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-386">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-387">为获得可接受的质量，它至少应为 30 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-387">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="7a0d4-388">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-388">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-389">CallerSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-389">CallerSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-390">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-390">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-391">为呼叫者发送的音频的模拟后增益控制音频噪音级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-391">Post-Analog Gain Control audio noise level for the audio the caller sent.</span></span> <span data-ttu-id="7a0d4-392">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-392">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-393">为获得可接受的质量，它应小于 35 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-393">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="7a0d4-394">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-394">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-395">CallerRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-395">CallerRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-396">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-396">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-397">呼叫者收到的音频的后模拟增益控制音频噪音级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-397">Post-Analog Gain Control audio noise level for the audio the caller received.</span></span> <span data-ttu-id="7a0d4-398">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-398">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-399">为获得可接受的质量，它应小于 35 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-399">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="7a0d4-400">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-400">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-401">CallerEchoReturn</span><span class="sxs-lookup"><span data-stu-id="7a0d4-401">CallerEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-402">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-402">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-403">呼叫方的回音返回损失增强。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-403">Echo Return Loss Enhancement for the caller.</span></span> <span data-ttu-id="7a0d4-404">此指标的单位为 dB。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-404">The unit for this metric is dB.</span></span> <span data-ttu-id="7a0d4-405">较低的值表示较少的回声。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-405">Lower values represent less echo.</span></span> <span data-ttu-id="7a0d4-406">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-406">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-407">CallerSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="7a0d4-407">CallerSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-408">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-408">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-409">呼叫者的扬声器呈现每五分钟的平均故障。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-409">Average glitches per five minutes for the caller’s loudspeaker rendering.</span></span> <span data-ttu-id="7a0d4-410">为了获得良好的质量，这应该小于每五分钟一次。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-410">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="7a0d4-411">不由 A/V 式会议服务器、中介服务器或 IP 电话报告。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-411">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-412">CallerMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="7a0d4-412">CallerMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-413">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-413">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-414">呼叫者的麦克风捕获每五分钟的平均故障。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-414">Average glitches per five minutes for the caller’s microphone capture.</span></span> <span data-ttu-id="7a0d4-415">为了获得良好的质量，这应该小于每五分钟一次。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-415">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="7a0d4-416">不由 A/V 式会议服务器、中介服务器或 IP 电话报告。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-416">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-417">CallerTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="7a0d4-417">CallerTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-418">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-418">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-419">呼叫者的麦克风设备时钟偏移速率，相对于 CPU 时钟。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-419">Caller’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-420">CallerTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="7a0d4-420">CallerTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-421">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-421">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-422">呼叫者的扬声器设备时钟偏移率（相对于 CPU 时钟）。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-422">Caller’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-423">CallerTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="7a0d4-423">CallerTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-424">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-424">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-425">在呼叫的最后20秒内，麦克风捕获流时间戳的平均时间戳错误（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-425">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-426">CallerTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="7a0d4-426">CallerTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-427">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-427">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-428">呼叫者最近20秒内呼叫者的扬声器渲染流时间戳错误的平均值。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-428">Average of the caller’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-429">CallerVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="7a0d4-429">CallerVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-430">smallint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-430">smallint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-431">语音开关是一种具有更低中断能力的半双工模式。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-431">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="7a0d4-432">有关详细信息，请参阅 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-432">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-433">CallerEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="7a0d4-433">CallerEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-434">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-434">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-435">呼叫方的 echo 事件的原因。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-435">Causes of an echo event for the caller.</span></span> <span data-ttu-id="7a0d4-436">有关详细信息，请参阅 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-436">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-437">CallerEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="7a0d4-437">CallerEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-438">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-438">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-439">在呼叫者的麦克风捕获流中检测到回声的时间的百分比。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-439">Percentage of time when echo is detected in the caller’s microphone capture stream.</span></span> <span data-ttu-id="7a0d4-440">如果使用耳机，则该值应较低。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-440">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-441">CallerEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="7a0d4-441">CallerEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-442">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-442">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-443">在呼叫方的发送流中检测到回显的时间的百分比。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-443">Percentage of time when echo is detected in the caller’s sent stream.</span></span> <span data-ttu-id="7a0d4-444">发送流中的高回显百分比表示回声泄漏。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-444">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-445">CallerRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-445">CallerRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-446">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-446">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-447">在中介服务器上收到来自呼叫者音频的网关的信号级别;这仅适用于中介服务器。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-447">Received signal level on the Mediation Server from the Gateway for the caller’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="7a0d4-448">此指标的单位为 dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-448">The unit of this metric is dBoV.</span></span> <span data-ttu-id="7a0d4-449">为了获得优质，可接受范围应为-30 至-18 dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-449">For good quality, the acceptable range should be -30 to -18 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-450">CallerRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-450">CallerRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-451">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-451">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-452">在中介服务器上从呼叫方音频的网关接收的信号级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-452">Received signal level on the Mediation Server from the Gateway for the caller’s audio.</span></span> <span data-ttu-id="7a0d4-453">这仅适用于中介服务器。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-453">This applies only to the Mediation Server.</span></span> <span data-ttu-id="7a0d4-454">此指标的单位为 dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-454">The unit of this metric is dBoV.</span></span> <span data-ttu-id="7a0d4-455">为了获得优质，可接受范围应小于-50 dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-455">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-456">CallerRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="7a0d4-456">CallerRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-457">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-457">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-458"> (AGC) 的自动增益控制应用于呼叫方音频的中介服务器端。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-458">Automatic gain control (AGC) on the Mediation Server side applied to the caller’s audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-459">CallerInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-459">CallerInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-460">float</span><span class="sxs-lookup"><span data-stu-id="7a0d4-460">float</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-461">根平均值平方 (将传入信号的 RMS) 到呼叫者的前30秒。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-461">Root mean square (RMS) of the incoming signal to the caller for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-462">CalleeSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-462">CalleeSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-463">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-463">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-464">表示被呼叫者发送的音频的后模拟增益控制音频信号级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-464">Represents the Post-Analog Gain Control audio signal level for the audio the callee sent.</span></span> <span data-ttu-id="7a0d4-465">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-465">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-466">为获得可接受的质量，它至少应为 30 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-466">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="7a0d4-467">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-467">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-468">CalleeRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-468">CalleeRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-469">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-469">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-470">被呼叫方收到的音频的音频信号级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-470">Audio signal level for the audio the callee received.</span></span> <span data-ttu-id="7a0d4-471">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-471">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-472">为获得可接受的质量，它至少应为 30 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-472">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="7a0d4-473">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-473">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-474">CalleeSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-474">CalleeSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-475">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-475">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-476">对被呼叫者发送的音频进行模拟提升控制音频噪音级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-476">Post-Analog Gain Control audio noise level for the audio the callee sent.</span></span> <span data-ttu-id="7a0d4-477">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-477">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-478">为获得可接受的质量，它应小于 35 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-478">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="7a0d4-479">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-479">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-480">CalleeRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-480">CalleeRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-481">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-481">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-482">被呼叫方接收的音频的模拟后增益控制音频噪音级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-482">Post-Analog Gain Control audio noise level for the audio the callee received.</span></span> <span data-ttu-id="7a0d4-483">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-483">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7a0d4-484">为获得可接受的质量，它应小于 35 dBmo。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-484">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="7a0d4-485">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-485">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-486">CalleeEchoReturn</span><span class="sxs-lookup"><span data-stu-id="7a0d4-486">CalleeEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-487">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-487">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-488">被调用方的回音返回损失增强。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-488">Echo Return Loss Enhancement for the callee.</span></span> <span data-ttu-id="7a0d4-489">此指标的单位为 dB。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-489">The unit for this metric is dB.</span></span> <span data-ttu-id="7a0d4-490">较低的值表示较少的回声。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-490">Lower values represent less echo.</span></span> <span data-ttu-id="7a0d4-491">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-491">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-492">CalleeSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="7a0d4-492">CalleeSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-493">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-493">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-494">被调用方的扬声器呈现每五分钟的平均故障。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-494">Average glitches per five minutes for the callee’s loudspeaker rendering.</span></span> <span data-ttu-id="7a0d4-495">为了获得良好的质量，这应该小于每五分钟一次。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-495">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="7a0d4-496">不由 A/V 式会议服务器、中介服务器或 IP 电话报告。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-496">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-497">CalleeMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="7a0d4-497">CalleeMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-498">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-498">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-499">被呼叫者的麦克风捕获每五分钟的平均故障。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-499">Average glitches per five minutes for the callee’s microphone capture.</span></span> <span data-ttu-id="7a0d4-500">为了获得良好的质量，这应该小于每五分钟一次。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-500">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="7a0d4-501">不由 A/V 式会议服务器、中介服务器或 IP 电话报告。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-501">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-502">CalleeTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="7a0d4-502">CalleeTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-503">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-503">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-504">被呼叫者的麦克风设备时钟偏移速率，相对于 CPU 时钟。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-504">Callee’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-505">CalleeTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="7a0d4-505">CalleeTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-506">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-506">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-507">被呼叫者的扬声器设备时钟偏移速率，相对于 CPU 时钟。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-507">Callee’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-508">CalleeTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="7a0d4-508">CalleeTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-509">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-509">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-510">在呼叫的最后20秒内，麦克风捕获流时间戳的平均时间戳错误（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-510">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-511">CalleeTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="7a0d4-511">CalleeTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-512">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-512">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-513">在呼叫的最后20秒内，被调用方的扬声器的平均呈现流时间戳错误（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-513">Average of the callee’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-514">CalleeVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="7a0d4-514">CalleeVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-515">smallint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-515">smallint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-516">语音开关是一种具有更低中断能力的半双工模式。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-516">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="7a0d4-517">有关详细信息，请参阅 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-517">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-518">CalleeEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="7a0d4-518">CalleeEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-519">tinyint</span><span class="sxs-lookup"><span data-stu-id="7a0d4-519">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-520">被调用方的 echo 事件的原因。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-520">Causes of an echo event for the callee.</span></span> <span data-ttu-id="7a0d4-521">有关详细信息，请参阅 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-521">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-522">CalleeEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="7a0d4-522">CalleeEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-523">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-523">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-524">在被呼叫者的麦克风捕获流中检测到回显的时间百分比。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-524">Percentage of time when echo is detected in the callee’s microphone capture stream.</span></span> <span data-ttu-id="7a0d4-525">如果使用耳机，则该值应较低。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-525">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-526">CalleeEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="7a0d4-526">CalleeEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-527">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-527">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-528">在被调用方的发送流中检测到回显的时间的百分比。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-528">Percentage of time when echo is detected in the callee’s sent stream.</span></span> <span data-ttu-id="7a0d4-529">发送流中的高回显百分比表示回声泄漏。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-529">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-530">CalleeRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-530">CalleeRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-531">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-531">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-532">在中介服务器上从被呼叫方的音频的网关接收的信号级别;这仅适用于中介服务器。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-532">Received signal level on the Mediation Server from the Gateway for the callee’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="7a0d4-533">此指标的单位为 dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-533">The unit of this metric is dBoV.</span></span> <span data-ttu-id="7a0d4-534">为了获得良好的质量，可接受的范围应为 [-30 至-18] dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-534">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-535">CalleeRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="7a0d4-535">CalleeRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-536">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-536">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-537">在中介服务器上从被呼叫方的音频的网关接收的信号级别。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-537">Received signal level on the Mediation Server from the Gateway for the callee’s audio.</span></span> <span data-ttu-id="7a0d4-538">这仅适用于中介服务器。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-538">This applies only to the Mediation Server.</span></span> <span data-ttu-id="7a0d4-539">此指标的单位为 dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-539">The unit of this metric is dBoV.</span></span> <span data-ttu-id="7a0d4-540">为了获得优质，可接受范围应小于-50 dBoV。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-540">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-541">CalleeRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="7a0d4-541">CalleeRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-542">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-542">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-543"> (AGC) 的自动增益控制应用于被调用方的音频的中介服务器端。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-543">Automatic gain control (AGC) on the Mediation Server side applied to the callee’s audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-544">CalleeInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-544">CalleeInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-545">float</span><span class="sxs-lookup"><span data-stu-id="7a0d4-545">float</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-546">根平均值平方 (RMS 传入信号的 RMS) ，最多可拨出前30秒的呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-546">Root mean square (RMS) of the incoming signal to the callee for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-547">RatioConcealedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="7a0d4-547">RatioConcealedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-548">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-548">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-549">通过音频康复为典型示例生成的隐藏样本的平均比率。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-549">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-550">RatioStretchedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="7a0d4-550">RatioStretchedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-551">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-551">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-552">通过音频康复为典型示例生成的拉伸样本的平均比率。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-552">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-553">RatioCompressedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="7a0d4-553">RatioCompressedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-554">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-554">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-555">从音频修复到典型示例生成的压缩样本的平均比率。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-555">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-556">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="7a0d4-556">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-557">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-557">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-558">从 RTCP 统计数据往返的时间。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-558">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-559">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="7a0d4-559">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-560">int</span><span class="sxs-lookup"><span data-stu-id="7a0d4-560">int</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-561">音频流的最大往返行程时间。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-561">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-562">OverallAvgNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-562">OverallAvgNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-563">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-563">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-564">通话的平均宽带网络 MOS。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-564">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="7a0d4-565">此指标取决于所使用的数据包丢失、抖动和编解码器。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-565">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="7a0d4-566">范围为1.0 到5.0。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-566">Range is 1.0 to 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-567">OverallMinNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-567">OverallMinNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-568">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-568">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-569">通话最少宽带网络 MOS。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-569">Minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-570">SendListenMOS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-570">SendListenMOS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-571">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-571">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-572">平均预测宽带为已发送音频的 MOS 分数，包括语音级别、噪声级别和捕获设备特征。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-572">Average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-573">SendListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="7a0d4-573">SendListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-574">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-574">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-575">通话的最低 SendListenMOS。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-575">Minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-576">RecvListenMOS</span><span class="sxs-lookup"><span data-stu-id="7a0d4-576">RecvListenMOS</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-577">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-577">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-578">平均预测宽带从网络接收的音频的 MOS 分数，包括语音级别、噪音级别、编解码器、网络条件和捕获设备特征。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-578">Average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-579">RecvListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="7a0d4-579">RecvListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-580">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="7a0d4-580">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-581">通话的最低 RecvListenMOS。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-581">Minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a0d4-582">AudioFECUsed</span><span class="sxs-lookup"><span data-stu-id="7a0d4-582">AudioFECUsed</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-583">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-583">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-584">指示是否已将音频 FEC 用于呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-584">Indicates whether audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a0d4-585">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="7a0d4-585">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-586">bit</span><span class="sxs-lookup"><span data-stu-id="7a0d4-586">bit</span></span></p></td>
<td><p><span data-ttu-id="7a0d4-587">指示 p 声明的标识信息的方向;1表示流方向从调用方到被调用方;0表示流方向来自被调用方的调用方。</span><span class="sxs-lookup"><span data-stu-id="7a0d4-587">Indicates direction of the p-asserted identify information; 1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7a0d4-588">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a0d4-588">


</div>

<span> </span>

</div>

</div>

</span></span></div>

