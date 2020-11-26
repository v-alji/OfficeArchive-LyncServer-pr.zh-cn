---
title: Lync Server 2013：备份和还原工作表
description: Lync Server 2013：备份和还原工作表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration worksheets
ms:assetid: 26c78155-0306-41ac-845b-7ad58000a1d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202169(v=OCS.15)
ms:contentKeyID: 51541460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1713e291ae7132cc96309fa499bd97bf7f4f5016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437957"
---
# <a name="backup-and-restoration-worksheets-for-lync-server-2013"></a><span data-ttu-id="ea0d0-103">Lync Server 2013 的备份和还原工作表</span><span class="sxs-lookup"><span data-stu-id="ea0d0-103">Backup and restoration worksheets for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea0d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea0d0-104">

<span> </span></span></span>

<span data-ttu-id="ea0d0-105">_**主题上次修改时间：** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="ea0d0-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="ea0d0-106">您的组织的备份和还原计划应包含有关备份数据和设置的方式和时间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-106">The backup and restoration plan for your organization should contain details about how and when you back up data and settings.</span></span> <span data-ttu-id="ea0d0-107">你可以使用此处介绍的工作表来帮助你为特定部署以及你的组织的备份和还原要求记录此信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-107">You can use the worksheets presented here to help you document this information for your specific deployment and for your organization's backup and restoration requirements.</span></span>

<span data-ttu-id="ea0d0-108">使用以下工作表记录用于备份和还原 Lync Server 池或标准版服务器的数据库、文件存储和设置信息所需的信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-108">Use the following worksheets to record the information that you need to back up and restore database, File Store, and settings information for a Lync Server pool or Standard Edition server.</span></span> <span data-ttu-id="ea0d0-109">将这些工作表的一个或多个副本保留在一个安全位置，以便在需要还原 Lync 服务器时可以随时访问它们。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-109">Keep one or more copies of these worksheets in a secure location so that they are readily accessible if you need to restore Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ea0d0-110">本部分中的工作表仅涵盖还原 Lync Server 数据库和服务器的数据和设置所需的信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-110">The worksheets in this section cover only the information that is required to restore the data and settings of Lync Server databases and servers.</span></span> <span data-ttu-id="ea0d0-111">如果需要记录其他还原信息，例如用于重新安装操作系统和其他软件的信息，请使用组织的部署计划和备份和还原计划来满足这些要求。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-111">If you need to document other restoration information, such as the information for reinstalling operating systems and other software, use your organization's deployment plans and backup and restoration plans to address those requirements.</span></span>



</div>

<div>

## <a name="database-backup-and-restoration-worksheet"></a><span data-ttu-id="ea0d0-112">数据库备份和还原工作表</span><span class="sxs-lookup"><span data-stu-id="ea0d0-112">Database Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ea0d0-113">使用下表记录备份和还原 Lync Server 数据库所需的信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-113">Use the following table to record the information that you need to back up and restore Lync Server databases.</span></span>

