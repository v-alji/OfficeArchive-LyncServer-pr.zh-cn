---
title: Lync Server 2013：强化和保护数据库
description: Lync Server 2013：强化和保护数据库。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting the databases of Lync Server 2013
ms:assetid: 6953e721-3511-4235-b848-51bab093dc89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518330(v=OCS.15)
ms:contentKeyID: 62625490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af1ed8f54384e8ecac3b1e4ce6a4253a10bcc2c6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427759"
---
# <a name="hardening-and-protecting-the-databases-of-lync-server-2013"></a>强化和保护 Lync Server 2013 数据库

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-12-05_

Microsoft Lync Server 2013 还取决于用于存储用户信息、会议状态、存档数据和通话详细记录 (CDRs) 的 SQL Server 数据库。 你可以在 Lync Server 后端数据库上最大限度地提高 Lync Server 2013 数据的可用性，方法是以提高容错和简化故障排除的方式分区应用程序数据。 若要实现这些目标，请按以下方式对应用程序数据进行分区：

  - **使用服务器分区最佳做法**   将你的操作系统、应用程序和程序文件与数据文件分开。

  - **存储事务日志文件和数据库文件**   单独存储这些文件以提高容错能力和优化恢复，并将它们存储在加密的磁盘或卷上。

  - **使用服务器群集**   群集后端服务器以优化 Lync Server 2013 系统可用性。

  - **确保所有数据备份均已加密并正确处理**   丢失、放弃或错放备份媒体会对 Lync Server 2013 部署的数据安全造成重大威胁

在除标准版服务器之外的任何 Lync Server 2013 服务器上，不能远程访问 SQL Server Express 实例 (RTCLOCAL 实例) ，并且不会创建任何本地防火墙例外，除非在标准版服务器上使用 SQL Server Express。 在标准版服务器上，会将后端数据库和中央管理存储 (CMS) 设置为可远程访问。 若要加强 SQL Server 数据库，您可以执行以下操作：

  - 自定义标准版服务器上的 SQL Server Express 防火墙，限制可远程访问数据库的服务器的范围。 默认情况下，任何 IP 地址都可以远程访问数据库。

  - 使用 SQL Server 配置管理器指定 SQL Server 远程访问的协议、IP 地址和端口：
    
      - Lync Server 2013 使用 TCP/IP 协议。 它支持 IP 版本 4 (IPv4) ，但不支持 IP 版本 6 (IPv6) 。
        
        <div>
        

        > [!NOTE]  
        > Lync Server 2013 可以在启用了双 IP 堆栈的网络中运行。

        
        </div>
    
      - Lync Server 2013 支持多个 IP 地址 (多主网络地址卡) 。 你可以指定 SQL Server 仅侦听特定 IP 地址 (单个地址或子网) ，并且仅使用特定的协议。
    
      - Lync Server 2013 支持静态和动态 SQL Server 端口。

  - 在静态 (非默认) 端口上运行 SQL Server，并且不运行 SQL Server Browser (因此它无法向客户端) 报告侦听端口。 这需要在每个 SQL Server 客户端上进行自定义配置，包括前端服务器、监视服务器、存档服务器和管理控制台 (运行 Lync Server Management Shell、Lync Server 控制面板或拓扑生成器) 以及所有其他运行 Lync Server) 数据库的服务器。

<div>


> [!NOTE]  
> 对数据库的访问权限必须限制为受信任的数据库管理员。 恶意数据库管理员可以在数据库中插入或修改数据，以通过 Lync Server 2013 服务器获取权限或从服务获取敏感信息，即使数据库管理员尚未被授予 Lync Server 2013 服务器的直接访问或控制权限。



</div>

有关自定义配置和强化 SQL Server 数据库的详细信息，请参阅 NextHop 博客文章 "将 Lync Server 2010 与自定义 SQL Server 网络配置结合使用" [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008) 。

<div>


> [!NOTE]  
> 你还可以加强操作系统和应用程序服务器，并且可以使用组策略在 Lync Server 部署中实施安全 lockdowns。 有关详细信息，请参阅 <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">强化和保护 Lync Server 2013 的服务器和应用程序</A>。



</div>

</div>

<span> </span>

</div>

</div>

</div>

