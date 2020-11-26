---
title: Lync Server 2013：tblPrincipal
description: Lync Server 2013： tblPrincipal。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444411"
---
# <a name="tblprincipal-in-lync-server-2013"></a><span data-ttu-id="a93a0-103">Lync Server 2013 中的 tblPrincipal</span><span class="sxs-lookup"><span data-stu-id="a93a0-103">tblPrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a93a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a93a0-104">

<span> </span></span></span>

<span data-ttu-id="a93a0-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a93a0-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a93a0-106">tblPrincipal 包含所有主体，包括用户、文件夹和组。</span><span class="sxs-lookup"><span data-stu-id="a93a0-106">tblPrincipal contains all principals, including users, folders, and groups.</span></span>

### <a name="columns"></a><span data-ttu-id="a93a0-107">多</span><span class="sxs-lookup"><span data-stu-id="a93a0-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a93a0-108">列</span><span class="sxs-lookup"><span data-stu-id="a93a0-108">Column</span></span></th>
<th><span data-ttu-id="a93a0-109">类型</span><span class="sxs-lookup"><span data-stu-id="a93a0-109">Type</span></span></th>
<th><span data-ttu-id="a93a0-110">说明</span><span class="sxs-lookup"><span data-stu-id="a93a0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-111">prinID</span><span class="sxs-lookup"><span data-stu-id="a93a0-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="a93a0-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="a93a0-113">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="a93a0-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-114">prinGuid</span><span class="sxs-lookup"><span data-stu-id="a93a0-114">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="a93a0-115">GUID，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="a93a0-116">主体 GUID。</span><span class="sxs-lookup"><span data-stu-id="a93a0-116">Principal GUID.</span></span> <span data-ttu-id="a93a0-117">它被广泛用作备用主键，因为它的含义与 Active Directory 域服务空间中的含义相同。</span><span class="sxs-lookup"><span data-stu-id="a93a0-117">This is broadly used as an alternate primary key because its meaning crosses over into the Active Directory Domain Services space.</span></span> <span data-ttu-id="a93a0-118"> (缓存主体的 GUID 等于相应的 Active Directory 对象 GUID。 ) </span><span class="sxs-lookup"><span data-stu-id="a93a0-118">(The GUID for a cached principal is equal to the corresponding Active Directory object GUID.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-119">prinUri</span><span class="sxs-lookup"><span data-stu-id="a93a0-119">prinUri</span></span></p></td>
<td><p><span data-ttu-id="a93a0-120">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-120">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="a93a0-121">主体 URI。</span><span class="sxs-lookup"><span data-stu-id="a93a0-121">Principal URI.</span></span> <span data-ttu-id="a93a0-122">SIP 方案用于用户，并且 ma-grp 用于几乎所有其他内容。</span><span class="sxs-lookup"><span data-stu-id="a93a0-122">The SIP scheme is used for users, and ma-grp is used for almost everything else.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-123">prinName</span><span class="sxs-lookup"><span data-stu-id="a93a0-123">prinName</span></span></p></td>
<td><p><span data-ttu-id="a93a0-124">nvarchar (256) </span><span class="sxs-lookup"><span data-stu-id="a93a0-124">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="a93a0-125">公用名。</span><span class="sxs-lookup"><span data-stu-id="a93a0-125">Common name.</span></span> <span data-ttu-id="a93a0-126">仅由用户类型使用。</span><span class="sxs-lookup"><span data-stu-id="a93a0-126">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-127">prinDisplayName</span><span class="sxs-lookup"><span data-stu-id="a93a0-127">prinDisplayName</span></span></p></td>
<td><p><span data-ttu-id="a93a0-128">Nvarchar (256) </span><span class="sxs-lookup"><span data-stu-id="a93a0-128">Nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="a93a0-129">显示名称。</span><span class="sxs-lookup"><span data-stu-id="a93a0-129">Display name.</span></span> <span data-ttu-id="a93a0-130">仅由用户类型使用。</span><span class="sxs-lookup"><span data-stu-id="a93a0-130">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-131">prinCompanyName</span><span class="sxs-lookup"><span data-stu-id="a93a0-131">prinCompanyName</span></span></p></td>
<td><p><span data-ttu-id="a93a0-132">nvarchar (256) </span><span class="sxs-lookup"><span data-stu-id="a93a0-132">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="a93a0-133">公司名称。</span><span class="sxs-lookup"><span data-stu-id="a93a0-133">Company name.</span></span> <span data-ttu-id="a93a0-134">仅由用户类型使用。</span><span class="sxs-lookup"><span data-stu-id="a93a0-134">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-135">prinEmail</span><span class="sxs-lookup"><span data-stu-id="a93a0-135">prinEmail</span></span></p></td>
<td><p><span data-ttu-id="a93a0-136">nvarchar (256) </span><span class="sxs-lookup"><span data-stu-id="a93a0-136">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="a93a0-137">电子邮件。</span><span class="sxs-lookup"><span data-stu-id="a93a0-137">Email.</span></span> <span data-ttu-id="a93a0-138">仅由用户类型使用。</span><span class="sxs-lookup"><span data-stu-id="a93a0-138">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-139">prinADPath</span><span class="sxs-lookup"><span data-stu-id="a93a0-139">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="a93a0-140">nvarchar (384) </span><span class="sxs-lookup"><span data-stu-id="a93a0-140">nvarchar (384)</span></span></p></td>
<td><p><span data-ttu-id="a93a0-141">Active Directory 对象的域名，主体是的缓存版本。</span><span class="sxs-lookup"><span data-stu-id="a93a0-141">Domain name of the Active Directory object that the principal is a cached version of.</span></span> <span data-ttu-id="a93a0-142">对于非 Active Directory (对象的类型（如系统用户) ）可能为 Null。</span><span class="sxs-lookup"><span data-stu-id="a93a0-142">Can be Null for types that are not Active Directory objects (such as system users).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-143">prinADUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a93a0-143">prinADUserPrincipalName</span></span></p></td>
<td><p><span data-ttu-id="a93a0-144">nvarchar (256) </span><span class="sxs-lookup"><span data-stu-id="a93a0-144">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="a93a0-145">用户的用户主体名称 (UPN) 。</span><span class="sxs-lookup"><span data-stu-id="a93a0-145">User’s user principal name (UPN).</span></span> <span data-ttu-id="a93a0-146">仅由常规用户类型使用。</span><span class="sxs-lookup"><span data-stu-id="a93a0-146">Used only by regular user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-147">prinDisabled</span><span class="sxs-lookup"><span data-stu-id="a93a0-147">prinDisabled</span></span></p></td>
<td><p><span data-ttu-id="a93a0-148">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-148">smallint, not null</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a93a0-149">0：主体处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="a93a0-149">0: Principal is active.</span></span></p></li>
<li><p><span data-ttu-id="a93a0-150">1：主体被禁用，因为用户的 SIP 功能已被禁用。</span><span class="sxs-lookup"><span data-stu-id="a93a0-150">1: Principal is disabled because user’s SIP capabilities are disabled.</span></span></p></li>
<li><p><span data-ttu-id="a93a0-151">2：删除主体，因为关联的 AD 对象已被删除。</span><span class="sxs-lookup"><span data-stu-id="a93a0-151">2: Principal is deleted because associated AD object has been deleted.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-152">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="a93a0-152">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="a93a0-153">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-153">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="a93a0-154">TblPrincipalType table 中的主体类型 () 。</span><span class="sxs-lookup"><span data-stu-id="a93a0-154">Principal type (from tblPrincipalType table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-155">prinPoolID</span><span class="sxs-lookup"><span data-stu-id="a93a0-155">prinPoolID</span></span></p></td>
<td><p><span data-ttu-id="a93a0-156">整形</span><span class="sxs-lookup"><span data-stu-id="a93a0-156">Int</span></span></p></td>
<td><p><span data-ttu-id="a93a0-157">主体的 Lync 池分配。</span><span class="sxs-lookup"><span data-stu-id="a93a0-157">Lync pool assignment for the principal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-158">prinPolicyID</span><span class="sxs-lookup"><span data-stu-id="a93a0-158">prinPolicyID</span></span></p></td>
<td><p><span data-ttu-id="a93a0-159">整形</span><span class="sxs-lookup"><span data-stu-id="a93a0-159">Int</span></span></p></td>
<td><p><span data-ttu-id="a93a0-160">用户的持久聊天服务器策略值（如果存在标记类型策略）。</span><span class="sxs-lookup"><span data-stu-id="a93a0-160">Persistent Chat Server policy value for user, if tag type policy is present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-161">prinAddedBy</span><span class="sxs-lookup"><span data-stu-id="a93a0-161">prinAddedBy</span></span></p></td>
<td><p><span data-ttu-id="a93a0-162">int</span><span class="sxs-lookup"><span data-stu-id="a93a0-162">int</span></span></p></td>
<td><p><span data-ttu-id="a93a0-163">创建者的主体 ID。</span><span class="sxs-lookup"><span data-stu-id="a93a0-163">Principal ID of the creator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-164">prinAddedOn</span><span class="sxs-lookup"><span data-stu-id="a93a0-164">prinAddedOn</span></span></p></td>
<td><p><span data-ttu-id="a93a0-165">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-165">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="a93a0-166">创建时间的时间戳。</span><span class="sxs-lookup"><span data-stu-id="a93a0-166">Time stamp for the creation time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-167">prinUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="a93a0-167">prinUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="a93a0-168">int</span><span class="sxs-lookup"><span data-stu-id="a93a0-168">int</span></span></p></td>
<td><p><span data-ttu-id="a93a0-169">上次更新此操作的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="a93a0-169">ID of the principal that last updated this.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-170">prinUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="a93a0-170">prinUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="a93a0-171">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-171">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="a93a0-172">上次更新的时间戳。</span><span class="sxs-lookup"><span data-stu-id="a93a0-172">Time stamp for the last update.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-173">prinVerifiedOn</span><span class="sxs-lookup"><span data-stu-id="a93a0-173">prinVerifiedOn</span></span></p></td>
<td><p><span data-ttu-id="a93a0-174">datetime，not null</span><span class="sxs-lookup"><span data-stu-id="a93a0-174">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="a93a0-175">主体的上次 Active Directory 同步刷新的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a93a0-175">Date and time of the last Active Directory Sync refresh for the principal.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="a93a0-176">标示</span><span class="sxs-lookup"><span data-stu-id="a93a0-176">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a93a0-177">列</span><span class="sxs-lookup"><span data-stu-id="a93a0-177">Column</span></span></th>
<th><span data-ttu-id="a93a0-178">说明</span><span class="sxs-lookup"><span data-stu-id="a93a0-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a93a0-179">prinID</span><span class="sxs-lookup"><span data-stu-id="a93a0-179">prinID</span></span></p></td>
<td><p><span data-ttu-id="a93a0-180">主键。</span><span class="sxs-lookup"><span data-stu-id="a93a0-180">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a93a0-181">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="a93a0-181">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="a93a0-182">TblPrincipalType 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="a93a0-182">Foreign key with lookup in tblPrincipalType.ptypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a93a0-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a93a0-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

