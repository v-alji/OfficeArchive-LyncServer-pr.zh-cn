---
title: Lync Server 2013： IP 手机的拓扑
description: Lync Server 2013： IP 电话的拓扑。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies for IP phones
ms:assetid: 26ebffcf-43ff-4e70-847d-0fbc90e94e57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425740(v=OCS.15)
ms:contentKeyID: 48183662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a151a83a69e1f7e14dcbed8d8ab1038157fa839
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439654"
---
# <a name="topologies-for-ip-phones-in-lync-server-2013"></a>Lync Server 2013 中的 IP 电话拓扑

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-06-21_

本部分概述了连接过程，并介绍了 IP 电话在内部和外部网络中的连接方式之间的区别。

<div>


> [!NOTE]  
> Lync Server 提供对以下 IP 手机的支持： Aastra 6721ip 常见的区域电话、Aastra 6725ip 桌面电话、HP 4110 IP 电话 (常见的区域电话) 、HP 4120 IP 手机 (桌面电话) 、Polycom CX600 IP 桌面电话、Polycom CX700 IP 桌面电话、Polycom CX500 IP 公共区域电话以及 Polycom CX3000 IP 会议电话。 在这些电话中，除 Polycom CX700 之外的所有其他设备都可以运行 Lync Phone Edition。



</div>

下图介绍了企业环境中的设备连接所涉及的所有组件。

**内部拓扑**

![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")

<div>


> [!NOTE]  
> 上图是逻辑表示形式，而不是物理概述。 例如， (AD DS) 的 Active Directory 域服务很少与任何 Lync Server 组件位于同一台计算机上。 用户存储可以位于后端服务器或存档和监视服务器上。 Lync Server Management Shell、web 服务器和更新服务均为前端服务器角色的一部分。



</div>

下图简要介绍了设备位于公司网络外部时所涉及的组件。

**外部拓扑**

![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")

<div>


> [!NOTE]  
> 设备更新 Web 服务提供外部和内部网站，但仅在此处显示外部网站。<BR>如果启用外部访问，则注册机构和设备更新 Web 服务的 URL 的位置必须在 DNS 中发布。 此外，还必须部署和正确配置边缘服务器，以便允许从设备到公司环境的外部通信。 这将从以前的图表中省略，因为 Edge 部署并非特定于设备连接。



</div>

</div>

<span> </span>

</div>

</div>

</div>

