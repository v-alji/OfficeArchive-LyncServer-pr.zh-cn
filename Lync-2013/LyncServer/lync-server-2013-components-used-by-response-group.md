---
title: Lync Server 2013：响应组使用的组件
description: Lync Server 2013：由响应组使用的组件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Response Group
ms:assetid: 2b058785-47ca-43b7-b3de-6928a60dc685
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425768(v=OCS.15)
ms:contentKeyID: 48183693
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a1e916d9e4bf986bf0337a6f1f1dd918ff2772e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434555"
---
# <a name="components-used-by-response-group-in-lync-server-2013"></a>Lync Server 2013 中响应组使用的组件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-11_

部署企业语音时，将自动启用响应组应用程序。 本部分介绍支持响应组应用程序的组件。

<div>

## <a name="response-group-components"></a>响应组组件

以下 Microsoft Lync Server 2013 组件支持响应组应用程序：

  - **应用程序服务**   应用程序服务提供了用于部署、托管和管理统一通信应用程序（如响应组）的平台。 应用程序服务将自动安装在前端池中的每个前端服务器上和每个标准版服务器上。

  - **响应组应用程序**   响应组应用程序是由应用程序服务托管的统一通信应用程序之一。 当你部署响应组时，它会自动包括在内。 响应组应用程序将传入呼叫路由和排队到多个代理组。

  - **语言包**   支持文本到语音转换和语音识别需要语言包。 配置消息（例如欢迎消息以及其他提示、互动语音响应 (IVR) 问题和答案）时，会使用这些语音技术。 默认情况下，当你部署 Lync Server 2013 时，将安装26个受支持的语言包。

  - **音频文件**   音频文件用于邮件和保留音乐。

  - **文件存储**   响应组使用文件存储来存储音频文件。 多个响应组池可以使用相同的文件存储实例。

  - **响应组配置工具**   "响应组配置" 工具是用于创建和配置响应组的基于 web 的工具。 在安装 Web 服务时，将包括 "响应组配置" 工具。

  - **Microsoft Lync Server 2013 控制面板**   可以使用 Lync Server "控制面板" 设置和配置响应组的代理组和队列。

  - **Lync Server 命令行管理**   程序  所有响应组设置均可使用 Lync Server Management Shell cmdlet 进行配置。

  - **Microsoft Lync 2013**   (代理接受组的呼叫之前必须登录到组的正式代理，) 使用 Lync 2013 登录到组并注销。 如果为正式代理配置了代理组，代理将单击 Lync 2013 中的菜单项以打开 Internet Explorer，并显示用于登录和注销组的网页控制台。

  - **Web 服务**   响应组配置工具、代理的登录和注销控制台、Lync Server 控制面板和响应组客户端 web 服务需要 Web 服务。

  - **响应组客户端 Web 服务**   响应组应用程序提供了一个客户端 web 服务，可供第三方应用程序用于检索有关代理、代理组成员身份、代理登录状态、组呼叫状态以及支持匿名呼叫的组的信息。 Lync 2013 和 Lync 2010 助理使用响应组客户端 Web 服务检索代理可用于进行匿名调用的响应组的列表。 在安装 Web 服务时，将包括客户端 web 服务。

</div>

</div>

<span> </span>

</div>

</div>

</div>

