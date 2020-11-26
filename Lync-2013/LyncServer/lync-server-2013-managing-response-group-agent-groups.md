---
title: Lync Server 2013：管理响应组代理组
description: Lync Server 2013：管理响应组代理组。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Response Group agent groups
ms:assetid: 36084cdc-38f1-4c45-922f-f81c7e86210c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520976(v=OCS.15)
ms:contentKeyID: 48183806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23a4f430981689f9794c05aa1472ff61cd32cd5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437264"
---
# <a name="managing-response-group-agent-groups-in-lync-server-2013"></a>在 Lync Server 2013 中管理响应组代理组

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-01_

代理组由一组用户组成，这些人被指定为向响应组接听呼叫。 创建代理组时，请选择分配给该组的代理并指定其他组设置，例如路由方法以及代理是否可以登录和注销组。

<div>


> [!NOTE]  
> 必须先为用户启用企业语音才能将其添加到代理组。 有关如何为用户启用企业语音的详细信息，请参阅 <A href="lync-server-2013-enable-users-for-enterprise-voice.md">在 Lync Server 2013 中启用企业语音用户</A>。



</div>

<div>


> [!NOTE]  
> 仅本地用户可成为代理。 如果代理从本地移动到联机，则响应组调用将不会路由到该代理。



</div>

必须登录和注销组的代理（不同于登录或注销 Lync 服务器的代理）称为 *正式代理*。 正式代理必须先登录到组，然后才能接收路由到该组的呼叫。 这对于以兼职形式应答组中的呼叫的代理很有用。 正式代理通过单击 Lync 2013 中的菜单项来登录和注销其组，以打开 Windows Internet Explorer Internet 浏览器并显示网页控制台。

不登录到组或从组注销的代理称为 *非正式代理*。 非正式代理在登录 Lync Server 时自动登录到该组，并且不能注销该组。

<div>


> [!IMPORTANT]  
> 如果将用户分配为响应组代理，需告知用户，如果用户已启用隐私模式，则需搜索“RGS Presence Watcher”联系人并将其添加到联系人列表。已启用隐私模式但未将“RGS Presence Watcher”添加到联系人列表中的代理将无法接收拨打到响应组的呼叫。未启用隐私模式的代理不受影响。



</div>

<div>

## <a name="in-this-section"></a>本节内容

  - [在 Lync Server 2013 中创建或修改代理组](lync-server-2013-create-or-modify-an-agent-group.md)

  - [在 Lync Server 2013 中删除代理组](lync-server-2013-delete-an-agent-group.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

