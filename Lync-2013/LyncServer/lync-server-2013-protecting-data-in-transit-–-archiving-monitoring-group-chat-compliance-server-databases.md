---
title: Lync Server 2013：保护传输途中的数据 – 存档、监控、群聊合规性服务器数据库
description: Lync Server 2013：保护传输中的数据-存档、监视、群组聊天合规性服务器数据库。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436844"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a>保护传输途中的数据 – Lync Server 2013 中的存档、监控、群聊合规性服务器数据库

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-12-05_

Microsoft Lync Server 2013 存档服务器和监视服务器均使用 "消息队列" (也称为 MSMQ) 服务，以收集数据消息并将其从集合点可靠地移动到存储库服务器。 合规性服务与群组聊天服务器一起收集数据，后者也使用消息队列。

在 Lync Server 2013 中，网络上没有数据的内部保护;但是，如果需要保护此通信流的安全，消息队列服务可以在发送消息队列上的邮件级别提供加密。 这是使用由 Active Directory 域服务管理的证书完成的。 有关详细信息，请参阅附录 D： windows server 2008 中的 "附录 D：消息队列和 Internet 通信" [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) 或 "附录 I"： windows server 2008 r2 [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) For windows Server 2008 r2 中的消息队列和 internet 通信。

</div>

<span> </span>

</div>

</div>

</div>

