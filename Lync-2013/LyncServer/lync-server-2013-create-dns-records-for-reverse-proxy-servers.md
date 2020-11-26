---
title: Lync Server 2013：为反向代理服务器创建 DNS 记录
description: Lync Server 2013：为反向代理服务器创建 DNS 记录。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create DNS records for reverse proxy servers
ms:assetid: b3513339-e49b-4665-80f1-b5a1c81a0e2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429719(v=OCS.15)
ms:contentKeyID: 48185181
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef785ebbd7160274b631a2d2b6b1f1dcc866e5fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431944"
---
# <a name="create-dns-records-for-reverse-proxy-servers-in-lync-server-2013"></a>在 Lync Server 2013 中为反向代理服务器创建 DNS 记录

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-03-29_

创建外部 DNS A 记录，指向 Microsoft Internet 安全和加速的公共外部接口 (ISA) Server 2006 SP1、Forefront 威胁管理网关2010服务器或 Internet 信息服务器应用程序请求路由，如在 [Lync Server 2013 中配置用于 edge 支持的 DNS](lync-server-2013-configure-dns-for-edge-support.md)中所述。 你需要针对每个池的外部 Web 服务 Fqdn 的 DNS 记录、Director (或控制器池) 以及每个简单的 URL。

客户端解析到反向代理的最低 DNS 记录，必须创建以下记录：

  - Host (一个) 记录 (s) ，用于为控制器和控制器池定义已发布的外部 web 服务 (例如， **webdirext.contoso.com**) 

  - 主机 () 记录 (s) ，用于定义托管在任何前端池和标准版服务器角色中的外部 web 服务的已发布外部 web 服务 (例如 **webext.contoso.com**) 

  - Host (简单 Url 的) 记录 (例如， **dialin.contoso.com** 和 **meet.contoso.com**) 

  - Host (Lync 发现外部记录的) 记录，还提供指向所有 Web 应用（包括 Lync Web App、计划程序和移动 (例如 **lyncdiscover.contoso.com**) ）的自动发现的指针

  - 主机 (Office Web Apps Server URL 的) 记录 (例如 **officewebapp01.contoso.com**) 

有关详细信息，请参阅 [Lync Server 2013 中的 "DNS 摘要-反向代理](lync-server-2013-dns-summary-reverse-proxy.md)"。

</div>

<span> </span>

</div>

</div>

</div>

