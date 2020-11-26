---
title: 从 Lync Server 2010 群聊或 Office Communications Server 2007 R2 群聊迁移到 Lync Server 2013 持久聊天服务器
description: 从 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013、持久聊天服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446855"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a>从 Lync Server 2010 群聊或 Office Communications Server 2007 R2 群聊迁移到 Lync Server 2013 持久聊天服务器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-06_

本部分中的主题将指导你完成将 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013、持久聊天服务器的过程。 如果你打算使用 Lync server 2013、持久聊天服务器部署与 Lync Server 2010 共存，群组聊天或 Office 通信服务器 2007 R2 组聊天部署，本指南还包括一些必要的信息，可用于在此混合环境中操作。 本指南主要侧重于持久聊天服务器的数据迁移。 对于从旧版 Lync Server 迁移到 Lync Server 2013 的用户，请参阅 [从 Lync server 2010 迁移到 Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) 和 [从 Office 通信服务器 2007 R2 迁移到 lync server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md)。

<div>


> [!IMPORTANT]  
> 本主题假定你已在与 Lync Server 2010 或 Office 通信服务器 2007 R2 共存的情况下安装了 Lync Server 2013。



</div>

<div>


> [!IMPORTANT]  
> 本指南介绍了完成迁移的每个阶段通常需要执行的步骤。 它不能解决每个可能的旧部署拓扑或每种可能的迁移方案。 因此，你可能不需要执行所述的每个步骤，或者你可能需要执行其他步骤，具体取决于你的部署。 本指南还提供了验证步骤的示例。 提供这些验证步骤旨在帮助你了解需要查找的内容，以确保在你完成迁移过程中每个阶段成功完成。 你可以将这些验证步骤修改为你的特定迁移过程。



</div>

本指南提供有关升级现有部署的特定信息。 它不介绍如何更改现有拓扑。 本指南不介绍新功能的实现。 当详细过程记录在其他位置时，本指南将指导你使用相应的文档或文档部分。

此文档定义了下表中指定的术语。

  - *移植*  
    将部署从以前版本的持久聊天服务器（以前称为组聊天服务器）移动到 Lync Server 2013 持久聊天服务器。

<!-- end list -->

  - *升级*  
    在服务器或客户端计算机上安装较新版本的软件。

<!-- end list -->

  - *既*  
    在迁移过程中，当某些功能已迁移到 Lync Server 2013、持久聊天服务器以及其他功能的临时环境仍然保留在早期版本的组聊天服务器上时。

持久聊天服务器是 Lync Server 2013 基础结构的扩展。 根据你的拓扑，你可以将 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013 持久聊天服务器。 有关可用拓扑和迁移群组聊天服务器的技术和软件要求的详细信息，请参阅规划文档中的在 [Lync server 2013 中规划持久聊天服务器](lync-server-2013-planning-for-persistent-chat-server.md) 。

如果您的组织要求合规性支持，则它现在会自动随每个持久聊天服务器一起安装。 不再需要一个单独的服务器来实现合规性。

<div>


> [!IMPORTANT]  
> 持久聊天服务器必须安装在 NTFS 文件系统上才能帮助强制实施文件系统安全。 FAT32 不是持久聊天服务器支持的文件系统。<BR>如果您的组织要求合规性支持，则它现在会自动随每个持久聊天服务器一起安装。 不再需要一个单独的服务器来实现合规性。 有关 Lync Server 2013 持久聊天服务器中的更改的更多详细信息 &nbsp; ，请参阅入门文档中 <A href="lync-server-2013-new-persistent-chat-server-features.md">Lync server 2013 中的新持久聊天服务器功能</A> 。



</div>

<div>

## <a name="in-this-section"></a>本节内容

  - [标准迁移方案 - 高级别](standard-migration-scenario-high-level.md)

  - [迁移过程 - 详细信息](migration-process-details.md)

  - [共存注意事项](coexistence-considerations.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

