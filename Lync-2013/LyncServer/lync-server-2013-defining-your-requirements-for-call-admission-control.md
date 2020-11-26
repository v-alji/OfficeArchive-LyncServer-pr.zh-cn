---
title: Lync Server 2013：定义呼叫允许控制要求
description: Lync Server 2013：定义呼叫许可控制的要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your organization's requirements for call admission control
ms:assetid: 5122171a-a5b0-4059-b033-846caec10d1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398334(v=OCS.15)
ms:contentKeyID: 48184104
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9f675ac5811e0c0c1c23dc76ebb8b4525857836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430863"
---
# <a name="defining-your-requirements-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="a3377-103">在 Lync Server 2013 中定义呼叫允许控制要求</span><span class="sxs-lookup"><span data-stu-id="a3377-103">Defining your requirements for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3377-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3377-104">

<span> </span></span></span>

<span data-ttu-id="a3377-105">_**主题上次修改时间：** 2013-10-28_</span><span class="sxs-lookup"><span data-stu-id="a3377-105">_**Topic Last Modified:** 2013-10-28_</span></span>

<span data-ttu-id="a3377-p101">规划呼叫允许控制 (CAC) 需要有关企业网络拓扑的详细信息。为了帮助您规划呼叫允许控制策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a3377-p101">Planning for call admission control (CAC) requires detailed information about your enterprise network topology. To help plan your call admission control policies, follow these steps.</span></span>

1.  <span data-ttu-id="a3377-108">确认企业网络中的中心/中枢（称为 *网络区域*）。</span><span class="sxs-lookup"><span data-stu-id="a3377-108">Identify the hubs/backbones (called *network regions*) within your enterprise network.</span></span>

2.  <span data-ttu-id="a3377-109">确认每个网络区域中的办公室或位置（称为 *网络站点*）。</span><span class="sxs-lookup"><span data-stu-id="a3377-109">Identify the offices or locations (called *network sites*) within each network region.</span></span>

3.  <span data-ttu-id="a3377-110">确定每对网络区域之间的网络路由。</span><span class="sxs-lookup"><span data-stu-id="a3377-110">Determine the network route between every pair of network regions.</span></span>

4.  <span data-ttu-id="a3377-111">确定对每个 WAN 链路的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="a3377-111">Determine the bandwidth limits for each WAN link.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a3377-112">带宽限制指 WAN 链接上的多少带宽已分配给企业语音和音频/视频流量。</span><span class="sxs-lookup"><span data-stu-id="a3377-112">Bandwidth limits refer to how much of the bandwidth on a WAN link is allocated to Enterprise Voice and audio/video traffic.</span></span> <span data-ttu-id="a3377-113">当 WAN 链路被描述为“带宽受限”时，表示该 WAN 链路具有低于链接上预期高峰流量的带宽限制。</span><span class="sxs-lookup"><span data-stu-id="a3377-113">When a WAN link is described as “bandwidth-constrained,” the WAN link has a bandwidth limit that is lower than the expected peak traffic over the link.</span></span>

    
    </div>

5.  <span data-ttu-id="a3377-114">标识分配给每个网络站点的 IP 子网。</span><span class="sxs-lookup"><span data-stu-id="a3377-114">Identify the IP subnets that are assigned to each network site.</span></span>

<span data-ttu-id="a3377-115">下面，我们将通过下图所示示例网络拓扑来解释这些概念。</span><span class="sxs-lookup"><span data-stu-id="a3377-115">To explain these concepts, we’ll use the example network topology shown in the following figure.</span></span>

<span data-ttu-id="a3377-116">**呼叫允许控制的示例拓扑**</span><span class="sxs-lookup"><span data-stu-id="a3377-116">**Example topology for call admission control**</span></span>

<span data-ttu-id="a3377-117">![Litware Inc. 网络拓扑示例](images/Gg398334.477f3b52-2973-4026-9bc0-b1c6bf9f4803(OCS.15).jpg "Litware Inc. 网络拓扑示例")</span><span class="sxs-lookup"><span data-stu-id="a3377-117">![Litware Inc. Network Topology Example](images/Gg398334.477f3b52-2973-4026-9bc0-b1c6bf9f4803(OCS.15).jpg "Litware Inc. Network Topology Example")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a3377-p103">所有网络站点都与一个网络区域关联。例如，波特兰、里诺和阿尔伯克基包括在北美区域中。在此图中，只显示应用了 CAC 策略、具有带宽限制的 WAN 链路。芝加哥、纽约和底特律的网络站点在北美区域椭圆中显示，因为这些区域没有带宽限定，因此不需要 CAC 策略。</span><span class="sxs-lookup"><span data-stu-id="a3377-p103">All network sites are associated with a network region. For example, Portland, Reno, and Albuquerque are included in the North America region. In this figure, only WAN links that have CAC policies applied are shown, with bandwidth limits. The network sites of Chicago, New York, and Detroit are shown inside the North America region oval because they are not bandwidth-constrained, and therefore do not require CAC policies.</span></span>



