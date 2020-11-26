---
title: Lync Server 2013：ErrorDef 表
description: Lync Server 2013： ErrorDef 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428536"
---
# <a name="errordef-table-in-lync-server-2013"></a><span data-ttu-id="cdc9c-103">Lync Server 2013 中的 ErrorDef 表</span><span class="sxs-lookup"><span data-stu-id="cdc9c-103">ErrorDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cdc9c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cdc9c-104">

<span> </span></span></span>

<span data-ttu-id="cdc9c-105">_**主题上次修改时间：** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="cdc9c-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="cdc9c-106">ErrorDef 表存储可能出现的每种类型的错误的相关信息。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-106">The ErrorDef table stores information about each type of error that may occur.</span></span> <span data-ttu-id="cdc9c-107">每条记录是一种类型的错误。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-107">Each record is one type of error.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdc9c-108">列</span><span class="sxs-lookup"><span data-stu-id="cdc9c-108">Column</span></span></th>
<th><span data-ttu-id="cdc9c-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="cdc9c-109">Data Type</span></span></th>
<th><span data-ttu-id="cdc9c-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="cdc9c-110">Key/Index</span></span></th>
<th><span data-ttu-id="cdc9c-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="cdc9c-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdc9c-112"><strong>ErrorId</strong></span><span class="sxs-lookup"><span data-stu-id="cdc9c-112"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="cdc9c-113">int</span><span class="sxs-lookup"><span data-stu-id="cdc9c-113">int</span></span></p></td>
<td><p><span data-ttu-id="cdc9c-114">Primary</span><span class="sxs-lookup"><span data-stu-id="cdc9c-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="cdc9c-115">标识此类型错误的唯一 ID 号。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-115">Unique ID number identifying this type of error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdc9c-116"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="cdc9c-116"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="cdc9c-117">int</span><span class="sxs-lookup"><span data-stu-id="cdc9c-117">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cdc9c-118">与此错误相关联的标准 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-118">Standard SIP response code associated with this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdc9c-119"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="cdc9c-119"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="cdc9c-120">int</span><span class="sxs-lookup"><span data-stu-id="cdc9c-120">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cdc9c-121">Microsoft 诊断 ID。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-121">Microsoft Diagnostic ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdc9c-122"><strong>CallTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="cdc9c-122"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="cdc9c-123">整形</span><span class="sxs-lookup"><span data-stu-id="cdc9c-123">Int</span></span></p></td>
<td><p><span data-ttu-id="cdc9c-124">外表</span><span class="sxs-lookup"><span data-stu-id="cdc9c-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="cdc9c-125">通话的类型。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-125">Type of the call.</span></span> <span data-ttu-id="cdc9c-126">有关详细信息，请参阅 <a href="lync-server-2013-calltype-table.md">Lync Server 2013 中的 CallType 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-126">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdc9c-127"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="cdc9c-127"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="cdc9c-128">varbinary (33) </span><span class="sxs-lookup"><span data-stu-id="cdc9c-128">varbinary(33)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cdc9c-129">失败的请求类型。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-129">Type of request that failed.</span></span></p>
<p><span data-ttu-id="cdc9c-130">可以使用以下语法将此数据转换为文本格式：</span><span class="sxs-lookup"><span data-stu-id="cdc9c-130">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdc9c-131"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="cdc9c-131"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="cdc9c-132">varbinary (257) </span><span class="sxs-lookup"><span data-stu-id="cdc9c-132">varbinary(257)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cdc9c-133">失败的请求的内容类型。</span><span class="sxs-lookup"><span data-stu-id="cdc9c-133">Content type of the request that failed.</span></span></p>
<p><span data-ttu-id="cdc9c-134">可使用此 syntaxt 将此数据转换为文本格式：</span><span class="sxs-lookup"><span data-stu-id="cdc9c-134">This data can be converted to text format by using this syntaxt:</span></span></p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cdc9c-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cdc9c-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

