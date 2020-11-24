---
title: 共存注意事项
description: 共存注意事项。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Coexistence considerations
ms:assetid: 9d1a3c0f-492a-4e37-bc2f-63509e328785
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205131(v=OCS.15)
ms:contentKeyID: 48184990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd1f9525b37bdee3249e0e47352fdea1bc7f012f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392162"
---
# <a name="coexistence-considerations"></a>共存注意事项

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-06_

迁移后，仅存在 Lync Server 2013、持久聊天服务器池，并且您可以停止使用旧部署。

在迁移完成之前以及完全取消当前组聊天服务器部署的配置之前，你可能会遇到以下任何部署：

  - Lync Server 2013 持久聊天服务器池，它必须托管在 Lync Server 2013 池。

  - Lync Server 2010、群组聊天池，它必须驻留在 Lync Server 2010 池中。

  - Office 通信服务器 2007 R2 群组聊天池，它必须驻留在 Office 通信服务器 2007 R2 池中。

这些部署可以并排存在。 但是，一个部署中的类别、会议室和外接程序不与附带的部署中的相同。

使用手动配置时，旧客户端 (组聊天客户端) 可以一次连接到一个池，以便用于 Office 通信服务器 2007 R2、Lync Server 2010、群组聊天或 Lync Server 2013。

Lync 2013 (客户端) 只能与 Lync Server 2013、持久聊天服务器池（而不是旧版群组聊天服务器池）交互。 若要在 Lync 2013 (客户端) 中使用持久聊天，用户必须驻留在 Lync 2013 并由策略启用。

</div>

<span> </span>

</div>

</div>

</div>