</div>

<span data-ttu-id="a3377-122">以下各节将介绍此示例拓扑的组件。</span><span class="sxs-lookup"><span data-stu-id="a3377-122">The components of this example topology are explained in the following sections.</span></span> <span data-ttu-id="a3377-123">有关如何计划此拓扑的详细信息，包括带宽限制，请参阅 [示例：在 Lync Server 2013 中收集呼叫许可控制的要求](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md)。</span><span class="sxs-lookup"><span data-stu-id="a3377-123">For details about how this topology was planned, including the bandwidth limits, see [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md).</span></span>

<div>

## <a name="identify-network-regions"></a><span data-ttu-id="a3377-124">确认网络区域</span><span class="sxs-lookup"><span data-stu-id="a3377-124">Identify Network Regions</span></span>

<span data-ttu-id="a3377-125">网络区域代表网络中枢或网络中心。</span><span class="sxs-lookup"><span data-stu-id="a3377-125">A network region represents a network backbone or a network hub.</span></span>

<span data-ttu-id="a3377-p105">网络中枢或中心是计算机网络基础结构的一部分，它将网络的不同部分相互连接起来，为不同 LAN 或子网间的信息交换提供路径。网络中枢可以将各种网络关联在一起，适用范围从较小区域到广阔的地理区域。网络中枢的容量通常大于与其连接的网络的容量。</span><span class="sxs-lookup"><span data-stu-id="a3377-p105">A network backbone or hub is a part of computer network infrastructure that interconnects different parts of the network, providing a path for the exchange of information between different LANs or subnets. A backbone can tie together diverse networks from a small location to a wide geographic area. The backbone's capacity is typically greater than that of the networks that connect to it.</span></span>

<span data-ttu-id="a3377-p106">示例拓扑具有三个网络区域：北美、EMEA 和 APAC。网络区域是网络站点的集合（请参阅本主题后面的网络站点定义）。与您的网络运营团队一起确认网络区域。</span><span class="sxs-lookup"><span data-stu-id="a3377-p106">Our example topology has three network regions: North America, EMEA, and APAC. A network region contains a collection of network sites (see the definition of network sites later in this topic). Work with your network operations team to identify your network regions.</span></span>

</div>

<div>

## <a name="associating-a-central-site-with-each-network-region"></a><span data-ttu-id="a3377-132">将中央站点与每个网络区域相关联</span><span class="sxs-lookup"><span data-stu-id="a3377-132">Associating a Central Site with each Network Region</span></span>

<span data-ttu-id="a3377-133">CAC 要求为每个网络区域定义 Lync Server 中心网站。</span><span class="sxs-lookup"><span data-stu-id="a3377-133">CAC requires that a Lync Server central site is defined for each network region.</span></span> <span data-ttu-id="a3377-134">从该网络区域中的所有站点中选择具有最佳网络连接性和最高带宽的站点作为中央站点。</span><span class="sxs-lookup"><span data-stu-id="a3377-134">The central site is selected with the best network connectivity and highest bandwidth to all the other sites within that network region.</span></span> <span data-ttu-id="a3377-135">前面的网络拓扑示例显示了三个网络区域，每个网络区域都有一个管理 CAC 决策的中央站点。</span><span class="sxs-lookup"><span data-stu-id="a3377-135">The preceding example of network topology shows three network regions, each with a central site that manages CAC decisions.</span></span> <span data-ttu-id="a3377-136">前面示例中的相应关联如下表所示。</span><span class="sxs-lookup"><span data-stu-id="a3377-136">From the preceding example, the appropriate association is shown in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a3377-137">中央站点不一定与网络站点对应。</span><span class="sxs-lookup"><span data-stu-id="a3377-137">Central sites do not necessarily correspond to network sites.</span></span> <span data-ttu-id="a3377-138">在本文档的示例中，某些中央站点（芝加哥、伦敦和北京）与网络站点共享同一名称。</span><span class="sxs-lookup"><span data-stu-id="a3377-138">In the examples in this documentation, some central sites—Chicago, London, and Beijing—share the same name as the network sites.</span></span> <span data-ttu-id="a3377-139">但是，即使中心网站和网络网站共享相同的名称，中心网站也是 Lync Server 拓扑的一个元素，而网络站点是 Lync Server 拓扑所在的整个网络的一部分。</span><span class="sxs-lookup"><span data-stu-id="a3377-139">However, even if a central site and network site share the same name, the central site is an element of the Lync Server topology, whereas the network site is a part of the overall network in which the Lync Server topology resides.</span></span>



