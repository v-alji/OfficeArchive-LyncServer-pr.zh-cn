---
title: Lync Server 2013：内部服务器的端口和协议
description: Lync Server 2013：内部服务器的端口和协议。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Ports and protocols for internal servers
ms:assetid: c94063f1-e802-4a61-be90-022fc185335e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398833(v=OCS.15)
ms:contentKeyID: 48185402
ms.date: 04/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7d8f12c78c5dec5caacaeb1156f4d228b7cd591
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424245"
---
# <a name="ports-and-protocols-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="78fc0-103">Lync Server 2013 中内部服务器的端口和协议</span><span class="sxs-lookup"><span data-stu-id="78fc0-103">Ports and protocols for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78fc0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78fc0-104">

<span> </span></span></span>

<span data-ttu-id="78fc0-105">_**主题上次修改时间：** 2016-04-06_</span><span class="sxs-lookup"><span data-stu-id="78fc0-105">_**Topic Last Modified:** 2016-04-06_</span></span>

<span data-ttu-id="78fc0-106">本部分概述了 Lync Server 部署中的服务器、负载平衡器和客户端使用的端口和协议。</span><span class="sxs-lookup"><span data-stu-id="78fc0-106">This section summarizes the ports and protocols used by servers, load balancers, and clients in a Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="78fc0-107">Lync 和 Communicator 客户参与一次通信时，通常称为对等。</span><span class="sxs-lookup"><span data-stu-id="78fc0-107">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="78fc0-108">从技术上讲，两个客户在一次对话中进行通信，并且即时消息 multipoint control 单位 (IMMCU) 在中间。</span><span class="sxs-lookup"><span data-stu-id="78fc0-108">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="78fc0-109">IMMCU 是前端服务器的组件。</span><span class="sxs-lookup"><span data-stu-id="78fc0-109">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="78fc0-110">将 IMMCU 放入所需的通信工作流中，可使呼叫详细记录和前端服务器启用的其他功能。</span><span class="sxs-lookup"><span data-stu-id="78fc0-110">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="78fc0-111">从客户端上的动态源端口到前端服务器端口 TLS/TCP/5061 (的通信是假设使用了推荐的传输层安全性) 。</span><span class="sxs-lookup"><span data-stu-id="78fc0-111">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="78fc0-112">根据设计、对等通信 (以及多方 IM) 仅当 Lync Server 和 IMMCU 处于活动状态且可用时才有可能。</span><span class="sxs-lookup"><span data-stu-id="78fc0-112">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="78fc0-113">端口和协议详细信息</span><span class="sxs-lookup"><span data-stu-id="78fc0-113">Port and Protocol Details</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="78fc0-114">在服务器上启动 Lync Server 服务之前，Windows 防火墙必须运行，因为这是 Lync 服务器在防火墙中打开所需端口的时候。</span><span class="sxs-lookup"><span data-stu-id="78fc0-114">Windows Firewall must be running before you start the Lync Server services on a server, because that is when Lync Server opens the required ports in the firewall.</span></span>



</div>

