---
title: Lync Server 2013：tblComplianceParticipant
description: Lync Server 2013： tblComplianceParticipant。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceParticipant
ms:assetid: 5d7e0dea-74f7-46d1-badf-b94abc8f066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558655(v=OCS.15)
ms:contentKeyID: 48184262
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1385b0a635f003a72de93f10f72642314ad7ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444453"
---
# <a name="tblcomplianceparticipant-in-lync-server-2013"></a>Lync Server 2013 中的 tblComplianceParticipant

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-12_

tblComplianceParticipant 包含每个频道和每台服务器的当前参与者。

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
<td><p>channelUri</p></td>
<td><p>nvarchar (255) ，not null</p></td>
<td><p>通道统一资源标识符 (URI) 。</p></td>
</tr>
<tr class="even">
<td><p>userId</p></td>
<td><p>int，not null</p></td>
<td><p>参与者的主体 ID (对应于 tblPrincipal prinID 表) 。</p></td>
</tr>
<tr class="odd">
<td><p>joinedAt</p></td>
<td><p>bigint，not null</p></td>
<td><p>联接事件的时间戳。</p></td>
</tr>
<tr class="even">
<td><p>partedAt</p></td>
<td><p>bigint</p></td>
<td><p>如果参与者仍处于加入，则为 Null。 如果 not null，则通道的时间戳会留下事件。</p>
<p>这些条目最终会在所有翻译人员处理该事件时被删除。</p></td>
</tr>
<tr class="odd">
<td><p>userUri</p></td>
<td><p>nvarchar (255) ，not null</p></td>
<td><p>用户 URI。</p></td>
</tr>
<tr class="even">
<td><p>serverID</p></td>
<td><p>int</p></td>
<td><p>服务器标识 (，tblServerIdentity serverID table) 中所示。</p></td>
</tr>
<tr class="odd">
<td><p>标识符</p></td>
<td><p>bigint</p></td>
<td><p>服务器会话。 这是每次启动聊天服务时生成的随机数字。 它用于为识别孤立参与者的目的而区分会话。</p></td>
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
<td><p>&lt;channelUri、userId、joinedAt&gt;</p></td>
<td><p>主键。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

