---
title: Lync Server 2013：还原托管中央管理存储的服务器
description: Lync Server 2013：还原托管中央管理存储的服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring the server hosting the Central Management store
ms:assetid: 3bd6c82c-07fb-4798-b8f9-e7c78a5a83d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202172(v=OCS.15)
ms:contentKeyID: 51541464
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0c07e4c6722695b2bfb4cb478a1f3eefa86b4eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442514"
---
# <a name="restoring-the-server-hosting-the-central-management-store-in-lync-server-2013"></a><span data-ttu-id="ef593-103">在 Lync Server 2013 中还原托管中央管理存储的服务器</span><span class="sxs-lookup"><span data-stu-id="ef593-103">Restoring the server hosting the Central Management store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef593-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef593-104">

<span> </span></span></span>

<span data-ttu-id="ef593-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ef593-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ef593-106">Lync 服务器部署具有单个中央管理存储，其副本将复制到运行 Lync Server 服务器角色的每台服务器。</span><span class="sxs-lookup"><span data-stu-id="ef593-106">A Lync Server deployment has a single Central Management store, a copy of which is replicated to each server running a Lync Server server role.</span></span> <span data-ttu-id="ef593-107">本主题介绍如何还原托管中央管理存储的后端服务器或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="ef593-107">This topic describes how to restore a Back End Server or Standard Edition server that hosts the Central Management store.</span></span>

<span data-ttu-id="ef593-108">若要查找中央管理服务器所在的池，请打开拓扑生成器，单击 " **Lync Server**"，然后在右窗格中的 " **中央管理服务器**" 下查找。</span><span class="sxs-lookup"><span data-stu-id="ef593-108">To find the pool where the Central Management Server is located, open Topology Builder, click **Lync Server**, and look in the right pane under **Central Management Server**.</span></span>

<span data-ttu-id="ef593-109">如果托管中央管理存储的后端服务器位于镜像设置中，并且镜像数据库仍正常运行，我们建议你对此仍运行的镜像进行备份，然后按照下面的还原过程使用此备份在主数据库和镜像数据库上执行完整还原。</span><span class="sxs-lookup"><span data-stu-id="ef593-109">If the Back End Server that hosts the Central Management store is in a mirrored setup and the mirror database is still functional, we recommend that you make a backup of this still-functioning mirror, and then perform a full restore on both the primary database and the mirror database, using this backup, by following the restoration procedure below.</span></span> <span data-ttu-id="ef593-110">这是必需的，因为后端还原需要修改和发布拓扑，并且只能在托管 CMS 的主数据库运行时执行此操作。</span><span class="sxs-lookup"><span data-stu-id="ef593-110">This is necessary because Back End restore requires modifying and publishing the topology, and this can be done only if the primary database hosting CMS is operational.</span></span> <span data-ttu-id="ef593-111">另请注意，如果无法发布拓扑，则无法交换主数据库角色和镜像数据库角色。</span><span class="sxs-lookup"><span data-stu-id="ef593-111">Also note that the primary and mirror database roles cannot be interchanged if the topology cannot be published.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ef593-112">如果未托管中央管理存储的后端服务器或标准版服务器已失败，请参阅 <A href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">在 Lync server 2013 中还原企业版后端服务器</A> 或 <A href="lync-server-2013-restoring-a-standard-edition-server.md">在 lync Server 2013 中还原标准版服务器</A>。</span><span class="sxs-lookup"><span data-stu-id="ef593-112">If a Back End Server or Standard Edition server that does not host the Central Management store failed, see <A href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</A> or <A href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</A>.</span></span> <span data-ttu-id="ef593-113">如果托管中央管理存储的后端服务器位于镜像配置中且只有镜像失败，请参阅 <A href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">在 Lync server 2013-镜像中还原镜像的企业版后端服务器</A>。</span><span class="sxs-lookup"><span data-stu-id="ef593-113">If a Back End Server that hosts the Central Management store is in a mirrored configuration and only the mirror failed, see <A href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</A>.</span></span> <span data-ttu-id="ef593-114">如果任何其他服务器出现故障，请参阅 <A href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">在 Lync server 2013 中还原企业版成员服务器</A>。</span><span class="sxs-lookup"><span data-stu-id="ef593-114">If any other server failed, see <A href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</A>.</span></span>



