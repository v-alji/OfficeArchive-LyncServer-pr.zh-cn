---
title: Lync Server 2013：前端池的 DNS 要求
description: Lync Server 2013：前端池的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429068"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a>Lync Server 2013 中前端池的 DNS 要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间** ：2012-11-07_

本部分介绍部署前端池 (DNS) 域名系统记录。

<div>

## <a name="dns-records-for-front-end-pools"></a>前端池的 DNS 记录

下表指定 Lync Server 2013 前端池部署的 DNS 要求。

### <a name="dns-requirements-for-a-front-end-pool"></a>前端池的 DNS 要求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>部署方案</th>
<th>DNS 要求</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>具有多个前端服务器和硬件负载均衡器 (不管是否在该池上部署了 DNS 负载均衡) </p></td>
<td><p>同时使用 DNS 负载均衡和硬件负载均衡器时，需要将 A (托管) 记录。 创建内部 A 记录，用于解析前端池的 FQDN (完全限定) DNS 负载均衡。 创建内部主机 (为) Web 服务创建到负载均衡器虚拟 IP (VIP) 记录。 必须使用拓扑生成器中定义的内部 Web 服务名称。</p>
<p>例如，如果同时使用 DNS 负载均衡和硬件负载均衡，则池中每个前端服务器的 A 记录用于 DNS 负载均衡，内部 Web 服务的 A 记录指向硬件负载均衡器虚拟 IP：</p>
<ul>
<li><p>DNS 负载均衡：Pool01.contoso.net 10.10.10.5 的 IP 地址</p>
<div>

> [!WARNING]  
> 每个前端服务器还将有一个不同的 A 记录：


</div>
<ol>
<li><p>FE01.contoso.net 10.10.10.1</p></li>
<li><p>FE02.contoso.net 10.10.10.2</p></li>
<li><p>FE03.contoso.net 10.10.10.3</p></li>
<li><p>FE04.contoso.net 10.10.10.4</p></li>
</ol></li>
<li><p>硬件负载均衡：WebInternal.contoso.net HLB VIP 192.168.10.5 的 IP 地址</p></li>
</ul>
<p>HTTP/HTTPS 流量之外的所有流量都将使用 Pool01.contoso.net 记录。 HTTP/HTTPS 流量将使用定义的内部 Web 服务地址 192.168.10.5</p></td>
</tr>
<tr class="even">
<td><p>部署了 DNS 负载均衡的前端池</p></td>
<td><p>一组内部 A 记录，用于将池的 FQDN 解析为池中每个服务器的 IP 地址。 池中每个服务器必须有一条 A 记录。</p></td>
</tr>
<tr class="odd">
<td><p>部署了 DNS 负载均衡的前端池</p></td>
<td><p>一组内部 A 记录，用于将池中每个服务器的 FQDN 解析为该服务器的 IP 地址。 有关详细信息，请参阅规划 <a href="lync-server-2013-dns-load-balancing.md">文档中的 Lync Server 2013</a> 中的 DNS 负载均衡。</p></td>
</tr>
<tr class="even">
<td><p>具有单个前端服务器和专用后端数据库但没有负载均衡器前端池</p></td>
<td><p>内部 A 记录，用于将前端池的 FQDN 解析为单个企业版前端服务器的 IP 地址。</p></td>
</tr>
<tr class="odd">
<td><p>自动客户端登录</p></td>
<td><p>对于每个支持的 SIP 域，_sipinternaltls._tcp 的 SRV 记录。 &lt;通过端口 5061 的域映射到前端池的 FQDN，该前端池对客户端登录请求进行身份验证和 &gt; 重定向。 有关详细信息，请参阅 <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013</a>中客户端自动登录的 DNS 要求。</p></td>
</tr>
<tr class="even">
<td><p>通过统一通信通过统一通信发现 (UC) 设备</p></td>
<td><p>名称为 ucupdates-r2 的内部 A 记录。 &lt;SIP 域，解析为托管设备更新 Web 服务的前端池的 &gt; IP 地址。 如果 UC 设备已打开，但用户从未登录到该设备，则 A 记录允许设备发现托管设备更新 Web 服务的前端池并获取更新。 否则，设备在用户首次登录时通过带内预配获取此信息。</p>
<div>

> [!IMPORTANT]  
> 如果您在 Lync Server 2010 中已部署设备更新 Web 服务，则已创建名称为 ucupdates 的内部 A 记录。 &lt;SIP 域 &gt; 。 对于 Microsoft Office Communications Server 2007 R2，必须创建一个名称为 ucupdates-r2 的其他 DNS A 记录。 &lt;SIP 域 &gt; 。


</div></td>
</tr>
<tr class="odd">
<td><p>支持 HTTP 流量的反向代理</p></td>
<td><p>外部 A 记录，用于将外部 Web 场 FQDN 解析为反向代理的外部 IP 地址。 客户端和 UC 设备使用此记录连接到反向代理。 有关详细信息，请参阅规划文档中的确定 <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013</a> 的 DNS 要求。</p></td>
</tr>
</tbody>
</table>


下表显示了内部 Web 场 FQDN 所需的 DNS 记录示例。

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a>内部 Web 场 FQDN 的示例 DNS 记录

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>内部 Web 场 FQDN</th>
<th>池 FQDN</th>
<th>DNS A 记录 () </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>webcon.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>DNS A 记录 ee-pool.contoso.com 前端服务器使用的负载均衡器 VIP 地址。</p>
<p>DNS A 记录 webcon.contoso.com 前端服务器使用的负载均衡器 VIP 地址。</p></td>
</tr>
<tr class="even">
<td><p>ee-pool.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>DNS A 记录 ee-pool.contoso.com，解析为前端池中企业版前端服务器使用的负载均衡器 (VIP) 地址。</p>
<p>请注意，如果在此池上使用 DNS 负载均衡，则前端池和内部 Web 场不能具有相同的 FQDN。</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

