---
title: Lync Server 2013 硬件负载平衡器要求
description: Lync Server 2013 硬件负载平衡器要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware load balancer requirements
ms:assetid: 32891268-2059-43d0-adf4-af4ff1e9ce66
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ656815(v=OCS.15)
ms:contentKeyID: 49287208
ms.date: 05/11/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69cbf79c1fd7551dfd428c23ed22c924d0805c43
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427717"
---
# <a name="hardware-load-balancer-requirements-for-lync-server-2013"></a><span data-ttu-id="3691b-103">Lync Server 2013 的硬件负载平衡器要求</span><span class="sxs-lookup"><span data-stu-id="3691b-103">Hardware load balancer requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3691b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3691b-104">

<span> </span></span></span>

<span data-ttu-id="3691b-105">_**主题上次修改时间：** 2015-05-11_</span><span class="sxs-lookup"><span data-stu-id="3691b-105">_**Topic Last Modified:** 2015-05-11_</span></span>

<span data-ttu-id="3691b-106">Lync Server 2013 缩放的合并边缘拓扑已针对新部署优化了 DNS 负载平衡，主要与使用 Lync Server 的其他组织联盟。</span><span class="sxs-lookup"><span data-stu-id="3691b-106">The Lync Server 2013 scaled consolidated Edge topology is optimized for DNS load balancing for new deployments federating primarily with other organizations using Lync Server.</span></span> <span data-ttu-id="3691b-107">如果以下任何方案需要高可用性，则必须在 Edge 服务器池中使用硬件负载平衡器才能执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3691b-107">If high availability is required for any of the following scenarios, a hardware load balancer must be used on Edge Server pools for the following:</span></span>

  - <span data-ttu-id="3691b-108">与使用 Office 通信服务器 2007 R2 或 Office 通信服务器2007的组织进行联盟</span><span class="sxs-lookup"><span data-stu-id="3691b-108">Federation with organizations using Office Communications Server 2007 R2 or Office Communications Server 2007</span></span>

  - <span data-ttu-id="3691b-109">在与 SP1 的 Exchange 2010 之前使用 Exchange UM 的远程用户的 exchange UM</span><span class="sxs-lookup"><span data-stu-id="3691b-109">Exchange UM for remote users using Exchange UM prior to Exchange 2010 with SP1</span></span>

  - <span data-ttu-id="3691b-110">与公共 IM 用户的连接</span><span class="sxs-lookup"><span data-stu-id="3691b-110">Connectivity to public IM users</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3691b-p102">不支持对一个接口使用 DNS 负载平衡，而对另一个接口使用硬件负载平衡。必须对两个接口都使用硬件负载平衡，或者对两个接口都使用 DNS 负载平衡。</span><span class="sxs-lookup"><span data-stu-id="3691b-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="3691b-p103">如果使用硬件负载平衡器，则为内部网络连接部署的负载平衡器必须配置为仅对发往运行访问边缘服务和 A/V 边缘服务的服务器的流量进行负载平衡。它不能对发往内部 Web 会议边缘服务或内部 XMPP 代理服务的流量进行负载平衡。</span><span class="sxs-lookup"><span data-stu-id="3691b-p103">If you are using a hardware load balancer, the load balancer deployed for connections with the internal network must be configured to load balance only the traffic to servers running the Access Edge service and the A/V Edge service. It cannot load balance the traffic to the internal Web Conferencing Edge service or the internal XMPP Proxy service.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="3691b-115">Lync Server 2013 不支持直接服务器返回 (DSR) NAT。</span><span class="sxs-lookup"><span data-stu-id="3691b-115">The direct server return (DSR) NAT is not supported with Lync Server 2013.</span></span>



</div>