<span data-ttu-id="78fc0-115">有关 edge 组件的防火墙配置的详细信息，请参阅 [确定 Lync Server 2013 的外部 A/V 防火墙和端口要求](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="78fc0-115">For details about firewall configuration for edge components, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

<span data-ttu-id="78fc0-116">下表依据每个内部服务器角色列出了需要打开的端口。</span><span class="sxs-lookup"><span data-stu-id="78fc0-116">The following table lists the ports that need to be open on each internal server role.</span></span>

### <a name="required-server-ports-by-server-role"></a><span data-ttu-id="78fc0-117">所需服务器端口（根据服务器角色）</span><span class="sxs-lookup"><span data-stu-id="78fc0-117">Required Server Ports (by Server Role)</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78fc0-118">服务器角色</span><span class="sxs-lookup"><span data-stu-id="78fc0-118">Server role</span></span></th>
<th><span data-ttu-id="78fc0-119">服务名称</span><span class="sxs-lookup"><span data-stu-id="78fc0-119">Service name</span></span></th>
<th><span data-ttu-id="78fc0-120">端口</span><span class="sxs-lookup"><span data-stu-id="78fc0-120">Port</span></span></th>
<th><span data-ttu-id="78fc0-121">协议</span><span class="sxs-lookup"><span data-stu-id="78fc0-121">Protocol</span></span></th>
<th><span data-ttu-id="78fc0-122">备注</span><span class="sxs-lookup"><span data-stu-id="78fc0-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-123">所有服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-123">All Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-124">SQL 浏览器</span><span class="sxs-lookup"><span data-stu-id="78fc0-124">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="78fc0-125">1434</span><span class="sxs-lookup"><span data-stu-id="78fc0-125">1434</span></span></p></td>
<td><p><span data-ttu-id="78fc0-126">UDP</span><span class="sxs-lookup"><span data-stu-id="78fc0-126">UDP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-127">中央管理存储数据库的本地复制副本的 SQL 浏览器。</span><span class="sxs-lookup"><span data-stu-id="78fc0-127">SQL Browser for the local replicated copy of the Central Management Store database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-128">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-128">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-129">Lync Server Front-End 服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-129">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-130">5060</span><span class="sxs-lookup"><span data-stu-id="78fc0-130">5060</span></span></p></td>
<td><p><span data-ttu-id="78fc0-131">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-131">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-132">（可选）Standard Edition Server 和前端服务器用于静态路由到受信任服务，例如，远程呼叫控制服务器。</span><span class="sxs-lookup"><span data-stu-id="78fc0-132">Optionally used by Standard Edition servers and Front End Servers for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-133">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-133">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-134">Lync Server Front-End 服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-134">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-135">5061</span><span class="sxs-lookup"><span data-stu-id="78fc0-135">5061</span></span></p></td>
<td><p><span data-ttu-id="78fc0-136">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-136">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-137">Standard Edition Server 和前端池用于在服务器 (MTLS) 之间进行所有的内部 SIP 通信、在服务器和客户端 (TLS) 之间进行 SIP 通信，以及在前端服务器和中介服务器 (MTLS) 之间进行 SIP 通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-137">Used by Standard Edition servers and Front End pools for all internal SIP communications between servers (MTLS), for SIP communications between Server and Client (TLS) and for SIP communications between Front End Servers and Mediation Servers (MTLS).</span></span> <span data-ttu-id="78fc0-138">也用于与监视服务器的通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-138">Also used for communications with Monitoring Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-139">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-139">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-140">Lync Server Front-End 服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-140">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-141">444</span><span class="sxs-lookup"><span data-stu-id="78fc0-141">444</span></span></p></td>
<td><p><span data-ttu-id="78fc0-142">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-142">HTTPS</span></span></p>
<p><span data-ttu-id="78fc0-143">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-143">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-144">用于管理会议状态) 和单个服务器的 (Lync Server 组件的焦点之间的 HTTPS 通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-144">Used for HTTPS communication between the Focus (the Lync Server component that manages conference state) and the individual servers.</span></span></p>
<p><span data-ttu-id="78fc0-145">此端口还用于 Survivable 分支装置和前端服务器之间的 TCP 通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-145">This port is also used for TCP communication between Survivable Branch Appliances and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-146">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-146">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-147">Lync Server Front-End 服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-147">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-148">135</span><span class="sxs-lookup"><span data-stu-id="78fc0-148">135</span></span></p></td>
<td><p><span data-ttu-id="78fc0-149">DCOM 和远程过程调用 (RPC)</span><span class="sxs-lookup"><span data-stu-id="78fc0-149">DCOM and remote procedure call (RPC)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-150">用于基于 DCOM 的操作，例如，移动用户、用户复制程序同步和通讯簿同步。</span><span class="sxs-lookup"><span data-stu-id="78fc0-150">Used for DCOM based operations such as Moving Users, User Replicator Synchronization, and Address Book Synchronization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-151">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-151">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-152">Lync Server IM 会议服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-152">Lync Server IM Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-153">5062</span><span class="sxs-lookup"><span data-stu-id="78fc0-153">5062</span></span></p></td>
<td><p><span data-ttu-id="78fc0-154">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-154">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-155">用于即时消息 (IM) 会议的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-155">Used for incoming SIP requests for instant messaging (IM) conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-156">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-156">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-157">Lync Server Web 会议服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-157">Lync Server Web Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-158">8057</span><span class="sxs-lookup"><span data-stu-id="78fc0-158">8057</span></span></p></td>
<td><p><span data-ttu-id="78fc0-159">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-159">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-160">用于侦听来自客户端的持续性共享对象模型 (PSOM) 连接。</span><span class="sxs-lookup"><span data-stu-id="78fc0-160">Used to listen for Persistent Shared Object Model (PSOM) connections from client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-161">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-161">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-162">Lync Server Web 会议兼容性服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-162">Lync Server Web Conferencing Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-163">8058</span><span class="sxs-lookup"><span data-stu-id="78fc0-163">8058</span></span></p></td>
<td><p><span data-ttu-id="78fc0-164">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-164">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-165">用于侦听永久共享对象模型 (PSOM 从 Live Meeting 客户端和早期版本的 Lync Server 中) 连接。</span><span class="sxs-lookup"><span data-stu-id="78fc0-165">Used to listen for Persistent Shared Object Model (PSOM) connections from the Live Meeting client and previous versions of Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-166">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-166">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-167">Lync Server 音频/视频会议服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-167">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-168">5063</span><span class="sxs-lookup"><span data-stu-id="78fc0-168">5063</span></span></p></td>
<td><p><span data-ttu-id="78fc0-169">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-169">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-170">用于音频/视频 (A/V) 会议的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-170">Used for incoming SIP requests for audio/video (A/V) conferencing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-171">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-171">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-172">Lync Server 音频/视频会议服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-172">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-173">57501-65535</span><span class="sxs-lookup"><span data-stu-id="78fc0-173">57501-65535</span></span></p></td>
<td><p><span data-ttu-id="78fc0-174">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="78fc0-174">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-175">用于视频会议的媒体端口范围。</span><span class="sxs-lookup"><span data-stu-id="78fc0-175">Media port range used for video conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-176">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-176">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-177">Lync Server Web 兼容性服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-177">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-178">80</span><span class="sxs-lookup"><span data-stu-id="78fc0-178">80</span></span></p></td>
<td><p><span data-ttu-id="78fc0-179">HTTP</span><span class="sxs-lookup"><span data-stu-id="78fc0-179">HTTP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-180">用于未使用 HTTPS 时从前端服务器到 Web 场 FQDN（IIS Web 组件使用的 URL）的通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-180">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components) when HTTPS is not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-181">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-181">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-182">Lync Server Web 兼容性服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-182">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-183">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-183">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-184">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-184">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="78fc0-185">用于从前端服务器到 Web 场 FQDN（IIS Web 组件使用的 URL）的通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-185">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-186">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-186">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-187">Lync Server Web 兼容性服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-187">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-188">8080</span><span class="sxs-lookup"><span data-stu-id="78fc0-188">8080</span></span></p></td>
<td><p><span data-ttu-id="78fc0-189">TCP 和 HTTP</span><span class="sxs-lookup"><span data-stu-id="78fc0-189">TCP and HTTP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-190">用于 Web 组件供外部访问。</span><span class="sxs-lookup"><span data-stu-id="78fc0-190">Used by web components for external access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-191">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-191">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-192">Web 服务器组件</span><span class="sxs-lookup"><span data-stu-id="78fc0-192">Web server component</span></span></p></td>
<td><p><span data-ttu-id="78fc0-193">4443</span><span class="sxs-lookup"><span data-stu-id="78fc0-193">4443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-194">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-194">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="78fc0-195">HTTPS（从反向代理）和 HTTPS 前端池间通信，用于自动发现登录。</span><span class="sxs-lookup"><span data-stu-id="78fc0-195">HTTPS (from Reverse Proxy) and HTTPS Front End inter-pool communications for Autodiscover sign-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-196">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-196">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-197">Web 服务器组件</span><span class="sxs-lookup"><span data-stu-id="78fc0-197">Web server component</span></span></p></td>
<td><p><span data-ttu-id="78fc0-198">8060</span><span class="sxs-lookup"><span data-stu-id="78fc0-198">8060</span></span></p></td>
<td><p><span data-ttu-id="78fc0-199">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-199">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-200">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-200">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-201">Web 服务器组件</span><span class="sxs-lookup"><span data-stu-id="78fc0-201">Web server component</span></span></p></td>
<td><p><span data-ttu-id="78fc0-202">8061</span><span class="sxs-lookup"><span data-stu-id="78fc0-202">8061</span></span></p></td>
<td><p><span data-ttu-id="78fc0-203">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-203">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-204">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-204">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-205">Mobility Service 组件</span><span class="sxs-lookup"><span data-stu-id="78fc0-205">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="78fc0-206">5086</span><span class="sxs-lookup"><span data-stu-id="78fc0-206">5086</span></span></p></td>
<td><p><span data-ttu-id="78fc0-207">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-207">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-208">Mobility Service 内部过程所使用的 SIP 端口。</span><span class="sxs-lookup"><span data-stu-id="78fc0-208">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-209">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-209">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-210">Mobility Service 组件</span><span class="sxs-lookup"><span data-stu-id="78fc0-210">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="78fc0-211">5087</span><span class="sxs-lookup"><span data-stu-id="78fc0-211">5087</span></span></p></td>
<td><p><span data-ttu-id="78fc0-212">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-212">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-213">Mobility Service 内部过程所使用的 SIP 端口。</span><span class="sxs-lookup"><span data-stu-id="78fc0-213">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-214">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-214">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-215">Mobility Service 组件</span><span class="sxs-lookup"><span data-stu-id="78fc0-215">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="78fc0-216">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-216">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-217">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-217">HTTPS</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-218">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-218">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-219">Lync Server 会议助理服务 (电话拨入式会议) </span><span class="sxs-lookup"><span data-stu-id="78fc0-219">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-220">5064</span><span class="sxs-lookup"><span data-stu-id="78fc0-220">5064</span></span></p></td>
<td><p><span data-ttu-id="78fc0-221">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-221">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-222">用于电话拨入式会议的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-222">Used for incoming SIP requests for dial-in conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-223">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-223">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-224">Lync Server 会议助理服务 (电话拨入式会议) </span><span class="sxs-lookup"><span data-stu-id="78fc0-224">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-225">5072</span><span class="sxs-lookup"><span data-stu-id="78fc0-225">5072</span></span></p></td>
<td><p><span data-ttu-id="78fc0-226">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-226">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-227">用于助理 (拨入式会议) 的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-227">Used for incoming SIP requests for Attendant (dial in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-228">也运行并置中介服务器的前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-228">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-229">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-229">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-230">5070</span><span class="sxs-lookup"><span data-stu-id="78fc0-230">5070</span></span></p></td>
<td><p><span data-ttu-id="78fc0-231">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-231">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-232">中介服务器用于从前端服务器到中介服务器的传入请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-232">Used by the Mediation Server for incoming requests from the Front End Server to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-233">也运行并置中介服务器的前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-233">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-234">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-234">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-235">5067</span><span class="sxs-lookup"><span data-stu-id="78fc0-235">5067</span></span></p></td>
<td><p><span data-ttu-id="78fc0-236">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-236">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-237">用于从 PSTN 网关到中介服务器的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-237">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-238">也运行并置中介服务器的前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-238">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-239">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-239">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-240">5068</span><span class="sxs-lookup"><span data-stu-id="78fc0-240">5068</span></span></p></td>
<td><p><span data-ttu-id="78fc0-241">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-241">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-242">用于从 PSTN 网关到中介服务器的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-242">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-243">也运行并置中介服务器的前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-243">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-244">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-244">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-245">5081</span><span class="sxs-lookup"><span data-stu-id="78fc0-245">5081</span></span></p></td>
<td><p><span data-ttu-id="78fc0-246">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-246">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-247">用于从中介服务器到 PSTN 网关的传出 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-247">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-248">也运行并置中介服务器的前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-248">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-249">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-249">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-250">5082</span><span class="sxs-lookup"><span data-stu-id="78fc0-250">5082</span></span></p></td>
<td><p><span data-ttu-id="78fc0-251">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-251">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-252">用于从中介服务器到 PSTN 网关的传出 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-252">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-253">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-253">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-254">Lync Server 应用程序共享服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-254">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-255">5065</span><span class="sxs-lookup"><span data-stu-id="78fc0-255">5065</span></span></p></td>
<td><p><span data-ttu-id="78fc0-256">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-256">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-257">用于应用程序共享的传入 SIP 侦听请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-257">Used for incoming SIP listening requests for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-258">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-258">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-259">Lync Server 应用程序共享服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-259">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-260">49152-65535</span><span class="sxs-lookup"><span data-stu-id="78fc0-260">49152-65535</span></span></p></td>
<td><p><span data-ttu-id="78fc0-261">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-261">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-262">用于应用程序共享的媒体端口范围。</span><span class="sxs-lookup"><span data-stu-id="78fc0-262">Media port range used for application sharing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-263">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-263">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-264">Lync Server 会议公告服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-264">Lync Server Conferencing Announcement service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-265">5073</span><span class="sxs-lookup"><span data-stu-id="78fc0-265">5073</span></span></p></td>
<td><p><span data-ttu-id="78fc0-266">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-266">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-267">用于 Lync Server 会议公告服务的传入 SIP 请求 (即电话拨入式会议) 。</span><span class="sxs-lookup"><span data-stu-id="78fc0-267">Used for incoming SIP requests for the Lync Server Conferencing Announcement service (that is, for dial-in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-268">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-268">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-269">Lync Server 呼叫寄存服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-269">Lync Server Call Park service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-270">5075</span><span class="sxs-lookup"><span data-stu-id="78fc0-270">5075</span></span></p></td>
<td><p><span data-ttu-id="78fc0-271">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-271">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-272">用于呼叫寄存应用程序的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-272">Used for incoming SIP requests for the Call Park application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-273">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-273">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-274">Lync Server 音频测试服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-274">Lync Server Audio Test service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-275">5076</span><span class="sxs-lookup"><span data-stu-id="78fc0-275">5076</span></span></p></td>
<td><p><span data-ttu-id="78fc0-276">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-276">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-277">用于音频测试服务的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-277">Used for incoming SIP requests for the Audio Test service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-278">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-278">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-279">不适用</span><span class="sxs-lookup"><span data-stu-id="78fc0-279">Not applicable</span></span></p></td>
<td><p><span data-ttu-id="78fc0-280">5066</span><span class="sxs-lookup"><span data-stu-id="78fc0-280">5066</span></span></p></td>
<td><p><span data-ttu-id="78fc0-281">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-281">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-282">用于出站增强型 9-1-1 (E9-1-1) 网关。</span><span class="sxs-lookup"><span data-stu-id="78fc0-282">Used for outbound Enhanced 9-1-1 (E9-1-1) gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-283">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-283">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-284">Lync Server 响应组服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-284">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-285">5071</span><span class="sxs-lookup"><span data-stu-id="78fc0-285">5071</span></span></p></td>
<td><p><span data-ttu-id="78fc0-286">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-286">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-287">用于响应组应用程序的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-287">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-288">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-288">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-289">Lync Server 响应组服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-289">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-290">8404</span><span class="sxs-lookup"><span data-stu-id="78fc0-290">8404</span></span></p></td>
<td><p><span data-ttu-id="78fc0-291">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-291">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-292">用于响应组应用程序的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-292">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-293">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-293">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-294">Lync Server 带宽策略服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-294">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-295">5080</span><span class="sxs-lookup"><span data-stu-id="78fc0-295">5080</span></span></p></td>
<td><p><span data-ttu-id="78fc0-296">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-296">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-297">用于通过带宽策略服务对 A/V 边缘 TURN 流量进行呼叫允许控制。</span><span class="sxs-lookup"><span data-stu-id="78fc0-297">Used for call admission control by the Bandwidth Policy service for A/V Edge TURN traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-298">前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-298">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-299">Lync Server 带宽策略服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-299">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-300">448</span><span class="sxs-lookup"><span data-stu-id="78fc0-300">448</span></span></p></td>
<td><p><span data-ttu-id="78fc0-301">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-301">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-302">由 Lync Server 带宽策略服务用于呼叫许可控制。</span><span class="sxs-lookup"><span data-stu-id="78fc0-302">Used for call admission control by the Lync Server Bandwidth Policy Service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-303">中央管理存储所在的前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-303">Front End Servers where the Central Management store resides</span></span></p></td>
<td><p><span data-ttu-id="78fc0-304">Lync Server 主复制程序代理服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-304">Lync Server Master Replicator Agent service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-305">445</span><span class="sxs-lookup"><span data-stu-id="78fc0-305">445</span></span></p></td>
<td><p><span data-ttu-id="78fc0-306">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-306">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-307">用于将配置数据从中央管理存储推送到运行 Lync Server 的服务器。</span><span class="sxs-lookup"><span data-stu-id="78fc0-307">Used to push configuration data from the Central Management store to servers running Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-308">所有服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-308">All Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-309">SQL 浏览器</span><span class="sxs-lookup"><span data-stu-id="78fc0-309">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="78fc0-310">1434</span><span class="sxs-lookup"><span data-stu-id="78fc0-310">1434</span></span></p></td>
<td><p><span data-ttu-id="78fc0-311">UDP</span><span class="sxs-lookup"><span data-stu-id="78fc0-311">UDP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-312">本地 SQL Server 实例中中央管理存储数据的本地复制副本的 SQL 浏览器</span><span class="sxs-lookup"><span data-stu-id="78fc0-312">SQL Browser for local replicated copy of Central Management store data in local SQL Server instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-313">所有内部服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-313">All internal servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-314">各种</span><span class="sxs-lookup"><span data-stu-id="78fc0-314">Various</span></span></p></td>
<td><p><span data-ttu-id="78fc0-315">49152-57500</span><span class="sxs-lookup"><span data-stu-id="78fc0-315">49152-57500</span></span></p></td>
<td><p><span data-ttu-id="78fc0-316">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="78fc0-316">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-317">用于所有内部服务器上的音频会议的媒体端口范围。</span><span class="sxs-lookup"><span data-stu-id="78fc0-317">Media port range used for audio conferencing on all internal servers.</span></span> <span data-ttu-id="78fc0-318">由终止音频的所有服务器使用：前端服务器 (Lync Server 会议助理服务、Lync Server 会议公告服务和 Lync Server 音频/视频会议服务) 以及中介服务器。</span><span class="sxs-lookup"><span data-stu-id="78fc0-318">Used by all servers that terminate audio: Front End Servers (for Lync Server Conferencing Attendant service, Lync Server Conferencing Announcement service, and Lync Server Audio/Video Conferencing service), and Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-319">Office Web Apps Servers</span><span class="sxs-lookup"><span data-stu-id="78fc0-319">Office Web Apps Servers</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78fc0-320">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-320">443</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78fc0-321">由 Lync Server 2013 用于连接到 Office Web Apps 服务器。</span><span class="sxs-lookup"><span data-stu-id="78fc0-321">Used by Lync Server 2013 to connect to Office Web Apps Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-322">控制器</span><span class="sxs-lookup"><span data-stu-id="78fc0-322">Directors</span></span></p></td>
<td><p><span data-ttu-id="78fc0-323">Lync Server Front-End 服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-323">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-324">5060</span><span class="sxs-lookup"><span data-stu-id="78fc0-324">5060</span></span></p></td>
<td><p><span data-ttu-id="78fc0-325">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-325">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-326">（可选）用于静态路由到受信任服务，例如，远程呼叫控制服务器。</span><span class="sxs-lookup"><span data-stu-id="78fc0-326">Optionally used for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-327">控制器</span><span class="sxs-lookup"><span data-stu-id="78fc0-327">Directors</span></span></p></td>
<td><p><span data-ttu-id="78fc0-328">Lync Server Front-End 服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-328">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-329">444</span><span class="sxs-lookup"><span data-stu-id="78fc0-329">444</span></span></p></td>
<td><p><span data-ttu-id="78fc0-330">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-330">HTTPS</span></span></p>
<p><span data-ttu-id="78fc0-331">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-331">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-332">前端与控制器之间的服务器间通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-332">Inter-server communication between Front End and Director.</span></span> <span data-ttu-id="78fc0-333">此外，客户端证书向前端服务器发布 () 或验证客户端证书是否已发布。</span><span class="sxs-lookup"><span data-stu-id="78fc0-333">Additionally, client certificate publish (to Front End Servers) or validate if the client certificate has already been published.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-334">控制器</span><span class="sxs-lookup"><span data-stu-id="78fc0-334">Directors</span></span></p></td>
<td><p><span data-ttu-id="78fc0-335">Lync Server Web 兼容性服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-335">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-336">80</span><span class="sxs-lookup"><span data-stu-id="78fc0-336">80</span></span></p></td>
<td><p><span data-ttu-id="78fc0-337">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-337">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-p105">用于从控制器到 Web 场 FQDN（IIS Web 组件使用的 URL）的初始通信。在常规操作中，将使用端口 443 和协议类型 TCP 切换到 HTTPS 通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-p105">Used for initial communication from Directors to the web farm FQDNs (the URLs used by IIS web components). In normal operation, will switch to HTTPS traffic, using port 443 and protocol type TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-340">控制器</span><span class="sxs-lookup"><span data-stu-id="78fc0-340">Directors</span></span></p></td>
<td><p><span data-ttu-id="78fc0-341">Lync Server Web 兼容性服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-341">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-342">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-342">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-343">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-343">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="78fc0-344">用于从控制器到 Web 场 FQDN（IIS Web 组件使用的 URL）之间的通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-344">Used for communication from Directors to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-345">控制器</span><span class="sxs-lookup"><span data-stu-id="78fc0-345">Directors</span></span></p></td>
<td><p><span data-ttu-id="78fc0-346">Lync Server Front-End 服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-346">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-347">5061</span><span class="sxs-lookup"><span data-stu-id="78fc0-347">5061</span></span></p></td>
<td><p><span data-ttu-id="78fc0-348">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-348">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-349">用于服务器之间的内部通信和客户端连接。</span><span class="sxs-lookup"><span data-stu-id="78fc0-349">Used for internal communications between servers and for client connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-350">中介服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-350">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-351">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-351">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-352">5070</span><span class="sxs-lookup"><span data-stu-id="78fc0-352">5070</span></span></p></td>
<td><p><span data-ttu-id="78fc0-353">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-353">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-354">中介服务器用于来自前端服务器的传入请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-354">Used by the Mediation Server for incoming requests from the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-355">中介服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-355">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-356">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-356">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-357">5067</span><span class="sxs-lookup"><span data-stu-id="78fc0-357">5067</span></span></p></td>
<td><p><span data-ttu-id="78fc0-358">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-358">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-359">用于来自 PSTN 网关的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-359">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-360">中介服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-360">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-361">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-361">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-362">5068</span><span class="sxs-lookup"><span data-stu-id="78fc0-362">5068</span></span></p></td>
<td><p><span data-ttu-id="78fc0-363">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-363">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-364">用于来自 PSTN 网关的传入 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-364">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-365">中介服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-365">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="78fc0-366">Lync Server 中介服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-366">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-367">5070</span><span class="sxs-lookup"><span data-stu-id="78fc0-367">5070</span></span></p></td>
<td><p><span data-ttu-id="78fc0-368">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-368">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-369">用于来自前端服务器的 SIP 请求。</span><span class="sxs-lookup"><span data-stu-id="78fc0-369">Used for SIP requests from the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-370">持久聊天前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-370">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-371">持久聊天 SIP</span><span class="sxs-lookup"><span data-stu-id="78fc0-371">Persistent Chat SIP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-372">5041</span><span class="sxs-lookup"><span data-stu-id="78fc0-372">5041</span></span></p></td>
<td><p><span data-ttu-id="78fc0-373">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-373">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-374">持久聊天前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-374">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-375">持久聊天 Windows Communication Foundation (WCF)</span><span class="sxs-lookup"><span data-stu-id="78fc0-375">Persistent Chat Windows Communication Foundation (WCF)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-376">881</span><span class="sxs-lookup"><span data-stu-id="78fc0-376">881</span></span></p></td>
<td><p><span data-ttu-id="78fc0-377">TCP (TLS) 和 TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-377">TCP (TLS) and TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-378">持久聊天前端服务器</span><span class="sxs-lookup"><span data-stu-id="78fc0-378">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="78fc0-379">持久聊天文件传输服务</span><span class="sxs-lookup"><span data-stu-id="78fc0-379">Persistent Chat File Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="78fc0-380">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-380">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-381">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-381">TCP (TLS)</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="78fc0-382">某些远程呼叫控制方案需要前端服务器或控制器与 PBX 之间的 TCP 连接。</span><span class="sxs-lookup"><span data-stu-id="78fc0-382">Some remote call control scenarios require a TCP connection between the Front End Server or Director and the PBX.</span></span> <span data-ttu-id="78fc0-383">虽然 Lync Server 不再使用 TCP 端口5060，但在远程呼叫控制部署期间，你创建了一个受信任的服务器配置，该配置将 RCC 线路服务器 FQDN 与前端服务器或控制器用于连接到 PBX 系统的 TCP 端口相关联。</span><span class="sxs-lookup"><span data-stu-id="78fc0-383">Although Lync Server no longer uses TCP port 5060, during remote call control deployment you create a trusted server configuration, which associates the RCC Line Server FQDN with the TCP port that the Front End Server or Director will use to connect to the PBX system.</span></span> <span data-ttu-id="78fc0-384">有关详细信息，请参阅 Lync Server Management Shell 文档中的 <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78fc0-384">For details, see the <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet in the Lync Server Management Shell documentation.</span></span>



</div>

<span data-ttu-id="78fc0-385">对于仅使用硬件负载平衡（不是 DNS 负载平衡）的池，下表显示了需要打开硬件负载平衡器的端口。</span><span class="sxs-lookup"><span data-stu-id="78fc0-385">For your pools that use only hardware load balancing (not DNS load balancing), the following table shows the ports that need to open the hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-only-hardware-load-balancing"></a><span data-ttu-id="78fc0-386">仅使用硬件负载平衡时的硬件负载平衡器端口</span><span class="sxs-lookup"><span data-stu-id="78fc0-386">Hardware Load Balancer Ports if Using Only Hardware Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78fc0-387">负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-387">Load Balancer</span></span></th>
<th><span data-ttu-id="78fc0-388">端口</span><span class="sxs-lookup"><span data-stu-id="78fc0-388">Port</span></span></th>
<th><span data-ttu-id="78fc0-389">协议</span><span class="sxs-lookup"><span data-stu-id="78fc0-389">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-390">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-390">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-391">5061</span><span class="sxs-lookup"><span data-stu-id="78fc0-391">5061</span></span></p></td>
<td><p><span data-ttu-id="78fc0-392">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-392">TCP (TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-393">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-393">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-394">444</span><span class="sxs-lookup"><span data-stu-id="78fc0-394">444</span></span></p></td>
<td><p><span data-ttu-id="78fc0-395">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-395">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-396">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-396">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-397">135</span><span class="sxs-lookup"><span data-stu-id="78fc0-397">135</span></span></p></td>
<td><p><span data-ttu-id="78fc0-398">DCOM 和远程过程调用 (RPC)</span><span class="sxs-lookup"><span data-stu-id="78fc0-398">DCOM and remote procedure call (RPC)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-399">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-399">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-400">80</span><span class="sxs-lookup"><span data-stu-id="78fc0-400">80</span></span></p></td>
<td><p><span data-ttu-id="78fc0-401">HTTP</span><span class="sxs-lookup"><span data-stu-id="78fc0-401">HTTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-402">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-402">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-403">8080</span><span class="sxs-lookup"><span data-stu-id="78fc0-403">8080</span></span></p></td>
<td><p><span data-ttu-id="78fc0-404">TCP - 从前端服务器中进行的客户端和设备根证书检索 – NTLM 授权的客户端和设备</span><span class="sxs-lookup"><span data-stu-id="78fc0-404">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-405">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-405">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-406">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-406">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-407">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-407">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-408">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-408">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-409">4443</span><span class="sxs-lookup"><span data-stu-id="78fc0-409">4443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-410">HTTPS（来自反向代理）</span><span class="sxs-lookup"><span data-stu-id="78fc0-410">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-411">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-411">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-412">5072</span><span class="sxs-lookup"><span data-stu-id="78fc0-412">5072</span></span></p></td>
<td><p><span data-ttu-id="78fc0-413">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-413">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-414">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-414">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-415">5073</span><span class="sxs-lookup"><span data-stu-id="78fc0-415">5073</span></span></p></td>
<td><p><span data-ttu-id="78fc0-416">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-416">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-417">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-417">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-418">5075</span><span class="sxs-lookup"><span data-stu-id="78fc0-418">5075</span></span></p></td>
<td><p><span data-ttu-id="78fc0-419">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-419">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-420">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-420">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-421">5076</span><span class="sxs-lookup"><span data-stu-id="78fc0-421">5076</span></span></p></td>
<td><p><span data-ttu-id="78fc0-422">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-422">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-423">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-423">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-424">5071</span><span class="sxs-lookup"><span data-stu-id="78fc0-424">5071</span></span></p></td>
<td><p><span data-ttu-id="78fc0-425">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-425">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-426">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-426">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-427">5080</span><span class="sxs-lookup"><span data-stu-id="78fc0-427">5080</span></span></p></td>
<td><p><span data-ttu-id="78fc0-428">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-428">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-429">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-429">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-430">448</span><span class="sxs-lookup"><span data-stu-id="78fc0-430">448</span></span></p></td>
<td><p><span data-ttu-id="78fc0-431">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-431">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-432">中介服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-432">Mediation Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-433">5070</span><span class="sxs-lookup"><span data-stu-id="78fc0-433">5070</span></span></p></td>
<td><p><span data-ttu-id="78fc0-434">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-434">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-435">前端服务器负载平衡器（如果池也运行中介服务器）</span><span class="sxs-lookup"><span data-stu-id="78fc0-435">Front End Server load balancer (if the pool also runs Mediation Server)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-436">5070</span><span class="sxs-lookup"><span data-stu-id="78fc0-436">5070</span></span></p></td>
<td><p><span data-ttu-id="78fc0-437">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-437">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-438">控制器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-438">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-439">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-439">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-440">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-440">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-441">控制器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-441">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-442">444</span><span class="sxs-lookup"><span data-stu-id="78fc0-442">444</span></span></p></td>
<td><p><span data-ttu-id="78fc0-443">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-443">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-444">控制器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-444">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-445">5061</span><span class="sxs-lookup"><span data-stu-id="78fc0-445">5061</span></span></p></td>
<td><p><span data-ttu-id="78fc0-446">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-446">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-447">控制器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-447">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-448">4443</span><span class="sxs-lookup"><span data-stu-id="78fc0-448">4443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-449">HTTPS（来自反向代理）</span><span class="sxs-lookup"><span data-stu-id="78fc0-449">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78fc0-p107">使用 DNS 负载平衡的前端池和控制器池还必须部署硬件负载平衡器。下表显示了需要在这些硬件负载平衡器上打开的端口。</span><span class="sxs-lookup"><span data-stu-id="78fc0-p107">Your Front End pools and Director pools that use DNS load balancing also must have a hardware load balancer deployed. The following table shows the ports that need to be open on these hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-dns-load-balancing"></a><span data-ttu-id="78fc0-452">使用 DNS 负载平衡时的硬件负载平衡器端口</span><span class="sxs-lookup"><span data-stu-id="78fc0-452">Hardware Load Balancer Ports if Using DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78fc0-453">负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-453">Load Balancer</span></span></th>
<th><span data-ttu-id="78fc0-454">端口</span><span class="sxs-lookup"><span data-stu-id="78fc0-454">Port</span></span></th>
<th><span data-ttu-id="78fc0-455">协议</span><span class="sxs-lookup"><span data-stu-id="78fc0-455">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-456">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-456">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-457">80</span><span class="sxs-lookup"><span data-stu-id="78fc0-457">80</span></span></p></td>
<td><p><span data-ttu-id="78fc0-458">HTTP</span><span class="sxs-lookup"><span data-stu-id="78fc0-458">HTTP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-459">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-459">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-460">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-460">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-461">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-461">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-462">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-462">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-463">8080</span><span class="sxs-lookup"><span data-stu-id="78fc0-463">8080</span></span></p></td>
<td><p><span data-ttu-id="78fc0-464">TCP - 从前端服务器中进行的客户端和设备根证书检索 – NTLM 授权的客户端和设备</span><span class="sxs-lookup"><span data-stu-id="78fc0-464">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-465">前端服务器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-465">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-466">4443</span><span class="sxs-lookup"><span data-stu-id="78fc0-466">4443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-467">HTTPS（来自反向代理）</span><span class="sxs-lookup"><span data-stu-id="78fc0-467">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-468">控制器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-468">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-469">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-469">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-470">HTTPS</span><span class="sxs-lookup"><span data-stu-id="78fc0-470">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-471">控制器负载平衡器</span><span class="sxs-lookup"><span data-stu-id="78fc0-471">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="78fc0-472">4443</span><span class="sxs-lookup"><span data-stu-id="78fc0-472">4443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-473">HTTPS（来自反向代理）</span><span class="sxs-lookup"><span data-stu-id="78fc0-473">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="required-client-ports"></a><span data-ttu-id="78fc0-474">所需客户端端口</span><span class="sxs-lookup"><span data-stu-id="78fc0-474">Required Client Ports</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78fc0-475">组件</span><span class="sxs-lookup"><span data-stu-id="78fc0-475">Component</span></span></th>
<th><span data-ttu-id="78fc0-476">端口</span><span class="sxs-lookup"><span data-stu-id="78fc0-476">Port</span></span></th>
<th><span data-ttu-id="78fc0-477">协议</span><span class="sxs-lookup"><span data-stu-id="78fc0-477">Protocol</span></span></th>
<th><span data-ttu-id="78fc0-478">备注</span><span class="sxs-lookup"><span data-stu-id="78fc0-478">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-479">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-479">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-480">67/68</span><span class="sxs-lookup"><span data-stu-id="78fc0-480">67/68</span></span></p></td>
<td><p><span data-ttu-id="78fc0-481">DHCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-481">DHCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-482">由 Lync Server 用于查找注册机构 FQDN (也就是说，如果 DNS SRV 失败，而手动设置未配置) 。</span><span class="sxs-lookup"><span data-stu-id="78fc0-482">Used by Lync Server to find the Registrar FQDN (that is, if DNS SRV fails and manual settings are not configured).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-483">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-483">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-484">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-484">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-485">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-485">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-486">用于外部用户访问的客户端到服务器 SIP 通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-486">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-487">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-487">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-488">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-488">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-489">TCP (PSOM/TLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-489">TCP (PSOM/TLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-490">用于外部用户访问 Web 会议会话。</span><span class="sxs-lookup"><span data-stu-id="78fc0-490">Used for external user access to web conferencing sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-491">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-491">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-492">443</span><span class="sxs-lookup"><span data-stu-id="78fc0-492">443</span></span></p></td>
<td><p><span data-ttu-id="78fc0-493">TCP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="78fc0-493">TCP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-494">用于外部用户访问 A/V 会话和媒体 (TCP)。</span><span class="sxs-lookup"><span data-stu-id="78fc0-494">Used for external user access to A/V sessions and media (TCP)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-495">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-495">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-496">3478</span><span class="sxs-lookup"><span data-stu-id="78fc0-496">3478</span></span></p></td>
<td><p><span data-ttu-id="78fc0-497">UDP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="78fc0-497">UDP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-498">用于外部用户访问 A/V 会话和媒体 (UDP)。</span><span class="sxs-lookup"><span data-stu-id="78fc0-498">Used for external user access to A/V sessions and media (UDP)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-499">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-499">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-500">5061</span><span class="sxs-lookup"><span data-stu-id="78fc0-500">5061</span></span></p></td>
<td><p><span data-ttu-id="78fc0-501">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="78fc0-501">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="78fc0-502">用于外部用户访问的客户端到服务器 SIP 通信。</span><span class="sxs-lookup"><span data-stu-id="78fc0-502">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-503">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-503">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-504">6891-6901</span><span class="sxs-lookup"><span data-stu-id="78fc0-504">6891-6901</span></span></p></td>
<td><p><span data-ttu-id="78fc0-505">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-505">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-506">用于 Lync 客户端和以前的客户端之间的文件传输 (Microsoft Office 通信服务器 2007 R2、Microsoft Office 通信服务器2007和实时通信服务器 2005) 的客户端。</span><span class="sxs-lookup"><span data-stu-id="78fc0-506">Used for file transfer between Lync clients and previous clients (clients of Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007, and Live Communications Server 2005).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-507">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-507">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-508">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="78fc0-508">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="78fc0-509">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="78fc0-509">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-510">音频端口范围（最少需要 20 个端口）。</span><span class="sxs-lookup"><span data-stu-id="78fc0-510">Audio port range (minimum of 20 ports required)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-511">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-511">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-512">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="78fc0-512">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="78fc0-513">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="78fc0-513">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-514">视频端口范围（最少需要 20 个端口）。</span><span class="sxs-lookup"><span data-stu-id="78fc0-514">Video port range (minimum of 20 ports required).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-515">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-515">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-516">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="78fc0-516">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="78fc0-517">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-517">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-518">对等文件传输（对于会议文件传输，客户端使用 PSOM）。</span><span class="sxs-lookup"><span data-stu-id="78fc0-518">Peer-to-peer file transfer (for conferencing file transfer, clients use PSOM).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78fc0-519">客户端</span><span class="sxs-lookup"><span data-stu-id="78fc0-519">Clients</span></span></p></td>
<td><p><span data-ttu-id="78fc0-520">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="78fc0-520">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="78fc0-521">TCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-521">TCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-522">应用程序共享。</span><span class="sxs-lookup"><span data-stu-id="78fc0-522">Application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78fc0-523">Aastra 6721ip 公用区域电话</span><span class="sxs-lookup"><span data-stu-id="78fc0-523">Aastra 6721ip common area phone</span></span></p>
<p><span data-ttu-id="78fc0-524">Aastra 6725ip 桌面电话</span><span class="sxs-lookup"><span data-stu-id="78fc0-524">Aastra 6725ip desk phone</span></span></p>
<p><span data-ttu-id="78fc0-525">HP 4110 IP Phone（公用区域电话）</span><span class="sxs-lookup"><span data-stu-id="78fc0-525">HP 4110 IP Phone (common area phone)</span></span></p>
<p><span data-ttu-id="78fc0-526">HP 4120 IP Phone（桌面电话）</span><span class="sxs-lookup"><span data-stu-id="78fc0-526">HP 4120 IP Phone (desk phone)</span></span></p>
<p><span data-ttu-id="78fc0-527">Polycom CX500 IP 公用区域电话</span><span class="sxs-lookup"><span data-stu-id="78fc0-527">Polycom CX500 IP common area phone</span></span></p>
<p><span data-ttu-id="78fc0-528">Polycom CX600 IP 桌面电话</span><span class="sxs-lookup"><span data-stu-id="78fc0-528">Polycom CX600 IP desk phone</span></span></p>
<p><span data-ttu-id="78fc0-529">Polycom CX700 IP 桌面电话</span><span class="sxs-lookup"><span data-stu-id="78fc0-529">Polycom CX700 IP desk phone</span></span></p>
<p><span data-ttu-id="78fc0-530">Polycom CX3000 IP 会议电话</span><span class="sxs-lookup"><span data-stu-id="78fc0-530">Polycom CX3000 IP conference phone</span></span></p></td>
<td><p><span data-ttu-id="78fc0-531">67/68</span><span class="sxs-lookup"><span data-stu-id="78fc0-531">67/68</span></span></p></td>
<td><p><span data-ttu-id="78fc0-532">DHCP</span><span class="sxs-lookup"><span data-stu-id="78fc0-532">DHCP</span></span></p></td>
<td><p><span data-ttu-id="78fc0-533">由列出的设备用于查找 Lync 服务器证书、配置 FQDN 和注册机构 FQDN。</span><span class="sxs-lookup"><span data-stu-id="78fc0-533">Used by the listed devices to find the Lync Server certificate, provisioning FQDN, and Registrar FQDN.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78fc0-534">**\*** 若要为这些媒体类型配置特定端口，请使用 CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled、ClientMediaPort 和 ClientMediaPortRange 参数) 。</span><span class="sxs-lookup"><span data-stu-id="78fc0-534">**\*** To configure specific ports for these media types, use the CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled, ClientMediaPort, and ClientMediaPortRange parameters).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="78fc0-535">为 Lync 客户端设置的程序在客户端计算机上自动创建所需的操作系统防火墙例外。</span><span class="sxs-lookup"><span data-stu-id="78fc0-535">The set programs for Lync clients automatically create the required operating-system firewall exceptions on the client computer.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="78fc0-536">在客户端必须遍历组织的防火墙的任何方案中，都需要用于外部用户访问的端口（例如，由其他组织承载的任何外部通信或会议）。</span><span class="sxs-lookup"><span data-stu-id="78fc0-536">The ports that are used for external user access are required for any scenario in which the client must traverse the organization’s firewall (for example, any external communications or meetings hosted by other organizations).</span></span>



<span data-ttu-id="78fc0-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78fc0-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

