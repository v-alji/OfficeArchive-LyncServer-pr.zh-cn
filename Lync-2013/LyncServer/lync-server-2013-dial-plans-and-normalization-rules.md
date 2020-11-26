---
title: Lync Server 2013：拨号计划和规范化规则
description: Lync Server 2013：拨号计划和规范化规则。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial plans and normalization rules
ms:assetid: fde45195-6eb4-403c-9094-57df7fc0bd2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413082(v=OCS.15)
ms:contentKeyID: 48185960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0341d0c5267a2272ff45bd93408b2bd14f0ceeaa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429208"
---
# <a name="dial-plans-and-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="db89e-103">Lync Server 2013 中的拨号计划和规范化规则</span><span class="sxs-lookup"><span data-stu-id="db89e-103">Dial plans and normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db89e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db89e-104">

<span> </span></span></span>

<span data-ttu-id="db89e-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="db89e-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="db89e-106">拨号计划是一组指定的规范化规则，可将指定位置、单个用户或联系人对象的电话号码转换为统一标准 (E.164) 格式，以进行电话授权和呼叫路由。</span><span class="sxs-lookup"><span data-stu-id="db89e-106">A dial plan is a named set of normalization rules that translates phone numbers for a named location, individual user, or contact object into a single standard (E.164) format for purposes of phone authorization and call routing.</span></span>

<span data-ttu-id="db89e-p101">规范化规则定义如何针对每个指定的位置、用户或联系人对象来路由以不同格式表示的电话号码。同一拨号串的解析和转换可能不同，具体取决于拨打该号码的位置，以及发出呼叫的人员或联系人对象。</span><span class="sxs-lookup"><span data-stu-id="db89e-p101">Normalization rules define how phone numbers expressed in various formats are to be routed for each specified location, user, or contact object. The same dial string may be interpreted and translated differently, depending on the location from which it is dialed and the person or contact object making the call.</span></span>

<div>

## <a name="dial-plan-scope"></a><span data-ttu-id="db89e-109">拨号计划作用域</span><span class="sxs-lookup"><span data-stu-id="db89e-109">Dial Plan Scope</span></span>

<span data-ttu-id="db89e-110">拨号计划的 *范围* 决定了拨号计划的应用层级。</span><span class="sxs-lookup"><span data-stu-id="db89e-110">A dial plan’s *scope* determines the hierarchical level at which the dial plan can be applied.</span></span> <span data-ttu-id="db89e-111">在 Lync Server 中，可以为用户分配特定的每个用户的拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-111">In Lync Server, a user can be assigned a specific per-user dial plan.</span></span> <span data-ttu-id="db89e-112">如果未分配用户拨号计划，则应用注册机构池拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-112">If a user dial plan is not assigned, the Registrar pool dial plan is applied.</span></span> <span data-ttu-id="db89e-113">如果没有注册机构池拨号计划，则应用网站拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-113">If there is no Registrar pool dial plan, the site dial plan is applied.</span></span> <span data-ttu-id="db89e-114">最后，如果没有其他适用于该用户的拨号计划，则会应用全局拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-114">Finally, if there is no other dial plan applicable to the user, the global dial plan is applied.</span></span>

<span data-ttu-id="db89e-115">客户通过在用户登录到 Lync Server 时提供的带内配置设置来获取拨号计划范围级别。</span><span class="sxs-lookup"><span data-stu-id="db89e-115">Clients obtain dial plan scope levels through in-band provisioning settings that are provided when users log on to Lync Server.</span></span> <span data-ttu-id="db89e-116">作为管理员，你可以使用 Lync Server 控制面板管理和分配拨号计划范围级别。</span><span class="sxs-lookup"><span data-stu-id="db89e-116">As the administrator, you can manage and assign dial plan scope levels by using Lync Server Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="db89e-117">服务级别公用电话交换网 (PSTN) 网关拨号计划应用于来自特定网关的传入呼叫。</span><span class="sxs-lookup"><span data-stu-id="db89e-117">The service level public switched telephone network (PSTN) gateway dial plan is applied to the incoming calls from a particular gateway.</span></span>



</div>

