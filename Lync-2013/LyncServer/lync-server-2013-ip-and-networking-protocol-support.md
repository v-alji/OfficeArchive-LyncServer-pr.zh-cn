---
title: Lync Server 2013：IP 和网络协议支持
description: Lync Server 2013： IP 和网络协议支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426744"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a>Lync Server 2013 中的 IP 和网络协议支持

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-21_

Lync Server 2013 支持下列 IP 和网络协议：

  - **IP 协议。**   Lync Server 2013 支持服务器网络的 IP 版本 4 (IPv4) 或 IP 版本 6 (IPv6) 。
    
    <div>
    

    > [!NOTE]  
    > Lync Server 2013 可以在启用了双 IP 堆栈的网络中运行。

    
    </div>

  - **SIP 传输协议。**   通常，SIP 可以使用至少三种传输类型：用户数据报协议 (UDP) 、传输控制协议 (TCP) 和传输层安全 (TLS) 。 在默认 SIP 传输配置中，TLS 将通过 TCP 运行。 TLS 在 Lync Server 2013 网络中使用。 在网络边缘，Lync Server 2013 可以通过 TCP 进行互操作。 Lync Server 2013 不支持 SIP 传输 UDP，因为它不符合企业通信安全性、可靠性和可伸缩性的最低标准。 有关详细信息，请参阅 NextHop 博客文章、"到 UDP" 或 "不是 UDP" （这是问题） [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) 。
    
    <div>
    

    > [!NOTE]  
    > 每个博客的内容及其 URL 如有更改，恕不另行通知。

    
    </div>

</div>

<span> </span>

</div>

</div>

</div>

