---
title: 从 Office Communications Server 2007 R2 迁移至 Lync Server 2013
description: 从 Office 通信服务器 2007 R2 迁移到 Lync Server 2013。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Office Communications Server 2007 R2 to Lync Server 2013
ms:assetid: f3fa4f5f-e9a2-4fb7-a12d-20f04173e697
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205375(v=OCS.15)
ms:contentKeyID: 48185802
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0afdc754ae691bc674c200addb9fb97c1eb4199
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446147"
---
# <a name="migration-from-office-communications-server-2007-r2-to-lync-server-2013"></a><span data-ttu-id="15f53-103">从 Office Communications Server 2007 R2 迁移至 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15f53-103">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15f53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15f53-104">

<span> </span></span></span>

<span data-ttu-id="15f53-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="15f53-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="15f53-106">本部分中的主题将指导你完成从 Office 通信服务器 2007 R2 迁移到 Lync Server 2013 的过程</span><span class="sxs-lookup"><span data-stu-id="15f53-106">The topics in this section guide you through the process of migrating from Office Communications Server 2007 R2 to Lync Server 2013</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="15f53-107">本文档介绍了完成迁移的每个阶段通常需要执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="15f53-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="15f53-108">它不能解决每个可能的旧部署拓扑或每种可能的迁移方案。</span><span class="sxs-lookup"><span data-stu-id="15f53-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="15f53-109">因此，你可能不需要执行所述的每个步骤，或者你可能需要执行其他步骤，具体取决于你的部署。</span><span class="sxs-lookup"><span data-stu-id="15f53-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="15f53-110">本文档还提供了验证步骤的示例。</span><span class="sxs-lookup"><span data-stu-id="15f53-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="15f53-111">提供这些验证步骤旨在帮助你了解需要查找的内容，以确保每个阶段在你的迁移过程中成功完成。</span><span class="sxs-lookup"><span data-stu-id="15f53-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="15f53-112">将这些验证步骤定制到特定迁移过程。</span><span class="sxs-lookup"><span data-stu-id="15f53-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="15f53-113">本指南提供有关升级现有部署的特定信息。</span><span class="sxs-lookup"><span data-stu-id="15f53-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="15f53-114">它不介绍如何更改现有拓扑。</span><span class="sxs-lookup"><span data-stu-id="15f53-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="15f53-115">本指南不介绍新功能的实现。</span><span class="sxs-lookup"><span data-stu-id="15f53-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="15f53-116">当详细过程记录在其他位置时，本指南将指导你使用相应的文档或文档部分。</span><span class="sxs-lookup"><span data-stu-id="15f53-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="15f53-117">此文档定义了下表中指定的术语。</span><span class="sxs-lookup"><span data-stu-id="15f53-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="15f53-118">*移植*</span><span class="sxs-lookup"><span data-stu-id="15f53-118">*migration*</span></span>  
    <span data-ttu-id="15f53-119">将生产部署从早期版本的 Office 通信服务器 2007 R2 迁移到 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="15f53-119">Moving your production deployment from a previous version of Office Communications Server 2007 R2 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="15f53-120">*升级*</span><span class="sxs-lookup"><span data-stu-id="15f53-120">*upgrade*</span></span>  
    <span data-ttu-id="15f53-121">在服务器或客户端计算机上安装较新版本的软件。</span><span class="sxs-lookup"><span data-stu-id="15f53-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="15f53-122">*既*</span><span class="sxs-lookup"><span data-stu-id="15f53-122">*coexistence*</span></span>  
    <span data-ttu-id="15f53-123">在迁移过程中，如果将某些功能迁移到 Lync Server 2013 且其他功能仍保留在以前版本的 Office 通信服务器 2007 R2 中，则迁移期间存在的临时环境。</span><span class="sxs-lookup"><span data-stu-id="15f53-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Office Communications Server 2007 R2.</span></span>

<!-- end list -->

  - <span data-ttu-id="15f53-124">*交互性*</span><span class="sxs-lookup"><span data-stu-id="15f53-124">*interoperability*</span></span>  
    <span data-ttu-id="15f53-125">部署在共存期间成功运行的能力。</span><span class="sxs-lookup"><span data-stu-id="15f53-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="15f53-126">本节内容</span><span class="sxs-lookup"><span data-stu-id="15f53-126">In This Section</span></span>

  - [<span data-ttu-id="15f53-127">开始迁移之前的准备工作</span><span class="sxs-lookup"><span data-stu-id="15f53-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="15f53-128">迁移阶段</span><span class="sxs-lookup"><span data-stu-id="15f53-128">Migration phases</span></span>](migration-phases.md)

  - [<span data-ttu-id="15f53-129">第1阶段：规划从 Office 通信服务器 2007 R2 迁移</span><span class="sxs-lookup"><span data-stu-id="15f53-129">Phase 1: Plan your migration from Office Communications Server 2007 R2</span></span>](phase-1-plan-your-migration-from-office-communications-server-2007-r2.md)

  - [<span data-ttu-id="15f53-130">第 2 阶段：准备迁移</span><span class="sxs-lookup"><span data-stu-id="15f53-130">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="15f53-131">第3阶段：部署 Lync Server 2013 试验池</span><span class="sxs-lookup"><span data-stu-id="15f53-131">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="15f53-132">第4阶段：合并拓扑</span><span class="sxs-lookup"><span data-stu-id="15f53-132">Phase 4: Merge topologies</span></span>](phase-4-merge-topologies.md)

  - [<span data-ttu-id="15f53-133">第5阶段：配置试行池</span><span class="sxs-lookup"><span data-stu-id="15f53-133">Phase 5: Configure the pilot pool</span></span>](phase-5-configure-the-pilot-pool.md)

  - [<span data-ttu-id="15f53-134">第6阶段：将用户移动到 "引导" 池</span><span class="sxs-lookup"><span data-stu-id="15f53-134">Phase 6: Move users to the pilot pool</span></span>](phase-6-move-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="15f53-135">第7阶段：将 Lync Server 2013 边缘服务器添加到试验池</span><span class="sxs-lookup"><span data-stu-id="15f53-135">Phase 7: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-7-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="15f53-136">第8阶段：从试验部署迁移到生产环境</span><span class="sxs-lookup"><span data-stu-id="15f53-136">Phase 8: Move from pilot deployment into production</span></span>](phase-8-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="15f53-137">第9阶段：完成迁移后任务</span><span class="sxs-lookup"><span data-stu-id="15f53-137">Phase 9: Complete post-migration tasks</span></span>](phase-9-complete-post-migration-tasks.md)

  - [<span data-ttu-id="15f53-138">第10阶段：停止旧版网站</span><span class="sxs-lookup"><span data-stu-id="15f53-138">Phase 10: Decommission legacy site</span></span>](phase-10-decommission-legacy-site.md)

<span data-ttu-id="15f53-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15f53-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

