---
title: Lync Server 2013：规划响应组灾难恢复
description: Lync Server 2013：规划响应组灾难恢复。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for response group disaster recovery
ms:assetid: 14e0f5dc-77cd-42cd-a9c9-4d0da38fb1cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204699(v=OCS.15)
ms:contentKeyID: 48183482
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5294ddf7dbd42d95c5eb17acd6be6a5abc7a5917
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392504"
---
# <a name="planning-for-response-group-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="67c9c-103">在 Lync Server 2013 中规划响应组灾难恢复</span><span class="sxs-lookup"><span data-stu-id="67c9c-103">Planning for response group disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67c9c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67c9c-104">

<span> </span></span></span>

<span data-ttu-id="67c9c-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="67c9c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="67c9c-106">本部分介绍了一些为灾难恢复准备响应组的方法，并提供了灾难恢复过程的概述。</span><span class="sxs-lookup"><span data-stu-id="67c9c-106">This section describes some ways to prepare response groups for disaster recovery and provides an overview of the disaster recovery process.</span></span>

<div>

## <a name="preparing-for-response-group-disaster-recovery"></a><span data-ttu-id="67c9c-107">准备响应组灾难恢复</span><span class="sxs-lookup"><span data-stu-id="67c9c-107">Preparing for Response Group Disaster Recovery</span></span>

<span data-ttu-id="67c9c-108">在准备和执行灾难恢复过程时，请牢记以下事项。</span><span class="sxs-lookup"><span data-stu-id="67c9c-108">Keep the following in mind when you prepare for and carry out disaster recovery procedures.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="67c9c-109">在共存环境中，本文档中所述的灾难恢复过程仅支持 Lync Server 2013 响应组。</span><span class="sxs-lookup"><span data-stu-id="67c9c-109">In a coexistence environment, only the Lync Server 2013 response groups are supported for the disaster recovery procedures described in this document.</span></span>



