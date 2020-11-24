---
title: Lync Server 2013 通配符证书支持
description: Lync Server 2013 通配符证书支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Wildcard certificate support
ms:assetid: 0bae2aa8-b6dc-46f5-a3be-3fe7581809d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202161(v=OCS.15)
ms:contentKeyID: 48183382
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46cc362eb925a86b5e90d51569db6d425ba88fa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392073"
---
# <a name="wildcard-certificate-support-in-lync-server-2013"></a><span data-ttu-id="0b05f-103">Lync Server 2013 中的通配符证书支持</span><span class="sxs-lookup"><span data-stu-id="0b05f-103">Wildcard certificate support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b05f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b05f-104">

<span> </span></span></span>

<span data-ttu-id="0b05f-105">_**主题上次修改时间：** 2013-03-21_</span><span class="sxs-lookup"><span data-stu-id="0b05f-105">_**Topic Last Modified:** 2013-03-21_</span></span>

<span data-ttu-id="0b05f-106">Lync Server 2013 使用证书提供通信加密和服务器身份身份验证。</span><span class="sxs-lookup"><span data-stu-id="0b05f-106">Lync Server 2013 uses certificates to provide communications encryption and server identity authentication.</span></span> <span data-ttu-id="0b05f-107">在某些情况下（例如，通过反向代理的 web 发布），强主题备用名称 (SAN) 条目与完全限定的域名 (FQDN) 提供该服务的服务器 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0b05f-107">In some cases, such as web publishing through the reverse proxy, strong subject alternative name (SAN) entry matching to the fully qualified domain name (FQDN) of the server presenting the service is not required.</span></span> <span data-ttu-id="0b05f-108">在这些情况下，你可以使用带有通配符 SAN 条目的证书 (通常称为 "通配证书" ) 以减少从公共证书颁发机构请求的证书的费用，并降低证书的规划过程的复杂性。</span><span class="sxs-lookup"><span data-stu-id="0b05f-108">In these cases, you can use certificates with wildcard SAN entries (commonly known as “wildcard certificates”) to reduce the cost of a certificate requested from a public certification authority and to reduce the complexity of the planning process for certificates.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="0b05f-109">若要保留统一通信的功能 (UC) 设备 (例如桌面电话) ，应仔细测试部署的证书，以确保设备在你实现通配符证书后正常工作。</span><span class="sxs-lookup"><span data-stu-id="0b05f-109">To retain the functionality of unified communications (UC) devices (for example, desk phones), you should test the deployed certificate carefully to ensure that devices function properly after you implement a wildcard certificate.</span></span>



</div>

<span data-ttu-id="0b05f-110">不支持通配符条目作为主题名称 (也称为公共名称或任何角色的 CN) 。</span><span class="sxs-lookup"><span data-stu-id="0b05f-110">There is no support for a wildcard entry as the subject name (also referred to as the common name or CN) for any role.</span></span> <span data-ttu-id="0b05f-111">在 SAN 中使用通配符条目时，支持以下服务器角色：</span><span class="sxs-lookup"><span data-stu-id="0b05f-111">The following server roles are supported when using wildcard entries in the SAN:</span></span>

  - <span></span>  
    <span data-ttu-id="0b05f-112">**反向代理。**</span><span class="sxs-lookup"><span data-stu-id="0b05f-112">**Reverse proxy.**</span></span>   <span data-ttu-id="0b05f-113">对于简单的 URL， (在) 发布证书时，支持通配符 SAN 条目。</span><span class="sxs-lookup"><span data-stu-id="0b05f-113">Wildcard SAN entry is supported for Simple URL (meet and dialin) publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="0b05f-114">**反向代理。**</span><span class="sxs-lookup"><span data-stu-id="0b05f-114">**Reverse proxy.**</span></span>   <span data-ttu-id="0b05f-115">LyncDiscover 发布证书上的 SAN 条目支持通配符 SAN 条目。</span><span class="sxs-lookup"><span data-stu-id="0b05f-115">Wildcard SAN entry is supported for the SAN entries for LyncDiscover on the publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="0b05f-116">**总监.**</span><span class="sxs-lookup"><span data-stu-id="0b05f-116">**Director.**</span></span>   <span data-ttu-id="0b05f-117">对于简单的 Url， (在) 和在控制器 web 组件中拨入和 LyncDiscoverInternal SAN 条目的简单 Url 中支持通配符 SAN 条目。</span><span class="sxs-lookup"><span data-stu-id="0b05f-117">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Director web components.</span></span>

  - <span></span>  
    <span data-ttu-id="0b05f-118">**前端服务器 (标准版) 和前端池 (企业版) 。**</span><span class="sxs-lookup"><span data-stu-id="0b05f-118">**Front End Server (Standard Edition) and Front End pool (Enterprise Edition).**</span></span> <span data-ttu-id="0b05f-119">对于简单的 Url， (在) 以及前端 web 组件中的 LyncDiscover 和 LyncDiscoverInternal SAN 条目的情况中支持通配符 SAN 条目。</span><span class="sxs-lookup"><span data-stu-id="0b05f-119">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Front End web components.</span></span>

  - <span></span>  
    <span data-ttu-id="0b05f-120">**Exchange 统一消息 (UM) 。**</span><span class="sxs-lookup"><span data-stu-id="0b05f-120">**Exchange Unified Messaging (UM).**</span></span>   <span data-ttu-id="0b05f-121">在作为独立服务器部署时，服务器不使用 SAN 条目。</span><span class="sxs-lookup"><span data-stu-id="0b05f-121">The server does not use SAN entries when deployed as a stand-alone server.</span></span>

  - <span></span>  
    <span data-ttu-id="0b05f-122">**Microsoft Exchange Server 客户端访问服务器。**</span><span class="sxs-lookup"><span data-stu-id="0b05f-122">**Microsoft Exchange Server Client Access server.**</span></span>   <span data-ttu-id="0b05f-123">SAN 中的通配符条目支持内部和外部客户端。</span><span class="sxs-lookup"><span data-stu-id="0b05f-123">Wildcard entries in the SAN are supported for internal and external clients.</span></span>

  - <span></span>  
    <span data-ttu-id="0b05f-124">**Exchange 统一消息 (UM) 和同一台服务器上的 Microsoft Exchange Server 客户端访问服务器。**</span><span class="sxs-lookup"><span data-stu-id="0b05f-124">**Exchange Unified Messaging (UM) and Microsoft Exchange Server Client Access server on same server.**</span></span>   <span data-ttu-id="0b05f-125">支持通配符 SAN 条目。</span><span class="sxs-lookup"><span data-stu-id="0b05f-125">Wildcard SAN entries are supported.</span></span>

