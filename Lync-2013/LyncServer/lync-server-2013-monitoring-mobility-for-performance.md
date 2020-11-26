---
title: Lync Server 2013：监视性能移动性
description: Lync Server 2013：监视移动性能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring mobility for performance
ms:assetid: 9c831c63-9a7d-48ec-9118-f8a7e80ddd04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690033(v=OCS.15)
ms:contentKeyID: 48184908
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6c366542e88406df043ba1a782ee12cd64bd804
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425400"
---
# <a name="monitoring-mobility-for-performance-in-lync-server-2013"></a><span data-ttu-id="2c2bd-103">在 Lync Server 2013 中监视移动性能</span><span class="sxs-lookup"><span data-stu-id="2c2bd-103">Monitoring mobility for performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c2bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c2bd-104">

<span> </span></span></span>

<span data-ttu-id="2c2bd-105">_**主题上次修改时间：** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="2c2bd-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="2c2bd-106">Lync Server 移动服务 (Mcx) 和统一通信 Web API (UCWA) 增加前端服务器和前端池的负载。</span><span class="sxs-lookup"><span data-stu-id="2c2bd-106">The Lync Server Mobility Service (Mcx) and the Unified Communications Web API (UCWA) increase the load on Front End Servers and Front End pools.</span></span> <span data-ttu-id="2c2bd-107">即使在移动应用程序被最小化的情况下也会保持与服务器的连接的移动设备（如运行 Lync 2010 Mobile 的 Android 和 Nokia 设备）以及运行 Lync 2013 移动设备的 Android 和 Apple 设备比在移动应用程序最小化时终止与服务器的连接的设备相比，增加了更大的负载。</span><span class="sxs-lookup"><span data-stu-id="2c2bd-107">Mobile devices that maintain a connection to the server even when the mobile application is minimized, such as Android and Nokia devices running Lync 2010 Mobile, as well as Android and Apple devices running Lync 2013 Mobile, impose a greater load than devices that terminate their connection to the server when the mobile application is minimized.</span></span> <span data-ttu-id="2c2bd-108">随着移动性用途的增加，您必须监视移动性性能以确定何时需要增加容量。</span><span class="sxs-lookup"><span data-stu-id="2c2bd-108">As your mobility usage increases, you must monitor mobility performance to determine when you need to increase your capacity.</span></span>

<span data-ttu-id="2c2bd-109">有几项限制会影响移动性能：</span><span class="sxs-lookup"><span data-stu-id="2c2bd-109">Several limits influence mobility performance:</span></span>

  - <span data-ttu-id="2c2bd-110">可用内存</span><span class="sxs-lookup"><span data-stu-id="2c2bd-110">Available memory</span></span>

  - <span data-ttu-id="2c2bd-111">请求队列限制</span><span class="sxs-lookup"><span data-stu-id="2c2bd-111">Request queue limit</span></span>

  - <span data-ttu-id="2c2bd-112">并发连接</span><span class="sxs-lookup"><span data-stu-id="2c2bd-112">Concurrent connections</span></span>

  - <span data-ttu-id="2c2bd-113">IIS 队列长度</span><span class="sxs-lookup"><span data-stu-id="2c2bd-113">IIS queue length</span></span>

<span data-ttu-id="2c2bd-114">对可能影响移动性能的服务器的其他限制是最多12个并发登录、身份验证、会话续订和终止。</span><span class="sxs-lookup"><span data-stu-id="2c2bd-114">Other limits on servers that can influence mobility performance are a maximum of twelve concurrent sign-ins, authentications, session renewals, and terminations.</span></span> <span data-ttu-id="2c2bd-115">对于大多数部署，无需修改这些最大值。</span><span class="sxs-lookup"><span data-stu-id="2c2bd-115">These maximums do not need to be modified for most deployments.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2c2bd-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="2c2bd-116">In This Section</span></span>

  - [<span data-ttu-id="2c2bd-117">在 Lync Server 2013 中监视服务器内存容量限制</span><span class="sxs-lookup"><span data-stu-id="2c2bd-117">Monitoring for server memory capacity limits in Lync Server 2013</span></span>](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)

  - [<span data-ttu-id="2c2bd-118">在 Lync Server 2013 中监视移动服务和 UCWA 使用情况</span><span class="sxs-lookup"><span data-stu-id="2c2bd-118">Monitoring Mobility Service and UCWA usage in Lync Server 2013</span></span>](lync-server-2013-monitoring-mobility-service-and-ucwa-usage.md)

  - [<span data-ttu-id="2c2bd-119">在 Lync Server 2013 中配置高性能的移动服务</span><span class="sxs-lookup"><span data-stu-id="2c2bd-119">Configuring Mobility Service for high performance in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-service-for-high-performance.md)

  - [<span data-ttu-id="2c2bd-120">在 Lync Server 2013 中监视 IIS 请求跟踪日志文件</span><span class="sxs-lookup"><span data-stu-id="2c2bd-120">Monitoring IIS request tracing log files in Lync Server 2013</span></span>](lync-server-2013-monitoring-iis-request-tracing-log-files.md)

  - [<span data-ttu-id="2c2bd-121">Lync Server 2013 中的移动性能计数器</span><span class="sxs-lookup"><span data-stu-id="2c2bd-121">Mobility performance counters in Lync Server 2013</span></span>](lync-server-2013-mobility-performance-counters.md)

<span data-ttu-id="2c2bd-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c2bd-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

