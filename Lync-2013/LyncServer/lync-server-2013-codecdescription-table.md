---
title: Lync Server 2013： CodecDescription 表
description: Lync Server 2013： CodecDescription 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CodecDescription table
ms:assetid: 3598acb8-7ea6-4748-8417-149c971c32a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204797(v=OCS.15)
ms:contentKeyID: 48183802
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b96ce75ee5ea4d1093314aa9e9543dd155a5eace
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434716"
---
# <a name="codecdescription-table-in-lync-server-2013"></a>Lync Server 2013 中的 CodecDescription 表

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-17_

CodecDescription 表将唯一的编解码器标识符映射到相应的编解码器。 编解码器用于为传输和广播编码数字信号，然后解码这些信号以进行播放。 此表是在 Microsoft Lync Server 2013 中引入的


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
<td><p><strong>CodecDescriptionKey</strong></p></td>
<td><p>smallint</p></td>
<td><p>Primary</p></td>
<td><p>分配给编解码器的唯一标识符。</p></td>
</tr>
<tr class="even">
<td><p><strong>CodecDescription</strong></p></td>
<td><p>varchar (256) </p></td>
<td><p>唯一</p></td>
<td><p>与 CodecDescriptionKey 对应的编解码器的唯一说明。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

