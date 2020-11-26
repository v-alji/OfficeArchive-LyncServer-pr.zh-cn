---
title: Lync Server 2013：查看网络网站信息
description: Lync Server 2013：查看网络网站信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network site information
ms:assetid: 24a97d98-b168-4016-81bf-c2c478092b87
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687996(v=OCS.15)
ms:contentKeyID: 49733586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b46dc91510cb5ff737977871470033374573ba8c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440400"
---
# <a name="viewing-network-site-information-in-lync-server-2013"></a><span data-ttu-id="d2cfa-103">在 Lync Server 2013 中查看网络站点信息</span><span class="sxs-lookup"><span data-stu-id="d2cfa-103">Viewing network site information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2cfa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2cfa-104">

<span> </span></span></span>

<span data-ttu-id="d2cfa-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="d2cfa-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="d2cfa-106">网络站点是在呼叫许可控制的每个区域内配置的办公室或位置 (CAC) 或增强的9-1-1 部署。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="d2cfa-107">可以在 Lync Server 2013 控制面板或 Lync Server 命令行管理程序中查看网络网站信息。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-107">You can view network site information in either Lync Server 2013 Control Panel or Lync Server Management Shell .</span></span> <span data-ttu-id="d2cfa-108">有关创建或修改网络站点的详细信息，请参阅 [在 Lync Server 2013 中创建或修改网络站点](lync-server-2013-creating-or-modifying-network-sites.md)。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-108">For details about creating or modifying network sites, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

<div>

## <a name="to-view-network-site-information-in-lync-server-control-panel"></a><span data-ttu-id="d2cfa-109">在 Lync Server "控制面板" 中查看网络站点信息</span><span class="sxs-lookup"><span data-stu-id="d2cfa-109">To view network site information in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="d2cfa-110">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d2cfa-111">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d2cfa-112">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d2cfa-113">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **网站**"。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-113">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="d2cfa-114">在 " **网站** " 页面上，单击要查看的网站。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-114">On the **Site** page, click the site that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d2cfa-115">您一次只能查看一个网站的信息。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-115">You can only view information for one site at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="d2cfa-116">在“编辑”菜单上，单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-116">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-site-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d2cfa-117">使用 Windows PowerShell Cmdlet 查看网络网站信息</span><span class="sxs-lookup"><span data-stu-id="d2cfa-117">Viewing Network Site Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d2cfa-118">你可以使用 Windows PowerShell 和 Get-CsNetworkSite cmdlet 查看网络网站信息。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-118">You can view network site information by using Windows PowerShell and the Get-CsNetworkSite cmdlet.</span></span> <span data-ttu-id="d2cfa-119">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d2cfa-120">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-site-information"></a><span data-ttu-id="d2cfa-121">查看网络站点信息</span><span class="sxs-lookup"><span data-stu-id="d2cfa-121">To view network site information</span></span>

  - <span data-ttu-id="d2cfa-122">若要查看有关所有网络网站的信息，请在 Lync Server 命令行管理程序中键入以下命令，然后按 ENTER：</span><span class="sxs-lookup"><span data-stu-id="d2cfa-122">To view information about all your network sites, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSite
    
    <span data-ttu-id="d2cfa-123">这将返回与以下类似的信息：</span><span class="sxs-lookup"><span data-stu-id="d2cfa-123">That will return information similar to this:</span></span>
    
        Identity          : Redmond
        NetworkSiteID     : Redmond
        Description       :
        NetworkRegionID   : Pacific Northwest
        BypassID          : 3b232b84-2c1d-4da2-8181-e9330bafebe9
        BWPolicyProfileID :
        LocationPolicy    :

</div>

<span data-ttu-id="d2cfa-124">有关详细信息，请参阅 [CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="d2cfa-124">For more information, see the help topic for the [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d2cfa-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2cfa-125">See Also</span></span>


[<span data-ttu-id="d2cfa-126">在 Lync Server 2013 中创建或修改网络站点</span><span class="sxs-lookup"><span data-stu-id="d2cfa-126">Creating or modifying network sites in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-sites.md)  
[<span data-ttu-id="d2cfa-127">在 Lync Server 2013 中删除现有网络网站</span><span class="sxs-lookup"><span data-stu-id="d2cfa-127">Deleting an existing network site in Lync Server 2013</span></span>](lync-server-2013-deleting-an-existing-network-site.md)  
  

<span data-ttu-id="d2cfa-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2cfa-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

