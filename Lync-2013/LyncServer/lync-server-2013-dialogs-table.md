---
title: Lync Server 2013：Dialogs 表
description: Lync Server 2013：对话框表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialogs table
ms:assetid: 487a430b-af66-4ea6-b28e-4e33cfdb7f9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425954(v=OCS.15)
ms:contentKeyID: 48184001
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c2c9cf9ec59fc48f7f5ffc6232980e3f8aa68c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429180"
---
# <a name="dialogs-table-in-lync-server-2013"></a><span data-ttu-id="2fef5-103">Lync Server 2013 中的 Dialogs 表</span><span class="sxs-lookup"><span data-stu-id="2fef5-103">Dialogs table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2fef5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2fef5-104">

<span> </span></span></span>

<span data-ttu-id="2fef5-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="2fef5-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="2fef5-106">对话框表是一个支持表，用于存储有关对等会话的 DialogIDs 的信息。</span><span class="sxs-lookup"><span data-stu-id="2fef5-106">The Dialogs table is a supporting table that stores the information about DialogIDs for peer-to-peer sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2fef5-107">列</span><span class="sxs-lookup"><span data-stu-id="2fef5-107">Column</span></span></th>
<th><span data-ttu-id="2fef5-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="2fef5-108">Data Type</span></span></th>
<th><span data-ttu-id="2fef5-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="2fef5-109">Key/Index</span></span></th>
<th><span data-ttu-id="2fef5-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="2fef5-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fef5-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="2fef5-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2fef5-112">datetime</span><span class="sxs-lookup"><span data-stu-id="2fef5-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="2fef5-113">Primary</span><span class="sxs-lookup"><span data-stu-id="2fef5-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="2fef5-114">会话请求的时间;与 SessionIDSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="2fef5-114">Time of session request; used in conjunction with SessionIDSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fef5-115"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="2fef5-115"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="2fef5-116">int</span><span class="sxs-lookup"><span data-stu-id="2fef5-116">int</span></span></p></td>
<td><p><span data-ttu-id="2fef5-117">Primary</span><span class="sxs-lookup"><span data-stu-id="2fef5-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="2fef5-118">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="2fef5-118">ID number to identify the session.</span></span> <span data-ttu-id="2fef5-119">与 SessionIDTime 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="2fef5-119">Used in conjunction with SessionIDTime to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fef5-120"><strong>ExternalChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="2fef5-120"><strong>ExternalChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="2fef5-121">int</span><span class="sxs-lookup"><span data-stu-id="2fef5-121">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="2fef5-122">ExternalID 的校验和。</span><span class="sxs-lookup"><span data-stu-id="2fef5-122">Checksum of the ExternalID.</span></span> <span data-ttu-id="2fef5-123">此字段用于提高数据库搜索的速度。</span><span class="sxs-lookup"><span data-stu-id="2fef5-123">This field is used to increase the speed of database searches.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fef5-124"><strong>ExternalId</strong></span><span class="sxs-lookup"><span data-stu-id="2fef5-124"><strong>ExternalId</strong></span></span></p></td>
<td><p><span data-ttu-id="2fef5-125">varbinary (775) </span><span class="sxs-lookup"><span data-stu-id="2fef5-125">varbinary(775)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="2fef5-126">SIP 对话框 ID，存储为二进制。</span><span class="sxs-lookup"><span data-stu-id="2fef5-126">SIP dialog ID, stored as a binary.</span></span> <span data-ttu-id="2fef5-127">二进制文件的格式为：</span><span class="sxs-lookup"><span data-stu-id="2fef5-127">The format of the binary is:</span></span></p>
<p><span data-ttu-id="2fef5-128">对话框; 从-标签; 到-标记</span><span class="sxs-lookup"><span data-stu-id="2fef5-128">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="2fef5-129">可以使用以下语法将此数据转换为文本格式：</span><span class="sxs-lookup"><span data-stu-id="2fef5-129">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2fef5-130">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2fef5-130">


</div>

<span> </span>

</div>

</div>

</span></span></div>

