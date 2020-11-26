---
title: Lync Server 2013：文件共享高可用性
description: Lync Server 2013：文件共享高可用性。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: File sharing high availability
ms:assetid: b8c8d5ec-9397-4128-8d1e-8ec6c30fade7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205203(v=OCS.15)
ms:contentKeyID: 48185238
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 29b0a77d2d03460c640c66b8e8ce2a551edf2d73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428186"
---
# <a name="file-sharing-high-availability-in-lync-server-2013"></a>Lync Server 2013 中的文件共享高可用性

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-03-30_

为确保在单个数据中心内 Lync Server 文件共享的高可用性，您可以使用分布式文件系统 (DFS) 。 DFS 支持从一台文件服务器故障转移到相同数据中心内的其他文件服务器。 对于大规模部署，我们建议您使用通过 DFS 配对的专用文件服务器。

根据你的网络大小以及所需的复原量，你可以使用一对服务器来托管网站中的所有文件共享，或者对每个前端池使用一对。

DFS 是一个最有效的文件复制机制，未发布任何恢复时间目标 (RTO) 或恢复点目标 (RPO) 承诺。 应快速完成 DFS 服务器之间的故障转移，但数据复制延迟可能会阻止用户在发生故障转移时继续进行工作。

如果你在文件共享上使用 DFS 和数据存储非常重要，应经常备份文件共享，例如每4到8小时。 如果某个文件共享不可用且复制的状态不是最新，则可使用该备份将故障服务器上的内容还原到与此时不可用的服务器配对的另一台服务器上。

</div>

<span> </span>

</div>

</div>

</div>

