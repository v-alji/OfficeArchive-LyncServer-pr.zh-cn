---
title: Lync Server 2013：内部服务器的证书要求
description: Lync Server 2013：内部服务器的证书要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for internal servers
ms:assetid: 0444cdbd-538c-43b1-b9a1-9d7d6cf818d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398094(v=OCS.15)
ms:contentKeyID: 48183270
ms.date: 02/17/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc1a627dd762c849b848087a96e00e19d320ef01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435352"
---
# <a name="certificate-requirements-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="88a9f-103">Lync Server 2013 中内部服务器的证书要求</span><span class="sxs-lookup"><span data-stu-id="88a9f-103">Certificate requirements for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88a9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88a9f-104">

<span> </span></span></span>

<span data-ttu-id="88a9f-105">_**主题上次修改时间：** 2017-02-17_</span><span class="sxs-lookup"><span data-stu-id="88a9f-105">_**Topic Last Modified:** 2017-02-17_</span></span>

<span data-ttu-id="88a9f-106">运行 Lync Server 且需要证书的内部服务器包括标准版 Server、企业版前端服务器、中介服务器和 Director。</span><span class="sxs-lookup"><span data-stu-id="88a9f-106">Internal servers that are running Lync Server and that require certificates include Standard Edition server, Enterprise Edition Front End Server, Mediation Server, and Director.</span></span> <span data-ttu-id="88a9f-107">下表显示了这些服务器的证书要求。</span><span class="sxs-lookup"><span data-stu-id="88a9f-107">The following table shows the certificate requirements for these servers.</span></span> <span data-ttu-id="88a9f-108">您可以使用 Lync Server 证书向导请求这些证书。</span><span class="sxs-lookup"><span data-stu-id="88a9f-108">You can use the Lync Server certificate wizard to request these certificates.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="88a9f-109">对于与前端池、前端服务器或控制器上的简单 Url 相关联的主题备用名称，支持通配符证书。</span><span class="sxs-lookup"><span data-stu-id="88a9f-109">Wildcard certificates are supported for the subject alternative names associated with the simple URLs on the Front End pool, Front End Server, or Director.</span></span> <span data-ttu-id="88a9f-110">有关通配符证书支持的详细信息，请参阅 <A href="lync-server-2013-wildcard-certificate-support.md">Lync Server 2013 中的通配证书支持</A>。</span><span class="sxs-lookup"><span data-stu-id="88a9f-110">For details about wildcard certificate support, see <A href="lync-server-2013-wildcard-certificate-support.md">Wildcard certificate support in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="88a9f-111">尽管推荐内部企业证书颁发机构 (CA) 供内部服务器使用，但你也可以使用公共 CA。</span><span class="sxs-lookup"><span data-stu-id="88a9f-111">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="88a9f-112">有关公共 Ca 的列表，这些 Ca 提供符合统一通信 (UC) 证书的特定要求的证书，并与 Microsoft 合作以确保它们能够使用 Lync Server 证书向导，请参阅 Microsoft 知识库929395： "Exchange Server 的统一通信证书合作伙伴和通信服务器" 一文 [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) 。</span><span class="sxs-lookup"><span data-stu-id="88a9f-112">For a list of public CAs that provide certificates that comply with specific requirements for unified communications (UC) certificates and have partnered with Microsoft to ensure they work with the Lync Server Certificate Wizard, see article Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<span data-ttu-id="88a9f-113">与其他应用程序和服务器（如 Exchange 2013）通信需要其他应用程序和产品支持的证书。</span><span class="sxs-lookup"><span data-stu-id="88a9f-113">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="88a9f-114">对于2013版本，Lync Server 2013 和其他 Microsoft Server 产品（包括 Exchange 2013 和 SharePoint Server）支持用于服务器到服务器身份验证和授权的开放授权 (OAuth) 协议。</span><span class="sxs-lookup"><span data-stu-id="88a9f-114">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="88a9f-115">有关详细信息，请参阅在部署文档或操作文档中 [管理 Lync server 2013 中的服务器到服务器身份验证 (OAuth) 和合作伙伴应用程序](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) 。</span><span class="sxs-lookup"><span data-stu-id="88a9f-115">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="88a9f-116">对于运行 Windows 7 操作系统、Windows Server 2008 操作系统、windows Server 2008 R2 操作系统、Windows Vista 操作系统和 Microsoft Lync Phone Edition 的客户端的连接，Lync Server 2013 包括对 (的支持，但不需要使用 SHA-256 加密哈希函数签名的) 证书。</span><span class="sxs-lookup"><span data-stu-id="88a9f-116">For connections from clients running Windows 7 operating system, Windows Server 2008 operating system, Windows Server 2008 R2 operating system, Windows Vista operating system, and Microsoft Lync Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="88a9f-117">若要支持使用 SHA-256 的外部访问，外部证书由使用 SHA-256 的公共 CA 颁发。</span><span class="sxs-lookup"><span data-stu-id="88a9f-117">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="88a9f-118">下表显示了前端池和标准版服务器的服务器角色的证书要求。</span><span class="sxs-lookup"><span data-stu-id="88a9f-118">The following tables show certificate requirements by server role for Front End pools and Standard Edition servers.</span></span> <span data-ttu-id="88a9f-119">所有这些都是标准 web 服务器证书、私钥、不可导出的。</span><span class="sxs-lookup"><span data-stu-id="88a9f-119">All these are standard web server certificates, private key, non-exportable.</span></span>

