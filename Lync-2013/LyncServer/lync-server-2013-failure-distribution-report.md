---
title: Lync Server 2013：失败分发报告
description: Lync Server 2013：失败分发报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure Distribution Report
ms:assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558635(v=OCS.15)
ms:contentKeyID: 48183849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5a87f779f87d6b7002fa108f1969c33739eed9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428214"
---
# <a name="failure-distribution-report-in-lync-server-2013"></a><span data-ttu-id="20393-103">Lync Server 2013 中的失败分配报告</span><span class="sxs-lookup"><span data-stu-id="20393-103">Failure Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20393-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20393-104">

<span> </span></span></span>

<span data-ttu-id="20393-105">_**主题上次修改时间：** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="20393-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="20393-106">故障分布报告按以下类别对失败会话进行分级：</span><span class="sxs-lookup"><span data-stu-id="20393-106">The Failure Distribution Report ranks failed sessions in the following categories:</span></span>

  - <span data-ttu-id="20393-107">主要诊断原因</span><span class="sxs-lookup"><span data-stu-id="20393-107">Top diagnostic reasons</span></span>

  - <span data-ttu-id="20393-108">主要形式</span><span class="sxs-lookup"><span data-stu-id="20393-108">Top modalities</span></span>

  - <span data-ttu-id="20393-109">主要池</span><span class="sxs-lookup"><span data-stu-id="20393-109">Top pools</span></span>

  - <span data-ttu-id="20393-110">主要来源</span><span class="sxs-lookup"><span data-stu-id="20393-110">Top sources</span></span>

  - <span data-ttu-id="20393-111">主要组件</span><span class="sxs-lookup"><span data-stu-id="20393-111">Top components</span></span>

  - <span data-ttu-id="20393-112">主要来源用户</span><span class="sxs-lookup"><span data-stu-id="20393-112">Top from users</span></span>

  - <span data-ttu-id="20393-113">主要目标用户</span><span class="sxs-lookup"><span data-stu-id="20393-113">Top to users</span></span>

  - <span data-ttu-id="20393-114">主要来源用户代理</span><span class="sxs-lookup"><span data-stu-id="20393-114">Top from user agents</span></span>

<span data-ttu-id="20393-p101">可以使用这些类别准确确定出现问题的位置，在某些情况下还可准确确定出现问题的原因。例如，假设您在指定的一天内记录了 242 个失败的音频/视频会话。如果您查看故障分布报告，它可能会指示这些失败会话中有 237 个发生在您的 Dublin 池中。在跟踪和诊断出现这些故障的原因时，这为您提供了一个良好的开端。如果单击“**主要池**”类别下的 Dublin 池，即可看到该池的故障分布报告。然后您可以开始分析 Dublin 池为何出现如此多的问题。</span><span class="sxs-lookup"><span data-stu-id="20393-p101">You can use these categories to determine exactly where a problem is occurring and, in some cases, why the problem is occurring. For example, suppose you recorded 242 failed audio/video sessions during a given day. If you look at the Failure Distribution Report, it might show that 237 of those failed sessions took place in your Dublin pool. That gives you a good place to start when it comes to tracking down and diagnosing the causes behind those failures. If you click on the Dublin pool under the **Top pools** category, you will see a Failure Distribution Report just for that pool. You can then begin analyzing why the Dublin pool was experiencing so many difficulties.</span></span>

<div>

## <a name="viewing-the-failure-distribution-report"></a><span data-ttu-id="20393-121">查看故障分布报告</span><span class="sxs-lookup"><span data-stu-id="20393-121">Viewing the Failure Distribution Report</span></span>

