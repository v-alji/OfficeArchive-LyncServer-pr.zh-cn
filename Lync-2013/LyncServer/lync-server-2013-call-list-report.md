---
title: Lync Server 2013：通话清单报告
description: Lync Server 2013：通话清单报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call List Report
ms:assetid: 9739f9f0-7a37-4844-91d5-f089d2011013
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615020(v=OCS.15)
ms:contentKeyID: 48184921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5b08d4c5f3011facc9cd8d4f6b2800638f3cc896
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435752"
---
# <a name="call-list-report-in-lync-server-2013"></a><span data-ttu-id="f8e8d-103">Lync Server 2013 中的通话清单报告</span><span class="sxs-lookup"><span data-stu-id="f8e8d-103">Call List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8e8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8e8d-104">

<span> </span></span></span>

<span data-ttu-id="f8e8d-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="f8e8d-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="f8e8d-106">呼叫列表报告提供了针对您组织中发出和接收的单个呼叫的用户体验质量 (QoE) 指标。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-106">The Call List Report provides Quality of Experience (QoE) metrics for individual calls made and received in your organization.</span></span> <span data-ttu-id="f8e8d-107">请注意，报告的实际指标将取决于您访问呼叫列表报告的方式。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-107">Note that the actual metrics reported will depend on how you access the Call List report.</span></span> <span data-ttu-id="f8e8d-108">例如，如果从 [Lync Server 2013 中的设备报表](lync-server-2013-device-report.md)打开报表，你将看到以下指标，这些指标也会在设备报表上报告：</span><span class="sxs-lookup"><span data-stu-id="f8e8d-108">For example, if you open the report from the [Device Report in Lync Server 2013](lync-server-2013-device-report.md), you'll see metrics such as the following, metrics that are also reported on the Device Report:</span></span>

  - <span data-ttu-id="f8e8d-109">呼叫者的麦克风</span><span class="sxs-lookup"><span data-stu-id="f8e8d-109">Caller's microphone</span></span>

  - <span data-ttu-id="f8e8d-110">呼叫者的扬声器</span><span class="sxs-lookup"><span data-stu-id="f8e8d-110">Caller's speaker</span></span>

  - <span data-ttu-id="f8e8d-111">被叫方的麦克风</span><span class="sxs-lookup"><span data-stu-id="f8e8d-111">Callee's microphone</span></span>

  - <span data-ttu-id="f8e8d-112">被叫方的扬声器</span><span class="sxs-lookup"><span data-stu-id="f8e8d-112">Callee's speaker</span></span>

  - <span data-ttu-id="f8e8d-113">语音切换时间比率</span><span class="sxs-lookup"><span data-stu-id="f8e8d-113">Ratio of voice switch time</span></span>

<span data-ttu-id="f8e8d-114">但是，如果从 [Lync Server 2013 中](lync-server-2013-location-report.md)的 "位置" 报表打开 "通话清单" 报告，将看不到任何这些指标;相反，你将看到如下所示的指标：</span><span class="sxs-lookup"><span data-stu-id="f8e8d-114">However, if you open the Call List Report from the [Location Report in Lync Server 2013](lync-server-2013-location-report.md), you won't see any of those metrics; instead, you'll see metrics like these:</span></span>

  - <span data-ttu-id="f8e8d-115">来回行程（毫秒）</span><span class="sxs-lookup"><span data-stu-id="f8e8d-115">Round trip (ms)</span></span>

  - <span data-ttu-id="f8e8d-116">性能降低 (MOS)</span><span class="sxs-lookup"><span data-stu-id="f8e8d-116">Degradation (MOS)</span></span>

  - <span data-ttu-id="f8e8d-117">数据包丢失</span><span class="sxs-lookup"><span data-stu-id="f8e8d-117">Packet loss</span></span>

  - <span data-ttu-id="f8e8d-118">抖动（毫秒）</span><span class="sxs-lookup"><span data-stu-id="f8e8d-118">Jitter (ms)</span></span>

<span data-ttu-id="f8e8d-p102">这些是在位置报告上报告的指标。但是，您始终能够从呼叫列表报告中单击“详细信息”指标来提供任何呼叫的完整 QoE 信息。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p102">Those are the metrics reported on the Location Report. However, from the Call List Report you can always click the Detail metric to provide complete QoE information for any call.</span></span>

