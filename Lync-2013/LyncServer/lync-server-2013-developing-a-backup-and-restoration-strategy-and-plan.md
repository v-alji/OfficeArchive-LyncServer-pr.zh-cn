---
title: Lync Server 2013：制定备份和还原策略及计划
description: Lync Server 2013：制定备份和还原策略及计划。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Developing a backup and restoration strategy and plan
ms:assetid: 17599b76-1a84-4dd6-b695-c19637deb8a6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202164(v=OCS.15)
ms:contentKeyID: 51541447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3d55eeb541cdde5c43d7d680ceb212d87da0d517
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429446"
---
# <a name="developing-a-backup-and-restoration-strategy-and-plan-for-lync-server-2013"></a><span data-ttu-id="6a069-103">开发 Lync Server 2013 的备份和还原策略和计划</span><span class="sxs-lookup"><span data-stu-id="6a069-103">Developing a backup and restoration strategy and plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a069-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a069-104">

<span> </span></span></span>

<span data-ttu-id="6a069-105">_**主题上次修改时间：** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="6a069-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="6a069-106">Lync Server 备份和还原操作的有效性取决于你的备份和还原策略以及计划。</span><span class="sxs-lookup"><span data-stu-id="6a069-106">The effectiveness of your Lync Server backup and restoration operations depends on your backup and restoration strategy and plan.</span></span> <span data-ttu-id="6a069-107">你应该建立一个用于备份和还原 Lync Server 的策略，该策略适用于你的组织的整体策略，以及用于备份数据和设置的全面、简明的计划，并且在发生中断时，是一种还原服务的计划。</span><span class="sxs-lookup"><span data-stu-id="6a069-107">You should establish a strategy for backing up and restoring Lync Server that fits with your organization's overall strategy, and a comprehensive, concise plan for backing up data and settings, and, in the event of an outage, a plan for restoring service.</span></span>

<span data-ttu-id="6a069-108">要获得最强健的前端池灾难恢复，请使用 Lync Server 2013 中引入的配对池灾难恢复拓扑。</span><span class="sxs-lookup"><span data-stu-id="6a069-108">For the most robust disaster recovery of a Front End Pool, use the paired-pool disaster recovery topology introduced in Lync Server 2013.</span></span> <span data-ttu-id="6a069-109">有关详细信息，请参阅 [在 Lync Server 2013 中规划高可用性和灾难恢复](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)。</span><span class="sxs-lookup"><span data-stu-id="6a069-109">For more information, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6a069-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="6a069-110">In This Section</span></span>

  - [<span data-ttu-id="6a069-111">为 Lync Server 2013 建立备份和还原策略</span><span class="sxs-lookup"><span data-stu-id="6a069-111">Establishing a backup and restoration strategy for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-strategy.md)

  - [<span data-ttu-id="6a069-112">为 Lync Server 2013 建立备份和还原计划</span><span class="sxs-lookup"><span data-stu-id="6a069-112">Establishing a backup and restoration plan for Lync Server 2013</span></span>](lync-server-2013-establishing-a-backup-and-restoration-plan.md)

  - [<span data-ttu-id="6a069-113">为 Lync Server 2013 设置备份位置</span><span class="sxs-lookup"><span data-stu-id="6a069-113">Setting up a backup location for Lync Server 2013</span></span>](lync-server-2013-setting-up-a-backup-location.md)

<span data-ttu-id="6a069-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a069-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

