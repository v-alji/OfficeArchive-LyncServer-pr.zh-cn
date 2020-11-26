---
title: Lync Server 2013：证书摘要-公共即时消息连接
description: Lync Server 2013：证书摘要-公共即时消息连接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Public instant messaging connectivity
ms:assetid: 2b3687ee-50c2-4c1c-880e-8dcf8bd4f309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618370(v=OCS.15)
ms:contentKeyID: 49105657
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: abf5a01bdeb03da158e221c623417a1b42cc82f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435290"
---
# <a name="certificate-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a>证书摘要-Lync Server 2013 中的公共即时消息连接

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-19_

若要配置公共即时消息连接的证书，应首先注意到其他 SIP 联合身份验证类型或标准边缘服务器证书没有什么不同，只是北美网络 (AOL) 需要唯一的证书配置。 除了常规服务器增强型密钥使用 (EKU) ，美洲 Online 还需要证书或证书 (边缘池的情况) 也包含客户端 EKU。 客户端 EKU 是证书的补充，并且是分配给 Edge 服务器的外部公共证书的一部分。

<div>

## <a name="certificate-summary--public-instant-messaging-connectivity"></a>证书摘要-公共即时消息连接


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>组件</th>
<th>主题名称</th>
<th> (SAN) /Order 的主题备用名称</th>
<th>备注</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>外部/访问边缘</p></td>
<td><p>sip.contoso.com</p></td>
<td><p>sip.contoso.com</p>
<p>webcon.contoso.com</p>
<p>sip.fabrikam.com</p></td>
<td><p>证书必须来自公共 CA，并且必须具有服务器 EKU 和客户端 EKU，前提是要部署与 AOL 的公共 IM 连接。 证书已分配给以下对象的外部边缘服务器接口：</p>
<ul>
<li><p>访问边缘服务</p></li>
<li><p>Web 会议边缘服务</p></li>
<li><p>A/V 边缘服务</p></li>
</ul>
<p>请注意，San 会根据拓扑生成器中的定义自动添加到证书。 根据需要为其他 SIP 域和其他需要支持的条目添加 SAN 条目。 主题名称是在 SAN 中复制的，并且必须存在才能正确操作。</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>另请参阅


[Lync Server 2013 中的外部用户访问方案](lync-server-2013-scenarios-for-external-user-access.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

