---
title: Lync Server 2013：监视 Lync 服务器性能
description: Lync Server 2013：监视 Lync 服务器性能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Lync Server 2013 performance
ms:assetid: 2acfd720-6120-4816-a2d4-30476bd5cd0e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720910(v=OCS.15)
ms:contentKeyID: 63969592
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: efe63a881c9db105fc36a1ccd0b0fdc15086a36f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445615"
---
# <a name="monitoring-lync-server-2013-performance"></a><span data-ttu-id="da610-103">监视 Lync Server 2013 性能</span><span class="sxs-lookup"><span data-stu-id="da610-103">Monitoring Lync Server 2013 performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da610-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da610-104">

<span> </span></span></span>

<span data-ttu-id="da610-105">_**主题上次修改时间：** 2014-05-15_</span><span class="sxs-lookup"><span data-stu-id="da610-105">_**Topic Last Modified:** 2014-05-15_</span></span>

<span data-ttu-id="da610-106">Lync Server 2013 的性能受各种因素（如用户配置文件、系统体系结构、软件、硬件组件、第三方集成点，如网关和电话设备、网络连接和性能、Windows Active Directory 服务配置和性能）的影响，以及 Windows 操作系统功能。</span><span class="sxs-lookup"><span data-stu-id="da610-106">Lync Server 2013 performance is affected by various factors such as user profiles, system architecture, software, hardware components, third-party integration points such as gateways and telephony equipment, network connectivity and performance, Windows Active Directory service configuration and performance in addition to the Windows operating system functionality.</span></span>

<span data-ttu-id="da610-107">在 Lync Server 2013 部署的核心中，"性能" 是指实施它的服务器软件和硬件。</span><span class="sxs-lookup"><span data-stu-id="da610-107">At the core of a Lync Server 2013 deployments’ performance is the server software and hardware it is implemented on.</span></span> <span data-ttu-id="da610-108">例如，前端服务器必须有足够的硬件资源来处理预期的 (短期) 用户负载。</span><span class="sxs-lookup"><span data-stu-id="da610-108">As an example, a front-end server must have sufficient hardware resources to cope with the expected (short-term) user load.</span></span> <span data-ttu-id="da610-109">如果需要使用各自的前端服务器向10000用户提供服务，则配置良好的服务器必须满足预期的负载要求，才能最终帮助确保最佳的最终用户体验。</span><span class="sxs-lookup"><span data-stu-id="da610-109">If a respective front-end server is required to provide services to 10 thousand users, then an adequately configured server must meet the expected load requirements to ultimately help ensure the best possible end-user experience.</span></span>

<span data-ttu-id="da610-110">因此，监视服务器性能非常重要，可衡量已实现的服务器基础结构是否具有适用于日常峰值负载要求的硬件资源。</span><span class="sxs-lookup"><span data-stu-id="da610-110">Monitoring server performance is therefore extremely important to gauge whether the implemented server infrastructure have suitable hardware resources for the day-to-day peak-load requirements.</span></span> <span data-ttu-id="da610-111">监视服务器性能有助于标识系统瓶颈，从而允许管理员在最终用户体验受到影响之前应用纠正操作。</span><span class="sxs-lookup"><span data-stu-id="da610-111">Monitoring server performance helps identify system bottlenecks allowing administrators to apply corrective action before the end-user experience is affected.</span></span> <span data-ttu-id="da610-112">应使用性能数据进行长期容量规划。</span><span class="sxs-lookup"><span data-stu-id="da610-112">The performance data should be used for long-term capacity planning.</span></span>

