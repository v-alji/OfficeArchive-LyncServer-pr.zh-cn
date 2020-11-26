---
title: Lync Server 2013：DNS 摘要 - 扩展的控制器池、硬件负载平衡器
description: Lync Server 2013： DNS 摘要-已缩放的 Director 池、硬件负载平衡器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled Director pool, hardware load balancer
ms:assetid: 08ba48e6-bfa1-4ab0-bc89-d58ddb9c20af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204655(v=OCS.15)
ms:contentKeyID: 48183340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7198e6a97feed8ce70cb16753ad1f21d58ef246c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428991"
---
# <a name="dns-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="85103-103">Lync Server 2013 中的 DNS 摘要 - 扩展的控制器池、硬件负载平衡器</span><span class="sxs-lookup"><span data-stu-id="85103-103">DNS summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85103-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85103-104">

<span> </span></span></span>

<span data-ttu-id="85103-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="85103-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="85103-106">下表包含支持硬件负载平衡控制器所需的 DNS 记录的摘要。</span><span class="sxs-lookup"><span data-stu-id="85103-106">The following table contains a summary of the DNS records that are required to support the hardware load balanced Director.</span></span> <span data-ttu-id="85103-107">Director 的角色需要类似的 DNS 记录作为前端服务器。</span><span class="sxs-lookup"><span data-stu-id="85103-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="85103-108">所需的记录数反映在 Director 证书所需的主题备用名称中。</span><span class="sxs-lookup"><span data-stu-id="85103-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="85103-109">与前端服务器不同，控制器池不托管用户帐户或托管移动服务。</span><span class="sxs-lookup"><span data-stu-id="85103-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-a-hardware-load-balancer-and-dns-load-balancing"></a><span data-ttu-id="85103-110">使用硬件负载平衡器和 DNS 负载平衡的控制器池所需的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="85103-110">DNS Records Required for the Director pool using a Hardware Load Balancer and DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85103-111">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="85103-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="85103-112">FQDN/DNS 记录</span><span class="sxs-lookup"><span data-stu-id="85103-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="85103-113">IP 地址/FQDN</span><span class="sxs-lookup"><span data-stu-id="85103-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="85103-114">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="85103-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85103-115">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="85103-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="85103-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="85103-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="85103-117">控制器</span><span class="sxs-lookup"><span data-stu-id="85103-117">Director</span></span></p></td>
<td><p><span data-ttu-id="85103-118">用于复制的控制器主机记录和服务器到服务器的通信</span><span class="sxs-lookup"><span data-stu-id="85103-118">Director host record used for replication and server to server communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85103-119">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="85103-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="85103-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="85103-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="85103-121">控制器池 HLB VIP</span><span class="sxs-lookup"><span data-stu-id="85103-121">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="85103-122">用于 DNS 负载平衡控制器池的主机记录</span><span class="sxs-lookup"><span data-stu-id="85103-122">Host record for the DNS load balanced Director pool</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85103-123">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="85103-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="85103-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="85103-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="85103-125">控制器池 HLB VIP</span><span class="sxs-lookup"><span data-stu-id="85103-125">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="85103-126">从边缘服务器的内部接口 (SIP) 的入站会话初始协议</span><span class="sxs-lookup"><span data-stu-id="85103-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85103-127">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="85103-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="85103-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="85103-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="85103-129">控制器池 HLB VIP</span><span class="sxs-lookup"><span data-stu-id="85103-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="85103-130">从反向代理的硬件负载平衡发布的拨入 web 服务</span><span class="sxs-lookup"><span data-stu-id="85103-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85103-131">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="85103-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="85103-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="85103-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="85103-133">控制器池 HLB VIP</span><span class="sxs-lookup"><span data-stu-id="85103-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="85103-134">硬件负载平衡已发布在反向代理中满足 web 服务</span><span class="sxs-lookup"><span data-stu-id="85103-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85103-135">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="85103-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="85103-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="85103-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="85103-137">控制器池 HLB VIP</span><span class="sxs-lookup"><span data-stu-id="85103-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="85103-138">通过 "反向代理 Web 票" 发布和定义的硬件负载平衡控制器池的外部 web 服务</span><span class="sxs-lookup"><span data-stu-id="85103-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="85103-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85103-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

