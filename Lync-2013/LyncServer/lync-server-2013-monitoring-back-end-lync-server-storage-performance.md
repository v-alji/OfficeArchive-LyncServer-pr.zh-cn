---
title: Lync Server 2013：监视后端 Lync 服务器存储性能
description: Lync Server 2013：监视后端 Lync 服务器存储性能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391924"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a><span data-ttu-id="061fa-103">监视后端 Lync 服务器2013存储性能</span><span class="sxs-lookup"><span data-stu-id="061fa-103">Monitoring back end Lync Server 2013 storage performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="061fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="061fa-104">

<span> </span></span></span>

<span data-ttu-id="061fa-105">_**主题上次修改时间：** 2014-05-02_</span><span class="sxs-lookup"><span data-stu-id="061fa-105">_**Topic Last Modified:** 2014-05-02_</span></span>

<span data-ttu-id="061fa-106">Lync Server 2013 后端数据库是 Lync Server 2013 部署的非常重要的部分。</span><span class="sxs-lookup"><span data-stu-id="061fa-106">The Lync Server 2013 back-end databases are a very important part of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="061fa-107">我们建议持续监视数据库和相应的事务日志，以帮助确保 Lync Server 2013 后端的性能最优化。</span><span class="sxs-lookup"><span data-stu-id="061fa-107">We recommend constantly monitoring the databases and respective transaction logs to help to make sure that the Lync Server 2013 back end is performing optimally.</span></span>

<span data-ttu-id="061fa-108">下表标识应监视的性能计数器，以了解有关存储性能的信息。</span><span class="sxs-lookup"><span data-stu-id="061fa-108">The following table identifies performance counters that should be monitored to learn information about Storage Performance.</span></span> <span data-ttu-id="061fa-109">当系统处于其正常负载) 时，必须 (首先确定这些计数器的基线值，以了解系统压力下的性能变化。</span><span class="sxs-lookup"><span data-stu-id="061fa-109">The baseline values for these counters must be determined first (when system is at its normal, expected load) to understand the performance changes when system is stressed.</span></span>

### <a name="performance-counters-to-be-monitored"></a><span data-ttu-id="061fa-110">要监视的性能计数器</span><span class="sxs-lookup"><span data-stu-id="061fa-110">Performance counters to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="061fa-111">性能计数器</span><span class="sxs-lookup"><span data-stu-id="061fa-111">Performance Counter</span></span></th>
<th><span data-ttu-id="061fa-112">基准阈值</span><span class="sxs-lookup"><span data-stu-id="061fa-112">Baseline thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="061fa-113">每秒 (RTC) 的事务</span><span class="sxs-lookup"><span data-stu-id="061fa-113">Transactions/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="061fa-114">每秒事务/秒 (rtcdyn) </span><span class="sxs-lookup"><span data-stu-id="061fa-114">Transactions/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="061fa-115">每秒事务数 (tempdb) </span><span class="sxs-lookup"><span data-stu-id="061fa-115">Transactions/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="061fa-116"> (RTC) 的日志刷新/秒</span><span class="sxs-lookup"><span data-stu-id="061fa-116">Log Flushes/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="061fa-117">日志刷新/秒 (rtcdyn) </span><span class="sxs-lookup"><span data-stu-id="061fa-117">Log Flushes/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="061fa-118">日志刷新/秒 (tempdb) </span><span class="sxs-lookup"><span data-stu-id="061fa-118">Log Flushes/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="061fa-119">Disk 传输/sec (读写) RTC db</span><span class="sxs-lookup"><span data-stu-id="061fa-119">Disk Transfers/sec (read+write) - RTC db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="061fa-120">磁盘传输/秒-RTC 日志</span><span class="sxs-lookup"><span data-stu-id="061fa-120">Disk Transfers/sec - RTC log</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="061fa-121">磁盘传输/秒-rtcdyn db</span><span class="sxs-lookup"><span data-stu-id="061fa-121">Disk Transfers/sec - rtcdyn db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="061fa-122">磁盘传输/秒-rtcdyn 日志</span><span class="sxs-lookup"><span data-stu-id="061fa-122">Disk Transfers/sec - rtcdyn log</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="061fa-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="061fa-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

