---
title: Lync Server 2013：对等 IM 报表
description: Lync Server 2013：对等 IM 报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer IM Report
ms:assetid: 19ec0145-2398-437b-8989-f780c179b798
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558620(v=OCS.15)
ms:contentKeyID: 48183533
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eac6291d0f099af8269ed15f7dc8c654ac944ed0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424680"
---
# <a name="peer-to-peer-im-report-in-lync-server-2013"></a><span data-ttu-id="383b1-103">Lync Server 2013 中的对等 IM 报表</span><span class="sxs-lookup"><span data-stu-id="383b1-103">Peer-to-Peer IM Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="383b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="383b1-104">

<span> </span></span></span>

<span data-ttu-id="383b1-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="383b1-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="383b1-p101">对等 IM 报告提供了有关按池和身份验证类型分类的对等即时消息 (IM) 会话的趋势信息。该报告可以显示在指定时间段内（例如，每天或每小时）进行的会话总数或显示在该时间段内发送的即时消息总数。</span><span class="sxs-lookup"><span data-stu-id="383b1-p101">The Peer-to-Peer IM Report provides trend information about peer-to-peer instant messaging (IM) sessions, broken down by pool and by authentication type. The report can show either the total number of sessions held during the specified time period (for example, day-by-day or hour-by-hour), or it can show the total number of instant messages sent during that time period.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-im-report"></a><span data-ttu-id="383b1-108">访问对等 IM 报告</span><span class="sxs-lookup"><span data-stu-id="383b1-108">Accessing the Peer-to-Peer IM Report</span></span>

<span data-ttu-id="383b1-109">只有 [在 Lync Server 2013 中打开 "对等活动摘要" 报表](lync-server-2013-peer-to-peer-activity-summary-report.md) ，然后单击以下任一度量值，才能访问对等 IM 报表：</span><span class="sxs-lookup"><span data-stu-id="383b1-109">You can access the Peer-to-Peer IM Report only by opening the [Peer-to-Peer Activity Summary Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md) and then clicking either of the following metrics:</span></span>

  - <span data-ttu-id="383b1-110">对等 IM 会话总数</span><span class="sxs-lookup"><span data-stu-id="383b1-110">Total peer-to-peer IM sessions</span></span>

  - <span data-ttu-id="383b1-111">对等 IM 消息总数</span><span class="sxs-lookup"><span data-stu-id="383b1-111">Total peer-to-peer IM messages</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-im-report"></a><span data-ttu-id="383b1-112">充分利用对等 IM 报告</span><span class="sxs-lookup"><span data-stu-id="383b1-112">Making the Best Use of the Peer-to-Peer IM Report</span></span>

<span data-ttu-id="383b1-p102">默认情况下，对等 IM 报告显示每小时（或每天，具体取决于设置）的消息计数。但是，还可以选择按每小时会话数来查看日期。为此，请单击“报告”窗口右上角的“**隐藏/显示参数**”，然后从“**报告依据**”列表中单击“**会话计数**”。</span><span class="sxs-lookup"><span data-stu-id="383b1-p102">By default, the Peer-to-Peer IM Report shows you the message count per-hour (or day, depending on your settings). However, you can also choose to view the day by sessions per hour. To do that, click **Hide/Show Parameters** in the upper-right corner of the Reports window, and then click **Session Count** from the **Report by** list.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="383b1-116">筛选器</span><span class="sxs-lookup"><span data-stu-id="383b1-116">Filters</span></span>

<span data-ttu-id="383b1-p103">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。下表列出了可用于对等 IM 报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="383b1-p103">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Peer-to-Peer IM Report.</span></span>

