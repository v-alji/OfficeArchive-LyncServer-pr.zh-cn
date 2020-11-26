---
title: Lync Server 2013：托管语音邮件策略
description: Lync Server 2013：托管语音邮件策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted voice mail policies
ms:assetid: d62a35ed-cbe2-4f06-86b4-e192c18435c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398932(v=OCS.15)
ms:contentKeyID: 48185506
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57461f4ffd2c6f2cd733dd7ec2c945c9e7b801c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427500"
---
# <a name="hosted-voice-mail-policies-in-lync-server-2013"></a><span data-ttu-id="8f88f-103">Lync Server 2013 中的托管语音邮件策略</span><span class="sxs-lookup"><span data-stu-id="8f88f-103">Hosted voice mail policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f88f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f88f-104">

<span> </span></span></span>

<span data-ttu-id="8f88f-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="8f88f-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="8f88f-106">*托管语音邮件策略* 向 Lync Server 2013 ExUM 路由应用程序提供有关邮箱位于托管 Exchange 服务上的用户的路由位置的信息。</span><span class="sxs-lookup"><span data-stu-id="8f88f-106">A *hosted voice mail policy* provides information to the Lync Server 2013 ExUM Routing application about where to route calls for users whose mailboxes are located on a hosted Exchange service.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8f88f-107">仅在与托管 Exchange UM 的 Lync Server 2013 集成中需要托管语音邮件策略。</span><span class="sxs-lookup"><span data-stu-id="8f88f-107">Hosted voice mail policies are required only for Lync Server 2013 integration with hosted Exchange UM.</span></span> <span data-ttu-id="8f88f-108">它们不是与本地 Exchange UM 集成所必需的。</span><span class="sxs-lookup"><span data-stu-id="8f88f-108">They are not needed for integration with on-premises Exchange UM.</span></span>



</div>

<div>

## <a name="hosted-voice-mail-policy-scope"></a><span data-ttu-id="8f88f-109">托管语音邮件策略作用域</span><span class="sxs-lookup"><span data-stu-id="8f88f-109">Hosted Voice Mail Policy Scope</span></span>

<span data-ttu-id="8f88f-110">托管语音邮件策略范围确定策略适用的层次结构级别。</span><span class="sxs-lookup"><span data-stu-id="8f88f-110">Hosted voice mail policy scope determines the hierarchical level at which the policy applies.</span></span> <span data-ttu-id="8f88f-111">你可以配置具有以下范围级别的托管语音邮件策略：</span><span class="sxs-lookup"><span data-stu-id="8f88f-111">You can configure hosted voice mail policies with the following scope levels:</span></span>

  - <span data-ttu-id="8f88f-112">*全局* 策略可能会影响 Lync Server 2013 部署中的所有用户。</span><span class="sxs-lookup"><span data-stu-id="8f88f-112">The *global* policy can potentially affect all users in the Lync Server 2013 deployment.</span></span> <span data-ttu-id="8f88f-113">如果用户已启用托管 Exchange UM 访问，并且尚未分配每用户策略，并且尚未向用户的网站分配网站策略，则应用全局策略。</span><span class="sxs-lookup"><span data-stu-id="8f88f-113">If a user is enabled for hosted Exchange UM access and has not been assigned a per-user policy, and if a site policy has not been assigned to the user’s site, the global policy applies.</span></span> <span data-ttu-id="8f88f-114">全局策略随 Lync Server 2013 一起安装。</span><span class="sxs-lookup"><span data-stu-id="8f88f-114">The global policy is installed with Lync Server 2013.</span></span> <span data-ttu-id="8f88f-115">你可以对其进行修改以满足你的需求，但不能重命名或删除它。</span><span class="sxs-lookup"><span data-stu-id="8f88f-115">You can modify it to meet your needs, but you cannot rename or delete it.</span></span>

  - <span data-ttu-id="8f88f-116">*网站* 策略可能会影响托管在定义了该策略的网站上的所有用户。</span><span class="sxs-lookup"><span data-stu-id="8f88f-116">A *site* policy can affect all users that are homed on the site for which the policy is defined.</span></span> <span data-ttu-id="8f88f-117">如果用户已配置为托管 Exchange UM 访问，并且尚未分配每用户策略，则应用网站策略。</span><span class="sxs-lookup"><span data-stu-id="8f88f-117">If a user is configured for hosted Exchange UM access and has not been assigned a per-user policy, the site policy applies.</span></span>

  - <span data-ttu-id="8f88f-118">*每用户* 策略只能影响单个用户或组。</span><span class="sxs-lookup"><span data-stu-id="8f88f-118">A *per-user* policy can affect only individual users or groups.</span></span> <span data-ttu-id="8f88f-119">若要强制执行每用户策略，必须将策略显式分配给单个用户、组和联系人对象。</span><span class="sxs-lookup"><span data-stu-id="8f88f-119">To enforce a per-user policy, you must explicitly assign the policy to individual users, groups, and contact objects.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8f88f-120">在大多数情况下，只需要一个托管语音邮件策略。</span><span class="sxs-lookup"><span data-stu-id="8f88f-120">In most cases, only one hosted voice mail policy is required.</span></span> <span data-ttu-id="8f88f-121">你可以经常修改全局策略以满足你的所有需求。</span><span class="sxs-lookup"><span data-stu-id="8f88f-121">You can often modify the global policy to meet all your needs.</span></span> <span data-ttu-id="8f88f-122">如果你部署多个托管语音邮件策略，则所有此类策略都具有每用户范围。</span><span class="sxs-lookup"><span data-stu-id="8f88f-122">If you deploy multiple hosted voice mail policies, all such policies have per-user scope.</span></span>



