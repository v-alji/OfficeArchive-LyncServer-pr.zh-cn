---
title: Lync Server 2013：建立备份和还原策略
description: Lync Server 2013：建立备份和还原策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration strategy
ms:assetid: f545a75f-bbc4-4968-b510-8f6f3920112b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202195(v=OCS.15)
ms:contentKeyID: 51541532
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4fdefed873d1fd69d82f8ecebceeb92f06f65f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428466"
---
# <a name="establishing-a-backup-and-restoration-strategy-for-lync-server-2013"></a><span data-ttu-id="f03f8-103">为 Lync Server 2013 建立备份和还原策略</span><span class="sxs-lookup"><span data-stu-id="f03f8-103">Establishing a backup and restoration strategy for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f03f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f03f8-104">

<span> </span></span></span>

<span data-ttu-id="f03f8-105">_**主题上次修改时间：** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="f03f8-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="f03f8-106">在你可以为 Lync Server 开发备份和还原计划之前，你需要开发符合你组织的目标的策略。</span><span class="sxs-lookup"><span data-stu-id="f03f8-106">Before you can develop a backup and restoration plan for Lync Server, you need to develop a strategy that fits with your organization's goals.</span></span> <span data-ttu-id="f03f8-107">若要制定有效的备份和还原策略，您需要：</span><span class="sxs-lookup"><span data-stu-id="f03f8-107">To develop an effective backup and restoration strategy, you will need to:</span></span>

  - <span data-ttu-id="f03f8-108">建立业务优先级。</span><span class="sxs-lookup"><span data-stu-id="f03f8-108">Establish business priorities.</span></span>

  - <span data-ttu-id="f03f8-109">确定备份和还原要求。</span><span class="sxs-lookup"><span data-stu-id="f03f8-109">Identify backup and restoration requirements.</span></span>

<div>

## <a name="establishing-business-priorities"></a><span data-ttu-id="f03f8-110">建立业务优先级</span><span class="sxs-lookup"><span data-stu-id="f03f8-110">Establishing Business Priorities</span></span>

<span data-ttu-id="f03f8-111">评估你的组织的业务优先级。</span><span class="sxs-lookup"><span data-stu-id="f03f8-111">Evaluate the business priorities of your organization.</span></span> <span data-ttu-id="f03f8-112">通常，影响你的备份和还原策略的主要业务优先级如下所示：</span><span class="sxs-lookup"><span data-stu-id="f03f8-112">Typically, the primary business priorities that affect your backup and restoration strategy are the following:</span></span>

  - <span data-ttu-id="f03f8-113">业务连续性要求</span><span class="sxs-lookup"><span data-stu-id="f03f8-113">Business continuity requirements</span></span>

  - <span data-ttu-id="f03f8-114">数据完整性</span><span class="sxs-lookup"><span data-stu-id="f03f8-114">Data completeness</span></span>

  - <span data-ttu-id="f03f8-115">数据重要程度</span><span class="sxs-lookup"><span data-stu-id="f03f8-115">Data criticality</span></span>

  - <span data-ttu-id="f03f8-116">可移植性要求</span><span class="sxs-lookup"><span data-stu-id="f03f8-116">Portability requirements</span></span>

  - <span data-ttu-id="f03f8-117">成本限制</span><span class="sxs-lookup"><span data-stu-id="f03f8-117">Cost constraints</span></span>

<span data-ttu-id="f03f8-118">业务需求（如以下帮助）确定与客户一起开发的服务级别协议 (Sla) 。</span><span class="sxs-lookup"><span data-stu-id="f03f8-118">Business needs such as these help to determine the service level agreements (SLAs) that you develop with your customers.</span></span> <span data-ttu-id="f03f8-119">服务级别协议极大地影响你的备份和恢复策略。</span><span class="sxs-lookup"><span data-stu-id="f03f8-119">Service level agreements greatly influence your backup and recovery strategy.</span></span>

</div>

<div>

## <a name="identifying-backup-and-restoration-requirements"></a><span data-ttu-id="f03f8-120">确定备份和还原要求</span><span class="sxs-lookup"><span data-stu-id="f03f8-120">Identifying Backup and Restoration Requirements</span></span>

