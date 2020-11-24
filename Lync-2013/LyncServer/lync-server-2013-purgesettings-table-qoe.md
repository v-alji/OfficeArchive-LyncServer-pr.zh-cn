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
# <a name="purgesettings-table-qoe-in-lync-server-2013"></a>PurgeSettings 表 (Lync Server 2013 中的 QoE) 

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-02_

PurgeSettings 表包含指定 (和何时) 已过期的体验记录质量的信息是否将自动从 QoE 数据库中删除。 请注意，通过运行以下命令，还可以从 Microsoft Lync Server 2013 管理程序外壳中获取清除相关信息：

    Get-CsQoEConfiguration

此表是在 Microsoft Lync Server 2013 中引入的。


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>列</strong></th>
<th><strong>数据类型</strong></th>
<th><strong>键/索引</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ID</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>QoE 清除设置集合的唯一标识符。</p></td>
</tr>
<tr class="even">
<td><p><strong>EnablePurge</strong></p></td>
<td><p>bit</p></td>
<td></td>
<td><p>设置为 True 时 (1) Microsoft Lync Server 2013 将定期从 QoE 数据库中清除过时的记录。 将在 PurgeHour 设置指定的圣多美中每天进行清除。 如果设置为 False (0) 则将不会从数据库中自动清除记录。 默认值为 True。</p></td>
</tr>
<tr class="odd">
<td><p><strong>KeepQoEDataForDays</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>指定将从数据库中清除 (按天) 的 QoE 记录的存留时间：如果启用清除，将从数据库中删除早于此值的 QoE 记录。 默认值为60天。</p></td>
</tr>
<tr class="even">
<td><p><strong>PurgeHour</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>指定每天执行数据库清除的本地时间。 该时间使用 24 小时制格式指定，0 表示午夜（晚上 12:00），23 表示晚上 11:00。 请注意，您只能指定一天中的小时数：值 10 (表示允许 10:00 AM) ，但值 10:30/10.5 (表示不允许 10:30) 。 默认值为 1 (1:00 AM) 。 指定每天执行数据库清除的本地时间。 该时间使用 24 小时制格式指定，0 表示午夜（晚上 12:00），23 表示晚上 11:00。 请注意，您只能指定一天中的小时数：值 10 (表示允许 10:00 AM) ，但值 10:30/10.5 (表示不允许 10:30) 。 默认值为 1 (1:00 AM) 。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

