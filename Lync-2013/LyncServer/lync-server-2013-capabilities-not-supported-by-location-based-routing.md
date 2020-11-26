---
title: Lync Server 2013：基于位置的路由不支持的功能
description: Lync Server 2013： Location-Based 路由不支持的功能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435605"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a>Lync Server 2013 中基于位置的路由不支持的功能

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-03-12_

Location-Based 路由不适用于以下类型的交互。 当 Lync 终结点使用这些功能与 PSTN 终结点交互时，不会强制执行 Location-Based 路由。

  - PSTN 电话拨入式会议

  - 通过响应组的传入和传出 PSTN 呼叫

  - 通过呼叫寄存对 PSTN 呼叫进行呼叫寄存或检索

  - 到公告服务的传入 PSTN 呼叫

  - 通过组内呼叫应答检索的传入 PSTN 呼叫

若要对以下列表中的交互类型强制使用 Location-Based 路由规则，必须为会议启用 Location-Based 路由：

  - PSTN 电话拨出式会议

  - 从点对点音频对话升级到涉及 PSTN 终结点的音频会议

  - 涉及 PSTN 终结点的咨询转接

若要为会议启用 Location-Based 路由，请参阅 [Lync Server 2013 中的会议基于位置的路由](lync-server-2013-location-based-routing-for-conferencing.md)。

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中规划基于位置的路由](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

