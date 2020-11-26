---
title: Lync Server 2013：适用于会议的 Location-Based 路由的要求
description: Lync Server 2013：对会议 Location-Based 路由的要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442661"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="d970d-103">Lync Server 2013 中的会议 Location-Based 路由要求</span><span class="sxs-lookup"><span data-stu-id="d970d-103">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d970d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d970d-104">

<span> </span></span></span>

<span data-ttu-id="d970d-105">_**主题上次修改时间：** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="d970d-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="d970d-106">以下是安装和配置 Location-Based 路由会议应用程序所需的要求：</span><span class="sxs-lookup"><span data-stu-id="d970d-106">The following are the requirements needed for the installation and configuration of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="d970d-107">Lync Server 2013 累积更新2必须部署在拓扑中的所有服务器或池上。</span><span class="sxs-lookup"><span data-stu-id="d970d-107">Lync Server 2013 Cumulative Update 2 must be deployed on all servers or pools in your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d970d-108">如果拓扑中的 Lync 服务器或池未安装 Lync Server 2013 累积更新2或更高版本，则无法保证 Lync 会议的 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="d970d-108">If a Lync server or pool in your topology does not have Lync Server 2013 Cumulative Update 2 or higher installed, then enforcement of Location-Based Routing of Lync meetings cannot be guaranteed.</span></span>