<span data-ttu-id="da610-113">尽管要观察的所有性能对象和计数器的详细信息均链接到 [使用 System Center Operations Manager 监视 Lync Server 2013](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)中，但你应该关注的一些性能计数器可以为管理员提供系统性能的快速视图：</span><span class="sxs-lookup"><span data-stu-id="da610-113">While detailed information on all performance objects and counters to be observed is linked to in [Monitoring Lync Server 2013 with System Center Operations Manager](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md), some performance counters that you should follow can provide administrators a quick view of the system performance:</span></span>

  - <span data-ttu-id="da610-114">为了跟踪前端服务器的整体系统运行状况，良好的起始点是检查处理器 \\ 的处理器时间。</span><span class="sxs-lookup"><span data-stu-id="da610-114">To track overall system health of the front-end server, a good starting point is to check Processor\\% Processor Time.</span></span> <span data-ttu-id="da610-115">该值应始终小于80%。</span><span class="sxs-lookup"><span data-stu-id="da610-115">The value should always be below 80 percent.</span></span>

  - <span data-ttu-id="da610-116">若要跟踪前端池使用的后端 SQL Server 数据库软件实例的性能，请监视以下性能计数器：</span><span class="sxs-lookup"><span data-stu-id="da610-116">To track the performance of the back end SQL Server database software instance used by the Front End pool, monitor the following performance counters:</span></span>
    
    <span data-ttu-id="da610-117">LC： USrv-DBStore \\ USrv – 002- (毫秒的队列延迟) </span><span class="sxs-lookup"><span data-stu-id="da610-117">LC:USrv – 00 – DBStore\\Usrv – 002 – Queue Latency (msec)</span></span>
    
    <span data-ttu-id="da610-118">LC： USrv-0 04 – DBStore \\ USrv-–过程延迟 (毫秒) </span><span class="sxs-lookup"><span data-stu-id="da610-118">LC:USrv – 00 – DBStore\\Usrv – 0 04– Sproc Latency (msec)</span></span>
    
    <span data-ttu-id="da610-119">处于稳定状态的正常服务器应显示 \< 100 ms 滞后时间值。</span><span class="sxs-lookup"><span data-stu-id="da610-119">The healthy server at steady state should show \<100 ms latency values.</span></span> <span data-ttu-id="da610-120">当延迟达到12秒时，节流机制将会起到这种情况，这意味着前端服务器会将请求限制到后端。</span><span class="sxs-lookup"><span data-stu-id="da610-120">The throttling mechanism will engage when latency reaches 12 seconds, which means the front-end server starts throttling requests to the back end.</span></span> <span data-ttu-id="da610-121">这使客户端能够接收503服务器太忙的错误消息。</span><span class="sxs-lookup"><span data-stu-id="da610-121">This causes clients to start to receive a 503 Server too busy error message.</span></span>

  - <span data-ttu-id="da610-122">若要跟踪前端服务器的处理时间，请监视以下计数器：</span><span class="sxs-lookup"><span data-stu-id="da610-122">To track the processing time at the front-end server, monitor the following counter:</span></span>
    
    <span data-ttu-id="da610-123">LC： SIP-2007-加载管理 \\ SIP-000-接收邮件的平均保留时间</span><span class="sxs-lookup"><span data-stu-id="da610-123">LC:SIP - 07 - Load Management\\SIP - 000 - Average Holding Time For Incoming Messages</span></span>
    
    <span data-ttu-id="da610-124">这是前端服务器上的另一限制机制，这次在前端处理时间较高时开始。</span><span class="sxs-lookup"><span data-stu-id="da610-124">This is another throttling mechanism on the front-end servers, this time starting when the processing time on the front end is high.</span></span> <span data-ttu-id="da610-125">如果平均处理时间超过6秒，则服务器将进入阻止模式，并仅允许每个客户端连接一个未完成的事务。</span><span class="sxs-lookup"><span data-stu-id="da610-125">If average processing time is more than six seconds, the server goes into throttling mode and only allows one outstanding transaction per client connection.</span></span>

  - <span data-ttu-id="da610-126">若要在 SQL 后端服务器上跟踪内存问题，请监视以下计数器：</span><span class="sxs-lookup"><span data-stu-id="da610-126">To track memory issues at SQL Back End Server, monitor the following counter:</span></span>
    
    <span data-ttu-id="da610-127">SQL Server 缓冲区管理器 \\ 页生命预期</span><span class="sxs-lookup"><span data-stu-id="da610-127">SQL Server Buffer Manager\\Page life expectancy</span></span>
    
    <span data-ttu-id="da610-128">较低值，低于3600秒 (，每秒最高延迟写入/秒和检查点页) 表示内存压力。</span><span class="sxs-lookup"><span data-stu-id="da610-128">A low value, below 3600 seconds (together with high latency writes/sec and checkpoint pages/sec) indicates memory pressure.</span></span>

<div>

## <a name="additional-counters-to-view"></a><span data-ttu-id="da610-129">要查看的其他计数器</span><span class="sxs-lookup"><span data-stu-id="da610-129">Additional Counters to View</span></span>

