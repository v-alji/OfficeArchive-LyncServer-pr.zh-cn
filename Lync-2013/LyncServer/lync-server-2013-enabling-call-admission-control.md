---
title: Lync Server 2013：启用呼叫许可控制
description: Lync Server 2013：启用呼叫许可控制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling call admission control
ms:assetid: 015f5c8f-2f90-4b9e-8149-b33767e90582
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520942(v=OCS.15)
ms:contentKeyID: 48183228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f5737f83a1965b920f2a23e1aabbbaec2af7b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392200"
---
# <a name="enabling-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="42044-103">在 Lync Server 2013 中启用呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="42044-103">Enabling call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42044-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42044-104">

<span> </span></span></span>

<span data-ttu-id="42044-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="42044-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="42044-106">呼叫允许控制 (CAC) 是区域、站点和子网的网络，通过它可基于可用带宽对音频和视频传输设置限制。</span><span class="sxs-lookup"><span data-stu-id="42044-106">Call admission control (CAC) is a network of regions, sites, and subnets that enable you to place restrictions on audio and video transmissions based on available bandwidth.</span></span> <span data-ttu-id="42044-107">配置 CAC 网络后，必须启用 CAC 才能强制实施带宽限制。</span><span class="sxs-lookup"><span data-stu-id="42044-107">After you configure the CAC network, you must enable CAC to enforce the bandwidth limitations.</span></span> <span data-ttu-id="42044-108">您可以使用 Lync Server "控制面板" 执行此操作。</span><span class="sxs-lookup"><span data-stu-id="42044-108">You can use Lync Server Control Panel to do this.</span></span>

<div>

## <a name="to-enable-cac-from-lync-server-control-panel"></a><span data-ttu-id="42044-109">从 Lync Server "控制面板" 中启用 CAC</span><span class="sxs-lookup"><span data-stu-id="42044-109">To enable CAC from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="42044-110">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="42044-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="42044-111">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="42044-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="42044-112">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="42044-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="42044-113">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **全局**"。</span><span class="sxs-lookup"><span data-stu-id="42044-113">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="42044-114">在 " **全局** " 页面上，单击 " **全局** 配置"。</span><span class="sxs-lookup"><span data-stu-id="42044-114">On the **Global** page, click the **Global** configuration.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="42044-115">只能为任何 Microsoft Lync Server 2013 部署配置一个网络，因此列表中永远不会有多个网络配置。</span><span class="sxs-lookup"><span data-stu-id="42044-115">Only one network can be configured for any Microsoft Lync Server 2013 deployment, so there will never be more than one network configuration in the list.</span></span> <span data-ttu-id="42044-116">不能重命名全局配置。</span><span class="sxs-lookup"><span data-stu-id="42044-116">You cannot rename the Global configuration.</span></span>

    
    </div>

5.  <span data-ttu-id="42044-117">在“编辑”菜单上，单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="42044-117">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="42044-118">在 " **编辑全局设置** " 页面上，选中 " **启用呼叫许可控制** " 复选框，然后单击 " **提交**"。</span><span class="sxs-lookup"><span data-stu-id="42044-118">On the **Edit Global Setting** page, select the **Enable call admission control** check box, and then click **Commit**.</span></span>

<span data-ttu-id="42044-119">单击 " **提交**" 时，将运行配置测试。</span><span class="sxs-lookup"><span data-stu-id="42044-119">When you click **Commit**, you run a test of the configuration.</span></span> <span data-ttu-id="42044-120">" **编辑全局设置** " 对话框将关闭，返回到 **全局** 页。</span><span class="sxs-lookup"><span data-stu-id="42044-120">The **Edit Global Settings** dialog box closes, returning you to the **Global** page.</span></span> <span data-ttu-id="42044-121">如果你的网络配置中发现了任何错误或不一致会阻止其正常工作的情况下，你将收到警告 (例如，如果每个区域未通过 interregion 路由) 连接到其他任何区域。</span><span class="sxs-lookup"><span data-stu-id="42044-121">You will receive a warning if any errors or inconsistencies are discovered in your network configuration that will prevent it from working correctly (for example, if every region is not connected to every other region through an interregion route).</span></span>

<span data-ttu-id="42044-122">如果你对网络配置进行了更改，则可以通过打开全局配置并单击 " **提交**" 来再次运行验证检查。</span><span class="sxs-lookup"><span data-stu-id="42044-122">If you make changes to your network configuration, you can run the validation check again by opening the Global configuration and clicking **Commit**.</span></span> <span data-ttu-id="42044-123">无需首先禁用 CAC：选中复选框，然后单击 " **提交**"。</span><span class="sxs-lookup"><span data-stu-id="42044-123">You do not need to disable CAC first: leave the check box checked and click **Commit**.</span></span> <span data-ttu-id="42044-124">您可以随时执行此操作，而无需进行任何配置更改。</span><span class="sxs-lookup"><span data-stu-id="42044-124">You can do this at any time without making any configuration changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="42044-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42044-125">See Also</span></span>


[<span data-ttu-id="42044-126">Lync Server 2013 中的呼叫许可控制概述</span><span class="sxs-lookup"><span data-stu-id="42044-126">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)  


[<span data-ttu-id="42044-127">在 Lync Server 2013 中规划呼叫允许控制</span><span class="sxs-lookup"><span data-stu-id="42044-127">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)  
[<span data-ttu-id="42044-128">在 Lync Server 2013 中配置呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="42044-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="42044-129">Set-csnetworkconfiguration</span><span class="sxs-lookup"><span data-stu-id="42044-129">Get-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkConfiguration)  
[<span data-ttu-id="42044-130">Set-Set-csnetworkconfiguration</span><span class="sxs-lookup"><span data-stu-id="42044-130">Set-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkConfiguration)  
[<span data-ttu-id="42044-131">Remove-Set-csnetworkconfiguration</span><span class="sxs-lookup"><span data-stu-id="42044-131">Remove-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkConfiguration)  
  

<span data-ttu-id="42044-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42044-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

