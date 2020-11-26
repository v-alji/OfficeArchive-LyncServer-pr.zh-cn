---
title: Lync Server 2013： AppSharingMetricsThreshold 表
description: Lync Server 2013： AppSharingMetricsThreshold 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439866"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="e9e64-103">Lync Server 2013 中的 AppSharingMetricsThreshold 表</span><span class="sxs-lookup"><span data-stu-id="e9e64-103">AppSharingMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9e64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9e64-104">

<span> </span></span></span>

<span data-ttu-id="e9e64-105">_**主题上次修改时间：** 2015-12-08_</span><span class="sxs-lookup"><span data-stu-id="e9e64-105">_**Topic Last Modified:** 2015-12-08_</span></span>

<span data-ttu-id="e9e64-106">AppSharingMetricsThreshold 表包含与应用程序共享一起使用的体验质量指标的最佳值和可接受值。</span><span class="sxs-lookup"><span data-stu-id="e9e64-106">The AppSharingMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span> <span data-ttu-id="e9e64-107">这些阈值用于确定应用程序共享体验是否应归类为较差。</span><span class="sxs-lookup"><span data-stu-id="e9e64-107">These thresholds are used to determine if the application sharing experience should be classified as poor.</span></span>

<span data-ttu-id="e9e64-108">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="e9e64-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9e64-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="e9e64-110"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="e9e64-111"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="e9e64-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-113"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-113"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-114">int</span><span class="sxs-lookup"><span data-stu-id="e9e64-114">int</span></span></p></td>
<td><p><span data-ttu-id="e9e64-115">Primary</span><span class="sxs-lookup"><span data-stu-id="e9e64-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="e9e64-116">所发出通话的类型。</span><span class="sxs-lookup"><span data-stu-id="e9e64-116">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9e64-117"><strong>AppliedBandwidthLimitOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-117"><strong>AppliedBandwidthLimitOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-118">int</span><span class="sxs-lookup"><span data-stu-id="e9e64-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-119">应用程序共享的最佳带宽限制。</span><span class="sxs-lookup"><span data-stu-id="e9e64-119">Optimal bandwidth limitation for application sharing.</span></span> <span data-ttu-id="e9e64-120">默认值为1000000。</span><span class="sxs-lookup"><span data-stu-id="e9e64-120">The default value is 1000000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-121"><strong>AppliedBandwidthLimitAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-121"><strong>AppliedBandwidthLimitAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-122">int</span><span class="sxs-lookup"><span data-stu-id="e9e64-122">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-123">应用程序共享的可接受带宽限制。</span><span class="sxs-lookup"><span data-stu-id="e9e64-123">Acceptable bandwidth limitation for application sharing.</span></span> <span data-ttu-id="e9e64-124">默认值为500000。</span><span class="sxs-lookup"><span data-stu-id="e9e64-124">The default value is 500000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9e64-125"><strong>SpoiledTilePercentTotalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-125"><strong>SpoiledTilePercentTotalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-126">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="e9e64-126">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-127">用于对应用程序共享质量进行分类的 "损坏" 图块的最佳百分比费率。</span><span class="sxs-lookup"><span data-stu-id="e9e64-127">Optimal percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="e9e64-128">此值表示来自共享者的未到达查看者的内容百分比。</span><span class="sxs-lookup"><span data-stu-id="e9e64-128">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="e9e64-129">当共享者从图形源或 ASMCU 中丢弃磁贴时，可能会放弃内容 (或损坏) 从共享内容中丢弃磁贴。</span><span class="sxs-lookup"><span data-stu-id="e9e64-129">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="e9e64-130">默认值为11%。</span><span class="sxs-lookup"><span data-stu-id="e9e64-130">The default value is 11 percent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-132">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="e9e64-132">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-133">用于对应用程序共享质量进行分类的 "损坏" 图块的 cceptable 百分比费率。</span><span class="sxs-lookup"><span data-stu-id="e9e64-133">cceptable percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="e9e64-134">此值表示来自共享者的未到达查看者的内容百分比。</span><span class="sxs-lookup"><span data-stu-id="e9e64-134">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="e9e64-135">当共享者从图形源或 ASMCU 中丢弃磁贴时，可能会放弃内容 (或损坏) 从共享内容中丢弃磁贴。</span><span class="sxs-lookup"><span data-stu-id="e9e64-135">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="e9e64-136">默认值为36%。</span><span class="sxs-lookup"><span data-stu-id="e9e64-136">The default value is 36 percent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9e64-137"><strong>JitterInterArrivalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-137"><strong>JitterInterArrivalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-138">int</span><span class="sxs-lookup"><span data-stu-id="e9e64-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-139">Microsoft Lync Server 2013 中不使用此列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-139">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-140"><strong>JitterInterArrivalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-140"><strong>JitterInterArrivalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-141">int</span><span class="sxs-lookup"><span data-stu-id="e9e64-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-142">Microsoft Lync Server 2013 中不使用此列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-142">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9e64-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-144">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-144">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-145">Microsoft Lync Server 2013 中不使用此列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-145">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-147">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-147">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-148">Microsoft Lync Server 2013 中不使用此列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-148">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9e64-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-150">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-150">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-151">Microsoft Lync Server 2013 中不使用此列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-151">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-153">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-153">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-154">Microsoft Lync Server 2013 中不使用此列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-154">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9e64-155"><strong>RelativeOneWayAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-155"><strong>RelativeOneWayAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-156">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-156">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-157">应用程序共享中涉及的两个媒体终结点之间的相对单向延迟的最佳值。</span><span class="sxs-lookup"><span data-stu-id="e9e64-157">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="e9e64-158">这是单跃点延迟度量。</span><span class="sxs-lookup"><span data-stu-id="e9e64-158">This is a single-hop latency measure.</span></span> <span data-ttu-id="e9e64-159">默认值为1.0 秒。</span><span class="sxs-lookup"><span data-stu-id="e9e64-159">The default value is 1.0 seconds.</span></span></p>
<p><span data-ttu-id="e9e64-160">在 Microsoft Lync Server 2013 中引入了该列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-160">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-161"><strong>RelativeOneWayAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-161"><strong>RelativeOneWayAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-162">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-162">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-163">应用程序共享中涉及的两个媒体终结点之间的相对单向延迟的最佳值。</span><span class="sxs-lookup"><span data-stu-id="e9e64-163">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="e9e64-164">这是单跃点延迟度量。</span><span class="sxs-lookup"><span data-stu-id="e9e64-164">This is a single-hop latency measure.</span></span> <span data-ttu-id="e9e64-165">默认值为1.75 秒。</span><span class="sxs-lookup"><span data-stu-id="e9e64-165">The default value is 1.75 seconds.</span></span></p>
<p><span data-ttu-id="e9e64-166">在 Microsoft Lync Server 2013 中引入了该列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-166">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9e64-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-168">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-168">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-169">在查看会话期间作为会议服务器中的平均 RDP 磁贴处理延迟的最佳值。</span><span class="sxs-lookup"><span data-stu-id="e9e64-169">Optimal value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="e9e64-170">滞后时间是在 (服务器上根据) 方案对启动帧进行编码的时间之间的时间差，并且在查看器上对同一开始帧进行解码。</span><span class="sxs-lookup"><span data-stu-id="e9e64-170">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="e9e64-171">高平均值反映了查看体验中的延迟较长。</span><span class="sxs-lookup"><span data-stu-id="e9e64-171">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="e9e64-172">过载的会议服务器可能会遇到更长的平均延迟。</span><span class="sxs-lookup"><span data-stu-id="e9e64-172">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="e9e64-173">默认值为200ms。</span><span class="sxs-lookup"><span data-stu-id="e9e64-173">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="e9e64-174">在 Microsoft Lync Server 2013 中引入了该列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-174">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9e64-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="e9e64-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="e9e64-176">float</span><span class="sxs-lookup"><span data-stu-id="e9e64-176">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e9e64-177">在查看会话期间作为会议服务器中的平均 RDP 磁贴处理延迟的可接受值。</span><span class="sxs-lookup"><span data-stu-id="e9e64-177">Acceptable value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="e9e64-178">滞后时间是在 (服务器上根据) 方案对启动帧进行编码的时间之间的时间差，并且在查看器上对同一开始帧进行解码。</span><span class="sxs-lookup"><span data-stu-id="e9e64-178">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="e9e64-179">高平均值反映了查看体验中的延迟较长。</span><span class="sxs-lookup"><span data-stu-id="e9e64-179">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="e9e64-180">过载的会议服务器可能会遇到更长的平均延迟。</span><span class="sxs-lookup"><span data-stu-id="e9e64-180">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="e9e64-181">默认值为200ms。</span><span class="sxs-lookup"><span data-stu-id="e9e64-181">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="e9e64-182">在 Microsoft Lync Server 2013 中引入了该列。</span><span class="sxs-lookup"><span data-stu-id="e9e64-182">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e9e64-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9e64-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

