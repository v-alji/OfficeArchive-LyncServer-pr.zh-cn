---
title: Lync Server 2013：Devices 表
description: Lync Server 2013： "设备" 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Devices table
ms:assetid: 532e2280-4bbc-4a6c-93da-45d9f80a30a0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398351(v=OCS.15)
ms:contentKeyID: 48184169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763e1788e2874f9f9831c089ffe8fa077621b030
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429337"
---
# <a name="devices-table-in-lync-server-2013"></a><span data-ttu-id="0e36d-103">Lync Server 2013 中的 Devices 表</span><span class="sxs-lookup"><span data-stu-id="0e36d-103">Devices table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e36d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e36d-104">

<span> </span></span></span>

<span data-ttu-id="0e36d-105">_**主题上次修改时间：** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="0e36d-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="0e36d-106">"设备" 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="0e36d-106">The Devices table is a supporting table.</span></span> <span data-ttu-id="0e36d-107">每个记录存储有关一个设备 (桌面电话) 的信息。</span><span class="sxs-lookup"><span data-stu-id="0e36d-107">Each record stores information about one device (desk phone).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e36d-108">列</span><span class="sxs-lookup"><span data-stu-id="0e36d-108">Column</span></span></th>
<th><span data-ttu-id="0e36d-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="0e36d-109">Data Type</span></span></th>
<th><span data-ttu-id="0e36d-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="0e36d-110">Key/Index</span></span></th>
<th><span data-ttu-id="0e36d-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="0e36d-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e36d-112"><strong>Keyroutedeventargs.deviceid</strong></span><span class="sxs-lookup"><span data-stu-id="0e36d-112"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e36d-113">int</span><span class="sxs-lookup"><span data-stu-id="0e36d-113">int</span></span></p></td>
<td><p><span data-ttu-id="0e36d-114">Primary</span><span class="sxs-lookup"><span data-stu-id="0e36d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="0e36d-115">标识此硬件版本的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="0e36d-115">Unique number identifying this hardware version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e36d-116"><strong>ManufacturerId</strong></span><span class="sxs-lookup"><span data-stu-id="0e36d-116"><strong>ManufacturerId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e36d-117">int</span><span class="sxs-lookup"><span data-stu-id="0e36d-117">int</span></span></p></td>
<td><p><span data-ttu-id="0e36d-118">外表</span><span class="sxs-lookup"><span data-stu-id="0e36d-118">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0e36d-119">此设备的制造商。</span><span class="sxs-lookup"><span data-stu-id="0e36d-119">Manufacturer of this device.</span></span> <span data-ttu-id="0e36d-120">有关详细信息，请参阅 <a href="lync-server-2013-manufacturers-table.md">Lync Server 2013 中的制造商表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0e36d-120">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e36d-121"><strong>HardwareVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="0e36d-121"><strong>HardwareVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e36d-122">int</span><span class="sxs-lookup"><span data-stu-id="0e36d-122">int</span></span></p></td>
<td><p><span data-ttu-id="0e36d-123">外表</span><span class="sxs-lookup"><span data-stu-id="0e36d-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0e36d-124">此设备的硬件版本。</span><span class="sxs-lookup"><span data-stu-id="0e36d-124">Hardware version of this device.</span></span> <span data-ttu-id="0e36d-125">有关详细信息，请参阅 <a href="lync-server-2013-hardwareversions-table.md">Lync Server 2013 中的 HardwareVersions 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="0e36d-125">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e36d-126"><strong>MacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="0e36d-126"><strong>MacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="0e36d-127">bigint</span><span class="sxs-lookup"><span data-stu-id="0e36d-127">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0e36d-128">MAC 地址</span><span class="sxs-lookup"><span data-stu-id="0e36d-128">MAC Address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0e36d-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e36d-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

