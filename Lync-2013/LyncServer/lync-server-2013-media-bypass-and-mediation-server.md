---
title: Lync Server 2013：媒体绕过和中介服务器
description: Lync Server 2013：媒体绕过和中介服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass and Mediation Server
ms:assetid: 8ed35f95-05cd-4b5d-8470-442d2323df71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398719(v=OCS.15)
ms:contentKeyID: 48184774
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebb005d3d52fa9e5a38fdf56a65dfcbd73616d87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425701"
---
# <a name="media-bypass-and-mediation-server-in-lync-server-2013"></a>Lync Server 2013 中的媒体绕过和中介服务器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-21_

媒体绕过是一种 Lync 服务器功能，使管理员能够将呼叫路由配置为直接在用户终结点和公共交换电话)  (网络之间直接流动，而无需遍历中介服务器。 媒体旁路通过减少延迟、不必要的转换、数据包丢失的可能性以及潜在的故障点数量来提高通话质量。 在以下情况下，如果没有中介服务器的远程网站通过受限制带宽的一个或多个 WAN 链接连接到中心网站，则媒体绕过会通过从远程网站中的客户端将媒体直接流向其本地网关来降低带宽要求，而无需首先将 WAN 链接流经中央站点的中介服务器。媒体处理的减少还会补充中介服务器控制多个网关的能力。

媒体旁路功能和呼叫允许控制 (CAC) 相互排斥。如果某次呼叫使用媒体旁路功能，则不会为此次呼叫执行 CAC。假定前提是此次呼叫不涉及具有限定带宽的链接。

<div>

## <a name="see-also"></a>另请参阅


[Lync Server 2013 中的呼叫允许控制和中介服务器](lync-server-2013-call-admission-control-and-mediation-server.md)  


[在 Lync Server 2013 中规划媒体旁路](lync-server-2013-planning-for-media-bypass.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

