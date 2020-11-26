---
title: Lync Server 2013： IP 电话清点报告
description: Lync Server 2013： IP 电话清点报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP Phone Inventory Report
ms:assetid: aa7d6b31-cb09-4e68-b020-aa5dd0081c20
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615027(v=OCS.15)
ms:contentKeyID: 48185044
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3bc05017775ad64e0e18f876215aa2c6b3882bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426737"
---
# <a name="ip-phone-inventory-report-in-lync-server-2013"></a><span data-ttu-id="c54ea-103">Lync Server 2013 中的 IP 电话清单报告</span><span class="sxs-lookup"><span data-stu-id="c54ea-103">IP Phone Inventory Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c54ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c54ea-104">

<span> </span></span></span>

<span data-ttu-id="c54ea-105">_**主题上次修改时间：** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="c54ea-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="c54ea-p101">IP 电话清单报告会报告有关您的组织中目前所使用的 IP 电话的信息。IP 清单报告提供了在指定的报告期间实际上所使用的详细 IP 电话列表。除此之外，管理员还可以通过此报告了解是否存在应进行替换但仍在使用中的任何旧的、过时的电话；该报告还可以就组织中存在很少使用的昂贵电话这一实际情况，向管理员发出警报。当应该购买新电话或重新分配现有的电话时，该类型的信息非常重要。（例如，可能要求很少使用其昂贵电话的用户与较为频繁使用其电话的用户交换电话。）</span><span class="sxs-lookup"><span data-stu-id="c54ea-p101">The IP Phone Inventory Report reports information about the IP phones currently in use in your organization. The IP Inventory Report provides a detailed list of the IP phones that were actually used during the specified reporting period. Among other things, this report lets administrators know if there are any old, outdated phones still in use that should be replaced; it can also alert administrators to the fact that there are expensive phones in the organization that are rarely being used. That type of information can be invaluable when it comes time to purchase new phones or to redistribute existing phones. (For example, a user who rarely uses his or her expensive phone might be asked to swap phones with a user who uses his or her phone much more frequently.)</span></span>

<span data-ttu-id="c54ea-111">值得注意的是，此报告在用作真正的清单报告时存在几点限制。</span><span class="sxs-lookup"><span data-stu-id="c54ea-111">It should be noted that this report does have a few limitations when it comes to being used as a true inventory report.</span></span> <span data-ttu-id="c54ea-112">首先，IP 电话报告只列出在指定时间段内登录到 Lync 服务器的所有电话，并按其上次登录时间进行排序。</span><span class="sxs-lookup"><span data-stu-id="c54ea-112">For one thing, the IP Phone Report simply lists all the phones that logged on to Lync Server during the specified time period, sorted by their last logon time.</span></span> <span data-ttu-id="c54ea-113">如果某个电话在指定的时间段内未登录，那么就不会在清单报告中列出。</span><span class="sxs-lookup"><span data-stu-id="c54ea-113">If a phone did not log on during the specified time period then it will not be listed in the inventory report.</span></span> <span data-ttu-id="c54ea-114">这包括在该时间段开始前已登录并且在指定的时间间隔内仍保持登录的电话。</span><span class="sxs-lookup"><span data-stu-id="c54ea-114">That includes phones that logged on before the time period started and were still logged on during the specified time interval.</span></span> <span data-ttu-id="c54ea-115">例如，假设您想要查看七月2012的所有电话清单。</span><span class="sxs-lookup"><span data-stu-id="c54ea-115">For example, suppose you wanted to look at all the phone inventory for July, 2012.</span></span> <span data-ttu-id="c54ea-116">假设您在2012年6月30日登录 Lync Server 的多个电话仍在7月1日登录。</span><span class="sxs-lookup"><span data-stu-id="c54ea-116">Suppose, as well, that several phones logged on to Lync Server on June 30, 2012 and were still logged on as of July 1st.</span></span> <span data-ttu-id="c54ea-117">这些电话将不会在 7 月 1 日的清单报告上出现。</span><span class="sxs-lookup"><span data-stu-id="c54ea-117">Those phones will not show up on the inventory report for July 1st.</span></span>