</div>

<div>


> [!TIP]  
> <span data-ttu-id="ef593-115">我们建议你先拍摄系统的映像副本，然后再开始还原。</span><span class="sxs-lookup"><span data-stu-id="ef593-115">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="ef593-116">你可以将此映像用作回退点，以防在还原过程中出现问题。</span><span class="sxs-lookup"><span data-stu-id="ef593-116">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="ef593-117">您可能希望在安装操作系统和 SQL Server 后获取图像副本，并还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="ef593-117">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-the-central-management-store"></a><span data-ttu-id="ef593-118">还原中央管理存储</span><span class="sxs-lookup"><span data-stu-id="ef593-118">To restore the Central Management store</span></span>

1.  <span data-ttu-id="ef593-119">从具有相同的完全限定的域名的全新服务器开始， (FQDN) 作为失败的计算机，安装操作系统，然后还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="ef593-119">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ef593-120">按照组织的服务器部署过程执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="ef593-120">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="ef593-121">从作为 RTCUniversalServerAdmins 组和本地管理员组成员的用户帐户，登录到要还原的服务器。</span><span class="sxs-lookup"><span data-stu-id="ef593-121">From a user account that is a member of the RTCUniversalServerAdmins group and the Local Administrators group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="ef593-122">如果要还原标准版服务器，请还原文件存储，方法是将相应的文件存储从 $Backup 复制到服务器上的文件存储位置，然后共享该文件夹。</span><span class="sxs-lookup"><span data-stu-id="ef593-122">If you are restoring a Standard Edition server, restore the File Store by copying the appropriate File Store from $Backup to the File Store location on the server, and then share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ef593-123">已还原文件存储的路径和文件名应与备份的文件存储完全相同，以便使用这些文件的组件可以访问它们。</span><span class="sxs-lookup"><span data-stu-id="ef593-123">The path and file name for the restored File Store should be exactly the same as the backed up File Store so that components that use the files can access them.</span></span>

    
    </div>

4.  <span data-ttu-id="ef593-124">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="ef593-124">Do one of the following:</span></span>
    
      - <span data-ttu-id="ef593-125">如果要安装标准版服务器，请通过浏览找到 Lync Server 安装文件夹或媒体，然后启动位于 \\ 安装 amd64Setup.exe 的 Lync Server 部署向导 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="ef593-125">If you are installing a Standard Edition server, browse to the Lync Server installation folder or media, and then start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="ef593-126">在部署向导中，单击 " **准备第一个标准版服务器** "，然后按照向导安装中央管理存储。</span><span class="sxs-lookup"><span data-stu-id="ef593-126">In the Deployment Wizard, click **Prepare first Standard Edition server** and follow the wizard to install the Central Management store.</span></span>
    
      - <span data-ttu-id="ef593-127">如果要安装企业后端服务器，请安装 SQL Server 2012 或 SQL Server 2008 R2，使实例名称保持与失败之前相同。</span><span class="sxs-lookup"><span data-stu-id="ef593-127">If you are installing an Enterprise Back End Server, install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="ef593-128">服务器可能包含多个 collocated 或单独的数据库，具体取决于你要还原的服务器和你的部署。</span><span class="sxs-lookup"><span data-stu-id="ef593-128">Depending on the server that you are restoring and on your deployment, the server might include multiple collocated or separate databases.</span></span> <span data-ttu-id="ef593-129">按照相同的步骤安装最初用于部署服务器的 SQL Server，包括 SQL Server 权限和登录。</span><span class="sxs-lookup"><span data-stu-id="ef593-129">Follow the same procedure to install SQL Server that you used originally to deploy the server, including SQL Server permissions and logins.</span></span>

        
        </div>

5.  <span data-ttu-id="ef593-130">从前端服务器，启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft lync server 2013**"，然后单击 " **Lync server Management Shell**"。</span><span class="sxs-lookup"><span data-stu-id="ef593-130">From a Front End Server, Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

