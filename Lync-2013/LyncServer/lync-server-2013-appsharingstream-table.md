---
title: Lync Server 2013： AppSharingStream 表
description: Lync Server 2013： AppSharingStream 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingStream table
ms:assetid: 391490cb-d7b8-44ca-b4d1-429600da909c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204808(v=OCS.15)
ms:contentKeyID: 48183852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b530af5b489e090e5d0d00fbb01b2b950bafbe5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440554"
---
# <a name="appsharingstream-table-in-lync-server-2013"></a><span data-ttu-id="94278-103">Lync Server 2013 中的 AppSharingStream 表</span><span class="sxs-lookup"><span data-stu-id="94278-103">AppSharingStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="94278-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="94278-104">

<span> </span></span></span>

<span data-ttu-id="94278-105">_**主题上次修改时间：** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="94278-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="94278-106">AppSharingStream 表包含用于应用程序共享的网络流的体验指标的质量。</span><span class="sxs-lookup"><span data-stu-id="94278-106">The AppSharingStream table contains Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="94278-107">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="94278-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94278-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="94278-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="94278-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="94278-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="94278-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="94278-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="94278-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="94278-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94278-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="94278-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-113">从中</span><span class="sxs-lookup"><span data-stu-id="94278-113">dateTime</span></span></p></td>
<td><p><span data-ttu-id="94278-114">主、外部</span><span class="sxs-lookup"><span data-stu-id="94278-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="94278-115">会话开始的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="94278-115">Date and time that the session started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="94278-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-117">int</span><span class="sxs-lookup"><span data-stu-id="94278-117">int</span></span></p></td>
<td><p><span data-ttu-id="94278-118">主、外部</span><span class="sxs-lookup"><span data-stu-id="94278-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="94278-119">用于区分在同一日期和同一时间启动的会话的顺序标识符。</span><span class="sxs-lookup"><span data-stu-id="94278-119">Sequential identifier used to distinguish between sessions that started on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="94278-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="94278-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="94278-122">主、外部</span><span class="sxs-lookup"><span data-stu-id="94278-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="94278-123">表示通话中使用的视频线路类型。</span><span class="sxs-lookup"><span data-stu-id="94278-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="94278-124">允许的值包括：</span><span class="sxs-lookup"><span data-stu-id="94278-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="94278-125">0-音频</span><span class="sxs-lookup"><span data-stu-id="94278-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="94278-126">1-视频</span><span class="sxs-lookup"><span data-stu-id="94278-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="94278-127">2-全景视频</span><span class="sxs-lookup"><span data-stu-id="94278-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="94278-128">3-应用程序/桌面共享</span><span class="sxs-lookup"><span data-stu-id="94278-128">3 –Application/Desktop Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-129"><strong>StreamID</strong></span><span class="sxs-lookup"><span data-stu-id="94278-129"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-130">int</span><span class="sxs-lookup"><span data-stu-id="94278-130">int</span></span></p></td>
<td><p><span data-ttu-id="94278-131">Primary</span><span class="sxs-lookup"><span data-stu-id="94278-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="94278-132">应用程序共享流的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="94278-132">Unique identifier of the application sharing stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="94278-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-134">int</span><span class="sxs-lookup"><span data-stu-id="94278-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-135">在 RTP 数据包到达之间检测到的平均抖动率。</span><span class="sxs-lookup"><span data-stu-id="94278-135">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="94278-136"> (抖动是 shakiness 的测量值 &quot; &quot; 。 ) 高抖动值通常由拥挤或过载的媒体服务器引起，并导致失真或丢失的音频。</span><span class="sxs-lookup"><span data-stu-id="94278-136">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-137"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-137"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-138">int</span><span class="sxs-lookup"><span data-stu-id="94278-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-139">在 RTP 数据包到达之间检测到最大抖动。</span><span class="sxs-lookup"><span data-stu-id="94278-139">Maximum jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="94278-140"> (抖动是 shakiness 的测量值 &quot; &quot; 。 ) 高抖动值通常由拥挤或过载的媒体服务器引起，并导致失真或丢失的音频。</span><span class="sxs-lookup"><span data-stu-id="94278-140">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-141"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="94278-141"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-142">int</span><span class="sxs-lookup"><span data-stu-id="94278-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-p105">实时传输协议数据包来往于另一个终结点所需的平均时间量（以毫秒为单位）。来回行程的时间小于或等于 200 毫秒被视为质量可接受。</span><span class="sxs-lookup"><span data-stu-id="94278-p105">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="94278-p106">高来回行程时间值可能是由国际呼叫路由、路由配置错误或媒体服务器超载造成的，从而导致双向实时音频对话存在问题。</span><span class="sxs-lookup"><span data-stu-id="94278-p106">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-147"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-147"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-148">int</span><span class="sxs-lookup"><span data-stu-id="94278-148">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-149">将 Real-Time 传输协议数据包传送到另一个终结点，然后返回到另一个终结点所需的最大 (（以毫秒为单位）) 。</span><span class="sxs-lookup"><span data-stu-id="94278-149">Maximum amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back.</span></span> <span data-ttu-id="94278-150">来回行程的时间小于或等于 200 毫秒被视为质量可接受。</span><span class="sxs-lookup"><span data-stu-id="94278-150">Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="94278-p108">高来回行程时间值可能是由国际呼叫路由、路由配置错误或媒体服务器超载造成的，从而导致双向实时音频对话存在问题。</span><span class="sxs-lookup"><span data-stu-id="94278-p108">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-153"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="94278-153"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-154">float</span><span class="sxs-lookup"><span data-stu-id="94278-154">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-p109">平均实时传输协议 (RTP) 数据包丢失率。（当 RTP 数据包（一项用于在 Internet 中传输音频和视频的协议）无法到达其目标位置时，即发生数据包丢失。）高丢失率通常是由拥塞、带宽不足、无线拥塞/干扰或媒体服务器超载造成的。数据包丢失通常导致音频失真或丢失。</span><span class="sxs-lookup"><span data-stu-id="94278-p109">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-158"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-158"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-159">float</span><span class="sxs-lookup"><span data-stu-id="94278-159">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-160">Real-Time 传输协议 (RTP) 数据包丢失的最大速率。</span><span class="sxs-lookup"><span data-stu-id="94278-160">Maximum rate of Real-Time Transport Protocol (RTP) packet loss.</span></span> <span data-ttu-id="94278-161">当 RTP 数据包（用于在 Internet 上传输音频和视频的协议）无法访问目标时，将出现 (数据包丢失。 ) 高丢失率通常由拥塞引起;缺少带宽;无线拥挤或干扰;或重载的媒体服务器。</span><span class="sxs-lookup"><span data-stu-id="94278-161">(Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server.</span></span> <span data-ttu-id="94278-162">数据包丢失通常导致音频失真或丢失。</span><span class="sxs-lookup"><span data-stu-id="94278-162">Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-163"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="94278-163"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-164">int</span><span class="sxs-lookup"><span data-stu-id="94278-164">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-165">发送的数据包数。</span><span class="sxs-lookup"><span data-stu-id="94278-165">Number of packets sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-166"><strong>BandwidthEst</strong></span><span class="sxs-lookup"><span data-stu-id="94278-166"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-167">int</span><span class="sxs-lookup"><span data-stu-id="94278-167">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-168">在会话结束时可用的估计单向带宽。</span><span class="sxs-lookup"><span data-stu-id="94278-168">Estimated one-way bandwidth available at the end of the session.</span></span> <span data-ttu-id="94278-169">以位/秒为单位报告。</span><span class="sxs-lookup"><span data-stu-id="94278-169">Reported in bits per second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-170"><strong>AppSharingPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="94278-170"><strong>AppSharingPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-171">int</span><span class="sxs-lookup"><span data-stu-id="94278-171">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-172">应用程序共享负载的说明。</span><span class="sxs-lookup"><span data-stu-id="94278-172">Description of the application sharing payload.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-173"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-173"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-174">float</span><span class="sxs-lookup"><span data-stu-id="94278-174">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-175">单向延迟的总金额。</span><span class="sxs-lookup"><span data-stu-id="94278-175">Total amount of one-way latency.</span></span> <span data-ttu-id="94278-176">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-176">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-177"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-177"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-178">float</span><span class="sxs-lookup"><span data-stu-id="94278-178">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-179">单向延迟的平均量。</span><span class="sxs-lookup"><span data-stu-id="94278-179">Average amount of one-way latency.</span></span> <span data-ttu-id="94278-180">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-180">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-181"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-181"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-182">float</span><span class="sxs-lookup"><span data-stu-id="94278-182">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-183">单向延迟的最大值。</span><span class="sxs-lookup"><span data-stu-id="94278-183">Maximum amount of one-way latency.</span></span> <span data-ttu-id="94278-184">相对单向延迟测量客户端与服务器之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-184">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-185"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-185"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-186">int</span><span class="sxs-lookup"><span data-stu-id="94278-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-187">总单向爆发次数。</span><span class="sxs-lookup"><span data-stu-id="94278-187">Total one-way burst occurrences.</span></span> <span data-ttu-id="94278-188">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="94278-188">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="94278-189">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="94278-189">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-190"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-190"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-191">float</span><span class="sxs-lookup"><span data-stu-id="94278-191">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-192">总单向脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="94278-192">Total one-way burst density.</span></span> <span data-ttu-id="94278-193">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="94278-193">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="94278-194">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="94278-194">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-195"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-195"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-196">float</span><span class="sxs-lookup"><span data-stu-id="94278-196">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-197">总的单向脉冲持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-197">Total one-way burst duration.</span></span> <span data-ttu-id="94278-198">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="94278-198">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="94278-199">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="94278-199">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-200"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-200"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-201">int</span><span class="sxs-lookup"><span data-stu-id="94278-201">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-202">总的单向间隔发生次数。</span><span class="sxs-lookup"><span data-stu-id="94278-202">Total one-way gap occurrences.</span></span> <span data-ttu-id="94278-203">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-203">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="94278-204">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="94278-204">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-205"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-205"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-206">float</span><span class="sxs-lookup"><span data-stu-id="94278-206">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-207">总单向间距密度。</span><span class="sxs-lookup"><span data-stu-id="94278-207">Total one-way gap density.</span></span> <span data-ttu-id="94278-208">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-208">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="94278-209">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="94278-209">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-210"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-210"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-211">float</span><span class="sxs-lookup"><span data-stu-id="94278-211">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-212">总的单间隔持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-212">Total one-way gap duration.</span></span> <span data-ttu-id="94278-213">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，其数据流可预料的猝发。间隙表示这些猝发之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-213">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="94278-214">此指标测量客户端与服务器之间的数据流。</span><span class="sxs-lookup"><span data-stu-id="94278-214">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-215"><strong>ApplicationSharingType</strong></span><span class="sxs-lookup"><span data-stu-id="94278-215"><strong>ApplicationSharingType</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-216">varChar (256) </span><span class="sxs-lookup"><span data-stu-id="94278-216">varChar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-217"> (共享者或查看者) 和内容类型的应用程序角色。</span><span class="sxs-lookup"><span data-stu-id="94278-217">Application role (Sharer or Viewer) and content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-218"><strong>RDPTileProcessingLatencyTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-218"><strong>RDPTileProcessingLatencyTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-219">float</span><span class="sxs-lookup"><span data-stu-id="94278-219">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-220">远程桌面协议 (RDP) 磁贴的处理总时间。</span><span class="sxs-lookup"><span data-stu-id="94278-220">Total processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-221">较高的总计等于查看体验中较长的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-221">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-222"><strong>RDPTileProcessingLatencyAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-222"><strong>RDPTileProcessingLatencyAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-223">float</span><span class="sxs-lookup"><span data-stu-id="94278-223">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-224">远程桌面协议 (RDP) 磁贴的平均处理时间。</span><span class="sxs-lookup"><span data-stu-id="94278-224">Average processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-225">较高的总计等于查看体验中较长的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-225">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-226"><strong>RDPTileProcessingLatencyMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-226"><strong>RDPTileProcessingLatencyMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-227">float</span><span class="sxs-lookup"><span data-stu-id="94278-227">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-228">远程桌面协议 (RDP) 磁贴的最长处理时间。</span><span class="sxs-lookup"><span data-stu-id="94278-228">Maximum processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-229">较高的总计等于查看体验中较长的延迟。</span><span class="sxs-lookup"><span data-stu-id="94278-229">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-231">int</span><span class="sxs-lookup"><span data-stu-id="94278-231">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-232">远程桌面协议的处理时间中的爆发次数 (RDP) 磁贴。</span><span class="sxs-lookup"><span data-stu-id="94278-232">Burst occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-233">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="94278-233">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-235">float</span><span class="sxs-lookup"><span data-stu-id="94278-235">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-236">远程桌面协议的处理时间内的爆发密度 (RDP) 磁贴。</span><span class="sxs-lookup"><span data-stu-id="94278-236">Burst density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-237">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="94278-237">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-239">float</span><span class="sxs-lookup"><span data-stu-id="94278-239">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-240">远程桌面协议的处理时间内的爆发期 (RDP) 磁贴。</span><span class="sxs-lookup"><span data-stu-id="94278-240">Burst duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-241">"Bursty" 传输是一种传输方式，其中的数据流与稳定流相反，数据流处于不可预知的突发流量。</span><span class="sxs-lookup"><span data-stu-id="94278-241">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-243">int</span><span class="sxs-lookup"><span data-stu-id="94278-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-244">远程桌面协议的处理时间中的间隔发生次数 (RDP) 磁贴。</span><span class="sxs-lookup"><span data-stu-id="94278-244">Gap occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-246">float</span><span class="sxs-lookup"><span data-stu-id="94278-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-247">远程桌面协议的处理时间方面的差距密度 (RDP) 磁贴。</span><span class="sxs-lookup"><span data-stu-id="94278-247">Gap density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-248">低间隙密度相当于更好的观看体验。</span><span class="sxs-lookup"><span data-stu-id="94278-248">Low gap density equates to a better viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-250">float</span><span class="sxs-lookup"><span data-stu-id="94278-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-251">远程桌面协议的处理时间中的间隔持续时间 (RDP) 磁贴。</span><span class="sxs-lookup"><span data-stu-id="94278-251">Gap duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="94278-252">短间隙持续时间等于更好的观看体验。</span><span class="sxs-lookup"><span data-stu-id="94278-252">Short gap durations equate to a better viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-253"><strong>CaptureTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-253"><strong>CaptureTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-254">float</span><span class="sxs-lookup"><span data-stu-id="94278-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-255">捕获的磁贴的总速率 (以每秒平铺) 。</span><span class="sxs-lookup"><span data-stu-id="94278-255">Total rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-256"><strong>CaptureTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-256"><strong>CaptureTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-257">float</span><span class="sxs-lookup"><span data-stu-id="94278-257">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-258">捕获的磁贴的平均费率 (以每秒平铺) 。</span><span class="sxs-lookup"><span data-stu-id="94278-258">Average rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-259"><strong>CaptureTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-259"><strong>CaptureTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-260">float</span><span class="sxs-lookup"><span data-stu-id="94278-260">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-261">捕获的磁贴的最大速率 (以每秒平铺) 。</span><span class="sxs-lookup"><span data-stu-id="94278-261">Maximum rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-262"><strong>CaptureTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-262"><strong>CaptureTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-263">在 t</span><span class="sxs-lookup"><span data-stu-id="94278-263">in t</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-264">以每秒磁贴) 的捕获磁 (贴速率为单位的爆发次数。</span><span class="sxs-lookup"><span data-stu-id="94278-264">Burst occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-265"><strong>CaptureTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-265"><strong>CaptureTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-266">float</span><span class="sxs-lookup"><span data-stu-id="94278-266">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-267">以每秒磁贴)  (的捕获磁贴速率为单位的脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="94278-267">Burst density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-268"><strong>CaptureTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-268"><strong>CaptureTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-269">float</span><span class="sxs-lookup"><span data-stu-id="94278-269">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-270">以已捕获磁贴的速率为单位的脉冲持续时间 (每秒平铺) 。</span><span class="sxs-lookup"><span data-stu-id="94278-270">Burst duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-271"><strong>CaptureTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-271"><strong>CaptureTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-272">int</span><span class="sxs-lookup"><span data-stu-id="94278-272">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-273">在捕获磁贴的速率中，在每秒平铺) 中 (的间隔发生次数。</span><span class="sxs-lookup"><span data-stu-id="94278-273">Gap occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-274"><strong>CaptureTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-274"><strong>CaptureTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-275">float</span><span class="sxs-lookup"><span data-stu-id="94278-275">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-276">间距密度，以每秒平铺) 的形式 (捕获的磁贴。</span><span class="sxs-lookup"><span data-stu-id="94278-276">Gap density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-277"><strong>CaptureTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-277"><strong>CaptureTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-278">float</span><span class="sxs-lookup"><span data-stu-id="94278-278">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-279">间隙持续时间以捕获磁贴的速率为单位， (每秒平铺) 。</span><span class="sxs-lookup"><span data-stu-id="94278-279">Gap duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-280"><strong>SpoiledTilePercentTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-280"><strong>SpoiledTilePercentTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-281">float</span><span class="sxs-lookup"><span data-stu-id="94278-281">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-282">未到达查看器但已被新内容放弃和覆盖的内容的总百分比。</span><span class="sxs-lookup"><span data-stu-id="94278-282">Total percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-283"><strong>SpoiledTilePercentAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-283"><strong>SpoiledTilePercentAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-284">float</span><span class="sxs-lookup"><span data-stu-id="94278-284">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-285">未到达查看器但已被新内容放弃和覆盖的内容的平均百分比。</span><span class="sxs-lookup"><span data-stu-id="94278-285">Average percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-286"><strong>SpoiledTilePercentMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-286"><strong>SpoiledTilePercentMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-287">float</span><span class="sxs-lookup"><span data-stu-id="94278-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-288">未到达查看的内容的最大百分比，而是丢弃并被新内容覆盖。</span><span class="sxs-lookup"><span data-stu-id="94278-288">Maximum percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-290">int</span><span class="sxs-lookup"><span data-stu-id="94278-290">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-291">未到达查看器但已被新内容放弃和覆盖的内容的突发事件发生。</span><span class="sxs-lookup"><span data-stu-id="94278-291">Burst occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-292"><strong>SpoiledTilePercentBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-292"><strong>SpoiledTilePercentBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-293">float</span><span class="sxs-lookup"><span data-stu-id="94278-293">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-294">未到达查看器的内容的爆发密度，但已被新内容放弃和覆盖。</span><span class="sxs-lookup"><span data-stu-id="94278-294">Burst density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-295"><strong>SpoiledTilePercentBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-295"><strong>SpoiledTilePercentBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-296">float</span><span class="sxs-lookup"><span data-stu-id="94278-296">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-297">未到达查看器的内容的爆发期，而是丢弃并被新内容覆盖。</span><span class="sxs-lookup"><span data-stu-id="94278-297">Burst duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-298"><strong>SpoiledTilePercentGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-298"><strong>SpoiledTilePercentGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-299">int</span><span class="sxs-lookup"><span data-stu-id="94278-299">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-300">未到达查看器的内容的间隙出现次数，但已被新内容放弃和覆盖。</span><span class="sxs-lookup"><span data-stu-id="94278-300">Gap occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-301"><strong>SpoiledTilePercentGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-301"><strong>SpoiledTilePercentGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-302">float</span><span class="sxs-lookup"><span data-stu-id="94278-302">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-303">未到达查看器但已被新内容放弃和覆盖的内容的差距密度。</span><span class="sxs-lookup"><span data-stu-id="94278-303">Gap density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-304"><strong>SpoiledTilePercentGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-304"><strong>SpoiledTilePercentGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-305">float</span><span class="sxs-lookup"><span data-stu-id="94278-305">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-306">未到达查看器的内容的间距持续时间，但已被新内容放弃和覆盖。</span><span class="sxs-lookup"><span data-stu-id="94278-306">Gap duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-307"><strong>ScrapingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-307"><strong>ScrapingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-308">float</span><span class="sxs-lookup"><span data-stu-id="94278-308">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-309">从图形源 scraped 的总帧数。</span><span class="sxs-lookup"><span data-stu-id="94278-309">Total number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-310"><strong>ScrapingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-310"><strong>ScrapingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-311">float</span><span class="sxs-lookup"><span data-stu-id="94278-311">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-312">从图形源 scraped 的平均帧数。</span><span class="sxs-lookup"><span data-stu-id="94278-312">Average number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-313"><strong>ScrapingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-313"><strong>ScrapingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-314">float</span><span class="sxs-lookup"><span data-stu-id="94278-314">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-315">从图形源 scraped 的最大帧数。</span><span class="sxs-lookup"><span data-stu-id="94278-315">Maximum number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-317">int</span><span class="sxs-lookup"><span data-stu-id="94278-317">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-318">帧 scraped 中的爆发出现在图形源中。</span><span class="sxs-lookup"><span data-stu-id="94278-318">Burst occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-319"><strong>ScrapingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-319"><strong>ScrapingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-320">float</span><span class="sxs-lookup"><span data-stu-id="94278-320">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-321">来自图形源的帧 scraped 中的脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="94278-321">Burst density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-322"><strong>ScrapingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-322"><strong>ScrapingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-323">float</span><span class="sxs-lookup"><span data-stu-id="94278-323">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-324">帧 scraped 中的爆发持续时间（来自图形源）。</span><span class="sxs-lookup"><span data-stu-id="94278-324">Burst duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-325"><strong>ScrapingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-325"><strong>ScrapingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-326">int</span><span class="sxs-lookup"><span data-stu-id="94278-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-327">从图形源 scraped 的帧中的间隙出现次数。</span><span class="sxs-lookup"><span data-stu-id="94278-327">Gap occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-328"><strong>ScrapingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-328"><strong>ScrapingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-329">float</span><span class="sxs-lookup"><span data-stu-id="94278-329">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-330">从图形源 scraped 的帧中的间隙密度。</span><span class="sxs-lookup"><span data-stu-id="94278-330">Gap density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-331"><strong>ScrapingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-331"><strong>ScrapingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-332">float</span><span class="sxs-lookup"><span data-stu-id="94278-332">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-333">帧 scraped 中的间距持续时间从图形源开始。</span><span class="sxs-lookup"><span data-stu-id="94278-333">Gap duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-334"><strong>IncomingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-334"><strong>IncomingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-335">float</span><span class="sxs-lookup"><span data-stu-id="94278-335">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-336">由查看器接收的传入帧速率总数。</span><span class="sxs-lookup"><span data-stu-id="94278-336">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-337"><strong>IncomingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-337"><strong>IncomingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-338">float</span><span class="sxs-lookup"><span data-stu-id="94278-338">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-339">查看器接收的平均传入帧速率。</span><span class="sxs-lookup"><span data-stu-id="94278-339">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-340"><strong>IncomingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-340"><strong>IncomingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-341">float</span><span class="sxs-lookup"><span data-stu-id="94278-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-342">查看器接收到的最大传入磁贴速度。</span><span class="sxs-lookup"><span data-stu-id="94278-342">Maximum incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-343"><strong>IncomingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-343"><strong>IncomingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-344">int</span><span class="sxs-lookup"><span data-stu-id="94278-344">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-345">由查看器接收的传入磁贴速率中的爆发次数。</span><span class="sxs-lookup"><span data-stu-id="94278-345">Burst occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-346"><strong>IncomingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-346"><strong>IncomingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-347">float</span><span class="sxs-lookup"><span data-stu-id="94278-347">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-348">由查看器接收的传入磁贴速率中的脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="94278-348">Burst density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-349"><strong>IncomingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-349"><strong>IncomingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-350">float</span><span class="sxs-lookup"><span data-stu-id="94278-350">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-351">由查看器接收的传入磁贴速率中的脉冲持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-351">Burst duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-352"><strong>IncomingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-352"><strong>IncomingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-353">int</span><span class="sxs-lookup"><span data-stu-id="94278-353">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-354">由查看器接收的传入磁贴速率中的间隙出现次数。</span><span class="sxs-lookup"><span data-stu-id="94278-354">Gap occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-355"><strong>IncomingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-355"><strong>IncomingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-356">float</span><span class="sxs-lookup"><span data-stu-id="94278-356">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-357">由查看器接收的传入磁贴费率中的间隙密度。</span><span class="sxs-lookup"><span data-stu-id="94278-357">Gap density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-358"><strong>IncomingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-358"><strong>IncomingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-359">float</span><span class="sxs-lookup"><span data-stu-id="94278-359">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-360">由查看器接收的传入磁贴速率中的间隙持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-360">Gap duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-361"><strong>IncomingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-361"><strong>IncomingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-362">float</span><span class="sxs-lookup"><span data-stu-id="94278-362">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-363">由查看器接收的传入帧速率总数。</span><span class="sxs-lookup"><span data-stu-id="94278-363">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-364"><strong>IncomingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-364"><strong>IncomingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-365">float</span><span class="sxs-lookup"><span data-stu-id="94278-365">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-366">查看器接收的平均传入帧速率。</span><span class="sxs-lookup"><span data-stu-id="94278-366">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-367"><strong>IncomingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-367"><strong>IncomingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-368">float</span><span class="sxs-lookup"><span data-stu-id="94278-368">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-369">查看器接收到的最大传入帧速率。</span><span class="sxs-lookup"><span data-stu-id="94278-369">Maximum incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-370"><strong>IncomingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-370"><strong>IncomingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-371">int</span><span class="sxs-lookup"><span data-stu-id="94278-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-372">由查看器接收的传入帧速率中的爆发次数。</span><span class="sxs-lookup"><span data-stu-id="94278-372">Burst occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-373"><strong>IncomingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-373"><strong>IncomingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-374">float</span><span class="sxs-lookup"><span data-stu-id="94278-374">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-375">查看器接收的传入帧速率中的脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="94278-375">Burst density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-376"><strong>IncomingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-376"><strong>IncomingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-377">float</span><span class="sxs-lookup"><span data-stu-id="94278-377">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-378">按浏览器接收的传入帧速率中的爆发持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-378">Burst duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-379"><strong>IncomingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-379"><strong>IncomingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-380">int</span><span class="sxs-lookup"><span data-stu-id="94278-380">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-381">由查看器接收的传入帧速率中的间隙出现次数。</span><span class="sxs-lookup"><span data-stu-id="94278-381">Gap occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-382"><strong>IncomingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-382"><strong>IncomingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-383">float</span><span class="sxs-lookup"><span data-stu-id="94278-383">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-384">查看器接收的传入帧速率中的间隙密度。</span><span class="sxs-lookup"><span data-stu-id="94278-384">Gap density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-385"><strong>IncomingFrameRateDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-385"><strong>IncomingFrameRateDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-386">float</span><span class="sxs-lookup"><span data-stu-id="94278-386">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-387">按查看器接收的传入帧速率中的间隙持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-387">Gap duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-388"><strong>OutgoingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-388"><strong>OutgoingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-389">float</span><span class="sxs-lookup"><span data-stu-id="94278-389">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-390">发件人的传出磁贴总费率。</span><span class="sxs-lookup"><span data-stu-id="94278-390">Total outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-391"><strong>OutgoingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-391"><strong>OutgoingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-392">float</span><span class="sxs-lookup"><span data-stu-id="94278-392">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-393">发件人的平均传出磁贴速率。</span><span class="sxs-lookup"><span data-stu-id="94278-393">Average outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-394"><strong>OutgoingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-394"><strong>OutgoingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-395">float</span><span class="sxs-lookup"><span data-stu-id="94278-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-396">发件人的最大传出磁贴费率。</span><span class="sxs-lookup"><span data-stu-id="94278-396">Maximum outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-397"><strong>OutgoingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-397"><strong>OutgoingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-398">int</span><span class="sxs-lookup"><span data-stu-id="94278-398">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-399">发件人的传出磁贴速率中的爆发次数。</span><span class="sxs-lookup"><span data-stu-id="94278-399">Burst occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-400"><strong>OutgoingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-400"><strong>OutgoingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-401">float</span><span class="sxs-lookup"><span data-stu-id="94278-401">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-402">发件人的传出磁贴费率的脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="94278-402">Burst density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-403"><strong>OutgoingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-403"><strong>OutgoingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-404">float</span><span class="sxs-lookup"><span data-stu-id="94278-404">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-405">发件人的传出磁贴费率的爆发持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-405">Burst duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-406"><strong>OutgoingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-406"><strong>OutgoingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-407">int</span><span class="sxs-lookup"><span data-stu-id="94278-407">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-408">发件人的传出磁贴费率中的间隙发生次数。</span><span class="sxs-lookup"><span data-stu-id="94278-408">Gap occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-409"><strong>OutgoingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-409"><strong>OutgoingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-410">float</span><span class="sxs-lookup"><span data-stu-id="94278-410">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-411">发件人的传出磁贴费率的差距密度。</span><span class="sxs-lookup"><span data-stu-id="94278-411">Gap density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-412"><strong>OutgoingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-412"><strong>OutgoingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-413">float</span><span class="sxs-lookup"><span data-stu-id="94278-413">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-414">发件人的传出磁贴费率的差距持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-414">Gap duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-415"><strong>OutgoingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="94278-415"><strong>OutgoingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-416">float</span><span class="sxs-lookup"><span data-stu-id="94278-416">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-417">发件人的传出帧费率总数。</span><span class="sxs-lookup"><span data-stu-id="94278-417">Total outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-418"><strong>OutgoingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="94278-418"><strong>OutgoingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-419">float</span><span class="sxs-lookup"><span data-stu-id="94278-419">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-420">发件人的平均传出帧速率。</span><span class="sxs-lookup"><span data-stu-id="94278-420">average outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-421"><strong>OutgoingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="94278-421"><strong>OutgoingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-422">float</span><span class="sxs-lookup"><span data-stu-id="94278-422">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-423">发件人的最大传出帧速率。</span><span class="sxs-lookup"><span data-stu-id="94278-423">Maximum outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-425">int</span><span class="sxs-lookup"><span data-stu-id="94278-425">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-426">发件人的传出帧费率中出现爆发。</span><span class="sxs-lookup"><span data-stu-id="94278-426">Burst occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-427"><strong>OutgoingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-427"><strong>OutgoingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-428">float</span><span class="sxs-lookup"><span data-stu-id="94278-428">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-429">发件人的传出帧费率的脉冲密度。</span><span class="sxs-lookup"><span data-stu-id="94278-429">Burst density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-430"><strong>OutgoingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-430"><strong>OutgoingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-431">float</span><span class="sxs-lookup"><span data-stu-id="94278-431">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-432">发件人的传出帧费率中的爆发持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-432">Burst duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-433"><strong>OutgoingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="94278-433"><strong>OutgoingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-434">int</span><span class="sxs-lookup"><span data-stu-id="94278-434">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-435">发件人的传出帧费率中的间隙出现次数。</span><span class="sxs-lookup"><span data-stu-id="94278-435">Gap occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-436"><strong>OutgoingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="94278-436"><strong>OutgoingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-437">float</span><span class="sxs-lookup"><span data-stu-id="94278-437">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-438">发件人的传出帧费率中的间隙密度。</span><span class="sxs-lookup"><span data-stu-id="94278-438">Gap density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-439"><strong>OutgoingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="94278-439"><strong>OutgoingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-440">float</span><span class="sxs-lookup"><span data-stu-id="94278-440">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-441">发件人的传出帧费率中的差距持续时间。</span><span class="sxs-lookup"><span data-stu-id="94278-441">Gap duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-442"><strong>AverageRectangleHeight</strong></span><span class="sxs-lookup"><span data-stu-id="94278-442"><strong>AverageRectangleHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-443">int</span><span class="sxs-lookup"><span data-stu-id="94278-443">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-444">平均视频分辨率高度（以像素为单位）。</span><span class="sxs-lookup"><span data-stu-id="94278-444">Average video resolution height, in pixels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-445"><strong>AverageRectangleWidth</strong></span><span class="sxs-lookup"><span data-stu-id="94278-445"><strong>AverageRectangleWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-446">int</span><span class="sxs-lookup"><span data-stu-id="94278-446">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-447">平均视频分辨率宽度（以像素为单位）。</span><span class="sxs-lookup"><span data-stu-id="94278-447">Average video resolution width, in pixels.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-448"><strong>封</strong></span><span class="sxs-lookup"><span data-stu-id="94278-448"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-449">bit</span><span class="sxs-lookup"><span data-stu-id="94278-449">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-450">平均帧速率 (入站传输的每秒帧数) 。</span><span class="sxs-lookup"><span data-stu-id="94278-450">Average frame rate (in frames per second) for inbound transmissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94278-451"><strong>出站</strong></span><span class="sxs-lookup"><span data-stu-id="94278-451"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-452">bit</span><span class="sxs-lookup"><span data-stu-id="94278-452">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-453">平均帧速率 (在出站传输的每秒帧数) 。</span><span class="sxs-lookup"><span data-stu-id="94278-453">Average frame rate (in frames per second) for outbound transmissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94278-454"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="94278-454"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="94278-455">bit</span><span class="sxs-lookup"><span data-stu-id="94278-455">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="94278-456">1表示流方向来自调用方的调用方。</span><span class="sxs-lookup"><span data-stu-id="94278-456">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="94278-457">0表示流方向来自被调用方的调用方。</span><span class="sxs-lookup"><span data-stu-id="94278-457">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="94278-458">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="94278-458">


</div>

<span> </span>

</div>

</div>

</span></span></div>

