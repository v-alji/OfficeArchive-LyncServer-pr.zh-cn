---
title: Lync Server 2013：向即时消息添加自定义文本
description: Lync Server 2013：向即时消息添加自定义文本。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding custom text to instant messages
ms:assetid: cabcc3ec-9d35-42ac-a403-e21b7d538c2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398847(v=OCS.15)
ms:contentKeyID: 48185458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54f5cf031da0ba4d5bd0b6dbaa7f5ebc9d0b3a6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439231"
---
# <a name="adding-custom-text-to-instant-messages-in-lync-server-2013"></a>在 Lync Server 2013 中向即时消息添加自定义文本

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-20_

通过将 **set-csclientpolicy** 或 **Set-csclientpolicy** Lync Server Management Shell cmdlet 与 IMWarning 参数一起使用，在每个 Lync 2013 即时)  (消息的开头添加一个免责声明或警告。

以下示例中的命令在新的 IM 对话开始时在对话窗口的顶部添加安全提醒：

    New-CsClientPolicy -Identity IMSecurityNotice -IMWarning 
    "Remember, security is everyone's responsibility. Keep it confidential."

使用 **Grant-set-csclientpolicy** 将此新策略分配给用户。 有关详细信息，请参阅 Lync Server Management Shell 文档中的 " **新建-set-csclientpolicy** " 和 " **授予" set-csclientpolicy** 。

</div>

<span> </span>

</div>

</div>

</div>

