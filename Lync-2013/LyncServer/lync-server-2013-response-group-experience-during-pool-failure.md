---
title: 池故障期间的 Lync Server 2013 响应组体验
description: 在池失败期间 Lync Server 2013 响应组体验。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group experience during pool failure
ms:assetid: 4e00fb38-64b1-4fd9-903d-7639177bc303
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204886(v=OCS.15)
ms:contentKeyID: 48184116
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d8d5904bc6934d4c330202bafa66d6dd8a16ff5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436242"
---
# <a name="response-group-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="24dcc-103">池故障期间 Lync Server 2013 中的响应组体验</span><span class="sxs-lookup"><span data-stu-id="24dcc-103">Response group experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24dcc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24dcc-104">

<span> </span></span></span>

<span data-ttu-id="24dcc-105">_**主题上次修改时间：** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="24dcc-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="24dcc-106">本部分详细介绍了如何在以下阶段影响响应组活动：</span><span class="sxs-lookup"><span data-stu-id="24dcc-106">This section describes in detail how response group activity is affected in the following stages:</span></span>

  - <span data-ttu-id="24dcc-107">主池出现中断，但尚未启动故障转移。</span><span class="sxs-lookup"><span data-stu-id="24dcc-107">An outage occurs in the primary pool, but failover is not yet initiated.</span></span>

  - <span data-ttu-id="24dcc-108">服务已故障转移到备份池。</span><span class="sxs-lookup"><span data-stu-id="24dcc-108">Service is failed over to the backup pool.</span></span>

  - <span data-ttu-id="24dcc-109">服务故障回复到主池。</span><span class="sxs-lookup"><span data-stu-id="24dcc-109">Service is failed back to the primary pool.</span></span>

<div>

## <a name="user-experience-when-outage-occurs"></a><span data-ttu-id="24dcc-110">出现停机时的用户体验</span><span class="sxs-lookup"><span data-stu-id="24dcc-110">User Experience When Outage Occurs</span></span>

<span data-ttu-id="24dcc-111">当池或网站发生停机，但管理员尚未启动故障转移时，将按下表中所述处理响应组活动。</span><span class="sxs-lookup"><span data-stu-id="24dcc-111">When a pool or site outage occurs, but the administrator has not yet initiated failover, response group activity is handled as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24dcc-112">在灾难恢复期间，取决于在恢复期间是否将主池响应组导入到备份池中，调用的行为有所不同。</span><span class="sxs-lookup"><span data-stu-id="24dcc-112">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="24dcc-113">在下表中，对导入的响应组的引用意味着在灾难恢复模式中将主要池响应组导入到备份池中。</span><span class="sxs-lookup"><span data-stu-id="24dcc-113">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="outage-occurs"></a><span data-ttu-id="24dcc-114">发生中断</span><span class="sxs-lookup"><span data-stu-id="24dcc-114">Outage Occurs</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24dcc-115">呼叫或用户操作的类型</span><span class="sxs-lookup"><span data-stu-id="24dcc-115">Type of call or user action</span></span></th>
<th><span data-ttu-id="24dcc-116">停机期间</span><span class="sxs-lookup"><span data-stu-id="24dcc-116">During outage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-117">连接到代理的通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-117">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-118">定期通话仍保持连接状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-118">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-119">匿名通话已断开连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-119">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-120">尚未连接到代理的正在进行的通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-120">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="24dcc-121">通话断开。</span><span class="sxs-lookup"><span data-stu-id="24dcc-121">Calls are disconnected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-122">新通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-122">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-123">通话断开。</span><span class="sxs-lookup"><span data-stu-id="24dcc-123">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-124">如果已导入响应组，则呼叫将连接到备份池，但无法访问托管在主池中的代理。</span><span class="sxs-lookup"><span data-stu-id="24dcc-124">If response groups were imported, calls connect to backup pool, but agents homed in primary pool are unreachable.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-125">代理代表响应组呼叫</span><span class="sxs-lookup"><span data-stu-id="24dcc-125">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="24dcc-126">在此阶段中禁用功能。</span><span class="sxs-lookup"><span data-stu-id="24dcc-126">Feature is disabled during this stage.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-127">代理登录和代理信息</span><span class="sxs-lookup"><span data-stu-id="24dcc-127">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-128">主池拥有的代理组可以在代理控制台上查看，但代理无法登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-128">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-129">可以在代理控制台上查看备份池所拥有的代理组，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-129">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-130">代理控制台上不显示导入的代理组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-130">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-131">响应组配置</span><span class="sxs-lookup"><span data-stu-id="24dcc-131">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-132">可以查看由主池拥有的响应组，具体取决于主池的后端数据库的可用性，但不能进行修改。</span><span class="sxs-lookup"><span data-stu-id="24dcc-132">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-133">可以查看和修改备份池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-133">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-134">无法使用 Lync Server 控制面板或响应组配置工具查看导入的响应组，但可以使用 Lync Server Management Shell cmdlet 进行配置。</span><span class="sxs-lookup"><span data-stu-id="24dcc-134">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="24dcc-135">故障转移期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="24dcc-135">User Experience During Failover</span></span>