<div>

## <a name="accessing-the-call-list-report"></a><span data-ttu-id="f8e8d-121">访问呼叫列表报告</span><span class="sxs-lookup"><span data-stu-id="f8e8d-121">Accessing the Call List Report</span></span>

<span data-ttu-id="f8e8d-122">可从以下任一报告访问呼叫列表报告：</span><span class="sxs-lookup"><span data-stu-id="f8e8d-122">The Call List Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="f8e8d-123">[Lync Server 2013 中的位置报告](lync-server-2013-location-report.md) (单击 "呼叫音量" 或 "不良呼叫百分比跃点数") </span><span class="sxs-lookup"><span data-stu-id="f8e8d-123">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="f8e8d-124">[Lync Server 2013 中的设备报表](lync-server-2013-device-report.md) (单击 "呼叫音量" 或 "不良呼叫百分比跃点数") </span><span class="sxs-lookup"><span data-stu-id="f8e8d-124">The [Device Report in Lync Server 2013](lync-server-2013-device-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="f8e8d-125">[Lync Server 2013 中的 "媒体质量摘要" 报表](lync-server-2013-media-quality-summary-report.md) (单击 "呼叫音量" 或 "不良呼叫百分比跃点数") </span><span class="sxs-lookup"><span data-stu-id="f8e8d-125">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="f8e8d-126">[Lync server 2013 中的 "服务器性能" 报表](lync-server-2013-server-performance-report.md) (单击 "呼叫音量" 或 "不良呼叫百分比跃点数") </span><span class="sxs-lookup"><span data-stu-id="f8e8d-126">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

<span data-ttu-id="f8e8d-127">从通话列表报告中，您可以通过单击详细信息指标来访问 [Lync Server 2013 中的 "呼叫详细信息" 报告](lync-server-2013-call-detail-report.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-127">From within the Call List Report you can access the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) by clicking the Detail metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-list-report"></a><span data-ttu-id="f8e8d-128">最充分地利用呼叫列表报告</span><span class="sxs-lookup"><span data-stu-id="f8e8d-128">Making the Best Use of the Call List Report</span></span>

<span data-ttu-id="f8e8d-129">如果您记不住实际度量哪些呼叫列表报告指标（例如语音切换时间比率），请将鼠标指针悬停在指标标签的上方；这将显示一个工具提示，它为您简述了此指标。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-129">If you can't remember what some of the Call List Report metrics (such as Ratio voice switch time) actually measure, hold your mouse over the metric label; a tool tip will then appear giving you a brief description of the metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="f8e8d-130">筛选器</span><span class="sxs-lookup"><span data-stu-id="f8e8d-130">Filters</span></span>

<span data-ttu-id="f8e8d-p103">无。您无法筛选呼叫列表报告。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p103">None. You cannot filter the Call List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="f8e8d-133">指标</span><span class="sxs-lookup"><span data-stu-id="f8e8d-133">Metrics</span></span>

<span data-ttu-id="f8e8d-134">下表列出了呼叫列表报告中提供的有关每个呼叫的信息。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-134">The following table lists the information provided in the Call List Report for each call.</span></span>

### <a name="call-list-report-metrics"></a><span data-ttu-id="f8e8d-135">呼叫列表报告指标</span><span class="sxs-lookup"><span data-stu-id="f8e8d-135">Call List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8e8d-136">名称</span><span class="sxs-lookup"><span data-stu-id="f8e8d-136">Name</span></span></th>
<th><span data-ttu-id="f8e8d-137">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="f8e8d-137">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f8e8d-138">描述</span><span class="sxs-lookup"><span data-stu-id="f8e8d-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-139"><strong>详细信息</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-139"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-140">否</span><span class="sxs-lookup"><span data-stu-id="f8e8d-140">No</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-141">单击此项时，报告将显示有关呼叫的其他信息。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-141">When you click this item, the report shows additional information on the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e8d-142"><strong>呼叫者</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-142"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-143">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-143">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-144">发起呼叫的人的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-144">SIP address of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-145"><strong>被叫方</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-145"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-146">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-147">被呼叫的人的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-147">SIP address of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e8d-148"><strong>开始时间</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-148"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-149">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-149">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-150">呼叫开始的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-150">Date and time that the call started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-151"><strong>结束时间</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-151"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-152">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-152">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-153">呼叫结束的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-153">Date and time that the call ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e8d-154"><strong>呼叫者用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-154"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-155">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-155">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-156">发出呼叫的人的终结点使用的软件。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-156">Software used by the endpoint of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-157"><strong>被叫方用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-157"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-158">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-158">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-159">被呼叫的人的终结点使用的软件。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-159">Software used by the endpoint of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e8d-160"><strong>来回行程（毫秒）</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-160"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-161">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-161">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-p104">实时传输协议 (RTP) 数据包来往于另一个终结点所需的平均时间量（以毫秒为单位）。来回行程的时间小于或等于 100 毫秒被视为质量可接受。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p104">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="f8e8d-p105">高来回行程时间值可能是由国际呼叫路由、路由配置错误或媒体服务器超载造成的，从而导致双向实时音频对话存在问题。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p105">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-166"><strong>性能降低 (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-166"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-167">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-167">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-168">呼叫过程中遇到的性能降低的平均意见得分 (MOS) 的平均值。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-168">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="f8e8d-169">性能降低值的范围介于 0.0 和 5.0 之间。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-169">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="f8e8d-170">该值小于或等于 0.5 表示可接受的性能降低。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-170">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="f8e8d-171">过去，平均意见得分是通过让用户对呼叫质量进行评级（范围为 1 到 5）来计算得出的。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-171">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="f8e8d-172">在 Lync Server 中，Lync Server 使用一组算法来预测用户对呼叫进行评分的方式。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-172">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="f8e8d-p107">高性能降低值可能是由拥塞、带宽不足、无线拥塞/干扰或媒体服务器或终结点超载造成的，从而导致音频失真或丢失。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p107">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e8d-175"><strong>数据包丢失</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-175"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-176">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-p108">平均 RTP 数据包丢失率。（当 RTP 数据包（一项用于在 Internet 中传输音频和视频的协议）无法到达其目标位置时将发生数据包丢失。）高丢失率通常是由拥塞、带宽不足、无线拥塞/干扰或媒体服务器超载造成的，从而导致音频失真或丢失。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p108">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-180"><strong>抖动</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-180"><strong>Jitter</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-181">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-181">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-182">在 RTP 数据包到达之间检测到的平均抖动率。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-182">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="f8e8d-183"> (抖动是 shakiness 的测量值 &quot; &quot; 。 ) 高抖动值通常由拥挤或过载的媒体服务器引起，并导致失真或丢失的音频。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-183">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e8d-184"><strong>修复程序隐藏比率</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-184"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-185">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-p110">隐藏的音频样本与样本总数的平均比率。（隐藏的音频样本是一项技术，用于消除通常由丢弃的网络数据包造成的意外转换。）高值指示数据包丢失或抖动造成的显著的丢失隐藏级别，从而导致音频失真或丢失。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p110">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-188"><strong>修复程序拉伸比率</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-188"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-189">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-189">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-p111">拉伸的音频样本数与样本总数的平均比率。（拉伸的音频是一类已扩展的音频，可在检测到丢弃的网络数据包时帮助保持呼叫质量。）高值指示抖动造成的显著的样本拉伸级别，从而导致音频听起来很机械或失真。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p111">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e8d-192"><strong>修复程序压缩比率</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-192"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-193">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-193">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-p112">压缩的音频样本与样本总数的平均比率。（压缩的音频是一类已压缩的音频，可在检测到丢弃的网络数据包时帮助保持呼叫质量。）高值指示抖动造成的显著的样本压缩级别，从而导致音频听起来像是已加速或失真。</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p112">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e8d-196"><strong>连接</strong></span><span class="sxs-lookup"><span data-stu-id="f8e8d-196"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e8d-197">是</span><span class="sxs-lookup"><span data-stu-id="f8e8d-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="f8e8d-p113">无线通信链路的类型。通常，这是以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p113">Type of wireless communication link. Typically, this is one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f8e8d-200">中继</span><span class="sxs-lookup"><span data-stu-id="f8e8d-200">Relay</span></span></p></li>
<li><p><span data-ttu-id="f8e8d-201">直接</span><span class="sxs-lookup"><span data-stu-id="f8e8d-201">Direct</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="f8e8d-202">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8e8d-202">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

