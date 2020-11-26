---
title: Lync Server 2013：响应组通话列表报告
description: Lync Server 2013：响应组呼叫列表报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response Group Call List Report
ms:assetid: a2d3e08b-511b-4507-abba-8ff71aa27c8e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615443(v=OCS.15)
ms:contentKeyID: 48184954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ffe4b62534d4849b4f0cdade9aeef8be5d69178
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436305"
---
# <a name="response-group-call-list-report-in-lync-server-2013"></a><span data-ttu-id="fd0f0-103">Lync Server 2013 中的响应组呼叫列表报告</span><span class="sxs-lookup"><span data-stu-id="fd0f0-103">Response Group Call List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd0f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd0f0-104">

<span> </span></span></span>

<span data-ttu-id="fd0f0-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="fd0f0-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="fd0f0-106">"响应组" 应用程序为 Microsoft Lync Server 2013 提供了一种方法，可根据所拨打的号码和呼叫者对一系列问题的响应（可选）应答和路由电话呼叫。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-106">The Response Group application provides a way for Microsoft Lync Server 2013 to answer and route phone calls based on the number that was dialed and, optionally, on the caller's responses to a series of questions.</span></span> <span data-ttu-id="fd0f0-107">通常，不会将响应组呼叫路由到个人，而是路由到称为代理组的一组人员。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-107">Typically, Response Group calls are not routed to an individual person but, instead, are routed to a team of people referred to as an agent group.</span></span> <span data-ttu-id="fd0f0-108">例如，如果某人呼叫帮助台的电话号码，则 Lync Server 2013 可以自动将呼叫路由到第一个可用的技术支持代理。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-108">For example, if someone calls the phone number for your help desk, Lync Server 2013 can automatically route that call to the first available help desk agent.</span></span> <span data-ttu-id="fd0f0-109">或者，如果遇到硬件问题，Lync Server 可能会询问一系列问题 ( "按1。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-109">Alternatively, Lync Server could ask a series of questions ("Press 1 if you are having hardware problems.</span></span> <span data-ttu-id="fd0f0-110">如果您有软件问题，请按 2。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-110">Press 2 if you are having software problems.</span></span> <span data-ttu-id="fd0f0-111">如果出现网络问题，请按3。 ") ，然后根据这些问题的答案将呼叫路由到最合适的技术支持代理。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-111">Press 3 if you are having network problems.") and then route the call to the most appropriate help desk agent based on the answer to those questions.</span></span>

<span data-ttu-id="fd0f0-p102">响应组呼叫列表报告代表针对指定的时间段和指定的呼叫类型所进行的呼叫集合。响应组使用报告（必需先打开该报告，才能打开响应组呼叫列表报告）可识别以下呼叫类型：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p102">The Response Group Call List Report represents a collection of calls made for a specified period of time and for a specified type of call. The Response Group Usage Report (which must be opened first before you can open the Response Group Call List Report) recognizes the following call types:</span></span>

  - <span data-ttu-id="fd0f0-p103">**收到的呼叫**。响应组应用程序的所有实例收到的呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p103">**Received calls**. Total number of calls received by all instances of the Response Group application.</span></span>

  - <span data-ttu-id="fd0f0-p104">**成功的呼叫**。响应组应用程序所接听的呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p104">**Successful calls**. Total number of calls that were picked up by the Response Group application.</span></span>

  - <span data-ttu-id="fd0f0-p105">**提供的呼叫**。已转接给响应组代理的呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p105">**Offered calls**. Total number of calls that were transferred to a Response Group agent.</span></span>

  - <span data-ttu-id="fd0f0-p106">**应答的呼叫**。响应组代理实际应答的呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p106">**Answered calls**. Total number of calls that were actually answered by a Response Group agent.</span></span>

  - <span data-ttu-id="fd0f0-122">放弃的呼叫的百分比。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-122">Percentage of abandoned calls.</span></span> <span data-ttu-id="fd0f0-123">响应组应用程序已收到但代理未应答的呼叫的百分比。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-123">Percentage of calls that were received by the Response Group application but were never answered by an agent.</span></span> <span data-ttu-id="fd0f0-124">此值的计算方法是用“收到的呼叫数”减去“应答的呼叫数”，然后用所得的值除以收到的呼叫数。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-124">This value is calculated by subtracting the Answered calls from the Received calls, and then dividing that value by the number of Received calls.</span></span> <span data-ttu-id="fd0f0-125">例如，如果收到 10 个呼叫，但应答了 7 个，则计算方法是 10 减去 7，得出未应答的呼叫是 3 个。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-125">For example, if you received 10 calls and 7 were answered, you would subtract 7 from 10, leaving 3 unanswered calls.</span></span> <span data-ttu-id="fd0f0-126">然后用该值除以 10，得出放弃的呼叫的百分比为 30%。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-126">That value would then be divided by 10, giving you an abandoned call percentage of 30%.</span></span>

  - <span data-ttu-id="fd0f0-p108">**转接的呼叫**。因队列超时或队列溢出而转接的响应组呼叫总数。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p108">**Transferred calls**. Total number of Response Group calls that were transferred because of a queue timeout or queue overflow.</span></span>

