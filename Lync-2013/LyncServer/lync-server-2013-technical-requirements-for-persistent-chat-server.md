---
title: Lync Server 2013：持久聊天服务器的技术要求
description: Lync Server 2013：持久聊天服务器的技术要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Persistent Chat Server
ms:assetid: 692b7d99-1bc9-4c99-a050-2bc2be8688b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398495(v=OCS.15)
ms:contentKeyID: 48184383
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 905563f31de36d41a48aea5fb8db3cfde9cb2434
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444320"
---
# <a name="technical-requirements-for-persistent-chat-server-in-lync-server-2013"></a>Lync Server 2013 中持久聊天服务器的技术要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-01-06_

托管持久聊天服务器的每台计算机都必须具有以下组件的现有 Lync Server 2013 拓扑的访问权限：

  - **Lync Server 2013、前端服务器。** 前端服务器是会话初始协议的基础， (SIP) 路由，这使得在运行持久聊天服务器的计算机与可能的持久聊天功能之间进行通信。 开始部署持久聊天服务器之前，请根据您的组织的需要，验证 Lync Server 2013、标准版或 Lync 服务器前端池和任何其他运行 Lync Server 的内部计算机的部署。

以下部分介绍持久聊天服务器和存储持久聊天数据的数据库的特定要求。

<div>

## <a name="persistent-chat-server-requirements"></a>持久聊天服务器要求

有关部署 Lync Server 和最新版本持久聊天服务器的推荐硬件的详细信息，请参阅支持文档中的 [Lync server 2013 的服务器硬件平台](lync-server-2013-server-hardware-platforms.md) 。

有关适用于 Lync Server 和持久聊天服务器的服务器和工具操作系统支持的详细信息，请参阅支持文档中 [Lync server 2013 中的 "服务器和工具" 操作系统支持](lync-server-2013-server-and-tools-operating-system-support.md) 。

有关部署持久聊天服务器所需的其他软件的详细信息，请参阅下表。

### <a name="persistent-chat-server-software-prerequisites"></a>持久聊天服务器软件先决条件

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>软件</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>消息队列</p></td>
<td><p>如果已部署，则为持久聊天服务器和持久聊天合规性服务使用。</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="persistent-chat-server-database-requirements"></a>持久聊天服务器数据库要求

持久聊天服务器使用持久聊天数据库来存储聊天历史记录、配置和用户预配数据。 或者，它使用持久聊天合规数据库来存储合规性数据。

<div>


> [!IMPORTANT]  
> 持久聊天数据库 (mgc) 和合规性数据库 (mgccomp) 可以位于 SQL Server 的同一实例中，也可以位于不同的 SQL 服务器上。



</div>

为准备数据库平台，务必保证每一台计算机都满足硬件要求，然后安装好必备软件。

持久聊天数据库服务器的服务器平台需要与 Lync Server 后端数据库服务器相同的硬件。 有关详细信息，请参阅支持文档中的 [Lync server 2013 的服务器硬件平台](lync-server-2013-server-hardware-platforms.md) 。

在数据库服务器上，确保安装了以下软件应用程序之一：

  - Microsoft SQL Server 2012。 有关如何安装 Microsoft SQL Server 2012 的详细信息，请参阅 "安装 SQL Server 2012" [https://go.microsoft.com/fwlink/p/?LinkID=248559](https://go.microsoft.com/fwlink/p/?linkid=248559) 。

  - Microsoft SQL Server 2008 R2。 有关如何安装 Microsoft SQL Server 2008 R2 的详细信息，请参阅 "SQL server 安装 (SQL Server 2008 R2") " [https://go.microsoft.com/fwlink/?LinkId=275702](https://go.microsoft.com/fwlink/?linkid=275702) 。

</div>

<div>

## <a name="persistent-chat-server-certificate-requirements"></a>持久聊天服务器证书要求

有关获取证书、创建 SQL Server 数据库和创建文件存储的详细信息，请参阅部署文档中的 " [部署 Lync Server 2013](lync-server-2013-deploying-lync-server.md) "。

</div>

</div>

<span> </span>

</div>

</div>

</div>

