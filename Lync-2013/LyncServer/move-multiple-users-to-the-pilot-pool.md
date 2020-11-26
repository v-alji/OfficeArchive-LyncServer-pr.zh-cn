---
title: 将多个用户移动到 "引导" 池
description: 将多个用户移动到 "引导" 池。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move multiple users to the pilot pool
ms:assetid: 90d0590c-922c-4933-b778-9dd850b59310
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205096(v=OCS.15)
ms:contentKeyID: 48184838
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 121509fbad863b0ce2d6cc9c7e9afaef360e2eb6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438480"
---
# <a name="move-multiple-users-to-the-pilot-pool"></a><span data-ttu-id="27cdc-103">将多个用户移动到 "引导" 池</span><span class="sxs-lookup"><span data-stu-id="27cdc-103">Move multiple users to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27cdc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27cdc-104">

<span> </span></span></span>

<span data-ttu-id="27cdc-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="27cdc-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="27cdc-106">您可以使用 Lync Server 2013 控制面板或 Lync Server 2013 命令行管理程序，将多个用户从 Lync Server 2010 池中移动到您的 Lync Server 2013 试验池。</span><span class="sxs-lookup"><span data-stu-id="27cdc-106">You can move multiple users from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="27cdc-107">使用 Lync Server 2013 "控制面板" 移动多个用户</span><span class="sxs-lookup"><span data-stu-id="27cdc-107">To move multiple users by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="27cdc-108">打开“Lync Server 控制面板”。</span><span class="sxs-lookup"><span data-stu-id="27cdc-108">Open **Lync Server Control Panel**.</span></span>

2.  <span data-ttu-id="27cdc-109">依次单击“用户”、“搜索”和“查找”。</span><span class="sxs-lookup"><span data-stu-id="27cdc-109">Click **Users**, click Search, and then click **Find**.</span></span>