<span data-ttu-id="3691b-116">若要确定你的硬件负载平衡器是否支持 Lync Server 2013 所需的功能，请参阅 at 中的 "Lync Server 2010 负载平衡器合作伙伴" [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452) 。</span><span class="sxs-lookup"><span data-stu-id="3691b-116">To determine whether your hardware load balancer supports the necessary features required by Lync Server 2013, see "Lync Server 2010 Load Balancer Partners" at [https://go.microsoft.com/fwlink/p/?linkId=202452](https://go.microsoft.com/fwlink/p/?linkid=202452).</span></span>

<div>

## <a name="hardware-load-balancer-requirements-for-edge-servers-running-the-av-edge-service"></a><span data-ttu-id="3691b-117">运行 A/V 边缘服务的边缘服务器的硬件负载平衡器要求</span><span class="sxs-lookup"><span data-stu-id="3691b-117">Hardware Load Balancer Requirements for Edge Servers Running the A/V Edge Service</span></span>

<span data-ttu-id="3691b-118">以下是运行 A/V 边缘服务的边缘服务器的硬件负载平衡器要求：</span><span class="sxs-lookup"><span data-stu-id="3691b-118">Following are the hardware load balancer requirements for Edge Servers running the A/V Edge service:</span></span>

  - <span data-ttu-id="3691b-p104">对内部和外部端口 443 关闭 TCP nagling。Nagling 是将若干小数据包整合到单个大数据包以提高传输效率的过程。</span><span class="sxs-lookup"><span data-stu-id="3691b-p104">Turn off TCP nagling for both internal and external ports 443. Nagling is the process of combining several small packets into a single, larger packet for more efficient transmission.</span></span>

  - <span data-ttu-id="3691b-121">对端口范围为 50,000 – 59,999 的外部端口关闭 TCP nagling。</span><span class="sxs-lookup"><span data-stu-id="3691b-121">Turn off TCP nagling for external port range 50,000 – 59,999.</span></span>

  - <span data-ttu-id="3691b-122">请不要对内部或外部防火墙使用 NAT。</span><span class="sxs-lookup"><span data-stu-id="3691b-122">Do not use NAT on the internal or external firewall.</span></span>

  - <span data-ttu-id="3691b-123">Edge 内部接口必须位于不同的网络上，而不是边缘服务器外部接口和必须禁用它们之间的路由。</span><span class="sxs-lookup"><span data-stu-id="3691b-123">The edge internal interface must be on a different network than the Edge Server external interface and routing between them must be disabled.</span></span>

  - <span data-ttu-id="3691b-124">运行 A/V 边缘服务的边缘服务器的外部接口必须使用可公开路由的 IP 地址，并且任何边缘外部 IP 地址上没有 NAT 或端口转换。</span><span class="sxs-lookup"><span data-stu-id="3691b-124">The external interface of the Edge Server running the A/V Edge Service must use publicly routable IP addresses and no NAT or port translation on any of the edge external IP addresses.</span></span>

</div>

<div>

## <a name="hardware-load-balancer-requirements"></a><span data-ttu-id="3691b-125">硬件负载平衡器要求</span><span class="sxs-lookup"><span data-stu-id="3691b-125">Hardware Load Balancer Requirements</span></span>

<span data-ttu-id="3691b-126">在 Lync Server 2013 for Web 服务中，基于 Cookie 的相关性要求大大减少。</span><span class="sxs-lookup"><span data-stu-id="3691b-126">Cookie-based affinity requirements are greatly reduced in Lync Server 2013 for Web services.</span></span> <span data-ttu-id="3691b-127">如果你要部署 Lync Server 2013，并且不会保留任何 Lync Server 2010 前端服务器或前端池，则不需要基于 cookie 的持久性。</span><span class="sxs-lookup"><span data-stu-id="3691b-127">If you are deploying Lync Server 2013 and will not retain any Lync Server 2010 Front End Servers or Front End pools, you do not need cookie-based persistence.</span></span> <span data-ttu-id="3691b-128">但是，如果你将临时或永久保留任何 Lync Server 2010 前端服务器或前端池，你仍然使用基于 cookie 的持久性，因为它是为 Lync Server 2010 部署和配置的。</span><span class="sxs-lookup"><span data-stu-id="3691b-128">However, if you will temporarily or permanently retain any Lync Server 2010 Front End Servers or Front End pools, you still use cookie-based persistence as it is deployed and configured for Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3691b-129"><STRONG>如果您决定使用基于 Cookie 的相关性，但您的部署不需要它</STRONG>，如此做没有任何负面影响。</span><span class="sxs-lookup"><span data-stu-id="3691b-129"><STRONG>If you decide to use cookie-based affinity even though your deployment does not require it</STRONG>, there is no negative impact to doing so.</span></span>



</div>

<span data-ttu-id="3691b-130">对于 **不使用** 基于 Cookie 的相关性的部署：</span><span class="sxs-lookup"><span data-stu-id="3691b-130">For deployments that **will not use** cookie-based affinity:</span></span>

  - <span data-ttu-id="3691b-p106">在端口 4443 的反向代理发布规则上，将“**转发主机头**”设置为 True。这可确保转发原始 URL。</span><span class="sxs-lookup"><span data-stu-id="3691b-p106">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

<span data-ttu-id="3691b-133">对于 **将使用** 基于 Cookie 的相关性的部署：</span><span class="sxs-lookup"><span data-stu-id="3691b-133">For deployments that **will use** cookie-based affinity:</span></span>

  - <span data-ttu-id="3691b-p107">在端口 4443 的反向代理发布规则上，将“**转发主机头**”设置为 True。这可确保转发原始 URL。</span><span class="sxs-lookup"><span data-stu-id="3691b-p107">On the reverse proxy publishing rule for port 4443, set **Forward host header** to True. This will ensure that the original URL is forwarded.</span></span>

  - <span data-ttu-id="3691b-136">不得将硬件负载平衡器 Cookie 标记为 httpOnly</span><span class="sxs-lookup"><span data-stu-id="3691b-136">Hardware load balancer cookie MUST NOT be marked httpOnly</span></span>

  - <span data-ttu-id="3691b-137">硬件负载平衡器 Cookie 不得具有过期时间</span><span class="sxs-lookup"><span data-stu-id="3691b-137">Hardware load balancer cookie MUST NOT have an expiration time</span></span>

  - <span data-ttu-id="3691b-138">硬件负载平衡器 Cookie 必须名为 **MS-WSMAN**（这是 Web 服务预期的值，不能更改）</span><span class="sxs-lookup"><span data-stu-id="3691b-138">Hardware load balancer cookie MUST be named **MS-WSMAN** (This is the value that the Web services expect, and cannot be changed)</span></span>

  - <span data-ttu-id="3691b-p108">必须在其传入 HTTP 请求没有 Cookie 的每个 HTTP 响应中设置硬件负载平衡器 Cookie，无论该同一 TCP 连接上的上一个 HTTP 响应是否已获得 Cookie 都是如此。如果负载平衡器将 Cookie 插入优化为每个 TCP 连接只发生一次，则不得使用该优化</span><span class="sxs-lookup"><span data-stu-id="3691b-p108">Hardware load balancer cookie MUST be set in every HTTP response for which the incoming HTTP request did not have a cookie, regardless of whether a previous HTTP response on that same TCP connection had already obtained a cookie. If the load balancer optimizes cookie insert to only occur once per TCP connection, that optimization MUST NOT be used</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3691b-141">典型的硬件负载平衡器配置使用源地址相关性和20分钟 TCP 会话生存期，这对于 Lync Server 和 Lync 2013 客户端来说非常合适，因为会话状态是通过客户端使用和/或应用程序交互维护的。</span><span class="sxs-lookup"><span data-stu-id="3691b-141">Typical hardware load balancer configurations use source-address affinity and a 20 min. TCP session lifetime, which is fine for Lync Server and Lync 2013 clients because session state is maintained through client usage and/or and application interaction.</span></span>



</div>

<span data-ttu-id="3691b-142">如果部署移动设备，则您的硬件负载平衡器必须能对 TCP 会话中的单个请求进行负载平衡（实际上，您必须能基于目标 IP 地址对单个请求进行负载平衡）。</span><span class="sxs-lookup"><span data-stu-id="3691b-142">If you are deploying mobile devices, your hardware load balancer must be able to load balance individual request within a TCP session (in effect, you must be able to load balance an individual request based on the target IP address).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="3691b-p109">F5 硬件负载平衡器具有一个名为 OneConnect 的功能，这可确保一个 TCP 连接中的每个请求是单独进行负载平衡的。如果部署的是移动设备，请确保您的硬件负载平衡器供应商支持这一相同功能。最新的 Apple iOS 移动应用程序要求传输层安全性 (TLS) 1.2 版。F5 提供专门针对这一要求的设置。</span><span class="sxs-lookup"><span data-stu-id="3691b-p109">F5 hardware load balancers have a feature called OneConnect that ensures each request within a TCP connection is individually load balanced. If you are deploying mobile devices, ensure your hardware load balancer vendor supports the same functionality. The latest Apple iOS mobile apps require Transport Layer Security (TLS) version 1.2. F5 provides specific settings for this.</span></span><BR><span data-ttu-id="3691b-147">有关第三方硬件负载平衡器的详细信息，请参阅 <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span><span class="sxs-lookup"><span data-stu-id="3691b-147">For details on third party hardware load balancers, see <A href="https://go.microsoft.com/fwlink/p/?linkid=230700">https://go.microsoft.com/fwlink/p/?linkId=230700</A></span></span>



</div>

<span data-ttu-id="3691b-148">以下是控制器和前端池 Web 服务的硬件负载平衡器要求：</span><span class="sxs-lookup"><span data-stu-id="3691b-148">Following are the hardware load balancer requirements for Director and Front End pool Web Services:</span></span>

  - <span data-ttu-id="3691b-149">对于内部 Web 服务 Vip，请 \_ 在硬件负载平衡器上设置源地址持久性 (内部端口80、443) 。</span><span class="sxs-lookup"><span data-stu-id="3691b-149">For internal Web Services VIPs, set Source\_addr persistence (internal port 80, 443) on the hardware load balancer.</span></span> <span data-ttu-id="3691b-150">对于 Lync Server 2013，源 \_ 地址持久性意味着来自单个 IP 地址的多个连接始终发送到一台服务器，以维护会话状态。</span><span class="sxs-lookup"><span data-stu-id="3691b-150">For Lync Server 2013, Source\_addr persistence means that multiple connections coming from a single IP address are always sent to one server to maintain session state.</span></span>

  - <span data-ttu-id="3691b-151">使用 TCP 空闲超时 1800 秒。</span><span class="sxs-lookup"><span data-stu-id="3691b-151">Use TCP idle timeout of 1800 seconds.</span></span>

  - <span data-ttu-id="3691b-p111">在反向代理和下一个跃点池的硬件负载平衡器之间的防火墙上，创建一条支持端口 4443 上从反向代理到硬件负载平衡器的 HTTPS 流量的规则。必须将硬件负载平衡器配置为侦听端口 80、443 和 4443。</span><span class="sxs-lookup"><span data-stu-id="3691b-p111">On the firewall between the reverse proxy and the next hop pool’s hardware load balancer, create a rule to allow https: traffic on port 4443, from the reverse proxy to the hardware load balancer. The hardware load balancer must be configured to listen on ports 80, 443, and 4443.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3691b-154">有关硬件负载平衡器配置的进一步阅读，请参阅 <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">端口摘要-在 Lync Server 2013 中通过硬件负载平衡器进行缩放的合并边缘</A>。</span><span class="sxs-lookup"><span data-stu-id="3691b-154">For further reading on configuration of the hardware load balancer, please review <A href="lync-server-2013-port-summary-scaled-consolidated-edge-with-hardware-load-balancers.md">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="summary-of-hardware-load-balancer-affinity-requirements"></a><span data-ttu-id="3691b-155">硬件负载平衡器关联要求的摘要</span><span class="sxs-lookup"><span data-stu-id="3691b-155">Summary of Hardware Load Balancer Affinity Requirements</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3691b-156">客户端/用户位置</span><span class="sxs-lookup"><span data-stu-id="3691b-156">Client/user location</span></span></th>
<th><span data-ttu-id="3691b-157">外部 Web 服务 FQDN 关联要求</span><span class="sxs-lookup"><span data-stu-id="3691b-157">External web services FQDN affinity requirements</span></span></th>
<th><span data-ttu-id="3691b-158">内部 Web 服务 FQDN 关联要求</span><span class="sxs-lookup"><span data-stu-id="3691b-158">Internal web services FQDN affinity requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3691b-159">Lync Web App (内部和外部用户) </span><span class="sxs-lookup"><span data-stu-id="3691b-159">Lync Web App (internal and external users)</span></span></p>
<p><span data-ttu-id="3691b-160">移动设备（内部和外部用户）</span><span class="sxs-lookup"><span data-stu-id="3691b-160">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="3691b-161">无相关性</span><span class="sxs-lookup"><span data-stu-id="3691b-161">No affinity</span></span></p></td>
<td><p><span data-ttu-id="3691b-162">源地址相关性</span><span class="sxs-lookup"><span data-stu-id="3691b-162">Source address affinity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3691b-163">Lync Web App (仅限外部用户) </span><span class="sxs-lookup"><span data-stu-id="3691b-163">Lync Web App (external users only)</span></span></p>
<p><span data-ttu-id="3691b-164">移动设备（内部和外部用户）</span><span class="sxs-lookup"><span data-stu-id="3691b-164">Mobile device (internal and external users)</span></span></p></td>
<td><p><span data-ttu-id="3691b-165">无相关性</span><span class="sxs-lookup"><span data-stu-id="3691b-165">No affinity</span></span></p></td>
<td><p><span data-ttu-id="3691b-166">源地址相关性</span><span class="sxs-lookup"><span data-stu-id="3691b-166">Source address affinity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3691b-167">Lync Web App (仅限内部用户) </span><span class="sxs-lookup"><span data-stu-id="3691b-167">Lync Web App (internal users only)</span></span></p>
<p><span data-ttu-id="3691b-168">移动设备（未部署）</span><span class="sxs-lookup"><span data-stu-id="3691b-168">Mobile device (not deployed)</span></span></p></td>
<td><p><span data-ttu-id="3691b-169">无相关性</span><span class="sxs-lookup"><span data-stu-id="3691b-169">No affinity</span></span></p></td>
<td><p><span data-ttu-id="3691b-170">源地址相关性</span><span class="sxs-lookup"><span data-stu-id="3691b-170">Source address affinity</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="port-monitoring-for-hardware-load-balancers"></a><span data-ttu-id="3691b-171">硬件负载平衡器的端口监控</span><span class="sxs-lookup"><span data-stu-id="3691b-171">Port Monitoring for Hardware Load Balancers</span></span>

<span data-ttu-id="3691b-172">在硬件负载平衡器上定义端口监控来确定特定服务何时由于硬件或通信故障而不再可用。</span><span class="sxs-lookup"><span data-stu-id="3691b-172">You define port monitoring on the hardware load balancers to determine when specific services are no longer available due to hardware or communications failure.</span></span> <span data-ttu-id="3691b-173">例如，如果前端服务器服务 (RTCSRV) 停止，因为前端服务器或前端池出现故障，则 HLB 监视还应停止接收 Web 服务的流量。</span><span class="sxs-lookup"><span data-stu-id="3691b-173">For example, if the Front End Server service (RTCSRV) stops because the Front End Server or Front End pool fails, the HLB monitoring should also stop receiving traffic on the Web Services.</span></span> <span data-ttu-id="3691b-174">可在 HLB 上实施端口监控来监控以下各项：</span><span class="sxs-lookup"><span data-stu-id="3691b-174">You implement port monitoring on the HLB to monitor the following:</span></span>

### <a name="front-end-server-user-pool--hlb-internal-interface"></a><span data-ttu-id="3691b-175">前端服务器用户池-HLB 内部接口</span><span class="sxs-lookup"><span data-stu-id="3691b-175">Front End Server User Pool – HLB Internal Interface</span></span>

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
<th><span data-ttu-id="3691b-176">虚拟 IP/端口</span><span class="sxs-lookup"><span data-stu-id="3691b-176">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="3691b-177">节点端口</span><span class="sxs-lookup"><span data-stu-id="3691b-177">Node Port</span></span></th>
<th><span data-ttu-id="3691b-178">节点计算机/监视器</span><span class="sxs-lookup"><span data-stu-id="3691b-178">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="3691b-179">持久性配置文件</span><span class="sxs-lookup"><span data-stu-id="3691b-179">Persistence Profile</span></span></th>
<th><span data-ttu-id="3691b-180">备注</span><span class="sxs-lookup"><span data-stu-id="3691b-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3691b-181">&lt;池 &gt; web-int_mco_443_vs</span><span class="sxs-lookup"><span data-stu-id="3691b-181">&lt;pool&gt;web-int_mco_443_vs</span></span></p>
<p><span data-ttu-id="3691b-182">443</span><span class="sxs-lookup"><span data-stu-id="3691b-182">443</span></span></p></td>
<td><p><span data-ttu-id="3691b-183">443</span><span class="sxs-lookup"><span data-stu-id="3691b-183">443</span></span></p></td>
<td><p><span data-ttu-id="3691b-184">前端</span><span class="sxs-lookup"><span data-stu-id="3691b-184">Front End</span></span></p>
<p><span data-ttu-id="3691b-185">5061</span><span class="sxs-lookup"><span data-stu-id="3691b-185">5061</span></span></p></td>
<td><p><span data-ttu-id="3691b-186">源</span><span class="sxs-lookup"><span data-stu-id="3691b-186">Source</span></span></p></td>
<td><p><span data-ttu-id="3691b-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="3691b-187">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3691b-188">&lt;池 &gt; web-int_mco_80_vs</span><span class="sxs-lookup"><span data-stu-id="3691b-188">&lt;pool&gt;web-int_mco_80_vs</span></span></p>
<p><span data-ttu-id="3691b-189">80</span><span class="sxs-lookup"><span data-stu-id="3691b-189">80</span></span></p></td>
<td><p><span data-ttu-id="3691b-190">80</span><span class="sxs-lookup"><span data-stu-id="3691b-190">80</span></span></p></td>
<td><p><span data-ttu-id="3691b-191">前端</span><span class="sxs-lookup"><span data-stu-id="3691b-191">Front End</span></span></p>
<p><span data-ttu-id="3691b-192">5061</span><span class="sxs-lookup"><span data-stu-id="3691b-192">5061</span></span></p></td>
<td><p><span data-ttu-id="3691b-193">源</span><span class="sxs-lookup"><span data-stu-id="3691b-193">Source</span></span></p></td>
<td><p><span data-ttu-id="3691b-194">HTTP</span><span class="sxs-lookup"><span data-stu-id="3691b-194">HTTP</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="front-end-server-user-pool--hlb-external-interface"></a><span data-ttu-id="3691b-195">前端服务器用户池-HLB 外部接口</span><span class="sxs-lookup"><span data-stu-id="3691b-195">Front End Server User Pool – HLB External Interface</span></span>

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
<th><span data-ttu-id="3691b-196">虚拟 IP/端口</span><span class="sxs-lookup"><span data-stu-id="3691b-196">Virtual IP/Port</span></span></th>
<th><span data-ttu-id="3691b-197">节点端口</span><span class="sxs-lookup"><span data-stu-id="3691b-197">Node Port</span></span></th>
<th><span data-ttu-id="3691b-198">节点计算机/监视器</span><span class="sxs-lookup"><span data-stu-id="3691b-198">Node Machine/Monitor</span></span></th>
<th><span data-ttu-id="3691b-199">持久性配置文件</span><span class="sxs-lookup"><span data-stu-id="3691b-199">Persistence Profile</span></span></th>
<th><span data-ttu-id="3691b-200">备注</span><span class="sxs-lookup"><span data-stu-id="3691b-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3691b-201">&lt;池 &gt; web_mco_443_vs</span><span class="sxs-lookup"><span data-stu-id="3691b-201">&lt;pool&gt;web_mco_443_vs</span></span></p>
<p><span data-ttu-id="3691b-202">443</span><span class="sxs-lookup"><span data-stu-id="3691b-202">443</span></span></p></td>
<td><p><span data-ttu-id="3691b-203">4443</span><span class="sxs-lookup"><span data-stu-id="3691b-203">4443</span></span></p></td>
<td><p><span data-ttu-id="3691b-204">前端</span><span class="sxs-lookup"><span data-stu-id="3691b-204">Front End</span></span></p>
<p><span data-ttu-id="3691b-205">5061</span><span class="sxs-lookup"><span data-stu-id="3691b-205">5061</span></span></p></td>
<td><p><span data-ttu-id="3691b-206">无</span><span class="sxs-lookup"><span data-stu-id="3691b-206">None</span></span></p></td>
<td><p><span data-ttu-id="3691b-207">HTTPS</span><span class="sxs-lookup"><span data-stu-id="3691b-207">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3691b-208">&lt;池 &gt; web_mco_80_vs</span><span class="sxs-lookup"><span data-stu-id="3691b-208">&lt;pool&gt;web_mco_80_vs</span></span></p>
<p><span data-ttu-id="3691b-209">80</span><span class="sxs-lookup"><span data-stu-id="3691b-209">80</span></span></p></td>
<td><p><span data-ttu-id="3691b-210">8080</span><span class="sxs-lookup"><span data-stu-id="3691b-210">8080</span></span></p></td>
<td><p><span data-ttu-id="3691b-211">前端</span><span class="sxs-lookup"><span data-stu-id="3691b-211">Front End</span></span></p>
<p><span data-ttu-id="3691b-212">5061</span><span class="sxs-lookup"><span data-stu-id="3691b-212">5061</span></span></p></td>
<td><p><span data-ttu-id="3691b-213">无</span><span class="sxs-lookup"><span data-stu-id="3691b-213">None</span></span></p></td>
<td><p><span data-ttu-id="3691b-214">HTTP</span><span class="sxs-lookup"><span data-stu-id="3691b-214">HTTP</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3691b-215">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3691b-215">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

