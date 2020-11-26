---
title: Lync Server 2013：还原企业版成员服务器
description: Lync Server 2013：还原企业版成员服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring an Enterprise Edition member server
ms:assetid: d960b19c-2104-4719-b736-0d940f254d42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202191(v=OCS.15)
ms:contentKeyID: 51541523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f9838f030205d92988e185798d982f835122c9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436207"
---
# <a name="restoring-an-enterprise-edition-member-server-in-lync-server-2013"></a>在 Lync Server 2013 中还原企业版成员服务器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-18_

如果运行下列服务器角色之一的服务器失败，请按照本主题中的过程还原服务器。 如果多台服务器独立失败，请按照每台服务器的步骤进行操作。

  - 前端服务器

  - 中介服务器

  - 控制器

  - 持久聊天服务器

  - 边缘服务器

<div>


> [!TIP]  
> 我们建议你先拍摄系统的映像副本，然后再开始还原。 你可以将此映像用作回退点，以防在还原过程中出现问题。 您可能希望在安装操作系统和 SQL Server 后获取图像副本，并还原或重新注册证书。



</div>

<div>

## <a name="to-restore-a-member-server"></a>还原成员服务器

1.  从具有相同的完全限定的域名（ (FQDN) 为失败的服务器）开始，安装操作系统，然后还原或重新注册证书。
    
    <div>
    

    > [!NOTE]  
    > 按照组织的服务器部署过程执行此步骤。

    
    </div>

2.  从作为 RTCUniversalServerAdmins 组成员的用户帐户，登录到要还原的服务器。

3.  浏览到 Lync Server 安装文件夹或媒体，然后启动位于 \\ 安装 amd64Setup.exe 的 Lync Server 部署向导 \\ \\ 。

4.  按照部署向导执行下列操作：
    
    1.  运行 **步骤1：安装本地配置存储** 以安装本地配置文件。
    
    2.  运行 **步骤2：设置或删除 Lync Server 组件** 以安装 lync server 服务器角色。
    
    3.  运行 **步骤3：请求、安装或分配证书** 以分配证书。
    
    4.  运行 **步骤4：启动服务** 以启动服务器上的服务。
    
    有关运行部署向导的详细信息，请参阅要还原的服务器角色的部署文档。

</div>

</div>

<span> </span>

</div>

</div>

</div>

