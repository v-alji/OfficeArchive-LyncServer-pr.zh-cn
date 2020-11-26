---
title: Lync Server 2013：边缘组件支持的服务器并置
description: Lync Server 2013：支持的适用于 edge 组件的服务器 collocation。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423636"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a>Lync Server 2013 中边缘组件支持的服务器并置

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-08_

访问边缘服务、Web 会议边缘服务、A/V 边缘服务和 XMPP 代理服务在边缘服务器上 collocated。 以下服务器提供外部用户访问所需的函数，并且必须部署为专用服务器：

  - 边缘服务器

  - 导演 (可选) 

  - 反向代理

<div>


> [!IMPORTANT]  
> 反向代理无需专门为 Lync Server 2013 提供服务。 例如，你可以提供用于发布 Lync Server Web 服务的服务，并同时为另一个网站提供已发布的网站，该网站与 Lync 服务器根本没有任何关系。 如果外围网络中已有反向代理服务器支持其他服务，则可以将其用于 Lync Server 2013。



</div>

</div>

<span> </span>

</div>

</div>

</div>

