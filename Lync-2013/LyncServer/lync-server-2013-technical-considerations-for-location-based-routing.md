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
# <a name="technical-considerations-for-location-based-routing-in-lync-server-2013"></a>Lync Server 2013 中基于位置的路由的技术注意事项

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-03-09_

规划 Location-Based 路由时，应考虑对以下方案的影响。

<div>

## <a name="disaster-recovery"></a>灾难恢复

在从主池到备份池的故障转移以及将正常操作还原到主池的过程中，Location-Based 在灾难和恢复过程中始终强制执行路由。

</div>

<div>

## <a name="survivable-branch-appliance"></a>Survivable Branch Appliance

配置 Location-Based 路由会影响你部署与 Survivable 分支装置关联的网关的计划。 与你的 SBA 关联的网关必须与 Survivable 分支装置位于同一网络站点;否则，不允许驻留在 Survivable 分支设备上的用户在 Location-Based 路由配置的情况下发出出站呼叫。 当 Survivable 分支设备和中心网站之间的 WAN 连接处于关闭状态时，Location-Based 路由限制将保持强制。

</div>

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中规划基于位置的路由](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

