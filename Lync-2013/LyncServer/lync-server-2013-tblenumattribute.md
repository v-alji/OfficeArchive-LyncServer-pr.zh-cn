---
title: Lync Server 2013：tblEnumAttribute
description: Lync Server 2013： tblEnumAttribute。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumAttribute
ms:assetid: 17f8b87e-36a6-4f6a-8630-7c76b61a7595
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558617(v=OCS.15)
ms:contentKeyID: 48183523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca979a68e758ad47b691ac704f24c68c1841938a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423538"
---
# <a name="tblenumattribute-in-lync-server-2013"></a><span data-ttu-id="7a5db-103">Lync Server 2013 中的 tblEnumAttribute</span><span class="sxs-lookup"><span data-stu-id="7a5db-103">tblEnumAttribute in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a5db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a5db-104">

<span> </span></span></span>

<span data-ttu-id="7a5db-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="7a5db-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="7a5db-106">tblEnumAttribute 是一个硬编码表，其中包含在节点表中使用的 Visibility 和行为属性。</span><span class="sxs-lookup"><span data-stu-id="7a5db-106">tblEnumAttribute is a hardcoded table that contains the Visibility and Behavior attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="7a5db-107">多</span><span class="sxs-lookup"><span data-stu-id="7a5db-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a5db-108">列</span><span class="sxs-lookup"><span data-stu-id="7a5db-108">Column</span></span></th>
<th><span data-ttu-id="7a5db-109">类型</span><span class="sxs-lookup"><span data-stu-id="7a5db-109">Type</span></span></th>
<th><span data-ttu-id="7a5db-110">说明</span><span class="sxs-lookup"><span data-stu-id="7a5db-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a5db-111">attributeID</span><span class="sxs-lookup"><span data-stu-id="7a5db-111">attributeID</span></span></p></td>
<td><p><span data-ttu-id="7a5db-112">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="7a5db-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="7a5db-113">属性的 ID。</span><span class="sxs-lookup"><span data-stu-id="7a5db-113">ID of the attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5db-114">attributeName</span><span class="sxs-lookup"><span data-stu-id="7a5db-114">attributeName</span></span></p></td>
<td><p><span data-ttu-id="7a5db-115">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="7a5db-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="7a5db-116">属性的名称。</span><span class="sxs-lookup"><span data-stu-id="7a5db-116">Name of the attribute.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="7a5db-117">密钥</span><span class="sxs-lookup"><span data-stu-id="7a5db-117">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a5db-118">列</span><span class="sxs-lookup"><span data-stu-id="7a5db-118">Column</span></span></th>
<th><span data-ttu-id="7a5db-119">说明</span><span class="sxs-lookup"><span data-stu-id="7a5db-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a5db-120">attributeID</span><span class="sxs-lookup"><span data-stu-id="7a5db-120">attributeID</span></span></p></td>
<td><p><span data-ttu-id="7a5db-121">主键。</span><span class="sxs-lookup"><span data-stu-id="7a5db-121">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="7a5db-122">表值</span><span class="sxs-lookup"><span data-stu-id="7a5db-122">Table Values</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a5db-123">attributeID</span><span class="sxs-lookup"><span data-stu-id="7a5db-123">attributeID</span></span></th>
<th><span data-ttu-id="7a5db-124">attributeName</span><span class="sxs-lookup"><span data-stu-id="7a5db-124">attributeName</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a5db-125">1</span><span class="sxs-lookup"><span data-stu-id="7a5db-125">1</span></span></p></td>
<td><p><span data-ttu-id="7a5db-126">了解.</span><span class="sxs-lookup"><span data-stu-id="7a5db-126">Visibility.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5db-127">2</span><span class="sxs-lookup"><span data-stu-id="7a5db-127">2</span></span></p></td>
<td><p><span data-ttu-id="7a5db-128">现象.</span><span class="sxs-lookup"><span data-stu-id="7a5db-128">Behavior.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="7a5db-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a5db-129">See Also</span></span>


[<span data-ttu-id="7a5db-130">Lync Server 2013 中的 tblNode</span><span class="sxs-lookup"><span data-stu-id="7a5db-130">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="7a5db-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a5db-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

