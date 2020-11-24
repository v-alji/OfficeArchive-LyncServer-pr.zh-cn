---
title: Lync Server 2013：部署统一联系人存储
description: Lync Server 2013：部署统一联系人存储。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying unified contact store
ms:assetid: 68959d58-ac8a-45de-afcd-b9de2c36799c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204963(v=OCS.15)
ms:contentKeyID: 48184373
ms.date: 06/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 056792d2e4ea66699b276d0d571e83c8a0256483
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391831"
---
# <a name="deploying-unified-contact-store-in-lync-server-2013"></a>在 Lync Server 2013 中部署统一联系人存储

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2016-06-06_

在 Lync Server 2013 中启用统一联系人存储不需要任何拓扑设置。 为用户启用统一联系人存储需要以下各项：

  - 启用统一的联系人存储库策略（将启用默认值）。

  - 用户至少以 Lync 2013 登录。

迁移用户的联系人后，当用户使用 Lync 2013 登录时，该用户可以在 Lync 2013、Outlook 2013 或 Outlook Web Access 中访问和管理其 Lync 联系人。 用户不必登录 Lync 即可从 Outlook 或 Outlook Web Access 管理其联系人。

<div>


> [!IMPORTANT]  
> 如果用户在迁移后从 Lync 2010 登录，则 "联系人" 和 "组" 可用且是最新的，但用户无法管理 (，即添加、删除、移动、标记、取消标记或修改) 这些联系人。



</div>

<div>

## <a name="in-this-section"></a>本节内容

  - [在 Lync Server 2013 中为用户启用统一联系人存储](lync-server-2013-enable-users-for-unified-contact-store.md)

  - [在 Lync Server 2013 中将用户迁移到统一联系人存储](lync-server-2013-migrate-users-to-unified-contact-store.md)

  - [在 Lync Server 2013 中回滚已迁移用户](lync-server-2013-roll-back-migrated-users.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

