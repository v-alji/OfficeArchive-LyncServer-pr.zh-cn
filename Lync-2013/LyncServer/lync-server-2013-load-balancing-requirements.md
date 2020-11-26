---
title: Lync Server 2013 负载平衡要求
description: Lync Server 2013 负载平衡要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Load balancing requirements
ms:assetid: 84489328-64a4-486c-9384-a3e5c8ed9c8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615011(v=OCS.15)
ms:contentKeyID: 48184697
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a768b2cbfe444e6915c932835d3cc2abaf6a98c3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426562"
---
# <a name="load-balancing-requirements-for-lync-server-2013"></a><span data-ttu-id="e3349-103">Lync Server 2013 的负载平衡要求</span><span class="sxs-lookup"><span data-stu-id="e3349-103">Load balancing requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3349-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3349-104">

<span> </span></span></span>

<span data-ttu-id="e3349-105">_**主题上次修改时间：** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="e3349-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="e3349-106">如果您有前端池、控制器池或边缘服务器池，则需要为这些池部署负载平衡。</span><span class="sxs-lookup"><span data-stu-id="e3349-106">If you have Front End pools, Director pools, or Edge Server pools, you need to deploy load balancing for these pools.</span></span> <span data-ttu-id="e3349-107">负载平衡会将流量分摊到池中的各台服务器上。</span><span class="sxs-lookup"><span data-stu-id="e3349-107">Load balancing distributes the traffic among the servers in a pool.</span></span>

<span data-ttu-id="e3349-108">Lync Server 2013 支持用于客户端到服务器流量的两种类型的负载平衡解决方案：域名系统 (DNS) 负载平衡和硬件负载平衡。</span><span class="sxs-lookup"><span data-stu-id="e3349-108">Lync Server 2013 supports two types of load balancing solutions for client-to-server traffic: Domain Name System (DNS) load balancing and hardware load balancing.</span></span> <span data-ttu-id="e3349-109">DNS 负载平衡提供了多项优势，包括更简单的管理、更高效的故障排除，以及能够隔离许多来自任何潜在硬件负载平衡器问题的 Lync 服务器流量。</span><span class="sxs-lookup"><span data-stu-id="e3349-109">DNS load balancing offers several advantages including simpler administration, more efficient troubleshooting, and the ability to isolate much of your Lync Server traffic from any potential hardware load balancer problems.</span></span>

<span data-ttu-id="e3349-110">在决定哪种负载平衡解决方案适合您部署中的每个池时，请记住以下限制：</span><span class="sxs-lookup"><span data-stu-id="e3349-110">Decide which load balancing solution is appropriate for each pool in your deployment, keeping in mind the following restrictions:</span></span>

  - <span data-ttu-id="e3349-p103">内部边缘接口和外部边缘接口必须使用同一类型的负载平衡。您不能在一个接口上使用 DNS 负载平衡的同时，在另一个接口上使用硬件负载平衡。</span><span class="sxs-lookup"><span data-stu-id="e3349-p103">The internal Edge interface and external Edge interface must use the same type of load balancing. You cannot use DNS load balancing on one interface and hardware load balancing on the other.</span></span>

  - <span data-ttu-id="e3349-p104">某些类型的流量需要硬件负载平衡器。例如，HTTP 流量需要硬件平衡负载器而非 DNS 负载平衡。DNS 负载平衡对客户端到服务器的 Web 流量不起作用。</span><span class="sxs-lookup"><span data-stu-id="e3349-p104">Some types of traffic require a hardware load balancer. For example, HTTP traffic requires a hardware load balancer instead of DNS load balancing. DNS load balancing does not work with client-to-server web traffic.</span></span>

<span data-ttu-id="e3349-116">有关选择硬件负载平衡器解决方案的更多详细信息，请参阅 [Lync Server 2013 的硬件负载平衡器要求](lync-server-2013-hardware-load-balancer-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e3349-116">For more details about choosing a hardware load balancer solution, see [Hardware load balancer requirements for Lync Server 2013](lync-server-2013-hardware-load-balancer-requirements.md).</span></span>

<span data-ttu-id="e3349-117">如果选择对某个池使用 DNS 负载平衡，但仍需对流量（如 HTTP 流量）实现硬件负载平衡器，则会大大简化硬件负载平衡器的管理。</span><span class="sxs-lookup"><span data-stu-id="e3349-117">If you choose to use DNS load balancing for a pool but still need to implement hardware load balancers for traffic such as HTTP traffic, the administration of the hardware load balancers is greatly simplified.</span></span> <span data-ttu-id="e3349-118">例如，配置硬件负载平衡器将更简单，因为它仅管理 HTTP 和 HTTPS 流量，而所有其他协议将由 DNS 负载平衡管理。</span><span class="sxs-lookup"><span data-stu-id="e3349-118">For example, configuring the hardware load balancer will be simpler as it will only manage the HTTP and HTTPS traffic, while all other protocols will be managed by DNS load balancing.</span></span> <span data-ttu-id="e3349-119">有关详细信息，请参阅 [Lync Server 2013 中的 "DNS 负载平衡](lync-server-2013-dns-load-balancing.md)"。</span><span class="sxs-lookup"><span data-stu-id="e3349-119">For details, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md).</span></span>

<span data-ttu-id="e3349-120">对于服务器到服务器的流量，Lync Server 2013 使用拓扑感知负载平衡。</span><span class="sxs-lookup"><span data-stu-id="e3349-120">For server-to-server traffic, Lync Server 2013 uses topology-aware load balancing.</span></span> <span data-ttu-id="e3349-121">服务器在中央管理存储中读取已发布的拓扑，以获取拓扑中服务器的 Fqdn，并自动在服务器之间分配流量。</span><span class="sxs-lookup"><span data-stu-id="e3349-121">Servers read the published topology in the Central Management store to obtain the FQDNs of servers in the topology, and automatically distribute the traffic among the servers.</span></span> <span data-ttu-id="e3349-122">管理员不必设置或管理此类型的负载平衡。</span><span class="sxs-lookup"><span data-stu-id="e3349-122">Administrators do not need to set up or manage this type of load balancing.</span></span>

<span data-ttu-id="e3349-p107">如果使用 DNS 负载平衡并且需要阻止至特定计算机的流量，则仅仅删除池 FQDN 中的 IP 地址条目是不够的。您还必须删除计算机的 DNS 条目。</span><span class="sxs-lookup"><span data-stu-id="e3349-p107">If you use DNS load balancing and you need to block traffic to a specific computer, it is not sufficient to just remove the IP address entries from the Pool FQDN. You must remove the DNS entry for the computer as well.</span></span>

<span data-ttu-id="e3349-125"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3349-125"></div>

<span> </span>

</div>

</div>

</span></span></div>

