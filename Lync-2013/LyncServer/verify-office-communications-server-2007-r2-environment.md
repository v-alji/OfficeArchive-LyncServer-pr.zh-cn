---
title: 验证 Office Communications Server 2007 R2 环境
description: 验证 Office 通信服务器 2007 R2 环境。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify Office Communications Server 2007 R2 environment
ms:assetid: e051bdd5-e7ef-4754-8705-900b2c57f37c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721906(v=OCS.15)
ms:contentKeyID: 49733840
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eb200941b3a35ece2b587bcfc89be743c9960d1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443630"
---
# <a name="verify-office-communications-server-2007-r2-environment"></a>验证 Office Communications Server 2007 R2 环境

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-16_

在使用 Office 通信服务器 2007 R2 在共存状态中部署 Lync Server 2013 之前，需要验证 Office 通信服务器是否已配置和启动 2007 R2 服务。

**验证池是否已使用 Office 通信服务器 2007 R2 管理工具启动**

1.  打开 Office 通信服务器 2007 R2 管理工具。

2.  展开 " **林** " 节点，展开 " **标准版服务器** " 或 " **企业版池** " 节点，然后展开 "池" 或 "服务器名称"。

3.  确保服务在标准版服务器或企业版池上运行。
    
    ![Office 通信服务器 2007 R2 管理控制台](images/JJ721906.76897b6d-f433-47d2-930d-0816fc30a3c2(OCS.15).jpg "Office 通信服务器 2007 R2 管理控制台")

**查看针对 Office 通信服务器 2007 R2 配置的用户**

1.  打开 Office 通信服务器 2007 R2 管理工具。

2.  展开 " **林** " 节点，展开 " **标准版服务器** " 或 " **企业版池** " 节点，然后展开 "池" 或 "服务器名称"。

3.  单击 " **用户**"。

4.  验证 Office 通信服务器 2007 R2 用户的列表。
    
    ![OCS 管理工具中的用户列表](images/JJ721906.f6bb7c4f-cbed-4389-8d0a-69a28577f17a(OCS.15).jpg "OCS 管理工具中的用户列表")

**验证旧版 XMPP 联盟合作伙伴配置**

1.  从旧的 XMPP 服务器中，导航到 "管理工具 \\ 服务" 小程序。

2.  验证是否已启动 Office 通信服务器 XMPP 网关服务。
    
    ![Office 通信服务器 XMPP 网关服务](images/JJ721906.23223724-3c4b-4cb9-ace2-1cab2c3c91c3(OCS.15).jpg "Office 通信服务器 XMPP 网关服务")

</div>

<span> </span>

</div>

</div>

</div>

