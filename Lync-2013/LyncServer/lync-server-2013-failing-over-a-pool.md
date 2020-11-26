---
title: Lync Server 2013：对池进行故障转移
description: Lync Server 2013：故障转移池。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a pool
ms:assetid: 10b13732-bc80-4cb2-a71c-56b1d6cb5bbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204678(v=OCS.15)
ms:contentKeyID: 48183432
ms.date: 10/10/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 819137c1277c5058f4e5d36ef5dbe71e672e8641
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428263"
---
# <a name="failing-over-a-pool-in-lync-server-2013"></a><span data-ttu-id="0cdca-103">在 Lync Server 2013 中对池进行故障转移</span><span class="sxs-lookup"><span data-stu-id="0cdca-103">Failing over a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0cdca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0cdca-104">

<span> </span></span></span>

<span data-ttu-id="0cdca-105">_**主题上次修改时间：** 2014-10-10_</span><span class="sxs-lookup"><span data-stu-id="0cdca-105">_**Topic Last Modified:** 2014-10-10_</span></span>

<span data-ttu-id="0cdca-106">如果单个前端池出现故障且需要故障转移，请使用以下过程。</span><span class="sxs-lookup"><span data-stu-id="0cdca-106">If a single Front End pool has failed and needs to be failed over, use the following procedure.</span></span> <span data-ttu-id="0cdca-107">在此过程中，Datacenter1 包含 Pool1，而 Pool1 失败。</span><span class="sxs-lookup"><span data-stu-id="0cdca-107">In this procedure, Datacenter1 contains Pool1, and Pool1 has failed.</span></span> <span data-ttu-id="0cdca-108">您将在 Datacenter2 中故障转移到 Pool2。</span><span class="sxs-lookup"><span data-stu-id="0cdca-108">You are failing over to Pool2 located in Datacenter2.</span></span>

<span data-ttu-id="0cdca-109">对于池故障转移，大部分工作都涉及到中央管理存储的故障（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="0cdca-109">Most of the work for the pool failover involves failing over the Central Management store, if it is required.</span></span> <span data-ttu-id="0cdca-110">这一点很重要，因为中央管理存储在池的用户故障转移时必须正常工作。</span><span class="sxs-lookup"><span data-stu-id="0cdca-110">This is important because the Central Management store must be functional when the pool’s users are failed over.</span></span>

<span data-ttu-id="0cdca-111">此外，如果前端池出现故障，但该站点上的边缘池仍在运行，则必须知道 Edge 池是否将失败的池用作下一个跃点池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-111">Additionally, if a Front End pool fails but the Edge pool at that site is still running, you must know whether the Edge pool uses the failed pool as a next hop pool.</span></span> <span data-ttu-id="0cdca-112">如果是，则必须将 Edge 池更改为使用不同的前端池，然后再进行故障转移失败的前端池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-112">If it does, you must change the Edge pool to use a different Front End pool before failing over the failed Front End pool.</span></span> <span data-ttu-id="0cdca-113">更改下一个跃点设置的方式取决于边缘是将同一站点上的池用作边缘池还是其他网站。</span><span class="sxs-lookup"><span data-stu-id="0cdca-113">How you change the next hop setting depends on whether the Edge will use a pool at the same site as the Edge pool, or a different site.</span></span>

<span data-ttu-id="0cdca-114">**将 "边缘池" 设置为在同一站点使用下一个跃点池**</span><span class="sxs-lookup"><span data-stu-id="0cdca-114">**To Set an Edge Pool to Use a Next Hop Pool at the Same Site**</span></span>

1.  <span data-ttu-id="0cdca-115">打开拓扑生成器，右键单击需要更改的边缘池，然后单击 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="0cdca-115">Open Topology Builder, right-click the Edge pool that needs to be changed, and click **Edit Properties**.</span></span>

2.  <span data-ttu-id="0cdca-116">单击 " **下一跃点**"。</span><span class="sxs-lookup"><span data-stu-id="0cdca-116">Click **Next Hop**.</span></span> <span data-ttu-id="0cdca-117">从 **下一个 "跃点池：** " 列表中，选择现在将用作下一个跃点池的池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-117">From the **Next hop pool:** list, select the pool which will now serve as the next hop pool.</span></span>

