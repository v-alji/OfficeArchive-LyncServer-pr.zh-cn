---
title: Lync Server 2013：将存档策略应用于用户
description: Lync Server 2013：将存档策略应用于用户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Applying an Archiving policy to users
ms:assetid: 624a7d3e-389d-403a-97e5-f7bb17023ef3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521004(v=OCS.15)
ms:contentKeyID: 48184290
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54b82a68a75da7b389167097d8b08358cf680e1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439870"
---
# <a name="applying-an-archiving-policy-to-users-in-lync-server-2013"></a><span data-ttu-id="ad5e9-103">将存档策略应用于 Lync Server 2013 中的用户</span><span class="sxs-lookup"><span data-stu-id="ad5e9-103">Applying an Archiving policy to users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad5e9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad5e9-104">

<span> </span></span></span>

<span data-ttu-id="ad5e9-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ad5e9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ad5e9-106">如果用户已启用 Lync Server 2013，并且已为驻留在 Lync Server 2013 上的用户创建了一个或多个用户策略，则可以通过向这些用户或用户组应用相应的策略来实现对特定用户的存档支持。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-106">If a user has been enabled for Lync Server 2013 and you have created one or more user policies for archiving for users homed on Lync Server 2013, you can implement archiving support for specific users by applying the appropriate policies to those users or user groups.</span></span> <span data-ttu-id="ad5e9-107">例如，如果创建了支持内部通信存档的策略，则可以将其应用到至少一个用户或用户组以支持用户的 Lync Server 2013 通信的存档。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-107">For example, if you create a policy to support archiving of internal communications, you can apply it to at least one user or user group to support archiving of the user’s Lync Server 2013 communications.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ad5e9-108">如果为你的部署启用了 Microsoft Exchange 集成，Exchange In-Place 保留策略控制是否为托管于 Exchange 2013 的用户启用存档，并将其邮箱置于 In-Place 保留状态。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-108">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="ad5e9-109">有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-109">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="ad5e9-110">在启用存档之前，应在存档配置中指定所有适当的选项。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="ad5e9-111">有关详细信息，请参阅在 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 中为你的组织、网站和池在操作文档中管理存档配置选项</A> 。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-111">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<span data-ttu-id="ad5e9-112">使用本主题中的过程将以前创建的存档用户策略应用于一个或多个用户帐户或用户组。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-112">Use the procedure in this topic to apply a previously created Archiving user policy to one or more user accounts or user groups.</span></span>

<div>

## <a name="to-apply-an-archiving-user-policy-to-a-user-account"></a><span data-ttu-id="ad5e9-113">将存档用户策略应用于用户帐户</span><span class="sxs-lookup"><span data-stu-id="ad5e9-113">To apply an archiving user policy to a user account</span></span>

1.  <span data-ttu-id="ad5e9-114">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-114">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ad5e9-115">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ad5e9-116">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ad5e9-117">在左侧导航栏中，单击“**用户**”，然后搜索要配置的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-117">In the left navigation bar, click **Users**, and then search for the user account that you want to configure.</span></span>

4.  <span data-ttu-id="ad5e9-118">在列出搜索结果的表中，单击相应的用户帐户，再单击“**编辑**”，然后单击“**显示详细信息**”。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-118">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="ad5e9-119">在 "在 **存档策略** 中 **编辑 Lync 服务器用户**" 下，选择要应用的存档用户策略。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-119">In **Edit Lync Server User** under **Archiving policy**, select the archiving user policy that you want to apply.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ad5e9-120">" <STRONG> &lt; 自动 &gt; </STRONG>设置" 应用默认服务器安装设置。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-120">The <STRONG>&lt;Automatic&gt;</STRONG> settings apply the default server installation settings.</span></span> <span data-ttu-id="ad5e9-121">服务器将自动应用这些设置。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-121">These settings are applied automatically by the server.</span></span>

    
    </div>

6.  <span data-ttu-id="ad5e9-122">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="assigning-a-per-user-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ad5e9-123">使用 Windows PowerShell Cmdlet 分配 Per-User 存档策略</span><span class="sxs-lookup"><span data-stu-id="ad5e9-123">Assigning a Per-User Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ad5e9-124">可以使用 Windows PowerShell 和 **CsArchivingPolicy** cmdlet 分配每用户存档策略。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-124">Per-user archiving policies can be assigned by using Windows PowerShell and the **Grant-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="ad5e9-125">你可以从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行此 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-125">You can run this cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ad5e9-126">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-assign-a-per-user-archiving-policy-to-a-single-user"></a><span data-ttu-id="ad5e9-127">将每用户存档策略分配给单个用户</span><span class="sxs-lookup"><span data-stu-id="ad5e9-127">To assign a per-user archiving policy to a single user</span></span>

  - <span data-ttu-id="ad5e9-128">以下命令向用户 Ken Myer 分配每用户存档策略 RedmondArchivingPolicy。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-128">The following command assigns the per-user archiving policy RedmondArchivingPolicy to the user Ken Myer.</span></span>
    
        Grant-CsArchivingPolicy -Identity "Ken Myer" -PolicyName "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-assign-a-per-user-archiving-policy-to-multiple-users"></a><span data-ttu-id="ad5e9-129">将每用户存档策略分配给多个用户</span><span class="sxs-lookup"><span data-stu-id="ad5e9-129">To assign a per-user archiving policy to multiple users</span></span>

  - <span data-ttu-id="ad5e9-130">此命令将每用户存档策略 RedmondArchivingPolicy 分配给所有帐户驻留在注册机构池 atl-cs-001.litwareinc.com 的用户。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-130">This command assigns the per-user archiving policy RedmondArchivingPolicy to all users who have accounts homed on the Registrar pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="ad5e9-131">有关此命令中使用的筛选器参数的详细信息，请参阅 [move-csuser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) cmdlet 文档。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-131">For details about the Filter parameter used in this command, see the [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) cmdlet documentation.</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "atl-cs-001.litwareinc.com"} | Grant-CsArchivingPolicy -PolicyName "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-assign-a-per-user-archiving-policy"></a><span data-ttu-id="ad5e9-132">分配每个用户的存档策略</span><span class="sxs-lookup"><span data-stu-id="ad5e9-132">To assign a per-user archiving policy</span></span>

  - <span data-ttu-id="ad5e9-133">以下命令取消之前分配给 Ken Myer 的任何每用户存档策略。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-133">The following command unassigns any per-user archiving policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="ad5e9-134">取消分配每用户策略后，将自动使用全局策略或本地站点策略（如果存在）管理 Ken Myer。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-134">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="ad5e9-135">站点策略优先于全局策略。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-135">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsArchivingPolicy -Identity "Ken Myer" -PolicyName $Null

</div>

<span data-ttu-id="ad5e9-136">有关详细信息，请参阅 [CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsArchivingPolicy) cmdlet 文档。</span><span class="sxs-lookup"><span data-stu-id="ad5e9-136">For details, see the [Grant-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsArchivingPolicy) cmdlet documentation.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ad5e9-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ad5e9-137">See Also</span></span>


[<span data-ttu-id="ad5e9-138">在 Lync Server 2013 中管理内部和外部通信的存档</span><span class="sxs-lookup"><span data-stu-id="ad5e9-138">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
[<span data-ttu-id="ad5e9-139">在 Lync Server 2013 中分配每个用户的策略</span><span class="sxs-lookup"><span data-stu-id="ad5e9-139">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)  
  

<span data-ttu-id="ad5e9-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad5e9-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

