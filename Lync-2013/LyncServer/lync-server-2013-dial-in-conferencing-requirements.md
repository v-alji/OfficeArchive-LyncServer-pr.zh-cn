---
title: Lync Server 2013 电话拨入式会议要求
description: Lync Server 2013 电话拨入式会议要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing requirements
ms:assetid: 9aff949e-3dac-481a-be46-a180c72e8066
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398802(v=OCS.15)
ms:contentKeyID: 48184969
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0850204993935998c4c098bc7c2866a8a6f3fa1e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429225"
---
# <a name="dial-in-conferencing-requirements-in-lync-server-2013"></a><span data-ttu-id="70cd3-103">Lync Server 2013 中的电话拨入式会议要求</span><span class="sxs-lookup"><span data-stu-id="70cd3-103">Dial-in conferencing requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70cd3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70cd3-104">

<span> </span></span></span>

<span data-ttu-id="70cd3-105">_**主题上次修改时间：** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="70cd3-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="70cd3-106">在开始 Lync Server 2013 部署过程之前，你需要针对以下各项进行规划：</span><span class="sxs-lookup"><span data-stu-id="70cd3-106">Before you start the Lync Server 2013 deployment process you need to plan for the following:</span></span>

  - <span data-ttu-id="70cd3-107">用于连接到公共交换电话网络 (PSTN) 的配置</span><span class="sxs-lookup"><span data-stu-id="70cd3-107">The configuration to use for connecting to the public switched telephone network (PSTN)</span></span>

  - <span data-ttu-id="70cd3-108">将电话拨入式会议区域分配给拨入访问号码的策略</span><span class="sxs-lookup"><span data-stu-id="70cd3-108">Your strategy for assigning dial-in conferencing regions to dial-in access numbers</span></span>

  - <span data-ttu-id="70cd3-109">创建会议目录的策略</span><span class="sxs-lookup"><span data-stu-id="70cd3-109">Your strategy for creating conference directories</span></span>

<div>

## <a name="planning-for-dial-in-pstn-connectivity"></a><span data-ttu-id="70cd3-110">规划电话拨入式 PSTN 连接</span><span class="sxs-lookup"><span data-stu-id="70cd3-110">Planning for Dial-in PSTN Connectivity</span></span>

<span data-ttu-id="70cd3-111">电话拨入式会议至少需要一个中介服务器和至少一个 PSTN 网关。</span><span class="sxs-lookup"><span data-stu-id="70cd3-111">Dial-in conferencing requires at least one Mediation Server and at least one PSTN gateway.</span></span>

<span data-ttu-id="70cd3-112">您可以在中央站点或分支站点部署中介服务器。</span><span class="sxs-lookup"><span data-stu-id="70cd3-112">You can deploy a Mediation Server in a central site or in a branch site.</span></span> <span data-ttu-id="70cd3-113">在中央站点，您可以在前端池或 Standard Edition Server 并置中介服务器，或者将其部署在独立服务器或池中。</span><span class="sxs-lookup"><span data-stu-id="70cd3-113">In a central site, you can collocate a Mediation Server on a Front End pool or Standard Edition server, or you can deploy it on a stand-alone server or pool.</span></span> <span data-ttu-id="70cd3-114">在分支站点，您可以将中介服务器部署在独立服务器中或部署为 Survivable Branch Appliance 的组件。</span><span class="sxs-lookup"><span data-stu-id="70cd3-114">In a branch site, you can deploy a Mediation Server on a stand-alone server or as a component of the Survivable Branch Appliance.</span></span>

<span data-ttu-id="70cd3-p102">您可以在中央站点或分支站点部署 PSTN 网关。在分支站点，PSTN 网关可以是独立的，也可以作为 Survivable Branch Appliance 的组件。</span><span class="sxs-lookup"><span data-stu-id="70cd3-p102">You can deploy a PSTN gateway in a central site or in a branch site. In a branch site, the PSTN gateway can be stand-alone or a component of the Survivable Branch Appliance.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="70cd3-117">电话拨入式会议不使用媒体旁路，因为 A/V 会议服务器不支持媒体绕过。</span><span class="sxs-lookup"><span data-stu-id="70cd3-117">Dial-in conferencing does not use media bypass because A/V Conferencing Server do not support media bypass.</span></span>



