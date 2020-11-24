---
title: 为试点池部署配置 DNS 记录
description: 为试验池部署配置 DNS 记录。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392059"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a>为试点池部署配置 DNS 记录

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-29_

在部署 Lync Server 2013 试验池之前，必须为试验池更新 DNS 主机的条目。 若要成功完成此过程，你应作为域管理员组的成员或 DnsAdmins 组的成员登录到服务器或域。

**配置 DNS 主机 A 记录**

1.  在域名系统 (DNS) 服务器上，单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。

2.  在您的域的控制台树中，展开 " **正向查找区域**"，然后右键单击将安装 Lync Server 2013 的域。

3.  单击 " **新建主机" (A 或 AAAA)**。

4.  单击 " **名称**"，键入 Lync Server 2013 池的主机名 (域名是从定义记录的区域中假定的，不需要作为 A 记录) 的一部分输入。

5.  单击 " **IP 地址**"，键入前端池的 ip 地址。

6.  单击 " **添加主机**"，然后单击 **"确定"**。

7.  完成后，单击 " **完成**"。

</div>

<span> </span>

</div>

</div>

</div>

