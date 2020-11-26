---
title: 证书摘要-SIP、XMPP 联盟和公共即时消息
description: 证书摘要-SIP、XMPP 联盟和公共即时消息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - SIP, XMPP federation, and public instant messaging
ms:assetid: 933d6351-cfa6-4432-b3ed-1aff3ac92065
ms:mtpsurl: https://technet.microsoft.com/library/JJ618372(v=OCS.15)
ms:contentKeyID: 49105659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565d3b935d304aa09588688bd8d71948b1b3ec3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435185"
---
# <a name="certificate-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="a5aad-103">证书摘要-Lync Server 2013 中的 SIP、XMPP 联盟和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="a5aad-103">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5aad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5aad-104">

<span> </span></span></span>

<span data-ttu-id="a5aad-105">_**主题上次修改时间：** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="a5aad-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="a5aad-106">您所需要的用于与 Microsoft Lync Server 2013、Lync Server 2010 和 Office 通信服务器进行联盟的证书通常由您配置、请求和分配给 Edge 服务器的证书满足。</span><span class="sxs-lookup"><span data-stu-id="a5aad-106">The certificates that you need for federating with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server will typically be met by the certificates that you configure, request and assign to your Edge Server.</span></span>

<span data-ttu-id="a5aad-107">启用和建立与可扩展消息和状态协议 (XMPP 的证书要求) 合作伙伴需要为 XMPP 域添加条目。</span><span class="sxs-lookup"><span data-stu-id="a5aad-107">Certificate requirements for enabling and establishing communications with extensible messaging and presence protocol (XMPP) partners require addition of entries for your XMPP domains.</span></span> <span data-ttu-id="a5aad-108">在证书上作为主题备用名称包含 (SAN) 的记录将是可参与 XMPP 通信的域。</span><span class="sxs-lookup"><span data-stu-id="a5aad-108">The record that is included on the certificate as a subject alternative name (SAN) will be the domain that can participate in XMPP communications.</span></span> <span data-ttu-id="a5aad-109">域可以是根级别的域 (例如，contoso.com) 如果你想要为整个域启用 XMPP，或者可以选择子域 (例如，corp.contoso.com、finance.contoso.com) 如果要为用户的子集启用 XMPP。</span><span class="sxs-lookup"><span data-stu-id="a5aad-109">The domain can be the root-level domain (for example, contoso.com) if you want to enable XMPP for your entire domain, or can be selected child domains (for example, corp.contoso.com, finance.contoso.com) if you are enabling XMPP for a subset of users.</span></span>

<span data-ttu-id="a5aad-110">若要配置公共即时消息连接的证书，请注意，与其他 SIP 联合身份验证类型或即使是标准边缘服务器证书没有什么不同，除了北美网络 (AOL) 需要证书或证书 (边缘池的情况下，) 也包含客户端 EKU。</span><span class="sxs-lookup"><span data-stu-id="a5aad-110">To configure certificates for public Instant Messaging connectivity, note that there is nothing different from other SIP federation types or even standard Edge Server certificates, except that America Online (AOL) requires a the certificate or certificates (in the case of an Edge pool) to also contain the client EKU.</span></span> <span data-ttu-id="a5aad-111">客户端 EKU 是证书的补充，并且是分配给 Edge 服务器的外部公共证书的一部分。</span><span class="sxs-lookup"><span data-stu-id="a5aad-111">The client EKU is an addition to the certificate, and is part of the external public certificate that is assigned to your Edge Server.</span></span>

<span data-ttu-id="a5aad-112">若要确认你已满足 Edge 服务器部署的正确证书要求，请查看标题为 " **另请参阅**" 的部分中列出的主题。</span><span class="sxs-lookup"><span data-stu-id="a5aad-112">To confirm that you have met the correct certificate requirements for your Edge Server deployment, review the topics listed in the section titled **See Also**.</span></span>

<div>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5aad-113">组件</span><span class="sxs-lookup"><span data-stu-id="a5aad-113">Component</span></span></th>
<th><span data-ttu-id="a5aad-114">主题名称</span><span class="sxs-lookup"><span data-stu-id="a5aad-114">Subject name</span></span></th>
<th><span data-ttu-id="a5aad-115"> (SAN) 的使用者备用名称</span><span class="sxs-lookup"><span data-stu-id="a5aad-115">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="a5aad-116">备注</span><span class="sxs-lookup"><span data-stu-id="a5aad-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5aad-117">外部/访问边缘</span><span class="sxs-lookup"><span data-stu-id="a5aad-117">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="a5aad-118">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a5aad-118">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a5aad-119">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a5aad-119">sip.contoso.com</span></span></p>
<p><span data-ttu-id="a5aad-120">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a5aad-120">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="a5aad-121">contoso.com</span><span class="sxs-lookup"><span data-stu-id="a5aad-121">contoso.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="a5aad-122">若要支持 contoso.com XMPP 命名空间</span><span class="sxs-lookup"><span data-stu-id="a5aad-122">To support the contoso.com XMPP namespace</span></span>


