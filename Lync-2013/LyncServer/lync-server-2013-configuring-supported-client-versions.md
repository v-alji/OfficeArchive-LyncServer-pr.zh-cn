---
title: Lync Server 2013：配置支持的客户端版本
description: Lync Server 2013：配置支持的客户端版本。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring supported client versions
ms:assetid: aebf7b48-9aa2-4a06-adc5-0c9d11b6358d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412832(v=OCS.15)
ms:contentKeyID: 48185137
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74396314cae864fae134531b71375c750be8d3da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432595"
---
# <a name="configuring-supported-client-versions-in-lync-server-2013"></a>在 Lync Server 2013 中配置支持的客户端版本

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-12-14_

在 Lync Server 2013 中，你可以设置客户端版本策略来指定你的环境支持的客户端版本。 此外，你可以使用全局客户端版本配置为尚未定义版本策略的客户端指定默认操作，因此不会明确支持或限制这些客户端。

你还可以使用客户端版本策略管理客户端更新。 当设置客户端版本策略并使用 " **允许和升级** " 和 " **阻止和升级**" 选项时，如果您使用的是此服务) 或 "Microsoft Update"，则客户端将从 Windows Server 更新服务 (收到更新的软件。

<div>

## <a name="client-version-policy-settings"></a>客户端版本策略设置

默认客户端版本策略要求所有客户端都运行 Lync。 如果你的环境中的客户运行的是早期版本的 Communicator，则你可能需要重新配置客户端版本规则，以防止在连接到 Lync Server 2013 时意外阻止或更新客户端设备。 你可以修改默认规则，也可以在客户端版本策略列表中添加更高的规则，以替代默认规则。 此外，当释放 (CUs) 的累积更新时，应将客户端版本策略配置为需要最新的更新。 有关详细信息，请参阅在操作文档中 [指定可用于登录 Lync Server 2013 的客户端应用程序](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md) 。

</div>

</div>

<span> </span>

</div>

</div>

</div>

