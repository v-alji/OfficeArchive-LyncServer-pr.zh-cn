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
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a>监视后端 Lync 服务器2013存储性能

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-05-02_

Lync Server 2013 后端数据库是 Lync Server 2013 部署的非常重要的部分。 我们建议持续监视数据库和相应的事务日志，以帮助确保 Lync Server 2013 后端的性能最优化。

下表标识应监视的性能计数器，以了解有关存储性能的信息。 当系统处于其正常负载) 时，必须 (首先确定这些计数器的基线值，以了解系统压力下的性能变化。

### <a name="performance-counters-to-be-monitored"></a>要监视的性能计数器

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>性能计数器</th>
<th>基准阈值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>每秒 (RTC) 的事务</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>每秒事务/秒 (rtcdyn) </p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>每秒事务数 (tempdb) </p></td>
<td></td>
</tr>
<tr class="even">
<td><p> (RTC) 的日志刷新/秒</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>日志刷新/秒 (rtcdyn) </p></td>
<td></td>
</tr>
<tr class="even">
<td><p>日志刷新/秒 (tempdb) </p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Disk 传输/sec (读写) RTC db</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>磁盘传输/秒-RTC 日志</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>磁盘传输/秒-rtcdyn db</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>磁盘传输/秒-rtcdyn 日志</p></td>
<td></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