<span data-ttu-id="20393-122">您可以通过单击“**预期失败量**”或“**意外失败量**”指标，从以下任意报告中访问故障分布报告：</span><span class="sxs-lookup"><span data-stu-id="20393-122">You can access the Failure Distribution Report from any of the following reports by clicking either the **Expected failure volume** or the **Unexpected failure volume** metric:</span></span>

  - [<span data-ttu-id="20393-123">Lync Server 2013 中的 "热门故障" 报表</span><span class="sxs-lookup"><span data-stu-id="20393-123">Top Failures Report in Lync Server 2013</span></span>](lync-server-2013-top-failures-report.md)

  - [<span data-ttu-id="20393-124">Lync Server 2013 中的会议诊断报告</span><span class="sxs-lookup"><span data-stu-id="20393-124">Conference Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-conference-diagnostic-report.md)

  - [<span data-ttu-id="20393-125">Lync Server 2013 中的对等活动诊断报告</span><span class="sxs-lookup"><span data-stu-id="20393-125">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)

<span data-ttu-id="20393-126">在 "失败分发" 报表中，可以单击以下任一指标，以 [在 Lync Server 2013 中查看 "失败列表" 报表](lync-server-2013-failure-list-report.md)：</span><span class="sxs-lookup"><span data-stu-id="20393-126">From the Failure Distribution Report, you can click any of the following metrics to view the [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md):</span></span>

  - <span data-ttu-id="20393-127">主要诊断原因（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-127">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="20393-128">主要形式（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-128">Top modalities (sessions)</span></span>

  - <span data-ttu-id="20393-129">主要池（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-129">Top pools (sessions)</span></span>

  - <span data-ttu-id="20393-130">主要来源（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-130">Top sources (sessions)</span></span>

  - <span data-ttu-id="20393-131">主要组件（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-131">Top components (sessions)</span></span>

  - <span data-ttu-id="20393-132">主要来源用户（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-132">Top from users (sessions)</span></span>

  - <span data-ttu-id="20393-133">主要目标用户（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-133">Top to users (sessions)</span></span>

  - <span data-ttu-id="20393-134">主要来源用户代理（会话）</span><span class="sxs-lookup"><span data-stu-id="20393-134">Top from user agents (sessions)</span></span>

</div>

<div>

## <a name="using-the-failure-distribution-report"></a><span data-ttu-id="20393-135">使用故障分布报告</span><span class="sxs-lookup"><span data-stu-id="20393-135">Using the Failure Distribution Report</span></span>

<span data-ttu-id="20393-p102">根据您的监视器尺寸和屏幕分辨率，当您在屏幕上查看故障分布报告中显示的某些数据时，这些数据可能会被截断。用户代理（可能具有很长的标签）等指标尤其可能出现这种情况。例如，具有类似“UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)”的名称的用户代理可能只会部分显示在屏幕上：</span><span class="sxs-lookup"><span data-stu-id="20393-p102">Depending on your monitor size and screen resolution, it's possible that some of the data shown in the Failure Distribution Report might be truncated when you view it onscreen. This is especially true for metrics such as user agents, which can have very long labels. For example, a user agent with a name like "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" might only partially appear onscreen:</span></span>

<span data-ttu-id="20393-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span><span class="sxs-lookup"><span data-stu-id="20393-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span></span>

<span data-ttu-id="20393-140">幸运的是，只需将鼠标指针停留在截断值上方即可查看整个标签。</span><span class="sxs-lookup"><span data-stu-id="20393-140">Fortunately, you can see the entire label simply by holding your mouse over the truncated value.</span></span>

<span data-ttu-id="20393-p103">可以使用故障分布报告按其进行筛选的一个有用指标是诊断 ID。如果您看到其他报告中出现相同的诊断 ID，则可以在故障分布报告中按此 ID 进行筛选，并获得有关失败会话期间报告此 ID 的准确位置及频率的十分详细的信息。</span><span class="sxs-lookup"><span data-stu-id="20393-p103">One interesting metric that you can filter on by using the Failure Distribution Report is Diagnostic ID. If you see the same Diagnostic ID cropping up in other reports you can filter on that ID in the Failure Distribution Report and get a very detailed look at exactly where, and how often, that ID has been reported during a failed session.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="20393-143">筛选器</span><span class="sxs-lookup"><span data-stu-id="20393-143">Filters</span></span>

