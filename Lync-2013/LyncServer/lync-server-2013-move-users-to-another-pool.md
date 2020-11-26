---
title: Lync Server 2013：将用户移动到另一个池
description: Lync Server 2013：将用户移动到另一个池。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move users to another pool
ms:assetid: e7b4968c-0e9d-4d56-b5f1-9edf0f7206f8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182600(v=OCS.15)
ms:contentKeyID: 48185879
ms.date: 02/09/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 21012e0df7567a79bca018d194878c85b8653ae4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425281"
---
# <a name="move-users-to-another-pool-in-lync-server-2013"></a><span data-ttu-id="8e09d-103">在 Lync Server 2013 中将用户移动到另一个池中</span><span class="sxs-lookup"><span data-stu-id="8e09d-103">Move users to another pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e09d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e09d-104">

<span> </span></span></span>

<span data-ttu-id="8e09d-105">_**主题上次修改时间：** 2018-02-09_</span><span class="sxs-lookup"><span data-stu-id="8e09d-105">_**Topic Last Modified:** 2018-02-09_</span></span>

<span data-ttu-id="8e09d-106">可以使用 Lync Server 控制面板将用户分配到特定的服务器或池。</span><span class="sxs-lookup"><span data-stu-id="8e09d-106">You can use Lync Server Control Panel to assign users to a specific server or pool.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="8e09d-107">将所有现有用户从运行 Lync Server 2010 或更早版本的源池中移动到复杂的 Active Directory 环境中的 Lync Server 2013 目标池可能会导致 Active Directory 复制速度较慢。</span><span class="sxs-lookup"><span data-stu-id="8e09d-107">Moving all existing users from a source pool that is running Lync Server 2010 or earlier to a Lync Server 2013 destination pool in a complex Active Directory environment might result in slower Active Directory replication.</span></span> <span data-ttu-id="8e09d-108">为避免这种情况，您可以使用搜索筛选器从运行 Lync Server 2010 或更早版本的池中移动用户，也可以使用 Lync Server Management Shell 将用户与 cmdlet 一起移动。</span><span class="sxs-lookup"><span data-stu-id="8e09d-108">To avoid this, you can use search filters to move users from pools that are running Lync Server 2010 or earlier separately, or you can use Lync Server Management Shell to move users with cmdlets.</span></span> <span data-ttu-id="8e09d-109">此外，筛选器功能适用于 Lync Server 2013 用户。</span><span class="sxs-lookup"><span data-stu-id="8e09d-109">Also, the filter functionality works with Lync Server 2013 users.</span></span>



</div>

<div>

## <a name="to-move-selected-users-to-a-different-server-or-pool"></a><span data-ttu-id="8e09d-110">将所选用户移动到其他服务器或池</span><span class="sxs-lookup"><span data-stu-id="8e09d-110">To move selected users to a different server or pool</span></span>

1.  <span data-ttu-id="8e09d-111">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="8e09d-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8e09d-112">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8e09d-113">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="8e09d-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8e09d-114">在左导航栏中，单击“用户”。</span><span class="sxs-lookup"><span data-stu-id="8e09d-114">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="8e09d-115">在 " **搜索用户** " 框中，键入显示名称、名字、姓氏、安全帐户管理器的全部或第一部分 (SAM) 帐户名、SIP 地址或行统一资源标识符 (URI) 所需的用户帐户，然后单击 " **查找**"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-115">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want, and then click **Find**.</span></span>

5.  <span data-ttu-id="8e09d-116">在表中，选择列表中的特定用户或用户。</span><span class="sxs-lookup"><span data-stu-id="8e09d-116">In the table, select a specific user or users in the list.</span></span>

6.  <span data-ttu-id="8e09d-117">在 " **操作** " 菜单上，单击 " **将所选用户移至池**"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-117">On the **Action** menu, click **Move selected users to pool**.</span></span>

7.  <span data-ttu-id="8e09d-118">在 " **移动用户**" 中，选择要将用户移动到 " **目标注册机构" 池中** 的池。</span><span class="sxs-lookup"><span data-stu-id="8e09d-118">In **Move Users**, select the pool that you want to move the users to in **Destination registrar pool**.</span></span>

