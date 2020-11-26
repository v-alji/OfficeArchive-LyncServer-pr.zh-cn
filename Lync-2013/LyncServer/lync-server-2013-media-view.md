---
title: Lync Server 2013：媒体视图
description: Lync Server 2013： "媒体" 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media view
ms:assetid: 1a7b2e59-082e-4188-98ae-48ae9bd3494a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687981(v=OCS.15)
ms:contentKeyID: 49733570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74643986b12a30b1055a46a37febf90eeb70c514
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446035"
---
# <a name="media-view-in-lync-server-2013"></a>Lync Server 2013 中的 "媒体" 视图

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-01_

媒体视图存储对等会话中使用的一种媒体类型的相关信息。 如果使用多个媒体类型，则表中的多个记录将表示一个会话。 此视图已在 Microsoft Lync Server 2013 中引入。

<div>


> [!NOTE]  
> 不应使用 "媒体" 视图计算会话的媒体持续时间。 此视图包含会话中媒体交换的信号详细信息。 媒体交换由邀请请求完成，并且 StartTime 指示发送邀请的时间。邀请时间不一定意味着媒体开始时间，因为媒体仅在接受会话后才开始。



</div>

媒体视图在 [Lync Server 2013 的 SessionDetails 视图](lync-server-2013-sessiondetails-view.md) 中包含所有列，此外还包含下面列出的列。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>数据类型</th>
<th>详细信息</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>媒体</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>媒体类型。 有关详细信息，请参阅 <a href="lync-server-2013-medialist-table.md">Lync Server 2013 中的 MediaList 表</a> 。</p></td>
</tr>
<tr class="even">
<td><p><strong>MediaStartTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>媒体请求发出的时间。</p></td>
</tr>
<tr class="odd">
<td><p><strong>MediaEndTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>会话的结束时间。</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

