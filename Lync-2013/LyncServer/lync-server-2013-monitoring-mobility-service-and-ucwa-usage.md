---
title: Lync Server 2013：监视移动服务和 UCWA 使用情况
description: Lync Server 2013：监视移动服务和 UCWA 用法。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Mobility Service and UCWA usage
ms:assetid: 8389b37a-ca3e-4047-8b51-85bc07da87e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690025(v=OCS.15)
ms:contentKeyID: 48184683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6575941faf904e46cd1f66d7226a16c88e8cbaa3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425393"
---
# <a name="monitoring-mobility-service-and-ucwa-usage-in-lync-server-2013"></a><span data-ttu-id="8f948-103">在 Lync Server 2013 中监视移动服务和 UCWA 使用情况</span><span class="sxs-lookup"><span data-stu-id="8f948-103">Monitoring Mobility Service and UCWA usage in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f948-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f948-104">

<span> </span></span></span>

<span data-ttu-id="8f948-105">_**主题上次修改时间：** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="8f948-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="8f948-106">在持续的基础上，你应该监视 Lync Server 移动服务 (Mcx) 和统一通信 Web API (UCWA) 所使用的 CPU 和内存。</span><span class="sxs-lookup"><span data-stu-id="8f948-106">On an ongoing basis, you should monitor the CPU and memory that is used by the Lync Server Mobility Service (Mcx) and the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="8f948-107">若要监视使用率，您可以使用以下任一方法：</span><span class="sxs-lookup"><span data-stu-id="8f948-107">To monitor usage, you can use the following:</span></span>

<span data-ttu-id="8f948-108">**对于统一通信 Web API (UCWA)：**</span><span class="sxs-lookup"><span data-stu-id="8f948-108">**For Unified Communications Web API (UCWA):**</span></span>

  - <span data-ttu-id="8f948-109"> (IIS) 管理器的 Internet 信息服务中的 **LyncUcwa** 工作进程。</span><span class="sxs-lookup"><span data-stu-id="8f948-109">The **LyncUcwa** worker process in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="8f948-110">在“**工作进程**”窗格中，查看“**CPU 百分比**”和“**专用字节 (KB)**”（内存）列。</span><span class="sxs-lookup"><span data-stu-id="8f948-110">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="8f948-111">**CPU** 和 **处理器** 性能计数器。</span><span class="sxs-lookup"><span data-stu-id="8f948-111">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="8f948-112">对于大多数部署，UCWA CPU 平均使用率应低于 15%。</span><span class="sxs-lookup"><span data-stu-id="8f948-112">For most deployments, UCWA CPU usage should be below 15 percent on average.</span></span> <span data-ttu-id="8f948-113">内存使用率应在 "在 [Lync server 2013 中监视服务器内存容量限制](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)" 中介绍的限制范围内。</span><span class="sxs-lookup"><span data-stu-id="8f948-113">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="8f948-114">除 CPU 和内存使用率计数器之外，您可以使用以下性能计数器来帮助确定服务器上的请求何时过载：</span><span class="sxs-lookup"><span data-stu-id="8f948-114">In addition to CPU and memory usage counters, you can use the following performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="8f948-115">**LS： WEB-限制和身份验证 \\WEB –处理中的总请求** 数，指示服务器上的挂起 web 请求数。</span><span class="sxs-lookup"><span data-stu-id="8f948-115">**LS:WEB – Throttling and Authentication\\WEB – Total Requests in Processing**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="8f948-116">当此计数器达到 10,000 时，后续请求将失败，错误消息为“503 - 服务不可用”。</span><span class="sxs-lookup"><span data-stu-id="8f948-116">When this counter reaches 10,000, subsequent requests will fail, with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="8f948-117">**ASP.NET \\排队** (的请求应始终为零) 。</span><span class="sxs-lookup"><span data-stu-id="8f948-117">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8f948-118">如果您达到或超过这些值，则应该重新访问和重新计算您的容量规划，以便对托管 Web 服务的计算机进行正确的 CPU、内核数和内存的调整。</span><span class="sxs-lookup"><span data-stu-id="8f948-118">If you meet or exceed these values, you should revisit and re-compute your capacity planning for the correct sizing of CPU, number of cores and memory for the computers hosting the Web services.</span></span>



