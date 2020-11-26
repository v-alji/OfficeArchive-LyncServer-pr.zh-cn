---
title: Lync Server 2013：AudioSignal 表
description: Lync Server 2013： AudioSignal 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioSignal table
ms:assetid: 0013c8c6-cdf9-4d70-bc2a-cddd1560f66b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398064(v=OCS.15)
ms:contentKeyID: 48183217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82f3b3119eaccfe56c4706cff07469bc3434461f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438203"
---
# <a name="audiosignal-table-in-lync-server-2013"></a><span data-ttu-id="53a04-103">Lync Server 2013 中的 AudioSignal 表</span><span class="sxs-lookup"><span data-stu-id="53a04-103">AudioSignal table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="53a04-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="53a04-104">

<span> </span></span></span>

<span data-ttu-id="53a04-105">_**主题上次修改时间：** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="53a04-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="53a04-106">每条记录表示一个终结点的音频信号指标。</span><span class="sxs-lookup"><span data-stu-id="53a04-106">Each record represents audio signal metrics for one endpoint.</span></span> <span data-ttu-id="53a04-107">通常，每个通话都有两条记录，一个用于呼叫方，另一个用于被呼叫方。</span><span class="sxs-lookup"><span data-stu-id="53a04-107">Usually, each call has two records, one is for caller, and one is for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53a04-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="53a04-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="53a04-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="53a04-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53a04-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-113">datetime</span><span class="sxs-lookup"><span data-stu-id="53a04-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="53a04-114">Primary</span><span class="sxs-lookup"><span data-stu-id="53a04-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="53a04-115">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="53a04-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-117">int</span><span class="sxs-lookup"><span data-stu-id="53a04-117">int</span></span></p></td>
<td><p><span data-ttu-id="53a04-118">Primary</span><span class="sxs-lookup"><span data-stu-id="53a04-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="53a04-119">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="53a04-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="53a04-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="53a04-122">Primary</span><span class="sxs-lookup"><span data-stu-id="53a04-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="53a04-123">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="53a04-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-125">bit</span><span class="sxs-lookup"><span data-stu-id="53a04-125">bit</span></span></p></td>
<td><p><span data-ttu-id="53a04-126">Primary</span><span class="sxs-lookup"><span data-stu-id="53a04-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="53a04-127">0：被调用方的数据</span><span class="sxs-lookup"><span data-stu-id="53a04-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="53a04-128">1：调用方的数据</span><span class="sxs-lookup"><span data-stu-id="53a04-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-129"><strong>SendSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-129"><strong>SendSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-130">int</span><span class="sxs-lookup"><span data-stu-id="53a04-130">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-131">表示模拟后增益控制音频信号级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-131">Represents the Post-Analog Gain Control audio signal level.</span></span> <span data-ttu-id="53a04-132">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="53a04-132">The unit for this metric is dBmo.</span></span> <span data-ttu-id="53a04-133">为获得可接受的质量，它至少应为 30 dBmo。</span><span class="sxs-lookup"><span data-stu-id="53a04-133">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="53a04-134">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="53a04-134">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-135"><strong>RecvSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-135"><strong>RecvSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-136">int</span><span class="sxs-lookup"><span data-stu-id="53a04-136">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-137">请参阅 SendSignalLevel。</span><span class="sxs-lookup"><span data-stu-id="53a04-137">See SendSignalLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-138"><strong>SendNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-138"><strong>SendNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-139">int</span><span class="sxs-lookup"><span data-stu-id="53a04-139">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-140">表示模拟后增益控制音频噪声级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-140">Represents the Post-Analog Gain Control audio noise level.</span></span> <span data-ttu-id="53a04-141">此指标的单位为 dBmo。</span><span class="sxs-lookup"><span data-stu-id="53a04-141">The unit for this metric is dBmo.</span></span> <span data-ttu-id="53a04-142">为获得可接受的质量，它应小于 35 dBmo。</span><span class="sxs-lookup"><span data-stu-id="53a04-142">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="53a04-143">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="53a04-143">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-144"><strong>RecvNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-144"><strong>RecvNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-145">int</span><span class="sxs-lookup"><span data-stu-id="53a04-145">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-146">请参阅 SendNoiseLevel。</span><span class="sxs-lookup"><span data-stu-id="53a04-146">See SendNoiseLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-147"><strong>EchoReturn</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-147"><strong>EchoReturn</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-148">int</span><span class="sxs-lookup"><span data-stu-id="53a04-148">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-149">回音返回损失增强指标。</span><span class="sxs-lookup"><span data-stu-id="53a04-149">Echo Return Loss Enhancement metric.</span></span> <span data-ttu-id="53a04-150">此指标的单位为 dB。</span><span class="sxs-lookup"><span data-stu-id="53a04-150">The unit for this metric is dB.</span></span> <span data-ttu-id="53a04-151">较低的值表示较少的回声。</span><span class="sxs-lookup"><span data-stu-id="53a04-151">Lower values represent less echo.</span></span> <span data-ttu-id="53a04-152">A/V 会议服务器或 IP 电话不报告此指标。</span><span class="sxs-lookup"><span data-stu-id="53a04-152">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-153"><strong>AudioSpeakerGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-153"><strong>AudioSpeakerGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-154">int</span><span class="sxs-lookup"><span data-stu-id="53a04-154">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-155">扬声器呈现每五分钟的平均故障。</span><span class="sxs-lookup"><span data-stu-id="53a04-155">Average glitches per five minutes for the loudspeaker rendering.</span></span> <span data-ttu-id="53a04-156">为了获得良好的质量，这应该小于每五分钟一次。</span><span class="sxs-lookup"><span data-stu-id="53a04-156">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="53a04-157">不由 A/V 式会议服务器、中介服务器或 IP 电话报告。</span><span class="sxs-lookup"><span data-stu-id="53a04-157">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-158"><strong>AudioMicGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-158"><strong>AudioMicGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-159">int</span><span class="sxs-lookup"><span data-stu-id="53a04-159">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-160">麦克风捕获每五分钟的平均故障。</span><span class="sxs-lookup"><span data-stu-id="53a04-160">Average glitches per five minutes for the microphone capture.</span></span> <span data-ttu-id="53a04-161">为了获得良好的质量，这应该小于每五分钟一次。</span><span class="sxs-lookup"><span data-stu-id="53a04-161">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="53a04-162">不由 A/V 式会议服务器、中介服务器或 IP 电话报告。</span><span class="sxs-lookup"><span data-stu-id="53a04-162">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-163"><strong>AudioTimestampDriftRateMic</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-163"><strong>AudioTimestampDriftRateMic</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-164">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="53a04-164">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-165">麦克风设备时钟相对于 CPU 时钟的偏移速率。</span><span class="sxs-lookup"><span data-stu-id="53a04-165">Microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-166"><strong>AudioTimestampDriftRateSpk</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-166"><strong>AudioTimestampDriftRateSpk</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-167">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="53a04-167">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-168">扬声器设备时钟相对于 CPU 时钟的偏移速率。</span><span class="sxs-lookup"><span data-stu-id="53a04-168">Speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-169"><strong>AudioTimestampErrorMicMs</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-169"><strong>AudioTimestampErrorMicMs</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-170">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="53a04-170">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-171">扬声器设备时钟相对于 CPU 时钟的偏移速率。</span><span class="sxs-lookup"><span data-stu-id="53a04-171">Speaker device clock drift rate, relative to CPU clock.</span></span></p>
<p><span data-ttu-id="53a04-172">在呼叫的最后20秒内，麦克风捕获流时间戳的平均时间戳错误（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="53a04-172">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-173"><strong>AudioTimestampErrorSpkMs</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-173"><strong>AudioTimestampErrorSpkMs</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-174">十进制 (9，2) </span><span class="sxs-lookup"><span data-stu-id="53a04-174">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-175">在呼叫的最后20秒内，演讲者渲染流的时间戳错误（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="53a04-175">Average speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-176"><strong>VsEntryCauses</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-176"><strong>VsEntryCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-177">smallint</span><span class="sxs-lookup"><span data-stu-id="53a04-177">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-178">语音开关是一种具有更低中断能力的半双工模式。</span><span class="sxs-lookup"><span data-stu-id="53a04-178">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="53a04-179">语音切换条目的原因：</span><span class="sxs-lookup"><span data-stu-id="53a04-179">Causes of voice switch entry:</span></span></p>
<p><span data-ttu-id="53a04-180">ENTER_VS_BADTS 0x01</span><span class="sxs-lookup"><span data-stu-id="53a04-180">ENTER_VS_BADTS 0x01</span></span></p>
<p><span data-ttu-id="53a04-181">ENTER_VS_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="53a04-181">ENTER_VS_ECHO 0x02</span></span></p>
<p><span data-ttu-id="53a04-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span><span class="sxs-lookup"><span data-stu-id="53a04-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span></span></p>
<p><span data-ttu-id="53a04-183">ENTER_VS_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="53a04-183">ENTER_VS_DNLP 0x08</span></span></p>
<p><span data-ttu-id="53a04-184">原因可能是这些个别原因的组合。</span><span class="sxs-lookup"><span data-stu-id="53a04-184">The cause can be a combination of those individual causes.</span></span> <span data-ttu-id="53a04-185">只有注册用途的 regkey 才能启用 ENTER_VS_FORCEORCONVERGENCE。</span><span class="sxs-lookup"><span data-stu-id="53a04-185">ENTER_VS_FORCEORCONVERGENCE can only be enabled by regkey for test purpose.</span></span></p>
<p><span data-ttu-id="53a04-186">在 Microsoft Lync Server 2013 中，此列的数据类型已更改。</span><span class="sxs-lookup"><span data-stu-id="53a04-186">The data type for this column was changed in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-187"><strong>EchoEventCauses</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-187"><strong>EchoEventCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-188">tinyint</span><span class="sxs-lookup"><span data-stu-id="53a04-188">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-189">回声事件的原因：</span><span class="sxs-lookup"><span data-stu-id="53a04-189">Causes of an echo event:</span></span></p>
<p><span data-ttu-id="53a04-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span><span class="sxs-lookup"><span data-stu-id="53a04-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span></span></p>
<p><span data-ttu-id="53a04-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="53a04-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span></span></p>
<p><span data-ttu-id="53a04-192">ECHO_EVENT_ANLP 0x04</span><span class="sxs-lookup"><span data-stu-id="53a04-192">ECHO_EVENT_ANLP 0x04</span></span></p>
<p><span data-ttu-id="53a04-193">ECHO_EVENT_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="53a04-193">ECHO_EVENT_DNLP 0x08</span></span></p>
<p><span data-ttu-id="53a04-194">ECHO_EVENT_MIC_CLIPPING 0x10</span><span class="sxs-lookup"><span data-stu-id="53a04-194">ECHO_EVENT_MIC_CLIPPING 0x10</span></span></p>
<p><span data-ttu-id="53a04-195">ECHO_EVENT_BAD_STATE 0x20</span><span class="sxs-lookup"><span data-stu-id="53a04-195">ECHO_EVENT_BAD_STATE 0x20</span></span></p>
<p><span data-ttu-id="53a04-196">原因可能是这些个别原因的组合。</span><span class="sxs-lookup"><span data-stu-id="53a04-196">The cause can be a combination of those individual causes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-197"><strong>EchoPercentMicIn</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-197"><strong>EchoPercentMicIn</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-198">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="53a04-198">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-p109">在麦克风捕获流量中检测回声时的时间百分比。通常，对于耳机或话筒，值较低，而对于扬声器电话或独立扬声器，值较高。对于支持板载声学回声消除的设备，高值表示回声泄漏。对于其他设备，不应使用此指标评估设备质量。</span><span class="sxs-lookup"><span data-stu-id="53a04-p109">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-203"><strong>EchoPercentSend</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-203"><strong>EchoPercentSend</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-204">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="53a04-204">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-205">在发送流中检测到回显的时间百分比。</span><span class="sxs-lookup"><span data-stu-id="53a04-205">Percentage of time when echo is detected in sent stream.</span></span> <span data-ttu-id="53a04-206">发送流中的高回显百分比表示回声泄漏。</span><span class="sxs-lookup"><span data-stu-id="53a04-206">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-207"><strong>RxAGCSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-207"><strong>RxAGCSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-208">int</span><span class="sxs-lookup"><span data-stu-id="53a04-208">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-209">从网关在中介服务器上收到信号级别;这仅适用于中介服务器。</span><span class="sxs-lookup"><span data-stu-id="53a04-209">Received signal level on the Mediation Server from the Gateway; this applies only to the Mediation Server.</span></span> <span data-ttu-id="53a04-210">此指标的单位为 dBoV。</span><span class="sxs-lookup"><span data-stu-id="53a04-210">The unit of this metric is dBoV.</span></span> <span data-ttu-id="53a04-211">为了获得良好的质量，可接受的范围应为 [-30 至-18] dBoV。</span><span class="sxs-lookup"><span data-stu-id="53a04-211">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-212"><strong>RxAGCNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-212"><strong>RxAGCNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-213">int</span><span class="sxs-lookup"><span data-stu-id="53a04-213">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-214">从网关在中介服务器上接收信号级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-214">Received signal level on the Mediation Server from the Gateway.</span></span> <span data-ttu-id="53a04-215">这仅适用于中介服务器。</span><span class="sxs-lookup"><span data-stu-id="53a04-215">This applies only to the Mediation Server.</span></span> <span data-ttu-id="53a04-216">此指标的单位为 dBoV。</span><span class="sxs-lookup"><span data-stu-id="53a04-216">The unit of this metric is dBoV.</span></span> <span data-ttu-id="53a04-217">为了获得优质，可接受范围应小于-50 dBoV。</span><span class="sxs-lookup"><span data-stu-id="53a04-217">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-218"><strong>RxAvgAGCGain</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-218"><strong>RxAvgAGCGain</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-219">int</span><span class="sxs-lookup"><span data-stu-id="53a04-219">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-220">在中介服务器端 (AGC) 的自动增益控制。</span><span class="sxs-lookup"><span data-stu-id="53a04-220">Automatic gain control (AGC) on the Mediation Server side.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-221"><strong>InitialSignalLevelRMS</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-221"><strong>InitialSignalLevelRMS</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-222">float</span><span class="sxs-lookup"><span data-stu-id="53a04-222">float</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53a04-223">由呼叫的前30秒内的传入信号的 (RMS) 的根平均值。</span><span class="sxs-lookup"><span data-stu-id="53a04-223">The root mean square (RMS) of the incoming signal of up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-224"><strong>RecvSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-224"><strong>RecvSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-225">int</span><span class="sxs-lookup"><span data-stu-id="53a04-225">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-226">频道1上接收的信号级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-226">Signal level as received on channel 1.</span></span></p>
<p><span data-ttu-id="53a04-227">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-228"><strong>RecvSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-228"><strong>RecvSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-229">int</span><span class="sxs-lookup"><span data-stu-id="53a04-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-230">频道2上接收的信号级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-230">Signal level as received on channel 2.</span></span></p>
<p><span data-ttu-id="53a04-231">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-232"><strong>RecvNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-232"><strong>RecvNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-233">int</span><span class="sxs-lookup"><span data-stu-id="53a04-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-234">频道1上接收的噪音级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-234">Noise level as received on channel 1.</span></span></p>
<p><span data-ttu-id="53a04-235">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-236"><strong>RecvNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-236"><strong>RecvNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-237">int</span><span class="sxs-lookup"><span data-stu-id="53a04-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-238">频道2上接收的噪音级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-238">Noise level as received on channel 2.</span></span></p>
<p><span data-ttu-id="53a04-239">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-240"><strong>SendSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-240"><strong>SendSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-241">int</span><span class="sxs-lookup"><span data-stu-id="53a04-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-242">频道1上发送的信号级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-242">Signal level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="53a04-243">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-244"><strong>SendSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-244"><strong>SendSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-245">int</span><span class="sxs-lookup"><span data-stu-id="53a04-245">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-246">频道2上发送的信号级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-246">Signal level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="53a04-247">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53a04-248"><strong>SendNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-248"><strong>SendNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-249">int</span><span class="sxs-lookup"><span data-stu-id="53a04-249">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-250">频道1上发送的噪音级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-250">Noise level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="53a04-251">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-251">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53a04-252"><strong>SendNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="53a04-252"><strong>SendNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="53a04-253">int</span><span class="sxs-lookup"><span data-stu-id="53a04-253">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="53a04-254">频道2上发送的噪音级别。</span><span class="sxs-lookup"><span data-stu-id="53a04-254">Noise level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="53a04-255">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="53a04-255">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="53a04-256">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="53a04-256">


</div>

<span> </span>

</div>

</div>

</span></span></div>

