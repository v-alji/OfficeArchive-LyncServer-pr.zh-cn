---
title: Lync Server 2013：设置边缘服务器的网络接口
description: Lync Server 2013：设置边缘服务器的网络接口。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up network interfaces for Edge Servers
ms:assetid: b0aecdf6-4ae2-46f6-b9b6-948bfc3df11e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412847(v=OCS.15)
ms:contentKeyID: 48185152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 576ca8670a34be022e3df0a699edaf0df10f5b70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441737"
---
# <a name="set-up-network-interfaces-for-edge-servers-in-lync-server-2013"></a><span data-ttu-id="d8831-103">在 Lync Server 2013 中设置边缘服务器的网络接口</span><span class="sxs-lookup"><span data-stu-id="d8831-103">Set up network interfaces for Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8831-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8831-104">

<span> </span></span></span>

<span data-ttu-id="d8831-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="d8831-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="d8831-106">每个边缘服务器都是具有外部接口和内部接口的多宿主计算机。</span><span class="sxs-lookup"><span data-stu-id="d8831-106">Each Edge Server is a multihomed computer with external and internal facing interfaces.</span></span> <span data-ttu-id="d8831-107">适配器域名系统 (DNS) 设置，取决于外围网络中是否存在 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="d8831-107">The adapter Domain Name System (DNS) settings depend on whether there are DNS servers in the perimeter network.</span></span> <span data-ttu-id="d8831-108">如果 DNS 服务器存在于外围，则它们必须具有一个区域，其中包含下一跃点服务器或池 (的一个或多个 DNS A 记录，或者是 Director 或指定的前端池) ，并且对于外部查询，它们引用其他公共 DNS 服务器的名称查找。</span><span class="sxs-lookup"><span data-stu-id="d8831-108">If DNS servers exist in the perimeter, they must have a zone containing one or more DNS A records for the next hop server or pool (that is, either a Director or a designated Front End pool), and for external queries they refer name lookups to other public DNS servers.</span></span> <span data-ttu-id="d8831-109">如果外围设备中不存在任何 DNS 服务器，则 Edge 服务器 (s) 使用外部 DNS 服务器解析 Internet 名称查找，并且每台边缘服务器使用主机将下一个跃点服务器名称解析为 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="d8831-109">If no DNS servers exist in the perimeter, the Edge Server(s) use external DNS servers to resolve Internet name lookups, and each Edge Server uses a HOST to resolve the next hop server names to IP addresses.</span></span>

<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="安全" alt="security" /><span data-ttu-id="d8831-111">安全说明：</span><span class="sxs-lookup"><span data-stu-id="d8831-111">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8831-112">出于安全考虑，我们建议你不要让 Edge 服务器访问位于内部网络中的 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="d8831-112">For security reasons, we recommend that you do not have your Edge Servers access a DNS server located in the internal network.</span></span></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="to-configure-interfaces-with-dns-servers-in-the-perimeter-network"></a><span data-ttu-id="d8831-113">在外围网络中配置具有 DNS 服务器的接口</span><span class="sxs-lookup"><span data-stu-id="d8831-113">To configure interfaces with DNS servers in the perimeter network</span></span>

1.  <span data-ttu-id="d8831-114">为每台边缘服务器安装两个网络适配器，一个用于面向内部的接口，另一个用于面向外部的接口。</span><span class="sxs-lookup"><span data-stu-id="d8831-114">Install two network adapters for each Edge Server, one for the internal-facing interface and one for the external-facing interface.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d8831-115">内部子网和外部子网不得相互路由。</span><span class="sxs-lookup"><span data-stu-id="d8831-115">The internal and external subnets must not be routable to each other.</span></span>

    
    </div>

2.  <span data-ttu-id="d8831-116">在外部接口上，在外部外围网络上配置三个静态 IP 地址 (也称为 DMZ、隔离区域和屏蔽子网) 子网，并将默认网关指向外部防火墙的内部接口。</span><span class="sxs-lookup"><span data-stu-id="d8831-116">On the external interface, configure three static IP addresses on the external perimeter network (also known as DMZ, demilitarized zone, and screened subnet) subnet, and point the default gateway to the internal interface of the external firewall.</span></span> <span data-ttu-id="d8831-117">将适配器 DNS 设置配置为指向一对外围 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="d8831-117">Configure adapter DNS settings to point to a pair of perimeter DNS servers.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d8831-118">可以为此接口使用最少的一个 IP 地址，但要执行此操作，您需要将端口分配更改为非标准值。</span><span class="sxs-lookup"><span data-stu-id="d8831-118">It is possible to use as few as one IP address for this interface, but to do this you need to change the port assignments to non-standard values.</span></span> <span data-ttu-id="d8831-119">在拓扑生成器中创建拓扑时，可以确定此情况。</span><span class="sxs-lookup"><span data-stu-id="d8831-119">You determine this when you create the topology in Topology Builder.</span></span>

    
    </div>

3.  <span data-ttu-id="d8831-120">在内部接口上，在内部外围网络子网中配置一个静态 IP 地址，不要设置默认网关。</span><span class="sxs-lookup"><span data-stu-id="d8831-120">On the internal interface, configure one static IP address on the internal perimeter network subnet and do not set a default gateway.</span></span> <span data-ttu-id="d8831-121">将适配器 DNS 设置配置为指向至少一个 DNS 服务器，最好是一对外围 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="d8831-121">Configure adapter DNS settings to point to at least one DNS server, preferably a pair of perimeter DNS servers.</span></span>