3.  <span data-ttu-id="0cdca-118">单击 **"确定**"，然后发布所做的更改。</span><span class="sxs-lookup"><span data-stu-id="0cdca-118">Click **OK**, and then publish the changes.</span></span>

<span data-ttu-id="0cdca-119">**将边缘池设置为在其他网站上使用下一个跃点池**</span><span class="sxs-lookup"><span data-stu-id="0cdca-119">**To Set an Edge Pool to Use a Next Hop Pool at a Different Site**</span></span>

1.  <span data-ttu-id="0cdca-120">打开 Lync Server Management Shell 窗口，键入以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="0cdca-120">Open a Lync Server Management Shell window and type the following cmdlet:</span></span>
    
        Set-CsEdgeServer -Identity EdgeServer:<Edge Server pool FQDN> -Registrar Registrar:<NextHopPoolFQDN>

<span data-ttu-id="0cdca-121">**在灾难中故障转移池**</span><span class="sxs-lookup"><span data-stu-id="0cdca-121">**To Fail Over a Pool in a Disaster**</span></span>

1.  <span data-ttu-id="0cdca-122">通过在 Pool2 中的前端服务器上键入以下 cmdlet 来查找哪个池是中央管理服务器的主机：</span><span class="sxs-lookup"><span data-stu-id="0cdca-122">Find which pool is the host for the Central Management Server by typing the following cmdlet on a Front End server in Pool2:</span></span>
    
        Invoke-CsManagementServerFailover -Whatif
    
    <span data-ttu-id="0cdca-123">此 cmdlet 的结果显示当前托管中央管理服务器的池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-123">The results of this cmdlet show which pool currently hosts the Central Management Server.</span></span> <span data-ttu-id="0cdca-124">在此过程的其余部分中，此池称为 CMS \_ 池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-124">In the rest of this procedure, this pool is known as CMS\_Pool.</span></span>

2.  <span data-ttu-id="0cdca-125">使用拓扑生成器查找 CMS 池中运行的 Lync Server 版本 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0cdca-125">Use Topology Builder to find the version of Lync Server running on the CMS\_Pool.</span></span> <span data-ttu-id="0cdca-126">如果它运行的是 Lync Server 2013，请使用以下 cmdlet 查找池1的备份池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-126">If it is running Lync Server 2013, use the following cmdlet to find the backup pool of Pool 1.</span></span>
    
        Get-CsPoolBackupRelationship -PoolFQDN <CMS_Pool FQDN>
    
    <span data-ttu-id="0cdca-127">让备份池 \_ 成为备份池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-127">Let Backup\_Pool be the backup pool.</span></span>

3.  <span data-ttu-id="0cdca-128">通过以下 cmdlet 检查中央管理存储的状态：</span><span class="sxs-lookup"><span data-stu-id="0cdca-128">Check the status of the Central Management store with the following cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
    
    <span data-ttu-id="0cdca-129">此 cmdlet 应显示 ActiveMasterFQDN 和 ActiveFileTransferAgents 都指向 CMS 池的 FQDN \_ 。</span><span class="sxs-lookup"><span data-stu-id="0cdca-129">This cmdlet should show that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of CMS\_Pool.</span></span> <span data-ttu-id="0cdca-130">如果它们为空，则中央管理服务器不可用，您必须将其故障转移。</span><span class="sxs-lookup"><span data-stu-id="0cdca-130">If they are empty, the Central Management Server is not available and you must fail it over.</span></span>

4.  <span data-ttu-id="0cdca-131">如果中央管理存储不可用，或者中央管理存储在 Pool1 上运行 (即) 失败的池，则必须先通过中央管理服务器进行故障转移，然后才能故障转移池。</span><span class="sxs-lookup"><span data-stu-id="0cdca-131">If the Central Management store is not available or if the Central Management store was running on Pool1 (that is, the pool that has failed), you must fail over the Central Management Server before failing over the pool.</span></span> <span data-ttu-id="0cdca-132">如果需要故障转移运行 Lync Server 2013 的池上托管的中央管理服务器，请使用此过程步骤5中的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cdca-132">If you need to fail over the Central Management Server that was hosted on a pool running Lync Server 2013, use the cmdlet in step 5 of this procedure.</span></span> <span data-ttu-id="0cdca-133">如果需要故障转移运行 Lync Server 2010 的池上托管的中央管理服务器，请使用此过程步骤6中的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cdca-133">If you need to fail over the Central Management Server that was hosted on a pool running Lync Server 2010, use the cmdlet in step 6 of this procedure.</span></span> <span data-ttu-id="0cdca-134">如果不需要故障转移中央管理服务器，请跳到此过程的步骤7。</span><span class="sxs-lookup"><span data-stu-id="0cdca-134">If you do not need to fail over the Central Management Server, skip to step 7 of this procedure.</span></span>