<span data-ttu-id="f03f8-121">你的企业优先级和服务级别协议在确定你的组织的备份和还原 Lync 服务器的要求方面起作用。</span><span class="sxs-lookup"><span data-stu-id="f03f8-121">Your business priorities and service level agreements act in determining your organizations' requirements for backing up and restoring Lync Server.</span></span> <span data-ttu-id="f03f8-122">确定并记录以下各项的要求：</span><span class="sxs-lookup"><span data-stu-id="f03f8-122">Identify and document your requirements for the following:</span></span>

  - <span data-ttu-id="f03f8-123">**备份频率**   有关备份频率的最佳做法的详细信息，请参阅 [Lync Server 2013 备份和还原的最佳做法](lync-server-2013-best-practices-for-backup-and-restoration.md)。</span><span class="sxs-lookup"><span data-stu-id="f03f8-123">**Frequency of backups**   For details about best practices for backup frequency, see [Best practices for backup and restoration for Lync Server 2013](lync-server-2013-best-practices-for-backup-and-restoration.md).</span></span>

  - <span data-ttu-id="f03f8-124">**备份和还原工具**   包括谁在哪些计算机上使用这些工具。</span><span class="sxs-lookup"><span data-stu-id="f03f8-124">**Backup and restoration tools**   Include who is to use the tools, and on which computers.</span></span> <span data-ttu-id="f03f8-125">有关本主题中讨论的工具和必要权限的详细信息，请参阅 [Lync Server 2013 中的备份和还原要求：工具和权限](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md)。</span><span class="sxs-lookup"><span data-stu-id="f03f8-125">For details about the tools discussed in this topic and necessary permissions, see [Backup and restoration requirements in Lync Server 2013: tools and permissions](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md).</span></span>

  - <span data-ttu-id="f03f8-126">**备份位置**   确定备份是保留在本地还是远程保存，以使安全性和可访问性考虑在内。</span><span class="sxs-lookup"><span data-stu-id="f03f8-126">**Backup location**   Identify whether the backups are kept locally or remotely, taking security and accessibility into consideration.</span></span> <span data-ttu-id="f03f8-127">指定要用于备份的媒体。</span><span class="sxs-lookup"><span data-stu-id="f03f8-127">Specify the media to be used for the backups.</span></span>

  - <span data-ttu-id="f03f8-128">**硬件和软件要求**   确定并记录你的特定硬件和软件要求，包括用于备份存储的硬件，以及支持备份和还原所需的任何软件和网络连接。</span><span class="sxs-lookup"><span data-stu-id="f03f8-128">**Hardware and software requirements**   Identify and document your specific hardware and software requirements, including the hardware for backup storage and restoration of specific components and any software and network connectivity required to support backup and restoration.</span></span> <span data-ttu-id="f03f8-129">在开发硬件和软件要求时，请记住下面的各种还原方案。</span><span class="sxs-lookup"><span data-stu-id="f03f8-129">As you develop your hardware and software requirements, keep in mind the various restoration scenarios that follow.</span></span>

  - <span data-ttu-id="f03f8-130">**还原方案**   下面是针对以下方案的还原过程：</span><span class="sxs-lookup"><span data-stu-id="f03f8-130">**Restoration scenarios**   Here are the restoration processes for the following scenarios:</span></span>
    
      - <span data-ttu-id="f03f8-131">Lync 服务器池失败。</span><span class="sxs-lookup"><span data-stu-id="f03f8-131">A Lync Server pool fails.</span></span> <span data-ttu-id="f03f8-132">此方案要求在池中重建每台服务器。</span><span class="sxs-lookup"><span data-stu-id="f03f8-132">This scenario requires rebuilding each server in the pool.</span></span>
    
      - <span data-ttu-id="f03f8-133">标准版服务器失败。</span><span class="sxs-lookup"><span data-stu-id="f03f8-133">A Standard Edition server fails.</span></span> <span data-ttu-id="f03f8-134">此方案要求在新计算机或全新计算机上重建服务器并还原数据库。</span><span class="sxs-lookup"><span data-stu-id="f03f8-134">This scenario requires rebuilding the server on a new or clean computer and restoring databases.</span></span>
    
      - <span data-ttu-id="f03f8-135">缺少中央管理存储。</span><span class="sxs-lookup"><span data-stu-id="f03f8-135">Loss of the Central Management store.</span></span> <span data-ttu-id="f03f8-136">此方案至少需要还原和发布中央管理存储。</span><span class="sxs-lookup"><span data-stu-id="f03f8-136">At a minimum, this scenario requires restoring and publishing the Central Management store.</span></span>
    
      - <span data-ttu-id="f03f8-137">当中央管理存储仍正常工作时，后端服务器的丢失。</span><span class="sxs-lookup"><span data-stu-id="f03f8-137">Loss of a Back End Server when the Central Management store is still functioning normally.</span></span> <span data-ttu-id="f03f8-138">此方案要求在新计算机或全新计算机上重建服务器并还原数据库。</span><span class="sxs-lookup"><span data-stu-id="f03f8-138">This scenario requires rebuilding the server on a new or clean computer and restoring databases.</span></span>
    
      - <span data-ttu-id="f03f8-139">作为 Lync 服务器池成员的服务器失败。</span><span class="sxs-lookup"><span data-stu-id="f03f8-139">A server that is a member of a Lync Server pool fails.</span></span> <span data-ttu-id="f03f8-140">此方案要求在新计算机或全新计算机上重建服务器。</span><span class="sxs-lookup"><span data-stu-id="f03f8-140">This scenario requires rebuilding the server on a new or clean computer.</span></span>
    
      - <span data-ttu-id="f03f8-141">文件存储失败。</span><span class="sxs-lookup"><span data-stu-id="f03f8-141">A File Store fails.</span></span> <span data-ttu-id="f03f8-142">此方案需要还原文件服务器或文件群集。</span><span class="sxs-lookup"><span data-stu-id="f03f8-142">This scenario requires restoring the file server or file cluster.</span></span>
    
      - <span data-ttu-id="f03f8-143">存档、监视或持久聊天数据库失败。</span><span class="sxs-lookup"><span data-stu-id="f03f8-143">An Archiving, Monitoring, or Persistent Chat database fails.</span></span> <span data-ttu-id="f03f8-144">此方案需要重新创建数据库，并且如果数据对你的组织非常重要，请还原数据。</span><span class="sxs-lookup"><span data-stu-id="f03f8-144">This scenario requires recreating the databases, and, if the data is critical to your organization, restoring the data.</span></span> <span data-ttu-id="f03f8-145">无需使用 "存档"、"监视" 和 "持久聊天" 数据即可恢复和运行 Lync 服务器。</span><span class="sxs-lookup"><span data-stu-id="f03f8-145">Archiving, Monitoring, and Persistent Chat data is not required to get Lync Server back up and running.</span></span>

<span data-ttu-id="f03f8-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f03f8-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

