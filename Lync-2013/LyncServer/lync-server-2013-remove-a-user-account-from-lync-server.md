---
title: Lync Server 2013：从 Lync Server 中删除用户帐户
description: Lync Server 2013：从 Lync Server 中删除用户帐户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove a user account from Lync Server
ms:assetid: 2f512aba-e358-45ae-af58-74312ee9c514
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688008(v=OCS.15)
ms:contentKeyID: 49733596
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201eb8a7ba620792b92e2c7983890047c249ce86
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436445"
---
# <a name="remove-a-user-account-from-lync-server-2013"></a><span data-ttu-id="90d6b-103">从 Lync Server 2013 中删除用户帐户</span><span class="sxs-lookup"><span data-stu-id="90d6b-103">Remove a user account from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90d6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90d6b-104">

<span> </span></span></span>

<span data-ttu-id="90d6b-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="90d6b-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="90d6b-106">你可以使用以下过程在 Lync Server 2013 中删除以前添加的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="90d6b-106">You can use the following procedure to remove a previously added user account in Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="90d6b-107">删除用户将导致你丢失为用户帐户配置的任何设置。</span><span class="sxs-lookup"><span data-stu-id="90d6b-107">Removing a user will cause you to lose any settings you configured for the user account.</span></span> <span data-ttu-id="90d6b-108">如果想要暂时禁用用户帐户，请参阅 <A href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">禁用或重新启用 Lync Server 2013 的用户帐户</A>主题。</span><span class="sxs-lookup"><span data-stu-id="90d6b-108">If you would like to temporarily disable a user account instead, see the topic <A href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Disable or re-enable user account for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-remove-a-user-account-by-using-lync-server-management-shell"></a><span data-ttu-id="90d6b-109">使用 Lync Server 命令行管理程序删除用户帐户</span><span class="sxs-lookup"><span data-stu-id="90d6b-109">To remove a user account by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="90d6b-110">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="90d6b-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="90d6b-111">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="90d6b-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="90d6b-112">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="90d6b-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="90d6b-113">在左导航栏中，单击“用户”。</span><span class="sxs-lookup"><span data-stu-id="90d6b-113">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="90d6b-114">在 " **搜索用户** " 框中，键入要禁用或重新启用的用户帐户的所有或第一部分显示名称 "名字"、"姓氏"、"安全帐户管理器" (SAM) 帐户名称、SIP 地址或行统一资源标识符 (URI) ，然后单击 " **查找**"。</span><span class="sxs-lookup"><span data-stu-id="90d6b-114">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to disable or re-enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="90d6b-115">在表中，单击要删除的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="90d6b-115">In the table, click the user account that you want to remove.</span></span>

6.  <span data-ttu-id="90d6b-116">在 " **操作** " 菜单上，选择 " **从 Lync Server 中删除**"，将出现一个对话框。</span><span class="sxs-lookup"><span data-stu-id="90d6b-116">On the **Action** menu, select **Remove from Lync Server**, and a dialog box appears.</span></span>

7.  <span data-ttu-id="90d6b-117">从对话框中，选择 **"确定"** 以删除用户。</span><span class="sxs-lookup"><span data-stu-id="90d6b-117">From the dialog box, select **OK** to remove the user.</span></span>

</div>

<div>

## <a name="removing-user-accounts-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="90d6b-118">使用 Windows PowerShell Cmdlet 删除用户帐户</span><span class="sxs-lookup"><span data-stu-id="90d6b-118">Removing User Accounts by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="90d6b-119">你可以使用 Disable-CsUser cmdlet 删除用户帐户。</span><span class="sxs-lookup"><span data-stu-id="90d6b-119">You can remove user accounts by using the Disable-CsUser cmdlet.</span></span> <span data-ttu-id="90d6b-120">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从远程会话 Windows PowerShell 运行。</span><span class="sxs-lookup"><span data-stu-id="90d6b-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session Windows PowerShell.</span></span> <span data-ttu-id="90d6b-121">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="90d6b-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-user-account"></a><span data-ttu-id="90d6b-122">删除用户帐户</span><span class="sxs-lookup"><span data-stu-id="90d6b-122">To remove a user account</span></span>

  - <span data-ttu-id="90d6b-123">若要删除用户帐户，请使用 Disable-CsUser cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90d6b-123">To remove a user account, use the Disable-CsUser cmdlet.</span></span> <span data-ttu-id="90d6b-124">例如：</span><span class="sxs-lookup"><span data-stu-id="90d6b-124">For example:</span></span>
    
        Disable-CsUser -Identity "Ken Myer"
    
    <span data-ttu-id="90d6b-125">此命令运行后，无法重新启用帐户及其以前的设置。</span><span class="sxs-lookup"><span data-stu-id="90d6b-125">After this command has run there is no way to re-enable the account and its previous settings.</span></span> <span data-ttu-id="90d6b-126">相反，你将需要使用 Enable-CsUser cmdlet 为 Ken Myer 创建全新帐户。</span><span class="sxs-lookup"><span data-stu-id="90d6b-126">Instead, you will need to use the Enable-CsUser cmdlet to create a brand-new account for Ken Myer.</span></span>

</div>

<span data-ttu-id="90d6b-127">有关详细信息，请参阅 Disable cmdlet 的帮助主题 [move-csuser](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser) 。</span><span class="sxs-lookup"><span data-stu-id="90d6b-127">For more information, see the help topic for the [Disable-CsUser](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="90d6b-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="90d6b-128">See Also</span></span>


[<span data-ttu-id="90d6b-129">禁用或重新启用 Lync Server 2013 的用户帐户</span><span class="sxs-lookup"><span data-stu-id="90d6b-129">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  


[<span data-ttu-id="90d6b-130">启用和禁用 Lync Server 2013 的用户</span><span class="sxs-lookup"><span data-stu-id="90d6b-130">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="90d6b-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90d6b-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

