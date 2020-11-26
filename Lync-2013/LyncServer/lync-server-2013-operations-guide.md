---
title: Lync Server 2013：操作指南
description: Lync Server 2013：操作指南。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operations Guide
ms:assetid: dcb9ddff-6fe3-4077-a2e3-0ba64f65e264
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720467(v=OCS.15)
ms:contentKeyID: 63969658
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 85e562b96e87f54529a9e2ce077a0a82574020c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445274"
---
# <a name="operations-guide-for-lync-server-2013"></a><span data-ttu-id="9aada-103">Operations Guide for Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aada-103">Operations Guide for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9aada-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9aada-104">

<span> </span></span></span>

<span data-ttu-id="9aada-105">_**主题上次修改时间：** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="9aada-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="9aada-106">本文档介绍维护 Microsoft Lync Server 2013 通信软件环境所需的操作过程、任务和工具。</span><span class="sxs-lookup"><span data-stu-id="9aada-106">This document describes the operational processes, tasks, and tools that are required for you to maintain a Microsoft Lync Server 2013 communications software environment.</span></span> <span data-ttu-id="9aada-107">它介绍了如何根据 Microsoft 操作框架 (MOF) 模型来管理 Lync Server 2013，它将帮助你设计高效的运营管理环境，其中包括实施计划、流程和过程来维护高效的工作环境。</span><span class="sxs-lookup"><span data-stu-id="9aada-107">It explains how to manage Lync Server 2013 according to the Microsoft Operations Framework (MOF) model and it will help you design an efficient operational management environment, which includes implementing schedules, processes and procedures to maintain an efficient working environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9aada-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="9aada-108">In This Section</span></span>

<span data-ttu-id="9aada-109">包括以下部分：</span><span class="sxs-lookup"><span data-stu-id="9aada-109">The following sections are included:</span></span>

  - [<span data-ttu-id="9aada-110">Lync Server 2013 环境的最佳做法</span><span class="sxs-lookup"><span data-stu-id="9aada-110">Best practices for Lync Server 2013 environments</span></span>](lync-server-2013-best-practices-for-lync-server-environments.md)

  - [<span data-ttu-id="9aada-111">Lync Server 2013 中的日常任务</span><span class="sxs-lookup"><span data-stu-id="9aada-111">Daily tasks in Lync Server 2013</span></span>](lync-server-2013-daily-tasks.md)

  - [<span data-ttu-id="9aada-112">Lync Server 2013 中的周任务</span><span class="sxs-lookup"><span data-stu-id="9aada-112">Weekly tasks in Lync Server 2013</span></span>](lync-server-2013-weekly-tasks.md)

  - [<span data-ttu-id="9aada-113">Lync Server 2013 中的每月任务</span><span class="sxs-lookup"><span data-stu-id="9aada-113">Monthly tasks in Lync Server 2013</span></span>](lync-server-2013-monthly-tasks.md)

  - [<span data-ttu-id="9aada-114">Lync Server 2013 中的 "需要" 任务</span><span class="sxs-lookup"><span data-stu-id="9aada-114">As-needed tasks in Lync Server 2013</span></span>](lync-server-2013-as-needed-tasks.md)

  - [<span data-ttu-id="9aada-115">Lync Server 2013 的操作清单</span><span class="sxs-lookup"><span data-stu-id="9aada-115">Operations checklists for Lync Server 2013</span></span>](lync-server-2013-operations-checklists.md)

  - [<span data-ttu-id="9aada-116">通过 System Center Operations Manager 监视 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aada-116">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)

  - [<span data-ttu-id="9aada-117">Lync Server 2013 中的操作相关性</span><span class="sxs-lookup"><span data-stu-id="9aada-117">Operational dependencies in Lync Server 2013</span></span>](lync-server-2013-operational-dependencies.md)

  - [<span data-ttu-id="9aada-118">Lync Server 2013 中的故障排除和关键运行状况指示器</span><span class="sxs-lookup"><span data-stu-id="9aada-118">Troubleshooting and Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-and-key-health-indicators.md)

<span data-ttu-id="9aada-119">假设您的 Microsoft Lync Server 2013 部署已完成。</span><span class="sxs-lookup"><span data-stu-id="9aada-119">It is assumed that your Microsoft Lync Server 2013 deployment is completed.</span></span> <span data-ttu-id="9aada-120">如果不是这种情况，请参阅 Microsoft Lync Server 2013 的规划和部署内容，然后再继续。</span><span class="sxs-lookup"><span data-stu-id="9aada-120">If this is not the case, refer to the planning and deployment content for Microsoft Lync Server 2013 before you continue.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9aada-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9aada-121">See Also</span></span>


[<span data-ttu-id="9aada-122">Lync Server 2013 入门</span><span class="sxs-lookup"><span data-stu-id="9aada-122">Getting started with Lync Server 2013</span></span>](lync-server-2013-getting-started.md)  
[<span data-ttu-id="9aada-123">规划 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9aada-123">Planning for Lync Server 2013</span></span>](lync-server-2013-planning.md)  
[<span data-ttu-id="9aada-124">Lync Server 2013 的部署</span><span class="sxs-lookup"><span data-stu-id="9aada-124">Deployment of Lync Server 2013</span></span>](lync-server-2013-deployment.md)  
[<span data-ttu-id="9aada-125">Lync Server 2013 命令行管理程序</span><span class="sxs-lookup"><span data-stu-id="9aada-125">Lync Server 2013 Management Shell</span></span>](lync-server-2013-lync-server-management-shell.md)  
  

<span data-ttu-id="9aada-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9aada-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

