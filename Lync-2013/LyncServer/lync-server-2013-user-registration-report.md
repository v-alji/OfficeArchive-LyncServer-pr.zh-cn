---
title: Lync Server 2013：用户注册报告
description: Lync Server 2013：用户注册报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User Registration Report
ms:assetid: 151d5cc9-cc1b-4cfa-be9c-55ebe321f7a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558614(v=OCS.15)
ms:contentKeyID: 48183486
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adb8ef7e94a24f0fd088f12e009fc9d63f3be9d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391990"
---
# <a name="user-registration-report-in-lync-server-2013"></a><span data-ttu-id="80c57-103">Lync Server 2013 中的用户注册报告</span><span class="sxs-lookup"><span data-stu-id="80c57-103">User Registration Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80c57-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80c57-104">

<span> </span></span></span>

<span data-ttu-id="80c57-105">_**主题上次修改时间：** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="80c57-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="80c57-106">"用户注册" 报表提供用户登录活动概述，有关在指定时间段内登录到 Microsoft Lync Server 2013 的用户数的最值得注意的信息 (每小时、每天、每周、每月) 。</span><span class="sxs-lookup"><span data-stu-id="80c57-106">The User Registration Report provides an overview of user logon activity, most notably information about the number of users who logged on to Microsoft Lync Server 2013 during a specified time period (hourly, daily, weekly, monthly).</span></span> <span data-ttu-id="80c57-107">请记住，报表仅告诉您登录的用户数。</span><span class="sxs-lookup"><span data-stu-id="80c57-107">Keep in mind that the report only tells you how many people logged on.</span></span> <span data-ttu-id="80c57-108">它不会告诉您登录 *的* 用户。</span><span class="sxs-lookup"><span data-stu-id="80c57-108">It does not tell you *which* people logged on.</span></span> <span data-ttu-id="80c57-109">监视报告不提供有关哪些特定用户使用 Lync Server 2013 (以及哪些特定用户未) 的信息。</span><span class="sxs-lookup"><span data-stu-id="80c57-109">Monitoring Reports do not provide information about which specific users are using Lync Server 2013 (and which ones are not).</span></span> <span data-ttu-id="80c57-110">但是，你可以使用 "用户活动" 报表大致估计用户信息。</span><span class="sxs-lookup"><span data-stu-id="80c57-110">However, you can get a rough estimate of user information by using the User Activity Report.</span></span>

<span data-ttu-id="80c57-111">在提供有关用户登录的信息时，用户注册报告会进行两项重要区分。</span><span class="sxs-lookup"><span data-stu-id="80c57-111">When providing information about user logons, the User Registration Report draws two important distinctions.</span></span> <span data-ttu-id="80c57-112">首先，它将登录细分为两个主要类别：内部登录和外部登录。</span><span class="sxs-lookup"><span data-stu-id="80c57-112">First, it breaks logons down into two primary categories: internal logons and external logons.</span></span> <span data-ttu-id="80c57-113">内部登录表示从组织防火墙内登录（即，在连接至企业网络时）的用户。</span><span class="sxs-lookup"><span data-stu-id="80c57-113">Internal logons represent users who logged on from inside your organization's firewall (that is, while connected to the corporate network).</span></span> <span data-ttu-id="80c57-114">外部登录表示从防火墙外部通过 Edge 服务器登录的用户 (例如，从 Internet 咖啡馆登录的用户将算作外部登录) 。</span><span class="sxs-lookup"><span data-stu-id="80c57-114">External logons represent users who logged on from outside the firewall through an Edge Server (for example, a user who logged on from an Internet café counts as an external logon).</span></span> <span data-ttu-id="80c57-115">如果需要了解从防火墙外登录的用户数，用户注册报告可为您提供此信息。</span><span class="sxs-lookup"><span data-stu-id="80c57-115">If you need to know how many of your users are logging on from outside the firewall, the User Registration Report can provide you with this information.</span></span>

