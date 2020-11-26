---
title: Lync Server 2013：启动服务器上的服务
description: Lync Server 2013：在服务器上启动服务。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Start services on servers
ms:assetid: fa26eaed-0529-4f32-9f3f-f32c4bd4b1c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413059(v=OCS.15)
ms:contentKeyID: 48185912
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c238d7ddbba66604314d146a2e7f86eaa85eeb9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441555"
---
# <a name="start-services-on-servers-for-lync-server-2013"></a>为 Lync Server 2013 启动服务器上的服务

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-09-03_

若要成功完成此过程，你应作为 RTCUniversalServerAdmins 组成员的用户登录，或者委派了正确的权限。 有关委派权限的详细信息，请参阅 [在 Lync Server 2013 中委派设置权限](lync-server-2013-delegate-setup-permissions.md)主题。

在服务器上安装本地配置存储后，安装 Lync Server 2013 组件，并在前端服务器或前端服务器上配置证书，必须在服务器上启动 Lync Server 2013 服务。 使用以下过程在部署中的每个前端服务器上启动服务。

<div>

## <a name="to-start-services-on-a-standard-edition-or-front-end-server"></a>在标准版或前端服务器上启动服务

1.  在 Lync Server 部署向导的 " **Lync server 2013** " 页面上，单击 "**步骤4：启动服务**" 旁边的 "**运行**"。

2.  在 " **启动服务** " 页面上，单击 " **下一步** " 以启动服务器上的 Lync Server 服务。

3.  在“**正在执行命令**”页上，成功启动所有服务后，单击“**完成**”。
    
    <div>
    

    > [!IMPORTANT]  
    > 在服务器上启动服务的命令是报告服务已开始的最佳方法。 该命令可能无法反映服务的实际状态。 我们建议你在 "<STRONG>启动服务</STRONG>") 立即使用 "分步<STRONG>服务状态" (可选</STRONG>，以打开 MICROSOFT 管理控制台 (MMC) 并确认服务已成功启动。 如果任何 Lync Server 服务尚未启动，可以右键单击 MMC 中的该服务，然后单击 " <STRONG>启动</STRONG>"。

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

