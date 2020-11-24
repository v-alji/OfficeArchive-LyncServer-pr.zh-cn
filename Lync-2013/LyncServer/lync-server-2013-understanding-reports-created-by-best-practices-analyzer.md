---
title: Lync Server 2013：了解最佳做法分析器创建的报告
description: Lync Server 2013：了解最佳做法分析器创建的报告。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding reports created by Best Practices Analyzer
ms:assetid: 1386dd6c-7f3e-4da9-905b-cef1468bf14a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591344(v=OCS.15)
ms:contentKeyID: 48183471
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5fbb84cdffe6e6e6f079c2d72aba4799f5538776
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392262"
---
# <a name="understanding-reports-created-by-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="613df-103">了解 Lync Server 2013 中由最佳做法分析器创建的报告</span><span class="sxs-lookup"><span data-stu-id="613df-103">Understanding reports created by Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="613df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="613df-104">

<span> </span></span></span>

<span data-ttu-id="613df-105">_**主题上次修改时间：** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="613df-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="613df-106">最佳做法分析器提供组织的多种类型的报表，以方便分析和解决问题。</span><span class="sxs-lookup"><span data-stu-id="613df-106">Best Practices Analyzer provides multiple types of reports that are organized to facilitate the analysis and resolution of issues.</span></span> <span data-ttu-id="613df-107">最佳做法分析器识别错误、警告和其他信息等问题。</span><span class="sxs-lookup"><span data-stu-id="613df-107">Best Practices Analyzer identifies issues such as errors, warnings, and other information.</span></span>

<div>

## <a name="reports"></a><span data-ttu-id="613df-108">报告会</span><span class="sxs-lookup"><span data-stu-id="613df-108">Reports</span></span>

<span data-ttu-id="613df-109">你可以通过查看以下每个报表来访问扫描结果：</span><span class="sxs-lookup"><span data-stu-id="613df-109">You can access the results of a scan by viewing each of the following reports:</span></span>

  - <span data-ttu-id="613df-110">**列表报表**   列表报表按特定条件进行组织。</span><span class="sxs-lookup"><span data-stu-id="613df-110">**List reports**   List reports are organized by specific criteria.</span></span> <span data-ttu-id="613df-111">你可以按类、严重性或问题排列结果。</span><span class="sxs-lookup"><span data-stu-id="613df-111">You can arrange the results by class, severity, or issue.</span></span> <span data-ttu-id="613df-112">例如，如果按类组织结果，则报表的 "董事" 部分下将包含与主管相关的问题。</span><span class="sxs-lookup"><span data-stu-id="613df-112">For example, if you organize results by class, issues related to Directors are included under the Directors section of the report.</span></span> <span data-ttu-id="613df-113">你可以查看所有问题，或仅查看信息性项目。</span><span class="sxs-lookup"><span data-stu-id="613df-113">You can view all of the issues, or just the informational items.</span></span> <span data-ttu-id="613df-114">您可以搜索特定项目（如内存）的列表报告。</span><span class="sxs-lookup"><span data-stu-id="613df-114">You can search a list report for specific items, such as memory.</span></span> <span data-ttu-id="613df-115">您也可以打印报表或将其导出。</span><span class="sxs-lookup"><span data-stu-id="613df-115">You can also print the report or export it.</span></span>

  - <span data-ttu-id="613df-116">**树报表**   树报表按用于运行扫描的规则和运行扫描时指定的其他选项进行组织。</span><span class="sxs-lookup"><span data-stu-id="613df-116">**Tree reports**   Tree reports are organized by the rules that are used to run the scan and other options that you specified at the time the scan was run.</span></span> <span data-ttu-id="613df-117">例如，与测试拓扑规则相关的问题包含在报告的 "测试拓扑" 部分中。</span><span class="sxs-lookup"><span data-stu-id="613df-117">For example, issues related to the Test Topology rules are included under the Test Topology section of the report.</span></span> <span data-ttu-id="613df-118">你可以查看所有问题的详细信息，或只查看问题摘要。</span><span class="sxs-lookup"><span data-stu-id="613df-118">You can view the details of all the issues, or just a summary of the issues.</span></span> <span data-ttu-id="613df-119">你可以搜索特定项目（如内存）的树报表。</span><span class="sxs-lookup"><span data-stu-id="613df-119">You can search a tree report for specific items, such as memory.</span></span> <span data-ttu-id="613df-120">您也可以打印报表或将其导出。</span><span class="sxs-lookup"><span data-stu-id="613df-120">You can also print the report or export it.</span></span>

  - <span data-ttu-id="613df-121">**其他报表**   其他报表中的项目包括扫描中包含的任务的运行时日志。</span><span class="sxs-lookup"><span data-stu-id="613df-121">**Other reports**   Items in other reports include the run-time log of tasks that were included in the scan.</span></span> <span data-ttu-id="613df-122">可以在其他报表中搜索特定项目（如内存）中的项目。</span><span class="sxs-lookup"><span data-stu-id="613df-122">You can search the items in other reports for specific items, such as memory.</span></span> <span data-ttu-id="613df-123">您也可以打印报表或将其导出。</span><span class="sxs-lookup"><span data-stu-id="613df-123">You can also print the report or export it.</span></span>