8.  <span data-ttu-id="8e09d-119"> (可选) 如果目标服务器或池不可用，请选中 " **强制** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="8e09d-119">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="8e09d-120">如果您选择 " <STRONG>强制</STRONG>"，则用户帐户将被移动，但相关联的用户数据（如计划的会议和联系人）不会移动。</span><span class="sxs-lookup"><span data-stu-id="8e09d-120">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-all-users-from-one-server-or-pool-to-a-different-server-or-pool"></a><span data-ttu-id="8e09d-121">将所有用户从一个服务器或池移动到另一个服务器或池</span><span class="sxs-lookup"><span data-stu-id="8e09d-121">To move all users from one server or pool to a different server or pool</span></span>

1.  <span data-ttu-id="8e09d-122">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="8e09d-122">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8e09d-123">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-123">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8e09d-124">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="8e09d-124">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8e09d-125">在左导航栏中，单击“用户”。</span><span class="sxs-lookup"><span data-stu-id="8e09d-125">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="8e09d-126">在 " **操作** " 菜单上，单击 " **将所有用户移至池**"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-126">On the **Action** menu, click **Move all users to pool**.</span></span>

5.  <span data-ttu-id="8e09d-127">在 " **移动用户**" 中，选择包含要在 **源注册机构池中** 移动的用户帐户的池。</span><span class="sxs-lookup"><span data-stu-id="8e09d-127">In **Move Users**, select the pool that contains the user accounts that you want to move in **Source registrar pool**.</span></span>

6.  <span data-ttu-id="8e09d-128">在 " **目标注册机构" 池中**，选择要将用户移动到的池。</span><span class="sxs-lookup"><span data-stu-id="8e09d-128">In **Destination registrar pool**, select the pool that you want to move the users to.</span></span>

7.  <span data-ttu-id="8e09d-129"> (可选) 如果目标服务器或池不可用，请选中 " **强制** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="8e09d-129">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="8e09d-130">如果您选择 " <STRONG>强制</STRONG>"，则用户帐户将被移动，但相关联的用户数据（如计划的会议和联系人）不会移动。</span><span class="sxs-lookup"><span data-stu-id="8e09d-130">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-users-from-one-pool-to-a-different-pool-by-using-a-filter"></a><span data-ttu-id="8e09d-131">使用筛选器将用户从一个池移动到另一个池</span><span class="sxs-lookup"><span data-stu-id="8e09d-131">To move users from one pool to a different pool by using a filter</span></span>

1.  <span data-ttu-id="8e09d-132">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="8e09d-132">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8e09d-133">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-133">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8e09d-134">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="8e09d-134">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8e09d-135">在左导航栏中，单击“用户”。</span><span class="sxs-lookup"><span data-stu-id="8e09d-135">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="8e09d-136">在 " **用户搜索**" 中，单击 " **搜索**"，然后单击 " **添加筛选器**"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-136">In **User Search**, click **Search**, and then click **Add Filter**.</span></span>

5.  <span data-ttu-id="8e09d-137">在搜索条件中，选择 " **注册机构池**"，选择 " **等于**"，选择 " **当前池 FQDN**"，然后单击 " **查找**"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-137">In the Search criteria, select **Registrar Pool**, select **Equal to**, select **Current Pool FQDN**, and then click **Find**.</span></span>

6.  <span data-ttu-id="8e09d-138">在 " **操作** " 菜单上，单击 " **将所有用户移至池**"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-138">On the **Action** menu, click **Move all users to pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e09d-139">将筛选器应用于现有用户集时，选项 " <STRONG>将所有用户移至池中</STRONG> " 将位于已筛选的用户子集的上下文中，而不是 <STRONG><EM>所有</EM></STRONG> 可能的用户。</span><span class="sxs-lookup"><span data-stu-id="8e09d-139">When a filter is applied to an existing set of users, the option <STRONG>Move all users to pool</STRONG> is in the context of the filtered subset of users, not <STRONG><EM>all</EM></STRONG> possible users.</span></span>

    
    </div>

7.  <span data-ttu-id="8e09d-140">在 " **移动用户**" 中，选择包含要在 **源注册机构池中** 移动的用户帐户的池。</span><span class="sxs-lookup"><span data-stu-id="8e09d-140">In **Move Users**, select the pool that contains the user accounts that you want to move in **Source registrar pool**.</span></span>

