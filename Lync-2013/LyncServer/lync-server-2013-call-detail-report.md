---
title: Lync Server 2013：呼叫详细信息报告
description: Lync Server 2013：呼叫详细信息报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Detail Report
ms:assetid: 38862e35-3fec-41b9-a035-0b301942d446
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558637(v=OCS.15)
ms:contentKeyID: 48183843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d72ae6c1c1ec869041eee5b0dc35941c33609710
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392241"
---
# <a name="call-detail-report-in-lync-server-2013"></a><span data-ttu-id="888d0-103">Lync Server 2013 中的呼叫详细信息报告</span><span class="sxs-lookup"><span data-stu-id="888d0-103">Call Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="888d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="888d0-104">

<span> </span></span></span>

<span data-ttu-id="888d0-105">_**主题上次修改时间：** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="888d0-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="888d0-106">通话详细信息报告提供单个通话的详细信息，请参阅。此报告包括由 Lync Server 收集的几乎所有经验的质量指标和统计信息，分为如下报表部分：</span><span class="sxs-lookup"><span data-stu-id="888d0-106">The Call Detail Report provides a detailed look at an individual call; the report includes nearly all the Quality of Experience metrics and statistics collected by Lync Server, divided into report sections such as:</span></span>

  - <span data-ttu-id="888d0-107">呼叫信息</span><span class="sxs-lookup"><span data-stu-id="888d0-107">Call Information</span></span>

  - <span data-ttu-id="888d0-108">呼叫者设备和信号指标</span><span class="sxs-lookup"><span data-stu-id="888d0-108">Caller Device and Signal Metrics</span></span>

  - <span data-ttu-id="888d0-109">被叫方设备和信号指标</span><span class="sxs-lookup"><span data-stu-id="888d0-109">Callee Device and Signal metrics</span></span>

  - <span data-ttu-id="888d0-110">呼叫者客户端事件</span><span class="sxs-lookup"><span data-stu-id="888d0-110">Caller Client Event</span></span>

  - <span data-ttu-id="888d0-111">被叫方客户端事件</span><span class="sxs-lookup"><span data-stu-id="888d0-111">Callee Client Event</span></span>

  - <span data-ttu-id="888d0-112">音频流（呼叫者到被叫方）</span><span class="sxs-lookup"><span data-stu-id="888d0-112">Audio Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="888d0-113">视频流（呼叫者到被叫方）</span><span class="sxs-lookup"><span data-stu-id="888d0-113">Video Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="888d0-114">音频流（被叫方到呼叫者）</span><span class="sxs-lookup"><span data-stu-id="888d0-114">Audio Stream (Callee to Caller)</span></span>

  - <span data-ttu-id="888d0-115">视频流（被叫方到呼叫者）</span><span class="sxs-lookup"><span data-stu-id="888d0-115">Video Stream (Callee to Caller)</span></span>

<span data-ttu-id="888d0-p101">请记住，您在指定报告上看到的类别和指标取决于两个因素：会话类型和会话中使用的终结点类型。例如，纯音频呼叫不会报告视频流的相关指标；这是因为该呼叫没有视频流。同样，您的报告可能列出了呼叫者统计信息，而没有列出被叫方统计信息。这通常是因为被叫方没有使用符合 SIP 的设备。终结点负责在呼叫结束时报告统计信息；但是，移动电话（不了解有关 SIP 或 SIP 统计信息的任何情况）无法报告此类信息。如果您呼叫某人且此人用其移动电话应答您的呼叫，则呼叫结束时您将不会获得来自该移动电话的报告。</span><span class="sxs-lookup"><span data-stu-id="888d0-p101">Keep in mind that the categories and the metrics you see on a given report depend on two things: the type of session and the type of endpoints used in the session. For example, an audio-only call will not report metrics for video streams; that's because the call didn't have a video stream. Likewise, you might have a report that lists caller statistics but not callee statistics. That's typically because the callee was not using a SIP-compliant device. Endpoints are responsible for reporting statistics at the end of a call; however, a cell phone (which knows nothing about SIP or SIP statistics) is unable to report that kind of information. If you call someone and they answer you on their cell phone, you will not get a report from that cell phone when the call ends.</span></span>

<span data-ttu-id="888d0-122">呼叫详情报告在您尝试准确确定指定呼叫遇到媒体质量问题的原因时最为有用。</span><span class="sxs-lookup"><span data-stu-id="888d0-122">The Call Detail Report is most useful when you are trying to determine exactly why a given call experienced media quality problems.</span></span>