6.  <span data-ttu-id="ef593-131">重新创建中央管理存储。</span><span class="sxs-lookup"><span data-stu-id="ef593-131">Re-create the Central Management store.</span></span> <span data-ttu-id="ef593-132">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="ef593-132">At the command line, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn <FQDN> -SqlInstanceName <instance name> -Verbose
    
    <span data-ttu-id="ef593-133">例如：</span><span class="sxs-lookup"><span data-stu-id="ef593-133">For example:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn Server01.contoso.com -SqlInstanceName cms -Verbose

7.  <span data-ttu-id="ef593-134">为中央管理存储设置 Active Directory 域服务控制点。</span><span class="sxs-lookup"><span data-stu-id="ef593-134">Set the Active Directory Domain Services control point for the Central Management store.</span></span> <span data-ttu-id="ef593-135">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="ef593-135">At the command line, type:</span></span>
    
        Set-CsConfigurationStoreLocation -SqlServerFqdn <FQDN> -SqlInstanceName <instance name> -Verbose
    
    <span data-ttu-id="ef593-136">例如：</span><span class="sxs-lookup"><span data-stu-id="ef593-136">For example:</span></span>
    
        Set-CsConfigurationStoreLocation -SqlServerFqdn Server01.contoso.com -SqlInstanceName cms -Verbose
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ef593-137">如果您丢失了连接点，则可以重新运行此 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef593-137">If you lose the connection point, you can rerun this cmdlet.</span></span>

    
    </div>

8.  <span data-ttu-id="ef593-138">从 $Backup 导入中央管理存储数据。</span><span class="sxs-lookup"><span data-stu-id="ef593-138">Import the Central Management store data from $Backup.</span></span> <span data-ttu-id="ef593-139">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="ef593-139">At the command line, type:</span></span>
    
        Import-CsConfiguration -FileName <CMS backup file name>
    
    <span data-ttu-id="ef593-140">例如：</span><span class="sxs-lookup"><span data-stu-id="ef593-140">For example:</span></span>
    
        Import-CsConfiguration -FileName "C:\Config.zip"

9.  <span data-ttu-id="ef593-141">启用刚进行的更改。</span><span class="sxs-lookup"><span data-stu-id="ef593-141">Enable the changes you have just made.</span></span> <span data-ttu-id="ef593-142">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="ef593-142">At the command line, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ef593-143">启用拓扑后，您可以在数据库中找到拓扑文档。</span><span class="sxs-lookup"><span data-stu-id="ef593-143">After you enable the topology, you can find the topology document in the database.</span></span>

    
    </div>

