---
title: 使用类别管理持久聊天服务器
description: 使用类别管理持久聊天服务器。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Using categories to administer Persistent Chat Server
ms:assetid: dfcb3ad1-da90-467e-b08c-f4e68673b7b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398988(v=OCS.15)
ms:contentKeyID: 48185628
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 181ecba944a042e3598b2964ad233590cf63349e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443160"
---
# <a name="using-categories-to-administer-persistent-chat-server"></a>使用类别管理持久聊天服务器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-10-01_

持久聊天服务器部署可以托管多个并发的持久聊天室。 聊天室可以组织到服务器上的一组类别中。 每个聊天室属于一个类别，并继承该类别的一些设置。 这种组织方式可创建一种非常有用的结构以基于对话的业务目的识别对话，并有助于委托管理和简化控制。

<div>


> [!NOTE]  
> 虽然聊天室的许多管理功能在运行持久聊天的计算机中都可用 (Lync 客户端) 用户、 <STRONG>cspersistentchatadministrator</STRONG> 角色中的持久聊天管理员 (，) 必须使用 Lync Server 控制面板或 Windows PowerShell cmdlet 来创建或管理类别。



</div>

持久聊天管理员使用 Lync Server 控制面板或 Windows PowerShell cmdlet 来创建和管理类别，并为组织中的用户设计对聊天室的访问。

具有管理一个或多个聊天室的持久聊天室管理器可以使用 Lync 客户端启动聊天室管理 Web 应用程序来创建和管理会议室 (或客户可以创建要) 调用的自定义解决方案和工作流。 持久聊天管理员还可以使用 Lync Server 控制面板或 Windows PowerShell cmdlet 来创建和管理会议室。

<div>


> [!NOTE]  
> 持久聊天室的名称不能与永久聊天类别相同。



</div>

除了更改聊天室类别之外，聊天室管理员还可以更改所有聊天室属性。不能限制其执行以下操作：

  - 禁用聊天室

  - 更改聊天室名称

  - 更改聊天室说明

  - 更改聊天室类型（大会堂还是普通）

  - 更改聊天室隐私（开放、关闭还是秘密）

  - 添加或删除成员

  - 添加或删除聊天室管理者

  - 添加或删除加载项

  - 更改邀请之类的设置（根据类别允许的内容）

<div>

## <a name="delegated-administration"></a>委派管理

使用正确的类别，创建和管理持久的聊天室更容易。 持续聊天管理员可以为每个类别定义 **AllowedMembers** 和 **创建者** ，还可以定义将应用于在类别中创建的所有聊天室的默认聊天室设置和行为。 持久聊天管理员使用 Lync Server 控制面板或 Windows PowerShell cmdlet 创建和管理类别。

标识为类别创建者的用户、组织单位 (OU) 和用户组是仅有的被允许在类别中创建聊天室的个人和组。创建类别后，他们可以从类别的 **AllowedMembers** 列表中选择用户、OU 和用户组作为聊天室的管理员和成员来管理和参与聊天室。

在类别中创建的聊天室遵守由类别 (的策略和设置，例如谁可以在会议室的成员身份、谁可以管理聊天室、是否允许进行文件上载、是否发送邀请等) 。

</div>

</div>

<span> </span>

</div>

</div>

</div>