<div>

## <a name="accessing-the-call-detail-report"></a><span data-ttu-id="888d0-123">访问呼叫详情报告</span><span class="sxs-lookup"><span data-stu-id="888d0-123">Accessing the Call Detail Report</span></span>

<span data-ttu-id="888d0-124">可以从下列任意报告中访问呼叫详情报告：</span><span class="sxs-lookup"><span data-stu-id="888d0-124">The Call Detail Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="888d0-125">[Lync Server 2013 中的位置报告](lync-server-2013-location-report.md) (单击 "呼叫音量" 或 "不良呼叫百分比跃点数") </span><span class="sxs-lookup"><span data-stu-id="888d0-125">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking either the Call volume or the Poor call percentage metric)</span></span>

  - <span data-ttu-id="888d0-126">[Lync Server 2013 (中的 "媒体质量摘要" 报告](lync-server-2013-media-quality-summary-report.md)：单击 "呼叫音量" 或 "不良呼叫百分比" 指标) </span><span class="sxs-lookup"><span data-stu-id="888d0-126">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="888d0-127">[Lync server 2013 (中的 "媒体质量比较" 报表](lync-server-2013-media-quality-comparison-report.md)，方法是单击[lync server 2013 中的 "呼叫列表" 报表](lync-server-2013-call-list-report.md)，然后单击 "详细信息度量") 。</span><span class="sxs-lookup"><span data-stu-id="888d0-127">The [Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md) (by clicking the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) and then clicking the Detail metric).</span></span>

  - <span data-ttu-id="888d0-128">[Lync server 2013 中的 "服务器性能" 报表](lync-server-2013-server-performance-report.md) (单击 "呼叫音量" 或 "不良呼叫百分比" 度量值) </span><span class="sxs-lookup"><span data-stu-id="888d0-128">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="888d0-129">[Lync Server 2013 (中的通话清单报告](lync-server-2013-call-list-report.md)，方法是单击 "详细指标") </span><span class="sxs-lookup"><span data-stu-id="888d0-129">The [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) (by clicking the Detail metric)</span></span>