<span data-ttu-id="20393-p104">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。例如，故障分布报告允许您依据活动类型（对等会话还是会议会话）或每个失败会话附带的诊断 ID 等条件进行筛选。</span><span class="sxs-lookup"><span data-stu-id="20393-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Failed Distribution Report enables you to filter on such things as the activity type (peer-to-peer session or conferencing session) or by the diagnostic ID that accompanied each failed session.</span></span>

<span data-ttu-id="20393-146">下表列出了可用于故障分布报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="20393-146">The following table lists the filters that you can use with the Failure Distribution Report.</span></span>

### <a name="failure-distribution-report-filters"></a><span data-ttu-id="20393-147">故障分布报告筛选器</span><span class="sxs-lookup"><span data-stu-id="20393-147">Failure Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-148">名称</span><span class="sxs-lookup"><span data-stu-id="20393-148">Name</span></span></th>
<th><span data-ttu-id="20393-149">描述</span><span class="sxs-lookup"><span data-stu-id="20393-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-150"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="20393-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-p105">时间范围的开始日期/时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="20393-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="20393-153">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="20393-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="20393-p106">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="20393-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="20393-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="20393-156">7/7/2012</span></span></p>
<p><span data-ttu-id="20393-157">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="20393-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="20393-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="20393-158">7/3/2012</span></span></p>
<p><span data-ttu-id="20393-159">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="20393-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-160"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="20393-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-p107">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="20393-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="20393-163">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="20393-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="20393-p108">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="20393-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="20393-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="20393-166">7/7/2012</span></span></p>
<p><span data-ttu-id="20393-167">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="20393-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="20393-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="20393-168">7/3/2012</span></span></p>
<p><span data-ttu-id="20393-169">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="20393-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-170"><strong>池</strong></span><span class="sxs-lookup"><span data-stu-id="20393-170"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-p109">注册器池或边缘服务器的完全限定域名 (FQDN)。可以选择单个池，也可以单击“<strong>[所有]</strong>”查看所有池的数据。系统根据数据库中的记录自动为您填充该下拉列表。</span><span class="sxs-lookup"><span data-stu-id="20393-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-174"><strong>活动类型</strong></span><span class="sxs-lookup"><span data-stu-id="20393-174"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-p110">要筛选的活动类型。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="20393-p110">Type of activity to filter on. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="20393-177">[所有]</span><span class="sxs-lookup"><span data-stu-id="20393-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="20393-178">对等</span><span class="sxs-lookup"><span data-stu-id="20393-178">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="20393-179">会议</span><span class="sxs-lookup"><span data-stu-id="20393-179">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-180"><strong>会话类别</strong></span><span class="sxs-lookup"><span data-stu-id="20393-180"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-p111">指示相应活动已成功还是失败。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="20393-p111">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="20393-183">[所有]</span><span class="sxs-lookup"><span data-stu-id="20393-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="20393-184">成功</span><span class="sxs-lookup"><span data-stu-id="20393-184">Success</span></span></p></li>
<li><p><span data-ttu-id="20393-185">预期失败</span><span class="sxs-lookup"><span data-stu-id="20393-185">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="20393-186">意外失败</span><span class="sxs-lookup"><span data-stu-id="20393-186">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="20393-187">&quot;预期的故障 &quot; 是预期发生的故障。</span><span class="sxs-lookup"><span data-stu-id="20393-187">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="20393-188">例如，如果用户将其状态设置为“请勿打扰”，那么向该用户发出的任何呼叫应该都会失败。</span><span class="sxs-lookup"><span data-stu-id="20393-188">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="20393-189">&quot;意外故障 &quot; 是指出现在其他正常运行的系统中的故障。</span><span class="sxs-lookup"><span data-stu-id="20393-189">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="20393-190">例如，如果呼叫者处于呼叫等待状态，则不应该终止呼叫。</span><span class="sxs-lookup"><span data-stu-id="20393-190">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="20393-191">如果终止，则会被标记为意外失败。</span><span class="sxs-lookup"><span data-stu-id="20393-191">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-192"><strong>诊断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="20393-192"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-p113">附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），提供的信息在排查错误时通常很有帮助。诊断标头是可选的（SIP 会话可以不包含这些标头），并且只对遇到此类问题的会话报告诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="20393-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="20393-195">主要诊断原因的指标</span><span class="sxs-lookup"><span data-stu-id="20393-195">Metrics for Top Diagnostic Reasons</span></span>

