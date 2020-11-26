---
title: Lync Server 2013：DNS 摘要 - 反向代理
description: Lync Server 2013： DNS 摘要-反向代理。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Reverse proxy
ms:assetid: 3073affa-4d92-4453-9974-3a82ca0c6445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204781(v=OCS.15)
ms:contentKeyID: 48183755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc2d806893786a11317be1eff9bfdc08c9230bf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437719"
---
# <a name="dns-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="f1e98-103">Lync Server 2013 中的 DNS 摘要 - 反向代理</span><span class="sxs-lookup"><span data-stu-id="f1e98-103">DNS summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1e98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1e98-104">

<span> </span></span></span>

<span data-ttu-id="f1e98-105">_**主题上次修改时间：** 2013-03-22_</span><span class="sxs-lookup"><span data-stu-id="f1e98-105">_**Topic Last Modified:** 2013-03-22_</span></span>

<span data-ttu-id="f1e98-106">您在反向代理服务器中配置两个网络适配器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f1e98-106">You configure two network adapters in your reverse proxy as follows:</span></span>

<div>

## <a name="reverse-proxy-network-adapter-requirements"></a><span data-ttu-id="f1e98-107">反向代理网络适配器要求</span><span class="sxs-lookup"><span data-stu-id="f1e98-107">Reverse Proxy Network Adapter Requirements</span></span>

  - <span data-ttu-id="f1e98-108">**网络适配器 1 (内部接口)** 示例</span><span class="sxs-lookup"><span data-stu-id="f1e98-108">**Network adapter 1 (Internal Interface)** example</span></span>
    
    <span data-ttu-id="f1e98-109">已分配172.25.33.40 的内部接口。</span><span class="sxs-lookup"><span data-stu-id="f1e98-109">Internal interface with 172.25.33.40 assigned.</span></span>
    
    <span data-ttu-id="f1e98-110">未定义默认网关。</span><span class="sxs-lookup"><span data-stu-id="f1e98-110">No default gateway is defined.</span></span>
    
    <span data-ttu-id="f1e98-111">确保存在从网络到包含 Lync Server 前端池服务器的反向代理内部接口的路由， (例如从172.25.33.0 到 192.168.10.0) 。</span><span class="sxs-lookup"><span data-stu-id="f1e98-111">Ensure there is a route from the network containing the reverse proxy internal interface to any networks that contain Lync Server Front End pool servers (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="f1e98-112">**网络适配器 2 (外部接口)** 示例</span><span class="sxs-lookup"><span data-stu-id="f1e98-112">**Network adapter 2 (External Interface)** example</span></span>
    
    <span data-ttu-id="f1e98-113">至少有一个公共 IP 地址分配给此网络适配器。</span><span class="sxs-lookup"><span data-stu-id="f1e98-113">A minimum of one public IP address is assigned to this network adapter.</span></span>
    
    <span data-ttu-id="f1e98-114">网关定义为指向外部外围设备中的路由器或集成防火墙。</span><span class="sxs-lookup"><span data-stu-id="f1e98-114">Gateway is defined to point to the router or integrated firewall in your outer perimeter.</span></span> <span data-ttu-id="f1e98-115"> (方案示例中的 10.45.16.1) </span><span class="sxs-lookup"><span data-stu-id="f1e98-115">(10.45.16.1 in the scenario examples)</span></span>

### <a name="dns-records-required-for-reverse-proxy"></a><span data-ttu-id="f1e98-116">反向代理所需的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="f1e98-116">DNS Records Required for Reverse Proxy</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1e98-117">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="f1e98-117">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="f1e98-118">FQDN</span><span class="sxs-lookup"><span data-stu-id="f1e98-118">FQDN</span></span></th>
<th><span data-ttu-id="f1e98-119">IP 地址</span><span class="sxs-lookup"><span data-stu-id="f1e98-119">IP address</span></span></th>
<th><span data-ttu-id="f1e98-120">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="f1e98-120">Maps to/comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1e98-121">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="f1e98-121">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f1e98-122">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f1e98-122">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f1e98-123">分配给外部已发布资源的侦听器</span><span class="sxs-lookup"><span data-stu-id="f1e98-123">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f1e98-124">内部部署中的外部 web 服务。</span><span class="sxs-lookup"><span data-stu-id="f1e98-124">External web services from the internal deployment.</span></span> <span data-ttu-id="f1e98-125">对于将使用此反向代理的任何 SIP 域，可以为所有池和单个服务器定义和创建其他记录，并且已定义外部 web 服务。</span><span class="sxs-lookup"><span data-stu-id="f1e98-125">Additional records can be defined and created for all pools and single servers for any SIP domain that will use this reverse proxy, and has defined external web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e98-126">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="f1e98-126">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f1e98-127">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f1e98-127">webdirext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f1e98-128">分配给外部已发布资源的侦听器</span><span class="sxs-lookup"><span data-stu-id="f1e98-128">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f1e98-129">部署中的控制器或控制器池的外部 web 服务。</span><span class="sxs-lookup"><span data-stu-id="f1e98-129">External web services for the Directors or Director pools in your deployment.</span></span> <span data-ttu-id="f1e98-130">你可以定义任意多个控制器，因为不同的控制器可能与其他 SIP 域相关联。</span><span class="sxs-lookup"><span data-stu-id="f1e98-130">You can define as many Directors as there are distinct Directors, of which may be associated with other SIP domains.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="f1e98-131">定义和发布控制器的 DNS 记录既不是前端池，也不是控制器决策。</span><span class="sxs-lookup"><span data-stu-id="f1e98-131">Defining the DNS records for and publishing the Directors is not an either the Front End pool or the Director decision.</span></span> <span data-ttu-id="f1e98-132">如果您使用的是董事，则必须定义和发布 Director 和前端池外部 web 服务。</span><span class="sxs-lookup"><span data-stu-id="f1e98-132">You must define and publish both the Director and the Front End pool external web services if you are using Directors.</span></span> <span data-ttu-id="f1e98-133">如果在拓扑中定义了身份验证和其他使用) 的特定流量类型 (将首先发送给 Director。</span><span class="sxs-lookup"><span data-stu-id="f1e98-133">Specific traffic types (for authentication and other uses) will be sent to the Director first, if it is defined in the topology.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1e98-134">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="f1e98-134">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f1e98-135">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f1e98-135">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f1e98-136">分配给外部已发布资源的侦听器</span><span class="sxs-lookup"><span data-stu-id="f1e98-136">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f1e98-137">外部发布的电话拨入式会议</span><span class="sxs-lookup"><span data-stu-id="f1e98-137">Dial-in conferencing published externally</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e98-138">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="f1e98-138">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f1e98-139">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f1e98-139">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f1e98-140">分配给外部已发布资源的侦听器</span><span class="sxs-lookup"><span data-stu-id="f1e98-140">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f1e98-141">外部发布的会议</span><span class="sxs-lookup"><span data-stu-id="f1e98-141">Conferences published externally</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1e98-142">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="f1e98-142">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f1e98-143">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f1e98-143">officewebapps01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f1e98-144">已分配 Office Web Apps 服务器侦听器</span><span class="sxs-lookup"><span data-stu-id="f1e98-144">Assigned listener for Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="f1e98-145">Office Web Apps 服务器内部部署或在外围部署，并且已发布外部客户端访问</span><span class="sxs-lookup"><span data-stu-id="f1e98-145">Office Web Apps Server deployed internally or in the perimeter, and published for external client access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e98-146">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="f1e98-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f1e98-147">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f1e98-147">lyncdiscover.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f1e98-148">分配给外部已发布资源的侦听器</span><span class="sxs-lookup"><span data-stu-id="f1e98-148">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f1e98-149">Lync 发现外部发布的自动发现的外部记录，包括移动性、Microsoft Lync Web App 和计划程序 Web 应用</span><span class="sxs-lookup"><span data-stu-id="f1e98-149">Lync Discover External record for externally published AutoDiscover, and includes Mobility, Microsoft Lync Web App, and scheduler Web app</span></span></p></td>
</tr><span data-ttu-id="f1e98-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1e98-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

