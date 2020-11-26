---
title: Lync Server 2013：前端池的 DNS 要求
description: Lync Server 2013：前端池的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pool
ms:assetid: 02d2aa6b-9e01-437b-a2df-00590280150d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398082(v=OCS.15)
ms:contentKeyID: 48183249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bfce90eccb8c8dff94d4122c96c4ca68ea9150f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437824"
---
# <a name="dns-requirements-for-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="70492-103">Lync Server 2013 中前端池的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="70492-103">DNS requirements for Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70492-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70492-104">

<span> </span></span></span>

<span data-ttu-id="70492-105">_**主题上次修改时间：** 2012-11-07_</span><span class="sxs-lookup"><span data-stu-id="70492-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="70492-106">若要成功完成此过程，你应至少作为域管理员组的成员或 DnsAdmins 组的成员登录到服务器或域。</span><span class="sxs-lookup"><span data-stu-id="70492-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="70492-107">在拓扑生成器中发布拓扑之前，需要配置所需的域名系统 (DNS) 记录。</span><span class="sxs-lookup"><span data-stu-id="70492-107">You need to configure the required Domain Name System (DNS) records prior to publishing your topology in Topology Builder.</span></span> <span data-ttu-id="70492-108">此外，Lync Server 2013 部署的配置中使用的一些完全限定域名 (Fqdn) 是逻辑的，而不是物理服务器 Fqdn，因此在发布之前需要其他 DNS 配置。</span><span class="sxs-lookup"><span data-stu-id="70492-108">Additionally, some of the fully qualified domain names (FQDNs) used in the configuration of a Lync Server 2013 deployment are logical and not physical server FQDNs, so additional DNS configuration is required prior to publishing.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="70492-109">Lync Server 2013 不支持单标记的域。</span><span class="sxs-lookup"><span data-stu-id="70492-109">Lync Server 2013 does not support single-labeled domains.</span></span> <span data-ttu-id="70492-110">例如，支持一个名为 " <STRONG>contoso. local</STRONG> " 的根域的林，但不支持名为 <STRONG>local</STRONG> 的根域。</span><span class="sxs-lookup"><span data-stu-id="70492-110">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="70492-111">有关详细信息，请参阅 Microsoft 知识库文章300684，"有关为具有单标签 DNS 名称的域配置 Windows 的信息"，请参阅<A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp kbid = 300684</A>。</span><span class="sxs-lookup"><span data-stu-id="70492-111">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=300684">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=300684</A>.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="70492-112">您指定的名称必须与服务器上配置的计算机名相同。</span><span class="sxs-lookup"><span data-stu-id="70492-112">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="70492-113">默认情况下，未加入域的计算机的计算机名是一个短名称，而不是 FQDN。</span><span class="sxs-lookup"><span data-stu-id="70492-113">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="70492-114">拓扑生成器使用 FQDN，而不是短名称。</span><span class="sxs-lookup"><span data-stu-id="70492-114">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="70492-115">在分配运行 Lync Server、Edge 服务器和池的服务器的 Fqdn 时，<STRONG>只能使用标准字符</STRONG> (包括 a-z、a – z、0–9和连字符) 。</span><span class="sxs-lookup"><span data-stu-id="70492-115"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your servers running Lync Server, Edge Servers, and pools.</span></span> <span data-ttu-id="70492-116">不要使用 Unicode 字符或下划线。</span><span class="sxs-lookup"><span data-stu-id="70492-116">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="70492-117">FQDN 中的非标准字符通常不受外部 DNS 和公共证书颁发机构的支持 (CAs)  (当必须将 FQDN 分配给证书) 中的 SN 时。</span><span class="sxs-lookup"><span data-stu-id="70492-117">Nonstandard characters in an FQDN are often not supported by external DNS and public certification authorities (CAs) (when the FQDN must be assigned to the SN in the certificate).</span></span>



</div>