</div>

### <a name="network-regions-central-sites-and-network-sites"></a><span data-ttu-id="a3377-140">网络区域、中央站点和网络站点</span><span class="sxs-lookup"><span data-stu-id="a3377-140">Network regions, central sites, and network sites</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3377-141">网络区域</span><span class="sxs-lookup"><span data-stu-id="a3377-141">Network Region</span></span></th>
<th><span data-ttu-id="a3377-142">中央站点</span><span class="sxs-lookup"><span data-stu-id="a3377-142">Central Site</span></span></th>
<th><span data-ttu-id="a3377-143">网络站点</span><span class="sxs-lookup"><span data-stu-id="a3377-143">Network Sites</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3377-144">北美</span><span class="sxs-lookup"><span data-stu-id="a3377-144">North America</span></span></p></td>
<td><p><span data-ttu-id="a3377-145">芝加哥</span><span class="sxs-lookup"><span data-stu-id="a3377-145">Chicago</span></span></p></td>
<td><p><span data-ttu-id="a3377-146">芝加哥</span><span class="sxs-lookup"><span data-stu-id="a3377-146">Chicago</span></span></p>
<p><span data-ttu-id="a3377-147">纽约</span><span class="sxs-lookup"><span data-stu-id="a3377-147">New York</span></span></p>
<p><span data-ttu-id="a3377-148">底特律</span><span class="sxs-lookup"><span data-stu-id="a3377-148">Detroit</span></span></p>
<p><span data-ttu-id="a3377-149">波特兰</span><span class="sxs-lookup"><span data-stu-id="a3377-149">Portland</span></span></p>
<p><span data-ttu-id="a3377-150">里诺</span><span class="sxs-lookup"><span data-stu-id="a3377-150">Reno</span></span></p>
<p><span data-ttu-id="a3377-151">阿尔伯克基</span><span class="sxs-lookup"><span data-stu-id="a3377-151">Albuquerque</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3377-152">EMEA</span><span class="sxs-lookup"><span data-stu-id="a3377-152">EMEA</span></span></p></td>
<td><p><span data-ttu-id="a3377-153">伦敦</span><span class="sxs-lookup"><span data-stu-id="a3377-153">London</span></span></p></td>
<td><p><span data-ttu-id="a3377-154">伦敦</span><span class="sxs-lookup"><span data-stu-id="a3377-154">London</span></span></p>
<p><span data-ttu-id="a3377-155">科隆</span><span class="sxs-lookup"><span data-stu-id="a3377-155">Cologne</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3377-156">APAC</span><span class="sxs-lookup"><span data-stu-id="a3377-156">APAC</span></span></p></td>
<td><p><span data-ttu-id="a3377-157">北京</span><span class="sxs-lookup"><span data-stu-id="a3377-157">Beijing</span></span></p></td>
<td><p><span data-ttu-id="a3377-158">北京</span><span class="sxs-lookup"><span data-stu-id="a3377-158">Beijing</span></span></p>
<p><span data-ttu-id="a3377-159">马尼拉</span><span class="sxs-lookup"><span data-stu-id="a3377-159">Manila</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="identify-network-sites"></a><span data-ttu-id="a3377-160">确认网络站点</span><span class="sxs-lookup"><span data-stu-id="a3377-160">Identify Network Sites</span></span>

<span data-ttu-id="a3377-p109">网络站点是指为组织提供了实际场地（如办公室、建筑群或校园）的位置。具有 LAN 并与其他站点建立 WAN 连接的实际场地被视为网络站点。从清点组织的所有办公室开始。在我们的示例拓扑中，北美网络区域包括以下网络站点：纽约、芝加哥、底特律、波特兰、里诺和阿尔伯克基。</span><span class="sxs-lookup"><span data-stu-id="a3377-p109">A network site represents a location where your organization has a physical venue—for example, offices, a set of buildings, or a campus. A physical venue with a LAN and has WAN connectivity to other sites is considered a network site. Start by inventorying all of your organization’s offices. In our example topology, the North America network region consists of the following network sites: New York, Chicago, Detroit, Portland, Reno, and Albuquerque.</span></span>

