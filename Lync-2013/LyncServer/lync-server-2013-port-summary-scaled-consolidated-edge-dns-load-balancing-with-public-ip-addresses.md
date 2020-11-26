---
title: Lync Server 2013：端口摘要 - 扩展的合并边缘（通过公用 IP 地址进行 DNS 负载平衡）
description: Lync Server 2013：端口摘要-缩放后的合并边缘，具有公共 IP 地址的 DNS 负载平衡。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: f7cbd0f1-841d-4116-8d17-e9d991daa4a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205394(v=OCS.15)
ms:contentKeyID: 48185865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8090435485b4b6a183702a608b139cec91ae26a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446337"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="3f805-103">Lync Server 2013 中的端口摘要 - 扩展的合并边缘（通过公用 IP 地址进行 DNS 负载平衡）</span><span class="sxs-lookup"><span data-stu-id="3f805-103">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f805-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f805-104">

<span> </span></span></span>

<span data-ttu-id="3f805-105">_**主题上次修改时间：** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="3f805-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="3f805-106">此方案体系结构中所述的 Lync Server 2013、Edge 服务器功能非常类似于 Lync Server 2010 中实现的功能。</span><span class="sxs-lookup"><span data-stu-id="3f805-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="3f805-107">最显著的相加是 TCP 条目 **上** 的端口5269，用于可扩展消息和状态协议 (XMPP) 。</span><span class="sxs-lookup"><span data-stu-id="3f805-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="3f805-108">Lync Server 2013 （可选）在 Edge 服务器或边缘池以及前端服务器或前端池中的 XMPP 网关服务器上部署 XMPP 代理。</span><span class="sxs-lookup"><span data-stu-id="3f805-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="3f805-109">除了 IPv4，Edge 服务器现在还支持 IPv6。</span><span class="sxs-lookup"><span data-stu-id="3f805-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="3f805-110">为了清楚起见，方案中仅使用了 IPv4。</span><span class="sxs-lookup"><span data-stu-id="3f805-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="3f805-111">**用于缩放合并边缘的企业外围网络，具有公共 IP 地址的 DNS 负载平衡**</span><span class="sxs-lookup"><span data-stu-id="3f805-111">**Enterprise perimeter network for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses**</span></span>

<span data-ttu-id="3f805-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="3f805-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="3f805-113">端口和协议详细信息</span><span class="sxs-lookup"><span data-stu-id="3f805-113">Port and Protocol Details</span></span>