<span data-ttu-id="70492-118">在部署拓扑后操作拓扑之前，请确保根据你的特定功能的需要创建以下 Active Directory 和 DNS 记录 () ：</span><span class="sxs-lookup"><span data-stu-id="70492-118">Prior to operating the topology after it has been deployed, ensure that the following Active Directory and DNS records are created (as your needs for specific features dictate):</span></span>

  - <span data-ttu-id="70492-119">将在拓扑中存在的每个服务器角色将发布为 Active Directory 对象 (将计算机加入域的操作将完成此) 。</span><span class="sxs-lookup"><span data-stu-id="70492-119">Each server role that will exist in the topology is published as an Active Directory object (joining the computer to the domain will accomplish this).</span></span>

  - <span data-ttu-id="70492-120">每个服务器都存在 DNS A 记录。</span><span class="sxs-lookup"><span data-stu-id="70492-120">A DNS A Record exists for each server.</span></span>

  - <span data-ttu-id="70492-121">如果计划使用 sipinternaltls tcp 形式的客户端自动登录，则每个 SIP 域都存在 DNS SRV 记录 \_ \_ \<SIP domain\> 。。</span><span class="sxs-lookup"><span data-stu-id="70492-121">A DNS SRV Record exists for each SIP domain if you plan to use automatic logon for clients in the form of \_sipinternaltls\_tcp.\<SIP domain\>.</span></span> <span data-ttu-id="70492-122">如果将手动配置用于客户端，则不需要此记录。</span><span class="sxs-lookup"><span data-stu-id="70492-122">If you will use manual configuration for clients, this record is not necessary.</span></span>

  - <span data-ttu-id="70492-123">每个配置的简单 URL 的 DNS A 记录，其中通常有四个： "满足"、"拨入"、"lwa" 和 "计划程序"。</span><span class="sxs-lookup"><span data-stu-id="70492-123">A DNS A Record for each configured simple URL, of which there are typically four: meet, dialin, lwa, and scheduler.</span></span> <span data-ttu-id="70492-124">此外，还有一个用于访问 Lync Server 2013 控制面板的特殊 URL 的管理员简单 URL。</span><span class="sxs-lookup"><span data-stu-id="70492-124">Additionally, there is the admin simple URL which is a special URL for access to the Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="70492-125">运行 SQL Server 的服务器必须加入域，并且拓扑生成器正在发布的计算机可以访问该服务器。</span><span class="sxs-lookup"><span data-stu-id="70492-125">The server running SQL Server must be joined to the domain, and reachable by the computer that Topology Builder is publishing from.</span></span>

<span data-ttu-id="70492-126">该表遵循 "规划" 部分中提供的参考体系结构。</span><span class="sxs-lookup"><span data-stu-id="70492-126">The table follows the reference architectures presented in the Planning section.</span></span> <span data-ttu-id="70492-127">有关详细信息，请参阅规划文档中 [Lync Server 2013 中的外部用户访问方案](lync-server-2013-scenarios-for-external-user-access.md) 。</span><span class="sxs-lookup"><span data-stu-id="70492-127">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) in the Planning documentation.</span></span>

<div id="sectionSection0" class="section">

