---
title: Lync Server 2013：删除现有网络区域路由
description: Lync Server 2013：删除现有网络区域路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network region routes
ms:assetid: 6256ff80-5f1e-48b4-928b-24aeb3c1a0e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688074(v=OCS.15)
ms:contentKeyID: 49733669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2501dc3f4ed88a56e9f591e3af11a673046280a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430334"
---
# <a name="deleting-existing-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="5335e-103">删除 Lync Server 2013 中的现有网络区域路由</span><span class="sxs-lookup"><span data-stu-id="5335e-103">Deleting existing network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5335e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5335e-104">

<span> </span></span></span>

<span data-ttu-id="5335e-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5335e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5335e-106">呼叫许可控制中的每个地区 (CAC) 配置都必须具有某种方式才能访问其他每个区域。</span><span class="sxs-lookup"><span data-stu-id="5335e-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="5335e-107">虽然区域链接为区域之间的连接设置带宽限制，同时也表示物理链接，但路由决定了连接从一个地区到另一个地区的链接路径。</span><span class="sxs-lookup"><span data-stu-id="5335e-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="5335e-108">您可以使用 Lync Server "控制面板" 配置网络区域路由。</span><span class="sxs-lookup"><span data-stu-id="5335e-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="5335e-109">从 Lync Server 控制面板中，你可以创建、修改或删除网络区域路由。</span><span class="sxs-lookup"><span data-stu-id="5335e-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="5335e-110">使用本主题删除现有网络区域路由。</span><span class="sxs-lookup"><span data-stu-id="5335e-110">Use this topic to delete existing network region routes.</span></span> <span data-ttu-id="5335e-111">有关创建或修改网络区域路由的详细信息，请参阅 [在 Lync Server 2013 中创建或修改网络区域路由](lync-server-2013-creating-or-modifying-network-region-routes.md)。</span><span class="sxs-lookup"><span data-stu-id="5335e-111">For details about creating or modifying network region routes, see [Creating or modifying network region routes in Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span></span>

<div>

## <a name="to-delete-a-network-region-route"></a><span data-ttu-id="5335e-112">删除网络区域路由</span><span class="sxs-lookup"><span data-stu-id="5335e-112">To delete a network region route</span></span>

1.  <span data-ttu-id="5335e-113">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="5335e-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5335e-114">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="5335e-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5335e-115">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="5335e-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5335e-116">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **区域路由**"。</span><span class="sxs-lookup"><span data-stu-id="5335e-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="5335e-117">在 " **区域路由** " 页面上，单击要删除的区域路由。</span><span class="sxs-lookup"><span data-stu-id="5335e-117">On the **Region Route** page, click the region route that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5335e-118">您可以一次删除多个区域路线。</span><span class="sxs-lookup"><span data-stu-id="5335e-118">You can delete more than one region route at a time.</span></span> <span data-ttu-id="5335e-119">若要执行此操作，请在按住 CTRL 键的同时按 CTRL 并选择多个区域路由。</span><span class="sxs-lookup"><span data-stu-id="5335e-119">To do this, press CTRL and select multiple region routes while holding down the CTRL key.</span></span> <span data-ttu-id="5335e-120">或者，若要选择所有区域路由，请单击 "<STRONG>编辑</STRONG>" 菜单上的 "<STRONG>全选</STRONG>"。</span><span class="sxs-lookup"><span data-stu-id="5335e-120">Or, to select all region routes, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="5335e-121">在 " **编辑** " 菜单上，单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="5335e-121">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="5335e-122">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="5335e-122">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5335e-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5335e-123">See Also</span></span>


[<span data-ttu-id="5335e-124">在 Lync Server 2013 中创建或修改网络区域路由</span><span class="sxs-lookup"><span data-stu-id="5335e-124">Creating or modifying network region routes in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-region-routes.md)  


<span data-ttu-id="5335e-125">[配置网络区域路由](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="5335e-125">[Configure a Network Region Route](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span></span>  


[<span data-ttu-id="5335e-126">New-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="5335e-126">New-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterRegionRoute)  
[<span data-ttu-id="5335e-127">Set-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="5335e-127">Set-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterRegionRoute)  
[<span data-ttu-id="5335e-128">Remove-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="5335e-128">Remove-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterRegionRoute)  
[<span data-ttu-id="5335e-129">Get-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="5335e-129">Get-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute)  
  

<span data-ttu-id="5335e-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5335e-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