</div>

<span data-ttu-id="70cd3-118">有关规划用于拨入式会议的中介服务器和 PSTN 网关配置的详细信息，请参阅规划文档中 Lync server 2013 中的 [中介服务器组件和拓扑](lync-server-2013-components-and-topologies-for-mediation-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="70cd3-118">For details about planning your configuration for Mediation Server and PSTN gateways for dial-in conferencing, see [Components and topologies for Mediation Server in Lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) in the Planning documentation.</span></span>

</div>

<span id="bkmk_PlanningforDialinConferencingRegions"></span>

<div>

## <a name="planning-for-dial-in-conferencing-regions"></a><span data-ttu-id="70cd3-119">规划电话拨入式会议区域</span><span class="sxs-lookup"><span data-stu-id="70cd3-119">Planning for Dial-in Conferencing Regions</span></span>

<span data-ttu-id="70cd3-120">在拨入配置期间，您可以创建拨号计划和电话拨入式会议访问号码。</span><span class="sxs-lookup"><span data-stu-id="70cd3-120">During dial-in configuration, you create dial plans and dial-in conferencing access numbers.</span></span> <span data-ttu-id="70cd3-121">拨号计划是一组规范化规则，用于指定电话号码中的数字和数字模式，并将该电话号码转换为标准的格式为164的呼叫路由格式。</span><span class="sxs-lookup"><span data-stu-id="70cd3-121">Dial plans are sets of normalization rules that specify the number and pattern of digits in a phone number and translate the phone number into the standard E.164 format for call routing.</span></span> <span data-ttu-id="70cd3-122">电话拨入式会议访问号码是参与者为加入会议而呼叫的号码。</span><span class="sxs-lookup"><span data-stu-id="70cd3-122">Dial-in conferencing access numbers are the numbers participants call to join a conference.</span></span>

<span data-ttu-id="70cd3-123">每个电话拨入式会议访问号码必须至少与一个拨号计划关联。</span><span class="sxs-lookup"><span data-stu-id="70cd3-123">Every dial-in conferencing access number must be associated with at least one dial plan.</span></span> <span data-ttu-id="70cd3-124">电话拨入式会议区域将电话拨入式会议接入号码与它的拨号计划相关联。</span><span class="sxs-lookup"><span data-stu-id="70cd3-124">Dial-in conferencing regions associate a dial-in conferencing access number with its dial plans.</span></span> <span data-ttu-id="70cd3-125">设置拨号计划时，指定适用于拨号计划的电话拨入式会议区域。</span><span class="sxs-lookup"><span data-stu-id="70cd3-125">When you set up a dial plan, you specify the dial-in conferencing region that applies to the dial plan.</span></span> <span data-ttu-id="70cd3-126">创建拨入访问号码时，要选择将访问号码与相应的拨号计划相关联的区域。</span><span class="sxs-lookup"><span data-stu-id="70cd3-126">When you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="70cd3-127">创建拨号计划时，请指定拨号计划的范围： "用户范围"、"池范围" 或 "网站范围"。</span><span class="sxs-lookup"><span data-stu-id="70cd3-127">When you create a dial plan, you specify the scope of the dial plan: user scope, pool scope, or site scope.</span></span> <span data-ttu-id="70cd3-128">会按照各用户适用的最小作用域为其分配拨号计划。</span><span class="sxs-lookup"><span data-stu-id="70cd3-128">Every user is assigned the dial plan from the narrowest scope that applies to the user.</span></span> <span data-ttu-id="70cd3-129">例如，如果适用，则为用户分配用户级别的拨号计划。</span><span class="sxs-lookup"><span data-stu-id="70cd3-129">For example, a user is assigned a user-level dial plan, if one applies.</span></span> <span data-ttu-id="70cd3-130">如果用户级别的拨号计划不适用，则为用户分配池级别的拨号计划。</span><span class="sxs-lookup"><span data-stu-id="70cd3-130">If a user-level dial plan does not apply, the user is assigned a pool-level dial plan.</span></span> <span data-ttu-id="70cd3-131">如果池级别的拨号计划不适用，则为用户分配站点级别的拨号计划。</span><span class="sxs-lookup"><span data-stu-id="70cd3-131">If a pool-level dial plan does not apply, the user is assigned a site-level dial plan.</span></span> <span data-ttu-id="70cd3-132">如果站点级别的拨号计划不适用，则为用户分配全局拨号计划。</span><span class="sxs-lookup"><span data-stu-id="70cd3-132">If a site-level dial plan does not apply, the user is assigned the global dial plan.</span></span>

<span data-ttu-id="70cd3-p106">配置拨号计划之前，规划命名和使用区域的方式非常重要。对于电话拨入式会议区域，请注意下列事项：</span><span class="sxs-lookup"><span data-stu-id="70cd3-p106">Before you configure the dial plans, is it important to plan how you want to name and use regions. The following considerations apply to dial-in conferencing regions:</span></span>

  - <span data-ttu-id="70cd3-135">区域通常是与某个办公室或一组办公室相关联的地理区域。</span><span class="sxs-lookup"><span data-stu-id="70cd3-135">A region is typically a geographical area that is associated with an office or group of offices.</span></span>

  - <span data-ttu-id="70cd3-p107">语言与拨入访问号码相关联。如果支持具有多种语言的地理区域，应该决定如何定义区域以便支持多种语言。例如，可以基于地理位置和语言的组合定义多个区域，或者基于地理位置定义一个区域，且每种语言拥有不同的拨入访问号码。</span><span class="sxs-lookup"><span data-stu-id="70cd3-p107">Languages are associated with dial-in access numbers. If you support geographical areas that have multiple languages, you should decide how you want to define regions to support the multiple languages. For example, you might define multiple regions based on a combination of geography and language, or you might define a single region based on geography and have a different dial-in access numbers for each language.</span></span>

  - <span data-ttu-id="70cd3-139">用户安排会议时，默认情况下会议将使用用户的拨号计划所指定的区域。</span><span class="sxs-lookup"><span data-stu-id="70cd3-139">When a user schedules a meeting, by default the meeting uses the region specified by that user's dial plan.</span></span>

  - <span data-ttu-id="70cd3-140">默认情况下，会议邀请中包含该区域的所有拨入访问号码。</span><span class="sxs-lookup"><span data-stu-id="70cd3-140">By default, the all of the dial-in access numbers for the region are included in the meeting invitation.</span></span>

  - <span data-ttu-id="70cd3-141">命名区域非常重要，这样就可以清楚地识别这些区域。</span><span class="sxs-lookup"><span data-stu-id="70cd3-141">It is important to name regions so that they are clearly recognizable.</span></span> <span data-ttu-id="70cd3-142">用户可以使用区域的名称更改会议的区域，以便邀请中包含不同的访问号码。</span><span class="sxs-lookup"><span data-stu-id="70cd3-142">The user can use the names of the regions to change a meeting's region so that different access numbers are included in the invitation.</span></span> <span data-ttu-id="70cd3-143"> (用户使用 Outlook 安排会议时，用户使用 Lync 2013 的联机会议加载项更改区域) 。</span><span class="sxs-lookup"><span data-stu-id="70cd3-143">(When users use Outlook to schedule a meeting, the user uses the Online Meeting Add-in for Lync 2013 to change the region).</span></span>

  - <span data-ttu-id="70cd3-144">应该对区域加以设计，以便想要拨入会议的被邀请者可以在会议邀请中看到本地访问号码。</span><span class="sxs-lookup"><span data-stu-id="70cd3-144">Regions should be designed so that any invitee who wants to dial into a conference can see a local access number in the conference invitation.</span></span>

  - <span data-ttu-id="70cd3-145">你可以配置区域内的访问号码在 "电话拨入式会议设置" 页面上显示的顺序 (，因此，它们在会议邀请) 中的显示顺序是使用 Lync Server Management Shell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70cd3-145">You can configure the order in which access numbers within a region appear on the Dial-in Conferencing Settings page (and, therefore, the order in which they appear in the conference invitation) by using Lync Server Management Shell cmdlets.</span></span>

  - <span data-ttu-id="70cd3-146">任何位置的任何用户均可拨打拨入访问号码来加入会议。</span><span class="sxs-lookup"><span data-stu-id="70cd3-146">Any user from any location can call any dial-in access number to join a conference.</span></span>

</div>

<div>

## <a name="planning-for-conference-directories"></a><span data-ttu-id="70cd3-147">规划会议目录</span><span class="sxs-lookup"><span data-stu-id="70cd3-147">Planning for Conference Directories</span></span>

<span data-ttu-id="70cd3-148">会议目录维护参与者在使用 Lync 2013 时用于加入会议的字母数字会议 ID 之间的映射，以及电话拨入式会议参与者用于加入会议的仅限数字的会议 ID。</span><span class="sxs-lookup"><span data-stu-id="70cd3-148">Conference directories maintain a mapping between the alphanumeric meeting ID that a participant uses to join a conference when using Lync 2013, and the numeric-only conference ID that a dial-in conferencing participant uses to join the conference.</span></span> <span data-ttu-id="70cd3-149">会议 ID 的格式如下：</span><span class="sxs-lookup"><span data-stu-id="70cd3-149">The format of the conference ID is as follows:</span></span>

    <housekeeping digit (1 digit)><conference directory (usually 1-2 digits)><conference number (variable number of digits><check digit (1 digit)>

<span data-ttu-id="70cd3-150">创建多个会议目录将确保会议 ID 将短暂停留，直到创建了大量会议。</span><span class="sxs-lookup"><span data-stu-id="70cd3-150">Creating multiple conference directories will ensure that conference IDs will stay short until a significant amount of conferences have been created.</span></span> <span data-ttu-id="70cd3-151">在每个用户需要参与典型数量会议的组织中，建议您为池中的每 999 个用户创建一个会议目录。</span><span class="sxs-lookup"><span data-stu-id="70cd3-151">In an organization with a typical number of conferences per user, we recommend that you create one conference directory for every 999 users in the pool.</span></span> <span data-ttu-id="70cd3-152">使用此准则时，会议 Id 通常可以保持较小。</span><span class="sxs-lookup"><span data-stu-id="70cd3-152">Using this guideline the conference IDs can generally be kept small.</span></span> <span data-ttu-id="70cd3-153">但是，一旦会议目录的数目（在池中）超过 9，则会议 ID 号将增大以支持其他会议。</span><span class="sxs-lookup"><span data-stu-id="70cd3-153">However, once the number of conference directories (across the pools) exceed 9, the Conference ID number will grow to support additional conferences.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="70cd3-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70cd3-154">See Also</span></span>


[<span data-ttu-id="70cd3-155">Lync Server 2013 中的中介服务器组件</span><span class="sxs-lookup"><span data-stu-id="70cd3-155">Mediation Server component in Lync Server 2013</span></span>](lync-server-2013-mediation-server-component.md)  
[<span data-ttu-id="70cd3-156">Lync Server 2013 中的拨号计划和规范化规则</span><span class="sxs-lookup"><span data-stu-id="70cd3-156">Dial plans and normalization rules in Lync Server 2013</span></span>](lync-server-2013-dial-plans-and-normalization-rules.md)  
  

<span data-ttu-id="70cd3-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70cd3-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