<span data-ttu-id="88a9f-120">请注意，使用证书向导申请证书时，系统会自动配置服务器增强型密钥用法 (EKU) 。</span><span class="sxs-lookup"><span data-stu-id="88a9f-120">Note that server enhanced key usage (EKU) is automatically configured when you use the certificate wizard to request certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88a9f-121">每个证书友好名称在计算机存储中必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="88a9f-121">Each certificate Friendly Name must be unique in the computer store.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="88a9f-122">如果您已在 DNS 中配置了 sipinternal.contoso.com 或 sipexternal.contoso.com，则需要在证书的 "主题备用名称" 中添加它们。</span><span class="sxs-lookup"><span data-stu-id="88a9f-122">If you have configured sipinternal.contoso.com or sipexternal.contoso.com in your DNS, you will need to add them in the certificate’s Subject Alternative Name.</span></span>



</div>

### <a name="certificates-for-standard-edition-server"></a><span data-ttu-id="88a9f-123">标准版服务器的证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-123">Certificates for Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88a9f-124">证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-124">Certificate</span></span></th>
<th><span data-ttu-id="88a9f-125">使用者名称/常用名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-125">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="88a9f-126">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-126">Subject alternative name</span></span></th>
<th><span data-ttu-id="88a9f-127">示例</span><span class="sxs-lookup"><span data-stu-id="88a9f-127">Example</span></span></th>
<th><span data-ttu-id="88a9f-128">备注</span><span class="sxs-lookup"><span data-stu-id="88a9f-128">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-129">默认</span><span class="sxs-lookup"><span data-stu-id="88a9f-129">Default</span></span></p></td>
<td><p><span data-ttu-id="88a9f-130"> () 池的 FQDN 的完全限定的域名</span><span class="sxs-lookup"><span data-stu-id="88a9f-130">Fully qualified domain name (FQDN) of the pool</span></span></p></td>
<td><p><span data-ttu-id="88a9f-131">池的 FQDN 和服务器的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-131">FQDN of the pool and the FQDN of the server</span></span></p>
<p><span data-ttu-id="88a9f-132">如果具有多个 SIP 域并已启用自动客户端配置，则证书向导会检测并添加所有受支持的 SIP 域 FQDN。</span><span class="sxs-lookup"><span data-stu-id="88a9f-132">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="88a9f-133">如果此池是客户端的自动登录服务器，而且组策略要求执行严格的域名系统 (DNS) 匹配，那么还需要 sip.sipdomain 条目（对应于您拥有的每个 SIP 域）。</span><span class="sxs-lookup"><span data-stu-id="88a9f-133">If this pool is the auto-logon server for clients and strict Domain Name System (DNS) matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="88a9f-134">SN=se01.contoso.com; SAN=se01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-134">SN=se01.contoso.com; SAN=se01.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-135">如果此池是客户端的自动登录服务器，而且组策略要求执行严格的 DNS 匹配，则还需要 SAN=sip.contoso.com; SAN=sip.fabrikam.com。</span><span class="sxs-lookup"><span data-stu-id="88a9f-135">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="88a9f-136">在标准版服务器上，服务器 FQDN 与池 FQDN 相同。</span><span class="sxs-lookup"><span data-stu-id="88a9f-136">On Standard Edition server, the server FQDN is the same as the pool FQDN.</span></span></p>
<p><span data-ttu-id="88a9f-137">证书向导会检测您在安装过程中所指定的任何 SIP 域，然后自动将它们添加到使用者可选名称中。</span><span class="sxs-lookup"><span data-stu-id="88a9f-137">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="88a9f-138">也可将此证书用于服务器到服务器身份验证。</span><span class="sxs-lookup"><span data-stu-id="88a9f-138">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88a9f-139">Web 内部</span><span class="sxs-lookup"><span data-stu-id="88a9f-139">Web internal</span></span></p></td>
<td><p><span data-ttu-id="88a9f-140">服务器的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-140">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="88a9f-141">以下各项：</span><span class="sxs-lookup"><span data-stu-id="88a9f-141">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="88a9f-142">内部 Web FQDN（与服务器的 FQDN 相同）</span><span class="sxs-lookup"><span data-stu-id="88a9f-142">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="88a9f-143">会议简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-143">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="88a9f-144">拨入简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-144">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-145">管理简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-145">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-146">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="88a9f-146">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88a9f-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-148">使用通配符证书：</span><span class="sxs-lookup"><span data-stu-id="88a9f-148">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="88a9f-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="88a9f-150">不能在拓扑生成器中替代内部 web FQDN。</span><span class="sxs-lookup"><span data-stu-id="88a9f-150">You cannot override the Internal web FQDN in Topology Builder.</span></span></p>
<p><span data-ttu-id="88a9f-151">如果您有多个会议简单 URL，则必须将它们作为使用者可选名称全部添加。</span><span class="sxs-lookup"><span data-stu-id="88a9f-151">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="88a9f-152">简单 URL 条目支持通配符条目。</span><span class="sxs-lookup"><span data-stu-id="88a9f-152">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-153">Web 外部</span><span class="sxs-lookup"><span data-stu-id="88a9f-153">Web external</span></span></p></td>
<td><p><span data-ttu-id="88a9f-154">服务器的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-154">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="88a9f-155">以下各项：</span><span class="sxs-lookup"><span data-stu-id="88a9f-155">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="88a9f-156">外部 Web FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-156">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="88a9f-157">拨入简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-157">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-158">每个 SIP 域的会议简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-158">Meet simple URLs per SIP domain</span></span></p></li>
<li><p><span data-ttu-id="88a9f-159">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="88a9f-159">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88a9f-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-161">使用通配符证书：</span><span class="sxs-lookup"><span data-stu-id="88a9f-161">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="88a9f-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="88a9f-163">如果您有多个会议简单 URL，则必须将它们作为使用者可选名称全部添加。</span><span class="sxs-lookup"><span data-stu-id="88a9f-163">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="88a9f-164">简单 URL 条目支持通配符条目。</span><span class="sxs-lookup"><span data-stu-id="88a9f-164">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-front-end-server-in-a-front-end-pool"></a><span data-ttu-id="88a9f-165">前端服务器在前端池中的证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-165">Certificates for Front End Server in a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88a9f-166">证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-166">Certificate</span></span></th>
<th><span data-ttu-id="88a9f-167">使用者名称/常用名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-167">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="88a9f-168">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-168">Subject alternative name</span></span></th>
<th><span data-ttu-id="88a9f-169">示例</span><span class="sxs-lookup"><span data-stu-id="88a9f-169">Example</span></span></th>
<th><span data-ttu-id="88a9f-170">备注</span><span class="sxs-lookup"><span data-stu-id="88a9f-170">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-171">默认</span><span class="sxs-lookup"><span data-stu-id="88a9f-171">Default</span></span></p></td>
<td><p><span data-ttu-id="88a9f-172">池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-172">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="88a9f-173">服务器的池和 FQDN 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="88a9f-173">FQDN of the pool and FQDN of the server.</span></span></p>
<p><span data-ttu-id="88a9f-174">如果具有多个 SIP 域并已启用自动客户端配置，则证书向导会检测并添加所有受支持的 SIP 域 FQDN。</span><span class="sxs-lookup"><span data-stu-id="88a9f-174">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="88a9f-175">如果此池是客户端的自动登录服务器，并且在组策略中需要严格的 DNS 匹配，则你还需要针对) 的每个 SIP 域的 sipdomain (的条目。</span><span class="sxs-lookup"><span data-stu-id="88a9f-175">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="88a9f-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-177">如果此池是客户端的自动登录服务器，而且组策略要求执行严格的 DNS 匹配，则还需要 SAN=sip.contoso.com; SAN=sip.fabrikam.com。</span><span class="sxs-lookup"><span data-stu-id="88a9f-177">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="88a9f-178">证书向导会检测您在安装过程中所指定的任何 SIP 域，然后自动将它们添加到使用者可选名称中。</span><span class="sxs-lookup"><span data-stu-id="88a9f-178">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="88a9f-179">也可将此证书用于服务器到服务器身份验证。</span><span class="sxs-lookup"><span data-stu-id="88a9f-179">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88a9f-180">Web 内部</span><span class="sxs-lookup"><span data-stu-id="88a9f-180">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="88a9f-181">池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-181">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="88a9f-182">以下各项：</span><span class="sxs-lookup"><span data-stu-id="88a9f-182">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="88a9f-183">内部 Web FQDN（与服务器的 FQDN 不同）</span><span class="sxs-lookup"><span data-stu-id="88a9f-183">Internal web FQDN (which is NOT the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="88a9f-184">服务器 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-184">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="88a9f-185">Lync 池 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-185">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="88a9f-186">会议简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-186">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="88a9f-187">拨入简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-187">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-188">管理简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-188">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-189">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="88a9f-189">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88a9f-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-191">使用通配符证书：</span><span class="sxs-lookup"><span data-stu-id="88a9f-191">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="88a9f-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="88a9f-193">如果您有多个会议简单 URL，则必须将它们作为使用者可选名称全部添加。</span><span class="sxs-lookup"><span data-stu-id="88a9f-193">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="88a9f-194">简单 URL 条目支持通配符条目。</span><span class="sxs-lookup"><span data-stu-id="88a9f-194">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-195">Web 外部</span><span class="sxs-lookup"><span data-stu-id="88a9f-195">Web external</span></span></p></td>
<td><p><span data-ttu-id="88a9f-196">池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-196">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="88a9f-197">以下各项：</span><span class="sxs-lookup"><span data-stu-id="88a9f-197">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="88a9f-198">外部 Web FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-198">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="88a9f-199">拨入简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-199">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-200">管理简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-200">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-201">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="88a9f-201">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88a9f-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-203">使用通配符证书：</span><span class="sxs-lookup"><span data-stu-id="88a9f-203">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="88a9f-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="88a9f-205">如果您有多个会议简单 URL，则必须将它们作为使用者可选名称全部添加。</span><span class="sxs-lookup"><span data-stu-id="88a9f-205">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="88a9f-206">简单 URL 条目支持通配符条目。</span><span class="sxs-lookup"><span data-stu-id="88a9f-206">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-director"></a><span data-ttu-id="88a9f-207">Director 的证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-207">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88a9f-208">证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-208">Certificate</span></span></th>
<th><span data-ttu-id="88a9f-209">使用者名称/常用名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-209">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="88a9f-210">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-210">Subject alternative name</span></span></th>
<th><span data-ttu-id="88a9f-211">示例</span><span class="sxs-lookup"><span data-stu-id="88a9f-211">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-212">默认</span><span class="sxs-lookup"><span data-stu-id="88a9f-212">Default</span></span></p></td>
<td><p><span data-ttu-id="88a9f-213">控制器池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-213">FQDN of the Director pool</span></span></p></td>
<td><p><span data-ttu-id="88a9f-214">Director 的 FQDN、控制器池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-214">FQDN of the Director, FQDN of the Director pool</span></span></p>
<p><span data-ttu-id="88a9f-215">如果此池是客户端的自动登录服务器，并且在组策略中需要严格的 DNS 匹配，则你还需要针对) 的每个 SIP 域的 sipdomain (的条目。</span><span class="sxs-lookup"><span data-stu-id="88a9f-215">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="88a9f-216">SN = dir-pool.contoso.com;SAN = dir-pool.contoso.com;SAN = dir01</span><span class="sxs-lookup"><span data-stu-id="88a9f-216">SN=dir-pool.contoso.com; SAN=dir-pool.contoso.com; SAN=dir01.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-217">如果此控制器池是客户端的自动登录服务器，而且组策略要求执行严格的 DNS 匹配，那么还需要 SAN=sip.contoso.com; SAN=sip.fabrikam.com。</span><span class="sxs-lookup"><span data-stu-id="88a9f-217">If this Director pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88a9f-218">Web 内部</span><span class="sxs-lookup"><span data-stu-id="88a9f-218">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="88a9f-219">服务器的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-219">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="88a9f-220">以下各项：</span><span class="sxs-lookup"><span data-stu-id="88a9f-220">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="88a9f-221">内部 Web FQDN（与服务器的 FQDN 相同）</span><span class="sxs-lookup"><span data-stu-id="88a9f-221">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="88a9f-222">服务器 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-222">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="88a9f-223">Lync 池 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-223">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="88a9f-224">会议简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-224">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="88a9f-225">拨入简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-225">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-226">管理简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-226">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-227">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="88a9f-227">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88a9f-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-230">Web 外部</span><span class="sxs-lookup"><span data-stu-id="88a9f-230">Web external</span></span></p></td>
<td><p><span data-ttu-id="88a9f-231">服务器的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-231">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="88a9f-232">以下各项：</span><span class="sxs-lookup"><span data-stu-id="88a9f-232">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="88a9f-233">外部 Web FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-233">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="88a9f-234">拨入简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-234">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-235">管理简单 URL</span><span class="sxs-lookup"><span data-stu-id="88a9f-235">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="88a9f-236">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="88a9f-236">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88a9f-237">控制器外部 Web FQDN 必须不同于前端池或前端服务器。</span><span class="sxs-lookup"><span data-stu-id="88a9f-237">The Director external web FQDN must be different from the Front End pool or Front End Server.</span></span></p>
<p><span data-ttu-id="88a9f-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="88a9f-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="88a9f-240">如果你有独立的中介服务器池，则其中的中介服务器需要下表中列出的证书。</span><span class="sxs-lookup"><span data-stu-id="88a9f-240">If you have a stand-alone Mediation Server pool, the Mediation Servers in it each need the certificates listed in the following table.</span></span> <span data-ttu-id="88a9f-241">如果你 collocate 前端服务器的中介服务器，本主题前面的 "前端服务器的前端服务器证书" 表中列出的证书已足够。</span><span class="sxs-lookup"><span data-stu-id="88a9f-241">If you collocate Mediation Server with the Front End Servers, the certificates listed in the “Certificates for Front End Server in Front End Pool” table earlier in this topic are sufficient.</span></span>

### <a name="certificates-for-stand-alone-mediation-server"></a><span data-ttu-id="88a9f-242">独立中介服务器的证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-242">Certificates for Stand-alone Mediation Server</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88a9f-243">证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-243">Certificate</span></span></th>
<th><span data-ttu-id="88a9f-244">使用者名称/常用名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-244">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="88a9f-245">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-245">Subject alternative name</span></span></th>
<th><span data-ttu-id="88a9f-246">示例</span><span class="sxs-lookup"><span data-stu-id="88a9f-246">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-247">默认</span><span class="sxs-lookup"><span data-stu-id="88a9f-247">Default</span></span></p></td>
<td><p><span data-ttu-id="88a9f-248">池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-248">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="88a9f-249">池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-249">FQDN of the pool</span></span></p>
<p><span data-ttu-id="88a9f-250">池成员服务器的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-250">FQDN of pool member server</span></span></p></td>
<td><p><span data-ttu-id="88a9f-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="88a9f-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-survivable-branch-appliance"></a><span data-ttu-id="88a9f-252">Survivable 分支装置的证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-252">Certificates for Survivable Branch Appliance</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88a9f-253">证书</span><span class="sxs-lookup"><span data-stu-id="88a9f-253">Certificate</span></span></th>
<th><span data-ttu-id="88a9f-254">使用者名称/常用名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-254">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="88a9f-255">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="88a9f-255">Subject alternative name</span></span></th>
<th><span data-ttu-id="88a9f-256">示例</span><span class="sxs-lookup"><span data-stu-id="88a9f-256">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88a9f-257">默认</span><span class="sxs-lookup"><span data-stu-id="88a9f-257">Default</span></span></p></td>
<td><p><span data-ttu-id="88a9f-258">设备的 FQDN</span><span class="sxs-lookup"><span data-stu-id="88a9f-258">FQDN of the appliance</span></span></p></td>
<td><p><span data-ttu-id="88a9f-259">SIP。 &lt;sipdomain &gt; (需要每个 SIP 域一个条目) </span><span class="sxs-lookup"><span data-stu-id="88a9f-259">SIP.&lt;sipdomain&gt; (need one entry per SIP domain)</span></span></p></td>
<td><p><span data-ttu-id="88a9f-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="88a9f-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="88a9f-261">另请参阅</span><span class="sxs-lookup"><span data-stu-id="88a9f-261">See Also</span></span>


[<span data-ttu-id="88a9f-262">Lync Server 2013 中的通配符证书支持</span><span class="sxs-lookup"><span data-stu-id="88a9f-262">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="88a9f-263"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88a9f-263"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

