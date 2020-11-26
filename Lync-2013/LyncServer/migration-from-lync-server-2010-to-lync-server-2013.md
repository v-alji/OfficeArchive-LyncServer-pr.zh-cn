---
title: 从 Lync Server 2010 迁移到 Lync Server 2013
description: 从 Lync Server 2010 迁移到 Lync Server 2013。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010 to Lync Server 2013
ms:assetid: ef99d4a9-a666-4a92-9994-4d7930f70d55
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205369(v=OCS.15)
ms:contentKeyID: 48185779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbe1bc1b7745c5ddc89a7f8fb64295a82f52c9bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438594"
---
# <a name="migration-from-lync-server-2010-to-lync-server-2013"></a><span data-ttu-id="67c42-103">从 Lync Server 2010 迁移到 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67c42-103">Migration from Lync Server 2010 to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67c42-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67c42-104">

<span> </span></span></span>

<span data-ttu-id="67c42-105">_**主题上次修改时间：** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="67c42-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="67c42-106">本部分中的主题将指导你完成从 Lync Server 2010 迁移到 Lync Server 2013 的过程。</span><span class="sxs-lookup"><span data-stu-id="67c42-106">The topics in this section guide you through the process of migrating from Lync Server 2010 to Lync Server 2013.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="67c42-107">本文档介绍了完成迁移的每个阶段通常需要执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="67c42-107">This document describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="67c42-108">它不能解决每个可能的旧部署拓扑或每种可能的迁移方案。</span><span class="sxs-lookup"><span data-stu-id="67c42-108">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="67c42-109">因此，你可能不需要执行所述的每个步骤，或者你可能需要执行其他步骤，具体取决于你的部署。</span><span class="sxs-lookup"><span data-stu-id="67c42-109">Therefore, you may not need to perform every step described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="67c42-110">本文档还提供了验证步骤的示例。</span><span class="sxs-lookup"><span data-stu-id="67c42-110">This document also provides examples of verification steps.</span></span> <span data-ttu-id="67c42-111">提供这些验证步骤旨在帮助你了解需要查找的内容，以确保每个阶段在你的迁移过程中成功完成。</span><span class="sxs-lookup"><span data-stu-id="67c42-111">These verification steps are provided to help you understand what you need to look for to ensure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="67c42-112">将这些验证步骤定制到特定迁移过程。</span><span class="sxs-lookup"><span data-stu-id="67c42-112">Tailor these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="67c42-113">本指南提供有关升级现有部署的特定信息。</span><span class="sxs-lookup"><span data-stu-id="67c42-113">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="67c42-114">它不介绍如何更改现有拓扑。</span><span class="sxs-lookup"><span data-stu-id="67c42-114">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="67c42-115">本指南不介绍新功能的实现。</span><span class="sxs-lookup"><span data-stu-id="67c42-115">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="67c42-116">当详细过程记录在其他位置时，本指南将指导你使用相应的文档或文档部分。</span><span class="sxs-lookup"><span data-stu-id="67c42-116">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="67c42-117">此文档定义了下表中指定的术语。</span><span class="sxs-lookup"><span data-stu-id="67c42-117">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="67c42-118">*移植*</span><span class="sxs-lookup"><span data-stu-id="67c42-118">*migration*</span></span>  
    <span data-ttu-id="67c42-119">将生产部署从以前版本的 Lync Server 2010 移动到 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="67c42-119">Moving your production deployment from a previous version of Lync Server 2010 to Lync Server 2013.</span></span>

<!-- end list -->

  - <span data-ttu-id="67c42-120">*升级*</span><span class="sxs-lookup"><span data-stu-id="67c42-120">*upgrade*</span></span>  
    <span data-ttu-id="67c42-121">在服务器或客户端计算机上安装较新版本的软件。</span><span class="sxs-lookup"><span data-stu-id="67c42-121">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="67c42-122">*既*</span><span class="sxs-lookup"><span data-stu-id="67c42-122">*coexistence*</span></span>  
    <span data-ttu-id="67c42-123">在迁移过程中，如果将某些功能迁移到 Lync Server 2013 且其他功能仍保留在以前版本的 Lync Server 2010 中，则在迁移期间存在的临时环境。</span><span class="sxs-lookup"><span data-stu-id="67c42-123">The temporary environment that exists during migration when some functionality has been migrated to Lync Server 2013 and other functionality still remains on a prior version of Lync Server 2010.</span></span>

<!-- end list -->

  - <span data-ttu-id="67c42-124">*交互性*</span><span class="sxs-lookup"><span data-stu-id="67c42-124">*interoperability*</span></span>  
    <span data-ttu-id="67c42-125">部署在共存期间成功运行的能力。</span><span class="sxs-lookup"><span data-stu-id="67c42-125">The ability of your deployment to operate successfully during the period of coexistence.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="67c42-126">本节内容</span><span class="sxs-lookup"><span data-stu-id="67c42-126">In This Section</span></span>

  - [<span data-ttu-id="67c42-127">开始迁移之前的准备工作</span><span class="sxs-lookup"><span data-stu-id="67c42-127">Before you begin the migration</span></span>](before-you-begin-the-migration.md)

  - [<span data-ttu-id="67c42-128">第1阶段：规划从 Lync Server 2010 的迁移</span><span class="sxs-lookup"><span data-stu-id="67c42-128">Phase 1: Plan your migration from Lync Server 2010</span></span>](phase-1-plan-your-migration-from-lync-server-2010.md)

  - [<span data-ttu-id="67c42-129">第 2 阶段：准备迁移</span><span class="sxs-lookup"><span data-stu-id="67c42-129">Phase 2: Prepare for migration</span></span>](phase-2-prepare-for-migration.md)

  - [<span data-ttu-id="67c42-130">第3阶段：部署 Lync Server 2013 试验池</span><span class="sxs-lookup"><span data-stu-id="67c42-130">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>](phase-3-deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="67c42-131">第4阶段：将测试用户移动到试验池</span><span class="sxs-lookup"><span data-stu-id="67c42-131">Phase 4: Move test users to the pilot pool</span></span>](phase-4-move-test-users-to-the-pilot-pool.md)

  - [<span data-ttu-id="67c42-132">第5阶段：将 Lync Server 2013 边缘服务器添加到试验池</span><span class="sxs-lookup"><span data-stu-id="67c42-132">Phase 5: Add Lync Server 2013 Edge Server to pilot pool</span></span>](phase-5-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [<span data-ttu-id="67c42-133">第 6 阶段：从试点部署移动到生产中</span><span class="sxs-lookup"><span data-stu-id="67c42-133">Phase 6: Move from pilot deployment into production</span></span>](phase-6-move-from-pilot-deployment-into-production.md)

  - [<span data-ttu-id="67c42-134">第 7 阶段：完成迁移后任务</span><span class="sxs-lookup"><span data-stu-id="67c42-134">Phase 7: Complete post-migration tasks</span></span>](phase-7-complete-post-migration-tasks.md)

  - [<span data-ttu-id="67c42-135">第 8 阶段：停用旧池</span><span class="sxs-lookup"><span data-stu-id="67c42-135">Phase 8: Decommission legacy pools</span></span>](phase-8-decommission-legacy-pools.md)

<span data-ttu-id="67c42-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67c42-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