<span data-ttu-id="20393-196">下表列出了故障分布报告中基于最常见的诊断 ID 提供的信息。</span><span class="sxs-lookup"><span data-stu-id="20393-196">The following table lists the information provided in the Failure Distribution Report based on the most frequently reported diagnostic ID.</span></span>

### <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="20393-197">主要诊断原因的指标</span><span class="sxs-lookup"><span data-stu-id="20393-197">Metrics for Top Diagnostic Reasons</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-198">名称</span><span class="sxs-lookup"><span data-stu-id="20393-198">Name</span></span></th>
<th><span data-ttu-id="20393-199">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-199">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-200">描述</span><span class="sxs-lookup"><span data-stu-id="20393-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-201"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-201"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-202">否</span><span class="sxs-lookup"><span data-stu-id="20393-202">No</span></span></p></td>
<td><p><span data-ttu-id="20393-p114">失败会话的相对等级，根据诊断 ID 确定。诊断 ID 是附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），提供的信息在排查错误时通常很有帮助。</span><span class="sxs-lookup"><span data-stu-id="20393-p114">Relative ranking of failed sessions based on diagnostic IDs. The diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-205"><strong>主要诊断原因</strong></span><span class="sxs-lookup"><span data-stu-id="20393-205"><strong>Top diagnostic reasons</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-206">否</span><span class="sxs-lookup"><span data-stu-id="20393-206">No</span></span></p></td>
<td><p><span data-ttu-id="20393-207">会话中生成的诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="20393-207">Diagnostic ID generated in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-208"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-208"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-209">否</span><span class="sxs-lookup"><span data-stu-id="20393-209">No</span></span></p></td>
<td><p><span data-ttu-id="20393-210">生成了指定诊断 ID 的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-210">Total number of failed sessions where the specified diagnostic ID was generated.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-modalities"></a><span data-ttu-id="20393-211">主要形式的指标</span><span class="sxs-lookup"><span data-stu-id="20393-211">Metrics for Top Modalities</span></span>

<span data-ttu-id="20393-212">下表列出了故障分布报告中基于所遇故障最多的会话形式提供的信息。</span><span class="sxs-lookup"><span data-stu-id="20393-212">The following table lists the information provided in the Failure Distribution Report based on the session modalities that experienced the most failures.</span></span>

### <a name="metrics-for-top-modalities"></a><span data-ttu-id="20393-213">主要形式的指标</span><span class="sxs-lookup"><span data-stu-id="20393-213">Metrics for Top Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-214">名称</span><span class="sxs-lookup"><span data-stu-id="20393-214">Name</span></span></th>
<th><span data-ttu-id="20393-215">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-215">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-216">描述</span><span class="sxs-lookup"><span data-stu-id="20393-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-217"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-217"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-218">否</span><span class="sxs-lookup"><span data-stu-id="20393-218">No</span></span></p></td>
<td><p><span data-ttu-id="20393-219">失败会话的相对等级，根据会话类型（例如，音频/视频会议或对等文件传输会话）确定。</span><span class="sxs-lookup"><span data-stu-id="20393-219">Relative ranking based of failed session based on session type (for example, an audio/video conference or a peer-to-peer file transfer session).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-220"><strong>主要形式</strong></span><span class="sxs-lookup"><span data-stu-id="20393-220"><strong>Top modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-221">否</span><span class="sxs-lookup"><span data-stu-id="20393-221">No</span></span></p></td>
<td><p><span data-ttu-id="20393-222">会话类型。</span><span class="sxs-lookup"><span data-stu-id="20393-222">Session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-223"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-223"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-224">否</span><span class="sxs-lookup"><span data-stu-id="20393-224">No</span></span></p></td>
<td><p><span data-ttu-id="20393-225">涉及指定形式的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-225">Total number of failed sessions involving the specified modality.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-pools"></a><span data-ttu-id="20393-226">主要池的指标</span><span class="sxs-lookup"><span data-stu-id="20393-226">Metrics for Top Pools</span></span>

