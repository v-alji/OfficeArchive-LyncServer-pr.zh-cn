---
title: Lync Server 2013：容量和可用性管理
description: Lync Server 2013：容量和可用性管理。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity and availability management
ms:assetid: 207a2997-f482-4bee-892d-d2b112294481
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720325(v=OCS.15)
ms:contentKeyID: 63969586
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d498649651f8cfbccc65f5b1b5f010025ac418e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435598"
---
# <a name="capacity-and-availability-management-in-lync-server-2013"></a><span data-ttu-id="81f69-103">Lync Server 2013 中的容量和可用性管理</span><span class="sxs-lookup"><span data-stu-id="81f69-103">Capacity and availability management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81f69-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81f69-104">

<span> </span></span></span>

<span data-ttu-id="81f69-105">_**主题上次修改时间：** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="81f69-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="81f69-106">容量管理和可用性管理的目的是衡量和控制系统性能。</span><span class="sxs-lookup"><span data-stu-id="81f69-106">The purpose of capacity management and availability management is to measure and control system performance.</span></span> <span data-ttu-id="81f69-107">我们建议你实施容量管理和可用性管理过程，以便你可以测量和控制系统性能。</span><span class="sxs-lookup"><span data-stu-id="81f69-107">We recommend that you implement capacity management and availability management procedures so that you can measure and control system performance.</span></span> <span data-ttu-id="81f69-108">你必须知道系统是否可用，以及它是否可以通过设置基线并监视系统以查找趋势来处理当前和所投影的请求。</span><span class="sxs-lookup"><span data-stu-id="81f69-108">You have to know whether the system is available and if it can handle the current and the projected demands by setting baselines and monitoring the system to look for trends.</span></span>

<div>

## <a name="capacity-management"></a><span data-ttu-id="81f69-109">容量管理</span><span class="sxs-lookup"><span data-stu-id="81f69-109">Capacity management</span></span>

<span data-ttu-id="81f69-110">容量管理涉及规划、调整大小和控制服务容量，以帮助确保超过你的 SLA 中指定的最低性能级别。</span><span class="sxs-lookup"><span data-stu-id="81f69-110">Capacity management involves planning, sizing, and controlling service capacity to help guarantee that the minimum performance levels specified in your SLA are exceeded.</span></span> <span data-ttu-id="81f69-111">良好的容量管理有助于确保你能够以合理的成本提供 IT 服务，并且仍能满足你在你的 Sla 中定义的性能级别和客户端。</span><span class="sxs-lookup"><span data-stu-id="81f69-111">Good capacity management helps ensure that you can provide IT services at a reasonable cost and still meet the levels of performance defined in your SLAs with the client.</span></span> <span data-ttu-id="81f69-112">这些条件可以包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="81f69-112">These criteria can include the following:</span></span>

  - <span data-ttu-id="81f69-113">**系统响应时间**   这是系统执行典型操作所需的测量时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-113">**System Response Time**   This is the measured time that the system takes to do typical actions.</span></span> <span data-ttu-id="81f69-114">示例包括音频/视频服务器角色处理音频/视频流量所需的时间、客户创建和加入会议所需的时间或在所有观察者客户端中更新状态所需的时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-114">Examples include the time that is required for the audio/video server role to process audio/video traffic, the time that is required for a client to create and join a conference, or the time taken for presence to be updated in all watcher clients.</span></span>

  - <span data-ttu-id="81f69-115">**存储容量**   这是存储系统的容量，无论它是内容数据库、备份设备还是本地驱动器。</span><span class="sxs-lookup"><span data-stu-id="81f69-115">**Storage Capacity**   This is the capacity of a storage system, whether it is a content database, a backup device, or a local drive.</span></span> <span data-ttu-id="81f69-116">示例包括每个网站提供的最大存储空间量以及备份在覆盖之前应存储的时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-116">Examples include the maximum amount of storage space to be provided per site and the time that backups should be stored before they are overwritten.</span></span>

<span data-ttu-id="81f69-117">调整容量通常是指确保有足够的物理资源可用，例如磁盘空间和网络带宽。</span><span class="sxs-lookup"><span data-stu-id="81f69-117">Adjusting capacity is frequently a case of making sure that enough physical resources are available, such as disk space and network bandwidth.</span></span> <span data-ttu-id="81f69-118">下表列出了与容量相关的问题的典型分辨率。</span><span class="sxs-lookup"><span data-stu-id="81f69-118">The following table lists typical resolutions for capacity-related issues.</span></span>

