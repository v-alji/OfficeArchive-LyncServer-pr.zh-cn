---
title: Lync Server 2013：规划企业语音
description: Lync Server 2013：规划企业语音。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Enterprise Voice
ms:assetid: fd8d5867-0ac9-47f8-94f0-1c3ee5e25575
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413081(v=OCS.15)
ms:contentKeyID: 48185959
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4dfa0d91fe8270e49524d648ef403cd69ede2407
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424581"
---
# <a name="planning-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="a63e5-103">在 Lync Server 2013 中规划企业语音</span><span class="sxs-lookup"><span data-stu-id="a63e5-103">Planning for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a63e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a63e5-104">

<span> </span></span></span>

<span data-ttu-id="a63e5-105">_**主题上次修改时间：** 2013-11-01_</span><span class="sxs-lookup"><span data-stu-id="a63e5-105">_**Topic Last Modified:** 2013-11-01_</span></span>

<span data-ttu-id="a63e5-106">企业语音的部署过程取决于你的现有拓扑、基础结构和你希望支持的企业语音功能。</span><span class="sxs-lookup"><span data-stu-id="a63e5-106">The deployment process for Enterprise Voice depends on your existing topology, infrastructure, and the Enterprise Voice functionality that you want to support.</span></span> <span data-ttu-id="a63e5-107">所需过程将取决于您选择的功能，但还有另一些规划注意事项需要您重点关注。</span><span class="sxs-lookup"><span data-stu-id="a63e5-107">The required procedures will depend on what features you choose, but there are other planning considerations that you must make at a high level.</span></span>

<span data-ttu-id="a63e5-108">一般情况下，请考虑要部署的网站的类型和数量、其地理位置、每个网站上的调用卷、连接网站的网络链接的类型、是否要为每个网站提供针对语音功能的冗余和故障转移，以及是否希望使用现有的 PBX 设备。</span><span class="sxs-lookup"><span data-stu-id="a63e5-108">In general, consider the type and number of sites that you want to deploy and their geographical locations, the call volume at each site, the types of network links that connect sites, whether you want to provide redundancy and failover for voice functionality for each site, and whether you want to use existing PBX equipment.</span></span> <span data-ttu-id="a63e5-109">在规划 Lync Server 通信软件的整体时，应考虑以下一些事项（如高可用性）。</span><span class="sxs-lookup"><span data-stu-id="a63e5-109">There are certain considerations, such as high availability, that you should consider when you plan for Lync Server  communications software as a whole.</span></span> <span data-ttu-id="a63e5-110">这些注意事项将根据需要在本部分中的主题中进行讨论。</span><span class="sxs-lookup"><span data-stu-id="a63e5-110">These considerations are discussed in topics throughout this section, as needed.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="a63e5-111">规划注意事项</span><span class="sxs-lookup"><span data-stu-id="a63e5-111">Planning Considerations</span></span>

<span data-ttu-id="a63e5-112">有关特定企业语音功能或组件部署的计划决策，请参阅本部分中的主题。</span><span class="sxs-lookup"><span data-stu-id="a63e5-112">For planning decisions that pertain to the deployment of a particular Enterprise Voice capability or deployment scenario or component, consult the topics in this section.</span></span>

  - [<span data-ttu-id="a63e5-113">在 Lync Server 2013 中定义企业语音要求</span><span class="sxs-lookup"><span data-stu-id="a63e5-113">Defining your requirements for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-enterprise-voice.md)

  - [<span data-ttu-id="a63e5-114">估计 Lync Server 2013 的语音使用和流量</span><span class="sxs-lookup"><span data-stu-id="a63e5-114">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="a63e5-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a63e5-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md)

  - [<span data-ttu-id="a63e5-116">Components required for Enterprise Voice in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a63e5-116">Components required for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-components-required-for-enterprise-voice.md)

  - [<span data-ttu-id="a63e5-117">在 Lync Server 2013 中规划企业语音恢复能力</span><span class="sxs-lookup"><span data-stu-id="a63e5-117">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="a63e5-118">在 Lync Server 2013 中规划 Exchange 统一消息集成</span><span class="sxs-lookup"><span data-stu-id="a63e5-118">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-planning-for-exchange-unified-messaging-integration.md)

  - [<span data-ttu-id="a63e5-119">在 Lync Server 2013 中规划呼叫允许控制</span><span class="sxs-lookup"><span data-stu-id="a63e5-119">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="a63e5-120">在 Lync Server 2013 中规划紧急服务 (E9-1-1)</span><span class="sxs-lookup"><span data-stu-id="a63e5-120">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="a63e5-121">在 Lync Server 2013 中规划媒体旁路</span><span class="sxs-lookup"><span data-stu-id="a63e5-121">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

  - [<span data-ttu-id="a63e5-122">在 Lync Server 2013 中规划私人电话线路</span><span class="sxs-lookup"><span data-stu-id="a63e5-122">Planning for private telephone lines with Lync Server 2013</span></span>](lync-server-2013-planning-for-private-telephone-lines.md)

  - [<span data-ttu-id="a63e5-123">在 Lync Server 2013 中规划基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="a63e5-123">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)

  - [<span data-ttu-id="a63e5-124">在 Lync Server 2013 中规划企业语音恢复能力</span><span class="sxs-lookup"><span data-stu-id="a63e5-124">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="a63e5-125">Lync Server 2013 中的企业语音部署准则</span><span class="sxs-lookup"><span data-stu-id="a63e5-125">Deployment guidelines for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-enterprise-voice.md)

  - [<span data-ttu-id="a63e5-126">Lync Server 2013 中的企业语音部署过程概述</span><span class="sxs-lookup"><span data-stu-id="a63e5-126">Deployment process overview for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-process-overview-for-enterprise-voice.md)

  - [<span data-ttu-id="a63e5-127">在 Lync Server 2013 中将用户迁移至企业语音</span><span class="sxs-lookup"><span data-stu-id="a63e5-127">Moving users to Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-moving-users-to-enterprise-voice.md)

  - [<span data-ttu-id="a63e5-128">Lync Server 2013 中的 lync PreCall 诊断工具</span><span class="sxs-lookup"><span data-stu-id="a63e5-128">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>](lync-server-2013-lync-precall-diagnostics-tool.md)

<span data-ttu-id="a63e5-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a63e5-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

