---
title: Lync Server 2013：测试控制器
description: Lync Server 2013：测试 Director。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the Director
ms:assetid: 9627a7e2-28cc-429c-b79b-7c7a27573bb7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398767(v=OCS.15)
ms:contentKeyID: 48184856
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f4cec23be01add5c02cc960cfe68c9256da07d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441209"
---
# <a name="test-the-director-in-lync-server-2013"></a>在 Lync Server 2013 中测试控制器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-08_

在此阶段，配置了 Director 或控制器池，但域名系统 (DNS) SRV 条目仍指向客户使用池或标准版服务器登录。 在更改 DNS 记录以使 Lync 2013 客户通过使用控制器自动登录时，请通过将客户端手动指向 Director 来测试客户端。

<div>

## <a name="to-test-the-deployment"></a>测试部署

1.  使用 **CSAdministrator** 组中包含的域帐户登录到安装了 Lync Server 控制面板的计算机。

2.  打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。 有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。

3.  在 "导航窗格" 中，单击 " **拓扑**"，然后在 " **状态** " 列中确认是否存在带有箭头的绿色服务器 (也就是说， ![带有绿色箭头的服务器图标](images/Gg398767.2263cdb7-7e60-457a-a528-a3a082bd051b(OCS.15).jpg "带有绿色箭头的服务器图标")) 用于你的 director 或控制器池。

4.  将安装了 Lync Server 2013 客户端的两台客户端计算机连接到每台计算机上启用了 Lync Server 2013 的不同用户帐户。

5.  在其中一个客户端计算机上，单击 " **选项** " 菜单，选择 " **个人** 设置" 组，单击 " **高级**"，单击 " **手动配置**"，然后将 **内部服务器名称或 IP 地址** 设置为新的 director 或 Director pool (FQDN) 的完全限定的域名称。

6.  登录到这两个客户端，验证通过使用 Director 登录的客户端是否能够成功登录、查看其他用户的状态以及他们是否可以交换即时消息。

</div>

</div>

<span> </span>

</div>

</div>

</div>

