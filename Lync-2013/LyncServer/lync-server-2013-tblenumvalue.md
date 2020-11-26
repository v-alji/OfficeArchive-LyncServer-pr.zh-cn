---
title: Lync Server 2013：tblEnumValue
description: Lync Server 2013： tblEnumValue。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444446"
---
# <a name="tblenumvalue-in-lync-server-2013"></a><span data-ttu-id="d850e-103">Lync Server 2013 中的 tblEnumValue</span><span class="sxs-lookup"><span data-stu-id="d850e-103">tblEnumValue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d850e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d850e-104">

<span> </span></span></span>

<span data-ttu-id="d850e-105">_**主题上次修改时间：** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="d850e-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="d850e-106">tblEnumValue 是一个硬编码表，其中包含在节点表中使用的属性的可见性和行为值。</span><span class="sxs-lookup"><span data-stu-id="d850e-106">tblEnumValue is a hardcoded table that contains the Visibility and Behavior values of the attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="d850e-107">多</span><span class="sxs-lookup"><span data-stu-id="d850e-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d850e-108">列</span><span class="sxs-lookup"><span data-stu-id="d850e-108">Column</span></span></th>
<th><span data-ttu-id="d850e-109">类型</span><span class="sxs-lookup"><span data-stu-id="d850e-109">Type</span></span></th>
<th><span data-ttu-id="d850e-110">说明</span><span class="sxs-lookup"><span data-stu-id="d850e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d850e-111">valueID</span><span class="sxs-lookup"><span data-stu-id="d850e-111">valueID</span></span></p></td>
<td><p><span data-ttu-id="d850e-112">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="d850e-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="d850e-113">值的 ID。</span><span class="sxs-lookup"><span data-stu-id="d850e-113">ID of the value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d850e-114">attributeID</span><span class="sxs-lookup"><span data-stu-id="d850e-114">attributeID</span></span></p></td>
<td><p><span data-ttu-id="d850e-115">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="d850e-115">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="d850e-116">属性的 ID。</span><span class="sxs-lookup"><span data-stu-id="d850e-116">ID of the attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d850e-117">attributeValue</span><span class="sxs-lookup"><span data-stu-id="d850e-117">attributeValue</span></span></p></td>
<td><p><span data-ttu-id="d850e-118">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="d850e-118">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="d850e-119">值的名称。</span><span class="sxs-lookup"><span data-stu-id="d850e-119">Name of the value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="d850e-120">标示</span><span class="sxs-lookup"><span data-stu-id="d850e-120">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d850e-121">列</span><span class="sxs-lookup"><span data-stu-id="d850e-121">Column</span></span></th>
<th><span data-ttu-id="d850e-122">说明</span><span class="sxs-lookup"><span data-stu-id="d850e-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d850e-123">valueID</span><span class="sxs-lookup"><span data-stu-id="d850e-123">valueID</span></span></p></td>
<td><p><span data-ttu-id="d850e-124">主键。</span><span class="sxs-lookup"><span data-stu-id="d850e-124">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d850e-125">attributeID</span><span class="sxs-lookup"><span data-stu-id="d850e-125">attributeID</span></span></p></td>
<td><p><span data-ttu-id="d850e-126">TblEnumAttribute 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="d850e-126">Foreign key with lookup in tblEnumAttribute.attributeID table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="d850e-127">表值</span><span class="sxs-lookup"><span data-stu-id="d850e-127">Table Values</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d850e-128">valueID</span><span class="sxs-lookup"><span data-stu-id="d850e-128">valueID</span></span></th>
<th><span data-ttu-id="d850e-129">attributeID</span><span class="sxs-lookup"><span data-stu-id="d850e-129">attributeID</span></span></th>
<th><span data-ttu-id="d850e-130">attributeValue</span><span class="sxs-lookup"><span data-stu-id="d850e-130">attributeValue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d850e-131">2</span><span class="sxs-lookup"><span data-stu-id="d850e-131">2</span></span></p></td>
<td><p><span data-ttu-id="d850e-132">1</span><span class="sxs-lookup"><span data-stu-id="d850e-132">1</span></span></p></td>
<td><p><span data-ttu-id="d850e-133">专用</span><span class="sxs-lookup"><span data-stu-id="d850e-133">private</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d850e-134">3</span><span class="sxs-lookup"><span data-stu-id="d850e-134">3</span></span></p></td>
<td><p><span data-ttu-id="d850e-135">1</span><span class="sxs-lookup"><span data-stu-id="d850e-135">1</span></span></p></td>
<td><p><span data-ttu-id="d850e-136">范畴</span><span class="sxs-lookup"><span data-stu-id="d850e-136">scope</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d850e-137">4</span><span class="sxs-lookup"><span data-stu-id="d850e-137">4</span></span></p></td>
<td><p><span data-ttu-id="d850e-138">2</span><span class="sxs-lookup"><span data-stu-id="d850e-138">2</span></span></p></td>
<td><p><span data-ttu-id="d850e-139">垂直</span><span class="sxs-lookup"><span data-stu-id="d850e-139">normal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d850e-140">5</span><span class="sxs-lookup"><span data-stu-id="d850e-140">5</span></span></p></td>
<td><p><span data-ttu-id="d850e-141">2</span><span class="sxs-lookup"><span data-stu-id="d850e-141">2</span></span></p></td>
<td><p><span data-ttu-id="d850e-142">auditorium</span><span class="sxs-lookup"><span data-stu-id="d850e-142">auditorium</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d850e-143">6</span><span class="sxs-lookup"><span data-stu-id="d850e-143">6</span></span></p></td>
<td><p><span data-ttu-id="d850e-144">1</span><span class="sxs-lookup"><span data-stu-id="d850e-144">1</span></span></p></td>
<td><p><span data-ttu-id="d850e-145">公开</span><span class="sxs-lookup"><span data-stu-id="d850e-145">open</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="d850e-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d850e-146">See Also</span></span>


[<span data-ttu-id="d850e-147">Lync Server 2013 中的 tblNode</span><span class="sxs-lookup"><span data-stu-id="d850e-147">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="d850e-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d850e-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