### <a name="database-information-for-backup-and-restoration"></a><span data-ttu-id="ea0d0-114">用于备份和还原的数据库信息</span><span class="sxs-lookup"><span data-stu-id="ea0d0-114">Database Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea0d0-115">数据库</span><span class="sxs-lookup"><span data-stu-id="ea0d0-115">Database</span></span></th>
<th><span data-ttu-id="ea0d0-116"> (FQDN) 的服务器名称</span><span class="sxs-lookup"><span data-stu-id="ea0d0-116">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ea0d0-117">备份计划</span><span class="sxs-lookup"><span data-stu-id="ea0d0-117">Backup schedule</span></span></th>
<th><span data-ttu-id="ea0d0-118">数据库备份工具</span><span class="sxs-lookup"><span data-stu-id="ea0d0-118">Database backup tool</span></span></th>
<th><span data-ttu-id="ea0d0-119">备份集</span><span class="sxs-lookup"><span data-stu-id="ea0d0-119">Backup set</span></span></th>
<th><span data-ttu-id="ea0d0-120">备份目标</span><span class="sxs-lookup"><span data-stu-id="ea0d0-120">Backup destination</span></span></th>
<th><span data-ttu-id="ea0d0-121">注释</span><span class="sxs-lookup"><span data-stu-id="ea0d0-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea0d0-122">用户数据的后端服务器上的 Rtc 数据库</span><span class="sxs-lookup"><span data-stu-id="ea0d0-122">Rtc database on Back End Server for user data</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="ea0d0-123"><strong>Export-CsUserData</strong> cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea0d0-123"><strong>Export-CsUserData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="ea0d0-124">姓</span><span class="sxs-lookup"><span data-stu-id="ea0d0-124">Name:</span></span></p>
<p><span data-ttu-id="ea0d0-125">满</span><span class="sxs-lookup"><span data-stu-id="ea0d0-125">Expiration:</span></span></p>
<p>                   </p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea0d0-126">LcsLog (存档数据库服务器上的数据库) 默认名称</span><span class="sxs-lookup"><span data-stu-id="ea0d0-126">LcsLog (default name) database on Archiving database server</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ea0d0-127">SQL Server 管理工具</span><span class="sxs-lookup"><span data-stu-id="ea0d0-127">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ea0d0-128">姓</span><span class="sxs-lookup"><span data-stu-id="ea0d0-128">Name:</span></span></p>
<p><span data-ttu-id="ea0d0-129">满</span><span class="sxs-lookup"><span data-stu-id="ea0d0-129">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea0d0-130">用于监视数据库服务器上的 LcsCdr 数据库的通话详细记录 (CDRs) </span><span class="sxs-lookup"><span data-stu-id="ea0d0-130">LcsCdr database on Monitoring database server for call detail records (CDRs)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ea0d0-131">SQL Server 管理工具</span><span class="sxs-lookup"><span data-stu-id="ea0d0-131">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ea0d0-132">姓</span><span class="sxs-lookup"><span data-stu-id="ea0d0-132">Name:</span></span></p>
<p><span data-ttu-id="ea0d0-133">满</span><span class="sxs-lookup"><span data-stu-id="ea0d0-133">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea0d0-134">监视数据库服务器上的 QoEMetrics 数据库以获得经验 (QoE) 数据</span><span class="sxs-lookup"><span data-stu-id="ea0d0-134">QoEMetrics database on Monitoring database server for Quality of Experience (QoE) data</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ea0d0-135">SQL Server 管理工具</span><span class="sxs-lookup"><span data-stu-id="ea0d0-135">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="ea0d0-136">姓</span><span class="sxs-lookup"><span data-stu-id="ea0d0-136">Name:</span></span></p>
<p><span data-ttu-id="ea0d0-137">满</span><span class="sxs-lookup"><span data-stu-id="ea0d0-137">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea0d0-138">持久聊天数据库</span><span class="sxs-lookup"><span data-stu-id="ea0d0-138">Persistent Chat Database</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="ea0d0-139">SQL Server 管理工具或 <strong>Export-CsPersistentChatData</strong> cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea0d0-139">SQL Server management tool or <strong>Export-CsPersistentChatData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="ea0d0-140">姓</span><span class="sxs-lookup"><span data-stu-id="ea0d0-140">Name:</span></span></p>
<p><span data-ttu-id="ea0d0-141">满</span><span class="sxs-lookup"><span data-stu-id="ea0d0-141">Expiration:</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ea0d0-142">不需要以下数据库的备份或还原：</span><span class="sxs-lookup"><span data-stu-id="ea0d0-142">No backup or restoration is required of the following databases:</span></span>

  - <span data-ttu-id="ea0d0-143">Rtcdyn.</span><span class="sxs-lookup"><span data-stu-id="ea0d0-143">Rtcdyn.</span></span> <span data-ttu-id="ea0d0-144">还原服务不需要此数据库中的瞬时用户数据。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-144">The transient user data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ea0d0-145">Rtcab.</span><span class="sxs-lookup"><span data-stu-id="ea0d0-145">Rtcab.</span></span> <span data-ttu-id="ea0d0-146">通讯簿数据库将从 Active Directory 域服务中 (GAL) 的全局地址列表中自动重新创建。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-146">The Address Book database is automatically recreated from the Global Address List (GAL) in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="ea0d0-147">Rgsdyn.</span><span class="sxs-lookup"><span data-stu-id="ea0d0-147">Rgsdyn.</span></span> <span data-ttu-id="ea0d0-148">还原服务不需要此数据库中的暂时性响应组服务数据。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-148">The transient Response Group service data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ea0d0-149">Cpsdyn.</span><span class="sxs-lookup"><span data-stu-id="ea0d0-149">Cpsdyn.</span></span> <span data-ttu-id="ea0d0-150">还原服务不需要调用寄存应用程序的动态信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-150">The dynamic information for the Call Park application is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="ea0d0-151">MgcComp.</span><span class="sxs-lookup"><span data-stu-id="ea0d0-151">MgcComp.</span></span> <span data-ttu-id="ea0d0-152">用于持久聊天的合规性数据库不是还原服务所必需的。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-152">The compliance database for Persistent Chat is not necessary for restoration of service.</span></span>

