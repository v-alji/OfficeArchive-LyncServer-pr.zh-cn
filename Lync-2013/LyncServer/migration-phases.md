---
title: 迁移阶段
description: 迁移阶段。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration phases
ms:assetid: cb7747ba-b872-42ca-ab41-76e3c4e77d06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205336(v=OCS.15)
ms:contentKeyID: 48185642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72ef47cb9b6c9eba75c395eb9bd94c887ca5a433
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443333"
---
# <a name="migration-phases"></a><span data-ttu-id="8e37e-103">迁移阶段</span><span class="sxs-lookup"><span data-stu-id="8e37e-103">Migration phases</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e37e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e37e-104">

<span> </span></span></span>

<span data-ttu-id="8e37e-105">_**主题上次修改时间：** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="8e37e-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="8e37e-106">在 Lync Server 2013 中，你可以在网络上定义包含 Lync Server 2013 组件的网站。</span><span class="sxs-lookup"><span data-stu-id="8e37e-106">In Lync Server 2013, you define sites on your network that contain Lync Server 2013 components.</span></span> <span data-ttu-id="8e37e-107">站点是一组计算机，这些计算机通过高速、低延迟网络连接，例如单个局域网 (局域网) 或通过高速光纤网络连接的两个网络。</span><span class="sxs-lookup"><span data-stu-id="8e37e-107">A site is a set of computers that are well-connected by a high-speed, low-latency network, such as a single local area network (LAN) or two networks connected by a high-speed fiber optic network.</span></span>

<span data-ttu-id="8e37e-108">*前端池* 是一组前端服务器，这些服务器配置相同，并且协同工作以提供一组通用用户的服务。</span><span class="sxs-lookup"><span data-stu-id="8e37e-108">A *Front End pool* is a set of Front End Servers that are configured identically and work together to provide services for a common group of users.</span></span> <span data-ttu-id="8e37e-109">池为你的用户提供了可伸缩性和故障转移功能。</span><span class="sxs-lookup"><span data-stu-id="8e37e-109">A pool provides scalability and failover capability to your users.</span></span> <span data-ttu-id="8e37e-110">池中的每台服务器必须运行一个或多个相同的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="8e37e-110">Each server in a pool must run an identical server role or roles.</span></span> <span data-ttu-id="8e37e-111">适用于小型组织的标准版服务器还定义了一个池并在单个服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="8e37e-111">A Standard Edition server, designed for small organizations, also defines a pool and runs on a single server.</span></span> <span data-ttu-id="8e37e-112">这使您能够以较低的成本获得 Lync Server 2013 功能，但不提供真正高可用性的解决方案。</span><span class="sxs-lookup"><span data-stu-id="8e37e-112">This enables you to have Lync Server 2013 functionality for a lesser cost, but does not provide a true high-availability solution.</span></span>

<span data-ttu-id="8e37e-113">以下阶段介绍从 Lync Server 2010 到 Lync Server 2013 的池迁移过程。</span><span class="sxs-lookup"><span data-stu-id="8e37e-113">The following phases describe the process of a pool migration from Lync Server 2010 to Lync Server 2013.</span></span> <span data-ttu-id="8e37e-114">对于包含多个池的多个网站，每个单独的池应遵循这种分段方法。</span><span class="sxs-lookup"><span data-stu-id="8e37e-114">For multiple sites containing multiple pools, each individual pool should follow this phased approach.</span></span>

1.  [<span data-ttu-id="8e37e-115">第1阶段：规划从 Lync Server 2010 的迁移</span><span class="sxs-lookup"><span data-stu-id="8e37e-115">Phase 1: Plan your migration from Lync Server 2010</span></span>](phase-1-plan-your-migration-from-lync-server-2010.md)

2.  [<span data-ttu-id="8e37e-116">第 2 阶段：准备迁移</span><span class="sxs-lookup"><span data-stu-id="8e37e-116">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

3.  [<span data-ttu-id="8e37e-117">第3阶段：部署 Lync Server 2013 试验池</span><span class="sxs-lookup"><span data-stu-id="8e37e-117">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

4.  [<span data-ttu-id="8e37e-118">第4阶段：将测试用户移动到试验池</span><span class="sxs-lookup"><span data-stu-id="8e37e-118">Phase 4: Move test users to the pilot pool</span></span>](phase-4-move-test-users-to-the-pilot-pool.md)

5.  [<span data-ttu-id="8e37e-119">第5阶段：将 Lync Server 2013 边缘服务器添加到试验池</span><span class="sxs-lookup"><span data-stu-id="8e37e-119">Phase 5: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-5-add-lync-server-2013-edge-server-to-pilot-pool.md)

6.  [<span data-ttu-id="8e37e-120">第 6 阶段：从试点部署移动到生产中</span><span class="sxs-lookup"><span data-stu-id="8e37e-120">Phase 6: Move from pilot deployment into production</span></span>](phase-6-move-from-pilot-deployment-into-production.md)

7.  [<span data-ttu-id="8e37e-121">第 7 阶段：完成迁移后任务</span><span class="sxs-lookup"><span data-stu-id="8e37e-121">Phase 7: Complete post-migration tasks</span></span>](phase-7-complete-post-migration-tasks.md)

8.  [<span data-ttu-id="8e37e-122">第 8 阶段：停用旧池</span><span class="sxs-lookup"><span data-stu-id="8e37e-122">Phase 8: Decommission legacy pools</span></span>](phase-8-decommission-legacy-pools.md)

<span data-ttu-id="8e37e-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e37e-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

