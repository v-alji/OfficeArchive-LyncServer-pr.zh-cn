---
title: Lync Server 2013：周任务
description: Lync Server 2013：周任务。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Weekly tasks
ms:assetid: d564839b-b49d-4c5d-b67e-dc5abb0f6980
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722432(v=OCS.15)
ms:contentKeyID: 63969650
ms.date: 08/20/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d818e1140141a470bb57a1471bb04931f505a6bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443844"
---
# <a name="weekly-tasks-in-lync-server-2013"></a><span data-ttu-id="6f7cd-103">Lync Server 2013 中的周任务</span><span class="sxs-lookup"><span data-stu-id="6f7cd-103">Weekly tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f7cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f7cd-104">

<span> </span></span></span>

<span data-ttu-id="6f7cd-105">_**主题上次修改时间：** 2015-08-17_</span><span class="sxs-lookup"><span data-stu-id="6f7cd-105">_**Topic Last Modified:** 2015-08-17_</span></span>

<span data-ttu-id="6f7cd-106">每周任务通常与收集和分析日志和报告相关。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-106">Weekly tasks are generally related to collecting and analyzing logs and reports.</span></span>

<div>

## <a name="archive-event-logs"></a><span data-ttu-id="6f7cd-107">存档事件日志</span><span class="sxs-lookup"><span data-stu-id="6f7cd-107">Archive event logs</span></span>

<span data-ttu-id="6f7cd-108">如果事件日志未配置为根据需要覆盖事件，则必须定期存档并删除这些事件。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-108">If event logs are not configured to overwrite events as required, they must be regularly archived and deleted.</span></span> <span data-ttu-id="6f7cd-109">此操作对安全日志特别重要，在调查尝试的安全违规时可能需要这样做。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-109">This action is especially important for security logs, which may be required when investigating attempted security breaches.</span></span>

<span data-ttu-id="6f7cd-110">您的组织将必须定义日志存档的策略和过程。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-110">Your organization will have to define policies and procedures for log archiving.</span></span>

</div>

<div>

## <a name="create-reports"></a><span data-ttu-id="6f7cd-111">创建报表</span><span class="sxs-lookup"><span data-stu-id="6f7cd-111">Create reports</span></span>

<span data-ttu-id="6f7cd-112">创建状态报告以帮助进行容量规划、SLA 审查和性能分析。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-112">Create status reports to help with capacity planning, SLA reviews, and performance analysis.</span></span> <span data-ttu-id="6f7cd-113">使用事件日志和系统监视器中的每日数据创建有关磁盘、内存和 CPU 使用率的报告。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-113">Use daily data from event log and System Monitor to create reports on disk, memory, and CPU usage.</span></span> <span data-ttu-id="6f7cd-114">使用 System Center Operations Manager 生成正常运行时间和可用性报告。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-114">Use System Center Operations Manager to generate uptime and availability reports.</span></span>

<span data-ttu-id="6f7cd-115">您的组织将必须定义状态报告的策略和过程。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-115">Your organization will have to define policies and procedures for status reports.</span></span>

</div>

<div>

## <a name="incident-reports"></a><span data-ttu-id="6f7cd-116">事件报告</span><span class="sxs-lookup"><span data-stu-id="6f7cd-116">Incident reports</span></span>

<span data-ttu-id="6f7cd-117">对与 Lync Server 相关的组织事件报告执行每周审核。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-117">Perform a weekly audit of your organization’s incident reports that relate to Lync Server.</span></span> <span data-ttu-id="6f7cd-118">本审核应包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-118">This audit should include the following:</span></span>

  - <span data-ttu-id="6f7cd-119">最热门的生成、已解决和挂起事件。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-119">The top generated, resolved, and pending incidents.</span></span>

  - <span data-ttu-id="6f7cd-120">未解决的事件的解决方案。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-120">Solutions for unresolved incidents.</span></span>

  - <span data-ttu-id="6f7cd-121">将报表更新为包含新的故障票证。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-121">Updating reports to include new trouble tickets.</span></span>

  - <span data-ttu-id="6f7cd-122">为疑难解答指南更新文档存储库并发布有关中断的剖析。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-122">Updating a document repository for troubleshooting guides and post mortems about outages.</span></span>

