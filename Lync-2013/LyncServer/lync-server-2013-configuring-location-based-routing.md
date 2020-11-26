---
title: Lync Server 2013：配置基于位置的路由
description: Lync Server 2013：配置 Location-Based 路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433040"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="04e1b-103">在 Lync Server 2013 中配置基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="04e1b-103">Configuring Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04e1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04e1b-104">

<span> </span></span></span>

<span data-ttu-id="04e1b-105">_**主题上次修改时间：** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="04e1b-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="04e1b-106">Lync Server 2013 CU1 Location-Based 路由是企业语音的一项功能。</span><span class="sxs-lookup"><span data-stu-id="04e1b-106">Lync Server 2013 CU1, Location-Based Routing is a feature of Enterprise Voice.</span></span> <span data-ttu-id="04e1b-107">Location-Based 路由是一种呼叫管理功能，用于控制 Lync Server 2013 CU1 路由呼叫的方式。</span><span class="sxs-lookup"><span data-stu-id="04e1b-107">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="04e1b-108">它对根据 Lync 呼叫者的位置是否可以将呼叫路由到 PBX 或 PSTN 目标施加限制。</span><span class="sxs-lookup"><span data-stu-id="04e1b-108">It enforces restrictions on whether calls can be routed to PBX or PSTN destinations based on the Lync caller’s location.</span></span> <span data-ttu-id="04e1b-109">Location-Based 路由根据呼叫者的网络位置将呼叫授权规则应用到 PSTN 呼叫。</span><span class="sxs-lookup"><span data-stu-id="04e1b-109">Location-Based Routing applies call authorization rules to PSTN calls based on the caller’s network location.</span></span> <span data-ttu-id="04e1b-110">呼叫方的位置取决于与呼叫者连接的网络子网相关联的网络站点。</span><span class="sxs-lookup"><span data-stu-id="04e1b-110">The caller’s location is determined based on the network site associated with the network subnet the caller is connected on.</span></span> <span data-ttu-id="04e1b-111">配置 Location-Based 路由需要首先部署企业语音，然后配置网络区域、站点和子网。</span><span class="sxs-lookup"><span data-stu-id="04e1b-111">Configuring Location-Based Routing requires first deploying Enterprise Voice, then configuring network regions, sites and subnets.</span></span> <span data-ttu-id="04e1b-112">这将设置启用 Location-Based 路由的基础。</span><span class="sxs-lookup"><span data-stu-id="04e1b-112">This sets up the foundation for enabling Location-Based Routing.</span></span>

