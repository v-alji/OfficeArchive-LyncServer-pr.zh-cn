---
title: Lync Server 2013：中继间路由
description: Lync Server 2013：中继间路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Inter-trunk routing
ms:assetid: f687a548-1f2e-48ed-9745-a13dc1f3698f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721940(v=OCS.15)
ms:contentKeyID: 49733877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e023956f28183423c04e94948acdec0df2c1284
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426863"
---
# <a name="inter-trunk-routing-in-lync-server-2013"></a><span data-ttu-id="b6718-103">Lync Server 2013 中的中继间路由</span><span class="sxs-lookup"><span data-stu-id="b6718-103">Inter-trunk routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6718-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6718-104">

<span> </span></span></span>

<span data-ttu-id="b6718-105">_**主题上次修改时间：** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="b6718-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="b6718-106">Lync Server 2013 通过支持 intertrunk 路由提供基本的会话管理。</span><span class="sxs-lookup"><span data-stu-id="b6718-106">Lync Server 2013 provides basic session management through the support of intertrunk routing.</span></span> <span data-ttu-id="b6718-107">此新功能使 Lync 服务器能够向下游电话系统提供呼叫控制功能。</span><span class="sxs-lookup"><span data-stu-id="b6718-107">This new capability enables Lync Server to provide call control functionalities to downstream telephony systems.</span></span> <span data-ttu-id="b6718-108">中继间路由可将 IP-PBX 互联到公用电话交换网 (PSTN) 网关，以便将来自专用交换机 (PBX) 电话的呼叫路由到 PSTN，而将传入 PSTN 呼叫路由到 PBX 电话。</span><span class="sxs-lookup"><span data-stu-id="b6718-108">Intertrunk routing can interconnect an IP-PBX to a public switched telephone network (PSTN) gateway so that calls from a private branch exchange (PBX) phone can be routed to the PSTN, and incoming PSTN calls can be routed to a PBX phone.</span></span> <span data-ttu-id="b6718-109">同样，Lync Server 可以互连两个或更多的 IP PBX 系统，以便可以在不同的 IP PBX 系统的 PBX 电话之间放置和接收呼叫。</span><span class="sxs-lookup"><span data-stu-id="b6718-109">Similarly, Lync Server can interconnect two or more IP-PBX systems so that calls can be placed and received between PBX phones from the different IP-PBX systems.</span></span>

<span data-ttu-id="b6718-110">下图说明了 Lync Server 2013 在 PSTN 网关和 IP PBX 之间提供 interconnectivity。</span><span class="sxs-lookup"><span data-stu-id="b6718-110">The following figure illustrates Lync Server 2013 providing interconnectivity between a PSTN gateway and an IP-PBX.</span></span>

<span data-ttu-id="b6718-111">![Lync Server - 连接 PSTN 网关/IP-PBX 图示](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server - 连接 PSTN 网关/IP-PBX 图示")</span><span class="sxs-lookup"><span data-stu-id="b6718-111">![Lync Server connecting PSTN gateway/IP-PBX diagram](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server connecting PSTN gateway/IP-PBX diagram")</span></span>

<span data-ttu-id="b6718-112">下图说明了连接两个 IP PBX 系统的 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="b6718-112">The next figure illustrates Lync Server 2013 connecting two IP-PBX systems.</span></span>

<span data-ttu-id="b6718-113">![Lync Server - 将 IP-PAX 系统相互连接的图示](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server - 将 IP-PAX 系统相互连接的图示")</span><span class="sxs-lookup"><span data-stu-id="b6718-113">![Lync Server interconnecting IP-PAX systems diagram](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server interconnecting IP-PAX systems diagram")</span></span>

<span data-ttu-id="b6718-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6718-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

