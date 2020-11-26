---
title: Lync Server 2013：证书摘要 - 单一控制器
description: Lync Server 2013：证书摘要-单控制器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Single Director
ms:assetid: 1b769a76-cbf3-46e9-a955-f6cde5faff93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204720(v=OCS.15)
ms:contentKeyID: 48183546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cf930a73d9989ec44f52f1d70ee9e0f900e4d6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435192"
---
# <a name="certificate-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="d6910-103">Lync Server 2013 中的证书摘要 - 单一控制器</span><span class="sxs-lookup"><span data-stu-id="d6910-103">Certificate summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6910-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6910-104">

<span> </span></span></span>

<span data-ttu-id="d6910-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="d6910-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="d6910-106">单个控制器的证书要求包括一个默认证书，该证书为 Director 可以接收的服务提供了主题名称和使用者备用名称。</span><span class="sxs-lookup"><span data-stu-id="d6910-106">Certificate requirements for a single Director consist of a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="d6910-107">此外，还有一个用于服务器到服务器身份验证的 OAuth 令牌证书。</span><span class="sxs-lookup"><span data-stu-id="d6910-107">Additionally, there is an OAuth Token certificate for server to server authentication purposes.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="d6910-108">Director 的证书</span><span class="sxs-lookup"><span data-stu-id="d6910-108">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6910-109">组件</span><span class="sxs-lookup"><span data-stu-id="d6910-109">Component</span></span></th>
<th><span data-ttu-id="d6910-110">使用者名称 (SN)</span><span class="sxs-lookup"><span data-stu-id="d6910-110">Subject name (SN)</span></span></th>
<th><span data-ttu-id="d6910-111"> (SAN) 的使用者备用名称</span><span class="sxs-lookup"><span data-stu-id="d6910-111">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="d6910-112">备注</span><span class="sxs-lookup"><span data-stu-id="d6910-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6910-113">默认</span><span class="sxs-lookup"><span data-stu-id="d6910-113">Default</span></span></p></td>
<td><p><span data-ttu-id="d6910-114">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d6910-114">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="d6910-115">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d6910-115">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="d6910-116">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6910-116">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="d6910-117">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6910-117">meet.contoso.com</span></span></p>
<p><span data-ttu-id="d6910-118">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6910-118">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="d6910-119">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6910-119">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="d6910-120"> (（可选）)\ * contoso.com</span><span class="sxs-lookup"><span data-stu-id="d6910-120">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d6910-121">可以从内部托管的证书颁发机构 (CA) 或公共 CA 请求控制器证书。</span><span class="sxs-lookup"><span data-stu-id="d6910-121">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="d6910-122">控制器在来自外围服务器或从边缘服务器中响应来自反向代理的请求。</span><span class="sxs-lookup"><span data-stu-id="d6910-122">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="d6910-123">内部客户端将不使用 Director。</span><span class="sxs-lookup"><span data-stu-id="d6910-123">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="d6910-124">或者是简单 Url 的通配符条目</span><span class="sxs-lookup"><span data-stu-id="d6910-124">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6910-125">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="d6910-125">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="d6910-126">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d6910-126">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="d6910-127">无条目</span><span class="sxs-lookup"><span data-stu-id="d6910-127">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="d6910-128">请注意，最小键长度为1024，但你可能会收到一条警告，指出推荐的最小密钥长度为2048位。</span><span class="sxs-lookup"><span data-stu-id="d6910-128">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="d6910-129">OAuthTokenIssuer 证书是单一用途的证书，用于在大规模环境中验证服务器，并且可以从内部 CA 或公共 CA 请求。</span><span class="sxs-lookup"><span data-stu-id="d6910-129">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="d6910-130">证书是必需的。</span><span class="sxs-lookup"><span data-stu-id="d6910-130">The certificate is required.</span></span></p><span data-ttu-id="d6910-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6910-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