</div>

  - <span data-ttu-id="d970d-109">Lync Server 2013 Location-Based 路由是 Location-Based 路由会议应用程序的先决条件。</span><span class="sxs-lookup"><span data-stu-id="d970d-109">Lync Server 2013 Location-Based Routing is a pre-requisite for Location-Based Routing Conferencing application.</span></span> <span data-ttu-id="d970d-110">有关配置 Lync Server 2013 Location-Based 路由的详细信息，请参阅 [配置 Location-Based 路由](lync-server-2013-configuring-location-based-routing.md)。</span><span class="sxs-lookup"><span data-stu-id="d970d-110">For further information on configuring Lync Server 2013 Location-Based Routing, please refer to [Configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

  - <span data-ttu-id="d970d-111">Location-Based 路由会议应用程序的要求与 Lync Server 2013 Location-Based 路由的要求相同。</span><span class="sxs-lookup"><span data-stu-id="d970d-111">Requirements of Location-Based Routing Conferencing application are the same as the requirements for Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="d970d-112">有关详细信息，请参阅 [规划 Location-Based 路由](lync-server-2013-planning-for-location-based-routing.md)。</span><span class="sxs-lookup"><span data-stu-id="d970d-112">For more information, please refer to [Planning for Location-Based Routing](lync-server-2013-planning-for-location-based-routing.md).</span></span>

<div>

## <a name="supported-servers"></a><span data-ttu-id="d970d-113">支持的服务器</span><span class="sxs-lookup"><span data-stu-id="d970d-113">Supported Servers</span></span>

<span data-ttu-id="d970d-114">Location-Based 路由会议应用程序要求在拓扑中的所有 Front-End 池和标准版服务器上部署 Lync Server 2013 累积更新2。</span><span class="sxs-lookup"><span data-stu-id="d970d-114">The Location-Based Routing Conferencing application requires that Lync Server 2013 Cumulative Update 2 is deployed on all Front-End pools and Standard Edition Servers in your topology.</span></span> <span data-ttu-id="d970d-115">如果你的拓扑中的某些 Lync 服务器上未安装 Lync Server 2013 累积更新2，则不能在 Lync 会议和咨询式呼叫传输上完全强制使用 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="d970d-115">If Lync Server 2013 Cumulative Update 2 is not installed on some Lync Servers in your topology, Location-Based Routing restrictions cannot be fully enforced on Lync meetings and consultative call transfers.</span></span>

<span data-ttu-id="d970d-116">下表列出了支持 Location-Based 路由的服务器角色和版本的组合。</span><span class="sxs-lookup"><span data-stu-id="d970d-116">The following table identifies the combination of server roles and versions that support Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d970d-117">前端池版本</span><span class="sxs-lookup"><span data-stu-id="d970d-117">Front-End Pool version</span></span></p></td>
<td><p><span data-ttu-id="d970d-118">中介服务器版本</span><span class="sxs-lookup"><span data-stu-id="d970d-118">Mediation Server version</span></span></p></td>
<td><p><span data-ttu-id="d970d-119">支持</span><span class="sxs-lookup"><span data-stu-id="d970d-119">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d970d-120">Lync Server 2013 累积更新 2</span><span class="sxs-lookup"><span data-stu-id="d970d-120">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="d970d-121">Lync Server 2013 累积更新 2</span><span class="sxs-lookup"><span data-stu-id="d970d-121">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="d970d-122">是</span><span class="sxs-lookup"><span data-stu-id="d970d-122">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d970d-123">Lync Server 2013 累积更新 2</span><span class="sxs-lookup"><span data-stu-id="d970d-123">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="d970d-124">Lync Server 2013 累积更新 1</span><span class="sxs-lookup"><span data-stu-id="d970d-124">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="d970d-125">否</span><span class="sxs-lookup"><span data-stu-id="d970d-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d970d-126">Lync Server 2013 累积更新 2</span><span class="sxs-lookup"><span data-stu-id="d970d-126">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="d970d-127">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d970d-127">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="d970d-128">否</span><span class="sxs-lookup"><span data-stu-id="d970d-128">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d970d-129">Lync Server 2013 累积更新 2</span><span class="sxs-lookup"><span data-stu-id="d970d-129">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="d970d-130">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d970d-130">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d970d-131">否</span><span class="sxs-lookup"><span data-stu-id="d970d-131">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d970d-132">Lync Server 2013 累积更新 1</span><span class="sxs-lookup"><span data-stu-id="d970d-132">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="d970d-133">任意</span><span class="sxs-lookup"><span data-stu-id="d970d-133">Any</span></span></p></td>
<td><p><span data-ttu-id="d970d-134">否</span><span class="sxs-lookup"><span data-stu-id="d970d-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d970d-135">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d970d-135">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="d970d-136">任意</span><span class="sxs-lookup"><span data-stu-id="d970d-136">Any</span></span></p></td>
<td><p><span data-ttu-id="d970d-137">否</span><span class="sxs-lookup"><span data-stu-id="d970d-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d970d-138">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d970d-138">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d970d-139">任意</span><span class="sxs-lookup"><span data-stu-id="d970d-139">Any</span></span></p></td>
<td><p><span data-ttu-id="d970d-140">否</span><span class="sxs-lookup"><span data-stu-id="d970d-140">No</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a><span data-ttu-id="d970d-141">支持的客户端</span><span class="sxs-lookup"><span data-stu-id="d970d-141">Supported Clients</span></span>

<span data-ttu-id="d970d-142">支持 Lync 会议 Location-Based 路由的 Lync 客户端与支持 Lync Server 2013 Location-Based 路由的客户端相同。</span><span class="sxs-lookup"><span data-stu-id="d970d-142">The Lync clients that support Location-Based Routing of Lync meetings are the same clients that support Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="d970d-143">有关详细信息，请参阅 [客户端和服务器支持 Location-Based 路由](lync-server-2013-client-and-server-support-for-location-based-routing.md)。</span><span class="sxs-lookup"><span data-stu-id="d970d-143">For more information, please refer to [Client and Server Support for Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span></span>

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a><span data-ttu-id="d970d-144">咨询式呼叫转移的中介服务器要求</span><span class="sxs-lookup"><span data-stu-id="d970d-144">Mediation Server Requirements for Consultative Call Transfers</span></span>

<span data-ttu-id="d970d-145">Location-Based 路由会议应用程序需要部署独立的中介服务器，才能在咨询式呼叫转移上强制执行 Location-Based 路由限制。</span><span class="sxs-lookup"><span data-stu-id="d970d-145">The Location-Based Routing Conferencing application requires deploying stand-alone Mediation Servers in order to enforce Location-Based Routing restrictions on consultative call transfers.</span></span>

<span data-ttu-id="d970d-146">若要强制 Location-Based 路由使用咨询式呼叫转移，中介服务器必须仅与需要 Location-Based 路由的网络区域中的一个中介服务器对等 (（如 PBX、SIP 网关等) 相关联）。</span><span class="sxs-lookup"><span data-stu-id="d970d-146">To enforce Location-Based Routing of consultative call transfers, the Mediation Server must be associated with only one Mediation Server peer (i.e. PBX, SIP gateway, etc) in network regions where Location-Based Routing is required.</span></span> <span data-ttu-id="d970d-147">如果在同一网络区域中部署其他中介服务器对等，则中介服务器必须与不同的中介服务器相关联。</span><span class="sxs-lookup"><span data-stu-id="d970d-147">If additional Mediation Server peers are deployed in the same network region, the Mediation Server peer must be associated with a different Mediation Server .</span></span> <span data-ttu-id="d970d-148">此要求的详细信息如下：</span><span class="sxs-lookup"><span data-stu-id="d970d-148">This Requirement is detailed as follows:</span></span>

  - <span data-ttu-id="d970d-149">每台多个中介服务器对等的单中介服务器当通过配置将多个 SIP 中继配置为多个对等 (的中介服务器（即 Pbx 和网关) ），将阻止咨询呼叫转接，阻止通过某些 SIP 中继使用咨询呼叫转接，但禁止通过其他 SIP 中继。</span><span class="sxs-lookup"><span data-stu-id="d970d-149">Single Mediation Server per multiple Mediation Server peers When a consultative call transfer is routed to a Mediation Server peer through a Mediation Server that’s configured with multiple SIP trunks to multiple peers (i.e. PBXs and gateways), the consultative call transfer is blocked to prevent PSTN toll bypass if the consultative call transfer is permitted through some SIP trunks but disallowed through other SIP trunks.</span></span>
    
    <span data-ttu-id="d970d-150">例如，在单个中介服务器处理 PSTN 网关中介服务器对等和 PBX 中介服务器对等的情况下，将看到以下行为：</span><span class="sxs-lookup"><span data-stu-id="d970d-150">For example, in the case of a single Mediation Server servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="d970d-151">当来自给定网站 (的 Lync 用户（即站点 1) 尝试将具有 PSTN 终结点的呼叫从另一个站点转移到 Lync 用户 (（即 site 2) 通过咨询式转移），将禁止呼叫阻止 PSTN 免绕过。</span><span class="sxs-lookup"><span data-stu-id="d970d-151">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="d970d-152">当来自给定网站的 Lync 用户 (（例如，站点 1) 尝试将同一 (站点中的 PBX 终结点与另一个站点中的 PBX 终结点)  (（即 site 2) 通过咨询转移），即使不是在潜在的 PSTN 长途电话中不会产生呼叫，也将禁止呼叫。</span><span class="sxs-lookup"><span data-stu-id="d970d-152">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed even if it doesn’t incur in potential PSTN toll bypassing.</span></span>

  - <span data-ttu-id="d970d-153">每个中介服务器对等单独的中介服务器</span><span class="sxs-lookup"><span data-stu-id="d970d-153">Separate Mediation Servers per Mediation Server peer</span></span>
    
    <span data-ttu-id="d970d-154">当向中介服务器对等进行定向传输时，将根据中介服务器提供服务的单个中介服务器对来评估咨询转移。</span><span class="sxs-lookup"><span data-stu-id="d970d-154">When a consultative transfer is targeted at a Mediation Server Peer, the consultative transfer will be evaluated against the single Mediation Server Peer serviced by the Mediation Server.</span></span> <span data-ttu-id="d970d-155">无论其他 Mediations 服务器在不同的中介服务器中提供服务，该呼叫都将在 PSTN 免绕过的可能性内被禁止或允许使用。</span><span class="sxs-lookup"><span data-stu-id="d970d-155">The call will be disallowed or allowed based in its potential to incur in PSTN toll bypass regardless of all other Mediations Server Peers in the site as they’re serviced by separate Mediation Servers.</span></span>
    
    <span data-ttu-id="d970d-156">例如，在单独的中介服务器处理 PSTN 网关中介服务器对等和 PBX 中介服务器对等的情况下，将看到以下行为：</span><span class="sxs-lookup"><span data-stu-id="d970d-156">For example, in the case of a separate Mediation Servers servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="d970d-157">当来自给定网站 (的 Lync 用户（即站点 1) 尝试将具有 PSTN 终结点的呼叫从另一个站点转移到 Lync 用户 (（即 site 2) 通过咨询式转移），将禁止呼叫阻止 PSTN 免绕过。</span><span class="sxs-lookup"><span data-stu-id="d970d-157">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="d970d-158">当来自给定网站的 Lync 用户 (（例如，站点 1) 尝试将同一 (站点中的 PBX 终结点与另一个站点中的 PBX 终结点)  (（即 site 2) 通过咨询转移）进行传输时，将允许呼叫，因为它不会在潜在的 PSTN 收费中发生。</span><span class="sxs-lookup"><span data-stu-id="d970d-158">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be allowed as it doesn’t incur in potential PSTN toll bypassing.</span></span>

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a><span data-ttu-id="d970d-159">Location-Based 路由会议应用程序不支持的功能</span><span class="sxs-lookup"><span data-stu-id="d970d-159">Capabilities Not Supported by the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="d970d-160">Location-Based 路由会议应用程序不支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="d970d-160">The following capabilities are not supported by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="d970d-161">电话拨入式会议。</span><span class="sxs-lookup"><span data-stu-id="d970d-161">Dial-in conferencing.</span></span> <span data-ttu-id="d970d-162">不能为电话拨入式会议强制使用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="d970d-162">Location-Based Routing cannot be enforced for Dial-in conferencing.</span></span> <span data-ttu-id="d970d-163">即使会议组织者是为 Location-Based 路由启用的 Lync 用户，Location-Based 路由也不会限制对给定会议的任何拨入请求。</span><span class="sxs-lookup"><span data-stu-id="d970d-163">Any dial-in request to a given conference will not be restricted by Location-Based Routing even if the conference organizer is a Lync user enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="d970d-164">建议在需要实施 Location-Based 路由限制的区域中设置会议访问号码。</span><span class="sxs-lookup"><span data-stu-id="d970d-164">It’s recommended not to provision conferencing access numbers in regions where Location-Based Routing restrictions need to be enforced.</span></span>

<span data-ttu-id="d970d-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d970d-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

