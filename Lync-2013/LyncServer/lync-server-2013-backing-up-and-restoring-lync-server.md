---
title: Lync Server 2013：备份和还原 Lync 服务器
description: Lync Server 2013：备份和还原 Lync 服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up and restoring Lync Server 2013
ms:assetid: 07dc1f5e-af66-4e18-bf39-881dceff8bc3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202160(v=OCS.15)
ms:contentKeyID: 51541443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1a7024b2264fb895d1562a6da0775f9397644b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438139"
---
# <a name="backing-up-and-restoring-lync-server-2013"></a><span data-ttu-id="7e43c-103">备份和还原 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7e43c-103">Backing up and restoring Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7e43c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7e43c-104">

<span> </span></span></span>

<span data-ttu-id="7e43c-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="7e43c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="7e43c-106">在本部分中，你将找到备份 Lync Server 2013 数据的最佳做法，以及在遇到故障时还原它的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="7e43c-106">In this section, you’ll find the best practices for backing up your Lync Server 2013 data, and for restoring it if you have a failure.</span></span> <span data-ttu-id="7e43c-107">这些最佳做法适用于以下情况：</span><span class="sxs-lookup"><span data-stu-id="7e43c-107">These best practices apply to the following situations:</span></span>

  - <span data-ttu-id="7e43c-108">任何类型 (前端服务器、边缘服务器、中介服务器、持久聊天服务器或控制器) 的整个 Lync Server 池，或者其中一个池中的单个服务器。</span><span class="sxs-lookup"><span data-stu-id="7e43c-108">An entire Lync Server pool of any type (Front End Server, Edge Server, Mediation Server, Persistent Chat Server, or Director), or an individual server in one of these pools.</span></span>

  - <span data-ttu-id="7e43c-109">中央管理服务器</span><span class="sxs-lookup"><span data-stu-id="7e43c-109">The Central Management Server</span></span>

  - <span data-ttu-id="7e43c-110">标准版服务器</span><span class="sxs-lookup"><span data-stu-id="7e43c-110">A Standard Edition server</span></span>

  - <span data-ttu-id="7e43c-111">企业版后端服务器</span><span class="sxs-lookup"><span data-stu-id="7e43c-111">An Enterprise Edition Back End Server</span></span>

  - <span data-ttu-id="7e43c-112">文件存储</span><span class="sxs-lookup"><span data-stu-id="7e43c-112">A File Store</span></span>

  - <span data-ttu-id="7e43c-113">存档数据库、监视数据库或持久聊天数据库</span><span class="sxs-lookup"><span data-stu-id="7e43c-113">An Archiving database, Monitoring database, or Persistent Chat database</span></span>

<span data-ttu-id="7e43c-114">本部分不包括有关还原整个网站或开发备用网站的信息。</span><span class="sxs-lookup"><span data-stu-id="7e43c-114">This section does not include information about restoring an entire site or for developing a standby site.</span></span> <span data-ttu-id="7e43c-115">有关使用配对的前端池开发灾难恢复解决方案的详细信息，请参阅 [在 Lync Server 2013 中规划高可用性和灾难恢复](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)。</span><span class="sxs-lookup"><span data-stu-id="7e43c-115">For details about developing a disaster recovery solution with paired Front End pools, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="7e43c-116">这是规划灾难恢复的推荐方法。</span><span class="sxs-lookup"><span data-stu-id="7e43c-116">This is the recommended method for planning for disaster recovery.</span></span>

<span data-ttu-id="7e43c-117">如果你已部署成对的前端池，并且其中一个池失败，并且无法恢复，则可以使用新的完全限定的域名（ (FQDN) 与其配对的池中）还原此池。</span><span class="sxs-lookup"><span data-stu-id="7e43c-117">If you have deployed paired Front End pools, if one of these pools fails and becomes unrecoverable, you can restore this pool with a new fully qualified domain name (FQDN) from its paired pool.</span></span> <span data-ttu-id="7e43c-118">有关执行此恢复的步骤的详细信息，请参阅 [在 Lync Server 2013 中故障转移池](lync-server-2013-failing-over-a-pool.md)。</span><span class="sxs-lookup"><span data-stu-id="7e43c-118">For details on the steps to perform this recovery, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="7e43c-119">此外，如果你稍后想要重新创建属于前端对的失败和不可恢复的池，你可以使用在 [Lync Server 2013 中执行 ABC 前端池故障转移](lync-server-2013-performing-an-abc-front-end-pool-failover.md)的步骤。</span><span class="sxs-lookup"><span data-stu-id="7e43c-119">Additionally, if you later want to recreate a failed and unrecoverable pool that was part of a Front End pair, you can use the steps in [Performing an ABC Front End pool failover in Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span></span>

<span data-ttu-id="7e43c-120">本文档中所述的方法涉及规划阶段中的特殊注意事项。</span><span class="sxs-lookup"><span data-stu-id="7e43c-120">The methodology described in this document involves special considerations during the planning phase.</span></span> <span data-ttu-id="7e43c-121">有关详细信息，请参阅为 [Lync Server 2013 建立备份和还原计划](lync-server-2013-establishing-a-backup-and-restoration-plan.md)。</span><span class="sxs-lookup"><span data-stu-id="7e43c-121">For details, see [Establishing a backup and restoration plan for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7e43c-122">本节内容</span><span class="sxs-lookup"><span data-stu-id="7e43c-122">In This Section</span></span>

  - [<span data-ttu-id="7e43c-123">准备 Lync Server 2013 备份和还原</span><span class="sxs-lookup"><span data-stu-id="7e43c-123">Preparing for Lync Server 2013 backup and restoration</span></span>](lync-server-2013-preparing-for-lync-server-backup-and-restoration.md)

  - [<span data-ttu-id="7e43c-124">在 Lync Server 2013 中备份数据和设置</span><span class="sxs-lookup"><span data-stu-id="7e43c-124">Backing up data and settings in Lync Server 2013</span></span>](lync-server-2013-backing-up-data-and-settings.md)

  - [<span data-ttu-id="7e43c-125">在 Lync Server 2013 中还原数据和设置</span><span class="sxs-lookup"><span data-stu-id="7e43c-125">Restoring data and settings in Lync Server 2013</span></span>](lync-server-2013-restoring-data-and-settings.md)

  - [<span data-ttu-id="7e43c-126">Lync Server 2013 的备份和还原工作表</span><span class="sxs-lookup"><span data-stu-id="7e43c-126">Backup and restoration worksheets for Lync Server 2013</span></span>](lync-server-2013-backup-and-restoration-worksheets.md)

<span data-ttu-id="7e43c-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7e43c-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

