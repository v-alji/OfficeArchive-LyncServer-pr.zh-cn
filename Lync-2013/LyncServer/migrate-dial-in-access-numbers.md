---
title: 迁移拨入访问号码
description: 迁移拨入访问号码。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate dial-in access numbers
ms:assetid: e0dfaed2-64c7-45cb-aaa9-d6117a26625d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721909(v=OCS.15)
ms:contentKeyID: 49733843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2c8bd34a30bc4b3f8999144cd84a1eee62e2ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446890"
---
# <a name="migrate-dial-in-access-numbers"></a><span data-ttu-id="37a8d-103">迁移拨入访问号码</span><span class="sxs-lookup"><span data-stu-id="37a8d-103">Migrate dial-in access numbers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37a8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37a8d-104">

<span> </span></span></span>

<span data-ttu-id="37a8d-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="37a8d-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="37a8d-106">将 Lync Server 2010 中的拨入访问号码迁移到 Lync Server 2013 需要运行 **CsApplicationEndpoint** cmdlet 以迁移联系人对象。</span><span class="sxs-lookup"><span data-stu-id="37a8d-106">Migrating dial-in access numbers from Lync Server 2010 to Lync Server 2013 requires running the **Move-CsApplicationEndpoint** cmdlet to migrate the contact objects.</span></span> <span data-ttu-id="37a8d-107">在 Lync Server 2010 和 Lync Server 2013 共存期内，在 Lync Server 2013 中创建的拨入访问号码与您在 Lync Server 2010 中创建的拨入访问号码类似，如本部分所述。</span><span class="sxs-lookup"><span data-stu-id="37a8d-107">During the Lync Server 2010 and Lync Server 2013 coexistence period, dial-in access numbers that you created in Lync Server 2013 behave similarly to the dial-in access numbers that you create in Lync Server 2010, as described in this section.</span></span>

<span data-ttu-id="37a8d-108">您在 Lync Server 2010 中创建的拨入接入号码，但迁移到 Lync Server 2013 或在迁移期间或之后在 Lync Server 2013 中创建的号码具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="37a8d-108">Dial-in access numbers that you created in Lync Server 2010 but moved to Lync Server 2013 or that you created in Lync Server 2013 before, during or after migration have the following characteristics:</span></span>

  - <span data-ttu-id="37a8d-109">不会出现在 Office 通信服务器 2007 R2 邀请和 "拨入访问号码" 页面上。</span><span class="sxs-lookup"><span data-stu-id="37a8d-109">Do not appear on Office Communications Server 2007 R2 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="37a8d-110">显示在 Lync Server 2010 的 "会议邀请" 和 "拨入访问号码" 页面上。</span><span class="sxs-lookup"><span data-stu-id="37a8d-110">Appear on Lync Server 2010 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="37a8d-111">显示在 Lync Server 2013 的 "会议邀请" 和 "拨入访问号码" 页面上。</span><span class="sxs-lookup"><span data-stu-id="37a8d-111">Appear on Lync Server 2013 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="37a8d-112">无法在 Office 通信服务器 2007 R2 管理工具中查看或修改。</span><span class="sxs-lookup"><span data-stu-id="37a8d-112">Cannot be viewed or modified in the Office Communications Server 2007 R2 administrative tool.</span></span>

  - <span data-ttu-id="37a8d-113">可在 Lync Server 2010 控制面板和 Lync Server 2010 管理外壳程序中查看和修改。</span><span class="sxs-lookup"><span data-stu-id="37a8d-113">Can be viewed and modified in the Lync Server 2010 Control Panel and in Lync Server 2010 Management Shell.</span></span>

  - <span data-ttu-id="37a8d-114">可在 Lync Server 2013 控制面板和 Lync Server 2013 管理外壳程序中查看和修改。</span><span class="sxs-lookup"><span data-stu-id="37a8d-114">Can be viewed and modified in the Lync Server 2013 Control Panel and in Lync Server 2013 Management Shell.</span></span>

  - <span data-ttu-id="37a8d-115">可通过将 Set-CsDialinConferencingAccessNumber cmdlet 与 Priority 参数一起使用来在区域内重新排序。</span><span class="sxs-lookup"><span data-stu-id="37a8d-115">Can be re-sequenced within the region by using the Set-CsDialinConferencingAccessNumber cmdlet with the Priority parameter.</span></span>

