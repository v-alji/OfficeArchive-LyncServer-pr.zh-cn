---
title: Lync Server 2013：创建存档策略以启用或禁用特定网站或用户的内部或外部通信的存档
description: Lync Server 2013：创建存档策略以启用或禁用特定网站或用户的内部或外部通信的存档。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431986"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a><span data-ttu-id="e8ba1-103">在 Lync Server 2013 中创建存档策略，以启用或禁用特定网站或用户的内部或外部通信的存档</span><span class="sxs-lookup"><span data-stu-id="e8ba1-103">Creating an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for specific sites or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8ba1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8ba1-104">

<span> </span></span></span>

<span data-ttu-id="e8ba1-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e8ba1-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e8ba1-106">在 Lync Server 2013 中，你可以使用策略为托管于 Lync Server 2013 的用户启用和禁用内部通信和外部通信的存档。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="e8ba1-107">这包括以下存档策略：</span><span class="sxs-lookup"><span data-stu-id="e8ba1-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="e8ba1-108">部署 Lync Server 2013 时默认创建的全局策略。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="e8ba1-109">可创建和使用的可选网站级和用户级策略，用于指定如何为特定网站或用户实现存档。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="e8ba1-110">你在部署存档时最初设置存档策略，但你可以在部署后更改、添加和删除策略。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="e8ba1-111">在 Lync Server 2013 控制面板中，你可以使用 "**存档和监视**" 组的 "**存档策略**" 页面管理全局级别、网站级别和用户级别的策略。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="e8ba1-112">如果你将 Lync Server 存储与 Exchange 2013 存储集成，Exchange 用户策略将优先于 Lync Server 2013 存档策略。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="e8ba1-113">有关如何实施策略的详细信息（包括策略的层次结构），请参阅规划文档、部署文档或操作文档中的在 [Lync Server 2013 中的存档的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="e8ba1-114">若要控制存档的实现，必须指定存档配置中的选项，例如，是存档 IM 还是会议、使用关键模式和清除选项。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-114">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="e8ba1-115">默认情况下，全局存档配置或任何网站或池存档配置中均未启用任何选项。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-115">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="e8ba1-116">应在存档配置中指定所有适当的选项，然后才能在存档策略中启用内部或外部通信的存档。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="e8ba1-117">有关详细信息，请参阅在 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 中为你的组织、网站和池在操作文档中管理存档配置选项</A> 。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="e8ba1-118">如果为你的部署启用了 Microsoft Exchange 集成，Exchange 策略将控制是否为托管于 Exchange 2013 的用户启用存档，并将其邮箱置于 In-Place 保留。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-118">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="e8ba1-119">有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-119">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a><span data-ttu-id="e8ba1-120">为网站或用户创建存档策略</span><span class="sxs-lookup"><span data-stu-id="e8ba1-120">To create an archiving policy for a site or users</span></span>

1.  <span data-ttu-id="e8ba1-121">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-121">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e8ba1-122">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e8ba1-123">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e8ba1-124">在左侧导航栏中，单击“监控和存档”，然后单击“存档策略”。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-124">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="e8ba1-125">单击“**新建**”，然后执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="e8ba1-125">Click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="e8ba1-126">若要创建网站级别的存档策略，请单击 " **网站策略** "，然后在 " **选择网站**" 中，单击要应用策略的网站。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-126">To create a site-level archiving policy, click **Site policy** and then, in **Select a site**, click the site to which the policy is to be applied.</span></span>
    
      - <span data-ttu-id="e8ba1-127">若要创建用户级别的存档策略，请单击“**用户策略**”。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-127">To create a user-level archiving policy, click **User policy**.</span></span>