5.  <span data-ttu-id="0cdca-135">若要在运行 Lync Server 2013 的池上故障转移中央管理存储，请执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="0cdca-135">To fail over the Central Management store on a pool running Lync Server 2013, do the following:</span></span>
    
      - <span data-ttu-id="0cdca-136">首先，检查备份池中的后端服务器 \_ 通过键入以下内容来运行中央管理存储的主体实例：</span><span class="sxs-lookup"><span data-stu-id="0cdca-136">First, check which Back End Server in Backup\_Pool runs the principal instance of the Central Management store by typing the following:</span></span>
        
            Get-CsDatabaseMirrorState -DatabaseType Centralmgmt -PoolFqdn <Backup_Pool Fqdn>
    
      - <span data-ttu-id="0cdca-137">如果备份池中的主后端服务器 \_ 是主体，请键入：</span><span class="sxs-lookup"><span data-stu-id="0cdca-137">If the primary Back End Server in Backup\_Pool is the principal, type:</span></span>
        
            Invoke-CSManagementServerFailover -BackupSQLServerFqdn <Backup_Pool Primary BackEnd Server FQDN> -BackupSQLInstanceName <Backup_Pool Primary SQL Instance Name>
        
        <span data-ttu-id="0cdca-138">如果备份池中的镜像后端服务器 \_ 是主体，请键入：</span><span class="sxs-lookup"><span data-stu-id="0cdca-138">If the mirror Back End Server in Backup\_Pool is the principal, type:</span></span>
        
            Invoke-CSManagementServerFailover -MirrorSQLServerFqdn <Backup_Pool Mirror BackEnd Server FQDN> -MirrorSQLInstanceName <Backup_Pool Mirror SQL Instance Name>
    
      - <span data-ttu-id="0cdca-139">验证中央管理服务器故障转移是否已完成。</span><span class="sxs-lookup"><span data-stu-id="0cdca-139">Validate that the Central Management Server failover is complete.</span></span> <span data-ttu-id="0cdca-140">键入以下内容：</span><span class="sxs-lookup"><span data-stu-id="0cdca-140">Type the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
        
        <span data-ttu-id="0cdca-141">检查 ActiveMasterFQDN 和 ActiveFileTransferAgents 是否都指向备份池的 FQDN \_ 。</span><span class="sxs-lookup"><span data-stu-id="0cdca-141">Check that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="0cdca-142">最后，通过键入以下内容检查所有前端服务器的副本状态：</span><span class="sxs-lookup"><span data-stu-id="0cdca-142">Finally, check the replica status for all Front End Servers by typing the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus 
        
        <span data-ttu-id="0cdca-143">检查所有副本的值是否均为 True。</span><span class="sxs-lookup"><span data-stu-id="0cdca-143">Check that all replicas have a value of True.</span></span>
        
        <span data-ttu-id="0cdca-144">跳转到此过程中的步骤7。</span><span class="sxs-lookup"><span data-stu-id="0cdca-144">Skip to step 7 in this procedure.</span></span>