<span data-ttu-id="3f805-114">建议你仅打开支持你为其提供外部访问的功能所需的端口。</span><span class="sxs-lookup"><span data-stu-id="3f805-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="3f805-115">若要使远程访问适用于任何 edge 服务，必须确保 SIP 流量可以双向排列，如入站/出站边缘流量图中所示。</span><span class="sxs-lookup"><span data-stu-id="3f805-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="3f805-116">另外一种方法是，在即时消息 (IM) 、状态、web 会议、音频/视频 (A/V) 和联盟）中涉及到 "访问边缘" 服务的 SIP 消息。</span><span class="sxs-lookup"><span data-stu-id="3f805-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="3f805-117">用于缩放后的合并边缘的防火墙摘要、具有公共 IP 地址的 DNS 负载平衡：外部接口-节点1和节点 2 (示例) </span><span class="sxs-lookup"><span data-stu-id="3f805-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f805-118">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="3f805-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3f805-119">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-119">Source IP address</span></span></th>
<th><span data-ttu-id="3f805-120">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-120">Destination IP address</span></span></th>
<th><span data-ttu-id="3f805-121">备注</span><span class="sxs-lookup"><span data-stu-id="3f805-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f805-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="3f805-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="3f805-123">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-123">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-124">XMPP 代理服务 (与 Access Edge 服务共享 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="3f805-125">XMPP 代理服务接受来自定义的 XMPP 联合的 XMPP 联系人的流量</span><span class="sxs-lookup"><span data-stu-id="3f805-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-126">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="3f805-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="3f805-127">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-128">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-128">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-129">证书吊销/CRL 检查和检索</span><span class="sxs-lookup"><span data-stu-id="3f805-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="3f805-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="3f805-131">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-132">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-132">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-133">通过 TCP 进行 DNS 查询</span><span class="sxs-lookup"><span data-stu-id="3f805-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="3f805-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="3f805-135">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-135">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-136">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-136">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-137">通过 UDP 进行 DNS 查询</span><span class="sxs-lookup"><span data-stu-id="3f805-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-138">Access/SIP (TLS) /TCP/443</span><span class="sxs-lookup"><span data-stu-id="3f805-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3f805-139">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-139">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-140">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-140">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-141">用于外部用户访问的客户端到服务器 SIP 流量</span><span class="sxs-lookup"><span data-stu-id="3f805-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-142">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3f805-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3f805-143">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-143">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-144">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-144">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-145">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="3f805-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-146">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3f805-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3f805-147">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-147">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-148">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-148">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-149">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="3f805-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-150">网络会议/PSOM (TLS) TCP/443</span><span class="sxs-lookup"><span data-stu-id="3f805-150">Web Conferencing/PSOM(TLS)TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3f805-151">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-151">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-152">Edge 服务器 Web 会议边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-152">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-153">网络会议媒体</span><span class="sxs-lookup"><span data-stu-id="3f805-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-154">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="3f805-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3f805-155">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-155">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-156">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-156">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-157">与运行 Office 通信服务器2007、Office 通信服务器 2007 R2、Lync Server 2010 和 Lync Server 2013 的合作伙伴进行联盟所必需。</span><span class="sxs-lookup"><span data-stu-id="3f805-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-158">A/V/RTP/UDP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="3f805-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3f805-159">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-159">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-160">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-160">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-161">仅适用于运行 Office 通信服务器2007的合作伙伴的联盟所必需。</span><span class="sxs-lookup"><span data-stu-id="3f805-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-162">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="3f805-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3f805-163">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-163">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-164">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-165">仅适用于运行 Office 通信服务器2007的合作伙伴的联盟所需</span><span class="sxs-lookup"><span data-stu-id="3f805-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-166">A/V/RTP/UDP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="3f805-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3f805-167">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-167">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-168">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-168">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-169">仅适用于运行 Office 通信服务器2007的合作伙伴的联盟所需</span><span class="sxs-lookup"><span data-stu-id="3f805-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-170">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3f805-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3f805-171">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-171">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-172">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-172">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-173">3478出站用于确定 Lync Server 与之通信的边缘服务器的版本以及边缘服务器到边缘服务器上的媒体流量。</span><span class="sxs-lookup"><span data-stu-id="3f805-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="3f805-174">对于具有 Lync Server 2010、Windows Live Messenger 和 Office 通信服务器 2007 R2 的联盟，以及在公司内部部署了多个边缘池的情况下，也是必需的。</span><span class="sxs-lookup"><span data-stu-id="3f805-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-175">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3f805-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3f805-176">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-176">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-177">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-177">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-178">通过 UDP/3478 对候选人的 STUN 进行协商/启用</span><span class="sxs-lookup"><span data-stu-id="3f805-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-179">A/V/STUN、MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3f805-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3f805-180">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-180">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-181">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-181">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-182">在 TCP/443 上 STUN/打开候选人的协商</span><span class="sxs-lookup"><span data-stu-id="3f805-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-183">A/V/STUN、MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3f805-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3f805-184">Edge 服务器 A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="3f805-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3f805-185">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-185">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-186">在 TCP/443 上 STUN/打开候选人的协商</span><span class="sxs-lookup"><span data-stu-id="3f805-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="3f805-187">用于缩放后的合并边缘的防火墙摘要、具有公共 IP 地址的 DNS 负载平衡：内部接口-节点1和节点 2 (示例) </span><span class="sxs-lookup"><span data-stu-id="3f805-187">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f805-188">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="3f805-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3f805-189">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-189">Source IP address</span></span></th>
<th><span data-ttu-id="3f805-190">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-190">Destination IP address</span></span></th>
<th><span data-ttu-id="3f805-191">备注</span><span class="sxs-lookup"><span data-stu-id="3f805-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f805-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="3f805-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="3f805-193">任何 (都可以定义为前端服务器地址或运行 XMPP 网关服务的前端池 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-193">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="3f805-194">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-195">来自前端服务器或前端池运行的 XMPP 网关服务的出站 XMPP 流量</span><span class="sxs-lookup"><span data-stu-id="3f805-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3f805-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3f805-197">任何 (都可以定义为 Director、Director pool IP 地址、前端服务器或前端池 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="3f805-198">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-199">出站 SIP 流量 (从 Director、Director pool IP 地址、前端服务器或前端池 IP 地址) 到边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3f805-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3f805-201">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-202">任何 (都可以定义为 Director、Director pool IP 地址、前端服务器或前端池 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="3f805-203">入站 SIP 流量 (来自边缘服务器内部接口的控制器、控制器池 IP 地址、前端服务器或前端池 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="3f805-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="3f805-205">任何 (都可以定义为前端服务器 IP 地址，或在前端池中的每个前端服务器 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="3f805-206">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-207">从前端服务器或每台前端服务器（如果在池中）到边缘服务器内部接口的 Web 会议流量</span><span class="sxs-lookup"><span data-stu-id="3f805-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="3f805-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="3f805-209">任何 (都可以定义为前端服务器 IP 地址或前端池 IP 地址，或使用此 Edge 服务器的任何 Survivable 分支装置或 Survivable 分支服务器) </span><span class="sxs-lookup"><span data-stu-id="3f805-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="3f805-210">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-211"> (A/v 身份验证服务的身份验证 A/V 身份验证服务) 使用此 Edge 服务器的前端服务器或前端池 IP 地址或任何 Survivable 分支装置或 Survivable 分支服务器</span><span class="sxs-lookup"><span data-stu-id="3f805-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-212">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3f805-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3f805-213">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-213">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-214">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-215">内部和外部用户之间的/V 媒体传输的首选路径，Survivable 分支装置或 Survivable 分支服务器</span><span class="sxs-lookup"><span data-stu-id="3f805-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-216">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3f805-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3f805-217">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-217">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-218">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-219">内部和外部用户、Survivable 分支装置或 Survivable 分支服务器之间的 A/V 媒体传输的回退路径如果无法建立 UDP 通信，则使用 TCP 进行文件传输和桌面共享</span><span class="sxs-lookup"><span data-stu-id="3f805-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="3f805-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="3f805-221">任何 (都可以定义为保留中央管理存储的前端服务器 IP 地址或池) </span><span class="sxs-lookup"><span data-stu-id="3f805-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="3f805-222">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-223">将中央管理存储中的更改复制到边缘服务器</span><span class="sxs-lookup"><span data-stu-id="3f805-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="3f805-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="3f805-225">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-225">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-226">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-227">使用 Lync Server Management Shell 和集中式日志记录服务 cmdlet、ClsController 命令行 ( # A0) 或代理 ( # A1) 命令和日志收集的集中式日志记录服务控制器</span><span class="sxs-lookup"><span data-stu-id="3f805-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="3f805-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="3f805-229">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-229">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-230">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-231">使用 Lync Server Management Shell 和集中式日志记录服务 cmdlet、ClsController 命令行 ( # A0) 或代理 ( # A1) 命令和日志收集的集中式日志记录服务控制器</span><span class="sxs-lookup"><span data-stu-id="3f805-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="3f805-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="3f805-233">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-233">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-234">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="3f805-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3f805-235">使用 Lync Server Management Shell 和集中式日志记录服务 cmdlet、ClsController 命令行 ( # A0) 或代理 ( # A1) 命令和日志收集的集中式日志记录服务控制器</span><span class="sxs-lookup"><span data-stu-id="3f805-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="3f805-236">联盟的防火墙摘要</span><span class="sxs-lookup"><span data-stu-id="3f805-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f805-237">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="3f805-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3f805-238">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-238">Source IP address</span></span></th>
<th><span data-ttu-id="3f805-239">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-239">Destination IP address</span></span></th>
<th><span data-ttu-id="3f805-240">备注</span><span class="sxs-lookup"><span data-stu-id="3f805-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f805-241">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3f805-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3f805-242">Access Edge 服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-243">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-243">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-244">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="3f805-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="3f805-245">防火墙摘要-公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="3f805-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f805-246">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="3f805-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3f805-247">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-247">Source IP address</span></span></th>
<th><span data-ttu-id="3f805-248">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-248">Destination IP address</span></span></th>
<th><span data-ttu-id="3f805-249">备注</span><span class="sxs-lookup"><span data-stu-id="3f805-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f805-250">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3f805-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3f805-251">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="3f805-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="3f805-252">Edge 服务器访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="3f805-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="3f805-253">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="3f805-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-254">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3f805-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3f805-255">Edge 服务器访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="3f805-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="3f805-256">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="3f805-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="3f805-257">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="3f805-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-258">Access/SIP (TLS) /TCP/443</span><span class="sxs-lookup"><span data-stu-id="3f805-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3f805-259">客户端</span><span class="sxs-lookup"><span data-stu-id="3f805-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="3f805-260">Edge 服务器访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="3f805-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="3f805-261">用于外部用户访问的客户端到服务器 SIP 流量</span><span class="sxs-lookup"><span data-stu-id="3f805-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-262">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="3f805-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3f805-263">Edge 服务器 A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="3f805-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3f805-264">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="3f805-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="3f805-265">如果配置了公用 IM 连接，则用于带有 Windows Live Messenger 的 A/V 会话。</span><span class="sxs-lookup"><span data-stu-id="3f805-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-266">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3f805-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3f805-267">Edge 服务器 A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="3f805-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3f805-268">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="3f805-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="3f805-269">与 Windows Live Messenger 的公共即时消息连接所必需</span><span class="sxs-lookup"><span data-stu-id="3f805-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-270">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3f805-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3f805-271">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="3f805-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="3f805-272">Edge 服务器 A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="3f805-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3f805-273">与 Windows Live Messenger 的公共即时消息连接所必需</span><span class="sxs-lookup"><span data-stu-id="3f805-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="3f805-274">可扩展消息和状态协议的防火墙摘要</span><span class="sxs-lookup"><span data-stu-id="3f805-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f805-275">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="3f805-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3f805-276">源 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="3f805-277">目标 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="3f805-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="3f805-278">备注</span><span class="sxs-lookup"><span data-stu-id="3f805-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f805-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="3f805-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="3f805-280">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-280">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-281">Edge 服务器访问边缘服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-282">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="3f805-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="3f805-283">允许与联盟 XMPP 合作伙伴的 Edge 服务器 XMPP 代理通信</span><span class="sxs-lookup"><span data-stu-id="3f805-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f805-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="3f805-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="3f805-285">Edge 服务器访问边缘服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="3f805-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="3f805-286">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-286">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-287">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="3f805-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="3f805-288">允许从 Edge 服务器 XMPP 代理到联合 XMPP 合作伙伴的通信</span><span class="sxs-lookup"><span data-stu-id="3f805-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f805-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="3f805-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="3f805-290">任意</span><span class="sxs-lookup"><span data-stu-id="3f805-290">Any</span></span></p></td>
<td><p><span data-ttu-id="3f805-291">每个内部边缘服务器接口 IP</span><span class="sxs-lookup"><span data-stu-id="3f805-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="3f805-292">从前端服务器或前端池中的 XMPP 网关到边缘服务器内部 IP 地址或每个边缘池成员的内部 IP 地址的内部 XMPP 流量</span><span class="sxs-lookup"><span data-stu-id="3f805-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3f805-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f805-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