<span data-ttu-id="da610-130">有多个关键计数器是前端服务器的整体运行状况的很好指示器。</span><span class="sxs-lookup"><span data-stu-id="da610-130">There are several key counters that are good indicators of overall health from the front end server.</span></span> <span data-ttu-id="da610-131">这不是一个完整的列表，也不是为了找出根本原因。</span><span class="sxs-lookup"><span data-stu-id="da610-131">This is not a comprehensive list and is not meant to identify root cause.</span></span> <span data-ttu-id="da610-132">这些计数器将允许你对服务器运行状况执行快速检查。</span><span class="sxs-lookup"><span data-stu-id="da610-132">These counters will let you perform a quick check on your server health.</span></span> <span data-ttu-id="da610-133">我们建议在池中的每台服务器上验证这些计数器。</span><span class="sxs-lookup"><span data-stu-id="da610-133">We recommend verifying these counters on each of the servers in the pool.</span></span> <span data-ttu-id="da610-134">当服务器运行正常时，了解这些计数器值的含义非常重要。</span><span class="sxs-lookup"><span data-stu-id="da610-134">It is important to understand what these counter values are when your server is healthy.</span></span> <span data-ttu-id="da610-135">需要使用基准来了解在用户体验下降时所发生的更改。</span><span class="sxs-lookup"><span data-stu-id="da610-135">A baseline is required to understand what changed when the user experience is degraded.</span></span>

<span data-ttu-id="da610-136">前端服务器可以指示可能由系统中其他地方的瓶颈导致的问题。</span><span class="sxs-lookup"><span data-stu-id="da610-136">The front-end server can indicate issues that may be caused by bottlenecks elsewhere in the system.</span></span> <span data-ttu-id="da610-137">这意味着它是查看整个系统运行状况的最佳起点。</span><span class="sxs-lookup"><span data-stu-id="da610-137">This means that it is the best place to start when looking at overall system health.</span></span>

<span data-ttu-id="da610-138">要首先查看的两个其他计数器如下所示：</span><span class="sxs-lookup"><span data-stu-id="da610-138">Two additional counters to review first are as follows:</span></span>

<span data-ttu-id="da610-139">LC： USrv-DBStore USrv- \\ (毫秒的队列延迟) </span><span class="sxs-lookup"><span data-stu-id="da610-139">LC:USrv-00-DBStore\\Usrv-002-Queue Latency (msec)</span></span>

<span data-ttu-id="da610-140">LC： USrv-DBStore \\ USrv-004-过程延迟 (毫秒) </span><span class="sxs-lookup"><span data-stu-id="da610-140">LC:USrv-00-DBStore\\Usrv-004-Sproc Latency (msec)</span></span>

<span data-ttu-id="da610-141">Queue 延迟计数器表示请求在队列中的后端的时间，而 "处理程序延迟" 表示用于处理请求的后端所花费的时间。</span><span class="sxs-lookup"><span data-stu-id="da610-141">The queue latency counter represents the time that a request spent in the queue to the back end and the Sproc latency represents the time that it took for the back end to process the request.</span></span> <span data-ttu-id="da610-142">如果由于任何原因而后端的磁盘、内存、网络和处理器出现问题，则队列延迟计数器将很高。</span><span class="sxs-lookup"><span data-stu-id="da610-142">If, for any reason, disk, memory, network, and processor on the back end are in trouble, the queue latency counter will be high.</span></span>

<span data-ttu-id="da610-143">如果前端和后端之间存在较高的网络延迟，它也会很高。</span><span class="sxs-lookup"><span data-stu-id="da610-143">It can also be high if there is high network latency between the front end and the back end.</span></span> <span data-ttu-id="da610-144">那么，哪些队列延迟是可接受的？</span><span class="sxs-lookup"><span data-stu-id="da610-144">So what is acceptable queue latency?</span></span>

