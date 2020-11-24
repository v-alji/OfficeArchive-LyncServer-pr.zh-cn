---
title: DNS 摘要-SIP、XMPP 联盟和公共即时消息
description: DNS 摘要-SIP、XMPP 联盟和公共即时消息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - SIP, XMPP federation, and public instant messaging
ms:assetid: 1ed24fb8-a849-44c0-a52e-7aef7527e644
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618369(v=OCS.15)
ms:contentKeyID: 49105656
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f40013b8346cc049f844a827b21bef81a66f6950
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391747"
---
# <a name="dns-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="14320-103">DNS 摘要-Lync Server 2013 中的 SIP、XMPP 联盟和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="14320-103">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14320-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14320-104">

<span> </span></span></span>

<span data-ttu-id="14320-105">_**主题上次修改时间：** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="14320-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="14320-106">域名系统 (用于定义与 Office 通信服务器或 Lync Server 合作伙伴联合身份的 DNS) 记录，由你决定允许其他视角合作伙伴自动 DNS 发现你的域。</span><span class="sxs-lookup"><span data-stu-id="14320-106">The Domain Name System (DNS) records that will be required for defining a federation with Office Communications Server or Lync Server partners is determined by your decision to either allow automatic DNS discovery of your domain by other perspective partners.</span></span> <span data-ttu-id="14320-107">如果发布 \_ sipfederationtls。 \_tcp-out.</span><span class="sxs-lookup"><span data-stu-id="14320-107">If you publish the \_sipfederationtls.\_tcp.</span></span> <span data-ttu-id="14320-108">*\<SIP domain name\>* SRV 记录，任何其他 SIP 联盟域都将能够 "发现" 您的联盟。</span><span class="sxs-lookup"><span data-stu-id="14320-108">*\<SIP domain name\>* SRV record, any other SIP federated domain will be able to “discover” your federation.</span></span> <span data-ttu-id="14320-109">通过使用 Lync Server 控制面板中的 "允许域和阻止域" 设置，或者通过使用 Lync Server Management Shell 和 **Get**、 **Set**、 **New**、 **CsAllowedDomain** 和 **-CsBlockedDomain** PowerShell cmdlet 设置允许或阻止的域配置，可以控制哪些联盟域可以与你进行通信。</span><span class="sxs-lookup"><span data-stu-id="14320-109">You can control which federated domains can communicate with you by using the Allows domains and Blocked Domains settings in the Lync Server Control Panel, or by setting the allowed or blocked domains configuration using the Lync Server Management Shell and the **Get**, **Set**, **New**, **Remove-CsAllowedDomain** and **-CsBlockedDomain** PowerShell cmdlets.</span></span> <span data-ttu-id="14320-110">有关如何配置这些设置以及如何使用 PowerShell cmdlet 的其他信息，请参阅本主题末尾的 **相关主题** 。</span><span class="sxs-lookup"><span data-stu-id="14320-110">For additional information on how to configure theses settings and the use of the PowerShell cmdlets, see **Related Topics** at the end of this topic.</span></span>