</div>

</div>

<div>

## <a name="hosted-voice-mail-policy-attributes"></a><span data-ttu-id="8f88f-123">托管语音邮件策略属性</span><span class="sxs-lookup"><span data-stu-id="8f88f-123">Hosted Voice Mail Policy Attributes</span></span>

<span data-ttu-id="8f88f-124">语音邮件策略定义 Lync Server 2013 ExUM 路由应用程序在发送到托管 Exchange UM 实现的邀请邮件的请求 URI 中插入的两个属性：</span><span class="sxs-lookup"><span data-stu-id="8f88f-124">A voice mail policy defines two attributes that the Lync Server 2013 ExUM Routing application inserts in the request URI of an INVITE message that is sent to the hosted Exchange UM implementation:</span></span>

  - <span data-ttu-id="8f88f-125">**目标：** 托管 Exchange UM 服务的完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="8f88f-125">**Destination:** The fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="8f88f-126">此值由本地 Lync Server Edge 服务器用于路由用途。</span><span class="sxs-lookup"><span data-stu-id="8f88f-126">This value is used by the on-premises Lync Server Edge Server for routing purposes.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8f88f-127">Exchange Online 的 FQDN 为 exap.um.outlook.com。</span><span class="sxs-lookup"><span data-stu-id="8f88f-127">The FQDN for Exchange Online is exap.um.outlook.com.</span></span>

    
    </div>

  - <span data-ttu-id="8f88f-128">**组织：** 寄存 Lync Server 2013 用户邮箱的托管 Exchange UM 服务上的租户的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8f88f-128">**Organization:** The FQDN of the tenant on the hosted Exchange UM service that homes your Lync Server 2013 users’ mailboxes.</span></span> <span data-ttu-id="8f88f-129">语音邮件策略可以包含多个组织。</span><span class="sxs-lookup"><span data-stu-id="8f88f-129">A voice mail policy can contain multiple organizations.</span></span> <span data-ttu-id="8f88f-130">如果策略中包含多个组织，则此属性必须为主 Lync Server 2013 用户邮箱的 Exchange Server 租户的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="8f88f-130">If more than one organization is included in the policy, this attribute must be a comma-separated list of the Exchange Server tenants that home your Lync Server 2013 user mailboxes.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8f88f-131">托管 Exchange UM 服务的租户管理员将为目标和组织属性设置提供必要的值。</span><span class="sxs-lookup"><span data-stu-id="8f88f-131">The tenant administrator of your hosted Exchange UM service will provide the necessary values for your Destination and Organization attribute settings.</span></span> <span data-ttu-id="8f88f-132">若要配置你的策略，你必须运行 New-CsHostedVoicemailPolicy cmdlet 或使用 Set-CsHostedVoicemailPolicy cmdlet 修改存在的 (例如全局策略) 。</span><span class="sxs-lookup"><span data-stu-id="8f88f-132">To configure your policy, you must run the New-CsHostedVoicemailPolicy cmdlet or use the Set-CsHostedVoicemailPolicy cmdlet to modify one that exists (for example, the global policy).</span></span>



</div>

<span data-ttu-id="8f88f-133">有关管理托管语音邮件策略的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="8f88f-133">For details about managing hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="8f88f-134">New-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="8f88f-134">New-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="8f88f-135">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="8f88f-135">Set-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="8f88f-136">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="8f88f-136">Get-CsHostedVoicemailPolicy</span></span>

</div>

<div>

## <a name="per-user-voice-mail-policy-assignment"></a><span data-ttu-id="8f88f-137">Per-User 语音邮件策略分配</span><span class="sxs-lookup"><span data-stu-id="8f88f-137">Per-User Voice Mail Policy Assignment</span></span>

<span data-ttu-id="8f88f-138">如果托管语音邮件策略是使用每用户范围定义的，则必须显式分配它。</span><span class="sxs-lookup"><span data-stu-id="8f88f-138">If your hosted voice mail policy is defined with per-user scope, you must explicitly assign it.</span></span> <span data-ttu-id="8f88f-139">你可以运行 Grant-CsHostedVoicemailPolicy cmdlet，将策略分配给单个用户或组。</span><span class="sxs-lookup"><span data-stu-id="8f88f-139">You can run the Grant-CsHostedVoicemailPolicy cmdlet to assign the policy to individual users or groups.</span></span>

<span data-ttu-id="8f88f-140">有关分配或删除每用户托管语音邮件策略的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="8f88f-140">For details about assigning or removing a per-user hosted voice mail policy, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="8f88f-141">Grant-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="8f88f-141">Grant-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="8f88f-142">Remove-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="8f88f-142">Remove-CsHostedVoicemailPolicy</span></span>

<span data-ttu-id="8f88f-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f88f-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

