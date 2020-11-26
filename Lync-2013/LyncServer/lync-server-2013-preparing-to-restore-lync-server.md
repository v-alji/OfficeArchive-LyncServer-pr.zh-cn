---
title: Lync Server 2013：正在准备还原 Lync Server
description: Lync Server 2013：正在准备还原 Lync Server。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing to restore Lync Server
ms:assetid: 857e4e02-908e-433a-96c6-be1795a9cb61
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202179(v=OCS.15)
ms:contentKeyID: 51541490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1875a691cfb70a6a824ab19bfde3dee4d699e48a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424091"
---
# <a name="preparing-to-restore-lync-server-2013"></a><span data-ttu-id="b9d2c-103">准备还原 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9d2c-103">Preparing to restore Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9d2c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9d2c-104">

<span> </span></span></span>

<span data-ttu-id="b9d2c-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="b9d2c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="b9d2c-106">在出现故障后开始还原服务器和数据库之前，需要确定以下事项：</span><span class="sxs-lookup"><span data-stu-id="b9d2c-106">Before you begin restoring servers and databases after a failure, you need to determine the following:</span></span>

  - <span data-ttu-id="b9d2c-107">需要还原哪些内容。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-107">What needs to be restored.</span></span>

  - <span data-ttu-id="b9d2c-108">您需要恢复的硬件、软件、数据和工具。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-108">The hardware, software, data, and tools you need for restoration.</span></span>

<div>

## <a name="determining-what-to-restore"></a><span data-ttu-id="b9d2c-109">确定要还原的内容</span><span class="sxs-lookup"><span data-stu-id="b9d2c-109">Determining What to Restore</span></span>

<span data-ttu-id="b9d2c-110">本主题介绍如何还原在服务器、池或中央管理存储级别发生的 Lync 服务器中断。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-110">This topic describes how to restore Lync Server outages that occur at the server, pool, or Central Management store level.</span></span> <span data-ttu-id="b9d2c-111">如果中央管理存储失败，则 Lync Server 部署将继续正常运行，但不能更改任何配置。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-111">If the Central Management store fails, your Lync Server deployment continues to function, but you cannot make any configuration changes.</span></span> <span data-ttu-id="b9d2c-112">如果后端服务器或标准版服务器出现故障，用户池将停止运行。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-112">If a Back End Server or Standard Edition server fails, the user pool stops functioning.</span></span> <span data-ttu-id="b9d2c-113">如果任何其他服务器出现故障，则故障的大小取决于服务器运行的服务器角色以及服务器托管一个还是多个数据库。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-113">If any other server fails, the magnitude of the failure depends on the server role the server is running and whether the server hosts one or more databases.</span></span>

### <a name="what-to-restore"></a><span data-ttu-id="b9d2c-114">还原内容</span><span class="sxs-lookup"><span data-stu-id="b9d2c-114">What to Restore</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9d2c-115">如果此操作失败</span><span class="sxs-lookup"><span data-stu-id="b9d2c-115">If this failed</span></span></th>
<th><span data-ttu-id="b9d2c-116">请参阅以下部分：</span><span class="sxs-lookup"><span data-stu-id="b9d2c-116">See this section:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9d2c-117">Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="b9d2c-117">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">在 Lync Server 2013 中还原标准版服务器</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9d2c-119">中央管理存储</span><span class="sxs-lookup"><span data-stu-id="b9d2c-119">Central Management store</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">在 Lync Server 2013 中还原托管中央管理存储的服务器</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Restoring the server hosting the Central Management store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9d2c-121">企业版后端</span><span class="sxs-lookup"><span data-stu-id="b9d2c-121">Enterprise Edition Back End</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">在 Lync Server 2013 中还原企业版后端服务器</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9d2c-123">企业版镜像后端主服务器</span><span class="sxs-lookup"><span data-stu-id="b9d2c-123">Enterprise Edition Mirrored Back End Primary Server</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">在 Lync Server 2013 中还原镜像的企业版后端服务器-主要</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9d2c-125">企业版镜像后端辅助服务器</span><span class="sxs-lookup"><span data-stu-id="b9d2c-125">Enterprise Edition Mirrored Back End Secondary Server</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">在 Lync Server 2013 中还原镜像的企业版后端服务器-镜像</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9d2c-127">任何运行服务器角色的企业版服务器，如前端服务器、边缘服务器、控制器、中介服务器、或持久聊天服务器。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-127">Any Enterprise Edition server running a server role, such as a Front End Server, Edge Server, Director, Mediation Server,.or Persistent Chat Server.</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">在 Lync Server 2013 中还原企业版成员服务器</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9d2c-129">整个 Lync 服务器池</span><span class="sxs-lookup"><span data-stu-id="b9d2c-129">An entire Lync Server pool</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">在 Lync Server 2013 中还原 Lync 服务器池</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">Restoring a Lync Server pool in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9d2c-131">企业版文件存储</span><span class="sxs-lookup"><span data-stu-id="b9d2c-131">Enterprise Edition File Store</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-132"><a href="lync-server-2013-restoring-a-file-store.md">在 Lync Server 2013 中还原文件存储</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-132"><a href="lync-server-2013-restoring-a-file-store.md">Restoring a file store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9d2c-133">独立监视数据库或存档数据库</span><span class="sxs-lookup"><span data-stu-id="b9d2c-133">A standalone Monitoring database or Archiving database</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">在 Lync Server 2013 中还原监视或存档数据</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Restoring monitoring or archiving data in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9d2c-135">独立的持久聊天数据库</span><span class="sxs-lookup"><span data-stu-id="b9d2c-135">A stand-alone Persistent Chat database</span></span></p></td>
<td><p><span data-ttu-id="b9d2c-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">在 Lync Server 2013 中还原永久聊天数据</a></span><span class="sxs-lookup"><span data-stu-id="b9d2c-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">Restoring Persistent Chat data in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="gathering-hardware-software-and-tools"></a><span data-ttu-id="b9d2c-137">收集硬件、软件和工具</span><span class="sxs-lookup"><span data-stu-id="b9d2c-137">Gathering Hardware, Software, and Tools</span></span>