<span data-ttu-id="a3377-p110">必须将每个网络站点与某个网络区域关联。根据网络站点是否具有受限 WAN 链路，将带宽策略与网络站点相关联。有关 CAC 策略以及使用这些策略分配的带宽的详细信息，请参阅本主题后面介绍的“定义带宽策略”。要配置 CAC，请将网络站点与网络区域相关联，然后创建应用于给定站点或区域之间的带宽受限连接以及站点和区域之间的 WAN 连接的带宽分配策略。</span><span class="sxs-lookup"><span data-stu-id="a3377-p110">You must associate every network site with a network region. Depending on whether the network site has a constrained WAN link, a bandwidth policy is associated with the network site. For details about CAC policies and the bandwidth that you allocate by using them, see "Define Bandwidth Policies" later in this topic. To configure CAC, you associate network sites with network regions, and then you create bandwidth-allocating policies to apply to the bandwidth-constrained connections between a given site or region and the WAN connections between the sites and regions.</span></span>

</div>

<div>

## <a name="identify-network-links"></a><span data-ttu-id="a3377-169">确认网络链接</span><span class="sxs-lookup"><span data-stu-id="a3377-169">Identify Network Links</span></span>

<span data-ttu-id="a3377-p111">网络链接是指与链接不同区域和站点的物理 WAN 的连接。我们的示例拓扑中包括两个区域网络链接，区域和站点之间的五个网络链接，以及两个站点之间的一个网络链接。</span><span class="sxs-lookup"><span data-stu-id="a3377-p111">Network links represent connections to the physical WAN that links different regions and sites. In our example topology, there are two regional network links, five network links between regions and sites, and one network link between two sites.</span></span>

<span data-ttu-id="a3377-172">两个区域链接分别为北美和 EMEA 之间的链接以及 APAC 和 EMEA 之间的链接，分别表示为 NA-EMEA-LINK 和 EMEA-APAC-LINK。</span><span class="sxs-lookup"><span data-stu-id="a3377-172">The two regional links are between North America and EMEA, represented as NA-EMEA-LINK, and between APAC and EMEA, represented as EMEA-APAC-LINK.</span></span>

<span data-ttu-id="a3377-p112">站点链接由将波特兰、里诺和阿尔伯克基连接到北美区域、将马尼拉连接到 APAC 区域、以及将科隆连接到 EMEA 区域的线路表示。里诺和阿尔伯克基之间的线路显示了这两个站点之间的直接网络链接。</span><span class="sxs-lookup"><span data-stu-id="a3377-p112">The site links are indicated by the lines connecting Portland, Reno, and Albuquerque to the North America region, Manila to the APAC region, and Cologne to the EMEA region. The line between Reno and Albuquerque shows a direct network link between these two sites.</span></span>

</div>

<div>

## <a name="define-bandwidth-policies"></a><span data-ttu-id="a3377-175">定义带宽策略</span><span class="sxs-lookup"><span data-stu-id="a3377-175">Define Bandwidth Policies</span></span>

<span data-ttu-id="a3377-p113">与您的网络运营团队一起确定可用于组织中跨 WAN 链路的实时音频和视频流量的带宽。如果带宽使用量受限；即，如果预期使用的带宽大于可为音频和视频形式分配的带宽，则带宽策略通常应用于 WAN 链路。</span><span class="sxs-lookup"><span data-stu-id="a3377-p113">Work with your network operations team to determine how much WAN bandwidth is available for real-time audio and video traffic across the WAN links in your organization. Bandwidth policies are typically applied to WAN links if the bandwidth usage is constrained; that is, if it expected to be more than the bandwidth that can be allocated for audio and video modalities.</span></span>

<span data-ttu-id="a3377-p114">CAC *带宽策略* 定义可为实时音频和视频形式保留的最大带宽。由于 CAC 不限制其他流量的带宽，因此它无法阻止其他数据流量（如大型文件传输、音乐流）占用所有网络带宽。</span><span class="sxs-lookup"><span data-stu-id="a3377-p114">CAC *bandwidth policies* define the maximum bandwidth that can be reserved for real-time audio and video modalities. Since CAC does not limit the bandwidth of other traffic, it cannot prevent other data traffic such as a large file transfer, music streaming, from using up all of the network bandwidth.</span></span>

