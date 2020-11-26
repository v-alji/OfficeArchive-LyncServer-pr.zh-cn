---
title: Lync Server 2013：PayloadDescription 表
description: Lync Server 2013： PayloadDescription 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PayloadDescription table
ms:assetid: c49d61c0-305a-4770-a5d2-5d9f05decc6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412971(v=OCS.15)
ms:contentKeyID: 48185353
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90ba6b3b85060601487b5b6d0d8747c5fbfa2a9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445048"
---
# <a name="payloaddescription-table-in-lync-server-2013"></a>Lync Server 2013 中的 PayloadDescription 表

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-02_

PayloadDescription 表是支持表。 每条记录表示一个编解码器，用于音频或视频会话。


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
<td><p><strong>PayloadDescriptionKey</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>标识编解码器的唯一号码。</p></td>
</tr>
<tr class="even">
<td><p><strong>PayloadDescription</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>唯一</p></td>
<td><p>编解码器名称。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

