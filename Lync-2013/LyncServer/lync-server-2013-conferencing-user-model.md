---
title: Lync Server 2013 会议用户模型
description: Lync Server 2013 会议用户模型。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434276"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a>Lync Server 2013 中的会议用户模式

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-22_

Lync Server 会议用户模式的一个关键部分是 "会议大小"。 从多个数据点收集数据后 () 上一节中所述），我们确定以下几点：

  - 大多数会议实际上是最小的协作式会议，平均有四个到六个参与者

  - 大约80% 的会议人数少于20位参与者。

  - 99.98% 的会议的参与者数少于100。

除了会议大小，会议用户模型还考虑各种因素，例如：

  - **并发会议**   希望有多少个用户同时参与会议？

  - **媒体组合**   哪些类型的媒体可用且希望由会议中的用户使用？

  - **用户类型**   用户是内部用户、远程用户、联盟用户还是匿名用户？

  - **会议提升时间**   会议的所有用户加入会议需要多长时间？

有关用户模型的详细信息，请参阅 [Lync Server 2013 中的用户模型](lync-server-2013-user-models.md)。

若要确定用于测试的会议和用户数，请执行以下操作：

  - 占用了组织中的总用户数 (例如，80000用户) 并乘以会议并发费率 (例如，5% 的 "所有用户") 确定在同一时间召开会议的总用户数 (在本示例中，4000用户) 。

  - 按部署 (中的 Lync Server 2013、前端服务器数划分的总用户数例如，8台服务器) 确定每个前端服务器的会议参与者预计数量 (在此示例中，每前端服务器的500用户) 。

  - 按平均会议大小划分每个前端服务器的用户数 (例如，4个用户) 确定每个前端服务器的估计平均每前端服务器的平均数量 (本示例中，125每前端服务器) 的会议数。

  - 为了在每个前端服务器上获取每个媒体负载，我们估计媒体混合。 例如，假设75% 的会议需要的不仅仅是音频支持和50% 的会议需要应用程序共享，则平均47会议和188用户同时连接到每个前端服务器以进行应用程序共享。

  - 测试了各种会议大小 (基于在共享池中最多250用户的用户模型) 以确保服务器的可伸缩性。

</div>

<span> </span>

</div>

</div>

</div>

