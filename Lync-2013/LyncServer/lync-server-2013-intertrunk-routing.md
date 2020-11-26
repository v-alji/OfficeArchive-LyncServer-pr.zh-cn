---
title: Lync Server 2013：中继间路由
description: Lync Server 2013： Intertrunk 路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Intertrunk routing
ms:assetid: d3a33b4a-8bf4-4a8c-a371-8ef79e740780
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205272(v=OCS.15)
ms:contentKeyID: 48185442
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 30c838ee94a2df0807195c172d7e2a3a393523af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426761"
---
# <a name="intertrunk-routing-in-lync-server-2013"></a><span data-ttu-id="6ee87-103">Lync Server 2013 中的中继间路由</span><span class="sxs-lookup"><span data-stu-id="6ee87-103">Intertrunk routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ee87-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ee87-104">

<span> </span></span></span>

<span data-ttu-id="6ee87-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="6ee87-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="6ee87-106">Lync Server 2013 可以将 IP PBX 互连到公共交换式电话网络 (PSTN) 网关，以便从 PBX 手机拨出的电话可以路由到 PSTN，并且可以将传入的 PSTN 呼叫路由到专用分支 exchange (PBX) 手机。</span><span class="sxs-lookup"><span data-stu-id="6ee87-106">Lync Server 2013 can interconnect an IP-PBX to a public switched telephone network (PSTN) gateway so that calls from a PBX phone can be routed to the PSTN, and incoming PSTN calls can be routed to a private branch exchange (PBX) phone.</span></span> <span data-ttu-id="6ee87-107">同样，Lync Server 2013 可以互连两个或更多的 IP PBX 系统，以便可以在不同的 IP PBX 系统中的 PBX 手机之间呼叫和接收呼叫。</span><span class="sxs-lookup"><span data-stu-id="6ee87-107">Similarly, Lync Server 2013 can interconnect two or more IP-PBX systems so that calls can be placed and received between PBX phones from the different IP-PBX systems.</span></span>

<span data-ttu-id="6ee87-108">此 intertrunk 路由功能可通过使用 Lync Server Management Shell cmdlet （ **new-cstrunkconfiguration**）以及新参数 PstnUsages 进行配置。</span><span class="sxs-lookup"><span data-stu-id="6ee87-108">This intertrunk routing feature can be configured by using the Lync Server Management Shell cmdlet, **Set-CsTrunkConfiguration**, with the new parameter, PstnUsages.</span></span> <span data-ttu-id="6ee87-109">此参数指定要使用的 PSTN 使用记录集。</span><span class="sxs-lookup"><span data-stu-id="6ee87-109">This parameter specifies the set of PSTN usage records to use.</span></span> <span data-ttu-id="6ee87-110">主干使用此 PSTN 用法确定路由并相应地路由所有传入呼叫。</span><span class="sxs-lookup"><span data-stu-id="6ee87-110">A trunk uses this PSTN usage to determine a route and to route all incoming calls accordingly.</span></span>

    Set-CsTrunkConfiguration -Identity <TrunkId> -PstnUsages @{add="<UsageString>"}

<span data-ttu-id="6ee87-111">下图说明了 Lync Server 2013 在 PSTN 网关和 IP PBX 之间提供 interconnectivity。</span><span class="sxs-lookup"><span data-stu-id="6ee87-111">The following diagram illustrates Lync Server 2013 providing interconnectivity between a PSTN gateway and an IP-PBX.</span></span>

<span data-ttu-id="6ee87-112">**网关和 IP PBX 之间的 Intertrunk 路由**</span><span class="sxs-lookup"><span data-stu-id="6ee87-112">**Intertrunk routing between gateway and IP PBX**</span></span>

<span data-ttu-id="6ee87-113">![Lync Server - 连接 PSTN 网关/IP-PBX 图示](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server - 连接 PSTN 网关/IP-PBX 图示")</span><span class="sxs-lookup"><span data-stu-id="6ee87-113">![Lync Server connecting PSTN gateway/IP-PBX diagram](images/JJ721940.cc3858ca-2ee3-4d51-8a51-db078366b50b(OCS.15).jpg "Lync Server connecting PSTN gateway/IP-PBX diagram")</span></span>

<span data-ttu-id="6ee87-114">下图说明了 Lync Server 2013 互连两个 IP PBX 系统的互连。</span><span class="sxs-lookup"><span data-stu-id="6ee87-114">The following diagram illustrates Lync Server 2013 interconnecting two IP-PBX systems.</span></span>

<span data-ttu-id="6ee87-115">**两个 IP Pbx 之间的 Intertrunk 路由**</span><span class="sxs-lookup"><span data-stu-id="6ee87-115">**Intertrunk routing between two IP PBXs**</span></span>

<span data-ttu-id="6ee87-116">![Lync Server - 将 IP-PAX 系统相互连接的图示](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server - 将 IP-PAX 系统相互连接的图示")</span><span class="sxs-lookup"><span data-stu-id="6ee87-116">![Lync Server interconnecting IP-PAX systems diagram](images/JJ721940.6ba18ec9-df70-498a-9cf7-7fc41e5ec432(OCS.15).jpg "Lync Server interconnecting IP-PAX systems diagram")</span></span>

<span data-ttu-id="6ee87-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ee87-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

