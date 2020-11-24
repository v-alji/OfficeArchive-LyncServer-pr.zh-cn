---
title: Lync Server 2013：tblSkippedAffiliations
description: Lync Server 2013： tblSkippedAffiliations。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblSkippedAffiliations
ms:assetid: 0b129b54-a7a8-42a6-9279-0e08410c06ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558611(v=OCS.15)
ms:contentKeyID: 48183373
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31746cee7302d34a1d19b3059ca1da6beab9345d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392370"
---
# <a name="tblskippedaffiliations-in-lync-server-2013"></a><span data-ttu-id="55c21-103">Lync Server 2013 中的 tblSkippedAffiliations</span><span class="sxs-lookup"><span data-stu-id="55c21-103">tblSkippedAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55c21-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55c21-104">

<span> </span></span></span>

<span data-ttu-id="55c21-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="55c21-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="55c21-106">由于 Active Directory 域服务访问错误) ，tblSkippedAffiliations 包含无法读取的隶属 (。</span><span class="sxs-lookup"><span data-stu-id="55c21-106">tblSkippedAffiliations contains the affiliations that could not be read (usually due to Active Directory Domain Services access errors).</span></span>

### <a name="columns"></a><span data-ttu-id="55c21-107">多</span><span class="sxs-lookup"><span data-stu-id="55c21-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55c21-108">列</span><span class="sxs-lookup"><span data-stu-id="55c21-108">Column</span></span></th>
<th><span data-ttu-id="55c21-109">类型</span><span class="sxs-lookup"><span data-stu-id="55c21-109">Type</span></span></th>
<th><span data-ttu-id="55c21-110">说明</span><span class="sxs-lookup"><span data-stu-id="55c21-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55c21-111">prinID</span><span class="sxs-lookup"><span data-stu-id="55c21-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="55c21-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="55c21-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="55c21-113">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="55c21-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55c21-114">affDescription</span><span class="sxs-lookup"><span data-stu-id="55c21-114">affDescription</span></span></p></td>
<td><p><span data-ttu-id="55c21-115">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="55c21-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="55c21-116">标识隶属关系的字符串。</span><span class="sxs-lookup"><span data-stu-id="55c21-116">A string identifying the affiliation.</span></span></p>
<p><span data-ttu-id="55c21-117">格式为： guid： {0} uri： {1} &gt; id：{2}</span><span class="sxs-lookup"><span data-stu-id="55c21-117">The format is: guid: {0} uri: {1}&gt; id: {2}</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55c21-118">updatedBy</span><span class="sxs-lookup"><span data-stu-id="55c21-118">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="55c21-119">int，not null</span><span class="sxs-lookup"><span data-stu-id="55c21-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="55c21-120">已更新此行的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="55c21-120">ID of the principal that updated this row.</span></span> <span data-ttu-id="55c21-121">由于 Active Directory 同步是这些条目的唯一源，因此它始终为 1 (系统用户) 。</span><span class="sxs-lookup"><span data-stu-id="55c21-121">It is always 1 (system user) because Active Directory Sync is the only source for these entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="55c21-122">标示</span><span class="sxs-lookup"><span data-stu-id="55c21-122">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55c21-123"> (s) 的列</span><span class="sxs-lookup"><span data-stu-id="55c21-123">Column(s)</span></span></th>
<th><span data-ttu-id="55c21-124">说明</span><span class="sxs-lookup"><span data-stu-id="55c21-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55c21-125">&lt;prinID, affDescription&gt;</span><span class="sxs-lookup"><span data-stu-id="55c21-125">&lt;prinID, affDescription&gt;</span></span></p></td>
<td><p><span data-ttu-id="55c21-126">主键。</span><span class="sxs-lookup"><span data-stu-id="55c21-126">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55c21-127">prinID</span><span class="sxs-lookup"><span data-stu-id="55c21-127">prinID</span></span></p></td>
<td><p><span data-ttu-id="55c21-128">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="55c21-128">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="55c21-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55c21-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

