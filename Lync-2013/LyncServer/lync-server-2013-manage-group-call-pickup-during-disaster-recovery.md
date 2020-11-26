---
title: Lync Server 2013：在灾难恢复过程中管理组呼叫装货
description: Lync Server 2013：在灾难恢复期间管理组呼叫装货。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Group Call Pickup during disaster recovery
ms:assetid: 2d32f19f-c649-4a72-a4fb-edd338e3a7cc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945618(v=OCS.15)
ms:contentKeyID: 51541455
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 04d85bc83cfe35571c2b0f47f707c9dcd8037d80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426100"
---
# <a name="manage-group-call-pickup-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="4e520-103">在 Lync Server 2013 中的灾难恢复期间管理组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="4e520-103">Manage Group Call Pickup during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4e520-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4e520-104">

<span> </span></span></span>

<span data-ttu-id="4e520-105">_**主题上次修改时间：** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="4e520-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="4e520-106">当前端池因计划外事件而变为不可用时，服务将故障转移到备份池。</span><span class="sxs-lookup"><span data-stu-id="4e520-106">When a Front End pool becomes unavailable due an unplanned incident, service is failed over to the backup pool.</span></span> <span data-ttu-id="4e520-107">在故障转移到备份池的过程中，用户将被重定向到备份池并处于复原模式。</span><span class="sxs-lookup"><span data-stu-id="4e520-107">During failover to the backup pool, users are redirected to the backup pool and are in resiliency mode.</span></span> <span data-ttu-id="4e520-108">在弹性模式下，用户无法获取其他用户的通话或让其他用户能够接听呼叫。</span><span class="sxs-lookup"><span data-stu-id="4e520-108">While in resiliency mode, users cannot pick up other users' calls or have their calls picked up by other users.</span></span> <span data-ttu-id="4e520-109">故障转移完成后，用户可以再次使用群组呼叫分拣。</span><span class="sxs-lookup"><span data-stu-id="4e520-109">When failover is complete, users can again use Group Call Pickup as usual.</span></span>

<span data-ttu-id="4e520-110">在回切到主池期间，用户将被重定向到主池，并再次进入恢复模式。</span><span class="sxs-lookup"><span data-stu-id="4e520-110">During failback to the primary pool, users are redirected to the primary pool and are again in resiliency mode.</span></span> <span data-ttu-id="4e520-111">只有在用户退出恢复模式后，组呼叫分拣功能才可用。</span><span class="sxs-lookup"><span data-stu-id="4e520-111">Group Call Pickup functionality is not available until the users are out of resiliency mode.</span></span>

<span data-ttu-id="4e520-112">本部分讨论了在灾难恢复过程中进行组呼叫拾取的一些注意事项，还介绍了用户体验。</span><span class="sxs-lookup"><span data-stu-id="4e520-112">This section discusses some considerations for Group Call Pickup during disaster recovery and also describes the user experience.</span></span>

<div>

## <a name="considerations-for-group-call-pickup-during-disaster-recovery"></a><span data-ttu-id="4e520-113">灾难恢复期间组呼叫装货的注意事项</span><span class="sxs-lookup"><span data-stu-id="4e520-113">Considerations for Group Call Pickup During Disaster Recovery</span></span>

<span data-ttu-id="4e520-114">在灾难恢复过程中，已被重定向到备份池的用户作为故障转移过程的一部分，使用在备份池中为呼叫装货组编号运行的调用寄存应用程序。</span><span class="sxs-lookup"><span data-stu-id="4e520-114">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park application running in the backup pool for the call pickup group numbers.</span></span> <span data-ttu-id="4e520-115">因此，在灾难恢复过程中对组呼叫拾取的支持要求在主池和备份池中部署和启用呼叫驻留应用程序。</span><span class="sxs-lookup"><span data-stu-id="4e520-115">Therefore, support for Group Call Pickup during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

<span data-ttu-id="4e520-116">在备份池完成故障转移过程后，必须将 "呼叫驻留" 轨道表中的组呼叫装货号码范围重定向到备份池。</span><span class="sxs-lookup"><span data-stu-id="4e520-116">The Group Call Pickup number ranges in the call park orbit table must be redirected to the backup pool after the failover process to the backup pool is complete.</span></span> <span data-ttu-id="4e520-117">在故障恢复过程完成后，必须将数字范围重定向到主池。</span><span class="sxs-lookup"><span data-stu-id="4e520-117">The number ranges must be redirected back to the primary pool after the failback process to the primary pool is complete.</span></span> <span data-ttu-id="4e520-118">若要重定向组呼叫的装货范围，请使用 **CsCallParkOrbit** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e520-118">To redirect the Group Call Pickup ranges, use the **Set-CsCallParkOrbit** cmdlet.</span></span>

