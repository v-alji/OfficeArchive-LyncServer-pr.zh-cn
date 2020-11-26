---
title: Lync Server 2013：证书摘要 - 已进行 DNS 和 HLB 负载平衡
description: Lync Server 2013：证书摘要-已平衡的 DNS 和 HLB 负载。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - DNS and HLB load balanced
ms:assetid: 8318a1a4-b423-47b7-95e6-9541adfad391
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205047(v=OCS.15)
ms:contentKeyID: 48184676
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 97a89975af16b6e39625677f787d3726f00c76c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435318"
---
# <a name="certificate-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="a02e2-103">Lync Server 2013 中的证书摘要 - 已进行 DNS 和 HLB 负载平衡</span><span class="sxs-lookup"><span data-stu-id="a02e2-103">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a02e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a02e2-104">

<span> </span></span></span>

<span data-ttu-id="a02e2-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="a02e2-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="a02e2-106">具有 DNS 负载平衡和硬件负载平衡器的 Director 的证书要求将使用一个默认证书，该默认证书具有适用于 Director 可接收的服务的主题名称和使用者备用名称。</span><span class="sxs-lookup"><span data-stu-id="a02e2-106">Certificate requirements for a Director with DNS load balancing and a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="a02e2-107">为池中的每个 Director 请求一个证书。</span><span class="sxs-lookup"><span data-stu-id="a02e2-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="a02e2-108">请务必记住，硬件负载平衡器仅负载平衡来自反向代理的流量。</span><span class="sxs-lookup"><span data-stu-id="a02e2-108">It is important to remember that the hardware load balancer is load balancing only the traffic from the reverse proxy.</span></span> <span data-ttu-id="a02e2-109">此外，在每台服务器上安装了服务器到服务器身份验证用途的 OAuth 令牌证书。</span><span class="sxs-lookup"><span data-stu-id="a02e2-109">Additionally, there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="a02e2-110">Director 的证书</span><span class="sxs-lookup"><span data-stu-id="a02e2-110">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a02e2-111">组件</span><span class="sxs-lookup"><span data-stu-id="a02e2-111">Component</span></span></th>
<th><span data-ttu-id="a02e2-112">使用者名称 (SN)</span><span class="sxs-lookup"><span data-stu-id="a02e2-112">Subject name (SN)</span></span></th>
<th><span data-ttu-id="a02e2-113"> (SAN) 的使用者备用名称</span><span class="sxs-lookup"><span data-stu-id="a02e2-113">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="a02e2-114">备注</span><span class="sxs-lookup"><span data-stu-id="a02e2-114">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a02e2-115">默认</span><span class="sxs-lookup"><span data-stu-id="a02e2-115">Default</span></span></p></td>
<td><p><span data-ttu-id="a02e2-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a02e2-116">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a02e2-117">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a02e2-117">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="a02e2-118">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a02e2-118">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="a02e2-119">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a02e2-119">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="a02e2-120">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a02e2-120">meet.contoso.com</span></span></p>
<p><span data-ttu-id="a02e2-121">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a02e2-121">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="a02e2-122">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a02e2-122">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="a02e2-123"> (（可选）)\ * contoso.com</span><span class="sxs-lookup"><span data-stu-id="a02e2-123">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a02e2-124">可以从内部托管的证书颁发机构 (CA) 或公共 CA 请求控制器证书。</span><span class="sxs-lookup"><span data-stu-id="a02e2-124">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="a02e2-125">控制器在来自外围服务器或从边缘服务器中响应来自反向代理的请求。</span><span class="sxs-lookup"><span data-stu-id="a02e2-125">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="a02e2-126">内部客户端将不使用 Director。</span><span class="sxs-lookup"><span data-stu-id="a02e2-126">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="a02e2-127">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="a02e2-127">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a02e2-128">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="a02e2-128">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="a02e2-129">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a02e2-129">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a02e2-130">无条目</span><span class="sxs-lookup"><span data-stu-id="a02e2-130">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="a02e2-131">请注意，最小键长度为1024，但你可能会收到一条警告，指出推荐的最小密钥长度为2048位。</span><span class="sxs-lookup"><span data-stu-id="a02e2-131">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="a02e2-132">OAuthTokenIssuer 证书是单一用途的证书，用于在大规模环境中验证服务器，并且可以从内部 CA 或公共 CA 请求。</span><span class="sxs-lookup"><span data-stu-id="a02e2-132">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="a02e2-133">证书是必需的。</span><span class="sxs-lookup"><span data-stu-id="a02e2-133">The certificate is required.</span></span></p><span data-ttu-id="a02e2-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a02e2-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

