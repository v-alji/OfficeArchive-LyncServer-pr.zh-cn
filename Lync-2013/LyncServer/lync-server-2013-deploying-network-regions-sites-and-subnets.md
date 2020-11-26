---
title: Lync Server 2013：部署网络区域、网站和子网
description: Lync Server 2013：部署网络区域、网站和子网。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1c4c08cd9b78b1439000cdb4a7bbe3ffc2f99d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429844"
---
# <a name="deploying-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="2cf65-103">在 Lync Server 2013 中部署网络区域、网站和子网</span><span class="sxs-lookup"><span data-stu-id="2cf65-103">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2cf65-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2cf65-104">

<span> </span></span></span>

<span data-ttu-id="2cf65-105">_**主题上次修改时间：** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="2cf65-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="2cf65-106">部署企业语音后，您需要配置：</span><span class="sxs-lookup"><span data-stu-id="2cf65-106">Once Enterprise Voice is deployed, you need to configure:</span></span>

  - <span data-ttu-id="2cf65-107">网络区域</span><span class="sxs-lookup"><span data-stu-id="2cf65-107">Network regions</span></span>

  - <span data-ttu-id="2cf65-108">网络站点</span><span class="sxs-lookup"><span data-stu-id="2cf65-108">Network sites</span></span>

  - <span data-ttu-id="2cf65-109">网络子网</span><span class="sxs-lookup"><span data-stu-id="2cf65-109">Network subnets</span></span>

<div>

## <a name="define-network-regions"></a><span data-ttu-id="2cf65-110">定义网络区域</span><span class="sxs-lookup"><span data-stu-id="2cf65-110">Define Network Regions</span></span>

<span data-ttu-id="2cf65-111">使用 Lync Server Windows PowerShell 命令、"新建-CsNetworkRegion" 或 "Lync Server 控制面板" 定义网络区域。</span><span class="sxs-lookup"><span data-stu-id="2cf65-111">Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.</span></span>

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

<span data-ttu-id="2cf65-112">有关详细信息，请参阅 [CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion)。</span><span class="sxs-lookup"><span data-stu-id="2cf65-112">For more information, see [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span></span>

<span data-ttu-id="2cf65-113">在此示例中，以下 Windows PowerShell 命令演示了在此方案中定义的网络区域，区域 1 (印度) 。</span><span class="sxs-lookup"><span data-stu-id="2cf65-113">For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.</span></span>

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"

<div>


</div>

</div>

<div>

## <a name="define-network-sites"></a><span data-ttu-id="2cf65-114">定义网络站点</span><span class="sxs-lookup"><span data-stu-id="2cf65-114">Define Network Sites</span></span>

<span data-ttu-id="2cf65-115">使用 Lync Server Windows PowerShell 命令、"新建-CsNetworkSite" 或 "Lync Server 控制面板" 定义网络站点。</span><span class="sxs-lookup"><span data-stu-id="2cf65-115">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.</span></span>

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

<span data-ttu-id="2cf65-116">有关详细信息，请参阅 [CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite)。</span><span class="sxs-lookup"><span data-stu-id="2cf65-116">For more information, see [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span></span>

<span data-ttu-id="2cf65-117">对于此示例，下表和 Lync Server Windows PowerShell 命令演示了在此方案中定义的网络站点。</span><span class="sxs-lookup"><span data-stu-id="2cf65-117">For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario.</span></span> <span data-ttu-id="2cf65-118">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="2cf65-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2cf65-119">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="2cf65-119">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="2cf65-120">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="2cf65-120">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cf65-121">网站 ID</span><span class="sxs-lookup"><span data-stu-id="2cf65-121">Site ID</span></span></p></td>
<td><p><span data-ttu-id="2cf65-122">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="2cf65-122">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="2cf65-123">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="2cf65-123">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cf65-124">区域 ID</span><span class="sxs-lookup"><span data-stu-id="2cf65-124">Region ID</span></span></p></td>
<td><p><span data-ttu-id="2cf65-125">地区 1 (印度) </span><span class="sxs-lookup"><span data-stu-id="2cf65-125">Region 1 (India)</span></span></p></td>
<td><p><span data-ttu-id="2cf65-126">地区 1 (印度) </span><span class="sxs-lookup"><span data-stu-id="2cf65-126">Region 1 (India)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-network-subnets"></a><span data-ttu-id="2cf65-127">定义网络子网</span><span class="sxs-lookup"><span data-stu-id="2cf65-127">Define Network Subnets</span></span>

<span data-ttu-id="2cf65-128">使用 Lync Server Windows PowerShell 命令、"新建-CsNetworkSubnet" 或 "Lync Server 控制面板" 定义网络子网并将其分配给网络站点。</span><span class="sxs-lookup"><span data-stu-id="2cf65-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.</span></span>

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

<span data-ttu-id="2cf65-129">有关详细信息，请参阅 [CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)。</span><span class="sxs-lookup"><span data-stu-id="2cf65-129">For more information, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<span data-ttu-id="2cf65-130">对于此示例，下表和 Windows PowerShell 命令演示在此方案中定义的网络子网到 Hyderabad 和的分配。</span><span class="sxs-lookup"><span data-stu-id="2cf65-130">For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario.</span></span> <span data-ttu-id="2cf65-131">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="2cf65-131">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2cf65-132">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="2cf65-132">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="2cf65-133">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="2cf65-133">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cf65-134">子网 ID</span><span class="sxs-lookup"><span data-stu-id="2cf65-134">Subnet ID</span></span></p></td>
<td><p><span data-ttu-id="2cf65-135">含</span><span class="sxs-lookup"><span data-stu-id="2cf65-135">192.168.0.0</span></span></p></td>
<td><p><span data-ttu-id="2cf65-136">192.168.1.0</span><span class="sxs-lookup"><span data-stu-id="2cf65-136">192.168.1.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cf65-137">Usm</span><span class="sxs-lookup"><span data-stu-id="2cf65-137">Mask</span></span></p></td>
<td><p><span data-ttu-id="2cf65-138">全</span><span class="sxs-lookup"><span data-stu-id="2cf65-138">24</span></span></p></td>
<td><p><span data-ttu-id="2cf65-139">全</span><span class="sxs-lookup"><span data-stu-id="2cf65-139">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cf65-140">网站 ID</span><span class="sxs-lookup"><span data-stu-id="2cf65-140">Site ID</span></span></p></td>
<td><p><span data-ttu-id="2cf65-141">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="2cf65-141">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="2cf65-142">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="2cf65-142">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2cf65-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2cf65-143">See Also</span></span>


[<span data-ttu-id="2cf65-144">在 Lync Server 2013 中配置基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="2cf65-144">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="2cf65-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2cf65-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

