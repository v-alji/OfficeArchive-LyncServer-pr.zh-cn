---
title: Lync Server 2013：病毒扫描排除
description: Lync Server 2013：防病毒扫描排除项。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440659"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a><span data-ttu-id="9279b-103">Lync Server 2013 的病毒扫描排除</span><span class="sxs-lookup"><span data-stu-id="9279b-103">Antivirus scanning exclusions for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9279b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9279b-104">

<span> </span></span></span>

<span data-ttu-id="9279b-105">_**主题上次修改时间：** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="9279b-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="9279b-106">为确保防病毒扫描程序不会干扰 Lync Server 2013 的操作，必须排除运行防病毒扫描程序的每个 Lync Server 2013 服务器或服务器角色的特定进程和目录。</span><span class="sxs-lookup"><span data-stu-id="9279b-106">To ensure that the antivirus scanner does not interfere with the operation of Lync Server 2013, you must exclude specific processes and directories for each Lync Server 2013 server or server role on which you run an antivirus scanner.</span></span> <span data-ttu-id="9279b-107">应排除以下进程和目录：</span><span class="sxs-lookup"><span data-stu-id="9279b-107">The following processes and directories should be excluded:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9279b-108">以下列出的文件夹和文件位置是 Lync Server 2013 的默认位置。</span><span class="sxs-lookup"><span data-stu-id="9279b-108">Folder and file locations listed below are the default locations for Lync Server 2013.</span></span> <span data-ttu-id="9279b-109">对于您没有使用默认值的任何位置，排除您为组织指定的位置，而不是本主题中指定的默认位置。</span><span class="sxs-lookup"><span data-stu-id="9279b-109">For any locations for which you did not use the default, exclude the locations you specified for your organization instead of the default locations specified in this topic.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9279b-110">请注意，某些防病毒程序可能需要对排除列表使用绝对路径而不是相对路径。</span><span class="sxs-lookup"><span data-stu-id="9279b-110">Please note that some antivirus programs may need absolute, not relative paths, for their exclusion list.</span></span>



