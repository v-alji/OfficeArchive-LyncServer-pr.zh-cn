---
title: Lync Server 2013：创建存档配置以管理特定网站或池的存档
description: Lync Server 2013：创建存档配置以管理特定网站或池的存档。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving configuration to manage Archiving for specific sites or pools
ms:assetid: c5c864a6-96c7-4bbb-ab7c-61eb1744246c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205251(v=OCS.15)
ms:contentKeyID: 48185361
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ab19f2d8900693ef0fcb14d8f6d862b22c355bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431531"
---
# <a name="creating-an-archiving-configuration-in-lync-server-2013-to-manage-archiving-for-specific-sites-or-pools"></a><span data-ttu-id="41a4d-103">在 Lync Server 2013 中创建存档配置以管理特定网站或池的存档</span><span class="sxs-lookup"><span data-stu-id="41a4d-103">Creating an Archiving configuration in Lync Server 2013 to manage Archiving for specific sites or pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41a4d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41a4d-104">

<span> </span></span></span>

<span data-ttu-id="41a4d-105">_**主题上次修改时间：** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="41a4d-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="41a4d-106">在 Lync Server 2013 "控制面板" 中，使用存档配置控制在部署中实现存档的方式。</span><span class="sxs-lookup"><span data-stu-id="41a4d-106">In Lync Server 2013 Control Panel, you use Archiving configurations to control how archiving is implemented in your deployment.</span></span> <span data-ttu-id="41a4d-107">这包括以下存档配置：</span><span class="sxs-lookup"><span data-stu-id="41a4d-107">This includes the following Archiving configurations:</span></span>

  - <span data-ttu-id="41a4d-108">部署 Lync Server 2013 时默认创建的全局配置。</span><span class="sxs-lookup"><span data-stu-id="41a4d-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="41a4d-109">可创建和使用的可选网站级和池级配置，用于指定如何为特定网站或池实现存档。</span><span class="sxs-lookup"><span data-stu-id="41a4d-109">Optional site-level and pool-level configurations that you can create and use to specify how archiving is implemented for specific sites or pools.</span></span>

<span data-ttu-id="41a4d-110">你在部署存档时开始设置存档配置，但你可以在部署后更改、添加和删除配置。</span><span class="sxs-lookup"><span data-stu-id="41a4d-110">You initially set up Archiving configurations when you deploy Archiving, but you can change, add, and delete configurations after deployment.</span></span> <span data-ttu-id="41a4d-111">有关如何实现存档配置的详细信息，包括你可以指定哪些选项和存档配置的层次结构，请参阅规划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="41a4d-111">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="41a4d-112">若要使用存档，必须配置存档策略以指定是为内部通信启用存档、对于外部通信还是对驻留在 Lync Server 2013 上的用户启用存档。</span><span class="sxs-lookup"><span data-stu-id="41a4d-112">To use archiving, you must configure Archiving policies to specify whether to enable archiving for internal communications, for external communications, or for both for users homed on Lync Server 2013.</span></span> <span data-ttu-id="41a4d-113">默认情况下，不会为内部或外部通信启用存档。</span><span class="sxs-lookup"><span data-stu-id="41a4d-113">By default, archiving is not enabled for either internal or external communications.</span></span> <span data-ttu-id="41a4d-114">在任何策略中启用存档之前，应为你的部署指定相应的存档配置，并根据需要为特定的网站和池指定相应的存档配置，如本节所述。</span><span class="sxs-lookup"><span data-stu-id="41a4d-114">Before enabling Archiving in any policies, you should specify the appropriate Archiving configurations for your deployment and, optionally, for specific sites and pools, as described in this section.</span></span> <span data-ttu-id="41a4d-115">有关启用存档的详细信息，请参阅部署文档中的 <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">在 Lync Server 2013 中配置和分配存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="41a4d-115">For details about enabling Archiving, see <A href="lync-server-2013-configuring-and-assigning-archiving-policies.md">Configuring and assigning Archiving policies in Lync Server 2013</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="41a4d-116">如果你在部署要使用 Microsoft Exchange 集成来存储 Exchange 2013 服务器上的存档数据和文件的存档之后，并且你的所有用户都托管在 Exchange 2013 服务器上，则应从拓扑中删除 SQL Server 数据库配置。</span><span class="sxs-lookup"><span data-stu-id="41a4d-116">If you decide after you deploy Archiving that you want to use Microsoft Exchange integration to store archiving data and files on Exchange 2013 servers and all your users are homed on your Exchange 2013 servers, you should remove the SQL Server database configuration from your topology.</span></span> <span data-ttu-id="41a4d-117">您必须使用拓扑生成器执行此操作。</span><span class="sxs-lookup"><span data-stu-id="41a4d-117">You must use Topology Builder to do this.</span></span> <span data-ttu-id="41a4d-118">有关详细信息，请参阅在操作文档中 <A href="lync-server-2013-changing-archiving-database-options.md">更改 Lync Server 2013 中的存档数据库选项</A> 。</span><span class="sxs-lookup"><span data-stu-id="41a4d-118">For details, see <A href="lync-server-2013-changing-archiving-database-options.md">Changing Archiving database options in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-configuration-for-a-site-or-pool"></a><span data-ttu-id="41a4d-119">为网站或池创建存档配置</span><span class="sxs-lookup"><span data-stu-id="41a4d-119">To create an archiving configuration for a site or pool</span></span>