</div>

<div>

## <a name="issues"></a><span data-ttu-id="613df-124">故障</span><span class="sxs-lookup"><span data-stu-id="613df-124">Issues</span></span>

<span data-ttu-id="613df-125">最佳做法分析器生成的报告指示在扫描环境期间确定的特定问题，包括以下类型的问题：</span><span class="sxs-lookup"><span data-stu-id="613df-125">The reports generated by Best Practices Analyzer indicate specific issues that are identified during the scan of your environment, including following types of issues:</span></span>

  - <span data-ttu-id="613df-126">**错误**   需要在你的环境中进行更改的关键问题。</span><span class="sxs-lookup"><span data-stu-id="613df-126">**Errors**   Critical issues that require you to make a change in your environment.</span></span> <span data-ttu-id="613df-127">例如，如果未安装 Lync Server 2013 核心组件，则会记录错误。</span><span class="sxs-lookup"><span data-stu-id="613df-127">For example, if Lync Server 2013 Core Components are not installed, an error is logged.</span></span>

    <span data-ttu-id="613df-128">在报表中，使用红色 X 符号标识被归为错误的问题。</span><span class="sxs-lookup"><span data-stu-id="613df-128">Issues that are classified as errors are identified in the report by a red X symbol.</span></span> <span data-ttu-id="613df-129">错误将显示在 "**列表报告**" 视图的 "**所有问题**" 选项卡上，以及 "**详细视图**" 选项卡和 "**树报表**" 视图的 "**摘要视图**" 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="613df-129">Errors are displayed on the **All Issues** tab of the **List Reports** view, and on the **Detailed View** tab and the **Summary View** tab of the **Tree Reports** view.</span></span> <span data-ttu-id="613df-130">如果您不想在报表中看到特定错误，则可以指定不会为单个实例或报表中该错误的所有实例显示错误。</span><span class="sxs-lookup"><span data-stu-id="613df-130">If you do not want to see a specific error in a report, you can specify that the error not be shown for a single instance or for all instances of that error in the report.</span></span> <span data-ttu-id="613df-131">然后，该错误仅显示在 "**其他报表**" 视图的 "**隐藏项目**" 选项卡上，除非您更改设置并指定该错误显示在报表中。</span><span class="sxs-lookup"><span data-stu-id="613df-131">The error is then displayed only on the **Hidden Items** tab of the **Other Reports** view, unless you change the setting and specify that the error be displayed in the report.</span></span>

  - <span data-ttu-id="613df-132">**警告**   与最佳做法实现不一致的问题。</span><span class="sxs-lookup"><span data-stu-id="613df-132">**Warnings**   Issues that are not consistent with the implementation of a best practice.</span></span> <span data-ttu-id="613df-133">这可能会也可能不表示你的环境需要更改。</span><span class="sxs-lookup"><span data-stu-id="613df-133">This may or may not indicate the need for a change in your environment.</span></span> <span data-ttu-id="613df-134">问题可能是你不需要更改的特定设置的已知问题。</span><span class="sxs-lookup"><span data-stu-id="613df-134">The issue could be a known issue with a specific setting that you do not need to change.</span></span> <span data-ttu-id="613df-135">例如，未在服务器上启动的服务将记录为警告。</span><span class="sxs-lookup"><span data-stu-id="613df-135">For example, services that are not started on a server are logged as warnings.</span></span>

    <span data-ttu-id="613df-136">在报表中，使用三角黄色警告符号确定归类为警告的问题。</span><span class="sxs-lookup"><span data-stu-id="613df-136">Issues that are classified as warnings are identified in the report by a triangular yellow warning symbol.</span></span> <span data-ttu-id="613df-137">警告显示在 "**列表报告**" 视图的 "**所有问题**" 选项卡上，以及 "**详细视图**" 选项卡和 "**树报表**" 视图的 "**摘要视图**" 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="613df-137">Warnings are displayed on the **All Issues** tab of the **List Reports** view, as well as on the **Detailed View** tab and the **Summary View** tab of the **Tree Reports** view.</span></span> <span data-ttu-id="613df-138">如果您不想在报表中看到特定错误，则可以指定不会为单个实例或报表中该错误的所有实例显示错误。</span><span class="sxs-lookup"><span data-stu-id="613df-138">If you do not want to see a specific error in a report, you can specify that the error not be shown for a single instance or for all instances of that error in the report.</span></span> <span data-ttu-id="613df-139">警告仅显示在 "**其他报表**" 视图的 "**隐藏的项目**" 选项卡上，除非您更改设置并指定在报表中显示警告。</span><span class="sxs-lookup"><span data-stu-id="613df-139">The warning is then displayed only on the **Hidden Items** tab of the **Other Reports** view, unless you change the setting and specify that the warning be displayed in the report.</span></span>

  - <span data-ttu-id="613df-140">**信息**   包括未分类为错误或警告的所有问题。</span><span class="sxs-lookup"><span data-stu-id="613df-140">**Information**   Includes all issues that are not classified as errors or warnings.</span></span> <span data-ttu-id="613df-141">例如，Active Directory 域服务中 Lync Server 2013 标准版服务器对象的数量被分类为信息问题。</span><span class="sxs-lookup"><span data-stu-id="613df-141">For example, the number of Lync Server 2013 Standard Edition server objects in Active Directory Domain Services is classified as an information issue.</span></span>

    <span data-ttu-id="613df-142">信息问题显示在 "**列表报告**" 视图的 "**所有问题**" 选项卡上，以及 "**树报表**" 视图的 "**详细视图**" 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="613df-142">Information issues are displayed on the **All Issues** tab of the **List Reports** view, and on the **Detailed View** tab of the **Tree Reports** view.</span></span>

