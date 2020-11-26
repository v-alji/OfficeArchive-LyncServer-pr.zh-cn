---
title: Lync Server 2013：备份和还原要求：工具和权限
description: Lync Server 2013：备份和还原要求：工具和权限。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: tools and permissions'
ms:assetid: 35ec2e33-f33e-4f84-9e64-6550fd78aa52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202171(v=OCS.15)
ms:contentKeyID: 51541465
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36327d1214854586b44024f126bbd87acad6c4b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437978"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-tools-and-permissions"></a><span data-ttu-id="7612d-103">Lync Server 2013 中的备份和还原要求：工具和权限</span><span class="sxs-lookup"><span data-stu-id="7612d-103">Backup and restoration requirements in Lync Server 2013: tools and permissions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7612d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7612d-104">

<span> </span></span></span>

<span data-ttu-id="7612d-105">_**主题上次修改时间：** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="7612d-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="7612d-106">本主题介绍可用于备份和还原 Lync Server 2013 的工具、所需权限以及是否可以远程或本地运行命令。</span><span class="sxs-lookup"><span data-stu-id="7612d-106">This topic identifies the tools that you can use to back up and restore Lync Server 2013, the permissions that you need, and whether you can run commands remotely or locally.</span></span> <span data-ttu-id="7612d-107">具体地说，本主题重点介绍 Lync Server 提供的用于备份和还原的工具。</span><span class="sxs-lookup"><span data-stu-id="7612d-107">Specifically, this topic focuses on tools that are provided with Lync Server for backup and restoration.</span></span>

<div>

## <a name="backups"></a><span data-ttu-id="7612d-108">量</span><span class="sxs-lookup"><span data-stu-id="7612d-108">Backups</span></span>

<span data-ttu-id="7612d-109">若要备份 Lync Server，请使用下表中标识的工具。</span><span class="sxs-lookup"><span data-stu-id="7612d-109">To back up Lync Server, use the tools identified in the following table.</span></span> <span data-ttu-id="7612d-110">您需要用于备份 Lync 服务器的所有命令都可以编写脚本，并且可以远程运行。</span><span class="sxs-lookup"><span data-stu-id="7612d-110">All the commands that you need to back up Lync Server can be scripted and can be run remotely.</span></span>

