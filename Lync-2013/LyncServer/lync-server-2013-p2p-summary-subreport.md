---
title: Lync Server 2013： P2P 摘要子报表
description: Lync Server 2013： P2P 摘要子报表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: P2P Summary Subreport
ms:assetid: fc36185a-3cc5-4167-8c93-8a755fa75ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205416(v=OCS.15)
ms:contentKeyID: 48185950
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eda51e76c4ed7b62535a2a2e4ab52982aa6381f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424700"
---
# <a name="p2p-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="1e094-103">Lync Server 2013 中的 P2P 摘要子报表</span><span class="sxs-lookup"><span data-stu-id="1e094-103">P2P Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1e094-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1e094-104">

<span> </span></span></span>

<span data-ttu-id="1e094-105">_**主题上次修改时间：** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="1e094-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="1e094-106">P2P 摘要子报表对失败对等通信会话提供一个总体视图。</span><span class="sxs-lookup"><span data-stu-id="1e094-106">The P2P Summary Subreport provides an overall view of your failed peer-to-peer communication sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="1e094-107">筛选器</span><span class="sxs-lookup"><span data-stu-id="1e094-107">Filters</span></span>

<span data-ttu-id="1e094-p101">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。下表列出了可用于 P2P 摘要子报表的筛选器。</span><span class="sxs-lookup"><span data-stu-id="1e094-p101">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-filters"></a><span data-ttu-id="1e094-110">P2P 摘要子报表筛选器</span><span class="sxs-lookup"><span data-stu-id="1e094-110">P2P Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e094-111">名称</span><span class="sxs-lookup"><span data-stu-id="1e094-111">Name</span></span></th>
<th><span data-ttu-id="1e094-112">描述</span><span class="sxs-lookup"><span data-stu-id="1e094-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e094-113"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="1e094-113"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="1e094-p102">时间范围的开始日期和时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1e094-p102">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="1e094-116">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="1e094-116">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="1e094-p103">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="1e094-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="1e094-119">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="1e094-119">7/7/2012</span></span></p>
<p><span data-ttu-id="1e094-120">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="1e094-120">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="1e094-121">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="1e094-121">7/3/2012</span></span></p>
<p><span data-ttu-id="1e094-122">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="1e094-122">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e094-123"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="1e094-123"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="1e094-p104">时间范围的结束日期和时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1e094-p104">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="1e094-126">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="1e094-126">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="1e094-p105">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="1e094-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="1e094-129">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="1e094-129">7/7/2012</span></span></p>
<p><span data-ttu-id="1e094-130">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="1e094-130">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="1e094-131">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="1e094-131">7/3/2012</span></span></p>
<p><span data-ttu-id="1e094-132">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="1e094-132">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e094-133"><strong>池</strong></span><span class="sxs-lookup"><span data-stu-id="1e094-133"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="1e094-p106">注册器池或边缘服务器的完全限定域名 (FQDN)。可以选择单个池，也可以单击“<strong>[所有]</strong>”查看所有池的数据。系统根据数据库中的记录自动为您填充该下拉列表。</span><span class="sxs-lookup"><span data-stu-id="1e094-p106">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="1e094-137">指标</span><span class="sxs-lookup"><span data-stu-id="1e094-137">Metrics</span></span>

<span data-ttu-id="1e094-138">下表列出了 P2P 摘要子报表中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="1e094-138">The following table lists the information provided in the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-metrics"></a><span data-ttu-id="1e094-139">P2P 摘要子报告指标</span><span class="sxs-lookup"><span data-stu-id="1e094-139">P2P Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e094-140">名称</span><span class="sxs-lookup"><span data-stu-id="1e094-140">Name</span></span></th>
<th><span data-ttu-id="1e094-141">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="1e094-141">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="1e094-142">描述</span><span class="sxs-lookup"><span data-stu-id="1e094-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e094-143"><strong>会话总数</strong></span><span class="sxs-lookup"><span data-stu-id="1e094-143"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="1e094-144">否</span><span class="sxs-lookup"><span data-stu-id="1e094-144">No</span></span></p></td>
<td><p><span data-ttu-id="1e094-145">会话的总数，包括成功的会话、失败的会话（预期失败和意外失败）及未归类的会话。</span><span class="sxs-lookup"><span data-stu-id="1e094-145">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e094-146"><strong>故障率</strong></span><span class="sxs-lookup"><span data-stu-id="1e094-146"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="1e094-147">否</span><span class="sxs-lookup"><span data-stu-id="1e094-147">No</span></span></p></td>
<td><p><span data-ttu-id="1e094-148">失败的对等会话百分比。</span><span class="sxs-lookup"><span data-stu-id="1e094-148">Percentage of peer-to-peer sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e094-149"><strong>按形式列出的会话</strong></span><span class="sxs-lookup"><span data-stu-id="1e094-149"><strong>Sessions by Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="1e094-150">否</span><span class="sxs-lookup"><span data-stu-id="1e094-150">No</span></span></p></td>
<td><p><span data-ttu-id="1e094-151">按形式分组的会话总数（例如，即时消息）。</span><span class="sxs-lookup"><span data-stu-id="1e094-151">Total number of sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e094-152"><strong>按形式列出的故障率</strong></span><span class="sxs-lookup"><span data-stu-id="1e094-152"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="1e094-153">否</span><span class="sxs-lookup"><span data-stu-id="1e094-153">No</span></span></p></td>
<td><p><span data-ttu-id="1e094-154">按形式分组的失败会话总数（例如，即时消息）。</span><span class="sxs-lookup"><span data-stu-id="1e094-154">Total number of failed sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1e094-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1e094-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

