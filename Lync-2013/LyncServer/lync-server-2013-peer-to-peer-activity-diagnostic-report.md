---
title: Lync Server 2013：对等活动诊断报告
description: Lync Server 2013：对等活动诊断报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Activity Diagnostic Report
ms:assetid: 025e8ab4-2e64-4a6b-8f52-caf756a5cac3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558602(v=OCS.15)
ms:contentKeyID: 48183242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 80172c5e0f8b23bf05fad6ec300f0d1ffefb3327
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424682"
---
# <a name="peer-to-peer-activity-diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="373bb-103">Lync Server 2013 中的对等活动诊断报告</span><span class="sxs-lookup"><span data-stu-id="373bb-103">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="373bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="373bb-104">

<span> </span></span></span>

<span data-ttu-id="373bb-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="373bb-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="373bb-106">对等活动诊断报告提供有关成功和失败的对等通信会话的信息。</span><span class="sxs-lookup"><span data-stu-id="373bb-106">The Peer-to-Peer Activity Diagnostic Report provides information about the success and failure of your peer-to-peer communication sessions.</span></span> <span data-ttu-id="373bb-107">请注意，Microsoft Lync Server 2013 区分不同类型的故障：</span><span class="sxs-lookup"><span data-stu-id="373bb-107">Note that Microsoft Lync Server 2013 distinguishes between different kinds of failure:</span></span>

  - <span data-ttu-id="373bb-108">**预期失败**。</span><span class="sxs-lookup"><span data-stu-id="373bb-108">**Expected failure**.</span></span> <span data-ttu-id="373bb-109">预期失败通常指纯技术意义上的失败。</span><span class="sxs-lookup"><span data-stu-id="373bb-109">An expected failure is typically a failure only in the most technical sense.</span></span> <span data-ttu-id="373bb-110">例如，假设您呼叫某人，但他或她不在办公室，因此无法接听电话。</span><span class="sxs-lookup"><span data-stu-id="373bb-110">For example, suppose you call someone, but he or she is away from the office and is unable to answer the phone.</span></span> <span data-ttu-id="373bb-111">此呼叫未被应答，因而在技术上视为失败。</span><span class="sxs-lookup"><span data-stu-id="373bb-111">Because the call was not answered, the call is technically considered a failure.</span></span> <span data-ttu-id="373bb-112">另一方面，这是预期的故障： Microsoft Lync Server 2013 不希望你接听电话（如果你不能接听电话）。</span><span class="sxs-lookup"><span data-stu-id="373bb-112">On the other hand, this was an expected failure: Microsoft Lync Server 2013 does not expect you to answer the phone if you're not available to answer the phone.</span></span> <span data-ttu-id="373bb-113">同样地，如果您尝试发送一条即时消息给某人，而对方处于脱机状态，或者对方只登录到不支持即时消息的电话时，也会发生预期失败。</span><span class="sxs-lookup"><span data-stu-id="373bb-113">Likewise, an expected failure will occur if you attempt to send an instant message to a user who is offline, or is logged on only to a phone that does not support instant messaging.</span></span>

  - <span data-ttu-id="373bb-114">**意外失败**。</span><span class="sxs-lookup"><span data-stu-id="373bb-114">**Unexpected failure**.</span></span> <span data-ttu-id="373bb-115">意外错误完全可顾名思义为：您预期不会发生的一种基于环境的错误。</span><span class="sxs-lookup"><span data-stu-id="373bb-115">An unexpected error is exactly what the name implies: an error that, based on the circumstances, you would not expect to occur.</span></span> <span data-ttu-id="373bb-116">例如，假设您呼叫某人，并且该人可以接听呼叫;但是，当 Lync Server 2013 尝试将呼叫路由到语音邮件时，呼叫将失败，因为与 Exchange 统一消息的连接已丢失。</span><span class="sxs-lookup"><span data-stu-id="373bb-116">For example, suppose you call someone and that person is available to answer the call; however, when Lync Server 2013 tries to route your call to voicemail the call fails because connectivity to Exchange Unified Messaging has been lost.</span></span> <span data-ttu-id="373bb-117">这是一个意外错误：您希望通话始终会传送到语音邮件。</span><span class="sxs-lookup"><span data-stu-id="373bb-117">That's an unexpected error: you would expect that calls could always be routed to voicemail.</span></span> <span data-ttu-id="373bb-118">一般说来，意外失败是真正意义上的失败：不能通过用户培训或类似措施加以补救。</span><span class="sxs-lookup"><span data-stu-id="373bb-118">As a general rule, unexpected failures are true failures: they are problems that likely cannot be remedied through user education or similar measures.</span></span>

