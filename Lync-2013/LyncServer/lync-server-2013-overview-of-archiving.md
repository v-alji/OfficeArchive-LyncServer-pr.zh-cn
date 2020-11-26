---
title: Lync Server 2013：存档概述
description: Lync Server 2013：存档概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Archiving
ms:assetid: 1e3c2ef1-f561-4f57-8b6a-7d78addc1ed1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204729(v=OCS.15)
ms:contentKeyID: 48183570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 548d82d6731fd28fafbde5816a7a0dc77a1fcc02
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424826"
---
# <a name="overview-of-archiving-in-lync-server-2013"></a>Lync Server 2013 中的存档概述

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-09-30_

Lync Server 2013 中的存档提供了一种存档通过 Lync Server 2013 发送的通信的方式。

你可以在初始 Lync Server 2013 部署中实现存档，也可以将其添加到现有部署。 若要使用 Lync Server 2013 存档数据库 (SQL Server 数据库) 以存储存档数据，请使用拓扑生成器将数据库添加到拓扑，然后再次发布拓扑。 如果你的所有用户都托管在 Exchange 2013 上，并且其邮箱放在 In-Place 保留，则不必更新拓扑，但只需启用 Microsoft Exchange 集成即可将已存档的数据存储在 Exchange 2013 中。

实现存档时，将其配置为指定存档内容。 默认情况下，不会存档任何内容。 使用 Lync Server 2013 控制面板配置和管理存档。 你可以实现内部通信、外部通信或两者的存档。 你可以配置整个组织的存档设置，也可以配置特定网站、特定池和特定用户和用户组的存档设置。 有关确定组织的相应选项的详细信息，请参阅在规划文档中 [定义 Lync Server 2013 中的存档要求](lync-server-2013-defining-your-requirements-for-archiving.md) 。 有关如何实施存档策略和配置的详细信息以及有关哪些信息可以或无法存档的详细信息，请参阅规划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作原理](lync-server-2013-how-archiving-works.md) 。

</div>

<span> </span>

</div>

</div>

</div>

