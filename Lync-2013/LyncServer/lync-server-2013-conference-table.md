---
title: Lync Server 2013：Conference 表
description: Lync Server 2013：电话会议表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference table
ms:assetid: 2a2c327c-4719-42dc-a3bb-6dbc0864d9af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425762(v=OCS.15)
ms:contentKeyID: 48183700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 565725b527399cb3be55c649dfd74d8bcb5f13a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434464"
---
# <a name="conference-table-in-lync-server-2013"></a><span data-ttu-id="365a5-103">Lync Server 2013 中的 Conference 表</span><span class="sxs-lookup"><span data-stu-id="365a5-103">Conference table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="365a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="365a5-104">

<span> </span></span></span>

<span data-ttu-id="365a5-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="365a5-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="365a5-106">会议表是支持表。</span><span class="sxs-lookup"><span data-stu-id="365a5-106">The Conference table is a supporting table.</span></span> <span data-ttu-id="365a5-107">每条记录表示一个会议或对等会话。</span><span class="sxs-lookup"><span data-stu-id="365a5-107">Each record represents one conference or peer-to-peer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="365a5-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="365a5-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="365a5-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="365a5-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="365a5-112"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-112"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="365a5-113">int</span><span class="sxs-lookup"><span data-stu-id="365a5-113">int</span></span></p></td>
<td><p><span data-ttu-id="365a5-114">Primary</span><span class="sxs-lookup"><span data-stu-id="365a5-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="365a5-115">标识此会议记录的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="365a5-115">Unique number identifying this conference record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="365a5-116"><strong>ConfURI</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-116"><strong>ConfURI</strong></span></span></p></td>
<td><p><span data-ttu-id="365a5-117">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="365a5-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="365a5-118">唯一</span><span class="sxs-lookup"><span data-stu-id="365a5-118">unique</span></span></p></td>
<td><p><span data-ttu-id="365a5-119">会议 URI （如果这是会议）或 DialogID （如果这是对等会话）。</span><span class="sxs-lookup"><span data-stu-id="365a5-119">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="365a5-120"><strong>检查</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-120"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="365a5-121">int</span><span class="sxs-lookup"><span data-stu-id="365a5-121">int</span></span></p></td>
<td><p><span data-ttu-id="365a5-122">食指</span><span class="sxs-lookup"><span data-stu-id="365a5-122">index</span></span></p></td>
<td><p><span data-ttu-id="365a5-123">会议 URI 的校验和。</span><span class="sxs-lookup"><span data-stu-id="365a5-123">Checksum of the conference URI.</span></span> <span data-ttu-id="365a5-124">此功能在内部使用。</span><span class="sxs-lookup"><span data-stu-id="365a5-124">This is used internally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="365a5-125"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="365a5-125"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="365a5-126">datetime</span><span class="sxs-lookup"><span data-stu-id="365a5-126">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="365a5-127">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="365a5-127">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="365a5-128">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="365a5-128">


</div>

<span> </span>

</div>

</div>

</span></span></div>