1.  <span data-ttu-id="41a4d-120">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="41a4d-120">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="41a4d-121">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="41a4d-121">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="41a4d-122">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="41a4d-122">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="41a4d-123">在左侧导航栏中，单击“监控和存档”，然后单击“存档配置”。</span><span class="sxs-lookup"><span data-stu-id="41a4d-123">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="41a4d-124">在“**存档配置**”页上，单击“**新建**”，然后执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="41a4d-124">On the **Archiving Configuration** page, click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="41a4d-125">若要创建网站存档配置，请单击 " **网站配置** "，然后在 " **选择网站**" 中选择要为存档配置的网站。</span><span class="sxs-lookup"><span data-stu-id="41a4d-125">To create a site archiving configuration, click **Site Configuration** and then, in **Select a site**, select the site to be configured for archiving.</span></span>
    
      - <span data-ttu-id="41a4d-126">若要创建池存档配置，请单击 " **池配置** "，然后在 " **选择池**" 中选择要为存档配置的池。</span><span class="sxs-lookup"><span data-stu-id="41a4d-126">To create a pool archiving configuration, click **Pool Configuration** and then, in **Select a pool**, select the pool to be configured for archiving.</span></span>

5.  <span data-ttu-id="41a4d-127">在“**新建存档设置**”的“**存档设置**”下拉列表框中，执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="41a4d-127">In **New Archiving Setting**, in the **Archiving setting** drop-down list box, do one of the following:</span></span>
    
      - <span data-ttu-id="41a4d-128">若要只为即时消息 (IM) 会话启用存档，请单击“**存档 IM 会话**”。</span><span class="sxs-lookup"><span data-stu-id="41a4d-128">To enable archiving only for instant messaging (IM) sessions, click **Archive IM sessions**.</span></span>
    
      - <span data-ttu-id="41a4d-129">若要为 IM 会话和 Web 会议启用存档，请单击“**存档 IM 和 Web 会议会话**”。</span><span class="sxs-lookup"><span data-stu-id="41a4d-129">To enable archiving for both IM sessions and web conferences, click **Archive IM and web conferencing sessions**.</span></span>
    
      - <span data-ttu-id="41a4d-130">若要为策略禁用存档，请单击“**禁用存档**”。</span><span class="sxs-lookup"><span data-stu-id="41a4d-130">To disable archiving for the policy, click **Disable archiving**.</span></span>

6.  <span data-ttu-id="41a4d-131">另请在“**新建存档设置**”中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="41a4d-131">Also in **New Archiving Setting**, do the following:</span></span>
    
      - <span data-ttu-id="41a4d-132">要在存档不可用时阻止活动，请选中“**存档失败时阻止即时消息 (IM) 或 Web 会议会话**”复选框。</span><span class="sxs-lookup"><span data-stu-id="41a4d-132">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="41a4d-133">若要使用 Microsoft Exchange Server 存储存档数据，请单击 " **Microsoft exchange 集成** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="41a4d-133">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="41a4d-134">若要启用数据清除，请选中“**启用存档数据清除**”复选框，然后执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="41a4d-134">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="41a4d-135">要指定在特定的天数之后清除，请单击“**在最长期限（天）后清除导出的存档数据和存储的存档数据**”，然后指定天数。</span><span class="sxs-lookup"><span data-stu-id="41a4d-135">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="41a4d-136">要限制仅清除已导出的存档数据，请单击“**仅清除导出的存档数据**”。</span><span class="sxs-lookup"><span data-stu-id="41a4d-136">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