8.  <span data-ttu-id="8e09d-141">在 " **目标注册机构" 池中**，选择要将用户移动到的池。</span><span class="sxs-lookup"><span data-stu-id="8e09d-141">In **Destination registrar pool**, select the pool where you want to move the users.</span></span>

9.  <span data-ttu-id="8e09d-142"> (可选) 如果目标服务器或池不可用，请选中 " **强制** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="8e09d-142">(Optional) If the destination server or pool is unavailable, select the **Force** check box.</span></span>
    
    <div>
    

    > [!Caution]  
    > <span data-ttu-id="8e09d-143">如果您选择 " <STRONG>强制</STRONG>"，则用户帐户将被移动，但相关联的用户数据（如计划的会议和联系人）不会移动。</span><span class="sxs-lookup"><span data-stu-id="8e09d-143">If you select <STRONG>Force</STRONG>, the user account is moved, but associated user data such scheduled conferences and contacts is not moved.</span></span>

    
    </div>

</div>

<div>

## <a name="to-move-users-from-one-pool-to-another-using-windows-powershell-cmdlets"></a><span data-ttu-id="8e09d-144">使用 Windows PowerShell cmdlet 将用户从一个池移动到另一个池</span><span class="sxs-lookup"><span data-stu-id="8e09d-144">To move users from one pool to another using Windows PowerShell cmdlets</span></span>

1.  <span data-ttu-id="8e09d-145">根据运行 (（本地或远程) ）运行 Windows PowerShell 命令的方式，您需要以正确的 Lync Server 2013 管理角色的成员身份登录，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8e09d-145">Depending on how you run Windows PowerShell commands (that is, locally or remotely), you need to log on as a member of the correct Lync Server 2013 administrative roles as follows:</span></span>
    
    1.  <span data-ttu-id="8e09d-146">如果您在本地计算机上运行命令 (例如，您直接登录到前端服务器) ：登录到安装了 Lync Server 管理外壳的计算机，RTCUniversalServerAdmins 组的成员或具有必要的用户权限，如在 [Lync Server 2013 中的委派设置权限](lync-server-2013-delegate-setup-permissions.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="8e09d-146">If you are running the commands on the local machine (for example, you log on directly to a Front End Server): Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>
    
    2.  <span data-ttu-id="8e09d-147">如果你在另一台计算机上远程运行命令 (例如，登录到你的计算机并在标准版前端服务器上远程运行命令) ：从分配给 CsUserAdministrator 角色或 CsAdministrator 角色的用户帐户登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="8e09d-147">If you are running the commands remotely on another computer (for example, you log on to your computer and run the commands remotely on a Standard Edition Front End Server): From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8e09d-148">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="8e09d-148">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="8e09d-149">若要移动单个用户，请使用 Move-CsUser cmdlet，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8e09d-149">To move single users, use the Move-CsUser cmdlet as follows:</span></span>
    
        Move-CsUser -Identity "Pilar Ackerman" -Target "pool01.contoso.net"
    
    <span data-ttu-id="8e09d-150">要移动的用户是用户 Pilar Ackerman，用户将从其当前分配的主池移动到该池 pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="8e09d-150">Where the user to move is the user Pilar Ackerman, and the user will be moved from their currently assigned home pool to the pool pool01.contoso.net</span></span>

4.  <span data-ttu-id="8e09d-151">若要移动大量用户，请将筛选器与 **move-csuser** cmdlet 配合使用，并将生成的用户集传递到 **move-csuser**：</span><span class="sxs-lookup"><span data-stu-id="8e09d-151">To move a large number of users, use filters with the **Get-CsUser** cmdlet and pass the resulting set of users to **Move-CsUser**:</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "CurrentPoolFqdn"} | Move-CsUser -Target "TargetPoolFQDN"
    
    <span data-ttu-id="8e09d-152">**Move-csuser** 和 **move-csuser** 的合并命令可能会导致以下情况：</span><span class="sxs-lookup"><span data-stu-id="8e09d-152">The combined commands of the **Get-CsUser** and **Move-CsUser** might result in this:</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "pool02.contoso.net"} | Move-CsUser -Target "pool01.contoso.net"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8e09d-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8e09d-153">See Also</span></span>


[<span data-ttu-id="8e09d-154">在 Lync Server 2013 中修改用户帐户属性</span><span class="sxs-lookup"><span data-stu-id="8e09d-154">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)  
  

<span data-ttu-id="8e09d-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e09d-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