4.  <span data-ttu-id="d8831-122">在内部接口上为客户端、Lync Server 2013 和 Exchange 统一消息 (UM) 服务器所在的所有内部网络创建永久静态路由。</span><span class="sxs-lookup"><span data-stu-id="d8831-122">Create persistent static routes on the internal interface to all internal networks where clients, Lync Server 2013, and Exchange Unified Messaging (UM) servers reside.</span></span>

</div>

<div>

## <a name="to-configure-interfaces-without-dns-servers-in-the-perimeter-network"></a><span data-ttu-id="d8831-123">在外围网络中配置没有 DNS 服务器的接口</span><span class="sxs-lookup"><span data-stu-id="d8831-123">To configure interfaces without DNS servers in the perimeter network</span></span>

1.  <span data-ttu-id="d8831-124">为每台边缘服务器安装两个网络适配器，一个用于面向内部的接口，另一个用于面向外部的接口。</span><span class="sxs-lookup"><span data-stu-id="d8831-124">Install two network adapters for each Edge Server, one for the internal-facing interface and one for the external-facing interface.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d8831-125">内部子网和外部子网不得相互路由。</span><span class="sxs-lookup"><span data-stu-id="d8831-125">The internal and external subnets must not be routable to each other.</span></span>

    
    </div>

2.  <span data-ttu-id="d8831-126">在外部接口上，在外部外围网络子网中配置三个静态 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="d8831-126">On the external interface, configure three static IP addresses on the external perimeter network subnet.</span></span> <span data-ttu-id="d8831-127">您还可以在外部接口上配置默认网关。</span><span class="sxs-lookup"><span data-stu-id="d8831-127">You also configure the default gateway on the external interface.</span></span> <span data-ttu-id="d8831-128">例如，将面向 Internet 的路由器或外部防火墙定义为默认网关。</span><span class="sxs-lookup"><span data-stu-id="d8831-128">For example, define the Internet-facing router or the external firewall as the default gateway.</span></span> <span data-ttu-id="d8831-129">将 DNS 设置配置为指向 DNS 服务器，最好使用一对外部 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="d8831-129">Configure DNS settings to point to a DNS server, preferably to a pair of external DNS servers.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d8831-130">可以使用，但不推荐使用一个 IP 地址作为外部接口。</span><span class="sxs-lookup"><span data-stu-id="d8831-130">It is possible, but not recommended, to use as few as one IP address for the external interface.</span></span> <span data-ttu-id="d8831-131">若要允许此操作，你需要将端口分配更改为非标准值，并离开默认端口443（通常为客户端通信 "防火墙友好"）。</span><span class="sxs-lookup"><span data-stu-id="d8831-131">To allow this to work, you need to change the port assignments to non-standard values, and away from the default port 443 that is typically “firewall friendly” for client communication.</span></span> <span data-ttu-id="d8831-132">在拓扑生成器中创建拓扑时，确定 IP 地址设置和端口设置。</span><span class="sxs-lookup"><span data-stu-id="d8831-132">You determine the IP address setting and the port settings when you create the topology in Topology Builder.</span></span>

    
    </div>

3.  <span data-ttu-id="d8831-133">在内部接口上，在内部外围网络子网中配置一个静态 IP 地址，不要设置默认网关。</span><span class="sxs-lookup"><span data-stu-id="d8831-133">On the internal interface, configure one static IP address on the internal perimeter network subnet and do not set a default gateway.</span></span> <span data-ttu-id="d8831-134">将适配器 DNS 设置保留为空。</span><span class="sxs-lookup"><span data-stu-id="d8831-134">Leave adapter DNS settings empty.</span></span>

4.  <span data-ttu-id="d8831-135">在内部接口上为运行 Lync Server 2013 的 Lync 客户端或服务器所驻留的所有内部网络创建永久静态路由。</span><span class="sxs-lookup"><span data-stu-id="d8831-135">Create persistent static routes on the internal interface to all internal networks where Lync clients or servers running Lync Server 2013 reside.</span></span>

5.  <span data-ttu-id="d8831-136">编辑每台边缘服务器上的主机文件，以包含下一个跃点服务器或虚拟 IP (VIP) 的记录 (该记录将是 Director、标准版服务器或作为边缘服务器的前端池，该服务器已配置为拓扑生成器) 中的下一个跃点地址。</span><span class="sxs-lookup"><span data-stu-id="d8831-136">Edit the HOST file on each Edge Server to contain a record for the next hop server or virtual IP (VIP) (the record will be the Director, Standard Edition server, or a Front End pool that was configured as the Edge Server next hop address in Topology Builder).</span></span> <span data-ttu-id="d8831-137">如果你使用的是 DNS 负载平衡，请为下一个跃点池的每个成员包含一行。</span><span class="sxs-lookup"><span data-stu-id="d8831-137">If you are using DNS load balancing, include a line for each member of the next hop pool.</span></span>

<span data-ttu-id="d8831-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8831-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

