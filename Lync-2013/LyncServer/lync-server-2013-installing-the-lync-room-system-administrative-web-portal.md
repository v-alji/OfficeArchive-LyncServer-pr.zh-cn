---
title: Lync Server 2013：安装 Lync 会议室系统管理 Web 门户
description: Lync Server 2013：安装 Lync 会议室系统管理 Web 门户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427003"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a>Installing the Lync Room System Administrative Web Portal in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2015-04-09_

您可以从 Microsoft 下载中心下载 Microsoft Lync 会议室系统管理 Web 门户 [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) 。

若要安装 Lync 会议室系统管理 Web 门户，请使用以下步骤。

1.  通过在 Lync Server 命令行管理程序中运行以下 cmdlet 来配置受信任的应用程序端口：
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  若要安装会议室门户，请下载 **LyncRoomAdminPortal.exe** ，然后以管理员身份运行。

3.  打开以下位置中的 Web.config 文件：
    
    % 程序文件% \\ Microsoft Lync Server 2013 \\ Web Components 会议室 \\ 门户 \\ 程序 Int \\ 处理程序\\

4.  在 Web.Config 文件中，将 PortalUserName 更改为在步骤2中创建的用户名，在 "配置 Lync 会议室系统管理员的先决条件" 部分中， (步骤中的推荐名称是 LRSApp) ：
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  由于 LRS 管理门户是一个受信任的应用程序，因此无需在门户配置中提供密码。 如果此用户使用的是非本地注册器，你需要通过在 Web.Config 文件中添加以下行来为其指定注册器：
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  如果使用的端口不是 5061，则需要在 Web.Config 文件中添加以下行：
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a>验证 Lync 会议室系统管理 Web 门户的安装

若要验证 Lync 会议室系统管理 Web 门户的安装，请执行以下操作：


1.  在前端服务器上，浏览至以下 URL：
    
    https:// \<fe-server\> /lrs
    
    你不应该看到任何错误，如下图所示：
    
    ![Lync 聊天室系统管理门户登录屏幕](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync 聊天室系统管理门户登录屏幕")

2.  如果你未看到任何错误，请尝试从拓扑中的任何其他计算机访问以下 URL：
    
    https:// \<fe-server\> /lrs
    
    若要访问页面，你需要添加 DNS 记录，如 "自动客户登录所需的 DNS 记录" 中所述 [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) 。

</div>

</div>

<span> </span>

</div>

</div>

</div>

