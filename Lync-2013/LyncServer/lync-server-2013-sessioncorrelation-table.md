---
title: Lync Server 2013：SessionCorrelation 表
description: Lync Server 2013： SessionCorrelation 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionCorrelation table
ms:assetid: 041705e1-7290-464f-95f8-96256cfa2e3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398091(v=OCS.15)
ms:contentKeyID: 48183267
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 814b7e8539d89f87e7df60ceb03e70800553fb55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424077"
---
# <a name="sessioncorrelation-table-in-lync-server-2013"></a><span data-ttu-id="a90a4-103">Lync Server 2013 中的 SessionCorrelation 表</span><span class="sxs-lookup"><span data-stu-id="a90a4-103">SessionCorrelation table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a90a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a90a4-104">

<span> </span></span></span>

<span data-ttu-id="a90a4-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="a90a4-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="a90a4-106">SessionCorrelation 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="a90a4-106">The SessionCorrelation table is a supporting table.</span></span> <span data-ttu-id="a90a4-107">每条记录表示一个 CorrelationID，用于关联多个会话。</span><span class="sxs-lookup"><span data-stu-id="a90a4-107">Each record represents one CorrelationID which is used to correlate multiple sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a90a4-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="a90a4-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="a90a4-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="a90a4-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a90a4-112"><strong>检查</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-112"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="a90a4-113">int</span><span class="sxs-lookup"><span data-stu-id="a90a4-113">int</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a90a4-114"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-114"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="a90a4-115">int</span><span class="sxs-lookup"><span data-stu-id="a90a4-115">int</span></span></p></td>
<td><p><span data-ttu-id="a90a4-116">Primary</span><span class="sxs-lookup"><span data-stu-id="a90a4-116">Primary</span></span></p></td>
<td><p><span data-ttu-id="a90a4-117">标识此 A/V 会议服务器的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="a90a4-117">Unique number identifying this A/V Conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a90a4-118"><strong>True&correlationid</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-118"><strong>CorrelationID</strong></span></span></p></td>
<td><p><span data-ttu-id="a90a4-119">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a90a4-119">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a90a4-120">唯一</span><span class="sxs-lookup"><span data-stu-id="a90a4-120">Unique</span></span></p></td>
<td><p><span data-ttu-id="a90a4-121">关联的会话将具有相同的相关性 ID。</span><span class="sxs-lookup"><span data-stu-id="a90a4-121">Sessions that are correlated will have the same correlation ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a90a4-122"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="a90a4-122"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="a90a4-123">datetime</span><span class="sxs-lookup"><span data-stu-id="a90a4-123">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a90a4-124">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="a90a4-124">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a90a4-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a90a4-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

