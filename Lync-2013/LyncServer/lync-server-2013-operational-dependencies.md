---
title: Lync Server 2013：操作依赖项
description: Lync Server 2013：操作依赖关系。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operational dependencies
ms:assetid: 450b6be2-7fb3-47d7-8b0b-c05faa331e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720559(v=OCS.15)
ms:contentKeyID: 63969597
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e240981f5dfded7c27f123c8483794ea3ffedff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445293"
---
# <a name="operational-dependencies-in-lync-server-2013"></a><span data-ttu-id="70b74-103">Lync Server 2013 中的操作相关性</span><span class="sxs-lookup"><span data-stu-id="70b74-103">Operational dependencies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70b74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70b74-104">

<span> </span></span></span>

<span data-ttu-id="70b74-105">_**主题上次修改时间：** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="70b74-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="70b74-106">本文档中讨论的参考体系结构将帮助确保你拥有的 Lync Server 2013 部署不仅可扩展到组织的要求，还可根据 Microsoft 最佳做法进行构建。</span><span class="sxs-lookup"><span data-stu-id="70b74-106">The Reference Architecture discussed in this document will help ensure that you have a Lync Server 2013 deployment that not only scales to the organization’s requirements but is architected as per Microsoft best practices.</span></span> <span data-ttu-id="70b74-107">请注意，它可能是 Lync Server 2013 实现是一种动态服务，与企业中的任何其他服务一样，它仍需要监视和主动管理，以便为企业保持高级别的服务可用性和服务质量。</span><span class="sxs-lookup"><span data-stu-id="70b74-107">Be that as it may the Lync Server 2013 implementation is a dynamic service and like any other service in the enterprise still requires monitoring and proactive management to maintain high level of service availability and service quality to the business.</span></span>

<span data-ttu-id="70b74-108">随着 Lync Server 2013 在组织的日常企业中变得更深 ingrained，该服务必须通过准确的有形服务级别管理来管理。</span><span class="sxs-lookup"><span data-stu-id="70b74-108">As Lync Server 2013 becomes deeply ingrained in the organization’s everyday business it is important that the service be managed by accurate and tangible service level management.</span></span> <span data-ttu-id="70b74-109">Lync 系统体系结构可能会变得复杂且非常集成，以便维护有效的服务级别管理并建立 Lync Server 2013 的 Sla，这对了解系统对其他平台和服务器的依赖非常重要。</span><span class="sxs-lookup"><span data-stu-id="70b74-109">The Lync system architecture can become complex and very integrated and in order to maintain effective service level management and establish SLAs for Lync Server 2013 it becomes critical to understand the system’s dependencies on other platforms and servers.</span></span> <span data-ttu-id="70b74-110">同样重要的是要注意哪些商业服务（如语音和 UC 集成应用程序）依赖于 Lync。</span><span class="sxs-lookup"><span data-stu-id="70b74-110">Equally important is to note which business services, such as voice and UC integrated applications, become dependent on Lync.</span></span>

<span data-ttu-id="70b74-111">必须建立 Lync Server 2013，注意所有所说的依赖关系。</span><span class="sxs-lookup"><span data-stu-id="70b74-111">Lync Server 2013 must be established noting all the said dependencies.</span></span> <span data-ttu-id="70b74-112">服务地图将允许你在 Lync 及其依赖的服务之间制定一个 SLA，并提供 SLA 协商的起始位置。</span><span class="sxs-lookup"><span data-stu-id="70b74-112">The service map will allow you to formulate a SLA between Lync and its dependent service and provide a starting place for SLA negotiation.</span></span>

<span data-ttu-id="70b74-113">下表列出了 Lync 基础结构的典型依赖服务。</span><span class="sxs-lookup"><span data-stu-id="70b74-113">The following table lists the typical dependency services for a Lync infrastructure.</span></span> <span data-ttu-id="70b74-114">其中每种技术都应具有其自己的主动预防性监控。</span><span class="sxs-lookup"><span data-stu-id="70b74-114">Each of these technologies should have its own proactive monitoring.</span></span>