</div>

  - <span data-ttu-id="67c9c-110">在执行容量规划时规划灾难恢复。</span><span class="sxs-lookup"><span data-stu-id="67c9c-110">Plan for disaster recovery when you do your capacity planning.</span></span> <span data-ttu-id="67c9c-111">对于灾难恢复容量，配对池中的每个池都应该能够处理两个池中所有响应组的工作负荷。</span><span class="sxs-lookup"><span data-stu-id="67c9c-111">For disaster recovery capacity, each pool in a paired pool should be able to handle the workloads of all the response groups in both pools.</span></span> <span data-ttu-id="67c9c-112">有关响应组容量规划的详细信息，请参阅 [Lync Server 2013 中的 "响应" 组的容量规划](lync-server-2013-capacity-planning-for-response-group.md)。</span><span class="sxs-lookup"><span data-stu-id="67c9c-112">For details about Response Group capacity planning, see [Capacity planning for Response Group in Lync Server 2013](lync-server-2013-capacity-planning-for-response-group.md).</span></span>

  - <span data-ttu-id="67c9c-113">通过使用本文档中所述的 export 过程，对部署了响应组应用程序的所有前端池中的所有响应组配置定期制作备份副本。</span><span class="sxs-lookup"><span data-stu-id="67c9c-113">Take regular backup copies of all the response group configurations in all the Front End pools where you deployed the Response Group application by using the export procedure described in this document.</span></span> <span data-ttu-id="67c9c-114">有关详细信息，请参阅 [Lync Server 2013 中的响应组灾难恢复过程](lync-server-2013-response-group-disaster-recovery-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="67c9c-114">For details, see [Response group disaster recovery procedures in Lync Server 2013](lync-server-2013-response-group-disaster-recovery-procedures.md).</span></span> <span data-ttu-id="67c9c-115">将备份副本保存在安全的位置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-115">Keep the backup copies in a safe location.</span></span>

  - <span data-ttu-id="67c9c-116">为您用于响应组应用程序的所有原始音频文件保留一个单独的备份副本，包括所有录制和包含音乐的文件。</span><span class="sxs-lookup"><span data-stu-id="67c9c-116">Keep a separate backup copy of all the original audio files you used for the Response Group application, including any recordings and music-on-hold files.</span></span> <span data-ttu-id="67c9c-117">将备份文件保留在安全的位置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-117">Keep the backup files in a safe location.</span></span>

  - <span data-ttu-id="67c9c-118">对于 Lync Server 2013 灾难恢复，所有响应组设置在你的部署中必须具有唯一的名称。</span><span class="sxs-lookup"><span data-stu-id="67c9c-118">For Lync Server 2013 disaster recovery, all Response Group settings must have unique names across your deployment.</span></span> <span data-ttu-id="67c9c-119">此要求适用于工作流、队列、代理组、假日集和工作时间。</span><span class="sxs-lookup"><span data-stu-id="67c9c-119">This requirement applies to workflows, queues, agent groups, holiday sets, and hours of business.</span></span> <span data-ttu-id="67c9c-120">当主池和备份池仍处于活动状态时，以及在你需要启动任何故障转移过程之前，应验证是否满足此要求。</span><span class="sxs-lookup"><span data-stu-id="67c9c-120">You should verify that this requirement is met when the primary and backup pools are still active, and before you need to initiate any failover procedure.</span></span> <span data-ttu-id="67c9c-121">如果在将响应组数据导入到备份池时遇到名称冲突，则导入失败。</span><span class="sxs-lookup"><span data-stu-id="67c9c-121">If you encounter name conflicts while importing response group data to the backup pool, the import fails.</span></span> <span data-ttu-id="67c9c-122">若要完成导入和故障转移过程，你需要通过在备份池中重命名响应组对象来解决名称冲突，或者通过将 **CsRgsConfiguration** cmdlet 与-ResolveNameConflicts 参数一起使用，通过将唯一的识别号附加到响应组对象来自动解决冲突。</span><span class="sxs-lookup"><span data-stu-id="67c9c-122">To complete the import and failover procedure, you need to resolve the name conflicts by renaming the response group object in the backup pool or by using the **Import-CsRgsConfiguration** cmdlet with the –ResolveNameConflicts parameter to automatically resolve the conflict by appending a unique identifying number to the response group object.</span></span>

  - <span data-ttu-id="67c9c-123">一般情况下，我们建议你执行每日备份，但如果你有大量更改，你可能希望计划更频繁的备份。</span><span class="sxs-lookup"><span data-stu-id="67c9c-123">In general, we recommend that you perform daily backups, but if you have a high volume of changes, you might want to schedule more frequent backups.</span></span> <span data-ttu-id="67c9c-124">灾难发生时可能会丢失的信息量取决于备份的频率，以及更改的频率和数量。</span><span class="sxs-lookup"><span data-stu-id="67c9c-124">The amount of information you can lose in the event of a disaster depends on the frequency of your backups, as well as the frequency and volume of changes.</span></span>

  - <span data-ttu-id="67c9c-125">在发生灾难或故障转移操作之前，可以将响应组导入到备份池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-125">It is possible to import response groups to a backup pool before a disaster or failover operation occurs.</span></span> <span data-ttu-id="67c9c-126">快速导入响应组会减少停机时间，因为一旦呼叫路由到备份池，就可以在备份池中还原 Lync Server 响应组服务。</span><span class="sxs-lookup"><span data-stu-id="67c9c-126">Importing response groups in advance reduces downtime, because the Lync Server Response Group service can be restored in the backup pool as soon as calls are routed to the backup pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="67c9c-127">在故障转移完成之前，响应组应用程序无法访问驻留在非活动池中的任何代理。</span><span class="sxs-lookup"><span data-stu-id="67c9c-127">The Response Group application cannot reach any agents homed in an inactive pool until failover is complete.</span></span> <span data-ttu-id="67c9c-128">在这段时间内，响应组应用程序处理的调用如同这些代理不可用。</span><span class="sxs-lookup"><span data-stu-id="67c9c-128">During this time, the Response Group application processes calls as if those agents are unavailable.</span></span>

    
    </div>

</div>

<div>

## <a name="response-group-disaster-recovery-process"></a><span data-ttu-id="67c9c-129">响应组灾难恢复过程</span><span class="sxs-lookup"><span data-stu-id="67c9c-129">Response Group Disaster Recovery Process</span></span>

<span data-ttu-id="67c9c-130">发生灾难时，您可以使用以下任一恢复方法恢复响应组：</span><span class="sxs-lookup"><span data-stu-id="67c9c-130">In the event of a disaster, you can recover response groups by using either of the following recovery approaches:</span></span>

  - <span data-ttu-id="67c9c-131">故障转移到备份池，然后故障回复到原始池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-131">Fail over to a backup pool and then fail back to the original pool.</span></span>

  - <span data-ttu-id="67c9c-132">故障转移到备份池，使用不同的完全限定的域名创建新池 (FQDN) ，然后将响应组导入新池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-132">Fail over to a backup pool, create a new pool with a different fully qualified domain name (FQDN), and then import the response groups to the new pool.</span></span>

<span data-ttu-id="67c9c-133">在灾难恢复的故障转移阶段，响应组驻留在多个池中：在主池 (中，在) 和备份池中不可用。</span><span class="sxs-lookup"><span data-stu-id="67c9c-133">During the failover phase of disaster recovery, the response groups reside in multiple pools: in the primary pool (which is unavailable) and in the backup pool.</span></span> <span data-ttu-id="67c9c-134">两个池中的响应组具有相同的名称和 (主池) 的所有者，但它们具有不同的父池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-134">The response groups in both pools have the same name and the same owner (the primary pool), but they have different parents.</span></span>

<span data-ttu-id="67c9c-135">通过使用不同的 FQDN 创建新池进行恢复时，你需要在导入时将新的池分配为响应组的所有者。</span><span class="sxs-lookup"><span data-stu-id="67c9c-135">When you recover by creating a new pool with a different FQDN, you need to assign the new pool as the owner of the response groups when you import them.</span></span> <span data-ttu-id="67c9c-136">除非使用-OverwriteOwner 参数和 **CsRgsConfiguration** cmdlet 显式重新分配所有权，否则响应组的所有权将保留原始池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-136">Ownership of response groups remains with the original pool unless or until you explicitly reassign ownership by using the –OverwriteOwner parameter with the **Import-CsRgsConfiguration** cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="67c9c-137">如果在恢复 (中重建池，还需要使用– OverwriteOwner 参数，即，无论是否使用相同的 FQDN，响应组数据库都为空) 。</span><span class="sxs-lookup"><span data-stu-id="67c9c-137">You also need to use the –OverwriteOwner parameter if you rebuilt the pool during the recovery (that is, the Response Group database is empty), whether or not you use the same FQDN.</span></span> <span data-ttu-id="67c9c-138">如果未重新生成池，则无需使用– OverwriteOwner 参数，但可以在将响应组重新导入到主池时使用此参数。</span><span class="sxs-lookup"><span data-stu-id="67c9c-138">You do not need to use the –OverwriteOwner parameter if you did not rebuild the pool, but it is permissible to use this parameter whenever you import response groups back to the primary pool.</span></span>



</div>

<span data-ttu-id="67c9c-139">每个池只能定义一组应用程序级响应组配置设置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-139">You can define only one set of application-level Response Group configuration settings per pool.</span></span> <span data-ttu-id="67c9c-140">这些设置包括默认的音乐保留配置、默认的音乐保留音频文件、代理 ringback 宽限期和呼叫上下文配置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-140">These settings include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="67c9c-141">若要查看这些配置设置，请运行 **CsRgsConfiguration** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67c9c-141">To view these configuration settings, run the **Get-CsRgsConfiguration** cmdlet.</span></span> <span data-ttu-id="67c9c-142">有关 **CsRgsConfiguration** cmdlet 的详细信息，请参阅 [CsRgsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration)。</span><span class="sxs-lookup"><span data-stu-id="67c9c-142">For details about the **Get-CsRgsConfiguration** cmdlet, see [Get-CsRgsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration).</span></span>

<span data-ttu-id="67c9c-143">你可以通过使用 **CsRgsConfiguration** cmdlet 和-ReplaceExistingSettings 参数将这些应用程序级别的设置从一个池中转移到另一个池中，但这样做会覆盖目标池中的设置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-143">You can transfer these application-level settings from one pool to another by using the **Import-CsRgsConfiguration** cmdlet with the –ReplaceExistingSettings parameter, but doing so overrides the settings in the destination pool.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="67c9c-144">有关将设置转移到另一个池的此约束条件仅适用于应用程序级设置和默认的音乐保留音频文件。</span><span class="sxs-lookup"><span data-stu-id="67c9c-144">This constraint about transferring settings to another pool is true only for the application-level settings and the default music-on-hold audio file.</span></span> <span data-ttu-id="67c9c-145">不适用于代理组、队列、工作流、营业时间和假日集。</span><span class="sxs-lookup"><span data-stu-id="67c9c-145">It does not apply to agent groups, queues, workflows, business hours, and holiday sets.</span></span>



</div>

<span data-ttu-id="67c9c-146">如果你不希望在灾难期间替换备份池中的应用程序级设置，并且无法恢复主池，则会丢失主池中的应用程序级别设置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-146">If you don't want to replace the application-level settings in the backup pool during a disaster and the primary pool can't be recovered, the application-level settings from the primary pool will be lost.</span></span> <span data-ttu-id="67c9c-147">如果在恢复期间需要创建新池来替换主池，使用相同的 FQDN 或不同的 FQDN，则不能恢复原始的应用程序级设置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-147">If you need to create a new pool to replace the primary pool during recovery, either with the same FQDN or with a different FQDN, you can't recover the original application-level settings.</span></span> <span data-ttu-id="67c9c-148">在这种情况下，你需要配置具有这些设置的新池，并包括 "音乐保留" 音频文件。</span><span class="sxs-lookup"><span data-stu-id="67c9c-148">In this case, you need to configure the new pool with these settings and include the music-on-hold audio file.</span></span>

<span data-ttu-id="67c9c-149">如果你决定使用 **CsRgsConfiguration** cmdlet 在灾难期间将应用程序级别的主池中的应用程序级别设置转移到备份池，则可以在恢复期间将备份池中的设置转移到新池，方法与将它们从主池转移到备份池的方式相同。</span><span class="sxs-lookup"><span data-stu-id="67c9c-149">If you decide to use the **Import-CsRgsConfiguration** cmdlet to transfer application-level settings from the primary pool to the backup pool during a disaster, you can then transfer the settings from the backup pool to the new pool during recovery in the same way that you transferred them from the primary pool to the backup pool.</span></span>

<span data-ttu-id="67c9c-150">下表概述了恢复响应组所涉及的步骤。</span><span class="sxs-lookup"><span data-stu-id="67c9c-150">The following table is an overview of the steps involved in recovering response groups.</span></span>

<span data-ttu-id="67c9c-151">有关执行这些步骤的详细信息，请参阅 [Lync Server 2013 中的响应组灾难恢复过程](lync-server-2013-response-group-disaster-recovery-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="67c9c-151">For details about performing these steps, see [Response group disaster recovery procedures in Lync Server 2013](lync-server-2013-response-group-disaster-recovery-procedures.md).</span></span>

### <a name="response-group-disaster-recovery-steps"></a><span data-ttu-id="67c9c-152">响应组灾难恢复步骤</span><span class="sxs-lookup"><span data-stu-id="67c9c-152">Response Group Disaster Recovery Steps</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67c9c-153">阶段</span><span class="sxs-lookup"><span data-stu-id="67c9c-153">Phase</span></span></th>
<th><span data-ttu-id="67c9c-154">步骤</span><span class="sxs-lookup"><span data-stu-id="67c9c-154">Steps</span></span></th>
<th><span data-ttu-id="67c9c-155">所需的组和角色</span><span class="sxs-lookup"><span data-stu-id="67c9c-155">Required groups and roles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67c9c-156">停机前</span><span class="sxs-lookup"><span data-stu-id="67c9c-156">Before outage</span></span></p></td>
<td><p><span data-ttu-id="67c9c-157">定期运行 <strong>CsRgsConfiguration</strong> cmdlet，以在部署响应组应用程序的所有前端池内创建所有响应组配置的备份。</span><span class="sxs-lookup"><span data-stu-id="67c9c-157">On a routine basis, run the <strong>Export-CsRgsConfiguration</strong> cmdlet to create backups of all Response Group configurations in all Front End pools where Response Group application is deployed.</span></span></p></td>
<td><p><span data-ttu-id="67c9c-158">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="67c9c-158">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="67c9c-159">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="67c9c-159">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67c9c-160">停机期间</span><span class="sxs-lookup"><span data-stu-id="67c9c-160">During outage</span></span></p></td>
<td><p><span data-ttu-id="67c9c-161">运行 <strong>CsRgsConfiguration</strong> cmdlet 以将备份的 Lync Server 响应组服务配置从主池中导入到备份池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-161">Run the <strong>Import-CsRgsConfiguration</strong> cmdlet to import the backed up Lync Server Response Group service configuration from the primary pool to the backup pool.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="67c9c-162">如果要使用主池中的设置替换备份池中的应用程序级响应组设置，请使用– ReplaceExistingSettings 参数。</span><span class="sxs-lookup"><span data-stu-id="67c9c-162">Use the –ReplaceExistingSettings parameter if you want to replace application-level Response Group settings in the backup pool with the settings from the primary pool.</span></span> <span data-ttu-id="67c9c-163">如果不将应用程序级别的设置从主池转移到备份池，并且无法恢复主池，则将丢失主池中的设置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-163">If you do not transfer the application-level settings from the primary pool to the backup pool, and the primary pool can't be recovered, you will lose the settings from the primary pool.</span></span>


</div></td>
<td><p><span data-ttu-id="67c9c-164">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="67c9c-164">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="67c9c-165">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="67c9c-165">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67c9c-166">导入后</span><span class="sxs-lookup"><span data-stu-id="67c9c-166">After importing</span></span></p></td>
<td><p><span data-ttu-id="67c9c-167">通过-ShowAll 参数 (运行响应组 cmdlet 以显示所有响应组) 或-Owner 参数 (仅显示导入的响应组) 以验证是否已将所有响应组配置导入到备份池中。</span><span class="sxs-lookup"><span data-stu-id="67c9c-167">Run Response Group cmdlets with either the –ShowAll parameter (to display all response groups) or the –Owner parameter (to display only imported response groups) to verify that all response group configurations were imported to the backup pool.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="67c9c-168">如果您不使用– ShowAll 参数或-Owner 参数，则导入到备份池中的响应组将不会在 cmdlet 返回的结果中列出。</span><span class="sxs-lookup"><span data-stu-id="67c9c-168">If you do not use either the –ShowAll parameter or the –Owner parameter, the response groups that you imported to the backup pool will not be listed in the results returned by the cmdlets.</span></span>


</div>
<p><span data-ttu-id="67c9c-169">运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="67c9c-169">Run the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="67c9c-170"><strong>CsRgsWorkflow</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-170"><strong>Get-CsRgsWorkflow</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-171"><strong>CsRgsQueue</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-171"><strong>Get-CsRgsQueue</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-172"><strong>CsRgsAgentGroup</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-172"><strong>Get-CsRgsAgentGroup</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-173"><strong>Get-CsRgsHoursOfBusiness</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-173"><strong>Get-CsRgsHoursOfBusiness</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-174"><strong>CsRgsHolidaySet</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-174"><strong>Get-CsRgsHolidaySet</strong></span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="67c9c-175">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="67c9c-175">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="67c9c-176">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="67c9c-176">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67c9c-177">故障转移后</span><span class="sxs-lookup"><span data-stu-id="67c9c-177">After failover</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="67c9c-178">将测试呼叫放置到已导入到备份池中的响应组，并验证是否正确处理了该呼叫。</span><span class="sxs-lookup"><span data-stu-id="67c9c-178">Place a test call to a response group that was imported to the backup pool and verify that the call is handled correctly.</span></span></p></li>
<li><p><span data-ttu-id="67c9c-179">所有正式代理必须再次登录到备份池上的正式组。</span><span class="sxs-lookup"><span data-stu-id="67c9c-179">All formal agents must sign in again to their formal groups on backup pool.</span></span></p></li>
<li><p><span data-ttu-id="67c9c-180">管理配置更改：</span><span class="sxs-lookup"><span data-stu-id="67c9c-180">Manage configuration changes:</span></span></p>
<p><span data-ttu-id="67c9c-181">备份池中的响应组，无论是导入到备份池还是由备份池拥有，都可以在中断期间进行正常修改。</span><span class="sxs-lookup"><span data-stu-id="67c9c-181">Response groups in the backup pool, whether imported to the backup pool or owned by the backup pool, can be modified as usual during the outage.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="67c9c-182">必须使用 Lync Server Management Shell 管理导入到备份池中的响应组。</span><span class="sxs-lookup"><span data-stu-id="67c9c-182">You must use Lync Server Management Shell to manage the response groups that you imported to the backup pool.</span></span> <span data-ttu-id="67c9c-183">当这些响应组位于备份池中时，无法使用 Lync Server "控制面板" 管理这些响应组。</span><span class="sxs-lookup"><span data-stu-id="67c9c-183">You cannot use Lync Server Control Panel to manage these response groups while they are in the backup pool.</span></span>


</div></li>
</ul></td>
<td><p><span data-ttu-id="67c9c-184">不适用</span><span class="sxs-lookup"><span data-stu-id="67c9c-184">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67c9c-185">恢复后，在故障回复之前</span><span class="sxs-lookup"><span data-stu-id="67c9c-185">After recovery, before failback</span></span></p></td>
<td><p><span data-ttu-id="67c9c-186">运行 <strong>CsRgsConfiguration</strong> cmdlet，将-Source 参数指定为备份池，并将– Owner 参数用作主池，以便从备份池中导出主池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="67c9c-186">Run the <strong>Export-CsRgsConfiguration</strong> cmdlet specifying the -Source parameter as the backup pool and the –Owner parameter as the primary pool to export the response groups owned by the primary pool from the backup pool.</span></span></p></td>
<td><p><span data-ttu-id="67c9c-187">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="67c9c-187">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="67c9c-188">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="67c9c-188">CsResponseGroupAdministrator</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67c9c-189">故障回复后</span><span class="sxs-lookup"><span data-stu-id="67c9c-189">After failback</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="67c9c-190">运行 <strong>CsRgsConfiguration</strong> cmdlet 以将响应组导入回主池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-190">Run the <strong>Import-CsRgsConfiguration</strong> cmdlet to import the response groups back to the primary pool.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="67c9c-191">如果无法恢复主池，并且你部署新池以替换它，请使用-ReplaceExistingSettings 参数将应用程序级别的设置从备份池传输到新池。</span><span class="sxs-lookup"><span data-stu-id="67c9c-191">If the primary pool can't be recovered and you deploy a new pool to replace it, use the –ReplaceExistingSettings parameter to transfer the application-level settings from the backup pool to the new pool.</span></span> <span data-ttu-id="67c9c-192">如果未从备份池中传输设置，新池将使用默认设置。</span><span class="sxs-lookup"><span data-stu-id="67c9c-192">If you do not transfer the settings from the backup pool, the new pool will use the default settings.</span></span>


</div></li>
<li><p><span data-ttu-id="67c9c-193">运行以下 cmdlet 和– ShowAll 参数 (以显示所有响应组) 或-Owner 参数 (仅显示导入的响应组) 验证是否已将所有响应组配置成功导入到主池：</span><span class="sxs-lookup"><span data-stu-id="67c9c-193">Run the following cmdlets with either the –ShowAll parameter (to display all response groups) or the –Owner parameter (to display only imported response groups) to verify that all response group configurations were successfully imported back to the primary pool:</span></span></p>
<ul>
<li><p><span data-ttu-id="67c9c-194"><strong>CsRgsWorkflow</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-194"><strong>Get-CsRgsWorkflow</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-195"><strong>CsRgsQueue</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-195"><strong>Get-CsRgsQueue</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-196"><strong>CsRgsAgentGroup</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-196"><strong>Get-CsRgsAgentGroup</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-197"><strong>Get-CsRgsHoursOfBusiness</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-197"><strong>Get-CsRgsHoursOfBusiness</strong></span></span></p></li>
<li><p><span data-ttu-id="67c9c-198"><strong>CsRgsHolidaySet</strong></span><span class="sxs-lookup"><span data-stu-id="67c9c-198"><strong>Get-CsRgsHolidaySet</strong></span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="67c9c-199">将测试呼叫放入已导入到主池的响应组，并验证是否正确处理了该呼叫。</span><span class="sxs-lookup"><span data-stu-id="67c9c-199">Place a test call to a response group that was imported back to the primary pool and verify that the call is handled correctly.</span></span></p></li>
<li><p><span data-ttu-id="67c9c-200">（可选）使用-RemoveExportedConfiguration 参数在备份池中运行 <strong>Export CsRgsConfiguration</strong> cmdlet，以从备份池中删除主池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="67c9c-200">Optionally, run the <strong>Export-CsRgsConfiguration</strong> cmdlet on the backup pool with the –RemoveExportedConfiguration parameter to remove the response groups owned by the primary pool from the backup pool.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="67c9c-201">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="67c9c-201">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="67c9c-202">CsResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="67c9c-202">CsResponseGroupAdministrator</span></span></p></td><span data-ttu-id="67c9c-203">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67c9c-203">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

