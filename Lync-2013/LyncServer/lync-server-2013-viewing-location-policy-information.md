---
title: Lync Server 2013：查看位置策略信息
description: Lync Server 2013：查看位置策略信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing location policy information
ms:assetid: 14e41bcb-ea0a-49c2-99b3-1f61fc34416d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520954(v=OCS.15)
ms:contentKeyID: 48183489
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fecc5de5fb71014a1641038e9e09afba0e90cdb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443956"
---
# <a name="viewing-location-policy-information-in-lync-server-2013"></a><span data-ttu-id="80dd4-103">在 Lync Server 2013 中查看位置策略信息</span><span class="sxs-lookup"><span data-stu-id="80dd4-103">Viewing location policy information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80dd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80dd4-104">

<span> </span></span></span>

<span data-ttu-id="80dd4-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="80dd4-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="80dd4-106">在 Lync Server 2013 中，你可以使用位置策略应用与增强的 9-1-1 (E9) 功能以及用户或联系人的位置设置相关的设置。</span><span class="sxs-lookup"><span data-stu-id="80dd4-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="80dd4-107">位置策略确定用户是否启用了 E9-1，如果是紧急呼叫，该行为是什么。</span><span class="sxs-lookup"><span data-stu-id="80dd4-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="80dd4-108">例如，您可以使用位置策略定义 (紧急呼叫的号码，例如，911在美国) 、公司安全是否应自动通知以及如何路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="80dd4-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="80dd4-109">你可以从 Lync Server 2013 控制面板中的 " **网络配置** " 组配置位置策略。</span><span class="sxs-lookup"><span data-stu-id="80dd4-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="80dd4-110">从 Lync Server 控制面板，您可以查看、创建、修改或删除位置策略。</span><span class="sxs-lookup"><span data-stu-id="80dd4-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="80dd4-111">使用以下过程查看有关位置策略的信息。</span><span class="sxs-lookup"><span data-stu-id="80dd4-111">Use the following procedure to view information about location policies.</span></span> <span data-ttu-id="80dd4-112">有关创建或修改位置策略的详细信息，请参阅 [在 Lync Server 2013 中创建或修改位置策略](lync-server-2013-creating-or-modifying-a-location-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="80dd4-112">For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span></span>

<div>

## <a name="to-view-information-about-a-location-policy"></a><span data-ttu-id="80dd4-113">查看有关位置策略的信息</span><span class="sxs-lookup"><span data-stu-id="80dd4-113">To view information about a location policy</span></span>

1.  <span data-ttu-id="80dd4-114">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="80dd4-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="80dd4-115">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="80dd4-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="80dd4-116">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="80dd4-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="80dd4-117">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **位置策略**"。</span><span class="sxs-lookup"><span data-stu-id="80dd4-117">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="80dd4-118">在 " **位置策略** " 页面上，选择要修改的位置策略。</span><span class="sxs-lookup"><span data-stu-id="80dd4-118">On the **Location Policy** page, select the location policy that you want to modify.</span></span>

5.  <span data-ttu-id="80dd4-119">在“编辑”菜单上，单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="80dd4-119">On the **Edit** menu, click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="80dd4-120">一次只能查看一个位置策略的相关信息。</span><span class="sxs-lookup"><span data-stu-id="80dd4-120">You can only view information about one location policy at a time.</span></span>

    
    </div>

<span data-ttu-id="80dd4-121">默认情况下存在一个名为 Global 的策略，不能删除或重命名。</span><span class="sxs-lookup"><span data-stu-id="80dd4-121">A single policy, called Global, exists by default and cannot be deleted or renamed.</span></span> <span data-ttu-id="80dd4-122">但是，你可以修改全局策略。</span><span class="sxs-lookup"><span data-stu-id="80dd4-122">However, you can modify the Global policy.</span></span> <span data-ttu-id="80dd4-123">此政策将应用于所有用户和联系人，除非你创建网站策略或每用户策略。</span><span class="sxs-lookup"><span data-stu-id="80dd4-123">This policy will apply to all users and contacts, unless you create site policies or per-user policies.</span></span> <span data-ttu-id="80dd4-124">每用户策略必须应用于特定用户。</span><span class="sxs-lookup"><span data-stu-id="80dd4-124">Per-user policies must be applied to specific users.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="80dd4-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80dd4-125">See Also</span></span>


[<span data-ttu-id="80dd4-126">在 Lync Server 2013 中创建或修改位置策略</span><span class="sxs-lookup"><span data-stu-id="80dd4-126">Creating or modifying a location policy in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[<span data-ttu-id="80dd4-127">在 Lync Server 2013 中创建位置策略</span><span class="sxs-lookup"><span data-stu-id="80dd4-127">Create location policies in Lync Server 2013</span></span>](lync-server-2013-create-location-policies.md)  
[<span data-ttu-id="80dd4-128">在 Lync Server 2013 中创建或修改网络站点</span><span class="sxs-lookup"><span data-stu-id="80dd4-128">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)  


[<span data-ttu-id="80dd4-129">新-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="80dd4-129">New-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy)  
[<span data-ttu-id="80dd4-130">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="80dd4-130">Set-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy)  
[<span data-ttu-id="80dd4-131">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="80dd4-131">Remove-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsLocationPolicy)  
[<span data-ttu-id="80dd4-132">CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="80dd4-132">Get-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsLocationPolicy)  
  

<span data-ttu-id="80dd4-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80dd4-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