<span data-ttu-id="0b05f-126">本主题中未解决的服务器角色：</span><span class="sxs-lookup"><span data-stu-id="0b05f-126">Server roles that are not addressed in this topic:</span></span>

  - <span data-ttu-id="0b05f-127">内部服务器角色 (包括但不限于中介服务器、存档和监视服务器、Survivable 分支装置或 Survivable 分支服务器) </span><span class="sxs-lookup"><span data-stu-id="0b05f-127">Internal server roles (including, but not limited to the Mediation Server, Archiving and Monitoring Server, Survivable Branch Appliance, or Survivable Branch Server)</span></span>

  - <span data-ttu-id="0b05f-128">外部边缘服务器接口</span><span class="sxs-lookup"><span data-stu-id="0b05f-128">External Edge Server interfaces</span></span>

  - <span data-ttu-id="0b05f-129">内部边缘服务器</span><span class="sxs-lookup"><span data-stu-id="0b05f-129">Internal Edge Server</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0b05f-130">对于内部边缘服务器接口，可以将通配符条目分配给 SAN，并且受支持。</span><span class="sxs-lookup"><span data-stu-id="0b05f-130">For the internal Edge Server interface, a wildcard entry can be assigned to the SAN, and is supported.</span></span> <span data-ttu-id="0b05f-131">不会查询内部边缘服务器上的 SAN，并且通配符 SAN 条目的价值有限。</span><span class="sxs-lookup"><span data-stu-id="0b05f-131">The SAN on the internal Edge Server is not queried, and a wildcard SAN entry is of limited value.</span></span>

    
    </div>

<span data-ttu-id="0b05f-132">有关证书配置的详细信息（包括在证书中使用通配符），请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="0b05f-132">For details about certificate configurations, including the use of wildcards in certificates, see the following topics:</span></span>

  - [<span data-ttu-id="0b05f-133">Lync Server 2013 中内部服务器的证书要求</span><span class="sxs-lookup"><span data-stu-id="0b05f-133">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="0b05f-134">Lync Server 2013 中外部用户访问的证书要求</span><span class="sxs-lookup"><span data-stu-id="0b05f-134">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="0b05f-135">Lync Server 2013 中的证书摘要 - 已进行 DNS 和 HLB 负载平衡</span><span class="sxs-lookup"><span data-stu-id="0b05f-135">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="0b05f-136">Lync Server 2013 中的证书摘要 - 单一控制器</span><span class="sxs-lookup"><span data-stu-id="0b05f-136">Certificate summary - Single Director in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-director.md)

  - [<span data-ttu-id="0b05f-137">Lync Server 2013 中的证书摘要 - 扩展的控制器池、硬件负载平衡器</span><span class="sxs-lookup"><span data-stu-id="0b05f-137">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="0b05f-138">Lync Server 2013 中的证书摘要 - 反向代理</span><span class="sxs-lookup"><span data-stu-id="0b05f-138">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="0b05f-139">集成本地统一消息与 Lync Server 2013 的指南</span><span class="sxs-lookup"><span data-stu-id="0b05f-139">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="0b05f-140">有关配置 Exchange 证书的详细信息（包括通配符使用），请参阅 Exchange 2013 产品文档。</span><span class="sxs-lookup"><span data-stu-id="0b05f-140">For details about configuring certificates for Exchange, including the use of wildcards, see the Exchange 2013 product documentation.</span></span>

<span data-ttu-id="0b05f-141"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b05f-141"></div>

<span> </span>

</div>

</div>

</span></span></div>

