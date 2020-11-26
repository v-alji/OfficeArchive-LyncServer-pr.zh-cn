---
title: Lync Server 2013： VideoMetricsThreshold 表
description: Lync Server 2013： VideoMetricsThreshold 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoMetricsThreshold table
ms:assetid: 2e2f4711-35ba-48c6-b15b-5aba61c4eb75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204778(v=OCS.15)
ms:contentKeyID: 48183736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 93cdd6fb4c3c54ac1470499490f36fee87ba283d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438867"
---
# <a name="videometricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="5a9ad-103">Lync Server 2013 中的 VideoMetricsThreshold 表</span><span class="sxs-lookup"><span data-stu-id="5a9ad-103">VideoMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a9ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a9ad-104">

<span> </span></span></span>

<span data-ttu-id="5a9ad-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5a9ad-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5a9ad-106">VideoMetricsThreshold 表包含用于视频通话的体验指标质量的最佳值和可接受值。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-106">The VideoMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a9ad-107"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="5a9ad-108"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="5a9ad-109"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="5a9ad-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-111"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-111"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-112">int</span><span class="sxs-lookup"><span data-stu-id="5a9ad-112">int</span></span></p></td>
<td><p><span data-ttu-id="5a9ad-113">Primary</span><span class="sxs-lookup"><span data-stu-id="5a9ad-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="5a9ad-114">所发出通话的类型。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-114">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-115"><strong>VideoPostFECPLROptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-115"><strong>VideoPostFECPLROptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-116">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-116">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-117">默认值为0.05。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-117">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-118"><strong>VideoPostFECPLRAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-118"><strong>VideoPostFECPLRAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-119">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-119">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-120">默认值为0.10。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-120">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-122">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-122">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-123">默认值为5.0。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-123">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-125">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-125">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-126">默认值为10.0。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-126">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-127"><strong>RecvFrameRateAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-127"><strong>RecvFrameRateAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-128">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-128">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-129">默认值为12.0000。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-129">The default value is 12.0000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-130"><strong>RecvFramerateAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-130"><strong>RecvFramerateAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-131">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-131">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-132">默认值为7.0000。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-132">The default value is 7.0000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-133"><strong>LowFrameRateCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-133"><strong>LowFrameRateCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-134">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-134">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-135">默认值为5.0。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-135">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-136"><strong>LowFrameRateCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-136"><strong>LowFrameRateCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-137">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-137">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-138">默认值为 10.0/</span><span class="sxs-lookup"><span data-stu-id="5a9ad-138">The default value is 10.0/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-139"><strong>LowResolutionCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-139"><strong>LowResolutionCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-140">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-140">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-141">默认值为5.0。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-141">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-142"><strong>LowResolutionCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-142"><strong>LowResolutionCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-143">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-143">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-144">默认值为10.0。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-144">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-145"><strong>VideoPacketLossRateOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-145"><strong>VideoPacketLossRateOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-146">foat</span><span class="sxs-lookup"><span data-stu-id="5a9ad-146">foat</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-147">默认值为0.05。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-147">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-148"><strong>VideoPacketLossRateAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-148"><strong>VideoPacketLossRateAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-149">float</span><span class="sxs-lookup"><span data-stu-id="5a9ad-149">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-150">默认值为0.10。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-150">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-151"><strong>VideoFrameRateAvgOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-151"><strong>VideoFrameRateAvgOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-152">float</span><span class="sxs-lookup"><span data-stu-id="5a9ad-152">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-153">默认值为12。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-153">The default value is 12.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-154"><strong>VideoFrameRateAvgAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-154"><strong>VideoFrameRateAvgAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-155">float</span><span class="sxs-lookup"><span data-stu-id="5a9ad-155">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-156">默认值为7。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-156">The default value is 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9ad-157"><strong>DynamicCapabilityPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-157"><strong>DynamicCapabilityPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-158">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-158">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-159">默认值为5.00。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-159">The default value is 5.00.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-160"><strong>DynamicCapabilityPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-160"><strong>DynamicCapabilityPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-161">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="5a9ad-161">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5a9ad-162">默认值为10.00。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-162">The default value is 10.00.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5a9ad-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a9ad-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