<div>

## <a name="accessing-the-response-group-call-list-report"></a><span data-ttu-id="fd0f0-129">访问响应组呼叫列表报告</span><span class="sxs-lookup"><span data-stu-id="fd0f0-129">Accessing the Response Group Call List Report</span></span>

<span data-ttu-id="fd0f0-130">只有通过单击在 [Lync Server 2013 的 "响应组使用情况" 报告中](lync-server-2013-response-group-usage-report.md)找到的以下指标之一，才能访问 "响应组呼叫列表" 报告：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-130">The Response Group Call List Report can only be accessed by clicking one of the following metrics found on the [Response Group Usage Report in Lync Server 2013](lync-server-2013-response-group-usage-report.md):</span></span>

  - <span data-ttu-id="fd0f0-131">收到的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-131">Received calls</span></span>

  - <span data-ttu-id="fd0f0-132">成功的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-132">Successful calls</span></span>

  - <span data-ttu-id="fd0f0-133">提供的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-133">Offered calls</span></span>

  - <span data-ttu-id="fd0f0-134">应答的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-134">Answered calls</span></span>

  - <span data-ttu-id="fd0f0-135">转接的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-135">Transferred calls</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-response-group-call-list-report"></a><span data-ttu-id="fd0f0-136">充分利用响应组呼叫列表报告</span><span class="sxs-lookup"><span data-stu-id="fd0f0-136">Making the Best Use of the Response Group Call List Report</span></span>

<span data-ttu-id="fd0f0-p109">响应组呼叫列表报告允许您将所显示的数据限制为涉及特定响应组工作流的呼叫。为执行此操作，需要在“工作流 URI”框中输入工作流 URI（工作流的 SIP 地址）。但是，您必须实际上能够看到“工作流 URI”框，才能执行此操作。要显示响应组呼叫列表报告的筛选选项，请单击报告窗口左上部分的“显示/隐藏参数”按钮。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p109">The Response Group Call List Report allows you to limit the displayed data to calls involving a particular Response Group workflow. To do that, you need to enter the workflow URI (the workflow's SIP address) in the Workflow URI box. Before you can do that, however, you must actually be able to see the Workflow URI box. To display the filtering options for the Response Group Call List Report, click the Show/Hide Parameters button in the upper left-hand portion of the report window.</span></span>

<span data-ttu-id="fd0f0-141">请注意，如果将鼠标停留在其中任一指标上，响应组呼叫列表不会显示有关响应代码或诊断 ID 的信息。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-141">Note that the Response Group Call List does not display information about either the Response code or the Diagnostic ID if you hold the mouse over either of those metrics.</span></span> <span data-ttu-id="fd0f0-142">如果你需要详细信息，你可能会注意到响应代码和/或诊断 ID，然后在 [Lync Server 2013 的 "热门故障" 报告](lync-server-2013-top-failures-report.md)中搜索这些值。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-142">If you need more information, you might note the Response code and/or Diagnostic ID, and then search for those values in the [Top Failures Report in Lync Server 2013](lync-server-2013-top-failures-report.md).</span></span>