7.  <span data-ttu-id="41a4d-137">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="41a4d-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-archiving-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="41a4d-138">使用 Windows PowerShell Cmdlet 创建存档配置设置</span><span class="sxs-lookup"><span data-stu-id="41a4d-138">Creating Archiving Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="41a4d-139">可以使用 Windows PowerShell 和 New-CsArchivingConfiguration cmdlet 创建存档配置设置。</span><span class="sxs-lookup"><span data-stu-id="41a4d-139">Archiving configuration settings can be created by using Windows PowerShell and the New-CsArchivingConfiguration cmdlet.</span></span> <span data-ttu-id="41a4d-140">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="41a4d-140">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="41a4d-141">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="41a4d-141">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-archiving-configuration-settings-for-a-site"></a><span data-ttu-id="41a4d-142">为网站创建新的存档配置设置集合</span><span class="sxs-lookup"><span data-stu-id="41a4d-142">To create a new collection of archiving configuration settings for a site</span></span>

  - <span data-ttu-id="41a4d-143">以下命令为 Redmond 站点创建一个新的存档配置设置集合：</span><span class="sxs-lookup"><span data-stu-id="41a4d-143">The following command creates a new collection of archiving configuration settings for the Redmond site:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-collection-of-archiving-configuration-settings-that-only-allow-im-archiving"></a><span data-ttu-id="41a4d-144">创建仅允许 IM 存档的一组新的存档配置设置</span><span class="sxs-lookup"><span data-stu-id="41a4d-144">To create a new collection of archiving configuration settings that only allow IM archiving</span></span>

  - <span data-ttu-id="41a4d-145">由于上述命令中未指定参数（不包括必需的 Identity 参数），新的配置设置集合的所有属性都将使用默认值。</span><span class="sxs-lookup"><span data-stu-id="41a4d-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span> <span data-ttu-id="41a4d-146">要创建使用不同属性值的设置，只需包含相应的参数和参数值。</span><span class="sxs-lookup"><span data-stu-id="41a4d-146">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="41a4d-147">例如，若要创建存档配置设置的集合，默认情况下允许存档即时消息会话，请仅使用如下所示的命令：</span><span class="sxs-lookup"><span data-stu-id="41a4d-147">For example, to create a collection of archiving configuration settings that, by default, allow archiving of instant messaging sessions, only use a command like this:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly"

</div>

<div>

## <a name="to-specify-multiple-property-values-when-creating-archiving-configuration-settings"></a><span data-ttu-id="41a4d-148">创建存档配置设置时指定多个属性值</span><span class="sxs-lookup"><span data-stu-id="41a4d-148">To specify multiple property values when creating archiving configuration settings</span></span>

  - <span data-ttu-id="41a4d-p108">可以通过包含多个参数来修改多个属性值。例如，以下命令将新设置配置为存档即时消息会话并阻止不可用的存档服务的即时消息：</span><span class="sxs-lookup"><span data-stu-id="41a4d-p108">Multiple property values can be modified by including multiple parameters. For example, this command configures the new settings to archive instant messaging sessions and to block instant messaging of the archiving service is not available:</span></span>
    
        New-CsArchivingConfiguration -Identity "site:Redmond" -EnableArchiving "ImOnly" -BlockOnArchiveFailure $True

</div>

<span data-ttu-id="41a4d-151">有关详细信息，请参阅 [CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="41a4d-151">For more information, see the help topic for the [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="41a4d-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41a4d-152">See Also</span></span>


[<span data-ttu-id="41a4d-153">在 Lync Server 2013 中存档的工作方式</span><span class="sxs-lookup"><span data-stu-id="41a4d-153">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="41a4d-154">管理您的组织、网站和池的 Lync Server 2013 中的存档配置选项</span><span class="sxs-lookup"><span data-stu-id="41a4d-154">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)  
  

<span data-ttu-id="41a4d-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41a4d-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