<span data-ttu-id="80c57-116">此外，用户注册报告还会记录在给定时间段内在线的 *活动* 用户数。</span><span class="sxs-lookup"><span data-stu-id="80c57-116">In addition, the User Registration Report notes how many *active* users were present during a given time period.</span></span> <span data-ttu-id="80c57-117">活动用户是在即时消息 (IM) 会话中参与即时消息的用户，在这段时间内参与 Lync 会议、进行或接收电话呼叫或其他使用的 Lync Server。</span><span class="sxs-lookup"><span data-stu-id="80c57-117">An active user is a user who took part in an instant messaging (IM) session, participated in a Lync Meeting, made or received a phone call, or otherwise used Lync Server during that period of time.</span></span> <span data-ttu-id="80c57-118">这与登录但从未实际使用系统的用户不同。</span><span class="sxs-lookup"><span data-stu-id="80c57-118">This is different from a user who logged on, but never actually used the system.</span></span>

<div>

## <a name="accessing-the-user-registration-report"></a><span data-ttu-id="80c57-119">访问用户注册报告</span><span class="sxs-lookup"><span data-stu-id="80c57-119">Accessing the User Registration Report</span></span>

<span data-ttu-id="80c57-p104">只能从“监控报告”主页中访问用户注册报告。用户注册报告不链接至其他任何报告。</span><span class="sxs-lookup"><span data-stu-id="80c57-p104">You access the User Registration Report only from the Monitoring Reports home page. The User Registration Report does not link to any other reports.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-user-registration-report"></a><span data-ttu-id="80c57-122">充分利用用户注册报告</span><span class="sxs-lookup"><span data-stu-id="80c57-122">Making the Best Use of the User Registration Report</span></span>

<span data-ttu-id="80c57-123">在你部署 Lync Server 后，一个常见问题是：如何知道我的用户是否确实在使用此新技术？</span><span class="sxs-lookup"><span data-stu-id="80c57-123">After you've deployed Lync Server one commonly-asked question is this: How do I know if my users are actually using this new technology?</span></span> <span data-ttu-id="80c57-124">尽管对于这一点仍存在一些限制，但用户注册报告可以帮助您回答此问题。</span><span class="sxs-lookup"><span data-stu-id="80c57-124">Although it has a few limitations in this regard, the User Registration Report can help you answer this question.</span></span> <span data-ttu-id="80c57-125">若要确定用户是否正在使用 Lync Server，你需要执行两个操作。</span><span class="sxs-lookup"><span data-stu-id="80c57-125">To determine whether or not users are using Lync Server, you need to do two things.</span></span> <span data-ttu-id="80c57-126">首先，从用户注册报告中获取“唯一登录用户”指标的值。</span><span class="sxs-lookup"><span data-stu-id="80c57-126">First, get the value of the Unique logon users metric from the User Registration Report.</span></span> <span data-ttu-id="80c57-127">此值告诉你登录到 Lync 服务器的不同个人的人数。</span><span class="sxs-lookup"><span data-stu-id="80c57-127">This value tells you how many distinct individuals logged on to Lync Server.</span></span>

<span data-ttu-id="80c57-128">通过比较，"总登录" 指标显示任何人登录到 Lync 服务器的总次数。</span><span class="sxs-lookup"><span data-stu-id="80c57-128">By comparison, the Total logons metric shows how many total times anyone logged on to Lync Server.</span></span> <span data-ttu-id="80c57-129">例如，假设 Ken Myer 在一天内登录到 Lync Server 五个不同的时间。</span><span class="sxs-lookup"><span data-stu-id="80c57-129">For example, suppose Ken Myer logged on to Lync Server five different times in a single day.</span></span> <span data-ttu-id="80c57-130">在此情况下，Ken Myer 将在“登录总数”指标中记为五次单独的登录会话，但对于“唯一登录用户”指标只是一个登录用户。</span><span class="sxs-lookup"><span data-stu-id="80c57-130">In that case, Ken Myer would count as five separate logon sessions for the Total logons metric, but just one logon user for the Unique logon users metric.</span></span> <span data-ttu-id="80c57-131">同样，一个用户从多个设备或多个位置登录的情况也很常见。</span><span class="sxs-lookup"><span data-stu-id="80c57-131">Likewise, it's not uncommon for a user to log on from multiple devices or multiple locations.</span></span> <span data-ttu-id="80c57-132">例如，用户可以使用她的台式计算机（她的膝上型电脑）登录，并且她可以拥有自动登录 Lync Server 的 IP 电话。</span><span class="sxs-lookup"><span data-stu-id="80c57-132">For example, a user can log on using her desktop computer, her laptop computer, and she can have an IP phone that automatically logs on to Lync Server.</span></span> <span data-ttu-id="80c57-133">在此示例中，一个唯一用户登录三次。</span><span class="sxs-lookup"><span data-stu-id="80c57-133">In this example, there is one unique user with three logons.</span></span>

