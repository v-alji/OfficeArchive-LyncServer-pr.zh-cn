---
title: Lync Server 2013：启用 Location-Based 路由
description: Lync Server 2013：启用 Location-Based 路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Location-Based Routing
ms:assetid: 029ede7e-0c4e-4ad2-af99-909ae674d6fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994014(v=OCS.15)
ms:contentKeyID: 51803920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7844af5792468cd5645b6b42c857c63b943c2df1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392197"
---
# <a name="enabling-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="c2f6f-103">在 Lync Server 2013 中启用 Location-Based 路由</span><span class="sxs-lookup"><span data-stu-id="c2f6f-103">Enabling Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2f6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2f6f-104">

<span> </span></span></span>

<span data-ttu-id="c2f6f-105">_**主题上次修改时间：** 2013-04-26_</span><span class="sxs-lookup"><span data-stu-id="c2f6f-105">_**Topic Last Modified:** 2013-04-26_</span></span>

<span data-ttu-id="c2f6f-106">部署企业语音并定义网络区域、网站和子网后，您可以启用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-106">Once Enterprise Voice is deployed and network regions, sites and subnets are defined, you can enable Location-Based Routing.</span></span> <span data-ttu-id="c2f6f-107">必须为以下企业语音元素启用 Location-Based 路由：</span><span class="sxs-lookup"><span data-stu-id="c2f6f-107">Location-Based Routing must be enabled for the following Enterprise Voice elements:</span></span>

  - <span data-ttu-id="c2f6f-108">网络站点</span><span class="sxs-lookup"><span data-stu-id="c2f6f-108">Network sites</span></span>

  - <span data-ttu-id="c2f6f-109">中继配置</span><span class="sxs-lookup"><span data-stu-id="c2f6f-109">Trunk configurations</span></span>

  - <span data-ttu-id="c2f6f-110">语音策略</span><span class="sxs-lookup"><span data-stu-id="c2f6f-110">Voice policies</span></span>

  - <span data-ttu-id="c2f6f-111">路由配置</span><span class="sxs-lookup"><span data-stu-id="c2f6f-111">Routing configuration</span></span>

<div>

## <a name="enable-location-based-routing-to-network-sites"></a><span data-ttu-id="c2f6f-112">启用 Location-Based 路由到网络站点</span><span class="sxs-lookup"><span data-stu-id="c2f6f-112">Enable Location-Based Routing to Network Sites</span></span>

<span data-ttu-id="c2f6f-113">部署企业语音和配置的网络站点后，即可配置 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-113">After you have deployed Enterprise Voice, and configured network sites, you are ready to configure Location-Based Routing.</span></span> <span data-ttu-id="c2f6f-114">首先，创建一个语音路由策略，将网络站点与适当的 PSTN 使用情况关联起来。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-114">First, you create a voice routing policy to associate the network site with the appropriate PSTN usages.</span></span> <span data-ttu-id="c2f6f-115">将 PSTN 使用分配给语音路由策略时，请确保仅使用与在不需要 Location-Based 路由限制的区域中使用该站点或 PSTN 网关本地的 pstn 网关相关的 PSTN 使用。使用 Lync Server Windows PowerShell 命令、"新建-CsVoiceRoutingPolicy" 或 "Lync Server 控制面板" 创建语音路由策略。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-115">When assigning PSTN usages to a voice routing policy, make sure to only use PSTN usages that are associated to voice routes that use a PSTN gateway local to the site or a PSTN gateway that is located in a region where Location-Based Routing restrictions are not needed.Use the Lync Server Windows PowerShell command, New-CsVoiceRoutingPolicy, or Lync Server Control Panel to create voice routing policies.</span></span>

    New-CsVoiceRoutingPolicy -Identity <voice routing policy ID> -Name <voice routing policy name> -PstnUsages <usages>

<span data-ttu-id="c2f6f-116">有关更多信息，请参阅 [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy)。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-116">For more information, see [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span></span>

