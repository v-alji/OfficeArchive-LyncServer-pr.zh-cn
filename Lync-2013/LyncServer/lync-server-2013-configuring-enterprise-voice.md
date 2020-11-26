---
title: Lync Server 2013：配置企业语音
description: Lync Server 2013：配置企业语音。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433120"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="64820-103">在 Lync Server 2013 中配置企业语音</span><span class="sxs-lookup"><span data-stu-id="64820-103">Configuring Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64820-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64820-104">

<span> </span></span></span>

<span data-ttu-id="64820-105">_**主题上次修改时间：** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="64820-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="64820-106">若要部署企业语音，需要配置下列内容：</span><span class="sxs-lookup"><span data-stu-id="64820-106">To deploy Enterprise Voice, you’ll need to configure the following:</span></span>

  - <span data-ttu-id="64820-107">创建主干</span><span class="sxs-lookup"><span data-stu-id="64820-107">Create a Trunk</span></span>

  - <span data-ttu-id="64820-108">定义语音策略</span><span class="sxs-lookup"><span data-stu-id="64820-108">Define a Voice Policy</span></span>

  - <span data-ttu-id="64820-109">定义语音路线</span><span class="sxs-lookup"><span data-stu-id="64820-109">Define a Voice Route</span></span>

  - <span data-ttu-id="64820-110">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="64820-110">Enable Users for Enterprise Voice</span></span>

<div>

## <a name="create-a-trunk"></a><span data-ttu-id="64820-111">创建主干</span><span class="sxs-lookup"><span data-stu-id="64820-111">Create a Trunk</span></span>

