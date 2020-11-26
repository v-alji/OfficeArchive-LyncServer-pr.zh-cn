---
title: Lync Server 2013：用户活动报表
description: Lync Server 2013：用户活动报表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User Activity Report
ms:assetid: 3aa6fef2-ea02-4f0f-93e8-fa2e0a953d79
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558638(v=OCS.15)
ms:contentKeyID: 48183862
ms.date: 02/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e959020e6ace6c72ecd570039d30a9ecc174c82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440792"
---
# <a name="user-activity-report-in-lync-server-2013"></a><span data-ttu-id="84638-103">Lync Server 2013 中的用户活动报表</span><span class="sxs-lookup"><span data-stu-id="84638-103">User Activity Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="84638-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="84638-104">

<span> </span></span></span>

<span data-ttu-id="84638-105">_**主题上次修改时间：** 2015-02-27_</span><span class="sxs-lookup"><span data-stu-id="84638-105">_**Topic Last Modified:** 2015-02-27_</span></span>

<span data-ttu-id="84638-p101">用户活动报告提供了由用户在给定时间段内执行的对等会话和会议会话的详细列表。与很多监控报告不同，用户活动报告会将每个呼叫与单个用户绑定。例如，对等会话指定发起呼叫（源用户）的人员以及被呼叫（目标用户）的人员的 SIP URI。如果展开会议的信息，则会看到所有会议参与者及其在该会议中担任的角色的列表。</span><span class="sxs-lookup"><span data-stu-id="84638-p101">The User Activity Report provides a detailed list of the peer-to-peer and conferencing sessions carried out by your users in a given time period. Unlike many of the Monitoring Reports, the User Activity Report ties each call to individual users. For example, peer-to-peer sessions specify the SIP URIs of the person who initiated the call (the From user) and the person who was being called (the To user). If you expand the information for a conference, you'll see a list of all the conference participants and the role they held for that conference.</span></span>

<span data-ttu-id="84638-p102">用户活动报告有时候称为“技术支持”报告。这是因为该报告通常由技术支持人员用于检索特定用户的会话信息。您可以筛选来自或发往单个用户的呼叫，只需在“用户 URI”前缀框中键入该用户的 SIP URI 即可。</span><span class="sxs-lookup"><span data-stu-id="84638-p102">The User Activity Report is sometimes referred to as the "help desk" report. That's because the report is often used by help desk personnel to retrieve session information for a specific user. You can filter for calls made to or made by an individual user simply by typing the user's SIP URI in the User URI prefix box.</span></span>

<span data-ttu-id="84638-113">如果执行此操作，则用户活动报表将返回其 SIP URI 以指定字符串开头的任何用户的信息。</span><span class="sxs-lookup"><span data-stu-id="84638-113">If you do this, the User Activity Report will return information for any user whose SIP URI begins with the specified string.</span></span> <span data-ttu-id="84638-114">例如，如果您在 URI 框中键入 **ken**，则用户活动报告将查找 **Ken**.Myer@litwareinc.com。</span><span class="sxs-lookup"><span data-stu-id="84638-114">For example, if you type **ken** in the URI box, the User Activity Report will locate **Ken**.Myer@litwareinc.com.</span></span> <span data-ttu-id="84638-115">但是，它还会查找以下用户：</span><span class="sxs-lookup"><span data-stu-id="84638-115">However, it will also locate these users:</span></span>

  - <span data-ttu-id="84638-116">**ken** azi@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="84638-116">**ken** azi@litwareinc.com</span></span>

  - <span data-ttu-id="84638-117">**ken** burg@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="84638-117">**ken** burg@litwareinc.com</span></span>

  - <span data-ttu-id="84638-118">**Ken**.Sanchez@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="84638-118">**Ken**.Sanchez@litwareinc.com</span></span>

  - <span data-ttu-id="84638-119">**Ken** nedy@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="84638-119">**Ken** nedy@litwareinc.com</span></span>

