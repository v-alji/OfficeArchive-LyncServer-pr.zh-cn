---
title: 还原镜像的企业版后端服务器-主服务器
description: 还原镜像的企业版后端服务器-主服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a mirrored Enterprise Edition Back End Server - primary
ms:assetid: bc555b46-70c5-4eee-ae91-e195df238293
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945648(v=OCS.15)
ms:contentKeyID: 51541512
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f186bc304dccc363e5a7e0bf89a2276043e361e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442584"
---
# <a name="restoring-a-mirrored-enterprise-edition-back-end-server-in-lync-server-2013---primary"></a><span data-ttu-id="da88e-103">在 Lync Server 2013 中还原镜像的企业版后端服务器-主要</span><span class="sxs-lookup"><span data-stu-id="da88e-103">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da88e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da88e-104">

<span> </span></span></span>

<span data-ttu-id="da88e-105">_**主题上次修改时间：** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="da88e-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="da88e-106">如果在镜像配置中有企业版后端服务器，并且只有主数据库出现故障，请按照本部分中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="da88e-106">If you have an Enterprise Edition Back End Server in a mirrored configuration and only the primary database fails, follow the procedures in this section.</span></span> <span data-ttu-id="da88e-107">如果主数据库和镜像均失败，请参阅 [在 Lync Server 2013 中还原企业版后端服务器](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md)。</span><span class="sxs-lookup"><span data-stu-id="da88e-107">If both the primary database and mirror fail, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span></span> <span data-ttu-id="da88e-108">如果只有镜像失败，请参阅 [在 Lync server 2013-镜像中还原镜像的企业版后端服务器](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md)。</span><span class="sxs-lookup"><span data-stu-id="da88e-108">If only the mirror fails, see [Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md).</span></span> <span data-ttu-id="da88e-109">如果托管中央管理存储的数据库失败，请参阅 [在 Lync server 2013 中还原托管中央管理存储的服务器](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)。</span><span class="sxs-lookup"><span data-stu-id="da88e-109">If the database hosting the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span> <span data-ttu-id="da88e-110">如果不是后端服务器的企业版成员服务器出现故障，请参阅 [在 Lync server 2013 中还原企业版成员服务器](lync-server-2013-restoring-an-enterprise-edition-member-server.md)。</span><span class="sxs-lookup"><span data-stu-id="da88e-110">If an Enterprise Edition member server that is not the Back End Server fails, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="da88e-111">我们建议你先拍摄系统的映像副本，然后再开始还原。</span><span class="sxs-lookup"><span data-stu-id="da88e-111">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="da88e-112">你可以将此映像用作回退点，以防在还原过程中出现问题。</span><span class="sxs-lookup"><span data-stu-id="da88e-112">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="da88e-113">您可能希望在安装操作系统和 SQL Server 后获取图像副本，并还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="da88e-113">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>

<span data-ttu-id="da88e-114">在本主题中，示例主数据库将具有完全限定的域名 (FQDN) 的 BE1.contoso.com，并且镜像数据库将具有 BE2.contoso.com 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="da88e-114">In this topic, the example primary database will have a fully qualified domain name (FQDN) of BE1.contoso.com, and the mirror database will have an FQDN of BE2.contoso.com.</span></span>

<div>

## <a name="to-restore-an-enterprise-edition-back-end-server-primary-database"></a><span data-ttu-id="da88e-115">还原企业版后端服务器主数据库</span><span class="sxs-lookup"><span data-stu-id="da88e-115">To restore an Enterprise Edition Back End Server Primary Database</span></span>

1.  <span data-ttu-id="da88e-116">从作为 RTCUniversalServerAdmins 组成员的用户帐户登录到前端服务器。</span><span class="sxs-lookup"><span data-stu-id="da88e-116">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

2.  <span data-ttu-id="da88e-117">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="da88e-118">强制所有已配置的数据库故障转移到镜像。</span><span class="sxs-lookup"><span data-stu-id="da88e-118">Force all of the configured databases to fail over to the Mirror.</span></span> <span data-ttu-id="da88e-119">对于您在此服务器上配置的每个数据库类型，请键入以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="da88e-119">For each of the database types that you have configured on this server, type the following cmdlet:</span></span>
    
        Invoke-CsDataBaseFailover -PoolFqdn <Pool FQDN> -DatabaseType <Configured Database Type> -NewPrincipal Mirror -Force -Verbose
    
    <span data-ttu-id="da88e-120">例如：</span><span class="sxs-lookup"><span data-stu-id="da88e-120">For example:</span></span>
    
        Invoke-CsDataBaseFailover -PoolFqdn pool0.vdomain.com -DatabaseType User -NewPrincipal Mirror -Force -Verbose
    
    <div>
    

    > [!WARNING]
    > <span data-ttu-id="da88e-121">如果你已将后端数据库配置为使用与见证的同步镜像，则自动故障转移。</span><span class="sxs-lookup"><span data-stu-id="da88e-121">If you have configured your back-end database to use synchronized mirroring with a witness, failover is automatic.</span></span>

    
    </div>

