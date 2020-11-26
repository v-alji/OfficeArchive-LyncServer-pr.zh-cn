---
title: Lync Server 2013：Device 表
description: Lync Server 2013： Device 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device table
ms:assetid: d5a4f777-bc12-4ce8-bc0d-867d5e22b436
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398930(v=OCS.15)
ms:contentKeyID: 48185544
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46de64a49eace52d62cbd6384fcae680b5c511b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429410"
---
# <a name="device-table-in-lync-server-2013"></a><span data-ttu-id="24590-103">Lync Server 2013 中的 Device 表</span><span class="sxs-lookup"><span data-stu-id="24590-103">Device table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24590-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24590-104">

<span> </span></span></span>

<span data-ttu-id="24590-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="24590-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="24590-106">Device 表是一个支持表，用于存储有关各种捕获或呈现设备的信息。</span><span class="sxs-lookup"><span data-stu-id="24590-106">The Device table is a supporting table that stores information about the various capture or render devices.</span></span> <span data-ttu-id="24590-107">表中的每条记录表示一个设备。</span><span class="sxs-lookup"><span data-stu-id="24590-107">Each record in the table represents one device.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24590-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="24590-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="24590-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="24590-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="24590-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="24590-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="24590-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="24590-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24590-112"><strong>DeviceKey</strong></span><span class="sxs-lookup"><span data-stu-id="24590-112"><strong>DeviceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="24590-113">int</span><span class="sxs-lookup"><span data-stu-id="24590-113">int</span></span></p></td>
<td><p><span data-ttu-id="24590-114">Primary</span><span class="sxs-lookup"><span data-stu-id="24590-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="24590-115">标识此设备的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="24590-115">Unique number identifying this device.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24590-116"><strong>DeviceName</strong></span><span class="sxs-lookup"><span data-stu-id="24590-116"><strong>DeviceName</strong></span></span></p></td>
<td><p><span data-ttu-id="24590-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="24590-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="24590-118">DeviceName + DeviceType 是唯一的</span><span class="sxs-lookup"><span data-stu-id="24590-118">DeviceName + DeviceType is unique</span></span></p></td>
<td><p><span data-ttu-id="24590-119">设备名称。</span><span class="sxs-lookup"><span data-stu-id="24590-119">Device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24590-120"><strong>DeviceType</strong></span><span class="sxs-lookup"><span data-stu-id="24590-120"><strong>DeviceType</strong></span></span></p></td>
<td><p><span data-ttu-id="24590-121">bit</span><span class="sxs-lookup"><span data-stu-id="24590-121">bit</span></span></p></td>
<td><p><span data-ttu-id="24590-122">DeviceName + DeviceType 是唯一的</span><span class="sxs-lookup"><span data-stu-id="24590-122">DeviceName + DeviceType is unique</span></span></p></td>
<td><p><span data-ttu-id="24590-123">设备类型。</span><span class="sxs-lookup"><span data-stu-id="24590-123">Device type.</span></span> <span data-ttu-id="24590-124">1是捕获设备，0是呈现设备。</span><span class="sxs-lookup"><span data-stu-id="24590-124">1 is a capture device, 0 is a render device.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="24590-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24590-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

