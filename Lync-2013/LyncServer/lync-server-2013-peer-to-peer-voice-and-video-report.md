---
title: Lync Server 2013：对等语音和视频报告
description: Lync Server 2013：对等语音和视频报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Voice and Video Report
ms:assetid: e17c36b5-5a2f-4673-9696-3b2d31c2bb2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615040(v=OCS.15)
ms:contentKeyID: 48185535
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43041926b3d6b57508b6ee4c53ca9cb055bcb348
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424683"
---
# <a name="peer-to-peer-voice-and-video-report-in-lync-server-2013"></a><span data-ttu-id="cce13-103">Lync Server 2013 中的对等语音和视频报告</span><span class="sxs-lookup"><span data-stu-id="cce13-103">Peer-to-Peer Voice and Video Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cce13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cce13-104">

<span> </span></span></span>

<span data-ttu-id="cce13-105">_**主题上次修改时间：** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="cce13-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="cce13-p101">对等语音和视频报告提供了指定时间段的语音和视频呼叫分布的详细信息（例如，按小时的呼叫或按每天的呼叫）。该报告还为您提供查看所有执行的语音和视频呼叫的选项或仅查看成功或失败呼叫的选项。这些报告显示细分为下列组的呼叫信息：</span><span class="sxs-lookup"><span data-stu-id="cce13-p101">The Peer-to-Peer Voice and Video Report provides a detailed look at the distribution of voice and video calls over a specified period of time (for example, calls per hour or calls per day). The report also gives you the option of viewing all the voice and video calls that were made, or of viewing only the successful or failed calls. The reports shows call information broken down into the following groupings:</span></span>

  - <span data-ttu-id="cce13-109">按池的呼叫</span><span class="sxs-lookup"><span data-stu-id="cce13-109">Calls per pool</span></span>

  - <span data-ttu-id="cce13-110">每个呼叫类型的呼叫 (例如，Lync to Lync 呼叫与 PSTN 网络上的某个人的 lync 呼叫) </span><span class="sxs-lookup"><span data-stu-id="cce13-110">Calls per call type (for example, a Lync to Lync call vs. a Lync call to a person on the PSTN network)</span></span>

  - <span data-ttu-id="cce13-111">按访问类型的呼叫（登录到内部网络上的用户与登录到外部网络上的用户）</span><span class="sxs-lookup"><span data-stu-id="cce13-111">Calls per access type (users logged on to the internal network vs. users logged on to the external network)</span></span>

  - <span data-ttu-id="cce13-112">每个中介服务器的通话</span><span class="sxs-lookup"><span data-stu-id="cce13-112">Calls per Mediation Server</span></span>

<div>

## <a name="to-access-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="cce13-113">访问对等语音和视频报告</span><span class="sxs-lookup"><span data-stu-id="cce13-113">To access the peer-to-peer voice and video report</span></span>

<span data-ttu-id="cce13-114">只需打开对等活动摘要报告，然后单击下列任意指标，即可访问对等语音和视频报告：</span><span class="sxs-lookup"><span data-stu-id="cce13-114">You can access the Peer-to-Peer Voice and Video Report only by opening the Peer-to-Peer Activity Summary Report and then clicking any of the following metrics:</span></span>

  - <span data-ttu-id="cce13-115">对等音频会话总数</span><span class="sxs-lookup"><span data-stu-id="cce13-115">Total peer-to-peer audio sessions</span></span>

  - <span data-ttu-id="cce13-116">对等音频总分钟数</span><span class="sxs-lookup"><span data-stu-id="cce13-116">Total peer-to-peer audio minutes</span></span>

  - <span data-ttu-id="cce13-117">对等视频会话总数</span><span class="sxs-lookup"><span data-stu-id="cce13-117">Total peer-to-peer video sessions</span></span>

  - <span data-ttu-id="cce13-118">对等视频总分钟数</span><span class="sxs-lookup"><span data-stu-id="cce13-118">Total peer-to-peer video minutes</span></span>

</div>

<div>

## <a name="to-make-the-best-use-of-the-peer-to-peer-voice-and-video-report"></a><span data-ttu-id="cce13-119">更好地使用对等语音和视频报告</span><span class="sxs-lookup"><span data-stu-id="cce13-119">To make the best use of the peer-to-peer voice and video report</span></span>

