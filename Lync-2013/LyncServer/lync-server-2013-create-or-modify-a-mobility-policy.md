---
title: Lync Server 2013：创建或修改移动策略
description: Lync Server 2013：创建或修改移动策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a mobility policy
ms:assetid: fc2dfea0-2215-440d-9f4b-7c985da29211
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721946(v=OCS.15)
ms:contentKeyID: 49733884
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcf593c568a8ecf1bd6791641affc4076672b250
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431797"
---
# <a name="create-or-modify-a-mobility-policy-in-lync-server-2013"></a><span data-ttu-id="ee867-103">在 Lync Server 2013 中创建或修改移动策略</span><span class="sxs-lookup"><span data-stu-id="ee867-103">Create or modify a mobility policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee867-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee867-104">

<span> </span></span></span>

<span data-ttu-id="ee867-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ee867-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ee867-106">你可以创建或修改移动策略，以允许移动用户将受支持的移动设备用于 Lync 功能，例如即时消息 (IM) 、状态和联系人。</span><span class="sxs-lookup"><span data-stu-id="ee867-106">You can create or modify mobility policy to allow mobile users to use supported mobile devices for Lync functionality such as instant messaging (IM), presence, and contacts.</span></span> <span data-ttu-id="ee867-107">可以从 Lync Server 2013 控制面板或 Lync Server 2013 管理外壳程序创建或修改移动策略</span><span class="sxs-lookup"><span data-stu-id="ee867-107">You can create or modify mobility policies from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell</span></span>

<div>

## <a name="to-create-a-mobility-policy-with-lync-server-control-panel"></a><span data-ttu-id="ee867-108">使用 Lync Server "控制面板" 创建移动策略</span><span class="sxs-lookup"><span data-stu-id="ee867-108">To create a mobility policy with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ee867-109">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="ee867-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ee867-110">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="ee867-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ee867-111">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="ee867-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ee867-112">在左侧导航栏中，单击 " **客户端**"，然后单击 " **移动策略** 导航" 按钮。</span><span class="sxs-lookup"><span data-stu-id="ee867-112">In the left navigation bar, click **Clients**, and then click the **Mobility Policy** navigation button.</span></span>

4.  <span data-ttu-id="ee867-113">在 " **移动策略** " 页面上，单击 " **新建**"，然后执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="ee867-113">On the **Mobility Policy** page, click **New**, and do one of the following:</span></span>
    
    1.  <span data-ttu-id="ee867-114">若要创建网站移动策略，请单击 " **网站策略**"，单击网站，单击 **"确定**"，查看默认设置，如果需要，可进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="ee867-114">To create a site mobility policy, click **Site policy**, click a site, click **OK**, review the default settings, and, if you want to, make any changes.</span></span>
    
    2.  <span data-ttu-id="ee867-115">若要创建用户移动策略，请单击 " **用户策略**"，键入名称，查看默认设置，如果需要，请进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="ee867-115">To create a user mobility policy, click **User policy**, type a name, review the default settings, and if you want to, make any changes.</span></span>

5.  <span data-ttu-id="ee867-116">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="ee867-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-mobility-policy-with-lync-server-control-panel"></a><span data-ttu-id="ee867-117">使用 Lync Server "控制面板" 修改移动策略</span><span class="sxs-lookup"><span data-stu-id="ee867-117">To modify a mobility policy with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ee867-118">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="ee867-118">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ee867-119">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="ee867-119">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ee867-120">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="ee867-120">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ee867-121">在左侧导航栏中，单击 " **客户端**"，然后单击 " **移动策略** 导航" 按钮。</span><span class="sxs-lookup"><span data-stu-id="ee867-121">In the left navigation bar, click **Clients**, and then click the **Mobility Policy** navigation button.</span></span>

4.  <span data-ttu-id="ee867-122">在 " **移动策略** " 页面上，单击现有移动策略之一。</span><span class="sxs-lookup"><span data-stu-id="ee867-122">On the **Mobility Policy** page, click one of the existing mobility policies.</span></span>

5.  <span data-ttu-id="ee867-123">在“编辑”菜单上，单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="ee867-123">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="ee867-124">编辑任何设置。</span><span class="sxs-lookup"><span data-stu-id="ee867-124">Edit any of the settings.</span></span>

