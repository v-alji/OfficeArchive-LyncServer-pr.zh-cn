---
title: Lync Server 2013： Location-Based 路由和咨询式呼叫转移
description: Lync Server 2013： Location-Based 路由和咨询式呼叫传输。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426552"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a>Lync Server 2013 中的 Location-Based 路由和咨询式呼叫转移

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-07-31_

除了强制 Location-Based 路由到 Lync 会议之外，Location-Based 路由会议应用程序在向 PSTN 终结点传出的咨询式呼叫传输上强制 Location-Based 路由限制。 咨询式呼叫转移是在双方将呼叫转移到新用户之间建立的呼叫。 例如，PSTN 终结点调用 (Lync 被呼叫方) 的用户。 用户 A 确定应将 PSTN 用户转发给用户 B (Lync 用户) 。 用户 A 将呼叫与 PSTN 用户保持通话状态，然后呼叫用户 B。用户 B 同意与 PSTN 用户交谈。 用户 A 将呼叫转接至用户 B。

**咨询呼叫转接呼叫流**

![会议的基于位置的路由图示](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "会议的基于位置的路由图示")

当启用 Location-Based 路由的用户启动 PSTN 终结点的咨询式呼叫转移时 (如前面的图所示) 所示，这将创建两个活动呼叫、PSTN 用户 A 和 Lync 用户 A 之间的一个通话以及 Lync 用户 A 和 Lync 用户 B 之间的另一个通话。以下行为由 Location-Based 路由会议应用程序强制执行：

  - 如果您有权将 pstn 呼叫路由到 PSTN 呼叫以将 PSTN 呼叫重新路由到网络站点（Lync 用户 B (即 "转移目标) "，则将允许呼叫转移;否则，将阻止咨询呼叫转接。 此授权的依据是转接方的位置与负责将活动呼叫路由到 PSTN 终结点的 SIP 中继位于相同网络站点。

  - 如果 SIP 中继路由入站 PSTN 呼叫没有授权将呼叫路由到 (Lync 用户 B) 的已传送方或已转移的当事方位于未知的网络站点，则向 PSTN 终结点进行咨询性呼叫转移 (例如将阻止呼叫转移目标) 。

下表介绍了 Location-Based 路由会议应用程序如何为咨询式呼叫传送应用 Location-Based 路由限制。 尽管 PBX 终结点并非直接与某个网络站点关联，但可以为 PBX 连接到的 SIP 中继分配一个网络站点。 因此，PBX 终结点可以间接与网络站点关联。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>呼叫被转接方的网络站点</p></td>
<td><p>呼叫转接目标的网络站点</p></td>
<td><p>行为</p></td>
</tr>
<tr class="even">
<td><p>PSTN 终结点</p></td>
<td><p>同一网络网站中的 Lync 用户 (亦即站点 1) </p></td>
<td><p>咨询转接将被允许</p></td>
</tr>
<tr class="odd">
<td><p>PSTN 终结点</p></td>
<td><p>不同网络站点中的 Lync 用户 (亦即站点 2) </p></td>
<td><p>咨询转接将被禁止</p></td>
</tr>
<tr class="even">
<td><p>PSTN 终结点</p></td>
<td><p>未知网络网站中的 Lync 用户</p></td>
<td><p>咨询转接将被禁止</p></td>
</tr>
<tr class="odd">
<td><p>PSTN 终结点</p></td>
<td><p>联合 Lync 用户</p></td>
<td><p>咨询转接将被禁止</p></td>
</tr>
<tr class="even">
<td><p>PSTN 终结点</p></td>
<td><p>PBX 终结点位于相同站点（即站点 1）</p></td>
<td><p>咨询转接将被允许</p></td>
</tr>
<tr class="odd">
<td><p>PSTN 终结点</p></td>
<td><p>PBX 终结点位于不同站点（即站点 2）</p></td>
<td><p>咨询转接将被禁止</p></td>
</tr>
<tr class="even">
<td><p>PBX 终结点位于相同站点（即站点 1）</p></td>
<td><p>PSTN 终结点</p></td>
<td><p>咨询转接将被允许</p></td>
</tr>
<tr class="odd">
<td><p>PBX 终结点位于不同站点（即站点 2）</p></td>
<td><p>PSTN 终结点</p></td>
<td><p>咨询转接将被禁止</p></td>
</tr>
<tr class="even">
<td><p>PBX 终结点位于任意站点</p></td>
<td><p>同一网络网站中的 Lync 用户 (亦即站点 1) </p></td>
<td><p>咨询转接将被允许</p></td>
</tr>
<tr class="odd">
<td><p>PBX 终结点位于任意站点</p></td>
<td><p>不同网络站点中的 Lync 用户 (亦即站点 2) </p></td>
<td><p>咨询转接将被允许</p></td>
</tr>
<tr class="even">
<td><p>PBX 终结点位于任意站点</p></td>
<td><p>未知网络网站中的 Lync 用户</p></td>
<td><p>咨询转接将被允许</p></td>
</tr>
<tr class="odd">
<td><p>PBX 终结点位于任意站点</p></td>
<td><p>联合 Lync 用户</p></td>
<td><p>咨询转接将被允许</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

