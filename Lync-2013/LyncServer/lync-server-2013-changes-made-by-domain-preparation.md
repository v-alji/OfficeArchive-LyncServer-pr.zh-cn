---
title: Lync Server 2013：由域准备进行的更改
description: Lync Server 2013：由域准备进行的更改。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435115"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a>Lync Server 2013 中的域准备进行的更改

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2010-10-18_

下表列出了 (Ace) "域准备" 在域根上创建的访问控制条目。 除非另有说明，否则将继承所有 Ace。

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a>添加到域根的 Ace

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th>棒</th>
<th>RTCUniversal-UserReadOnly</th>
<th>RTCUniversal-ServerReadOnly</th>
<th>RTCUniversal-UserAdmins</th>
<th>RTCHSUniversal-Services</th>
<th>Authenticated-Users</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>未继承 (读取容器) </p></td>
<td><p><strong>是</strong></p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>阅读用户 PropertySet 用户帐户-限制</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="odd">
<td><p>阅读用户 PropertySet Personal-Information</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>阅读用户 PropertySet General-Information</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="odd">
<td><p>阅读用户 PropertySet Public-Information</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>阅读用户 PropertySet RTCUserSearchProperty-Set</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p><strong>是</strong></p></td>
</tr>
<tr class="odd">
<td><p>阅读用户 PropertySet RTCPropertySet</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>编写用户属性 Proxy-Addresses</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="odd">
<td><p>编写用户 PropertySet RTCUserSearchProperty-Set</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>编写用户 PropertySet RTCPropertySet</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
<td><p>否</p></td>
</tr>
<tr class="odd">
<td><p>读取 PropertySet DS-复制-对所有 Active Directory 对象的获取更改</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p>否</p></td>
<td><p><strong>是</strong></p></td>
<td><p>否</p></td>
</tr>
</tbody>
</table>


下表列出了域准备在三个内置容器中创建的 Ace：用户、计算机和域控制器。 除非另有说明，否则将继承所有 Ace。

### <a name="aces-added-to-built-in-containers"></a>添加到内置容器的 Ace

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>棒</th>
<th>RTCUniversal-UserReadOnly</th>
<th>RTCUniversal-ServerReadOnly</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>未继承 (读取容器) </p></td>
<td><p><strong>是</strong></p></td>
<td><p><strong>是</strong></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