<span data-ttu-id="b9d2c-138">还原服务器时，需要从新的或全新的计算机开始。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-138">When you restore a server, you need to start with a new or clean computer.</span></span> <span data-ttu-id="b9d2c-139">此外，你必须具有以下可用硬件和软件：</span><span class="sxs-lookup"><span data-stu-id="b9d2c-139">Additionally, you must have the following hardware and software available:</span></span>

  - <span data-ttu-id="b9d2c-140">具有相同的完全限定的域名的干净或新服务器 (FQDN) 为失败的服务器。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-140">A clean or new server with the same fully qualified domain name (FQDN) as the server that failed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b9d2c-141">在安装操作系统时，请确保不要删除 Active Directory 域服务中的计算机帐户，并验证是否保留帐户的组权限。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-141">When you install the operating system, make sure that you do not delete the computer account in Active Directory Domain Services, and verify that the group permissions for the account are retained.</span></span>

    
    </div>

  - <span data-ttu-id="b9d2c-142">操作系统的安装软件。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-142">Installation software for the operating system.</span></span> <span data-ttu-id="b9d2c-143">若要安装操作系统，请使用服务器部署过程和由你的组织建立的配置。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-143">To install the operating system, use the server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="b9d2c-144">还原服务时，应具备这些过程和配置要求。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-144">You should have these procedures and configuration requirements available when you restore service.</span></span>

  - <span data-ttu-id="b9d2c-145">SQL Server 2012 或 SQL Server 2008 R2 的安装软件。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-145">Installation software for SQL Server 2012 or SQL Server 2008 R2.</span></span> <span data-ttu-id="b9d2c-146">若要安装数据库服务器，请使用相应版本的 SQL Server 和由你的组织建立的数据库服务器部署过程和配置。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-146">To install a database server, use the appropriate version of SQL Server and the database server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="b9d2c-147">还原服务时，应具备这些过程和配置要求。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-147">You should have these procedures and configuration requirements available when you restore service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b9d2c-148">在安装本地配置存储时，Lync Server 部署向导会在每个标准版服务器和任何其他 Lync Server 服务器上自动安装 SQL Server 2012 Express，除非已在服务器上预安装了 SQL Server 2012 或 SQL Server 2008 R2。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-148">The Lync Server Deployment Wizard automatically installs SQL Server 2012 Express on each Standard Edition server and on any other Lync Server server when a local configuration store is installed, unless you have preinstalled SQL Server 2012 or SQL Server 2008 R2 on the server.</span></span>

    
    </div>

  - <span data-ttu-id="b9d2c-149">用于拍摄系统映像的软件。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-149">Software for taking system images.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="b9d2c-150">我们建议你在安装操作系统和 SQL Server 之后以及开始还原之前获取系统的映像副本，以便你可以将此映像用作回退点，以防还原过程中出现错误。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-150">We recommend that you take an image copy of the system after you install the operating system and SQL Server, and before you start restoration, so that you can use this image as a rollback point in case something goes wrong during restoration.</span></span>

    
    </div>

  - <span data-ttu-id="b9d2c-151">Lync Server 2013 安装软件。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-151">Lync Server 2013 installation software.</span></span> <span data-ttu-id="b9d2c-152">Lync Server 部署向导位于 Lync Server 安装文件夹或位于 \\ 安装 amd64Setup.exe 的媒体中 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-152">The Lync Server Deployment Wizard is located in the Lync Server installation folder or media at \\setup\\amd64\\Setup.exe.</span></span>