<span data-ttu-id="84638-p104">为确保仅返回 Ken Myer 的信息，请在搜索框中键入其完整的 URI (Ken.Myer@litwareinc.com)，或者至少键入 Ken 的 URI 的类型以将其与您所在组织中的其他用户区分开来。例如：</span><span class="sxs-lookup"><span data-stu-id="84638-p104">To ensure that information only for Ken Myer is returned, either type his full URI (Ken.Myer@litwareinc.com) in the search box or at least enough type of Ken’s URI to uniquely distinguish him from other users in your organization. For example:</span></span>

<span data-ttu-id="84638-122">Ken.my</span><span class="sxs-lookup"><span data-stu-id="84638-122">Ken.my</span></span>

<div>

## <a name="to-access-the-user-activity-report"></a><span data-ttu-id="84638-123">访问用户活动报告</span><span class="sxs-lookup"><span data-stu-id="84638-123">To access the user activity report</span></span>

<span data-ttu-id="84638-124">用户活动报告是从“监控报告”主页访问的。</span><span class="sxs-lookup"><span data-stu-id="84638-124">The User Activity Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="84638-125">您也可以通过单击 [Lync Server 2013 中的 "IP 电话清点" 报表](lync-server-2013-ip-phone-inventory-report.md)上的用户 URI 指标来访问用户活动报表。</span><span class="sxs-lookup"><span data-stu-id="84638-125">You can also reach the User Activity Report by clicking the User URI metric on the [IP Phone Inventory Report in Lync Server 2013](lync-server-2013-ip-phone-inventory-report.md).</span></span> <span data-ttu-id="84638-126">在用户活动报告中，单击“会议 URI”（针对会议）会将您转到会议详细信息报告。</span><span class="sxs-lookup"><span data-stu-id="84638-126">From within the User Activity Report, clicking the Conference URI (for a conference) takes you to the Conference Detail Report.</span></span> <span data-ttu-id="84638-127">同样，单击对等呼叫的详细指标将转到 [Lync Server 2013 中的对等会话详细信息报告](lync-server-2013-peer-to-peer-session-detail-report.md)。</span><span class="sxs-lookup"><span data-stu-id="84638-127">Similarly, clicking the Detail metric for a peer-to-peer call takes you to the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md).</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-user-activity-report"></a><span data-ttu-id="84638-128">充分利用用户活动报告</span><span class="sxs-lookup"><span data-stu-id="84638-128">Making the best use of the user activity report</span></span>

<span data-ttu-id="84638-129">尽管用户活动报告中有很多有用的信息，但这些信息有时候可能很难找到。</span><span class="sxs-lookup"><span data-stu-id="84638-129">Although there is a lot of good information in the User Activity Report, that information can sometimes be difficult to locate.</span></span> <span data-ttu-id="84638-130">例如，在指定期间内，你的组织中发生的所有用户活动均包括在用户活动报表中;这意味着，隐藏在报表内是有关哪些用户在某些方面实际使用过 Microsoft Lync Server 2013 的信息。</span><span class="sxs-lookup"><span data-stu-id="84638-130">For example, all the user activity that takes place in your organization during a specified period is included in the User Activity Report; that means that, buried, within the report is information about which users actually used Microsoft Lync Server 2013 in some way.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="84638-131">从技术上讲，某些用户活动可能会 unrecorded：尽管 Lync Server 努力保留有关所有电话呼叫的信息，但如果没有有关该调用的信息正在写入数据库，则可能会进行呼叫。</span><span class="sxs-lookup"><span data-stu-id="84638-131">Technically, it’s possible that some user activity might go unrecorded: while Lync Server strives to keep information about all phone calls it's possible that a call could have been made without the information about that call being written to the database.</span></span> <span data-ttu-id="84638-132">Lync Server 旨在提供极其准确但不一定完全了解 Lync Server 2013 的使用方法。</span><span class="sxs-lookup"><span data-stu-id="84638-132">Lync Server is designed to give an extremely accurate but not necessarily perfect look at how Lync Server 2013 is being used.</span></span> <span data-ttu-id="84638-133"> (不保证所有通话通话的100% 将解释为什么不应将 Lync 服务器监视用作帐单系统。 ) </span><span class="sxs-lookup"><span data-stu-id="84638-133">(The fact that there is no guarantee that 100% of all calls are recorded explains why Lync Server monitoring should not be used as a billing system.)</span></span><BR><span data-ttu-id="84638-134">第二，监视报告报告最多只能显示1000条记录。</span><span class="sxs-lookup"><span data-stu-id="84638-134">Second, a Monitoring Report report can only display, at most, 1,000 records.</span></span> <span data-ttu-id="84638-135">根据您具有的用户活动的数量以及您工作的时间段，这意味着您的查询可能无法返回数据库中实际存储的所有数据。</span><span class="sxs-lookup"><span data-stu-id="84638-135">Depending on the amount of user activity you have, and depending on the time period you are working with, that means your query might not return all the data actually stored in the database.</span></span>