4.  <span data-ttu-id="da88e-122">完成故障转移后，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="da88e-122">After completing failover, perform the following:</span></span>
    
      - <span data-ttu-id="da88e-123">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-123">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="da88e-124">在后端服务器上禁用镜像：右键单击 " **企业版前端池** " 下的 "池"，然后选择 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-124">Disable mirroring on the Back End Server: Right-click on the pool under **Enterprise Edition Front End pools** and select **Edit Properties**.</span></span> <span data-ttu-id="da88e-125">在 " **常规** " 选项卡上的 " **关联**" 下，清除 " **启用 SQL Server 应用商店镜像** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="da88e-125">On the **General** tab, under **Associations**, clear the **Enable SQL Server store mirroring** check box.</span></span> <span data-ttu-id="da88e-126">根据需要执行此操作以进行存档和监视。</span><span class="sxs-lookup"><span data-stu-id="da88e-126">Do this for Archiving and Monitoring as necessary.</span></span> <span data-ttu-id="da88e-127">然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="da88e-127">Then click **OK**.</span></span>
    
      - <span data-ttu-id="da88e-128">右键单击 "Lync Server 2013" 节点，单击 " **拓扑**"，然后单击 " **发布**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-128">Right-click the Lync Server 2013 node, click **Topology**, and then click **Publish**.</span></span>
    
      - <span data-ttu-id="da88e-129">选择仍在运行的后端 (BE2.contoso.com) 新的 SQL 应用商店。</span><span class="sxs-lookup"><span data-stu-id="da88e-129">Select the still functioning backend (BE2.contoso.com) to be the new SQL store.</span></span> <span data-ttu-id="da88e-130">若要执行此操作，请右键单击 " **企业版前端池** " 下的 "池"，然后选择 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-130">To do this, right-click on the pool under **Enterprise Edition Front End pools** and select **Edit Properties**.</span></span> <span data-ttu-id="da88e-131">在 " **常规** " 选项卡上的 " **关联**" 下，在 BE2.contoso.com) 中的示例中，在 " **SQL Server 应用商店** " (字段中键入 "运行后端的 FQDN"。</span><span class="sxs-lookup"><span data-stu-id="da88e-131">On the **General** tab, under **Associations**, type the FQDN of the functioning backend in the **SQL Server store** field (in our example, BE2.contoso.com).</span></span>
    
      - <span data-ttu-id="da88e-132">右键单击 "Lync Server 2013" 节点，单击 " **拓扑**"，然后单击 " **发布**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-132">Right-click the Lync Server 2013 node, click **Topology**, and then click **Publish**.</span></span>
    
      - <span data-ttu-id="da88e-133">重启服务，以便每台服务器可以读取新拓扑。</span><span class="sxs-lookup"><span data-stu-id="da88e-133">Restart services so that each server can read the new topology.</span></span> <span data-ttu-id="da88e-134">从 Lync Server 命令行管理程序中，在属于此池的每个前端服务器上运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="da88e-134">From a Lync Server Management Shell, run the following cmdlets on each Front End Server that belongs to this pool:</span></span>
        
            Stop-CsWindowsService
            Start-CsWindowsService

5.  <span data-ttu-id="da88e-135">卸载镜像。</span><span class="sxs-lookup"><span data-stu-id="da88e-135">Uninstall mirroring.</span></span> <span data-ttu-id="da88e-136">从 Lync Server 命令行管理程序中，运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="da88e-136">From a Lync Server Management Shell, run the following cmdlet:</span></span>
    
        Uninstall-CsMirrorDatabase -DatabaseType User -SqlServerFqdn <MirrorServerFqdn> -SqlInstanceName <SQLInstance> -verbose
    
    <span data-ttu-id="da88e-137">例如：</span><span class="sxs-lookup"><span data-stu-id="da88e-137">For example:</span></span>
    
        Uninstall-CsMirrorDatabase -DatabaseType User -SqlServerFqdn DB2.contoso.com -SqlInstanceName rtc -verbose
    
    <span data-ttu-id="da88e-138">对此服务器上的所有数据库类型执行此操作。</span><span class="sxs-lookup"><span data-stu-id="da88e-138">Do this for all database types on this server.</span></span>

