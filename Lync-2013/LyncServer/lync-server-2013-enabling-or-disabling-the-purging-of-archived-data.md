---
title: Lync Server 2013：启用或禁用已存档数据的清除
description: Lync Server 2013：启用或禁用已存档数据的清除。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling the purging of archived data
ms:assetid: 28cef09f-0970-4fc3-8315-f26689e3e187
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520968(v=OCS.15)
ms:contentKeyID: 48183678
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 442b99e2cfa6db303ca8edd216cbdf3b5c13cea9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428746"
---
# <a name="enabling-or-disabling-the-purging-of-archived-data-in-lync-server-2013"></a><span data-ttu-id="c23d1-103">在 Lync Server 2013 中启用或禁用已存档数据的清除</span><span class="sxs-lookup"><span data-stu-id="c23d1-103">Enabling or disabling the purging of archived data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c23d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c23d1-104">

<span> </span></span></span>

<span data-ttu-id="c23d1-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="c23d1-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="c23d1-106">在 Lync Server 2013 "控制面板" 中，使用存档配置启用和禁用清除和配置执行清除的方式。</span><span class="sxs-lookup"><span data-stu-id="c23d1-106">In Lync Server 2013 Control Panel, you use Archiving configurations to enable and disable purging and configure how purging is implemented.</span></span> <span data-ttu-id="c23d1-107">这包括以下存档配置：</span><span class="sxs-lookup"><span data-stu-id="c23d1-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="c23d1-108">部署 Lync Server 2013 时默认创建的全局配置。</span><span class="sxs-lookup"><span data-stu-id="c23d1-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="c23d1-109">可创建和使用的可选网站级和池级配置，用于指定如何为特定网站或池实现存档。</span><span class="sxs-lookup"><span data-stu-id="c23d1-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="c23d1-110">你在部署存档时开始设置存档配置，但你可以在部署后更改、添加和删除配置。</span><span class="sxs-lookup"><span data-stu-id="c23d1-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="c23d1-111">有关如何实现存档配置的详细信息，包括你可以指定哪些选项和存档配置的层次结构，请参阅规划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="c23d1-111">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c23d1-112">若要对托管在 Lync Server 2013 上的用户使用存档，必须配置存档策略，以指定是为内部通信还是在外部通信中启用存档。</span><span class="sxs-lookup"><span data-stu-id="c23d1-112">To use archiving for users who are homed on Lync Server 2013 you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both.</span></span> <span data-ttu-id="c23d1-113">默认情况下，不会为内部或外部通信启用存档。</span><span class="sxs-lookup"><span data-stu-id="c23d1-113">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="c23d1-114">在任何策略中启用存档之前，应为你的部署指定相应的存档配置，并根据需要为特定的网站和池指定相应的存档配置，如本节所述。</span><span class="sxs-lookup"><span data-stu-id="c23d1-114">Prior to enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="c23d1-115">有关启用存档的详细信息，请参阅部署文档中的 <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">在 Lync Server 2013 中配置和分配存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="c23d1-115">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="c23d1-116">如果你在部署要使用 Microsoft Exchange 集成来存储 Exchange 2013 服务器上的存档数据和文件的存档之后，并且你的所有用户都托管在 Exchange 2013 服务器上，则应从拓扑中删除 SQL Server 数据库配置。</span><span class="sxs-lookup"><span data-stu-id="c23d1-116">If you decide after you deploy Archiving that you want to use Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers and all your users are homed on your Exchange 2013 servers, you should remove the SQL Server database configuration from your topology.</span></span> <span data-ttu-id="c23d1-117">您必须使用拓扑生成器执行此操作。</span><span class="sxs-lookup"><span data-stu-id="c23d1-117">You must use Topology Builder to do this.</span></span> <span data-ttu-id="c23d1-118">有关详细信息，请参阅在操作文档中 <A href="lync-server-2013-changing-archiving-database-options.md">更改 Lync Server 2013 中的存档数据库选项</A> 。</span><span class="sxs-lookup"><span data-stu-id="c23d1-118">For details, see <A href="lync-server-2013-changing-archiving-database-options.md">Changing Archiving database options in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-purging-for-archiving"></a><span data-ttu-id="c23d1-119">启用或禁用清除存档</span><span class="sxs-lookup"><span data-stu-id="c23d1-119">To enable or disable purging for archiving</span></span>

1.  <span data-ttu-id="c23d1-120">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="c23d1-120">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="c23d1-121">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="c23d1-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c23d1-122">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="c23d1-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c23d1-123">在左侧导航栏中，单击“监控和存档”，然后单击“存档配置”。</span><span class="sxs-lookup"><span data-stu-id="c23d1-123">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="c23d1-124">单击存档配置列表中相应的全局、站点或池配置的名称，单击“**编辑**”，再单击“**显示详细信息**”，然后执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="c23d1-124">Click the name of the appropriate global, site, or pool configuration in the list of archiving configurations, click **Edit**, click **Show details**, and then do the following:</span></span>
    
      - <span data-ttu-id="c23d1-125">要启用清除，请选中“**启用清除存档数据功能**”复选框，然后执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="c23d1-125">To enable purging, select the **Enable purging of archiving data** check box and then do one of the following:</span></span>
        
          - <span data-ttu-id="c23d1-126">要清除所有记录，请单击“**清除超过以下最长持续时间（天）的已导出存档数据和已存储存档数据**”，然后指定天数。</span><span class="sxs-lookup"><span data-stu-id="c23d1-126">To purge all records, click the **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="c23d1-127">要仅清除已导出的数据，请单击“**仅清除已导出的存档数据**”。</span><span class="sxs-lookup"><span data-stu-id="c23d1-127">To purge only the data that has been exported, click **Purge exported archiving data only**.</span></span>
    
      - <span data-ttu-id="c23d1-128">要禁用清除，请清除“**启用清除存档数据功能**”复选框。</span><span class="sxs-lookup"><span data-stu-id="c23d1-128">To disable purging, clear the **Enable purging of archiving data** check box.</span></span>

