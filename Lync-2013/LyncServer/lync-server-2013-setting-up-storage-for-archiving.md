---
title: Lync Server 2013：设置用于存档的存储
description: Lync Server 2013：设置用于存档的存储。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up storage for Archiving
ms:assetid: f751245c-743e-454f-8325-968ae5e3de71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205392(v=OCS.15)
ms:contentKeyID: 48185858
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7ee431b17b31c49ace7fae1f90d79ec6de2ada4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391813"
---
# <a name="setting-up-storage-for-archiving-in-lync-server-2013"></a>在 Lync Server 2013 中设置用于存档的存储

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-12-17_

Lync Server 2013 的存档存储包括以下内容：

  - **数据存储**   存储 IM 内容需要数据存储。

  - **文件存储**   需要文件存储才能存储会议 (会议) 内容数据存储和文件存储。

<div>

## <a name="setting-up-data-storage"></a>设置数据存储

在 Lync Server 2013 中设置用于存档的数据存储的要求取决于您希望存储存档数据的方式：

  - 将 Lync Server 2013 存档与 Exchange 部署集成，以使用 Exchange 存储存储存档数据。

  - 设置单独的 SQL Server 数据库服务器以存储存档数据。

<div>

## <a name="setting-up-exchange-storage-for-archiving-data"></a>设置用于存档数据的 Exchange 存储

设置用于存储存档数据的 Exchange 需要 Exchange 部署运行 Exchange 2013。 此外，用户邮箱必须托管在 Exchange 2013 服务器上，并且其邮箱必须置于 In-Place 保留状态。 有关配置 Exchange 2013 的详细信息，请参阅 Exchange 产品文档。

</div>

<div>

## <a name="setting-up-sql-server-database-servers-for-storage-of-archiving-data"></a>设置用于存储存档数据的 SQL Server 数据库服务器

Lync Server 2013 中的存档需要 SQL Server 数据库软件存储已存档的数据，除非你将部署与 Exchange 集成。

对于 SQL Server 存档数据库，必须在将托管存档数据库的计算机上安装 SQL Server。 你可以使用用于前端池的后端数据库的相同 SQL 实例。 为了获得最佳性能，你应该在独立于中央管理存储的计算机上部署存档数据库。 有关 collocating Lync Server 2013 组件的详细信息，请参阅支持文档中的 [Lync server 2013 中的 "支持的服务器 collocation](lync-server-2013-supported-server-collocation.md) "。

每个数据库服务器都必须运行受支持的 SQL Server 版本。 有关受支持的版本的详细信息，请参阅规划文档中 [Lync Server 2013 中存档的技术要求](lync-server-2013-technical-requirements-for-archiving.md) 。

在部署和启用存档之前，必须设置 SQL Server 平台。 如果用于发布拓扑的帐户具有适当的管理员权限，则可在发布拓扑时创建存档数据库 (LcsLog)。 你还可以稍后创建数据库，包括安装过程的一部分。 有关 SQL Server 的详细信息，请参阅 SQL Server 技术中心 [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) 。

<div>


> [!NOTE]  
> 确保 SQL Server 代理服务启动类型为 "自动"，并且 SQL Server 代理服务正在为持有存档数据库的 SQL 实例运行，因此默认的存档 SQL Server 维护作业可以按其计划在 SQL Server 代理服务的控制下运行。



</div>

</div>

</div>

<div>

## <a name="setting-up-file-storage"></a>设置文件存储

存档使用您在设置前端池或标准版服务器时指定的 Lync Server 2013 文件共享。 您不能更改用于存档的文件共享。 有关受支持的文件存储系统的详细信息，请参阅支持文档中的 [Lync Server 2013 中的文件存储支持](lync-server-2013-file-storage-support.md) 。

</div>

</div>

<span> </span>

</div>

</div>

</div>