<span data-ttu-id="cce13-p102">有多种方法可供筛选对等语音和视频报告。但是，默认情况下这些筛选选项处于隐藏状态，无法查看。要查看为您提供的筛选选项，请单击报告窗口右上角的“**显示/隐藏参数**”按钮。</span><span class="sxs-lookup"><span data-stu-id="cce13-p102">There are a number of ways you can filter the Peer-to-Peer Voice and Video Report. However, those filtering options are hidden from view by default. To view the filtering options available to you, click **Show/Hide Parameters** button in the upper-right corner of the Report window.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="cce13-123">筛选器</span><span class="sxs-lookup"><span data-stu-id="cce13-123">Filters</span></span>

<span data-ttu-id="cce13-p103">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方法查看数据。下表列出了可用于对等语音和视频报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="cce13-p103">Filters provide a way for you to return a more finely targeted set of data or to view the data in different ways. The following table lists the filters that you can use with the Peer-to-Peer Voice and Video Report.</span></span>

### <a name="peer-to-peer-voice-and-video-report-filters"></a><span data-ttu-id="cce13-126">对等语音和视频报告筛选器</span><span class="sxs-lookup"><span data-stu-id="cce13-126">Peer-to-peer voice and video report filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cce13-127">名称</span><span class="sxs-lookup"><span data-stu-id="cce13-127">Name</span></span></th>
<th><span data-ttu-id="cce13-128">描述</span><span class="sxs-lookup"><span data-stu-id="cce13-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cce13-129"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-129"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-p104">时间范围的开始日期和时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="cce13-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="cce13-132">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="cce13-132">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="cce13-p105">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="cce13-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="cce13-135">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="cce13-135">7/7/2012</span></span></p>
<p><span data-ttu-id="cce13-136">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="cce13-136">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="cce13-137">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="cce13-137">7/3/2012</span></span></p>
<p><span data-ttu-id="cce13-138">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="cce13-138">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cce13-139"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-139"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-p106">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="cce13-p106">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="cce13-142">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="cce13-142">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="cce13-p107">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="cce13-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="cce13-145">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="cce13-145">7/7/2012</span></span></p>
<p><span data-ttu-id="cce13-146">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="cce13-146">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="cce13-147">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="cce13-147">7/3/2012</span></span></p>
<p><span data-ttu-id="cce13-148">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="cce13-148">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cce13-149"><strong>间隔</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-149"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-p108">时间间隔。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="cce13-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="cce13-152">每小时（最多可显示 25 个小时）</span><span class="sxs-lookup"><span data-stu-id="cce13-152">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="cce13-153">每天（最多可显示 31 天）</span><span class="sxs-lookup"><span data-stu-id="cce13-153">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="cce13-154">每周（最多可显示 12 周）</span><span class="sxs-lookup"><span data-stu-id="cce13-154">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="cce13-155">每月（最多可显示 12 个月）</span><span class="sxs-lookup"><span data-stu-id="cce13-155">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="cce13-156">如果开始日期和结束日期超出了所选间隔允许的最长时间，则仅显示最长时间（从开始日期开始）。</span><span class="sxs-lookup"><span data-stu-id="cce13-156">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="cce13-157">例如，如果选择 "开始日期 7/7/2012" 和 "结束日期 2/28/2012" 的 "每日间隔"，则会显示 8/7/2012 12:00 AM 至 9/7/2012 12:00 AM (的数据，即，总数据) 31 天。</span><span class="sxs-lookup"><span data-stu-id="cce13-157">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cce13-158"><strong>媒体类型</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-158"><strong>Media type</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-p110">指示会话中使用的媒体的类型。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="cce13-p110">Indicates the type of media used in the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="cce13-161">两者</span><span class="sxs-lookup"><span data-stu-id="cce13-161">Both</span></span></p></li>
<li><p><span data-ttu-id="cce13-162">音频</span><span class="sxs-lookup"><span data-stu-id="cce13-162">Audio</span></span></p></li>
<li><p><span data-ttu-id="cce13-163">视频</span><span class="sxs-lookup"><span data-stu-id="cce13-163">Video</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cce13-164"><strong>呼叫处置</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-164"><strong>Call disposition</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-p111">指示会话是成功还是失败。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="cce13-p111">Indicates the success or failure of the session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="cce13-167">[所有]</span><span class="sxs-lookup"><span data-stu-id="cce13-167">[All]</span></span></p></li>
<li><p><span data-ttu-id="cce13-168">成功的呼叫</span><span class="sxs-lookup"><span data-stu-id="cce13-168">Success Calls</span></span></p></li>
<li><p><span data-ttu-id="cce13-169">失败的呼叫</span><span class="sxs-lookup"><span data-stu-id="cce13-169">Failed Calls</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cce13-170"><strong>报告依据</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-170"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-p112">指示要在报告中使用的值。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="cce13-p112">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="cce13-173">会话计数</span><span class="sxs-lookup"><span data-stu-id="cce13-173">Session count</span></span></p></li>
<li><p><span data-ttu-id="cce13-174">呼叫分钟数</span><span class="sxs-lookup"><span data-stu-id="cce13-174">Call minutes</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="cce13-175">按池列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-175">Metrics for peer-to-peer voice and video activity by Pool</span></span>