<span data-ttu-id="fd0f0-143">对于类似如下的问题：“哪个个别工作流收到的呼叫数最多？”，您可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-143">a question like this one: "Which individual workflow received the most calls?", you can do the following:</span></span>

1.  <span data-ttu-id="fd0f0-p111">在“响应组使用报告”上，设置所需的时间段，然后单击“收到的呼叫”指标。这样即会打开“响应组呼叫列表报告”。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p111">On the Response Group Usage Report, set the desired time period and then click the Received Calls metric. That will open the Response Group Call List Report.</span></span>

2.  <span data-ttu-id="fd0f0-p112">导出“响应组呼叫列表报告”上所显示的数据。例如，可以使用 Microsoft Excel 格式导出数据，然后使用 Excel 将该数据转换为逗号分隔值文件。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p112">Export the data shown on the Response Group Call List Report. For example, you might export the data in Microsoft Excel format, and then use Excel to convert that data to a comma-separated values file.</span></span>

3.  <span data-ttu-id="fd0f0-148">使用 Windows PowerShell 运行您的分析。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-148">Run your analyses using Windows PowerShell.</span></span>

<span data-ttu-id="fd0f0-149">例如，如果已将数据保存到名为 C： \\ data \\ Response \_ Group \_ 呼叫 \_ 列表Report.csv 的文件 \_ 中，则可以使用以下命令返回报表中列出的每个工作流的已接收调用总数：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-149">For example, if you have saved the data to a file named C:\\Data\\Response\_Group\_Call\_List\_Report.csv, you can then use the following command to return the total number of received calls for each workflow listed in the report:</span></span>

    $calls = Import-Csv -Path "C:\ Data\Response_Group_Call_List_Report.csv"
    $calls | Group-Object Workflow | Select-Object Count, Name | Sort-Object Count -Descending

<span data-ttu-id="fd0f0-150">这将返回与以下类似的信息：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-150">That will information similar to this:</span></span>

    Count    Name
    -----    ----
      160    Redmond Help Desk
       47    Dublin Help Desk
       31    North America Customer Support
       16    EMEA Customer Support
       14    Employment Opportunities

</div>

<div>

## <a name="filters"></a><span data-ttu-id="fd0f0-151">筛选器</span><span class="sxs-lookup"><span data-stu-id="fd0f0-151">Filters</span></span>

<span data-ttu-id="fd0f0-p113">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。下表列出了可用于响应组呼叫列表报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p113">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Response Group Call List Report.</span></span>

### <a name="response-group-call-list-report-filters"></a><span data-ttu-id="fd0f0-154">响应组呼叫列表报告筛选器</span><span class="sxs-lookup"><span data-stu-id="fd0f0-154">Response Group Call List Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd0f0-155">名称</span><span class="sxs-lookup"><span data-stu-id="fd0f0-155">Name</span></span></th>
<th><span data-ttu-id="fd0f0-156">描述</span><span class="sxs-lookup"><span data-stu-id="fd0f0-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd0f0-157"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-157"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-p114">时间范围的开始日期/时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p114">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="fd0f0-160">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="fd0f0-160">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="fd0f0-p115">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p115">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="fd0f0-163">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="fd0f0-163">7/7/2012</span></span></p>
<p><span data-ttu-id="fd0f0-164">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-164">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="fd0f0-165">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="fd0f0-165">7/3/2012</span></span></p>
<p><span data-ttu-id="fd0f0-166">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-166">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0f0-167"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-167"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-p116">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p116">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="fd0f0-170">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="fd0f0-170">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="fd0f0-p117">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p117">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="fd0f0-173">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="fd0f0-173">7/7/2012</span></span></p>
<p><span data-ttu-id="fd0f0-174">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-174">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="fd0f0-175">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="fd0f0-175">7/3/2012</span></span></p>
<p><span data-ttu-id="fd0f0-176">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-176">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd0f0-177"><strong>工作流 URI</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-177"><strong>Workflow URI</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-p118">允许您限制返回的数据，以便仅显示指定响应组工作流的数据。若要使用该筛选器，请输入工作流 SIP 地址。例如：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-p118">Enables you to limit the returned data to the specified Response Group workflow. To use this filter, enter the Workflow SIP address. For example:</span></span></p>
<p><span data-ttu-id="fd0f0-181">sip:helpdesk@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="fd0f0-181">sip:helpdesk@litwareinc.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0f0-182"><strong>呼叫</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-182"><strong>Calls</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-183">可以选择以下呼叫类型之一：</span><span class="sxs-lookup"><span data-stu-id="fd0f0-183">You can select one of the following call types:</span></span></p>
<ul>
<li><p><span data-ttu-id="fd0f0-184">收到的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-184">Received Calls</span></span></p></li>
<li><p><span data-ttu-id="fd0f0-185">成功的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-185">Successful Calls</span></span></p></li>
<li><p><span data-ttu-id="fd0f0-186">提供的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-186">Offered Calls</span></span></p></li>
<li><p><span data-ttu-id="fd0f0-187">应答的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-187">Answered Calls</span></span></p></li>
<li><p><span data-ttu-id="fd0f0-188">转接的呼叫</span><span class="sxs-lookup"><span data-stu-id="fd0f0-188">Transferred Calls</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="fd0f0-189">指标</span><span class="sxs-lookup"><span data-stu-id="fd0f0-189">Metrics</span></span>

