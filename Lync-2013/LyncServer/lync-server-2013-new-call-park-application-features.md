---
title: Lync Server 2013：新的呼叫寄存应用程序功能
description: Lync Server 2013：新的通话寄存应用程序功能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Call Park application features
ms:assetid: bddff13c-92cc-47fd-bfd4-6e8bfbfed11b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412927(v=OCS.15)
ms:contentKeyID: 48185277
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a000fc288a920773b0dc1e4a7e8fe1fb20fbb3dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445461"
---
# <a name="new-call-park-application-features-in-lync-server-2013"></a><span data-ttu-id="b15c4-103">Lync Server 2013 中新的呼叫寄存应用程序功能</span><span class="sxs-lookup"><span data-stu-id="b15c4-103">New Call Park application features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b15c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b15c4-104">

<span> </span></span></span>

<span data-ttu-id="b15c4-105">_**主题上次修改时间：** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="b15c4-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="b15c4-106">"呼叫驻留" 应用程序使企业语音用户可以将呼叫置于保持状态，然后在以后通过任何电话取回呼叫。</span><span class="sxs-lookup"><span data-stu-id="b15c4-106">The Call Park application makes it possible for Enterprise Voice users to put a call on hold and then retrieve it later from any phone.</span></span> <span data-ttu-id="b15c4-107">停用呼叫的用户可以拨打由呼叫公园提供的 "轨道" 编号以检索寄存的呼叫，或使用外部机制（如即时消息 (IM) 或页面系统），让其他人检索呼叫。</span><span class="sxs-lookup"><span data-stu-id="b15c4-107">The user who parked the call can either dial the orbit number provided by Call Park to retrieve the parked call or use an external mechanism, such as instant messaging (IM) or a paging system, to ask someone else to retrieve the call.</span></span>

<span data-ttu-id="b15c4-108">Lync Server 2013 以故障转移和故障回复进程的形式提供了新的灾难恢复机制。</span><span class="sxs-lookup"><span data-stu-id="b15c4-108">Lync Server 2013 provides new disaster recovery mechanisms in the form of failover and failback processes.</span></span> <span data-ttu-id="b15c4-109">这些故障转移和故障回复进程支持通过主池中托管的用户在主池中出现中断时利用备份池的调用寄存应用程序，从而支持呼叫寄存功能的恢复。</span><span class="sxs-lookup"><span data-stu-id="b15c4-109">These failover and failback processes support recovery of Call Park functionality by allowing users who are homed in the primary pool to leverage the Call Park application of the backup pool when an outage occurs in the primary pool.</span></span> <span data-ttu-id="b15c4-110">对调用寄存应用程序进行灾难恢复的支持作为成对的前端池配置和部署的一部分启用。</span><span class="sxs-lookup"><span data-stu-id="b15c4-110">Support for disaster recovery of the Call Park application is enabled as part of the configuration and deployment of paired Front End pools.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="b15c4-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b15c4-111">See Also</span></span>


[<span data-ttu-id="b15c4-112">在 Lync Server 2013 中规划呼叫寄存</span><span class="sxs-lookup"><span data-stu-id="b15c4-112">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)  
  

<span data-ttu-id="b15c4-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b15c4-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