<span data-ttu-id="613df-143">Lync Server 2013，最佳做法分析器不会对你的环境进行更改来解决问题。</span><span class="sxs-lookup"><span data-stu-id="613df-143">The Lync Server 2013, Best Practices Analyzer does not make changes to your environment to resolve issues.</span></span> <span data-ttu-id="613df-144">扫描仅检测潜在问题，并提供报告，其中包含有关如何解决每个问题的信息。</span><span class="sxs-lookup"><span data-stu-id="613df-144">The scan only detects potential issues and provides reports that contain information about how to resolve each issue.</span></span>

<span data-ttu-id="613df-145">如果单击某个问题，将显示特定问题的说明和某些选项。</span><span class="sxs-lookup"><span data-stu-id="613df-145">If you click an issue, an explanation and some options are displayed for specific issues.</span></span> <span data-ttu-id="613df-146">然后，您可以执行以下任一操作：</span><span class="sxs-lookup"><span data-stu-id="613df-146">Then, you can do any of the following:</span></span>

  - <span data-ttu-id="613df-147">查找有关该问题的更多详细信息，以及如何解决该问题。</span><span class="sxs-lookup"><span data-stu-id="613df-147">Find more detailed information about the issue, and how to resolve it.</span></span>

  - <span data-ttu-id="613df-148">停止在报表中显示问题：</span><span class="sxs-lookup"><span data-stu-id="613df-148">Stop showing issues in reports:</span></span>

      - <span data-ttu-id="613df-149">停止显示所选实例的问题。</span><span class="sxs-lookup"><span data-stu-id="613df-149">Stop showing issues for the selected instance.</span></span>

      - <span data-ttu-id="613df-150">停止显示该问题的所有实例的相关问题。</span><span class="sxs-lookup"><span data-stu-id="613df-150">Stop showing issues for all instances of that issue.</span></span>

    <span data-ttu-id="613df-151">若要查看已停止显示在报表中的问题，请转到 "**其他报表**" 视图的 "**隐藏项目**" 选项卡。</span><span class="sxs-lookup"><span data-stu-id="613df-151">To see the issues you have stopped showing in reports, go to the **Hidden Items** tab of the **Other Reports** view.</span></span> <span data-ttu-id="613df-152">在此处，你可以指定再次开始显示报表中的问题。</span><span class="sxs-lookup"><span data-stu-id="613df-152">From there, you can specify to start showing issues in reports again.</span></span>

<span data-ttu-id="613df-153">有关解决特定问题的详细信息，请参阅 [分析和解决 Lync Server 2013 中由最佳做法分析器标识的问题](lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md)。</span><span class="sxs-lookup"><span data-stu-id="613df-153">For details about resolving specific issues, see [Analyzing and resolving issues identified by Best Practices Analyzer in Lync Server 2013](lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md).</span></span>

<span data-ttu-id="613df-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="613df-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
