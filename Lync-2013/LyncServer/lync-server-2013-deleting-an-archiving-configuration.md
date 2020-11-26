---
title: Lync Server 2013：删除存档配置
description: Lync Server 2013：删除存档配置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving configuration
ms:assetid: a8744d39-5cf2-474c-9a99-a0f3a37f846f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205167(v=OCS.15)
ms:contentKeyID: 48185093
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bb267c119b49c9bbf06f365c3bdf2cbab459628
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430376"
---
# <a name="deleting-an-archiving-configuration-in-lync-server-2013"></a><span data-ttu-id="a04c9-103">在 Lync Server 2013 中删除存档配置</span><span class="sxs-lookup"><span data-stu-id="a04c9-103">Deleting an Archiving configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a04c9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a04c9-104">

<span> </span></span></span>

<span data-ttu-id="a04c9-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="a04c9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="a04c9-106">你可以删除网站配置或池配置。</span><span class="sxs-lookup"><span data-stu-id="a04c9-106">You can delete a site configuration or pool configuration.</span></span> <span data-ttu-id="a04c9-107">无法删除全局配置。</span><span class="sxs-lookup"><span data-stu-id="a04c9-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="a04c9-108">如果删除全局配置，该配置将自动重置为默认值。</span><span class="sxs-lookup"><span data-stu-id="a04c9-108">If you delete the global configuration, it is automatically reset to the default values.</span></span> <span data-ttu-id="a04c9-109">有关如何实现存档配置的详细信息，包括你可以指定哪些选项和存档配置的层次结构，请参阅规划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="a04c9-109">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>

## <a name="to-delete-a-site-or-pool-configuration-for-archiving"></a><span data-ttu-id="a04c9-110">删除网站或池配置以进行存档</span><span class="sxs-lookup"><span data-stu-id="a04c9-110">To delete a site or pool configuration for archiving</span></span>

1.  <span data-ttu-id="a04c9-111">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="a04c9-111">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a04c9-112">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="a04c9-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a04c9-113">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="a04c9-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a04c9-114">在左侧导航栏中，单击“监控和存档”，然后单击“存档配置”。</span><span class="sxs-lookup"><span data-stu-id="a04c9-114">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="a04c9-115">在存档配置的列表中，单击要删除的站点或池配置，单击“**编辑**”，然后单击“**删除**”。</span><span class="sxs-lookup"><span data-stu-id="a04c9-115">In the list of archiving configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="a04c9-116">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="a04c9-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="removing-archiving-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a04c9-117">使用 Windows PowerShell Cmdlet 删除存档配置设置</span><span class="sxs-lookup"><span data-stu-id="a04c9-117">Removing Archiving Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="a04c9-118">可以使用 Windows PowerShell 和 **CsArchivingConfiguration** cmdlet 删除存档配置设置。</span><span class="sxs-lookup"><span data-stu-id="a04c9-118">Archiving configuration settings can be deleted by using Windows PowerShell and the **Remove-CsArchivingConfiguration** cmdlet.</span></span> <span data-ttu-id="a04c9-119">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="a04c9-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a04c9-120">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="a04c9-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-archiving-configuration-settings"></a><span data-ttu-id="a04c9-121">删除指定的存档配置设置集合</span><span class="sxs-lookup"><span data-stu-id="a04c9-121">To remove a specified collection of archiving configuration settings</span></span>

  - <span data-ttu-id="a04c9-122">以下命令将删除应用于 Redmond 网站的存档配置设置：</span><span class="sxs-lookup"><span data-stu-id="a04c9-122">The following command removes the archiving configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsArchivingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-archiving-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="a04c9-123">删除应用到网站范围的所有存档配置设置</span><span class="sxs-lookup"><span data-stu-id="a04c9-123">To remove all the archiving configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="a04c9-124">此命令将删除应用到服务作用域的所有存档配置设置：</span><span class="sxs-lookup"><span data-stu-id="a04c9-124">This command removes all the archiving configuration settings applied to the service scope:</span></span>
    
        Get-CsArchivingConfiguration -Filter "site:*" | Remove-CsArchivingConfiguration

</div>

<div>

## <a name="to-remove-archiving-configuration-settings-based-on-a-specified-property-value"></a><span data-ttu-id="a04c9-125">根据指定的属性值删除存档配置设置</span><span class="sxs-lookup"><span data-stu-id="a04c9-125">To remove archiving configuration settings based on a specified property value</span></span>

  - <span data-ttu-id="a04c9-126">此命令将删除 Exchange 存档已禁用的所有存档配置设置：</span><span class="sxs-lookup"><span data-stu-id="a04c9-126">This command removes all the archiving configuration settings where Exchange archiving has been disabled:</span></span>
    
        Get-CsArchivingConfiguration | Where-Object {$_.EnableExchangeArchiving -eq $False} | Remove-CsArchivingConfiguration

</div>

<span data-ttu-id="a04c9-127">有关详细信息，请参阅 [CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingConfiguration) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="a04c9-127">For more information, see the help topic for the [Remove-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a04c9-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a04c9-128">See Also</span></span>


[<span data-ttu-id="a04c9-129">在 Lync Server 2013 中存档的工作方式</span><span class="sxs-lookup"><span data-stu-id="a04c9-129">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="a04c9-130">在 Lync Server 2013 中管理内部和外部通信的存档</span><span class="sxs-lookup"><span data-stu-id="a04c9-130">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="a04c9-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a04c9-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