<span data-ttu-id="373bb-p104">请注意，“成功”、“预期失败”、“意外失败”度量值加起来可能并不等于“会话总数”度量值。例如，在前面的说明中，我们获得以下值：</span><span class="sxs-lookup"><span data-stu-id="373bb-p104">Note that the Success, Expected failure, and Unexpected failure metrics might not add up to the Total sessions metric. For example, in the preceding illustration, we have the following values:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="373bb-121">成功</span><span class="sxs-lookup"><span data-stu-id="373bb-121">Successes</span></span></th>
<th><span data-ttu-id="373bb-122">预期失败</span><span class="sxs-lookup"><span data-stu-id="373bb-122">Expected failures</span></span></th>
<th><span data-ttu-id="373bb-123">意外失败</span><span class="sxs-lookup"><span data-stu-id="373bb-123">Unexpected failures</span></span></th>
<th><span data-ttu-id="373bb-124">会话总数</span><span class="sxs-lookup"><span data-stu-id="373bb-124">Total sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="373bb-125">2024</span><span class="sxs-lookup"><span data-stu-id="373bb-125">2024</span></span></p></td>
<td><p><span data-ttu-id="373bb-126">469</span><span class="sxs-lookup"><span data-stu-id="373bb-126">469</span></span></p></td>
<td><p><span data-ttu-id="373bb-127">utf-16</span><span class="sxs-lookup"><span data-stu-id="373bb-127">16</span></span></p></td>
<td><p><span data-ttu-id="373bb-128">2521</span><span class="sxs-lookup"><span data-stu-id="373bb-128">2521</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="373bb-129">2024 + 469 + 16 将获得总共 2,509 个会话，而“会话总数”列显示总共 2,521 个会话。</span><span class="sxs-lookup"><span data-stu-id="373bb-129">If you add 2024 + 469 + 16 you get a total of 2,509 sessions, yet the Total sessions column shows a total of 2,521 sessions.</span></span> <span data-ttu-id="373bb-130">“丢失的”12 个会话是系统无法归类为是成功还是失败的会话。</span><span class="sxs-lookup"><span data-stu-id="373bb-130">The "missing" 12 sessions are sessions that the system was unable to categorize as successful or unsuccessful.</span></span> <span data-ttu-id="373bb-131">在第三方产品引入了一种不熟悉 Lync 服务器的新诊断代码的情况下，有时会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="373bb-131">That will sometimes be the case when a third-party product introduces a new diagnostic code that is unfamiliar to Lync Server.</span></span> <span data-ttu-id="373bb-132">这时，使用该产品并报告该诊断代码的呼叫并非总是能归类为“成功”、“预期失败”或“意外失败”。</span><span class="sxs-lookup"><span data-stu-id="373bb-132">When that happens, calls made using that product, and reporting that diagnostic code, cannot always be categorized as being a Success, an Expected failure, or an Unexpected failure.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-activity-diagnostic-report"></a><span data-ttu-id="373bb-133">访问对等活动诊断报告</span><span class="sxs-lookup"><span data-stu-id="373bb-133">Accessing the Peer-to-Peer Activity Diagnostic Report</span></span>

<span data-ttu-id="373bb-134">可以从“监控报告”主页访问对等诊断报告。</span><span class="sxs-lookup"><span data-stu-id="373bb-134">The Peer-to-Peer Diagnostic Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="373bb-135">您可以通过单击以下任一指标来访问 [Lync Server 2013 中的失败分发报告](lync-server-2013-failure-distribution-report.md) ：</span><span class="sxs-lookup"><span data-stu-id="373bb-135">You can access the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="373bb-136">意外失败量</span><span class="sxs-lookup"><span data-stu-id="373bb-136">Unexpected failure volume</span></span>

  - <span data-ttu-id="373bb-137">预期失败量</span><span class="sxs-lookup"><span data-stu-id="373bb-137">Expected failure volume</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-activity-diagnostic-report"></a><span data-ttu-id="373bb-138">充分利用对等活动诊断报告</span><span class="sxs-lookup"><span data-stu-id="373bb-138">Making the Best Use of the Peer-to-Peer Activity Diagnostic Report</span></span>

<span data-ttu-id="373bb-p107">虽然可以通过多种方法来筛选对等活动诊断报告，但默认情况下，那些筛选选项在视图中是隐藏的。若要查看您可以使用的筛选选项，请单击报告窗口右上角中的“显示/隐藏参数”按钮。然后，即可使用筛选选项。</span><span class="sxs-lookup"><span data-stu-id="373bb-p107">There are a number of ways you can filter the Peer-to-Peer Activity Diagnostic Report but, by default, those filtering options are hidden from view. To view the filtering options available to you, click the Show/Hide Parameters button in the upper right-hand corner of the report window. Once you do that the filtering options will be available for use.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="373bb-142">筛选器</span><span class="sxs-lookup"><span data-stu-id="373bb-142">Filters</span></span>