### <a name="typical-dependency-services"></a><span data-ttu-id="70b74-115">典型的依赖服务</span><span class="sxs-lookup"><span data-stu-id="70b74-115">Typical dependency services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70b74-116">依赖服务</span><span class="sxs-lookup"><span data-stu-id="70b74-116">Dependency Service</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70b74-117">操作系统</span><span class="sxs-lookup"><span data-stu-id="70b74-117">Operating systems</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-118">服务器硬件</span><span class="sxs-lookup"><span data-stu-id="70b74-118">Server Hardware</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-119">Active Directory</span><span class="sxs-lookup"><span data-stu-id="70b74-119">Active Directory</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-120">公钥基础结构</span><span class="sxs-lookup"><span data-stu-id="70b74-120">Public Key Infrastructure</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-121">域命名服务</span><span class="sxs-lookup"><span data-stu-id="70b74-121">Domain Naming Service</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-122">数据库服务</span><span class="sxs-lookup"><span data-stu-id="70b74-122">Database Services</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-123">存储服务</span><span class="sxs-lookup"><span data-stu-id="70b74-123">Storage Services</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-124">系统管理-监视和分发</span><span class="sxs-lookup"><span data-stu-id="70b74-124">System Management – Monitoring and distribution</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-125">安全服务-防病毒</span><span class="sxs-lookup"><span data-stu-id="70b74-125">Security Services - Antivirus</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-126">网络基础结构-Internet</span><span class="sxs-lookup"><span data-stu-id="70b74-126">Network Infrastructure - Internet</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-127">网络基础结构-内部 (LAN/WAN) </span><span class="sxs-lookup"><span data-stu-id="70b74-127">Network Infrastructure – Internal (LAN/WAN)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-128">电话服务基础结构-IP-PBX 和网关</span><span class="sxs-lookup"><span data-stu-id="70b74-128">Telephony Infrastructure – IP-PBX and Gateways</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-129">云服务</span><span class="sxs-lookup"><span data-stu-id="70b74-129">Cloud Services</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70b74-130">假定组织在使用由 MOF 规定的基本服务级别管理功能（如更改、事件和发布管理）中运行成熟。</span><span class="sxs-lookup"><span data-stu-id="70b74-130">It is assumed that the organization is operationally mature in exercising basic service level management functions such as change, incident and release management as prescribed by the MOF.</span></span> <span data-ttu-id="70b74-131">Lync 解决方案应由这些函数采纳，并遵循相同的操作管理过程。</span><span class="sxs-lookup"><span data-stu-id="70b74-131">The Lync solution should be adopted by these functions and become subject to the same operational management processes.</span></span>

<span data-ttu-id="70b74-132">根据以上获取的信息构建，我们现在更深入地了解对企业中的 Lync 服务有哪些影响。</span><span class="sxs-lookup"><span data-stu-id="70b74-132">Building on the information obtained above we now have a greater understanding of what can impact the Lync service in the enterprise.</span></span> <span data-ttu-id="70b74-133">为了帮助确保 Lync Server 2013 服务可用性和质量，以下监视工具必须附带参考体系结构部署：</span><span class="sxs-lookup"><span data-stu-id="70b74-133">To help ensure Lync Server 2013 service availability and quality, the following monitoring tools must accompany the reference architecture deployment:</span></span>