6.  <span data-ttu-id="da88e-139">创建具有相同 FQDN (的干净或新服务器在此示例中，DB1.contoso.com) 为失败的计算机，安装操作系统，然后还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="da88e-139">Create a clean or new server that has the same FQDN (in this example, DB1.contoso.com) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span> <span data-ttu-id="da88e-140">此服务器将作为新镜像运行。</span><span class="sxs-lookup"><span data-stu-id="da88e-140">This server will function as the new mirror.</span></span>

7.  <span data-ttu-id="da88e-141">从 RTCUniversalServerAdmins 组成员的用户帐户登录到新服务器。</span><span class="sxs-lookup"><span data-stu-id="da88e-141">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the new server.</span></span>

8.  <span data-ttu-id="da88e-142">安装 SQL Server 2012 或 SQL Server 2008 R2，使实例名称与失败之前保持相同。</span><span class="sxs-lookup"><span data-stu-id="da88e-142">Install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>

9.  <span data-ttu-id="da88e-143">从作为 RTCUniversalServerAdmins 组成员的用户帐户登录到前端服务器。</span><span class="sxs-lookup"><span data-stu-id="da88e-143">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

10. <span data-ttu-id="da88e-144">使用拓扑生成器安装镜像数据库。</span><span class="sxs-lookup"><span data-stu-id="da88e-144">Use Topology Builder to install mirror DB.</span></span> <span data-ttu-id="da88e-145">执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="da88e-145">Perform the following steps:</span></span>
    
      - <span data-ttu-id="da88e-146">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-146">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="da88e-147">在后端服务器上启用镜像。</span><span class="sxs-lookup"><span data-stu-id="da88e-147">Enable mirroring on the Back End Server.</span></span> <span data-ttu-id="da88e-148">若要执行此操作，请右键单击 " **企业版前端池** " 下的 "池"，然后选择 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-148">To do so, right-click on the pool under **Enterprise Edition Front End pools** and select **Edit Properties**.</span></span> <span data-ttu-id="da88e-149">在 " **常规** " 选项卡上的 " **关联**" 下，选中 " **启用 SQL Server 应用商店镜像** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="da88e-149">On the **General** tab, under **Associations**, select the **Enable SQL Server store mirroring** check box.</span></span> <span data-ttu-id="da88e-150">如果需要，还可执行存档和监视等操作。</span><span class="sxs-lookup"><span data-stu-id="da88e-150">Also do this for Archiving and Monitoring, if necessary.</span></span>
        
        <span data-ttu-id="da88e-151">然后，在 " **镜像 SQL Server 应用商店** " 字段中，键入新服务器的 FQDN (n 本示例的 BE1.contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="da88e-151">Then, in the **Mirroring SQL Server store** field, type the FQDN of the new server (n this example, BE1.contoso.com).</span></span> <span data-ttu-id="da88e-152">然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="da88e-152">Then click **OK**.</span></span>
    
      - <span data-ttu-id="da88e-153">右键单击 "Lync Server 2013" 节点，单击 " **拓扑结构**"，然后单击 " **安装数据库**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-153">Right-click the Lync Server 2013 node, click **Topology**, and then click **Install Database**.</span></span>
    
      - <span data-ttu-id="da88e-154">按照 **安装数据库** 向导操作。</span><span class="sxs-lookup"><span data-stu-id="da88e-154">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="da88e-155">在 " **创建数据库** " 页面上，选择要重新创建的数据库。</span><span class="sxs-lookup"><span data-stu-id="da88e-155">On the **Create databases** page, select the databases that you want to recreate.</span></span>
    
      - <span data-ttu-id="da88e-156">按照向导中的步骤操作，直到出现提示 " **创建镜像数据库**"。</span><span class="sxs-lookup"><span data-stu-id="da88e-156">Follow the wizard until you come to the prompt, **Create Mirror Database**.</span></span> <span data-ttu-id="da88e-157">选择要安装的数据库，然后完成此过程。</span><span class="sxs-lookup"><span data-stu-id="da88e-157">Select the database that you want to install, and complete this process.</span></span>

<span data-ttu-id="da88e-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da88e-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