<span data-ttu-id="20393-227">下表列出了故障分布报告中基于所遇故障最多的池提供的信息。</span><span class="sxs-lookup"><span data-stu-id="20393-227">The following table lists the information provided in the Failure Distribution Report based on the pools that experienced the most failures.</span></span>

### <a name="metrics-for-top-pools"></a><span data-ttu-id="20393-228">主要池的指标</span><span class="sxs-lookup"><span data-stu-id="20393-228">Metrics for Top Pools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-229">名称</span><span class="sxs-lookup"><span data-stu-id="20393-229">Name</span></span></th>
<th><span data-ttu-id="20393-230">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-230">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-231">描述</span><span class="sxs-lookup"><span data-stu-id="20393-231">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-232"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-232"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-233">否</span><span class="sxs-lookup"><span data-stu-id="20393-233">No</span></span></p></td>
<td><p><span data-ttu-id="20393-234">基于执行会话的注册池或边缘服务器的失败会话的相对级别。</span><span class="sxs-lookup"><span data-stu-id="20393-234">Relative ranking of failed sessions based on the Registrar pool or Edge Server where the session was conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-235"><strong>主要池</strong></span><span class="sxs-lookup"><span data-stu-id="20393-235"><strong>Top pools</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-236">否</span><span class="sxs-lookup"><span data-stu-id="20393-236">No</span></span></p></td>
<td><p><span data-ttu-id="20393-237">注册机构池或边缘服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="20393-237">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-238"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-238"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-239">否</span><span class="sxs-lookup"><span data-stu-id="20393-239">No</span></span></p></td>
<td><p><span data-ttu-id="20393-240">每个注册池或边缘服务器的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-240">Total number of failed sessions per Registrar pool or Edge Server.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-sources"></a><span data-ttu-id="20393-241">主要来源的指标</span><span class="sxs-lookup"><span data-stu-id="20393-241">Metrics for Top Sources</span></span>

<span data-ttu-id="20393-242">下表列出了故障分布报告中基于所遇故障最多的计算机提供的信息。</span><span class="sxs-lookup"><span data-stu-id="20393-242">The following table lists the information provided in the Failure Distribution Report based on the computers that experienced the most failures.</span></span>

### <a name="metrics-for-top-sources"></a><span data-ttu-id="20393-243">主要来源的指标</span><span class="sxs-lookup"><span data-stu-id="20393-243">Metrics for Top Sources</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-244">名称</span><span class="sxs-lookup"><span data-stu-id="20393-244">Name</span></span></th>
<th><span data-ttu-id="20393-245">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-245">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-246">描述</span><span class="sxs-lookup"><span data-stu-id="20393-246">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-247"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-247"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-248">否</span><span class="sxs-lookup"><span data-stu-id="20393-248">No</span></span></p></td>
<td><p><span data-ttu-id="20393-249">失败会话的相对等级，根据计算机确定。</span><span class="sxs-lookup"><span data-stu-id="20393-249">Relative ranking failed sessions per computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-250"><strong>主要来源</strong></span><span class="sxs-lookup"><span data-stu-id="20393-250"><strong>Top sources</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-251">否</span><span class="sxs-lookup"><span data-stu-id="20393-251">No</span></span></p></td>
<td><p><span data-ttu-id="20393-252">失败会话所涉及的计算机的名称。</span><span class="sxs-lookup"><span data-stu-id="20393-252">Name of the computer involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-253"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-253"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-254">否</span><span class="sxs-lookup"><span data-stu-id="20393-254">No</span></span></p></td>
<td><p><span data-ttu-id="20393-255">每台计算机的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-255">Total number of failed sessions per computer.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-components"></a><span data-ttu-id="20393-256">主要组件的指标</span><span class="sxs-lookup"><span data-stu-id="20393-256">Metrics for Top Components</span></span>

