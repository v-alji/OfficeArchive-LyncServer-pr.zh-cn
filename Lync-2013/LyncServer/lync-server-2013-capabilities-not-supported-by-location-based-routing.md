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
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="76bfd-103">Lync Server 2013 中基于位置的路由不支持的功能</span><span class="sxs-lookup"><span data-stu-id="76bfd-103">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76bfd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76bfd-104">

<span> </span></span></span>

<span data-ttu-id="76bfd-105">_**主题上次修改时间：** 2014-03-12_</span><span class="sxs-lookup"><span data-stu-id="76bfd-105">_**Topic Last Modified:** 2014-03-12_</span></span>

<span data-ttu-id="76bfd-106">Location-Based 路由不适用于以下类型的交互。</span><span class="sxs-lookup"><span data-stu-id="76bfd-106">Location-Based Routing does not apply to the following types of interactions.</span></span> <span data-ttu-id="76bfd-107">当 Lync 终结点使用这些功能与 PSTN 终结点交互时，不会强制执行 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="76bfd-107">Location-Based Routing is not enforced when Lync endpoints interact with PSTN endpoints using these capabilities.</span></span>

  - <span data-ttu-id="76bfd-108">PSTN 电话拨入式会议</span><span class="sxs-lookup"><span data-stu-id="76bfd-108">PSTN dial-in to conferences</span></span>

  - <span data-ttu-id="76bfd-109">通过响应组的传入和传出 PSTN 呼叫</span><span class="sxs-lookup"><span data-stu-id="76bfd-109">Incoming and outgoing PSTN calls through Response Group</span></span>

  - <span data-ttu-id="76bfd-110">通过呼叫寄存对 PSTN 呼叫进行呼叫寄存或检索</span><span class="sxs-lookup"><span data-stu-id="76bfd-110">Call park or retrieval of PSTN calls through Call Park</span></span>

  - <span data-ttu-id="76bfd-111">到公告服务的传入 PSTN 呼叫</span><span class="sxs-lookup"><span data-stu-id="76bfd-111">Incoming PSTN calls to Announcement Service</span></span>

  - <span data-ttu-id="76bfd-112">通过组内呼叫应答检索的传入 PSTN 呼叫</span><span class="sxs-lookup"><span data-stu-id="76bfd-112">Incoming PSTN calls retrieved via Group Call Pickup</span></span>

<span data-ttu-id="76bfd-113">若要对以下列表中的交互类型强制使用 Location-Based 路由规则，必须为会议启用 Location-Based 路由：</span><span class="sxs-lookup"><span data-stu-id="76bfd-113">To enforce Location-Based Routing rules to the types of interactions in the following list, you must enable Location-Based Routing for Conferencing:</span></span>

  - <span data-ttu-id="76bfd-114">PSTN 电话拨出式会议</span><span class="sxs-lookup"><span data-stu-id="76bfd-114">PSTN dial-out from conferences</span></span>

  - <span data-ttu-id="76bfd-115">从点对点音频对话升级到涉及 PSTN 终结点的音频会议</span><span class="sxs-lookup"><span data-stu-id="76bfd-115">Escalations from peer-to-peer audio conversations to conferencing involving PSTN endpoints</span></span>

  - <span data-ttu-id="76bfd-116">涉及 PSTN 终结点的咨询转接</span><span class="sxs-lookup"><span data-stu-id="76bfd-116">Consultative transfers involving PSTN endpoints</span></span>

<span data-ttu-id="76bfd-117">若要为会议启用 Location-Based 路由，请参阅 [Lync Server 2013 中的会议基于位置的路由](lync-server-2013-location-based-routing-for-conferencing.md)。</span><span class="sxs-lookup"><span data-stu-id="76bfd-117">To enable Location-Based Routing for Conferencing, see [Location-Based Routing for conferencing in Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="76bfd-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="76bfd-118">See Also</span></span>


[<span data-ttu-id="76bfd-119">在 Lync Server 2013 中规划基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="76bfd-119">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="76bfd-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76bfd-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