<span data-ttu-id="da610-145">在12秒后，前端服务器将对后端服务器启动限制请求。</span><span class="sxs-lookup"><span data-stu-id="da610-145">At 12 seconds, the Front End Servers start throttling requests to the Back End Servers.</span></span> <span data-ttu-id="da610-146">这意味着服务器开始返回的服务器太忙-503 错误会出现在客户端。</span><span class="sxs-lookup"><span data-stu-id="da610-146">This means the servers start returning Server too busy – 503 errors to the clients.</span></span> <span data-ttu-id="da610-147">正常状态的服务器在稳定状态下应具有小于100毫秒的 DBStore 队列等待时间，但在服务器刚刚联机且用户同时登录的时间段内，该计数器可能会非常高，甚至你可能会看到它遇到了多长时间。</span><span class="sxs-lookup"><span data-stu-id="da610-147">A healthy server should have less than 100 msec DBStore queue latencies at steady state, but during times where the server has just come online and users are all logging in at the same time, that counter can be very high and you may even see it hit multiple seconds.</span></span>

<span data-ttu-id="da610-148">你可能具有负载平衡的配置，其中包含使用多个前端服务器部署的池和配置为 "最少连接数" 的负载平衡器。</span><span class="sxs-lookup"><span data-stu-id="da610-148">You may have a load-balanced configuration, where you have a pool deployed with multiple front-end servers and a load balancer that is configured for "least number of connections."</span></span> <span data-ttu-id="da610-149">在这种情况下，如果重新启动了一个前端服务器，则尝试重新连接的所有用户都将指向重新启动的服务器，因为该服务器与其他池成员相比的连接较少。</span><span class="sxs-lookup"><span data-stu-id="da610-149">In this case, if one front-end server is restarted, then all users who attempt to reconnect will be pointed to the restarted server, because that server will have fewer connections compared to the other pool members.</span></span> <span data-ttu-id="da610-150">在这段时间内，可能会重载相应的前端服务器，而其他池成员则不会。</span><span class="sxs-lookup"><span data-stu-id="da610-150">During this time, the respective front-end server may be overloaded while the other pool members are not.</span></span>

<span data-ttu-id="da610-151">我们建议你在非工作时间内执行维护以减少性能影响，因为用户不会同时与服务器同时连接。</span><span class="sxs-lookup"><span data-stu-id="da610-151">We recommend that you perform maintenance during off-hours to reduce the performance affect as users will not all be competing to connect to the server at the same time.</span></span>

<span data-ttu-id="da610-152">如果前两个性能计数器较高，则最可能的瓶颈是 SQL 后端服务器。</span><span class="sxs-lookup"><span data-stu-id="da610-152">If the previous two performance counters are high, the most likely bottleneck is the SQL Back End Server.</span></span> <span data-ttu-id="da610-153">要确认的下一个组件如下所示：</span><span class="sxs-lookup"><span data-stu-id="da610-153">The next components to confirm are as follows:</span></span>

  - <span data-ttu-id="da610-154">SQL Server CPU 是否太高？</span><span class="sxs-lookup"><span data-stu-id="da610-154">Is the SQL Server CPU too high?</span></span> <span data-ttu-id="da610-155">例如，它是否大于80%？</span><span class="sxs-lookup"><span data-stu-id="da610-155">For example, is it greater than 80 percent?</span></span>

  - <span data-ttu-id="da610-156">磁盘延迟是否高？</span><span class="sxs-lookup"><span data-stu-id="da610-156">Is the disk latency high?</span></span>

<span data-ttu-id="da610-157">在理想的世界中，你有足够的 RAM 在内存中同时具有 RTC 和 RTCDYN 数据库。</span><span class="sxs-lookup"><span data-stu-id="da610-157">In an ideal world, you have enough RAM to have both the RTC and RTCDYN databases in memory.</span></span> <span data-ttu-id="da610-158">然后，服务器访问该磁盘的唯一原因是写入日志文件并刷新数据库。</span><span class="sxs-lookup"><span data-stu-id="da610-158">Then, the only reason the server would be accessing the disk, is to write to the log files and flush to the databases.</span></span> <span data-ttu-id="da610-159">测试显示，12 GB RAM 足以满足100000用户部署的需要。</span><span class="sxs-lookup"><span data-stu-id="da610-159">Tests have shown that 12 GB of RAM is sufficient for 100 thousand user deployments.</span></span> <span data-ttu-id="da610-160">这假设 RTC 和 RTCDYN 数据库的大小不超过 12 GB。</span><span class="sxs-lookup"><span data-stu-id="da610-160">This assumes that the RTC and RTCDYN databases size totals less than 12 GB.</span></span> <span data-ttu-id="da610-161">如果你的数据库大于该数据库，则你可能需要额外的内存。</span><span class="sxs-lookup"><span data-stu-id="da610-161">If your databases are larger than that, then you may need additional memory.</span></span>