<span data-ttu-id="64820-112">您必须在您的企业语音部署中定义中继。</span><span class="sxs-lookup"><span data-stu-id="64820-112">You must define trunks in your Enterprise Voice deployment.</span></span> <span data-ttu-id="64820-113">对于 Location-Based 路由，必须为每个主干创建中继配置。</span><span class="sxs-lookup"><span data-stu-id="64820-113">For Location-Based Routing, you must create a trunk configuration per trunk.</span></span> <span data-ttu-id="64820-114">使用 Lync Server 拓扑生成器定义你的中继，并使用 Lync Server Windows PowerShell 命令、新 New-cstrunkconfiguration 或 Lync Server 控制面板定义相应的 trunk 配置。</span><span class="sxs-lookup"><span data-stu-id="64820-114">Use the Lync Server Topology Builder to define your trunks, and use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, or the Lync Server Control Panel to define the corresponding trunk configurations.</span></span> <span data-ttu-id="64820-115">有关如何启用中继配置上 Location-Based 路由的详细信息，请参阅本部分中的在 [Lync Server 2013 中启用 Location-Based 路由](lync-server-2013-enabling-location-based-routing.md)的 Location-Based 路由到中继。</span><span class="sxs-lookup"><span data-stu-id="64820-115">More information on how to enable Location-Based Routing on trunk configurations can be found in the section, Enable Location-Based Routing to Trunks, in the topic, [Enabling Location-Based Routing in Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span></span> <span data-ttu-id="64820-116">对于此示例，下表介绍了此方案中使用的中继。</span><span class="sxs-lookup"><span data-stu-id="64820-116">For this example, the following table illustrates the trunks used in this scenario.</span></span>

<span data-ttu-id="64820-117">有关详细信息，请参阅 [在 Lync Server 2013 的拓扑生成器中定义其他中继](lync-server-2013-define-additional-trunks-in-topology-builder.md)。</span><span class="sxs-lookup"><span data-stu-id="64820-117">For more information, see [Define additional trunks in Topology Builder in Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64820-118">主干名称</span><span class="sxs-lookup"><span data-stu-id="64820-118">Trunk name</span></span></th>
<th><span data-ttu-id="64820-119">系统类型</span><span class="sxs-lookup"><span data-stu-id="64820-119">System type</span></span></th>
<th><span data-ttu-id="64820-120">名称</span><span class="sxs-lookup"><span data-stu-id="64820-120">Name</span></span></th>
<th><span data-ttu-id="64820-121">位置</span><span class="sxs-lookup"><span data-stu-id="64820-121">Location</span></span></th>
<th><span data-ttu-id="64820-122">中介服务器</span><span class="sxs-lookup"><span data-stu-id="64820-122">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64820-123">干线 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="64820-123">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="64820-124">PSTN 网关</span><span class="sxs-lookup"><span data-stu-id="64820-124">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="64820-125">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="64820-125">DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="64820-126">Delhi</span><span class="sxs-lookup"><span data-stu-id="64820-126">Delhi</span></span></p></td>
<td><p><span data-ttu-id="64820-127">MS1</span><span class="sxs-lookup"><span data-stu-id="64820-127">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64820-128">主干 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="64820-128">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="64820-129">PSTN 网关</span><span class="sxs-lookup"><span data-stu-id="64820-129">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="64820-130">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="64820-130">HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="64820-131">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="64820-131">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="64820-132">MS1</span><span class="sxs-lookup"><span data-stu-id="64820-132">MS1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64820-133">干线 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="64820-133">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="64820-134">PBX</span><span class="sxs-lookup"><span data-stu-id="64820-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="64820-135">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="64820-135">DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="64820-136">Delhi</span><span class="sxs-lookup"><span data-stu-id="64820-136">Delhi</span></span></p></td>
<td><p><span data-ttu-id="64820-137">MS1</span><span class="sxs-lookup"><span data-stu-id="64820-137">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64820-138">主干 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="64820-138">Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="64820-139">PBX</span><span class="sxs-lookup"><span data-stu-id="64820-139">PBX</span></span></p></td>
<td><p><span data-ttu-id="64820-140">HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="64820-140">HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="64820-141">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="64820-141">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="64820-142">MS1</span><span class="sxs-lookup"><span data-stu-id="64820-142">MS1</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a><span data-ttu-id="64820-143">定义语音策略</span><span class="sxs-lookup"><span data-stu-id="64820-143">Defines Voice Policies</span></span>

<span data-ttu-id="64820-144">您必须为您的企业语音部署定义语音策略。</span><span class="sxs-lookup"><span data-stu-id="64820-144">You must define voice policies for your Enterprise Voice deployment.</span></span> <span data-ttu-id="64820-145">定义语音策略，以对用户的子集强制执行 Location-Based 路由限制，前提是只有它们的子集才能使用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="64820-145">Define a Voice Policy to enforce Location-Based Routing restrictions to a subset of users if only a subset of them is required to use Location-Based Routing.</span></span> <span data-ttu-id="64820-146">对于此示例，下表介绍了此方案中使用的语音策略。</span><span class="sxs-lookup"><span data-stu-id="64820-146">For this example, the following table illustrates the voice policies used in this scenario.</span></span> <span data-ttu-id="64820-147">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="64820-147">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="64820-148">有关详细信息，请参阅 [配置语音策略和 PSTN 使用记录以在 Lync Server 2013 中授权呼叫功能和权限](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md)。</span><span class="sxs-lookup"><span data-stu-id="64820-148">For more information, see [Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="64820-149">语音策略1</span><span class="sxs-lookup"><span data-stu-id="64820-149">Voice policy 1</span></span></th>
<th><span data-ttu-id="64820-150">语音政策2</span><span class="sxs-lookup"><span data-stu-id="64820-150">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64820-151">语音策略 ID</span><span class="sxs-lookup"><span data-stu-id="64820-151">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="64820-152">新德里语音政策</span><span class="sxs-lookup"><span data-stu-id="64820-152">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="64820-153">Hyderabad 语音政策</span><span class="sxs-lookup"><span data-stu-id="64820-153">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64820-154">PSTN 用法</span><span class="sxs-lookup"><span data-stu-id="64820-154">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="64820-155">新德里使用，PBX Del 用法，PBX Hyd 用法</span><span class="sxs-lookup"><span data-stu-id="64820-155">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="64820-156">Hyderabad 使用，PBX Hyd 使用，PBX Del 使用</span><span class="sxs-lookup"><span data-stu-id="64820-156">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64820-157">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="64820-157">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="64820-158">False</span><span class="sxs-lookup"><span data-stu-id="64820-158">False</span></span></p></td>
<td><p><span data-ttu-id="64820-159">False</span><span class="sxs-lookup"><span data-stu-id="64820-159">False</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a><span data-ttu-id="64820-160">定义语音路由</span><span class="sxs-lookup"><span data-stu-id="64820-160">Define Voice Routes</span></span>

<span data-ttu-id="64820-161">您必须为您的企业语音部署定义语音路由。</span><span class="sxs-lookup"><span data-stu-id="64820-161">You must define voice routes for your Enterprise Voice deployment.</span></span> <span data-ttu-id="64820-162">对于此示例，下表介绍了在此方案中使用的语音路线。</span><span class="sxs-lookup"><span data-stu-id="64820-162">For this example, the following table illustrates the voice routes used in this scenario.</span></span> <span data-ttu-id="64820-163">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="64820-163">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="64820-164">有关详细信息，请参阅 [在 Lync Server 2013 中配置出站呼叫的语音路由](lync-server-2013-configuring-voice-routes-for-outbound-calls.md)。</span><span class="sxs-lookup"><span data-stu-id="64820-164">For more information, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="64820-165">语音路由1</span><span class="sxs-lookup"><span data-stu-id="64820-165">Voice route 1</span></span></th>
<th><span data-ttu-id="64820-166">语音路由2</span><span class="sxs-lookup"><span data-stu-id="64820-166">Voice route 2</span></span></th>
<th><span data-ttu-id="64820-167">语音路由3</span><span class="sxs-lookup"><span data-stu-id="64820-167">Voice route 3</span></span></th>
<th><span data-ttu-id="64820-168">语音路由4</span><span class="sxs-lookup"><span data-stu-id="64820-168">Voice route 4</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64820-169">名称</span><span class="sxs-lookup"><span data-stu-id="64820-169">Name</span></span></p></td>
<td><p><span data-ttu-id="64820-170">新德里路线</span><span class="sxs-lookup"><span data-stu-id="64820-170">Delhi route</span></span></p></td>
<td><p><span data-ttu-id="64820-171">Hyderabad 路线</span><span class="sxs-lookup"><span data-stu-id="64820-171">Hyderabad route</span></span></p></td>
<td><p><span data-ttu-id="64820-172">PBX Del 路由</span><span class="sxs-lookup"><span data-stu-id="64820-172">PBX Del route</span></span></p></td>
<td><p><span data-ttu-id="64820-173">PBX Hyd 路线</span><span class="sxs-lookup"><span data-stu-id="64820-173">PBX Hyd route</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64820-174">PSTN 用法</span><span class="sxs-lookup"><span data-stu-id="64820-174">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="64820-175">新德里使用</span><span class="sxs-lookup"><span data-stu-id="64820-175">Delhi usage</span></span></p></td>
<td><p><span data-ttu-id="64820-176">Hyderabad 用法</span><span class="sxs-lookup"><span data-stu-id="64820-176">Hyderabad usage</span></span></p></td>
<td><p><span data-ttu-id="64820-177">PBX Del 使用</span><span class="sxs-lookup"><span data-stu-id="64820-177">PBX Del usage</span></span></p></td>
<td><p><span data-ttu-id="64820-178">PBX Hyd 使用情况</span><span class="sxs-lookup"><span data-stu-id="64820-178">PBX Hyd usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64820-179">中继</span><span class="sxs-lookup"><span data-stu-id="64820-179">Trunk</span></span></p></td>
<td><p><span data-ttu-id="64820-180">干线 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="64820-180">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="64820-181">主干 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="64820-181">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="64820-182">干线 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="64820-182">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="64820-183">主干 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="64820-183">Trunk 4 HYD-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a><span data-ttu-id="64820-184">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="64820-184">Enable Users for Enterprise Voice</span></span>

<span data-ttu-id="64820-185">为用户启用企业语音，并为他们分配你以前定义的语音策略。</span><span class="sxs-lookup"><span data-stu-id="64820-185">Enable users for Enterprise Voice and assign them a voice policy you’ve previously defined.</span></span> <span data-ttu-id="64820-186">对于此示例，下表介绍了此方案中使用的作业。</span><span class="sxs-lookup"><span data-stu-id="64820-186">For this example, the following table illustrates the assignment used in this scenario.</span></span> <span data-ttu-id="64820-187">只有特定于 Location-Based 路由的设置才会包含在表中，以供说明之用。</span><span class="sxs-lookup"><span data-stu-id="64820-187">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="64820-188">有关详细信息，请参阅 [在 Lync Server 2013 中启用企业语音用户](lync-server-2013-enable-users-for-enterprise-voice.md)。</span><span class="sxs-lookup"><span data-stu-id="64820-188">For more information, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="64820-189">位于新德里的用户</span><span class="sxs-lookup"><span data-stu-id="64820-189">Users located in Delhi</span></span></th>
<th><span data-ttu-id="64820-190">位于 Hyderabad 的用户</span><span class="sxs-lookup"><span data-stu-id="64820-190">Users located in Hyderabad</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64820-191">关联的语音政策</span><span class="sxs-lookup"><span data-stu-id="64820-191">Associated voice policy</span></span></p></td>
<td><p><span data-ttu-id="64820-192">新德里语音政策</span><span class="sxs-lookup"><span data-stu-id="64820-192">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="64820-193">Hyderabad 语音政策</span><span class="sxs-lookup"><span data-stu-id="64820-193">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64820-194">示例用户</span><span class="sxs-lookup"><span data-stu-id="64820-194">Sample users</span></span></p></td>
<td><p><span data-ttu-id="64820-195">DEL-LYNC-1、DEL-LYNC-2、DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="64820-195">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
<td><p><span data-ttu-id="64820-196">HYD-LYNC-1，HYD-LYNC-2，HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="64820-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="64820-197">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64820-197">See Also</span></span>


[<span data-ttu-id="64820-198">在 Lync Server 2013 中配置基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="64820-198">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="64820-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64820-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