### <a name="monitoring-tools"></a><span data-ttu-id="70b74-134">监视工具</span><span class="sxs-lookup"><span data-stu-id="70b74-134">Monitoring tools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70b74-135">组件</span><span class="sxs-lookup"><span data-stu-id="70b74-135">Component</span></span></th>
<th><span data-ttu-id="70b74-136">说明</span><span class="sxs-lookup"><span data-stu-id="70b74-136">Description</span></span></th>
<th><span data-ttu-id="70b74-137">适用网站</span><span class="sxs-lookup"><span data-stu-id="70b74-137">Applicable Site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70b74-138">Lync Server 2013 监视服务器</span><span class="sxs-lookup"><span data-stu-id="70b74-138">Lync Server 2013 Monitoring Server</span></span></p></td>
<td><p><span data-ttu-id="70b74-139">每个中心网站至少部署一个 Lync Server 2013 监视服务器角色，并配置 (QoE) 报告包的体验质量。</span><span class="sxs-lookup"><span data-stu-id="70b74-139">Deploy at least one Lync Server 2013 Monitoring Server role per Central site and configure Quality of Experience (QoE) Reporting Pack.</span></span></p>
<p><span data-ttu-id="70b74-140">有关详细信息，请参阅 Lync Server 2013 部署文档：</span><span class="sxs-lookup"><span data-stu-id="70b74-140">Refer to the Lync Server 2013 Deployment documentation for further details:</span></span></p>
<p><span data-ttu-id="70b74-141"><a href="lync-server-2013-deploying-monitoring.md">在 Lync Server 2013 中部署监视</a></span><span class="sxs-lookup"><span data-stu-id="70b74-141"><a href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="70b74-142">中心网站</span><span class="sxs-lookup"><span data-stu-id="70b74-142">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="70b74-143">将每个池 Tether 到最接近的监视服务器角色实例。</span><span class="sxs-lookup"><span data-stu-id="70b74-143">Tether each pool to its nearest instance of the Monitoring Server role.</span></span></p></td>
<td><p><span data-ttu-id="70b74-144">中心网站</span><span class="sxs-lookup"><span data-stu-id="70b74-144">Central sites</span></span></p>
<p><span data-ttu-id="70b74-145">分支站点</span><span class="sxs-lookup"><span data-stu-id="70b74-145">Branch sites</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-146">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="70b74-146">System Center Operations Manager 2012</span></span></p></td>
<td><p><span data-ttu-id="70b74-147">System Center Operations Manager 2012 与 Microsoft Lync Server 2013 管理包 (MP) 导入。</span><span class="sxs-lookup"><span data-stu-id="70b74-147">System Center Operations Manager 2012 with the Microsoft Lync Server 2013 Management Pack (MP) imported.</span></span></p>
<p><span data-ttu-id="70b74-148">管理包实现传统事件日志和基于性能计数器的检测使用，并在 Lync Server 2013 中启用新可用的检测。</span><span class="sxs-lookup"><span data-stu-id="70b74-148">The Management Pack implements traditional Event Log and Performance counter based instrumentation is utilized as well as enabling newly available instrumentation in Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="70b74-149">中心网站</span><span class="sxs-lookup"><span data-stu-id="70b74-149">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="70b74-150">确保基于用于读取管理中心数据库中发布的拓扑文档的中心发现脚本，自动完成发现需要监视的角色和组件的集中发现。</span><span class="sxs-lookup"><span data-stu-id="70b74-150">Make sure that Central Discovery to discovery of roles and components that need to be monitored are automatically completed based on a central discovery script that reads the topology document published in Central Management Database.</span></span></p></td>
<td><p><span data-ttu-id="70b74-151">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-151">Central Site</span></span></p>
<p><span data-ttu-id="70b74-152">分支站点</span><span class="sxs-lookup"><span data-stu-id="70b74-152">Branch Site</span></span></p>
<p><span data-ttu-id="70b74-153">边缘网站</span><span class="sxs-lookup"><span data-stu-id="70b74-153">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="70b74-154">将 System 中心 Operations Manager 2007 代理部署到运行 Lync Server 的所有已部署服务器。</span><span class="sxs-lookup"><span data-stu-id="70b74-154">Deploy System Centre Operations Manager 2007 agents to all deployed servers running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="70b74-155">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-155">Central Site</span></span></p>
<p><span data-ttu-id="70b74-156">分支站点</span><span class="sxs-lookup"><span data-stu-id="70b74-156">Branch Site</span></span></p>
<p><span data-ttu-id="70b74-157">边缘网站</span><span class="sxs-lookup"><span data-stu-id="70b74-157">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="70b74-158">请确保为通知配置了优先警报：</span><span class="sxs-lookup"><span data-stu-id="70b74-158">Make sure Prioritized Alerts are configured for notification:</span></span></p>
<p><span data-ttu-id="70b74-159">高优先级警报</span><span class="sxs-lookup"><span data-stu-id="70b74-159">High Priority Alerts</span></span></p>
<p><span data-ttu-id="70b74-160">中等优先级的警报</span><span class="sxs-lookup"><span data-stu-id="70b74-160">Medium Priority Alerts</span></span></p>
<p><span data-ttu-id="70b74-161">其他通知。</span><span class="sxs-lookup"><span data-stu-id="70b74-161">Other Alerts.</span></span></p></td>
<td><p><span data-ttu-id="70b74-162">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-162">Central Site</span></span></p>
<p><span data-ttu-id="70b74-163">分支站点</span><span class="sxs-lookup"><span data-stu-id="70b74-163">Branch Site</span></span></p>
<p><span data-ttu-id="70b74-164">边缘网站</span><span class="sxs-lookup"><span data-stu-id="70b74-164">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="70b74-165">为你的部署配置端口监视。</span><span class="sxs-lookup"><span data-stu-id="70b74-165">Configure Port monitoring for your deployment.</span></span></p></td>
<td><p><span data-ttu-id="70b74-166">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-166">Central Site</span></span></p>
<p><span data-ttu-id="70b74-167">分支站点</span><span class="sxs-lookup"><span data-stu-id="70b74-167">Branch Site</span></span></p>
<p><span data-ttu-id="70b74-168">边缘网站</span><span class="sxs-lookup"><span data-stu-id="70b74-168">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="70b74-169">为你的部署配置 URL 监视</span><span class="sxs-lookup"><span data-stu-id="70b74-169">Configure URL monitoring for your deployment</span></span></p></td>
<td><p><span data-ttu-id="70b74-170">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-170">Central Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-171">Lync 和 System Center Operations Manager 集成</span><span class="sxs-lookup"><span data-stu-id="70b74-171">Lync and System Center Operations Manager integration</span></span></p></td>
<td><p><span data-ttu-id="70b74-172">部署通话可靠性和媒体质量 MonitoringCall 可靠性和媒体质量监视将监视服务器计算机用作其观察程序节点，以监视 Lync 服务器的调用可靠性和媒体质量。</span><span class="sxs-lookup"><span data-stu-id="70b74-172">Deploy Call Reliability and Media Quality MonitoringCall reliability and media quality monitoring use the Monitoring Server computer as their watcher node to monitor call reliability and media quality of Lync Server.</span></span> <span data-ttu-id="70b74-173">这两个功能都可查询监视服务器数据库以进行分析。</span><span class="sxs-lookup"><span data-stu-id="70b74-173">Both of these features query the Monitoring Server databases to do analysis.</span></span></p></td>
<td><p><span data-ttu-id="70b74-174">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-174">Central Site</span></span></p>
<p><span data-ttu-id="70b74-175">分支站点</span><span class="sxs-lookup"><span data-stu-id="70b74-175">Branch Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="70b74-176">确保准确配置媒体质量警告阈值。</span><span class="sxs-lookup"><span data-stu-id="70b74-176">Ensure Media Quality warning thresholds are accurately configured.</span></span> <span data-ttu-id="70b74-177">下表显示了编解码器的最大网络平均观点。</span><span class="sxs-lookup"><span data-stu-id="70b74-177">The following table indicates the maximum Network Mean Opinion Scores by Codec.</span></span> <span data-ttu-id="70b74-178">在生产中，这些分数应针对设定的时间段进行监视，并且必须根据组织特定的 NMOS 分数来建立可接受的阈值。</span><span class="sxs-lookup"><span data-stu-id="70b74-178">In production these scores should be monitored for a set period and acceptable thresholds must be established based on the organization specific NMOS scores.</span></span></p></td>
<td><p><span data-ttu-id="70b74-179">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-179">Central Site</span></span></p>
<p><span data-ttu-id="70b74-180">分支站点</span><span class="sxs-lookup"><span data-stu-id="70b74-180">Branch Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-181">Lync Server 2013 合成事务观察程序</span><span class="sxs-lookup"><span data-stu-id="70b74-181">Lync Server 2013 Synthetic Transaction Watcher</span></span></p></td>
<td><p><span data-ttu-id="70b74-182">将专用 Lync 服务器部署为合成事务观察程序。</span><span class="sxs-lookup"><span data-stu-id="70b74-182">Deploy a dedicated Lync Server to be a synthetic transaction watcher.</span></span></p>
<p><span data-ttu-id="70b74-183">合成事务是 Lync Server 2013 Windows PowerShell cmdlet，这些 cmdlet 由管理包在预定义的时间间隔内自动触发。</span><span class="sxs-lookup"><span data-stu-id="70b74-183">Synthetic transactions are Lync Server 2013 Windows PowerShell cmdlets that are automatically triggered by the management pack on a predefined interval.</span></span> <span data-ttu-id="70b74-184">这些操作在综合事务观察程序节点上执行，该节点是管理员指定的服务器，负责为每个池发现和执行 STs。</span><span class="sxs-lookup"><span data-stu-id="70b74-184">These are executed on a synthetic transaction watcher node which is an administrator designated server responsible for discovery and execution of STs for each pool.</span></span></p>
<p><span data-ttu-id="70b74-185">我们不建议使用现有的 Microsoft Lync Server 2013 服务器作为合成事务观察程序节点。</span><span class="sxs-lookup"><span data-stu-id="70b74-185">We do not recommend that you use an existing Microsoft Lync Server 2013 server as a synthetic transaction watcher node.</span></span> <span data-ttu-id="70b74-186">这是由于运行 STs 的 CPU/内存使用要求较高。</span><span class="sxs-lookup"><span data-stu-id="70b74-186">This is due to the high CPU/memory usage requirements for running STs.</span></span> <span data-ttu-id="70b74-187">为 "合成事务观察程序" 节点使用新的服务器计算机 (或虚拟服务器) 。</span><span class="sxs-lookup"><span data-stu-id="70b74-187">Use a new server computer (or a virtual server) for the synthetic transaction watcher node.</span></span></p></td>
<td><p><span data-ttu-id="70b74-188">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-188">Central Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="70b74-189">部署合成事务观察程序节点。</span><span class="sxs-lookup"><span data-stu-id="70b74-189">Deploying synthetic transactions watcher node.</span></span></p>
<p><span data-ttu-id="70b74-190">请参阅 UCTAP connect 文档中的 MonitoringCS_withSCOM.docx 文档。</span><span class="sxs-lookup"><span data-stu-id="70b74-190">Refer to the MonitoringCS_withSCOM.docx document from UCTAP connect documentation.</span></span></p></td>
<td><p><span data-ttu-id="70b74-191">中央站点</span><span class="sxs-lookup"><span data-stu-id="70b74-191">Central Site</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="maximum-network-mos-scores-per-codec"></a><span data-ttu-id="70b74-192">每个编解码器的最大网络 MOS 分数</span><span class="sxs-lookup"><span data-stu-id="70b74-192">Maximum Network MOS scores per codec</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70b74-193">使用场景</span><span class="sxs-lookup"><span data-stu-id="70b74-193">Scenario</span></span></th>
<th><span data-ttu-id="70b74-194">编解码器</span><span class="sxs-lookup"><span data-stu-id="70b74-194">Codec</span></span></th>
<th><span data-ttu-id="70b74-195">最大 NMOS</span><span class="sxs-lookup"><span data-stu-id="70b74-195">Max NMOS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70b74-196">UC-UC 呼叫</span><span class="sxs-lookup"><span data-stu-id="70b74-196">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="70b74-197">RTAudio WB</span><span class="sxs-lookup"><span data-stu-id="70b74-197">RTAudio WB</span></span></p></td>
<td><p><span data-ttu-id="70b74-198">4.10</span><span class="sxs-lookup"><span data-stu-id="70b74-198">4.10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-199">UC-UC 呼叫</span><span class="sxs-lookup"><span data-stu-id="70b74-199">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="70b74-200">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="70b74-200">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="70b74-201">2.95</span><span class="sxs-lookup"><span data-stu-id="70b74-201">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-202">电话会议</span><span class="sxs-lookup"><span data-stu-id="70b74-202">Conference call</span></span></p></td>
<td><p><span data-ttu-id="70b74-203">Siren</span><span class="sxs-lookup"><span data-stu-id="70b74-203">Siren</span></span></p></td>
<td><p><span data-ttu-id="70b74-204">3.72</span><span class="sxs-lookup"><span data-stu-id="70b74-204">3.72</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70b74-205">UC-PSTN 呼叫</span><span class="sxs-lookup"><span data-stu-id="70b74-205">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="70b74-206">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="70b74-206">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="70b74-207">2.95</span><span class="sxs-lookup"><span data-stu-id="70b74-207">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70b74-208">UC-PSTN 呼叫</span><span class="sxs-lookup"><span data-stu-id="70b74-208">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="70b74-209">G-711</span><span class="sxs-lookup"><span data-stu-id="70b74-209">G-711</span></span></p></td>
<td><p><span data-ttu-id="70b74-210">3.61</span><span class="sxs-lookup"><span data-stu-id="70b74-210">3.61</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70b74-211">在以前的 pro 活动监视活动之前和之后，应根据 Lync RA 操作指南中定义的每天、每周和每月定期执行维护任务。</span><span class="sxs-lookup"><span data-stu-id="70b74-211">Over and above the previous pro-active monitoring activities, maintenance tasks should be executed for Central, Edge and Branch sites on a recurring daily, weekly and monthly basis as defined in the Lync RA Operations Guide.</span></span>

<span data-ttu-id="70b74-212"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70b74-212"></div>

<span> </span>

</div>

</div>

</span></span></div>

