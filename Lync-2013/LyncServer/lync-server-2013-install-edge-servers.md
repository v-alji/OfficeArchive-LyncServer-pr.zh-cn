---
title: Lync Server 2013：安装边缘服务器
description: Lync Server 2013：安装 Edge 服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Edge Servers
ms:assetid: 1655ab69-3899-4ee4-a1cc-8243bc1bfa0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398230(v=OCS.15)
ms:contentKeyID: 48183503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e699a7f41b0ee554bc85fb2d9a72a2d9a42870cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427206"
---
# <a name="install-edge-servers-for-lync-server-2013"></a>安装适用于 Lync Server 2013 的边缘服务器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-08_

使用 Lync Server 部署向导在 Edge 服务器上安装 Lync Server 2013。 通过在每台边缘服务器上运行部署向导，可以完成设置边缘服务器所需的大部分任务。 为了在 Edge 服务器上部署 Lync Server 2013，你必须已运行拓扑生成器才能定义和发布你的 Edge 服务器拓扑，并将其导出到从 Edge 服务器中可用的媒体。 有关详细信息，请参阅 [Lync server 2013 中的外部用户访问应用场景](lync-server-2013-scenarios-for-external-user-access.md) 和 [导出 Lync server 2013 拓扑并将其复制到外部媒体进行边缘安装](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)。

使用部署向导安装每台边缘服务器、安装和分配所需的证书并启动所需的服务后，你可以通过在 [lync server 2013 中配置对外部用户访问的支持](lync-server-2013-configuring-support-for-external-user-access.md) 中的信息来完成设置，以启用和配置外部用户访问以及在 [lync Server 2013 中验证边缘部署](lync-server-2013-verifying-your-edge-deployment.md) 以验证设置（包括服务器和客户端连接）的信息。

<div>

## <a name="to-install-an-edge-server"></a>安装边缘服务器

1.  登录到要将边缘服务器安装为本地管理员组的成员的计算机，或者登录到具有等效用户权利和权限的帐户。

2.  请确保使用拓扑生成器创建的拓扑配置文件，然后导出并复制到外部媒体，例如，访问在其 (上复制拓扑配置文件的 USB 驱动器，或验证对将文件复制到的网络共享的访问权限) 。

3.  启动部署向导。
    
    <div>
    

    > [!NOTE]  
    > 如果收到一条消息，指出需要安装 Microsoft Visual c + + 可再发行组件，请单击 <STRONG>"是"</STRONG>。 在下一个对话框中，您可以接受默认 <STRONG>安装位置</STRONG> ，也可以单击 " <STRONG>浏览</STRONG> " 以选择备用位置，然后单击 " <STRONG>安装</STRONG>"。 在 "下一个" 对话框中，选中 " <STRONG>我接受许可协议中的条款</STRONG> " 复选框，然后单击 <STRONG>"确定"</STRONG>。

    
    </div>

4.  在部署向导中，单击 " **安装或更新 Lync Server 系统**"。

5.  向导确定部署状态后，针对 **步骤1。安装本地配置存储**，单击 " **运行** "，然后执行以下操作：
    
      - 在 " **配置中央管理存储的本地副本** " 对话框中，单击 " **从文件导入 (对于边缘服务器) 推荐的文件**，转到导出的拓扑配置文件的位置，选择 .zip 文件，单击" **打开**"，然后单击" **下一步**"。
    
      - 部署向导从配置文件中读取配置信息，并将 XML 配置文件写入本地计算机。
    
      - “**正在执行命令**”过程完成后，单击“**完成**”。

6.  在 "部署向导" 中，单击 " **步骤2：设置" 或 "删除 Lync Server 组件** " 以安装在存储在本地计算机上的 XML 配置文件中指定的 Lync server 2013 edge 组件。

7.  完成安装后，使用 [Lync Server 2013 的边缘证书为 Lync Server 设置边缘证书](lync-server-2013-set-up-edge-certificates.md) ，以便在启动服务之前安装和分配所需的证书。

</div>

</div>

<span> </span>

</div>

</div>

</div>