<span data-ttu-id="fd0f0-190">下表列出了响应组应用程序收到的每个呼叫的响应组呼叫列表报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-190">The following table lists the information provided in the Response Group Call List Report for each call received by the Response Group application.</span></span>

### <a name="response-group-call-list-report-metrics"></a><span data-ttu-id="fd0f0-191">响应组呼叫列表报告指标</span><span class="sxs-lookup"><span data-stu-id="fd0f0-191">Response Group Call List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd0f0-192">名称</span><span class="sxs-lookup"><span data-stu-id="fd0f0-192">Name</span></span></th>
<th><span data-ttu-id="fd0f0-193">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="fd0f0-193">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="fd0f0-194">描述</span><span class="sxs-lookup"><span data-stu-id="fd0f0-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd0f0-195"><strong>呼叫者</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-195"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-196">否</span><span class="sxs-lookup"><span data-stu-id="fd0f0-196">No</span></span></p></td>
<td><p><span data-ttu-id="fd0f0-197">呼叫者的 SIP 地址</span><span class="sxs-lookup"><span data-stu-id="fd0f0-197">SIP address of the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0f0-198"><strong>工作流</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-198"><strong>Workflow</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-199">否</span><span class="sxs-lookup"><span data-stu-id="fd0f0-199">No</span></span></p></td>
<td><p><span data-ttu-id="fd0f0-200">响应组工作流的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-200">SIP address of the Response Group workflow.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd0f0-201"><strong>开始时间</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-201"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-202">否</span><span class="sxs-lookup"><span data-stu-id="fd0f0-202">No</span></span></p></td>
<td><p><span data-ttu-id="fd0f0-203">呼叫开始的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-203">Date and time that the call started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0f0-204"><strong>结束时间</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-204"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-205">否</span><span class="sxs-lookup"><span data-stu-id="fd0f0-205">No</span></span></p></td>
<td><p><span data-ttu-id="fd0f0-206">呼叫结束的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-206">Date and time that the call ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd0f0-207"><strong>响应代码</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-207"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-208">否</span><span class="sxs-lookup"><span data-stu-id="fd0f0-208">No</span></span></p></td>
<td><p><span data-ttu-id="fd0f0-209">会话失败时发送的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-209">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd0f0-210"><strong>诊断 ID</strong></span><span class="sxs-lookup"><span data-stu-id="fd0f0-210"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="fd0f0-211">否</span><span class="sxs-lookup"><span data-stu-id="fd0f0-211">No</span></span></p></td>
<td><p><span data-ttu-id="fd0f0-212">附加到 SIP 消息的唯一标识符（采用 ms-diagnostics 标头的形式），提供的信息在排查错误时通常很有帮助。</span><span class="sxs-lookup"><span data-stu-id="fd0f0-212">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fd0f0-213">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd0f0-213">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

