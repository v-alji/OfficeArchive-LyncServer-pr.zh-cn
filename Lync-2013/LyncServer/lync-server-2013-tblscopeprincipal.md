---
title: Lync Server 2013：tblScopePrincipal
description: Lync Server 2013： tblScopePrincipal。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblScopePrincipal
ms:assetid: 422d6c7f-7ba7-4dd4-bacc-95ace47959ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558639(v=OCS.15)
ms:contentKeyID: 48184009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63315f8525e5c2f05fe54a0f9ed9e8a97b9e8bce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391791"
---
# <a name="tblscopeprincipal-in-lync-server-2013"></a><span data-ttu-id="96037-103">Lync Server 2013 中的 tblScopePrincipal</span><span class="sxs-lookup"><span data-stu-id="96037-103">tblScopePrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96037-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96037-104">

<span> </span></span></span>

<span data-ttu-id="96037-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="96037-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="96037-106">tblScopePrincipal 包含分配给节点的作用域。</span><span class="sxs-lookup"><span data-stu-id="96037-106">tblScopePrincipal contains scopes assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="96037-107">多</span><span class="sxs-lookup"><span data-stu-id="96037-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96037-108">列</span><span class="sxs-lookup"><span data-stu-id="96037-108">Column</span></span></th>
<th><span data-ttu-id="96037-109">类型</span><span class="sxs-lookup"><span data-stu-id="96037-109">Type</span></span></th>
<th><span data-ttu-id="96037-110">说明</span><span class="sxs-lookup"><span data-stu-id="96037-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96037-111">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="96037-111">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="96037-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="96037-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="96037-113">作用域所适用的节点 ID。</span><span class="sxs-lookup"><span data-stu-id="96037-113">Node ID that the scope applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96037-114">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="96037-114">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="96037-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="96037-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="96037-116">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="96037-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96037-117">scopeIsDenied</span><span class="sxs-lookup"><span data-stu-id="96037-117">scopeIsDenied</span></span></p></td>
<td><p><span data-ttu-id="96037-118">位，not null</span><span class="sxs-lookup"><span data-stu-id="96037-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="96037-119">如果范围的类型为 "拒绝"，则为 True;如果允许，则为 False。</span><span class="sxs-lookup"><span data-stu-id="96037-119">True if type of scope is Deny; False if Allow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96037-120">scopeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="96037-120">scopeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="96037-121">int，not null</span><span class="sxs-lookup"><span data-stu-id="96037-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="96037-122">上次更新此条目的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="96037-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="96037-123">标示</span><span class="sxs-lookup"><span data-stu-id="96037-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96037-124">列</span><span class="sxs-lookup"><span data-stu-id="96037-124">Column</span></span></th>
<th><span data-ttu-id="96037-125">说明</span><span class="sxs-lookup"><span data-stu-id="96037-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96037-126">&lt;scopeNodeID, scopePrinID&gt;</span><span class="sxs-lookup"><span data-stu-id="96037-126">&lt;scopeNodeID, scopePrinID&gt;</span></span></p></td>
<td><p><span data-ttu-id="96037-127">主键。</span><span class="sxs-lookup"><span data-stu-id="96037-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96037-128">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="96037-128">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="96037-129">带有 tblNode 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="96037-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96037-130">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="96037-130">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="96037-131">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="96037-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="96037-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96037-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

