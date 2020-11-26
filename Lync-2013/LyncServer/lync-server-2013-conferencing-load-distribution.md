---
title: Lync Server 2013 会议加载分发
description: Lync Server 2013 会议加载分发。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing load distribution
ms:assetid: 5901a076-1b6f-4720-8837-95fc7f3c37f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204922(v=OCS.15)
ms:contentKeyID: 48184233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28897b26d7351bf0ea577e2678d916aec6d15647
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434324"
---
# <a name="conferencing-load-distribution-in-lync-server-2013"></a>Lync Server 2013 中的会议负载分配

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-22_

与其他一些专用会议解决方案不同，Lync 服务器体系结构是共享硬件模型。 这意味着同一硬件由许多软件组件共享，每个组件都支持不同的实时通信。 每种类型的实时通信都将在服务器上放置特定负载。 例如，前端服务器可以 (SIP) 路由组件、web 应用程序 (（如通讯簿搜索) 、Web 会议服务、A/V 会议服务、企业语音应用程序 (和中介服务器）运行会话初始协议。 前端服务器上的一组数据库还为用户、联系人、联机状态、会议和语音路由数据提供存储和处理。 通过这种硬件共享、组件、服务和进程来争用 CPU 和内存资源，因此非会议工作负载对服务器缩放有直接影响。

与其他基于硬件的其他会议解决方案相比，Lync Server 会议体系结构是一个无保留模型。 当用户安排会议时，Lync Server 在会议数据库中创建记录，该记录用于存储会议数据，但不会提前为计划会议保留任何硬件资源。 因此，Lync Server 具有内置负载平衡逻辑，可通过在池中的所有前端服务器上平均分配负载的方式在前端服务器上动态分配会议资源。 这将有效地预配和利用硬件资源，但如果没有适当的计划) ，则很难支持非常大的会议 (尤其如此。 例如，当 Lync Server 2013 池的运行速度接近其最高容量时，每台前端服务器可能会主持大约125平均大小的会议。 再添加一个小型会议不会有问题，但是添加一个 1000 用户的会议就会出现问题，因为前端服务器可能无法在已有其他 125 个会议的同时支持这样的大型会议。

</div>

<span> </span>

</div>

</div>

</div>