<span data-ttu-id="6f7cd-123">由于组织的事件跟踪系统是独立于 Lync Server 的选项，因此特定说明或指针不可用。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-123">Since your organization’s incident tracking system is a choice independent of Lync Server, specific instructions or pointers are not available.</span></span> <span data-ttu-id="6f7cd-124">请参阅你的组织选择的系统的文档。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-124">Consult the documentation for the system your organization chose.</span></span>

</div>

<div>

## <a name="check-iis-logs-and-performance"></a><span data-ttu-id="6f7cd-125">检查 IIS 日志和性能</span><span class="sxs-lookup"><span data-stu-id="6f7cd-125">Check IIS logs and performance</span></span>

<span data-ttu-id="6f7cd-126"> (IIS) 日志和性能，对 Internet 信息服务执行每周查看。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-126">Perform a weekly review of Internet Information Services (IIS) logs and performance.</span></span> <span data-ttu-id="6f7cd-127">有关如何监视 IIS 日志和性能的详细信息，请参阅 [Windows Server 2003 Internet 信息服务 (IIS) 事件日志概述](https://go.microsoft.com/fwlink/?linkid=36077)。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-127">For more information about how to monitor IIS logs and performance, see [Windows Server 2003 Internet Information Services (IIS) Event Logging Overview](https://go.microsoft.com/fwlink/?linkid=36077).</span></span> <span data-ttu-id="6f7cd-128">评审应包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-128">The review should include the following:</span></span>

  - <span data-ttu-id="6f7cd-129">用于监视 WWW 服务缓存的 Web 服务缓存计数器。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-129">Web Service Cache counters to monitor the WWW service cache.</span></span>

  - <span data-ttu-id="6f7cd-130"> (Asp) 计数器的活动服务器页面，用于监视以 Asp 的形式运行的应用程序。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-130">Active Server Pages (ASPs) counters to monitor applications that run as ASPs.</span></span>

</div>

<div>

## <a name="generate-database-reports"></a><span data-ttu-id="6f7cd-131">生成数据库报告</span><span class="sxs-lookup"><span data-stu-id="6f7cd-131">Generate database reports</span></span>

<span data-ttu-id="6f7cd-132">**生成 SQL 数据库报表**</span><span class="sxs-lookup"><span data-stu-id="6f7cd-132">**To generate reports on the SQL Database**</span></span>

1.  <span data-ttu-id="6f7cd-133">打开 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-133">Open Lync Server 2013.</span></span>

2.  <span data-ttu-id="6f7cd-134">在控制台树中，展开 "林" 节点，展开 " **企业版池**"，然后单击要为其生成数据库报告的池。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-134">In the console tree, expand the forest node, expand **Enterprise pools**, and then click the pool for which you want to generate a database report.</span></span>

3.  <span data-ttu-id="6f7cd-135">在 "详细信息" 窗格中，单击 " **数据库** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-135">In the details pane, click the **Database** tab.</span></span>

4.  <span data-ttu-id="6f7cd-136">在 " **数据库** " 选项卡上，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-136">On the **Database** tab, do the following:</span></span>
    
    1.  <span data-ttu-id="6f7cd-137">若要查看数据库的名称，请展开 " **常规设置**"，然后查看数据库名称。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-137">To view the name of the database, expand **General Settings**, and view the database name.</span></span>
    
    2.  <span data-ttu-id="6f7cd-138">若要检索池的当前用户汇总统计信息，请展开 " **用户摘要报告**"，单击 " **转到**"，然后查看结果。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-138">To retrieve current user summary statistics for the pool, expand **User Summary Reports**, click **Go**, and view the results.</span></span>
    
    3.  <span data-ttu-id="6f7cd-139">若要检索池的单个用户的当前每用户数据，请展开 " **每用户报告**"，键入用户的 SIP URI，单击 " **转到**"，然后查看结果。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-139">To retrieve current per-user data for a single user of the pool, expand **Per-User Reports**, type the user’s SIP URI, click **Go**, and view the results.</span></span>

<span data-ttu-id="6f7cd-140">若要检索池的当前会议摘要统计信息，请展开 " **会议摘要" 报表**，单击 " **转到**"，然后查看结果。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-140">To retrieve current conference summary statistics for the pool, expand **Conference Summary Reports**, click **Go**, and view the results.</span></span>

</div>

<div>

## <a name="check-for-security-and-lync-server-updates"></a><span data-ttu-id="6f7cd-141">检查安全和 Lync 服务器更新</span><span class="sxs-lookup"><span data-stu-id="6f7cd-141">Check for security and Lync Server updates</span></span>

<span data-ttu-id="6f7cd-142">标识任何新服务包、修补程序或更新。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-142">Identify any new service packs, hotfixes, or updates.</span></span> <span data-ttu-id="6f7cd-143">如果适用，请在测试实验室中测试这些项，并使用更改控制过程安排部署到生产服务器。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-143">If appropriate, test these in a test lab, and use the change control procedures to arrange for deployment to the production servers.</span></span> <span data-ttu-id="6f7cd-144">此外，Lync Server 组件更新现已作为 Windows 更新的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-144">Also, Lync Server component updates are now available as part of Windows update.</span></span> <span data-ttu-id="6f7cd-145">所有 Lync Server 组件更新都必须在运行 Lync Server 的所有服务器上同时更新，这些更新均适用于这些更新。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-145">All Lync Server component updates must be updated at the same time on all of the servers that are running Lync Server for which the updates are applicable.</span></span>

</div>

<div>

## <a name="run-the-lync-server-2013-best-practice-analyzer"></a><span data-ttu-id="6f7cd-146">运行 Lync Server 2013 最佳做法分析器</span><span class="sxs-lookup"><span data-stu-id="6f7cd-146">Run the Lync Server 2013 Best Practice Analyzer</span></span>

<span data-ttu-id="6f7cd-147">Lync Server 2013 最佳做法分析器工具是一种诊断工具，用于收集配置信息并确定是否根据 Microsoft 最佳做法设置配置。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-147">The Lync Server 2013 Best Practices Analyzer Tool is a diagnostic tool that collects configuration information and determines whether the configuration is set according to Microsoft best practices.</span></span> <span data-ttu-id="6f7cd-148">此工具的文档位于 [Lync Server 2013 最佳做法分析器](lync-server-2013-lync-server-best-practices-analyzer.md)中。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-148">Documentation for this tool is at [Lync Server 2013 Best Practices Analyzer](lync-server-2013-lync-server-best-practices-analyzer.md).</span></span>

<span data-ttu-id="6f7cd-149">该工具将部署的配置数据与 Lync Server 的一组预定义的规则进行比较，并报告潜在问题。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-149">The tool compares your deployment’s configuration data against a set of pre-defined rules for Lync Server, and reports potential issues.</span></span> <span data-ttu-id="6f7cd-150">对于报告的每个问题，该工具都提供了 Lync Server 环境中的当前配置和推荐的配置。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-150">For every issue reported, the tool provides the current configuration in the Lync Server environment, and the recommended configuration.</span></span>

<span data-ttu-id="6f7cd-151">使用正确的网络访问，该工具可以检查运行 Lync Server 2013 的 AD DS 和服务器，以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-151">With the correct network access, the tool can examine your AD DS and servers that are running Lync Server 2013 to do the following:</span></span>

  - <span data-ttu-id="6f7cd-152">主动执行运行状况检查，验证是否根据推荐的最佳做法设置了配置</span><span class="sxs-lookup"><span data-stu-id="6f7cd-152">Proactively perform health checks, verifying that the configuration is set according to recommended best practices</span></span>

  - <span data-ttu-id="6f7cd-153">生成问题列表，如 "最优" 配置设置或不支持或不推荐的选项</span><span class="sxs-lookup"><span data-stu-id="6f7cd-153">Generate a list of issues, such as suboptimal configuration settings or unsupported or not recommended options</span></span>

  - <span data-ttu-id="6f7cd-154">判断系统的常规运行状况</span><span class="sxs-lookup"><span data-stu-id="6f7cd-154">Judge the general health of a system</span></span>

  - <span data-ttu-id="6f7cd-155">帮助解决特定问题</span><span class="sxs-lookup"><span data-stu-id="6f7cd-155">Help troubleshoot specific issues</span></span>

  - <span data-ttu-id="6f7cd-156">提示您下载更新（如果有）</span><span class="sxs-lookup"><span data-stu-id="6f7cd-156">Prompt you to download updates if they are available</span></span>

  - <span data-ttu-id="6f7cd-157">提供有关报告问题的联机文档和本地文档，包括疑难解答提示</span><span class="sxs-lookup"><span data-stu-id="6f7cd-157">Provide online and local documentation about reported issues, and include troubleshooting tips</span></span>

  - <span data-ttu-id="6f7cd-158">生成可供将来查看的配置信息</span><span class="sxs-lookup"><span data-stu-id="6f7cd-158">Generate configuration information that can be captured for later review</span></span>

<span data-ttu-id="6f7cd-159">确保 RTCBPA.msi 安装在所有 Lync Server 2013 服务器上，并生成每周运行状况检查报告。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-159">Ensure that the RTCBPA.msi is installed on all Lync Server 2013 servers, and generate a weekly Health Check Report.</span></span> <span data-ttu-id="6f7cd-160">注意结果并更正错误（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-160">Note the results and correct, if necessary.</span></span>

</div>

<div>

## <a name="review-sla-performance-figures"></a><span data-ttu-id="6f7cd-161">查看 SLA 性能数据</span><span class="sxs-lookup"><span data-stu-id="6f7cd-161">Review SLA performance figures</span></span>

<span data-ttu-id="6f7cd-162">检查上一周的关键性能数据。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-162">Check the key performance data for the previous week.</span></span> <span data-ttu-id="6f7cd-163">根据 SLA 的要求查看性能。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-163">Review performance against the requirements of the SLA.</span></span> <span data-ttu-id="6f7cd-164">确定未满足其目标的趋势和项目。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-164">Identify trends and items that have not met their targets.</span></span>

</div>

<div>

## <a name="review-system-center-operations-manager-management-pack-and-quality-of-experience-reports"></a><span data-ttu-id="6f7cd-165">查看 System Center Operations Manager 管理包和体验报告质量</span><span class="sxs-lookup"><span data-stu-id="6f7cd-165">Review System Center Operations Manager Management Pack and quality of experience reports</span></span>

<span data-ttu-id="6f7cd-166">获取和查看 Lync Server 2013 管理包和体验报告质量。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-166">Obtain and review Lync Server 2013 Management Pack and Quality of Experience reports.</span></span>

</div>

<div>

## <a name="generating-and-viewing-database-reports-for-enterprise-pools"></a><span data-ttu-id="6f7cd-167">生成和查看企业版池的数据库报告</span><span class="sxs-lookup"><span data-stu-id="6f7cd-167">Generating and viewing database reports for enterprise pools</span></span>

<span data-ttu-id="6f7cd-168">**生成池报告**</span><span class="sxs-lookup"><span data-stu-id="6f7cd-168">**To generate pool reports**</span></span>

1.  <span data-ttu-id="6f7cd-169">打开 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-169">Open Lync Server 2013.</span></span>

2.  <span data-ttu-id="6f7cd-170">在控制台树中，展开 "林" 节点，展开 " **企业版池**"，然后单击要为其生成数据库报告的池。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-170">In the console tree, expand the forest node, expand **Enterprise pools**, and then click the pool for which you want to generate a database report.</span></span>

3.  <span data-ttu-id="6f7cd-171">在 "详细信息" 窗格中，单击 " **数据库** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-171">In the details pane, click the **Database** tab.</span></span>

4.  <span data-ttu-id="6f7cd-172">在 " **数据库** " 选项卡上，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-172">On the **Database** tab, do the following:</span></span>
    
    1.  <span data-ttu-id="6f7cd-173">若要查看数据库的名称，请展开 " **常规设置**"，然后查看数据库名称。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-173">To view the name of the database, expand **General Settings**, and view the database name.</span></span>
    
    2.  <span data-ttu-id="6f7cd-174">若要检索池的当前用户汇总统计信息，请展开 " **用户摘要报告**"，单击 " **转到**"，然后查看结果。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-174">To retrieve current user summary statistics for the pool, expand **User Summary Reports**, click **Go**, and view the results.</span></span>
    
    3.  <span data-ttu-id="6f7cd-175">若要检索池的单个用户的当前每用户数据，请展开 " **每用户报告**"，键入用户的 SIP URI，单击 " **转到**"，然后查看结果。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-175">To retrieve current per-user data for a single user of the pool, expand **Per-User Reports**, type the user’s SIP URI, click **Go**, and view the results.</span></span>

<span data-ttu-id="6f7cd-176">若要检索池的当前会议摘要统计信息，请展开 " **会议摘要" 报表**，单击 " **转到**"，然后查看结果。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-176">To retrieve current conference summary statistics for the pool, expand **Conference Summary Reports**, click **Go**, and view the results.</span></span>

<span data-ttu-id="6f7cd-177">对于每个企业版池，管理员可以使用 " **数据库** " 选项卡查看数据库名称，并从数据库中检索和查看报表。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-177">For each Enterprise Pool, administrators can use the **Database** tab to view the database name and retrieve and view reports from the database.</span></span>

### <a name="database-reports-and-descriptions"></a><span data-ttu-id="6f7cd-178">数据库报告和说明</span><span class="sxs-lookup"><span data-stu-id="6f7cd-178">Database Reports and Descriptions</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f7cd-179">部分</span><span class="sxs-lookup"><span data-stu-id="6f7cd-179">Section</span></span></th>
<th><span data-ttu-id="6f7cd-180">说明</span><span class="sxs-lookup"><span data-stu-id="6f7cd-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f7cd-181">用户摘要报告</span><span class="sxs-lookup"><span data-stu-id="6f7cd-181">User Summary Reports</span></span></p></td>
<td><p><span data-ttu-id="6f7cd-182">Dbanalyze/v/report：/sqlserver： value]</span><span class="sxs-lookup"><span data-stu-id="6f7cd-182">Dbanalyze /v /report:diag [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="6f7cd-183">此部分显示有关池中用户的聚合信息，例如启用的用户数、每位用户的平均联系人数以及特定功能的用户数。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-183">This section displays aggregate information about users in a pool, such as the number of enabled users, the average number of contacts per user, and the number of users for specific features.</span></span></p>
<p><span data-ttu-id="6f7cd-184">使用这些报表时，以下信息可能会有所帮助：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-184">When using these reports, the following information may be helpful:</span></span></p>
<ul>
<li><p><span data-ttu-id="6f7cd-185">已启用的用户是通过使用 Active Directory 用户和计算机管理单元启用 Lync Server 2013 的用户。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-185">An enabled user is a user who is enabled for Lync Server 2013 by using the Active Directory Users and Computers Snap-in.</span></span></p></li>
<li><p><span data-ttu-id="6f7cd-186">活动用户是已登录或已注册的用户。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-186">An active user is a user who has logged on or registered.</span></span></p></li>
<li><p><span data-ttu-id="6f7cd-187">摘要报告还提供了一组有关联系人的统计信息。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-187">The summary reports also offer a set of statistical information about contacts.</span></span> <span data-ttu-id="6f7cd-188">这些统计信息仅适用于至少已登录过一次且至少有一个联系人的用户的人口。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-188">These statistics are only valid for the population of users who have logged on at least one time, and who have at least one contact.</span></span> <span data-ttu-id="6f7cd-189">因此，你通常看不到最少数量的联系人。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-189">Consequently, you'll typically not see a minimum number of contacts of 0.</span></span> <span data-ttu-id="6f7cd-190">由于此行为，如果用户没有联系人 (但处于活动状态，则在用户注册) 的情况下，你可能会看到： &lt; &gt; 对于某些统计信息字段为空。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-190">Because of this behavior, if a user has no contacts (but is active, in that the user has registered), you may see: &lt;empty&gt; for some statistics fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f7cd-191">Per-User 报表</span><span class="sxs-lookup"><span data-stu-id="6f7cd-191">Per-User Reports</span></span></p></td>
<td><p><span data-ttu-id="6f7cd-192">Dbanalyze/v/report： disk [/sqlserver： value]</span><span class="sxs-lookup"><span data-stu-id="6f7cd-192">Dbanalyze /v /report:disk [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="6f7cd-193">与通过用户填充计算的摘要报表不同，这些报表是有关特定用户的报表。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-193">Unlike the summary reports, which are calculated over a user population, these are reports about a specific user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f7cd-194">会议摘要报告</span><span class="sxs-lookup"><span data-stu-id="6f7cd-194">Conference Summary Reports</span></span></p></td>
<td><p><span data-ttu-id="6f7cd-195">Dbanalyze/v/report：会议 [/sqlserver： value]</span><span class="sxs-lookup"><span data-stu-id="6f7cd-195">Dbanalyze /v /report:conf [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="6f7cd-196">此部分显示有关池的会议摘要统计信息（例如活动会议数和参与者总数）的聚合信息。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-196">This section displays aggregate information about conference summary statistics for the pool, such as the number of active conferences and total number of participants.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="running-bandwidth-utilization-analyzer"></a><span data-ttu-id="6f7cd-197">运行带宽利用率分析器</span><span class="sxs-lookup"><span data-stu-id="6f7cd-197">Running Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="6f7cd-198">带宽用量分析器工具可创建有关企业网络中各个 WAN 链路上 UC 端点的带宽消耗的各种视图的报告。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-198">Bandwidth Utilization Analyzer is a tool that creates reports about various views of bandwidth consumption by the UC endpoints across WAN links in the enterprise network.</span></span> <span data-ttu-id="6f7cd-199">这些报告可用于了解当前带宽使用模式，并有助于进行带宽容量规划。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-199">These reports can be used to understand the current bandwidth consumption pattern and to help with bandwidth capacity planning.</span></span> <span data-ttu-id="6f7cd-200">它还会循环访问分配给各个链路的带宽容量。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-200">It also iterates on the bandwidth capacity that is assigned to various links.</span></span>

<span data-ttu-id="6f7cd-201">此工具可执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-201">This tool does the following:</span></span>

  - <span data-ttu-id="6f7cd-202">通过网络生成特定于音频使用情况的报告</span><span class="sxs-lookup"><span data-stu-id="6f7cd-202">Generates specific reports for audio usage over the network</span></span>

  - <span data-ttu-id="6f7cd-203">帮助更高效地进行容量规划并循环访问分配给各个链路的带宽容量</span><span class="sxs-lookup"><span data-stu-id="6f7cd-203">Helps with more effective capacity planning and iteration on the bandwidth capacity that is assigned to various links</span></span>

<span data-ttu-id="6f7cd-204">带宽利用率分析器可生成带宽容量和使用情况报告的图形化图形。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-204">Bandwidth Utilization Analyzer can generate graphical plots of bandwidth capacity and usage reports.</span></span> <span data-ttu-id="6f7cd-205">它们如下所示：</span><span class="sxs-lookup"><span data-stu-id="6f7cd-205">They are as follows:</span></span>

  - <span data-ttu-id="6f7cd-206">企业网络中的所有 WAN 链路</span><span class="sxs-lookup"><span data-stu-id="6f7cd-206">All the WAN links in the enterprise network</span></span>

  - <span data-ttu-id="6f7cd-207">已选择的所选 WAN 链接进行筛选</span><span class="sxs-lookup"><span data-stu-id="6f7cd-207">Filtered by selected WAN links that were chosen</span></span>

  - <span data-ttu-id="6f7cd-208">按已超过链路容量的 WAN 链路进行筛选</span><span class="sxs-lookup"><span data-stu-id="6f7cd-208">Filtered by WAN links that have exceeded link capacity</span></span>

  - <span data-ttu-id="6f7cd-209">使用预配带宽下的 WAN 链接进行筛选</span><span class="sxs-lookup"><span data-stu-id="6f7cd-209">Filtered by WAN links that were under-using the provisioned bandwidth</span></span>

  - <span data-ttu-id="6f7cd-210">按关键级别进行筛选的 WAN 链接 (大于90% 的 WAN link 带宽容量的带宽使用情况) </span><span class="sxs-lookup"><span data-stu-id="6f7cd-210">Filter by WAN links that were reaching critical levels (a bandwidth usage that is greater than 90 percent of bandwidth capacity of the WAN link)</span></span>

  - <span data-ttu-id="6f7cd-211">按 WAN 链接类型（网络-网站链接、interregional 链接和网站内的链接）进行筛选</span><span class="sxs-lookup"><span data-stu-id="6f7cd-211">Filtered by WAN link type—network-site links, interregional links, and links inside a site</span></span>

  - <span data-ttu-id="6f7cd-212">按网络区域进行筛选</span><span class="sxs-lookup"><span data-stu-id="6f7cd-212">Filtered by network region</span></span>

<span data-ttu-id="6f7cd-213">有关此工具的文档在 [Lync Server 2013 资源工具包工具文档](https://go.microsoft.com/fwlink/?linkid=623245)中提供。</span><span class="sxs-lookup"><span data-stu-id="6f7cd-213">Documentation for this tool is available at [Lync Server 2013 Resource Kit Tools Documentation](https://go.microsoft.com/fwlink/?linkid=623245).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f7cd-214">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f7cd-214">See Also</span></span>


[<span data-ttu-id="6f7cd-215">每周任务清单</span><span class="sxs-lookup"><span data-stu-id="6f7cd-215">Weekly task checklist</span></span>](lync-server-2013-operations-checklists.md)  
  

<span data-ttu-id="6f7cd-216"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f7cd-216"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