<span data-ttu-id="80c57-134">为了进一步解释登录总数和唯一登录之间的差别，请考虑下表中给定时间段的登录数。</span><span class="sxs-lookup"><span data-stu-id="80c57-134">To further explain the difference between total logons and unique logons, consider the logons for a given time period in the following table.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80c57-135">用户</span><span class="sxs-lookup"><span data-stu-id="80c57-135">User</span></span></th>
<th><span data-ttu-id="80c57-136">登录时间</span><span class="sxs-lookup"><span data-stu-id="80c57-136">Logon time</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80c57-137">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="80c57-137">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="80c57-138">7/7/2012 8:45 AM</span><span class="sxs-lookup"><span data-stu-id="80c57-138">7/7/2012 8:45 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c57-139">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="80c57-139">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="80c57-140">7/7/2012 8:46 AM</span><span class="sxs-lookup"><span data-stu-id="80c57-140">7/7/2012 8:46 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80c57-141">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="80c57-141">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="80c57-142">7/7/2012 9:17 AM</span><span class="sxs-lookup"><span data-stu-id="80c57-142">7/7/2012 9:17 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c57-143">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="80c57-143">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="80c57-144">7/7/2012 9:22 AM</span><span class="sxs-lookup"><span data-stu-id="80c57-144">7/7/2012 9:22 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80c57-145">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="80c57-145">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="80c57-146">7/7/2012 9:31 AM</span><span class="sxs-lookup"><span data-stu-id="80c57-146">7/7/2012 9:31 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80c57-p107">请注意，总共有五次登录；但只有两个唯一登录用户：Ken Myer（登录三次）和 Pilar Ackerman（登录两次）。这就是登录用户和唯一登录用户之间的差异。</span><span class="sxs-lookup"><span data-stu-id="80c57-p107">Notice that there is a total of five logons; however, there are only two unique logon users: Ken Myer (who logged on three times) and Pilar Ackerman (who logged on twice). That's the difference between logons and unique logon users.</span></span>

<span data-ttu-id="80c57-149">除了了解唯一登录次数外，你还需要了解已为 Lync Server 启用的用户总数。</span><span class="sxs-lookup"><span data-stu-id="80c57-149">In addition to knowing the number of unique logons, you need to know the total number of users who have been enabled for Lync Server.</span></span> <span data-ttu-id="80c57-150">通过打开 Lync Server 2013 命令行管理程序并运行以下 Windows PowerShell 命令，可以检索该值：</span><span class="sxs-lookup"><span data-stu-id="80c57-150">That value can be retrieved by opening the Lync Server 2013 Management Shell and running the following Windows PowerShell command:</span></span>

    (Get-CsUser).Count

<span data-ttu-id="80c57-151">如果前面的命令返回一个值1236和唯一的登录用户指标，则表示平均值为667，这表示每个用户每 (日实际登录到系统的时间为，667除以1236（大约是 54% ) ）。</span><span class="sxs-lookup"><span data-stu-id="80c57-151">If the preceding command returns a value of 1,236 and Unique logon users metric returns an average value of 667, that suggests that a little over half of your users enable for Lync are actually logging on to the system each day (that is, 667 divided by 1,236, which is approximately 54%).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="80c57-152">请记住，登录指标记录在指定时间段内实际登录的用户。</span><span class="sxs-lookup"><span data-stu-id="80c57-152">Keep in mind that the logon metrics record users who actually logged on during the specified time period.</span></span> <span data-ttu-id="80c57-153">他们不跟踪已登录到系统的用户。</span><span class="sxs-lookup"><span data-stu-id="80c57-153">They don't keep track of users who were already logged on to the system.</span></span> <span data-ttu-id="80c57-154">例如，如果唯一的登录用户指标显示667登录，并且您有1236用户，则表示您的用户登录到系统的一半。</span><span class="sxs-lookup"><span data-stu-id="80c57-154">For example, if your Unique logon users metric shows 667 logons and you have 1,236 users, that suggests that about half your users are logging on to the system.</span></span> <span data-ttu-id="80c57-155">但是，假设您开始检查登录数据时，300用户已登录到系统。</span><span class="sxs-lookup"><span data-stu-id="80c57-155">However, suppose 300 users were already logged on to the system at the time you began checking the logon data.</span></span> <span data-ttu-id="80c57-156">这意味着你真正拥有登录 Lync Server 的将近1000用户，这意味着更接近80% 的用户已登录。</span><span class="sxs-lookup"><span data-stu-id="80c57-156">That would mean that you actually had nearly 1,000 users logged on to Lync Server, which would mean that closer to 80% of your users were logged on.</span></span>