7.  <span data-ttu-id="ee867-125">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="ee867-125">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-external-access-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ee867-126">使用 Windows PowerShell Cmdlet 创建外部访问策略</span><span class="sxs-lookup"><span data-stu-id="ee867-126">Creating External Access Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ee867-127">你可以使用 Windows PowerShell 和 **CsMobilityPolicy** cmdlet 在网站范围或每用户范围) 中创建移动策略 (。</span><span class="sxs-lookup"><span data-stu-id="ee867-127">You can create mobility policies (at the site scope or the per-user scope) by using Windows PowerShell and the **New-CsMobilityPolicy** cmdlet.</span></span> <span data-ttu-id="ee867-128">此外，你可以使用 **CsMobilityPolicy** cmdlet 修改你的任何现有策略，包括全局策略。</span><span class="sxs-lookup"><span data-stu-id="ee867-128">Additionally, you can use the **Set-CsMobilityPolicy** cmdlet to modify any of your existing policies, including the global policy.</span></span> <span data-ttu-id="ee867-129">这些 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="ee867-129">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ee867-130">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="ee867-130">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-mobility-policy-at-the-site-scope"></a><span data-ttu-id="ee867-131">在网站范围内创建移动策略</span><span class="sxs-lookup"><span data-stu-id="ee867-131">To create a mobility policy at the site scope</span></span>

  - <span data-ttu-id="ee867-132">此命令为 Redmond 网站创建新的移动策略：</span><span class="sxs-lookup"><span data-stu-id="ee867-132">This command creates a new mobility policy for the Redmond site:</span></span>
    
        New-CsMobilityPolicy -Identity "site:Redmond"
    
    <span data-ttu-id="ee867-133">由于在前面的命令中未指定必需的 Identity) 参数 (之外的任何参数，因此策略将对其所有属性使用默认值。</span><span class="sxs-lookup"><span data-stu-id="ee867-133">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the policies will use the default values for all its properties.</span></span>

</div>

<div>

## <a name="to-create-a-mobility-policy-at-the-per-user-scope"></a><span data-ttu-id="ee867-134">在每用户范围内创建移动策略</span><span class="sxs-lookup"><span data-stu-id="ee867-134">To create a mobility policy at the per-user scope</span></span>

  - <span data-ttu-id="ee867-135">若要在每用户范围内创建移动策略，请为策略指定唯一标识：</span><span class="sxs-lookup"><span data-stu-id="ee867-135">To create a mobility policy at the per-user scope, specify a unique Identity for the policy:</span></span>
    
        New-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-a-mobility-policy"></a><span data-ttu-id="ee867-136">创建移动策略时更改单个属性值</span><span class="sxs-lookup"><span data-stu-id="ee867-136">To change a single property value when creating a mobility policy</span></span>

  - <span data-ttu-id="ee867-137">若要创建使用不同属性值的策略，请包含相应的参数和参数值。</span><span class="sxs-lookup"><span data-stu-id="ee867-137">To create policies that use different property values, include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="ee867-138">例如，此命令将创建通过工作禁用呼叫的移动策略：</span><span class="sxs-lookup"><span data-stu-id="ee867-138">For example, this command creates mobility policy that disables Call via Work:</span></span>
    
        New-CsMobilityPolicy -Identity "site:Redmond" -EnableOutsideVoice $False

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-a-mobility-policy"></a><span data-ttu-id="ee867-139">创建移动策略时更改多个属性值</span><span class="sxs-lookup"><span data-stu-id="ee867-139">To change multiple property values when creating a mobility policy</span></span>

  - <span data-ttu-id="ee867-140">可以通过包含多个参数来修改多个属性值。</span><span class="sxs-lookup"><span data-stu-id="ee867-140">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="ee867-141">例如，此命令将创建一个策略，该策略通过工作禁用移动和呼叫：</span><span class="sxs-lookup"><span data-stu-id="ee867-141">For example, this command creates a policy that disables both mobility and Call via Work:</span></span>
    
        New-CsMobilityPolicy "site:Redmond" -EnableMobility $False -EnableOutsideVoice $False

</div>

<span data-ttu-id="ee867-142">有关详细信息，请参阅 [新的-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy) 和 [CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="ee867-142">For details, see the Help topic for the [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy) and the [Set-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy) cmdlets.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee867-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ee867-143">See Also</span></span>


[<span data-ttu-id="ee867-144">在 Lync Server 2013 中配置移动策略</span><span class="sxs-lookup"><span data-stu-id="ee867-144">Configuring mobility policy in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-policy.md)  
  

<span data-ttu-id="ee867-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee867-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

