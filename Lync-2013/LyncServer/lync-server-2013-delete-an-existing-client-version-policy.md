---
title: Lync Server 2013：删除现有客户端版本策略
description: Lync Server 2013：删除现有的客户端版本策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing client version policy
ms:assetid: b88aaa25-97ff-4eb6-bd34-b97332cd6890
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ923064(v=OCS.15)
ms:contentKeyID: 50675349
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1328d54790b2a7856fa2776bb59feeb515bab1cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430600"
---
# <a name="delete-an-existing-client-version-policy-in-lync-server-2013"></a><span data-ttu-id="952ed-103">在 Lync Server 2013 中删除现有客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="952ed-103">Delete an existing client version policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="952ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="952ed-104">

<span> </span></span></span>

<span data-ttu-id="952ed-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="952ed-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="952ed-106">如果要删除以前配置的客户端版本策略，则可以从 Lync Server 2013 控制面板或 Lync Server 2013 管理外壳中将其删除。</span><span class="sxs-lookup"><span data-stu-id="952ed-106">If you want to delete a client version policy that was previously configured, you can delete it from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-delete-client-version-policies-by-using-lync-server-control-panel"></a><span data-ttu-id="952ed-107">使用 Lync Server "控制面板" 删除客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="952ed-107">To delete client version policies by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="952ed-108">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="952ed-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="952ed-109">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="952ed-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="952ed-110">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="952ed-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="952ed-111">在左侧导航栏中，单击 " **客户端**"，然后单击 " **客户端版本策略** 导航" 按钮。</span><span class="sxs-lookup"><span data-stu-id="952ed-111">In the left navigation bar, click **Clients**, and then click the **Client Version Policy** navigation button.</span></span>

4.  <span data-ttu-id="952ed-112">在 " **客户端版本策略** " 页面上，选择要删除的客户端版本策略或策略，单击 " **编辑**"，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="952ed-112">On the **Client Version Policy** page, select the client version policy or policies you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="deleting-client-version-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="952ed-113">使用 Windows PowerShell Cmdlet 删除客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="952ed-113">Deleting Client Version Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="952ed-114">你可以使用 **CsClientVersionPolicy** cmdlet 删除客户端版本策略。</span><span class="sxs-lookup"><span data-stu-id="952ed-114">You can delete client version policies by using the **Remove-CsClientVersionPolicy** cmdlet.</span></span> <span data-ttu-id="952ed-115">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="952ed-115">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="952ed-116">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="952ed-116">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-client-version-policy"></a><span data-ttu-id="952ed-117">删除特定客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="952ed-117">To remove a specific client version policy</span></span>

  - <span data-ttu-id="952ed-118">此命令将删除应用于 Redmond 网站的客户端版本策略：</span><span class="sxs-lookup"><span data-stu-id="952ed-118">This command deletes the client version policy applied to the Redmond site:</span></span>
    
        Remove-CsClientVersionPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-client-version-policies-applied-to-the-site-scope"></a><span data-ttu-id="952ed-119">删除应用到网站范围的所有客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="952ed-119">To remove all the client version policies applied to the site scope</span></span>

  - <span data-ttu-id="952ed-120">此命令将删除在网站范围内配置的所有客户端版本策略：</span><span class="sxs-lookup"><span data-stu-id="952ed-120">This command removes all the client version policies configured at the site scope:</span></span>
    
        Get-CsClientVersionPolicy -Fiter "site:*" | Remove-CsClientVersionPolicy

</div>

<div>

## <a name="to-remove-client-version-policies-that-do-not-include-a-specific-user-agent"></a><span data-ttu-id="952ed-121">删除不包含特定用户代理的客户端版本策略</span><span class="sxs-lookup"><span data-stu-id="952ed-121">To remove client version policies that do not include a specific user agent</span></span>

  - <span data-ttu-id="952ed-122">此命令将删除不包括 Windows Phone Lync (WPLync) 用户代理规则的任何客户端版本策略：</span><span class="sxs-lookup"><span data-stu-id="952ed-122">And this command removes any client version policies that do not include a rule for the Windows Phone Lync (WPLync) user agent:</span></span>
    
        Get-CsClientVersionPolicy | Where-Object {$_.Rules -notmatch "UserAgent=WPLync" | Remove-CsClientVersionPolicy

</div>

<span data-ttu-id="952ed-123">有关详细信息，请参阅 [CsClientVersionPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsClientVersionPolicy) Cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="952ed-123">For details, see the Help topic for the [Remove-CsClientVersionPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsClientVersionPolicy) cmdlet.</span></span>

<span data-ttu-id="952ed-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="952ed-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