5.  <span data-ttu-id="c23d1-129">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="c23d1-129">Click **Commit**.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-the-purging-of-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="c23d1-130">使用 Windows PowerShell Cmdlet 启用或禁用存档数据的清除</span><span class="sxs-lookup"><span data-stu-id="c23d1-130">Enabling or Disabling the Purging of Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="c23d1-131">启用和禁用存档数据的自动清除可以使用 Windows PowerShell 和 **CsArchivingConfiguration** cmdlet 进行管理。</span><span class="sxs-lookup"><span data-stu-id="c23d1-131">Enabling and disabling the automated purging of archiving data can be managed by using Windows PowerShell and the **Set-CsArchivingConfiguration** cmdlet.</span></span> <span data-ttu-id="c23d1-132">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="c23d1-132">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="c23d1-133">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="c23d1-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-purging-of-all-archiving-data"></a><span data-ttu-id="c23d1-134">启用清除所有存档数据</span><span class="sxs-lookup"><span data-stu-id="c23d1-134">To enable the purging of all archiving data</span></span>

  - <span data-ttu-id="c23d1-135">若要启用清除所有存档数据，请将 **EnablePurging** 属性设置为 true ($True) 。</span><span class="sxs-lookup"><span data-stu-id="c23d1-135">To enable the purging of all archiving data set the **EnablePurging** property to true ($True).</span></span> <span data-ttu-id="c23d1-136">例如：</span><span class="sxs-lookup"><span data-stu-id="c23d1-136">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $True
    
    <span data-ttu-id="c23d1-137">运行此命令后，Lync Server 每天将清除早于为 **KeepArchivingDataForDays** 属性指定的值的所有存档记录。</span><span class="sxs-lookup"><span data-stu-id="c23d1-137">After this command is run, then every day Lync Server will purge all archiving records older than the value specified for the **KeepArchivingDataForDays** property.</span></span>

</div>

<div>

## <a name="to-enable-the-purging-only-of-exported-archiving-data"></a><span data-ttu-id="c23d1-138">仅允许清除导出的存档数据</span><span class="sxs-lookup"><span data-stu-id="c23d1-138">To enable the purging only of exported archiving data</span></span>

  - <span data-ttu-id="c23d1-139">若要通过使用 [CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)) cmdlet 限制清除以将已导出到数据文件的记录存档 (，还必须将 PurgeExportedArchivesOnly 属性设置为 True ($True) 。</span><span class="sxs-lookup"><span data-stu-id="c23d1-139">To limit purging to archiving records that have been exported to a data file (by using the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet) you must also set the PurgeExportedArchivesOnly property to True ($True).</span></span> <span data-ttu-id="c23d1-140">例如：</span><span class="sxs-lookup"><span data-stu-id="c23d1-140">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $True -PurgeExportedArchivesOnly $True
    
    <span data-ttu-id="c23d1-141">运行此命令后，Lync Server 将仅清除满足两个条件的存档记录： 1) 它们早于为 **KeepArchivingDataForDays** 属性指定的值;然后，2) 使用 **CsArchivingData** cmdlet 导出它们。</span><span class="sxs-lookup"><span data-stu-id="c23d1-141">After this command is run, Lync Server will only purge archiving records that meet two criteria: 1) they are older than the value specified for the **KeepArchivingDataForDays** property; and, 2) they have been exported by using the **Export-CsArchivingData** cmdlet.</span></span>

</div>

<div>

## <a name="to-disable-the-purging-of-all-archiving-data"></a><span data-ttu-id="c23d1-142">禁用对所有存档数据的清除</span><span class="sxs-lookup"><span data-stu-id="c23d1-142">To disable the purging of all archiving data</span></span>

  - <span data-ttu-id="c23d1-143">若要禁用自动清除存档记录，请将 **EnablePurging** 属性设置为 False ($False) 。</span><span class="sxs-lookup"><span data-stu-id="c23d1-143">To disable the automated purging of archiving records, set the **EnablePurging** property to False ($False).</span></span> <span data-ttu-id="c23d1-144">例如：</span><span class="sxs-lookup"><span data-stu-id="c23d1-144">For example:</span></span>
    
        Set-CsArchivingConfiguration -Identity "site:Redmond" -EnablePurging $False

</div>

<span data-ttu-id="c23d1-145">有关详细信息，包括用于清除存档数据的其他选项，请参阅 [CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="c23d1-145">For more information, including additional options for purging archiving data, see the help topic for the [Set-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c23d1-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c23d1-146">See Also</span></span>


[<span data-ttu-id="c23d1-147">在 Lync Server 2013 中存档的工作方式</span><span class="sxs-lookup"><span data-stu-id="c23d1-147">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="c23d1-148">在 Lync Server 2013 中配置和分配存档策略</span><span class="sxs-lookup"><span data-stu-id="c23d1-148">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)  
[<span data-ttu-id="c23d1-149">管理您的组织、网站和池的 Lync Server 2013 中的存档配置选项</span><span class="sxs-lookup"><span data-stu-id="c23d1-149">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

<span data-ttu-id="c23d1-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c23d1-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