<span data-ttu-id="20393-257">下表列出了故障分布报告中提供的信息，这些信息基于遇到最多失败的 Microsoft Lync Server 2010 组件。</span><span class="sxs-lookup"><span data-stu-id="20393-257">The following table lists the information provided in the Failure Distribution Report based on the Microsoft Lync Server 2010 components that experienced the most failures.</span></span>

### <a name="metrics-for-top-components"></a><span data-ttu-id="20393-258">主要组件的指标</span><span class="sxs-lookup"><span data-stu-id="20393-258">Metrics for Top Components</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-259">名称</span><span class="sxs-lookup"><span data-stu-id="20393-259">Name</span></span></th>
<th><span data-ttu-id="20393-260">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-260">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-261">描述</span><span class="sxs-lookup"><span data-stu-id="20393-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-262"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-262"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-263">否</span><span class="sxs-lookup"><span data-stu-id="20393-263">No</span></span></p></td>
<td><p><span data-ttu-id="20393-264">基于 Lync Server 2010 组件的失败会话的相对排名 (例如，ExumRouting、GroupChat 或 MediationServer) 。</span><span class="sxs-lookup"><span data-stu-id="20393-264">Relative ranking of failed sessions based on Lync Server 2010 component (for example, ExumRouting, GroupChat, or MediationServer).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-265"><strong>主要组件</strong></span><span class="sxs-lookup"><span data-stu-id="20393-265"><strong>Top components</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-266">否</span><span class="sxs-lookup"><span data-stu-id="20393-266">No</span></span></p></td>
<td><p><span data-ttu-id="20393-267">失败会话所涉及的组件的名称。</span><span class="sxs-lookup"><span data-stu-id="20393-267">Name of the component involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-268"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-268"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-269">否</span><span class="sxs-lookup"><span data-stu-id="20393-269">No</span></span></p></td>
<td><p><span data-ttu-id="20393-270">每个组件的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-270">Total number of failed sessions per component.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-from-users"></a><span data-ttu-id="20393-271">主要来源用户的指标</span><span class="sxs-lookup"><span data-stu-id="20393-271">Metrics for Top From Users</span></span>

<span data-ttu-id="20393-272">下表列出了故障分布报告中基于尝试呼叫其他人时所遇故障最多的用户提供的信息，尝试呼叫其他人的用户称为“来源”用户。</span><span class="sxs-lookup"><span data-stu-id="20393-272">The following table lists the information provided in the Failure Distribution Report based on users who experienced the most failures when they tried to call someone else (known as "From" users).</span></span>

### <a name="metrics-for-top-from-users"></a><span data-ttu-id="20393-273">主要来源用户的指标</span><span class="sxs-lookup"><span data-stu-id="20393-273">Metrics for Top From Users</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-274">名称</span><span class="sxs-lookup"><span data-stu-id="20393-274">Name</span></span></th>
<th><span data-ttu-id="20393-275">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-275">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-276">描述</span><span class="sxs-lookup"><span data-stu-id="20393-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-277"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-277"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-278">否</span><span class="sxs-lookup"><span data-stu-id="20393-278">No</span></span></p></td>
<td><p><span data-ttu-id="20393-279">失败会话的相对等级，根据受邀加入会话的用户确定。</span><span class="sxs-lookup"><span data-stu-id="20393-279">Relative ranking of failed sessions based on the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-280"><strong>主要来源用户</strong></span><span class="sxs-lookup"><span data-stu-id="20393-280"><strong>Top from users</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-281">否</span><span class="sxs-lookup"><span data-stu-id="20393-281">No</span></span></p></td>
<td><p><span data-ttu-id="20393-282">受邀加入会话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="20393-282">SIP address of the user invited to join the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-283"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-283"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-284">否</span><span class="sxs-lookup"><span data-stu-id="20393-284">No</span></span></p></td>
<td><p><span data-ttu-id="20393-285">每个用户的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-285">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-to-users"></a><span data-ttu-id="20393-286">主要目标用户的指标</span><span class="sxs-lookup"><span data-stu-id="20393-286">Metrics for Top To Users</span></span>