<span data-ttu-id="24dcc-136">当管理员将故障转移调用到备份池时，将在故障转移期间和之后处理响应组活动，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="24dcc-136">When an administrator invokes failover to a backup pool, response group activity is handled during and after the failover as described in the following table.</span></span> <span data-ttu-id="24dcc-137">第一列描述可能发生的活动类型。</span><span class="sxs-lookup"><span data-stu-id="24dcc-137">The first column describes the type of activity that might be taking place.</span></span> <span data-ttu-id="24dcc-138">中间列描述了如何在短时间内处理每个活动，以故障转移到备份池。</span><span class="sxs-lookup"><span data-stu-id="24dcc-138">The middle column describes how each activity is handled during the brief time that it takes to fail over to the backup pool.</span></span> <span data-ttu-id="24dcc-139">最后一列介绍在故障转移过程完成并且为主池准备了备份池后，在持续时间内活动的处理方式。</span><span class="sxs-lookup"><span data-stu-id="24dcc-139">The last column describes how the activity is handled for the duration, after the failover process is complete and the backup pool is standing in for the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24dcc-140">在灾难恢复期间，取决于在恢复期间是否将主池响应组导入到备份池中，调用的行为有所不同。</span><span class="sxs-lookup"><span data-stu-id="24dcc-140">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="24dcc-141">在下表中，对导入的响应组的引用意味着在灾难恢复模式中将主要池响应组导入到备份池中。</span><span class="sxs-lookup"><span data-stu-id="24dcc-141">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="failover-is-initiated"></a><span data-ttu-id="24dcc-142">已启动故障转移</span><span class="sxs-lookup"><span data-stu-id="24dcc-142">Failover Is Initiated</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24dcc-143">呼叫或用户操作的类型</span><span class="sxs-lookup"><span data-stu-id="24dcc-143">Type of call or user action</span></span></th>
<th><span data-ttu-id="24dcc-144">故障转移期间</span><span class="sxs-lookup"><span data-stu-id="24dcc-144">During Failover</span></span></th>
<th><span data-ttu-id="24dcc-145">故障转移完成后</span><span class="sxs-lookup"><span data-stu-id="24dcc-145">After Failover Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-146">连接到代理的通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-146">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-147">定期通话仍保持连接状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-147">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-148">匿名通话已断开连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-148">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-149">定期通话仍保持连接状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-149">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-150">对于导入的响应组，已达到备份池的匿名呼叫仍保持连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-150">For imported response groups, anonymous calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-151">尚未连接到代理的正在进行的通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-151">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="24dcc-152">通话断开。</span><span class="sxs-lookup"><span data-stu-id="24dcc-152">Calls are disconnected.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-153">如果未导入响应组，则没有通话处于此状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-153">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-154">对于导入的响应组，已达到备份池的呼叫仍保持连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-154">For imported response groups, calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-155">新通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-155">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-156">通话断开。</span><span class="sxs-lookup"><span data-stu-id="24dcc-156">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-157">对于导入的响应组，呼叫将连接到备份池，但无法访问主池中托管的代理。</span><span class="sxs-lookup"><span data-stu-id="24dcc-157">For imported response groups, calls connect to the backup pool, but agents homed in the primary pool are unreachable.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-158">如果未导入响应组，则通话将断开连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-158">If response groups were not imported, calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-159">对于导入的响应组，呼叫将连接到备份池。</span><span class="sxs-lookup"><span data-stu-id="24dcc-159">For imported response groups, calls connect to the backup pool.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-160">代理代表响应组呼叫</span><span class="sxs-lookup"><span data-stu-id="24dcc-160">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="24dcc-161">在此阶段中禁用功能</span><span class="sxs-lookup"><span data-stu-id="24dcc-161">Feature is disabled during this stage</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-162">如果未导入响应组，呼叫将失败。</span><span class="sxs-lookup"><span data-stu-id="24dcc-162">If response groups were not imported, calls fail.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-163">对于导入的响应组，通话成功。</span><span class="sxs-lookup"><span data-stu-id="24dcc-163">For imported response groups, calls succeed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-164">代理登录和代理信息</span><span class="sxs-lookup"><span data-stu-id="24dcc-164">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-165">主池拥有的代理组可以在代理控制台上查看，但代理无法登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-165">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-166">可以在代理控制台上查看备份池所拥有的代理组，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-166">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-167">已导入的代理组将显示在代理控制台上，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-167">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-168">主池拥有的代理组可以在代理控制台上查看，但代理无法登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-168">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-169">可以在代理控制台上查看备份池所拥有的代理组，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-169">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-170">已导入的代理组将显示在代理控制台上，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-170">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-171">响应组配置</span><span class="sxs-lookup"><span data-stu-id="24dcc-171">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-172">可以查看由主池拥有的响应组，具体取决于主池的后端数据库的可用性，但不能进行修改。</span><span class="sxs-lookup"><span data-stu-id="24dcc-172">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-173">可以查看和修改备份池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-173">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-174">无法使用 Lync Server 控制面板或响应组配置工具查看导入的响应组，但可以使用 Lync Server Management Shell cmdlet 进行配置。</span><span class="sxs-lookup"><span data-stu-id="24dcc-174">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-175">可以查看由主池拥有的响应组，具体取决于后端数据库的可用性，但不能进行修改。</span><span class="sxs-lookup"><span data-stu-id="24dcc-175">Response groups owned by the primary pool can be viewed, depending on the availability of the back end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-176">可以查看和修改备份池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-176">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-177">无法使用 Lync Server 控制面板或响应组配置工具查看导入的响应组，但可以使用 Lync Server Management Shell cmdlet 进行配置。</span><span class="sxs-lookup"><span data-stu-id="24dcc-177">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="24dcc-178">故障回复期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="24dcc-178">User Experience During Failback</span></span>

