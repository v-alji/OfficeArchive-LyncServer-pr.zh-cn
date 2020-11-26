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
# <a name="dialogs-table-in-lync-server-2013"></a>Lync Server 2013 中的 Dialogs 表

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-28_

对话框表是一个支持表，用于存储有关对等会话的 DialogIDs 的信息。


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
<td><p><strong>SessionIdTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>Primary</p></td>
<td><p>会话请求的时间;与 SessionIDSeq 结合使用以唯一标识会话。</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionIdSeq</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>标识会话的 ID 号。 与 SessionIDTime 结合使用以唯一标识会话。</p></td>
</tr>
<tr class="odd">
<td><p><strong>ExternalChecksum</strong></p></td>
<td><p>int</p></td>
<td><p> </p></td>
<td><p>ExternalID 的校验和。 此字段用于提高数据库搜索的速度。</p></td>
</tr>
<tr class="even">
<td><p><strong>ExternalId</strong></p></td>
<td><p>varbinary (775) </p></td>
<td><p> </p></td>
<td><p>SIP 对话框 ID，存储为二进制。 二进制文件的格式为：</p>
<p>对话框; 从-标签; 到-标记</p>
<p>可以使用以下语法将此数据转换为文本格式：</p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

