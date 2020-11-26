---
title: Lync Server 2013：重置外部用户访问的全局策略
description: Lync Server 2013：重置外部用户访问的全局策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reset the global policy for external user access
ms:assetid: 8207e1b1-de9e-461f-975f-fcc5c526849a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182545(v=OCS.15)
ms:contentKeyID: 48184675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 061f86fd454cea851a8e8cfbd4f40921daeecd98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436361"
---
# <a name="reset-the-global-policy-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="30643-103">在 Lync Server 2013 中重置外部用户访问的全局策略</span><span class="sxs-lookup"><span data-stu-id="30643-103">Reset the global policy for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30643-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30643-104">

<span> </span></span></span>

<span data-ttu-id="30643-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="30643-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="30643-106">您不能完全删除全局策略。</span><span class="sxs-lookup"><span data-stu-id="30643-106">You cannot completely delete a global policy.</span></span> <span data-ttu-id="30643-107">使用全局策略中的 " **删除** " 选项仅将全局策略重置为默认设置，不包括对任何外部用户访问选项的支持。</span><span class="sxs-lookup"><span data-stu-id="30643-107">Using the **Delete** option on the global policy only resets the global policy to the default settings, which do not include support for any external user access options.</span></span>

<div>

## <a name="to-reset-the-global-policy-to-the-default-settings"></a><span data-ttu-id="30643-108">将全局策略重置为默认设置</span><span class="sxs-lookup"><span data-stu-id="30643-108">To reset the global policy to the default settings</span></span>

1.  <span data-ttu-id="30643-109">使用 RTCUniversalServerAdmins 组成员（或具有同等用户权限）的用户帐户，或分配给 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="30643-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="30643-110">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="30643-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="30643-111">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="30643-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="30643-112">在左侧导航栏中，单击 " **外部用户访问**"，单击 " **外部访问策略**"。</span><span class="sxs-lookup"><span data-stu-id="30643-112">In the left navigation bar, click **External User Access**, click **External Access Policy**.</span></span>

4.  <span data-ttu-id="30643-113">在 " **外部访问策略** " 选项卡上，单击 "全局策略"，单击 " **编辑**"，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="30643-113">On the **External Access Policy** tab, click the global policy, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="30643-114">当系统提示确认删除时，单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="30643-114">When prompted to confirm the deletion, click **OK**.</span></span> <span data-ttu-id="30643-115">将在页面顶部显示一条消息，通知您全局策略已重置。</span><span class="sxs-lookup"><span data-stu-id="30643-115">A message appears at the top of the page informing you that the global policy has been reset.</span></span>

</div>

<div>

## <a name="resetting-the-global-external-access-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="30643-116">使用 Windows PowerShell Cmdlet 重置全局外部访问策略</span><span class="sxs-lookup"><span data-stu-id="30643-116">Resetting the Global External Access Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="30643-117">全局外部访问策略可以通过使用 Windows PowerShell 和 Remove-CsExternalAccessPolicy cmdlet 进行重置。</span><span class="sxs-lookup"><span data-stu-id="30643-117">The global external access policy can be reset by using Windows PowerShell and the Remove-CsExternalAccessPolicy cmdlet.</span></span> <span data-ttu-id="30643-118">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从远程会话 Windows PowerShell 运行。</span><span class="sxs-lookup"><span data-stu-id="30643-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session Windows PowerShell.</span></span> <span data-ttu-id="30643-119">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="30643-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-reset-the-global-external-access-policy"></a><span data-ttu-id="30643-120">重置全局外部访问策略</span><span class="sxs-lookup"><span data-stu-id="30643-120">To reset the global external access policy</span></span>

  - <span data-ttu-id="30643-121">此命令将重置全局外部访问策略：</span><span class="sxs-lookup"><span data-stu-id="30643-121">This command resets the global external access policy:</span></span>
    
        Remove-CsExternalAccessPolicy -Identity "global"

</div>

<span data-ttu-id="30643-122">有关详细信息，请参阅 [CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="30643-122">For more information, see the help topic for the [Remove-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy) cmdlet.</span></span>

<span data-ttu-id="30643-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30643-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

