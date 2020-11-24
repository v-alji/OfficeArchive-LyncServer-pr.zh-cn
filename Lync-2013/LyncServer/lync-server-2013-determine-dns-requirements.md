---
title: Lync Server 2013：确定 DNS 要求
description: Lync Server 2013：确定 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine DNS requirements
ms:assetid: 95777017-6282-44c0-a685-f246af0501b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398758(v=OCS.15)
ms:contentKeyID: 48184839
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a4bfe682314fa4f91826f4bf85f8eac36ea91d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392354"
---
# <a name="determine-dns-requirements-for-lync-server-2013"></a><span data-ttu-id="65126-103">确定 Lync Server 2013 的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="65126-103">Determine DNS requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65126-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65126-104">

<span> </span></span></span>

<span data-ttu-id="65126-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="65126-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="65126-106">使用以下流程图确定域名系统 (DNS) 要求。</span><span class="sxs-lookup"><span data-stu-id="65126-106">Use the following flow chart to determine Domain Name System (DNS) requirements.</span></span> <span data-ttu-id="65126-107">Lync Server 2013 的累积更新的更改：2月2013的适用位置。</span><span class="sxs-lookup"><span data-stu-id="65126-107">Changes for the Cumulative Updates for Lync Server 2013: February 2013 are noted where they apply.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="65126-108">Microsoft Lync Server 2013 支持使用 IPv6 寻址。</span><span class="sxs-lookup"><span data-stu-id="65126-108">Microsoft Lync Server 2013 supports the use of IPv6 addressing.</span></span> <span data-ttu-id="65126-109">要使用 IPv6 地址，还必须提供 IPv6 DNS 支持和配置 DNS 主机 AAAA（称为“4 A”）记录。</span><span class="sxs-lookup"><span data-stu-id="65126-109">To use IPv6 addresses, you must also provide support for IPv6 DNS and configure DNS host AAAA (known as “quad-A”) records.</span></span> <span data-ttu-id="65126-110">在使用 IPv4 和 IPv6 的部署中，最好为 IPv4 配置和维护 A 记录，并为 IPv6 配置主机 AAAA。</span><span class="sxs-lookup"><span data-stu-id="65126-110">In deployments where both IPv4 and IPv6 are being used, it is best to configure and maintain both host A records for IPv4 and host AAAA for IPv6.</span></span> <span data-ttu-id="65126-111">即使您的部署已完全转换为 IPv6，当外部用户仍在使用 IPv4 时，也仍需要 IPv4 DNS 主机记录。</span><span class="sxs-lookup"><span data-stu-id="65126-111">Even if your deployment has transitioned fully to IPv6, IPv4 DNS host records may still be required when external users are still using IPv4.</span></span>



</div>

<span data-ttu-id="65126-112">**确定 DNS 要求流程图**</span><span class="sxs-lookup"><span data-stu-id="65126-112">**Determining DNS Requirements Flow Chart**</span></span>

