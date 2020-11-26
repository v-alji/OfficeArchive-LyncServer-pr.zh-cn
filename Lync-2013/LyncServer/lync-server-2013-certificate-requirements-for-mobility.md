---
title: Lync Server 2013：移动的证书要求
description: Lync Server 2013：移动性的证书要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for mobility
ms:assetid: bb0e97af-cf60-4271-a0ab-654429d884ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690044(v=OCS.15)
ms:contentKeyID: 48185251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51af74b3efc1ffcb4fe38d7431e315f9b55af943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435360"
---
# <a name="certificate-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="a4cd4-103">Lync Server 2013 中移动的证书要求</span><span class="sxs-lookup"><span data-stu-id="a4cd4-103">Certificate requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4cd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4cd4-104">

<span> </span></span></span>

<span data-ttu-id="a4cd4-105">_**主题上次修改时间：** 2012-06-24_</span><span class="sxs-lookup"><span data-stu-id="a4cd4-105">_**Topic Last Modified:** 2012-06-24_</span></span>

<span data-ttu-id="a4cd4-106">如果你部署移动版功能并支持自动发现移动客户端，你需要在证书上包含特定主题备用名称条目以支持来自移动客户端的安全连接。</span><span class="sxs-lookup"><span data-stu-id="a4cd4-106">If you deploy the mobility feature and support automatic discovery for mobile clients, you need to include certain subject alternative name entries on certificates to support secure connections from the mobile clients.</span></span>

<span data-ttu-id="a4cd4-107">您需要在以下证书上包含 "使用者备用名称" 条目以自动发现：</span><span class="sxs-lookup"><span data-stu-id="a4cd4-107">You need to include subject alternative name entries for automatic discovery on the following certificates:</span></span>

  - <span data-ttu-id="a4cd4-108">控制器池</span><span class="sxs-lookup"><span data-stu-id="a4cd4-108">Director pool</span></span>

  - <span data-ttu-id="a4cd4-109">前端池</span><span class="sxs-lookup"><span data-stu-id="a4cd4-109">Front End pool</span></span>

  - <span data-ttu-id="a4cd4-110">反向代理</span><span class="sxs-lookup"><span data-stu-id="a4cd4-110">Reverse proxy</span></span>

<span data-ttu-id="a4cd4-111">本部分介绍自动发现证书所需的主题备用名称条目。</span><span class="sxs-lookup"><span data-stu-id="a4cd4-111">This section describes the subject alternative name entries that are required on your certificates for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a4cd4-112">通过使用内部证书颁发机构重新发起证书通常是一个简单的过程，但向反向代理使用的公共证书添加多个主题备用名称条目可能会很高。</span><span class="sxs-lookup"><span data-stu-id="a4cd4-112">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="a4cd4-113">如果您有多个 SIP 域，增加了使用者备用名称的费用，您可以将反向代理配置为对初始自动发现服务请求使用 HTTP，而不是使用 HTTPS (默认配置) 。</span><span class="sxs-lookup"><span data-stu-id="a4cd4-113">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to use HTTP for the initial Autodiscover Service request, instead of using HTTPS (the default configuration).</span></span> <span data-ttu-id="a4cd4-114">有关详细信息，请参阅 <A href="lync-server-2013-technical-requirements-for-mobility.md">Lync Server 2013 中的移动技术要求</A>。</span><span class="sxs-lookup"><span data-stu-id="a4cd4-114">For details, see <A href="lync-server-2013-technical-requirements-for-mobility.md">Technical requirements for mobility in Lync Server 2013</A>.</span></span>



</div>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="a4cd4-115">控制器池证书要求</span><span class="sxs-lookup"><span data-stu-id="a4cd4-115">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4cd4-116">说明</span><span class="sxs-lookup"><span data-stu-id="a4cd4-116">Description</span></span></th>
<th><span data-ttu-id="a4cd4-117">主题可选名称条目</span><span class="sxs-lookup"><span data-stu-id="a4cd4-117">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4cd4-118">内部自动发现服务 URL</span><span class="sxs-lookup"><span data-stu-id="a4cd4-118">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="a4cd4-119">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="a4cd4-119">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4cd4-120">外部自动发现服务 URL</span><span class="sxs-lookup"><span data-stu-id="a4cd4-120">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="a4cd4-121">SAN=lyncdiscover.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="a4cd4-121">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a4cd4-122">或者，您可以使用 SAN = \*。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="a4cd4-122">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="a4cd4-123">前端池证书要求</span><span class="sxs-lookup"><span data-stu-id="a4cd4-123">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4cd4-124">说明</span><span class="sxs-lookup"><span data-stu-id="a4cd4-124">Description</span></span></th>
<th><span data-ttu-id="a4cd4-125">主题可选名称条目</span><span class="sxs-lookup"><span data-stu-id="a4cd4-125">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4cd4-126">内部自动发现服务 URL</span><span class="sxs-lookup"><span data-stu-id="a4cd4-126">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="a4cd4-127">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="a4cd4-127">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4cd4-128">外部自动发现服务 URL</span><span class="sxs-lookup"><span data-stu-id="a4cd4-128">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="a4cd4-129">SAN=lyncdiscover.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="a4cd4-129">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a4cd4-130">或者，您可以使用 SAN = \*。 &lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="a4cd4-130">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="a4cd4-131">反向代理 (公共 CA) 证书要求</span><span class="sxs-lookup"><span data-stu-id="a4cd4-131">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4cd4-132">说明</span><span class="sxs-lookup"><span data-stu-id="a4cd4-132">Description</span></span></th>
<th><span data-ttu-id="a4cd4-133">主题可选名称条目</span><span class="sxs-lookup"><span data-stu-id="a4cd4-133">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4cd4-134">外部自动发现服务 URL</span><span class="sxs-lookup"><span data-stu-id="a4cd4-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="a4cd4-135">SAN=lyncdiscover.&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="a4cd4-135">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a4cd4-136">将此 SAN 分配给分配给反向代理上的 SSL 侦听器的证书。</span><span class="sxs-lookup"><span data-stu-id="a4cd4-136">You assign this SAN to the certificate assigned to the SSL Listener on the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="a4cd4-137">反向代理侦听器将具有你的外部 Web 服务 URL 的主题备用名称 (s)  (例如，SAN = lyncwebextpool01 和 dirwebexternal.contoso.com （如果已部署可选的 Director) ）。</span><span class="sxs-lookup"><span data-stu-id="a4cd4-137">Your reverse proxy listener will have subject alternative names for your external Web Services URL(s) (for example, SAN=lyncwebextpool01.contoso.com, and dirwebexternal.contoso.com if you have deployed the optional Director).</span></span>



<span data-ttu-id="a4cd4-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4cd4-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

