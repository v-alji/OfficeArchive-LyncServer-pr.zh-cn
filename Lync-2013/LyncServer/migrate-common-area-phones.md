---
title: 迁移公共区域电话
description: 迁移常用的区域电话。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443823"
---
# <a name="migrate-common-area-phones"></a>迁移公共区域电话

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-29_

常见的区域电话是指通常位于共享工作区或通用区域（如大厅、厨房或工厂地板）的 IP 电话。 常用的区域电话无需连接到计算机即可提供 Lync Server UC 功能。 将 Lync Server 2010 部署迁移到 Lync Server 2013 之后，您还必须迁移与旧式公共区域电话相关联的联系人对象。 使用 Lync Server 管理外壳程序将首先检索与 Lync Server 2010 公共区域电话相关联的所有联系人对象，然后将这些对象移动到 Lync Server 2013 池。

**迁移公共区域电话**

1.  从 Lync Server 2013 前端服务器，打开 Lync Server 命令行管理程序。

2.  在命令行中，键入以下内容：
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  若要验证所有联系人对象是否已被移动到 Lync Server 2013 池，请从 Lync Server Management Shell 键入以下内容：
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    验证所有联系人对象现在是否与 Lync Server 2013 池相关联。

</div>

<span> </span>

</div>

</div>

</div>

