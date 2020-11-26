---
title: Lync Server 2013：使用公用 IP 地址的单一合并边缘
description: Lync Server 2013：具有公共 IP 地址的单个统一边缘。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Single consolidated edge with public IP addresses
ms:assetid: a92d1179-6a1f-4efe-908a-f8dfc5024f30
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205148(v=OCS.15)
ms:contentKeyID: 48185035
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac829cd15a592a86d2ba5fdfe174703d0c933037
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423850"
---
# <a name="single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="93005-103">Lync Server 2013 中使用公用 IP 地址的单一合并边缘</span><span class="sxs-lookup"><span data-stu-id="93005-103">Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93005-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93005-104">

<span> </span></span></span>

<span data-ttu-id="93005-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="93005-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="93005-106">如果你的组织需要支持少于15000的 Access Edge 服务客户端连接，1000个活动 Lync Server Web 会议服务客户端连接，并且500并发的 A/V 边缘会话以及更高的边缘服务器的可用性不重要，此拓扑提供降低硬件成本和简化部署的优势。</span><span class="sxs-lookup"><span data-stu-id="93005-106">If your organization needs support for fewer than 15,000 Access Edge service client connections, 1,000 active Lync Server Web Conferencing service client connections, and 500 concurrent A/V Edge sessions, and high availability of the Edge Server is not important, this topology offers the advantages of lower hardware cost and simpler deployment.</span></span> <span data-ttu-id="93005-107">如果你需要更大的容量或需要高可用性，你应该部署缩放的合并边缘服务器拓扑。</span><span class="sxs-lookup"><span data-stu-id="93005-107">If you need greater capacity or you require high availability, you should deploy a scaled consolidated Edge Server topology.</span></span>

  - <span></span>  
    [<span data-ttu-id="93005-108">Lync Server 2013 中的扩展的合并边缘（使用 NAT 通过专用 IP 地址进行 DNS 负载平衡）</span><span class="sxs-lookup"><span data-stu-id="93005-108">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - <span></span>  
    [<span data-ttu-id="93005-109">Lync Server 2013 中的扩展的合并边缘（通过公用 IP 地址进行 DNS 负载平衡）</span><span class="sxs-lookup"><span data-stu-id="93005-109">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - <span></span>  
    [<span data-ttu-id="93005-110">Lync Server 2013 中使用硬件负载平衡器的扩展的合并边缘</span><span class="sxs-lookup"><span data-stu-id="93005-110">Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="93005-111">在边缘服务器上使用公共 IP 地址时，边缘服务器上的默认网关不再是你的防火墙或路由器，而是您的公共外围边缘的路由器或防火墙-它将是公共地址。</span><span class="sxs-lookup"><span data-stu-id="93005-111">When using public IP address on the Edge Server, the default gateway on the Edge Server is no longer your firewall or router, but the router or firewall at your public perimeter edge – which will be a public address.</span></span> <span data-ttu-id="93005-112">反向代理继续使用与最外面的外围网络关联的路由器或防火墙。</span><span class="sxs-lookup"><span data-stu-id="93005-112">The reverse proxy continues to use the router or firewall associated with the outermost perimeter network.</span></span> <span data-ttu-id="93005-113">反向代理和边缘服务器与公共 IP 地址之间的区别是反向代理仍在使用 NAT，而边缘服务器使用的是路由关系。</span><span class="sxs-lookup"><span data-stu-id="93005-113">The difference between the reverse proxy and the Edge Server with public IP addresses is that the reverse proxy is still using NAT and the Edge Server is using a route relationship.</span></span>



</div>

<span data-ttu-id="93005-114">该图不显示 Director、在边缘服务器与前端池或服务器之间部署的可选服务器角色。</span><span class="sxs-lookup"><span data-stu-id="93005-114">The figure does not show Directors, an optional server role deployed in the internal network between the Edge Servers and your Front End pools or server.</span></span> <span data-ttu-id="93005-115">有关董事拓扑的详细信息，请参阅 [Lync Server 2013 中的 Director 所需的组件](lync-server-2013-components-required-for-the-director.md)。</span><span class="sxs-lookup"><span data-stu-id="93005-115">For details about the topology for Directors, see [Components required for the Director in Lync Server 2013](lync-server-2013-components-required-for-the-director.md).</span></span> <span data-ttu-id="93005-116">该图表示单个反向代理。</span><span class="sxs-lookup"><span data-stu-id="93005-116">The figure represents a single reverse proxy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="93005-117">所示的图针对方向和示例 IP 寻址，但不打算表示具有正确的传入和传出流量的实际通信流。</span><span class="sxs-lookup"><span data-stu-id="93005-117">The figure shown is for orientation and example IP addressing, but does not intend to represent actual communication flows with the correct incoming and outgoing traffic.</span></span> <span data-ttu-id="93005-118">该图表示可能流量的高级视图。</span><span class="sxs-lookup"><span data-stu-id="93005-118">The figure represents a high level view of possible traffic.</span></span> <span data-ttu-id="93005-119">与侦听端口有关的传入 (的通信流的详细信息，) 和传出 (到目标服务器或客户) 在每个方案的端口摘要图中表示。</span><span class="sxs-lookup"><span data-stu-id="93005-119">Details for traffic flow as they pertain to incoming (to listening ports) and outgoing (to destination servers or clients) is represented in the Port Summary diagram in each scenario.</span></span> <span data-ttu-id="93005-120">例如，TCP 443 实际上是入站或反向代理) 的入站 (，并且只是来自 TCP) 透视的 (协议的双向流。</span><span class="sxs-lookup"><span data-stu-id="93005-120">For example, TCP 443 is actually inbound (to the Edge or reverse proxy) only, and is only a two-way flow from a protocol (TCP) perspective.</span></span> <span data-ttu-id="93005-121">此外，该图显示了当 NAT (网络地址转换) 时发生的流量的本质 (在入站上更改了目标地址时，源地址在出站) 上更改。</span><span class="sxs-lookup"><span data-stu-id="93005-121">Additionally, the figure shows the nature of traffic as it changes when NAT (network address translation) occurs (destination address is changed on inbound, source address is changed on outbound).</span></span> <span data-ttu-id="93005-122">示例外部和内部防火墙以及服务器接口的显示仅供参考之用。</span><span class="sxs-lookup"><span data-stu-id="93005-122">Example external and internal firewall, and server interfaces are shown for reference purposes only.</span></span> <span data-ttu-id="93005-123">最后，显示默认网关和路由关系的示例（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="93005-123">Finally, example default gateway and route relationships are shown, where applicable.</span></span> <span data-ttu-id="93005-124">另请注意，图表使用 <EM>.Com</EM> dns 区域表示反向代理服务器和边缘服务器的外部 DNS 区域，而 <EM>.net</EM> DNS 区域则指内部 DNS 区域。</span><span class="sxs-lookup"><span data-stu-id="93005-124">Note also that the diagram uses the <EM>.com</EM> DNS zone to represent the external DNS zone for both reverse proxy and Edge Servers, and the <EM>.net</EM> DNS zone refers to the internal DNS zone.</span></span>



</div>

<span data-ttu-id="93005-125">Microsoft Lync Server 2013 的新增功能支持 IPv6 寻址。</span><span class="sxs-lookup"><span data-stu-id="93005-125">New to Microsoft Lync Server 2013 is support for IPv6 addressing.</span></span> <span data-ttu-id="93005-126">与 IPv4 寻址非常相似，必须以一种方式分配 IPv6 地址，这些地址是分配的 IPv6 地址空间的一部分。</span><span class="sxs-lookup"><span data-stu-id="93005-126">Much like IPv4 addressing, IPv6 addresses must be assigned in such a way that the addresses are part of your assigned IPv6 address space.</span></span> <span data-ttu-id="93005-127">本主题中的地址仅适用于示例。</span><span class="sxs-lookup"><span data-stu-id="93005-127">The addresses in this topic are for example only.</span></span> <span data-ttu-id="93005-128">你必须获取将在你的部署中运行的 IPv6 地址，提供正确的范围，并将与内部和外部寻址进行互操作。</span><span class="sxs-lookup"><span data-stu-id="93005-128">You must acquire IPv6 addresses that will function in your deployment, provide the correct scope and will interoperate with internal and external addressing.</span></span> <span data-ttu-id="93005-129">Windows Server 提供对过渡的 IPv6 操作和 IPv4 到称为 *双重堆栈* 的 ipv6 通信非常重要的功能。</span><span class="sxs-lookup"><span data-stu-id="93005-129">Windows Server provides a feature that is important to transitional IPv6 operation and IPv4 to IPv6 communication called the *dual stack*.</span></span> <span data-ttu-id="93005-130">双重堆栈是 IPv4 和 IPv6 的单独且独特的网络堆栈。</span><span class="sxs-lookup"><span data-stu-id="93005-130">The dual stack is a separate and distinct network stack for IPv4 and for IPv6.</span></span> <span data-ttu-id="93005-131">双重堆栈使你可以同时为 IPv4 和 IPv6 分配寻址，并允许服务器根据其要求与其他主机和客户端进行通信。</span><span class="sxs-lookup"><span data-stu-id="93005-131">The dual stack is what allows you to assign addressing for IPv4 and IPv6 concurrently, and allows the server to communicate with other hosts and clients based on what their requirements are.</span></span>

<span data-ttu-id="93005-132">用于 IPv6 寻址的典型地址类型将是 IPv6 全局地址， (类似于公用 IPv4 地址) 、IPv6 唯一本地地址 (类似于专用 IPv4 地址范围) 和 IPv6 链接本地地址 (类似于 Windows Server for IPv4 中的自动专用 IP 地址) </span><span class="sxs-lookup"><span data-stu-id="93005-132">Typical address types that you will use for IPv6 addressing will be the IPv6 global addresses (similar to public IPv4 addresses), IPv6 unique local addresses (similar to the private IPv4 address ranges) and IPv6 link-local addresses (similar to automatic private IP addresses in Windows Server for IPv4)</span></span>

<span data-ttu-id="93005-133">网络地址转换技术 (适用于 IPv6 的 NAT) ，这将允许将 NAT IPv6 转换为 IPv4 (通常称为 NAT64) ，对于 NAT IPv6 到 IPv6 (通常称为 NAT66) 。</span><span class="sxs-lookup"><span data-stu-id="93005-133">Network address translation technologies (NAT) for IPv6 exist that will allow for NAT IPv6 to IPv4 (commonly referred to as NAT64) and for NAT IPv6 to IPv6 (commonly referred to as NAT66).</span></span> <span data-ttu-id="93005-134">NAT 技术的存在意味着为 Lync Server Edge 服务器提供的五种方案仍然有效。</span><span class="sxs-lookup"><span data-stu-id="93005-134">The existence of NAT technologies means that the five scenarios presented for Lync Server Edge Servers are still valid.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="93005-135">IPv6 是一个复杂的主题，需要仔细规划网络团队和 Internet 提供商，以确保您在 Windows 服务器级别和 Lync Server 2013 级别分配的地址将按预期工作。</span><span class="sxs-lookup"><span data-stu-id="93005-135">IPv6 is a complex topic and requires careful planning with your networking team and your Internet provider to ensure that the addresses you assign at the Windows server level and at the Lync Server 2013 level will work as expected.</span></span> <span data-ttu-id="93005-136">请参阅本主题结尾处的链接，以了解有关 IPv6 寻址和规划的其他资源。</span><span class="sxs-lookup"><span data-stu-id="93005-136">See the links at the end of this topic for additional resources on IPv6 addressing and planning.</span></span>



</div>

<span data-ttu-id="93005-137">**具有公共 IP 地址拓扑的单个统一边缘**</span><span class="sxs-lookup"><span data-stu-id="93005-137">**Single Consolidated Edge with Public IP Addresses topology**</span></span>

<span data-ttu-id="93005-138">![2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d](images/JJ205148.2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d(OCS.15).jpg "2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d")</span><span class="sxs-lookup"><span data-stu-id="93005-138">![2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d](images/JJ205148.2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d(OCS.15).jpg "2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="93005-139">如果您使用的是 "呼叫许可控制" (CAC) ，仍必须将 IPv4 地址分配给 Edge 服务器内部接口。</span><span class="sxs-lookup"><span data-stu-id="93005-139">If you are using Call Admission Control (CAC), you still must assign IPv4 addresses to the Edge Server internal interface.</span></span> <span data-ttu-id="93005-140">CAC 使用 IPv4 地址，并且必须具有它们才能运行。</span><span class="sxs-lookup"><span data-stu-id="93005-140">CAC uses IPv4 addresses and must have them available to operate.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="93005-141">本节内容</span><span class="sxs-lookup"><span data-stu-id="93005-141">In This Section</span></span>

  - [<span data-ttu-id="93005-142">Lync Server 2013 中的证书摘要 - 使用公用 IP 地址的单一合并边缘</span><span class="sxs-lookup"><span data-stu-id="93005-142">Certificate summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="93005-143">Lync Server 2013 中的端口摘要 - 使用公用 IP 地址的单一合并边缘</span><span class="sxs-lookup"><span data-stu-id="93005-143">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="93005-144">Lync Server 2013 中的证书摘要 - 使用公用 IP 地址的单一合并边缘</span><span class="sxs-lookup"><span data-stu-id="93005-144">DNS summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-public-ip-addresses.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="93005-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="93005-145">See Also</span></span>


[<span data-ttu-id="93005-146">IP 版本6寻址体系结构</span><span class="sxs-lookup"><span data-stu-id="93005-146">IP Version 6 Addressing Architecture</span></span>](https://tools.ietf.org/html/rfc4291)  
[<span data-ttu-id="93005-147">IPv6 全局单播地址格式</span><span class="sxs-lookup"><span data-stu-id="93005-147">IPv6 Global Unicast Address Format</span></span>](https://tools.ietf.org/html/rfc3587)  
[<span data-ttu-id="93005-148">唯一本地 IPv6 单播地址</span><span class="sxs-lookup"><span data-stu-id="93005-148">Unique Local IPv6 Unicast Addresses</span></span>](https://tools.ietf.org/html/rfc4193)  
  

<span data-ttu-id="93005-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93005-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

