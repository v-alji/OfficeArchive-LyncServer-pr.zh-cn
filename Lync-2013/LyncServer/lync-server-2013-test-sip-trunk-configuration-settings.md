---
title: Lync Server 2013：测试 SIP 中继配置设置
description: Lync Server 2013：测试 SIP 中继配置设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test SIP trunk configuration settings
ms:assetid: c8712308-0e2d-4e39-8f90-d1a250487a94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721880(v=OCS.15)
ms:contentKeyID: 49733814
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d44fe2ef5123bec31fafaff2d811a501e5cca4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444250"
---
# <a name="test-sip-trunk-configuration-settings-in-lync-server-2013"></a>在 Lync Server 2013 中测试 SIP 中继配置设置

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-11-01_

SIP 中继配置设置在服务提供商处定义中介服务器与公共交换电话网络之间的关系和功能 (PSTN) 网关、IP 公共分支 exchange (PBX) 或会话边界控制器 (SBC) 。 这些设置可执行如下所指定内容的操作：

  - 是否在中继上启用媒体旁路功能。

  - 发送 RTCP) 数据包的实时传输控制协议 (的条件。

  -  (SRTP 是否需要安全的实时协议) 加密在每个主干上都是必需的。

安装 Microsoft Lync Server 2013 时，将为你创建一个全局 SIP 中继配置设置集合。 此外，管理员还可以在站点作用域或服务作用域（仅针对 PSTN 网关服务）内创建自定义设置集合。 管理员还可以使用 Test-CsTrunkConfiguration cmdlet 验证中继是否可以将用户拨打的号码转换为网关可处理的号码。

只能使用 Windows PowerShell 和 [Test-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsTrunkConfiguration) cmdlet 测试中继配置设置。 此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。 有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。

<div>

## <a name="to-test-sip-trunk-configuration-settings"></a>测试 SIP 中继配置设置

  - 以下命令可验证 Redmond 站点的中继配置设置是否能正确转换拨号号码 4255551212。
    
        $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
        Test-CsTrunkConfiguration -DialedNumber 4255551212 -TrunkConfiguration $trunk

</div>

</div>

<span> </span>

</div>

</div>

</div>

