---
title: Lync Server 2013：tblPrincipalRole
description: Lync Server 2013： tblPrincipalRole。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalRole
ms:assetid: dcd16dc1-a66c-4720-a48f-ec8b28337383
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615039(v=OCS.15)
ms:contentKeyID: 48185597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f58ffda3136c254ee77f14d33dcb42af5d172c4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391797"
---
# <a name="tblprincipalrole-in-lync-server-2013"></a><span data-ttu-id="077b3-103">Lync Server 2013 中的 tblPrincipalRole</span><span class="sxs-lookup"><span data-stu-id="077b3-103">tblPrincipalRole in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="077b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="077b3-104">

<span> </span></span></span>

<span data-ttu-id="077b3-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="077b3-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="077b3-106">tblPrincipalRole 包含分配给节点的显式角色。</span><span class="sxs-lookup"><span data-stu-id="077b3-106">tblPrincipalRole contains explicit roles assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="077b3-107">多</span><span class="sxs-lookup"><span data-stu-id="077b3-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="077b3-108">列</span><span class="sxs-lookup"><span data-stu-id="077b3-108">Column</span></span></th>
<th><span data-ttu-id="077b3-109">类型</span><span class="sxs-lookup"><span data-stu-id="077b3-109">Type</span></span></th>
<th><span data-ttu-id="077b3-110">说明</span><span class="sxs-lookup"><span data-stu-id="077b3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="077b3-111">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="077b3-111">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="077b3-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="077b3-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="077b3-113">角色所应用的节点 ID。</span><span class="sxs-lookup"><span data-stu-id="077b3-113">Node ID that the role applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="077b3-114">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="077b3-114">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="077b3-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="077b3-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="077b3-116">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="077b3-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="077b3-117">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="077b3-117">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="077b3-118">int，not null</span><span class="sxs-lookup"><span data-stu-id="077b3-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="077b3-119">从 tblRoleType) 中 (的角色类型 ID。</span><span class="sxs-lookup"><span data-stu-id="077b3-119">Role type ID (from tblRoleType).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="077b3-120">prinRoleUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="077b3-120">prinRoleUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="077b3-121">int，not null</span><span class="sxs-lookup"><span data-stu-id="077b3-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="077b3-122">上次更新此条目的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="077b3-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="077b3-123">标示</span><span class="sxs-lookup"><span data-stu-id="077b3-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="077b3-124">列</span><span class="sxs-lookup"><span data-stu-id="077b3-124">Column</span></span></th>
<th><span data-ttu-id="077b3-125">说明</span><span class="sxs-lookup"><span data-stu-id="077b3-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="077b3-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span><span class="sxs-lookup"><span data-stu-id="077b3-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="077b3-127">主键。</span><span class="sxs-lookup"><span data-stu-id="077b3-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="077b3-128">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="077b3-128">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="077b3-129">带有 tblNode 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="077b3-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="077b3-130">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="077b3-130">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="077b3-131">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="077b3-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="077b3-132">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="077b3-132">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="077b3-133">TblRoleType 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="077b3-133">Foreign key with lookup in tblRoleType.rtypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="077b3-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="077b3-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