</div>

<span data-ttu-id="80c57-157">还应将“唯一登录用户”值与“唯一活动用户”指标的值进行比较。</span><span class="sxs-lookup"><span data-stu-id="80c57-157">You should also compare the Unique logon users value with the value of the Unique active users metric.</span></span> <span data-ttu-id="80c57-158">"唯一活动用户" 指标告诉你使用 Lync Server 的唯一用户数：他们进行了电话呼叫、加入 Lync 会议或参与 IM 会话。</span><span class="sxs-lookup"><span data-stu-id="80c57-158">The Unique active users metric tells you how many unique users actually used Lync Server: they made a phone call, they joined a Lync Meeting, or they participated in an IM session.</span></span> <span data-ttu-id="80c57-159">这是有用的信息，因为 Microsoft Lync 2013 可以配置为在用户每次启动 Windows 时自动启动。</span><span class="sxs-lookup"><span data-stu-id="80c57-159">This is useful information, because Microsoft Lync 2013 can be configured to automatically start each time a user starts Windows.</span></span> <span data-ttu-id="80c57-160">因此，你可能有大量用户在每天登录到 Windows 时自动登录到 Lync，但在该时间段内不会实际使用 Lync Server。</span><span class="sxs-lookup"><span data-stu-id="80c57-160">Because of that, you might have a large number of users who automatically log on to Lync when they log on to Windows each day, but then never actually use Lync Server during that time period.</span></span>

<span data-ttu-id="80c57-161">"唯一活动用户" 指标还会在组织中提供更有意义的数据，用户通常不会在一天结束时注销 Windows。</span><span class="sxs-lookup"><span data-stu-id="80c57-161">The Unique active users metric also provides more meaningful data in an organization where users typically do not log off Windows at the end of the day.</span></span> <span data-ttu-id="80c57-162">相反，他们只是锁定其计算机，让 Windows 和 Lync 保持运行。</span><span class="sxs-lookup"><span data-stu-id="80c57-162">Instead, they simply lock their computers and leave Windows and Lync running.</span></span> <span data-ttu-id="80c57-163">在此类情况下，由于用户在若干天之前登录并且从未注销，因此每天的登录数可能很少。</span><span class="sxs-lookup"><span data-stu-id="80c57-163">In a situation like that, you might end up with very few logons per day because your users logged on several days ago and never logged off.</span></span> <span data-ttu-id="80c57-164">但是，唯一的活动用户会告诉你用户是否正在使用 Lync 或其他 Lync Server 客户端。</span><span class="sxs-lookup"><span data-stu-id="80c57-164">However, Unique active users tells you whether users are actively using Lync or another Lync Server client.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="80c57-165">筛选器</span><span class="sxs-lookup"><span data-stu-id="80c57-165">Filters</span></span>

<span data-ttu-id="80c57-166">利用筛选器，您可以返回一组针对性更强的数据或通过不同的方式查看返回的数据。</span><span class="sxs-lookup"><span data-stu-id="80c57-166">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="80c57-167">例如，用户注册报告可让你查看所有注册机构池和边缘服务器的数据，或者查看单个池的数据。</span><span class="sxs-lookup"><span data-stu-id="80c57-167">For example, the User Registration Report enables you to view data for all your Registrar pool and Edge Servers or to view data for an individual pool.</span></span> <span data-ttu-id="80c57-168">您还可以选择数据的分组方式。</span><span class="sxs-lookup"><span data-stu-id="80c57-168">You can also choose how data should be grouped.</span></span> <span data-ttu-id="80c57-169">在此示例中，将按小时、日、周或月对注册进行分组。</span><span class="sxs-lookup"><span data-stu-id="80c57-169">In this case, registrations grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="80c57-170">下表列出了可用于用户注册报告的筛选器。</span><span class="sxs-lookup"><span data-stu-id="80c57-170">The following table lists the filters that you can use with the User Registration Report.</span></span>

