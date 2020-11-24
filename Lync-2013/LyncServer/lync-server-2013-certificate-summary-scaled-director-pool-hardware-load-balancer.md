---
title: 证书摘要 - 扩展的控制器池、硬件负载平衡器
description: 证书摘要-缩放的控制器池、硬件负载平衡器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08abc37940cd41a29d6620cfc0a2a801de4a8e38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392239"
---
# <a name="certificate-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="34ce1-103">Lync Server 2013 中的证书摘要 - 扩展的控制器池、硬件负载平衡器</span><span class="sxs-lookup"><span data-stu-id="34ce1-103">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34ce1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34ce1-104">

<span> </span></span></span>

<span data-ttu-id="34ce1-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="34ce1-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="34ce1-106">带有硬件负载平衡器的 Director 的证书要求将使用一个默认证书，该默认证书具有 "接受方名称" 和 "使用者备用名称"，用于控制器池可以接收的服务。</span><span class="sxs-lookup"><span data-stu-id="34ce1-106">Certificate requirements for a Director with a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director pool can receive.</span></span> <span data-ttu-id="34ce1-107">为池中的每个 Director 请求一个证书。</span><span class="sxs-lookup"><span data-stu-id="34ce1-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="34ce1-108">此外，在每台服务器上安装了服务器到服务器身份验证用途的 OAuth 令牌证书。</span><span class="sxs-lookup"><span data-stu-id="34ce1-108">Additionally there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-a-scaled-director-using-a-hardware-load-balancer"></a><span data-ttu-id="34ce1-109">使用硬件负载平衡器的缩放控制器的证书</span><span class="sxs-lookup"><span data-stu-id="34ce1-109">Certificates for a Scaled Director Using a Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34ce1-110">组件</span><span class="sxs-lookup"><span data-stu-id="34ce1-110">Component</span></span></th>
<th><span data-ttu-id="34ce1-111">使用者名称 (SN)</span><span class="sxs-lookup"><span data-stu-id="34ce1-111">Subject name (SN)</span></span></th>
<th><span data-ttu-id="34ce1-112"> (SAN) 的使用者备用名称</span><span class="sxs-lookup"><span data-stu-id="34ce1-112">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="34ce1-113">备注</span><span class="sxs-lookup"><span data-stu-id="34ce1-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34ce1-114">默认</span><span class="sxs-lookup"><span data-stu-id="34ce1-114">Default</span></span></p></td>
<td><p><span data-ttu-id="34ce1-115">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="34ce1-115">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="34ce1-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="34ce1-116">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="34ce1-117">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="34ce1-117">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="34ce1-118">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="34ce1-118">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="34ce1-119">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="34ce1-119">meet.contoso.com</span></span></p>
<p><span data-ttu-id="34ce1-120">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="34ce1-120">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="34ce1-121">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="34ce1-121">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="34ce1-122"> (（可选）)\ * contoso.com</span><span class="sxs-lookup"><span data-stu-id="34ce1-122">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="34ce1-123">可以从内部托管的证书颁发机构 (CA) 或公共 CA 请求控制器证书。</span><span class="sxs-lookup"><span data-stu-id="34ce1-123">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="34ce1-124">控制器在来自外围服务器或从边缘服务器中响应来自反向代理的请求。</span><span class="sxs-lookup"><span data-stu-id="34ce1-124">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span></p>
<p><span data-ttu-id="34ce1-125">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="34ce1-125">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34ce1-126">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="34ce1-126">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="34ce1-127">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="34ce1-127">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="34ce1-128">无条目</span><span class="sxs-lookup"><span data-stu-id="34ce1-128">No Entry</span></span></p></td>
<td>


> [!IMPORTANT]
> <span data-ttu-id="34ce1-129">请注意，最小键长度为1024，但你可能会收到一条警告，指出推荐的最小密钥长度为2048位。</span><span class="sxs-lookup"><span data-stu-id="34ce1-129">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


<p><span data-ttu-id="34ce1-130">OAuthTokenIssuer 证书是单一用途的证书，用于在大规模环境中验证服务器，并且可以从内部 CA 或公共 CA 请求。</span><span class="sxs-lookup"><span data-stu-id="34ce1-130">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="34ce1-131">证书是必需的。</span><span class="sxs-lookup"><span data-stu-id="34ce1-131">The certificate is required.</span></span></p><span data-ttu-id="34ce1-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34ce1-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