<span data-ttu-id="c2f6f-117">对于此示例，下表和 Windows PowerShell 命令演示了这种情况下定义的两个语音路由策略及其关联的 PSTN 用法。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-117">For this example, the following table and Windows PowerShell commands illustrate two voice routing policies and their associated PSTN usages defined in this scenario.</span></span> <span data-ttu-id="c2f6f-118">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsVoiceRoutingPolicy -Identity "DelhiVoiceRoutingPolicy" -Name "Delhi voice routing policy" -PstnUsages @{add="Delhi usage", "PBX Del usage", "PBX Hyd usage"}
    New-CsVoiceRoutingPolicy -Identity "HyderabadVoiceRoutingPolicy" -Name " Hyderabad voice routing policy" -PstnUsages @{add="Hyderabad usage", "PBX Del usage", "PBX Hyd usage"}


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c2f6f-119">语音路由策略1</span><span class="sxs-lookup"><span data-stu-id="c2f6f-119">Voice routing policy 1</span></span></th>
<th><span data-ttu-id="c2f6f-120">语音路由策略2</span><span class="sxs-lookup"><span data-stu-id="c2f6f-120">Voice routing policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f6f-121">语音策略 ID</span><span class="sxs-lookup"><span data-stu-id="c2f6f-121">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-122">新德里语音路由策略</span><span class="sxs-lookup"><span data-stu-id="c2f6f-122">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-123">Hyderabad 语音路由策略</span><span class="sxs-lookup"><span data-stu-id="c2f6f-123">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f6f-124">PSTN 用法</span><span class="sxs-lookup"><span data-stu-id="c2f6f-124">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-125">新德里使用，PBX Del 用法，PBX Hyd 用法</span><span class="sxs-lookup"><span data-stu-id="c2f6f-125">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-126">Hyderabad 使用，PBX Hyd 使用，PBX Del 使用</span><span class="sxs-lookup"><span data-stu-id="c2f6f-126">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="c2f6f-127">接下来，为适用的网络网站配置 Location-Based 路由，并将你的语音路由策略关联到它们。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-127">Next, configure Location-Based Routing for the applicable network sites and associate your voice routing policies to them.</span></span> <span data-ttu-id="c2f6f-128">使用 Lync Server Windows PowerShell 命令 "CsNetworkSite" 启用 Location-Based 路由，并将语音路由策略关联到必须强制使用路由限制的网络站点。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, to enable Location-Based Routing and associate voice routing policies to your network sites that must enforce routing restrictions.</span></span>

    Set-CsNetworkSite -Identity <site ID> -EnableLocationBasedRouting <$true|$false> -VoiceRoutingPolicy <voice routing policy ID>

<span data-ttu-id="c2f6f-129">在此示例中，下表介绍 Location-Based 了使用 Lync Server Windows PowerShell 在此方案中定义的两个不同网络站点 Hyderabad、新德里和的路由。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-129">In this example, the following table illustrates Location-Based Routing for two different network sites, Delhi and Hyderabad, defined in this scenario using the Lync Server Windows PowerShell.</span></span> <span data-ttu-id="c2f6f-130">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-130">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsNetworkSite -Identity "Delhi" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "DelhiVoiceRoutingPolicy"
    Set-CsNetworkSite -Identity "Hyderabad" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "HyderabadVoiceRoutingPolicy"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c2f6f-131">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-131">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="c2f6f-132">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-132">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f6f-133">站点名称</span><span class="sxs-lookup"><span data-stu-id="c2f6f-133">Site Name</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-134">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-134">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-135">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-135">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f6f-136">EnableLocationBasedRouting</span><span class="sxs-lookup"><span data-stu-id="c2f6f-136">EnableLocationBasedRouting</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-137">True</span><span class="sxs-lookup"><span data-stu-id="c2f6f-137">True</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-138">True</span><span class="sxs-lookup"><span data-stu-id="c2f6f-138">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f6f-139">语音路由策略</span><span class="sxs-lookup"><span data-stu-id="c2f6f-139">Voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-140">新德里语音路由策略</span><span class="sxs-lookup"><span data-stu-id="c2f6f-140">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-141">Hyderabad 语音路由策略</span><span class="sxs-lookup"><span data-stu-id="c2f6f-141">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f6f-142">子网</span><span class="sxs-lookup"><span data-stu-id="c2f6f-142">Subnets</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-143">子网 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-143">Subnet 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-144">子网 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-144">Subnet 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-trunks"></a><span data-ttu-id="c2f6f-145">启用 Location-Based 路由到中继</span><span class="sxs-lookup"><span data-stu-id="c2f6f-145">Enable Location-Based Routing to Trunks</span></span>

