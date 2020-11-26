---
title: Lync Server 2013：配置持久聊天服务器
description: Lync Server 2013：配置持久聊天服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Persistent Chat Server
ms:assetid: 85028aff-a38e-4748-958e-59e707a47532
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205054(v=OCS.15)
ms:contentKeyID: 48184709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d45320e1fa6b247f13cfffa9945b45390f2ae6c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433813"
---
# <a name="configure-persistent-chat-server-in-lync-server-2013"></a>在 Lync Server 2013 中配置持久聊天服务器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-06_

创建新的持久聊天配置

    New-CsPersistentChatConfiguration -Identity <XdsIdentity> [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject>] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

获取持久聊天配置

    Get-CsPersistentChatConfiguration [-LocalStore <Switch Parameter>] [-Identity <XdsIdentity>]

删除持久聊天配置

    Remove-CsPersistentChatConfiguration -Identity <XdsIdentity>

设置持久聊天配置

    Set-CsPersistentChatConfiguration [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject >] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

对于 Lync Server 2013，所有 web 服务流量均受 Lync Server 2013 的前端服务器支持。 因此，不需要持久聊天服务器上的 gcweb01 地址。 我们仍然支持内部 web 服务访问，因为我们仅向 *内部* 网站提供文件上载/下载 web 服务 (不会向) 的远程用户提供 *外部* 网站。

</div>

<span> </span>

</div>

</div>

</div>

