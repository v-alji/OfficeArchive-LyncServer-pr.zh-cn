---
title: Lync Server 2013：规划媒体旁路
description: Lync Server 2013：规划媒体绕过。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for media bypass
ms:assetid: 8ac732b6-8538-4d7b-b1a9-2035e419dac2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398703(v=OCS.15)
ms:contentKeyID: 48184768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92a50d9d838b0f13fd6837cbfadee1c48712f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424480"
---
# <a name="planning-for-media-bypass-in-lync-server-2013"></a>在 Lync Server 2013 中规划媒体旁路

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-21_

媒体绕过指信号遍历中介服务器的呼叫可以从媒体路径中删除中介服务器。

媒体旁路功能可通过减少延迟、不必要的转换、可能的数据包丢失和潜在的故障点数来提高语音质量。 可伸缩性得到改进，因为消除绕过通话的媒体处理会减少中介服务器上的负载。 负载的减少使中介服务器控制多个网关的能力有所补充。

如果没有中介服务器的分支站点通过受限制带宽的一个或多个 WAN 链接连接到中心站点，则媒体绕过会允许来自分支站点的客户端的媒体直接流向其本地网关，而无需首先将 WAN 链接流经中央站点的中介服务器。

通过从媒体处理中免除中介服务器，媒体绕过可能还会减少企业语音基础结构所需的中介服务器的数量。

下图显示了具有和没有媒体旁路功能的拓扑中的基本媒体和信号路径。

**具有和没有媒体旁路功能的媒体和信号路径**

![语音 CAC 媒体绕过连接强制实施](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "语音 CAC 媒体绕过连接强制实施")

一般而言，应尽可能启用媒体旁路。

<div>

## <a name="in-this-section"></a>本节内容

  - [Lync Server 2013 中绕过媒体的概述](lync-server-2013-overview-of-media-bypass.md)

  - [Lync Server 2013 中的媒体绕过模式](lync-server-2013-media-bypass-modes.md)

  - [Lync Server 2013 中的媒体绕过和呼叫允许控制](lync-server-2013-media-bypass-and-call-admission-control.md)

  - [Lync Server 2013 中媒体旁路的技术要求](lync-server-2013-technical-requirements-for-media-bypass.md)

</div>

<div>

## <a name="related-sections"></a>相关部分

[在 Lync Server 2013 中部署高级企业语音功能](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

</div>

<div>

## <a name="see-also"></a>另请参阅


[Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md)  


[Lync Server 2013 中的全局媒体绕过选项](lync-server-2013-global-media-bypass-options.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