<span data-ttu-id="db89e-118">拨号计划作用域级别定义如下：</span><span class="sxs-lookup"><span data-stu-id="db89e-118">Dial plan scope levels are defined as follows:</span></span>

  - <span data-ttu-id="db89e-119">**用户拨号计划：** 可以分配给单个用户、组或联系人对象。</span><span class="sxs-lookup"><span data-stu-id="db89e-119">**User dial plan:** Can be assigned to individual users, groups, or contact objects.</span></span> <span data-ttu-id="db89e-120">当接收到其为用户默认的电话上下文设置的呼叫时，语音应用程序可查找每用户拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-120">Voice applications can look up a per-user dial plan when a call is received with the phone-context set to user-default.</span></span> <span data-ttu-id="db89e-121">为便于分配拨号计划，将联系人对象视为单个用户。</span><span class="sxs-lookup"><span data-stu-id="db89e-121">For the purpose of assigning a dial plan, a contact object is treated as an individual user.</span></span>

  - <span data-ttu-id="db89e-122">**池拨号计划：** 可在拓扑中的任何 PSTN 网关或注册机构的服务级别创建。</span><span class="sxs-lookup"><span data-stu-id="db89e-122">**Pool dial plan:** Can be created at the service level for any PSTN gateway or Registrar in your topology.</span></span> <span data-ttu-id="db89e-123">要定义池拨号计划，必须指定要应用拨号计划的特定服务（PSTN 网关或注册器池）。</span><span class="sxs-lookup"><span data-stu-id="db89e-123">To define a pool dial plan, you must specify the particular service (PSTN gateway or Registrar pool) to which the dial plan applies.</span></span>

  - <span data-ttu-id="db89e-124">**网站拨号计划：** 可为整个网站创建，除了分配有池拨号计划或用户拨号计划的任何用户、组或联系人对象之外。</span><span class="sxs-lookup"><span data-stu-id="db89e-124">**Site dial plan:** Can be created for an entire site, except for any users, groups, or contact objects that are assigned a pool dial plan or user dial plan.</span></span> <span data-ttu-id="db89e-125">要定义站点拨号计划，必须指定要应用拨号计划的站点。</span><span class="sxs-lookup"><span data-stu-id="db89e-125">To define a site dial plan, you must specify the site to which the dial plan applies.</span></span>

  - <span data-ttu-id="db89e-126">**全局拨号计划：** 随产品一起安装的默认拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-126">**Global dial plan:** The default dial plan installed with the product.</span></span> <span data-ttu-id="db89e-127">可以编辑全局拨号计划，但无法将其删除。</span><span class="sxs-lookup"><span data-stu-id="db89e-127">You can edit the global dial plan, but you cannot delete it.</span></span> <span data-ttu-id="db89e-128">此拨号计划适用于部署中的所有企业语音用户、组和联系人对象，除非你使用更具体的作用域配置和分配拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-128">This dial plan applies to all Enterprise Voice users, groups, and contact objects in your deployment, unless you configure and assign a dial plan with a more specific scope.</span></span>

</div>

<div>

## <a name="planning-for-dial-plans"></a><span data-ttu-id="db89e-129">规划拨号计划</span><span class="sxs-lookup"><span data-stu-id="db89e-129">Planning for Dial Plans</span></span>

