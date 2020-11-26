---
title: 从 Lync Server 2010 群聊或 Office Communications Server 2007 R2 群聊迁移到 Lync Server 2013 持久聊天服务器
description: 从 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013、持久聊天服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446855"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="3b49d-103">从 Lync Server 2010 群聊或 Office Communications Server 2007 R2 群聊迁移到 Lync Server 2013 持久聊天服务器</span><span class="sxs-lookup"><span data-stu-id="3b49d-103">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b49d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b49d-104">

<span> </span></span></span>

<span data-ttu-id="3b49d-105">_**主题上次修改时间：** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="3b49d-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="3b49d-106">本部分中的主题将指导你完成将 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013、持久聊天服务器的过程。</span><span class="sxs-lookup"><span data-stu-id="3b49d-106">The topics in this section guide you through the process of migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="3b49d-107">如果你打算使用 Lync server 2013、持久聊天服务器部署与 Lync Server 2010 共存，群组聊天或 Office 通信服务器 2007 R2 组聊天部署，本指南还包括一些必要的信息，可用于在此混合环境中操作。</span><span class="sxs-lookup"><span data-stu-id="3b49d-107">If you intend for your Lync Server 2013, Persistent Chat Server deployment to coexist with a Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat deployment, this guide also includes some essential information for operating in this mixed environment.</span></span> <span data-ttu-id="3b49d-108">本指南主要侧重于持久聊天服务器的数据迁移。</span><span class="sxs-lookup"><span data-stu-id="3b49d-108">This guide primarily focuses on data migration for Persistent Chat Server.</span></span> <span data-ttu-id="3b49d-109">对于从旧版 Lync Server 迁移到 Lync Server 2013 的用户，请参阅 [从 Lync server 2010 迁移到 Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) 和 [从 Office 通信服务器 2007 R2 迁移到 lync server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="3b49d-109">For users who are migrating from legacy versions of Lync Server to Lync Server 2013, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3b49d-110">本主题假定你已在与 Lync Server 2010 或 Office 通信服务器 2007 R2 共存的情况下安装了 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="3b49d-110">This topic assumes that you have already installed Lync Server 2013 in coexistence with Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3b49d-111">本指南介绍了完成迁移的每个阶段通常需要执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="3b49d-111">This guide describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="3b49d-112">它不能解决每个可能的旧部署拓扑或每种可能的迁移方案。</span><span class="sxs-lookup"><span data-stu-id="3b49d-112">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="3b49d-113">因此，你可能不需要执行所述的每个步骤，或者你可能需要执行其他步骤，具体取决于你的部署。</span><span class="sxs-lookup"><span data-stu-id="3b49d-113">Therefore, you may not need to perform every step that is described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="3b49d-114">本指南还提供了验证步骤的示例。</span><span class="sxs-lookup"><span data-stu-id="3b49d-114">The guide also provides examples of verification steps.</span></span> <span data-ttu-id="3b49d-115">提供这些验证步骤旨在帮助你了解需要查找的内容，以确保在你完成迁移过程中每个阶段成功完成。</span><span class="sxs-lookup"><span data-stu-id="3b49d-115">These verification steps are provided to help you understand what you need to look for to be sure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="3b49d-116">你可以将这些验证步骤修改为你的特定迁移过程。</span><span class="sxs-lookup"><span data-stu-id="3b49d-116">You can modify these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="3b49d-117">本指南提供有关升级现有部署的特定信息。</span><span class="sxs-lookup"><span data-stu-id="3b49d-117">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="3b49d-118">它不介绍如何更改现有拓扑。</span><span class="sxs-lookup"><span data-stu-id="3b49d-118">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="3b49d-119">本指南不介绍新功能的实现。</span><span class="sxs-lookup"><span data-stu-id="3b49d-119">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="3b49d-120">当详细过程记录在其他位置时，本指南将指导你使用相应的文档或文档部分。</span><span class="sxs-lookup"><span data-stu-id="3b49d-120">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="3b49d-121">此文档定义了下表中指定的术语。</span><span class="sxs-lookup"><span data-stu-id="3b49d-121">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="3b49d-122">*移植*</span><span class="sxs-lookup"><span data-stu-id="3b49d-122">*migration*</span></span>  
    <span data-ttu-id="3b49d-123">将部署从以前版本的持久聊天服务器（以前称为组聊天服务器）移动到 Lync Server 2013 持久聊天服务器。</span><span class="sxs-lookup"><span data-stu-id="3b49d-123">Moving your deployment from a previous version of Persistent Chat Server, formerly known as Group Chat Server, to Lync Server 2013, Persistent Chat Server.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b49d-124">*升级*</span><span class="sxs-lookup"><span data-stu-id="3b49d-124">*upgrade*</span></span>  
    <span data-ttu-id="3b49d-125">在服务器或客户端计算机上安装较新版本的软件。</span><span class="sxs-lookup"><span data-stu-id="3b49d-125">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b49d-126">*既*</span><span class="sxs-lookup"><span data-stu-id="3b49d-126">*coexistence*</span></span>  
    <span data-ttu-id="3b49d-127">在迁移过程中，当某些功能已迁移到 Lync Server 2013、持久聊天服务器以及其他功能的临时环境仍然保留在早期版本的组聊天服务器上时。</span><span class="sxs-lookup"><span data-stu-id="3b49d-127">The temporary environment that exists during migration, when some functionality has been migrated to Lync Server 2013, Persistent Chat Server, and other functionality still remains on a prior version of Group Chat Server.</span></span>

