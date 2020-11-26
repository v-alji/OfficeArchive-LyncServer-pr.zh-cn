---
title: 端口摘要 - 使用公用 IP 地址的单一合并边缘
description: 端口摘要-具有公共 IP 地址的单个统一边缘。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with public IP addresses
ms:assetid: 28407acc-8b92-4f78-875c-fd6b4323b602
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204756(v=OCS.15)
ms:contentKeyID: 48183685
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82ab2d89404fb174994d8e5b798f64bb68768326
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424256"
---
# <a name="port-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="48612-103">Lync Server 2013 中的端口摘要 - 使用公用 IP 地址的单一合并边缘</span><span class="sxs-lookup"><span data-stu-id="48612-103">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48612-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48612-104">

<span> </span></span></span>

<span data-ttu-id="48612-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="48612-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="48612-106">此方案体系结构中所述的 Lync Server 2013、Edge 服务器功能非常类似于 Lync Server 2010 中实现的功能。</span><span class="sxs-lookup"><span data-stu-id="48612-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="48612-107">最显著的相加是 TCP 条目 **上** 的端口5269，用于可扩展消息和状态协议 (XMPP) 。</span><span class="sxs-lookup"><span data-stu-id="48612-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="48612-108">Lync Server 2013 （可选）在 Edge 服务器或边缘池以及前端服务器或前端池中的 XMPP 网关服务器上部署 XMPP 代理。</span><span class="sxs-lookup"><span data-stu-id="48612-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span> <span data-ttu-id="48612-109">在 [lync server 2013 中的反向代理](lync-server-2013-scenarios-for-reverse-proxy.md) 和在 [lync server 2013 部分中规划 SIP、XMPP 联盟和公共即时消息](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) 的方案中，可以找到反向代理和联合的规划信息。</span><span class="sxs-lookup"><span data-stu-id="48612-109">Planning information for the reverse proxy and federation are found in [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) and [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) sections, respectively.</span></span>

<span data-ttu-id="48612-110">除了 IPv4，Edge 服务器现在还支持 IPv6。</span><span class="sxs-lookup"><span data-stu-id="48612-110">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="48612-111">为了清楚起见，方案中仅使用了 IPv4。</span><span class="sxs-lookup"><span data-stu-id="48612-111">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="48612-112">**具有公共 IP 寻址的单个统一边缘的企业外围网络**</span><span class="sxs-lookup"><span data-stu-id="48612-112">**Enterprise perimeter network for single consolidated edge with public IP addressing**</span></span>

<span data-ttu-id="48612-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="48612-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="48612-114">端口和协议详细信息</span><span class="sxs-lookup"><span data-stu-id="48612-114">Port and Protocol Details</span></span>