<span data-ttu-id="c54ea-118">还必须注意的是，清单报告可能包括您的组织不再使用的电话。</span><span class="sxs-lookup"><span data-stu-id="c54ea-118">It's also important to note that the inventory report could include phones that your organization no longer uses.</span></span> <span data-ttu-id="c54ea-119">例如，假设有许多 Fabrikam 电话在2012年7月1日登录到系统上;5天后，您的组织会删除所有这些 Fabrikam 手机，并使用较新的 Contoso 型号替换它们。</span><span class="sxs-lookup"><span data-stu-id="c54ea-119">For example, suppose a number of Fabrikam phones logged on to the system on July 1, 2012; 5 days later your organization got rid of all those Fabrikam phones and replaced them with a newer Contoso model.</span></span> <span data-ttu-id="c54ea-120">Fabrikam 电话仍会显示在“清单”报告中，原因很简单，就是它们在 7 月份已登录到系统。</span><span class="sxs-lookup"><span data-stu-id="c54ea-120">The Fabrikam phones will still appear on the "inventory" report simply because they logged on to the system during the month of July.</span></span>

<span data-ttu-id="c54ea-p104">此外，IP 电话清单报告不会报告不同类型的电话总数摘要。例如，假设您拥有 105 个 Polycom CX600 电话。该报告不会告知您拥有 105 个此类电话；相反，您只会看到 105 个单独的 Polycom Cx600 条目。知道有 105 个 Polycom Cx600 条目的唯一方法是手动计算其中每一个条目。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p104">In addition, the IP Phone Inventory Report does not report summary totals for the different types of phones. For example, suppose you have 105 Polycom CX600 phones. The report will not tell you that you have 105 of these phones; instead, you will simply see 105 separate entries for the Polycom Cx600. The only way to know that there are 105 entries for the Polycom Cx600 would be to count each of those entries manually.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="c54ea-125">或者，导出数据，然后使用 Microsoft Excel 或 Windows PowerShell 为您进行计数。</span><span class="sxs-lookup"><span data-stu-id="c54ea-125">Or, export the data and use Microsoft Excel or Windows PowerShell to do that counting for you.</span></span>



</div>

<div>

## <a name="accessing-the-ip-phone-inventory-report"></a><span data-ttu-id="c54ea-126">访问 IP 电话清单报告</span><span class="sxs-lookup"><span data-stu-id="c54ea-126">Accessing the IP Phone Inventory Report</span></span>

<span data-ttu-id="c54ea-p105">可以从“监控报告”主页访问 IP 电话清单报告。如果您单击“用户 URI”指标，即可访问该用户的“用户活动报告”。针对对等呼叫单击“最后一次活动”指标，会将您带到“对等会话详细信息报告”；针对会议单击相同的指标，会将您带到“会议详细信息报告”。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p105">The IP Phone Inventory Report is accessed from the Monitoring Reports home page. If you click the User URI metric you can access the User Activity Report for that user. Clicking the Last activity metric for a peer-to-peer call will take you to the Peer-to-Peer Session Detail Report; clicking that same metric for a conference will take you to the Conference Detail Report.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-ip-phone-inventory-report"></a><span data-ttu-id="c54ea-130">充分利用 IP 电话清单报告</span><span class="sxs-lookup"><span data-stu-id="c54ea-130">Making the Best Use of the IP Phone Inventory Report</span></span>

<span data-ttu-id="c54ea-131">如果您只对一种特定类型电话的使用信息感兴趣 (例如，"用户使用 Polycom CX600 电话的频率是多少？") 您可以通过筛选特定类型的电话直接从 IP 电话清点报告获取该信息。</span><span class="sxs-lookup"><span data-stu-id="c54ea-131">If you're only interested in usage information for one particular kind of phone (for example, "How often are users using a Polycom CX600 phone?") you can get that information directly from the IP Phone Inventory Report by filtering for that particular kind of phone.</span></span> <span data-ttu-id="c54ea-132">但是，如果您想要了解所有电话的摘要信息（多少人正在使用 Polycom CX600、多少人正在使用 LG-Nortel IP8540 等），则需要导出数据，然后使用另一个应用程序（如 Windows PowerShell）执行该类型的分析。</span><span class="sxs-lookup"><span data-stu-id="c54ea-132">However, if you want summary information for all your phones (how many people are using a Polycom CX600, how many are using an LG-Nortel IP8540, etc.) then you will need to export the data and use another application (such as Windows PowerShell) to do that type of analysis.</span></span> <span data-ttu-id="c54ea-133">例如，假设你将数据导出到逗号分隔值文件 (C： \\ 数据 \\ IP \_ 手机 \_ 清点 \_Report.csv) 。</span><span class="sxs-lookup"><span data-stu-id="c54ea-133">For example, suppose you export the data to a comma-separated values file (C:\\Data\\IP\_Phone\_Inventory\_Report.csv).</span></span> <span data-ttu-id="c54ea-134">在这种情况下，您可以使用以下这两个命令提供所有电话的摘要数据：</span><span class="sxs-lookup"><span data-stu-id="c54ea-134">In that case, you could use these two commands to provide summary data for all your phones:</span></span>

    $phones = Import-Csv "C:\Data\IP_Phone_Inventory_Report.csv"
    $phones |Group-Object Manufacturer, "Hardware version" | Select-Object Count, Name | Sort-Object Count -Descending