### <a name="typical-resolutions-for-capacity-related-issues"></a><span data-ttu-id="81f69-119">与容量相关的问题的典型解决方案</span><span class="sxs-lookup"><span data-stu-id="81f69-119">Typical resolutions for capacity-related issues</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81f69-120">问题</span><span class="sxs-lookup"><span data-stu-id="81f69-120">Issue</span></span></th>
<th><span data-ttu-id="81f69-121">可能的解决方法</span><span class="sxs-lookup"><span data-stu-id="81f69-121">Possible resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81f69-122">音频/视频性能较差的远程用户</span><span class="sxs-lookup"><span data-stu-id="81f69-122">Remote users having poor audio/video performance</span></span></p></td>
<td><p><span data-ttu-id="81f69-123">检查以查看 WAN 链接是否提供合适的带宽，以及是否已启用和正确配置 QoS。</span><span class="sxs-lookup"><span data-stu-id="81f69-123">Check to see whether appropriate bandwidth is available on the WAN links and if QoS is enabled and appropriately configured.</span></span> <span data-ttu-id="81f69-124">检查 QoE 数据。</span><span class="sxs-lookup"><span data-stu-id="81f69-124">Check QoE data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81f69-125">Lync 环境的整体响应速度较慢。</span><span class="sxs-lookup"><span data-stu-id="81f69-125">Overall response of the Lync environment is slow.</span></span></p></td>
<td><p><span data-ttu-id="81f69-126">运行测试以检查现有前端服务器是否可以处理负载。</span><span class="sxs-lookup"><span data-stu-id="81f69-126">Run tests to check that the existing front-end servers can deal with the load.</span></span> <span data-ttu-id="81f69-127">引入新的前端服务器（如果需要）。检查 SQL 数据库响应时间并修复延迟的原因 (例如，改善磁盘输入/输出) 。</span><span class="sxs-lookup"><span data-stu-id="81f69-127">Introduce a new front-end server if it is needed.Check SQL database response times and fix the causes for the delays (for example, improve disk I/O).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="81f69-128">有关更多详细信息的疑难解答将在 Lync Server 网络指南中介绍。</span><span class="sxs-lookup"><span data-stu-id="81f69-128">Troubleshooting in greater detail is covered in the Lync Server Networking Guide.</span></span>

<span data-ttu-id="81f69-129">容量受系统配置的影响，取决于物理资源（如网络带宽）。</span><span class="sxs-lookup"><span data-stu-id="81f69-129">Capacity is affected by system configuration and depends on physical resources such as network bandwidth.</span></span> <span data-ttu-id="81f69-130">例如，如果将 Lync 环境配置为在夜间执行完整备份，则必须小心，以帮助确保对最终用户体验的交互式性能的影响最小。</span><span class="sxs-lookup"><span data-stu-id="81f69-130">For example, if a Lync environment is configured to perform a full backup nightly, care must be taken to help guarantee that the effect on the interactive performance experienced by end-users is minimized.</span></span>

<span data-ttu-id="81f69-131">容量管理是在可接受的级别内保持系统容量并解决以下问题的过程：</span><span class="sxs-lookup"><span data-stu-id="81f69-131">Capacity management is the process of keeping the capacity of a system within acceptable levels and addresses the following issues:</span></span>

  - <span data-ttu-id="81f69-132">对 **要求的更改做出反应**  必须对产能需求进行调整，以考虑系统或组织中的更改。</span><span class="sxs-lookup"><span data-stu-id="81f69-132">**Reacting to changes in requirements**   Capacity requirements have to be adjusted to account for changes in the system or the organization.</span></span> <span data-ttu-id="81f69-133">例如，如果你的环境决定实现企业语音，则中介服务器和公共交换电话网络的数量和位置 (PSTN) 网关将非常重要。</span><span class="sxs-lookup"><span data-stu-id="81f69-133">For example, if your environment decides to implement Enterprise Voice, the number and placement of Mediation Servers and public switched telephone network (PSTN) gateways will be very important.</span></span> <span data-ttu-id="81f69-134">如果你将执行会话初始协议 (SIP) 中继或直接 SIP，整体设计将显著改变，以提供最佳的企业语音性能。</span><span class="sxs-lookup"><span data-stu-id="81f69-134">If you'll be doing Session Initiation Protocol (SIP) trunking or direct SIP, the overall design will be significantly changed to provide the best Enterprise Voice performance.</span></span>

  - <span data-ttu-id="81f69-135">**预测未来要求**   某些容量要求随时间的推移而变化。</span><span class="sxs-lookup"><span data-stu-id="81f69-135">**Predicting future requirements**   Some capacity requirements change predictably over time.</span></span> <span data-ttu-id="81f69-136">通过跟踪趋势，你可以提前规划升级。</span><span class="sxs-lookup"><span data-stu-id="81f69-136">By tracking trends you can plan upgrades in advance.</span></span> <span data-ttu-id="81f69-137">例如，必须监视各种 Lync 网站之间的可用带宽才能创建基线。</span><span class="sxs-lookup"><span data-stu-id="81f69-137">For example, available bandwidth between various Lync sites must be monitored to create a baseline.</span></span> <span data-ttu-id="81f69-138">此基线将允许你预测何时必须为这些链接添加更多带宽，因为这些远程网站中的用户计数会随着时间的增加而增加。</span><span class="sxs-lookup"><span data-stu-id="81f69-138">This baseline will allow you to predict when you have to add more bandwidth to these links as user count in these remote sites increases with time.</span></span>

