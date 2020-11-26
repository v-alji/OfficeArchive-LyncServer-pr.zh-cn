---
title: Lync Server 2013：AudioClientEvent 表
description: Lync Server 2013： AudioClientEvent 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438204"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a><span data-ttu-id="ec4f1-103">Lync Server 2013 中的 AudioClientEvent 表</span><span class="sxs-lookup"><span data-stu-id="ec4f1-103">AudioClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec4f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec4f1-104">

<span> </span></span></span>

<span data-ttu-id="ec4f1-105">_**主题上次修改时间：** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="ec4f1-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="ec4f1-106">每条记录都包含音频呼叫中一个终结点的客户端事件。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-106">Each record contains a client event for one endpoint in an audio call.</span></span> <span data-ttu-id="ec4f1-107">通常，一个通话有两个记录，一个用于呼叫方，另一个用于被呼叫方。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec4f1-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ec4f1-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ec4f1-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ec4f1-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-113">datetime</span><span class="sxs-lookup"><span data-stu-id="ec4f1-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-114">Primary</span><span class="sxs-lookup"><span data-stu-id="ec4f1-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-115">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-117">int</span><span class="sxs-lookup"><span data-stu-id="ec4f1-117">int</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-118">Primary</span><span class="sxs-lookup"><span data-stu-id="ec4f1-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-119">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="ec4f1-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-122">Primary</span><span class="sxs-lookup"><span data-stu-id="ec4f1-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-123">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-125">bit</span><span class="sxs-lookup"><span data-stu-id="ec4f1-125">bit</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-126">Primary</span><span class="sxs-lookup"><span data-stu-id="ec4f1-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="ec4f1-127">0：被调用方的数据</span><span class="sxs-lookup"><span data-stu-id="ec4f1-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="ec4f1-128">1：调用方的数据</span><span class="sxs-lookup"><span data-stu-id="ec4f1-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-129"><strong>NetworkSendQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-129"><strong>NetworkSendQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-130">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-130">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-131">会话百分比为 "坏" 状态引发 NetworkSendQuality 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-131">Percentage of session the NetworkSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="ec4f1-132">"抖动" 或 "数据包丢失" 方面的网络质量非常严重，影响音频的质量。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-132">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-133"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-133"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-134">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-134">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-135">会话百分比为 "坏" 状态引发 ReceiveSendQuality 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-135">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="ec4f1-136">"抖动" 或 "数据包丢失" 方面的网络质量非常严重，影响了接收音频的质量。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-136">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-137"><strong>NetworkDelayEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-137"><strong>NetworkDelayEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-138">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-138">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-139">会话百分比延迟事件针对 "错误" 状态引发。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-139">Percentage of session the Delay event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-140">网络延迟非常严重，并通过阻止交互式通信影响体验</span><span class="sxs-lookup"><span data-stu-id="ec4f1-140">Network latency is severe and impacting the experience by preventing interactive communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-141"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-141"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-142">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-142">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-143">会话百分比为 "坏" 状态引发 LowBandwidth 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-143">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-144">可用带宽不足以获得可接受的语音体验。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-144">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-145"><strong>CPUInsufficientEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-145"><strong>CPUInsufficientEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-146">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-146">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-147">会话百分比为 "坏" 状态引发的 CPU 事件不足。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-147">Percentage of session the insufficient CPU event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-148">没有足够的 CPU 周期用于处理当前形式和正在使用的应用程序。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-148">There are insufficient CPU cycles for processing with the current modalities and applications in use.</span></span> <span data-ttu-id="ec4f1-149">这将导致音频通道出现扭曲。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-149">This causes distortions with the audio channel.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-151">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-151">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-152">会话百分比为 "坏" 状态引发 DeviceHalfDuplexAEC 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-152">Percentage of session the DeviceHalfDuplexAEC event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-153">为了防止回声，系统已输入半双工。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-153">In order to prevent echo, the system has enter half duplex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-155">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-155">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-156">会话百分比为 "坏" 状态引发 DeviceRenderNotFunctioning 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-156">Percentage of session the DeviceRenderNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-157">当前用于会话的渲染设备不能正常工作。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-157">The render device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="ec4f1-158">这可能会导致单向音频问题。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-158">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-160">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-160">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-161">会话百分比为 "坏" 状态引发 DeviceCaptureNotFunctioning 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-161">Percentage of session the DeviceCaptureNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-162">当前用于会话的捕获设备不能正常工作。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-162">The capture device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="ec4f1-163">这可能会导致单向音频问题。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-163">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-164"><strong>DeviceGlitchesEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-164"><strong>DeviceGlitchesEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-165">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-165">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-166">会话百分比为 "坏" 状态引发 DeviceGlitches 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-166">Percentage of session the DeviceGlitches event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-167">呈现导致扭曲的音频有严重的难题。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-167">There are severe glitches in the rendering of audio which is causing distortions.</span></span> <span data-ttu-id="ec4f1-168">这些故障可能是由驱动程序问题、延迟的过程调用 (DPC) 风暴 (驱动程序) 和 CPU 使用率较高导致的。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-168">These glitches can be caused by driver issues, deferred procedure calls (DPC) storm (drivers), and high CPU usage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-169"><strong>DeviceLowSNREventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-169"><strong>DeviceLowSNREventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-170">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-170">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-171">会话百分比为 "坏" 状态引发 DeviceLowSNR 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-171">Percentage of session the DeviceLowSNR event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-172">捕获质量非常差，很大噪音，或者用户距离麦克风太远。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-172">The capture quality is very poor, either very noisy or user is talking too far away from the microphone.</span></span> <span data-ttu-id="ec4f1-173">这将导致扭曲。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-173">This will cause distortions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-175">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-175">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-176">会话百分比为 "坏" 状态引发 DeviceLowSpeechLevel 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-176">Percentage of session the DeviceLowSpeechLevel event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-177">用户的语音级别太低，系统无法再进一步增加。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-177">User‘s speech level is too low and the system cannot increase it any further.</span></span> <span data-ttu-id="ec4f1-178">这可能会导致扭曲或视为单向音频。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-178">This can either cause distortions or perceived as one-way audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-179"><strong>DeviceClippingEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-179"><strong>DeviceClippingEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-180">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-180">Decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-181">会话百分比为 "坏" 状态引发 DeviceClipping 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-181">Percentage of session the DeviceClipping event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="ec4f1-182">近距离的语音剪辑时，麦克风的最大声音将因剪辑而被听到。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-182">When near-end speech clips the microphone, far-end hears distortion due to clipping.</span></span> <span data-ttu-id="ec4f1-183">避免接近结束的麦克风剪辑非常重要。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-183">It is important to avoid near-end microphone clipping.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-184"><strong>DeviceEchoEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-184"><strong>DeviceEchoEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-185">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-185">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-186">会话百分比为 "坏" 状态引发 DeviceEchoEvent 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-186">Percentage of session the DeviceEchoEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-187">设备或安装程序导致回声超出了系统进行补偿的能力。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-187">Device or setup is causing echo beyond the ability of the system to compensate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-189">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-189">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-190">会话百分比为 "坏" 状态引发 DeviceNearEndToEchoRatio 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-190">Percentage of session the DeviceNearEndToEchoRatio event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-191">与正在捕获的回显相比，用户的语音太低，这会影响用户体验，因为它限制了中断用户的难易程度。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-191">The user’s speech is too low compared to the echo being captured which impacts the users experience because it limits how easy it is to interrupt a user.</span></span> <span data-ttu-id="ec4f1-192">缩小扬声器音量，将麦克风移近讲话者。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-192">Reduce speaker volume, move the microphone closer to the talker.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-193"><strong>DeviceMultipleEndpointsEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-193"><strong>DeviceMultipleEndpointsEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-194">int</span><span class="sxs-lookup"><span data-stu-id="ec4f1-194">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ec4f1-195">会话期间的次数 DeviceMultipleEndpoints 事件针对 "错误" 状态引发。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-195">Number of times during session the DeviceMultipleEndpoints event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-196">检测到同一会话中有多个音频终结点，并且系统通过减少呈现音量进行了补偿。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-196">Multiple audio endpoints in the same session detected and the system has compensated by reducing render volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-197"><strong>DeviceHowlingEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-197"><strong>DeviceHowlingEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-198">int</span><span class="sxs-lookup"><span data-stu-id="ec4f1-198">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ec4f1-199">会话期间的次数 DeviceHowlingEvent 事件针对 "错误" 状态引发。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-199">Number of times during session the DeviceHowlingEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="ec4f1-200">检测到的音频反馈循环 (由多个终结点共享音频路径) 导致的。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-200">Audio feedback loop detected (caused by multiple endpoints sharing audio path).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec4f1-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-202">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-202">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ec4f1-203">触发 DeviceRenderZeroVolume 事件以处于 "错误" 状态的会话百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-203">Percentage of session the DeviceRenderZeroVolume event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="ec4f1-204">呈现设备已设置为零卷。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-204">The render device was set to zero volume.</span></span></p>
<p><span data-ttu-id="ec4f1-205">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-205">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec4f1-206"><strong>DeviceRenderMuteEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="ec4f1-206"><strong>DeviceRenderMuteEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4f1-207">十进制 (5，2) </span><span class="sxs-lookup"><span data-stu-id="ec4f1-207">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ec4f1-208">触发 DeviceRenderMute 事件以处于 "错误" 状态的会话百分比。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-208">Percentage of session the DeviceRenderMute event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="ec4f1-209">呈现设备已静音。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-209">The render device was muted.</span></span></p>
<p><span data-ttu-id="ec4f1-210">此列已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="ec4f1-210">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ec4f1-211">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec4f1-211">


</div>

<span> </span>

</div>

</div>

</span></span></div>

