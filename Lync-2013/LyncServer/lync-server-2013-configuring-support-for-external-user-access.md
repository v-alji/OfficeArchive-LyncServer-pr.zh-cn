---
title: Lync Server 2013：配置对外部用户访问的支持
description: Lync Server 2013：配置对外部用户访问的支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for external user access
ms:assetid: f8424f8c-f965-4414-8485-30f07e10214a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413051(v=OCS.15)
ms:contentKeyID: 48185874
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d5a91f9b285a80ff6a0f3c58c2c12f88d72aac98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432616"
---
# <a name="configuring-support-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="67ce0-103">在 Lync Server 2013 中配置对外部用户访问的支持</span><span class="sxs-lookup"><span data-stu-id="67ce0-103">Configuring support for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67ce0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67ce0-104">

<span> </span></span></span>

<span data-ttu-id="67ce0-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="67ce0-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="67ce0-106">部署边缘服务器或边缘池是支持外部用户的第一步。</span><span class="sxs-lookup"><span data-stu-id="67ce0-106">Deploying an Edge Server or Edge pool is the first step to supporting external users.</span></span> <span data-ttu-id="67ce0-107">有关部署边缘服务器的详细信息，请参阅部署文档中 [Lync Server 2013 中的 "部署外部用户访问](lync-server-2013-deploying-external-user-access.md) "。</span><span class="sxs-lookup"><span data-stu-id="67ce0-107">For details about deploying Edge Servers, see [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span> <span data-ttu-id="67ce0-108">策略配置的一个重要考虑因素是了解策略的优先级以及策略的应用方式。</span><span class="sxs-lookup"><span data-stu-id="67ce0-108">An important consideration for the configuration of policies is to understand the precedence of policies and how the policies are applied.</span></span> <span data-ttu-id="67ce0-109">在一个策略级别应用的 Lync Server 策略设置可以覆盖在其他策略级别应用的设置。</span><span class="sxs-lookup"><span data-stu-id="67ce0-109">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="67ce0-110">Lync 服务器策略优先级为：用户策略 (大多数影响) 覆盖网站策略，然后网站策略将覆盖全局策略 (最少影响) 。</span><span class="sxs-lookup"><span data-stu-id="67ce0-110">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="67ce0-111">这意味着，策略设置与策略所影响的对象距离越近，它对该对象的影响力越大。</span><span class="sxs-lookup"><span data-stu-id="67ce0-111">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>

<span data-ttu-id="67ce0-112">完成边缘服务器或边缘池的设置后，必须启用要提供的外部用户访问类型，并配置外部访问的设置。</span><span class="sxs-lookup"><span data-stu-id="67ce0-112">After completing the setup of an Edge Server or Edge pool, you must enable the types of external user access that you want to provide, and configure the settings for the external access.</span></span> <span data-ttu-id="67ce0-113">在 Lync Server 2013 中，你可以使用 Lync Server 控制面板、Lync Server Management Shell 或两者（基于任务要求）启用和配置外部用户访问和策略。</span><span class="sxs-lookup"><span data-stu-id="67ce0-113">In Lync Server 2013, you enable and configure external user access and policies using the Lync Server Control Panel, the Lync Server Management Shell or both, based on the task requirements.</span></span>

<span data-ttu-id="67ce0-114">若要支持外部用户访问，必须执行以下两项操作：</span><span class="sxs-lookup"><span data-stu-id="67ce0-114">To support external user access, you must do both of the following:</span></span>

  - <span data-ttu-id="67ce0-115">**为你的组织启用支持**   若要在你的部署中启用外部用户访问支持，你可以启用希望支持的每种类型的外部访问。</span><span class="sxs-lookup"><span data-stu-id="67ce0-115">**Enable support for your organization**   To enable support for external user access in your deployment, you enable each type of external access that you want to support.</span></span> <span data-ttu-id="67ce0-116">通过在 Lync Server 控制面板的 "**联盟和外部访问**" 组中编辑全局设置或在 "**外部访问策略**" 页面上创建和配置网站或用户策略来启用和禁用对外部用户访问的支持，或使用 lync server 管理外壳程序和相关 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67ce0-116">You enable and disable support for external user access by editing the global settings or creating and configuring a site or user policy on the **External Access Policy** page in the **Federation and External Access** group of the Lync Server Control Panel or by using the Lync Server Management Shell and associated cmdlets.</span></span> <span data-ttu-id="67ce0-117">用于管理 **外部访问策略** 的 Cmdlet 位于 [Lync Server 2013 中的主题联盟和外部访问 cmdlet](https://docs.microsoft.com/powershell/module/skype/)中。</span><span class="sxs-lookup"><span data-stu-id="67ce0-117">Cmdlets for managing the **External Access Policy** are found in the topic [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/).</span></span> <span data-ttu-id="67ce0-118">启用对外部访问的支持指定运行 Lync Server Access Edge 服务的服务器支持与外部用户和服务器的通信。</span><span class="sxs-lookup"><span data-stu-id="67ce0-118">Enabling support for external access specifies that your servers running the Lync Server Access Edge service support communications with external users and servers.</span></span> <span data-ttu-id="67ce0-119">外部用户访问被禁用，或者策略尚未配置为支持它时，内部和外部用户无法进行通信。</span><span class="sxs-lookup"><span data-stu-id="67ce0-119">Internal and external users cannot communicate while external user access is disabled or if policies have not yet been configured to support it.</span></span>

  - <span data-ttu-id="67ce0-120">**配置和分配一个或多个策略**   若要支持外部用户访问，请配置策略来解决要求，包括：</span><span class="sxs-lookup"><span data-stu-id="67ce0-120">**Configure and assign one or more policies**   To support external user access, you configure policies to address requirements that include:</span></span>
    
      - <span data-ttu-id="67ce0-121">**外部访问策略**   使用 "网站" 或 "用户" 作用域创建 (全局策略默认情况下存在，并且没有启用的设置) 。</span><span class="sxs-lookup"><span data-stu-id="67ce0-121">**External access policies**   Created with either a site or user scope (a global policy exists by default and has no enabled settings).</span></span> <span data-ttu-id="67ce0-122">你可以创建和配置策略来控制使用一个或多个类型的外部用户访问权限，包括联合用户访问 (，包括（如果已选中）联盟 XMPP 域) 远程用户用户访问和受支持的公共 IM 服务提供商。</span><span class="sxs-lookup"><span data-stu-id="67ce0-122">You create and configure policies to control the use of one or more types of external user access, including, federated user access (including, if selected, federated XMPP domains)remote users user access, and supported public IM service providers.</span></span> <span data-ttu-id="67ce0-123">在 "**联盟和外部访问**" 组中的 "**外部访问策略**" 页面上，使用全局策略或一个或多个管理员创建的网站和用户策略在 Lync Server 控制面板中配置外部策略。</span><span class="sxs-lookup"><span data-stu-id="67ce0-123">You configure external policies in Lync Server Control Panel using the global policy or one or more administratively created site and user policies, on the **External Access Policy** page in the **Federation and External Access** group.</span></span> <span data-ttu-id="67ce0-124">无法删除全局策略。</span><span class="sxs-lookup"><span data-stu-id="67ce0-124">The global policy cannot be deleted.</span></span> <span data-ttu-id="67ce0-125">你可以创建和配置你希望用于限制特定网站或用户的外部用户访问的任何网站和用户策略。</span><span class="sxs-lookup"><span data-stu-id="67ce0-125">You create and configure any site and user policies that you want to use to limit external user access for specific sites or users.</span></span> <span data-ttu-id="67ce0-126">全局和网站策略将自动分配。</span><span class="sxs-lookup"><span data-stu-id="67ce0-126">Global and site policies are automatically assigned.</span></span> <span data-ttu-id="67ce0-127">如果创建和配置用户策略，则必须使用 " **用户** " 页面上 "Lync Server 控制面板" 中的 "用户配置" 页面将其分配给特定用户。</span><span class="sxs-lookup"><span data-stu-id="67ce0-127">If you create and configure a user policy, you must then assign it to the specific users by using the user configuration page in the Lync Server Control Panel on the **Users** page.</span></span> <span data-ttu-id="67ce0-128">查找要应用此策略的一个或一用户，然后分配该策略。</span><span class="sxs-lookup"><span data-stu-id="67ce0-128">Find the user or users that you want this policy to apply to and assign the policy.</span></span> <span data-ttu-id="67ce0-129">要对其应用。</span><span class="sxs-lookup"><span data-stu-id="67ce0-129">to whom you want it to apply.</span></span> <span data-ttu-id="67ce0-130">若要为用户分配已配置的用户策略，请参阅 [在 Lync Server 2013 中将外部用户访问策略分配给启用 Lync 的用户](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)。</span><span class="sxs-lookup"><span data-stu-id="67ce0-130">To assign a configured user policy to a user, see [Assign an external user access policy to a Lync enabled user in Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md).</span></span> <span data-ttu-id="67ce0-131">每个外部用户访问策略都可以支持下列一项或多项操作：远程用户访问、SIP 联合用户访问、XMPP 联盟用户访问和公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="67ce0-131">Each external user access policy can support one or more of the following: remote user access, SIP federated user access, XMPP federated user access and public IM connectivity.</span></span>
    
      - <span data-ttu-id="67ce0-132">**会议策略**   你可以创建和配置策略来控制你的组织中的会议，包括组织中的哪些用户可以邀请匿名用户参与他们托管的会议。</span><span class="sxs-lookup"><span data-stu-id="67ce0-132">**Conferencing policies**   You create and configure policies to control conferencing in your organization, including which users in your organization can invite anonymous users to conferences that they host.</span></span> <span data-ttu-id="67ce0-133">在 Lync Server "控制面板 **会议** " 页面上是全局、网站和用户范围内的策略设置，用于控制实际会议的设置。</span><span class="sxs-lookup"><span data-stu-id="67ce0-133">On the Lync Server Control Panel **Conferencing** page are policy settings at the global, site and user scope that control settings for the actual conferences.</span></span> <span data-ttu-id="67ce0-134">有关详细信息，请参阅 [在 Lync Server 2013 中管理会议和会议](lync-server-2013-managing-meetings-and-conferences.md)。</span><span class="sxs-lookup"><span data-stu-id="67ce0-134">For details, see [Managing meetings and conferences in Lync Server 2013](lync-server-2013-managing-meetings-and-conferences.md).</span></span> <span data-ttu-id="67ce0-135">在 " **访问边缘配置** " 页面上为会议、远程用户和联盟用户启用匿名用户。</span><span class="sxs-lookup"><span data-stu-id="67ce0-135">You enable anonymous users for conferencing, remote users and federated users on the **Access Edge Configuration** page.</span></span> <span data-ttu-id="67ce0-136">**访问边缘配置** 上的策略在范围内为全局。</span><span class="sxs-lookup"><span data-stu-id="67ce0-136">The policy on the **Access Edge Configuration** is global in scope.</span></span> <span data-ttu-id="67ce0-137">没有可用于定义网站或用户策略的选项。</span><span class="sxs-lookup"><span data-stu-id="67ce0-137">There are no options to define a site or user policy.</span></span> <span data-ttu-id="67ce0-138">通过使用全局、网站或用户策略设置，可在 **外部访问策略** 页面上控制范围。</span><span class="sxs-lookup"><span data-stu-id="67ce0-138">The scope is controlled on the **External Access Policy** page through the use of global, site, or user policy settings.</span></span>
        
        <span data-ttu-id="67ce0-139">例如，如果您希望允许用户创建、邀请和管理与远程用户的会议，则必须在 "**外部访问策略** 全局"、"网站或用户策略" 上设置 "**启用与远程用户的通信**"，并 **启用与**"**访问边缘配置**" 页面上的远程用户的通信。</span><span class="sxs-lookup"><span data-stu-id="67ce0-139">For example, if you want to allow users to create, invite and manage conferencing with remote users, you must set **Enable communications with remote users** on the **External Access Policy** global, site or user policy, and **Enable Communications with remote users** on the **Access Edge Configuration** page.</span></span> <span data-ttu-id="67ce0-140">同样，若要允许具有已定义关系的匿名用户或联盟合作伙伴与 (（如配置的联合 SIP 域和提供程序）具有定义的关系（如已配置的联合 SIP 域和提供程序) ），则在 "**外部访问策略** 全局、网站或用户策略" 中设置 **与公共用户进行通信** 并 **启用联盟用户的通信**。</span><span class="sxs-lookup"><span data-stu-id="67ce0-140">Similarly, to allow conferencing with anonymous users or federated partners that you have a defined relationship with (such as configured federated SIP domains and providers – XMPP federation does not support conferencing), you set **Enable communications with public users** and **Enable communications with federated users** in the **External Access Policy** global, site or user policy.</span></span> <span data-ttu-id="67ce0-141">然后，选择 "已获取的全局策略设置"，在 "**访问边缘配置**" 页面上 **启用对会议的匿名用户访问** 并 **启用联盟和公共 IM 连接**。</span><span class="sxs-lookup"><span data-stu-id="67ce0-141">You then select complimentary global policy settings **Enable anonymous user access to conferences** and **Enable federated and public IM connectivity** on the **Access Edge Configuration** page.</span></span>

<span data-ttu-id="67ce0-142">你可以配置外部用户访问设置，包括你希望用于控制外部用户访问的任何策略，即使你未启用组织的外部用户访问权限也是如此。</span><span class="sxs-lookup"><span data-stu-id="67ce0-142">You can configure external user access settings, including any policies that you want to use to control external user access, even if you have not enabled external user access for your organization.</span></span> <span data-ttu-id="67ce0-143">但是，你配置的策略和其他设置仅在你为你的组织启用外部用户访问时才有效。</span><span class="sxs-lookup"><span data-stu-id="67ce0-143">However, the policies and other settings that you configure are in effect only when you have external user access enabled for your organization.</span></span> <span data-ttu-id="67ce0-144">当外部用户访问被禁用或者没有配置任何外部用户访问策略来支持它时，外部用户无法与组织用户通信。</span><span class="sxs-lookup"><span data-stu-id="67ce0-144">External users cannot communicate with users of your organization when external user access is disabled or if no external user access policies are configured to support it.</span></span>

<span data-ttu-id="67ce0-145">你的 edge 部署对外部 (用户的类型进行身份验证，但匿名用户除外，这些用户通过会议 ID 进行身份验证，并根据你配置 edge 支持的方式向匿名参与者发送到匿名参与者) 和控制访问权限。</span><span class="sxs-lookup"><span data-stu-id="67ce0-145">Your edge deployment authenticates the types of external users (except for anonymous users, who are authenticated by the conference ID and a passkey that is sent to the anonymous participant when you create the conference and invite participants) and controls access based on how you configure your edge support.</span></span> <span data-ttu-id="67ce0-146">为了控制通信，你可以配置一个或多个策略，并配置定义你的部署内部和外部的用户之间如何相互通信的设置。</span><span class="sxs-lookup"><span data-stu-id="67ce0-146">In order to control communications, you can configure one or more policies and configure settings that define how users inside and outside your deployment communicate with each other.</span></span> <span data-ttu-id="67ce0-147">除了可创建和配置以启用特定网站或用户的一种或多种类型的外部用户访问的网站和用户策略之外，策略和设置包括外部用户访问的默认全局策略。</span><span class="sxs-lookup"><span data-stu-id="67ce0-147">The policies and settings include the default global policy for external user access, in addition to site and user policies that you can create and configure to enable one or more types of external user access for specific sites or users.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="67ce0-148">本节内容</span><span class="sxs-lookup"><span data-stu-id="67ce0-148">In This Section</span></span>

  - [<span data-ttu-id="67ce0-149">在 Lync Server 2013 中配置策略以控制远程用户访问</span><span class="sxs-lookup"><span data-stu-id="67ce0-149">Configure policies to control remote user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-remote-user-access.md)

  - [<span data-ttu-id="67ce0-150">在 Lync Server 2013 中启用或禁用远程用户访问</span><span class="sxs-lookup"><span data-stu-id="67ce0-150">Enable or disable remote user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-remote-user-access.md)

  - [<span data-ttu-id="67ce0-151">在 Lync Server 2013 中启用或禁用匿名用户访问</span><span class="sxs-lookup"><span data-stu-id="67ce0-151">Enable or disable anonymous user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-anonymous-user-access.md)

  - [<span data-ttu-id="67ce0-152">在 Lync Server 2013 中分配会议策略以支持匿名用户</span><span class="sxs-lookup"><span data-stu-id="67ce0-152">Assign conferencing policies to support anonymous users in Lync Server 2013</span></span>](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md)

<span data-ttu-id="67ce0-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67ce0-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