<span data-ttu-id="20393-287">下表列出了故障分布报告中基于其他人尝试呼叫的所遇故障最多的用户提供的信息，其他人尝试呼叫的用户称为“目标”用户。</span><span class="sxs-lookup"><span data-stu-id="20393-287">The following table lists the information provided in the Failure Distribution Report based on the users who experienced the most failures when another user tried to call them (known as "To" users).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-288">名称</span><span class="sxs-lookup"><span data-stu-id="20393-288">Name</span></span></th>
<th><span data-ttu-id="20393-289">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-289">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-290">描述</span><span class="sxs-lookup"><span data-stu-id="20393-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-291"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-291"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-292">否</span><span class="sxs-lookup"><span data-stu-id="20393-292">No</span></span></p></td>
<td><p><span data-ttu-id="20393-293">失败会话的相对等级，根据发起会话的用户确定。</span><span class="sxs-lookup"><span data-stu-id="20393-293">Relative ranking of failed sessions based on the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-294"><strong>主要目标用户</strong></span><span class="sxs-lookup"><span data-stu-id="20393-294"><strong>Top to users</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-295">否</span><span class="sxs-lookup"><span data-stu-id="20393-295">No</span></span></p></td>
<td><p><span data-ttu-id="20393-296">发起会话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="20393-296">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-297"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-297"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-298">否</span><span class="sxs-lookup"><span data-stu-id="20393-298">No</span></span></p></td>
<td><p><span data-ttu-id="20393-299">每个用户的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-299">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-user-agents"></a><span data-ttu-id="20393-300">主要用户代理的指标</span><span class="sxs-lookup"><span data-stu-id="20393-300">Metrics for Top User Agents</span></span>

<span data-ttu-id="20393-301">下表列出了故障分布报告中基于所遇故障最多的终结点软件提供的信息。</span><span class="sxs-lookup"><span data-stu-id="20393-301">The following table lists the information provided in the Failure Distribution Report based on the endpoint software that experienced the most failures.</span></span>

### <a name="metrics-for-top-user-agents"></a><span data-ttu-id="20393-302">主要用户代理的指标</span><span class="sxs-lookup"><span data-stu-id="20393-302">Metrics for Top User Agents</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20393-303">名称</span><span class="sxs-lookup"><span data-stu-id="20393-303">Name</span></span></th>
<th><span data-ttu-id="20393-304">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="20393-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="20393-305">描述</span><span class="sxs-lookup"><span data-stu-id="20393-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20393-306"><strong>等级</strong></span><span class="sxs-lookup"><span data-stu-id="20393-306"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-307">否</span><span class="sxs-lookup"><span data-stu-id="20393-307">No</span></span></p></td>
<td><p><span data-ttu-id="20393-p115">失败会话的相对等级，根据会话所涉及的用户代理（软件）确定。例如：RTCC/4.0.0.0 Inbound Routing/4.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="20393-p115">Relative ranking of failed sessions based on the user agent (software) involved in the session. For example: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20393-310"><strong>主要用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="20393-310"><strong>Top user agents</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-311">否</span><span class="sxs-lookup"><span data-stu-id="20393-311">No</span></span></p></td>
<td><p><span data-ttu-id="20393-312">失败会话所涉及的用户代理的名称。</span><span class="sxs-lookup"><span data-stu-id="20393-312">Name of the user agent involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20393-313"><strong>会话数</strong></span><span class="sxs-lookup"><span data-stu-id="20393-313"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="20393-314">否</span><span class="sxs-lookup"><span data-stu-id="20393-314">No</span></span></p></td>
<td><p><span data-ttu-id="20393-315">每个用户代理的失败会话总数。</span><span class="sxs-lookup"><span data-stu-id="20393-315">Total number of failed sessions per user agent.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="20393-316">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20393-316">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

