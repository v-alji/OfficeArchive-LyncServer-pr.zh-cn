---
title: Lync Server 2013：综合事务的特殊设置说明
description: Lync Server 2013：合成事务的特殊设置说明。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Special setup instructions for synthetic transactions
ms:assetid: 694cbe05-5dba-4035-a01c-c87ebfb0478b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688080(v=OCS.15)
ms:contentKeyID: 49733676
ms.date: 11/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e288a9d7f15f4b84df591d152a912509c77129a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441597"
---
# <a name="special-setup-instructions-for-synthetic-transactions-in-lync-server-2013"></a>Lync Server 2013 中的综合事务的特殊设置说明

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2015-11-16_

大多数合成事务可以按原样在观察程序节点上运行;也就是说，一旦将合成事务添加到观察程序节点配置设置，观察程序节点就可以在其测试传递期间开始使用合成事务。 但是，并非所有合成事务都是如此。 异常（需要特殊设置说明的合成事务）将在以下部分中讨论。

<div>

## <a name="dealing-with-server-timeout-errors"></a>处理服务器超时错误

在某些情况下，你可能会发现你的综合事务失败，并出现服务器超时错误 (错误代码 504) 。 这些错误通常由防火墙问题引起。 执行合成事务时，该事务将在 MonitoringHost.exe 进程下运行;MonitoringHost.exe 将启动 PowerShell.exe 进程的一个实例。 如果你的防火墙阻止 MonitoringHost.exe 或 PowerShell.exe，则合成事务将失败，并将生成504错误。

若要解决此问题，应在本地计算机上手动创建 MonitoringHost.exe 和 PowerShell.exe 的入站防火墙规则。 这可以通过 Windows 防火墙或第三方本地防火墙软件完成，具体取决于你的服务器的预先配置。

如果在综合事务主机和要监视的 Lync 服务器之间使用网络防火墙设备，则应将主机视为客户端计算机，并观察来自 [Lync Server 2013 中内部服务器的端口和协议的](lync-server-2013-ports-and-protocols-for-internal-servers.md)所有防火墙端口要求。

</div>

<div>

## <a name="data-conferencing-synthetic-transactions"></a>数据会议综合事务

如果你的观察程序节点计算机位于你的外围网络之外，则你可能无法运行数据会议合成事务，除非你首先禁用网络服务帐户的 Internet Explorer 代理设置。 若要禁用此服务的代理设置，请完成以下过程：

1.  在观察程序节点计算机上，单击 " **开始**"，单击 " **所有程序**"，单击 " **附件**"，右键单击 " **命令提示符**"，然后单击 "以 **管理员身份运行**"。

2.  在控制台窗口中，键入以下命令，然后按 ENTER：
    
        bitsadmin /util /SetIEProxy NetworkService NO_PROXY

命令窗口中将显示以下消息：

    BITSAdmin is deprecated and is not guaranteed to be available in future versions of Windows. Administration tools for the BITS service are now provided by BITS PowerShell cmdlets.
    
    Internet proxy settings for account NetworkService set to NO_PROXY. 
    (connection = default)

此消息表示已禁用网络服务帐户的 Internet Explorer 代理设置。

</div>

<div>

## <a name="exchange-unified-messaging-synthetic-transactions"></a>Exchange 统一消息合成事务

Exchange 统一消息 (UM) 合成事务验证测试用户是否可以连接到 Exchange 中的语音邮件帐户。 这些测试用户将需要使用语音邮件帐户进行预配置，然后他们才能使用 Exchange UM 测试。

</div>

<div>

## <a name="persistent-chat-synthetic-transactions"></a>持久聊天合成事务

