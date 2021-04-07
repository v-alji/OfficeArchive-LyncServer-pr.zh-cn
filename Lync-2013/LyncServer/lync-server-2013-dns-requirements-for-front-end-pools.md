---
title: Lync Server 2013：前端池的 DNS 要求
description: Lync Server 2013：前端池的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429068"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="6da17-103">Lync Server 2013 中前端池的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="6da17-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6da17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6da17-104">

<span> </span></span></span>

<span data-ttu-id="6da17-105">_**主题上次修改时间** ：2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="6da17-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="6da17-106">本部分介绍部署前端池 (DNS) 域名系统记录。</span><span class="sxs-lookup"><span data-stu-id="6da17-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="6da17-107">前端池的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="6da17-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="6da17-108">下表指定 Lync Server 2013 前端池部署的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="6da17-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="6da17-109">前端池的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="6da17-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6da17-110">部署方案</span><span class="sxs-lookup"><span data-stu-id="6da17-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="6da17-111">DNS 要求</span><span class="sxs-lookup"><span data-stu-id="6da17-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6da17-112">具有多个前端服务器和硬件负载均衡器 (不管是否在该池上部署了 DNS 负载均衡) </span><span class="sxs-lookup"><span data-stu-id="6da17-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="6da17-113">同时使用 DNS 负载均衡和硬件负载均衡器时，需要将 A (托管) 记录。</span><span class="sxs-lookup"><span data-stu-id="6da17-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="6da17-114">创建内部 A 记录，用于解析前端池的 FQDN (完全限定) DNS 负载均衡。</span><span class="sxs-lookup"><span data-stu-id="6da17-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="6da17-115">创建内部主机 (为) Web 服务创建到负载均衡器虚拟 IP (VIP) 记录。</span><span class="sxs-lookup"><span data-stu-id="6da17-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="6da17-116">必须使用拓扑生成器中定义的内部 Web 服务名称。</span><span class="sxs-lookup"><span data-stu-id="6da17-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="6da17-117">例如，如果同时使用 DNS 负载均衡和硬件负载均衡，则池中每个前端服务器的 A 记录用于 DNS 负载均衡，内部 Web 服务的 A 记录指向硬件负载均衡器虚拟 IP：</span><span class="sxs-lookup"><span data-stu-id="6da17-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="6da17-118">DNS 负载均衡：Pool01.contoso.net 10.10.10.5 的 IP 地址</span><span class="sxs-lookup"><span data-stu-id="6da17-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="6da17-119">每个前端服务器还将有一个不同的 A 记录：</span><span class="sxs-lookup"><span data-stu-id="6da17-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="6da17-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="6da17-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="6da17-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="6da17-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="6da17-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="6da17-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="6da17-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="6da17-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="6da17-124">硬件负载均衡：WebInternal.contoso.net HLB VIP 192.168.10.5 的 IP 地址</span><span class="sxs-lookup"><span data-stu-id="6da17-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="6da17-125">HTTP/HTTPS 流量之外的所有流量都将使用 Pool01.contoso.net 记录。</span><span class="sxs-lookup"><span data-stu-id="6da17-125">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record.</span></span> <span data-ttu-id="6da17-126">HTTP/HTTPS 流量将使用定义的内部 Web 服务地址 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="6da17-126">HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da17-127">部署了 DNS 负载均衡的前端池</span><span class="sxs-lookup"><span data-stu-id="6da17-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="6da17-128">一组内部 A 记录，用于将池的 FQDN 解析为池中每个服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="6da17-129">池中每个服务器必须有一条 A 记录。</span><span class="sxs-lookup"><span data-stu-id="6da17-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da17-130">部署了 DNS 负载均衡的前端池</span><span class="sxs-lookup"><span data-stu-id="6da17-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="6da17-131">一组内部 A 记录，用于将池中每个服务器的 FQDN 解析为该服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="6da17-132">有关详细信息，请参阅规划 <a href="lync-server-2013-dns-load-balancing.md">文档中的 Lync Server 2013</a> 中的 DNS 负载均衡。</span><span class="sxs-lookup"><span data-stu-id="6da17-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da17-133">具有单个前端服务器和专用后端数据库但没有负载均衡器前端池</span><span class="sxs-lookup"><span data-stu-id="6da17-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="6da17-134">内部 A 记录，用于将前端池的 FQDN 解析为单个企业版前端服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da17-135">自动客户端登录</span><span class="sxs-lookup"><span data-stu-id="6da17-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="6da17-136">对于每个支持的 SIP 域，_sipinternaltls._tcp 的 SRV 记录。 &lt;通过端口 5061 的域映射到前端池的 FQDN，该前端池对客户端登录请求进行身份验证和 &gt; 重定向。</span><span class="sxs-lookup"><span data-stu-id="6da17-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="6da17-137">有关详细信息，请参阅 <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013</a>中客户端自动登录的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="6da17-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da17-138">通过统一通信通过统一通信发现 (UC) 设备</span><span class="sxs-lookup"><span data-stu-id="6da17-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="6da17-139">名称为 ucupdates-r2 的内部 A 记录。 &lt;SIP 域，解析为托管设备更新 Web 服务的前端池的 &gt; IP 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="6da17-140">如果 UC 设备已打开，但用户从未登录到该设备，则 A 记录允许设备发现托管设备更新 Web 服务的前端池并获取更新。</span><span class="sxs-lookup"><span data-stu-id="6da17-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="6da17-141">否则，设备在用户首次登录时通过带内预配获取此信息。</span><span class="sxs-lookup"><span data-stu-id="6da17-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="6da17-142">如果您在 Lync Server 2010 中已部署设备更新 Web 服务，则已创建名称为 ucupdates 的内部 A 记录。 &lt;SIP 域 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="6da17-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="6da17-143">对于 Microsoft Office Communications Server 2007 R2，必须创建一个名称为 ucupdates-r2 的其他 DNS A 记录。 &lt;SIP 域 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="6da17-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da17-144">支持 HTTP 流量的反向代理</span><span class="sxs-lookup"><span data-stu-id="6da17-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="6da17-145">外部 A 记录，用于将外部 Web 场 FQDN 解析为反向代理的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="6da17-146">客户端和 UC 设备使用此记录连接到反向代理。</span><span class="sxs-lookup"><span data-stu-id="6da17-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="6da17-147">有关详细信息，请参阅规划文档中的确定 <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013</a> 的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="6da17-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6da17-148">下表显示了内部 Web 场 FQDN 所需的 DNS 记录示例。</span><span class="sxs-lookup"><span data-stu-id="6da17-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="6da17-149">内部 Web 场 FQDN 的示例 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="6da17-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6da17-150">内部 Web 场 FQDN</span><span class="sxs-lookup"><span data-stu-id="6da17-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="6da17-151">池 FQDN</span><span class="sxs-lookup"><span data-stu-id="6da17-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="6da17-152">DNS A 记录 () </span><span class="sxs-lookup"><span data-stu-id="6da17-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6da17-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6da17-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6da17-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6da17-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6da17-155">DNS A 记录 ee-pool.contoso.com 前端服务器使用的负载均衡器 VIP 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="6da17-156">DNS A 记录 webcon.contoso.com 前端服务器使用的负载均衡器 VIP 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da17-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6da17-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6da17-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6da17-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="6da17-159">DNS A 记录 ee-pool.contoso.com，解析为前端池中企业版前端服务器使用的负载均衡器 (VIP) 地址。</span><span class="sxs-lookup"><span data-stu-id="6da17-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="6da17-160">请注意，如果在此池上使用 DNS 负载均衡，则前端池和内部 Web 场不能具有相同的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6da17-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6da17-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6da17-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

