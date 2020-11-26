---
title: Lync Server 2013 响应组灾难恢复过程
description: Lync Server 2013 响应组灾难恢复过程。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group disaster recovery procedures
ms:assetid: b49577b7-0ca3-4f20-b614-f3a2a0046b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205186(v=OCS.15)
ms:contentKeyID: 48185171
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9021fb75c8f937bfd298578a9241d6256d26d85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436298"
---
# <a name="response-group-disaster-recovery-procedures-in-lync-server-2013"></a><span data-ttu-id="e395c-103">Lync Server 2013 中的响应组灾难恢复过程</span><span class="sxs-lookup"><span data-stu-id="e395c-103">Response group disaster recovery procedures in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e395c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e395c-104">

<span> </span></span></span>

<span data-ttu-id="e395c-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e395c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e395c-106">在灾难恢复的故障转移阶段，响应组驻留在多个池中：在主池 (中，在) 和备份池中不可用。</span><span class="sxs-lookup"><span data-stu-id="e395c-106">During the failover phase of disaster recovery, the response groups reside in multiple pools: in the primary pool (which is unavailable) and in the backup pool.</span></span> <span data-ttu-id="e395c-107">两个池中的响应组具有相同的名称和 (主池) 的所有者，但它们具有不同的父池。</span><span class="sxs-lookup"><span data-stu-id="e395c-107">The response groups in both pools have the same name and the same owner (the primary pool), but they have different parents.</span></span> <span data-ttu-id="e395c-108">在这段时间内，响应组 cmdlet 的工作方式略有不同。</span><span class="sxs-lookup"><span data-stu-id="e395c-108">During this time, Response Group cmdlets work a little differently.</span></span> <span data-ttu-id="e395c-109">请确保使用以下过程中指定的参数。</span><span class="sxs-lookup"><span data-stu-id="e395c-109">Be sure to use parameters as specified in the following procedure.</span></span> <span data-ttu-id="e395c-110">有关 cmdlet 在故障转移阶段的工作原理的详细信息，请参阅 NextHop 博客文章 "Lync Server 2013：在灾难恢复期间恢复响应组" [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957) 。</span><span class="sxs-lookup"><span data-stu-id="e395c-110">For details about how cmdlets work during the failover phase, see NextHop blog article "Lync Server 2013: Recovering Response Groups During Disaster Recovery" at [https://go.microsoft.com/fwlink/p/?LinkId=263957](https://go.microsoft.com/fwlink/p/?linkid=263957).</span></span> <span data-ttu-id="e395c-111">此博客文章还适用于 Lync Server 2013 的已发布版本。</span><span class="sxs-lookup"><span data-stu-id="e395c-111">This blog article also applies to the released version of Lync Server 2013.</span></span>

<span data-ttu-id="e395c-112">使用以下过程中的步骤为 Lync Server 响应组服务准备和执行灾难恢复。</span><span class="sxs-lookup"><span data-stu-id="e395c-112">Use the steps in the following procedure to prepare for and perform disaster recovery for Lync Server Response Group service.</span></span>

<div>

## <a name="to-fail-over-and-fail-back-response-group"></a><span data-ttu-id="e395c-113">故障转移和故障回复响应组</span><span class="sxs-lookup"><span data-stu-id="e395c-113">To fail over and fail back Response Group</span></span>

1.  <span data-ttu-id="e395c-114">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="e395c-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="e395c-115">定期执行备份。</span><span class="sxs-lookup"><span data-stu-id="e395c-115">Routinely perform backups.</span></span> <span data-ttu-id="e395c-116">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-116">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="e395c-117">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-117">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimary.zip"

3.  <span data-ttu-id="e395c-118">在中断期间，在故障转移到备份池后，将响应组导入到备份池。</span><span class="sxs-lookup"><span data-stu-id="e395c-118">During an outage, after failover to the backup pool, import the response groups to the backup pool.</span></span> <span data-ttu-id="e395c-119">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-119">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<backup pool FQDN>" -FileName "<backup path and file name>"
    
    <span data-ttu-id="e395c-120">如果要将备份池中的应用程序级设置替换为主池中的设置，请包括-ReplaceExistingSettings 参数。</span><span class="sxs-lookup"><span data-stu-id="e395c-120">If you want to replace the application-level settings in the backup pool with the settings from the primary pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="e395c-121">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-121">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:backup.contoso.com" -FileName "C:\RgsExportPrimary.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="e395c-122">如果不替换备份池中的设置，并且无法恢复主池，则主池设置将丢失。</span><span class="sxs-lookup"><span data-stu-id="e395c-122">If you do not replace the settings in the backup pool and the primary pool can't be recovered, the primary pool settings will be lost.</span></span> <span data-ttu-id="e395c-123">有关详细信息，请参阅 <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">在 Lync Server 2013 中规划响应组灾难恢复</A>。</span><span class="sxs-lookup"><span data-stu-id="e395c-123">For details, see <A href="lync-server-2013-planning-for-response-group-disaster-recovery.md">Planning for response group disaster recovery in Lync Server 2013</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="e395c-124">通过显示导入的响应组来验证导入是否成功。</span><span class="sxs-lookup"><span data-stu-id="e395c-124">Verify that the import was successful by displaying the imported response groups.</span></span> <span data-ttu-id="e395c-125">导入的响应组仍由主池拥有。</span><span class="sxs-lookup"><span data-stu-id="e395c-125">The imported response groups are still owned by the primary pool.</span></span> <span data-ttu-id="e395c-126">执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="e395c-126">Do the following:</span></span>
    
      - <span data-ttu-id="e395c-127">显示由主池拥有的备份池中的所有工作流，并验证是否包含所有主池工作流。</span><span class="sxs-lookup"><span data-stu-id="e395c-127">Display all the workflows in the backup pool that are owned by the primary pool, and verify that all the primary pool workflows are included.</span></span> <span data-ttu-id="e395c-128">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-128">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="e395c-129">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-129">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com"
    
      - <span data-ttu-id="e395c-130">显示由主池拥有的备份池中的所有队列，并验证是否包含所有主池队列。</span><span class="sxs-lookup"><span data-stu-id="e395c-130">Display all the queues in the backup pool that are owned by the primary pool, and verify that all the primary pool queues are included.</span></span> <span data-ttu-id="e395c-131">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-131">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="e395c-132">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-132">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="e395c-133">显示由主池拥有的备份池中的所有代理组，并验证是否包含所有主池代理组。</span><span class="sxs-lookup"><span data-stu-id="e395c-133">Display all the agent groups in the backup pool that are owned by the primary pool, and verify that all the primary pool agent groups are included.</span></span> <span data-ttu-id="e395c-134">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-134">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="e395c-135">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-135">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="e395c-136">显示由主池拥有的备份池中的所有工作时间，并验证是否包括所有主池的工作时间。</span><span class="sxs-lookup"><span data-stu-id="e395c-136">Display all the hours of business in the backup pool that are owned by the primary pool, and verify that all the primary pool hours of business are included.</span></span> <span data-ttu-id="e395c-137">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-137">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="e395c-138">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-138">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
      - <span data-ttu-id="e395c-139">显示由主池拥有的备份池中的所有假日集，并验证是否包含所有主池假日集。</span><span class="sxs-lookup"><span data-stu-id="e395c-139">Display all the holiday sets in the backup pool that are owned by the primary pool, and verify that all the primary pool holiday sets are included.</span></span> <span data-ttu-id="e395c-140">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-140">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer"<primary pool FQDN>
        
        <span data-ttu-id="e395c-141">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-141">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer"primary.contoso.com"
    
    <span data-ttu-id="e395c-142">或者，你可以显示备份池中的所有响应组，包括由主池拥有的所有响应组以及由备份池拥有的所有响应组，方法是使用– ShowAll 参数而不是-Owner 参数。</span><span class="sxs-lookup"><span data-stu-id="e395c-142">Alternatively, you can display all the response groups in the backup pool, including the ones owned by the primary pool and the ones owned by the backup pool by using the –ShowAll parameter instead of the –Owner parameter.</span></span> <span data-ttu-id="e395c-143">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-143">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity "service:ApplicationServer:<backup pool FQDN>" -ShowAll
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e395c-144">你必须使用– ShowAll 参数或– Owner 参数。</span><span class="sxs-lookup"><span data-stu-id="e395c-144">You must use either the –ShowAll parameter or the –Owner parameter.</span></span> <span data-ttu-id="e395c-145">如果不使用这两个参数中的任何一个，则导入到备份池的响应组将不会在 cmdlet 返回的结果中列出。</span><span class="sxs-lookup"><span data-stu-id="e395c-145">If you do not use either of these parameters, the response groups that you imported to the backup pool will not be listed in the results returned by the cmdlets.</span></span>

    
    </div>

5.  <span data-ttu-id="e395c-146">通过在导入的响应组中拨打电话并验证是否正确处理了呼叫，验证导入是否成功。</span><span class="sxs-lookup"><span data-stu-id="e395c-146">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

6.  <span data-ttu-id="e395c-147">请求代理是正式代理组的成员，以登录到备份池中的代理组。</span><span class="sxs-lookup"><span data-stu-id="e395c-147">Request agents who are members of formal agent groups to sign in to their agent groups in the backup pool.</span></span>

7.  <span data-ttu-id="e395c-148">照常管理和修改导入的响应组。</span><span class="sxs-lookup"><span data-stu-id="e395c-148">Manage and modify the imported response groups as usual.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e395c-149">当响应组位于备份池中时，你需要使用 Lync Server Management Shell 管理它们。</span><span class="sxs-lookup"><span data-stu-id="e395c-149">While the response groups are in the backup pool, you need to use Lync Server Management Shell to manage them.</span></span> <span data-ttu-id="e395c-150">无法使用 Lync Server "控制面板" 管理导入到备份池中的响应组。</span><span class="sxs-lookup"><span data-stu-id="e395c-150">You cannot use Lync Server Control Panel to manage the response groups that you imported to the backup pool.</span></span>

    
    </div>

8.  <span data-ttu-id="e395c-151">在还原主池并完成故障回复后，请导出已导入到备份池中的主要池响应组。</span><span class="sxs-lookup"><span data-stu-id="e395c-151">After the primary pool is restored and failback is complete, export the primary pool response groups that were imported to the backup pool.</span></span> <span data-ttu-id="e395c-152">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-152">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source ApplicationServer:<backup pool FQDN> -Owner ApplicationServer:<primary pool FQDN> -FileName "<backup path and file name>"

9.  <span data-ttu-id="e395c-153">将响应组导入回主池。</span><span class="sxs-lookup"><span data-stu-id="e395c-153">Import the response groups back to the primary pool.</span></span> <span data-ttu-id="e395c-154">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-154">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>"
    
    <span data-ttu-id="e395c-155">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-155">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:primary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e395c-156">如果你在恢复期间重新生成池，而不是使用相同或不同的完全限定的域名 (FQDN) ，则需要使用– OverwriteOwner 参数。</span><span class="sxs-lookup"><span data-stu-id="e395c-156">If you rebuild a pool during recovery, whether with the same or a different fully qualified domain name (FQDN), you need to use the –OverwriteOwner parameter.</span></span> <span data-ttu-id="e395c-157">根据经验法则，将响应组导入到主池时，始终可以使用– OverwriteOwner 参数。</span><span class="sxs-lookup"><span data-stu-id="e395c-157">As a rule of thumb, you can always use the –OverwriteOwner parameter when you import response groups back to the primary pool.</span></span>

    
    </div>
    
    <span data-ttu-id="e395c-158">如果你部署了具有相同或不同 FQDN 的新池 () 替换主池，并且想要使用来自新池的备份池中的应用程序级别设置，请包括-ReplaceExistingSettings 参数。</span><span class="sxs-lookup"><span data-stu-id="e395c-158">If you deployed a new pool (with the same or a different FQDN) to replace the primary pool, and you want to use the application-level settings from the backup pool for the new pool, include the –ReplaceExistingSettings parameter.</span></span> <span data-ttu-id="e395c-159">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-159">At the command line, type:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<new primary pool FQDN>" -OverwriteOwner -FileName "<exported path and file name>" -ReplaceExistingSettings
    
    <span data-ttu-id="e395c-160">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-160">For example:</span></span>
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:newprimary.contoso.com" -OverwriteOwner -FileName "C:\RgsExportPrimaryUpdated.zip" -ReplaceExistingSettings
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e395c-161">如果您不想将新池的应用程序级设置和默认的音乐保留音频文件替换为具有备份池中的设置，则新池将使用默认的应用程序级设置。</span><span class="sxs-lookup"><span data-stu-id="e395c-161">If you don't want to replace the application-level settings and default music-on-hold audio file for the new pool with the settings from the backup pool, the new pool will use the default application-level settings.</span></span>

    
    </div>

10. <span data-ttu-id="e395c-162">通过显示导入的响应组配置来验证是否已成功导入到主池。</span><span class="sxs-lookup"><span data-stu-id="e395c-162">Verify that the import back to the primary pool was successful by displaying the imported response group configuration.</span></span> <span data-ttu-id="e395c-163">执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="e395c-163">Do the following:</span></span>
    
      - <span data-ttu-id="e395c-164">显示主池中的所有工作流，并验证是否包含所有导入的工作流。</span><span class="sxs-lookup"><span data-stu-id="e395c-164">Display all the workflows in the primary pool, and verify that all the imported workflows are included.</span></span> <span data-ttu-id="e395c-165">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-165">At the command line, type:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="e395c-166">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-166">For example:</span></span>
        
            Get-CsRgsWorkflow -Identity "service:ApplicationServer: primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="e395c-167">显示主池中的所有队列，并验证是否包含所有导入的队列。</span><span class="sxs-lookup"><span data-stu-id="e395c-167">Display all the queues in the primary pool, and verify that all the imported queues are included.</span></span> <span data-ttu-id="e395c-168">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-168">At the command line, type:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="e395c-169">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-169">For example:</span></span>
        
            Get-CsRgsQueue -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="e395c-170">显示主池中的所有代理组，并验证是否包含所有导入的代理组。</span><span class="sxs-lookup"><span data-stu-id="e395c-170">Display all the agent groups in the primary pool, and verify that all the imported agent groups are included.</span></span> <span data-ttu-id="e395c-171">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-171">At the command line, type:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer: <primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="e395c-172">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-172">For example:</span></span>
        
            Get-CsRgsAgentGroup -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="e395c-173">显示主池中的所有工作时间，并验证是否包括所有导入的公司工时。</span><span class="sxs-lookup"><span data-stu-id="e395c-173">Display all the hours of business in the primary pool, and verify that all the imported hours of business are included.</span></span> <span data-ttu-id="e395c-174">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-174">At the command line, type:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="e395c-175">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-175">For example:</span></span>
        
            Get-CsRgsHoursOfBusiness -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll
    
      - <span data-ttu-id="e395c-176">显示主池中的所有假日集，并验证是否包含所有导入的假日集。</span><span class="sxs-lookup"><span data-stu-id="e395c-176">Display all the holiday sets in the primary pool, and verify that all the imported holiday sets are included.</span></span> <span data-ttu-id="e395c-177">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-177">At the command line, type:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:<primary pool FQDN>" -ShowAll
        
        <span data-ttu-id="e395c-178">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-178">For example:</span></span>
        
            Get-CsRgsHolidaySet -Identity "service:ApplicationServer:primary.contoso.com" -ShowAll

11. <span data-ttu-id="e395c-179">通过在导入的响应组中拨打电话并验证是否正确处理了呼叫，验证导入是否成功。</span><span class="sxs-lookup"><span data-stu-id="e395c-179">Verify that the import was successful by placing a call to an imported response group and verifying that the call is handled correctly.</span></span>

12. <span data-ttu-id="e395c-180">（可选）从备份池中删除主池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="e395c-180">Optionally, remove the response groups owned by the primary pool from the backup pool.</span></span> <span data-ttu-id="e395c-181">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e395c-181">At the command line, type:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<backup pool FQDN>" -Owner "service:ApplicationServer:<primary pool FQDN>" -FileName "<backup path and file name>" -RemoveExportedConfiguration
    
    <span data-ttu-id="e395c-182">例如：</span><span class="sxs-lookup"><span data-stu-id="e395c-182">For example:</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:backup.contoso.com" -Owner "service:ApplicationServer:primary.contoso.com" -FileName "C:\RgsExportPrimaryUpdated.zip" -RemoveExportedConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e395c-183">此步骤将使用导出的配置创建一个新文件，然后将其从备份池中删除。</span><span class="sxs-lookup"><span data-stu-id="e395c-183">This step creates a new file with the exported configuration, and then removes it from the backup pool.</span></span>

    
    <span data-ttu-id="e395c-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e395c-184"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

