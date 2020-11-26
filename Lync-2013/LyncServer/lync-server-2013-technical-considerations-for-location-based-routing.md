---
title: Lync Server 2013：基于位置的路由的技术注意事项
description: Lync Server 2013： Location-Based 路由的技术注意事项。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical considerations for Location-Based Routing
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994027(v=OCS.15)
ms:contentKeyID: 51803936
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54a025af81ab148ad41f95d0a8cf4f900beb7e00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423426"
---
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="73f2b-103">Lync Server 2013 中基于位置的路由的技术注意事项</span><span class="sxs-lookup"><span data-stu-id="73f2b-103">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73f2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73f2b-104">

<span> </span></span></span>

<span data-ttu-id="73f2b-105">_**主题上次修改时间：** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="73f2b-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="73f2b-106">规划 Location-Based 路由时，应考虑对以下方案的影响。</span><span class="sxs-lookup"><span data-stu-id="73f2b-106">When planning Location-Based Routing, you should consider the impact to the following scenarios.</span></span>

<div>

## <a name="disaster-recovery"></a><span data-ttu-id="73f2b-107">灾难恢复</span><span class="sxs-lookup"><span data-stu-id="73f2b-107">Disaster Recovery</span></span>

<span data-ttu-id="73f2b-108">在从主池到备份池的故障转移以及将正常操作还原到主池的过程中，Location-Based 在灾难和恢复过程中始终强制执行路由。</span><span class="sxs-lookup"><span data-stu-id="73f2b-108">During a failover from the primary pool to a backup pool as well as when restoring normal operations to the primary pool, Location-Based Routing remains enforced at all times during a disaster and recovery procedure.</span></span>

</div>

<div>

## <a name="survivable-branch-appliance"></a><span data-ttu-id="73f2b-109">Survivable Branch Appliance</span><span class="sxs-lookup"><span data-stu-id="73f2b-109">Survivable Branch Appliance</span></span>

<span data-ttu-id="73f2b-110">配置 Location-Based 路由会影响你部署与 Survivable 分支装置关联的网关的计划。</span><span class="sxs-lookup"><span data-stu-id="73f2b-110">Configuring Location-Based Routing impacts the planning of where you deploy the gateways associated to your Survivable Branch Appliances.</span></span> <span data-ttu-id="73f2b-111">与你的 SBA 关联的网关必须与 Survivable 分支装置位于同一网络站点;否则，不允许驻留在 Survivable 分支设备上的用户在 Location-Based 路由配置的情况下发出出站呼叫。</span><span class="sxs-lookup"><span data-stu-id="73f2b-111">The gateway associated to your SBA must be located in the same network site as your Survivable Branch Appliance; otherwise, users homed on your Survivable Branch Appliance will not be permitted to place outbound calls if Location-Based Routing is configured.</span></span> <span data-ttu-id="73f2b-112">当 Survivable 分支设备和中心网站之间的 WAN 连接处于关闭状态时，Location-Based 路由限制将保持强制。</span><span class="sxs-lookup"><span data-stu-id="73f2b-112">When the WAN connection between your Survivable Branch Appliance and the central site is down, Location-Based Routing restrictions remains enforced.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="73f2b-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="73f2b-113">See Also</span></span>


[<span data-ttu-id="73f2b-114">在 Lync Server 2013 中规划基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="73f2b-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="73f2b-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73f2b-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