<span data-ttu-id="37a8d-116">在解除 Lync Server 2010 池之前，必须完成指向 Lync Server 2010 池的迁移拨入访问号码的迁移。</span><span class="sxs-lookup"><span data-stu-id="37a8d-116">You must finish migrating dial-in access numbers that point to a Lync Server 2010 pool before you decommission the Lync Server 2010 pool.</span></span> <span data-ttu-id="37a8d-117">如果您没有完成拨入访问号码迁移，如以下过程中所述，对接入号码的拨入调用将失败。</span><span class="sxs-lookup"><span data-stu-id="37a8d-117">If you do not complete dial-in access number migration as described in the following procedure, incoming calls to the access numbers will fail.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="37a8d-118">必须先执行此过程，然后才能解除 Lync Server 2010 池。</span><span class="sxs-lookup"><span data-stu-id="37a8d-118">You must perform this procedure prior to decommissioning the Lync Server 2010 pool.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="37a8d-119">我们建议你在网络使用率较低时移动拨入访问号码，以防出现短时间的服务中断。</span><span class="sxs-lookup"><span data-stu-id="37a8d-119">We recommend that you move dial-in access numbers when network usage is low, in case there is a short period of service outage.</span></span>



</div>

<span data-ttu-id="37a8d-120">**标识和移动拨入访问号码**</span><span class="sxs-lookup"><span data-stu-id="37a8d-120">**To identify and move dial-in access numbers**</span></span>

1.  <span data-ttu-id="37a8d-121">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="37a8d-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="37a8d-122">要将每个拨入访问号码从命令行运行到 Lync Server 2013 上托管的池，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="37a8d-122">To move each dial-in access number to a pool hosted on Lync Server 2013, from the command line run:</span></span>
    
        Move-CsApplicationEndpoint -Identity <SIP URI of the access number to be moved> -Target <FQDN of the pool to which the access number is moving>

3.  <span data-ttu-id="37a8d-123">打开“Lync Server 控制面板”。</span><span class="sxs-lookup"><span data-stu-id="37a8d-123">Open Lync Server Control Panel.</span></span>

4.  <span data-ttu-id="37a8d-124">在左侧导航栏中，单击“**会议**”。</span><span class="sxs-lookup"><span data-stu-id="37a8d-124">In the left navigation bar, click **Conferencing**.</span></span>

5.  <span data-ttu-id="37a8d-125">单击 " **拨入访问号码** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="37a8d-125">Click the **Dial-in Access Number** tab.</span></span>

6.  <span data-ttu-id="37a8d-126">验证你要从中迁移的 Lync Server 2010 池不会保留拨入访问号码。</span><span class="sxs-lookup"><span data-stu-id="37a8d-126">Verify that no dial-in access numbers remain for the Lync Server 2010 pool from which you are migrating.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="37a8d-127">当所有拨入访问号码都指向 Lync Server 2013 池时，您就可以停止 Lync Server 2010 池。</span><span class="sxs-lookup"><span data-stu-id="37a8d-127">When all dial-in access numbers point to the Lync Server 2013 pool, you can then decommission the Lync Server 2010 pool.</span></span>

    
    </div>

<span data-ttu-id="37a8d-128">**使用 Lync Server "控制面板" 验证拨入访问号码迁移**</span><span class="sxs-lookup"><span data-stu-id="37a8d-128">**Verify the dial-in access number migration using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="37a8d-129">从分配给 **CsUserAdministrator** 角色或 **CsAdministrator** 角色的用户帐户登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="37a8d-129">From a user account that is assigned to the **CsUserAdministrator** role or the **CsAdministrator** role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="37a8d-130">打开“Lync Server 控制面板”。</span><span class="sxs-lookup"><span data-stu-id="37a8d-130">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="37a8d-131">在左侧导航栏中，单击“**会议**”。</span><span class="sxs-lookup"><span data-stu-id="37a8d-131">In the left navigation bar, click **Conferencing**.</span></span>

4.  <span data-ttu-id="37a8d-132">单击 " **拨入访问号码** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="37a8d-132">Click the **Dial-in Access Number** tab.</span></span>

5.  <span data-ttu-id="37a8d-133">验证所有拨入访问号码是否已迁移到 Lync Server 2013 上托管的池。</span><span class="sxs-lookup"><span data-stu-id="37a8d-133">Verify all the dial-in access number are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="37a8d-134">**使用 Lync Server 命令行管理程序验证拨入访问号码迁移**</span><span class="sxs-lookup"><span data-stu-id="37a8d-134">**Verify the dial-in access number migration using Lync Server Management Shell**</span></span>

1.  <span data-ttu-id="37a8d-135">打开 Lync Server 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="37a8d-135">Open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="37a8d-136">要从命令行中返回已迁移的所有拨入式会议访问号码，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="37a8d-136">To return all the dial-in conferencing access numbers migrated, from the command line run:</span></span>
    
        Get-CsDialInConferencingAccessNumber -Filter {Pool -eq "<FQDN of the pool to which the access number is moved>"}

3.  <span data-ttu-id="37a8d-137">验证所有拨入访问号码是否已迁移到 Lync Server 2013 上托管的池。</span><span class="sxs-lookup"><span data-stu-id="37a8d-137">Verify all the dial-in access numbers are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="37a8d-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37a8d-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

