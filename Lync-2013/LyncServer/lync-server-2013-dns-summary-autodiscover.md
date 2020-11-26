---
title: Lync Server 2013： DNS 摘要-自动发现
description: Lync Server 2013： DNS 摘要-自动发现。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Autodiscover
ms:assetid: b336a2ae-0e58-4b74-b606-aedbbd411587
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945644(v=OCS.15)
ms:contentKeyID: 51541504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eef9bd6a2489561145718c7bbf2f710ab0b1f248
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429040"
---
# <a name="dns-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="7a9e3-103">DNS 摘要-Lync Server 2013 中的自动发现</span><span class="sxs-lookup"><span data-stu-id="7a9e3-103">DNS summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a9e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a9e3-104">

<span> </span></span></span>

<span data-ttu-id="7a9e3-105">_**主题上次修改时间：** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="7a9e3-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="7a9e3-106">自动发现是一种灵活的服务，它将通过 HTTP 或 HTTPS 接受通信。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-106">Autodiscover is a flexible service in that it will accept communication over HTTP or HTTPS.</span></span> <span data-ttu-id="7a9e3-107">为此，域名系统 (DNS) ，必须正确配置托管自动发现服务的服务器所使用的证书。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-107">To accomplish this, the domain name system (DNS) and the certificates used by servers that host the Autodiscover service must be configured correctly.</span></span> <span data-ttu-id="7a9e3-108">证书要求在 " [证书摘要-Lync Server 2013 中的自动发现](lync-server-2013-certificate-summary-autodiscover.md)" 中介绍。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-108">Certificate requirements are covered in [Certificate summary - Autodiscover in Lync Server 2013](lync-server-2013-certificate-summary-autodiscover.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7a9e3-109">Lync Server 客户端的 DNS 查找逻辑使用特定的解决方案顺序。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-109">DNS lookup logic for the Lync Server clients uses a specific order of resolution.</span></span> <span data-ttu-id="7a9e3-110">你应始终同时包含 lyncdiscoverinternal。 &lt;域 &gt; 和 lyncdiscover。 &lt;&gt;您的 DNS 中的域。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-110">You should always include both the lyncdiscoverinternal.&lt;domain&gt; and the lyncdiscover.&lt;domain&gt; in your DNS.</span></span> <span data-ttu-id="7a9e3-111">不包括 lyncdiscoverinternal。 &lt;域 &gt; 记录将导致内部客户端无法连接到预期服务或接收不正确的自动发现响应。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-111">Excluding the lyncdiscoverinternal.&lt;domain&gt; record will cause internal clients to fail to connect to the intended services or receive the incorrect Autodiscover response.</span></span>



</div>

### <a name="internal-dns-records"></a><span data-ttu-id="7a9e3-112">内部 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="7a9e3-112">Internal DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a9e3-113">记录类型</span><span class="sxs-lookup"><span data-stu-id="7a9e3-113">Record type</span></span></th>
<th><span data-ttu-id="7a9e3-114">主机名</span><span class="sxs-lookup"><span data-stu-id="7a9e3-114">Host name</span></span></th>
<th><span data-ttu-id="7a9e3-115">解析为</span><span class="sxs-lookup"><span data-stu-id="7a9e3-115">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a9e3-116">CNAME</span><span class="sxs-lookup"><span data-stu-id="7a9e3-116">CNAME</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-117">Lyncdiscoverinternal。 &lt;内部域名&gt;</span><span class="sxs-lookup"><span data-stu-id="7a9e3-117">Lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-118">如果你有控制器池的内部 Web 服务 FQDN，或者如果你没有 Director，则为你的前端池。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-118">Internal Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a9e3-119"> (主机（如果 IPv6） AAAA) </span><span class="sxs-lookup"><span data-stu-id="7a9e3-119">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-120">lyncdiscoverinternal。 &lt;内部域名&gt;</span><span class="sxs-lookup"><span data-stu-id="7a9e3-120">lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-121">内部 Web 服务 IP 地址 (虚拟 IP (VIP) 地址如果你拥有控制器池的负载平衡器) （如果你有），或者如果你没有 Director，则使用前端池。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-121">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a9e3-122">您需要创建下列外部 DNS 记录之一：</span><span class="sxs-lookup"><span data-stu-id="7a9e3-122">You need to create one of the following external DNS records:</span></span>

### <a name="external-dns-records"></a><span data-ttu-id="7a9e3-123">外部 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="7a9e3-123">External DNS Records</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a9e3-124">记录类型</span><span class="sxs-lookup"><span data-stu-id="7a9e3-124">Record type</span></span></th>
<th><span data-ttu-id="7a9e3-125">主机名</span><span class="sxs-lookup"><span data-stu-id="7a9e3-125">Host name</span></span></th>
<th><span data-ttu-id="7a9e3-126">解析为</span><span class="sxs-lookup"><span data-stu-id="7a9e3-126">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a9e3-127">CNAME</span><span class="sxs-lookup"><span data-stu-id="7a9e3-127">CNAME</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-128">lyncdiscover。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="7a9e3-128">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-129">如果你有控制器池的外部 Web 服务 FQDN，或者如果你没有 Director，则为你的前端池。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-129">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a9e3-130"> (主机（如果 IPv6） AAAA) </span><span class="sxs-lookup"><span data-stu-id="7a9e3-130">A (host, if IPv6, AAAA)</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-131">lyncdiscover。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="7a9e3-131">lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="7a9e3-132">反向代理的外部或公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-132">External or public IP address of the reverse proxy.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="7a9e3-133">外部流量通过反向代理。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-133">External traffic goes through the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="7a9e3-134">移动设备客户端不支持多个安全套接字层 (来自不同域的 SSL) 证书。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-134">Mobile device clients do not support multiple Secure Sockets Layer (SSL) certificates from different domains.</span></span> <span data-ttu-id="7a9e3-135">因此，不支持通过 HTTPS 对不同域进行 CNAME 重定向。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-135">Therefore, CNAME redirection to different domains is not supported over HTTPS.</span></span> <span data-ttu-id="7a9e3-136">例如，不支持通过 HTTPS 重定向到 director.contoso.net 地址的 lyncdiscover.contoso.com 的 DNS CNAME 记录。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-136">For example, a DNS CNAME record for lyncdiscover.contoso.com that redirects to an address of director.contoso.net is not supported over HTTPS.</span></span> <span data-ttu-id="7a9e3-137">在此类拓扑中，移动设备客户端需要对第一个请求使用 HTTP，以便 CNAME 重定向通过 HTTP 进行解析。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-137">In such a topology, a mobile device client needs to use HTTP for the first request, so that the CNAME redirection is resolved over HTTP.</span></span> <span data-ttu-id="7a9e3-138">随后的请求将使用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-138">Subsequent requests then use HTTPS.</span></span> <span data-ttu-id="7a9e3-139">若要支持此方案，你需要使用端口 80 (HTTP) 的 web 发布规则配置反向代理。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-139">To support this scenario, you need to configure your reverse proxy with a web publishing rule for port 80 (HTTP).</span></span> <span data-ttu-id="7a9e3-140">有关详细信息，请参阅在 <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Lync Server 2013 中配置反向代理</A>中的 "为端口80创建 web 发布规则"。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-140">For details, see "To create a web publishing rule for port 80" in <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</A>.</span></span> <span data-ttu-id="7a9e3-141">通过 HTTPS 支持到同一域的 CNAME 重定向。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-141">CNAME redirection to the same domain is supported over HTTPS.</span></span> <span data-ttu-id="7a9e3-142">在这种情况下，目标域的证书覆盖了始发域。</span><span class="sxs-lookup"><span data-stu-id="7a9e3-142">In this case, the destination domain's certificate covers the originating domain.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7a9e3-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a9e3-143">See Also</span></span>


[<span data-ttu-id="7a9e3-144">在 Lync Server 2013 中配置反向代理以实现移动功能</span><span class="sxs-lookup"><span data-stu-id="7a9e3-144">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)  


[<span data-ttu-id="7a9e3-145">证书摘要-Lync Server 2013 中的自动发现</span><span class="sxs-lookup"><span data-stu-id="7a9e3-145">Certificate summary - Autodiscover in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-autodiscover.md)  
  

<span data-ttu-id="7a9e3-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a9e3-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

