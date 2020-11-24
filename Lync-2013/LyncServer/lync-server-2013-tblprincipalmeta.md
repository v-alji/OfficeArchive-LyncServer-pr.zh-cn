---
title: Lync Server 2013：tblPrincipalMeta
description: Lync Server 2013： tblPrincipalMeta。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMeta
ms:assetid: 808490d4-7d6d-47a2-b8af-b5940d47073b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615009(v=OCS.15)
ms:contentKeyID: 48184648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 899fd1e450dac52afa56c1ee1de86da82b2db309
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391804"
---
# <a name="tblprincipalmeta-in-lync-server-2013"></a><span data-ttu-id="e8139-103">Lync Server 2013 中的 tblPrincipalMeta</span><span class="sxs-lookup"><span data-stu-id="e8139-103">tblPrincipalMeta in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8139-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8139-104">

<span> </span></span></span>

<span data-ttu-id="e8139-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="e8139-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="e8139-106">tblPrincipalMeta 包含必须从 Active Directory 域服务刷新的主体。</span><span class="sxs-lookup"><span data-stu-id="e8139-106">tblPrincipalMeta contains the principals that have to be refreshed from Active Directory Domain Services.</span></span>

### <a name="columns"></a><span data-ttu-id="e8139-107">多</span><span class="sxs-lookup"><span data-stu-id="e8139-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8139-108">列</span><span class="sxs-lookup"><span data-stu-id="e8139-108">Column</span></span></th>
<th><span data-ttu-id="e8139-109">类型</span><span class="sxs-lookup"><span data-stu-id="e8139-109">Type</span></span></th>
<th><span data-ttu-id="e8139-110">说明</span><span class="sxs-lookup"><span data-stu-id="e8139-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8139-111">prinID</span><span class="sxs-lookup"><span data-stu-id="e8139-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="e8139-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="e8139-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="e8139-113">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="e8139-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8139-114">prinAffiliationsDirty</span><span class="sxs-lookup"><span data-stu-id="e8139-114">prinAffiliationsDirty</span></span></p></td>
<td><p><span data-ttu-id="e8139-115">位，not null</span><span class="sxs-lookup"><span data-stu-id="e8139-115">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="e8139-116">如果必须刷新主体隶属关系，则为 True。</span><span class="sxs-lookup"><span data-stu-id="e8139-116">True if principal affiliations have to be refreshed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8139-117">prinAttributesDirty</span><span class="sxs-lookup"><span data-stu-id="e8139-117">prinAttributesDirty</span></span></p></td>
<td><p><span data-ttu-id="e8139-118">位，not null</span><span class="sxs-lookup"><span data-stu-id="e8139-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="e8139-119">如果必须刷新主体属性，则为 True。</span><span class="sxs-lookup"><span data-stu-id="e8139-119">True if principal attributes have to be refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8139-120">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="e8139-120">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="e8139-121">位，not null</span><span class="sxs-lookup"><span data-stu-id="e8139-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="e8139-122">如果主体已被删除，则为 True。</span><span class="sxs-lookup"><span data-stu-id="e8139-122">True if the principal has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8139-123">tryCount</span><span class="sxs-lookup"><span data-stu-id="e8139-123">tryCount</span></span></p></td>
<td><p><span data-ttu-id="e8139-124">int</span><span class="sxs-lookup"><span data-stu-id="e8139-124">int</span></span></p></td>
<td><p><span data-ttu-id="e8139-125">尝试从目前为止发生的 AD DS 刷新主体的次数。</span><span class="sxs-lookup"><span data-stu-id="e8139-125">Number of attempts to refresh the principal from AD DS that have happened so far.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8139-126">lastTry</span><span class="sxs-lookup"><span data-stu-id="e8139-126">lastTry</span></span></p></td>
<td><p><span data-ttu-id="e8139-127">datetime</span><span class="sxs-lookup"><span data-stu-id="e8139-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="e8139-128">从最新尝试刷新主体的时间戳。</span><span class="sxs-lookup"><span data-stu-id="e8139-128">Time stamp from the latest attempt to refresh the principal.</span></span> <span data-ttu-id="e8139-129">如果尚未尝试刷新，则可以为 null。</span><span class="sxs-lookup"><span data-stu-id="e8139-129">Can be null if no refresh has been attempted yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8139-130">nextTry</span><span class="sxs-lookup"><span data-stu-id="e8139-130">nextTry</span></span></p></td>
<td><p><span data-ttu-id="e8139-131">datetime</span><span class="sxs-lookup"><span data-stu-id="e8139-131">datetime</span></span></p></td>
<td><p><span data-ttu-id="e8139-132">下一次计划刷新的时间戳。</span><span class="sxs-lookup"><span data-stu-id="e8139-132">Time stamp for the next scheduled refresh.</span></span> <span data-ttu-id="e8139-133">如果尚未安排进一步刷新，则可以为 null。</span><span class="sxs-lookup"><span data-stu-id="e8139-133">Can be null if no further refresh has been scheduled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="e8139-134">标示</span><span class="sxs-lookup"><span data-stu-id="e8139-134">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8139-135">列</span><span class="sxs-lookup"><span data-stu-id="e8139-135">Column</span></span></th>
<th><span data-ttu-id="e8139-136">说明</span><span class="sxs-lookup"><span data-stu-id="e8139-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8139-137">prinID</span><span class="sxs-lookup"><span data-stu-id="e8139-137">prinID</span></span></p></td>
<td><p><span data-ttu-id="e8139-138">主键。</span><span class="sxs-lookup"><span data-stu-id="e8139-138">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8139-139">prinID</span><span class="sxs-lookup"><span data-stu-id="e8139-139">prinID</span></span></p></td>
<td><p><span data-ttu-id="e8139-140">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="e8139-140">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e8139-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8139-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

