---
title: Lync Server 2013： ErrorCategory 表
description: Lync Server 2013： ErrorCategory 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorCategory table
ms:assetid: 0fde3b73-9a2f-44dd-b8dc-6df512303ff1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204675(v=OCS.15)
ms:contentKeyID: 48183425
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8154c73f33b5dad62a338335a960553cfc06ec13
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428564"
---
# <a name="errorcategory-table-in-lync-server-2013"></a><span data-ttu-id="02800-103">Lync Server 2013 中的 ErrorCategory 表</span><span class="sxs-lookup"><span data-stu-id="02800-103">ErrorCategory table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02800-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02800-104">

<span> </span></span></span>

<span data-ttu-id="02800-105">_**主题上次修改时间：** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="02800-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="02800-106">ErrorCategory 表包含每个 Microsoft Lync Server 2013 诊断分类的友好名称。</span><span class="sxs-lookup"><span data-stu-id="02800-106">The ErrorCategory table contains the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span> <span data-ttu-id="02800-107">默认情况下，Lync Server 2013 使用以下分类：</span><span class="sxs-lookup"><span data-stu-id="02800-107">By default, Lync Server 2013 uses the following classifications:</span></span>

  - <span data-ttu-id="02800-108">0--成功</span><span class="sxs-lookup"><span data-stu-id="02800-108">0 -- Success</span></span>

  - <span data-ttu-id="02800-109">1--预期故障</span><span class="sxs-lookup"><span data-stu-id="02800-109">1 -- Expected failure</span></span>

  - <span data-ttu-id="02800-110">2-意外故障</span><span class="sxs-lookup"><span data-stu-id="02800-110">2 – Unexpected failure</span></span>

<span data-ttu-id="02800-111">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="02800-111">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02800-112">列</span><span class="sxs-lookup"><span data-stu-id="02800-112">Column</span></span></th>
<th><span data-ttu-id="02800-113">数据类型</span><span class="sxs-lookup"><span data-stu-id="02800-113">Data Type</span></span></th>
<th><span data-ttu-id="02800-114">键/索引</span><span class="sxs-lookup"><span data-stu-id="02800-114">Key/Index</span></span></th>
<th><span data-ttu-id="02800-115">详细信息</span><span class="sxs-lookup"><span data-stu-id="02800-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02800-116"><strong>CategoryId</strong></span><span class="sxs-lookup"><span data-stu-id="02800-116"><strong>CategoryId</strong></span></span></p></td>
<td><p><span data-ttu-id="02800-117">tinyint</span><span class="sxs-lookup"><span data-stu-id="02800-117">tinyint</span></span></p></td>
<td><p><span data-ttu-id="02800-118">Primary</span><span class="sxs-lookup"><span data-stu-id="02800-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="02800-119">分类的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="02800-119">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02800-120"><strong>名称</strong> - 按 WAN 链路进行筛选（筛选器位于图形右侧）。</span><span class="sxs-lookup"><span data-stu-id="02800-120"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="02800-121">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="02800-121">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="02800-122">分配给分类的值和友好名称。</span><span class="sxs-lookup"><span data-stu-id="02800-122">Value and friendly name assigned to the classification.</span></span> <span data-ttu-id="02800-123">允许的值包括：</span><span class="sxs-lookup"><span data-stu-id="02800-123">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="02800-124">0--成功</span><span class="sxs-lookup"><span data-stu-id="02800-124">0 -- Success</span></span></p></li>
<li><p><span data-ttu-id="02800-125">1--预期故障</span><span class="sxs-lookup"><span data-stu-id="02800-125">1 -- Expected failure</span></span></p></li>
<li><p><span data-ttu-id="02800-126">2-意外故障</span><span class="sxs-lookup"><span data-stu-id="02800-126">2 – Unexpected failure</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="02800-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02800-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