<span data-ttu-id="db89e-130">要规划拨号计划，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="db89e-130">To plan a dial plan, follow these steps:</span></span>

  - <span data-ttu-id="db89e-131">列出贵组织拥有办事处的全部区域设置。</span><span class="sxs-lookup"><span data-stu-id="db89e-131">List all the locales in which your organization has an office.</span></span>
    
    <span data-ttu-id="db89e-p108">该列表必须是最新且完整的。随着公司的发展，将需要对该列表进行修订。在拥有许多小型分支机构的大型跨国公司中，这可能会是一个非常耗时的任务。</span><span class="sxs-lookup"><span data-stu-id="db89e-p108">The list must be up-to-date and complete. It will need to be revised as company organization evolves. In a large, multinational company with numerous small branch offices, this can be a time-consuming task.</span></span>

  - <span data-ttu-id="db89e-135">标识每个站点的有效号码模式。</span><span class="sxs-lookup"><span data-stu-id="db89e-135">Identify valid number patterns for each site.</span></span>
    
    <span data-ttu-id="db89e-p109">在规划拨号计划时，最耗时的任务就是确定每个站点的有效号码模式。在某些情况下，尤其是当相应站点位于同一个国家/地区甚至同一个大陆上时，可以将为一个拨号计划编写的规范化规则复制到其他拨号计划中。在另一些情况下，只需对一个拨号计划中的号码进行微小的更改即可将这些号码用于其他拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-p109">The most time-consuming part of planning your dial plans is identifying the valid number patterns for each site. In some cases, you may be able to copy normalization rules that you have written for one dial plan to other dial plans, especially if the corresponding sites are within the same country/region or even continent. In other cases, small changes to numbers in one dial plan may be enough to use them in other dial plans.</span></span>

  - <span data-ttu-id="db89e-139">制定组织级别的方案来命名拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-139">Develop an organization-wide scheme for naming dial plans.</span></span>
    
    <span data-ttu-id="db89e-140">实行标准命名方案可确保组织内的一致性，并使维护和更新更加容易。</span><span class="sxs-lookup"><span data-stu-id="db89e-140">Adopting a standard naming scheme assures consistency across an organization and makes maintenance and updates easier.</span></span>

  - <span data-ttu-id="db89e-141">确定单个位置是否需要多个拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-141">Decide whether multiple dial plans are required for a single location.</span></span>
    
    <span data-ttu-id="db89e-142">如果你的组织在多个位置维护单个拨号计划，你可能仍然需要为企业语音用户创建单独的拨号计划，这些用户是从专用分支 exchange 迁移 (PBX) 并且需要保留其现有扩展名的用户。</span><span class="sxs-lookup"><span data-stu-id="db89e-142">If your organization maintains a single dial plan across multiple locations, you may still need to create a separate dial plan for Enterprise Voice users who are migrating from a private branch exchange (PBX) and who need to have their existing extensions retained.</span></span>

  - <span data-ttu-id="db89e-143">确定是否需要每用户拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-143">Decide whether per-user dial plans are required.</span></span> <span data-ttu-id="db89e-144">例如，如果分支站点上有用户已向中心网站注册，或者如果你拥有在 Survivable 分支设备上注册的用户，则可以考虑使用每个用户的拨号计划和规范化规则对此类用户进行特殊的拨号方案。</span><span class="sxs-lookup"><span data-stu-id="db89e-144">For example, if you have users at a branch site who are registered with the central site or if you have users who are registered on a Survivable Branch Appliance, you can consider special dialing scenarios for such users using per-user dial plans and normalization rules.</span></span> <span data-ttu-id="db89e-145">有关详细信息，请参阅 [Lync Server 2013 的分支站点恢复要求](lync-server-2013-branch-site-resiliency-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db89e-145">For details, see [Branch-site resiliency requirements for Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md).</span></span>

  - <span data-ttu-id="db89e-146">确定拨号计划作用域（如本主题上文所述）。</span><span class="sxs-lookup"><span data-stu-id="db89e-146">Determine dial plan scope (as previously described in this topic).</span></span>

<span data-ttu-id="db89e-147">若要创建拨号计划，请根据需要在以下字段中指定值，方法是使用 Lync Server 控制面板或 Lync Server 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="db89e-147">To create a dial plan, you specify values in the following fields, as required, by using Lync Server Control Panel or Lync Server Management Shell.</span></span>

<div>

## <a name="name-and-simple-name"></a><span data-ttu-id="db89e-148">名称和简单名称</span><span class="sxs-lookup"><span data-stu-id="db89e-148">Name and Simple Name</span></span>