### <a name="dns-records-required-for-the-front-end-pool"></a><span data-ttu-id="70492-128">前端池所需的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="70492-128">DNS Records Required for the Front End pool</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70492-129">位置</span><span class="sxs-lookup"><span data-stu-id="70492-129">Location</span></span></th>
<th><span data-ttu-id="70492-130">类型</span><span class="sxs-lookup"><span data-stu-id="70492-130">Type</span></span></th>
<th><span data-ttu-id="70492-131">FQDN</span><span class="sxs-lookup"><span data-stu-id="70492-131">FQDN</span></span></th>
<th><span data-ttu-id="70492-132">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="70492-132">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70492-133">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-133">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-134">A</span><span class="sxs-lookup"><span data-stu-id="70492-134">A</span></span></p></td>
<td><p><span data-ttu-id="70492-135">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-135">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="70492-136">Pool01 () 的 DNS 负载平衡。</span><span class="sxs-lookup"><span data-stu-id="70492-136">Pool01 (DNS load balancing).</span></span> <span data-ttu-id="70492-137">需要针对池中每个前端服务器的 IP 地址的 DNS A 记录，映射到池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="70492-137">Requires a DNS A record for the IP address of each Front End Server within the pool, mapping to the pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70492-138">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-138">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-139">A</span><span class="sxs-lookup"><span data-stu-id="70492-139">A</span></span></p></td>
<td><p><span data-ttu-id="70492-140">pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-140">pool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="70492-141">Pool01 (虚拟 IP (VIP) 硬件负载平衡器) 。</span><span class="sxs-lookup"><span data-stu-id="70492-141">Pool01 (virtual IP (VIP) of hardware load balancer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70492-142">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-142">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-143">A</span><span class="sxs-lookup"><span data-stu-id="70492-143">A</span></span></p></td>
<td><p><span data-ttu-id="70492-144">fe01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-144">fe01.contoso.net</span></span></p>
<p><span data-ttu-id="70492-145">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-145">fe02.contoso.net</span></span></p>
<p><span data-ttu-id="70492-146">fe03.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-146">fe03.contoso.net</span></span></p>
<p><span data-ttu-id="70492-147">…</span><span class="sxs-lookup"><span data-stu-id="70492-147">…</span></span></p></td>
<td><p><span data-ttu-id="70492-148">Pool01 前端服务器 (节点 1) 。</span><span class="sxs-lookup"><span data-stu-id="70492-148">Pool01 Front End Server (NODE 1).</span></span></p>
<p><span data-ttu-id="70492-149">Pool01 前端服务器 (节点 2) 。</span><span class="sxs-lookup"><span data-stu-id="70492-149">Pool01 Front End Server (NODE 2).</span></span></p>
<p><span data-ttu-id="70492-150">Pool01 前端服务器 (节点 3) 。</span><span class="sxs-lookup"><span data-stu-id="70492-150">Pool01 Front End Server (NODE 3).</span></span></p>
<p><span data-ttu-id="70492-151">…</span><span class="sxs-lookup"><span data-stu-id="70492-151">…</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70492-152">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-152">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-153">A</span><span class="sxs-lookup"><span data-stu-id="70492-153">A</span></span></p></td>
<td><p><span data-ttu-id="70492-154">fe02.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-154">fe02.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="70492-155">Pool01 前端服务器 (节点 2) 。</span><span class="sxs-lookup"><span data-stu-id="70492-155">Pool01 Front End Server (NODE 2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70492-156">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-156">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-157">A</span><span class="sxs-lookup"><span data-stu-id="70492-157">A</span></span></p></td>
<td><p><span data-ttu-id="70492-158">lsweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-158">lsweb.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="70492-159">Pool01 (客户端到服务器 web 流量的 VIP) 。</span><span class="sxs-lookup"><span data-stu-id="70492-159">Pool01 (VIP) for client-to-server web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70492-160">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-160">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-161">A</span><span class="sxs-lookup"><span data-stu-id="70492-161">A</span></span></p></td>
<td><p><span data-ttu-id="70492-162">sqlbe.contoso.net</span><span class="sxs-lookup"><span data-stu-id="70492-162">sqlbe.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="70492-163">运行 SQL Server 2008 R2 的 Pool01 后端服务器。</span><span class="sxs-lookup"><span data-stu-id="70492-163">Pool01 Back End Server running SQL Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70492-164">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-164">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-165">A</span><span class="sxs-lookup"><span data-stu-id="70492-165">A</span></span></p></td>
<td><p><span data-ttu-id="70492-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="70492-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="70492-167">对于 Lync Phone Edition 是必需的，或者自动登录未安装 DNS SRV 记录的客户端，并且对于严格的域匹配。</span><span class="sxs-lookup"><span data-stu-id="70492-167">Required for Lync Phone Edition, or automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="70492-168">在所有情况下均不需要。</span><span class="sxs-lookup"><span data-stu-id="70492-168">Not required in all cases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70492-169">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-169">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-170">A</span><span class="sxs-lookup"><span data-stu-id="70492-170">A</span></span></p></td>
<td><p><span data-ttu-id="70492-171">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="70492-171">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="70492-172">假定第二 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="70492-172">Assumes a second SIP domain.</span></span> <span data-ttu-id="70492-173">适用于 Lync Phone Edition、自动登录没有 DNS SRV 记录的客户端以及严格的域匹配。</span><span class="sxs-lookup"><span data-stu-id="70492-173">Required for Lync Phone Edition, automatic logon of clients without DNS SRV records, and for strict domain matching.</span></span> <span data-ttu-id="70492-174">在所有情况下均不需要。</span><span class="sxs-lookup"><span data-stu-id="70492-174">Not required in all cases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70492-175">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-175">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-176">A</span><span class="sxs-lookup"><span data-stu-id="70492-176">A</span></span></p></td>
<td><p><span data-ttu-id="70492-177">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="70492-177">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="70492-178">在内部发布的拨入式会议的简单 URL-前端服务器 (或 Director （如果已安装) 响应简单的 URL 查询）。</span><span class="sxs-lookup"><span data-stu-id="70492-178">Simple URL for dial-in conferencing published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70492-179">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-179">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-180">A</span><span class="sxs-lookup"><span data-stu-id="70492-180">A</span></span></p></td>
<td><p><span data-ttu-id="70492-181">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="70492-181">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="70492-182">在内部发布的会议的简单 URL-前端服务器 (或 Director （如果已安装) 响应简单的 URL 查询）。</span><span class="sxs-lookup"><span data-stu-id="70492-182">Simple URL for conferences published internally – Front End Server (or Director, if installed) responds to simple URL queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70492-183">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-183">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-184">A</span><span class="sxs-lookup"><span data-stu-id="70492-184">A</span></span></p></td>
<td><p><span data-ttu-id="70492-185">admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="70492-185">admin.contoso.com</span></span></p>
<p><span data-ttu-id="70492-186">iis</span><span class="sxs-lookup"><span data-stu-id="70492-186">admin</span></span></p></td>
<td><p><span data-ttu-id="70492-187">可选记录、Lync Server 2013 控制面板的简单 URL 发布内部-前端服务器 (或 Director （如果已安装) 响应简单的 URL 查询）。</span><span class="sxs-lookup"><span data-stu-id="70492-187">Optional record, simple URL for Lync Server 2013 Control Panel published internally - Front End Server (or Director, if installed) responds to simple URL queries.</span></span> <span data-ttu-id="70492-188">仅限主机名 (不建议使用域名) 。</span><span class="sxs-lookup"><span data-stu-id="70492-188">Host name only (no domain name) is recommended.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="70492-189">VIP = 硬件负载平衡器的虚拟 IP 地址</span><span class="sxs-lookup"><span data-stu-id="70492-189">VIP = Virtual IP address for hardware load balancer</span></span>