</div>

  - <span data-ttu-id="9279b-111">Lync Server 2013 进程：</span><span class="sxs-lookup"><span data-stu-id="9279b-111">Lync Server 2013 processes:</span></span>
    
      - <span data-ttu-id="9279b-112">ABServer.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-112">ABServer.exe</span></span>
    
      - <span data-ttu-id="9279b-113">AcpMcuSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-113">AcpMcuSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-114">ASMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-114">ASMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-115">AVMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-115">AVMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-116">ChannelService.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-116">ChannelService.exe</span></span>
    
      - <span data-ttu-id="9279b-117">ClsAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-117">ClsAgent.exe</span></span>
    
      - <span data-ttu-id="9279b-118">ComplianceService.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-118">ComplianceService.exe</span></span>
    
      - <span data-ttu-id="9279b-119">DataMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-119">DataMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-120">DataProxy.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-120">DataProxy.exe</span></span>
    
      - <span data-ttu-id="9279b-121">FileTransferAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-121">FileTransferAgent.exe</span></span>
    
      - <span data-ttu-id="9279b-122">IMMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-122">IMMCUSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-123">LysSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-123">LysSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-124">MasterReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-124">MasterReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="9279b-125">MediaRelaySvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-125">MediaRelaySvc.exe</span></span>
    
      - <span data-ttu-id="9279b-126">MediationServerSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-126">MediationServerSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-127">MRASSvc.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-127">MRASSvc.exe</span></span>
    
      - <span data-ttu-id="9279b-128">OcsAppServerHost.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-128">OcsAppServerHost.exe</span></span>
    
      - <span data-ttu-id="9279b-129">ReplicaReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-129">ReplicaReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="9279b-130">ReplicationApp.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-130">ReplicationApp.exe</span></span>
    
      - <span data-ttu-id="9279b-131">RtcHost.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-131">RtcHost.exe</span></span>
    
      - <span data-ttu-id="9279b-132">RTCSrv.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-132">RTCSrv.exe</span></span>
    
      - <span data-ttu-id="9279b-133">XmppProxy.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-133">XmppProxy.exe</span></span>
    
      - <span data-ttu-id="9279b-134">XmppTGW.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-134">XmppTGW.exe</span></span>

  - <span data-ttu-id="9279b-135">Windows Fabric Host Service 进程：</span><span class="sxs-lookup"><span data-stu-id="9279b-135">Windows Fabric Host Service processes:</span></span>
    
      - <span data-ttu-id="9279b-136">Fabric.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-136">Fabric.exe</span></span>
    
      - <span data-ttu-id="9279b-137">FabricDCA.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-137">FabricDCA.exe</span></span>
    
      - <span data-ttu-id="9279b-138">FabricHost.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-138">FabricHost.exe</span></span>

  - <span data-ttu-id="9279b-139">IIS 进程：</span><span class="sxs-lookup"><span data-stu-id="9279b-139">IIS processes:</span></span>
    
      - <span data-ttu-id="9279b-140">% systemroot% \\ system32 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-140">%systemroot%\\system32\\inetsrv\\w3wp.exe</span></span>
    
      - <span data-ttu-id="9279b-141">% systemroot% \\ SysWOW64 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-141">%systemroot%\\SysWOW64\\inetsrv\\w3wp.exe</span></span>

  - <span data-ttu-id="9279b-142">SQL Server 后端进程：</span><span class="sxs-lookup"><span data-stu-id="9279b-142">SQL Server Back-End processes:</span></span>
    
      - <span data-ttu-id="9279b-143">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。MSSQLSERVER \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-143">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="9279b-144">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSRS11。MSSQLSERVER \\ Reporting Services \\ ReportServer \\ Bin \\ReportingServicesService.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-144">%ProgramFiles%\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\Bin\\ReportingServicesService.exe</span></span>
    
      - <span data-ttu-id="9279b-145">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSAS11。MSSQLSERVER \\ OLAP \\ Bin \\MSMDSrv.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-145">%ProgramFiles%\\Microsoft SQL Server\\MSAS11.MSSQLSERVER\\OLAP\\Bin\\MSMDSrv.exe</span></span>

  - <span data-ttu-id="9279b-146">SQL Server 前端进程：</span><span class="sxs-lookup"><span data-stu-id="9279b-146">SQL Server Front-End processes:</span></span>
    
      - <span data-ttu-id="9279b-147">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。LYNCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-147">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.LYNCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="9279b-148">% ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。RTCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="9279b-148">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.RTCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>

  - <span data-ttu-id="9279b-149">目录和文件：</span><span class="sxs-lookup"><span data-stu-id="9279b-149">Directories and files:</span></span>
    
      - <span data-ttu-id="9279b-150">% systemroot% \\ System32 \\ 日志</span><span class="sxs-lookup"><span data-stu-id="9279b-150">%systemroot%\\System32\\LogFiles</span></span>
    
      - <span data-ttu-id="9279b-151">% systemroot% \\ SysWow64 \\ 日志日志</span><span class="sxs-lookup"><span data-stu-id="9279b-151">%systemroot%\\SysWow64\\LogFiles</span></span>
    
      - <span data-ttu-id="9279b-152">% systemroot% \\ Microsoft.NET \\ 程序集 \\ GAC \_ MSIL</span><span class="sxs-lookup"><span data-stu-id="9279b-152">%systemroot%\\Microsoft.NET\\assembly\\GAC\_MSIL</span></span>
    
      - <span data-ttu-id="9279b-153">% programfiles% \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9279b-153">%programfiles%\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="9279b-154">% programfiles% 的 \\ 常见文件 \\ Microsoft Lync Server 2013 \\ 观察程序节点</span><span class="sxs-lookup"><span data-stu-id="9279b-154">%programfiles%\\Common Files\\Microsoft Lync Server 2013\\Watcher Node</span></span>
    
      - <span data-ttu-id="9279b-155">% programfiles% 的 \\ 常见文件 \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9279b-155">%programfiles%\\Common Files\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="9279b-156">% SystemDrive% \\ RtcReplicaRoot</span><span class="sxs-lookup"><span data-stu-id="9279b-156">%SystemDrive%\\RtcReplicaRoot</span></span>
    
      - <span data-ttu-id="9279b-157">文件共享存储（在拓扑生成器中指定）。</span><span class="sxs-lookup"><span data-stu-id="9279b-157">File share store (specified in Topology Builder).</span></span> <span data-ttu-id="9279b-158">文件存储在拓扑生成器中指定。</span><span class="sxs-lookup"><span data-stu-id="9279b-158">File stores are specified in Topology Builder.</span></span>
    
      - <span data-ttu-id="9279b-159">SQL Server 数据和日志文件，包括后端数据库、用户存储、存档存储、监控存储和应用程序存储的这些文件。</span><span class="sxs-lookup"><span data-stu-id="9279b-159">SQL Server data and log files, including those for the back-end database, user store, archiving store, monitoring store, and application store.</span></span> <span data-ttu-id="9279b-160">可以在拓扑生成器中指定数据库和日志文件。</span><span class="sxs-lookup"><span data-stu-id="9279b-160">Database and log files can be specified in Topology Builder.</span></span> <span data-ttu-id="9279b-161">有关每个数据库的数据和日志文件（包括默认名称）的详细信息，请参阅部署文档中 [Lync server 2013 的 SQL Server 数据和日志文件放置](lync-server-2013-sql-server-data-and-log-file-placement.md) 。</span><span class="sxs-lookup"><span data-stu-id="9279b-161">For details about the data and log files for each database, including default names, see [SQL Server data and log file placement for Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="9279b-162">SQL Server 数据和日志文件，包括前端数据库、Lync 应用商店和 RtcDatabase 应用商店的文件。</span><span class="sxs-lookup"><span data-stu-id="9279b-162">SQL Server data and log files, including those for the Front-end database, Lync store, and RtcDatabase store.</span></span> <span data-ttu-id="9279b-163">它们通常位于% localdrive% \\ CSData。</span><span class="sxs-lookup"><span data-stu-id="9279b-163">They are normally under %localdrive%\\CSData.</span></span>

<span data-ttu-id="9279b-164"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9279b-164"></div>

<span> </span>

</div>

</div>

</span></span></div>

