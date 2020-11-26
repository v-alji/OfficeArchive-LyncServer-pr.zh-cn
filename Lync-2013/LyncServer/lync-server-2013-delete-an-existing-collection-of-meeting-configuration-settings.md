---
title: 删除会议配置设置的现有集合
description: 删除会议配置设置的现有集合。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of meeting configuration settings
ms:assetid: 92ff8a91-05c5-4047-a533-5dff12f22299
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688136(v=OCS.15)
ms:contentKeyID: 49733736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc0985023a1459130c7d589327535436145a0ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430530"
---
# <a name="delete-an-existing-collection-of-meeting-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="1d60c-103">删除 Lync Server 2013 中现有的会议配置设置集合</span><span class="sxs-lookup"><span data-stu-id="1d60c-103">Delete an existing collection of meeting configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d60c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d60c-104">

<span> </span></span></span>

<span data-ttu-id="1d60c-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="1d60c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="1d60c-106">您可以删除网站或用户配置。</span><span class="sxs-lookup"><span data-stu-id="1d60c-106">You can delete a site or user configuration.</span></span> <span data-ttu-id="1d60c-107">无法删除全局配置。</span><span class="sxs-lookup"><span data-stu-id="1d60c-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="1d60c-108">如果删除全局配置，该配置将自动重置为默认值。</span><span class="sxs-lookup"><span data-stu-id="1d60c-108">If you delete the global configuration, it is automatically reset to the default values.</span></span>

<div>

## <a name="to-delete-a-site-or-user-meeting-configuration"></a><span data-ttu-id="1d60c-109">删除网站或用户会议配置</span><span class="sxs-lookup"><span data-stu-id="1d60c-109">To delete a site or user meeting configuration</span></span>

1.  <span data-ttu-id="1d60c-110">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="1d60c-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="1d60c-111">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="1d60c-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1d60c-112">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="1d60c-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1d60c-113">在左侧导航栏中，单击 " **会议** "，然后单击 " **会议配置**"。</span><span class="sxs-lookup"><span data-stu-id="1d60c-113">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="1d60c-114">在会议配置的列表中，单击要删除的站点或池配置，单击“**编辑**”，然后单击“**删除**”。</span><span class="sxs-lookup"><span data-stu-id="1d60c-114">In the list of meeting configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-meeting-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="1d60c-115">使用 Windows PowerShell Cmdlet 删除会议配置设置</span><span class="sxs-lookup"><span data-stu-id="1d60c-115">Removing Meeting Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="1d60c-116">可使用 Windows PowerShell 和 Remove-CsMeetingConfiguration cmdlet 删除会议设置。</span><span class="sxs-lookup"><span data-stu-id="1d60c-116">Meeting settings can be deleted by using Windows PowerShell and the Remove-CsMeetingConfiguration cmdlet.</span></span> <span data-ttu-id="1d60c-117">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="1d60c-117">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="1d60c-118">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="1d60c-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-meeting-configuration-settings"></a><span data-ttu-id="1d60c-119">删除指定的会议配置设置集合</span><span class="sxs-lookup"><span data-stu-id="1d60c-119">To remove a specified collection of meeting configuration settings</span></span>

  - <span data-ttu-id="1d60c-120">此命令将删除应用于雷德蒙网站的会议配置设置：</span><span class="sxs-lookup"><span data-stu-id="1d60c-120">This command removes the meeting configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsMeetingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="1d60c-121">删除应用到网站范围的所有会议配置设置</span><span class="sxs-lookup"><span data-stu-id="1d60c-121">To remove all the meeting configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="1d60c-122">此命令将删除应用到网站范围的所有会议配置设置：</span><span class="sxs-lookup"><span data-stu-id="1d60c-122">This command removes all the meeting configuration settings applied to the site scope:</span></span>
    
        Get-CsMeetingConfiguration -Filter "site:*" | Remove-CsMeetingConfiguration

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-that-admit-anonymous-users-by-default"></a><span data-ttu-id="1d60c-123">删除默认情况下承认匿名用户的所有会议配置设置</span><span class="sxs-lookup"><span data-stu-id="1d60c-123">To remove all the meeting configuration settings that admit anonymous users by default</span></span>

  - <span data-ttu-id="1d60c-124">这一方法将删除所有允许匿名用户默认获准的设置：</span><span class="sxs-lookup"><span data-stu-id="1d60c-124">And this one removes all the settings that allow anonymous users to be admitted by default:</span></span>
    
        Get-CsMeetingConfiguration | Where-Object {$_.AdmitAnonymousUsersByDefault -eq $True} | Remove-CsMeetingConfiguration

</div>

<span data-ttu-id="1d60c-125">有关详细信息，请参阅 [CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="1d60c-125">For more information, see the help topic for the [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="1d60c-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d60c-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

