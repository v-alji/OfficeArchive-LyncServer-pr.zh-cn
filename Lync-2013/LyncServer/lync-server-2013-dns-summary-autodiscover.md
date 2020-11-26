---
title: Lync Server 2013： DNS 摘要-自动发现
description: Lync Server 2013： DNS 摘要-自动发现。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Autodiscover
ms:assetid: b336a2ae-0e58-4b74-b606-aedbbd411587
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945644(v=OCS.15)
ms:contentKeyID: 51541504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eef9bd6a2489561145718c7bbf2f710ab0b1f248
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429040"
---
# <a name="dns-summary---autodiscover-in-lync-server-2013"></a>DNS 摘要-Lync Server 2013 中的自动发现

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-13_

自动发现是一种灵活的服务，它将通过 HTTP 或 HTTPS 接受通信。 为此，域名系统 (DNS) ，必须正确配置托管自动发现服务的服务器所使用的证书。 证书要求在 " [证书摘要-Lync Server 2013 中的自动发现](lync-server-2013-certificate-summary-autodiscover.md)" 中介绍。

<div>


> [!IMPORTANT]  
> Lync Server 客户端的 DNS 查找逻辑使用特定的解决方案顺序。 你应始终同时包含 lyncdiscoverinternal。 &lt;域 &gt; 和 lyncdiscover。 &lt;&gt;您的 DNS 中的域。 不包括 lyncdiscoverinternal。 &lt;域 &gt; 记录将导致内部客户端无法连接到预期服务或接收不正确的自动发现响应。



</div>

### <a name="internal-dns-records"></a>内部 DNS 记录

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
<td><p>Lyncdiscoverinternal。 &lt;内部域名&gt;</p></td>
<td><p>如果你有控制器池的内部 Web 服务 FQDN，或者如果你没有 Director，则为你的前端池。</p></td>
</tr>
<tr class="even">
<td><p> (主机（如果 IPv6） AAAA) </p></td>
<td><p>lyncdiscoverinternal。 &lt;内部域名&gt;</p></td>
<td><p>内部 Web 服务 IP 地址 (虚拟 IP (VIP) 地址如果你拥有控制器池的负载平衡器) （如果你有），或者如果你没有 Director，则使用前端池。</p></td>
</tr>
</tbody>
</table>


您需要创建下列外部 DNS 记录之一：

### <a name="external-dns-records"></a>外部 DNS 记录

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
<td><p>lyncdiscover。 &lt;sipdomain&gt;</p></td>
<td><p>如果你有控制器池的外部 Web 服务 FQDN，或者如果你没有 Director，则为你的前端池。</p></td>
</tr>
<tr class="even">
<td><p> (主机（如果 IPv6） AAAA) </p></td>
<td><p>lyncdiscover。 &lt;sipdomain&gt;</p></td>
<td><p>反向代理的外部或公共 IP 地址。</p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> 外部流量通过反向代理。



</div>

<div>


> [!NOTE]  
> 移动设备客户端不支持多个安全套接字层 (来自不同域的 SSL) 证书。 因此，不支持通过 HTTPS 对不同域进行 CNAME 重定向。 例如，不支持通过 HTTPS 重定向到 director.contoso.net 地址的 lyncdiscover.contoso.com 的 DNS CNAME 记录。 在此类拓扑中，移动设备客户端需要对第一个请求使用 HTTP，以便 CNAME 重定向通过 HTTP 进行解析。 随后的请求将使用 HTTPS。 若要支持此方案，你需要使用端口 80 (HTTP) 的 web 发布规则配置反向代理。 有关详细信息，请参阅在 <A href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Lync Server 2013 中配置反向代理</A>中的 "为端口80创建 web 发布规则"。 通过 HTTPS 支持到同一域的 CNAME 重定向。 在这种情况下，目标域的证书覆盖了始发域。



</div>

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中配置反向代理以实现移动功能](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)  


[证书摘要-Lync Server 2013 中的自动发现](lync-server-2013-certificate-summary-autodiscover.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