<span data-ttu-id="373bb-p108">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。例如，对等活动诊断报告允许您根据会话形式（例如，即时消息、文件传输或应用程序共享）等内容进行筛选。您还可以选择数据的分组方式。在此示例中，将按小时、天、周或月对呼叫进行分组。</span><span class="sxs-lookup"><span data-stu-id="373bb-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Peer-to-Peer Activity Diagnostic Report enables you to filter on such things as the session modality (for example, instant messaging, file transfer, or application sharing). You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="373bb-147">下表列出了可用于对等活动诊断报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="373bb-147">The following table lists the filters that you can use with the Peer-to-Peer Activity Diagnostic Report.</span></span>

### <a name="peer-to-peer-activity-diagnostic-report-filters"></a><span data-ttu-id="373bb-148">对等活动诊断报告筛选器</span><span class="sxs-lookup"><span data-stu-id="373bb-148">Peer-to-Peer Activity Diagnostic Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="373bb-149">名称</span><span class="sxs-lookup"><span data-stu-id="373bb-149">Name</span></span></th>
<th><span data-ttu-id="373bb-150">描述</span><span class="sxs-lookup"><span data-stu-id="373bb-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="373bb-151"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-151"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-p109">时间范围的开始日期/时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="373bb-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="373bb-154">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="373bb-154">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="373bb-p110">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="373bb-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="373bb-157">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="373bb-157">7/7/2012</span></span></p>
<p><span data-ttu-id="373bb-158">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="373bb-158">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="373bb-159">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="373bb-159">7/3/2012</span></span></p>
<p><span data-ttu-id="373bb-160">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="373bb-160">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="373bb-161"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-161"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-p111">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="373bb-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="373bb-164">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="373bb-164">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="373bb-p112">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="373bb-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="373bb-167">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="373bb-167">7/7/2012</span></span></p>
<p><span data-ttu-id="373bb-168">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="373bb-168">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="373bb-169">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="373bb-169">7/3/2012</span></span></p>
<p><span data-ttu-id="373bb-170">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="373bb-170">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="373bb-171"><strong>间隔</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-171"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-p113">时间间隔。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="373bb-p113">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="373bb-174">每小时（最多可显示 25 个小时）</span><span class="sxs-lookup"><span data-stu-id="373bb-174">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="373bb-175">每天（最多可显示 31 天）</span><span class="sxs-lookup"><span data-stu-id="373bb-175">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="373bb-176">每周（最多可显示 12 周）</span><span class="sxs-lookup"><span data-stu-id="373bb-176">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="373bb-177">每月（最多可显示 12 个月）</span><span class="sxs-lookup"><span data-stu-id="373bb-177">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="373bb-178">如果开始日期和结束日期超出了所选间隔允许的最长时间，则仅显示最长时间（从开始日期开始）。</span><span class="sxs-lookup"><span data-stu-id="373bb-178">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="373bb-179">例如，如果选择 "开始日期 7/7/2012" 和 "结束日期 2/28/2012" 的 "每日间隔"，则会显示 8/7/2012 12:00 AM 至 9/7/2012 12:00 AM (的数据，即，总数据) 31 天。</span><span class="sxs-lookup"><span data-stu-id="373bb-179">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="373bb-180"><strong>池</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-180"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-p115">注册器池或边缘服务器的完全限定域名 (FQDN)。可以选择单个池，也可以单击“<strong>[所有]</strong>”查看所有池的数据。系统根据数据库中的记录自动为您填充该下拉列表。</span><span class="sxs-lookup"><span data-stu-id="373bb-p115">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="373bb-184"><strong>形式</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-184"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-p116">指示发生的通信活动的类型。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="373bb-p116">Indicates the type of communication activity that took place. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="373bb-187">[所有]</span><span class="sxs-lookup"><span data-stu-id="373bb-187">[All]</span></span></p></li>
<li><p><span data-ttu-id="373bb-188">即时消息</span><span class="sxs-lookup"><span data-stu-id="373bb-188">Instant messaging</span></span></p></li>
<li><p><span data-ttu-id="373bb-189">文件传输</span><span class="sxs-lookup"><span data-stu-id="373bb-189">File transfer</span></span></p></li>
<li><p><span data-ttu-id="373bb-190">应用程序共享</span><span class="sxs-lookup"><span data-stu-id="373bb-190">Application sharing</span></span></p></li>
<li><p><span data-ttu-id="373bb-191">音频</span><span class="sxs-lookup"><span data-stu-id="373bb-191">Audio</span></span></p></li>
<li><p><span data-ttu-id="373bb-192">视频</span><span class="sxs-lookup"><span data-stu-id="373bb-192">Video</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-per-modality"></a><span data-ttu-id="373bb-193">每种形式的指标</span><span class="sxs-lookup"><span data-stu-id="373bb-193">Metrics (per modality)</span></span>