### <a name="user-registration-report-filters"></a><span data-ttu-id="80c57-171">用户注册报告筛选器</span><span class="sxs-lookup"><span data-stu-id="80c57-171">User Registration Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80c57-172">名称</span><span class="sxs-lookup"><span data-stu-id="80c57-172">Name</span></span></th>
<th><span data-ttu-id="80c57-173">描述</span><span class="sxs-lookup"><span data-stu-id="80c57-173">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80c57-174"><strong>从</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-174"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-p113">时间范围的开始日期和时间。若要按小时查看数据，请输入开始日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="80c57-p113">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="80c57-177">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="80c57-177">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="80c57-p114">如果您未输入开始时间，该报告会自动将将某个特定日期的上午 12:00 作为开始时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="80c57-p114">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="80c57-180">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="80c57-180">7/7/2012</span></span></p>
<p><span data-ttu-id="80c57-181">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="80c57-181">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="80c57-182">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="80c57-182">7/3/2012</span></span></p>
<p><span data-ttu-id="80c57-183">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="80c57-183">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c57-184"><strong>到</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-184"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-p115">时间范围的结束日期和时间。若要按小时查看数据，请输入结束日期和时间，如下所示：</span><span class="sxs-lookup"><span data-stu-id="80c57-p115">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="80c57-187">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="80c57-187">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="80c57-p116">如果您未输入结束时间，该报告会自动将某个特定日期的上午 12:00 作为结束时间。若要按日查看数据，请只输入日期：</span><span class="sxs-lookup"><span data-stu-id="80c57-p116">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="80c57-190">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="80c57-190">7/7/2012</span></span></p>
<p><span data-ttu-id="80c57-191">若要按周或按月查看，请输入您要查看的周或月中的任一日期（您不必输入周或月的第一天）：</span><span class="sxs-lookup"><span data-stu-id="80c57-191">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="80c57-192">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="80c57-192">7/3/2012</span></span></p>
<p><span data-ttu-id="80c57-193">一周始终是从星期日开始至星期六结束。</span><span class="sxs-lookup"><span data-stu-id="80c57-193">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80c57-194"><strong>间隔</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-194"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-p117">时间间隔。选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="80c57-p117">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="80c57-197">每小时（最多可显示 25 个小时）</span><span class="sxs-lookup"><span data-stu-id="80c57-197">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="80c57-198">每天（最多可显示 31 天）</span><span class="sxs-lookup"><span data-stu-id="80c57-198">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="80c57-199">每周（最多可显示 12 周）</span><span class="sxs-lookup"><span data-stu-id="80c57-199">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="80c57-200">每月（最多可显示 12 个月）</span><span class="sxs-lookup"><span data-stu-id="80c57-200">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="80c57-201">如果开始日期和结束日期超出了所选间隔允许的最长时间，则仅显示最长时间（从开始日期开始）。</span><span class="sxs-lookup"><span data-stu-id="80c57-201">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="80c57-202">例如，如果选择 "开始日期 7/7/2012" 和 "结束日期 2/28/2012" 的 "每日间隔"，则会显示 8/7/2012 12:00 AM 至 9/7/2012 12:00 AM (的数据，即，总数据) 31 天。</span><span class="sxs-lookup"><span data-stu-id="80c57-202">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c57-203"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-203"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-204">注册器池或边缘服务器的完全限定域名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="80c57-204">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server.</span></span> <span data-ttu-id="80c57-205">可以选择单个池，也可以选择“<strong>[所有]</strong>”查看所有池的数据。</span><span class="sxs-lookup"><span data-stu-id="80c57-205">You can either select an individual pool or choose <strong>[All]</strong> to view data for all the pools.</span></span> <span data-ttu-id="80c57-206">系统根据数据库中的记录自动为您填充该下拉列表。</span><span class="sxs-lookup"><span data-stu-id="80c57-206">This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="80c57-207">指标</span><span class="sxs-lookup"><span data-stu-id="80c57-207">Metrics</span></span>

