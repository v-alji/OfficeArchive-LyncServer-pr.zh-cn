---
title: Lync Server 2013：DNS 摘要 - 单一控制器
description: Lync Server 2013： DNS 摘要-单控制器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Single Director
ms:assetid: 790ecb56-92cd-41f4-baf6-c290a707aa4d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205021(v=OCS.15)
ms:contentKeyID: 48184568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78ef19383df45644ad951ca5da69ef893b231980
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391748"
---
# <a name="dns-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="eb4cb-103">Lync Server 2013 中的 DNS 摘要 - 单一控制器</span><span class="sxs-lookup"><span data-stu-id="eb4cb-103">DNS summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb4cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb4cb-104">

<span> </span></span></span>

<span data-ttu-id="eb4cb-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="eb4cb-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="eb4cb-106">下表包含支持单个控制器所需的 DNS 记录的摘要。</span><span class="sxs-lookup"><span data-stu-id="eb4cb-106">The following table contains a summary of the DNS records that are required to support the single Director.</span></span> <span data-ttu-id="eb4cb-107">Director 的角色需要类似的 DNS 记录作为前端服务器。</span><span class="sxs-lookup"><span data-stu-id="eb4cb-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="eb4cb-108">所需的记录数反映在 Director 证书所需的主题备用名称中。</span><span class="sxs-lookup"><span data-stu-id="eb4cb-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="eb4cb-109">与前端服务器不同，控制器不会托管用户帐户或托管移动服务。</span><span class="sxs-lookup"><span data-stu-id="eb4cb-109">Different from the Front End Server, the Director does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director"></a><span data-ttu-id="eb4cb-110">Director 所需的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="eb4cb-110">DNS Records Required for the Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb4cb-111">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="eb4cb-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="eb4cb-112">FQDN/DNS 记录</span><span class="sxs-lookup"><span data-stu-id="eb4cb-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="eb4cb-113">IP 地址/FQDN</span><span class="sxs-lookup"><span data-stu-id="eb4cb-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="eb4cb-114">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="eb4cb-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb4cb-115">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb4cb-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="eb4cb-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-117">控制器</span><span class="sxs-lookup"><span data-stu-id="eb4cb-117">Director</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-118">用于复制和服务器到服务器的控制器主机记录</span><span class="sxs-lookup"><span data-stu-id="eb4cb-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb4cb-119">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb4cb-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-120">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb4cb-120">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-121">控制器</span><span class="sxs-lookup"><span data-stu-id="eb4cb-121">Director</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-122">从边缘服务器的内部边缘界面 (SIP) 的入站会话初始协议</span><span class="sxs-lookup"><span data-stu-id="eb4cb-122">Inbound session initiation protocol (SIP) from the internal Edge interface of the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb4cb-123">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb4cb-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-124">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb4cb-124">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-125">控制器</span><span class="sxs-lookup"><span data-stu-id="eb4cb-125">Director</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-126">从反向代理已发布的拨入 web 服务</span><span class="sxs-lookup"><span data-stu-id="eb4cb-126">Published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb4cb-127">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb4cb-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-128">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb4cb-128">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-129">控制器</span><span class="sxs-lookup"><span data-stu-id="eb4cb-129">Director</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-130">已发布通过反向代理的 web 服务</span><span class="sxs-lookup"><span data-stu-id="eb4cb-130">Published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb4cb-131">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="eb4cb-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-132">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eb4cb-132">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-133">控制器</span><span class="sxs-lookup"><span data-stu-id="eb4cb-133">Director</span></span></p></td>
<td><p><span data-ttu-id="eb4cb-134">由 "反向代理 Web 票" 发布和定义的由 Director 的外部 web 服务</span><span class="sxs-lookup"><span data-stu-id="eb4cb-134">Published and defined by the reverse proxy Web Ticket external web services for the Director</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="eb4cb-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb4cb-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