<span data-ttu-id="cce13-176">下表列出了每个池的对等语音和视频报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="cce13-176">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each pool.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-pool"></a><span data-ttu-id="cce13-177">按池列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-177">Metrics for peer-to-peer voice and video activity by pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cce13-178">名称</span><span class="sxs-lookup"><span data-stu-id="cce13-178">Name</span></span></th>
<th><span data-ttu-id="cce13-179">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="cce13-179">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="cce13-180">描述</span><span class="sxs-lookup"><span data-stu-id="cce13-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cce13-181"><strong>池</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-181"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-182">否</span><span class="sxs-lookup"><span data-stu-id="cce13-182">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-183">用于呼叫的注册机构池或边缘服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="cce13-183">Name of the Registrar pool or Edge Server used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cce13-184"><strong>日期/时间</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-185">否</span><span class="sxs-lookup"><span data-stu-id="cce13-185">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-186">进行呼叫的日期和时间段。</span><span class="sxs-lookup"><span data-stu-id="cce13-186">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cce13-187"><strong>总计</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-188">否</span><span class="sxs-lookup"><span data-stu-id="cce13-188">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-189">会话总数或消息总数。</span><span class="sxs-lookup"><span data-stu-id="cce13-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="cce13-190">按呼叫类型列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-190">Metrics for peer-to-peer voice and video activity by call type</span></span>

<span data-ttu-id="cce13-191">下表列出了发起的每种呼叫类型的对等语音和视频报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="cce13-191">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each type of call that was made.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-call-type"></a><span data-ttu-id="cce13-192">按呼叫类型列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-192">Metrics for peer-to-peer voice and video activity by call type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cce13-193">名称</span><span class="sxs-lookup"><span data-stu-id="cce13-193">Name</span></span></th>
<th><span data-ttu-id="cce13-194">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="cce13-194">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="cce13-195">描述</span><span class="sxs-lookup"><span data-stu-id="cce13-195">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cce13-196"><strong>呼叫类型</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-196"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-197">否</span><span class="sxs-lookup"><span data-stu-id="cce13-197">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-p113">指示发起的呼叫类型。可以指定下列值之一：</span><span class="sxs-lookup"><span data-stu-id="cce13-p113">Indicates the type of call that was made. Values are one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="cce13-200">UC 到 UC</span><span class="sxs-lookup"><span data-stu-id="cce13-200">UC-to-UC</span></span></p></li>
<li><p><span data-ttu-id="cce13-201">UC 到 PSTN</span><span class="sxs-lookup"><span data-stu-id="cce13-201">UC-to-PSTN</span></span></p></li>
<li><p><span data-ttu-id="cce13-202">PSTN 到 UC</span><span class="sxs-lookup"><span data-stu-id="cce13-202">PSTN-to-UC</span></span></p></li>
<li><p><span data-ttu-id="cce13-203">PSTN 到 PSTN</span><span class="sxs-lookup"><span data-stu-id="cce13-203">PSTN-to-PSTN</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cce13-204"><strong>日期/时间</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-204"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-205">否</span><span class="sxs-lookup"><span data-stu-id="cce13-205">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-206">进行呼叫的日期和时间段。</span><span class="sxs-lookup"><span data-stu-id="cce13-206">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cce13-207"><strong>总计</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-207"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-208">否</span><span class="sxs-lookup"><span data-stu-id="cce13-208">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-209">会话总数或消息总数。</span><span class="sxs-lookup"><span data-stu-id="cce13-209">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="cce13-210">按访问类型列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-210">Metrics for peer-to-peer voice and video activity by access type</span></span>