<span data-ttu-id="3b49d-128">持久聊天服务器是 Lync Server 2013 基础结构的扩展。</span><span class="sxs-lookup"><span data-stu-id="3b49d-128">Persistent Chat Server is an extension of the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="3b49d-129">根据你的拓扑，你可以将 Lync Server 2010、群组聊天或 Office 通信服务器 2007 R2 组聊天迁移到 Lync Server 2013 持久聊天服务器。</span><span class="sxs-lookup"><span data-stu-id="3b49d-129">Depending on your topology, you can migrate Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="3b49d-130">有关可用拓扑和迁移群组聊天服务器的技术和软件要求的详细信息，请参阅规划文档中的在 [Lync server 2013 中规划持久聊天服务器](lync-server-2013-planning-for-persistent-chat-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="3b49d-130">For details about available topologies and the technical and software requirements for migrating Group Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="3b49d-131">如果您的组织要求合规性支持，则它现在会自动随每个持久聊天服务器一起安装。</span><span class="sxs-lookup"><span data-stu-id="3b49d-131">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="3b49d-132">不再需要一个单独的服务器来实现合规性。</span><span class="sxs-lookup"><span data-stu-id="3b49d-132">A separate server is no longer needed for compliance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3b49d-133">持久聊天服务器必须安装在 NTFS 文件系统上才能帮助强制实施文件系统安全。</span><span class="sxs-lookup"><span data-stu-id="3b49d-133">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="3b49d-134">FAT32 不是持久聊天服务器支持的文件系统。</span><span class="sxs-lookup"><span data-stu-id="3b49d-134">FAT32 is not a supported file system for Persistent Chat Server.</span></span><BR><span data-ttu-id="3b49d-135">如果您的组织要求合规性支持，则它现在会自动随每个持久聊天服务器一起安装。</span><span class="sxs-lookup"><span data-stu-id="3b49d-135">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="3b49d-136">不再需要一个单独的服务器来实现合规性。</span><span class="sxs-lookup"><span data-stu-id="3b49d-136">A separate server is no longer needed for compliance.</span></span> <span data-ttu-id="3b49d-137">有关 Lync Server 2013 持久聊天服务器中的更改的更多详细信息 &nbsp; ，请参阅入门文档中 <A href="lync-server-2013-new-persistent-chat-server-features.md">Lync server 2013 中的新持久聊天服务器功能</A> 。</span><span class="sxs-lookup"><span data-stu-id="3b49d-137">For more details about changes in Lync Server 2013&nbsp;Persistent Chat Server, see <A href="lync-server-2013-new-persistent-chat-server-features.md">New Persistent Chat Server features in Lync Server 2013</A> in the Getting Started documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3b49d-138">本节内容</span><span class="sxs-lookup"><span data-stu-id="3b49d-138">In This Section</span></span>

  - [<span data-ttu-id="3b49d-139">标准迁移方案 - 高级别</span><span class="sxs-lookup"><span data-stu-id="3b49d-139">Standard migration scenario - high-level</span></span>](standard-migration-scenario-high-level.md)

  - [<span data-ttu-id="3b49d-140">迁移过程 - 详细信息</span><span class="sxs-lookup"><span data-stu-id="3b49d-140">Migration process - details</span></span>](migration-process-details.md)

  - [<span data-ttu-id="3b49d-141">共存注意事项</span><span class="sxs-lookup"><span data-stu-id="3b49d-141">Coexistence considerations</span></span>](coexistence-considerations.md)

<span data-ttu-id="3b49d-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b49d-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

