---
title: Lync Server 2013：AudioStream 表
description: Lync Server 2013： AudioStream 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438174"
---
# <a name="audiostream-table-in-lync-server-2013"></a><span data-ttu-id="72626-103">Lync Server 2013 中的 AudioStream 表</span><span class="sxs-lookup"><span data-stu-id="72626-103">AudioStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72626-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72626-104">

<span> </span></span></span>

<span data-ttu-id="72626-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="72626-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="72626-106">每条记录表示一个音频流。</span><span class="sxs-lookup"><span data-stu-id="72626-106">Each record represents one audio stream.</span></span> <span data-ttu-id="72626-107">一个音频媒体行通常包含两个音频流。</span><span class="sxs-lookup"><span data-stu-id="72626-107">One audio media line usually contains two audio streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72626-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="72626-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="72626-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="72626-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="72626-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="72626-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="72626-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="72626-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72626-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="72626-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-113">datetime</span><span class="sxs-lookup"><span data-stu-id="72626-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="72626-114">Primary</span><span class="sxs-lookup"><span data-stu-id="72626-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="72626-115">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="72626-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="72626-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-117">int</span><span class="sxs-lookup"><span data-stu-id="72626-117">int</span></span></p></td>
<td><p><span data-ttu-id="72626-118">Primary</span><span class="sxs-lookup"><span data-stu-id="72626-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="72626-119">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="72626-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="72626-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="72626-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="72626-122">Primary</span><span class="sxs-lookup"><span data-stu-id="72626-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="72626-123">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="72626-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="72626-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-125">int</span><span class="sxs-lookup"><span data-stu-id="72626-125">int</span></span></p></td>
<td><p><span data-ttu-id="72626-126">Primary</span><span class="sxs-lookup"><span data-stu-id="72626-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="72626-127">媒体行内的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="72626-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-128"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="72626-128"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-129">int</span><span class="sxs-lookup"><span data-stu-id="72626-129">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-130">实时控制协议 (RTCP) 统计信息的平均网络抖动。</span><span class="sxs-lookup"><span data-stu-id="72626-130">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-131"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="72626-131"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-132">int</span><span class="sxs-lookup"><span data-stu-id="72626-132">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-133">通话期间网络抖动的最大值。</span><span class="sxs-lookup"><span data-stu-id="72626-133">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-134"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="72626-134"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-135">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="72626-135">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-136">通话期间平均数据包丢失速率。</span><span class="sxs-lookup"><span data-stu-id="72626-136">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-137"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="72626-137"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-138">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="72626-138">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-139">通话过程中观察到的最大数据包丢失。</span><span class="sxs-lookup"><span data-stu-id="72626-139">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-140"><strong>BurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="72626-140"><strong>BurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-141">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="72626-141">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-142">通话期间出现猝发损失期间的数据包丢失的平均密度。</span><span class="sxs-lookup"><span data-stu-id="72626-142">Average density of packet Loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-143"><strong>BurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="72626-143"><strong>BurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-144">int</span><span class="sxs-lookup"><span data-stu-id="72626-144">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-145">通话期间出现猝发损失期间的数据包丢失的平均持续时间。</span><span class="sxs-lookup"><span data-stu-id="72626-145">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-146"><strong>BurstGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="72626-146"><strong>BurstGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-147">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="72626-147">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-148">出现猝发数据包丢失之间的平均数据包损失的平均密度。</span><span class="sxs-lookup"><span data-stu-id="72626-148">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-149"><strong>BurstGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="72626-149"><strong>BurstGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-150">int</span><span class="sxs-lookup"><span data-stu-id="72626-150">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-151">爆发数据包损失之间的平均持续时间。</span><span class="sxs-lookup"><span data-stu-id="72626-151">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-152"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="72626-152"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-153">整形</span><span class="sxs-lookup"><span data-stu-id="72626-153">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-154">音频流的数据包计数。</span><span class="sxs-lookup"><span data-stu-id="72626-154">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-155"><strong>BandwidthEst</strong></span><span class="sxs-lookup"><span data-stu-id="72626-155"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-156">整形</span><span class="sxs-lookup"><span data-stu-id="72626-156">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-157">音频流的带宽估计。</span><span class="sxs-lookup"><span data-stu-id="72626-157">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-158"><strong>DegradationAvg</strong></span><span class="sxs-lookup"><span data-stu-id="72626-158"><strong>DegradationAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-159">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-159">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-160">整个通话的网络 MOS 降级。</span><span class="sxs-lookup"><span data-stu-id="72626-160">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="72626-161">范围为0.0 到5.0。</span><span class="sxs-lookup"><span data-stu-id="72626-161">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="72626-162">此指标显示由于抖动和数据包丢失，网络 MOS 的减少量。</span><span class="sxs-lookup"><span data-stu-id="72626-162">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="72626-163">对于可接受的质量，它应小于0.5。</span><span class="sxs-lookup"><span data-stu-id="72626-163">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-164"><strong>DegradationMax</strong></span><span class="sxs-lookup"><span data-stu-id="72626-164"><strong>DegradationMax</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-165">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-165">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-166">通话期间最大网络 MOS 性能下降。</span><span class="sxs-lookup"><span data-stu-id="72626-166">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-167"><strong>DegradationJitterAvg</strong></span><span class="sxs-lookup"><span data-stu-id="72626-167"><strong>DegradationJitterAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-168">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-168">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-169">由抖动导致的网络 MOS 性能下降。</span><span class="sxs-lookup"><span data-stu-id="72626-169">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-170"><strong>DegradationPacketLossAvg</strong></span><span class="sxs-lookup"><span data-stu-id="72626-170"><strong>DegradationPacketLossAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-171">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-171">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-172">由于数据包丢失导致网络 MOS 性能下降。</span><span class="sxs-lookup"><span data-stu-id="72626-172">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-173"><strong>AudioPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="72626-173"><strong>AudioPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-174">int</span><span class="sxs-lookup"><span data-stu-id="72626-174">int</span></span></p></td>
<td><p><span data-ttu-id="72626-175">外表</span><span class="sxs-lookup"><span data-stu-id="72626-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="72626-176">用于呼叫的音频编解码器，从 PayloadDescription 表中引用。</span><span class="sxs-lookup"><span data-stu-id="72626-176">The audio Codec used for the call, referenced from PayloadDescription Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-177"><strong>AudioSampleRate</strong></span><span class="sxs-lookup"><span data-stu-id="72626-177"><strong>AudioSampleRate</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-178">int</span><span class="sxs-lookup"><span data-stu-id="72626-178">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-179">音频流的采样率。</span><span class="sxs-lookup"><span data-stu-id="72626-179">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-180"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="72626-180"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-181">int</span><span class="sxs-lookup"><span data-stu-id="72626-181">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-182">从 RTCP 统计数据往返的时间。</span><span class="sxs-lookup"><span data-stu-id="72626-182">Round trip time from RTCP statistics.</span></span> <span data-ttu-id="72626-183">为获得可接受的质量，这应该小于100ms。</span><span class="sxs-lookup"><span data-stu-id="72626-183">For acceptable quality this should be less than 100ms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-184"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="72626-184"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-185">int</span><span class="sxs-lookup"><span data-stu-id="72626-185">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-186">音频流的最大往返行程时间。</span><span class="sxs-lookup"><span data-stu-id="72626-186">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-187"><strong>OverallAvgNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="72626-187"><strong>OverallAvgNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-188">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-188">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-189">通话的平均宽带网络 MOS。</span><span class="sxs-lookup"><span data-stu-id="72626-189">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="72626-190">此指标取决于所使用的数据包丢失、抖动和编解码器。</span><span class="sxs-lookup"><span data-stu-id="72626-190">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="72626-191">范围为 [1.0 到 5.0]。</span><span class="sxs-lookup"><span data-stu-id="72626-191">Range is [1.0 to 5.0].</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-192"><strong>OverallMinNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="72626-192"><strong>OverallMinNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-193">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-193">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-194">通话的最低宽带网络 MOS。</span><span class="sxs-lookup"><span data-stu-id="72626-194">The minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-195"><strong>SendListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="72626-195"><strong>SendListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-196">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-196">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-197">平均预测宽带的 MOS 分数，包括语音级别、噪声级别和捕获设备特征。</span><span class="sxs-lookup"><span data-stu-id="72626-197">The average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-198"><strong>SendListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="72626-198"><strong>SendListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-199">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-199">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-200">通话的最低 SendListenMOS。</span><span class="sxs-lookup"><span data-stu-id="72626-200">The minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-201"><strong>RecvListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="72626-201"><strong>RecvListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-202">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-202">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-203">平均预测宽带从网络接收的音频的 MOS 分数，包括语音级别、噪音级别、编解码器、网络条件和捕获设备特征。</span><span class="sxs-lookup"><span data-stu-id="72626-203">The average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-204"><strong>RecvListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="72626-204"><strong>RecvListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-205">十进制 (3，2) </span><span class="sxs-lookup"><span data-stu-id="72626-205">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-206">通话的最低 RecvListenMOS。</span><span class="sxs-lookup"><span data-stu-id="72626-206">The minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-207"><strong>AudioFECUsed</strong></span><span class="sxs-lookup"><span data-stu-id="72626-207"><strong>AudioFECUsed</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-208">bit</span><span class="sxs-lookup"><span data-stu-id="72626-208">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-209">指示是否已将音频 FEC 用于呼叫的标志。</span><span class="sxs-lookup"><span data-stu-id="72626-209">Flag indicating if audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-210"><strong>RatioConcealedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="72626-210"><strong>RatioConcealedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-211">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="72626-211">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-212">通过音频康复为典型示例生成的隐藏样本的平均比率。</span><span class="sxs-lookup"><span data-stu-id="72626-212">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-213"><strong>RatioStretchedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="72626-213"><strong>RatioStretchedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-214">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="72626-214">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-215">通过音频康复为典型示例生成的拉伸样本的平均比率。</span><span class="sxs-lookup"><span data-stu-id="72626-215">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-216"><strong>RatioCompressedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="72626-216"><strong>RatioCompressedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-217">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="72626-217">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-218">从音频修复到典型示例生成的压缩样本的平均比率。</span><span class="sxs-lookup"><span data-stu-id="72626-218">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-219"><strong>封</strong></span><span class="sxs-lookup"><span data-stu-id="72626-219"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-220">bit</span><span class="sxs-lookup"><span data-stu-id="72626-220">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-221">接收接收方的数据流数据。</span><span class="sxs-lookup"><span data-stu-id="72626-221">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-222"><strong>出站</strong></span><span class="sxs-lookup"><span data-stu-id="72626-222"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-223">bit</span><span class="sxs-lookup"><span data-stu-id="72626-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-224">接收发件人端的数据流数据。</span><span class="sxs-lookup"><span data-stu-id="72626-224">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-225"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="72626-225"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-226">bit</span><span class="sxs-lookup"><span data-stu-id="72626-226">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="72626-227">1表示流方向从调用方到被调用方。</span><span class="sxs-lookup"><span data-stu-id="72626-227">1 means the stream direction is from the caller to the callee.</span></span></p>
<p><span data-ttu-id="72626-228">0表示流方向来自被调用方的调用方。</span><span class="sxs-lookup"><span data-stu-id="72626-228">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-229"><strong>JitterInterArrivalSD</strong></span><span class="sxs-lookup"><span data-stu-id="72626-229"><strong>JitterInterArrivalSD</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-230">float</span><span class="sxs-lookup"><span data-stu-id="72626-230">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-231">抖动到达时间的标准偏差。</span><span class="sxs-lookup"><span data-stu-id="72626-231">Standard deviation for jitter arrival times.</span></span></p>
<p><span data-ttu-id="72626-232">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-232">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-233"><strong>ConcealRatioMax</strong></span><span class="sxs-lookup"><span data-stu-id="72626-233"><strong>ConcealRatioMax</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-234">float</span><span class="sxs-lookup"><span data-stu-id="72626-234">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-235">由 healer 隐藏的数据包的最大比率。</span><span class="sxs-lookup"><span data-stu-id="72626-235">Maximum ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="72626-236">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-236">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-237"><strong>ConcealRatioSD</strong></span><span class="sxs-lookup"><span data-stu-id="72626-237"><strong>ConcealRatioSD</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-238">float</span><span class="sxs-lookup"><span data-stu-id="72626-238">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-239">由 healer 隐藏的数据包比率的标准偏差。</span><span class="sxs-lookup"><span data-stu-id="72626-239">Standard deviation for the ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="72626-240">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-240">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-241"><strong>HealerPacketDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="72626-241"><strong>HealerPacketDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-242">float</span><span class="sxs-lookup"><span data-stu-id="72626-242">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-243">Healer 丢弃的数据包与接收的总数据包数之比。</span><span class="sxs-lookup"><span data-stu-id="72626-243">Ratio of packets dropped by the healer compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="72626-244">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-244">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-245"><strong>HealerFECPacketUsedRatio</strong></span><span class="sxs-lookup"><span data-stu-id="72626-245"><strong>HealerFECPacketUsedRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-246">float</span><span class="sxs-lookup"><span data-stu-id="72626-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-247">与接收的总数据包数相比已使用的转发纠错数据包的比率。</span><span class="sxs-lookup"><span data-stu-id="72626-247">Ratio of used forward error correction packets compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="72626-248">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-248">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-249"><strong>MaxCompressedSamples</strong></span><span class="sxs-lookup"><span data-stu-id="72626-249"><strong>MaxCompressedSamples</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-250">float</span><span class="sxs-lookup"><span data-stu-id="72626-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-251">由 healer 压缩的音频数据包的最大数量。</span><span class="sxs-lookup"><span data-stu-id="72626-251">Maximum number of audio packets that were compressed by the healer.</span></span></p>
<p><span data-ttu-id="72626-252">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-253"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="72626-253"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-254">float</span><span class="sxs-lookup"><span data-stu-id="72626-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-255">指示通话处于损失拥塞状态的时间百分比。</span><span class="sxs-lookup"><span data-stu-id="72626-255">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="72626-256">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-256">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-257"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="72626-257"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-258">float</span><span class="sxs-lookup"><span data-stu-id="72626-258">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-259">指示由于网络数据包的延迟到达而导致的阻塞的调用百分比。</span><span class="sxs-lookup"><span data-stu-id="72626-259">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="72626-260">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-260">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-261"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="72626-261"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-262">float</span><span class="sxs-lookup"><span data-stu-id="72626-262">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-263">表示呼叫竞争网络资源的时间百分比。</span><span class="sxs-lookup"><span data-stu-id="72626-263">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="72626-264">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-264">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-265"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="72626-265"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-266">int</span><span class="sxs-lookup"><span data-stu-id="72626-266">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-267">在通话期间测量的最小带宽估计量。</span><span class="sxs-lookup"><span data-stu-id="72626-267">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="72626-268">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-269"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="72626-269"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-270">int</span><span class="sxs-lookup"><span data-stu-id="72626-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-271">在通话期间测量的最大带宽估计量。</span><span class="sxs-lookup"><span data-stu-id="72626-271">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="72626-272">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-272">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-273"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="72626-273"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-274">int</span><span class="sxs-lookup"><span data-stu-id="72626-274">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-275">在通话过程中测量的带宽估计的标准偏差。</span><span class="sxs-lookup"><span data-stu-id="72626-275">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="72626-276">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-276">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-277"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="72626-277"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-278">int</span><span class="sxs-lookup"><span data-stu-id="72626-278">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-279">通话期间测量的平均估计带宽量。</span><span class="sxs-lookup"><span data-stu-id="72626-279">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="72626-280">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-281"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="72626-281"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-282">float</span><span class="sxs-lookup"><span data-stu-id="72626-282">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-283">单向延迟的总金额。</span><span class="sxs-lookup"><span data-stu-id="72626-283">Total amount of one-way latency.</span></span> <span data-ttu-id="72626-284">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="72626-284">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-285">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-285">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-286"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="72626-286"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-287">float</span><span class="sxs-lookup"><span data-stu-id="72626-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-288">单向延迟的平均量。</span><span class="sxs-lookup"><span data-stu-id="72626-288">Average amount of one-way latency.</span></span> <span data-ttu-id="72626-289">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="72626-289">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-290">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-290">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-291"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="72626-291"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-292">float</span><span class="sxs-lookup"><span data-stu-id="72626-292">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-293">单向延迟的最大值。</span><span class="sxs-lookup"><span data-stu-id="72626-293">Maximum amount of one-way latency.</span></span> <span data-ttu-id="72626-294">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="72626-294">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-295">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-295">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-296"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="72626-296"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-297">int</span><span class="sxs-lookup"><span data-stu-id="72626-297">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-298">总单向爆发次数。</span><span class="sxs-lookup"><span data-stu-id="72626-298">Total one-way burst occurrences.</span></span> <span data-ttu-id="72626-299">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="72626-299">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="72626-300">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="72626-300">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-301">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-302"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="72626-302"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-303">float</span><span class="sxs-lookup"><span data-stu-id="72626-303">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-304">总单向脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="72626-304">Total one-way burst density.</span></span> <span data-ttu-id="72626-305">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="72626-305">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="72626-306">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="72626-306">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-307">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-307">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-308"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="72626-308"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-309">float</span><span class="sxs-lookup"><span data-stu-id="72626-309">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-310">总的单向脉冲持续时间。</span><span class="sxs-lookup"><span data-stu-id="72626-310">Total one-way burst duration.</span></span> <span data-ttu-id="72626-311">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="72626-311">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="72626-312">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="72626-312">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-313">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-313">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-314"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="72626-314"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-315">int</span><span class="sxs-lookup"><span data-stu-id="72626-315">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-316">总的单向间隔发生次数。</span><span class="sxs-lookup"><span data-stu-id="72626-316">Total one-way gap occurrences.</span></span> <span data-ttu-id="72626-317">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="72626-317">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="72626-318">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="72626-318">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-319">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-319">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-320"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="72626-320"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-321">float</span><span class="sxs-lookup"><span data-stu-id="72626-321">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-322">总单向间距密度。</span><span class="sxs-lookup"><span data-stu-id="72626-322">Total one-way gap density.</span></span> <span data-ttu-id="72626-323">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="72626-323">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="72626-324">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="72626-324">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-325">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-326"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="72626-326"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-327">float</span><span class="sxs-lookup"><span data-stu-id="72626-327">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-328">总的单间隔持续时间。</span><span class="sxs-lookup"><span data-stu-id="72626-328">Total one-way gap duration.</span></span> <span data-ttu-id="72626-329">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="72626-329">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="72626-330">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="72626-330">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="72626-331">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-332"><strong>DecodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="72626-332"><strong>DecodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-333">float</span><span class="sxs-lookup"><span data-stu-id="72626-333">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-334">解码为立体声的通话百分比。</span><span class="sxs-lookup"><span data-stu-id="72626-334">Percentage of the call decoded as stereo.</span></span></p>
<p><span data-ttu-id="72626-335">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-336"><strong>AecRenderStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="72626-336"><strong>AecRenderStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-337">float</span><span class="sxs-lookup"><span data-stu-id="72626-337">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-338">通过音响回声抵消器呈现为立体声的通话百分比。</span><span class="sxs-lookup"><span data-stu-id="72626-338">Percentage of the call rendered as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="72626-339">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-339">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-340"><strong>AudioPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="72626-340"><strong>AudioPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-341">float</span><span class="sxs-lookup"><span data-stu-id="72626-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-342">已应用转发纠错后的数据包丢失率。</span><span class="sxs-lookup"><span data-stu-id="72626-342">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="72626-343">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-343">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72626-344"><strong>EncodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="72626-344"><strong>EncodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-345">float</span><span class="sxs-lookup"><span data-stu-id="72626-345">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-346">编码为立体声的通话百分比。</span><span class="sxs-lookup"><span data-stu-id="72626-346">Percentage of the call encoded as stereo.</span></span></p>
<p><span data-ttu-id="72626-347">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-347">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72626-348"><strong>AecCaptureStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="72626-348"><strong>AecCaptureStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="72626-349">float</span><span class="sxs-lookup"><span data-stu-id="72626-349">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="72626-350">通过音响回声抵消器以立体声形式捕获的通话百分比。</span><span class="sxs-lookup"><span data-stu-id="72626-350">Percentage of the call captured as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="72626-351">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="72626-351">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="72626-352">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72626-352">


</div>

<span> </span>

</div>

</div>

</span></span></div>

