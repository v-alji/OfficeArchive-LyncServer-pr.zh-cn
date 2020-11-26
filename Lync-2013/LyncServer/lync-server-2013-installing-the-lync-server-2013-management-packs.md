---
title: Lync Server 2013：安装 Lync Server 2013 管理包
description: Lync Server 2013：安装 Lync Server 2013 管理包。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: nstalling the Lync Server 2013 management packs
ms:assetid: b800d4ab-fdc8-4c72-a76a-b78932779fe3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205202(v=OCS.15)
ms:contentKeyID: 48185233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbb50146474211c12dbd95801ed2b20f6bbfd8c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426926"
---
# <a name="installing-the-lync-server-2013-management-packs"></a><span data-ttu-id="afeb3-103">安装 Lync Server 2013 管理包</span><span class="sxs-lookup"><span data-stu-id="afeb3-103">Installing the Lync Server 2013 management packs</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="afeb3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="afeb3-104">

<span> </span></span></span>

<span data-ttu-id="afeb3-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="afeb3-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="afeb3-106">System Center Operations Manager 本身能够仅监视 Windows 操作系统的一小部分。</span><span class="sxs-lookup"><span data-stu-id="afeb3-106">By itself, System Center Operations Manager has the ability to monitor only a small portion of the Windows operating system.</span></span> <span data-ttu-id="afeb3-107">但是，你可以通过安装管理包来扩展 System Center Operations Manager 的功能，该软件指示 System Center Operations Manager 可以监视哪些项目，包括应如何监视这些项目以及应如何触发和报告警报。</span><span class="sxs-lookup"><span data-stu-id="afeb3-107">However, you can extend the capabilities of System Center Operations Manager by installing management packs, software that dictates which items System Center Operations Manager can monitor, including how those items should be monitored and how alerts should be triggered and reported.</span></span> <span data-ttu-id="afeb3-108">Microsoft Lync Server 2013 包括两个 System Center Operations Manager 管理包，它们提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="afeb3-108">Microsoft Lync Server 2013 includes two System Center Operations Manager management packs that provide the following capabilities:</span></span>

  - <span data-ttu-id="afeb3-109">组件和用户管理包 (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) 跟踪在事件日志中记录的 Lync Server 问题（由性能计数器注册），或记录在 QoE (数据库的 " (CDR) 的" 调用详细信息 "中的" 调用详细信息 "记录中。</span><span class="sxs-lookup"><span data-stu-id="afeb3-109">The Component and User Management Pack (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) tracks Lync Server issues recorded in event logs, registered by performance counters, or logged in the call detail records (CDR) or the Quality of Experience (QoE) databases.</span></span> <span data-ttu-id="afeb3-110">对于严重问题，System Center Operations Manager 可以配置为通过电子邮件、即时消息或短消息服务立即通知管理员 (SMS) 消息。</span><span class="sxs-lookup"><span data-stu-id="afeb3-110">For critical problems, System Center Operations Manager can be configured to immediately notify administrators via email, instant message, or Short Message Service (SMS) messaging.</span></span> <span data-ttu-id="afeb3-111">SMS 是用于将文本消息从一个移动设备发送到另一个移动设备的技术。</span><span class="sxs-lookup"><span data-stu-id="afeb3-111">SMS is the technology used to send text messages from one mobile device to another.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="afeb3-112">有关配置 Operations Manager 通知的详细信息，请参阅在 TechNet 库中配置通知 <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A> 。</span><span class="sxs-lookup"><span data-stu-id="afeb3-112">For more information on configuring Operations Manager notification, see Configuring Notification in the TechNet Library at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A>.</span></span>

    
    </div>

  - <span data-ttu-id="afeb3-113">活动监视包 (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) 主动测试关键 Lync 服务器组件，如登录到系统、交换即时消息或拨打位于公共交换电话网络 (PSTN) 的电话。</span><span class="sxs-lookup"><span data-stu-id="afeb3-113">The Active Monitoring Pack (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) proactively tests key Lync Server components such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="afeb3-114">这些测试通过 Lync Server 合成事务 cmdlet 进行。</span><span class="sxs-lookup"><span data-stu-id="afeb3-114">These tests are conducted using the Lync Server synthetic transaction cmdlets.</span></span> <span data-ttu-id="afeb3-115">例如，**Test-CsIM** cmdlet 用来模拟一对测试用户之间的即时消息对话。</span><span class="sxs-lookup"><span data-stu-id="afeb3-115">For example, the **Test-CsIM** cmdlet is used to simulate an instant messaging conversation between a pair of test users.</span></span> <span data-ttu-id="afeb3-116">如果此模拟消息对话失败，将生成警报。</span><span class="sxs-lookup"><span data-stu-id="afeb3-116">If this simulated messaging conversation fails an alert will be generated.</span></span>

<span data-ttu-id="afeb3-117">Lync Server 2013 中包含的两个管理包包含大量增强了与 Microsoft Lync Server 2010 一起使用的管理包。</span><span class="sxs-lookup"><span data-stu-id="afeb3-117">The two management packs included with Lync Server 2013 include a large number of enhancements over the management packs used with Microsoft Lync Server 2010.</span></span> <span data-ttu-id="afeb3-118">例如，Lync Server 2013 组件管理包不仅限于监视 Lync 服务器本身。</span><span class="sxs-lookup"><span data-stu-id="afeb3-118">For example, the Lync Server 2013 Component Management Pack is not limited to monitoring Lync Server itself.</span></span> <span data-ttu-id="afeb3-119">除了监视 Lync Server 的事件日志和性能计数器，组件管理包还可以跟踪重要项目的性能以及发出警报，如：</span><span class="sxs-lookup"><span data-stu-id="afeb3-119">In addition to monitoring event logs and performance counters for Lync Server, the Component Management pack can also track the performance of, and issue alerts for, crucial items such as:</span></span>

  - <span data-ttu-id="afeb3-120">**(IIS) 的 Internet 信息服务**   如果 Internet 信息服务离线，将发出警报。</span><span class="sxs-lookup"><span data-stu-id="afeb3-120">**Internet Information Services (IIS)**   Alerts will be issued if Internet Information Services goes offline.</span></span> <span data-ttu-id="afeb3-121">这一点很重要，因为 Lync Server web 服务依赖于 IIS。</span><span class="sxs-lookup"><span data-stu-id="afeb3-121">This is important, because the Lync Server web services rely on IIS.</span></span>

  - <span data-ttu-id="afeb3-122">**进程使用情况**   如果系统资源 (（如可用内存) 开始运行不足），将发出警报。</span><span class="sxs-lookup"><span data-stu-id="afeb3-122">**Process usage**   Alerts will be issued if system resources (such as available memory) begin to run low.</span></span> <span data-ttu-id="afeb3-123">即使 Lync 服务器对高系统使用率不负责，也会发出这些警报。</span><span class="sxs-lookup"><span data-stu-id="afeb3-123">These alerts will be issued even if Lync Server is not responsible for the high system usage.</span></span>

  - <span data-ttu-id="afeb3-124">**计算机故障事件**   如果硬件或软件问题会威胁服务器的生存能力，将发出警报。</span><span class="sxs-lookup"><span data-stu-id="afeb3-124">**Computer failure events**   Alerts will be issued in case of a hardware or software issue that threatens the viability of a server.</span></span> <span data-ttu-id="afeb3-125">例如，如果服务器似乎存在遇到硬盘故障的危险，则将通知 Lync 服务器管理员。</span><span class="sxs-lookup"><span data-stu-id="afeb3-125">For example, Lync Server administrators will be notified if a server appears to be in danger of experiencing a hard disk failure.</span></span>

<span data-ttu-id="afeb3-126">新的管理包还具有增强的报告功能。</span><span class="sxs-lookup"><span data-stu-id="afeb3-126">The new management packs also feature enhanced reporting.</span></span> <span data-ttu-id="afeb3-127">Lync Server 2013 的新报告包括：</span><span class="sxs-lookup"><span data-stu-id="afeb3-127">New reports for Lync Server 2013 include:</span></span>

  - <span data-ttu-id="afeb3-128">**端到端方案可用性报表**   此报告详细介绍了关键 Lync 服务器服务（如注册或联机状态）的可用性/正常运行时间。</span><span class="sxs-lookup"><span data-stu-id="afeb3-128">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="afeb3-129">**容量报告**   使用性能计数器信息，此报告显示系统组件（如内存可用性和处理器使用情况）的趋势。</span><span class="sxs-lookup"><span data-stu-id="afeb3-129">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="afeb3-130">**组件报告**   此报告列出按 Lync Server 组件分组的热门警报生成器。</span><span class="sxs-lookup"><span data-stu-id="afeb3-130">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="afeb3-131">除了这些预先设计好的报表，Lync Server 2013 的管理包还会自动报告调用可靠性 (指标（按呼叫详细记录) 和 QoE (状态），使用 ") 质量" 衡量指标。</span><span class="sxs-lookup"><span data-stu-id="afeb3-131">In addition to these predesigned reports, the management packs for Lync Server 2013 automatically report alerts for both Call Reliability (metrics measured by Call Detail Recording) and QoE states (metrics measured by Quality of Experience).</span></span> <span data-ttu-id="afeb3-132">如果已启用 "呼叫详细信息录制"，则可以通过 System Center Operations Manager 控制台完成以下过程来查看呼叫可靠性警报：</span><span class="sxs-lookup"><span data-stu-id="afeb3-132">If you have enabled Call Detail Recording, you can review Call Reliability alerts by completing the following procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="afeb3-133">展开 " **监视**"，展开 " **Microsoft Lync Server 2013 运行状况**"，展开 " **呼叫可靠性和媒体质量**"，然后单击 " **调用可靠性**"。</span><span class="sxs-lookup"><span data-stu-id="afeb3-133">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then click **Call Reliability**.</span></span>

<span data-ttu-id="afeb3-134">若要查看体验警报的质量，请从 System Center Operations Manager 控制台完成此过程：</span><span class="sxs-lookup"><span data-stu-id="afeb3-134">To view Quality of Experience alerts, complete this procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="afeb3-135">展开 " **监视**"，展开 " **Microsoft Lync Server 2013 运行状况**"，展开 " **呼叫可靠性和媒体质量**"，然后展开 " **媒体质量**"。</span><span class="sxs-lookup"><span data-stu-id="afeb3-135">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then expand **Media Quality**.</span></span>

<span data-ttu-id="afeb3-136">Lync Server 2013 的管理包现在使用计算机级发现，而不是在 Microsoft Lync Server 2010 中使用的集中发现机制。</span><span class="sxs-lookup"><span data-stu-id="afeb3-136">The management packs for Lync Server 2013 now use machine-level discovery instead of the central discovery mechanism used in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="afeb3-137">这意味着每个 System Center 代理实质上都会发现自己，并报告它是否存在于中央管理服务器。</span><span class="sxs-lookup"><span data-stu-id="afeb3-137">This means that each System Center agent essentially discovers itself and reports its existence to the Central Management Server.</span></span> <span data-ttu-id="afeb3-138">使用计算机级发现可简化 System Center 基础结构的管理，还允许使用不同版本的 Lync Server 管理包 (例如，lync server 2010 的管理包和 Lync Server 2013 的管理包) 共存。</span><span class="sxs-lookup"><span data-stu-id="afeb3-138">Using machine-level discovery simplifies administration of your System Center infrastructure and also allows different versions of the Lync Server management packs (for example, management packs for Lync Server 2010 and management packs for Lync Server 2013) to coexist.</span></span>

<span data-ttu-id="afeb3-139"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="afeb3-139"></div>

<span> </span>

</div>

</div>

</span></span></div>

