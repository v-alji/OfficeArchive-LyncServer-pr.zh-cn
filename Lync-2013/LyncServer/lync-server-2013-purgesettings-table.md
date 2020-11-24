---
title: Lync Server 2013： PurgeSettings 表
description: Lync Server 2013： PurgeSettings 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table
ms:assetid: 9ff2c8fc-4ae8-4f22-96a8-1f4d5eecbf2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205121(v=OCS.15)
ms:contentKeyID: 48184932
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec2d1508d8362988bddbab2fe7303a23a8ee2d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392106"
---
# <a name="purgesettings-table-in-lync-server-2013"></a>Lync Server 2013 中的 PurgeSettings 表

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-28_

PurgeSettings 表包含用于指定) 过期呼叫详细记录 (是否将从 CDR 数据库中自动删除的信息。 请注意，通过运行以下命令，还可以从 Microsoft Lync Server 2013 管理程序外壳中获取清除相关信息：

    Get-CsCdrConfiguration

管理员应将 PurgeSettings 表视为只读：仅应使用 [新的-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) 或 [CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet 进行对呼叫详细信息清除设置的更改。

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
<th>列</th>
<th>数据类型</th>
<th>键/索引</th>
<th>详细信息</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>标识号</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>CDR 清除设置集合的唯一标识符。</p></td>
</tr>
<tr class="even">
<td><p><strong>EnablePurge</strong></p></td>
<td><p>bit</p></td>
<td></td>
<td><p>设置为 True 时 (1) Microsoft Lync Server 2013 将定期从 CDR 数据库中清除过时的记录。 将在 PurgeHour 设置指定的圣多美中每天进行清除。 如果设置为 False (0) 则将不会从数据库中自动清除记录。 默认值为 True。</p></td>
</tr>
<tr class="odd">
<td><p><strong>KeepCallDetailForDays</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>指定将从数据库中清除的 CDR 记录的存在时间 (按天) ：如果启用清除，将从数据库中删除早于此值的 CDR 记录。 默认值为60天。</p></td>
</tr>
<tr class="even">
<td><p><strong>KeepErrorReportForDays</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>指定将从数据库中清除的 "错误报告" 记录的年龄 (按天) ：如果启用清除，则早于此值的错误报告记录将从数据库中删除。 默认值为60天。</p></td>
</tr>
<tr class="odd">
<td><p><strong>PurgeHour</strong></p></td>
<td><p>int</p></td>
<td></td>
<td><p>指定每天执行数据库清除的本地时间。 该时间使用 24 小时制格式指定，0 表示午夜（晚上 12:00），23 表示晚上 11:00。 请注意，您只能指定一天中的小时数：值 10 (表示允许 10:00 AM) ，但值 10:30/10.5 (表示不允许 10:30) 。 默认值为 2 (2:00 AM)。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