若要使用持久聊天合成事务，管理员必须首先创建一个通道，并向测试用户提供使用它的权限。 [CsPersistentChatMessage](https://docs.microsoft.com/powershell/module/skype/Test-CsPersistentChatMessage) cmdlet 可用于正确配置这些测试用户：

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-cs-001.litwareinc.com -SenderSipAddress sip:kenmyer@litwareinc.com -SenderCredential $cred1 -ReceiverSipAddress sip:pilar@litwareinc.com -ReceiverCredential $cred2 -TestUser1SipAddress sip:kenmyer@litwareinc.com -TestUser2SipAddress sip:pilar@litwareinc.com -Setup $True

此设置任务必须从企业内部运行：

  - 如果从 nonserver 计算机运行，则运行 cmdlet 的用户必须是 Role-Based 访问控制 (RBAC) 的 PersistentChatAdministrators 角色的成员。

  - 如果从服务器本身运行，则运行 cmdlet 的用户应是 RTCUniversalServerAdmins 组的成员。

在前面的命令中，包含了 Setup 参数，并将其设置为 True ($True) 。 如果包含 Setup 参数，Test-CsPersistentChatMessage 将创建一个特殊的持久聊天室，并使用测试用户填充该聊天室。 这有助于确保实际有一个聊天室可供测试之用。 请注意，只能从前端服务器运行 Setup 参数。

由 Test-CsPersistentChatMessage 创建的聊天室只能由管理员删除。

</div>

<div>

## <a name="pstn-peer-to-peer-call-synthetic-transactions"></a>PSTN 对等呼叫合成事务

[CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall)合成事务通过公共交换电话网络 (PSTN) 验证是否有权拨打和接听呼叫。

若要运行此合成事务，管理员必须配置：

  -  (呼叫者和接收器的两个测试用户，) 支持企业语音。

  - 对于每个用户帐户，直接向内拨号 () 号码。

  - 语音策略和语音路由，可呼叫接收器的号码以到达 PSTN 网关。

  - 可接受呼叫的 PSTN 网关，以及根据所拨打的号码将呼叫路由到接收器主池的媒体。

</div>

<div>

## <a name="unified-contact-store-synthetic-transactions"></a>统一联系人存储合成事务

统一联系人存储综合事务验证 Lync Server 2013 是否可以代表用户从 Microsoft Exchange Server 2013 检索联系人。

若要使用此合成事务，必须满足以下条件：

  - [若要管理服务器到服务器身份验证，请 (Lync server 2013 中的 OAuth) 和合作伙伴应用程序](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) 必须在 lync server 2013 和 Exchange 2013 之间配置。

  - 测试用户必须具有有效的 Exchange 2013 邮箱。

满足这些条件后，管理员可以运行以下命令来验证具有 SIP 地址 kenmyer@litwareinc.com 的用户是否可以从 "统一联系人存储" 检索其联系人：

    Test-CsUnifiedContactStore -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -RegistrarPort 5061 -Authentication TrustedServer -Setup

请注意在前面的命令中使用的 Setup 参数的使用。 如果在运行 Test-CsUnifiedContactStore 时包含 Setup 参数，则指定用户的联系人 (在这种情况下，sip:kenmyer@litwareinc.com) 将被移动到 "统一联系人存储"。  (当然，如果用户的联系人已在 "统一联系人存储" 中，则不需要移动它们。 ) Setup 参数通常仅在第一 Test-CsUnifiedContactStore 次执行) 时才使用 (，并且应仅与测试用户一起使用;也就是说，将永远不会登录到 Lync Server 的用户帐户。 当测试用户已迁移到 "统一联系人存储" 之后，您可以通过不使用 Setup 参数调用 Test-CsUnifiedContactStore 来验证用户的联系人是否可以检索：

    Test-CsUnifiedContactStore -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -RegistrarPort 5061 -Authentication TrustedServer

</div>

<div>

## <a name="xmpp-synthetic-transactions"></a>XMPP 合成事务

XMPP (可扩展消息和状态协议) IM 合成事务要求 XMPP 功能配置一个或多个联合域。

若要启用 XMPP 合成事务，必须向可路由的 XMPP 域中的用户帐户提供 XmppTestReceiverMailAddress 参数。 例如：

    Set-CsWatcherNodeConfiguration -Identity pool0.contoso.com -Tests @{Add="XmppIM"} -XmppTestReceiverMailAddress user1@litwareinc.com

在此示例中，需要存在 Lync Server 2013 规则才能将 litwareinc.com 的邮件路由到 XMPP 网关。

</div>

</div>

<span> </span>

</div>

</div>

</div>