</div>

<div>

## <a name="file-store-backup-and-restoration-worksheet"></a><span data-ttu-id="ea0d0-153">文件存储备份和还原工作表</span><span class="sxs-lookup"><span data-stu-id="ea0d0-153">File Store Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ea0d0-154">使用下表记录备份和还原文件存储所需的信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-154">Use the following table to record the information that you need to back up and restore the File Stores.</span></span> <span data-ttu-id="ea0d0-155">文件存储包含会议内容元数据、会议合规性日志、更新设备更新日志以及响应组的音频文件、呼叫寄存和发布应用程序等数据。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-155">File Stores contain data such as meeting content metadata, meeting compliance logs, update logs for device updates, and audio files for the Response Group, Call Park, and Announcement applications.</span></span>

### <a name="file-store-information-for-backup-and-restoration"></a><span data-ttu-id="ea0d0-156">用于备份和还原的文件存储信息</span><span class="sxs-lookup"><span data-stu-id="ea0d0-156">File Store Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea0d0-157">内容</span><span class="sxs-lookup"><span data-stu-id="ea0d0-157">Content</span></span></th>
<th><span data-ttu-id="ea0d0-158"> (FQDN) 的服务器名称</span><span class="sxs-lookup"><span data-stu-id="ea0d0-158">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ea0d0-159">备份计划</span><span class="sxs-lookup"><span data-stu-id="ea0d0-159">Backup schedule</span></span></th>
<th><span data-ttu-id="ea0d0-160">文件系统备份工具</span><span class="sxs-lookup"><span data-stu-id="ea0d0-160">File system backup tool</span></span></th>
<th><span data-ttu-id="ea0d0-161">要备份的文件共享 \*</span><span class="sxs-lookup"><span data-stu-id="ea0d0-161">File share to be backed up \*</span></span></th>
<th><span data-ttu-id="ea0d0-162">备份目标</span><span class="sxs-lookup"><span data-stu-id="ea0d0-162">Backup destination</span></span></th>
<th><span data-ttu-id="ea0d0-163">注释</span><span class="sxs-lookup"><span data-stu-id="ea0d0-163">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea0d0-164">Lync Server 文件存储</span><span class="sxs-lookup"><span data-stu-id="ea0d0-164">Lync Server File Store</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="ea0d0-165">标准备份工具，如 Robocopy</span><span class="sxs-lookup"><span data-stu-id="ea0d0-165">Standard backup tool, such as Robocopy</span></span></p></td>
<td><p><span data-ttu-id="ea0d0-166">在 "适用于企业版的文件服务器" 上。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-166">On file server for Enterprise Edition.</span></span> <span data-ttu-id="ea0d0-167">对于标准版，默认情况下为标准版部署。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-167">On Standard Edition by default, for Standard Edition deployment.</span></span> <span data-ttu-id="ea0d0-168">通常，每个站点一个。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-168">Typically, one per site.</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ea0d0-169">名为 " <strong>会议" 的</strong> 文件不应备份。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-169">Files named <strong>Meeting.Active</strong> should not be backed up.</span></span> <span data-ttu-id="ea0d0-170">这些文件正在使用中，并且在会议发生时被锁定。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-170">These files are in use and are locked while a meeting takes place.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="settings-backup-and-restoration-worksheet"></a><span data-ttu-id="ea0d0-171">设置备份和还原工作表</span><span class="sxs-lookup"><span data-stu-id="ea0d0-171">Settings Backup and Restoration Worksheet</span></span>

