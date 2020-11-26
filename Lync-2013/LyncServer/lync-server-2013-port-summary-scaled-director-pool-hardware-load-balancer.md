---
title: Lync Server 2013：端口摘要 - 扩展的控制器池、硬件负载平衡器
description: Lync Server 2013：端口摘要-已缩放的控制器池、硬件负载平衡器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled Director pool, hardware load balancer
ms:assetid: 6ae2f4ac-5b64-4e45-8253-133308f5812d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204983(v=OCS.15)
ms:contentKeyID: 48184434
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10bfb3a3ad3a38b6cb0e46414bf22deecc71d7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442794"
---
# <a name="port-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="69cc0-103">Lync Server 2013 中的端口摘要 - 扩展的控制器池、硬件负载平衡器</span><span class="sxs-lookup"><span data-stu-id="69cc0-103">Port summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69cc0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69cc0-104">

<span> </span></span></span>

<span data-ttu-id="69cc0-105">_**主题上次修改时间：** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="69cc0-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="69cc0-106">控制器池的防火墙端口要求由用于从边缘服务器的内部接口或反向代理的内部接口内部接口中的控制器建立通信的端口。</span><span class="sxs-lookup"><span data-stu-id="69cc0-106">Firewall port requirements for a Director pool consist of the ports that are used to establish communication with the Director from the internal interface of the Edge Server or internal-facing interface of the reverse proxy.</span></span> <span data-ttu-id="69cc0-107">默认情况下，Microsoft Lync Server 2013 需要从反向代理（以及前端池和前端服务器）打开端口 HTTP/TCP 8080 和 HTTPS/TCP 4443。</span><span class="sxs-lookup"><span data-stu-id="69cc0-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="69cc0-108">此外，必须存在) 从边缘服务器内部接口到 Director 以及前端池和前端服务器的会话初始协议 (SIP 的通信。</span><span class="sxs-lookup"><span data-stu-id="69cc0-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="69cc0-109">SIP 协议使用 SIP/MTLS/TCP 5061，从边缘服务器到前端池和前端服务器。</span><span class="sxs-lookup"><span data-stu-id="69cc0-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="69cc0-110">还必须创建允许从 Director、前端池和前端服务器到边缘服务器内部接口的 SIP/MTLS/TCP 5061 通信的规则。</span><span class="sxs-lookup"><span data-stu-id="69cc0-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="69cc0-111">防火墙定义的控制器端口和协议</span><span class="sxs-lookup"><span data-stu-id="69cc0-111">Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69cc0-112">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="69cc0-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="69cc0-113">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="69cc0-113">Source IP address</span></span></th>
<th><span data-ttu-id="69cc0-114">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="69cc0-114">Destination IP address</span></span></th>
<th><span data-ttu-id="69cc0-115">备注</span><span class="sxs-lookup"><span data-stu-id="69cc0-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69cc0-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="69cc0-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="69cc0-117">反向代理内部接口</span><span class="sxs-lookup"><span data-stu-id="69cc0-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="69cc0-118">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="69cc0-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="69cc0-119">从反向代理的外部方开始，通信将发送到 Director HLB VIP 和前端服务器 web 服务</span><span class="sxs-lookup"><span data-stu-id="69cc0-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69cc0-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="69cc0-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="69cc0-121">反向代理内部接口</span><span class="sxs-lookup"><span data-stu-id="69cc0-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="69cc0-122">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="69cc0-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="69cc0-123">从反向代理的外部方开始，通信将发送到 Director HLB VIP 和前端服务器 web 服务</span><span class="sxs-lookup"><span data-stu-id="69cc0-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69cc0-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="69cc0-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="69cc0-125">控制器</span><span class="sxs-lookup"><span data-stu-id="69cc0-125">Director</span></span></p></td>
<td><p><span data-ttu-id="69cc0-126">前端服务器或前端池</span><span class="sxs-lookup"><span data-stu-id="69cc0-126">Front End Server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="69cc0-127">Director HLB VIP 和前端服务器之间的服务器间通信</span><span class="sxs-lookup"><span data-stu-id="69cc0-127">Inter-server communication between the Director HLB VIP and the Front End Servers</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69cc0-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="69cc0-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="69cc0-129">内部客户端</span><span class="sxs-lookup"><span data-stu-id="69cc0-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="69cc0-130">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="69cc0-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="69cc0-131">Director 向内部和外部客户端提供 web 服务。</span><span class="sxs-lookup"><span data-stu-id="69cc0-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69cc0-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="69cc0-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="69cc0-133">内部客户端</span><span class="sxs-lookup"><span data-stu-id="69cc0-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="69cc0-134">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="69cc0-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="69cc0-135">Director 向内部和外部客户端提供 web 服务。</span><span class="sxs-lookup"><span data-stu-id="69cc0-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69cc0-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="69cc0-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="69cc0-137">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="69cc0-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="69cc0-138">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="69cc0-138">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="69cc0-139">从边缘服务器到控制器和前端服务器的 SIP 通信。</span><span class="sxs-lookup"><span data-stu-id="69cc0-139">SIP communication from the Edge Server to the Director, and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69cc0-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="69cc0-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="69cc0-141">任意</span><span class="sxs-lookup"><span data-stu-id="69cc0-141">Any</span></span></p></td>
<td><p><span data-ttu-id="69cc0-142">控制器</span><span class="sxs-lookup"><span data-stu-id="69cc0-142">Director</span></span></p></td>
<td><p><span data-ttu-id="69cc0-143">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="69cc0-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69cc0-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="69cc0-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="69cc0-145">任意</span><span class="sxs-lookup"><span data-stu-id="69cc0-145">Any</span></span></p></td>
<td><p><span data-ttu-id="69cc0-146">控制器</span><span class="sxs-lookup"><span data-stu-id="69cc0-146">Director</span></span></p></td>
<td><p><span data-ttu-id="69cc0-147">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="69cc0-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69cc0-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="69cc0-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="69cc0-149">任意</span><span class="sxs-lookup"><span data-stu-id="69cc0-149">Any</span></span></p></td>
<td><p><span data-ttu-id="69cc0-150">控制器</span><span class="sxs-lookup"><span data-stu-id="69cc0-150">Director</span></span></p></td>
<td><p><span data-ttu-id="69cc0-151">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="69cc0-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="69cc0-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69cc0-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

