---
title: 迁移存档和监控服务器
description: 迁移存档和监视服务器。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating Archiving and Monitoring servers
ms:assetid: 77831579-df45-4697-b8c5-207b74a07a40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205015(v=OCS.15)
ms:contentKeyID: 48184550
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2dabd16fd38dbf463a4bc608fe77368e781571fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443746"
---
# <a name="migrating-archiving-and-monitoring-servers"></a>迁移存档和监控服务器

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-02_

如果在 Lync Server 2010 环境中部署了存档服务器和监视服务器，则可以在迁移前端池后在 Lync Server 2013 环境中部署这些服务器。 但是，如果存档和监视功能对你的组织至关重要，则应在迁移之前将存档和监视添加到 Lync Server 2013 试验池，以便在迁移过程中使用该功能。

如果在迁移过程中需要存档和监视功能，请记住以下注意事项：

  - 存档数据和监视数据不会迁移到 Lync Server 2013 部署。 您在取消旧版环境之前备份的数据将是 Lync Server 2010 环境中的活动历史记录。

  - Lync Server 2010 版本的存档服务器和监视服务器只能与 Lync Server 2010 前端池关联。 在 Lync Server 2013 中，存档和监控不再是服务器角色，而是与 Lync Server 2013 前端池集成的服务。

  - 在旧版本和 Lync Server 2013 部署共存期间，将在 Lync server 2010 版本的存档服务器和监视服务器上为驻留在 Lync Server 2010 池中的用户收集数据。 Lync Server 2013 中的存档和监视为驻留在 Lync Server 2013 池中的用户收集数据。
    
    <div>
    

    > [!NOTE]  
    > 在迁移阶段，当你仍将旧式 Edge 服务器与新的 Lync Server 2013 试验池配合使用时，存档服务器的 Lync Server 2010 版本会继续为驻留2010在 lync server 2013 中的用户收集数据，以供驻留在 lync server 2013 池中的用户收集数据。

    
    </div>

  - 如果您将第三方存档和监视解决方案与 Lync Server 2013 中的存档和监视结合使用，请咨询您的供应商，了解何时以及如何将第三方解决方案与 Lync Server 2013 集成。

</div>

<span> </span>

</div>

</div>

</div>