<span data-ttu-id="cce13-211">下表列出了每种网络访问类型的对等语音和视频报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="cce13-211">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each network access type.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-access-type"></a><span data-ttu-id="cce13-212">按访问类型列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-212">Metrics for peer-to-peer voice and video activity by access type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cce13-213">名称</span><span class="sxs-lookup"><span data-stu-id="cce13-213">Name</span></span></th>
<th><span data-ttu-id="cce13-214">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="cce13-214">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="cce13-215">描述</span><span class="sxs-lookup"><span data-stu-id="cce13-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cce13-216"><strong>活动类型</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-216"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-217">否</span><span class="sxs-lookup"><span data-stu-id="cce13-217">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-p114">指示客户端在发起呼叫时已登录到内部网络还是外部网络。通常可指定下列值之一：</span><span class="sxs-lookup"><span data-stu-id="cce13-p114">Indicates whether the clients were logged on to the internal network or the external network when the call was placed. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="cce13-220">内部</span><span class="sxs-lookup"><span data-stu-id="cce13-220">Internal</span></span></p></li>
<li><p><span data-ttu-id="cce13-221">外部</span><span class="sxs-lookup"><span data-stu-id="cce13-221">External</span></span></p></li>
<li><p><span data-ttu-id="cce13-222">混合</span><span class="sxs-lookup"><span data-stu-id="cce13-222">Mixed</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cce13-223"><strong>日期/时间</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-223"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-224">否</span><span class="sxs-lookup"><span data-stu-id="cce13-224">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-225">进行呼叫的日期和时间段。</span><span class="sxs-lookup"><span data-stu-id="cce13-225">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cce13-226"><strong>总计</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-226"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-227">否</span><span class="sxs-lookup"><span data-stu-id="cce13-227">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-228">会话总数或消息总数。</span><span class="sxs-lookup"><span data-stu-id="cce13-228">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="cce13-229">按中介服务器列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-229">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<span data-ttu-id="cce13-230">下表列出了针对每个中介服务器的对等语音和视频报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="cce13-230">The following table lists the information provided in the Peer-to-Peer Voice and Video Report for each Mediation Server.</span></span>

### <a name="metrics-for-peer-to-peer-voice-and-video-activity-by-mediation-server"></a><span data-ttu-id="cce13-231">按中介服务器列出的对等语音和视频活动的指标</span><span class="sxs-lookup"><span data-stu-id="cce13-231">Metrics for peer-to-peer voice and video activity by mediation server</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cce13-232">名称</span><span class="sxs-lookup"><span data-stu-id="cce13-232">Name</span></span></th>
<th><span data-ttu-id="cce13-233">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="cce13-233">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="cce13-234">描述</span><span class="sxs-lookup"><span data-stu-id="cce13-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cce13-235"><strong>中介服务器</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-235"><strong>Mediation Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-236">否</span><span class="sxs-lookup"><span data-stu-id="cce13-236">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-237">中介服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="cce13-237">Name of the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cce13-238"><strong>日期/时间</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-238"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-239">否</span><span class="sxs-lookup"><span data-stu-id="cce13-239">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-240">进行呼叫的日期和时间段。</span><span class="sxs-lookup"><span data-stu-id="cce13-240">Date and time period in which the call took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cce13-241"><strong>总计</strong></span><span class="sxs-lookup"><span data-stu-id="cce13-241"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="cce13-242">否</span><span class="sxs-lookup"><span data-stu-id="cce13-242">No</span></span></p></td>
<td><p><span data-ttu-id="cce13-243">会话总数或消息总数。</span><span class="sxs-lookup"><span data-stu-id="cce13-243">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cce13-244">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cce13-244">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