</div>

<span data-ttu-id="8f948-119">**对于 Mobility Service (Mcx)：**</span><span class="sxs-lookup"><span data-stu-id="8f948-119">**For the Mobility Service (Mcx):**</span></span>

  - <span data-ttu-id="8f948-120"> (IIS) 管理器的 Internet 信息服务中的 **CSIntMcxAppPool** 和 **CSExtMcxAppPool** 工作进程。</span><span class="sxs-lookup"><span data-stu-id="8f948-120">The **CSIntMcxAppPool** and **CSExtMcxAppPool** worker processes in Internet Information Services (IIS) Manager.</span></span> <span data-ttu-id="8f948-121">在“**工作进程**”窗格中，查看“**CPU 百分比**”和“**专用字节 (KB)**”（内存）列。</span><span class="sxs-lookup"><span data-stu-id="8f948-121">In the **Worker Processes** pane, look at the **CPU %** and **Private Bytes (KB)** (memory) columns.</span></span>

  - <span data-ttu-id="8f948-122">**CPU** 和 **处理器** 性能计数器。</span><span class="sxs-lookup"><span data-stu-id="8f948-122">The **CPU** and **Processor** performance counters.</span></span>

<span data-ttu-id="8f948-123">对于大多数部署，Mobility Service CPU 平均使用率应低于 15%。</span><span class="sxs-lookup"><span data-stu-id="8f948-123">For most deployments, Mobility Service CPU usage should be below 15 percent, on average.</span></span> <span data-ttu-id="8f948-124">内存使用率应在 "在 [Lync server 2013 中监视服务器内存容量限制](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)" 中介绍的限制范围内。</span><span class="sxs-lookup"><span data-stu-id="8f948-124">Memory usage should fall within the limits described in [Monitoring for server memory capacity limits in Lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md).</span></span>

<span data-ttu-id="8f948-125">除 CPU 和内存使用率计数器之外，您可以使用以下 ASP.NET 性能计数器来帮助确定服务器上的请求何时过载：</span><span class="sxs-lookup"><span data-stu-id="8f948-125">In addition to CPU and memory usage counters, you can use the following ASP.NET performance counters to help determine when a server is overloaded with requests:</span></span>

  - <span data-ttu-id="8f948-126">**ASP.NET v 2.0.50727 \\请求 "当前**"，指示服务器上的挂起 web 请求的数量。</span><span class="sxs-lookup"><span data-stu-id="8f948-126">**ASP.NET v2.0.50727\\Requests Current**, which indicates the number of pending web requests on the server.</span></span> <span data-ttu-id="8f948-127">当此计数器达到 5,000 时，后续请求将失败，错误消息为“503 - 服务不可用”。</span><span class="sxs-lookup"><span data-stu-id="8f948-127">When this counter reaches 5,000, subsequent requests will fail with the error message, "503 - Service Unavailable."</span></span>

  - <span data-ttu-id="8f948-128">**ASP.NET \\排队** (的请求应始终为零) 。</span><span class="sxs-lookup"><span data-stu-id="8f948-128">**ASP.NET\\Requests Queued** (should always be zero).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8f948-129">如果您达到或超过这些值，则应该重新访问和重新计算您的容量规划，以便正确调整托管 Web 服务的计算机的 CPU、内核数和内存的大小。</span><span class="sxs-lookup"><span data-stu-id="8f948-129">If you meet or exceed these values, you should revisit and recompute your capacity planning for the correct sizing of CPU, number of cores, and memory for the computers hosting the Web services.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8f948-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f948-130">See Also</span></span>


[<span data-ttu-id="8f948-131">在 Lync Server 2013 中监视服务器内存容量限制</span><span class="sxs-lookup"><span data-stu-id="8f948-131">Monitoring for server memory capacity limits in Lync Server 2013</span></span>](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)  
  

<span data-ttu-id="8f948-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f948-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

