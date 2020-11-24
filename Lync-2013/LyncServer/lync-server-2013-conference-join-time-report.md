---
title: Lync Server 2013：会议加入时间报表
description: Lync Server 2013：会议加入时间报表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Join Time Report
ms:assetid: e64dc89a-25e4-4cb8-bcb1-51712e69ba5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205344(v=OCS.15)
ms:contentKeyID: 48185686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd4aa5d21a8109a323bb953c7196f43715d51413
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391939"
---
# <a name="conference-join-time-report-in-lync-server-2013"></a><span data-ttu-id="32bd8-103">Lync Server 2013 中的会议加入时间报表</span><span class="sxs-lookup"><span data-stu-id="32bd8-103">Conference Join Time Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32bd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32bd8-104">

<span> </span></span></span>

<span data-ttu-id="32bd8-105">_**主题上次修改时间：** 2014-04-23_</span><span class="sxs-lookup"><span data-stu-id="32bd8-105">_**Topic Last Modified:** 2014-04-23_</span></span>

<span data-ttu-id="32bd8-p101">会议加入时间摘要可使您确定用户要花多长时间才能加入会议。该报告显示平均加入时间（以毫秒计），同时提供一个细目，让您知道有多少用户在 2 秒或更少时间内加入了会议，有多少用户要求在 2 秒和 5 秒间加入会议等。</span><span class="sxs-lookup"><span data-stu-id="32bd8-p101">The Conference Join Time Summary enables you to determine how long it takes your users to join a conference. The report shows the average join time (in milliseconds), and also provides a breakdown that lets you know how many users were able to join a conference in 2 seconds or less, how many users required between 2 and 5 seconds to join the conference, and so on.</span></span>

<div>

## <a name="accessing-the-conference-join-time-report"></a><span data-ttu-id="32bd8-108">访问会议加入时间报告</span><span class="sxs-lookup"><span data-stu-id="32bd8-108">Accessing the Conference Join Time Report</span></span>

<span data-ttu-id="32bd8-109">可从监控报告主页访问会议加入时间报告。</span><span class="sxs-lookup"><span data-stu-id="32bd8-109">The Conference Join Time Report is accessed from the Monitoring Reports home page.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="32bd8-110">筛选器</span><span class="sxs-lookup"><span data-stu-id="32bd8-110">Filters</span></span>

<span data-ttu-id="32bd8-p102">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。下表列出了可用于会议加入时间报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="32bd8-p102">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Join Time Report.</span></span>

