---
title: Lync Server 2013：端口摘要 - 已进行 DNS 和 HLB 负载平衡
description: Lync Server 2013： Port summary-已平衡的 DNS 和 HLB 负载。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - DNS and HLB load balanced
ms:assetid: b07c37e4-820e-46ee-a678-1da95d1b87af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205179(v=OCS.15)
ms:contentKeyID: 48185149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be2e8204e792fd9c4718cb9171e90784af2d0104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424336"
---
# <a name="port-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="09d2e-103">Lync Server 2013 中的端口摘要 - 已进行 DNS 和 HLB 负载平衡</span><span class="sxs-lookup"><span data-stu-id="09d2e-103">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09d2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09d2e-104">

<span> </span></span></span>

<span data-ttu-id="09d2e-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="09d2e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="09d2e-106">单个控制器的防火墙端口要求由用于从内部接口或反向代理的面向内部网络的控制器建立通信的端口组成。</span><span class="sxs-lookup"><span data-stu-id="09d2e-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="09d2e-107">默认情况下，Microsoft Lync Server 2013 需要从反向代理（以及前端池和前端服务器）打开端口 HTTP/TCP 8080 和 HTTPS/TCP 4443。</span><span class="sxs-lookup"><span data-stu-id="09d2e-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="09d2e-108">此外，必须存在) 从边缘服务器内部接口到 Director 以及前端池和前端服务器的会话初始协议 (SIP 的通信。</span><span class="sxs-lookup"><span data-stu-id="09d2e-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="09d2e-109">SIP 协议使用 SIP/MTLS/TCP 5061，从边缘服务器到前端池和前端服务器。</span><span class="sxs-lookup"><span data-stu-id="09d2e-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="09d2e-110">还必须创建允许从 Director、前端池和前端服务器到边缘服务器内部接口的 SIP/MTLS/TCP 5061 通信的规则。</span><span class="sxs-lookup"><span data-stu-id="09d2e-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="09d2e-111">用于防火墙定义的单控制器端口和协议</span><span class="sxs-lookup"><span data-stu-id="09d2e-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09d2e-112">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="09d2e-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="09d2e-113">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="09d2e-113">Source IP address</span></span></th>
<th><span data-ttu-id="09d2e-114">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="09d2e-114">Destination IP address</span></span></th>
<th><span data-ttu-id="09d2e-115">备注</span><span class="sxs-lookup"><span data-stu-id="09d2e-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09d2e-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="09d2e-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="09d2e-117">反向代理内部接口</span><span class="sxs-lookup"><span data-stu-id="09d2e-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="09d2e-118">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="09d2e-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="09d2e-119">从反向代理的外部方开始，通信将发送到 Director HLB VIP 和前端服务器 web 服务。</span><span class="sxs-lookup"><span data-stu-id="09d2e-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09d2e-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="09d2e-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="09d2e-121">反向代理内部接口</span><span class="sxs-lookup"><span data-stu-id="09d2e-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="09d2e-122">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="09d2e-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="09d2e-123">从反向代理的外部方开始，通信将发送到 Director HLB VIP 和前端服务器 web 服务。</span><span class="sxs-lookup"><span data-stu-id="09d2e-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09d2e-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="09d2e-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="09d2e-125">控制器</span><span class="sxs-lookup"><span data-stu-id="09d2e-125">Director</span></span></p></td>
<td><p><span data-ttu-id="09d2e-126">前端池或前端服务器</span><span class="sxs-lookup"><span data-stu-id="09d2e-126">Front End pool or Front End Server</span></span></p></td>
<td><p><span data-ttu-id="09d2e-127">Director HLB VIP 与前端服务器或前端服务器之间的服务器间通信。</span><span class="sxs-lookup"><span data-stu-id="09d2e-127">Inter-server communication between the Director HLB VIP and the Front End Server or Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09d2e-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="09d2e-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="09d2e-129">内部客户端</span><span class="sxs-lookup"><span data-stu-id="09d2e-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="09d2e-130">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="09d2e-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="09d2e-131">Director 向内部和外部客户端提供 web 服务。</span><span class="sxs-lookup"><span data-stu-id="09d2e-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09d2e-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="09d2e-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="09d2e-133">内部客户端</span><span class="sxs-lookup"><span data-stu-id="09d2e-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="09d2e-134">控制器硬件负载平衡器 VIP</span><span class="sxs-lookup"><span data-stu-id="09d2e-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="09d2e-135">Director 向内部和外部客户端提供 web 服务。</span><span class="sxs-lookup"><span data-stu-id="09d2e-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09d2e-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="09d2e-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="09d2e-137">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="09d2e-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="09d2e-138">控制器</span><span class="sxs-lookup"><span data-stu-id="09d2e-138">Director</span></span></p></td>
<td><p><span data-ttu-id="09d2e-139">从边缘服务器到控制器以及前端服务器的 SIP 通信。</span><span class="sxs-lookup"><span data-stu-id="09d2e-139">SIP communication from the Edge Server to the Director, as well as the Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09d2e-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="09d2e-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="09d2e-141">任意</span><span class="sxs-lookup"><span data-stu-id="09d2e-141">Any</span></span></p></td>
<td><p><span data-ttu-id="09d2e-142">控制器</span><span class="sxs-lookup"><span data-stu-id="09d2e-142">Director</span></span></p></td>
<td><p><span data-ttu-id="09d2e-143">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="09d2e-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09d2e-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="09d2e-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="09d2e-145">任意</span><span class="sxs-lookup"><span data-stu-id="09d2e-145">Any</span></span></p></td>
<td><p><span data-ttu-id="09d2e-146">控制器</span><span class="sxs-lookup"><span data-stu-id="09d2e-146">Director</span></span></p></td>
<td><p><span data-ttu-id="09d2e-147">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="09d2e-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09d2e-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="09d2e-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="09d2e-149">任意</span><span class="sxs-lookup"><span data-stu-id="09d2e-149">Any</span></span></p></td>
<td><p><span data-ttu-id="09d2e-150">控制器</span><span class="sxs-lookup"><span data-stu-id="09d2e-150">Director</span></span></p></td>
<td><p><span data-ttu-id="09d2e-151">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="09d2e-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="09d2e-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09d2e-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

