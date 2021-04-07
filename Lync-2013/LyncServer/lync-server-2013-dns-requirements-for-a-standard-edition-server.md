---
title: Lync Server 2013：Standard Edition 服务器的 DNS 要求
description: Lync Server 2013：标准版服务器的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392352"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a>Lync Server 2013 中 Standard Edition 服务器的 DNS 要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间** ：2013-02-22_

本部分介绍域名系统 (DNS) 部署标准版服务器所需的记录。

<div>

## <a name="dns-records-for-standard-edition-servers"></a>标准版服务器的 DNS 记录

下表指定 Lync Server 2013 Standard Edition 服务器部署的 DNS 要求。


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
<td><p>Standard Edition Server</p></td>
<td><p>内部 A 记录，用于将服务器的 FQDN (FQDN) 到其 IP 地址。</p></td>
</tr>
<tr class="even">
<td><p>自动客户端登录</p></td>
<td><p>对于每个支持的 SIP 域，_sipinternaltls._tcp 的 SRV 记录。 &lt;通过端口 5061 的域，该域映射到标准版服务器的 FQDN，该服务器对客户端登录请求进行身份验证和 &gt; 重定向。 有关详细信息，请参阅 <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013</a>中客户端自动登录的 DNS 要求。</p></td>
</tr>
<tr class="odd">
<td><p>通过统一通信通过统一通信发现 (UC) 设备</p></td>
<td><p>名称为 ucupdates-r2 的内部 A 记录。 &lt;SIP 域，解析为托管设备更新 Web &gt; 服务的标准版本服务器的 IP 地址。 如果 UC 设备已打开，但用户从未登录到该设备，则 A 记录允许设备发现托管设备更新 Web 服务的服务器并获取更新。 否则，设备在用户首次登录时通过带内预配获取服务器信息。 有关详细信息，请参阅 <a href="lync-server-2013-device-update-web-service.md">操作文档中的 Lync Server 2013</a> 中的设备更新 Web 服务。</p></td>
</tr>
<tr class="even">
<td><p>支持 HTTP 流量的反向代理</p></td>
<td><p>外部 A 记录，用于将外部 Web 场 FQDN 解析为反向代理的外部 IP 地址。 客户端和 UC 设备使用此记录连接到反向代理。 有关详细信息，请参阅规划文档中的确定 <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013</a> 的 DNS 要求。</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>另请参阅


[Lync Server 2013 中自动客户端登录的 DNS 要求](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[确定 Lync Server 2013 的 DNS 要求](lync-server-2013-determine-dns-requirements.md)  


[Lync Server 2013 中的设备更新 Web 服务](lync-server-2013-device-update-web-service.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

