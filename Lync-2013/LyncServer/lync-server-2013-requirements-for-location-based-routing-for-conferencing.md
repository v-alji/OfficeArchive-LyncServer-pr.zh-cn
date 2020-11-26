---
title: Lync Server 2013：适用于会议的 Location-Based 路由的要求
description: Lync Server 2013：对会议 Location-Based 路由的要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442661"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a>Lync Server 2013 中的会议 Location-Based 路由要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-07-19_

以下是安装和配置 Location-Based 路由会议应用程序所需的要求：

  - Lync Server 2013 累积更新2必须部署在拓扑中的所有服务器或池上。

<div>


> [!NOTE]  
> 如果拓扑中的 Lync 服务器或池未安装 Lync Server 2013 累积更新2或更高版本，则无法保证 Lync 会议的 Location-Based 路由。



</div>

  - Lync Server 2013 Location-Based 路由是 Location-Based 路由会议应用程序的先决条件。 有关配置 Lync Server 2013 Location-Based 路由的详细信息，请参阅 [配置 Location-Based 路由](lync-server-2013-configuring-location-based-routing.md)。

  - Location-Based 路由会议应用程序的要求与 Lync Server 2013 Location-Based 路由的要求相同。 有关详细信息，请参阅 [规划 Location-Based 路由](lync-server-2013-planning-for-location-based-routing.md)。

<div>

## <a name="supported-servers"></a>支持的服务器

Location-Based 路由会议应用程序要求在拓扑中的所有 Front-End 池和标准版服务器上部署 Lync Server 2013 累积更新2。 如果你的拓扑中的某些 Lync 服务器上未安装 Lync Server 2013 累积更新2，则不能在 Lync 会议和咨询式呼叫传输上完全强制使用 Location-Based 路由限制。

下表列出了支持 Location-Based 路由的服务器角色和版本的组合。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>前端池版本</p></td>
<td><p>中介服务器版本</p></td>
<td><p>支持</p></td>
</tr>
<tr class="even">
<td><p>Lync Server 2013 累积更新 2</p></td>
<td><p>Lync Server 2013 累积更新 2</p></td>
<td><p>是</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2013 累积更新 2</p></td>
<td><p>Lync Server 2013 累积更新 1</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>Lync Server 2013 累积更新 2</p></td>
<td><p>Lync Server 2010</p></td>
<td><p>否</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2013 累积更新 2</p></td>
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>Lync Server 2013 累积更新 1</p></td>
<td><p>任意</p></td>
<td><p>否</p></td>
</tr>
<tr class="odd">
<td><p>Lync Server 2010</p></td>
<td><p>任意</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>Office Communications Server 2007 R2</p></td>
<td><p>任意</p></td>
<td><p>否</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a>支持的客户端

支持 Lync 会议 Location-Based 路由的 Lync 客户端与支持 Lync Server 2013 Location-Based 路由的客户端相同。 有关详细信息，请参阅 [客户端和服务器支持 Location-Based 路由](lync-server-2013-client-and-server-support-for-location-based-routing.md)。

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a>咨询式呼叫转移的中介服务器要求

Location-Based 路由会议应用程序需要部署独立的中介服务器，才能在咨询式呼叫转移上强制执行 Location-Based 路由限制。

若要强制 Location-Based 路由使用咨询式呼叫转移，中介服务器必须仅与需要 Location-Based 路由的网络区域中的一个中介服务器对等 (（如 PBX、SIP 网关等) 相关联）。 如果在同一网络区域中部署其他中介服务器对等，则中介服务器必须与不同的中介服务器相关联。 此要求的详细信息如下：

  - 每台多个中介服务器对等的单中介服务器当通过配置将多个 SIP 中继配置为多个对等 (的中介服务器（即 Pbx 和网关) ），将阻止咨询呼叫转接，阻止通过某些 SIP 中继使用咨询呼叫转接，但禁止通过其他 SIP 中继。
    
    例如，在单个中介服务器处理 PSTN 网关中介服务器对等和 PBX 中介服务器对等的情况下，将看到以下行为：
    
      - 当来自给定网站 (的 Lync 用户（即站点 1) 尝试将具有 PSTN 终结点的呼叫从另一个站点转移到 Lync 用户 (（即 site 2) 通过咨询式转移），将禁止呼叫阻止 PSTN 免绕过。
    
      - 当来自给定网站的 Lync 用户 (（例如，站点 1) 尝试将同一 (站点中的 PBX 终结点与另一个站点中的 PBX 终结点)  (（即 site 2) 通过咨询转移），即使不是在潜在的 PSTN 长途电话中不会产生呼叫，也将禁止呼叫。

  - 每个中介服务器对等单独的中介服务器
    
    当向中介服务器对等进行定向传输时，将根据中介服务器提供服务的单个中介服务器对来评估咨询转移。 无论其他 Mediations 服务器在不同的中介服务器中提供服务，该呼叫都将在 PSTN 免绕过的可能性内被禁止或允许使用。
    
    例如，在单独的中介服务器处理 PSTN 网关中介服务器对等和 PBX 中介服务器对等的情况下，将看到以下行为：
    
      - 当来自给定网站 (的 Lync 用户（即站点 1) 尝试将具有 PSTN 终结点的呼叫从另一个站点转移到 Lync 用户 (（即 site 2) 通过咨询式转移），将禁止呼叫阻止 PSTN 免绕过。
    
      - 当来自给定网站的 Lync 用户 (（例如，站点 1) 尝试将同一 (站点中的 PBX 终结点与另一个站点中的 PBX 终结点)  (（即 site 2) 通过咨询转移）进行传输时，将允许呼叫，因为它不会在潜在的 PSTN 收费中发生。

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a>Location-Based 路由会议应用程序不支持的功能

Location-Based 路由会议应用程序不支持以下功能：

  - 电话拨入式会议。 不能为电话拨入式会议强制使用 Location-Based 路由。 即使会议组织者是为 Location-Based 路由启用的 Lync 用户，Location-Based 路由也不会限制对给定会议的任何拨入请求。

  - 建议在需要实施 Location-Based 路由限制的区域中设置会议访问号码。

</div>

</div>

<span> </span>

</div>

</div>

</div>