<span data-ttu-id="04e1b-113">在部署 Location-Based 路由之前，必须先部署企业语音，并配置网络区域、网站，并将网络子网与网络站点关联。</span><span class="sxs-lookup"><span data-stu-id="04e1b-113">Before deploying Location-Based Routing, you must first deploy Enterprise Voice, and configure network regions, sites, and associate network subnets to your network sites.</span></span> <span data-ttu-id="04e1b-114">完成后，你可以配置 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="04e1b-114">Once completed, you can configure Location-Based Routing.</span></span> <span data-ttu-id="04e1b-115">有关如何配置网络区域、网站和子网的步骤，请参阅[Lync Server 2013 中的 "部署高级企业语音功能](lync-server-2013-deploying-advanced-enterprise-voice-features.md)"</span><span class="sxs-lookup"><span data-stu-id="04e1b-115">For steps on how to configure network regions, sites and subnets, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span></span>

<span data-ttu-id="04e1b-116">本部分将指导你使用以下示例（如图）完成 Location-Based 路由的配置。</span><span class="sxs-lookup"><span data-stu-id="04e1b-116">This section guides you through the configuration of Location-Based Routing using the following example as illustration.</span></span>

<span data-ttu-id="04e1b-117">![基于企业语音位置的路由示例](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "基于企业语音位置的路由示例")</span><span class="sxs-lookup"><span data-stu-id="04e1b-117">![Enterprise Voice location-based routing example](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Enterprise Voice location-based routing example")</span></span>

  
<span data-ttu-id="04e1b-118">下表表示在此示例中定义的用户。</span><span class="sxs-lookup"><span data-stu-id="04e1b-118">The following table represents the users defined in this example.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04e1b-119">终结点类型</span><span class="sxs-lookup"><span data-stu-id="04e1b-119">Endpoint type</span></span></th>
<th><span data-ttu-id="04e1b-120">位置</span><span class="sxs-lookup"><span data-stu-id="04e1b-120">Location</span></span></th>
<th><span data-ttu-id="04e1b-121">用户</span><span class="sxs-lookup"><span data-stu-id="04e1b-121">Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04e1b-122">Lync</span><span class="sxs-lookup"><span data-stu-id="04e1b-122">Lync</span></span></p></td>
<td><p><span data-ttu-id="04e1b-123">新德里企业办公室</span><span class="sxs-lookup"><span data-stu-id="04e1b-123">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="04e1b-124">DEL-LYNC-1、DEL-LYNC-2、DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="04e1b-124">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04e1b-125">Lync</span><span class="sxs-lookup"><span data-stu-id="04e1b-125">Lync</span></span></p></td>
<td><p><span data-ttu-id="04e1b-126">Hyderabad 公司办公室</span><span class="sxs-lookup"><span data-stu-id="04e1b-126">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="04e1b-127">HYD-LYNC-1，HYD-LYNC-2，HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="04e1b-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04e1b-128">Lync</span><span class="sxs-lookup"><span data-stu-id="04e1b-128">Lync</span></span></p></td>
<td><p><span data-ttu-id="04e1b-129">未知 (，即旅馆) </span><span class="sxs-lookup"><span data-stu-id="04e1b-129">Unknown (i.e. hotel)</span></span></p></td>
<td><p><span data-ttu-id="04e1b-130">UNK-LYNC-1</span><span class="sxs-lookup"><span data-stu-id="04e1b-130">UNK-LYNC-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04e1b-131">PBX</span><span class="sxs-lookup"><span data-stu-id="04e1b-131">PBX</span></span></p></td>
<td><p><span data-ttu-id="04e1b-132">新德里企业办公室</span><span class="sxs-lookup"><span data-stu-id="04e1b-132">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="04e1b-133">DEL-PBX-1，DEL-PBX-2</span><span class="sxs-lookup"><span data-stu-id="04e1b-133">DEL-PBX-1, DEL-PBX-2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04e1b-134">PBX</span><span class="sxs-lookup"><span data-stu-id="04e1b-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="04e1b-135">Hyderabad 公司办公室</span><span class="sxs-lookup"><span data-stu-id="04e1b-135">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="04e1b-136">HYD-PBX-1，HYD-2</span><span class="sxs-lookup"><span data-stu-id="04e1b-136">HYD-PBX-1, HYD-PBX-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04e1b-137">PSTN</span><span class="sxs-lookup"><span data-stu-id="04e1b-137">PSTN</span></span></p></td>
<td><p><span data-ttu-id="04e1b-138">可知</span><span class="sxs-lookup"><span data-stu-id="04e1b-138">Unknown</span></span></p></td>
<td><p><span data-ttu-id="04e1b-139">PSTN-1、PSTN-2、PSTN-3</span><span class="sxs-lookup"><span data-stu-id="04e1b-139">PSTN-1, PSTN-2, PSTN-3</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="04e1b-140">下表表示此示例环境中所示的系统。</span><span class="sxs-lookup"><span data-stu-id="04e1b-140">The following table represents the systems illustrated in this example environment.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04e1b-141">系统</span><span class="sxs-lookup"><span data-stu-id="04e1b-141">System</span></span></th>
<th><span data-ttu-id="04e1b-142">位置</span><span class="sxs-lookup"><span data-stu-id="04e1b-142">Location</span></span></th>
<th><span data-ttu-id="04e1b-143">名称</span><span class="sxs-lookup"><span data-stu-id="04e1b-143">Name</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04e1b-144">Lync Server 2013 CU1 池</span><span class="sxs-lookup"><span data-stu-id="04e1b-144">Lync Server 2013 CU1 pool</span></span></p></td>
<td><p><span data-ttu-id="04e1b-145">任何</span><span class="sxs-lookup"><span data-stu-id="04e1b-145">any</span></span></p></td>
<td><p><span data-ttu-id="04e1b-146">LS-PL1</span><span class="sxs-lookup"><span data-stu-id="04e1b-146">LS-PL1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04e1b-147">Lync Server 2013 CU1、中介服务器</span><span class="sxs-lookup"><span data-stu-id="04e1b-147">Lync Server 2013 CU1, Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="04e1b-148">任何</span><span class="sxs-lookup"><span data-stu-id="04e1b-148">any</span></span></p></td>
<td><p><span data-ttu-id="04e1b-149">MS-PL1</span><span class="sxs-lookup"><span data-stu-id="04e1b-149">MS-PL1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04e1b-150">PSTN 网关1</span><span class="sxs-lookup"><span data-stu-id="04e1b-150">PSTN gateway 1</span></span></p></td>
<td><p><span data-ttu-id="04e1b-151">Delhi</span><span class="sxs-lookup"><span data-stu-id="04e1b-151">Delhi</span></span></p></td>
<td><p><span data-ttu-id="04e1b-152">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="04e1b-152">DEL-GW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04e1b-153">PSTN 网关2</span><span class="sxs-lookup"><span data-stu-id="04e1b-153">PSTN gateway 2</span></span></p></td>
<td><p><span data-ttu-id="04e1b-154">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="04e1b-154">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="04e1b-155">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="04e1b-155">HYD-GW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04e1b-156">PBX 1</span><span class="sxs-lookup"><span data-stu-id="04e1b-156">PBX 1</span></span></p></td>
<td><p><span data-ttu-id="04e1b-157">Delhi</span><span class="sxs-lookup"><span data-stu-id="04e1b-157">Delhi</span></span></p></td>
<td><p><span data-ttu-id="04e1b-158">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="04e1b-158">DEL-PBX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04e1b-159">PBX 2</span><span class="sxs-lookup"><span data-stu-id="04e1b-159">PBX 2</span></span></p></td>
<td><p><span data-ttu-id="04e1b-160">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="04e1b-160">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="04e1b-161">红 PBX</span><span class="sxs-lookup"><span data-stu-id="04e1b-161">RED-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="04e1b-162">本节内容</span><span class="sxs-lookup"><span data-stu-id="04e1b-162">In This Section</span></span>

  - [<span data-ttu-id="04e1b-163">在 Lync Server 2013 中配置企业语音</span><span class="sxs-lookup"><span data-stu-id="04e1b-163">Configuring Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-configuring-enterprise-voice.md)

  - [<span data-ttu-id="04e1b-164">在 Lync Server 2013 中部署网络区域、网站和子网</span><span class="sxs-lookup"><span data-stu-id="04e1b-164">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="04e1b-165">在 Lync Server 2013 中启用 Location-Based 路由</span><span class="sxs-lookup"><span data-stu-id="04e1b-165">Enabling Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="04e1b-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04e1b-166">See Also</span></span>


[<span data-ttu-id="04e1b-167">在 Lync Server 2013 中部署高级企业语音功能</span><span class="sxs-lookup"><span data-stu-id="04e1b-167">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

<span data-ttu-id="04e1b-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04e1b-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

