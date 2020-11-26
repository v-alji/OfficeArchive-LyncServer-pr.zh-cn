---
title: Lync Server 2013：删除现有会议策略
description: Lync Server 2013：删除现有会议策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing conferencing policy
ms:assetid: 709ed771-790f-4bf1-a4de-b37ca5168688
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688089(v=OCS.15)
ms:contentKeyID: 49733688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b64e51acc6e6dc91b938244da28057b01957069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430502"
---
# <a name="delete-an-existing-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="a5400-103">在 Lync Server 2013 中删除现有会议策略</span><span class="sxs-lookup"><span data-stu-id="a5400-103">Delete an existing conferencing policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5400-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5400-104">

<span> </span></span></span>

<span data-ttu-id="a5400-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="a5400-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="a5400-106">请按照以下步骤删除用户级或网站级会议策略。</span><span class="sxs-lookup"><span data-stu-id="a5400-106">Follow these steps to delete a user-level or a site-level conferencing policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a5400-107">您不能删除全局会议策略。</span><span class="sxs-lookup"><span data-stu-id="a5400-107">You cannot delete the global conferencing policy.</span></span>



</div>

<div>

## <a name="to-delete-a-site-or-user-conferencing-policy"></a><span data-ttu-id="a5400-108">删除网站或用户会议策略</span><span class="sxs-lookup"><span data-stu-id="a5400-108">To delete a site or user conferencing policy</span></span>

1.  <span data-ttu-id="a5400-109">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="a5400-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a5400-110">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="a5400-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a5400-111">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="a5400-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a5400-112">在左侧导航栏中，单击 " **会议** "，然后单击 " **会议策略**"。</span><span class="sxs-lookup"><span data-stu-id="a5400-112">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="a5400-113">在会议策略列表中，单击要删除的站点策略或用户策略，再单击“**编辑**”，然后单击“**删除**”。</span><span class="sxs-lookup"><span data-stu-id="a5400-113">In the list of conferencing policies, click the site or user policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-conferencing-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a5400-114">使用 Windows PowerShell Cmdlet 删除会议策略</span><span class="sxs-lookup"><span data-stu-id="a5400-114">Removing Conferencing Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="a5400-115">你可以使用 Lync Server 命令行管理程序和 **CsConferencingPolicy** cmdlet 删除会议策略。</span><span class="sxs-lookup"><span data-stu-id="a5400-115">You can delete conferencing policies by using Lync Server Management Shell and the **Remove-CsConferencingPolicy** cmdlet.</span></span> <span data-ttu-id="a5400-116">你可以从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行此 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5400-116">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a5400-117">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="a5400-117">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-conferencing-policy"></a><span data-ttu-id="a5400-118">删除指定的会议策略</span><span class="sxs-lookup"><span data-stu-id="a5400-118">To remove a specified conferencing policy</span></span>

  - <span data-ttu-id="a5400-119">以下命令删除 Identity 为 RedmondConferencingPolicy 的会议策略：</span><span class="sxs-lookup"><span data-stu-id="a5400-119">The following command removes the conferencing policy with the Identity RedmondConferencingPolicy:</span></span>
    
        Remove-CsConferencingPolicy -Identity "RedmondConferencingPolicy"

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="a5400-120">删除应用到每用户范围的所有会议策略</span><span class="sxs-lookup"><span data-stu-id="a5400-120">To remove all of the conferencing policies applied to the per-user scope</span></span>

  - <span data-ttu-id="a5400-121">以下命令将删除在每用户作用域上配置的所有会议策略：</span><span class="sxs-lookup"><span data-stu-id="a5400-121">The following command removes all the conferencing policies configured at the per-user scope:</span></span>
    
        Get-CsConferencingPolicy -Filter "tag:*" | Remove-CsConferencingPolicy

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-polices-that-allow-recording-by-external-users"></a><span data-ttu-id="a5400-122">删除允许外部用户录制的所有会议策略</span><span class="sxs-lookup"><span data-stu-id="a5400-122">To remove all of the conferencing polices that allow recording by external users</span></span>

  - <span data-ttu-id="a5400-123">以下命令将删除任何允许外部用户录制会议的会议策略：</span><span class="sxs-lookup"><span data-stu-id="a5400-123">The following command deletes any conferencing policies that allow external users to record the conference:</span></span>
    
        Get-CsConferencingPolicy | Where-Object {$_.AllowExternalUsersToRecordMeetings -eq $True} | Remove-CsConferencingPolicy

</div>

<span data-ttu-id="a5400-124">有关详细信息，请参阅 [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy)。</span><span class="sxs-lookup"><span data-stu-id="a5400-124">For details, see [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).</span></span>

<span data-ttu-id="a5400-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5400-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