<span data-ttu-id="48612-115">我们建议你仅打开支持你为其提供外部访问的功能所需的端口。</span><span class="sxs-lookup"><span data-stu-id="48612-115">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="48612-116">若要使远程访问适用于任何 edge 服务，必须确保 SIP 流量能够流过 bidirectionally，如入站/出站边缘流量图所示。</span><span class="sxs-lookup"><span data-stu-id="48612-116">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bidirectionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="48612-117">另外一种方法是，在即时消息 (IM) 、状态、web 会议、音频/视频 (A/V) 和联盟）中涉及到 "访问边缘" 服务的 SIP 消息。</span><span class="sxs-lookup"><span data-stu-id="48612-117">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-external-interface"></a><span data-ttu-id="48612-118">具有公共 IP 地址的单个统一边缘的防火墙摘要：外部接口</span><span class="sxs-lookup"><span data-stu-id="48612-118">Firewall Summary for Single Consolidated Edge with Public IP Addresses: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48612-119">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="48612-119">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="48612-120">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-120">Source IP address</span></span></th>
<th><span data-ttu-id="48612-121">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-121">Destination IP address</span></span></th>
<th><span data-ttu-id="48612-122">备注</span><span class="sxs-lookup"><span data-stu-id="48612-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48612-123">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="48612-123">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="48612-124">任意</span><span class="sxs-lookup"><span data-stu-id="48612-124">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-125">XMPP 代理服务 (与 Access Edge 服务共享 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="48612-125">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="48612-126">XMPP 代理服务接受来自定义的 XMPP 联合的 XMPP 联系人的流量</span><span class="sxs-lookup"><span data-stu-id="48612-126">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-127">Access/HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="48612-127">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="48612-128">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-128">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-129">任意</span><span class="sxs-lookup"><span data-stu-id="48612-129">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-130">证书吊销/CRL 检查和检索</span><span class="sxs-lookup"><span data-stu-id="48612-130">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-131">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="48612-131">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="48612-132">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-132">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-133">任意</span><span class="sxs-lookup"><span data-stu-id="48612-133">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-134">通过 TCP 进行 DNS 查询</span><span class="sxs-lookup"><span data-stu-id="48612-134">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-135">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="48612-135">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="48612-136">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-136">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-137">任意</span><span class="sxs-lookup"><span data-stu-id="48612-137">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-138">通过 UDP 进行 DNS 查询</span><span class="sxs-lookup"><span data-stu-id="48612-138">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-139">Access/SIP (TLS) /TCP/443</span><span class="sxs-lookup"><span data-stu-id="48612-139">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="48612-140">任意</span><span class="sxs-lookup"><span data-stu-id="48612-140">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-141">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-141">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-142">用于外部用户访问的客户端到服务器 SIP 流量</span><span class="sxs-lookup"><span data-stu-id="48612-142">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-143">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="48612-143">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="48612-144">任意</span><span class="sxs-lookup"><span data-stu-id="48612-144">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-145">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-145">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-146">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="48612-146">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-147">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="48612-147">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="48612-148">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-148">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-149">任意</span><span class="sxs-lookup"><span data-stu-id="48612-149">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-150">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="48612-150">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-151">网络会议/PSOM (TLS) /TCP/443</span><span class="sxs-lookup"><span data-stu-id="48612-151">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="48612-152">任意</span><span class="sxs-lookup"><span data-stu-id="48612-152">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-153">Edge 服务器 Web 会议边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-153">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-154">网络会议媒体</span><span class="sxs-lookup"><span data-stu-id="48612-154">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-155">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="48612-155">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="48612-156">边缘服务器访问边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-156">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-157">任意</span><span class="sxs-lookup"><span data-stu-id="48612-157">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-158">与运行 Office 通信服务器2007、Office 通信服务器 2007 R2、Lync Server 2010 和 Lync Server 2013 的合作伙伴进行联盟所必需。</span><span class="sxs-lookup"><span data-stu-id="48612-158">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-159">A/V/RTP/UDP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="48612-159">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="48612-160">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-160">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-161">任意</span><span class="sxs-lookup"><span data-stu-id="48612-161">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-162">仅适用于运行 Office 通信服务器2007的合作伙伴的联盟所需</span><span class="sxs-lookup"><span data-stu-id="48612-162">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-163">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="48612-163">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="48612-164">任意</span><span class="sxs-lookup"><span data-stu-id="48612-164">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-165">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-165">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-166">仅适用于运行 Office 通信服务器2007的合作伙伴的联盟所必需。</span><span class="sxs-lookup"><span data-stu-id="48612-166">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-167">A/V/RTP/UDP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="48612-167">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="48612-168">任意</span><span class="sxs-lookup"><span data-stu-id="48612-168">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-169">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-169">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-170">仅适用于运行 Office 通信服务器2007的合作伙伴的联盟所必需。</span><span class="sxs-lookup"><span data-stu-id="48612-170">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-171">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="48612-171">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="48612-172">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-172">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-173">任意</span><span class="sxs-lookup"><span data-stu-id="48612-173">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-174">3478出站用于确定 Lync Server 与之通信的边缘服务器的版本以及边缘服务器到边缘服务器上的媒体流量。</span><span class="sxs-lookup"><span data-stu-id="48612-174">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="48612-175">对于具有 Lync Server 2010、Windows Live Messenger 和 Office 通信服务器 2007 R2 的联盟，以及在公司内部部署了多个边缘池的情况下，也是必需的。</span><span class="sxs-lookup"><span data-stu-id="48612-175">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-176">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="48612-176">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="48612-177">任意</span><span class="sxs-lookup"><span data-stu-id="48612-177">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-178">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-178">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-179">通过 UDP/3478 对候选人的 STUN 进行协商/启用</span><span class="sxs-lookup"><span data-stu-id="48612-179">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-180">A/V/STUN、MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="48612-180">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="48612-181">任意</span><span class="sxs-lookup"><span data-stu-id="48612-181">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-182">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-182">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-183">在 TCP/443 上 STUN/打开候选人的协商</span><span class="sxs-lookup"><span data-stu-id="48612-183">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-184">A/V/STUN、MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="48612-184">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="48612-185">Edge 服务器 A/V 边缘服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-185">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-186">任意</span><span class="sxs-lookup"><span data-stu-id="48612-186">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-187">在 TCP/443 上 STUN/打开候选人的协商</span><span class="sxs-lookup"><span data-stu-id="48612-187">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-internal-interface"></a><span data-ttu-id="48612-188">具有公共 IP 地址的单个统一边缘的防火墙摘要：内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-188">Firewall Summary for Single Consolidated Edge with Public IP Addresses: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48612-189">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="48612-189">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="48612-190">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-190">Source IP address</span></span></th>
<th><span data-ttu-id="48612-191">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-191">Destination IP address</span></span></th>
<th><span data-ttu-id="48612-192">备注</span><span class="sxs-lookup"><span data-stu-id="48612-192">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48612-193">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="48612-193">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="48612-194">任何 (都可以定义为运行 XMPP 网关服务的标准版服务器 IP、标准版服务器 IP 地址或池 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="48612-194">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="48612-195">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-195">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-196">来自前端服务器或前端池运行的 XMPP 网关服务的出站 XMPP 流量</span><span class="sxs-lookup"><span data-stu-id="48612-196">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-197">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="48612-197">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="48612-198">任何 (都可以定义为 Director、Director pool IP 地址、前端服务器或前端池 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="48612-198">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="48612-199">包含内部接口的边缘服务器 IP 或池</span><span class="sxs-lookup"><span data-stu-id="48612-199">Edge Server IP, or pool that holds the internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-200">出站 SIP 流量 (从 Director、Director pool IP 地址、前端服务器或前端池 IP 地址) 到边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-200">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-201">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="48612-201">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="48612-202">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-203">任何 (都可以定义为 Director、Director pool IP 地址、前端服务器或前端池地址) </span><span class="sxs-lookup"><span data-stu-id="48612-203">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool address)</span></span></p></td>
<td><p><span data-ttu-id="48612-204">入站 SIP 流量 (来自边缘服务器内部接口的控制器、控制器池 IP 地址、前端服务器或前端池 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="48612-204">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-205">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="48612-205">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="48612-206">任何 (都可以定义为前端服务器 IP 地址，或在前端池中的每个前端服务器 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="48612-206">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="48612-207">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-207">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-208">从前端服务器或每台前端服务器（如果在池中）到边缘服务器内部接口的 Web 会议流量</span><span class="sxs-lookup"><span data-stu-id="48612-208">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-209">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="48612-209">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="48612-210">任何 (都可以定义为前端服务器 IP 地址或前端池 IP 地址，或使用此 Edge 服务器的任何 Survivable 分支装置或 Survivable 分支服务器) </span><span class="sxs-lookup"><span data-stu-id="48612-210">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="48612-211">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-211">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-212"> (A/v 身份验证服务的身份验证 A/V 身份验证服务) 使用此 Edge 服务器的前端服务器或前端池 IP 地址或任何 Survivable 分支装置或 Survivable 分支服务器</span><span class="sxs-lookup"><span data-stu-id="48612-212">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-213">STUN/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="48612-213">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="48612-214">任意</span><span class="sxs-lookup"><span data-stu-id="48612-214">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-215">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-215">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-216">内部和外部用户之间的/V 媒体传输的首选路径，Survivable 分支装置或 Survivable 分支服务器</span><span class="sxs-lookup"><span data-stu-id="48612-216">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-217">STUN/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="48612-217">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="48612-218">任意</span><span class="sxs-lookup"><span data-stu-id="48612-218">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-219">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-219">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-220">内部和外部用户、Survivable 分支装置或 Survivable 分支服务器之间的 A/V 媒体传输的回退路径如果无法建立 UDP 通信，则使用 TCP 进行文件传输和桌面共享</span><span class="sxs-lookup"><span data-stu-id="48612-220">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-221">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="48612-221">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="48612-222">任何 (都可以定义为保留中央管理存储的前端服务器 IP 地址或池) </span><span class="sxs-lookup"><span data-stu-id="48612-222">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="48612-223">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-223">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-224">将中央管理存储中的更改复制到边缘服务器</span><span class="sxs-lookup"><span data-stu-id="48612-224">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-225">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="48612-225">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="48612-226">任意</span><span class="sxs-lookup"><span data-stu-id="48612-226">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-227">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-227">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-228">使用 Lync Server Management Shell 和集中式日志记录服务 cmdlet、ClsController 命令行 ( # A0) 或代理 ( # A1) 命令和日志收集的集中式日志记录服务控制器</span><span class="sxs-lookup"><span data-stu-id="48612-228">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-229">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="48612-229">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="48612-230">任意</span><span class="sxs-lookup"><span data-stu-id="48612-230">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-231">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-231">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-232">使用 Lync Server Management Shell 和集中式日志记录服务 cmdlet、ClsController 命令行 ( # A0) 或代理 ( # A1) 命令和日志收集的集中式日志记录服务控制器</span><span class="sxs-lookup"><span data-stu-id="48612-232">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-233">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="48612-233">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="48612-234">任意</span><span class="sxs-lookup"><span data-stu-id="48612-234">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-235">边缘服务器内部接口</span><span class="sxs-lookup"><span data-stu-id="48612-235">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="48612-236">使用 Lync Server Management Shell 和集中式日志记录服务 cmdlet、ClsController 命令行 ( # A0) 或代理 ( # A1) 命令和日志收集的集中式日志记录服务控制器</span><span class="sxs-lookup"><span data-stu-id="48612-236">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="48612-237">联盟的防火墙摘要</span><span class="sxs-lookup"><span data-stu-id="48612-237">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48612-238">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="48612-238">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="48612-239">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-239">Source IP address</span></span></th>
<th><span data-ttu-id="48612-240">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-240">Destination IP address</span></span></th>
<th><span data-ttu-id="48612-241">备注</span><span class="sxs-lookup"><span data-stu-id="48612-241">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48612-242">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="48612-242">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="48612-243">Access Edge 服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-243">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-244">任意</span><span class="sxs-lookup"><span data-stu-id="48612-244">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-245">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="48612-245">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="48612-246">防火墙摘要-公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="48612-246">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48612-247">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="48612-247">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="48612-248">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-248">Source IP address</span></span></th>
<th><span data-ttu-id="48612-249">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-249">Destination IP address</span></span></th>
<th><span data-ttu-id="48612-250">备注</span><span class="sxs-lookup"><span data-stu-id="48612-250">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48612-251">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="48612-251">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="48612-252">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="48612-252">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="48612-253">Edge 服务器访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="48612-253">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="48612-254">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="48612-254">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-255">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="48612-255">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="48612-256">Edge 服务器访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="48612-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="48612-257">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="48612-257">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="48612-258">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="48612-258">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-259">Access/SIP (TLS) /TCP/443</span><span class="sxs-lookup"><span data-stu-id="48612-259">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="48612-260">客户端</span><span class="sxs-lookup"><span data-stu-id="48612-260">Clients</span></span></p></td>
<td><p><span data-ttu-id="48612-261">Edge 服务器访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="48612-261">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="48612-262">用于外部用户访问的客户端到服务器 SIP 流量</span><span class="sxs-lookup"><span data-stu-id="48612-262">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-263">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="48612-263">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="48612-264">Edge 服务器 A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="48612-264">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="48612-265">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="48612-265">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="48612-266">如果配置了公用 IM 连接，则用于带有 Windows Live Messenger 的 A/V 会话。</span><span class="sxs-lookup"><span data-stu-id="48612-266">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-267">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="48612-267">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="48612-268">Edge 服务器 A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="48612-268">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="48612-269">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="48612-269">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="48612-270">与 Windows Live Messenger 的公共即时消息连接所必需</span><span class="sxs-lookup"><span data-stu-id="48612-270">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-271">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="48612-271">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="48612-272">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="48612-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="48612-273">Edge 服务器 A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="48612-273">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="48612-274">与 Windows Live Messenger 的公共即时消息连接所必需</span><span class="sxs-lookup"><span data-stu-id="48612-274">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="48612-275">可扩展消息和状态协议的防火墙摘要</span><span class="sxs-lookup"><span data-stu-id="48612-275">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48612-276">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="48612-276">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="48612-277">源 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="48612-277">Source (IP address)</span></span></th>
<th><span data-ttu-id="48612-278">目标 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="48612-278">Destination (IP address)</span></span></th>
<th><span data-ttu-id="48612-279">备注</span><span class="sxs-lookup"><span data-stu-id="48612-279">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48612-280">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="48612-280">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="48612-281">任意</span><span class="sxs-lookup"><span data-stu-id="48612-281">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-282">Edge 服务器访问边缘服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-282">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-283">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="48612-283">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="48612-284">允许与联盟 XMPP 合作伙伴的 Edge 服务器 XMPP 代理通信</span><span class="sxs-lookup"><span data-stu-id="48612-284">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48612-285">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="48612-285">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="48612-286">Edge 服务器访问边缘服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="48612-286">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="48612-287">任意</span><span class="sxs-lookup"><span data-stu-id="48612-287">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-288">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="48612-288">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="48612-289">允许从 Edge 服务器 XMPP 代理到联合 XMPP 合作伙伴的通信</span><span class="sxs-lookup"><span data-stu-id="48612-289">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48612-290">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="48612-290">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="48612-291">任意</span><span class="sxs-lookup"><span data-stu-id="48612-291">Any</span></span></p></td>
<td><p><span data-ttu-id="48612-292">每个内部边缘服务器接口 IP</span><span class="sxs-lookup"><span data-stu-id="48612-292">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="48612-293">从前端服务器或前端池中的 XMPP 网关到边缘服务器内部 IP 地址或每个边缘池成员的内部 IP 地址的内部 XMPP 流量</span><span class="sxs-lookup"><span data-stu-id="48612-293">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="48612-294">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48612-294">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