<span data-ttu-id="24dcc-179">当管理员将故障回复调用到主池时，将在故障回复期间和之后处理响应组活动，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="24dcc-179">When an administrator invokes failback to the primary pool, response group activity is handled during and after the failback as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24dcc-180">在灾难恢复期间，取决于在恢复期间是否将主池响应组导入到备份池中，调用的行为有所不同。</span><span class="sxs-lookup"><span data-stu-id="24dcc-180">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="24dcc-181">在下表中，对导入的响应组的引用意味着在灾难恢复模式中将主要池响应组导入到备份池中。</span><span class="sxs-lookup"><span data-stu-id="24dcc-181">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="call-handling-in-failback"></a><span data-ttu-id="24dcc-182">故障回复中的呼叫处理</span><span class="sxs-lookup"><span data-stu-id="24dcc-182">Call Handling in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24dcc-183">呼叫或用户操作的类型</span><span class="sxs-lookup"><span data-stu-id="24dcc-183">Type of call or user action</span></span></th>
<th><span data-ttu-id="24dcc-184">在故障回复期间</span><span class="sxs-lookup"><span data-stu-id="24dcc-184">During Failback</span></span></th>
<th><span data-ttu-id="24dcc-185">故障回复完成后</span><span class="sxs-lookup"><span data-stu-id="24dcc-185">After Failback Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-186">连接到代理的通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-186">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-187">定期通话仍保持连接状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-187">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-188">如果未导入响应组，则没有任何匿名通话处于此状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-188">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-189">对于导入的响应组，匿名通话仍保持连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-189">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-190">定期通话仍保持连接状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-190">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-191">如果未导入响应组，则没有任何匿名通话处于此状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-191">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-192">对于导入的响应组，匿名通话仍保持连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-192">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-193">尚未连接到代理的正在进行的通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-193">In progress calls not yet connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-194">如果未导入响应组，则没有通话处于此状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-194">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-195">对于导入的响应组，呼叫将断开连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-195">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-196">如果未导入响应组，则没有通话处于此状态。</span><span class="sxs-lookup"><span data-stu-id="24dcc-196">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-197">对于导入的响应组，呼叫将断开连接。</span><span class="sxs-lookup"><span data-stu-id="24dcc-197">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-198">新通话</span><span class="sxs-lookup"><span data-stu-id="24dcc-198">New calls</span></span></p></td>
<td><p><span data-ttu-id="24dcc-199">呼叫连接到主池，但驻留在主池中的代理不可访问。</span><span class="sxs-lookup"><span data-stu-id="24dcc-199">Calls connect to the primary pool, but agents homed in the primary pool are unreachable.</span></span></p></td>
<td><p><span data-ttu-id="24dcc-200">呼叫将连接到主池。</span><span class="sxs-lookup"><span data-stu-id="24dcc-200">Calls connect to the primary pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-201">代理代表响应组呼叫</span><span class="sxs-lookup"><span data-stu-id="24dcc-201">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="24dcc-202">在此阶段中禁用功能。</span><span class="sxs-lookup"><span data-stu-id="24dcc-202">Feature is disabled during this stage.</span></span></p></td>
<td><p><span data-ttu-id="24dcc-203">通话成功。</span><span class="sxs-lookup"><span data-stu-id="24dcc-203">Calls succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24dcc-204">代理登录和代理信息</span><span class="sxs-lookup"><span data-stu-id="24dcc-204">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-205">主池拥有的代理组可以在代理控制台上查看，但代理无法登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-205">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-206">可以在代理控制台上查看备份池所拥有的代理组，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-206">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-207">已导入的代理组将显示在代理控制台上，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-207">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-208">可以在代理控制台上查看主池拥有的代理组，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-208">Agent groups owned by the primary pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-209">可以在代理控制台上查看备份池所拥有的代理组，并且代理可以登录。</span><span class="sxs-lookup"><span data-stu-id="24dcc-209">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-210">代理控制台上不显示导入的代理组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-210">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24dcc-211">响应组配置</span><span class="sxs-lookup"><span data-stu-id="24dcc-211">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-212">可以查看由主池拥有的响应组，具体取决于主池的后端数据库的可用性，但不能进行修改。</span><span class="sxs-lookup"><span data-stu-id="24dcc-212">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-213">可以查看和修改备份池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-213">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-214">无法使用 Lync Server 控制面板或响应组配置工具查看导入的响应组，但可以使用 Lync Server Management Shell cmdlet 进行配置。</span><span class="sxs-lookup"><span data-stu-id="24dcc-214">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="24dcc-215">可以查看和修改主池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-215">Response groups owned by the primary pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-216">可以查看和修改备份池拥有的响应组。</span><span class="sxs-lookup"><span data-stu-id="24dcc-216">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="24dcc-217">无法使用 Lync Server 控制面板或响应组配置工具查看导入的响应组，但可以使用 Lync Server Management Shell cmdlet 进行配置。</span><span class="sxs-lookup"><span data-stu-id="24dcc-217">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="24dcc-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24dcc-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

