---
title: Lync Server 2013：管理混合部署中的用户
description: Lync Server 2013：管理混合部署中的用户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391771"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a>管理混合 Lync Server 2013 部署中的用户

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-05-29_

你可以使用 Microsoft 365 管理中心提供的用户管理功能管理迁移到 Lync Online 的用户的用户设置和策略。 您必须使用租户管理员帐户登录才能执行管理任务。

<div>

## <a name="moving-users-back-to-on-premises"></a>将用户移回本地

<div class="">


> [!IMPORTANT]  
> 此部分仅适用于为本地 Lync 创建和启用的用户，然后从本地部署移动到 Lync Online。 如果你想要移动在 Lync Online 中创建的用户 (并且尚未在本地) 部署中启用 Lync，请参阅在 <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013 中将用户从 Lync Online 移动到本地 lync</A>。



</div>

  - 运行以下 cmdlet，将用户从 Lync Online 移回本地 Lync：
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

为 **HostedMigrationOverrideUrl** 参数指定的 URL 的格式必须为运行托管迁移服务的池的 URL，格式如下：

Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc。 你可以通过查看 Microsoft 365 或 Office 365 组织帐户的 Lync Online 控制面板的 URL 来确定托管迁移服务的 URL。

**确定 Microsoft 365 或 Office 365 组织的托管迁移服务 URL**

1.  以管理员身份登录您的组织。

2.  打开 **Lync 管理中心**。

3.  在显示 **Lync 管理中心** 的情况下，在地址栏中选择并将 URL 复制到 **lync.com**。 示例 URL 如下所示：
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  将 URL 中的 **webdir** 替换为 **admin**，得到以下 URL：
    
    `https://admin0a.online.lync.com`

5.  向 URL 附加以下字符串：**/HostedMigration/hostedmigrationservice.svc**。
    
    得到的 URL 是 **HostedMigrationOverrideUrl** 的值，应类似于以下形式：
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

</div>

</div>

<span> </span>

</div>

</div>

</div>

