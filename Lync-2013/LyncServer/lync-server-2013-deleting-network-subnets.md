---
title: Lync Server 2013：删除网络子网
description: Lync Server 2013：删除网络子网。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network subnets
ms:assetid: c1850f38-40a3-48c9-b6f1-f181c5e63b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721873(v=OCS.15)
ms:contentKeyID: 49733806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6635ec99b68c4ceb10d1cda343fef35c951bf152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430278"
---
# <a name="deleting-network-subnets-in-lync-server-2013"></a><span data-ttu-id="0a0c7-103">在 Lync Server 2013 中删除网络子网</span><span class="sxs-lookup"><span data-stu-id="0a0c7-103">Deleting network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a0c7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a0c7-104">

<span> </span></span></span>

<span data-ttu-id="0a0c7-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0a0c7-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0a0c7-106">可以使用以下过程删除子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-106">You can use the following procedure to delete a subnet.</span></span> <span data-ttu-id="0a0c7-107">从 Lync Server 控制面板中，您可以创建、修改或删除网络子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="0a0c7-108">有关创建或修改网络子网的详细信息，请参阅 [在 Lync Server 2013 中创建或修改网络子网](lync-server-2013-create-or-modify-network-subnets.md)。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-108">For details on creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<span data-ttu-id="0a0c7-109">在大多数部署 Microsoft Lync Server 2013 的情况下，呼叫许可控制 (CAC) 已实施，通常会有大量子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-109">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="0a0c7-110">因此，通常最好从 Lync Server 命令行管理程序中配置子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-110">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="0a0c7-111">从这里，你可以将 CsNetworkSubnet 与 Windows PowerShell cmdlet **Import-CSV** 结合在一起调用 **新的**。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-111">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="0a0c7-112">通过将这些 cmdlet 结合使用，你可以从逗号分隔的值中读取子网设置 ( .csv) 文件，并同时创建多个子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-112">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="0a0c7-113">有关如何从 .csv 文件创建子网的示例，请参阅 [CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-113">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-delete-a-network-subnet"></a><span data-ttu-id="0a0c7-114">删除网络子网</span><span class="sxs-lookup"><span data-stu-id="0a0c7-114">To delete a network subnet</span></span>

1.  <span data-ttu-id="0a0c7-115">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0a0c7-116">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0a0c7-117">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0a0c7-118">在左侧导航栏中，单击 " **网络配置** "，然后单击 " **子网**"。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-118">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="0a0c7-119">在 " **子网** " 页面上，单击要删除的子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-119">On the **Subnet** page, click the subnet that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0a0c7-120">您可以一次删除多个子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-120">You can delete more than one subnet at a time.</span></span> <span data-ttu-id="0a0c7-121">若要执行此操作，请在按住 CTRL 键的同时按 CTRL 并选择多个子网。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-121">To do this, press CTRL and select multiple subnets while holding down the CTRL key.</span></span> <span data-ttu-id="0a0c7-122">或者，若要选择所有子网，请单击 "<STRONG>编辑</STRONG>" 菜单上的 "<STRONG>全选</STRONG>"。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-122">Or, to select all subnets, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="0a0c7-123">在 " **编辑** " 菜单上，单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="0a0c7-124">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="0a0c7-124">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0a0c7-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a0c7-125">See Also</span></span>


[<span data-ttu-id="0a0c7-126">在 Lync Server 2013 中创建或修改网络子网</span><span class="sxs-lookup"><span data-stu-id="0a0c7-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
  

<span data-ttu-id="0a0c7-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a0c7-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