<span data-ttu-id="65126-113">![175782ac-363e-408a-912f-8991bf152970](images/Gg398758.175782ac-363e-408a-912f-8991bf152970(OCS.15).jpg "175782ac-363e-408a-912f-8991bf152970")</span><span class="sxs-lookup"><span data-stu-id="65126-113">![175782ac-363e-408a-912f-8991bf152970](images/Gg398758.175782ac-363e-408a-912f-8991bf152970(OCS.15).jpg "175782ac-363e-408a-912f-8991bf152970")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="65126-114">默认情况下，未加入域的计算机的计算机名是主机名，而不是完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="65126-114">By default the computer name of a computer that is not joined to a domain is a host name, not a fully qualified domain name (FQDN).</span></span> <span data-ttu-id="65126-115">拓扑生成器使用 Fqdn，而不是主机名。</span><span class="sxs-lookup"><span data-stu-id="65126-115">Topology Builder uses FQDNs, not host names.</span></span> <span data-ttu-id="65126-116">因此，您必须在要部署为域外边缘服务器的计算机的名称上配置 DNS 后缀。</span><span class="sxs-lookup"><span data-stu-id="65126-116">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="65126-117">分配您的 Lync Server、边缘服务器和池的 FQDN 时，<STRONG>只使用标准字符</STRONG>（包括 A–Z、a–z、0–9 和连字符）。</span><span class="sxs-lookup"><span data-stu-id="65126-117"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="65126-118">不要使用 Unicode 字符或下划线。</span><span class="sxs-lookup"><span data-stu-id="65126-118">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="65126-119">外部 DNS 和公共 CA（即，在 FQDN 必须分配给证书中的 SN 时）通常不支持在 FQDN 中使用非标准字符。</span><span class="sxs-lookup"><span data-stu-id="65126-119">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (that is, when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="65126-120">有关其他详细信息，请参阅 <A href="lync-server-2013-configure-dns-host-records.md">为 Lync Server 2013 配置 DNS 主机记录</A></span><span class="sxs-lookup"><span data-stu-id="65126-120">For additional details, see <A href="lync-server-2013-configure-dns-host-records.md">Configure DNS Host records for Lync Server 2013</A></span></span>



</div>

<div>

## <a name="how-lync-clients-locate-services"></a><span data-ttu-id="65126-121">Lync 客户端如何查找服务</span><span class="sxs-lookup"><span data-stu-id="65126-121">How Lync Clients Locate Services</span></span>

<span data-ttu-id="65126-122">Microsoft Lync 2010、Lync 2013 和 Lync Mobile 与客户在 Lync Server 2013 中查找和访问服务的方式类似。</span><span class="sxs-lookup"><span data-stu-id="65126-122">Microsoft Lync 2010, Lync 2013, and Lync Mobile are similar in how the client finds and accesses services in Lync Server 2013.</span></span> <span data-ttu-id="65126-123">显著的例外是使用不同服务位置进程的 Lync Windows 应用商店应用。</span><span class="sxs-lookup"><span data-stu-id="65126-123">The notable exception is the Lync Windows Store app that uses a different service location process.</span></span> <span data-ttu-id="65126-124">本节详细介绍客户端定位服务的两种方案，第一种为传统方法，使用一系列 SRV 和 A 主机记录，第二种只使用自动发现服务记录。</span><span class="sxs-lookup"><span data-stu-id="65126-124">This section details two scenarios of how the clients locate services, first the traditional method using a series of SRV and A host records, second using only the Autodiscover service records.</span></span> <span data-ttu-id="65126-125">对桌面客户端的累积更新从 Lync Server 2010 更改所有客户端的 DNS 位置过程，DNS 查询过程将继续，直到返回成功的查询，或者可能的 DNS 记录的列表已用尽，最后一个错误将返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="65126-125">Cumulative updates to the desktop clients change the DNS location process from Lync Server 2010 For all clients, the DNS query process continues until a successful query is returned, or the list of possible DNS records is exhausted, and the final error is returned to the client.</span></span>

<span data-ttu-id="65126-126">对于在 DNS 查找期间除 Lync Windows 应用商店应用 **之外** 的所有客户端，将按以下顺序查询和返回到客户端的 SRV 记录：</span><span class="sxs-lookup"><span data-stu-id="65126-126">For all clients **except** for the Lync Windows Store app During DNS lookup, SRV records are queried and returned to the client in the following order:</span></span>

1.  <span data-ttu-id="65126-127">lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-127">lyncdiscoverinternal.\<domain\></span></span>   <span data-ttu-id="65126-128">内部 Web 服务上的自动发现服务的 (主机) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-128">A (host) record for the Autodiscover service on the internal Web services</span></span>

2.  <span data-ttu-id="65126-129">lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-129">lyncdiscover.\<domain\></span></span>   <span data-ttu-id="65126-130">外部 Web 服务上的自动发现服务的 (主机) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-130">A (host) record for the Autodiscover service on the external Web services</span></span>

3.  <span data-ttu-id="65126-131">\_sipinternaltls。 \_tcp-out.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-131">\_sipinternaltls.\_tcp.\<domain\></span></span>   <span data-ttu-id="65126-132">用于内部 TLS 连接的 SRV (服务定位器) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-132">SRV (service locator) record for internal TLS connections</span></span>

4.  <span data-ttu-id="65126-133">\_sipinternal。 \_tcp-out.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-133">\_sipinternal.\_tcp.\<domain\></span></span>   <span data-ttu-id="65126-134">SRV (服务定位器) 内部 TCP 连接的记录 (仅在允许 TCP 的情况中执行) </span><span class="sxs-lookup"><span data-stu-id="65126-134">SRV (service locator) record for internal TCP connections (performed only if TCP is allowed)</span></span>

5.  <span data-ttu-id="65126-135">\_sip。 \_采用.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-135">\_sip.\_tls.\<domain\></span></span>   <span data-ttu-id="65126-136">用于外部 TLS 连接的 SRV (服务定位器) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-136">SRV (service locator) record for external TLS connections</span></span>

6.  <span data-ttu-id="65126-137">sipinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-137">sipinternal.\<domain\></span></span>   <span data-ttu-id="65126-138">前端池或控制器的 (主机) 记录，仅在内部网络上可解析</span><span class="sxs-lookup"><span data-stu-id="65126-138">A (host) record for the Front End pool or Director, resolvable only on the internal network</span></span>

7.  <span data-ttu-id="65126-139">sip.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-139">sip.\<domain\></span></span>   <span data-ttu-id="65126-140">在客户端为外部网络上的前端池或控制器的 (主机) 记录，或者当客户端为外部客户端时的访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="65126-140">A (host) record for the Front End pool or Director on the internal network, or the Access Edge service when the client is external</span></span>

8.  <span data-ttu-id="65126-141">sipexternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-141">sipexternal.\<domain\></span></span>   <span data-ttu-id="65126-142">当客户端为外部客户端时，为 Access Edge 服务 (主机) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-142">A (host) record for the Access Edge service when the client is external</span></span>

<span data-ttu-id="65126-143">Lync Windows 应用商店应用将完全更改该过程，因为它使用两个记录：</span><span class="sxs-lookup"><span data-stu-id="65126-143">The Lync Windows Store app changes the process completely because it uses two records:</span></span>

1.  <span data-ttu-id="65126-144">lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-144">lyncdiscoverinternal.\<domain\></span></span>   <span data-ttu-id="65126-145">内部 Web 服务上的自动发现服务的 (主机) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-145">A (host) record for the Autodiscover service on the internal Web services</span></span>

2.  <span data-ttu-id="65126-146">lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="65126-146">lyncdiscover.\<domain\></span></span>   <span data-ttu-id="65126-147">外部 Web 服务上的自动发现服务的 (主机) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-147">A (host) record for the Autodiscover service on the external Web services</span></span>

<span data-ttu-id="65126-148">不回退到其他记录类型。</span><span class="sxs-lookup"><span data-stu-id="65126-148">There is no fallback to the other record types.</span></span>

<span data-ttu-id="65126-149">用于较新客户端和较旧客户端的方法的区别在于，自动发现服务将成为定位所有服务的首选方法。</span><span class="sxs-lookup"><span data-stu-id="65126-149">The difference between the methods used for newer clients as compared to older clients is that the Autodiscover service is becoming the preferred method to locate all services.</span></span>

<span data-ttu-id="65126-150">连接成功后，自动发现服务将返回用户的主池的所有 Web 服务 Url，包括移动服务 (称为 Mcx 由在 IIS) 、Microsoft Lync Web App 和 Web 计划程序 Url 中为该服务创建的虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="65126-150">When a connection is successful, the Autodiscover Service returns all the Web Services URLs for the user's home pool, including the Mobility Service (known as Mcx by the virtual directory created for the service in IIS), Microsoft Lync Web App and Web scheduler URLs.</span></span> <span data-ttu-id="65126-151">但是，内部 Mobility Service URL 和外部 Mobility Service URL 都与外部 Web 服务 FQDN 关联。</span><span class="sxs-lookup"><span data-stu-id="65126-151">However, both the internal Mobility Service URL and the external Mobility Service URL is associated with the external Web Services FQDN.</span></span> <span data-ttu-id="65126-152">因此，不管移动设备是在网络内部还是外部，该设备都始终从外部通过反向代理连接到 Mobility Service。</span><span class="sxs-lookup"><span data-stu-id="65126-152">Therefore, regardless of whether a mobile device is internal or external to the network, the device always connects to the Mobility Service externally through the reverse proxy.</span></span>

<span data-ttu-id="65126-153">如果 Lync Server 2013 的累积更新：已安装2月2013，则自动发现服务还返回对 Internal/UCWA、External/UCWA 和 UCWA 的引用。</span><span class="sxs-lookup"><span data-stu-id="65126-153">If the Cumulative Updates for Lync Server 2013: February 2013 has been installed, the Autodiscover Service also returns references to Internal/UCWA, External/UCWA and UCWA.</span></span> <span data-ttu-id="65126-154">这些条目是指统一通信 Web API (UCWA) Web 组件。</span><span class="sxs-lookup"><span data-stu-id="65126-154">These entries refer to the Unified Communications Web API (UCWA) web component.</span></span> <span data-ttu-id="65126-155">目前，只使用条目 UCWA，它提供对该 Web 组件 URL 的引用。</span><span class="sxs-lookup"><span data-stu-id="65126-155">Currently, only the entry UCWA is used and provides a reference to a URL for the web component.</span></span> <span data-ttu-id="65126-156">UCWA 由 Lync 2013 移动客户端使用，而不是 Lync 2010 移动客户端使用的 Mcx 移动服务。</span><span class="sxs-lookup"><span data-stu-id="65126-156">UCWA is used by Lync 2013 Mobile clients instead of the Mcx Mobility Service used by the Lync 2010 Mobile clients.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="65126-157">创建 SRV 记录时，请务必记住，这些记录必须指向在其中创建了 DNS SRV 记录的同一域中的 DNS A 和 AAAA（如果您使用的是 IPv6 寻址）记录。</span><span class="sxs-lookup"><span data-stu-id="65126-157">When creating SRV records, it is important to remember that they must point to a DNS A and AAAA (if you are using IPv6 addressing) record in the same domain in which the DNS SRV record is created.</span></span> <span data-ttu-id="65126-158">例如，如果 SRV 记录在 contoso.com 中，则 A 和 AAAA (如果你使用的是 IPv6 寻址) 记录其指向的不能在 fabrikam.com 中。</span><span class="sxs-lookup"><span data-stu-id="65126-158">For example, if the SRV record is in contoso.com, the A and AAAA (if you are using IPv6 addressing) record it points to cannot be in fabrikam.com.</span></span>



</div>

<div>


> [!TIP]  
> <span data-ttu-id="65126-159">默认配置是使所有移动客户端流量通过外部网站。</span><span class="sxs-lookup"><span data-stu-id="65126-159">The default configuration is to direct all mobile client traffic through the external site.</span></span> <span data-ttu-id="65126-160">您可以修改设置，以便仅返回内部 URL（如果这更符合您的需求）。</span><span class="sxs-lookup"><span data-stu-id="65126-160">You can modify settings to return only the internal URL, if this is more preferable for your requirements.</span></span> <span data-ttu-id="65126-161">在此配置下，仅当用户位于企业网络内部时才能在其移动设备上使用 Lync 移动应用程序。</span><span class="sxs-lookup"><span data-stu-id="65126-161">With this configuration, users can use Lync mobile applications on their mobile devices only when they are inside the corporate network.</span></span> <span data-ttu-id="65126-162">若要定义此配置，需要使用 <STRONG>Set-CsMcxConfiguration</STRONG> cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65126-162">To define this configuration, you use the <STRONG>Set-CsMcxConfiguration</STRONG> cmdlet.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="65126-163">虽然移动应用程序也可以连接到其他 Lync Server 2013 服务（如通讯簿服务），但内部移动应用程序 web 请求仅转到移动服务的外部 web FQDN。</span><span class="sxs-lookup"><span data-stu-id="65126-163">Although mobile applications can also connect to other Lync Server 2013 services, such as Address Book Service, internal mobile application web requests go to the external web FQDN only for the Mobility Service.</span></span> <span data-ttu-id="65126-164">其他服务请求（如通讯簿请求）不需要此配置。</span><span class="sxs-lookup"><span data-stu-id="65126-164">Other service requests, such as Address Book requests, do not require this configuration.</span></span>



</div>

<span data-ttu-id="65126-p120">移动设备支持手动发现服务。在此情况下，每个用户必须使用整个内部和外部自动发现服务 URI（包括协议和路径）配置移动设备设置，如下所示：</span><span class="sxs-lookup"><span data-stu-id="65126-p120">Mobile devices support manual discovery of services. In this case, each user must configure the mobile device settings with the full internal and external Autodiscover Service URIs, including the protocol and path, as follows:</span></span>

  - <span data-ttu-id="65126-167"> https:// \<ExtPoolFQDN\> /Autodiscover/autodiscoverservice.svc/Root 用于外部访问</span><span class="sxs-lookup"><span data-stu-id="65126-167">https://\<ExtPoolFQDN\>/Autodiscover/autodiscoverservice.svc/Root for external access</span></span>

  - <span data-ttu-id="65126-168"> https:// \<IntPoolFQDN\> /AutoDiscover/AutoDiscover.svc/Root 用于内部访问</span><span class="sxs-lookup"><span data-stu-id="65126-168">https://\<IntPoolFQDN\>/AutoDiscover/AutoDiscover.svc/Root for internal access</span></span>

<span data-ttu-id="65126-169">建议使用自动发现而非手动发现。</span><span class="sxs-lookup"><span data-stu-id="65126-169">We recommend that you use automatic discovery, rather than manual discovery.</span></span> <span data-ttu-id="65126-170">但是，手动设置对解决移动设备连接问题很有用。</span><span class="sxs-lookup"><span data-stu-id="65126-170">However, manual settings can be useful for troubleshooting mobile device connectivity issues.</span></span>

</div>

<div>

## <a name="configuring-split-brain-dns-with-lync-server"></a><span data-ttu-id="65126-171">配置 Lync Server Split-Brain DNS</span><span class="sxs-lookup"><span data-stu-id="65126-171">Configuring Split-Brain DNS with Lync Server</span></span>

<span data-ttu-id="65126-p122">拆分式 DNS 以名称编号得名，例如，拆分 DNS 或水平拆分 DNS。它仅仅描述其中具有相同命名空间的两个 DNS 区域（其中一个 DNS 区域仅为内部请求提供服务，而另一个 DNS 区域仅为外部请求提供服务）的 DNS 配置。但是，内部 DNS 所包含的许多 DNS SRV 和 A 记录不包含在外部 DNS 中，反之亦然。如果内部和外部 DNS 中存在相同的 DNS 记录（例如，www.contoso.com），则根据启动 DNS 查询的位置（内部或外部）不同，返回的 IP 地址也将不同。</span><span class="sxs-lookup"><span data-stu-id="65126-p122">Split-brain DNS is known by a number of names, for example, split DNS or split-horizon DNS. Simply, it describes a DNS configuration where there are two DNS zones with the same namespace – but one DNS zone services internal-only requests, and the other DNS zone services external-only requests. However, many of the DNS SRV and A records contained in the internal DNS will not be contained in the external DNS, and the reverse is also true. In cases where the same DNS record exists in both the internal and external DNS (for example, www.contoso.com), the IP address returned will be different based on where (internal or external) the query was initiated.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="65126-p123">当前，移动性（或者更具体讲，LyncDiscover 和 LyncDiscoverInternal DNS 记录）不支持拆分式 DNS。必须在外部 DNS 服务器上定义 LyncDiscover，在内部 DNS 服务器上定义 LyncDiscoverInternal。</span><span class="sxs-lookup"><span data-stu-id="65126-p123">Currently, Split-Brain DNS is not supported for the mobility, or more specifically, the LyncDiscover and LyncDiscoverInternal DNS records. LyncDiscover must be defined on an external DNS server and LyncDiscoverInternal must be defined on an internal DNS server.</span></span>



</div>

<span data-ttu-id="65126-178">出于这些主题的目的，将使用术语“拆分式 DNS”。</span><span class="sxs-lookup"><span data-stu-id="65126-178">For the purposes of these topics, the term split-brain DNS will be used.</span></span>

<span data-ttu-id="65126-179">如果要配置拆分式 DNS，以下内部和外部区域包含每个区域所需的 DNS 记录类型的摘要。</span><span class="sxs-lookup"><span data-stu-id="65126-179">If you are configuring split-brain DNS, the following internal and external zone contain a summary of the types of DNS records required in each zone.</span></span> <span data-ttu-id="65126-180">有关详细信息，请参阅 [Lync Server 2013 中的外部用户访问方案](lync-server-2013-scenarios-for-external-user-access.md)。</span><span class="sxs-lookup"><span data-stu-id="65126-180">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="65126-181">**内部 DNS：**</span><span class="sxs-lookup"><span data-stu-id="65126-181">**Internal DNS:**</span></span>

  - <span data-ttu-id="65126-182">包含名为 contoso.com 且受其管辖的 DNS 区域</span><span class="sxs-lookup"><span data-stu-id="65126-182">Contains a DNS zone called contoso.com for which it is authoritative</span></span>

  - <span data-ttu-id="65126-183">内部 contoso.com 区域包含：</span><span class="sxs-lookup"><span data-stu-id="65126-183">The internal contoso.com zone contains:</span></span>
    
      - <span data-ttu-id="65126-184">DNS A 和 AAAA (如果你使用 IPv6 寻址) 和用于内部 Lync Server 2013 客户端自动配置的 SRV 记录 (可选) </span><span class="sxs-lookup"><span data-stu-id="65126-184">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for internal Lync Server 2013 client autoconfiguration (optional)</span></span>
    
      - <span data-ttu-id="65126-185">DNS A 和 AAAA (如果你使用 IPv6 寻址) 或用于自动发现 Lync Server 2013 Web 服务的 CNAME 记录 (可选) </span><span class="sxs-lookup"><span data-stu-id="65126-185">DNS A and AAAA (if you are using IPv6 addressing) or CNAME records for automatic discovery of Lync Server 2013 Web Services (optional)</span></span>
    
      - <span data-ttu-id="65126-186">DNS A 和 AAAA (如果你使用的是用于在企业网络中运行 Lync Server 2013 的所有内部服务器的 IPv6 寻址) 记录，则为 "Director" 或 "Director" 池名称</span><span class="sxs-lookup"><span data-stu-id="65126-186">DNS A and AAAA (if you are using IPv6 addressing) records for Front End pool name, Director or Director pool name, and all internal servers running Lync Server 2013 in the corporate network</span></span>
    
      - <span data-ttu-id="65126-187">DNS A 和 AAAA (如果你对外围网络中每个 Lync Server 2013 和 Edge 服务器的边际内部接口使用 IPv6 寻址) 记录</span><span class="sxs-lookup"><span data-stu-id="65126-187">DNS A and AAAA (if you are using IPv6 addressing) records for the Edge internal interface of each Lync Server 2013, Edge Server in the perimeter network</span></span>
    
      - <span data-ttu-id="65126-188">外围网络中每台反向代理服务器的内部接口的 DNS A 和 AAAA（如果使用的是 IPv6 寻址）记录（仅对反向代理的管理是可选的）</span><span class="sxs-lookup"><span data-stu-id="65126-188">DNS A and AAAA (if you are using IPv6 addressing) records for the internal interface of each reverse proxy server in the perimeter network (optional for management of reverse proxy)</span></span>
    
      - <span data-ttu-id="65126-189">外围网络中的所有 Lync Server 2013 Edge 服务器内部边缘接口使用内部 DNS 区域将查询解析为 contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-189">All Lync Server 2013  Edge Server internal edge interfaces in the perimeter network use the internal DNS zone for resolving queries to contoso.com</span></span>
    
      - <span data-ttu-id="65126-190">运行 Lync Server 2013 和运行 Lync 2013 的客户端在企业网络中的所有服务器指向内部 DNS 服务器，以便将查询解析到 contoso.com，或在每台边缘服务器上使用 HOSTS 文件，并列出 A 和 AAAA (如果你使用 IPv6 寻址) 下一个跃点服务器的记录，特别是 Director 或 Director VIP、前端池 VIP 或标准版服务器</span><span class="sxs-lookup"><span data-stu-id="65126-190">All servers running Lync Server 2013 and clients running Lync 2013 in the corporate network point to the internal DNS servers for resolving queries to contoso.com, or use of HOSTS file on each Edge server and list A and AAAA (if you are using IPv6 addressing) records for next hop server, specifically the Director or Director VIP, Front End pool VIP, or Standard Edition server</span></span>

<span data-ttu-id="65126-191">**外部 DNS：**</span><span class="sxs-lookup"><span data-stu-id="65126-191">**External DNS:**</span></span>

  - <span data-ttu-id="65126-192">包含名为 contoso.com 且受其管辖的 DNS 区域</span><span class="sxs-lookup"><span data-stu-id="65126-192">Contains a DNS zone called contoso.com for which it is authoritative</span></span>

  - <span data-ttu-id="65126-193">外部 contoso.com 区域包含：</span><span class="sxs-lookup"><span data-stu-id="65126-193">The external contoso.com zone contains:</span></span>
    
      - <span data-ttu-id="65126-194">DNS A 和 AAAA (如果使用的是 IPv6 寻址) 和 Lync Server 2013 客户端自动配置的 SRV 记录 (可选) </span><span class="sxs-lookup"><span data-stu-id="65126-194">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for Lync Server 2013 client autoconfiguration (optional)</span></span>
    
      - <span data-ttu-id="65126-195">DNS A 和 AAAA (如果你使用 IPv6 寻址) 或 CNAME 记录自动发现 Lync Server 2013 Web 服务以供移动使用</span><span class="sxs-lookup"><span data-stu-id="65126-195">DNS A and AAAA (if you are using IPv6 addressing) or CNAME records for automatic discovery of Lync Server 2013 Web Services for use with mobility</span></span>
    
      - <span data-ttu-id="65126-196">DNS A 和 AAAA (如果你使用 IPv6 寻址) 和 SRV 记录，了解每个 Lync Server 2013、Edge 服务器或外围网络中的硬件负载平衡器虚拟 IP (VIP) </span><span class="sxs-lookup"><span data-stu-id="65126-196">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for the Edge external interface of each Lync Server 2013, Edge Server or hardware load balancer virtual IP (VIP) in the perimeter network</span></span>
    
      - <span data-ttu-id="65126-197">外围网络中反向代理服务器的外部接口的 DNS A 和 AAAA（如果使用的是 IPv6 寻址）记录或反向代理服务器池的 VIP</span><span class="sxs-lookup"><span data-stu-id="65126-197">DNS A and AAAA (if you are using IPv6 addressing) records for the external interface of the reverse proxy server or VIP for a pool of reverse proxy servers in the perimeter network</span></span>

</div>

<div>

## <a name="automatic-configuration-without-split-brain-dns"></a><span data-ttu-id="65126-198">没有拆分式 DNS 时的自动配置</span><span class="sxs-lookup"><span data-stu-id="65126-198">Automatic Configuration without Split-Brain DNS</span></span>

<span data-ttu-id="65126-199">如果内部 DNS 区域包含 sipinternaltls，则使用 "分裂" DNS，登录内部的 Lync Server 2013 用户可以利用自动配置 \_ 。 \_正在使用的每个 SIP 域的 tcp SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="65126-199">Using split-brain DNS, a Lync Server 2013 user that signs in internally can take advantage of automatic configuration if the internal DNS zone contains a \_sipinternaltls.\_tcp SRV record for each SIP domain in use.</span></span> <span data-ttu-id="65126-200">但是，如果您不使用分裂的 DNS，则运行 Lync 的客户端的内部自动配置将不起作用，除非实施本部分后面部分中所述的解决方法之一。</span><span class="sxs-lookup"><span data-stu-id="65126-200">However, if you do not use split-brain DNS, internal automatic configuration of clients running Lync will not work unless one of the workarounds described in later in this section is implemented.</span></span> <span data-ttu-id="65126-201">这是因为 Lync Server 2013 要求用户的 SIP URI 与为自动配置指定的前端池的域匹配。</span><span class="sxs-lookup"><span data-stu-id="65126-201">This is because Lync Server 2013 requires the user’s SIP URI to match the domain of the Front End pool designated for automatic configuration.</span></span> <span data-ttu-id="65126-202">这也是早期版本的 Communicator 的情况。</span><span class="sxs-lookup"><span data-stu-id="65126-202">This was also the case with earlier versions of Communicator.</span></span>

<span data-ttu-id="65126-203">例如，如果正在使用两个 SIP 域，则需要以下 DNS 服务 (SRV) 记录：</span><span class="sxs-lookup"><span data-stu-id="65126-203">For example, if you have two SIP domains in use, the following DNS service (SRV) records would be required:</span></span>

  - <span data-ttu-id="65126-204">如果用户使用 bob@contoso.com 登录，由于用户的 SIP 域 (contoso.com) 与自动配置前端池的域相匹配，因此，以下 SRV 记录将用于自动配置：</span><span class="sxs-lookup"><span data-stu-id="65126-204">If a user signs in as bob@contoso.com the following SRV record will work for automatic configuration because the user’s SIP domain (contoso.com) matches the domain of automatic configuration Front End pool):</span></span>
    
     <span data-ttu-id="65126-205">\_sipinternaltls。 \_tcp.contoso.com。</span><span class="sxs-lookup"><span data-stu-id="65126-205">\_sipinternaltls.\_tcp.contoso.com.</span></span> <span data-ttu-id="65126-206">86400 IN SRV 0 0 5061 pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-206">86400 IN SRV 0 0 5061 pool01.contoso.com</span></span>

  - <span data-ttu-id="65126-207">如果用户使用 alice@fabrikam.com 登录，则以下 DNS SRV 记录将用于第二个 SIP 域的自动配置。</span><span class="sxs-lookup"><span data-stu-id="65126-207">If a user signs in as alice@fabrikam.com the following DNS SRV record will work for automatic configuration of the second SIP domain.</span></span>
    
     <span data-ttu-id="65126-208">\_sipinternaltls。 \_tcp.fabrikam.com。</span><span class="sxs-lookup"><span data-stu-id="65126-208">\_sipinternaltls.\_tcp.fabrikam.com.</span></span> <span data-ttu-id="65126-209">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="65126-209">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span></span>