<span data-ttu-id="c2f6f-146">在可以为 Location-Based 路由启用中继配置之前，你需要为每个主干或每个网络站点创建中继配置。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-146">Before a trunk configuration can be enabled for Location-Based Routing, you need to create a trunk configuration for each trunk or each network site.</span></span> <span data-ttu-id="c2f6f-147">使用 Lync Server Windows PowerShell 命令 New-cstrunkconfiguration 创建中继配置。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-147">Use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, to create a trunk configuration.</span></span> <span data-ttu-id="c2f6f-148">如果多个中继与给定的 (系统（即网关或 PBX) ）相关联，则必须修改每个干线配置以启用 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-148">If multiple trunks are associated with a given system (i.e. Gateway or PBX), each trunk configuration must be modified to enable Location-Based Routing restrictions.</span></span>

    New-CsTrunkConfiguration -Identity < trunk configuration ID>

<span data-ttu-id="c2f6f-149">有关详细信息，请参阅 [new-cstrunkconfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration)。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-149">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="c2f6f-150">对于此示例，以下 Windows PowerShell 命令演示了为此方案中定义的部署中的每个主干创建一个 trunk 配置。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-150">For this example, the following Windows PowerShell commands illustrate creating one trunk configuration for each trunk in the deployment defined in this scenario.</span></span>

    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 1 DEL-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 2 HYD-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 3 DEL-PBX>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 4 HYD-PBX>"

<span data-ttu-id="c2f6f-151">每个干线配置中继配置后，您可以使用 Lync Server Windows PowerShell 命令 New-cstrunkconfiguration 来启用 Location-Based 路由到必须强制使用路由限制的中继。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-151">Once a trunk configuration is configured per trunk, you can use the Lync Server Windows PowerShell command, Set-CsTrunkConfiguration, to enable Location-Based Routing to your trunks that must enforce routing restrictions.</span></span> <span data-ttu-id="c2f6f-152">启用 Location-Based 路由到将呼叫路由到 pstn 网关的 PSTN 网关的中继，并将网关所在的网络站点关联起来。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-152">Enable Location-Based Routing to trunks that route calls to PSTN gateways that route calls to the PSTN, and associate the network site where the gateway is located.</span></span>

    Set-CsTrunkConfiguration -Identity <trunk configuration ID> -EnableLocationRestriction $true -NetworkSiteID <site ID>

<span data-ttu-id="c2f6f-153">有关详细信息，请参阅 [new-cstrunkconfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration)。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-153">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="c2f6f-154">在此示例中，将为与 Hyderabad 和中的 PSTN 网关关联的每个主干启用 "路由 Location-Based"：</span><span class="sxs-lookup"><span data-stu-id="c2f6f-154">In this example, Location-Based Routing is enabled for each trunk that is associated to PSTN gateways in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 1 DEL-GW -EnableLocationRestriction $true -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 2 HYD-GW -EnableLocationRestriction $true -NetworkSiteID "Hyderabad"

  