5.  <span data-ttu-id="e8ba1-128">在“**新建存档策略**”中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="e8ba1-128">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="e8ba1-129">在“**名称**”中，指定新策略的名称（例如，externalContoso）。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-129">In **Name**, specify a name for the new policy (for example, externalContoso).</span></span>
    
      - <span data-ttu-id="e8ba1-130">在“**说明**”中，提供有关该策略内容的详细信息（例如，Contoso 的外部用户存档策略）。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-130">In **Description**, provide details about what the policy is (for example, External user archiving policy for Contoso).</span></span>
    
      - <span data-ttu-id="e8ba1-131">要控制内部用户通信的存档，请选中或清除“**存档内部通信**”复选框。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-131">To control archiving of communications with internal users, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="e8ba1-132">要控制外部用户通信的存档，请选中或清除“**存档外部通信**”复选框。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-132">To control archiving of communications with external users, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="e8ba1-133">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-133">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="e8ba1-134">用户策略的设置仅适用于要应用该策略的特定用户和用户组。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-134">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="e8ba1-135">有关详细信息，请参阅 <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">将存档策略应用于 Lync Server 2013 中的用户</A></span><span class="sxs-lookup"><span data-stu-id="e8ba1-135">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e8ba1-136">使用 Windows PowerShell Cmdlet 创建存档策略</span><span class="sxs-lookup"><span data-stu-id="e8ba1-136">Creating an Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e8ba1-137">可以使用 Windows PowerShell 和 **CsArchivingPolicy** cmdlet 创建存档策略。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-137">Archiving policies can be created by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="e8ba1-138">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e8ba1-139">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a><span data-ttu-id="e8ba1-140">在网站范围内创建新的存档策略</span><span class="sxs-lookup"><span data-stu-id="e8ba1-140">To create a new archiving policy at the site scope</span></span>

  - <span data-ttu-id="e8ba1-141">此命令可为 Redmond 站点创建新的存档策略：</span><span class="sxs-lookup"><span data-stu-id="e8ba1-141">This command creates a new archiving policy for the Redmond site:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a><span data-ttu-id="e8ba1-142">在每用户范围内创建新的存档策略</span><span class="sxs-lookup"><span data-stu-id="e8ba1-142">To create a new archiving policy at the per-user scope</span></span>

  - <span data-ttu-id="e8ba1-143">若要在每用户范围内创建新的存档策略，只需在创建策略时指定唯一标识：</span><span class="sxs-lookup"><span data-stu-id="e8ba1-143">To create a new archiving policy at the per-user scope, simply specify a unique Identity when creating the policy:</span></span>
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a><span data-ttu-id="e8ba1-144">要创建允许对内部通信会话进行存档的新存档策略</span><span class="sxs-lookup"><span data-stu-id="e8ba1-144">To create a new archiving policy that enables archiving of internal communication sessions</span></span>

  - <span data-ttu-id="e8ba1-145">由于前面的命令中未指定参数（必需的 Identity 参数之外），因此新策略将对其所有属性使用默认值。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding commands, the new policies will use the default values for all their properties.</span></span> <span data-ttu-id="e8ba1-146">若要创建使用其他属性值的策略，只需包括适当的参数和参数值。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-146">To create policies that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="e8ba1-147">例如，若要创建允许存档内部即时消息会话的存档策略，请使用如下所示的命令：</span><span class="sxs-lookup"><span data-stu-id="e8ba1-147">For example, to create an archiving policy that permits archiving of internal instant messaging sessions use a command like this:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="e8ba1-148">要创建允许对内部和外部通信会话进行存档的新存档策略</span><span class="sxs-lookup"><span data-stu-id="e8ba1-148">To create a new archiving policy that enables archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="e8ba1-149">可通过包含多个参数来修改多个属性值。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-149">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="e8ba1-150">例如，此命令将配置新策略以存档内部和外部即时消息会话：</span><span class="sxs-lookup"><span data-stu-id="e8ba1-150">For example, this command configures the new policy to archiving both internal and external instant messaging sessions:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

<span data-ttu-id="e8ba1-151">有关详细信息，请参阅 [CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="e8ba1-151">For more information, see the help topic for the [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e8ba1-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8ba1-152">See Also</span></span>


[<span data-ttu-id="e8ba1-153">在 Lync Server 2013 中管理内部和外部通信的存档</span><span class="sxs-lookup"><span data-stu-id="e8ba1-153">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="e8ba1-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8ba1-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