6.  <span data-ttu-id="0cdca-145">在备份池的后端服务器上安装中央管理存储 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0cdca-145">Install the Central Management store on the Back End Server of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="0cdca-146">首先，运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="0cdca-146">First, run the following command:</span></span>
        
        ```PowerShell 
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn <Backup_Pool Back End Server FQDN> -SqlInstanceName rtc  
        ```
    
      - <span data-ttu-id="0cdca-147">在备份池的前端服务器之一上运行下一个命令 \_ 以强制移动中央管理存储：</span><span class="sxs-lookup"><span data-stu-id="0cdca-147">Run the next command on one of the Front End Servers of Backup\_Pool to force the move of the Central Management store:</span></span>
        
            Move-CsManagementServer -ConfigurationFileName c:\CsConfigurationFile.zip -LisConfigurationFileName c:\CsLisConfigurationFile.zip -Force 
    
      - <span data-ttu-id="0cdca-148">验证移动是否已完成：</span><span class="sxs-lookup"><span data-stu-id="0cdca-148">Validate the move is complete:</span></span>
        
            Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
        
        <span data-ttu-id="0cdca-149">检查 ActiveMasterFQDN 和 ActiveFileTransferAgents 是否都指向备份池的 FQDN \_ 。</span><span class="sxs-lookup"><span data-stu-id="0cdca-149">Check that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="0cdca-150">通过键入以下内容检查所有前端服务器的副本状态：</span><span class="sxs-lookup"><span data-stu-id="0cdca-150">Check the replica status for all Front End Servers by typing the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus 
        
        <span data-ttu-id="0cdca-151">检查所有副本的值是否均为 True。</span><span class="sxs-lookup"><span data-stu-id="0cdca-151">Check that all replicas have a value of True.</span></span>
    
      - <span data-ttu-id="0cdca-152">在备份池中的其他前端服务器上安装中央管理服务器服务 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0cdca-152">Install the Central Management Server service on the rest of the Front End Servers in Backup\_Pool.</span></span> <span data-ttu-id="0cdca-153">若要执行此操作，请在所有前端服务器上运行以下命令，除了在此过程前面强制执行中央管理存储移动时使用的所有服务器：</span><span class="sxs-lookup"><span data-stu-id="0cdca-153">To do so, run the following command on all the Front End Servers, except the one you used when forcing the Central Management store move earlier in this procedure:</span></span>
        
            Bootstrapper /Setup 

7.  <span data-ttu-id="0cdca-154">通过在 Lync Server Management Shell 窗口中运行以下 cmdlet，将用户从 Pool1 故障转移到 Pool2：</span><span class="sxs-lookup"><span data-stu-id="0cdca-154">Fail over the users from Pool1 to Pool2 by running the following cmdlet in a Lync Server Management Shell window:</span></span>
    
        Invoke-CsPoolFailover -PoolFQDN <Pool1 FQDN> -DisasterMode -Verbose
    
    <span data-ttu-id="0cdca-155">由于本过程的前面部分中所执行的检查中央管理存储状态的步骤不是通用的，因此此 cmdlet 仍会失败，因为中央管理存储尚未完全故障转移。</span><span class="sxs-lookup"><span data-stu-id="0cdca-155">Because the steps taken in the previous parts of this procedure to check the Central Management store status are not universal, there is still a chance this cmdlet will fail because the Central Management store is not yet fully failed over.</span></span> <span data-ttu-id="0cdca-156">在这种情况下，你必须根据你看到的错误消息修复中央管理存储，然后再次运行此 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cdca-156">In this case, you must fix the Central Management store based on the error messages that you see, and then run this cmdlet again.</span></span>
    
    <span data-ttu-id="0cdca-157">如果你看到以下错误消息，则你需要更改此网站上的边缘池，以便在对池进行故障转移之前使用其他池作为下一个跃点。</span><span class="sxs-lookup"><span data-stu-id="0cdca-157">If you see the following error message, then you need to change the Edge pool at this site to use a different pool as its next hop before failing over the pool.</span></span> <span data-ttu-id="0cdca-158">有关详细信息，请参阅本主题开头的过程。</span><span class="sxs-lookup"><span data-stu-id="0cdca-158">For details, see the procedures at the beginning of this topic.</span></span>
    
        Invoke-CsPoolFailOver : This Front-end pool "pool1.contoso.com" is specified in
        topology as the next hop for the Edge server. Failing over this pool may cause External
        access/Federation/Split-domain/XMPP features to stop working. Please use Topology Builder to
        change the Edge internal next hop setting to point to a different Front-end pool,  before you
        proceed.

<span data-ttu-id="0cdca-159"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0cdca-159"></div>

<span> </span>

</div>

</div>

</span></span></div>