10. <span data-ttu-id="ef593-144">如果您要还原同时托管 CMS 的企业版后端服务器，或者需要重新创建 CMS 的镜像，请执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="ef593-144">If you are restoring an Enterprise Edition Back End Server that also hosted the CMS, or if you need to re-create a mirror of the CMS, then follow this step.</span></span> <span data-ttu-id="ef593-145">否则，请跳到步骤11。</span><span class="sxs-lookup"><span data-stu-id="ef593-145">Otherwise, skip to step 11.</span></span>
    
    <span data-ttu-id="ef593-146">通过执行下列操作来安装独立数据库：</span><span class="sxs-lookup"><span data-stu-id="ef593-146">Install the stand-alone databases by doing the following:</span></span>
    
    1.  <span data-ttu-id="ef593-147">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="ef593-147">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
    2.  <span data-ttu-id="ef593-148">单击 " **从现有部署下载拓扑**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="ef593-148">Click **Download Topology from existing deployment**, and then click **OK**.</span></span>
    
    3.  <span data-ttu-id="ef593-149">选择拓扑，然后单击 " **保存**"。</span><span class="sxs-lookup"><span data-stu-id="ef593-149">Select the topology, and then click **Save**.</span></span> <span data-ttu-id="ef593-150">单击 **"是"** 以确认您的选择。</span><span class="sxs-lookup"><span data-stu-id="ef593-150">Click **Yes** to confirm your selection.</span></span>
    
    4.  <span data-ttu-id="ef593-151">右键单击 " **Lync Server 2013** " 节点，然后单击 " **安装数据库**"。</span><span class="sxs-lookup"><span data-stu-id="ef593-151">Right-click the **Lync Server 2013** node, and then click **Install Database**.</span></span>
    
    5.  <span data-ttu-id="ef593-152">按照 **安装数据库** 向导操作。</span><span class="sxs-lookup"><span data-stu-id="ef593-152">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="ef593-153">如果你要还原的数据库不是此服务器上的中央管理存储，请在 " **创建数据库** " 页面上，选择要重新创建的数据库。</span><span class="sxs-lookup"><span data-stu-id="ef593-153">If you are restoring a database other than the Central Management store on this server, on the **Create databases** page, select the databases you want to recreate.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="ef593-154">" <STRONG>创建数据库</STRONG> " 页面上仅显示独立数据库。</span><span class="sxs-lookup"><span data-stu-id="ef593-154">Only stand-alone databases are displayed on the <STRONG>Create databases</STRONG> page.</span></span> <span data-ttu-id="ef593-155">Collocated 数据库是在运行 Lync Server 部署向导时创建的。</span><span class="sxs-lookup"><span data-stu-id="ef593-155">Collocated databases are created when you run the Lync Server Deployment Wizard.</span></span>

        
        </div>
    
    6.  <span data-ttu-id="ef593-156">如果你要还原镜像后端服务器，请继续按照向导的其余部分操作，直到你转到创建镜像数据库的提示。</span><span class="sxs-lookup"><span data-stu-id="ef593-156">If you are restoring a mirrored Back End Server, continue to follow the rest of the wizard until you come to a prompt of Create Mirror Database.</span></span> <span data-ttu-id="ef593-157">选择要安装的数据库，然后完成此过程。</span><span class="sxs-lookup"><span data-stu-id="ef593-157">Select the database you want to install, and complete the process.</span></span>
    
    7.  <span data-ttu-id="ef593-158">按照向导的其余部分，然后单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="ef593-158">Follow the rest of the wizard, and then click **Finish**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="ef593-159">你可以使用 <STRONG>CsDatabase</STRONG> cmdlet 创建每个数据库，使用 <STRONG>CsMirrorDatabase</STRONG> cmdlet 来配置镜像，而不是运行拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="ef593-159">Instead of running Topology Builder, you can use the <STRONG>Install-CsDatabase</STRONG> cmdlet to create each database, and the <STRONG>Install-CsMirrorDatabase</STRONG> cmdlet to configure mirroring.</span></span> <span data-ttu-id="ef593-160">有关详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsDatabase">安装 CsDatabase</A> 和 <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsMirrorDatabase">安装 CsMirrorDatabase</A>。</span><span class="sxs-lookup"><span data-stu-id="ef593-160">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsDatabase">Install-CsDatabase</A> and <A href="https://docs.microsoft.com/powershell/module/skype/Install-CsMirrorDatabase">Install-CsMirrorDatabase</A>.</span></span>

    
    </div>

11. <span data-ttu-id="ef593-161">如果你要还原标准版服务器，请浏览到 Lync Server 安装文件夹或媒体，然后启动位于 \\ 安装 amd64Setup.exe 的 Lync Server 部署向导 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="ef593-161">If you are restoring a Standard Edition server, browse to the Lync Server installation folder or media, and start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="ef593-162">使用 Lync Server 部署向导执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="ef593-162">Use the Lync Server Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="ef593-163">运行 **步骤1：安装本地配置存储** 以安装本地配置文件。</span><span class="sxs-lookup"><span data-stu-id="ef593-163">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="ef593-164">运行 **步骤2：设置或删除 Lync Server 组件** 以安装 lync server 服务器角色。</span><span class="sxs-lookup"><span data-stu-id="ef593-164">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server roles.</span></span>
    
    3.  <span data-ttu-id="ef593-165">运行 **步骤3：请求、安装或分配证书** 以分配证书。</span><span class="sxs-lookup"><span data-stu-id="ef593-165">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="ef593-166">运行 **步骤4：启动服务** 以启动服务器上的服务。</span><span class="sxs-lookup"><span data-stu-id="ef593-166">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="ef593-167">有关运行部署向导的详细信息，请参阅要还原的服务器角色的部署文档。</span><span class="sxs-lookup"><span data-stu-id="ef593-167">For details about running the Deployment Wizard, see the Deployment documentation for the server role that you are restoring.</span></span>