<span data-ttu-id="db89e-149">对于用户拨号计划，应指定描述性名称，以标识要为其分配拨号计划的用户、组或联系人对象。</span><span class="sxs-lookup"><span data-stu-id="db89e-149">For user dial plans, you should specify a descriptive name that identifies the users, groups, or contact objects to which the dial plan will be assigned.</span></span> <span data-ttu-id="db89e-150">对于网站拨号计划，"名称" 字段已预填充网站名称，不能更改。</span><span class="sxs-lookup"><span data-stu-id="db89e-150">For site dial plans, the Name field is prepopulated with the site name and cannot be changed.</span></span> <span data-ttu-id="db89e-151">对于池拨号计划，"名称" 字段预填充了 PSTN 网关或前端池 (FQDN) 的完全限定的域名，并且不能更改。</span><span class="sxs-lookup"><span data-stu-id="db89e-151">For pool dial plans, the Name field is prepopulated with the PSTN gateway or Front End pool fully qualified domain name (FQDN) and cannot be changed.</span></span>

<span data-ttu-id="db89e-152">使用从拨号计划名称派生的字符串预填充拨号计划的 *简单名称* 。</span><span class="sxs-lookup"><span data-stu-id="db89e-152">The dial plan *Simple Name* is prepopulated with a string that is derived from the dial plan name.</span></span> <span data-ttu-id="db89e-153">“简单名称”字段是可编辑的，从而使您可以为拨号计划创建更具描述性的命名约定。</span><span class="sxs-lookup"><span data-stu-id="db89e-153">The Simple Name field is editable, which enables you to create a more descriptive naming convention for your dial plans.</span></span> <span data-ttu-id="db89e-154">“*简单名称*”值不能为空，且必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="db89e-154">The *Simple Name* value cannot be empty and must be unique.</span></span> <span data-ttu-id="db89e-155">最佳实践是为整个组织制定一个命名约定，然后在所有站点和用户中统一使用此约定。</span><span class="sxs-lookup"><span data-stu-id="db89e-155">A best practice is to develop a naming convention for your entire organization and then use this convention consistently across all sites and users.</span></span>

</div>

<div>

## <a name="description"></a><span data-ttu-id="db89e-156">描述</span><span class="sxs-lookup"><span data-stu-id="db89e-156">Description</span></span>

<span data-ttu-id="db89e-p113">建议您键入一个要应用相应的拨号计划的通用可辨识地理位置名称。例如，如果拨号计划的名称是 London.Contoso.com，则建议的说明将为 London。</span><span class="sxs-lookup"><span data-stu-id="db89e-p113">We recommend that you type the common, recognizable name of the geographic location to which the corresponding dial plan applies. For example, if the dial plan name is London.Contoso.com, the recommended description would be London.</span></span>

</div>

<div>

## <a name="dial-in-conferencing-region"></a><span data-ttu-id="db89e-159">电话拨入式会议区域</span><span class="sxs-lookup"><span data-stu-id="db89e-159">Dial-in Conferencing Region</span></span>

<span data-ttu-id="db89e-160">如果要部署电话拨入式会议，则需要指定电话拨入式会议区域，以将电话拨入式会议访问号码与拨号计划关联起来。</span><span class="sxs-lookup"><span data-stu-id="db89e-160">If you are deploying dial-in conferencing, you will need to specify a dial-in conferencing region to associate dial-in conferencing access numbers with a dial plan.</span></span>

</div>

<div>

## <a name="external-access-prefix"></a><span data-ttu-id="db89e-161">外部访问前缀</span><span class="sxs-lookup"><span data-stu-id="db89e-161">External Access Prefix</span></span>