</div>

  - <span data-ttu-id="84638-136">哪些用户在此时间段内实际上使用了系统？</span><span class="sxs-lookup"><span data-stu-id="84638-136">Which users actually used the system during this time period?</span></span>

  - <span data-ttu-id="84638-137">我的哪些用户在此时间段内最活跃？</span><span class="sxs-lookup"><span data-stu-id="84638-137">Which of my users were the most active during this time period?</span></span>

  - <span data-ttu-id="84638-138">发出电话呼叫最多的用户是否也是参与即时消息会话最多的用户？</span><span class="sxs-lookup"><span data-stu-id="84638-138">Are the users who make the most phone calls also the users who participate in the most instant messaging sessions?</span></span>

<span data-ttu-id="84638-139">如果需要回答此类问题，您可以将监视报告检索到的数据导出到 Excel 电子表格。</span><span class="sxs-lookup"><span data-stu-id="84638-139">If you need to answer questions like this, you can export the data retrieved by the Monitoring Reports to an Excel spreadsheet.</span></span> <span data-ttu-id="84638-140">然后，使用该电子表格和/或逗号分隔的值文件以用户活动报告的方式分析数据。</span><span class="sxs-lookup"><span data-stu-id="84638-140">You then use that spreadsheet and/or a comma-separated values file to analyze the data in ways that the User Activity Report.</span></span> <span data-ttu-id="84638-141">例如，假设您已将报告数据导出到 Excel，然后导出到逗号分隔的值文件。</span><span class="sxs-lookup"><span data-stu-id="84638-141">For example, suppose you have exported the report data to Excel and then to a comma-separated values file.</span></span> <span data-ttu-id="84638-142">此时，您可以从导入数据。CSV 文件到 Windows PowerShell，方法是使用如下所示的命令：</span><span class="sxs-lookup"><span data-stu-id="84638-142">At that point, you can import the data from the .CSV file to Windows PowerShell by using a command similar to this:</span></span>

    $x = Import-Csv -Path "C:\Data\User_Activity_Report.csv"

<span data-ttu-id="84638-143">导入数据后，您可以使用简单的 Windows PowerShell 命令来帮助解答您的问题。</span><span class="sxs-lookup"><span data-stu-id="84638-143">After the data has been imported you can then use simple Windows PowerShell commands to help answer your questions.</span></span> <span data-ttu-id="84638-144">例如，以下命令将返回至少在一个会话中充当“源用户”的唯一用户的列表：</span><span class="sxs-lookup"><span data-stu-id="84638-144">For example, this command returns a list of unique users who served as the "From user" in at least one session:</span></span>

    $x | Group-Object "From user" | Select Name | Sort-Object Name

<span data-ttu-id="84638-145">换言之：</span><span class="sxs-lookup"><span data-stu-id="84638-145">In other words:</span></span>

    Name
    ----
    David.Ahs@litwareinc.com
    Gilead.Amosnino@litwareinc.com
    Henrik.Jensen@litwareinc.com
    Ken.Myer@litwareinc.com
    Pilar.Ackerman@litwareinc.com

