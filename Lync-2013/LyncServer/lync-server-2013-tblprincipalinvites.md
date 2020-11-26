---
title: Lync Server 2013：tblPrincipalInvites
description: Lync Server 2013： tblPrincipalInvites。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423503"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a><span data-ttu-id="11767-103">Lync Server 2013 中的 tblPrincipalInvites</span><span class="sxs-lookup"><span data-stu-id="11767-103">tblPrincipalInvites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="11767-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="11767-104">

<span> </span></span></span>

<span data-ttu-id="11767-105">_**主题上次修改时间：** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="11767-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="11767-106">tblPrincipalInvites 包含所有已预配用户的带有自动邀请的所有节点的邀请。</span><span class="sxs-lookup"><span data-stu-id="11767-106">tblPrincipalInvites contains invitations for all provisioned users for all nodes with auto-invite on.</span></span>

### <a name="columns"></a><span data-ttu-id="11767-107">多</span><span class="sxs-lookup"><span data-stu-id="11767-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11767-108">列</span><span class="sxs-lookup"><span data-stu-id="11767-108">Column</span></span></th>
<th><span data-ttu-id="11767-109">类型</span><span class="sxs-lookup"><span data-stu-id="11767-109">Type</span></span></th>
<th><span data-ttu-id="11767-110">说明</span><span class="sxs-lookup"><span data-stu-id="11767-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11767-111">prinID</span><span class="sxs-lookup"><span data-stu-id="11767-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="11767-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="11767-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="11767-113">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="11767-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11767-114">invID</span><span class="sxs-lookup"><span data-stu-id="11767-114">invID</span></span></p></td>
<td><p><span data-ttu-id="11767-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="11767-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="11767-116"> (从 tblLastInviteId 表生成的每个主体 ID) 唯一序列号。</span><span class="sxs-lookup"><span data-stu-id="11767-116">Unique sequential number (per principal ID) generated from tblLastInviteId table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11767-117">a</span><span class="sxs-lookup"><span data-stu-id="11767-117">nodeID</span></span></p></td>
<td><p><span data-ttu-id="11767-118">int，not null</span><span class="sxs-lookup"><span data-stu-id="11767-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="11767-119">节点 ID (仅) 聊天室。</span><span class="sxs-lookup"><span data-stu-id="11767-119">Node ID (chat room only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11767-120">createdOn</span><span class="sxs-lookup"><span data-stu-id="11767-120">createdOn</span></span></p></td>
<td><p><span data-ttu-id="11767-121">datetime，not null</span><span class="sxs-lookup"><span data-stu-id="11767-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="11767-122">创建时间。</span><span class="sxs-lookup"><span data-stu-id="11767-122">Time of creation.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="11767-123">标示</span><span class="sxs-lookup"><span data-stu-id="11767-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11767-124">列</span><span class="sxs-lookup"><span data-stu-id="11767-124">Column</span></span></th>
<th><span data-ttu-id="11767-125">说明</span><span class="sxs-lookup"><span data-stu-id="11767-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11767-126">&lt;prinID、&gt;</span><span class="sxs-lookup"><span data-stu-id="11767-126">&lt;prinID, nodeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="11767-127">主键。</span><span class="sxs-lookup"><span data-stu-id="11767-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11767-128">prinID</span><span class="sxs-lookup"><span data-stu-id="11767-128">prinID</span></span></p></td>
<td><p><span data-ttu-id="11767-129">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="11767-129">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11767-130">a</span><span class="sxs-lookup"><span data-stu-id="11767-130">nodeID</span></span></p></td>
<td><p><span data-ttu-id="11767-131">带有 tblNode 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="11767-131">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="11767-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="11767-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

