---
title: Lync Server 2013：VideoStream 表
description: Lync Server 2013： VideoStream 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444124"
---
# <a name="videostream-table-in-lync-server-2013"></a><span data-ttu-id="67424-103">Lync Server 2013 中的 VideoStream 表</span><span class="sxs-lookup"><span data-stu-id="67424-103">VideoStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67424-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67424-104">

<span> </span></span></span>

<span data-ttu-id="67424-105">_**主题上次修改时间：** 2013-12-13_</span><span class="sxs-lookup"><span data-stu-id="67424-105">_**Topic Last Modified:** 2013-12-13_</span></span>

<span data-ttu-id="67424-106">每条记录表示一个视频流。</span><span class="sxs-lookup"><span data-stu-id="67424-106">Each record represents one video stream.</span></span> <span data-ttu-id="67424-107">一个视频媒体线通常包含两个视频流。</span><span class="sxs-lookup"><span data-stu-id="67424-107">One video media line usually contains two video streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67424-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="67424-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="67424-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="67424-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="67424-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="67424-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="67424-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="67424-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67424-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="67424-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-113">datetime</span><span class="sxs-lookup"><span data-stu-id="67424-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="67424-114">Primary</span><span class="sxs-lookup"><span data-stu-id="67424-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="67424-115">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="67424-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="67424-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-117">int</span><span class="sxs-lookup"><span data-stu-id="67424-117">int</span></span></p></td>
<td><p><span data-ttu-id="67424-118">Primary</span><span class="sxs-lookup"><span data-stu-id="67424-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="67424-119"><a href="lync-server-2013-medialine-table.md">在 Lync Server 2013 中从 MediaLine 表</a>引用的 R。</span><span class="sxs-lookup"><span data-stu-id="67424-119">R Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="67424-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="67424-122">Primary</span><span class="sxs-lookup"><span data-stu-id="67424-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="67424-123">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="67424-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-124"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="67424-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-125">int</span><span class="sxs-lookup"><span data-stu-id="67424-125">int</span></span></p></td>
<td><p><span data-ttu-id="67424-126">Primary</span><span class="sxs-lookup"><span data-stu-id="67424-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="67424-127">媒体行内的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="67424-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-128"><strong>VideoPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="67424-128"><strong>VideoPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-129">smallint</span><span class="sxs-lookup"><span data-stu-id="67424-129">smallint</span></span></p></td>
<td><p><span data-ttu-id="67424-130">外部、主要</span><span class="sxs-lookup"><span data-stu-id="67424-130">Foreign, Primary</span></span></p></td>
<td><p><span data-ttu-id="67424-131">负载说明。</span><span class="sxs-lookup"><span data-stu-id="67424-131">Payload description.</span></span> <span data-ttu-id="67424-132">有关详细信息，请参阅 <a href="lync-server-2013-payloaddescription-table.md">Lync Server 2013 中的 PayloadDescription 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="67424-132">See the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="67424-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-134">int</span><span class="sxs-lookup"><span data-stu-id="67424-134">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-135">实时控制协议 (RTCP) 统计信息的平均网络抖动。</span><span class="sxs-lookup"><span data-stu-id="67424-135">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-136"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-136"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-137">int</span><span class="sxs-lookup"><span data-stu-id="67424-137">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-138">视频会话期间的最大网络抖动。</span><span class="sxs-lookup"><span data-stu-id="67424-138">Maximum network jitter during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-139"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="67424-139"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-140">int</span><span class="sxs-lookup"><span data-stu-id="67424-140">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-141">从 RTCP 统计数据往返的时间。</span><span class="sxs-lookup"><span data-stu-id="67424-141">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-142"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-142"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-143">int</span><span class="sxs-lookup"><span data-stu-id="67424-143">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-144">视频流的最大往返行程时间。</span><span class="sxs-lookup"><span data-stu-id="67424-144">Maximum round trip time for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-145"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="67424-145"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-146">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="67424-146">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-147">通话期间平均数据包丢失速率。</span><span class="sxs-lookup"><span data-stu-id="67424-147">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-148"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-148"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-149">十进制 (5，4) </span><span class="sxs-lookup"><span data-stu-id="67424-149">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-150">通话过程中观察到的最大数据包丢失。</span><span class="sxs-lookup"><span data-stu-id="67424-150">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-151"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="67424-151"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-152">int</span><span class="sxs-lookup"><span data-stu-id="67424-152">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-153">视频流的数据包计数 (实时传输协议，RTP) 。</span><span class="sxs-lookup"><span data-stu-id="67424-153">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-154"><strong>BandwidthEst</strong></span><span class="sxs-lookup"><span data-stu-id="67424-154"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-155">int</span><span class="sxs-lookup"><span data-stu-id="67424-155">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-156">视频流的带宽估计。</span><span class="sxs-lookup"><span data-stu-id="67424-156">Bandwidth estimates for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-157"><strong>VideoResolution</strong></span><span class="sxs-lookup"><span data-stu-id="67424-157"><strong>VideoResolution</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-158">char (9) </span><span class="sxs-lookup"><span data-stu-id="67424-158">char(9)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-159">以像素为单位的视频分辨率（以像素为单位）乘以像素高度。</span><span class="sxs-lookup"><span data-stu-id="67424-159">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="67424-160">报告为字符串。</span><span class="sxs-lookup"><span data-stu-id="67424-160">Reported as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-161"><strong>VideoBitRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="67424-161"><strong>VideoBitRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-162">int</span><span class="sxs-lookup"><span data-stu-id="67424-162">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-163">视频流的平均比特率。</span><span class="sxs-lookup"><span data-stu-id="67424-163">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-164"><strong>InboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="67424-164"><strong>InboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-165">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="67424-165">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-166">收到的视频帧速率。</span><span class="sxs-lookup"><span data-stu-id="67424-166">The video frame rate received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-167"><strong>OutboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="67424-167"><strong>OutboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-168">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="67424-168">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-169">已发送视频帧速率。</span><span class="sxs-lookup"><span data-stu-id="67424-169">The video frame rate sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-170"><strong>VideoBitRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-170"><strong>VideoBitRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-171">int</span><span class="sxs-lookup"><span data-stu-id="67424-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-172">视频会话期间的最大视频比特率。</span><span class="sxs-lookup"><span data-stu-id="67424-172">The maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-173"><strong>VideoFrameLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="67424-173"><strong>VideoFrameLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-174">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="67424-174">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-175">丢失的视频帧总数的百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-175">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-176"><strong>VideoFEC</strong></span><span class="sxs-lookup"><span data-stu-id="67424-176"><strong>VideoFEC</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-177">bit</span><span class="sxs-lookup"><span data-stu-id="67424-177">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-178">不可用。</span><span class="sxs-lookup"><span data-stu-id="67424-178">Not available.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span><span class="sxs-lookup"><span data-stu-id="67424-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-180">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="67424-180">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-181">丢失的视频帧总数的百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-181">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-182"><strong>CIFQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-182"><strong>CIFQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-183">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-183">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-184">以常见交换格式 (的通话百分比 CIF) 分辨率。</span><span class="sxs-lookup"><span data-stu-id="67424-184">The percentage of the call that was at the Common Interchange Format (CIF) resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-185"><strong>VGAQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-185"><strong>VGAQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-186">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-186">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-187">以 VGA 分辨率表示的通话百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-187">The percentage of the call that was at VGA resolution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-188"><strong>HD720QualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-188"><strong>HD720QualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-189">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-190">以 HD720 分辨率表示的通话百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-190">The percentage of the call that was at HD720 resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-191"><strong>NoneDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-191"><strong>NoneDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-192">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-193">不带帧丢弃的通话持续时间百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-193">Percentage of call duration with no frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-194"><strong>BDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-194"><strong>BDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-195">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-195">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-196">B 帧丢弃的通话持续时间百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-196">Percentage of call duration with B frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-197"><strong>BPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-197"><strong>BPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-198">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-198">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-199">具有 BP 帧丢弃的通话持续百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-199">Percentage of call duration with BP frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-200"><strong>BPSPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-200"><strong>BPSPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-201">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-202">带有 BPSP 帧丢弃的通话持续时间百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-202">Percentage of call duration with BPSP frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-203"><strong>BPSPIDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="67424-203"><strong>BPSPIDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-204">tinyint</span><span class="sxs-lookup"><span data-stu-id="67424-204">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-205">带有 BPSPI 帧丢弃的通话持续时间百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-205">Percentage of call duration with BPSPI frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-206"><strong>封</strong></span><span class="sxs-lookup"><span data-stu-id="67424-206"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-207">bit</span><span class="sxs-lookup"><span data-stu-id="67424-207">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-208">接收接收方的数据流数据。</span><span class="sxs-lookup"><span data-stu-id="67424-208">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-209"><strong>出站</strong></span><span class="sxs-lookup"><span data-stu-id="67424-209"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-210">bit</span><span class="sxs-lookup"><span data-stu-id="67424-210">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-211">接收发件人端的数据流数据。</span><span class="sxs-lookup"><span data-stu-id="67424-211">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-212"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="67424-212"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-213">bit</span><span class="sxs-lookup"><span data-stu-id="67424-213">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="67424-214">1表示流方向来自调用方的调用方。</span><span class="sxs-lookup"><span data-stu-id="67424-214">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="67424-215">0表示流方向来自被调用方的调用方。</span><span class="sxs-lookup"><span data-stu-id="67424-215">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-216"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="67424-216"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-217">float</span><span class="sxs-lookup"><span data-stu-id="67424-217">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-218">指示通话处于损失拥塞状态的时间百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-218">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="67424-219">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-219">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-220"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="67424-220"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-221">float</span><span class="sxs-lookup"><span data-stu-id="67424-221">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-222">指示由于网络数据包的延迟到达而导致的阻塞的调用百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-222">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="67424-223">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-223">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-224"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="67424-224"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-225">float</span><span class="sxs-lookup"><span data-stu-id="67424-225">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-226">表示呼叫竞争网络资源的时间百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-226">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="67424-227">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-228"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="67424-228"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-229">int</span><span class="sxs-lookup"><span data-stu-id="67424-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-230">在通话期间测量的最小带宽估计量。</span><span class="sxs-lookup"><span data-stu-id="67424-230">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="67424-231">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-232"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-232"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-233">int</span><span class="sxs-lookup"><span data-stu-id="67424-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-234">在通话期间测量的最大带宽估计量。</span><span class="sxs-lookup"><span data-stu-id="67424-234">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="67424-235">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-236"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="67424-236"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-237">int</span><span class="sxs-lookup"><span data-stu-id="67424-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-238">在通话过程中测量的带宽估计的标准偏差。</span><span class="sxs-lookup"><span data-stu-id="67424-238">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="67424-239">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-240"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="67424-240"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-241">int</span><span class="sxs-lookup"><span data-stu-id="67424-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-242">通话期间测量的平均估计带宽量。</span><span class="sxs-lookup"><span data-stu-id="67424-242">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="67424-243">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-244"><strong>LowBandwidthForMultiview</strong></span><span class="sxs-lookup"><span data-stu-id="67424-244"><strong>LowBandwidthForMultiview</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-245">float</span><span class="sxs-lookup"><span data-stu-id="67424-245">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-246">终结点确定网络连接无法支持多种显示视频的调用的百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-246">Percentage of the call where the endpoint determined that the network connection could not support multiview video.</span></span></p>
<p><span data-ttu-id="67424-247">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-248"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="67424-248"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-249">float</span><span class="sxs-lookup"><span data-stu-id="67424-249">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-250">单向延迟的总金额。</span><span class="sxs-lookup"><span data-stu-id="67424-250">Total amount of one-way latency.</span></span> <span data-ttu-id="67424-251">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="67424-251">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-252">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-253"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="67424-253"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-254">float</span><span class="sxs-lookup"><span data-stu-id="67424-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-255">单向延迟的平均量。</span><span class="sxs-lookup"><span data-stu-id="67424-255">Average amount of one-way latency.</span></span> <span data-ttu-id="67424-256">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="67424-256">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-257">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-257">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-258"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-258"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-259">float</span><span class="sxs-lookup"><span data-stu-id="67424-259">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-260">单向延迟的最大值。</span><span class="sxs-lookup"><span data-stu-id="67424-260">Maximum amount of one-way latency.</span></span> <span data-ttu-id="67424-261">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="67424-261">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-262">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-262">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-263"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="67424-263"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-264">int</span><span class="sxs-lookup"><span data-stu-id="67424-264">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-265">总单向爆发次数。</span><span class="sxs-lookup"><span data-stu-id="67424-265">Total one-way burst occurrences.</span></span> <span data-ttu-id="67424-266">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="67424-266">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="67424-267">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="67424-267">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-268">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-269"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="67424-269"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-270">int</span><span class="sxs-lookup"><span data-stu-id="67424-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-271">总单向脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="67424-271">Total one-way burst density.</span></span> <span data-ttu-id="67424-272">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="67424-272">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="67424-273">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="67424-273">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-274">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-274">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-275"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="67424-275"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-276">float</span><span class="sxs-lookup"><span data-stu-id="67424-276">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-277">总的单向脉冲持续时间。</span><span class="sxs-lookup"><span data-stu-id="67424-277">Total one-way burst duration.</span></span> <span data-ttu-id="67424-278">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="67424-278">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="67424-279">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="67424-279">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-280">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-281"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="67424-281"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-282">int</span><span class="sxs-lookup"><span data-stu-id="67424-282">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-283">总的单向间隔发生次数。</span><span class="sxs-lookup"><span data-stu-id="67424-283">Total one-way gap occurrences.</span></span> <span data-ttu-id="67424-284">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="67424-284">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="67424-285">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="67424-285">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-286">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-286">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-287"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="67424-287"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-288">float</span><span class="sxs-lookup"><span data-stu-id="67424-288">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-289">总单向间距密度。</span><span class="sxs-lookup"><span data-stu-id="67424-289">Total one-way gap density.</span></span> <span data-ttu-id="67424-290">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="67424-290">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="67424-291">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="67424-291">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-292">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-292">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-293"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="67424-293"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-294">float</span><span class="sxs-lookup"><span data-stu-id="67424-294">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-295">总的单间隔持续时间。</span><span class="sxs-lookup"><span data-stu-id="67424-295">Total one-way gap duration.</span></span> <span data-ttu-id="67424-296">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="67424-296">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="67424-297">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="67424-297">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="67424-298">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-298">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-299"><strong>VideoPacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="67424-299"><strong>VideoPacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-300">十进制 (9，4) </span><span class="sxs-lookup"><span data-stu-id="67424-300">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-301">视频数据包丢失的速率。</span><span class="sxs-lookup"><span data-stu-id="67424-301">Rate at which video packets were lost.</span></span></p>
<p><span data-ttu-id="67424-302">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-302">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-303"><strong>VideoAllocateBWAvg</strong></span><span class="sxs-lookup"><span data-stu-id="67424-303"><strong>VideoAllocateBWAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-304">int</span><span class="sxs-lookup"><span data-stu-id="67424-304">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-305">为视频分配的平均带宽量。</span><span class="sxs-lookup"><span data-stu-id="67424-305">Average amount of bandwidth allocated for video.</span></span></p>
<p><span data-ttu-id="67424-306">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-306">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-307"><strong>SendCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="67424-307"><strong>SendCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-308">smallint</span><span class="sxs-lookup"><span data-stu-id="67424-308">smallint</span></span></p></td>
<td><p><span data-ttu-id="67424-309">外表</span><span class="sxs-lookup"><span data-stu-id="67424-309">Foreign</span></span></p></td>
<td><p><span data-ttu-id="67424-310">发件人使用的视频编解码器类型。</span><span class="sxs-lookup"><span data-stu-id="67424-310">Type of video codecs used by the sender.</span></span> <span data-ttu-id="67424-311">有关详细信息，请参阅 <a href="lync-server-2013-codecdescription-table.md">Lync Server 2013 中的 CodecDescription 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="67424-311">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="67424-312">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-312">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-313"><strong>SendResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="67424-313"><strong>SendResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-314">int</span><span class="sxs-lookup"><span data-stu-id="67424-314">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-315">发件人使用的分辨率宽度。</span><span class="sxs-lookup"><span data-stu-id="67424-315">Resolution width used by the sender.</span></span></p>
<p><span data-ttu-id="67424-316">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-316">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-317"><strong>SendResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="67424-317"><strong>SendResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-318">int</span><span class="sxs-lookup"><span data-stu-id="67424-318">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-319">发件人使用的分辨率高度。</span><span class="sxs-lookup"><span data-stu-id="67424-319">Resolution height used by the sender.</span></span></p>
<p><span data-ttu-id="67424-320">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-321"><strong>SendFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="67424-321"><strong>SendFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-322">float</span><span class="sxs-lookup"><span data-stu-id="67424-322">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-323">发件人使用的平均视频帧速率传输。</span><span class="sxs-lookup"><span data-stu-id="67424-323">Average video frame rate transmission used by the sender.</span></span></p>
<p><span data-ttu-id="67424-324">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-324">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-325"><strong>SendBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="67424-325"><strong>SendBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-326">int</span><span class="sxs-lookup"><span data-stu-id="67424-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-327">发件人的最大比特率。</span><span class="sxs-lookup"><span data-stu-id="67424-327">Maximum bit rate for the sender.</span></span></p>
<p><span data-ttu-id="67424-328">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-328">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-329"><strong>SendBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="67424-329"><strong>SendBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-330">int</span><span class="sxs-lookup"><span data-stu-id="67424-330">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-331">发件人的平均比特率。</span><span class="sxs-lookup"><span data-stu-id="67424-331">Average bit rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-332"><strong>SendVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-332"><strong>SendVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-333">int</span><span class="sxs-lookup"><span data-stu-id="67424-333">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-334">发件人使用的视频流的最大数量。</span><span class="sxs-lookup"><span data-stu-id="67424-334">Maximum number of video streams used by the sender.</span></span></p>
<p><span data-ttu-id="67424-335">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-336"><strong>RecvCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="67424-336"><strong>RecvCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-337">smallint</span><span class="sxs-lookup"><span data-stu-id="67424-337">smallint</span></span></p></td>
<td><p><span data-ttu-id="67424-338">外表</span><span class="sxs-lookup"><span data-stu-id="67424-338">Foreign</span></span></p></td>
<td><p><span data-ttu-id="67424-339">接收方使用的视频代码。</span><span class="sxs-lookup"><span data-stu-id="67424-339">Video codes used by the receiver.</span></span> <span data-ttu-id="67424-340">有关详细信息，请参阅 <a href="lync-server-2013-codecdescription-table.md">Lync Server 2013 中的 CodecDescription 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="67424-340">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="67424-341">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-342"><strong>RecvResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="67424-342"><strong>RecvResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-343">int</span><span class="sxs-lookup"><span data-stu-id="67424-343">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-344">接收器使用的分辨率宽度。</span><span class="sxs-lookup"><span data-stu-id="67424-344">Resolution width used by the receiver.</span></span></p>
<p><span data-ttu-id="67424-345">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-345">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-346"><strong>RecvResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="67424-346"><strong>RecvResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-347">int</span><span class="sxs-lookup"><span data-stu-id="67424-347">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-348">接收方使用的分辨率高度。</span><span class="sxs-lookup"><span data-stu-id="67424-348">Resolution height used by the receiver.</span></span></p>
<p><span data-ttu-id="67424-349">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-349">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-350"><strong>RecvFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="67424-350"><strong>RecvFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-351">float</span><span class="sxs-lookup"><span data-stu-id="67424-351">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-352">接收方使用的平均视频帧速率。</span><span class="sxs-lookup"><span data-stu-id="67424-352">Average video frame rate used by the receiver.</span></span></p>
<p><span data-ttu-id="67424-353">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-353">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-354"><strong>RecvBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="67424-354"><strong>RecvBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-355">int</span><span class="sxs-lookup"><span data-stu-id="67424-355">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-356">接收方的最大比特率。</span><span class="sxs-lookup"><span data-stu-id="67424-356">Maximum bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="67424-357">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-357">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-358"><strong>RecvBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="67424-358"><strong>RecvBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-359">int</span><span class="sxs-lookup"><span data-stu-id="67424-359">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-360">接收方的平均比特率。</span><span class="sxs-lookup"><span data-stu-id="67424-360">Average bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="67424-361">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-361">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-362"><strong>RecvVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="67424-362"><strong>RecvVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-363">int</span><span class="sxs-lookup"><span data-stu-id="67424-363">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-364">接收方的最大视频流。</span><span class="sxs-lookup"><span data-stu-id="67424-364">Maximum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="67424-365">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-365">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-366"><strong>RecvVideoStreamsMin</strong></span><span class="sxs-lookup"><span data-stu-id="67424-366"><strong>RecvVideoStreamsMin</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-367">int</span><span class="sxs-lookup"><span data-stu-id="67424-367">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-368">接收方的最小视频流。</span><span class="sxs-lookup"><span data-stu-id="67424-368">Minimum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="67424-369">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-369">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-370"><strong>RecvVideoStreamsMode</strong></span><span class="sxs-lookup"><span data-stu-id="67424-370"><strong>RecvVideoStreamsMode</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-371">int</span><span class="sxs-lookup"><span data-stu-id="67424-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-372">视频模式 (接收器的 "库" 或 "单流") 。</span><span class="sxs-lookup"><span data-stu-id="67424-372">Video mode (for example, gallery or single stream) for the receiver.</span></span></p>
<p><span data-ttu-id="67424-373">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-373">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-374"><strong>VideoPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="67424-374"><strong>VideoPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-375">float</span><span class="sxs-lookup"><span data-stu-id="67424-375">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-376">已应用转发纠错后的数据包丢失率。</span><span class="sxs-lookup"><span data-stu-id="67424-376">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="67424-377">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-377">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-378"><strong>DynamicCapabilityPercent</strong></span><span class="sxs-lookup"><span data-stu-id="67424-378"><strong>DynamicCapabilityPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-379">float</span><span class="sxs-lookup"><span data-stu-id="67424-379">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-380">动态功能标志处于活动状态的时间百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-380">Percentage of time that the dynamic capability flag was active.</span></span></p>
<p><span data-ttu-id="67424-381">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-381">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-382"><strong>ResolutionMin</strong></span><span class="sxs-lookup"><span data-stu-id="67424-382"><strong>ResolutionMin</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-383">char (9) </span><span class="sxs-lookup"><span data-stu-id="67424-383">char(9)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-384">通话过程中测量的最低分辨率。</span><span class="sxs-lookup"><span data-stu-id="67424-384">Minimum resolution measured during the call.</span></span></p>
<p><span data-ttu-id="67424-385">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-385">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-386"><strong>LowBitRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="67424-386"><strong>LowBitRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-387">float</span><span class="sxs-lookup"><span data-stu-id="67424-387">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-388">通话百分比低于低比特率阈值 (70 千位/秒) 。</span><span class="sxs-lookup"><span data-stu-id="67424-388">Percentage of the call below the low bit rate threshold (70 kilobits per second).</span></span></p>
<p><span data-ttu-id="67424-389">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-389">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-390"><strong>LowFrameRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="67424-390"><strong>LowFrameRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-391">float</span><span class="sxs-lookup"><span data-stu-id="67424-391">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-392">通话百分比低于低帧速率阈值 (7.5 帧每秒、入站) 。</span><span class="sxs-lookup"><span data-stu-id="67424-392">Percentage of the call below the low frame rate threshold (7.5 frames per second, inbound).</span></span></p>
<p><span data-ttu-id="67424-393">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-393">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-394"><strong>LowResolutionCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="67424-394"><strong>LowResolutionCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-395">float</span><span class="sxs-lookup"><span data-stu-id="67424-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-396">以最低分辨率发生的通话的百分比。</span><span class="sxs-lookup"><span data-stu-id="67424-396">Percentage of the call that occurred at the lowest resolution.</span></span></p>
<p><span data-ttu-id="67424-397">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-397">This column was introduced in Microsoft Lync Server 2013.</span></span></p>
<p><span data-ttu-id="67424-398">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-398">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67424-399"><strong>DurationSeconds</strong></span><span class="sxs-lookup"><span data-stu-id="67424-399"><strong>DurationSeconds</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-400">float</span><span class="sxs-lookup"><span data-stu-id="67424-400">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-401">通话长度（以秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="67424-401">Length of the call in seconds.</span></span></p>
<p><span data-ttu-id="67424-402">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-402">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67424-403"><strong>IsAggregatedData</strong></span><span class="sxs-lookup"><span data-stu-id="67424-403"><strong>IsAggregatedData</strong></span></span></p></td>
<td><p><span data-ttu-id="67424-404">bit</span><span class="sxs-lookup"><span data-stu-id="67424-404">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="67424-405">指示数据是否已从多个调用聚合。</span><span class="sxs-lookup"><span data-stu-id="67424-405">Indicates whether the data has been aggregated from multiple calls.</span></span></p>
<p><span data-ttu-id="67424-406">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="67424-406">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="67424-407">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67424-407">


</div>

<span> </span>

</div>

</div>

</span></span></div>