<span data-ttu-id="65126-210">与此相对，如果用户使用 tim@litwareinc.com 登录，则以下 DNS SRV 记录不会用于自动配置，因为客户端的 SIP 域 (litwareinc.com) 与池所在的域 (fabrikam.com) 不匹配：</span><span class="sxs-lookup"><span data-stu-id="65126-210">For comparison, if a user signs in as tim@litwareinc.com the following DNS SRV record will not work for automatic configuration, because the client’s SIP domain (litwareinc.com) does not match the domain that the pool is in (fabrikam.com):</span></span>

 <span data-ttu-id="65126-211">\_sipinternaltls。 \_tcp.litwareinc.com。</span><span class="sxs-lookup"><span data-stu-id="65126-211">\_sipinternaltls.\_tcp.litwareinc.com.</span></span> <span data-ttu-id="65126-212">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="65126-212">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span></span>

<span data-ttu-id="65126-213">如果运行 Lync 的客户端需要 "自动配置"，请选择下列选项之一：</span><span class="sxs-lookup"><span data-stu-id="65126-213">If automatic configuration is required for clients running Lync, select one of the following options:</span></span>

  - <span data-ttu-id="65126-214">**组策略对象**   使用组策略对象 (GPO) 填充正确的服务器值。</span><span class="sxs-lookup"><span data-stu-id="65126-214">**Group Policy Objects**   Use Group Policy objects (GPOs) to populate the correct server values.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="65126-215">此选项不会启用自动配置，但可以自动化手动配置的过程，因此，使用这种方法时不需要与自动配置关联的 SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="65126-215">This option does not enable automatic configuration, but it does automate the process of manual configuration, so if this approach is used, the SRV records associated with automatic configuration are not required.</span></span>

    
    </div>

  - <span data-ttu-id="65126-216">**匹配内部区域**   在内部 DNS 中创建与外部 DNS 区域相匹配的区域 (例如，如果使用的是与用于自动配置的 Lync Server 2013 池对应的 IPv6 寻址) 记录，contoso.com) 和创建 DNS A 和 AAAA (。</span><span class="sxs-lookup"><span data-stu-id="65126-216">**Matching internal zone**   Create a zone in the internal DNS that matches the external DNS zone (for example, contoso.com) and create DNS A and AAAA (if you are using IPv6 addressing) records corresponding to the Lync Server 2013 pool used for automatic configuration.</span></span> <span data-ttu-id="65126-217">例如，如果用户托管在 pool01.contoso.net 上，但在 bob@contoso.com 中登录为 Lync，请创建名为 contoso.com 的内部 DNS 区域，并在其中创建一个名为的内部 DNS 区域，如果) 记录 for pool01.contoso.com 使用 IPv6 寻址，则创建一个 DNS A 和 AAAA (。</span><span class="sxs-lookup"><span data-stu-id="65126-217">For example, if a user is homed on pool01.contoso.net but signs into Lync as bob@contoso.com, create an internal DNS zone called contoso.com and inside it, create a DNS A and AAAA (if IPv6 addressing is used) record for pool01.contoso.com.</span></span>

  - <span data-ttu-id="65126-218">**固定点内部区域**   如果在内部 DNS 中创建整个区域不是一个选项，则可以创建针点 (，即专用) 区域，这些区域对应于自动配置所需的 SRV 记录，并使用 dnscmd.exe 填充这些区域。</span><span class="sxs-lookup"><span data-stu-id="65126-218">**Pin-point internal zone**   If you are creating an entire zone in the internal DNS is not an option, you can create pin-point (that is, dedicated) zones that correspond to the SRV records that are required for automatic configuration, and populate those zones using dnscmd.exe.</span></span> <span data-ttu-id="65126-219">Dnscmd.exe 是必需的，因为 DNS 用户界面不支持创建固定点区域。</span><span class="sxs-lookup"><span data-stu-id="65126-219">Dnscmd.exe is required because the DNS user interface does not support creation of pin-point zones.</span></span> <span data-ttu-id="65126-220">例如，如果 SIP 域为 contoso.com，并且你有一个名为 pool01 的前端池，该池包含两个前端服务器，则你需要内部 DNS 中的以下 pin 点区域和记录：</span><span class="sxs-lookup"><span data-stu-id="65126-220">For example, if the SIP domain is contoso.com and you have a Front End pool called pool01 that contains two Front End Servers, you need the following pin-point zones and A records in your internal DNS:</span></span>
    
        dnscmd . /zoneadd _sipinternaltls._tcp.contoso.com. /dsprimary
        dnscmd . /recordadd _sipinternaltls._tcp.contoso.com. @ SRV 0 0 5061 pool01.contoso.com.
        dnscmd . /zoneadd pool01.contoso.com. /dsprimary
        dnscmd . /recordadd pool01.contoso.com. @ A 192.168.10.90
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
        dnscmd . /recordadd pool01.contoso.com. @ A 192.168.10.91 
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
    
    <span data-ttu-id="65126-221">如果环境中包含第二个 SIP 域（例如，fabrikam.com），则内部 DNS 中需要以下精确区域和 A 记录：</span><span class="sxs-lookup"><span data-stu-id="65126-221">If your environment contains a second SIP domain (for example, fabrikam.com), you need the following pin-point zones and A records in your internal DNS:</span></span>
    
        dnscmd . /zoneadd _sipinternaltls._tcp.fabrikam.com. /dsprimary
        dnscmd . /recordadd _sipinternaltls._tcp.fabrikam.com. @ SRV 0 0 5061 pool01.fabrikam.com.
        dnscmd . /zoneadd pool01.fabrikam.com. /dsprimary
        dnscmd . /recordadd pool01.fabrikam.com. @ A 192.168.10.90
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
        dnscmd . /recordadd pool01.fabrikam.com. @ A 192.168.10.91
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>

<div>


> [!NOTE]  
> <span data-ttu-id="65126-222">前端池 FQDN 出现两次，但两次的 IP 地址不同。</span><span class="sxs-lookup"><span data-stu-id="65126-222">The Front End pool FQDN appears twice, but with two different IP addresses.</span></span> <span data-ttu-id="65126-223">这是因为使用了 DNS 负载平衡，但如果使用硬件负载平衡，则只有一个前端池条目。</span><span class="sxs-lookup"><span data-stu-id="65126-223">This is because DNS load balancing is used, but if hardware load balancing is used, there would be only a single Front End pool entry.</span></span> <span data-ttu-id="65126-224">并且，前端池 FQDN 值因 contoso.com 示例和 fabrikam.com 示例的不同而变化，但 IP 地址保持不变。</span><span class="sxs-lookup"><span data-stu-id="65126-224">Also, the Front End pool FQDN values change between the contoso.com example and the fabrikam.com example, but the IP addresses remain the same.</span></span> <span data-ttu-id="65126-225">这是因为用户从任一 SIP 域登录，所以使用相同的前端池进行自动配置。</span><span class="sxs-lookup"><span data-stu-id="65126-225">This is because users signing in from either SIP domain, use the same Front End pool for automatic configuration.</span></span>



</div>

<span data-ttu-id="65126-226">有关详细信息，请参阅 DMTF 博客文章 "Communicator 自动配置和 Split-Brain DNS" [https://go.microsoft.com/fwlink/p/?linkId=200707](https://go.microsoft.com/fwlink/p/?linkid=200707) 。</span><span class="sxs-lookup"><span data-stu-id="65126-226">For details, see the DMTF blog article, "Communicator Automatic Configuration and Split-Brain DNS," at [https://go.microsoft.com/fwlink/p/?linkId=200707](https://go.microsoft.com/fwlink/p/?linkid=200707).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="65126-227">每个博客的内容及其 URL 如有更改，恕不另行通知。</span><span class="sxs-lookup"><span data-stu-id="65126-227">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

</div>

<div>

## <a name="configuring-the-domain-name-system-dns-for-disaster-recovery"></a><span data-ttu-id="65126-228">为灾难恢复配置域名系统 (DNS)</span><span class="sxs-lookup"><span data-stu-id="65126-228">Configuring the domain name system (DNS) for Disaster Recovery</span></span>

<span data-ttu-id="65126-229">若要将 DNS 配置为将 Lync Server 2013 Web 流量重定向到你的灾难恢复和故障转移网站，你必须使用支持 GeoDNS 的 DNS 提供程序。</span><span class="sxs-lookup"><span data-stu-id="65126-229">To configure DNS to redirect Lync Server 2013 Web traffic to your disaster recovery and failover sites, you must be using a DNS provider that supports GeoDNS.</span></span> <span data-ttu-id="65126-230">你可以设置 Web 的 DNS 记录以支持灾难恢复，因此即使一个完整的前端池停机，使用 Web 服务的功能仍继续。</span><span class="sxs-lookup"><span data-stu-id="65126-230">You can set up your DNS records for Web to support disaster recovery, so that features that use Web services continue even if one entire Front End pool goes down.</span></span> <span data-ttu-id="65126-231">此灾难恢复功能支持自动发现 (Lyncdiscover URL)、会议和拨入式简单 URL。</span><span class="sxs-lookup"><span data-stu-id="65126-231">This disaster recovery feature supports the Autodiscover (Lyncdiscover URL), Meet and Dial-In simple URLs.</span></span>

<span data-ttu-id="65126-p133">您可以在 GeoDNS 提供程序上为 Web 服务的内部和外部解决方案定义和配置其他 DNS 主机（如果使用的是 IPv6 地址，则为 A 和 AAAA）记录。以下详细信息假定池已配对，地理位置分散，且 GeoDNS 支持的提供程序使用循环 DNS 或被配置为使用 Pool1 作为主池，并且在发生通信丢失或硬件失败时故障转移到 Pool2。</span><span class="sxs-lookup"><span data-stu-id="65126-p133">You define and configure additional DNS host (A and AAAA if using IPv6) records for internal and external resolution of Web services at your GeoDNS provider. The following details assume paired pools, geographically dispersed, and GeoDNS supported by your provider with either round-robin DNS, or configured to use Pool1 as primary, and fail over to Pool2 in the event of communications loss or hardware failure.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65126-234">GeoDNS 记录 (示例) </span><span class="sxs-lookup"><span data-stu-id="65126-234">GeoDNS record (example)</span></span></th>
<th><span data-ttu-id="65126-235"> (示例) 的池记录</span><span class="sxs-lookup"><span data-stu-id="65126-235">Pool records (example)</span></span></th>
<th><span data-ttu-id="65126-236">CNAME 记录 (示例) </span><span class="sxs-lookup"><span data-stu-id="65126-236">CNAME records (example)</span></span></th>
<th><span data-ttu-id="65126-237">DNS 设置（选择一个选项）</span><span class="sxs-lookup"><span data-stu-id="65126-237">DNS settings (select one option)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65126-238">Meet-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-238">Meet-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-239">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-239">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-240">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-240">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-241">Pool1InternalWebFQDN.contoso.com 的 Meet.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-241">Meet.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-242">Pool2InternalWebFQDN.contoso.com 的 Meet.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-242">Meet.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-243">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-243">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-244">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-244">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65126-245">Meet-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-245">Meet-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-246">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-246">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-247">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-247">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-248">Pool1ExternalWebFQDN.contoso.com 的 Meet.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-248">Meet.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-249">Pool2ExternalWebFQDN.contoso.com 的 Meet.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-249">Meet.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-250">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-250">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-251">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-251">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65126-252">Dialin-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-252">Dialin-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-253">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-253">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-254">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-254">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-255">Pool1InternalWebFQDN.contoso.com 的 Dialin.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-255">Dialin.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-256">Pool2InternalWebFQDN.contoso.com 的 Dialin.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-256">Dialin.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-257">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-257">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-258">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-258">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65126-259">Dialin-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-259">Dialin-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-260">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-260">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-261">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-261">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-262">Pool1ExternalWebFQDN.contoso.com 的 Dialin.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-262">Dialin.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-263">Pool2ExternalWebFQDN.contoso.com 的 Dialin.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-263">Dialin.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-264">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-264">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-265">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-265">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65126-266">Lyncdiscoverint-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-266">Lyncdiscoverint-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-267">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-267">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-268">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-268">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-269">Pool1InternalWebFQDN.contoso.com 的 Lyncdiscoverinternal.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-269">Lyncdiscoverinternal.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-270">Pool2InternalWebFQDN.contoso.com 的 Lyncdiscoverinternal.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-270">Lyncdiscoverinternal.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-271">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-271">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-272">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-272">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65126-273">Lyncdiscover-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-273">Lyncdiscover-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-274">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-274">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-275">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-275">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-276">Pool1ExternalWebFQDN.contoso.com 的 Lyncdiscover.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-276">Lyncdiscover.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-277">Pool2ExternalWebFQDN.contoso.com 的 Lyncdiscover.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-277">Lyncdiscover.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-278">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-278">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-279">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-279">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65126-280">Scheduler-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-280">Scheduler-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-281">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-281">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-282">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-282">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-283">Pool1InternalWebFQDN.contoso.com 的 Scheduler.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-283">Scheduler.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-284">Pool2InternalWebFQDN.contoso.com 的 Scheduler.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-284">Scheduler.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-285">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-285">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-286">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-286">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65126-287">Scheduler-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-287">Scheduler-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-288">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-288">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-289">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="65126-289">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-290">Pool1ExternalWebFQDN.contoso.com 的 Scheduler.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-290">Scheduler.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="65126-291">Pool2ExternalWebFQDN.contoso.com 的 Scheduler.contoso.com 别名</span><span class="sxs-lookup"><span data-stu-id="65126-291">Scheduler.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="65126-292">在池之间启用循环</span><span class="sxs-lookup"><span data-stu-id="65126-292">Round Robin between pools</span></span></p>
<p><span data-ttu-id="65126-293">使用主映像，如果失败则连接到辅助</span><span class="sxs-lookup"><span data-stu-id="65126-293">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-load-balancing"></a><span data-ttu-id="65126-294">DNS Load Balancing</span><span class="sxs-lookup"><span data-stu-id="65126-294">DNS Load Balancing</span></span>

<span data-ttu-id="65126-295">DNS 负载平衡通常在应用程序级别实现。</span><span class="sxs-lookup"><span data-stu-id="65126-295">DNS load balancing is typically implemented at the application level.</span></span> <span data-ttu-id="65126-296">应用程序 (例如，运行 Lync) 的客户端通过连接到从 DNS A 和 (AAAA 返回的其中一个 IP 地址来尝试连接到池中的服务器，如果使用 IPv6 寻址)  (FQDN) 的池完全限定的域名的记录查询。</span><span class="sxs-lookup"><span data-stu-id="65126-296">The application (for example, a client running Lync), tries to connect to a server in a pool by connecting to one of the IP addresses returned from the DNS A and AAAA (if IPv6 addressing is used) record query for the pool fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="65126-297">例如，如果一个名为 pool01.contoso.com 的池中有三个前端服务器，则将发生以下情况：</span><span class="sxs-lookup"><span data-stu-id="65126-297">For example, if there are three front end servers in a pool named pool01.contoso.com, the following will happen:</span></span>

  - <span data-ttu-id="65126-298">运行 Lync 的 pool01.contoso.com 查询 DNS 的客户端。</span><span class="sxs-lookup"><span data-stu-id="65126-298">Clients running Lync query DNS for pool01.contoso.com.</span></span> <span data-ttu-id="65126-299">该查询返回三个 IP 地址，并将其缓存如下 (不一定按此顺序) ：</span><span class="sxs-lookup"><span data-stu-id="65126-299">The query returns three IP addresses and caches them as follows (not necessarily in this order):</span></span>
    
    <span data-ttu-id="65126-300">pool01.contoso.com 192.168.10.90</span><span class="sxs-lookup"><span data-stu-id="65126-300">pool01.contoso.com      192.168.10.90</span></span>
    
    <span data-ttu-id="65126-301">pool01.contoso.com 192.168.10.91</span><span class="sxs-lookup"><span data-stu-id="65126-301">pool01.contoso.com      192.168.10.91</span></span>
    
    <span data-ttu-id="65126-302">pool01.contoso.com 192.168.10.92</span><span class="sxs-lookup"><span data-stu-id="65126-302">pool01.contoso.com      192.168.10.92</span></span>

  - <span data-ttu-id="65126-303">客户端尝试建立与其中一个 IP 地址的 TCP) 连接的传输控制协议 (。</span><span class="sxs-lookup"><span data-stu-id="65126-303">The client attempts to establish a Transmission Control Protocol (TCP) connection to one of the IP addresses.</span></span> <span data-ttu-id="65126-304">如果此操作失败，客户端将尝试缓存中的下一个 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="65126-304">If that fails, the client tries the next IP address in the cache.</span></span>

  - <span data-ttu-id="65126-305">如果 TCP 连接成功，则客户端与 TLS 协商连接到 pool01.contoso.com 上的主注册器。</span><span class="sxs-lookup"><span data-stu-id="65126-305">If the TCP connection succeeds, the client negotiates TLS to connect to the primary registrar on pool01.contoso.com.</span></span>

  - <span data-ttu-id="65126-306">如果客户在未成功连接的情况下尝试所有缓存的条目，则系统将通知用户目前没有运行 Lync Server 2013 的服务器。</span><span class="sxs-lookup"><span data-stu-id="65126-306">If the client tries all cached entries without a successful connection, the user is notified that no servers running Lync Server 2013 are available at the moment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="65126-307">基于 DNS 的负载平衡不同于 dns 循环 (DNS RR) 这通常是指负载平衡，具体取决于 DNS 以提供与池中的服务器对应的 IP 地址的不同顺序。</span><span class="sxs-lookup"><span data-stu-id="65126-307">DNS-based load balancing is different from DNS round robin (DNS RR) which typically refers to load balancing by relying on DNS to provide a different order of IP addresses corresponding to the servers in a pool.</span></span> <span data-ttu-id="65126-308">通常，DNS RR 仅支持负载分配，但不支持故障转移。</span><span class="sxs-lookup"><span data-stu-id="65126-308">Typically DNS RR only enables load distribution, but does not enable failover.</span></span> <span data-ttu-id="65126-309">例如，如果使用 IPv6 寻址) 查询失败，则连接到 DNS A 和 (AAAA 返回的一个 IP 地址时，连接失败。</span><span class="sxs-lookup"><span data-stu-id="65126-309">For example, if the connection to the one IP address returned by the DNS A and AAAA (if you are using IPv6 addressing) query fails, the connection fails.</span></span> <span data-ttu-id="65126-310">因此，DNS 循环复用本身比基于 DNS 的负载平衡的可靠性更低。</span><span class="sxs-lookup"><span data-stu-id="65126-310">Therefore, DNS round robin by itself is less reliable than DNS-based load balancing.</span></span> <span data-ttu-id="65126-311">你可以将 DNS 循环与 DNS 负载平衡结合使用。</span><span class="sxs-lookup"><span data-stu-id="65126-311">You can use DNS round robin in conjunction with DNS load balancing.</span></span>



</div>

<span data-ttu-id="65126-312">DNS 负载平衡用于以下情况：</span><span class="sxs-lookup"><span data-stu-id="65126-312">DNS load balancing is used for the following:</span></span>

  - <span data-ttu-id="65126-313">将服务器到服务器 SIP 负载平衡到边缘服务器</span><span class="sxs-lookup"><span data-stu-id="65126-313">Load balancing server-to-server SIP to the Edge Servers</span></span>

  - <span data-ttu-id="65126-314">负载平衡 "统一通信" 应用程序服务 (UCAS) 应用程序（如会议自动助理、响应组和呼叫寄存）</span><span class="sxs-lookup"><span data-stu-id="65126-314">Load balancing Unified Communications Application Services (UCAS) applications such as Conferencing Auto Attendant, Response Group, and Call Park</span></span>

  - <span data-ttu-id="65126-315">阻止新连接 UCAS 应用程序 (也称为 "排出" ) </span><span class="sxs-lookup"><span data-stu-id="65126-315">Preventing new connections to UCAS applications (also known as "draining")</span></span>

  - <span data-ttu-id="65126-316">负载平衡客户端和边缘服务器之间的所有客户端到服务器流量</span><span class="sxs-lookup"><span data-stu-id="65126-316">Load balancing all client-to-server traffic between clients and Edge Servers</span></span>

<span data-ttu-id="65126-317">无法将 DNS 负载平衡用于以下情况：</span><span class="sxs-lookup"><span data-stu-id="65126-317">DNS load balancing cannot be used for the following:</span></span>

  - <span data-ttu-id="65126-318">客户端到服务器 web 流量到控制器或前端服务器</span><span class="sxs-lookup"><span data-stu-id="65126-318">Client-to-server web traffic to Director or Front End Servers</span></span>

<span data-ttu-id="65126-319">DNS 负载平衡和联合通信：</span><span class="sxs-lookup"><span data-stu-id="65126-319">DNS load balancing and federated traffic:</span></span>

<span data-ttu-id="65126-320">如果 DNS SRV 查询返回多个 DNS 记录，则 Access Edge 服务始终使用最小的数值优先级和最高的数字权重来选取 DNS SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="65126-320">If multiple DNS records are returned by a DNS SRV query, the Access Edge service always picks the DNS SRV record with the lowest numeric priority and highest numeric weight.</span></span> <span data-ttu-id="65126-321">Internet 工程任务组文档 "用于指定服务位置 (DNS SRV) " 的 DNS RR <http://www.ietf.org/rfc/rfc2782.txt> 指定如果已定义多个 DNS srv 记录，将首先使用 "优先级"，然后按 "权重"。</span><span class="sxs-lookup"><span data-stu-id="65126-321">The Internet Engineering Task Force document “A DNS RR for specifying the location of services (DNS SRV)” <http://www.ietf.org/rfc/rfc2782.txt> specifies that if there are multiple DNS SRV records defined, priority is first used, then weight.</span></span> <span data-ttu-id="65126-322">例如，DNS SRV 记录 A 的权重为20，优先级为40，DNS SRV 记录 B 的权重为10，优先级为50。</span><span class="sxs-lookup"><span data-stu-id="65126-322">For example DNS SRV record A has a weight of 20 and a priority of 40 and DNS SRV record B has a weight of 10 and priority of 50.</span></span> <span data-ttu-id="65126-323">将选择优先级为40的 DNS SRV 记录 A。</span><span class="sxs-lookup"><span data-stu-id="65126-323">DNS SRV record A with priority 40 will be selected.</span></span> <span data-ttu-id="65126-324">以下规则适用于 DNS SRV 记录选择：</span><span class="sxs-lookup"><span data-stu-id="65126-324">The following rules apply to DNS SRV record selection:</span></span>

  - <span data-ttu-id="65126-325">首先考虑优先级。</span><span class="sxs-lookup"><span data-stu-id="65126-325">Priority is considered first.</span></span> <span data-ttu-id="65126-326">客户端必须尝试联系由 DNS SRV 记录定义的目标主机，该目标主机可以访问的最低优先级。</span><span class="sxs-lookup"><span data-stu-id="65126-326">A client MUST attempt to contact the target host defined by the DNS SRV record with the lowest numbered priority it can reach.</span></span> <span data-ttu-id="65126-327">应按照权重字段定义的顺序尝试具有相同优先级的目标。</span><span class="sxs-lookup"><span data-stu-id="65126-327">Targets with the same priority SHOULD be tried in an order defined by the weight field.</span></span>

  - <span data-ttu-id="65126-328">"权重" 域为具有相同优先级的条目指定相对权重。</span><span class="sxs-lookup"><span data-stu-id="65126-328">The weight field specifies a relative weight for entries with the same priority.</span></span> <span data-ttu-id="65126-329">应按比例增加所选的概率。</span><span class="sxs-lookup"><span data-stu-id="65126-329">Larger weights SHOULD be given a proportionately higher probability of being selected.</span></span> <span data-ttu-id="65126-330">当没有任何服务器选择要执行时，DNS 管理员应使用权重0。</span><span class="sxs-lookup"><span data-stu-id="65126-330">DNS administrators SHOULD use Weight 0 when there isn’t any server selection to do.</span></span> <span data-ttu-id="65126-331">如果记录包含的权重大于0，则权重为0的记录应具有非常小的选择机会。</span><span class="sxs-lookup"><span data-stu-id="65126-331">In the presence of records containing weights greater than 0, records with weight 0 should have a very small chance of being selected.</span></span>

<span data-ttu-id="65126-332">如果返回具有相同优先级和权重的多个 DNS SRV 记录，则 Access Edge 服务将选择首先从 DNS 服务器接收的 SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="65126-332">If multiple DNS SRV records with equal priority and weight are returned, the Access Edge service will select the SRV record that was received first from the DNS server.</span></span>

<span data-ttu-id="65126-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65126-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

