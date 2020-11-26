---
title: Lync Server 2013：移动性的 DNS 要求
description: Lync Server 2013：移动性的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for mobility
ms:assetid: df6962bc-2a16-440e-a333-022ebd14f957
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690040(v=OCS.15)
ms:contentKeyID: 48185624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2a8377dc7c856bb7250817cb3b8b66ed7789d3b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437803"
---
# <a name="dns-requirements-for-mobility-with-lync-server-2013"></a>具有 Lync Server 2013 的移动性 DNS 要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-11-13_

部署 Lync Server 2013 移动功能时，你可以使用 Microsoft Lync Server 2013 自动发现服务中提供的新 Url，或者你可以使用现有的 Web 服务 Url。 如果您使用现有的 Url，则用户需要在其移动设备设置中手动输入 Url。 此选项通常用于故障排除。 使用新 Url 时，移动客户端可以自动发现 Lync Server 2013 资源。 当你支持自动发现时，你需要将新的域名系统添加 (DNS) 记录。 本部分介绍自动发现所需的 DNS 记录。

若要支持自动发现，你需要为每个 SIP 域创建以下 DNS 记录：

  - 支持从组织的网络中连接的移动用户的内部 DNS 记录

  - 支持从 Internet 连接的移动用户的外部 DNS 记录或公共 DNS 记录

内部自动发现 URL 不应从您的网络外部寻址。 外部自动发现 URL 不应从你的网络中寻址。 但是，如果您无法满足外部 URL 的此要求，则移动客户端功能不应受到影响。

DNS 记录可以是 CNAME 记录，也可以是 (主机) 记录。

**内部 DNS 记录**

您需要创建以下内部 DNS 记录之一：


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>记录类型</th>
<th>主机名或 SRV 定义</th>
<th>解析为</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CNAME</p></td>
<td><p>lyncdiscoverinternal。 &lt;sipdomain&gt;</p></td>
<td><p>内部 Web 服务完全限定的域名 (FQDN) 对于你的 Director 池（如果你有），或者对于你的前端池，如果你没有 Director</p></td>
</tr>
<tr class="even">
<td><p> (主机) </p></td>
<td><p>lyncdiscoverinternal。 &lt;sipdomain&gt;</p></td>
<td><p>内部 Web 服务 IP 地址 (虚拟 IP (VIP) 地址如果你拥有控制器池的负载平衡器) （如果你有），或者如果你没有 Director，则使用前端池</p></td>
</tr>
</tbody>
</table>


**外部 DNS 记录**

您需要创建下列外部 DNS 记录之一：


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>记录类型</th>
<th>主机名</th>
<th>解析为</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CNAME</p></td>
<td><p>lyncdiscover. &lt;sipdomain&gt;</p></td>
<td><p>如果你有控制器池的外部 Web 服务 FQDN，或者如果你没有 Director，则为你的前端池</p></td>
</tr>
<tr class="even">
<td><p> (主机) </p></td>
<td><p>lyncdiscover. &lt;sipdomain&gt;</p></td>
<td><p> (VIP 地址的外部或公共 IP 地址（如果使用反向代理的负载平衡器) ）</p></td>
</tr>
<tr class="odd">
<td><p>SRV</p></td>
<td><p>_sipfederationtls _sipfederationtls._tcp。 &lt;sipdomain&gt;</p>
<p>解析为访问边缘服务的主机 (A 或 AAAA) 记录</p></td>
<td><p>若要支持推送通知服务和 Apple 推送通知服务，请为具有 Microsoft Lync 移动客户端的每个 SIP 域创建一个 SRV 记录。</p>
<div>

> [!IMPORTANT]  
> 此要求仅适用于 Apple 或基于 Microsoft 的移动设备上的 Microsoft Lync 移动客户端。 Android 和 Nokia Symbian 设备不使用推送通知。


</div></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> Lyncdiscover 也称为自动发现，流量通过反向代理。 SRV 记录指向通过访问边缘服务解析的记录。



</div>

</div>

<span> </span>

</div>

</div>

</div>