### <a name="tools-for-backing-up-lync-server"></a><span data-ttu-id="7612d-111">用于备份 Lync Server 的工具</span><span class="sxs-lookup"><span data-stu-id="7612d-111">Tools for Backing Up Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7612d-112">若要备份，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7612d-112">To back up this:</span></span></th>
<th><span data-ttu-id="7612d-113">使用此工具或 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="7612d-113">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7612d-114">拓扑配置数据 (Xds) </span><span class="sxs-lookup"><span data-stu-id="7612d-114">Topology configuration data (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-115">Export-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="7612d-115">Export-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-116">位置信息服务 (E9-1-1) 数据 (.Lis) </span><span class="sxs-lookup"><span data-stu-id="7612d-116">Location information service (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-117">Export-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="7612d-117">Export-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-118"> (RgsConfig) 的响应组配置数据</span><span class="sxs-lookup"><span data-stu-id="7612d-118">Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-119">Export-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="7612d-119">Export-CsRgsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-120">持久性用户数据 (Rtcxds 数据库) </span><span class="sxs-lookup"><span data-stu-id="7612d-120">Persistent user data (Rtcxds.mdf database)</span></span></p>
<p><span data-ttu-id="7612d-121">会议 Id</span><span class="sxs-lookup"><span data-stu-id="7612d-121">Conference IDs</span></span></p></td>
<td><p><span data-ttu-id="7612d-122">Export-CsUserData</span><span class="sxs-lookup"><span data-stu-id="7612d-122">Export-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><ul>
<li><p><span data-ttu-id="7612d-123">将数据库存档 (LcsLog) </span><span class="sxs-lookup"><span data-stu-id="7612d-123">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="7612d-124">监视通话详细信息记录数据库 (LcsCDR) </span><span class="sxs-lookup"><span data-stu-id="7612d-124">Monitoring call detail record database (LcsCDR.mdf)</span></span></p></li>
<li><p><span data-ttu-id="7612d-125">监视 QoE 数据库 (QoEMetrics) </span><span class="sxs-lookup"><span data-stu-id="7612d-125">Monitoring QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7612d-126">SQL Server 数据库工具，例如 SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="7612d-126">SQL Server database tool, such as SQL Server Management Studio</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-127">持久聊天数据库 (Mgc) </span><span class="sxs-lookup"><span data-stu-id="7612d-127">Persistent Chat database (Mgc.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-128">SQL Server 备份过程或导出-CsPersistentChatData。</span><span class="sxs-lookup"><span data-stu-id="7612d-128">SQL Server backup procedures or Export-CsPersistentChatData.</span></span> <span data-ttu-id="7612d-129">Export-CsPersistentChatData 将永久聊天数据导出为文件。</span><span class="sxs-lookup"><span data-stu-id="7612d-129">Export-CsPersistentChatData exports Persistent Chat data as a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-130">所有文件存储： Lync Server 文件存储、存档文件存储</span><span class="sxs-lookup"><span data-stu-id="7612d-130">All file stores: Lync Server file store, Archiving file store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="7612d-131">名为 " <STRONG>会议" 的</STRONG> 文件不应备份。</span><span class="sxs-lookup"><span data-stu-id="7612d-131">Files named <STRONG>Meeting.Active</STRONG> should not be backed up.</span></span> <span data-ttu-id="7612d-132">这些文件正在使用中，并且在召开会议时被锁定。</span><span class="sxs-lookup"><span data-stu-id="7612d-132">These files are in use and locked while a meeting takes place.</span></span>


</div></td>
<td><p><span data-ttu-id="7612d-133">标准文件系统管理工具，例如 Robocopy。</span><span class="sxs-lookup"><span data-stu-id="7612d-133">Standard file system management tool, such as Robocopy.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="restoration"></a><span data-ttu-id="7612d-134">还原</span><span class="sxs-lookup"><span data-stu-id="7612d-134">Restoration</span></span>

<span data-ttu-id="7612d-135">若要还原 Lync Server，请使用下表中的工具。</span><span class="sxs-lookup"><span data-stu-id="7612d-135">To restore Lync Server, use the tools in the following table.</span></span> <span data-ttu-id="7612d-136">可以为还原 Lync Server 所需的所有命令编写脚本。</span><span class="sxs-lookup"><span data-stu-id="7612d-136">All the commands that you need to restore Lync Server can be scripted.</span></span> <span data-ttu-id="7612d-137">有些可以远程运行，但其他人需要在下表中指定的本地运行。</span><span class="sxs-lookup"><span data-stu-id="7612d-137">Some can be run remotely, but others need to be run locally, as specified in the following table.</span></span>

### <a name="tools-for-restoring-lync-server"></a><span data-ttu-id="7612d-138">用于还原 Lync Server 的工具</span><span class="sxs-lookup"><span data-stu-id="7612d-138">Tools for Restoring Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7612d-139">要执行此操作：</span><span class="sxs-lookup"><span data-stu-id="7612d-139">To do this:</span></span></th>
<th><span data-ttu-id="7612d-140">使用此工具或 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="7612d-140">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7612d-141">构建新的或全新的计算机</span><span class="sxs-lookup"><span data-stu-id="7612d-141">Build a new or clean computer</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7612d-142">Windows 操作系统安装软件</span><span class="sxs-lookup"><span data-stu-id="7612d-142">Windows operating system installation software</span></span></p></li>
<li><p><span data-ttu-id="7612d-143">SQL Server 安装软件</span><span class="sxs-lookup"><span data-stu-id="7612d-143">SQL Server installation software</span></span></p></li>
<li><p><span data-ttu-id="7612d-144">证书 Microsoft 管理控制台 (MMC) 管理单元（如果使用可导出私钥还原证书）</span><span class="sxs-lookup"><span data-stu-id="7612d-144">Certificates Microsoft Management Console (MMC) snap-in, if restoring certificates with an exportable private key</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-145">还原文件存储数据</span><span class="sxs-lookup"><span data-stu-id="7612d-145">Restore file store data</span></span></p></td>
<td><p><span data-ttu-id="7612d-146">标准文件系统管理工具，例如 Robocopy</span><span class="sxs-lookup"><span data-stu-id="7612d-146">Standard file system management tool, such as Robocopy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-147">重新创建空数据库并为以下项设置权限：</span><span class="sxs-lookup"><span data-stu-id="7612d-147">Recreate empty databases and set permissions for the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="7612d-148">中央管理存储</span><span class="sxs-lookup"><span data-stu-id="7612d-148">Central Management store</span></span></p></li>
<li><p><span data-ttu-id="7612d-149">后端服务器</span><span class="sxs-lookup"><span data-stu-id="7612d-149">Back End Server</span></span></p></li>
<li><p><span data-ttu-id="7612d-150">监控数据库</span><span class="sxs-lookup"><span data-stu-id="7612d-150">Monitoring database</span></span></p></li>
<li><p><span data-ttu-id="7612d-151">存档数据库</span><span class="sxs-lookup"><span data-stu-id="7612d-151">Archiving database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7612d-152">Install-CsDatabase</span><span class="sxs-lookup"><span data-stu-id="7612d-152">Install-CsDatabase</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-153">将 Active Directory 域服务指针还原到中央管理存储</span><span class="sxs-lookup"><span data-stu-id="7612d-153">Restore the Active Directory Domain Services pointer to the Central Management store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="7612d-154">如果您随时失去服务连接点，则可以重新运行此 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7612d-154">If you lose the service connection point at any time, you can rerun this cmdlet.</span></span>


</div></td>
<td><p><span data-ttu-id="7612d-155">Set-CsConfigurationStoreLocation</span><span class="sxs-lookup"><span data-stu-id="7612d-155">Set-CsConfigurationStoreLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-156">将拓扑、策略和配置设置导入中央管理存储 (Xds) </span><span class="sxs-lookup"><span data-stu-id="7612d-156">Import the topology, policies, and configuration settings to the Central Management store (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-157">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="7612d-157">Import-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-158">发布和启用拓扑</span><span class="sxs-lookup"><span data-stu-id="7612d-158">Publish and enable the topology</span></span></p></td>
<td><p><span data-ttu-id="7612d-159">拓扑生成器</span><span class="sxs-lookup"><span data-stu-id="7612d-159">Topology Builder</span></span></p>
<p><span data-ttu-id="7612d-160">或</span><span class="sxs-lookup"><span data-stu-id="7612d-160">-or-</span></span></p>
<p><span data-ttu-id="7612d-161">Publish-CsTopology 和 Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="7612d-161">Publish-CsTopology and Enable-CsTopology</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-162">启用上次发布的拓扑</span><span class="sxs-lookup"><span data-stu-id="7612d-162">Enable the last published topology</span></span></p></td>
<td><p><span data-ttu-id="7612d-163">Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="7612d-163">Enable-CsTopology</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-164">重新安装 Lync Server 组件</span><span class="sxs-lookup"><span data-stu-id="7612d-164">Reinstall Lync Server components</span></span></p></td>
<td><p><span data-ttu-id="7612d-165">Lync Server 安装程序</span><span class="sxs-lookup"><span data-stu-id="7612d-165">Lync Server Setup</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="7612d-166">位于 Lync Server 安装文件夹或媒体中的 \setup\amd64\Setup.exe。</span><span class="sxs-lookup"><span data-stu-id="7612d-166">Located in the Lync Server installation folder or media at \setup\amd64\Setup.exe.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-167">还原位置信息 (E9-1-1) 数据 (.Lis) </span><span class="sxs-lookup"><span data-stu-id="7612d-167">Restore location information (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-168">Import-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="7612d-168">Import-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-169">还原永久性用户数据 (Rtcxds) </span><span class="sxs-lookup"><span data-stu-id="7612d-169">Restore persistent user data (Rtcxds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-170">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="7612d-170">Import-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-171">还原响应组配置数据 (RgsConfig) </span><span class="sxs-lookup"><span data-stu-id="7612d-171">Restore Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-172">Import-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="7612d-172">Import-CsRgsConfiguration</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="7612d-173">如果在数据库中没有响应组数据的新部署的池中还原配置，则应使用– OverwriteOwner 选项。</span><span class="sxs-lookup"><span data-stu-id="7612d-173">If the configuration is being restored in a newly deployed pool that has no Response Group data in the database, then you should use the –OverwriteOwner option.</span></span> <span data-ttu-id="7612d-174">即使正在还原的数据位于具有相同的完全限定域名的池中 (FQDN) ，也可使用此选项。</span><span class="sxs-lookup"><span data-stu-id="7612d-174">Use this option even if the data being restored is in a pool with the same fully qualified domain name (FQDN).</span></span> <span data-ttu-id="7612d-175">否则，导入将不会成功，原因是 Active Directory 中已存在对响应组的联系人对象。</span><span class="sxs-lookup"><span data-stu-id="7612d-175">Otherwise, the import will not succeed, due to the contact objects to the Response Groups already existing in Active Directory.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612d-176">还原以下数据库：</span><span class="sxs-lookup"><span data-stu-id="7612d-176">Restore the following databases:</span></span></p>
<ul>
<li><p><span data-ttu-id="7612d-177">将数据库存档 (LcsLog) </span><span class="sxs-lookup"><span data-stu-id="7612d-177">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="7612d-178">监视数据库：调用详细信息记录数据库 (LcsCDR) 和 QoE 数据库 (QoEMetrics) </span><span class="sxs-lookup"><span data-stu-id="7612d-178">Monitoring databases: call detail record database (LcsCDR.mdf) and QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7612d-179">SQL Server 数据库管理工具</span><span class="sxs-lookup"><span data-stu-id="7612d-179">SQL Server database management tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612d-180">持久聊天数据库 (Mgs) </span><span class="sxs-lookup"><span data-stu-id="7612d-180">Persistent Chat database (Mgs.mdf)</span></span></p></td>
<td><p><span data-ttu-id="7612d-181">SQL Server 还原过程或导入-CsPersistentChatData。</span><span class="sxs-lookup"><span data-stu-id="7612d-181">SQL Server restore procedures or Import-CsPersistentChatData.</span></span> <span data-ttu-id="7612d-182">你可以将 Import-CsPersistentChatData 用于使用 Export-CsPersistentChatData 创建的文件，并且数据将导入到持久聊天数据库中。</span><span class="sxs-lookup"><span data-stu-id="7612d-182">You can use Import-CsPersistentChatData with a file created by Export-CsPersistentChatData, and the data will be imported into the Persistent Chat database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="required-permissions"></a><span data-ttu-id="7612d-183">所需权限</span><span class="sxs-lookup"><span data-stu-id="7612d-183">Required Permissions</span></span>

<span data-ttu-id="7612d-184">用户必须是 **RTCUniversalServerAdmins** 组的成员才能执行本主题中所述的所有命令。</span><span class="sxs-lookup"><span data-stu-id="7612d-184">Users must be a member of the **RTCUniversalServerAdmins** group to perform all the commands described in this topic.</span></span> <span data-ttu-id="7612d-185">大多数备份和还原命令不支持基于角色的访问控制 (RBAC) 。</span><span class="sxs-lookup"><span data-stu-id="7612d-185">Most backup and restore commands do not support role-based access control (RBAC).</span></span> <span data-ttu-id="7612d-186">有两个例外是持久聊天 cmdlet Export-CsPersistentChatData 和 Import-CsPersistentChatData，它必须由属于 CsPersistentChatAdministrator 组成员的用户运行。</span><span class="sxs-lookup"><span data-stu-id="7612d-186">Two exceptions are the Persistent Chat cmdlets Export-CsPersistentChatData and Import-CsPersistentChatData, which must be run by a user who is a member of the CsPersistentChatAdministrator group.</span></span> <span data-ttu-id="7612d-187">若要运行 Lync Server 部署向导，用户还必须是本地管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="7612d-187">To run Lync Server Deployment Wizard, a user must also be a member of the Local Adminstrators group.</span></span>

<span data-ttu-id="7612d-188"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7612d-188"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