<span data-ttu-id="c54ea-135">这将返回与以下类似的数据：</span><span class="sxs-lookup"><span data-stu-id="c54ea-135">That will return data similar to this:</span></span>

    Count    Name
    -----    ----
      267    POLYCOM, CX700
      267    POLYCOM, CX600
      166    POLYCOM, C
       68    Microsoft, CPE
       64    LG-Nortel, IP8540
       59    Aastra, 6725ip
       37    LG-Nortel, IP
       22    POLYCOM, CX3000
       11    Microsoft, CPE_A
        9    POLYCOM, CX500
        7    Aastra, 6721ip

<span data-ttu-id="c54ea-136">类似地，这两个命令会告诉您哪些电话已登录到系统，但实际上从未用来发出呼叫（“最后一次活动”指标的值为空白，表示没有任何最后一次活动）：</span><span class="sxs-lookup"><span data-stu-id="c54ea-136">Similarly, these two commands tell you which phones logged on to the system but were never actually used to make a call (the value of the Last activity metric is blank, indicating that there hasn't been any last activity):</span></span>

    $phones = Import-Csv "C:\Data\IP_Phone_Inventory_Report.csv"
    $phones | Where-Object {$_."Last activity" -eq ""}

<span data-ttu-id="c54ea-137">针对尚未使用的每一个电话，将返回与以下类似的数据：</span><span class="sxs-lookup"><span data-stu-id="c54ea-137">That returns data similar to this for each phone that has not been used:</span></span>

    Manufacturer     : POLYCOM
    Hardware version : CX600
    MAC address      : 00-04-F2-00-01-76
    User URI         : 422
    User agent       : CPE/4.0.7423.1 OCPhone/4.0.7423.1 (Microsoft Lync 2010 (Beta) Phone Edition)
    Last logon time  : 8/30/2010 4:44:48 PM
    Last logoff time : 8/30/2010 5:59:07 PM
    Last activity    :

<span data-ttu-id="c54ea-138">使用 IP 电话清单报告的另一种有趣的方式如下：如果您具有 IP 电话的 MAC 地址，则只需在 MAC 地址文本框中输入该地址，即可判断最后一次使用该电话的用户。</span><span class="sxs-lookup"><span data-stu-id="c54ea-138">Another interesting way to use the IP Phone Inventory Report is this: if you have the MAC address of an IP Phone you can find out the user who last used that phone simply by entering that address in the MAC address text box.</span></span> <span data-ttu-id="c54ea-139">然后，IP 电话清单报告将返回使用该电话最后一次登录的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="c54ea-139">The IP Phone Inventory report will then report back (among other things) the SIP address of the user who last logged on with that phone.</span></span> <span data-ttu-id="c54ea-140">或者，您可以在“用户 URI”前缀框中输入用户 SIP 地址，以查明该用户已使用的所有电话。</span><span class="sxs-lookup"><span data-stu-id="c54ea-140">Alternatively, you can enter a user SIP address (in the User URI prefix box) to find out all the phones that have been used by that user.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="c54ea-141">筛选器</span><span class="sxs-lookup"><span data-stu-id="c54ea-141">Filters</span></span>

<span data-ttu-id="c54ea-p108">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。例如，通过 IP 电话清单，您可以只查看特定公司制造的电话，甚至只查看这些电话的某个特定版本。您还可以选择数据的分组方式。在此示例中，将按小时、日、周或月对注册进行分组。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the IP Phone Inventory enables you to view only the phones manufactured by a specific company, or even a specific version of those phones. You can also choose how data should be grouped. In this case, registrations are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="c54ea-146">下表列出了可用于 IP 电话清单报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="c54ea-146">The following table lists the filters that you can use with the IP Phone Inventory Report.</span></span>

### <a name="ip-phone-inventory-report-filters"></a><span data-ttu-id="c54ea-147">IP 电话清单报告筛选器</span><span class="sxs-lookup"><span data-stu-id="c54ea-147">IP Phone Inventory Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c54ea-148">名称</span><span class="sxs-lookup"><span data-stu-id="c54ea-148">Name</span></span></th>
<th><span data-ttu-id="c54ea-149">描述</span><span class="sxs-lookup"><span data-stu-id="c54ea-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-150"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-p109">时间范围的开始日期/时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c54ea-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="c54ea-153">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="c54ea-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="c54ea-p110">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="c54ea-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="c54ea-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="c54ea-156">7/7/2012</span></span></p>
<p><span data-ttu-id="c54ea-157">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="c54ea-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="c54ea-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="c54ea-158">7/3/2012</span></span></p>
<p><span data-ttu-id="c54ea-159">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="c54ea-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-160"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-p111">时间范围的结束日期/时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c54ea-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="c54ea-163">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="c54ea-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="c54ea-p112">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="c54ea-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="c54ea-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="c54ea-166">7/7/2012</span></span></p>
<p><span data-ttu-id="c54ea-167">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="c54ea-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="c54ea-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="c54ea-168">7/3/2012</span></span></p>
<p><span data-ttu-id="c54ea-169">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="c54ea-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-170"><strong>制造商</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-170"><strong>Manufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-p113">制造 IP 电话的公司的名称。此筛选器的值将根据数据库中当前存有的 IP 电话自动填充。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p113">Name of the company that manufactured the IP phone. The values for this filter are automatically populated for you based on the IP phones that are currently in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-173"><strong>硬件版本</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-173"><strong>Hardware version</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-174">IP 电话的版本号；使用您可以专门识别特定电话类型的制造商和硬件版本筛选器。</span><span class="sxs-lookup"><span data-stu-id="c54ea-174">Version number of the IP phone; by using the Manufacturer and the Hardware version filters you can uniquely identity a particular type of phone.</span></span> <span data-ttu-id="c54ea-175">此筛选器的值将根据数据库中当前存有的 IP 电话自动填充。</span><span class="sxs-lookup"><span data-stu-id="c54ea-175">The values for this filter are automatically populated for you based on the IP phones that are currently in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-176"><strong>用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-176"><strong>User agent</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-p115">IP 电话使用的软件的标识符。此筛选器的值将根据数据库中当前存有的 IP 电话自动填充。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p115">Identifier for the software used by the IP phone. The values for this filter are automatically populated for you based on the IP phones currently in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-179"><strong>MAC 地址</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-179"><strong>MAC address</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-p116">IP 电话的网络接口的唯一标识符。媒体访问控制 (MAC) 地址通常在电话制造时分配，并硬接线到设备硬件。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p116">Unique identifier for the network interface on the IP phone. The Media Access Control (MAC) address is typically assigned at the time the phone is manufactured and is hard-wired into the device hardware.</span></span></p>
<p><span data-ttu-id="c54ea-p117">要搜索与特定 MAC 地址有关的记录，只需输入该地址。例如：</span><span class="sxs-lookup"><span data-stu-id="c54ea-p117">To search for records pertaining to a specific MAC address simply enter that address. For example:</span></span></p>
<p><span data-ttu-id="c54ea-184">00-08-5D-16-16-48</span><span class="sxs-lookup"><span data-stu-id="c54ea-184">00-08-5D-16-16-48</span></span></p>
<p><span data-ttu-id="c54ea-p118">您必须输入完整地址。只输入一部分地址（例如 00-08-5D）不会返回任何数据。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p118">You must enter the complete address. A partial address (for example 00-08-5D) does not return any data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-187"><strong>此天数前的最后一次活动</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-187"><strong>Last activity before days</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-188">选择下列值之一：</span><span class="sxs-lookup"><span data-stu-id="c54ea-188">Select one of the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="c54ea-189">[所有]</span><span class="sxs-lookup"><span data-stu-id="c54ea-189">[All]</span></span></p></li>
<li><p><span data-ttu-id="c54ea-190">10</span><span class="sxs-lookup"><span data-stu-id="c54ea-190">10</span></span></p></li>
<li><p><span data-ttu-id="c54ea-191">名</span><span class="sxs-lookup"><span data-stu-id="c54ea-191">20</span></span></p></li>
<li><p><span data-ttu-id="c54ea-192">大约</span><span class="sxs-lookup"><span data-stu-id="c54ea-192">30</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-193"><strong>此天数前的最后注销时间</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-193"><strong>Last logoff time before days</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-194">选择下列值之一：</span><span class="sxs-lookup"><span data-stu-id="c54ea-194">Select one of the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="c54ea-195">[所有]</span><span class="sxs-lookup"><span data-stu-id="c54ea-195">[All]</span></span></p></li>
<li><p><span data-ttu-id="c54ea-196">10</span><span class="sxs-lookup"><span data-stu-id="c54ea-196">10</span></span></p></li>
<li><p><span data-ttu-id="c54ea-197">名</span><span class="sxs-lookup"><span data-stu-id="c54ea-197">20</span></span></p></li>
<li><p><span data-ttu-id="c54ea-198">大约</span><span class="sxs-lookup"><span data-stu-id="c54ea-198">30</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-199"><strong>用户 URI 前缀</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-199"><strong>User URI prefix</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-200">使用 IP 电话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="c54ea-200">SIP address of the user who used the IP phone.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="c54ea-201">指标</span><span class="sxs-lookup"><span data-stu-id="c54ea-201">Metrics</span></span>

<span data-ttu-id="c54ea-202">下表列出了 IP 电话清单报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="c54ea-202">The following table lists the information provided in the IP Phone Inventory Report.</span></span>

### <a name="ip-phone-inventory-report-metrics"></a><span data-ttu-id="c54ea-203">IP 电话清单报告指标</span><span class="sxs-lookup"><span data-stu-id="c54ea-203">IP Phone Inventory Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c54ea-204">名称</span><span class="sxs-lookup"><span data-stu-id="c54ea-204">Name</span></span></th>
<th><span data-ttu-id="c54ea-205">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="c54ea-205">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c54ea-206">描述</span><span class="sxs-lookup"><span data-stu-id="c54ea-206">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-207"><strong>制造商</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-207"><strong>Manufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-208">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-209">制造 IP 电话的公司的名称。</span><span class="sxs-lookup"><span data-stu-id="c54ea-209">Name of the company that manufactured the IP phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-210"><strong>硬件版本</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-210"><strong>Hardware version</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-211">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-212">IP 电话的版本号。</span><span class="sxs-lookup"><span data-stu-id="c54ea-212">Version number of the IP phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-213"><strong>MAC 地址</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-213"><strong>MAC address</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-214">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-p119">IP 电话的网络接口的唯一标识符。MAC 地址通常在电话制造时分配，并硬接线到设备硬件。</span><span class="sxs-lookup"><span data-stu-id="c54ea-p119">Unique identifier for the network interface on the IP phone. The MAC address is typically assigned at the time the phone is manufactured and is hard-wired into the device hardware.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-217"><strong>用户 URI</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-217"><strong>User URI</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-218">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-218">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-219">使用 IP 电话的用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="c54ea-219">SIP address of the user who used the IP phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-220"><strong>用户代理</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-220"><strong>User agent</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-221">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-222">IP 电话使用的软件的标识符。</span><span class="sxs-lookup"><span data-stu-id="c54ea-222">Identifier for the software used by the IP phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-223"><strong>上次登录时间</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-223"><strong>Last logon time</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-224">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-225">IP 电话上次登录到 Lync Server 的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c54ea-225">Date and time that the IP phone last logged on to Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c54ea-226"><strong>上次注销时间</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-226"><strong>Last logoff time</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-227">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-228">IP 电话上次从 Lync Server 注销的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c54ea-228">Date and time that the IP phone last logged off from Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c54ea-229"><strong>最后一次活动</strong></span><span class="sxs-lookup"><span data-stu-id="c54ea-229"><strong>Last activity</strong></span></span></p></td>
<td><p><span data-ttu-id="c54ea-230">是</span><span class="sxs-lookup"><span data-stu-id="c54ea-230">Yes</span></span></p></td>
<td><p><span data-ttu-id="c54ea-231">上一次使用 IP 电话的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="c54ea-231">Date and time that the IP phone was last used.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c54ea-232">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c54ea-232">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

