---
title: Lync Server 2013 会议用户模型
description: Lync Server 2013 会议用户模型。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434276"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a><span data-ttu-id="3d77e-103">Lync Server 2013 中的会议用户模式</span><span class="sxs-lookup"><span data-stu-id="3d77e-103">The conferencing user model in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d77e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d77e-104">

<span> </span></span></span>

<span data-ttu-id="3d77e-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="3d77e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="3d77e-106">Lync Server 会议用户模式的一个关键部分是 "会议大小"。</span><span class="sxs-lookup"><span data-stu-id="3d77e-106">A critical part of the Lync Server conferencing user model is meeting size.</span></span> <span data-ttu-id="3d77e-107">从多个数据点收集数据后 () 上一节中所述），我们确定以下几点：</span><span class="sxs-lookup"><span data-stu-id="3d77e-107">After collecting data from the multiple data points (as described in the previous section), we determined the following:</span></span>

  - <span data-ttu-id="3d77e-108">大多数会议实际上是最小的协作式会议，平均有四个到六个参与者</span><span class="sxs-lookup"><span data-stu-id="3d77e-108">Most meetings are actually small collaborative meetings with an average of four to six participants</span></span>

  - <span data-ttu-id="3d77e-109">大约80% 的会议人数少于20位参与者。</span><span class="sxs-lookup"><span data-stu-id="3d77e-109">Approximately 80 percent of meetings have fewer than 20 participants.</span></span>

  - <span data-ttu-id="3d77e-110">99.98% 的会议的参与者数少于100。</span><span class="sxs-lookup"><span data-stu-id="3d77e-110">99.98 percent of meetings have fewer than 100 participants.</span></span>

<span data-ttu-id="3d77e-111">除了会议大小，会议用户模型还考虑各种因素，例如：</span><span class="sxs-lookup"><span data-stu-id="3d77e-111">In addition to meeting size, the conferencing user model also takes into account a variety of factors, such as:</span></span>

  - <span data-ttu-id="3d77e-112">**并发会议**   希望有多少个用户同时参与会议？</span><span class="sxs-lookup"><span data-stu-id="3d77e-112">**Concurrent meetings**   How many users are expected to be in meetings at the same time?</span></span>

  - <span data-ttu-id="3d77e-113">**媒体组合**   哪些类型的媒体可用且希望由会议中的用户使用？</span><span class="sxs-lookup"><span data-stu-id="3d77e-113">**Media mix**   What types of media are available and expected to be used by users in meetings?</span></span>

  - <span data-ttu-id="3d77e-114">**用户类型**   用户是内部用户、远程用户、联盟用户还是匿名用户？</span><span class="sxs-lookup"><span data-stu-id="3d77e-114">**User types**   Are users internal users, remote users, federated users, or anonymous users?</span></span>

  - <span data-ttu-id="3d77e-115">**会议提升时间**   会议的所有用户加入会议需要多长时间？</span><span class="sxs-lookup"><span data-stu-id="3d77e-115">**Meeting ramp up time**   How long does it take for all users of a meeting to join a meeting?</span></span>

<span data-ttu-id="3d77e-116">有关用户模型的详细信息，请参阅 [Lync Server 2013 中的用户模型](lync-server-2013-user-models.md)。</span><span class="sxs-lookup"><span data-stu-id="3d77e-116">For details about the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<span data-ttu-id="3d77e-117">若要确定用于测试的会议和用户数，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3d77e-117">To determine the number of meetings and users to use for testing, we did the following:</span></span>

  - <span data-ttu-id="3d77e-118">占用了组织中的总用户数 (例如，80000用户) 并乘以会议并发费率 (例如，5% 的 "所有用户") 确定在同一时间召开会议的总用户数 (在本示例中，4000用户) 。</span><span class="sxs-lookup"><span data-stu-id="3d77e-118">Took the total number of users in an organization (for example, 80,000 users) and multiplied it by the meeting concurrency rate (for example, 5% of all users) to determine the total number of users expected to be in meetings at the same time (in this example, 4000 users).</span></span>

  - <span data-ttu-id="3d77e-119">按部署 (中的 Lync Server 2013、前端服务器数划分的总用户数例如，8台服务器) 确定每个前端服务器的会议参与者预计数量 (在此示例中，每前端服务器的500用户) 。</span><span class="sxs-lookup"><span data-stu-id="3d77e-119">Divided the total number of users by the number of Lync Server 2013, Front End Servers in the deployment (for example, 8 servers) to determine the estimated number of meeting participants per Front End Server (in this example, 500 users per Front End Server).</span></span>

  - <span data-ttu-id="3d77e-120">按平均会议大小划分每个前端服务器的用户数 (例如，4个用户) 确定每个前端服务器的估计平均每前端服务器的平均数量 (本示例中，125每前端服务器) 的会议数。</span><span class="sxs-lookup"><span data-stu-id="3d77e-120">Divided the number of users per Front End Server by the average meeting size (for example, 4 users) to determine the estimated average number of meetings per Front End Server (in this example, 125 meetings per Front End Server).</span></span>

  - <span data-ttu-id="3d77e-121">为了在每个前端服务器上获取每个媒体负载，我们估计媒体混合。</span><span class="sxs-lookup"><span data-stu-id="3d77e-121">To get the per media load on each Front End Server, we estimated the media mix.</span></span> <span data-ttu-id="3d77e-122">例如，假设75% 的会议需要的不仅仅是音频支持和50% 的会议需要应用程序共享，则平均47会议和188用户同时连接到每个前端服务器以进行应用程序共享。</span><span class="sxs-lookup"><span data-stu-id="3d77e-122">For example, assuming that 75% of the meetings require more than just audio support and 50% of those meetings require application sharing, an average of 47 meetings and 188 users connect concurrently to each Front End Server for application sharing.</span></span>

  - <span data-ttu-id="3d77e-123">测试了各种会议大小 (基于在共享池中最多250用户的用户模型) 以确保服务器的可伸缩性。</span><span class="sxs-lookup"><span data-stu-id="3d77e-123">Tested a variety of meeting sizes (based our user model of up to 250 users in a shared pool) to ensure server scalability.</span></span>

<span data-ttu-id="3d77e-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d77e-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

