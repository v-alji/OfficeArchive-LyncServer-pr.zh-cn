---
title: 扩展的控制器池 - DNS 负载平衡和硬件负载平衡器
description: 缩放的控制器池-DNS 负载平衡和硬件负载平衡器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - DNS load balancing and hardware load balancer
ms:assetid: a1f6ffc0-9e6e-4217-a923-025c9679e154
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205142(v=OCS.15)
ms:contentKeyID: 48185023
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b30dfcc3515420ffb34343e4653e9518b1b9c3ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442048"
---
# <a name="scaled-director-pool---dns-load-balancing-and-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="5b1f5-103">Lync Server 2013 中扩展的控制器池 - DNS 负载平衡和硬件负载平衡器</span><span class="sxs-lookup"><span data-stu-id="5b1f5-103">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b1f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b1f5-104">

<span> </span></span></span>

<span data-ttu-id="5b1f5-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="5b1f5-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="5b1f5-106">一个缩放的控制器池，为处理更多容量和提供高可用性而部署了多个控制器，需要负载平衡才能将客户端和服务器通信分配给该池的所有成员。</span><span class="sxs-lookup"><span data-stu-id="5b1f5-106">A scaled Director pool, where there are more than one Director deployed to handle additional capacity and to provide high availability, requires load balancing to distribute client and server communication to all members of the pool.</span></span> <span data-ttu-id="5b1f5-107">控制器承载 web 服务的方式非常类似于前端池。</span><span class="sxs-lookup"><span data-stu-id="5b1f5-107">A Director hosts web services much like a Front End pool.</span></span> <span data-ttu-id="5b1f5-108">若要提供负载平衡，你可以使用硬件负载平衡或域名系统 (DNS) 负载平衡和硬件负载平衡。</span><span class="sxs-lookup"><span data-stu-id="5b1f5-108">To provide the load balancing, you can use either hardware load balancing or domain name system (DNS) load balancing and hardware load balancing.</span></span> <span data-ttu-id="5b1f5-109">对于 web 服务，硬件负载平衡是必需的，并且 DNS 负载平衡本身不提供 web 服务所需的功能。</span><span class="sxs-lookup"><span data-stu-id="5b1f5-109">Hardware load balancing is required for the web services, and DNS load balancing alone does not provide the capabilities required for the web services.</span></span>

<span data-ttu-id="5b1f5-110">以下主题介绍了使用 DNS 负载平衡结合硬件负载平衡来部署控制器池的规划注意事项。</span><span class="sxs-lookup"><span data-stu-id="5b1f5-110">The following topics describe the planning considerations for deploying a Director pool using DNS load balancing in conjunction with hardware load balancing.</span></span> <span data-ttu-id="5b1f5-111">如果你打算使用硬件负载平衡，而不是控制器池的 DNS 负载平衡，请参阅 [Lync Server 2013 中的主题缩放的控制器池-硬件负载平衡器](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) ，描述该拓扑的规划要求。</span><span class="sxs-lookup"><span data-stu-id="5b1f5-111">If you intend to use hardware load balancing, but not DNS load balancing for the Director pool, see the topic [Scaled Director pool - hardware load balancer in Lync Server 2013](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) that describes the planning requirements for that topology.</span></span>

<span data-ttu-id="5b1f5-112">![缩放的控制器池](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "缩放的控制器池")</span><span class="sxs-lookup"><span data-stu-id="5b1f5-112">![Scaled Director Pool](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Scaled Director Pool")</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5b1f5-113">本节内容</span><span class="sxs-lookup"><span data-stu-id="5b1f5-113">In This Section</span></span>

  - [<span data-ttu-id="5b1f5-114">Lync Server 2013 中的证书摘要 - 已进行 DNS 和 HLB 负载平衡</span><span class="sxs-lookup"><span data-stu-id="5b1f5-114">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="5b1f5-115">Lync Server 2013 中的端口摘要 - 已进行 DNS 和 HLB 负载平衡</span><span class="sxs-lookup"><span data-stu-id="5b1f5-115">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-port-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="5b1f5-116">Lync Server 2013 中的 DNS 摘要 - 已进行 DNS 和 HLB 负载平衡</span><span class="sxs-lookup"><span data-stu-id="5b1f5-116">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-dns-summary-dns-and-hlb-load-balanced.md)

<span data-ttu-id="5b1f5-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b1f5-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

