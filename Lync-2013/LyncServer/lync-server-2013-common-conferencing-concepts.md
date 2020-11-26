---
title: Lync Server 2013：常见的会议概念
description: Lync Server 2013：常见的会议概念。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Common conferencing concepts
ms:assetid: a21d4987-1c0a-44c8-8a39-9c17ffb57f3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688158(v=OCS.15)
ms:contentKeyID: 49733762
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2eeea52070c65a8a037eb44e75ceb2d937b91a9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434709"
---
# <a name="common-conferencing-concepts-in-lync-server-2013"></a>Lync Server 2013 中的常见会议概念

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-19_

许多概念是所有类型的会议所共有的。 以下部分将介绍这些内容。

<div>

## <a name="policies-and-bandwidth-management"></a>策略和带宽管理

Lync Server 2013 允许管理员为用户可组织的会议类型设置策略。 这可帮助你强制实施你的组织的策略和控制带宽使用。 你可以定义各种会议策略，并将其分配给单个用户和用户组。 还可以设置管理对等对话的策略。 有关设置会议策略的详细信息，请参阅操作文档中 [Lync Server 2013 中的会议策略](lync-server-2013-conferencing-policies.md) 。 有关带宽管理的详细信息，请参阅 [Lync server 2013 中的 "呼叫许可控制" 概述](lync-server-2013-overview-of-call-admission-control.md) 和 [在 lync Server 2013 中配置视频带宽](lync-server-2013-configuring-video-bandwidth.md)。

</div>

<div>

## <a name="archiving-and-compliance-features"></a>存档和合规性功能

如果您的组织必须遵守合规性法规，则 Lync Server 2013 提供了可使用的功能。 你可以使用存档功能存档会议中显示的内容，还可以使用即时消息 (IM) 对话和 IM 会议的内容。 有关详细信息，请参阅规划文档中的 [在 Lync Server 2013 中规划存档](lync-server-2013-planning-for-archiving.md) 。 你可以使用持久聊天服务器的合规性功能来存档随时间变化的基于主题的多个对话。 有关详细信息，请参阅规划文档中的在 [Lync Server 2013 中规划持久聊天服务器](lync-server-2013-planning-for-persistent-chat-server.md) 。

</div>

<div>

## <a name="monitoring-feature"></a>监视功能

"监视服务器" 功能可捕获 (CDRs) 的呼叫详细记录，您可以使用该记录跟踪与使用 Lync Server 2013 的其他用户交谈的用户。 有关部署和配置监视的详细信息，请参阅 [在 Lync Server 2013 中部署监视](lync-server-2013-deploying-monitoring.md)。

</div>

<div>

## <a name="enabling-external-participation-in-conferences"></a>在会议中启用外部参与

通过使外部用户也可以在受邀的会议中参与会议，您可以在 Lync Server 2013 会议中大大增加投资的优势。 外部用户可能包括：

  - **远程用户**   您的组织的用户在防火墙外部工作时使用其笔记本或其他 Lync Server 2013 设备。

  - **联盟用户**   您与其他人一起工作的公司的用户也运行 Lync Server 2013。 要使用户轻松与这些用户联系，应与这些公司建立联盟关系。

  - **匿名用户**   您的用户专门邀请其加入特定会议的任何其他外部用户。 公司的会议组织者可以向外部用户发送电子邮件以邀请他们参加会议。 该电子邮件包含一个链接，外部用户通过单击该链接即可加入会议。

若要启用任何或所有这些方案，你需要部署边缘服务器以帮助在 Lync Server 2013 部署和外部用户之间实现安全通信。 使用 Edge 服务器的 Lync Server 2013 解决方案比其他解决方案（如虚拟专用网络 (VPN) ）提供更高质量的媒体。 有关详细信息，请参阅 [在 Lync Server 2013 中规划外部用户访问](lync-server-2013-planning-for-external-user-access.md)。

此外，无论是否部署 Edge 服务器，你都可以启用 (的用户（即组织内部或外部的用户）) 从标准 PSTN 电话拨入以加入本地音频会议。 这可通过部署 Lync Server 2013 拨入式会议来完成。

</div>

<div>

## <a name="compatibility-among-meeting-types-and-client-versions"></a>会议类型和客户端版本之间的兼容性

如果您要让 Lync Server 2013 与以前版本的 Office 通信服务器及其客户端互操作，则必须注意以下问题：

  - 使用 Lync Server 2013 的用户无法安排 Live Meeting 会议或修改此类型的任何已迁移的会议。

  - 使用 Lync Server 2013 的用户需要参与运行 Office 通信服务器 2007 R2 的服务器上托管 Live Meeting 会议的用户必须在其计算机上安装 Live meeting 客户端 (除了 Lync Server 2013) 参加这些会议。

  - 当 Live Meeting 会议迁移到 Lync Server 2013 时，会议内容不会迁移。 如果需要此内容，必须重新上传。

</div>

</div>

<span> </span>

</div>

</div>

</div>