<span data-ttu-id="373bb-194">下表列出了每种形式的对等活动诊断报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="373bb-194">The following table lists the information provided in the Peer-to-Peer Activity Diagnostic Report for each modality.</span></span>

### <a name="metrics-per-modality"></a><span data-ttu-id="373bb-195">每种形式的指标</span><span class="sxs-lookup"><span data-stu-id="373bb-195">Metrics (per modality)</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="373bb-196">名称</span><span class="sxs-lookup"><span data-stu-id="373bb-196">Name</span></span></th>
<th><span data-ttu-id="373bb-197">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="373bb-197">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="373bb-198">描述</span><span class="sxs-lookup"><span data-stu-id="373bb-198">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="373bb-199"><strong>成功量</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-199"><strong>Success volume</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-200">否</span><span class="sxs-lookup"><span data-stu-id="373bb-200">No</span></span></p></td>
<td><p><span data-ttu-id="373bb-201">成功的对等会话总数。</span><span class="sxs-lookup"><span data-stu-id="373bb-201">Total number of successful peer-to-peer sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="373bb-202"><strong>成功百分比</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-202"><strong>Success percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-203">否</span><span class="sxs-lookup"><span data-stu-id="373bb-203">No</span></span></p></td>
<td><p><span data-ttu-id="373bb-p117">已完成且没有严重问题的对等会话百分比。计算方法是“成功量”除以“会话总数”。</span><span class="sxs-lookup"><span data-stu-id="373bb-p117">Percentage of peer-to-peer sessions that completed with significant problems. Calculated by dividing the Success volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="373bb-206"><strong>预期失败量</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-206"><strong>Expected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-207">否</span><span class="sxs-lookup"><span data-stu-id="373bb-207">No</span></span></p></td>
<td><p><span data-ttu-id="373bb-208">预期失败发生的会话的总数 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="373bb-208">Total number of sessions where an &quot;expected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="373bb-p118">预期失败是指预计会出现的失败情况。例如，如果用户将其状态设置为“请勿打扰”，那么向该用户发出的任何呼叫应该都会失败。</span><span class="sxs-lookup"><span data-stu-id="373bb-p118">An expected failure is a failure that is expected to happen. For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="373bb-211"><strong>预期失败百分比</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-211"><strong>Expected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-212">否</span><span class="sxs-lookup"><span data-stu-id="373bb-212">No</span></span></p></td>
<td><p><span data-ttu-id="373bb-p119">遇到预期错误的对等会话百分比。计算方法是“预期失败量”除以“会话总数”。</span><span class="sxs-lookup"><span data-stu-id="373bb-p119">Percentage of peer-to-peer sessions that experienced an expected error. Calculated by dividing the Expected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="373bb-215"><strong>意外失败量</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-215"><strong>Unexpected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-216">否</span><span class="sxs-lookup"><span data-stu-id="373bb-216">No</span></span></p></td>
<td><p><span data-ttu-id="373bb-217">发生意外失败的会话的总数 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="373bb-217">Total number of sessions where an &quot;unexpected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="373bb-p120">意外失败是指在本该正常运行的系统中出现的失败情况。例如，如果呼叫者处于呼叫等待状态，则不应该终止呼叫。如果终止，则会被标记为意外失败。</span><span class="sxs-lookup"><span data-stu-id="373bb-p120">An unexpected failure is a failure that occurs in what would appear to be an otherwise healthy system. For example, a call should not be terminated if the caller is placed on hold. If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="373bb-221"><strong>意外失败百分比</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-221"><strong>Unexpected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-222">否</span><span class="sxs-lookup"><span data-stu-id="373bb-222">No</span></span></p></td>
<td><p><span data-ttu-id="373bb-p121">遇到意外错误的对等会话百分比。计算方法是“意外失败量”除以“会话总数”。</span><span class="sxs-lookup"><span data-stu-id="373bb-p121">Percentage of peer-to-peer sessions that experienced an unexpected error. Calculated by dividing the Unexpected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="373bb-225"><strong>会话总数</strong></span><span class="sxs-lookup"><span data-stu-id="373bb-225"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="373bb-226">否</span><span class="sxs-lookup"><span data-stu-id="373bb-226">No</span></span></p></td>
<td><p><span data-ttu-id="373bb-227">会话的总数，包括成功的会话、失败的会话（预期失败和意外失败）及未归类的会话。</span><span class="sxs-lookup"><span data-stu-id="373bb-227">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="373bb-228">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="373bb-228">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