<span data-ttu-id="84638-146">以下命令将根据唯一用户参与的会话的总数列出这些用户：</span><span class="sxs-lookup"><span data-stu-id="84638-146">This command lists the unique users (based on the total number of sessions that they participated in:</span></span>

    $x | Group-Object "From user" | Select Count, Name | Sort-Object Count -Descending

<span data-ttu-id="84638-147">这将返回类似于下面的数据：</span><span class="sxs-lookup"><span data-stu-id="84638-147">That returns data similar to this:</span></span>

    Count    Name
    -----    ----
      523    Ken.Myer@litwareinc.com
       63    David.Ahs@litwareinc.com
       29    Pilar.Ackerman@litwareinc.com
       17    Gilead.Amosnino@litwareinc.com
       10    Henrik.Jensen@litwareinc.com

<span data-ttu-id="84638-148">以下命令会将报告的会话限制为将音频作为一种形式包含的会话：</span><span class="sxs-lookup"><span data-stu-id="84638-148">This command limits the reported sessions to those that included audio as a modality:</span></span>

    $x | Where-Object {$_.Modalities -match "audio"} | Group-Object "From user" | Select Count, Name | Sort-Object Count -Descending

<span data-ttu-id="84638-149">如果将鼠标悬停在报告上显示的任何诊断 ID 上，则会出现一个描述该 ID 的工具提示。</span><span class="sxs-lookup"><span data-stu-id="84638-149">If you hold your mouse over any Diagnostic ID shown on the report, a tooltip will appear describing that ID.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="84638-150">筛选器</span><span class="sxs-lookup"><span data-stu-id="84638-150">Filters</span></span>

<span data-ttu-id="84638-p111">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。例如，用户活动报告允许您基于活动类型（即对等会话还是会议会话）或用户的 SIP 地址（允许您查看一个用户的活动）筛选返回的数据。您还可以选择数据的分组方式。在此示例中，将按小时、日、周或月对使用情况进行分组。</span><span class="sxs-lookup"><span data-stu-id="84638-p111">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the User Activity Report enables you to filter the returned data based on such things as activity type (that is, peer-to-peer sessions or conferencing sessions) or by the user's SIP address (allowing you to view the activities for one user). You can also choose how data should be grouped. In this case, usages are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="84638-155">下表列出了可用于用户活动报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="84638-155">The following table lists the filters that you can use with the User Activity Report.</span></span>

### <a name="user-activity-report-filters"></a><span data-ttu-id="84638-156">用户活动报告筛选器</span><span class="sxs-lookup"><span data-stu-id="84638-156">User activity report filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84638-157">名称</span><span class="sxs-lookup"><span data-stu-id="84638-157">Name</span></span></th>
<th><span data-ttu-id="84638-158">描述</span><span class="sxs-lookup"><span data-stu-id="84638-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84638-159"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="84638-159"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-p112">时间范围的开始日期/时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="84638-p112">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="84638-162">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="84638-162">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="84638-p113">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="84638-p113">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="84638-165">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="84638-165">7/17/12012</span></span></p>
<p><span data-ttu-id="84638-166">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="84638-166">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="84638-167">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="84638-167">7/13/2012</span></span></p>
<p><span data-ttu-id="84638-168">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="84638-168">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-169"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="84638-169"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-p114">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="84638-p114">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="84638-172">7/17/12012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="84638-172">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="84638-p115">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="84638-p115">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="84638-175">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="84638-175">7/17/12012</span></span></p>
<p><span data-ttu-id="84638-176">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="84638-176">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="84638-177">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="84638-177">7/13/2012</span></span></p>
<p><span data-ttu-id="84638-178">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="84638-178">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-179"><strong>活动类型</strong></span><span class="sxs-lookup"><span data-stu-id="84638-179"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-p116">活动的类型。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="84638-p116">Type of activity. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="84638-182">[所有]</span><span class="sxs-lookup"><span data-stu-id="84638-182">[All]</span></span></p></li>
<li><p><span data-ttu-id="84638-183">对等</span><span class="sxs-lookup"><span data-stu-id="84638-183">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="84638-184">会议</span><span class="sxs-lookup"><span data-stu-id="84638-184">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-185"><strong>形式</strong></span><span class="sxs-lookup"><span data-stu-id="84638-185"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-186">可用的形式取决于选择的“活动类型”。</span><span class="sxs-lookup"><span data-stu-id="84638-186">The Modality available to you varies depending on the select Activity Type.</span></span> <span data-ttu-id="84638-187">如果活动类型是对等，则可以选择 "IM";文件传输;应用程序共享;语态或视频作为模态。</span><span class="sxs-lookup"><span data-stu-id="84638-187">If the Activity Type is Peer-to-Peer, you can select IM; File Transfer; Application Sharing; Voice; or Video as the modality.</span></span></p>
<p><span data-ttu-id="84638-188">如果“活动类型”是“会议”，您可以选择“IM 电话会议”、“Web 会议”、“应用程序共享”、“语音/视频会议”或“电话会议”。</span><span class="sxs-lookup"><span data-stu-id="84638-188">If the Activity Type is Conference, you can select IM Phone conference; Web conference; Application Sharing; Voice/Video conference; or Telephony conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-189"><strong>会话类别</strong></span><span class="sxs-lookup"><span data-stu-id="84638-189"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-p118">指示相应活动已成功还是失败。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="84638-p118">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="84638-192">[所有]</span><span class="sxs-lookup"><span data-stu-id="84638-192">[All]</span></span></p></li>
<li><p><span data-ttu-id="84638-193">成功</span><span class="sxs-lookup"><span data-stu-id="84638-193">Success</span></span></p></li>
<li><p><span data-ttu-id="84638-194">预期失败</span><span class="sxs-lookup"><span data-stu-id="84638-194">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="84638-195">意外失败</span><span class="sxs-lookup"><span data-stu-id="84638-195">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="84638-196">&quot;预期故障 &quot; 是预期发生的故障; 例如，如果用户已将其状态设置为 "请勿打扰"，则你可能需要对该用户的任何调用失败。</span><span class="sxs-lookup"><span data-stu-id="84638-196">An &quot;expected failure&quot; is a failure that is expected to happen; for example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="84638-197">&quot;意外故障 &quot; 是指出现在其他正常运行的系统中的故障。</span><span class="sxs-lookup"><span data-stu-id="84638-197">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="84638-198">例如，如果呼叫者处于呼叫等待状态，则不应该终止呼叫。</span><span class="sxs-lookup"><span data-stu-id="84638-198">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="84638-199">如果终止，则会被标记为意外失败。</span><span class="sxs-lookup"><span data-stu-id="84638-199">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-200"><strong>用户 URI 前缀</strong></span><span class="sxs-lookup"><span data-stu-id="84638-200"><strong>User URI prefix</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-p120">用户的 SIP 地址。要仅查看用户 Ken Myer 的记录，您需要输入 Ken Myer 的 SIP 地址。例如：</span><span class="sxs-lookup"><span data-stu-id="84638-p120">SIP address for the user. To view records only for the user Ken Myer you need to enter Ken Myer's SIP address. For example:</span></span></p>
<p><span data-ttu-id="84638-204">sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="84638-204">sip:kenmyer@litwareinc.com</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="84638-205">对等会话的指标</span><span class="sxs-lookup"><span data-stu-id="84638-205">Metrics for peer-to-peer sessions</span></span>

<span data-ttu-id="84638-206">下表列出了对等会话（即，只涉及两个参与者的会话）的用户活动报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="84638-206">The following table lists the information provided in the User Activity Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="84638-207">对等会话的指标</span><span class="sxs-lookup"><span data-stu-id="84638-207">Metrics for peer-to-peer sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84638-208">名称</span><span class="sxs-lookup"><span data-stu-id="84638-208">Name</span></span></th>
<th><span data-ttu-id="84638-209">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="84638-209">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="84638-210">描述</span><span class="sxs-lookup"><span data-stu-id="84638-210">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84638-211"><strong>详情</strong></span><span class="sxs-lookup"><span data-stu-id="84638-211"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-212">否</span><span class="sxs-lookup"><span data-stu-id="84638-212">No</span></span></p></td>
<td><p><span data-ttu-id="84638-213">单击此项时，报告将显示所选会话的对等会话详细信息报告。</span><span class="sxs-lookup"><span data-stu-id="84638-213">When you click this item, the report shows you the Peer-to-Peer Session Detail Report for the selected session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-214"><strong>来源用户</strong></span><span class="sxs-lookup"><span data-stu-id="84638-214"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-215">是</span><span class="sxs-lookup"><span data-stu-id="84638-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-216">发起对等会话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="84638-216">SIP address of the user who initiated the peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-217"><strong>目标用户</strong></span><span class="sxs-lookup"><span data-stu-id="84638-217"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-218">是</span><span class="sxs-lookup"><span data-stu-id="84638-218">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-219">加入对等会话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="84638-219">SIP address of the user who joined the peer-to-peer session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-220"><strong>形式</strong></span><span class="sxs-lookup"><span data-stu-id="84638-220"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-221">是</span><span class="sxs-lookup"><span data-stu-id="84638-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-p121">会话中使用的通信类型。例如，IM、音频或文件传输。</span><span class="sxs-lookup"><span data-stu-id="84638-p121">Type of communication used in the session. For example, IM, audio, or file transfer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-224"><strong>邀请时间</strong></span><span class="sxs-lookup"><span data-stu-id="84638-224"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-225">是</span><span class="sxs-lookup"><span data-stu-id="84638-225">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-226">发送加入对等会话的初始邀请的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="84638-226">Date and time the initial invitation to join the peer-to-peer session was sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-227"><strong>响应时间</strong></span><span class="sxs-lookup"><span data-stu-id="84638-227"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-228">是</span><span class="sxs-lookup"><span data-stu-id="84638-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-229">&quot; &quot; 用户接受会话邀请的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="84638-229">Date and time that the &quot;To&quot; user accepted the session invitation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-230"><strong>结束时间</strong></span><span class="sxs-lookup"><span data-stu-id="84638-230"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-231">是</span><span class="sxs-lookup"><span data-stu-id="84638-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-232">对等会话结束的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="84638-232">Date and time the peer-to-peer session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-233"><strong>诊断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="84638-233"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-234">是</span><span class="sxs-lookup"><span data-stu-id="84638-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-p122">附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），提供的信息在排查错误时通常很有帮助。诊断标头是可选的（SIP 会话可以不包含这些标头），并且只对遇到此类问题的会话报告诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="84638-p122">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="84638-237">会议会话的指标</span><span class="sxs-lookup"><span data-stu-id="84638-237">Metrics for conferencing sessions</span></span>

<span data-ttu-id="84638-238">下表列出了会议会话（即，涉及三个或更多参与者的会话）的用户活动报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="84638-238">The following table lists the information provided in the User Activity Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="84638-239">会议会话的指标</span><span class="sxs-lookup"><span data-stu-id="84638-239">Metrics for conferencing sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84638-240">名称</span><span class="sxs-lookup"><span data-stu-id="84638-240">Name</span></span></th>
<th><span data-ttu-id="84638-241">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="84638-241">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="84638-242">描述</span><span class="sxs-lookup"><span data-stu-id="84638-242">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84638-243"><strong>会议 URI</strong></span><span class="sxs-lookup"><span data-stu-id="84638-243"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-244">是</span><span class="sxs-lookup"><span data-stu-id="84638-244">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-245">唯一会议标识符。</span><span class="sxs-lookup"><span data-stu-id="84638-245">Unique conference identifier.</span></span> <span data-ttu-id="84638-246">单击此项时，报告将显示所选会话的会议详细信息报告。</span><span class="sxs-lookup"><span data-stu-id="84638-246">When you click this item, the report shows you the Conference Detail Report for the selected session.</span></span> <span data-ttu-id="84638-247">展开此项时，报告将显示有关会议参与者的信息。</span><span class="sxs-lookup"><span data-stu-id="84638-247">When you expand this item, the report shows you information about the conference participants.</span></span> <span data-ttu-id="84638-248">有关详细信息，请参阅 &quot; &quot; 本主题后面部分的会议参与者的 "指标" 部分。</span><span class="sxs-lookup"><span data-stu-id="84638-248">For details, see the &quot;Metrics for Conference Participants&quot; section later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-249"><strong>组织者</strong></span><span class="sxs-lookup"><span data-stu-id="84638-249"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-250">是</span><span class="sxs-lookup"><span data-stu-id="84638-250">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-251">组织会议的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="84638-251">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-252"><strong>池</strong></span><span class="sxs-lookup"><span data-stu-id="84638-252"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-253">是</span><span class="sxs-lookup"><span data-stu-id="84638-253">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-254">会议中使用的边缘服务器（如果有）的名称。</span><span class="sxs-lookup"><span data-stu-id="84638-254">Name of the Edge Server (if any) used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-255"><strong>开始时间</strong></span><span class="sxs-lookup"><span data-stu-id="84638-255"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-256">是</span><span class="sxs-lookup"><span data-stu-id="84638-256">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-257">会议开始的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="84638-257">Date and time that the conference began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-258"><strong>结束时间</strong></span><span class="sxs-lookup"><span data-stu-id="84638-258"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-259">是</span><span class="sxs-lookup"><span data-stu-id="84638-259">Yes</span></span></p></td>
<td><p><span data-ttu-id="84638-260">会议结束的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="84638-260">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conference-participants"></a><span data-ttu-id="84638-261">会议参与者的指标</span><span class="sxs-lookup"><span data-stu-id="84638-261">Metrics for conference participants</span></span>

<span data-ttu-id="84638-262">下表列出了会议的每个参与者的用户活动报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="84638-262">The following table lists the information provided in the User Activity Report provides for each participant in a conference.</span></span>

### <a name="metrics-for-conference-participants"></a><span data-ttu-id="84638-263">会议参与者的指标</span><span class="sxs-lookup"><span data-stu-id="84638-263">Metrics for conference participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84638-264">名称</span><span class="sxs-lookup"><span data-stu-id="84638-264">Name</span></span></th>
<th><span data-ttu-id="84638-265">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="84638-265">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="84638-266">描述</span><span class="sxs-lookup"><span data-stu-id="84638-266">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84638-267"><strong>角色</strong></span><span class="sxs-lookup"><span data-stu-id="84638-267"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-268">否</span><span class="sxs-lookup"><span data-stu-id="84638-268">No</span></span></p></td>
<td><p><span data-ttu-id="84638-269">用户的会议角色（例如，演示者）。</span><span class="sxs-lookup"><span data-stu-id="84638-269">Conference role (for example, Presenter) for the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-270"><strong>参与者</strong></span><span class="sxs-lookup"><span data-stu-id="84638-270"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-271">否</span><span class="sxs-lookup"><span data-stu-id="84638-271">No</span></span></p></td>
<td><p><span data-ttu-id="84638-272">用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="84638-272">SIP address of the user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-273"><strong>连接</strong></span><span class="sxs-lookup"><span data-stu-id="84638-273"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-274">否</span><span class="sxs-lookup"><span data-stu-id="84638-274">No</span></span></p></td>
<td><p><span data-ttu-id="84638-275">网络连接类型。</span><span class="sxs-lookup"><span data-stu-id="84638-275">Network connection type.</span></span> <span data-ttu-id="84638-276">例如，内部 &quot; &quot; 连接内部的内部连接或 &quot; 来自 PSTN &quot; 的电话拨入用户。</span><span class="sxs-lookup"><span data-stu-id="84638-276">For example &quot;From Internal&quot; for internal connection or &quot;From PSTN&quot; for dial-in users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-277"><strong>加入时间</strong></span><span class="sxs-lookup"><span data-stu-id="84638-277"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-278">否</span><span class="sxs-lookup"><span data-stu-id="84638-278">No</span></span></p></td>
<td><p><span data-ttu-id="84638-279">用户加入会议的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="84638-279">Date and time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84638-280"><strong>离开时间</strong></span><span class="sxs-lookup"><span data-stu-id="84638-280"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-281">否</span><span class="sxs-lookup"><span data-stu-id="84638-281">No</span></span></p></td>
<td><p><span data-ttu-id="84638-282">用户离开会议的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="84638-282">Date and time that the user left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84638-283"><strong>诊断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="84638-283"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="84638-284">否</span><span class="sxs-lookup"><span data-stu-id="84638-284">No</span></span></p></td>
<td><p><span data-ttu-id="84638-p125">附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），提供的信息在排查错误时通常很有帮助。诊断标头是可选的（SIP 会话可以不包含这些标头），并且只对遇到此类问题的会话报告诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="84638-p125">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="84638-287">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="84638-287">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