<p><span data-ttu-id="a5aad-123">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="a5aad-123">sip.fabrikam.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="a5aad-124">支持 fabrikam.com SIP 命名空间</span><span class="sxs-lookup"><span data-stu-id="a5aad-124">To support the fabrikam.com SIP namespace</span></span>


<p><span data-ttu-id="a5aad-125">fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="a5aad-125">fabrikam.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="a5aad-126">若要支持 fabrikam.com XMPP 命名空间</span><span class="sxs-lookup"><span data-stu-id="a5aad-126">To support the fabrikam.com XMPP namespace</span></span>

</td>
<td><p><span data-ttu-id="a5aad-127">证书必须来自公共 CA，并且必须具有服务器 EKU 和客户端 EKU，前提是要部署与 AOL 的公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="a5aad-127">The certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="a5aad-128">证书已分配给以下对象的外部边缘服务器接口：</span><span class="sxs-lookup"><span data-stu-id="a5aad-128">The certificate is assigned to the external Edge Server interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="a5aad-129">访问边缘服务</span><span class="sxs-lookup"><span data-stu-id="a5aad-129">Access Edge service</span></span></p></li>
<li><p><span data-ttu-id="a5aad-130">Web 会议边缘服务</span><span class="sxs-lookup"><span data-stu-id="a5aad-130">Web Conferencing Edge service</span></span></p></li>
<li><p><span data-ttu-id="a5aad-131">A/V 边缘服务</span><span class="sxs-lookup"><span data-stu-id="a5aad-131">A/V Edge service</span></span></p></li>
</ul>



> [!NOTE]
> <span data-ttu-id="a5aad-132">从技术上讲，证书未分配给 A/V 边缘。</span><span class="sxs-lookup"><span data-stu-id="a5aad-132">Technically, a certificate is not assigned to the A/V Edge.</span></span> <span data-ttu-id="a5aad-133">安全通信和身份验证通过媒体中继身份验证服务 (MRAS) 进行管理。</span><span class="sxs-lookup"><span data-stu-id="a5aad-133">Secure communication and authentication is managed by way of the Media Relay Authentication Service (MRAS).</span></span> <span data-ttu-id="a5aad-134">MRAS 使用分配给 Edge 服务器内部接口的证书。</span><span class="sxs-lookup"><span data-stu-id="a5aad-134">MRAS uses the certificate assigned to the Edge Server internal interface.</span></span>


<p><span data-ttu-id="a5aad-135">请注意，San 会根据拓扑生成器中的定义自动添加到证书。</span><span class="sxs-lookup"><span data-stu-id="a5aad-135">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="a5aad-136">根据需要为其他 SIP 域和其他需要支持的条目添加 SAN 条目。</span><span class="sxs-lookup"><span data-stu-id="a5aad-136">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="a5aad-137">主题名称是在 SAN 中复制的，并且必须存在才能正确操作。</span><span class="sxs-lookup"><span data-stu-id="a5aad-137">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a5aad-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a5aad-138">See Also</span></span>


[<span data-ttu-id="a5aad-139">Lync Server 2013 中的示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="a5aad-139">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="a5aad-140">在 Lync Server 2013 中规划边缘服务器证书</span><span class="sxs-lookup"><span data-stu-id="a5aad-140">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  
[<span data-ttu-id="a5aad-141">Lync Server 2013 中的证书摘要 - 单一合并边缘（使用 NAT 通过专用 IP 地址进行）</span><span class="sxs-lookup"><span data-stu-id="a5aad-141">Certificate summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-private-ip-addresses-using-nat.md)  
[<span data-ttu-id="a5aad-142">Lync Server 2013 中的证书摘要 - 使用公用 IP 地址的单一合并边缘</span><span class="sxs-lookup"><span data-stu-id="a5aad-142">Certificate summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-public-ip-addresses.md)  
[<span data-ttu-id="a5aad-143">Lync Server 2013 中的证书摘要 - 扩展的合并边缘（使用 NAT 通过专用 IP 地址进行 DNS 负载平衡）</span><span class="sxs-lookup"><span data-stu-id="a5aad-143">Certificate summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-private-ip.md)  
[<span data-ttu-id="a5aad-144">Lync Server 2013 中的证书摘要 - 扩展的合并边缘（通过公用 IP 地址进行 DNS 负载平衡）</span><span class="sxs-lookup"><span data-stu-id="a5aad-144">Certificate summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)  
[<span data-ttu-id="a5aad-145">Lync Server 2013 中的证书摘要 - 使用硬件负载平衡器的扩展的合并边缘</span><span class="sxs-lookup"><span data-stu-id="a5aad-145">Certificate summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-with-hardware-load-balancers.md)  
  

<span data-ttu-id="a5aad-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5aad-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