### <a name="conference-join-time-report-filters"></a><span data-ttu-id="32bd8-113">会议加入时间报告筛选器</span><span class="sxs-lookup"><span data-stu-id="32bd8-113">Conference Join Time Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32bd8-114">名称</span><span class="sxs-lookup"><span data-stu-id="32bd8-114">Name</span></span></th>
<th><span data-ttu-id="32bd8-115">描述</span><span class="sxs-lookup"><span data-stu-id="32bd8-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-116"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-116"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-p103">时间范围的开始日期/时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="32bd8-p103">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="32bd8-119">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="32bd8-119">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="32bd8-p104">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="32bd8-p104">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="32bd8-122">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="32bd8-122">7/7/2012</span></span></p>
<p><span data-ttu-id="32bd8-123">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="32bd8-123">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="32bd8-124">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="32bd8-124">7/3/2012</span></span></p>
<p><span data-ttu-id="32bd8-125">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="32bd8-125">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bd8-126"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-126"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-p105">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="32bd8-p105">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="32bd8-129">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="32bd8-129">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="32bd8-p106">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="32bd8-p106">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="32bd8-132">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="32bd8-132">7/7/2012</span></span></p>
<p><span data-ttu-id="32bd8-133">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="32bd8-133">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="32bd8-134">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="32bd8-134">7/3/2012</span></span></p>
<p><span data-ttu-id="32bd8-135">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="32bd8-135">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-136"><strong>间隔</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-136"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-p107">时间间隔。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="32bd8-p107">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="32bd8-139">每小时（最多可显示 25 个小时）</span><span class="sxs-lookup"><span data-stu-id="32bd8-139">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="32bd8-140">每天（最多可显示 31 天）</span><span class="sxs-lookup"><span data-stu-id="32bd8-140">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="32bd8-141">每周（最多可显示 12 周）</span><span class="sxs-lookup"><span data-stu-id="32bd8-141">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="32bd8-142">每月（最多可显示 12 个月）</span><span class="sxs-lookup"><span data-stu-id="32bd8-142">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="32bd8-143">如果开始日期和结束日期超出了所选间隔允许的最长时间，则仅显示最长时间（从开始日期开始）。</span><span class="sxs-lookup"><span data-stu-id="32bd8-143">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="32bd8-144">例如，如果选择 "开始日期 7/7/2012" 和 "结束日期 2/28/2012" 的 "每日间隔"，则会显示 8/7/2012 12:00 AM 至 9/7/2012 12:00 AM (的数据，即，总数据) 31 天。</span><span class="sxs-lookup"><span data-stu-id="32bd8-144">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bd8-145"><strong>池</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-145"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-p109">注册器池或边缘服务器的完全限定域名 (FQDN)。可以选择单个池，也可以单击“<strong>[所有]</strong>”查看所有池的数据。系统根据数据库中的记录自动为您填充该下拉列表。</span><span class="sxs-lookup"><span data-stu-id="32bd8-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-149"><strong>会议会话</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-149"><strong>Conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-p110">会话类型。允许的值包括：</span><span class="sxs-lookup"><span data-stu-id="32bd8-p110">Type of session. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="32bd8-152">[所有]</span><span class="sxs-lookup"><span data-stu-id="32bd8-152">[All]</span></span></p></li>
<li><p><span data-ttu-id="32bd8-153">焦点会话（“焦点”是联机会议的中央策略和状态管理者，负责协调会议的各个方面</span><span class="sxs-lookup"><span data-stu-id="32bd8-153">Focus sessions (the Focus is the central policy and state manager for online meetings and coordinates all aspects of A conference</span></span></p></li>
<li><p><span data-ttu-id="32bd8-154">应用程序共享</span><span class="sxs-lookup"><span data-stu-id="32bd8-154">Application sharing</span></span></p></li>
<li><p><span data-ttu-id="32bd8-155">A/V 会议</span><span class="sxs-lookup"><span data-stu-id="32bd8-155">A/V conferencing</span></span></p></li>
</ul>
<p><span data-ttu-id="32bd8-p111">如果选择 [所有]，则总会议加入时间将显示在报告的顶部。请注意，这些总数仅用于通过使用 Microsoft Exchange 或 Microsoft Outlook 安排的会议。</span><span class="sxs-lookup"><span data-stu-id="32bd8-p111">If you select [All], the total conference join time will be displayed at the top of the report. Note that these totals are only for conferences which were scheduled by using Microsoft Exchange or Microsoft Outlook.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="32bd8-158">指标</span><span class="sxs-lookup"><span data-stu-id="32bd8-158">Metrics</span></span>

<span data-ttu-id="32bd8-159">下表列出了会议加入时间报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="32bd8-159">The following table lists the information provided in the Conference Join Time Report.</span></span>

### <a name="conference-join-time-report-metrics"></a><span data-ttu-id="32bd8-160">会议加入时间报告标准</span><span class="sxs-lookup"><span data-stu-id="32bd8-160">Conference Join Time Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32bd8-161">名称</span><span class="sxs-lookup"><span data-stu-id="32bd8-161">Name</span></span></th>
<th><span data-ttu-id="32bd8-162">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="32bd8-162">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="32bd8-163">描述</span><span class="sxs-lookup"><span data-stu-id="32bd8-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-164"><strong>日期</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-164"><strong>Date</strong></span></span></p>
<p><span data-ttu-id="32bd8-165">此指标的实际标题完全取决于所选的间隔。</span><span class="sxs-lookup"><span data-stu-id="32bd8-165">The actual title for this metric will vary depending on the Interval that was selected.</span></span></p></td>
<td><p><span data-ttu-id="32bd8-166">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-166">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-167">会议发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="32bd8-167">Date and time that the conference took place.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bd8-168"><strong>会话总数</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-168"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-169">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-169">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-170">会话的总数，包括成功的会话、失败的会话（预期失败和意外失败）及未归类的会话。</span><span class="sxs-lookup"><span data-stu-id="32bd8-170">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-171"><strong>平均 (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-171"><strong>Average (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-172">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-172">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-173">参与者加入会议花费的平均时间量（以毫秒计）。</span><span class="sxs-lookup"><span data-stu-id="32bd8-173">Average amount of time (in milliseconds) that it took participants to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bd8-174"><strong>会话 &lt; 2 秒，卷</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-174"><strong>Sessions &lt; 2 seconds, Volume</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-175">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-175">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-176">在不到 2 秒的时间内加入会议的参与者的人数。</span><span class="sxs-lookup"><span data-stu-id="32bd8-176">Number of participants who were able to join the conference in less than 2 seconds.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-177"><strong>会话 &lt; 2 秒，百分比</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-177"><strong>Sessions &lt; 2 seconds, Percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-178">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-178">No</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bd8-179"><strong>会话 2-5 秒，量</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-179"><strong>Sessions 2-5 seconds, Volume</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-180">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-180">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-181">在 2 秒到 5 秒之间加入到会议参与者的人数。</span><span class="sxs-lookup"><span data-stu-id="32bd8-181">Number of participants who took between 2 seconds and 5 seconds to join the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-182"><strong>会话 2-5 秒，百分比</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-182"><strong>Sessions 2-5 seconds, Percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-183">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-183">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-184">在 2 秒到 5 秒间加入会议的总呼叫参与者的百分比。</span><span class="sxs-lookup"><span data-stu-id="32bd8-184">Percentage of the total call participants who took between 2 seconds and 5 seconds to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bd8-185"><strong>会话 5-10 秒，量</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-185"><strong>Sessions 5-10 seconds, Volume</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-186">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-186">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-187">在 5 秒到 10 秒之间加入到会议参与者的人数。</span><span class="sxs-lookup"><span data-stu-id="32bd8-187">Number of participants who took between 5 seconds and 10 seconds to join the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-188"><strong>会话 5-10 秒，百分比</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-188"><strong>Sessions 5-10 seconds, Percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-189">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-189">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-190">在 5 秒到 10 秒间加入会议的总呼叫参与者的百分比。</span><span class="sxs-lookup"><span data-stu-id="32bd8-190">Percentage of the total call participants who took between 5 seconds and 10 seconds to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bd8-191"><strong>会话 &gt; 10 秒，卷</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-191"><strong>Sessions &gt; 10 seconds, Volume</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-192">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-192">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-193">需要 10 秒之上加入会议的参与者人数。</span><span class="sxs-lookup"><span data-stu-id="32bd8-193">Number of participants who required more than 10 seconds to join the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bd8-194"><strong>会话 &gt; 10 秒，百分比</strong></span><span class="sxs-lookup"><span data-stu-id="32bd8-194"><strong>Sessions &gt; 10 seconds, Percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="32bd8-195">否</span><span class="sxs-lookup"><span data-stu-id="32bd8-195">No</span></span></p></td>
<td><p><span data-ttu-id="32bd8-196">需要 10 秒之上加入会议的总呼叫参与者百分比。</span><span class="sxs-lookup"><span data-stu-id="32bd8-196">Percentage of the total call participants who required more than 10 seconds to join the conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="32bd8-197">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32bd8-197">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