12. <span data-ttu-id="ef593-168">通过执行下列操作还原用户数据：</span><span class="sxs-lookup"><span data-stu-id="ef593-168">Restore user data by performing the following:</span></span>
    
    1.  <span data-ttu-id="ef593-169">将 ExportedUserData.zip 从 $Backup 复制 \\ 到本地目录。</span><span class="sxs-lookup"><span data-stu-id="ef593-169">Copy ExportedUserData.zip from $Backup\\ to a local directory.</span></span>
    
    2.  <span data-ttu-id="ef593-170">还原用户数据之前，必须停止 Lync 服务。</span><span class="sxs-lookup"><span data-stu-id="ef593-170">Before you restore the user data, you must stop Lync services.</span></span> <span data-ttu-id="ef593-171">若要执行此操作，请键入：</span><span class="sxs-lookup"><span data-stu-id="ef593-171">To do so, type:</span></span>
        
            Stop-CsWindowsService
    
    3.  <span data-ttu-id="ef593-172">若要还原用户数据，请在命令行键入：</span><span class="sxs-lookup"><span data-stu-id="ef593-172">To restore the user data, at the command line, type:</span></span>
        
            Import-CsUserData -PoolFqdn <Fqdn> -FileName <String>
        
        <span data-ttu-id="ef593-173">例如：</span><span class="sxs-lookup"><span data-stu-id="ef593-173">For example:</span></span>
        
            Import-CsUserData -PoolFqdn "atl0cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserDatal.zip"
    
    4.  <span data-ttu-id="ef593-174">通过键入以下内容重启 Lync 服务：</span><span class="sxs-lookup"><span data-stu-id="ef593-174">Restart Lync services by typing:</span></span>
        
            Start-CsWindowsService

13. <span data-ttu-id="ef593-175">将位置信息数据还原到中央管理存储。</span><span class="sxs-lookup"><span data-stu-id="ef593-175">Restore Location Information data to the Central Management store.</span></span> <span data-ttu-id="ef593-176">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="ef593-176">At the command line, type:</span></span>
    
        Import-CsLisConfiguration -FileName <LIS backup file name>
    
    <span data-ttu-id="ef593-177">例如：</span><span class="sxs-lookup"><span data-stu-id="ef593-177">For example:</span></span>
    
        Import-CsLisConfiguration -FileName "D:\E911Config.zip"

14. <span data-ttu-id="ef593-178">如果你已在此池或标准版服务器上部署了响应组，请还原响应组配置数据。</span><span class="sxs-lookup"><span data-stu-id="ef593-178">If you deployed Response Group on this pool or Standard Edition server, restore the Response Group configuration data.</span></span> <span data-ttu-id="ef593-179">有关详细信息，请参阅 [在 Lync Server 2013 中还原响应组设置](lync-server-2013-restoring-response-group-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="ef593-179">For details, see [Restoring Response Group settings in Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span></span>

15. <span data-ttu-id="ef593-180">如果要还原包括存档或监视数据库的后端服务器，请使用 SQL Server 管理工具（如 SQL Server Management Studio）还原存档或监视数据。</span><span class="sxs-lookup"><span data-stu-id="ef593-180">If you are restoring a Back End Server that includes Archiving or Monitoring databases, restore the Archiving or Monitoring data by using a SQL Server management tool, such as SQL Server Management Studio.</span></span> <span data-ttu-id="ef593-181">有关详细信息，请参阅 [在 Lync Server 2013 中还原监视或存档数据](lync-server-2013-restoring-monitoring-or-archiving-data.md)。</span><span class="sxs-lookup"><span data-stu-id="ef593-181">For details, see [Restoring monitoring or archiving data in Lync Server 2013](lync-server-2013-restoring-monitoring-or-archiving-data.md).</span></span>

<span data-ttu-id="ef593-182"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef593-182"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

