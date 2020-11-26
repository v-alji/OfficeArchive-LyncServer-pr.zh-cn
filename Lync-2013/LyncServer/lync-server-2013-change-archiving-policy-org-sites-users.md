---
title: Lync Server 2013：更改存档策略以启用或禁用组织、网站或用户的内部或外部通信的存档
description: Lync Server 2013：更改存档策略以启用或禁用组织、网站或用户的内部或外部通信的存档。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435178"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a><span data-ttu-id="db79a-103">在 Lync Server 2013 中更改存档策略以启用或禁用组织、网站或用户的内部或外部通信的存档</span><span class="sxs-lookup"><span data-stu-id="db79a-103">Changing an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for your organization, sites, or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db79a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db79a-104">

<span> </span></span></span>

<span data-ttu-id="db79a-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="db79a-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="db79a-106">在 Lync Server 2013 中，你可以使用策略为托管于 Lync Server 2013 的用户启用和禁用内部通信和外部通信的存档。</span><span class="sxs-lookup"><span data-stu-id="db79a-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="db79a-107">这包括以下存档策略：</span><span class="sxs-lookup"><span data-stu-id="db79a-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="db79a-108">部署 Lync Server 2013 时默认创建的全局策略。</span><span class="sxs-lookup"><span data-stu-id="db79a-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="db79a-109">可创建和使用的可选网站级和用户级策略，用于指定如何为特定网站或用户实现存档。</span><span class="sxs-lookup"><span data-stu-id="db79a-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="db79a-110">你在部署存档时最初设置存档策略，但你可以在部署后更改、添加和删除策略。</span><span class="sxs-lookup"><span data-stu-id="db79a-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="db79a-111">在 Lync Server 2013 控制面板中，你可以使用 "**存档和监视**" 组的 "**存档策略**" 页面管理全局级别、网站级别和用户级别的策略。</span><span class="sxs-lookup"><span data-stu-id="db79a-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="db79a-112">如果你将 Lync Server 存储与 Exchange 2013 存储集成，Exchange 用户策略将优先于 Lync Server 2013 存档策略。</span><span class="sxs-lookup"><span data-stu-id="db79a-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="db79a-113">有关如何实施策略的详细信息（包括策略的层次结构），请参阅规划文档、部署文档或操作文档中的在 [Lync Server 2013 中的存档的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="db79a-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="db79a-114">如果为你的部署启用了 Microsoft Exchange 集成，Exchange 策略将控制是否为托管于 Exchange 2013 的用户启用存档，并将其邮箱置于 In-Place 保留。</span><span class="sxs-lookup"><span data-stu-id="db79a-114">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="db79a-115">有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="db79a-115">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="db79a-116">在启用存档之前，应在存档配置中指定所有适当的选项。</span><span class="sxs-lookup"><span data-stu-id="db79a-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="db79a-117">有关详细信息，请参阅在 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 中为你的组织、网站和池在操作文档中管理存档配置选项</A> 。</span><span class="sxs-lookup"><span data-stu-id="db79a-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-change-an-archiving-policy"></a><span data-ttu-id="db79a-118">更改存档策略</span><span class="sxs-lookup"><span data-stu-id="db79a-118">To change an archiving policy</span></span>