<span data-ttu-id="db89e-162">可以指定最多四个字符的外部访问前缀 (\# \* 和 0-9) 如果用户需要拨打一个或多个附加前导数字 (例如，9) 以获取外部线路。</span><span class="sxs-lookup"><span data-stu-id="db89e-162">You can specify an external access prefix of up to four characters (\#, \*, and 0-9) if users need to dial one or more additional leading digits (for example, 9) to get an external line.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="db89e-163">如果指定了外部访问前缀，则不需要另外创建规范化规则来满足前缀。</span><span class="sxs-lookup"><span data-stu-id="db89e-163">If you specify an external access prefix, you do not need to create an additional normalization rule to accommodate the prefix.</span></span>



</div>

</div>

</div>

<div>

## <a name="normalization-rules"></a><span data-ttu-id="db89e-164">规范化规则</span><span class="sxs-lookup"><span data-stu-id="db89e-164">Normalization Rules</span></span>

<span data-ttu-id="db89e-p114">规范化规则定义如何针对命名的位置来路由以不同格式表示的电话号码。同一号码字符串的解析和转换方式可能不同，具体取决于拨打该号码的场所。规范化规则是呼叫路由所必需的，因为用户在其联系人列表中输入电话号码时，可以而且确实会使用各种格式。</span><span class="sxs-lookup"><span data-stu-id="db89e-p114">Normalization rules define how phone numbers expressed in various formats are to be routed for the named location. The same number string may be interpreted and translated differently, depending on the locale from which it is dialed. Normalization rules are necessary for call routing because users can, and do, use various formats when entering phone numbers in their Contacts lists.</span></span>

<span data-ttu-id="db89e-168">对用户提供的电话号码进行规范化可以提供一致的格式，从而便于执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="db89e-168">Normalizing user-supplied phone numbers provides a consistent format that facilitates the following tasks:</span></span>

  - <span data-ttu-id="db89e-169">将所拨打的号码与预期收件人的 SIP-URI 相匹配。</span><span class="sxs-lookup"><span data-stu-id="db89e-169">Match a dialed number to the intended recipient’s SIP-URI.</span></span>

  - <span data-ttu-id="db89e-170">对呼叫者应用拨号授权规则。</span><span class="sxs-lookup"><span data-stu-id="db89e-170">Apply dialing authorization rules to the calling party.</span></span>

<span data-ttu-id="db89e-171">规范化规则可能需要考虑下列号码字段：</span><span class="sxs-lookup"><span data-stu-id="db89e-171">The following number fields are among those that your normalization rules may need to account for:</span></span>

  - <span data-ttu-id="db89e-172">拨号计划</span><span class="sxs-lookup"><span data-stu-id="db89e-172">Dial plan</span></span>

  - <span data-ttu-id="db89e-173">国家/地区代码</span><span class="sxs-lookup"><span data-stu-id="db89e-173">Country code</span></span>

  - <span data-ttu-id="db89e-174">区号</span><span class="sxs-lookup"><span data-stu-id="db89e-174">Area code</span></span>

  - <span data-ttu-id="db89e-175">分机号长度</span><span class="sxs-lookup"><span data-stu-id="db89e-175">Length of extension</span></span>

  - <span data-ttu-id="db89e-176">站点前缀</span><span class="sxs-lookup"><span data-stu-id="db89e-176">Site prefix</span></span>

<div>

## <a name="creating-normalization-rules"></a><span data-ttu-id="db89e-177">创建规范化规则</span><span class="sxs-lookup"><span data-stu-id="db89e-177">Creating Normalization Rules</span></span>

<span data-ttu-id="db89e-178">规范化规则使用 .NET Framework 正则表达式指定数字匹配模式，服务器使用该模式将拨号串转换为 E.164 格式，以便执行反向号码查找。</span><span class="sxs-lookup"><span data-stu-id="db89e-178">Normalization rules use .NET Framework regular expressions to specify numeric match patterns that the server uses to translate dial strings to E.164 format for the purpose of performing reverse number lookup.</span></span> <span data-ttu-id="db89e-179">在 Lync Server 控制面板中创建规范化规则，方法是手动输入表达式，或者输入要匹配的拨号字符串的起始位位和长度，并让 Lync Server 控制面板为你生成相应的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="db89e-179">You create normalization rules in the Lync Server Control Panel either by entering the expressions manually, or by entering the starting digits and the length of the dial strings to be matched and letting the Lync Server Control Panel generate the corresponding regular expression for you.</span></span> <span data-ttu-id="db89e-180">无论采用何种方式，完成操作后，都可以输入一个测试号码来验证规范化规则能否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="db89e-180">Either way, when you finish, you can enter a test number to verify that the normalization rule works as expected.</span></span>

<span data-ttu-id="db89e-181">有关使用 .NET Framework 正则表达式的详细信息，请参阅的 ".NET Framework 正则表达式" [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) 。</span><span class="sxs-lookup"><span data-stu-id="db89e-181">For details about using .NET Framework regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

</div>

<span id="BKMK_SampleNormalizationRules"></span>

<div>

## <a name="sample-normalization-rules"></a><span data-ttu-id="db89e-182">规范化规则示例</span><span class="sxs-lookup"><span data-stu-id="db89e-182">Sample Normalization Rules</span></span>

<span data-ttu-id="db89e-p116">下表显示以 .NET Framework 正则表达式编写的规范化规则示例。这些仅为示例，不应作为创建自己的规范化规则时的规定性参考。</span><span class="sxs-lookup"><span data-stu-id="db89e-p116">The following table shows sample normalization rules that are written as .NET Framework regular expressions. The samples are examples only and are not meant to be a prescriptive reference for creating your own normalization rules.</span></span>

### <a name="table-1normalization-rules-using-net-framework-regular-expressions"></a><span data-ttu-id="db89e-185">表 1. 使用 .NET Framework 正则表达式的规范化规则</span><span class="sxs-lookup"><span data-stu-id="db89e-185">Table 1.Normalization Rules Using .NET Framework Regular Expressions</span></span>

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
<th><span data-ttu-id="db89e-186">规则名称</span><span class="sxs-lookup"><span data-stu-id="db89e-186">Rule name</span></span></th>
<th><span data-ttu-id="db89e-187">描述</span><span class="sxs-lookup"><span data-stu-id="db89e-187">Description</span></span></th>
<th><span data-ttu-id="db89e-188">号码模式</span><span class="sxs-lookup"><span data-stu-id="db89e-188">Number pattern</span></span></th>
<th><span data-ttu-id="db89e-189">转换</span><span class="sxs-lookup"><span data-stu-id="db89e-189">Translation</span></span></th>
<th><span data-ttu-id="db89e-190">示例</span><span class="sxs-lookup"><span data-stu-id="db89e-190">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db89e-191">4digitExtension</span><span class="sxs-lookup"><span data-stu-id="db89e-191">4digitExtension</span></span></p></td>
<td><p><span data-ttu-id="db89e-192">转换 4 位分机号</span><span class="sxs-lookup"><span data-stu-id="db89e-192">Translates 4-digit extensions</span></span></p></td>
<td><p><span data-ttu-id="db89e-193">^ ( \d {4}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-193">^(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-194">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="db89e-194">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-195">将 0100 转换为 +14255550100</span><span class="sxs-lookup"><span data-stu-id="db89e-195">0100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-196">5digitExtension</span><span class="sxs-lookup"><span data-stu-id="db89e-196">5digitExtension</span></span></p></td>
<td><p><span data-ttu-id="db89e-197">转换 5 位分机号</span><span class="sxs-lookup"><span data-stu-id="db89e-197">Translates 5-digit extensions</span></span></p></td>
<td><p><span data-ttu-id="db89e-198">^ 5 ( \d {4}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-198">^5(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-199">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="db89e-199">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-200">将 50100 转换为 +14255550100</span><span class="sxs-lookup"><span data-stu-id="db89e-200">50100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-201">7digitcallingRedmond</span><span class="sxs-lookup"><span data-stu-id="db89e-201">7digitcallingRedmond</span></span></p></td>
<td><p><span data-ttu-id="db89e-202">将 7 位号码转换为雷德蒙德本地号码</span><span class="sxs-lookup"><span data-stu-id="db89e-202">Translates 7-digit numbers to Redmond local numbers</span></span></p></td>
<td><p><span data-ttu-id="db89e-203">^ ( \d {7}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-203">^(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-204">+1425$1</span><span class="sxs-lookup"><span data-stu-id="db89e-204">+1425$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-205">将 5550100 转换为 +14255550100</span><span class="sxs-lookup"><span data-stu-id="db89e-205">5550100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-206">7digitcallingDallas</span><span class="sxs-lookup"><span data-stu-id="db89e-206">7digitcallingDallas</span></span></p></td>
<td><p><span data-ttu-id="db89e-207">将 7 位号码转换为达拉斯本地号码</span><span class="sxs-lookup"><span data-stu-id="db89e-207">Translates 7-digit numbers to Dallas local numbers</span></span></p></td>
<td><p><span data-ttu-id="db89e-208">^ ( \d {7}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-208">^(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-209">+1972$1</span><span class="sxs-lookup"><span data-stu-id="db89e-209">+1972$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-210">将 5550100 转换为 +19725550100</span><span class="sxs-lookup"><span data-stu-id="db89e-210">5550100 is translated to +19725550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-211">10digitcallingUS</span><span class="sxs-lookup"><span data-stu-id="db89e-211">10digitcallingUS</span></span></p></td>
<td><p><span data-ttu-id="db89e-212">转换美国的 10 位号码</span><span class="sxs-lookup"><span data-stu-id="db89e-212">Translates 10-digit numbers in the United States</span></span></p></td>
<td><p><span data-ttu-id="db89e-213">^ ( \d {10}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-213">^(\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-214">+1$1</span><span class="sxs-lookup"><span data-stu-id="db89e-214">+1$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-215">将 2065550100 转换为 +12065550100</span><span class="sxs-lookup"><span data-stu-id="db89e-215">2065550100 is translated to +12065550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-216">LDCallingUS</span><span class="sxs-lookup"><span data-stu-id="db89e-216">LDCallingUS</span></span></p></td>
<td><p><span data-ttu-id="db89e-217">用美国的长途前缀转换号码</span><span class="sxs-lookup"><span data-stu-id="db89e-217">Translates numbers with long distance prefixes in the United States</span></span></p></td>
<td><p><span data-ttu-id="db89e-218">^ 1 ( \d {10}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-218">^1(\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-219">+$1</span><span class="sxs-lookup"><span data-stu-id="db89e-219">+$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-220">将 12145550100 转换为 +2145550100</span><span class="sxs-lookup"><span data-stu-id="db89e-220">12145550100 is translated to +2145550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-221">IntlCallingUS</span><span class="sxs-lookup"><span data-stu-id="db89e-221">IntlCallingUS</span></span></p></td>
<td><p><span data-ttu-id="db89e-222">用美国的国际前缀转换号码</span><span class="sxs-lookup"><span data-stu-id="db89e-222">Translates numbers with international prefixes in the United States</span></span></p></td>
<td><p><span data-ttu-id="db89e-223">^011(\d\*)$</span><span class="sxs-lookup"><span data-stu-id="db89e-223">^011(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="db89e-224">+$1</span><span class="sxs-lookup"><span data-stu-id="db89e-224">+$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-225">将 01191445550100 转换为 +91445550100</span><span class="sxs-lookup"><span data-stu-id="db89e-225">01191445550100 is translated to +91445550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-226">RedmondOperator</span><span class="sxs-lookup"><span data-stu-id="db89e-226">RedmondOperator</span></span></p></td>
<td><p><span data-ttu-id="db89e-227">将 0 转换为雷德蒙德号码</span><span class="sxs-lookup"><span data-stu-id="db89e-227">Translates 0 to Redmond Operator</span></span></p></td>
<td><p><span data-ttu-id="db89e-228">^0$</span><span class="sxs-lookup"><span data-stu-id="db89e-228">^0$</span></span></p></td>
<td><p><span data-ttu-id="db89e-229">+14255550100</span><span class="sxs-lookup"><span data-stu-id="db89e-229">+14255550100</span></span></p></td>
<td><p><span data-ttu-id="db89e-230">将 0 转换为 +14255550100</span><span class="sxs-lookup"><span data-stu-id="db89e-230">0 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-231">RedmondSitePrefix</span><span class="sxs-lookup"><span data-stu-id="db89e-231">RedmondSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="db89e-232">用网内前缀 (6) 和雷德蒙德站点代码 (222) 转换号码</span><span class="sxs-lookup"><span data-stu-id="db89e-232">Translates numbers with on-net prefix (6) and Redmond site code (222)</span></span></p></td>
<td><p><span data-ttu-id="db89e-233">^ 6222 ( \d {4}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-233">^6222(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-234">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="db89e-234">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-235">将 62220100 转换为 +14255550100</span><span class="sxs-lookup"><span data-stu-id="db89e-235">62220100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-236">NYSitePrefix</span><span class="sxs-lookup"><span data-stu-id="db89e-236">NYSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="db89e-237">用网内前缀 (6) 和纽约站点代码 (333) 转换号码</span><span class="sxs-lookup"><span data-stu-id="db89e-237">Translates numbers with on-net prefix (6) and NY site code (333)</span></span></p></td>
<td><p><span data-ttu-id="db89e-238">^ 6333 ( \d {4}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-238">^6333(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-239">+1202555$1</span><span class="sxs-lookup"><span data-stu-id="db89e-239">+1202555$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-240">将 63330100 转换为 +12025550100</span><span class="sxs-lookup"><span data-stu-id="db89e-240">63330100 is translated to +12025550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-241">DallasSitePrefix</span><span class="sxs-lookup"><span data-stu-id="db89e-241">DallasSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="db89e-242">用网内前缀 (6) 和达拉斯站点代码 (444) 转换号码</span><span class="sxs-lookup"><span data-stu-id="db89e-242">Translates numbers with on-net prefix (6) and Dallas site code (444)</span></span></p></td>
<td><p><span data-ttu-id="db89e-243">^ 6444 ( \d {4}) $</span><span class="sxs-lookup"><span data-stu-id="db89e-243">^6444(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="db89e-244">+1972555$1</span><span class="sxs-lookup"><span data-stu-id="db89e-244">+1972555$1</span></span></p></td>
<td><p><span data-ttu-id="db89e-245">将 64440100 转换为 +19725550100</span><span class="sxs-lookup"><span data-stu-id="db89e-245">64440100 is translated to +19725550100</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db89e-246">下表基于上表中显示的规范化规则，说明了美国华盛顿雷德蒙德的示例拨号计划。</span><span class="sxs-lookup"><span data-stu-id="db89e-246">The following table illustrates a sample dial plan for Redmond, Washington, United States, based on the normalization rules shown in the previous table.</span></span>

### <a name="table-2-redmond-dial-plan-based-on-normalization-rules-shown-in-table-1"></a><span data-ttu-id="db89e-p117">表 2. 基于表 1 中所示规范化规则的雷德蒙德拨号计划</span><span class="sxs-lookup"><span data-stu-id="db89e-p117">Table 2. Redmond Dial Plan Based on Normalization Rules Shown in Table 1</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db89e-249">Redmond.forestFQDN</span><span class="sxs-lookup"><span data-stu-id="db89e-249">Redmond.forestFQDN</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db89e-250">5digitExtension</span><span class="sxs-lookup"><span data-stu-id="db89e-250">5digitExtension</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-251">7digitcallingRedmond</span><span class="sxs-lookup"><span data-stu-id="db89e-251">7digitcallingRedmond</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-252">10digitcallingUS</span><span class="sxs-lookup"><span data-stu-id="db89e-252">10digitcallingUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-253">IntlCallingUS</span><span class="sxs-lookup"><span data-stu-id="db89e-253">IntlCallingUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-254">RedmondSitePrefix</span><span class="sxs-lookup"><span data-stu-id="db89e-254">RedmondSitePrefix</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-255">NYSitePrefix</span><span class="sxs-lookup"><span data-stu-id="db89e-255">NYSitePrefix</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db89e-256">DallasSitePrefix</span><span class="sxs-lookup"><span data-stu-id="db89e-256">DallasSitePrefix</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db89e-257">RedmondOperator</span><span class="sxs-lookup"><span data-stu-id="db89e-257">RedmondOperator</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="db89e-p118">[!注释] 上表中所示的规范化规则名称不包含空格，你可以选择是否要包含。例如，该表中的第一个名称，本应写成"5 digit extension"或"5-digit Extension"，但它仍然有效。</span><span class="sxs-lookup"><span data-stu-id="db89e-p118">The normalization rules names shown in the preceding table do not include spaces, but this is a matter of choice. The first name in the table, for example, could have been written "5 digit extension" or "5-digit Extension" and still be valid.</span></span>



<span data-ttu-id="db89e-260"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db89e-260"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

