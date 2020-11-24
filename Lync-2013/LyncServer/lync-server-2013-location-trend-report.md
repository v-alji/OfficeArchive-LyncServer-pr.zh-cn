---
title: Lync Server 2013：位置趋势报表
description: Lync Server 2013：位置趋势报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location Trend Report
ms:assetid: 61e2db3c-9f10-4411-8e7e-c6950faf8533
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204941(v=OCS.15)
ms:contentKeyID: 48184280
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 83035bf81e793416035e1bd90906b3c27e51f7f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392383"
---
# <a name="location-trend-report-in-lync-server-2013"></a><span data-ttu-id="13b3a-103">Lync Server 2013 中的 "位置趋势" 报表</span><span class="sxs-lookup"><span data-stu-id="13b3a-103">Location Trend Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13b3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13b3a-104">

<span> </span></span></span>

<span data-ttu-id="13b3a-105">_**主题上次修改时间：** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="13b3a-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="13b3a-106">位置趋势报告提供网络位置的呼叫质量趋势信息。</span><span class="sxs-lookup"><span data-stu-id="13b3a-106">The Location Trend Report provides call quality trend information for network locations.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="13b3a-107">筛选器</span><span class="sxs-lookup"><span data-stu-id="13b3a-107">Filters</span></span>

<span data-ttu-id="13b3a-p101">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。例如，位置趋势报告使您能够按访问类型（即内部访问与外部访问）或有线/无线网络连接等条件来筛选返回的数据。您还可以选择数据的分组方式。在此示例中，将按小时、日或周对呼叫进行分组。</span><span class="sxs-lookup"><span data-stu-id="13b3a-p101">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Location Trend Report enables you to filter the returned data by such things as access type (that is, interval access vs. external access) or by wired/wireless network connection. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, or week.</span></span>

<span data-ttu-id="13b3a-112">下表列出了可用于位置趋势报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="13b3a-112">The following table lists the filters that you can use with the Location Trend Report.</span></span>

### <a name="location-trend-report-filters"></a><span data-ttu-id="13b3a-113">位置趋势报告筛选器</span><span class="sxs-lookup"><span data-stu-id="13b3a-113">Location Trend Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13b3a-114">名称</span><span class="sxs-lookup"><span data-stu-id="13b3a-114">Name</span></span></th>
<th><span data-ttu-id="13b3a-115">描述</span><span class="sxs-lookup"><span data-stu-id="13b3a-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13b3a-116"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="13b3a-116"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="13b3a-p102">时间范围的开始日期/时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p102">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="13b3a-119">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="13b3a-119">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="13b3a-p103">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="13b3a-122">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="13b3a-122">7/7/2012</span></span></p>
<p><span data-ttu-id="13b3a-123">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="13b3a-123">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="13b3a-124">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="13b3a-124">7/3/2012</span></span></p>
<p><span data-ttu-id="13b3a-125">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="13b3a-125">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b3a-126"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="13b3a-126"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="13b3a-p104">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p104">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="13b3a-129">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="13b3a-129">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="13b3a-p105">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="13b3a-132">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="13b3a-132">7/7/2012</span></span></p>
<p><span data-ttu-id="13b3a-133">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="13b3a-133">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="13b3a-134">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="13b3a-134">7/3/2012</span></span></p>
<p><span data-ttu-id="13b3a-135">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="13b3a-135">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13b3a-136"><strong>间隔</strong></span><span class="sxs-lookup"><span data-stu-id="13b3a-136"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="13b3a-p106">时间间隔。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p106">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="13b3a-139">每小时（最多可显示 25 个小时）</span><span class="sxs-lookup"><span data-stu-id="13b3a-139">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="13b3a-140">每天（最多可显示 31 天）</span><span class="sxs-lookup"><span data-stu-id="13b3a-140">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="13b3a-141">每周（最多可显示 12 周）</span><span class="sxs-lookup"><span data-stu-id="13b3a-141">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="13b3a-p107">如果开始日期和结束日期超出了所选间隔允许的最长时间，则仅显示最长时间（从开始日期开始）。例如，如果选择的开始日期为 2011/1/1、结束日期为 2011/2/28、间隔为“每天”，则显示从 2011/8/1 12:00 AM 到 2011/9/1 12:00 AM 这些天的数据（即总共 31 天的数据）。</span><span class="sxs-lookup"><span data-stu-id="13b3a-p107">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed. For example, if you select the Daily interval with a start date of 1/1/2011 and an end date of 2/28/2011, data is displayed for the days 8/1/2011 12:00 AM to 9/1/2011 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b3a-144"><strong>访问类型</strong></span><span class="sxs-lookup"><span data-stu-id="13b3a-144"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="13b3a-p108">指示客户端在发起呼叫时已登录到内部网络还是外部网络。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p108">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="13b3a-147">[所有]</span><span class="sxs-lookup"><span data-stu-id="13b3a-147">[All]</span></span></p></li>
<li><p><span data-ttu-id="13b3a-148">内部</span><span class="sxs-lookup"><span data-stu-id="13b3a-148">Internal</span></span></p></li>
<li><p><span data-ttu-id="13b3a-149">外部</span><span class="sxs-lookup"><span data-stu-id="13b3a-149">External</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13b3a-150"><strong>网络类型</strong></span><span class="sxs-lookup"><span data-stu-id="13b3a-150"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="13b3a-p109">指示客户端在发起呼叫时已连接到的网络的类型。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p109">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="13b3a-153">[所有]</span><span class="sxs-lookup"><span data-stu-id="13b3a-153">[All]</span></span></p></li>
<li><p><span data-ttu-id="13b3a-154">有线</span><span class="sxs-lookup"><span data-stu-id="13b3a-154">Wired</span></span></p></li>
<li><p><span data-ttu-id="13b3a-155">无线</span><span class="sxs-lookup"><span data-stu-id="13b3a-155">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b3a-156"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="13b3a-156"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="13b3a-p110">指示外部客户端在发起呼叫时是否使用了虚拟专用网 (VPN) 连接。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="13b3a-p110">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="13b3a-159">[所有]</span><span class="sxs-lookup"><span data-stu-id="13b3a-159">[All]</span></span></p></li>
<li><p><span data-ttu-id="13b3a-160">VPN</span><span class="sxs-lookup"><span data-stu-id="13b3a-160">VPN</span></span></p></li>
<li><p><span data-ttu-id="13b3a-161">非 VPN</span><span class="sxs-lookup"><span data-stu-id="13b3a-161">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="13b3a-162">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13b3a-162">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

