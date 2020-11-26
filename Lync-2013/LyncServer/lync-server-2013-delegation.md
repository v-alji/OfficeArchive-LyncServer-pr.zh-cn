---
title: Lync Server 2013：委派
description: Lync Server 2013：委派。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430740"
---
# <a name="delegation-in-lync-server-2013"></a><span data-ttu-id="e5057-103">Lync Server 2013 中的委派</span><span class="sxs-lookup"><span data-stu-id="e5057-103">Delegation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5057-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5057-104">

<span> </span></span></span>

<span data-ttu-id="e5057-105">_**主题上次修改时间：** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="e5057-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="e5057-106">Lync 中的委派功能受以下方式 Location-Based 路由的影响：</span><span class="sxs-lookup"><span data-stu-id="e5057-106">The delegation capabilities in Lync are affected by Location-Based Routing in the following manner:</span></span>

  - <span data-ttu-id="e5057-107">当启用 Location-Based 路由的代理人代表经理呼叫时，代理人的语音政策将用于授权呼叫，代理人的网站语音路由策略将用于路由呼叫</span><span class="sxs-lookup"><span data-stu-id="e5057-107">When a delegate enabled for Location-Based Routing places a call on behalf of a manager, the delegate’s voice policy is used to authorize the call and the delegate’s site voice routing policy will be used to route the call</span></span>

  - <span data-ttu-id="e5057-108">对于打给经理的传入 PSTN 呼叫，适用于呼叫转接或同时响铃的相同规则将按照呼叫转接和同时响铃主题所述进行应用。</span><span class="sxs-lookup"><span data-stu-id="e5057-108">For incoming PSTN calls to a manager, the same rules applicable for call forwarding or simultaneously ringing will apply as described in the Call transfers and forwarding and Simultaneous ringing topics.</span></span>

  - <span data-ttu-id="e5057-109">当代理人将 PSTN 终结点设置为同时响铃目标时，对于打给经理的传入呼叫，与传入中继相关联的站点的语音路由策略将用于将呼叫路由到代理人的 PSTN 终结点。</span><span class="sxs-lookup"><span data-stu-id="e5057-109">When a delegate sets a PSTN endpoint as a simultaneous ring target, for an incoming call to the manager, the voice routing policy of the site that is associated to the incoming trunk will be used to route the call to the delegate’s PSTN endpoint.</span></span>

  - <span data-ttu-id="e5057-110">对于委派，通常建议经理及其关联的代理人位于相同网络站点中。</span><span class="sxs-lookup"><span data-stu-id="e5057-110">For delegation, it’s recommended that the manager and his associated delegates to be usually located in the same network site.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="e5057-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e5057-111">See Also</span></span>


[<span data-ttu-id="e5057-112">Lync Server 2013 中基于位置的路由的方案</span><span class="sxs-lookup"><span data-stu-id="e5057-112">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="e5057-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5057-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