</div>

</div>

<div>

## <a name="dns-srv-records-for-the-front-end-pool"></a><span data-ttu-id="70492-190">前端池的 DNS SRV 记录</span><span class="sxs-lookup"><span data-stu-id="70492-190">DNS SRV Records for the Front End pool</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70492-191">位置</span><span class="sxs-lookup"><span data-stu-id="70492-191">Location</span></span></th>
<th><span data-ttu-id="70492-192">类型</span><span class="sxs-lookup"><span data-stu-id="70492-192">Type</span></span></th>
<th><span data-ttu-id="70492-193">FQDN</span><span class="sxs-lookup"><span data-stu-id="70492-193">FQDN</span></span></th>
<th><span data-ttu-id="70492-194">目标 FQDN</span><span class="sxs-lookup"><span data-stu-id="70492-194">Target FQDN</span></span></th>
<th><span data-ttu-id="70492-195">端口</span><span class="sxs-lookup"><span data-stu-id="70492-195">Port</span></span></th>
<th><span data-ttu-id="70492-196">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="70492-196">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70492-197">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-197">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-198">SRV</span><span class="sxs-lookup"><span data-stu-id="70492-198">SRV</span></span></p></td>
<td><p><span data-ttu-id="70492-199">_sipinternaltls _sipinternaltls._tcp .com</span><span class="sxs-lookup"><span data-stu-id="70492-199">_sipinternaltls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="70492-200">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="70492-200">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="70492-201">5061</span><span class="sxs-lookup"><span data-stu-id="70492-201">5061</span></span></p></td>
<td><p><span data-ttu-id="70492-202">自动配置要在内部工作的 Lync 2013 客户端所需。</span><span class="sxs-lookup"><span data-stu-id="70492-202">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70492-203">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-203">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-204">SRV</span><span class="sxs-lookup"><span data-stu-id="70492-204">SRV</span></span></p></td>
<td><p><span data-ttu-id="70492-205">_sipinternaltls _sipinternaltls._tcp .com</span><span class="sxs-lookup"><span data-stu-id="70492-205">_sipinternaltls._tcp.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="70492-206">pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="70492-206">pool01.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="70492-207">5061</span><span class="sxs-lookup"><span data-stu-id="70492-207">5061</span></span></p></td>
<td><p><span data-ttu-id="70492-208">自动配置要在内部工作的 Lync 2013 客户端所需。</span><span class="sxs-lookup"><span data-stu-id="70492-208">Required for automatic configuration of Lync 2013 clients to work internally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70492-209">内部 DNS</span><span class="sxs-lookup"><span data-stu-id="70492-209">Internal DNS</span></span></p></td>
<td><p><span data-ttu-id="70492-210">SRV</span><span class="sxs-lookup"><span data-stu-id="70492-210">SRV</span></span></p></td>
<td><p><span data-ttu-id="70492-211">_ntp _ntp._udp .com</span><span class="sxs-lookup"><span data-stu-id="70492-211">_ntp._udp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="70492-212">dc01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="70492-212">dc01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="70492-213">123</span><span class="sxs-lookup"><span data-stu-id="70492-213">123</span></span></p></td>
<td><p><span data-ttu-id="70492-214">运行 Lync Phone Edition 的设备所需的网络时间协议 (NTP) 源。</span><span class="sxs-lookup"><span data-stu-id="70492-214">Network Time Protocol (NTP) source required for devices running Lync Phone Edition.</span></span> <span data-ttu-id="70492-215">在内部，这应该指向域控制器。</span><span class="sxs-lookup"><span data-stu-id="70492-215">Internally, this should point to the domain controller.</span></span> <span data-ttu-id="70492-216">如果域控制器未定义，它将尝试使用 NTP 服务器 time.windows.com。</span><span class="sxs-lookup"><span data-stu-id="70492-216">If the domain controller is not defined, it will try to use the NTP server time.windows.com.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="70492-217">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70492-217">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

