---
title: 'Lync Server 2013： PurgeSettings table (QoE) '
description: Lync Server 2013： PurgeSettings table (QoE) 。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table (QoE)
ms:assetid: 31b85d1c-3f32-4f67-94bf-9389cdd282c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204788(v=OCS.15)
ms:contentKeyID: 48183777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d515d799a7cc442dc6d34f2ece1a968de51cdad6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392107"
---
# <a name="purgesettings-table-qoe-in-lync-server-2013"></a><span data-ttu-id="ad907-103">PurgeSettings 表 (Lync Server 2013 中的 QoE) </span><span class="sxs-lookup"><span data-stu-id="ad907-103">PurgeSettings table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad907-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad907-104">

<span> </span></span></span>

<span data-ttu-id="ad907-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="ad907-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="ad907-106">PurgeSettings 表包含指定 (和何时) 已过期的体验记录质量的信息是否将自动从 QoE 数据库中删除。</span><span class="sxs-lookup"><span data-stu-id="ad907-106">The PurgeSettings table contains information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span> <span data-ttu-id="ad907-107">请注意，通过运行以下命令，还可以从 Microsoft Lync Server 2013 管理程序外壳中获取清除相关信息：</span><span class="sxs-lookup"><span data-stu-id="ad907-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsQoEConfiguration

<span data-ttu-id="ad907-108">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="ad907-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad907-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="ad907-110"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="ad907-111"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="ad907-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad907-113"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-113"><strong>ID</strong></span></span></p></td>
<td><p><span data-ttu-id="ad907-114">int</span><span class="sxs-lookup"><span data-stu-id="ad907-114">int</span></span></p></td>
<td><p><span data-ttu-id="ad907-115">Primary</span><span class="sxs-lookup"><span data-stu-id="ad907-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="ad907-116">QoE 清除设置集合的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="ad907-116">Unique identifier for the collection of QoE purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad907-117"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-117"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="ad907-118">bit</span><span class="sxs-lookup"><span data-stu-id="ad907-118">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ad907-119">设置为 True 时 (1) Microsoft Lync Server 2013 将定期从 QoE 数据库中清除过时的记录。</span><span class="sxs-lookup"><span data-stu-id="ad907-119">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the QoE database.</span></span> <span data-ttu-id="ad907-120">将在 PurgeHour 设置指定的圣多美中每天进行清除。</span><span class="sxs-lookup"><span data-stu-id="ad907-120">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="ad907-121">如果设置为 False (0) 则将不会从数据库中自动清除记录。</span><span class="sxs-lookup"><span data-stu-id="ad907-121">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="ad907-122">默认值为 True。</span><span class="sxs-lookup"><span data-stu-id="ad907-122">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad907-123"><strong>KeepQoEDataForDays</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-123"><strong>KeepQoEDataForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="ad907-124">int</span><span class="sxs-lookup"><span data-stu-id="ad907-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ad907-125">指定将从数据库中清除 (按天) 的 QoE 记录的存留时间：如果启用清除，将从数据库中删除早于此值的 QoE 记录。</span><span class="sxs-lookup"><span data-stu-id="ad907-125">Specifies the age of QoE records (in days) that will be purged from the database: if purging is enabled, QoE records older than this value will be removed from the database.</span></span> <span data-ttu-id="ad907-126">默认值为60天。</span><span class="sxs-lookup"><span data-stu-id="ad907-126">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad907-127"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="ad907-127"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="ad907-128">int</span><span class="sxs-lookup"><span data-stu-id="ad907-128">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ad907-129">指定每天执行数据库清除的本地时间。</span><span class="sxs-lookup"><span data-stu-id="ad907-129">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="ad907-130">该时间使用 24 小时制格式指定，0 表示午夜（晚上 12:00），23 表示晚上 11:00。</span><span class="sxs-lookup"><span data-stu-id="ad907-130">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="ad907-131">请注意，您只能指定一天中的小时数：值 10 (表示允许 10:00 AM) ，但值 10:30/10.5 (表示不允许 10:30) 。</span><span class="sxs-lookup"><span data-stu-id="ad907-131">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="ad907-132">默认值为 1 (1:00 AM) 。</span><span class="sxs-lookup"><span data-stu-id="ad907-132">The default value is 1 (1:00 AM).</span></span> <span data-ttu-id="ad907-133">指定每天执行数据库清除的本地时间。</span><span class="sxs-lookup"><span data-stu-id="ad907-133">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="ad907-134">该时间使用 24 小时制格式指定，0 表示午夜（晚上 12:00），23 表示晚上 11:00。</span><span class="sxs-lookup"><span data-stu-id="ad907-134">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="ad907-135">请注意，您只能指定一天中的小时数：值 10 (表示允许 10:00 AM) ，但值 10:30/10.5 (表示不允许 10:30) 。</span><span class="sxs-lookup"><span data-stu-id="ad907-135">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="ad907-136">默认值为 1 (1:00 AM) 。</span><span class="sxs-lookup"><span data-stu-id="ad907-136">The default value is 1 (1:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ad907-137">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad907-137">


</div>

<span> </span>

</div>

</div>

</span></span></div>