</div>

<div>

## <a name="availability-management"></a><span data-ttu-id="81f69-139">可用性管理</span><span class="sxs-lookup"><span data-stu-id="81f69-139">Availability management</span></span>

<span data-ttu-id="81f69-140">可用性管理是确保任何 IT 服务一致、经济高效地提供客户所需的一致、可靠服务级别的过程。</span><span class="sxs-lookup"><span data-stu-id="81f69-140">Availability management is the process of making sure that any IT service consistently and cost effectively delivers the level of consistent, reliable service that is required by the customer.</span></span> <span data-ttu-id="81f69-141">可用性管理处理的服务损失最小，并确保在服务丢失时采取相应措施。</span><span class="sxs-lookup"><span data-stu-id="81f69-141">Availability management deals with minimizing loss of service and with making sure that appropriate action is taken if service is lost.</span></span> <span data-ttu-id="81f69-142">在 Lync 环境中，你可能关心企业语音服务是否可用、用户是否可以加入计划的会议等。</span><span class="sxs-lookup"><span data-stu-id="81f69-142">In a Lync environment, you may be concerned about whether the Enterprise Voice service is available, whether users can join scheduled conferences, and so on.</span></span> <span data-ttu-id="81f69-143">SLA 定义了可接受的频率和中断长度，并允许在系统不可用于计划维护时获得特定时间段。</span><span class="sxs-lookup"><span data-stu-id="81f69-143">An SLA defines an acceptable frequency and length of outages and allows for certain periods when the system is unavailable for planned maintenance.</span></span>

<span data-ttu-id="81f69-144">如果你必须向管理层提供有关系统可用性的报表，或者如果你有财务或与缺少可用性目标相关的其他处罚，则必须记录可用性数据。</span><span class="sxs-lookup"><span data-stu-id="81f69-144">If you have to provide reports to your management about the availability of systems, or if you have financial or other penalties associated with missing availability targets, you must record availability data.</span></span> <span data-ttu-id="81f69-145">即使你没有这种正式的要求，也最好至少知道系统在特定时间段内失败的频率。</span><span class="sxs-lookup"><span data-stu-id="81f69-145">Even if you do not have such formal requirements, it is a good idea to at least know how frequently a system has failed in a certain time period.</span></span> <span data-ttu-id="81f69-146">例如，过去12个月中的系统可用性以及从每次失败恢复所需的时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-146">For example, system availability in the last 12 months and how long it took to recover from each failure.</span></span> <span data-ttu-id="81f69-147">此信息将帮助你衡量和改进你的团队对系统故障做出响应的有效性。</span><span class="sxs-lookup"><span data-stu-id="81f69-147">This information will help you measure and improve your team’s effectiveness in responding to a system failure.</span></span> <span data-ttu-id="81f69-148">如果存在争议，它还可以提供有用的信息。</span><span class="sxs-lookup"><span data-stu-id="81f69-148">It can also give you useful information if there is a dispute.</span></span>

