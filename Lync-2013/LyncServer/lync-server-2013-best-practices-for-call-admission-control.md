---
title: Lync Server 2013：呼叫允许控制的最佳做法
description: Lync Server 2013：呼叫许可控制的最佳做法。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for call admission control
ms:assetid: 97173cca-8175-4ae2-a247-eb7ef809da93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398770(v=OCS.15)
ms:contentKeyID: 48184913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c32af904dc7fb48a1a5d1903bd6ed1f81f4cb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436067"
---
# <a name="best-practices-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="20cd1-103">Lync Server 2013 中呼叫允许控制的最佳做法</span><span class="sxs-lookup"><span data-stu-id="20cd1-103">Best practices for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20cd1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20cd1-104">

<span> </span></span></span>

<span data-ttu-id="20cd1-105">_**主题上次修改时间：** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="20cd1-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="20cd1-106">为了提高性能以及方便部署，在部署呼叫允许控制时，请应用以下最佳做法：</span><span class="sxs-lookup"><span data-stu-id="20cd1-106">To enhance performance and facilitate deployment, apply the following best practices when you deploy call admission control:</span></span>

  - <span data-ttu-id="20cd1-107">确保已为当前媒体流量和预期媒体流量提供了充足的 WAN。</span><span class="sxs-lookup"><span data-stu-id="20cd1-107">Ensure that WANs are adequately provisioned for current and anticipated media traffic.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="20cd1-p101">建议在设置带宽限制时预留一定的缓冲区。有些方案（如争用情况）会影响使用的带宽总量，可能导致出现超出带宽限制的情况。例如，当媒体流量接近带宽限制时，如果两个呼叫都尝试启动，则其中一个呼叫可能会因为另一个设法首先启动而被拒绝。</span><span class="sxs-lookup"><span data-stu-id="20cd1-p101">We recommend that you factor in a buffer to your bandwidth limits. There are scenarios such as race conditions that affect the total bandwidth used and can result in situations where the bandwidth limit is exceeded. For example, if two calls try to start while media traffic is approaching a bandwidth limit, one of them may be denied because the other managed to start first.</span></span>

    
    </div>

  - <span data-ttu-id="20cd1-111">监控网络使用情况以及呼叫详细信息记录，这样便可以根据网络使用情况的变化来选择最佳 CAC 设置并更新 CAC 设置。</span><span class="sxs-lookup"><span data-stu-id="20cd1-111">Monitor network usage and call detail records so that you can choose optimal CAC settings and update CAC settings as network usage changes.</span></span>

  - <span data-ttu-id="20cd1-112">使用 CAC 带宽策略补充 QoS 设置。</span><span class="sxs-lookup"><span data-stu-id="20cd1-112">Use CAC bandwidth policies to complement QoS settings.</span></span>

  - <span data-ttu-id="20cd1-113">如果要将已阻止的呼叫重新路由到 PSTN，请验证 PSTN 功能和容量。</span><span class="sxs-lookup"><span data-stu-id="20cd1-113">If you want to re-route blocked calls onto the PSTN, verify PSTN functionality and capacity.</span></span> <span data-ttu-id="20cd1-114">有关详细信息，请参阅 [在 Lync Server 2013 中规划出站语音路由](lync-server-2013-planning-outbound-voice-routing.md)。</span><span class="sxs-lookup"><span data-stu-id="20cd1-114">For details, see [Planning outbound voice routing in Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="20cd1-115">容量指为支持潜在 PSTN 重新路由而需要打开的端口数量。</span><span class="sxs-lookup"><span data-stu-id="20cd1-115">Capacity refers to the number of ports you need to open to support potential PSTN re-routing.</span></span>

    
    <span data-ttu-id="20cd1-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20cd1-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

