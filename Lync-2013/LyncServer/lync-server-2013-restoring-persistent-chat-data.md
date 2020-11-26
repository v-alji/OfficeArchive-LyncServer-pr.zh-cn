---
title: Lync Server 2013：还原持久聊天数据
description: Lync Server 2013：还原持久聊天数据。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442507"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a>在 Lync Server 2013 中还原永久聊天数据

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-18_

持久聊天室内容存储在持久聊天数据库 (mgc) 中。 这是应定期备份的业务关键型数据。 除了聊天室内容之外，主体 (（如用户和组) 以及他们拥有的用于聊天聊天室和聊天室内容的角色和访问）也存储在持久聊天数据库中。

还原持久聊天数据的方式取决于用于备份的方法。

  - 如果您使用 SQL Server 备份过程，则必须使用 SQL Server 还原过程。

  - 如果你使用 **Export CsPersistentChatData** Cmdlet 备份持久聊天数据，则必须使用 **CsPersistentChatData** cmdlet 来还原数据。

</div>

<span> </span>

</div>

</div>

</div>

