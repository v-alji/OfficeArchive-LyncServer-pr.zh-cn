---
title: Lync Server 2013：还原标准版服务器
description: Lync Server 2013：还原标准版服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Standard Edition server
ms:assetid: d1845663-3138-4fd6-b3e7-337e294d40d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202190(v=OCS.15)
ms:contentKeyID: 51541519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2cd6976324492e0539c47999f78434e1a82706
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436221"
---
# <a name="restoring-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="18500-103">在 Lync Server 2013 中还原标准版服务器</span><span class="sxs-lookup"><span data-stu-id="18500-103">Restoring a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18500-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18500-104">

<span> </span></span></span>

<span data-ttu-id="18500-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="18500-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="18500-106">如果未托管中央管理存储的标准版服务器出现故障，请按照本部分中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="18500-106">If a Standard Edition server that does not host the Central Management store fails, follow the procedures in this section.</span></span> <span data-ttu-id="18500-107">如果中央管理存储失败，请参阅 [在 Lync server 2013 中还原托管中央管理存储的服务器](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)。</span><span class="sxs-lookup"><span data-stu-id="18500-107">If the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="18500-108">我们建议你先拍摄系统的映像副本，然后再开始还原。</span><span class="sxs-lookup"><span data-stu-id="18500-108">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="18500-109">你可以将此映像用作回退点，以防在还原过程中出现问题。</span><span class="sxs-lookup"><span data-stu-id="18500-109">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="18500-110">您可能希望在安装操作系统和 SQL Server 后获取图像副本，并还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="18500-110">You might want to take the image copy after you install the operating system and SQL Server, and restore or re-enroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-a-standard-edition-server"></a><span data-ttu-id="18500-111">还原标准版服务器</span><span class="sxs-lookup"><span data-stu-id="18500-111">To restore a Standard Edition server</span></span>

1.  <span data-ttu-id="18500-112">从具有相同的完全限定的域名的全新服务器开始， (FQDN) 作为失败的计算机，安装操作系统，然后还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="18500-112">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="18500-113">按照组织的服务器部署过程执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="18500-113">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="18500-114">从作为 RTCUniversalServerAdmins 组和本地管理员组成员的用户帐户，登录到要还原的服务器。</span><span class="sxs-lookup"><span data-stu-id="18500-114">From a user account that is a member of the RTCUniversalServerAdmins group and the Local Administrators group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="18500-115">通过将相应的文件存储从 $Backup 复制到服务器上的文件存储位置并共享该文件夹，还原文件存储。</span><span class="sxs-lookup"><span data-stu-id="18500-115">Restore the File Store by copying the appropriate File Store from $Backup to the File Store location on the server and share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="18500-116">已还原文件存储的路径和文件名应与备份的文件存储完全相同，以便使用这些文件的组件可以访问它们。</span><span class="sxs-lookup"><span data-stu-id="18500-116">The path and file name for the restored File Store should be exactly the same as the backed up File Store so that components that use the files can access them.</span></span>

    
    </div>

4.  <span data-ttu-id="18500-117">运行拓扑生成器：</span><span class="sxs-lookup"><span data-stu-id="18500-117">Run Topology Builder:</span></span>
    
    1.  <span data-ttu-id="18500-118">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="18500-118">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
    2.  <span data-ttu-id="18500-119">单击 " **从现有部署下载拓扑**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="18500-119">Click **Download Topology from existing deployment**, and then click **OK**.</span></span>
    
    3.  <span data-ttu-id="18500-120">选择拓扑，然后单击 " **保存**"。</span><span class="sxs-lookup"><span data-stu-id="18500-120">Select the topology, and then click **Save**.</span></span> <span data-ttu-id="18500-121">单击 **"是"** 以确认您的选择。</span><span class="sxs-lookup"><span data-stu-id="18500-121">Click **Yes** to confirm your selection.</span></span>