<span data-ttu-id="da610-162">你可以通过查看 SQL Server 缓冲区管理器页面寿命性能计数器确定你的 SQL Server 是否需要其他 RAM。</span><span class="sxs-lookup"><span data-stu-id="da610-162">You can determine whether your SQL Server requires additional RAM by reviewing the SQL Server Buffer Manager page life expectancy performance counter.</span></span> <span data-ttu-id="da610-163">小于3600的值表示内存压力。</span><span class="sxs-lookup"><span data-stu-id="da610-163">A value less than 3,600 indicates memory pressure.</span></span> <span data-ttu-id="da610-164">如果您有足够的内存，您还可以在数据库驱动器上看不到任何读取，因为 SQL Server 只能写入数据库。</span><span class="sxs-lookup"><span data-stu-id="da610-164">You should also see little to no reads on your database drive if you have sufficient memory because SQL Server should only be writing to the database.</span></span>

<span data-ttu-id="da610-165">如果服务器处理时间较高，则在 Lync Server 2013 前端服务器中有一种额外的限制机制。</span><span class="sxs-lookup"><span data-stu-id="da610-165">There is an additional throttling mechanism in a Lync Server 2013 Front End Server that starts if the server processing time is high.</span></span> <span data-ttu-id="da610-166">仅当 SQL Server 的延迟较高时，DBStore 延迟限制才会启用。</span><span class="sxs-lookup"><span data-stu-id="da610-166">The DBStore latency throttling is only enabled if the latency to the SQL Server is high.</span></span> <span data-ttu-id="da610-167">启用此限制的一个示例是在前端服务器受 CPU 限制的情况中。</span><span class="sxs-lookup"><span data-stu-id="da610-167">One example in which such throttling is enabled is if the front-end server is CPU-bound.</span></span>

<span data-ttu-id="da610-168">如果 (LC 的平均处理时间：) 在服务器上的 **\\ 接收邮件的平均保留时间** 超过6秒，则服务器将进入阻止模式，并仅为用户提供每个客户端连接的一个未完成的事务。</span><span class="sxs-lookup"><span data-stu-id="da610-168">If the average processing time **(LC:SIP-07-Load Management\\SIP-000-Average Holding Time For Incoming Messages)** on the server exceeds six seconds, then the server goes into throttling mode and only gives users one outstanding transaction per client connection.</span></span> <span data-ttu-id="da610-169">当处理时间降到3秒后，服务器将断开阻止模式，并为用户提供每个客户端连接20个未完成的事务。</span><span class="sxs-lookup"><span data-stu-id="da610-169">Once the processing time drops to three seconds, then the server drops out of throttling mode and gives users up to 20 outstanding transactions per client connection.</span></span> <span data-ttu-id="da610-170">只要特定连接的事务数超过上述阈值，连接将被标记为 "流控制"。</span><span class="sxs-lookup"><span data-stu-id="da610-170">Whenever the number of transactions on a specific connection exceeds the threshold above, the connection is marked as flow controlled.</span></span> <span data-ttu-id="da610-171">结果是服务器不会在其上发布任何接收，并且 **LC： SIP 对等 \\ 流控制的连接** 计数器将递增。</span><span class="sxs-lookup"><span data-stu-id="da610-171">The result is the server does not post any receives on it, and the **LC:SIP-01-Peers\\Flow Controlled Connections** counter is incremented.</span></span> <span data-ttu-id="da610-172">如果连接处于流控制状态的时间超过一分钟，则服务器将其关闭。</span><span class="sxs-lookup"><span data-stu-id="da610-172">If a connection stays in a flow-controlled state for more than one minute, then the server closes it.</span></span> <span data-ttu-id="da610-173">这样做会发生延迟。</span><span class="sxs-lookup"><span data-stu-id="da610-173">It does so lazily.</span></span> <span data-ttu-id="da610-174">当它有机会检查连接时，它会确定它是否被限制太长，如果超过一分钟，则将其关闭。</span><span class="sxs-lookup"><span data-stu-id="da610-174">When it has an opportunity to check the connection, it determines whether it was throttled for too long and closes it if it has more than one minute.</span></span>

