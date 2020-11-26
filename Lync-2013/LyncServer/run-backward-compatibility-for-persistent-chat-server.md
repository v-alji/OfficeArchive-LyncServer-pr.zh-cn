---
title: 为持久聊天服务器运行向后兼容
description: 持久聊天服务器的运行向后兼容性。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run backward compatibility for Persistent Chat Server
ms:assetid: 53f1a706-3104-4a94-8b4e-8badd9a066d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204901(v=OCS.15)
ms:contentKeyID: 48184175
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0486992d44e6385559d3e9df9f9ffc2125120da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423377"
---
# <a name="run-backward-compatibility-for-persistent-chat-server"></a>为持久聊天服务器运行向后兼容

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-21_

Lync Server 2013、持久聊天服务器终结点提供一种方法来创建指向持久聊天服务器池的简单 URL。 这对于旧版客户端 (Microsoft Office 通信服务器 2007 R2 群组聊天服务器或 Lync Server 2010，群组聊天) ，因为当尝试将旧客户端指向运行 Lync 2013 的计算机时，用户可以在手动配置中输入简单的 URL，持续聊天。 此终结点不会由永久聊天使用，并且仅对旧客户端是必需的。 这对于可以迁移会议室的中间时期非常有用，但 Lync 2013 客户端尚未在整个组织中部署。 运行 Lync 2010 组聊天 (客户端) 之后仍然可以连接到持久聊天服务器后端服务器。

无需创建多个持久聊天服务器终结点;您只需要每个持久聊天服务器池的一个。 管理员可以 (每个池) 创建多个终结点，但旧客户端可以配置为一次仅连接到一个池。 在常规或主流方案中，旧式部署仅为一个池。 新部署通常会将该池迁移到新的 Lync Server 2013，并且可能会添加一些新的附加持久聊天服务器池。

此主流方案通常遵循以下模式：

  - 你可以使用一个 Lync Server 2010、群组聊天池和 Lync 2010 组聊天客户端连接到该池，方法是使用某些已知用户 (默认 sip： ocschat@ \<domainName\> .com 或类似) 。 用户是启用 SIP 的 Active Directory 域服务，并且查找服务会向他们注册以接收传入的请求。

  - 然后，安装 Lync Server 2013 持久聊天服务器和持久聊天服务器池。

  - 在用户通常脱机的时间内 (例如，周末) ：
    
      - 关闭 Lync Server 2010，群组聊天。
    
      - 将数据从 Lync Server 2010、群组聊天池迁移到 Lync Server 2013 持久聊天服务器池。
    
      - 从 Active Directory 域服务中删除众所周知的用户。
    
      - 使用与以前删除的已知用户相同的 SIP URI 创建新的 *旧式终结点* 。
    
      - 启动 Lync Server 2013 和持久聊天服务器。

  - 用户使用其 Lync 2010 组聊天 (客户端) 并连接到其数据，而无需更改任何配置。

  - 以后，您可以解除 Lync Server 2010、群组聊天。 然后，你可以部署 Lync Server 2013、持久聊天服务器以及安装新的 Lync Server 2013 持久聊天服务器池。

有关从 Lync Server 2010 进行迁移的详细信息，群组聊天到 Lync Server 2013，持久聊天服务器，请参阅 [从 Lync server 2010 迁移、群组聊天或 Office 通信服务器 2007 R2 群组聊天到 Lync Server 2013、持久聊天服务器](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)。

若要运行向后兼容性 (以创建指向持久聊天服务器池的持久聊天服务器终结点，该终结点可由旧式群组聊天池客户端使用) ：

    New-CsPersistentChatEndpoint -SipAddress <CO name, ex. persistentchat@contoso.com> -PersistentChatPoolFqdn <pool FQDN, like pcpool.contoso.com>

接下来，配置持久聊天客户端以将该 SIP 地址用作其 contact 对象。 SIP 地址是使用特定持久聊天服务器池的 **CsPersistentChatEndpoint** cmdlet 创建的。

若要使用 Windows PowerShell 命令行界面添加持久聊天服务器终结点，请考虑以下示例。 在此情况下，你正在将 contact 对象配置为 "contoso.com" 拓扑中的 "persistentchat"，其中池 (FQDN) 的池完全限定的域名为 "pcpool.contoso.com"：

    New-CsPersistentChatEndpoint -SipAddress sip:persistentchat@contoso.com -PersistentChatPoolFqdn pcpool.contoso.com

<div>

## <a name="see-also"></a>另请参阅


[从 Lync Server 2010 群聊或 Office Communications Server 2007 R2 群聊迁移到 Lync Server 2013 持久聊天服务器](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

