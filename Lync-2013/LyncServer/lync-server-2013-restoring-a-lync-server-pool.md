---
title: Lync Server 2013：还原 Lync Server 池
description: Lync Server 2013：还原 Lync Server 池。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Lync Server pool
ms:assetid: 6fe80fb3-38ad-4931-a07b-1763b61aa448
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202176(v=OCS.15)
ms:contentKeyID: 51541488
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02e92b4e7af9cf782d49c265425006e0118b9161
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442598"
---
# <a name="restoring-a-lync-server-pool-in-lync-server-2013"></a>在 Lync Server 2013 中还原 Lync 服务器池

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-18_

Lync Server 部署可能包含以下任何类型的池：

  - 前端服务器

  - 中介服务器

  - 持久聊天服务器

  - 边缘服务器

如果整个池遇到中断，请针对池中的每个成员服务器执行这些过程。

  - 对于前端池，先还原后端服务器，然后还原每个前端服务器。 有关详细信息，请参阅 [在 Lync server 2013 中还原企业版后端服务器](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md) 和 [在 lync Server 2013 中还原企业版成员服务器](lync-server-2013-restoring-an-enterprise-edition-member-server.md)。

  - 对于所有其他类型的池，请还原每个成员服务器。 有关详细信息，请参阅 [在 Lync server 2013 中还原企业版成员服务器](lync-server-2013-restoring-an-enterprise-edition-member-server.md)。

</div>

<span> </span>

</div>

</div>

</div>