<span data-ttu-id="c2f6f-155">不要为不将呼叫路由到 PSTN 的中继启用 Location-Based 路由;但是，你仍然必须将主干与系统所在的网络站点相关联，以使 PSTN 呼叫达到通过此主干连接的终结点所需的 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-155">Do not enable Location-Based Routing for trunks that do not route calls to the PSTN; however, you must still associate the trunk to the network site where the system is located as Location-Based Routing restrictions need to be enforced for PSTN calls reaching endpoints connected via this trunk.</span></span> <span data-ttu-id="c2f6f-156">对于此示例，对于与新德里和 Hyderabad 中的 PBX 系统相关联的每个主干，不启用 Location-Based 路由：</span><span class="sxs-lookup"><span data-stu-id="c2f6f-156">For this example, Location-Based Routing is not enabled for each trunk that is associated to PBX systems in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 3 DEL-PBX -EnableLocationRestriction $false -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 4 HYD-PBX -EnableLocationRestriction $false -NetworkSiteID "Hyderabad"

  
<span data-ttu-id="c2f6f-157">连接到不路由到 PSTN 的系统的终结点 (即 PBX) 将具有与启用 Location-Based 路由的用户的 Lync 终结点类似的限制。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-157">Endpoints that are connected to systems that do not route calls to the PSTN (i.e. a PBX) will have similar restrictions as Lync endpoints of users enabled for Location-Based Routing.</span></span> <span data-ttu-id="c2f6f-158">这意味着，无论用户的位置如何，这些用户都可以将呼叫放入和接收 Lync 用户。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-158">This means that these users will be able to place and receive calls to and from Lync user regardless of the user’s location.</span></span> <span data-ttu-id="c2f6f-159">他们还可以在不将呼叫路由到 PSTN 网络的其他系统上进行接收呼叫，也可以在不路由到 PSTN 网络的其他系统上进行接收呼叫 (也就是说，连接到其他 PBX 的终结点) 无论与系统关联的网络站点。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-159">They will also be able to place an receive calls to and from other systems that do not route calls to the PSTN network (i.e. an endpoint connected to a different PBX) regardless of the network site to which the system is associated.</span></span> <span data-ttu-id="c2f6f-160">涉及 PSTN 终结点的所有入站呼叫、出站呼叫、呼叫转移和呼叫转接将受到 Location-Based 路由 enforcements。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-160">All inbound calls, outbound calls, call transfers and call forwarding involving PSTN endpoints will be subject to Location-Based Routing enforcements.</span></span> <span data-ttu-id="c2f6f-161">此类通话只能使用定义为此类系统本地的 PSTN 网关。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-161">Such calls must use only PSTN gateways that are defined as local to such systems.</span></span>

<span data-ttu-id="c2f6f-162">下表说明了两个不同网络站点中四个中继的干线配置：两个连接到 PSTN 网关的两个连接和连接到 PBX 系统的两个。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-162">The following table illustrates the trunk configuration of four trunks in two different network sites: two connected to PSTN gateways and two connected to PBX systems.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2f6f-163">名称</span><span class="sxs-lookup"><span data-stu-id="c2f6f-163">Name</span></span></th>
<th><span data-ttu-id="c2f6f-164">EnableLocationRestriction</span><span class="sxs-lookup"><span data-stu-id="c2f6f-164">EnableLocationRestriction</span></span></th>
<th><span data-ttu-id="c2f6f-165">NetworkSiteID</span><span class="sxs-lookup"><span data-stu-id="c2f6f-165">NetworkSiteID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f6f-166">PstnGateway：干线 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="c2f6f-166">PstnGateway:Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-167">True</span><span class="sxs-lookup"><span data-stu-id="c2f6f-167">True</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-168">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-168">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f6f-169">PstnGateway：主干 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="c2f6f-169">PstnGateway:Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-170">True</span><span class="sxs-lookup"><span data-stu-id="c2f6f-170">True</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-171">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-171">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f6f-172">PstnGateway：干线 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="c2f6f-172">PstnGateway:Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-173">False</span><span class="sxs-lookup"><span data-stu-id="c2f6f-173">False</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-174">站点 1 (新德里) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-174">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f6f-175">PstnGateway：干线 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="c2f6f-175">PstnGateway:Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-176">False</span><span class="sxs-lookup"><span data-stu-id="c2f6f-176">False</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-177">网站 2 (Hyderabad) </span><span class="sxs-lookup"><span data-stu-id="c2f6f-177">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-voice-policies"></a><span data-ttu-id="c2f6f-178">启用 Location-Based 路由到语音策略</span><span class="sxs-lookup"><span data-stu-id="c2f6f-178">Enable Location-Based Routing to Voice Policies</span></span>