<span data-ttu-id="da610-175">这些是两种限制机制，并且有一个性能计数器，用于汇总服务器执行的限制（如果有）。</span><span class="sxs-lookup"><span data-stu-id="da610-175">These are the two throttling mechanisms and there is one performance counter that summarizes what, if any, throttling the server is performing.</span></span>

<span data-ttu-id="da610-176">**LC： SIP-04-响应 \\ SIP-053-本地503响应/秒**</span><span class="sxs-lookup"><span data-stu-id="da610-176">**LC:SIP-04-Responses\\SIP-053-Local 503 Responses/sec**</span></span>

  - <span data-ttu-id="da610-177">以前计数器中的术语 "本地" 指本地生成的响应。</span><span class="sxs-lookup"><span data-stu-id="da610-177">The term "Local" in the previous counter refers to locally generated responses.</span></span>

  - <span data-ttu-id="da610-178">503代码对应于服务器不可用，您在正常服务器上不应看到任何503代码。</span><span class="sxs-lookup"><span data-stu-id="da610-178">The 503 code corresponds to server unavailable—where you should not see any 503 codes on a healthy server.</span></span> <span data-ttu-id="da610-179">在服务器刚联机的期间，您可能会看到一些503代码。</span><span class="sxs-lookup"><span data-stu-id="da610-179">During the period after a server is just brought online, you may see some 503 codes.</span></span> <span data-ttu-id="da610-180">当所有用户重新登录，并且服务器返回到稳定状态时，不应该有其他503代码。</span><span class="sxs-lookup"><span data-stu-id="da610-180">When all of the users sign back in and the server returns to a stable state, there should no additional 503 codes.</span></span>

<span data-ttu-id="da610-181">**LC： SIP-04-响应 \\ SIP-074-本地504响应/秒**</span><span class="sxs-lookup"><span data-stu-id="da610-181">**LC:SIP-04-Responses\\SIP-074-Local 504 Responses/sec**</span></span>

<span data-ttu-id="da610-182">此性能计数器指示其他服务器的连接问题，并且它可以指示连接失败或连接延迟。</span><span class="sxs-lookup"><span data-stu-id="da610-182">This performance counter indicates connectivity issues with other servers and it can indicate failures to connect or delays in connecting.</span></span> <span data-ttu-id="da610-183">如果看到504错误，则应选中以下性能计数器。</span><span class="sxs-lookup"><span data-stu-id="da610-183">If you are seeing 504 errors then the following performance counter should be checked.</span></span>

<span data-ttu-id="da610-184">**LC： SIP-01-对等 \\ sip-017-发送未完成**</span><span class="sxs-lookup"><span data-stu-id="da610-184">**LC:SIP-01-Peers\\SIP-017-Sends Outstanding**</span></span>

<span data-ttu-id="da610-185">此计数器表示传出的排队请求和响应的数量。</span><span class="sxs-lookup"><span data-stu-id="da610-185">This counter indicates the number of outgoing queued requests and responses.</span></span> <span data-ttu-id="da610-186">如果此计数器较高，则问题很可能不在本地服务器上。</span><span class="sxs-lookup"><span data-stu-id="da610-186">If this counter is high then the issue is most likely not on the local server.</span></span> <span data-ttu-id="da610-187">请注意，如果存在网络延迟问题，此计数器可能会很高。</span><span class="sxs-lookup"><span data-stu-id="da610-187">Note that this counter can be high if there are network latency issues.</span></span> <span data-ttu-id="da610-188">它还可以指示本地网络适配器的问题，但更可能是由于远程服务器上的问题导致的。</span><span class="sxs-lookup"><span data-stu-id="da610-188">It could also indicate issues with the local network adapter, but is more likely caused by an issue on a remote server.</span></span> <span data-ttu-id="da610-189">当它尝试与其通信的池超载时，此计数器最有可能在控制器服务器上很高。</span><span class="sxs-lookup"><span data-stu-id="da610-189">This counter would most likely be high on a Director server when the pool it is trying to communicate with is overloaded.</span></span> <span data-ttu-id="da610-190">此计数器的键是查看实例，而不仅仅是总数。</span><span class="sxs-lookup"><span data-stu-id="da610-190">The key with this counter is to look at the instances, not just the total.</span></span>

<span data-ttu-id="da610-191"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da610-191"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

