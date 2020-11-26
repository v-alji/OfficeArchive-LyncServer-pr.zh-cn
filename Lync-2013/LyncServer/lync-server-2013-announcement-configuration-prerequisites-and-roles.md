---
title: Lync Server 2013：通知配置先决条件和角色
description: Lync Server 2013：声明配置先决条件和角色。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439966"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a>Lync Server 2013 中的通知配置先决条件和角色

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-25_

"发布" 是企业语音呼叫管理功能。 本主题介绍了在配置公告和执行配置任务所需的角色分配之前需要具备的准备工作。

本部分假设你已阅读与公告 (有关的计划文档，请参阅 [在 Lync Server 2013) 中规划呼叫管理功能](lync-server-2013-planning-for-call-management-features.md) 。

<div>

## <a name="announcement-configuration-prerequisites"></a>公告配置先决条件

通知应用程序需要以下组件：

  - 应用程序服务

  - 响应组应用程序

  - 文件存储，用于保存音频文件

在部署企业语音时，默认情况下会安装所有这些组件。

</div>

<div>

## <a name="announcement-configuration-roles"></a>公告配置角色

可以使用以下管理工具配置公告：

  - Lync Server 控制面板

  - Lync Server 命令行管理程序

配置公告应用程序需要以下管理角色之一：

  - **CsVoiceAdministrator**   管理员角色可以创建、配置和管理所有与语音相关的设置和策略，包括公告设置。

  - **CsServerAdministrator**   管理员角色可以管理、监视和排除服务器和服务，以及配置所有公告设置。

  - **CsAdministrator**   管理员角色可以执行所有管理任务和修改所有设置。

  - **CsViewOnlyAdministrator**   此管理员角色可以查看部署以监控部署运行状况。

<div>


> [!NOTE]  
> 有关管理员用户权限的详细信息，请参阅规划文档中的在 <A href="lync-server-2013-planning-for-role-based-access-control.md">Lync Server 2013 中规划基于角色的访问控制</A> 。



</div>

</div>

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中部署企业语音](lync-server-2013-deploying-enterprise-voice.md)  


[在 Lync Server 2013 中规划呼叫管理功能](lync-server-2013-planning-for-call-management-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

