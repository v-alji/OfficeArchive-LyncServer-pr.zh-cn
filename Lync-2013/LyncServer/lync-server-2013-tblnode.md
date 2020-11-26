---
title: Lync Server 2013：tblNode
description: Lync Server 2013： tblNode。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblNode
ms:assetid: a31d2961-aa83-4286-a12e-15d279c95f19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615024(v=OCS.15)
ms:contentKeyID: 48184960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0a5d630621c32cbc54501249c7a679bf4023c60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423517"
---
# <a name="tblnode-in-lync-server-2013"></a><span data-ttu-id="b2653-103">Lync Server 2013 中的 tblNode</span><span class="sxs-lookup"><span data-stu-id="b2653-103">tblNode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2653-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2653-104">

<span> </span></span></span>

<span data-ttu-id="b2653-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="b2653-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="b2653-106">tblNode 包含类别或聊天室节点 (的对象树，) 在 Lync Server 2013 控制面板和管理 cmdlet 中托管。</span><span class="sxs-lookup"><span data-stu-id="b2653-106">tblNode contains the object tree (with category or chat room nodes) as managed in the Lync Server 2013 Control Panel and administrative cmdlets.</span></span>

### <a name="columns"></a><span data-ttu-id="b2653-107">多</span><span class="sxs-lookup"><span data-stu-id="b2653-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2653-108">列</span><span class="sxs-lookup"><span data-stu-id="b2653-108">Column</span></span></th>
<th><span data-ttu-id="b2653-109">类型</span><span class="sxs-lookup"><span data-stu-id="b2653-109">Type</span></span></th>
<th><span data-ttu-id="b2653-110">说明</span><span class="sxs-lookup"><span data-stu-id="b2653-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2653-111">a</span><span class="sxs-lookup"><span data-stu-id="b2653-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="b2653-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-113">节点 ID (唯一编号) 。</span><span class="sxs-lookup"><span data-stu-id="b2653-113">Node ID (unique number).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-114">nodeGuid</span><span class="sxs-lookup"><span data-stu-id="b2653-114">nodeGuid</span></span></p></td>
<td><p><span data-ttu-id="b2653-115">GUID，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-116">节点 GUID。</span><span class="sxs-lookup"><span data-stu-id="b2653-116">Node GUID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-117">parentID</span><span class="sxs-lookup"><span data-stu-id="b2653-117">parentID</span></span></p></td>
<td><p><span data-ttu-id="b2653-118">int</span><span class="sxs-lookup"><span data-stu-id="b2653-118">int</span></span></p></td>
<td><p><span data-ttu-id="b2653-119">父项的节点 ID。</span><span class="sxs-lookup"><span data-stu-id="b2653-119">Node ID of parent.</span></span> <span data-ttu-id="b2653-120">ID 为 1) 的根节点 (将其本身包含到父节点。</span><span class="sxs-lookup"><span data-stu-id="b2653-120">The root node (with ID 1) includes itself as parent as well.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-121">nodeType</span><span class="sxs-lookup"><span data-stu-id="b2653-121">nodeType</span></span></p></td>
<td><p><span data-ttu-id="b2653-122">位，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-122">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-123">如果节点是类别，则为 True。</span><span class="sxs-lookup"><span data-stu-id="b2653-123">True if the node is a category.</span></span></p>
<p><span data-ttu-id="b2653-124">如果节点是聊天室，则为 False。</span><span class="sxs-lookup"><span data-stu-id="b2653-124">False if the node is a chat room.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-125">nodeName</span><span class="sxs-lookup"><span data-stu-id="b2653-125">nodeName</span></span></p></td>
<td><p><span data-ttu-id="b2653-126">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-126">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-127">节点名称。</span><span class="sxs-lookup"><span data-stu-id="b2653-127">Node name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-128">nodeDesc</span><span class="sxs-lookup"><span data-stu-id="b2653-128">nodeDesc</span></span></p></td>
<td><p><span data-ttu-id="b2653-129">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-129">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-130">节点说明。</span><span class="sxs-lookup"><span data-stu-id="b2653-130">Node description.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-131">邀请</span><span class="sxs-lookup"><span data-stu-id="b2653-131">invite</span></span></p></td>
<td><p><span data-ttu-id="b2653-132">bit</span><span class="sxs-lookup"><span data-stu-id="b2653-132">bit</span></span></p></td>
<td><p><span data-ttu-id="b2653-133">对于类别：</span><span class="sxs-lookup"><span data-stu-id="b2653-133">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-134">如果邀请已打开，则为 True。</span><span class="sxs-lookup"><span data-stu-id="b2653-134">True if invites are on.</span></span></p></li>
<li><p><span data-ttu-id="b2653-135">如果邀请已关闭，则为 False。</span><span class="sxs-lookup"><span data-stu-id="b2653-135">False if invites are off.</span></span></p></li>
</ul>
<p><span data-ttu-id="b2653-136">对于会议室：</span><span class="sxs-lookup"><span data-stu-id="b2653-136">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-137">如果邀请已关闭，则为 False (覆盖父类别) 。</span><span class="sxs-lookup"><span data-stu-id="b2653-137">False if invites are off (overrides the parent category).</span></span></p></li>
<li><p><span data-ttu-id="b2653-138">如果 "邀请" 设置继承自父类别，则为 Null。</span><span class="sxs-lookup"><span data-stu-id="b2653-138">Null if the invites setting is inherited from the parent category.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-139">身份</span><span class="sxs-lookup"><span data-stu-id="b2653-139">logged</span></span></p></td>
<td><p><span data-ttu-id="b2653-140">bit</span><span class="sxs-lookup"><span data-stu-id="b2653-140">bit</span></span></p></td>
<td><p><span data-ttu-id="b2653-141">对于类别：</span><span class="sxs-lookup"><span data-stu-id="b2653-141">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-142">如果打开聊天记录，则为 True。</span><span class="sxs-lookup"><span data-stu-id="b2653-142">True if chat history is on.</span></span></p></li>
<li><p><span data-ttu-id="b2653-143">如果聊天历史记录处于关闭状态，则为 False。</span><span class="sxs-lookup"><span data-stu-id="b2653-143">False if chat history is off.</span></span></p></li>
</ul>
<p><span data-ttu-id="b2653-144">对于会议室：</span><span class="sxs-lookup"><span data-stu-id="b2653-144">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-145">Null.</span><span class="sxs-lookup"><span data-stu-id="b2653-145">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-146">filePost</span><span class="sxs-lookup"><span data-stu-id="b2653-146">filePost</span></span></p></td>
<td><p><span data-ttu-id="b2653-147">bit</span><span class="sxs-lookup"><span data-stu-id="b2653-147">bit</span></span></p></td>
<td><p><span data-ttu-id="b2653-148">对于类别：</span><span class="sxs-lookup"><span data-stu-id="b2653-148">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-149">如果允许文件上载，则为 True。</span><span class="sxs-lookup"><span data-stu-id="b2653-149">True if file uploads are allowed.</span></span></p></li>
<li><p><span data-ttu-id="b2653-150">如果不允许文件上载，则为 False。</span><span class="sxs-lookup"><span data-stu-id="b2653-150">False if file uploads are disallowed.</span></span></p></li>
</ul>
<p><span data-ttu-id="b2653-151">对于会议室：</span><span class="sxs-lookup"><span data-stu-id="b2653-151">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-152">Null.</span><span class="sxs-lookup"><span data-stu-id="b2653-152">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-153">禁用</span><span class="sxs-lookup"><span data-stu-id="b2653-153">disabled</span></span></p></td>
<td><p><span data-ttu-id="b2653-154">位，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-154">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-155">如果禁用聊天室，则为 True。</span><span class="sxs-lookup"><span data-stu-id="b2653-155">True if the chat room is disabled.</span></span> <span data-ttu-id="b2653-156">仅适用于聊天室。</span><span class="sxs-lookup"><span data-stu-id="b2653-156">Applies only to chat rooms.</span></span> <span data-ttu-id="b2653-157">对类别 (False。 ) </span><span class="sxs-lookup"><span data-stu-id="b2653-157">(False for categories.)</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-158">现象</span><span class="sxs-lookup"><span data-stu-id="b2653-158">behavior</span></span></p></td>
<td><p><span data-ttu-id="b2653-159">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-159">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-160">在 EnumValue 表) 中查找的行为 (：</span><span class="sxs-lookup"><span data-stu-id="b2653-160">Behavior (looked up in EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-161">4：正常 (正常聊天会议室) 。</span><span class="sxs-lookup"><span data-stu-id="b2653-161">4: Normal (normal chat rooms).</span></span></p></li>
<li><p><span data-ttu-id="b2653-162">5： Auditorium (Auditorium 聊天室，只有演示者可以参与) 。</span><span class="sxs-lookup"><span data-stu-id="b2653-162">5: Auditorium (auditorium chat rooms, only presenters can contribute).</span></span></p></li>
</ul>
<p><span data-ttu-id="b2653-163">仅适用于聊天室。</span><span class="sxs-lookup"><span data-stu-id="b2653-163">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-164">了解</span><span class="sxs-lookup"><span data-stu-id="b2653-164">visibility</span></span></p></td>
<td><p><span data-ttu-id="b2653-165">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-165">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-166">在 EnumValue 表格) 上查找的可见性 (：</span><span class="sxs-lookup"><span data-stu-id="b2653-166">Visibility (looked up on EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="b2653-167">2：私密</span><span class="sxs-lookup"><span data-stu-id="b2653-167">2: Private</span></span></p></li>
<li><p><span data-ttu-id="b2653-168">3：范围</span><span class="sxs-lookup"><span data-stu-id="b2653-168">3: Scoped</span></span></p></li>
<li><p><span data-ttu-id="b2653-169">6：打开</span><span class="sxs-lookup"><span data-stu-id="b2653-169">6: Open</span></span></p></li>
</ul>
<p><span data-ttu-id="b2653-170">仅适用于聊天室。</span><span class="sxs-lookup"><span data-stu-id="b2653-170">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-171">siopID</span><span class="sxs-lookup"><span data-stu-id="b2653-171">siopID</span></span></p></td>
<td><p><span data-ttu-id="b2653-172">GUID</span><span class="sxs-lookup"><span data-stu-id="b2653-172">GUID</span></span></p></td>
<td><p><span data-ttu-id="b2653-173">如果外接程序与此聊天室关联，则 Add-In GUID。</span><span class="sxs-lookup"><span data-stu-id="b2653-173">Add-In GUID if an add-in is associated with this chat room.</span></span> <span data-ttu-id="b2653-174"> (类别没有外接程序。 ) </span><span class="sxs-lookup"><span data-stu-id="b2653-174">(Categories do not have add-ins.)</span></span></p>
<p><span data-ttu-id="b2653-175">外接程序信息在 SiopWhiteList 表中查找。</span><span class="sxs-lookup"><span data-stu-id="b2653-175">The add-in information is looked up in SiopWhiteList table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-176">nodeAddedBy</span><span class="sxs-lookup"><span data-stu-id="b2653-176">nodeAddedBy</span></span></p></td>
<td><p><span data-ttu-id="b2653-177">int，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-177">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-178">创建此节点的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="b2653-178">ID of the principal that created this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-179">nodeAddedOn</span><span class="sxs-lookup"><span data-stu-id="b2653-179">nodeAddedOn</span></span></p></td>
<td><p><span data-ttu-id="b2653-180">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-180">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-181">节点创建的时间戳。</span><span class="sxs-lookup"><span data-stu-id="b2653-181">Time stamp of the node creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-182">nodeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="b2653-182">nodeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="b2653-183">int，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-183">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-184">执行此节点的最新更新的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="b2653-184">ID of the principal that did the latest update of this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-185">nodeUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="b2653-185">nodeUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="b2653-186">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="b2653-186">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="b2653-187">此节点的最新更新的时间戳。</span><span class="sxs-lookup"><span data-stu-id="b2653-187">Time stamp of the latest update of this node.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-188">purgedOn</span><span class="sxs-lookup"><span data-stu-id="b2653-188">purgedOn</span></span></p></td>
<td><p><span data-ttu-id="b2653-189">datetime</span><span class="sxs-lookup"><span data-stu-id="b2653-189">datetime</span></span></p></td>
<td><p><span data-ttu-id="b2653-190">最新的清除操作的时间 (从影响此节点的 tblPrincipalRole table) 中删除 tblScopedPrincipal 表和角色中的作用域。</span><span class="sxs-lookup"><span data-stu-id="b2653-190">Time of the latest purge operation (removal of scopes from tblScopedPrincipal table and roles from tblPrincipalRole table) that affected this node.</span></span> <span data-ttu-id="b2653-191">此功能由聊天服务的内部缓存更新机制使用。</span><span class="sxs-lookup"><span data-stu-id="b2653-191">This is used by the Chat service’s internal cache update mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="b2653-192">标示</span><span class="sxs-lookup"><span data-stu-id="b2653-192">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2653-193">列</span><span class="sxs-lookup"><span data-stu-id="b2653-193">Column</span></span></th>
<th><span data-ttu-id="b2653-194">说明</span><span class="sxs-lookup"><span data-stu-id="b2653-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2653-195">a</span><span class="sxs-lookup"><span data-stu-id="b2653-195">nodeID</span></span></p></td>
<td><p><span data-ttu-id="b2653-196">主键。</span><span class="sxs-lookup"><span data-stu-id="b2653-196">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-197">现象</span><span class="sxs-lookup"><span data-stu-id="b2653-197">behavior</span></span></p></td>
<td><p><span data-ttu-id="b2653-198">TblEnumValue 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="b2653-198">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-199">了解</span><span class="sxs-lookup"><span data-stu-id="b2653-199">visibility</span></span></p></td>
<td><p><span data-ttu-id="b2653-200">TblEnumValue 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="b2653-200">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2653-201">parentID</span><span class="sxs-lookup"><span data-stu-id="b2653-201">parentID</span></span></p></td>
<td><p><span data-ttu-id="b2653-202">带有 tblNode 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="b2653-202">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2653-203">siopID</span><span class="sxs-lookup"><span data-stu-id="b2653-203">siopID</span></span></p></td>
<td><p><span data-ttu-id="b2653-204">TblSiopWhiteList 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="b2653-204">Foreign key with lookup in tblSiopWhiteList.siopId table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b2653-205">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2653-205">


</div>

<span> </span>

</div>

</div>

</span></span></div>