<span data-ttu-id="888d0-130">从 "呼叫详细信息" 报告中，您可以通过单击以下任一指标 [在 Lync Server 2013 中访问设备报告](lync-server-2013-device-report.md) ：</span><span class="sxs-lookup"><span data-stu-id="888d0-130">From within the Call Detail Report you can access the [Device Report in Lync Server 2013](lync-server-2013-device-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="888d0-131">捕获设备</span><span class="sxs-lookup"><span data-stu-id="888d0-131">Capture device</span></span>

  - <span data-ttu-id="888d0-132">呈现设备</span><span class="sxs-lookup"><span data-stu-id="888d0-132">Render device</span></span>

<span data-ttu-id="888d0-133">您还可以通过单击“A/V 边缘服务器”指标访问服务器媒体质量趋势报告。</span><span class="sxs-lookup"><span data-stu-id="888d0-133">You can also access the Server Media Quality Trend Report by clicking the A/V edge server metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-detail-report"></a><span data-ttu-id="888d0-134">充分利用呼叫详情报告</span><span class="sxs-lookup"><span data-stu-id="888d0-134">Making the Best Use of the Call Detail Report</span></span>

<span data-ttu-id="888d0-p102">呼叫详情报告通常包括 250 多个不同的指标，其中包括麦克风时间戳偏移、低 SNR 时间和近端回声时间等项目。如果您不记得所有这些指标实际度量的内容，请尝试将鼠标指针置于指标标签上方；通常，将显示描述该指标的工具提示。</span><span class="sxs-lookup"><span data-stu-id="888d0-p102">The Call Detail Report typically includes over 250 different metrics, including such items as Microphone timestamp drift, Low SNR time, and Near end to echo time. If you can't remember what all of these metrics actually measure, try holding your mouse over the metric label; often-times, a tooltip will appear describing that metric.</span></span>

<span data-ttu-id="888d0-137">如果查找指标时遇到问题，请在 "搜索" 框中键入 "指标" 标签的一部分，然后单击 "查找"。</span><span class="sxs-lookup"><span data-stu-id="888d0-137">If you have problems locating a metric, type part of the metric label in the search box and then click Find.</span></span> <span data-ttu-id="888d0-138">例如，如果找不到低 SNR 时间度量值，请在 "搜索" 框中键入 "SNR"，然后单击 "查找"。</span><span class="sxs-lookup"><span data-stu-id="888d0-138">For example, if you can't find the Low SNR time metric, type SNR in the search box and then click Find.</span></span>

<span data-ttu-id="888d0-p104">请注意，报告仅跟踪关于呼叫的信息。不记录呼叫本身。</span><span class="sxs-lookup"><span data-stu-id="888d0-p104">Note that the report only tracks information about a call. The call itself is not recorded.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="888d0-141">筛选器</span><span class="sxs-lookup"><span data-stu-id="888d0-141">Filters</span></span>

<span data-ttu-id="888d0-p105">无。您无法筛选呼叫详情报告。</span><span class="sxs-lookup"><span data-stu-id="888d0-p105">None. You cannot filter the Call Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="888d0-144">指标</span><span class="sxs-lookup"><span data-stu-id="888d0-144">Metrics</span></span>

<span data-ttu-id="888d0-145">下表列出了每个呼叫的呼叫详情报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="888d0-145">The following table lists the information provided in the Call Detail Report for each call.</span></span>

### <a name="call-detail-report-metrics"></a><span data-ttu-id="888d0-146">呼叫详情报告指标</span><span class="sxs-lookup"><span data-stu-id="888d0-146">Call Detail Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="888d0-147">名称</span><span class="sxs-lookup"><span data-stu-id="888d0-147">Name</span></span></th>
<th><span data-ttu-id="888d0-148">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="888d0-148">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="888d0-149">描述</span><span class="sxs-lookup"><span data-stu-id="888d0-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="888d0-150"><strong>呼叫者 PAI</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-150"><strong>Caller PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-151">否</span><span class="sxs-lookup"><span data-stu-id="888d0-151">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-p106">发起呼叫的用户的 P-Asserted-Identity。P-Asserted-Identity 用于传达受信任网络内用户经验证的身份。</span><span class="sxs-lookup"><span data-stu-id="888d0-p106">P-Asserted-Identity of the user who initiated the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-154"><strong>呼叫者 URI</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-154"><strong>Caller URI</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-155">否</span><span class="sxs-lookup"><span data-stu-id="888d0-155">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-156">发起呼叫的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="888d0-156">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-157"><strong>呼叫者终结点</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-157"><strong>Caller endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-158">否</span><span class="sxs-lookup"><span data-stu-id="888d0-158">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-159">用于发出呼叫的设备。</span><span class="sxs-lookup"><span data-stu-id="888d0-159">Device used to make the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-160"><strong>呼叫者用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-160"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-161">否</span><span class="sxs-lookup"><span data-stu-id="888d0-161">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-162">发出呼叫的设备上使用的软件。</span><span class="sxs-lookup"><span data-stu-id="888d0-162">Software used on the device that made the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-163"><strong>呼叫开始</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-163"><strong>Call start</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-164">否</span><span class="sxs-lookup"><span data-stu-id="888d0-164">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-165">最初发出呼叫的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="888d0-165">Date and time that the call was initially placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-166"><strong>中介服务器旁路呼叫</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-166"><strong>Mediation Server bypass call</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-167">否</span><span class="sxs-lookup"><span data-stu-id="888d0-167">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-168">指示呼叫是否在不通过中介服务器的情况下连接到 PSTN 语音网关或合格的 IP-PBX。</span><span class="sxs-lookup"><span data-stu-id="888d0-168">Indicates whether the call connected to a PSTN voice gateway or qualified IP-PBX without passing through the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-169"><strong>呼叫者 OS</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-169"><strong>Caller OS</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-170">否</span><span class="sxs-lookup"><span data-stu-id="888d0-170">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-171">呼叫者计算机的操作系统。</span><span class="sxs-lookup"><span data-stu-id="888d0-171">Operating system of the caller's computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-172"><strong>呼叫者 CPU</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-172"><strong>Caller CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-173">否</span><span class="sxs-lookup"><span data-stu-id="888d0-173">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-174">发起呼叫的用户的计算机中安装的 CPU。</span><span class="sxs-lookup"><span data-stu-id="888d0-174">CPU installed in the computer of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-175"><strong>呼叫者 CPU 内核数</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-175"><strong>Caller CPU core number</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-176">否</span><span class="sxs-lookup"><span data-stu-id="888d0-176">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-177">发起呼叫的人员使用的计算机中的处理器数量。</span><span class="sxs-lookup"><span data-stu-id="888d0-177">Processor number in the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-178"><strong>呼叫者 CPU 速度</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-178"><strong>Caller CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-179">否</span><span class="sxs-lookup"><span data-stu-id="888d0-179">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-180">发起呼叫的人员使用的计算机的 CPU 时钟频率。</span><span class="sxs-lookup"><span data-stu-id="888d0-180">Clock speed of the CPU of the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-181"><strong>呼叫者 CPU 虚拟化</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-181"><strong>Caller CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-182">否</span><span class="sxs-lookup"><span data-stu-id="888d0-182">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-183">发起呼叫的人员使用的计算机上使用的虚拟化（如果有）。</span><span class="sxs-lookup"><span data-stu-id="888d0-183">Virtualization (if any) used on the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-184"><strong>被叫方 PAI</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-184"><strong>Callee PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-185">否</span><span class="sxs-lookup"><span data-stu-id="888d0-185">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-p107">受邀加入呼叫的用户的 P-Asserted-Identity。P-Asserted-Identity 用于传达受信任网络内用户经验证的身份。</span><span class="sxs-lookup"><span data-stu-id="888d0-p107">P-Asserted-Identity of the user who was invited to join the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-188"><strong>被叫方 URI</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-188"><strong>Callee URI</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-189">否</span><span class="sxs-lookup"><span data-stu-id="888d0-189">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-190">被叫的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="888d0-190">SIP address of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-191"><strong>被叫方终结点</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-191"><strong>Callee endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-192">否</span><span class="sxs-lookup"><span data-stu-id="888d0-192">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-193">用于接收呼叫的设备。</span><span class="sxs-lookup"><span data-stu-id="888d0-193">Device used to receive the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-194"><strong>被叫方用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-194"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-195">否</span><span class="sxs-lookup"><span data-stu-id="888d0-195">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-196">接收呼叫的设备上使用的软件。</span><span class="sxs-lookup"><span data-stu-id="888d0-196">Software used on the device that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-197"><strong>持续时间</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-197"><strong>Duration</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-198">否</span><span class="sxs-lookup"><span data-stu-id="888d0-198">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-199">呼叫的时长。</span><span class="sxs-lookup"><span data-stu-id="888d0-199">Length of time for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-200"><strong>媒体旁路警告标记</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-200"><strong>Media bypass warning flag</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-201">否</span><span class="sxs-lookup"><span data-stu-id="888d0-201">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-202">在绕过中介服务器时发出的警告。</span><span class="sxs-lookup"><span data-stu-id="888d0-202">Warning issued when the Mediation Server was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-203"><strong>被叫方 OS</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-203"><strong>Callee OS</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-204">否</span><span class="sxs-lookup"><span data-stu-id="888d0-204">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-205">被叫用户的计算机的操作系统。</span><span class="sxs-lookup"><span data-stu-id="888d0-205">Operating system of the computer for the user who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-206"><strong>被叫方 CPU</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-206"><strong>Callee CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-207">否</span><span class="sxs-lookup"><span data-stu-id="888d0-207">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-208">被叫用户的计算机中安装的 CPU。</span><span class="sxs-lookup"><span data-stu-id="888d0-208">CPU installed in the computer of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-209"><strong>被叫方内核数</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-209"><strong>Callee core number</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-210">否</span><span class="sxs-lookup"><span data-stu-id="888d0-210">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-211">被叫人员使用的计算机中的处理器数量。</span><span class="sxs-lookup"><span data-stu-id="888d0-211">Processor number in the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888d0-212"><strong>被叫方 CPU 速度</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-212"><strong>Callee CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-213">否</span><span class="sxs-lookup"><span data-stu-id="888d0-213">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-214">被叫人员使用的计算机的 CPU 时钟频率。</span><span class="sxs-lookup"><span data-stu-id="888d0-214">Clock speed of the CPU of the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888d0-215"><strong>被叫方 CPU 虚拟化</strong></span><span class="sxs-lookup"><span data-stu-id="888d0-215"><strong>Callee CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="888d0-216">否</span><span class="sxs-lookup"><span data-stu-id="888d0-216">No</span></span></p></td>
<td><p><span data-ttu-id="888d0-217">被叫人员使用的计算机上使用的虚拟化（如果有）。</span><span class="sxs-lookup"><span data-stu-id="888d0-217">Virtualization (if any) used on the computer used by the person who was called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="888d0-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="888d0-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