<span data-ttu-id="4e520-119">如果使用不同的完全限定的域名部署新池 (FQDN) 替换主池，则需要将与主池相关联的所有组呼叫装货号码范围重新分配给新池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="4e520-119">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Group Call Pickup number ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="4e520-120">若要将号码范围重新分配给新池，你可以使用 **CsCallParkOrbit** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e520-120">To reassign number ranges to the new pool, you can use the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="4e520-121">有关 **CsCallParkOrbit** cmdlet 的详细信息，请参阅 [set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit)。</span><span class="sxs-lookup"><span data-stu-id="4e520-121">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

</div>

<div>

## <a name="group-call-pickup-experience-during-pool-failure"></a><span data-ttu-id="4e520-122">池故障期间的组呼叫装货体验</span><span class="sxs-lookup"><span data-stu-id="4e520-122">Group Call Pickup Experience During Pool Failure</span></span>

<span data-ttu-id="4e520-123">下表总结了组通过灾难恢复阶段的装货体验。</span><span class="sxs-lookup"><span data-stu-id="4e520-123">The following table summarizes the Group Call Pickup experience through the phases of disaster recovery.</span></span>

### <a name="user-experience-during-disaster-recovery"></a><span data-ttu-id="4e520-124">灾难恢复期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="4e520-124">User Experience During Disaster Recovery</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e520-125">通话状态</span><span class="sxs-lookup"><span data-stu-id="4e520-125">Call state</span></span></th>
<th><span data-ttu-id="4e520-126">故障转移到备份池</span><span class="sxs-lookup"><span data-stu-id="4e520-126">Failover to backup pool</span></span></th>
<th><span data-ttu-id="4e520-127">回切到主池</span><span class="sxs-lookup"><span data-stu-id="4e520-127">Failback to primary pool</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e520-128">新通话</span><span class="sxs-lookup"><span data-stu-id="4e520-128">New calls</span></span></p></td>
<td><p><span data-ttu-id="4e520-129"><strong>在故障转移过程中：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-129"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-130">用户在复原模式下无法使用组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="4e520-130">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="4e520-131"><strong>故障切换完成后：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-131"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-132">当用户退出弹性和组呼叫装货号码范围被重定向到备份池时，可以使用组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="4e520-132">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected to backup pool</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4e520-133"><strong>在故障回复过程中：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-133"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-134">用户在复原模式下无法使用组呼叫装货</span><span class="sxs-lookup"><span data-stu-id="4e520-134">Group Call Pickup not available for users in resiliency mode</span></span></p></li>
</ul>
<p><span data-ttu-id="4e520-135"><strong>故障回复完成后：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-135"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-136">当用户退出弹性和组呼叫时，组呼叫的装货号码范围将被重定向到主池</span><span class="sxs-lookup"><span data-stu-id="4e520-136">Group Call Pickup available when users out of resiliency and Group Call Pickup number ranges are redirected back to primary pool</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e520-137">组呼叫装货队列中的呼叫</span><span class="sxs-lookup"><span data-stu-id="4e520-137">Calls in Group Call Pickup queue</span></span></p></td>
<td><p><span data-ttu-id="4e520-138"><strong>在故障转移过程中：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-138"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-139">无法通过组呼叫提货应答队列中的通话。</span><span class="sxs-lookup"><span data-stu-id="4e520-139">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="4e520-140"><strong>故障切换完成后：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-140"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-141">此状态下没有通话</span><span class="sxs-lookup"><span data-stu-id="4e520-141">No calls in this state</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4e520-142"><strong>在故障回复过程中：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-142"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-143">无法通过组呼叫提货应答队列中的通话。</span><span class="sxs-lookup"><span data-stu-id="4e520-143">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul>
<p><span data-ttu-id="4e520-144"><strong>故障回复完成后：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-144"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-145">无法通过组呼叫提货应答队列中的通话。</span><span class="sxs-lookup"><span data-stu-id="4e520-145">Calls in queue cannot be answered through Group Call Pickup.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e520-146">已建立通话</span><span class="sxs-lookup"><span data-stu-id="4e520-146">Established call</span></span></p></td>
<td><p><span data-ttu-id="4e520-147"><strong>在故障转移过程中：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-147"><strong>During failover process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-148">通话保持连接</span><span class="sxs-lookup"><span data-stu-id="4e520-148">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="4e520-149"><strong>故障切换完成后：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-149"><strong>After failover is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-150">通话保持连接</span><span class="sxs-lookup"><span data-stu-id="4e520-150">Calls stay connected</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="4e520-151"><strong>在故障回复过程中：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-151"><strong>During failback process:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-152">通话保持连接</span><span class="sxs-lookup"><span data-stu-id="4e520-152">Calls stay connected</span></span></p></li>
</ul>
<p><span data-ttu-id="4e520-153"><strong>故障回复完成后：</strong></span><span class="sxs-lookup"><span data-stu-id="4e520-153"><strong>After failback is complete:</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="4e520-154">通话保持连接</span><span class="sxs-lookup"><span data-stu-id="4e520-154">Calls stay connected</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="4e520-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4e520-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