<span data-ttu-id="81f69-149">与可用性相关的度量标准如下所示：</span><span class="sxs-lookup"><span data-stu-id="81f69-149">Measures related to availability are as follows:</span></span>

  - <span data-ttu-id="81f69-150">**可用性**   这通常表示为系统或服务可以被访问的时间与它处于关闭状态的时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-150">**Availability**   This is typically expressed as the time that a system or service can be accessed compared to the time that it is down.</span></span> <span data-ttu-id="81f69-151">它通常表示为百分比。</span><span class="sxs-lookup"><span data-stu-id="81f69-151">It is typically expressed as a percentage.</span></span> <span data-ttu-id="81f69-152"> (你可能会看到对 "三个 9" 或 "五个 9" 的引用。</span><span class="sxs-lookup"><span data-stu-id="81f69-152">(You may see references to “three nines” or “five nines”.</span></span> <span data-ttu-id="81f69-153">这是99.9% 或99.999% 的可用容量。 ) </span><span class="sxs-lookup"><span data-stu-id="81f69-153">These refer to 99.9 percent or 99.999 percent availability.)</span></span>

  - <span data-ttu-id="81f69-154">**可靠性**   这是对系统故障之间的时间的衡量，有时表示为平均 (或 (MTBF) 之间的平均) 时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-154">**Reliability**   This is a measure of the time between failures of a system and is sometimes expressed as mean (or average) time between failures (MTBF).</span></span>

  - <span data-ttu-id="81f69-155">**修复时间**   这是在出现故障后恢复服务所用的时间，通常表示为 (MTTR) 修复的平均) 时间 (表示的平均时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-155">**Time to Repair**   This is the time taken to recover a service after a failure has occurred and is often expressed as mean (meaning average) time to repair (MTTR).</span></span>

<span data-ttu-id="81f69-156">可用性、可靠性和修复时间相关，如下所示：</span><span class="sxs-lookup"><span data-stu-id="81f69-156">Availability, reliability, and time to repair are related as follows:</span></span>

<span data-ttu-id="81f69-157">**可用性 = (MTBF-MTTR) /MTBF**   例如，如果服务器在六个月的时间段内失败两次，并且平均不超过20分钟，则 MTBF 为3个月或90天，并且 MTTR 为20分钟。</span><span class="sxs-lookup"><span data-stu-id="81f69-157">**Availability = (MTBF – MTTR) / MTBF**   For example, if a server fails two times over a six-month period and is unavailable for an average of 20 minutes, the MTBF is three months or 90 days and the MTTR is 20 minutes.</span></span> <span data-ttu-id="81f69-158">因此，可用性 = (90 天-20 分钟) /90 天 = 99.985%。</span><span class="sxs-lookup"><span data-stu-id="81f69-158">Therefore, Availability = (90 days – 20 minutes) / 90 days = 99.985 percent.</span></span>

<span data-ttu-id="81f69-159">可用性管理是确保可用性最大化并保留在 Sla 中定义的参数中的过程。</span><span class="sxs-lookup"><span data-stu-id="81f69-159">Availability management is the process of making sure that availability is maximized and kept within the parameters that are defined in SLAs.</span></span> <span data-ttu-id="81f69-160">可用性管理包括以下过程：</span><span class="sxs-lookup"><span data-stu-id="81f69-160">Availability management includes the following processes:</span></span>

  - <span data-ttu-id="81f69-161">**监控**    检查服务不可用的时间和时间。</span><span class="sxs-lookup"><span data-stu-id="81f69-161">**Monitoring**    Examining when and for how long services are unavailable.</span></span>

  - <span data-ttu-id="81f69-162">**报告**   应定期向管理层、用户和运营团队提供可用性图。</span><span class="sxs-lookup"><span data-stu-id="81f69-162">**Reporting**   Availability figures should be regularly provided to management, users, and operations teams.</span></span> <span data-ttu-id="81f69-163">这些报表应突出显示趋势并确定正在进行良好工作的区域以及需要注意的区域。</span><span class="sxs-lookup"><span data-stu-id="81f69-163">These reports should highlight trends and identify areas that are doing well and areas that require attention.</span></span> <span data-ttu-id="81f69-164">该报告应总结 Sla 中设置的目标合规性。</span><span class="sxs-lookup"><span data-stu-id="81f69-164">The report should summarize compliance with targets set in the SLAs.</span></span>

  - <span data-ttu-id="81f69-165">**改进**   如果可用性不满足在 Sla 中定义的目标或趋势在降低可用性的位置，则可用性管理过程应计划补救步骤。</span><span class="sxs-lookup"><span data-stu-id="81f69-165">**Improvement**   If availability does not meet targets that are defined in the SLAs or where the trend is toward reduced availability, the availability management process should plan remedial steps.</span></span> <span data-ttu-id="81f69-166">这应包括与其他责任团队协作，以突出显示中断的原因并计划补救措施以防止中断的重复。</span><span class="sxs-lookup"><span data-stu-id="81f69-166">This should include working with other responsible teams to highlight reasons for outages and to plan remedial actions to prevent a recurrence of the outages.</span></span>

<span data-ttu-id="81f69-167">容量和可用性度量是重复性任务，非常适合自动工具和脚本，例如 Microsoft System Center Operations Manager (以前的 Microsoft Operations Manager) ，本文档后面部分将进行讨论。</span><span class="sxs-lookup"><span data-stu-id="81f69-167">Capacity and availability measurements are repetitive tasks that are ideally suited to automated tools and scripts such as Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which is discussed later in this document.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="81f69-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="81f69-168">See Also</span></span>


[<span data-ttu-id="81f69-169">通过 System Center Operations Manager 监视 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81f69-169">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)  
  

<span data-ttu-id="81f69-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81f69-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