1.  <span data-ttu-id="db79a-119">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="db79a-119">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="db79a-120">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="db79a-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="db79a-121">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="db79a-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="db79a-122">在左侧导航栏中，单击“监控和存档”，然后单击“存档策略”。</span><span class="sxs-lookup"><span data-stu-id="db79a-122">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="db79a-123">在策略列表中，执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="db79a-123">In the list of policies, do one of the following:</span></span>
    
      - <span data-ttu-id="db79a-124">若要更改整个部署的策略，请单击策略列表中的“**全局**”，再单击“**编辑**”，然后单击“**显示详细信息**”。</span><span class="sxs-lookup"><span data-stu-id="db79a-124">To change the policy for your entire deployment, click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="db79a-125">若要更改单个站点的策略，请单击策略列表中的站点名称，再单击“**编辑**”，然后单击“**显示详细信息**”。</span><span class="sxs-lookup"><span data-stu-id="db79a-125">To change the policy for a single site, click the site name in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="db79a-126">若要更改单个用户或用户组的策略，请单击策略列表中的用户或用户组的名称，再单击“**编辑**”，然后单击“**显示详细信息**”。</span><span class="sxs-lookup"><span data-stu-id="db79a-126">To change the policy for a single user or user group, click the user or user group name in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="db79a-127">在“**编辑存档策略**”页中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="db79a-127">On the **Edit Archiving Policy** page, do the following:</span></span>
    
      - <span data-ttu-id="db79a-128">若要为策略启用或禁用内部存档，请选中或清除“**存档内部通信**”复选框。</span><span class="sxs-lookup"><span data-stu-id="db79a-128">To enable or disable internal archiving for the policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="db79a-129">若要为策略启用或禁用外部存档，请选中或清除“**存档外部通信**”复选框。</span><span class="sxs-lookup"><span data-stu-id="db79a-129">To enable or disable external archiving for the policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="db79a-130">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="db79a-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="db79a-131">用户策略的设置仅适用于要应用该策略的特定用户和用户组。</span><span class="sxs-lookup"><span data-stu-id="db79a-131">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="db79a-132">有关详细信息，请参阅 <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">将存档策略应用于 Lync Server 2013 中的用户</A></span><span class="sxs-lookup"><span data-stu-id="db79a-132">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="db79a-133">使用 Windows PowerShell Cmdlet 启用和禁用存档</span><span class="sxs-lookup"><span data-stu-id="db79a-133">Enabling and Disabling Archiving by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="db79a-134">可以使用 **CsArchivingPolicy** cmdlet 在内部和外部通信会话) 启用和禁用存档 (。</span><span class="sxs-lookup"><span data-stu-id="db79a-134">Archiving can be enabled and disabled (for both internal and external communication sessions) by using the **Set-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="db79a-135">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="db79a-135">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="db79a-136">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="db79a-136">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a><span data-ttu-id="db79a-137">启用内部通信会话的存档</span><span class="sxs-lookup"><span data-stu-id="db79a-137">To enable the archiving of internal communication sessions</span></span>

  - <span data-ttu-id="db79a-138">若要启用内部通信会话的存档，请将 **ArchiveInternal** 属性的值设置为 True ($True) 。</span><span class="sxs-lookup"><span data-stu-id="db79a-138">To enable archiving of internal communication sessions, set the value of the **ArchiveInternal** property to True ($True).</span></span> <span data-ttu-id="db79a-139">例如：</span><span class="sxs-lookup"><span data-stu-id="db79a-139">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a><span data-ttu-id="db79a-140">启用外部通信会话的存档</span><span class="sxs-lookup"><span data-stu-id="db79a-140">To enable the archiving of external communication sessions</span></span>

  - <span data-ttu-id="db79a-141">若要启用外部通信会话的存档，请将 **ArchiveExternal** 属性的值设置为 True ($True) 。</span><span class="sxs-lookup"><span data-stu-id="db79a-141">To enable archiving of external communication sessions, set the value of the **ArchiveExternal** property to True ($True).</span></span> <span data-ttu-id="db79a-142">例如：</span><span class="sxs-lookup"><span data-stu-id="db79a-142">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="db79a-143">启用内部和外部通信会话的存档</span><span class="sxs-lookup"><span data-stu-id="db79a-143">To enable the archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="db79a-144">若要同时启用内部和外部通信会话的存档，请将 **ArchiveInternal** 和 **ArchiveExternal** 属性设置为 True：</span><span class="sxs-lookup"><span data-stu-id="db79a-144">To enable archiving of both internal and external communications sessions, set both the **ArchiveInternal** and the **ArchiveExternal** properties to True:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a><span data-ttu-id="db79a-145">禁用存档</span><span class="sxs-lookup"><span data-stu-id="db79a-145">To disable archiving</span></span>

  - <span data-ttu-id="db79a-146">若要完全禁用存档，请将 **ArchiveInternal** 和 **ArchiveExternal** 属性设置为 False ($False) 。</span><span class="sxs-lookup"><span data-stu-id="db79a-146">To disable archiving altogether, set both the **ArchiveInternal** and **ArchiveExternal** properties to False ($False).</span></span> <span data-ttu-id="db79a-147">例如：</span><span class="sxs-lookup"><span data-stu-id="db79a-147">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

<span data-ttu-id="db79a-148">有关详细信息，请参阅 [CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="db79a-148">For more information, see the help topic for the [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="db79a-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db79a-149">See Also</span></span>


[<span data-ttu-id="db79a-150">在 Lync Server 2013 中管理内部和外部通信的存档</span><span class="sxs-lookup"><span data-stu-id="db79a-150">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="db79a-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db79a-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