<span data-ttu-id="ea0d0-172">使用下表记录备份和还原设置所需的信息。</span><span class="sxs-lookup"><span data-stu-id="ea0d0-172">Use the following table to record the information that you need to back up and restore settings.</span></span>

### <a name="settings-information-for-backup-and-restoration"></a><span data-ttu-id="ea0d0-173">备份和还原的设置信息</span><span class="sxs-lookup"><span data-stu-id="ea0d0-173">Settings Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea0d0-174">数据库</span><span class="sxs-lookup"><span data-stu-id="ea0d0-174">Database</span></span></th>
<th><span data-ttu-id="ea0d0-175"> (FQDN) 的服务器名称</span><span class="sxs-lookup"><span data-stu-id="ea0d0-175">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="ea0d0-176">备份计划</span><span class="sxs-lookup"><span data-stu-id="ea0d0-176">Backup schedule</span></span></th>
<th><span data-ttu-id="ea0d0-177">备份工具</span><span class="sxs-lookup"><span data-stu-id="ea0d0-177">Backup tool</span></span></th>
<th><span data-ttu-id="ea0d0-178">配置文件 ( .xml) 名称</span><span class="sxs-lookup"><span data-stu-id="ea0d0-178">Configuration file (.xml) name</span></span></th>
<th><span data-ttu-id="ea0d0-179">备份位置</span><span class="sxs-lookup"><span data-stu-id="ea0d0-179">Backup location</span></span></th>
<th><span data-ttu-id="ea0d0-180">注释</span><span class="sxs-lookup"><span data-stu-id="ea0d0-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea0d0-181"> (全局) 的 "中央管理存储" 中的 "拓扑配置" 的 Xds 数据库</span><span class="sxs-lookup"><span data-stu-id="ea0d0-181">Xds database in Central Management store for topology configuration (global)</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="ea0d0-182"><strong>Export-CsConfiguration</strong> cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea0d0-182"><strong>Export-CsConfiguration</strong> cmdlet</span></span></p></td>
<td><p>                   </p></td>
<td><p>                    </p></td>
<td><p>                   </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea0d0-183">中央管理存储中的 .lis 数据库 E9-1-1-1 位置信息 (全局) </span><span class="sxs-lookup"><span data-stu-id="ea0d0-183">Lis database in Central Management store for E9-1-1 location information (global)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ea0d0-184"><strong>Export-CsLisConfiguration</strong> cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea0d0-184"><strong>Export-CsLisConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea0d0-185">RgsConfig) 的 "后端服务器" 上的 "响应组 (配置" 的数据库</span><span class="sxs-lookup"><span data-stu-id="ea0d0-185">RgsConfig database on Back End Server for Response Group configuration (pool)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ea0d0-186"><strong>Export-CsRgsConfiguration</strong> cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea0d0-186"><strong>Export-CsRgsConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
</tbody>
</table><span data-ttu-id="ea0d0-187">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea0d0-187">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