<span data-ttu-id="a3377-180">CAC 带宽策略可定义下列任何内容或所有内容：</span><span class="sxs-lookup"><span data-stu-id="a3377-180">CAC bandwidth policies can define any or all of the following:</span></span>

  - <span data-ttu-id="a3377-181">分配给音频的最大带宽总量。</span><span class="sxs-lookup"><span data-stu-id="a3377-181">Maximum total bandwidth allocated for audio.</span></span>

  - <span data-ttu-id="a3377-182">分配给视频的最大带宽总量。</span><span class="sxs-lookup"><span data-stu-id="a3377-182">Maximum total bandwidth allocated for video.</span></span>

  - <span data-ttu-id="a3377-183">分配给单个音频呼叫（会话）的最大带宽。</span><span class="sxs-lookup"><span data-stu-id="a3377-183">Maximum bandwidth allocated for a single audio call (session).</span></span>

  - <span data-ttu-id="a3377-184">分配给单个视频呼叫（会话）的最大带宽。</span><span class="sxs-lookup"><span data-stu-id="a3377-184">Maximum bandwidth allocated for a single video call (session).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a3377-185">所有 CAC 带宽值均表示最大“<EM>单向</EM>”带宽限制。</span><span class="sxs-lookup"><span data-stu-id="a3377-185">All CAC bandwidth values represent the maximum <EM>unidirectional</EM> bandwidth limits.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="a3377-186">Lync Server 2013 语音策略功能提供了将对传入呼叫的带宽策略检查覆盖给用户 (的功能，而不是由用户) 发出的传出呼叫。</span><span class="sxs-lookup"><span data-stu-id="a3377-186">The Lync Server 2013 Voice Policy features provide the ability to override bandwidth policy checks for incoming calls to the user (not for outgoing calls that are placed by the user).</span></span> <span data-ttu-id="a3377-187">建立会话后，将准确计算带宽消耗。</span><span class="sxs-lookup"><span data-stu-id="a3377-187">After the session is established, the bandwidth consumption will be accurately accounted for.</span></span> <span data-ttu-id="a3377-188">应慎用此设置。</span><span class="sxs-lookup"><span data-stu-id="a3377-188">This setting should be used sparingly.</span></span> <span data-ttu-id="a3377-189">有关详细信息，请参阅在 <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">Lync server 2013 中创建语音策略和配置 pstn 使用记录</A> 或在部署文档的 <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">lync Server 2013 中修改语音策略和配置 pstn 使用记录</A> 。</span><span class="sxs-lookup"><span data-stu-id="a3377-189">For details, see <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">Create a voice policy and configure PSTN usage records in Lync Server 2013</A> or <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">Modify a voice policy and configure PSTN usage records in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="a3377-p116">要基于每个会话优化带宽用量，请考虑将要使用的音频和视频编解码器的类型。特别要避免出现为预期要频繁使用的编解码器分配的带宽不足的情况。相反，如果要阻止媒体使用需要更多带宽的编解码器，则应将每个会话的最大带宽设置为足以阻止此类使用的较低值。对于音频，并不是每一种编解码器都适用于每一种方案。例如：</span><span class="sxs-lookup"><span data-stu-id="a3377-p116">To optimize bandwidth utilization on a per-session basis, consider the type of audio and video codecs that will be used. In particular, avoid allocating insufficient bandwidth for a codec that you expect to be used frequently. Conversely, if you want to prevent media from using a codec that requires more bandwidth, you should set the maximum bandwidth per session low enough to discourage such use. For audio, not every codec is available for every scenario. For example:</span></span>

  - <span data-ttu-id="a3377-195">当你考虑编解码器的带宽和优先级时，Lync 终结点之间的对等音频呼叫将使用 RTAudio (8kHz) 或 RTAudio (16kHz) 。</span><span class="sxs-lookup"><span data-stu-id="a3377-195">Peer-to-peer audio calls between Lync endpoints will use either RTAudio (8kHz) or RTAudio (16kHz) when you factor in the bandwidth and prioritization of codecs.</span></span>

  - <span data-ttu-id="a3377-196">Lync 终结点和 A/V 会议服务之间的电话会议将使用722或 Siren。</span><span class="sxs-lookup"><span data-stu-id="a3377-196">Conference calls between Lync endpoints and the A/V Conferencing service will use either G.722 or Siren.</span></span>

  - <span data-ttu-id="a3377-197">对公共交换电话网络 (PSTN) 或来自 Lync 终结点的呼叫将使用711或 RTAudio (8kHz) 。</span><span class="sxs-lookup"><span data-stu-id="a3377-197">Calls to the public switched telephone network (PSTN) either to or from Lync endpoints will use either G.711 or RTAudio (8kHz).</span></span>