### <a name="peer-to-peer-im-report-filters"></a><span data-ttu-id="383b1-119">对等 IM 报告筛选器</span><span class="sxs-lookup"><span data-stu-id="383b1-119">Peer-to-Peer IM Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="383b1-120">名称</span><span class="sxs-lookup"><span data-stu-id="383b1-120">Name</span></span></th>
<th><span data-ttu-id="383b1-121">描述</span><span class="sxs-lookup"><span data-stu-id="383b1-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="383b1-122"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-122"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-p104">时间范围的开始日期和时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="383b1-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="383b1-125">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="383b1-125">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="383b1-p105">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="383b1-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="383b1-128">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="383b1-128">7/7/2012</span></span></p>
<p><span data-ttu-id="383b1-129">若要按周或按月查看，请输入周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="383b1-129">To view by week or by month, enter a date that falls anywhere within the week or month (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="383b1-130">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="383b1-130">7/3/2012</span></span></p>
<p><span data-ttu-id="383b1-131">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="383b1-131">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="383b1-132"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-132"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-p106">时间范围的结束日期和时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="383b1-p106">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="383b1-135">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="383b1-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="383b1-p107">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="383b1-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="383b1-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="383b1-138">7/7/2012</span></span></p>
<p><span data-ttu-id="383b1-139">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="383b1-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="383b1-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="383b1-140">7/3/2012</span></span></p>
<p><span data-ttu-id="383b1-141">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="383b1-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="383b1-142"><strong>间隔</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-142"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-p108">时间间隔。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="383b1-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="383b1-145">每小时（最多可显示 25 个小时）</span><span class="sxs-lookup"><span data-stu-id="383b1-145">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="383b1-146">每天（最多可显示 31 天）</span><span class="sxs-lookup"><span data-stu-id="383b1-146">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="383b1-147">每周（最多可显示 12 周）</span><span class="sxs-lookup"><span data-stu-id="383b1-147">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="383b1-148">每月（最多可显示 12 个月）</span><span class="sxs-lookup"><span data-stu-id="383b1-148">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="383b1-149">如果开始日期和结束日期超出了所选间隔允许的最长时间，则仅显示最长时间（从开始日期开始）。</span><span class="sxs-lookup"><span data-stu-id="383b1-149">If the start and end dates exceed the maximum number of values allowed for the selected interval then only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="383b1-150">例如，如果选择 "开始日期 7/7/2012" 和 "结束日期 2/28/2012" 的 "每日间隔"，则会显示 8/7/2012 12:00 AM 至 9/7/2012 12:00 AM (的数据，即，总数据) 31 天。</span><span class="sxs-lookup"><span data-stu-id="383b1-150">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="383b1-151"><strong>报告依据</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-151"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-p110">指示要在报告中使用的值。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="383b1-p110">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="383b1-154">会话计数</span><span class="sxs-lookup"><span data-stu-id="383b1-154">Session count</span></span></p></li>
<li><p><span data-ttu-id="383b1-155">消息计数</span><span class="sxs-lookup"><span data-stu-id="383b1-155">Message count</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-im-session-by-pool"></a><span data-ttu-id="383b1-156">按池列出的对等 IM 会话的指标</span><span class="sxs-lookup"><span data-stu-id="383b1-156">Metrics for Peer-to-Peer IM Session by Pool</span></span>

<span data-ttu-id="383b1-157">下表列出了对等 IM 报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="383b1-157">The following table lists the information provided in the Peer-to-Peer IM Report.</span></span>

### <a name="metrics-for-peer-to-peer-im-session-by-pool"></a><span data-ttu-id="383b1-158">按池列出的对等 IM 会话的指标</span><span class="sxs-lookup"><span data-stu-id="383b1-158">Metrics for Peer-to-Peer IM Session by Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="383b1-159">名称</span><span class="sxs-lookup"><span data-stu-id="383b1-159">Name</span></span></th>
<th><span data-ttu-id="383b1-160">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="383b1-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="383b1-161">描述</span><span class="sxs-lookup"><span data-stu-id="383b1-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="383b1-162"><strong>池</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-162"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-163">否</span><span class="sxs-lookup"><span data-stu-id="383b1-163">No</span></span></p></td>
<td><p><span data-ttu-id="383b1-164">注册机构池或边缘服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="383b1-164">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="383b1-165"><strong>日期/时间</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-165"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-166">否</span><span class="sxs-lookup"><span data-stu-id="383b1-166">No</span></span></p></td>
<td><p><span data-ttu-id="383b1-167">会话发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="383b1-167">Date and time that the sessions took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="383b1-168"><strong>总计</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-168"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-169">否</span><span class="sxs-lookup"><span data-stu-id="383b1-169">No</span></span></p></td>
<td><p><span data-ttu-id="383b1-170">会话总数或消息总数。</span><span class="sxs-lookup"><span data-stu-id="383b1-170">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-im-session-by-authentication-type"></a><span data-ttu-id="383b1-171">按身份验证类型列出的对等 IM 会话的指标</span><span class="sxs-lookup"><span data-stu-id="383b1-171">Metrics for Peer-to-Peer IM Session by Authentication Type</span></span>

<span data-ttu-id="383b1-172">下表列出了对等会话中的参与者所用各个身份验证类型的对等 IM 报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="383b1-172">The following table lists the information provided in the Peer-to-Peer IM Report for each type of authentication used by the participants in a peer-to-peer session.</span></span>

### <a name="metrics-for-peer-to-peer-im-session-by-authentication-type"></a><span data-ttu-id="383b1-173">按身份验证类型列出的对等 IM 会话的指标</span><span class="sxs-lookup"><span data-stu-id="383b1-173">Metrics for Peer-to-Peer IM Session by Authentication Type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="383b1-174">名称</span><span class="sxs-lookup"><span data-stu-id="383b1-174">Name</span></span></th>
<th><span data-ttu-id="383b1-175">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="383b1-175">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="383b1-176">描述</span><span class="sxs-lookup"><span data-stu-id="383b1-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="383b1-177"><strong>身份验证类型</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-177"><strong>Authentication type</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-178">否</span><span class="sxs-lookup"><span data-stu-id="383b1-178">No</span></span></p></td>
<td><p><span data-ttu-id="383b1-p111">会话参与者使用的身份验证的类型。通常可指定下列值之一：</span><span class="sxs-lookup"><span data-stu-id="383b1-p111">Type of authentication used by the session participants. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="383b1-181">Enterprise</span><span class="sxs-lookup"><span data-stu-id="383b1-181">Enterprise</span></span></p></li>
<li><p><span data-ttu-id="383b1-182">Federated</span><span class="sxs-lookup"><span data-stu-id="383b1-182">Federated</span></span></p></li>
<li><p><span data-ttu-id="383b1-183">PIC</span><span class="sxs-lookup"><span data-stu-id="383b1-183">PIC</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="383b1-184"><strong>日期/时间</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-185">否</span><span class="sxs-lookup"><span data-stu-id="383b1-185">No</span></span></p></td>
<td><p><span data-ttu-id="383b1-186">会话发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="383b1-186">Date and time that the sessions took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="383b1-187"><strong>总计</strong></span><span class="sxs-lookup"><span data-stu-id="383b1-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="383b1-188">否</span><span class="sxs-lookup"><span data-stu-id="383b1-188">No</span></span></p></td>
<td><p><span data-ttu-id="383b1-189">会话总数或消息总数。</span><span class="sxs-lookup"><span data-stu-id="383b1-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="383b1-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="383b1-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

