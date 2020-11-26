---
title: Lync Server 2013：端口摘要 - 单一控制器
description: Lync Server 2013： Port summary-单控制器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single Director
ms:assetid: 079c1414-723f-4499-b7d4-a0d7121c1626
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204648(v=OCS.15)
ms:contentKeyID: 48183322
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a46e394121dbc7dd6158016d39511e9487cec1ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436977"
---
# <a name="port-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="a9eb1-103">Lync Server 2013 中的端口摘要 - 单一控制器</span><span class="sxs-lookup"><span data-stu-id="a9eb1-103">Port summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a9eb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a9eb1-104">

<span> </span></span></span>

<span data-ttu-id="a9eb1-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="a9eb1-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="a9eb1-106">单个控制器的防火墙端口要求由用于从内部接口或反向代理的面向内部网络的控制器建立通信的端口组成。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="a9eb1-107">默认情况下，Microsoft Lync Server 2013 需要从反向代理（以及前端池和前端服务器）打开端口 HTTP/TCP 8080 和 HTTPS/TCP 4443。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="a9eb1-108">此外，必须存在) 从边缘服务器内部接口到 Director 以及前端池和前端服务器的会话初始协议 (SIP 的通信。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="a9eb1-109">SIP 协议使用 SIP/MTLS/TCP 5061，从边缘服务器到前端池和前端服务器。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="a9eb1-110">还必须创建允许从 Director、前端池和前端服务器到边缘服务器内部接口的 SIP/MTLS/TCP 5061 通信的规则。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="a9eb1-111">用于防火墙定义的单控制器端口和协议</span><span class="sxs-lookup"><span data-stu-id="a9eb1-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9eb1-112">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="a9eb1-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="a9eb1-113">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="a9eb1-113">Source IP address</span></span></th>
<th><span data-ttu-id="a9eb1-114">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="a9eb1-114">Destination IP address</span></span></th>
<th><span data-ttu-id="a9eb1-115">备注</span><span class="sxs-lookup"><span data-stu-id="a9eb1-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9eb1-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="a9eb1-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-117">反向代理内部接口</span><span class="sxs-lookup"><span data-stu-id="a9eb1-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-118">控制器</span><span class="sxs-lookup"><span data-stu-id="a9eb1-118">Director</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-119">从反向代理的外部方开始，通信将发送到控制器和前端服务器 web 服务</span><span class="sxs-lookup"><span data-stu-id="a9eb1-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9eb1-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="a9eb1-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-121">反向代理内部接口</span><span class="sxs-lookup"><span data-stu-id="a9eb1-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-122">控制器</span><span class="sxs-lookup"><span data-stu-id="a9eb1-122">Director</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-123">从反向代理的外部方开始，通信将发送到控制器和前端服务器 web 服务</span><span class="sxs-lookup"><span data-stu-id="a9eb1-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9eb1-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="a9eb1-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-125">控制器</span><span class="sxs-lookup"><span data-stu-id="a9eb1-125">Director</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-126">前端服务器或前端池</span><span class="sxs-lookup"><span data-stu-id="a9eb1-126">Front End server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-127">控制器和前端服务器之间的服务器间通信</span><span class="sxs-lookup"><span data-stu-id="a9eb1-127">Inter-server communication between the Director and the Front End Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9eb1-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="a9eb1-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-129">内部客户端</span><span class="sxs-lookup"><span data-stu-id="a9eb1-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-130">控制器 web 服务</span><span class="sxs-lookup"><span data-stu-id="a9eb1-130">Director web services</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-131">控制器向内部和外部客户端提供 web 服务。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-131">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9eb1-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="a9eb1-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-133">内部客户端</span><span class="sxs-lookup"><span data-stu-id="a9eb1-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-134">控制器 web 服务</span><span class="sxs-lookup"><span data-stu-id="a9eb1-134">Director web services</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-135">控制器向内部和外部客户端提供 web 服务。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-135">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9eb1-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="a9eb1-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-137">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="a9eb1-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-138">控制器</span><span class="sxs-lookup"><span data-stu-id="a9eb1-138">Director</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-139">从边缘服务器到控制器的 SIP 通信，以及前端服务器。</span><span class="sxs-lookup"><span data-stu-id="a9eb1-139">SIP communication from the Edge Server to the Director, and the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9eb1-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="a9eb1-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-141">任意</span><span class="sxs-lookup"><span data-stu-id="a9eb1-141">Any</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-142">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="a9eb1-142">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-143">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="a9eb1-143">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9eb1-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="a9eb1-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-145">任意</span><span class="sxs-lookup"><span data-stu-id="a9eb1-145">Any</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-146">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="a9eb1-146">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-147">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="a9eb1-147">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9eb1-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="a9eb1-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-149">任意</span><span class="sxs-lookup"><span data-stu-id="a9eb1-149">Any</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-150">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="a9eb1-150">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="a9eb1-151">集中式日志记录服务控制器 ( # A0) 或代理 ( # A1) 命令和日志收集</span><span class="sxs-lookup"><span data-stu-id="a9eb1-151">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a9eb1-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a9eb1-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