<span data-ttu-id="b9d2c-153">在还原期间，你可以使用以下工具：</span><span class="sxs-lookup"><span data-stu-id="b9d2c-153">During restoration, you use the following tools:</span></span>

  - <span data-ttu-id="b9d2c-154">Lync Server Management Shell cmdlet</span><span class="sxs-lookup"><span data-stu-id="b9d2c-154">Lync Server Management Shell cmdlets</span></span>

  - <span data-ttu-id="b9d2c-155">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="b9d2c-155">Import-CsUserData</span></span>

  - <span data-ttu-id="b9d2c-156">用于还原 Windows 文件夹的工具</span><span class="sxs-lookup"><span data-stu-id="b9d2c-156">Tools for restoring Windows folders</span></span>

  - <span data-ttu-id="b9d2c-157">拓扑生成器</span><span class="sxs-lookup"><span data-stu-id="b9d2c-157">Topology Builder</span></span>

  - <span data-ttu-id="b9d2c-158">SQL Server 数据库实用工具，例如 SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="b9d2c-158">SQL Server database utilities, such as SQL Server Management Studio</span></span>

</div>

<div>

## <a name="preparing-to-restore-a-server"></a><span data-ttu-id="b9d2c-159">准备还原服务器</span><span class="sxs-lookup"><span data-stu-id="b9d2c-159">Preparing to Restore a Server</span></span>

<span data-ttu-id="b9d2c-160">在还原服务器之前，必须执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="b9d2c-160">Before you restore the server, you must perform the following steps:</span></span>

1.  <span data-ttu-id="b9d2c-161">安装操作系统。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-161">Install the operating system.</span></span>

2.  <span data-ttu-id="b9d2c-162">如果服务器是后端服务器，请安装 SQL Server 2012 或 SQL Server 2008 R2。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-162">If the server is a Back End Server, install SQL Server 2012 or SQL Server 2008 R2.</span></span>

3.  <span data-ttu-id="b9d2c-163">还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-163">Restore or reenroll your certificates.</span></span> <span data-ttu-id="b9d2c-164">有关证书的详细信息，请参阅 [Lync Server 2013： data 中的 "备份和还原要求](lync-server-2013-backup-and-restoration-requirements-data.md)" 中的 "其他备份要求"。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-164">For details about certificates, see "Additional Backup Requirements" in [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md).</span></span>

4.  <span data-ttu-id="b9d2c-165">在启动还原之前获取系统的映像，以用作回滚点，以防还原过程中出现问题。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-165">Take an image of the system before starting restoration to use as a rollback point, in case something goes wrong during restoration.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b9d2c-166">在本主题的过程中介绍的 Lync Server 部署向导和 cmdlet 以及相关主题，将所有必需的访问控制列表设置 (Acl) 。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-166">The Lync Server Deployment Wizard and cmdlets described in the procedures in this topic, and related topics, set all required access control lists (ACLs).</span></span>



</div>

<span data-ttu-id="b9d2c-167">验证在开始还原之前，验证你要还原的组件是否可用所需的硬件和软件。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-167">Verify that the hardware and the software that you need for the components that you plan to restore are available before you start restoration.</span></span> <span data-ttu-id="b9d2c-168">安装操作系统和 SQL Server 后，可以远程运行以下还原过程中的大部分步骤。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-168">After you install the operating system and SQL Server, most of the steps in the following restoration procedures can be run remotely.</span></span> <span data-ttu-id="b9d2c-169">这些过程中将注明异常。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-169">The exceptions are noted in the procedures.</span></span>

<span data-ttu-id="b9d2c-170">您还应了解您的组织的备份和还原计划以及上次备份中的信息，如本文档中的工作表中的信息 (有关详细信息，请参阅开始还原之前可用的 [Lync Server 2013) 的备份和还原工作表](lync-server-2013-backup-and-restoration-worksheets.md) 。</span><span class="sxs-lookup"><span data-stu-id="b9d2c-170">You should also have your organization's backup and restoration plan and the information from your last backup, such as the information in the worksheets in this document (for details, see [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)), available before you begin restoration.</span></span>

<span data-ttu-id="b9d2c-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9d2c-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