<span data-ttu-id="c2f6f-179">若要强制 Location-Based 路由到特定用户，请将这些用户的语音策略配置为阻止 PSTN 免绕过。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-179">To enforce Location-Based Routing to specific users, configure those users’ voice policy to prevent PSTN toll bypass.</span></span> <span data-ttu-id="c2f6f-180">使用 Lync Server Windows PowerShell 命令 CsVoicePolicy 创建新的语音策略或设置 CsVoicePolicy （如果使用现有策略）以通过阻止 PSTN 免绕过，从而启用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-180">Use the Lync Server Windows PowerShell command, New-CsVoicePolicy, to create a new voice policy or Set-CsVoicePolicy, if using an existing policy, to enable Location-Based Routing by preventing PSTN toll bypass.</span></span>

    Set-CsVoicePolicy -Identity <voice policy ID> -PreventPSTNTollBypass <$true|$false>

<span data-ttu-id="c2f6f-181">有关详细信息，请参阅 [CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy)。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-181">For more information, see [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span></span>

<span data-ttu-id="c2f6f-182">在此示例中，下表和 Windows PowerShell 命令演示了如何为本方案中定义的 Hyderabad 语音策略启用 PSTN 免绕过保护。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-182">For this example, the following table and Windows PowerShell commands illustrate enabling the prevention of PSTN toll bypass to the Delhi and Hyderabad voice policies defined in this scenario.</span></span> <span data-ttu-id="c2f6f-183">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-183">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsVoicePolicy -Identity "Delhi voice policy" -PreventPSTNTollBypass $true
    Set-CsVoicePolicy -Identity "Hyderabad voice policy" -PreventPSTNTollBypass $true


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c2f6f-184">语音策略1</span><span class="sxs-lookup"><span data-stu-id="c2f6f-184">Voice policy 1</span></span></th>
<th><span data-ttu-id="c2f6f-185">语音政策2</span><span class="sxs-lookup"><span data-stu-id="c2f6f-185">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f6f-186">语音策略 ID</span><span class="sxs-lookup"><span data-stu-id="c2f6f-186">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-187">新德里语音政策</span><span class="sxs-lookup"><span data-stu-id="c2f6f-187">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-188">Hyderabad 语音政策</span><span class="sxs-lookup"><span data-stu-id="c2f6f-188">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f6f-189">PSTN 用法</span><span class="sxs-lookup"><span data-stu-id="c2f6f-189">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-190">新德里使用，PBX Del 用法，PBX Hyd 用法</span><span class="sxs-lookup"><span data-stu-id="c2f6f-190">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-191">Hyderabad 使用，PBX Hyd 使用，PBX Del 使用</span><span class="sxs-lookup"><span data-stu-id="c2f6f-191">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f6f-192">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="c2f6f-192">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-193">True</span><span class="sxs-lookup"><span data-stu-id="c2f6f-193">True</span></span></p></td>
<td><p><span data-ttu-id="c2f6f-194">True</span><span class="sxs-lookup"><span data-stu-id="c2f6f-194">True</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-in-the-routing-configuration"></a><span data-ttu-id="c2f6f-195">在路由配置中启用 Location-Based 路由</span><span class="sxs-lookup"><span data-stu-id="c2f6f-195">Enable Location-Based Routing in the routing configuration</span></span>

<span data-ttu-id="c2f6f-196">最后，全局启用 Location-Based 路由到路由配置。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-196">Finally, globally enable Location-Based Routing to your routing configuration.</span></span> <span data-ttu-id="c2f6f-197">使用 Lync Server Windows PowerShell 命令 "CsRoutingConfiguration" 启用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-197">Use the Lync Server Windows PowerShell command, New-CsRoutingConfiguration, to enable Location-Based Routing.</span></span>

    Set-CsRoutingConfiguration -EnableLocationBasedRouting $true

<span data-ttu-id="c2f6f-198">有关详细信息，请参阅 [设置 CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration)。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-198">For more information, see [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c2f6f-199">虽然 Location-Based 路由必须通过全局配置启用，但将仅针对此文档中指定的网站、用户和中继强制执行要应用的规则集。</span><span class="sxs-lookup"><span data-stu-id="c2f6f-199">while Location-Based Routing must be enabled via a global configuration, the set of rules to be applied will only be enforced for the sites, users and trunks for which it has been configured as specified in this documentation.</span></span>



</div>

<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c2f6f-200">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2f6f-200">See Also</span></span>


[<span data-ttu-id="c2f6f-201">在 Lync Server 2013 中配置基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="c2f6f-201">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="c2f6f-202"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2f6f-202"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