3.  <span data-ttu-id="27cdc-110">选择要移动到 Lync Server 2013 池的两个用户。</span><span class="sxs-lookup"><span data-stu-id="27cdc-110">Select two users that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="27cdc-111">在此示例中，我们将用户移动 Chen's 的 Hansen 和 Claus。</span><span class="sxs-lookup"><span data-stu-id="27cdc-111">In this example, we will move users Chen Yang and Claus Hansen.</span></span>
    
    <span data-ttu-id="27cdc-112">![将用户移动到特定注册池](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "将用户移动到特定注册池")</span><span class="sxs-lookup"><span data-stu-id="27cdc-112">![Move users to specific register pool](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Move users to specific register pool")</span></span>  

4.  <span data-ttu-id="27cdc-113">从 " **操作** " 菜单中，选择 " **将所选用户移至池**"。</span><span class="sxs-lookup"><span data-stu-id="27cdc-113">From the **Action** menu, select **Move selected users to pool**.</span></span>

5.  <span data-ttu-id="27cdc-114">从下拉列表中，选择 "Lync Server 2013" 池。</span><span class="sxs-lookup"><span data-stu-id="27cdc-114">From the drop-down list, select the Lync Server 2013 pool.</span></span>

6.  <span data-ttu-id="27cdc-115">单击“操作”，然后单击“将所选用户移动到池”。</span><span class="sxs-lookup"><span data-stu-id="27cdc-115">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="27cdc-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="27cdc-116">Click OK.</span></span>
    
    <span data-ttu-id="27cdc-117">!["移动用户"、"目标注册机构池" 对话框](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png ""移动用户"、"目标注册机构池" 对话框")</span><span class="sxs-lookup"><span data-stu-id="27cdc-117">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

7.  <span data-ttu-id="27cdc-118">验证用户的 **注册池** 列现在是否包含 Lync Server 2013 池，这表示用户已成功移动。</span><span class="sxs-lookup"><span data-stu-id="27cdc-118">Verify that the **Registrar pool** column for the users now contains the Lync Server 2013 pool, which indicates that the users have been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="27cdc-119">使用 Lync Server 2013 命令行管理程序移动多个用户</span><span class="sxs-lookup"><span data-stu-id="27cdc-119">To move multiple users by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="27cdc-120">打开 Lync Server 2013 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="27cdc-120">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="27cdc-121">在命令行中，键入以下内容并将 **User1** 和用户2与要移动的特定 **用户名进行替换** ，并将 **池 \_ FQDN** 替换为目标池的名称。</span><span class="sxs-lookup"><span data-stu-id="27cdc-121">At the command line, type the following and replace **User1** and **User2** with specific user names you want to move and replace **pool\_FQDN** with the name of the destination pool.</span></span> <span data-ttu-id="27cdc-122">在此示例中，我们将在 Hao Chen's 和 Katie 约旦之间移动用户。</span><span class="sxs-lookup"><span data-stu-id="27cdc-122">In this example we will move users Hao Chen and Katie Jordan.</span></span>
    
        Get-CsUser -Filter {DisplayName -eq "User1" -or DisplayName - eq "User2"} | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="27cdc-123">![PowerShell Get-CsUser cmdlet 示例](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "PowerShell Get-CsUser cmdlet 示例")</span><span class="sxs-lookup"><span data-stu-id="27cdc-123">![Example of PowerShell Get-CsUser cmdlet](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Example of PowerShell Get-CsUser cmdlet")</span></span>  

3.  <span data-ttu-id="27cdc-124">在命令行中，键入以下内容</span><span class="sxs-lookup"><span data-stu-id="27cdc-124">At the command line, type the following</span></span>
    
        Get-CsUser -Identity "User1"

4.  <span data-ttu-id="27cdc-125">**注册机构池** 标识现在应指向您在上一步中指定为 **池 \_ FQDN** 的池。</span><span class="sxs-lookup"><span data-stu-id="27cdc-125">The **Registrar Pool** identity should now point to the pool you specified as **pool\_FQDN** in the previous step.</span></span> <span data-ttu-id="27cdc-126">此标识的存在可确认用户已成功移动。</span><span class="sxs-lookup"><span data-stu-id="27cdc-126">The presence of this identity confirms that the user has been successfully moved.</span></span> <span data-ttu-id="27cdc-127">重复步骤 **以验证服务2是否已** 移动。</span><span class="sxs-lookup"><span data-stu-id="27cdc-127">Repeat step to verify **User2** has been moved.</span></span>
    
    <span data-ttu-id="27cdc-128">![PowerShell Get-UsUser 身份 cmdlet 的输出](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "PowerShell Get-UsUser 身份 cmdlet 的输出")</span><span class="sxs-lookup"><span data-stu-id="27cdc-128">![Output of PowerShell Get-UsUser -Identity cmdlet](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Output of PowerShell Get-UsUser -Identity  cmdlet")</span></span>  

</div>

<div>

## <a name="to-move-all-users-at-the-same-time-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="27cdc-129">使用 Lync Server 2013 命令行管理程序同时移动所有用户</span><span class="sxs-lookup"><span data-stu-id="27cdc-129">To move all users at the same time by using the Lync Server 2013 Management Shell</span></span>

<span data-ttu-id="27cdc-130">在此示例中，所有用户都已返回到 Lync Server 2010 池 (pool01.contoso.net) 。</span><span class="sxs-lookup"><span data-stu-id="27cdc-130">In this example, all users have been returned to the Lync Server 2010 pool (pool01.contoso.net).</span></span> <span data-ttu-id="27cdc-131">使用 Lync Server 2013 命令行管理程序时，我们会同时将所有用户同时移动到 Lync Server 2013 池 (pool02.contoso.net) 。</span><span class="sxs-lookup"><span data-stu-id="27cdc-131">Using the Lync Server 2013 Management Shell, we will move all users at the same time to the Lync Server 2013 pool (pool02.contoso.net).</span></span>

1.  <span data-ttu-id="27cdc-132">打开 **Lync Server 2013 命令行管理** 程序。</span><span class="sxs-lookup"><span data-stu-id="27cdc-132">Open the **Lync Server 2013 Management Shell**.</span></span>

2.  <span data-ttu-id="27cdc-133">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="27cdc-133">At the command line, type the following:</span></span>
    
        Get-CsUser -OnLyncServer | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="27cdc-134">![PowerShell cmdlet 和结果在管理外壳程序中](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell cmdlet 和结果在管理外壳程序中")</span><span class="sxs-lookup"><span data-stu-id="27cdc-134">![PowerShell cmdlet and results in Management Shell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell cmdlet and results in Management Shell")</span></span>  

3.  <span data-ttu-id="27cdc-135">接下来，为一个试验用户运行 **move-csuser** 。</span><span class="sxs-lookup"><span data-stu-id="27cdc-135">Next, run **Get-CsUser** for one of the pilot users.</span></span>
    
        Get-CsUser -Identity "Hao Chen"

4.  <span data-ttu-id="27cdc-136">每个用户的 **注册池** 标识现在指向您 \_ 在上一步中指定为 "池 FQDN" 的池。</span><span class="sxs-lookup"><span data-stu-id="27cdc-136">The **Registrar Pool** identity for each user now points to the pool you specified as “pool\_FQDN” in the previous step.</span></span> <span data-ttu-id="27cdc-137">此标识的存在可确认用户已成功移动。</span><span class="sxs-lookup"><span data-stu-id="27cdc-137">The presence of this identity confirms that the user has been successfully moved.</span></span>

5.  <span data-ttu-id="27cdc-138">此外，我们还可以查看 Lync Server 2013 控制面板中的用户列表，并验证注册机构池值是否现在指向 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="27cdc-138">Additionally, we can view the list of users in the Lync Server 2013 Control Panel and verify that the Registrar Pool value now points to the Lync Server 2013 pool.</span></span>
    
    <span data-ttu-id="27cdc-139">![Lync Server 2013 控制面板用户列表](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 控制面板用户列表")</span><span class="sxs-lookup"><span data-stu-id="27cdc-139">![Lync Server 2013 Control Panel user list](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 Control Panel user list")</span></span>  

<span data-ttu-id="27cdc-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27cdc-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

