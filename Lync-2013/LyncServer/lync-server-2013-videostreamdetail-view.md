---
title: Lync Server 2013： VideoStreamDetail 视图
description: Lync Server 2013： VideoStreamDetail 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443424"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="5723e-103">Lync Server 2013 中的 VideoStreamDetail 视图</span><span class="sxs-lookup"><span data-stu-id="5723e-103">VideoStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5723e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5723e-104">

<span> </span></span></span>

<span data-ttu-id="5723e-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="5723e-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="5723e-106">VideoStreamDetail 视图存储有关数据库中每个视频流的信息。</span><span class="sxs-lookup"><span data-stu-id="5723e-106">The VideoStreamDetail View stores information about each video stream in the database.</span></span> <span data-ttu-id="5723e-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="5723e-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5723e-108">列</span><span class="sxs-lookup"><span data-stu-id="5723e-108">Column</span></span></th>
<th><span data-ttu-id="5723e-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="5723e-109">Data Type</span></span></th>
<th><span data-ttu-id="5723e-110">说明</span><span class="sxs-lookup"><span data-stu-id="5723e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5723e-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="5723e-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="5723e-112">datetime</span><span class="sxs-lookup"><span data-stu-id="5723e-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="5723e-113">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="5723e-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="5723e-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="5723e-115">int</span><span class="sxs-lookup"><span data-stu-id="5723e-115">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-116">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="5723e-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-117">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="5723e-117">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="5723e-118">tinyint</span><span class="sxs-lookup"><span data-stu-id="5723e-118">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5723e-119">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="5723e-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-120">StreamId</span><span class="sxs-lookup"><span data-stu-id="5723e-120">StreamId</span></span></p></td>
<td><p><span data-ttu-id="5723e-121">int</span><span class="sxs-lookup"><span data-stu-id="5723e-121">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-122">媒体行内的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="5723e-122">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-123">StartTime</span><span class="sxs-lookup"><span data-stu-id="5723e-123">StartTime</span></span></p></td>
<td><p><span data-ttu-id="5723e-124">datetime</span><span class="sxs-lookup"><span data-stu-id="5723e-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="5723e-125">会话的开始时间。</span><span class="sxs-lookup"><span data-stu-id="5723e-125">Start time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-126">EndTime</span><span class="sxs-lookup"><span data-stu-id="5723e-126">EndTime</span></span></p></td>
<td><p><span data-ttu-id="5723e-127">datetime</span><span class="sxs-lookup"><span data-stu-id="5723e-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="5723e-128">会话的结束时间。</span><span class="sxs-lookup"><span data-stu-id="5723e-128">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-129">CallPriority</span><span class="sxs-lookup"><span data-stu-id="5723e-129">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="5723e-130">int</span><span class="sxs-lookup"><span data-stu-id="5723e-130">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-131">通话的优先级。</span><span class="sxs-lookup"><span data-stu-id="5723e-131">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-132">CallerPool</span><span class="sxs-lookup"><span data-stu-id="5723e-132">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="5723e-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5723e-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-134">呼叫方池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5723e-134">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-135">CalleePool</span><span class="sxs-lookup"><span data-stu-id="5723e-135">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="5723e-136">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5723e-136">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-137">被调用池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5723e-137">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-138">呼叫者</span><span class="sxs-lookup"><span data-stu-id="5723e-138">Caller</span></span></p></td>
<td><p><span data-ttu-id="5723e-139">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="5723e-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5723e-140">调用方的 URI。</span><span class="sxs-lookup"><span data-stu-id="5723e-140">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-141">被叫方</span><span class="sxs-lookup"><span data-stu-id="5723e-141">Callee</span></span></p></td>
<td><p><span data-ttu-id="5723e-142">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="5723e-142">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="5723e-143">被调用方的 URI。</span><span class="sxs-lookup"><span data-stu-id="5723e-143">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-144">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="5723e-144">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="5723e-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5723e-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-146">呼叫方的用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="5723e-146">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-147">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="5723e-147">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="5723e-148">smallint</span><span class="sxs-lookup"><span data-stu-id="5723e-148">smallint</span></span></p></td>
<td><p><span data-ttu-id="5723e-149">呼叫方的用户代理的类型。</span><span class="sxs-lookup"><span data-stu-id="5723e-149">Type of caller’s user agent.</span></span> <span data-ttu-id="5723e-150">有关详细信息，请参阅 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="5723e-150">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-151">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="5723e-151">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="5723e-152">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="5723e-152">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="5723e-153">呼叫者的用户代理类别。</span><span class="sxs-lookup"><span data-stu-id="5723e-153">Category of caller’s user agent.</span></span> <span data-ttu-id="5723e-154">有关详细信息，请参阅 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 中的 UserAgentDef 表 (QoE) </a> 。</span><span class="sxs-lookup"><span data-stu-id="5723e-154">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-155">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="5723e-155">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="5723e-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5723e-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-157">被呼叫方的用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="5723e-157">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-158">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="5723e-158">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="5723e-159">smallint</span><span class="sxs-lookup"><span data-stu-id="5723e-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="5723e-160">被调用方的用户代理的类型。</span><span class="sxs-lookup"><span data-stu-id="5723e-160">Type of callee’s user agent.</span></span> <span data-ttu-id="5723e-161">有关信息，请参阅 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="5723e-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-162">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="5723e-162">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="5723e-163">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="5723e-163">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="5723e-164">被呼叫方的用户代理类别。</span><span class="sxs-lookup"><span data-stu-id="5723e-164">Category of callee’s user agent.</span></span> <span data-ttu-id="5723e-165">有关信息，请参阅 <a href="lync-server-2013-useragentdef-table-qoe.md">Lync Server 2013 中的 UserAgentDef 表 (QoE) </a> 。</span><span class="sxs-lookup"><span data-stu-id="5723e-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-166">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5723e-166">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="5723e-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5723e-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-168">调用方的终结点名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-168">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-169">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="5723e-169">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="5723e-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="5723e-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-171">被调用方的终结点名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-171">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-172">CallerOS</span><span class="sxs-lookup"><span data-stu-id="5723e-172">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="5723e-173">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-173">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-174">呼叫方终结点 (操作系统) 的操作系统。</span><span class="sxs-lookup"><span data-stu-id="5723e-174">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-175">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="5723e-175">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="5723e-176">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-176">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-177">被调用方终结点的操作系统 (操作系统) 。</span><span class="sxs-lookup"><span data-stu-id="5723e-177">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-178">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="5723e-178">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="5723e-179">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-179">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-180">呼叫方终结点的 CPU 名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-180">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-181">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="5723e-181">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="5723e-182">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-182">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-183">被调用方终结点的 CPU 名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-183">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-184">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="5723e-184">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="5723e-185">smallint</span><span class="sxs-lookup"><span data-stu-id="5723e-185">smallint</span></span></p></td>
<td><p><span data-ttu-id="5723e-186">呼叫方终结点的 CPU 内核数。</span><span class="sxs-lookup"><span data-stu-id="5723e-186">Number of CPU cores of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-187">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="5723e-187">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="5723e-188">smallint</span><span class="sxs-lookup"><span data-stu-id="5723e-188">smallint</span></span></p></td>
<td><p><span data-ttu-id="5723e-189">被调用方终结点的 CPU 内核数。</span><span class="sxs-lookup"><span data-stu-id="5723e-189">Number of CPU cores of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-190">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="5723e-190">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="5723e-191">int</span><span class="sxs-lookup"><span data-stu-id="5723e-191">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-192">呼叫方终结点的 CPU 处理器速度。</span><span class="sxs-lookup"><span data-stu-id="5723e-192">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-193">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="5723e-193">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="5723e-194">int</span><span class="sxs-lookup"><span data-stu-id="5723e-194">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-195">被调用方终结点的 CPU 处理器速度。</span><span class="sxs-lookup"><span data-stu-id="5723e-195">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-196">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="5723e-196">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="5723e-197">tinyint</span><span class="sxs-lookup"><span data-stu-id="5723e-197">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5723e-198">指示呼叫者的系统是否在虚拟化环境中运行。</span><span class="sxs-lookup"><span data-stu-id="5723e-198">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="5723e-199">有关详细信息，请参阅 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 中的终结点表</a> 。</span><span class="sxs-lookup"><span data-stu-id="5723e-199">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-200">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="5723e-200">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="5723e-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="5723e-201">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5723e-202">指示被调用方的系统是否在虚拟化环境中运行。</span><span class="sxs-lookup"><span data-stu-id="5723e-202">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="5723e-203">有关详细信息，请参阅 <a href="lync-server-2013-endpoint-table.md">Lync Server 2013 中的终结点表</a> 。</span><span class="sxs-lookup"><span data-stu-id="5723e-203">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-204">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="5723e-204">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="5723e-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="5723e-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5723e-206">有关媒体路径（如直接或中继）的信息。</span><span class="sxs-lookup"><span data-stu-id="5723e-206">Information about media path, such as direct or relayed.</span></span> <span data-ttu-id="5723e-207">有关详细信息，请参阅 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="5723e-207">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-208">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="5723e-208">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="5723e-209">int</span><span class="sxs-lookup"><span data-stu-id="5723e-209">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-210">有关交互式连接的信息 (冰) 过程（在调用方的位标志中描述）。</span><span class="sxs-lookup"><span data-stu-id="5723e-210">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="5723e-211">有关详细信息，请参阅体验质量监视服务器协议规范。</span><span class="sxs-lookup"><span data-stu-id="5723e-211">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-212">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="5723e-212">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="5723e-213">int</span><span class="sxs-lookup"><span data-stu-id="5723e-213">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-214">有关交互式连接的信息 (冰) 进程（在被呼叫方的位标志中描述）。</span><span class="sxs-lookup"><span data-stu-id="5723e-214">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="5723e-215">有关详细信息，请参阅体验质量监视服务器协议规范。</span><span class="sxs-lookup"><span data-stu-id="5723e-215">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-216">Transport</span><span class="sxs-lookup"><span data-stu-id="5723e-216">Transport</span></span></p></td>
<td><p><span data-ttu-id="5723e-217">int</span><span class="sxs-lookup"><span data-stu-id="5723e-217">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-218">传输类型：0是 UDP，1是 TCP。</span><span class="sxs-lookup"><span data-stu-id="5723e-218">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-219">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="5723e-219">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="5723e-220">var (50) </span><span class="sxs-lookup"><span data-stu-id="5723e-220">var(50)</span></span></p></td>
<td><p><span data-ttu-id="5723e-221">呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="5723e-221">IP address of the caller.</span></span> <span data-ttu-id="5723e-222">这可能是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="5723e-222">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-223">CallerPort</span><span class="sxs-lookup"><span data-stu-id="5723e-223">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="5723e-224">int</span><span class="sxs-lookup"><span data-stu-id="5723e-224">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-225">呼叫方使用的端口。</span><span class="sxs-lookup"><span data-stu-id="5723e-225">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-226">CallerInside</span><span class="sxs-lookup"><span data-stu-id="5723e-226">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="5723e-227">bit</span><span class="sxs-lookup"><span data-stu-id="5723e-227">bit</span></span></p></td>
<td><p><span data-ttu-id="5723e-228">指示呼叫者是否在组织网络内。</span><span class="sxs-lookup"><span data-stu-id="5723e-228">Indicates whether the caller is inside the organization network.</span></span> <span data-ttu-id="5723e-229">1表示呼叫方位于企业网络内，0表示呼叫方位于网络外部。</span><span class="sxs-lookup"><span data-stu-id="5723e-229">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-230">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="5723e-230">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="5723e-231">var (50) </span><span class="sxs-lookup"><span data-stu-id="5723e-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="5723e-232">被呼叫方的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="5723e-232">IP address of the callee.</span></span> <span data-ttu-id="5723e-233">这可能是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="5723e-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-234">CalleePort</span><span class="sxs-lookup"><span data-stu-id="5723e-234">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="5723e-235">int</span><span class="sxs-lookup"><span data-stu-id="5723e-235">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-236">被呼叫方使用的端口。</span><span class="sxs-lookup"><span data-stu-id="5723e-236">Port used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-237">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="5723e-237">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="5723e-238">bit</span><span class="sxs-lookup"><span data-stu-id="5723e-238">bit</span></span></p></td>
<td><p><span data-ttu-id="5723e-239">指示呼叫者是否在组织网络内。1表示被呼叫方位于企业网络内，0表示被呼叫方在网络外部。</span><span class="sxs-lookup"><span data-stu-id="5723e-239">Indicates whether the caller is inside the organization network.1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-240">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="5723e-240">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="5723e-241">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-241">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-242">呼叫者站点的名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-242">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-243">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="5723e-243">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="5723e-244">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-244">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-245">呼叫方网站的国家/地区的名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-245">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-246">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="5723e-246">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="5723e-247">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-247">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-248">被调用方的网站的名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-248">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-249">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="5723e-249">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="5723e-250">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="5723e-250">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="5723e-251">被呼叫方网站的国家/地区的名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-251">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-252">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="5723e-252">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="5723e-253">var (50) </span><span class="sxs-lookup"><span data-stu-id="5723e-253">var(50)</span></span></p></td>
<td><p><span data-ttu-id="5723e-254">呼叫方使用的 A/V 边缘服务的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="5723e-254">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="5723e-255">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="5723e-255">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-256">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="5723e-256">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="5723e-257">int</span><span class="sxs-lookup"><span data-stu-id="5723e-257">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-258">呼叫方使用的 A/V 边缘服务上的端口。</span><span class="sxs-lookup"><span data-stu-id="5723e-258">Port on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-259">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="5723e-259">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="5723e-260">var (50) </span><span class="sxs-lookup"><span data-stu-id="5723e-260">var(50)</span></span></p></td>
<td><p><span data-ttu-id="5723e-261">被呼叫方使用的 A/V 边缘服务的 IP 地址密钥。</span><span class="sxs-lookup"><span data-stu-id="5723e-261">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="5723e-262">有关详细信息，请参阅 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 中</a> 的 "IPAddress" 表。</span><span class="sxs-lookup"><span data-stu-id="5723e-262">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-263">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="5723e-263">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="5723e-264">int</span><span class="sxs-lookup"><span data-stu-id="5723e-264">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-265">被呼叫方使用的 A/V 边缘服务上的端口。</span><span class="sxs-lookup"><span data-stu-id="5723e-265">Port on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-266">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="5723e-266">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="5723e-267">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-267">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-268">呼叫方的捕获设备名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-268">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-269">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="5723e-269">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="5723e-270">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-270">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-271">调用方的呈现设备名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-271">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-272">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="5723e-272">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="5723e-273">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-273">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-274">呼叫方的捕获设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-274">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-275">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="5723e-275">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="5723e-276">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-276">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-277">呼叫方的呈现设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-277">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-278">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="5723e-278">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="5723e-279">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-279">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-280">被调用方的捕获设备名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-280">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-281">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="5723e-281">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="5723e-282">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-282">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-283">被调用方的呈现设备名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-283">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-284">CalleCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="5723e-284">CalleCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="5723e-285">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-285">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-286">被调用方的捕获设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-286">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-287">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="5723e-287">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="5723e-288">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="5723e-288">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="5723e-289">被调用方的呈现设备驱动程序名称。</span><span class="sxs-lookup"><span data-stu-id="5723e-289">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-290">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="5723e-290">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="5723e-291">tinyint</span><span class="sxs-lookup"><span data-stu-id="5723e-291">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5723e-292">呼叫者的网络连接类型：0是 "有线"，1是 "无线"。</span><span class="sxs-lookup"><span data-stu-id="5723e-292">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-293">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="5723e-293">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="5723e-294">bit</span><span class="sxs-lookup"><span data-stu-id="5723e-294">bit</span></span></p></td>
<td><p><span data-ttu-id="5723e-295">指示呼叫者是否通过虚拟专用网络连接。</span><span class="sxs-lookup"><span data-stu-id="5723e-295">Indicates whether or not the caller connected over a virtual private network.</span></span> <span data-ttu-id="5723e-296">1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="5723e-296">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-297">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="5723e-297">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="5723e-298">十进制 (18，) </span><span class="sxs-lookup"><span data-stu-id="5723e-298">decimal(18,)</span></span></p></td>
<td><p><span data-ttu-id="5723e-299">呼叫方终结点的网络链接速度（以 bps 为实现）。</span><span class="sxs-lookup"><span data-stu-id="5723e-299">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-300">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="5723e-300">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="5723e-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="5723e-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5723e-302">被呼叫方的网络连接类型：0是 "有线"，1是 "无线"。</span><span class="sxs-lookup"><span data-stu-id="5723e-302">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-303">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="5723e-303">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="5723e-304">bit</span><span class="sxs-lookup"><span data-stu-id="5723e-304">bit</span></span></p></td>
<td><p><span data-ttu-id="5723e-305">指示被呼叫方是否通过虚拟专用网络进行连接。</span><span class="sxs-lookup"><span data-stu-id="5723e-305">Indicates whether or not the callee connected over a virtual private network.</span></span> <span data-ttu-id="5723e-306">1是虚拟专用网 (VPN) ，0是非 VPN。</span><span class="sxs-lookup"><span data-stu-id="5723e-306">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-307">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="5723e-307">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="5723e-308">十进制 (18，0) </span><span class="sxs-lookup"><span data-stu-id="5723e-308">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="5723e-309">被调用方终结点的网络链接速度 (bps) 。</span><span class="sxs-lookup"><span data-stu-id="5723e-309">Network link speed for the callee’s endpoint (in bps).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-310">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="5723e-310">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="5723e-311">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="5723e-311">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="5723e-312">Narrowband) 的音频 (会话的会话 MOS。</span><span class="sxs-lookup"><span data-stu-id="5723e-312">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-313">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="5723e-313">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="5723e-314">int</span><span class="sxs-lookup"><span data-stu-id="5723e-314">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-315">在给定各种策略设置 (、API、SDP、策略服务器等) 的情况下，应用到给定发送方流的实际带宽。</span><span class="sxs-lookup"><span data-stu-id="5723e-315">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="5723e-316">此操作不会与有效的带宽混淆，因为根据带宽估计，可能会有较低的有效带宽。</span><span class="sxs-lookup"><span data-stu-id="5723e-316">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="5723e-317">这基本上是发送流可以通过带宽估计限制限制的最大带宽。</span><span class="sxs-lookup"><span data-stu-id="5723e-317">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-318">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="5723e-318">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="5723e-319">int</span><span class="sxs-lookup"><span data-stu-id="5723e-319">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-320">实时控制协议 (RTCP) 统计信息的平均网络抖动。</span><span class="sxs-lookup"><span data-stu-id="5723e-320">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-321">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="5723e-321">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="5723e-322">int</span><span class="sxs-lookup"><span data-stu-id="5723e-322">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-323">通话期间网络抖动的最大值。</span><span class="sxs-lookup"><span data-stu-id="5723e-323">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-324">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="5723e-324">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="5723e-325">int</span><span class="sxs-lookup"><span data-stu-id="5723e-325">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-326">从 RTCP 统计数据往返的时间。</span><span class="sxs-lookup"><span data-stu-id="5723e-326">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-327">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="5723e-327">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="5723e-328">int</span><span class="sxs-lookup"><span data-stu-id="5723e-328">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-329">音频流的最大往返行程时间。</span><span class="sxs-lookup"><span data-stu-id="5723e-329">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-330">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="5723e-330">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="5723e-331">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="5723e-331">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="5723e-332">通话期间平均数据包丢失速率。</span><span class="sxs-lookup"><span data-stu-id="5723e-332">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-333">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="5723e-333">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="5723e-334">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="5723e-334">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="5723e-335">通话过程中观察到的最大数据包丢失。</span><span class="sxs-lookup"><span data-stu-id="5723e-335">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-336">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="5723e-336">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="5723e-337">int</span><span class="sxs-lookup"><span data-stu-id="5723e-337">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-338">视频流的数据包计数 (实时传输协议，RTP) 。</span><span class="sxs-lookup"><span data-stu-id="5723e-338">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-339">BandwidthEst</span><span class="sxs-lookup"><span data-stu-id="5723e-339">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="5723e-340">int</span><span class="sxs-lookup"><span data-stu-id="5723e-340">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-341">音频流的带宽估计。</span><span class="sxs-lookup"><span data-stu-id="5723e-341">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-342">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="5723e-342">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="5723e-343">int</span><span class="sxs-lookup"><span data-stu-id="5723e-343">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-344">用于呼叫的音频编解码器，从 <a href="lync-server-2013-payloaddescription-table.md">Lync Server 2013 中的 PayloadDescription 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="5723e-344">Audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-345">VideoResolution</span><span class="sxs-lookup"><span data-stu-id="5723e-345">VideoResolution</span></span></p></td>
<td><p><span data-ttu-id="5723e-346">char (9) </span><span class="sxs-lookup"><span data-stu-id="5723e-346">char(9)</span></span></p></td>
<td><p><span data-ttu-id="5723e-347">以像素为单位的视频分辨率（以像素为单位）乘以像素高度。</span><span class="sxs-lookup"><span data-stu-id="5723e-347">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="5723e-348">报告为字符串。</span><span class="sxs-lookup"><span data-stu-id="5723e-348">Reported as a string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-349">VideoBitRateAvg</span><span class="sxs-lookup"><span data-stu-id="5723e-349">VideoBitRateAvg</span></span></p></td>
<td><p><span data-ttu-id="5723e-350">int</span><span class="sxs-lookup"><span data-stu-id="5723e-350">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-351">视频流的平均比特率。</span><span class="sxs-lookup"><span data-stu-id="5723e-351">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-352">InboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="5723e-352">InboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="5723e-353">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="5723e-353">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="5723e-354">收到的视频的帧速率。</span><span class="sxs-lookup"><span data-stu-id="5723e-354">Frame rate of video received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-355">OutboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="5723e-355">OutboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="5723e-356">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="5723e-356">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="5723e-357">已发送视频的帧速率。</span><span class="sxs-lookup"><span data-stu-id="5723e-357">Frame rate of video sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-358">ViideoBitRateMax</span><span class="sxs-lookup"><span data-stu-id="5723e-358">ViideoBitRateMax</span></span></p></td>
<td><p><span data-ttu-id="5723e-359">int</span><span class="sxs-lookup"><span data-stu-id="5723e-359">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-360">视频会话期间的最大视频比特率。</span><span class="sxs-lookup"><span data-stu-id="5723e-360">Maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-361">VideoPacketLossRate</span><span class="sxs-lookup"><span data-stu-id="5723e-361">VideoPacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="5723e-362">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="5723e-362">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="5723e-363">视频数据包丢失的速率。</span><span class="sxs-lookup"><span data-stu-id="5723e-363">Rate at which video packets were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-364">VideoFrameLossRate</span><span class="sxs-lookup"><span data-stu-id="5723e-364">VideoFrameLossRate</span></span></p></td>
<td><p><span data-ttu-id="5723e-365">十进制 (9.4) </span><span class="sxs-lookup"><span data-stu-id="5723e-365">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="5723e-366">丢失的视频帧总数的百分比。</span><span class="sxs-lookup"><span data-stu-id="5723e-366">Percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-367">VideoFEC</span><span class="sxs-lookup"><span data-stu-id="5723e-367">VideoFEC</span></span></p></td>
<td><p><span data-ttu-id="5723e-368">bit</span><span class="sxs-lookup"><span data-stu-id="5723e-368">bit</span></span></p></td>
<td><p><span data-ttu-id="5723e-369">未使用。</span><span class="sxs-lookup"><span data-stu-id="5723e-369">Not used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-370">VideoAllocateBWAvg</span><span class="sxs-lookup"><span data-stu-id="5723e-370">VideoAllocateBWAvg</span></span></p></td>
<td><p><span data-ttu-id="5723e-371">int</span><span class="sxs-lookup"><span data-stu-id="5723e-371">int</span></span></p></td>
<td><p><span data-ttu-id="5723e-372">为视频分配的平均带宽量。</span><span class="sxs-lookup"><span data-stu-id="5723e-372">Average amount of bandwidth allocated for video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5723e-373">VideoLocalFrameLossPercentageAvg</span><span class="sxs-lookup"><span data-stu-id="5723e-373">VideoLocalFrameLossPercentageAvg</span></span></p></td>
<td><p><span data-ttu-id="5723e-374">十进制 (9.4) </span><span class="sxs-lookup"><span data-stu-id="5723e-374">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="5723e-375">丢失的视频帧总数的百分比。</span><span class="sxs-lookup"><span data-stu-id="5723e-375">Percentage of total video frames that were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5723e-376">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="5723e-376">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="5723e-377">bit</span><span class="sxs-lookup"><span data-stu-id="5723e-377">bit</span></span></p></td>
<td><p><span data-ttu-id="5723e-378">P 声明的标识信息的流方向。</span><span class="sxs-lookup"><span data-stu-id="5723e-378">Stream direction for p-asserted identity information.</span></span> <span data-ttu-id="5723e-379">1表示流方向从调用方到被调用方;0表示流方向来自被调用方的调用方。</span><span class="sxs-lookup"><span data-stu-id="5723e-379">1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5723e-380">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5723e-380">


</div>

<span> </span>

</div>

</div>

</span></span></div>