<span data-ttu-id="a3377-198">借助下表优化每个会话的最大带宽设置。</span><span class="sxs-lookup"><span data-stu-id="a3377-198">Use the following table to help optimize the maximum per-session bandwidth settings.</span></span>

### <a name="bandwidth-utilization-by-codecs"></a><span data-ttu-id="a3377-199">不同编解码器的带宽用量要求</span><span class="sxs-lookup"><span data-stu-id="a3377-199">Bandwidth utilization by codecs</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3377-200">编解码器</span><span class="sxs-lookup"><span data-stu-id="a3377-200">Codec</span></span></th>
<th><span data-ttu-id="a3377-201">不带前向纠错 (FEC) 的带宽要求</span><span class="sxs-lookup"><span data-stu-id="a3377-201">Bandwidth requirement with no forward error correction (FEC)</span></span></th>
<th><span data-ttu-id="a3377-202">带前向纠错 (FEC) 的带宽要求</span><span class="sxs-lookup"><span data-stu-id="a3377-202">Bandwidth requirement with forward error correction (FEC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3377-203">RTAudio (8kHz)</span><span class="sxs-lookup"><span data-stu-id="a3377-203">RTAudio (8kHz)</span></span></p></td>
<td><p><span data-ttu-id="a3377-204">49.8 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-204">49.8 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-205">61.6 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-205">61.6 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3377-206">RTAudio (16kHz)</span><span class="sxs-lookup"><span data-stu-id="a3377-206">RTAudio (16kHz)</span></span></p></td>
<td><p><span data-ttu-id="a3377-207">67 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-207">67 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-208">96 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-208">96 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3377-209">Siren</span><span class="sxs-lookup"><span data-stu-id="a3377-209">Siren</span></span></p></td>
<td><p><span data-ttu-id="a3377-210">57.6 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-210">57.6 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-211">73.6 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-211">73.6 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3377-212">G.711</span><span class="sxs-lookup"><span data-stu-id="a3377-212">G.711</span></span></p></td>
<td><p><span data-ttu-id="a3377-213">102 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-213">102 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-214">166 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-214">166 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3377-215">G.722</span><span class="sxs-lookup"><span data-stu-id="a3377-215">G.722</span></span></p></td>
<td><p><span data-ttu-id="a3377-216">105.6 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-216">105.6 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-217">169.6 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-217">169.6 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3377-218">RTVideo (CIF 15 fps)</span><span class="sxs-lookup"><span data-stu-id="a3377-218">RTVideo (CIF 15 fps)</span></span></p></td>
<td><p><span data-ttu-id="a3377-219">260 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-219">260 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-220">不适用</span><span class="sxs-lookup"><span data-stu-id="a3377-220">Not applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3377-221">RTVideo (VGA 30 fps)</span><span class="sxs-lookup"><span data-stu-id="a3377-221">RTVideo (VGA 30 fps)</span></span></p></td>
<td><p><span data-ttu-id="a3377-222">610 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-222">610 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-223">不适用</span><span class="sxs-lookup"><span data-stu-id="a3377-223">Not applicable</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a3377-p117">带宽要求考虑以下几项的开销：以太网 II、IP、用户数据报协议 (UDP)、RTP（实时传输协议）和 SRTP（安全实时传输协议）。其中还包括 RTCP 开销 (10 kbps)。</span><span class="sxs-lookup"><span data-stu-id="a3377-p117">Bandwidth requirements take into account overhead for the following: Ethernet II, IP, User Datagram Protocol (UDP), RTP (real-time transport protocol), and SRTP (secure real-time transport protocol). They also include 10 kbps for RTCP overhead.</span></span>



</div>

<span data-ttu-id="a3377-226">G.722.1 和 Siren 编解码器类似，但是它们提供不同的比特率。</span><span class="sxs-lookup"><span data-stu-id="a3377-226">The G.722.1 and Siren codecs are similar, but they offer different bit rates.</span></span>

<span data-ttu-id="a3377-227">722是 Lync Server 会议的默认编解码器，与722.1 和 Siren 编解码器完全不同。</span><span class="sxs-lookup"><span data-stu-id="a3377-227">G.722, the default codec for Lync Server conferencing, is completely different from the G.722.1 and Siren codecs.</span></span>

<span data-ttu-id="a3377-228">在以下情况下，在 Lync Server 中使用 Siren 编解码器：</span><span class="sxs-lookup"><span data-stu-id="a3377-228">The Siren codec is used in Lync Server in the following situations:</span></span>

  - <span data-ttu-id="a3377-229">带宽策略设置太低而无法使用 G.722 时。</span><span class="sxs-lookup"><span data-stu-id="a3377-229">If the bandwidth policy is set too low for G.722 to be used.</span></span>

  - <span data-ttu-id="a3377-230">如果通信服务器2007或通信服务器 2007 R2 客户端连接到 Lync Server 会议服务 (，因为这些客户端不支持722编解码器) 。</span><span class="sxs-lookup"><span data-stu-id="a3377-230">If a Communications Server 2007 or Communications Server 2007 R2 client connects to a Lync Server conferencing service (because those clients do not support the G.722 codec).</span></span>

### <a name="bandwidth-utilization-by-scenario"></a><span data-ttu-id="a3377-231">不同方案的带宽用量要求</span><span class="sxs-lookup"><span data-stu-id="a3377-231">Bandwidth utilization by scenario</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3377-232">方案</span><span class="sxs-lookup"><span data-stu-id="a3377-232">Scenario</span></span></th>
<th><span data-ttu-id="a3377-233">针对量优化的带宽要求 (kbps)</span><span class="sxs-lookup"><span data-stu-id="a3377-233">Bandwidth requirement optimized for quantity (kbps)</span></span></th>
<th><span data-ttu-id="a3377-234">平衡模式下的带宽要求 (kbps)</span><span class="sxs-lookup"><span data-stu-id="a3377-234">Bandwidth requirement for Balanced mode (kbps)</span></span></th>
<th><span data-ttu-id="a3377-235">针对质优化的带宽要求 (kbps)</span><span class="sxs-lookup"><span data-stu-id="a3377-235">Bandwidth requirement optimized for quality (kbps)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3377-236">对等音频呼叫</span><span class="sxs-lookup"><span data-stu-id="a3377-236">Peer-to-peer audio calls</span></span></p></td>
<td><p><span data-ttu-id="a3377-237">45 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-237">45 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-238">62 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-238">62 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-239">91 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-239">91 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3377-240">电话会议</span><span class="sxs-lookup"><span data-stu-id="a3377-240">Conference calls</span></span></p></td>
<td><p><span data-ttu-id="a3377-241">53 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-241">53 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-242">101 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-242">101 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-243">165 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-243">165 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3377-244">PSTN 呼叫在 Lync 2013 和 PSTN 网关之间 (，使用媒体旁路) </span><span class="sxs-lookup"><span data-stu-id="a3377-244">PSTN calls (between Lync 2013 and PSTN gateway, with media bypass)</span></span></p></td>
<td><p><span data-ttu-id="a3377-245">97 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-245">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-246">97 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-246">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-247">161 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-247">161 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3377-248">PSTN 呼叫 (Lync 2013 和中介服务器之间，没有媒体旁路) </span><span class="sxs-lookup"><span data-stu-id="a3377-248">PSTN calls (between Lync 2013 and Mediation Server, without media bypass)</span></span></p></td>
<td><p><span data-ttu-id="a3377-249">45 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-249">45 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-250">97 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-250">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-251">161 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-251">161 kbps</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3377-252">PSTN 呼叫在中介服务器和 PSTN 网关之间 (，没有媒体旁路) </span><span class="sxs-lookup"><span data-stu-id="a3377-252">PSTN calls (between Mediation Server and PSTN gateway, without media bypass)</span></span></p></td>
<td><p><span data-ttu-id="a3377-253">97 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-253">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-254">97 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-254">97 kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-255">161 kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-255">161 kbps</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3377-256">Lync-Polycom 呼叫</span><span class="sxs-lookup"><span data-stu-id="a3377-256">Lync - Polycom calls</span></span></p></td>
<td><p><span data-ttu-id="a3377-257">101 Kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-257">101 Kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-258">101 Kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-258">101 Kbps</span></span></p></td>
<td><p><span data-ttu-id="a3377-259">101 Kbps</span><span class="sxs-lookup"><span data-stu-id="a3377-259">101 Kbps</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="identify-ip-subnets"></a><span data-ttu-id="a3377-260">标识 IP 子网</span><span class="sxs-lookup"><span data-stu-id="a3377-260">Identify IP Subnets</span></span>

<span data-ttu-id="a3377-p118">对于每个网络站点，您将需要和网络管理员一起确定分配给每个网络站点的 IP 子网。如果网络管理员已经将 IP 子网组织到网络区域和网络站点中，则您的工作将大为简化。</span><span class="sxs-lookup"><span data-stu-id="a3377-p118">For each network site, you will need to work with your network administrator to determine what IP subnets are assigned to each network site. If your network administrator has already organized the IP subnets into network regions and network sites, then your work is significantly simplified.</span></span>

<span data-ttu-id="a3377-p119">在我们的示例中，为北美区域中的纽约站点分配了以下 IP 子网：172.29.80.0/23、157.57.216.0/25、172.29.91.0/23、172.29.81.0/24。假设通常在底特律工作的 Bob 到纽约办事处出差进行培训。当他打开计算机并连接到网络时，他的计算机将获取为纽约预留的四个范围之一中的 IP 地址，例如 172.29.80.103。</span><span class="sxs-lookup"><span data-stu-id="a3377-p119">In our example, the New York site in the North America region is assigned the following IP subnets: 172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24. Suppose Bob, who typically works in Detroit, travels to the New York office for training. When he turns on his computer and connects to the network, his computer will get an IP address in one of the four ranges reserved for New York, for example 172.29.80.103.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="a3377-266">在服务器上的网络配置期间指定的 IP 子网必须与客户端计算机提供的格式匹配，才能正确用于媒体绕过。</span><span class="sxs-lookup"><span data-stu-id="a3377-266">The IP subnets specified during network configuration on the server must match the format provided by client computers in order to be properly used for media bypass.</span></span> <span data-ttu-id="a3377-267">Lync 客户端使用其本地 IP 地址并使用关联的子网掩码屏蔽 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="a3377-267">A Lync client takes its local IP address and masks the IP address with the associated subnet mask.</span></span> <span data-ttu-id="a3377-268">确定与每个客户端关联的绕过 ID 时，注册机构会将与每个网络站点相关联的 IP 子网的列表与客户端提供的子网进行比较，以精确匹配。</span><span class="sxs-lookup"><span data-stu-id="a3377-268">When determining the bypass ID associated with each client, the Registrar will compare the list of IP subnets associated with each network site against the subnet provided by the client for an exact match.</span></span> <span data-ttu-id="a3377-269">出于此原因，在服务器上的网络配置期间输入的子网必须是实际的子网，而不是虚拟子网。</span><span class="sxs-lookup"><span data-stu-id="a3377-269">For this reason, it is important that subnets entered during network configuration on the server are actual subnets instead of virtual subnets.</span></span> <span data-ttu-id="a3377-270"> (如果您部署了 "呼叫许可控制"，但没有媒体旁路，则即使配置了虚拟子网，呼叫许可控制也会正常运行。 ) </span><span class="sxs-lookup"><span data-stu-id="a3377-270">(If you deploy call admission control, but not media bypass, call admission control will function properly even if you configure virtual subnets.)</span></span><BR><span data-ttu-id="a3377-271">例如，如果客户在具有 ip 地址为255.255.255.0 的 ip 地址为172.29.81.57 的计算机上登录，Lync 2013 将请求与子网172.29.81.0 关联的绕过 ID。</span><span class="sxs-lookup"><span data-stu-id="a3377-271">For example, if a client signs in on a computer with an IP address of 172.29.81.57 with an IP subnet mask of 255.255.255.0, Lync 2013 will request the bypass ID associated with subnet 172.29.81.0.</span></span> <span data-ttu-id="a3377-272">如果子网定义为 172.29.0.0/16，那么即使客户端属于虚拟子网，注册器也不会将此看做匹配，因为注册器会专门查找子网 172.29.81.0。</span><span class="sxs-lookup"><span data-stu-id="a3377-272">If the subnet is defined as 172.29.0.0/16, although the client belongs to the virtual subnet, the Registrar will not consider this a match because the Registrar is specifically looking for subnet 172.29.81.0.</span></span> <span data-ttu-id="a3377-273">因此，管理员必须严格按照 Lync 客户端提供的方式输入子网， (通过静态或通过 DHCP 在网络配置期间预配子网。 ) </span><span class="sxs-lookup"><span data-stu-id="a3377-273">Therefore, it is important that the administrator enters subnets exactly as provided by Lync clients (which are provisioned with subnets during network configuration either statically or by DHCP.)</span></span>



<span data-ttu-id="a3377-274"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3377-274"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

