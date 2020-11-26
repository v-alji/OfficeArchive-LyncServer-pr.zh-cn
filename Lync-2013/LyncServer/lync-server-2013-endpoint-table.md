---
title: Lync Server 2013：Endpoint 表
description: Lync Server 2013：终结点表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Endpoint table
ms:assetid: 500f330d-4d7d-4e88-b1cc-fef9a9de6b5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398327(v=OCS.15)
ms:contentKeyID: 48184098
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614872eee41b5d8e56da4b96cf5bbe3a4a1cf4d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428676"
---
# <a name="endpoint-table-in-lync-server-2013"></a><span data-ttu-id="bda9f-103">Lync Server 2013 中的 Endpoint 表</span><span class="sxs-lookup"><span data-stu-id="bda9f-103">Endpoint table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bda9f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bda9f-104">

<span> </span></span></span>

<span data-ttu-id="bda9f-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="bda9f-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="bda9f-106">终结点表是一个支持表，用于存储参与数据库中记录的会话的终结点的相关信息。</span><span class="sxs-lookup"><span data-stu-id="bda9f-106">The Endpoint table is a supporting table that stores information about the endpoints that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="bda9f-107">表中的每条记录表示一个终结点。</span><span class="sxs-lookup"><span data-stu-id="bda9f-107">Each record in the table represents one endpoint.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bda9f-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="bda9f-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="bda9f-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="bda9f-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bda9f-112"><strong>EndpointKey</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-112"><strong>EndpointKey</strong></span></span></p></td>
<td><p><span data-ttu-id="bda9f-113">int</span><span class="sxs-lookup"><span data-stu-id="bda9f-113">int</span></span></p></td>
<td><p><span data-ttu-id="bda9f-114">Primary</span><span class="sxs-lookup"><span data-stu-id="bda9f-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="bda9f-115">标识此终结点的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="bda9f-115">Unique number identifying this endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bda9f-116"><strong>名称</strong> - 按 WAN 链路进行筛选（筛选器位于图形右侧）。</span><span class="sxs-lookup"><span data-stu-id="bda9f-116"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="bda9f-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bda9f-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bda9f-118">唯一</span><span class="sxs-lookup"><span data-stu-id="bda9f-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="bda9f-119">终结点名称。</span><span class="sxs-lookup"><span data-stu-id="bda9f-119">Endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bda9f-120"><strong>OS</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-120"><strong>OS</strong></span></span></p></td>
<td><p><span data-ttu-id="bda9f-121">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="bda9f-121">nvarchar(128)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="bda9f-122">终结点 (操作系统) 。</span><span class="sxs-lookup"><span data-stu-id="bda9f-122">Operating system (OS) of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bda9f-123"><strong>CPUName</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-123"><strong>CPUName</strong></span></span></p></td>
<td><p><span data-ttu-id="bda9f-124">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="bda9f-124">nvarchar(128)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bda9f-125">终结点的 CPU 名称。</span><span class="sxs-lookup"><span data-stu-id="bda9f-125">CPU name of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bda9f-126"><strong>CPUNumberOfCores</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-126"><strong>CPUNumberOfCores</strong></span></span></p></td>
<td><p><span data-ttu-id="bda9f-127">smallint</span><span class="sxs-lookup"><span data-stu-id="bda9f-127">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bda9f-128">终结点的 CPU 内核数。</span><span class="sxs-lookup"><span data-stu-id="bda9f-128">Number of CPU cores of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bda9f-129"><strong>CPUProcessorSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-129"><strong>CPUProcessorSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="bda9f-130">int</span><span class="sxs-lookup"><span data-stu-id="bda9f-130">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bda9f-131">终结点的 CPU 处理器速度。</span><span class="sxs-lookup"><span data-stu-id="bda9f-131">CPU processor speed of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bda9f-132"><strong>VirtualizationFlag</strong></span><span class="sxs-lookup"><span data-stu-id="bda9f-132"><strong>VirtualizationFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="bda9f-133">tinyint</span><span class="sxs-lookup"><span data-stu-id="bda9f-133">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bda9f-134">指示系统是否在虚拟化环境中运行的位标志：</span><span class="sxs-lookup"><span data-stu-id="bda9f-134">Bit flag that indicates if the system is running in a virtualized environment:</span></span></p>
<ul>
<li><p><span data-ttu-id="bda9f-135">0x0000 –无</span><span class="sxs-lookup"><span data-stu-id="bda9f-135">0x0000 – None</span></span></p></li>
<li><p><span data-ttu-id="bda9f-136">0x0001-HyperV</span><span class="sxs-lookup"><span data-stu-id="bda9f-136">0x0001 – HyperV</span></span></p></li>
<li><p><span data-ttu-id="bda9f-137">0x0002-VMWare</span><span class="sxs-lookup"><span data-stu-id="bda9f-137">0x0002 – VMWare</span></span></p></li>
<li><p><span data-ttu-id="bda9f-138">0x0004-虚拟电脑</span><span class="sxs-lookup"><span data-stu-id="bda9f-138">0x0004 – Virtual PC</span></span></p></li>
<li><p><span data-ttu-id="bda9f-139">0x0008-Xen 电脑</span><span class="sxs-lookup"><span data-stu-id="bda9f-139">0x0008 – Xen PC</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="bda9f-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bda9f-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

