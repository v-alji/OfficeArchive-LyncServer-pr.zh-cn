---
title: Lync Server 2013：查看网络子网信息
description: Lync Server 2013：查看网络子网信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network subnet information
ms:assetid: 46f165f2-efe3-4cc1-9fee-a78b7f2ed41e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688044(v=OCS.15)
ms:contentKeyID: 49733636
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 313135c43318817391d54f2fa3e73dd318f7a11f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438853"
---
# <a name="viewing-network-subnet-information-in-lync-server-2013"></a><span data-ttu-id="ba2bf-103">在 Lync Server 2013 中查看网络子网信息</span><span class="sxs-lookup"><span data-stu-id="ba2bf-103">Viewing network subnet information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba2bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba2bf-104">

<span> </span></span></span>

<span data-ttu-id="ba2bf-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ba2bf-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ba2bf-106">你可以使用以下过程查看网络子网。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-106">You can use the following procedure to view a network subnet.</span></span> <span data-ttu-id="ba2bf-107">从 Lync Server 控制面板中，您可以创建、修改或删除网络子网。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="ba2bf-108">有关创建或修改网络子网的详细信息，请参阅 [在 Lync Server 2013 中创建或修改网络子网](lync-server-2013-create-or-modify-network-subnets.md)。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-108">For details about creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<div>

## <a name="to-view-a-network-subnet"></a><span data-ttu-id="ba2bf-109">查看网络子网</span><span class="sxs-lookup"><span data-stu-id="ba2bf-109">To view a network subnet</span></span>

1.  <span data-ttu-id="ba2bf-110">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ba2bf-111">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ba2bf-112">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ba2bf-113">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **子网**"。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-113">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="ba2bf-114">在 " **子网** " 页面上，单击要查看的子网。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-114">On the **Subnet** page, click the subnet that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ba2bf-115">一次只能查看一个子网。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-115">You can only view one subnet at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="ba2bf-116">在 " **编辑** " 菜单上，单击 " **显示详细信息 ...**"。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-116">On the **Edit** menu, click **Show details…**.</span></span>

</div>

<div>

## <a name="viewing-network-subnet-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ba2bf-117">使用 Windows PowerShell Cmdlet 查看网络子网配置信息</span><span class="sxs-lookup"><span data-stu-id="ba2bf-117">Viewing Network Subnet Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ba2bf-118">可以使用 Windows PowerShell 和 Get-CsNetworkSubnet cmdlet 查看网络子网信息。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-118">Network subnet information can be viewed by using Windows PowerShell and the Get-CsNetworkSubnet cmdlet.</span></span> <span data-ttu-id="ba2bf-119">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ba2bf-120">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-subnet-information"></a><span data-ttu-id="ba2bf-121">查看网络子网信息</span><span class="sxs-lookup"><span data-stu-id="ba2bf-121">To view network subnet information</span></span>

  - <span data-ttu-id="ba2bf-122">若要查看有关所有网络子网的信息，请在 Lync Server 命令行管理程序中键入以下命令，然后按 ENTER：</span><span class="sxs-lookup"><span data-stu-id="ba2bf-122">To view information about all your network subnets, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSubnet
    
    <span data-ttu-id="ba2bf-123">这将返回与以下类似的信息：</span><span class="sxs-lookup"><span data-stu-id="ba2bf-123">That will return information similar to this:</span></span>
    
        Identity      : 172.11.15.0
        MaskBits      : 28
        Description   :
        NetworkSiteID : Redmond
        SubnetID      : 172.11.15.0

</div>

<span data-ttu-id="ba2bf-124">有关详细信息，请参阅 [CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="ba2bf-124">For more information, see the help topic for the [Get-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ba2bf-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba2bf-125">See Also</span></span>


[<span data-ttu-id="ba2bf-126">在 Lync Server 2013 中创建或修改网络子网</span><span class="sxs-lookup"><span data-stu-id="ba2bf-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
[<span data-ttu-id="ba2bf-127">在 Lync Server 2013 中删除网络子网</span><span class="sxs-lookup"><span data-stu-id="ba2bf-127">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  
  

<span data-ttu-id="ba2bf-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba2bf-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