<span data-ttu-id="14320-111">"DNS 记录" 摘要表描述了开放的或可发现的联盟的必需条目。</span><span class="sxs-lookup"><span data-stu-id="14320-111">The DNS records summary table depicts the required entries for an open, or discoverable, federation.</span></span> <span data-ttu-id="14320-112">如果您不想实现联合发现，则可以决定不配置 \_ sipfederationtls。 \_tcp-out.</span><span class="sxs-lookup"><span data-stu-id="14320-112">If you do not want to implement Federation Discovery, You can decide to not configure the \_sipfederationtls.\_tcp.</span></span> <span data-ttu-id="14320-113">*\<SIP domain name\>* 录制.</span><span class="sxs-lookup"><span data-stu-id="14320-113">*\<SIP domain name\>* record.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="14320-114">在某些特定情况下，您必须拥有 _sipfederationtls _tcp。</span><span class="sxs-lookup"><span data-stu-id="14320-114">There are specific scenarios in which you must have the _sipfederationtls._tcp.</span></span> <span data-ttu-id="14320-115"><EM> &lt; SIP 域名 &gt; </EM> SRV 记录，但不希望具有可发现的联盟。</span><span class="sxs-lookup"><span data-stu-id="14320-115"><EM>&lt;SIP domain name&gt;</EM> SRV record, but you do not want to have a discoverable federation.</span></span> <span data-ttu-id="14320-116">其中一个实例是为用户部署移动性的位置。</span><span class="sxs-lookup"><span data-stu-id="14320-116">One such instance is where you have deployed mobility for your users.</span></span> <span data-ttu-id="14320-117">移动推送通知交换所 (PNCH) 是一种特殊类型的联盟，用于 Apple iPhone 或 2010 iPad 上使用 lync 2010 移动客户端或使用 lync 2013 移动客户端或 Windows Phone 的 Microsoft Lync 移动客户端。</span><span class="sxs-lookup"><span data-stu-id="14320-117">The mobility push notification clearinghouse (PNCH) is a special type of federation that is used for Microsoft Lync Mobile clients on Apple iPhone or iPad using the Lync 2010 Mobile client or Windows Phone using the Lync 2010 Mobile or Lync 2013 Mobile clients.</span></span> <span data-ttu-id="14320-118">_Sipfederationtls。 _tcp。</span><span class="sxs-lookup"><span data-stu-id="14320-118">The _sipfederationtls._tcp.</span></span> <span data-ttu-id="14320-119"><EM> &lt; SIP 域名称 &gt; </EM> SRV 记录在移动性和推送通知的情况下使用。</span><span class="sxs-lookup"><span data-stu-id="14320-119"><EM>&lt;SIP domain name&gt;</EM> SRV record is used in the case of mobility and push notification.</span></span> <span data-ttu-id="14320-120">若要缓解此问题并控制你的发现，请清除 " <STRONG>启用合作伙伴域发现</STRONG> " 设置以关闭发现。</span><span class="sxs-lookup"><span data-stu-id="14320-120">To mitigate this issue and control your discoverability, clear the setting <STRONG>Enable partner domain discovery</STRONG> to turn off discovery.</span></span>



</div>

<span data-ttu-id="14320-121">若要配置可扩展消息和状态协议 (XMPP) 对于你的部署，你将在外部 DNS 服务器中创建两个域名系统 (DNS) 记录，该 DNS 服务器会将记录解析为 Edge 服务器或边缘池的访问边缘服务。</span><span class="sxs-lookup"><span data-stu-id="14320-121">To configure extensible messaging and presence protocol (XMPP) for your deployment, you create two domain name system (DNS) records in an external DNS server that will resolve the records to the Access Edge service of your Edge Server or Edge pool.</span></span>

<span data-ttu-id="14320-122">将域名系统配置 (用于公共即时消息连接的 DNS) 时，你将发现支持外部用户的配置将支持公用 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="14320-122">When you configure domain name system (DNS) for public instant messaging connectivity, you will find that the configuration that supports external users will support public IM connectivity.</span></span> <span data-ttu-id="14320-123">如果你已配置了 Edge 服务器或边缘池，则应具有支持公用 IM 连接所必需的 DNS 记录。</span><span class="sxs-lookup"><span data-stu-id="14320-123">If you have already configured your Edge Server or Edge pool, you should have the DNS records necessary to support public IM connectivity.</span></span>

<div>

