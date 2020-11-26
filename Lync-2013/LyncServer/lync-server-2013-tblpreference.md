---
title: Lync Server 2013：tblPreference
description: Lync Server 2013： tblPreference。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPreference
ms:assetid: f94eb128-f782-42ff-a568-ed3529573bc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615052(v=OCS.15)
ms:contentKeyID: 48185913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86e8b81a6af93e9bf1d7673e54492579a1bed08e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441373"
---
# <a name="tblpreference-in-lync-server-2013"></a>Lync Server 2013 中的 tblPreference

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-24_

tblPreference 包含用户的客户端首选项。 这通常由 Lync 2013 之前的客户端使用。

### <a name="columns"></a>多

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>类型</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>prefLabel</p></td>
<td><p>nvarchar (255) ，not null</p></td>
<td><p>带格式的标签，如： &lt; 用户 sip uri &gt; | 用户名。 &lt;首选项集 &gt; 。</p></td>
</tr>
<tr class="even">
<td><p>prefSeqID</p></td>
<td><p>int，not null</p></td>
<td><p>用于进行版本控制)  (每个标签的序列号。</p></td>
</tr>
<tr class="odd">
<td><p>prefContent</p></td>
<td><p>nvarchar (max) </p></td>
<td><p>编码内容。</p></td>
</tr>
<tr class="even">
<td><p>lastModifiedBy</p></td>
<td><p>int，not null</p></td>
<td><p>已更新首选项的主体的 ID。</p></td>
</tr>
</tbody>
</table>


### <a name="key"></a>密钥

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;prefLabel, prefSeqID&gt;</p></td>
<td><p>主键。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