<span data-ttu-id="80c57-208">下表列出了用户注册报告中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="80c57-208">The following table lists the information provided in the User Registration Report.</span></span>

### <a name="user-registration-report-metrics"></a><span data-ttu-id="80c57-209">用户注册报告指标</span><span class="sxs-lookup"><span data-stu-id="80c57-209">User Registration Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80c57-210">名称</span><span class="sxs-lookup"><span data-stu-id="80c57-210">Name</span></span></th>
<th><span data-ttu-id="80c57-211">是否可按此项排序？</span><span class="sxs-lookup"><span data-stu-id="80c57-211">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="80c57-212">描述</span><span class="sxs-lookup"><span data-stu-id="80c57-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80c57-213"><strong>每小时</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-213"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="80c57-214"><strong>每天</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-214"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="80c57-215"><strong>每周</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-215"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="80c57-216"><strong>每月</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-216"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-217">否</span><span class="sxs-lookup"><span data-stu-id="80c57-217">No</span></span></p></td>
<td><p><span data-ttu-id="80c57-218">指示在筛选器工具栏上选择的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="80c57-218">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="80c57-219">如果适用，可单击某一给定的时间间隔以查看该间隔的详细信息。</span><span class="sxs-lookup"><span data-stu-id="80c57-219">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="80c57-220">例如，如果你使用的是每日间隔，并且单击 "7/7/2012"，你将看到该日期的用户注册活动的每小时细目。</span><span class="sxs-lookup"><span data-stu-id="80c57-220">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c57-221"><strong>登录总数</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-221"><strong>Total logons</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-222">否</span><span class="sxs-lookup"><span data-stu-id="80c57-222">No</span></span></p></td>
<td><p><span data-ttu-id="80c57-223">成功的登录会话总数。</span><span class="sxs-lookup"><span data-stu-id="80c57-223">Total number of successful logon sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80c57-224"><strong>内部登录数</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-224"><strong>Internal logons</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-225">否</span><span class="sxs-lookup"><span data-stu-id="80c57-225">No</span></span></p></td>
<td><p><span data-ttu-id="80c57-226">内部网络中的登录总数。</span><span class="sxs-lookup"><span data-stu-id="80c57-226">Total number of logons within the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c57-227"><strong>外部登录数</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-227"><strong>External logons</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-228">否</span><span class="sxs-lookup"><span data-stu-id="80c57-228">No</span></span></p></td>
<td><p><span data-ttu-id="80c57-229">内部网络之外使用边缘服务器的登录总数。</span><span class="sxs-lookup"><span data-stu-id="80c57-229">Total number of logons from outside the internal network, using the Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80c57-230"><strong>唯一登录用户数</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-230"><strong>Unique logon users</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-231">否</span><span class="sxs-lookup"><span data-stu-id="80c57-231">No</span></span></p></td>
<td><p><span data-ttu-id="80c57-p121">至少具有一个登录会话的用户总数。具有多个登录会话的用户算作一个用户，与只具有一个登录会话的用户相同。</span><span class="sxs-lookup"><span data-stu-id="80c57-p121">Total number of users who had at least one logon session. A user who had multiple logon sessions counts as one user, the same as a person who had just a single logon session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c57-234"><strong>唯一活动用户数</strong></span><span class="sxs-lookup"><span data-stu-id="80c57-234"><strong>Unique active users</strong></span></span></p></td>
<td><p><span data-ttu-id="80c57-235">否</span><span class="sxs-lookup"><span data-stu-id="80c57-235">No</span></span></p></td>
<td><p><span data-ttu-id="80c57-p122">对等会话或会议会话中涉及的用户总数。具有多个会话的用户算作一个用户，与只具有一个会话的用户相同。</span><span class="sxs-lookup"><span data-stu-id="80c57-p122">Total number of users who were involved in a peer-to-peer or conferencing session. A user who had multiple sessions counts as one user, the same as a person who had just a single session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="80c57-238">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80c57-238">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