5.  <span data-ttu-id="18500-122">通过浏览找到 Lync Server 安装文件夹或媒体，然后启动位于 \\ 安装 amd64Setup.exe 的 Lync Server 部署向导 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="18500-122">Browse to the Lync Server installation folder or media, and then start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="18500-123">使用 Lync Server 部署向导执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="18500-123">Use the Lync Server Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="18500-124">运行 **步骤1：安装本地配置存储** 以安装本地配置文件。</span><span class="sxs-lookup"><span data-stu-id="18500-124">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="18500-125">运行 **步骤2：设置或删除 Lync Server 组件** 以安装 lync server 服务器角色。</span><span class="sxs-lookup"><span data-stu-id="18500-125">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server roles.</span></span>
    
    3.  <span data-ttu-id="18500-126">运行 **步骤3：请求、安装或分配证书** 以分配证书。</span><span class="sxs-lookup"><span data-stu-id="18500-126">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="18500-127">运行 **步骤4：启动服务** 以启动服务器上的服务。</span><span class="sxs-lookup"><span data-stu-id="18500-127">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="18500-128">有关运行部署向导的详细信息，请参阅要还原的服务器角色的部署文档。</span><span class="sxs-lookup"><span data-stu-id="18500-128">For details about running the Deployment Wizard, see the Deployment documentation for the server role you are restoring.</span></span>

6.  <span data-ttu-id="18500-129">通过执行下列操作还原用户数据：</span><span class="sxs-lookup"><span data-stu-id="18500-129">Restore user data by performing the following:</span></span>
    
    1.  <span data-ttu-id="18500-130">将 ExportedUserData.zip 从 $Backup 复制 \\ 到本地目录。</span><span class="sxs-lookup"><span data-stu-id="18500-130">Copy ExportedUserData.zip from $Backup\\ to a local directory.</span></span>
    
    2.  <span data-ttu-id="18500-131">还原用户数据之前，必须停止 Lync 服务。</span><span class="sxs-lookup"><span data-stu-id="18500-131">Before you restore the user data, you must stop Lync services.</span></span> <span data-ttu-id="18500-132">若要执行此操作，请键入：</span><span class="sxs-lookup"><span data-stu-id="18500-132">To do so, type:</span></span>
        
            Stop-CsWindowsService
    
    3.  <span data-ttu-id="18500-133">若要还原用户数据，请在命令行键入：</span><span class="sxs-lookup"><span data-stu-id="18500-133">To restore the user data, at the command line, type:</span></span>
        
            Import-CsUserData -PoolFqdn <Fqdn> -FileName <String>
        
        <span data-ttu-id="18500-134">例如：</span><span class="sxs-lookup"><span data-stu-id="18500-134">For example:</span></span>
        
            Import-CsUserData -PoolFqdn "atl0cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserDatal.zip"
    
    4.  <span data-ttu-id="18500-135">通过键入以下内容重启 Lync 服务：</span><span class="sxs-lookup"><span data-stu-id="18500-135">Restart Lync services by typing:</span></span>
        
            Start-CsWindowsService

7.  <span data-ttu-id="18500-136">如果你在此标准版服务器上部署了响应组，请还原响应组配置数据。</span><span class="sxs-lookup"><span data-stu-id="18500-136">If you deployed Response Group on this Standard Edition server, restore the Response Group configuration data.</span></span> <span data-ttu-id="18500-137">有关详细信息，请参阅 [在 Lync Server 2013 中还原响应组设置](lync-server-2013-restoring-response-group-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="18500-137">For details, see [Restoring Response Group settings in Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span></span>

8.  <span data-ttu-id="18500-138">如果你已在此标准版服务器上部署持久聊天，请还原持久聊天数据库 (mgc) 。</span><span class="sxs-lookup"><span data-stu-id="18500-138">If you deployed Persistent Chat on this Standard Edition server, restore the Persistent Chat database (mgc.mdf).</span></span>
    
    <span data-ttu-id="18500-139">如果使用 SQL Server 备份备份持久聊天数据库，请使用 SQL Server 还原过程还原它。</span><span class="sxs-lookup"><span data-stu-id="18500-139">If you used SQL Server Backup to back up the Persistent Chat database, use SQL Server restore procedures to restore it.</span></span>
    
    <span data-ttu-id="18500-140">如果使用 Export-CsPersistentChatData cmdlet 对其进行备份，请使用 Import-CsPersistentChatData 还原它。</span><span class="sxs-lookup"><span data-stu-id="18500-140">If you used the Export-CsPersistentChatData cmdlet to back it up, use the Import-CsPersistentChatData to restore it.</span></span>

<span data-ttu-id="18500-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18500-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