## <a name="dns-summary---sip-federation-including-public-instant-messaging-connectivity"></a><span data-ttu-id="14320-124">DNS 摘要-SIP 联盟，包括公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="14320-124">DNS Summary - SIP Federation including Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14320-125">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="14320-125">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="14320-126">FQDN</span><span class="sxs-lookup"><span data-stu-id="14320-126">FQDN</span></span></th>
<th><span data-ttu-id="14320-127">IP 地址/FQDN 主机记录</span><span class="sxs-lookup"><span data-stu-id="14320-127">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="14320-128">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="14320-128">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14320-129">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="14320-129">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="14320-130">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="14320-130">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="14320-131">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="14320-131">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="14320-132">Access Edge 服务外部接口，将联合身份验证自动 DNS 发现到其他潜在的联合合作伙伴，并称为 "允许的 SIP 域" (在以前版本的版本中称为 "增强联盟") 。根据需要对启用了 Lync 的用户的所有 SIP 域重复此操作</span><span class="sxs-lookup"><span data-stu-id="14320-132">Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="14320-133">移动和推送通知交换所需要此 SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="14320-133">This SRV record is required for mobility and the push notification clearing house.</span></span> <span data-ttu-id="14320-134">在有多个 SIP 域的情况下，为将具有 Lync 移动客户端的每个域创建和发布 SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="14320-134">In cases where there is more than one SIP domain, create and publish an SRV record for each domain that will have Lync Mobile clients.</span></span> <span data-ttu-id="14320-135">如果部署支持的每个 SIP 域没有明确的 SRV 记录，则推送通知服务和 Apple 推送通知服务可能不会按预期运行。</span><span class="sxs-lookup"><span data-stu-id="14320-135">The Push Notification Service and Apple Push Notification service may not operate as expected if there is not an explicit SRV record for each SIP domain that the deployment supports.</span></span>

</td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="14320-136">DNS 摘要-可扩展消息和状态协议 (XMPP) </span><span class="sxs-lookup"><span data-stu-id="14320-136">DNS Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14320-137">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="14320-137">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="14320-138">FQDN</span><span class="sxs-lookup"><span data-stu-id="14320-138">FQDN</span></span></th>
<th><span data-ttu-id="14320-139">IP 地址/FQDN 主机记录</span><span class="sxs-lookup"><span data-stu-id="14320-139">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="14320-140">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="14320-140">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14320-141">外部 DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="14320-141">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="14320-142">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="14320-142">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="14320-143">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="14320-143">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="14320-144">"访问边缘服务" 或 "边缘池" 上的 XMPP 代理外部接口。对于启用了 Lync 的用户，通过全局策略、用户所在的网站策略或应用到启用了 Lync 的用户的用户策略，可以为所有内部 SIP 域重复此操作。</span><span class="sxs-lookup"><span data-stu-id="14320-144">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="14320-145">还必须在 XMPP 联盟合作伙伴策略中配置允许的 XMPP 域。</span><span class="sxs-lookup"><span data-stu-id="14320-145">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="14320-146">有关其他详细信息，请参阅 <strong>另请参阅</strong> 中的主题</span><span class="sxs-lookup"><span data-stu-id="14320-146">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14320-147">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="14320-147">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="14320-148">xmpp.contoso.com (例如) </span><span class="sxs-lookup"><span data-stu-id="14320-148">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="14320-149">边缘服务器上的访问边缘服务的 IP 地址或托管 XMPP 代理的边缘池的 IP 地址</span><span class="sxs-lookup"><span data-stu-id="14320-149">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="14320-150">指向托管 XMPP 代理服务的访问边缘服务或边缘池。</span><span class="sxs-lookup"><span data-stu-id="14320-150">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="14320-151">通常，你创建的 SRV 记录将指向此主机 (A 或 AAAA) 记录</span><span class="sxs-lookup"><span data-stu-id="14320-151">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="14320-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14320-152">See Also</span></span>


[<span data-ttu-id="14320-153">在 Lync Server 2013 中设置 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="14320-153">Setting up XMPP federation in Lync Server 2013</span></span>](lync-server-2013-setting-up-xmpp-federation.md)  
[<span data-ttu-id="14320-154">在 Lync Server 2013 中配置推送通知</span><span class="sxs-lookup"><span data-stu-id="14320-154">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
[<span data-ttu-id="14320-155">在 Lync Server 2013 中启用或禁用联盟伙伴发现</span><span class="sxs-lookup"><span data-stu-id="14320-155">Enable or disable discovery of federation partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)  


[<span data-ttu-id="14320-156">Lync Server 2013 中的外部用户访问方案</span><span class="sxs-lookup"><span data-stu-id="14320-156">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="14320-157">确定 Lync Server 2013 的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="14320-157">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="14320-158">在 Lync Server 2013 中管理组织的 SIP 联盟域</span><span class="sxs-lookup"><span data-stu-id="14320-158">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
  

<span data-ttu-id="14320-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14320-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

