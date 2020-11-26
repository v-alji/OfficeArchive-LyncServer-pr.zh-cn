---
title: Lync Server 2013：启用或禁用客户端版本控制
description: Lync Server 2013：启用或禁用客户端版本控制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable client versioning
ms:assetid: 33a98cb9-a979-4bb6-afb2-512f601d7ac5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898475(v=OCS.15)
ms:contentKeyID: 50873755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0bbd190e827e028efc37365c3cd8ecab16b35dac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428914"
---
# <a name="enable-or-disable-client-versioning-in-lync-server-2013"></a><span data-ttu-id="43ec2-103">在 Lync Server 2013 中启用或禁用客户端版本</span><span class="sxs-lookup"><span data-stu-id="43ec2-103">Enable or disable client versioning in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="43ec2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="43ec2-104">

<span> </span></span></span>

<span data-ttu-id="43ec2-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="43ec2-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="43ec2-106">客户端版本配置设置用于打开或关闭客户端版本控制，无论是全局还是针对特定网站。</span><span class="sxs-lookup"><span data-stu-id="43ec2-106">Client version configuration settings are used to turn client version control on or off, either globally or for particular sites.</span></span> <span data-ttu-id="43ec2-107">全局客户端版本配置与 Lync Server 2013 一起安装，用于为整个服务器部署启用或禁用客户端版本控制。</span><span class="sxs-lookup"><span data-stu-id="43ec2-107">The global client version configuration installs with Lync Server 2013 and is used to enable or disable client version control for the entire server deployment.</span></span> <span data-ttu-id="43ec2-108">启用全局配置后，任何已有的客户端版本策略将在用户尝试登录时生效。</span><span class="sxs-lookup"><span data-stu-id="43ec2-108">When the global configuration is enabled, any client version policies you have in place will take effect when users attempt to log on.</span></span> <span data-ttu-id="43ec2-109">如果不希望发生任何客户端版本控制，则可以禁用全局客户端版本配置。</span><span class="sxs-lookup"><span data-stu-id="43ec2-109">You can disable the global client version configuration if you do not want any client version control to occur.</span></span> <span data-ttu-id="43ec2-110">可以从 Lync Server 2013 控制面板或 Lync Server 2013 管理外壳程序启用或禁用客户端版本控制。</span><span class="sxs-lookup"><span data-stu-id="43ec2-110">You can enable or disable client versioning from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="43ec2-111">由于匿名用户未与用户、站点或服务关联，因此匿名用户仅受全局级别策略的影响。</span><span class="sxs-lookup"><span data-stu-id="43ec2-111">Because anonymous users are not associated with a user, site, or service, anonymous users are affected by global-level policies only.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-client-versioning-by-using-lync-server-control-panel"></a><span data-ttu-id="43ec2-112">使用 Lync Server "控制面板" 启用或禁用客户端版本</span><span class="sxs-lookup"><span data-stu-id="43ec2-112">To enable or disable client versioning by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="43ec2-113">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="43ec2-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="43ec2-114">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="43ec2-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="43ec2-115">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="43ec2-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="43ec2-116">在左侧导航栏中，单击 " **客户端**"，然后单击 " **客户端版本配置** 导航" 按钮。</span><span class="sxs-lookup"><span data-stu-id="43ec2-116">In the left navigation bar, click **Clients**, and then click the **Client Version Configuration** navigation button.</span></span>

4.  <span data-ttu-id="43ec2-117">执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="43ec2-117">Do the following:</span></span>
    
      - <span data-ttu-id="43ec2-118">若要全局启用或禁用客户端版本控制，请双击 **全局** 配置，然后修改设置。</span><span class="sxs-lookup"><span data-stu-id="43ec2-118">To globally enable or disable client versioning, double-click the **Global** configuration, and then modify the settings.</span></span>
    
      - <span data-ttu-id="43ec2-119">若要启用或禁用特定网站的客户端版本，请单击 " **新建**"，选择网站，单击 **"确定**"，然后修改网站的设置。</span><span class="sxs-lookup"><span data-stu-id="43ec2-119">To enable or disable client versioning for a particular site, click **New**, select the site, click **OK**, and then modify the settings for the site.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-client-versioning-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="43ec2-120">使用 Windows PowerShell Cmdlet 启用或禁用客户端版本管理</span><span class="sxs-lookup"><span data-stu-id="43ec2-120">Enabling or Disabling Client Versioning by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="43ec2-121">你可以使用 **CsClientVersionConfiguration** cmdlet 启用或禁用客户端版本控制。</span><span class="sxs-lookup"><span data-stu-id="43ec2-121">You can enable or disable client versioning by using the **Set-CsClientVersionConfiguration** cmdlet.</span></span> <span data-ttu-id="43ec2-122">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="43ec2-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="43ec2-123">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="43ec2-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-client-versioning"></a><span data-ttu-id="43ec2-124">启用客户端版本控制</span><span class="sxs-lookup"><span data-stu-id="43ec2-124">To enable client versioning</span></span>

  - <span data-ttu-id="43ec2-125">你可以通过将 **Enabled** 属性设置为 True ($True) 来启用客户端版本控制。</span><span class="sxs-lookup"><span data-stu-id="43ec2-125">You can enable client versioning by setting the **Enabled** property to True ($True).</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -Enabled $True

</div>

<div>

## <a name="to-disable-client-versioning"></a><span data-ttu-id="43ec2-126">禁用客户端版本</span><span class="sxs-lookup"><span data-stu-id="43ec2-126">To disable client versioning</span></span>

  - <span data-ttu-id="43ec2-127">你可以通过将 **Enabled** 属性设置为 False ($False) 来禁用客户端版本控制。</span><span class="sxs-lookup"><span data-stu-id="43ec2-127">You can disable client versioning by setting the **Enabled** property to False ($False).</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -Enabled $True

</div>

<span data-ttu-id="43ec2-128">有关详细信息，请参阅 [CsClientVersionConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsClientVersionConfiguration) Cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="43ec2-128">For details, see the Help topic for the [Set-CsClientVersionConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsClientVersionConfiguration) cmdlet.</span></span>

<span data-ttu-id="43ec2-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="43ec2-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

