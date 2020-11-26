---
title: Lync Server 2013：在主镜像和日志传送辅助数据库之间设置 SQL Server 日志传送
description: Lync Server 2013：在主镜像和日志传送辅助数据库之间设置 SQL Server 日志传送。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database
ms:assetid: 4e8e9ce9-4301-47f2-a0c3-669afeb53295
ms:mtpsurl: https://technet.microsoft.com/library/JJ204887(v=OCS.15)
ms:contentKeyID: 48184119
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b1655721410da23d569af4df7aa656f3be69e383
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423958"
---
# <a name="setting-up-sql-server-log-shipping-between-the-primary-mirror-and-the-log-shipping-secondary-database-in-lync-server-2013"></a><span data-ttu-id="46296-103">在 Lync Server 2013 中在主镜像和日志传送辅助数据库之间设置 SQL Server 日志传送</span><span class="sxs-lookup"><span data-stu-id="46296-103">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46296-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46296-104">

<span> </span></span></span>

<span data-ttu-id="46296-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="46296-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="46296-106">如果主持久聊天数据库故障转移到其镜像数据库，请执行以下步骤，以使日志传送继续进行。</span><span class="sxs-lookup"><span data-stu-id="46296-106">Perform the following steps for log shipping to continue if the primary Persistent Chat database is failed over to its mirror database.</span></span>

1.  <span data-ttu-id="46296-107">将主持久聊天数据库手动故障转移到镜像。</span><span class="sxs-lookup"><span data-stu-id="46296-107">Manually fail over the primary Persistent Chat database to the mirror.</span></span> <span data-ttu-id="46296-108">这可通过使用 Lync Server 命令行管理程序和 **CsDatabaseFailover** cmdlet 来完成。</span><span class="sxs-lookup"><span data-stu-id="46296-108">This is done by using the Lync Server Management Shell and the **Invoke-CsDatabaseFailover** cmdlet.</span></span> <span data-ttu-id="46296-109">有关详细信息，请参阅在 [Lync server 2013 中部署 SQL 镜像以获得后端服务器高可用性](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)的 "使用 Lync Server Management Shell cmdlet"。</span><span class="sxs-lookup"><span data-stu-id="46296-109">For details, see "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

2.  <span data-ttu-id="46296-110">使用 SQL Server Management Studio 连接到主持久聊天服务器镜像实例。</span><span class="sxs-lookup"><span data-stu-id="46296-110">Using the SQL Server Management Studio, connect to the primary Persistent Chat Server mirror instance.</span></span>

3.  <span data-ttu-id="46296-111">请确保 SQL Server 代理正在运行。</span><span class="sxs-lookup"><span data-stu-id="46296-111">Be sure that the SQL Server Agent is running.</span></span>

4.  <span data-ttu-id="46296-112">右键单击 mgc 数据库，然后单击“**属性**”。</span><span class="sxs-lookup"><span data-stu-id="46296-112">Right-click the mgc database, and then click **Properties**.</span></span>

5.  <span data-ttu-id="46296-113">在“**选择页**”下，单击“**事务日志传送**”。</span><span class="sxs-lookup"><span data-stu-id="46296-113">Under **Select a page**, click **Transaction Log Shipping**.</span></span>

6.  <span data-ttu-id="46296-114">选中“**将此数据库启用为日志传送配置中的主数据库**”复选框。</span><span class="sxs-lookup"><span data-stu-id="46296-114">Select the **Enable this as a primary database in a log shipping configuration** check box.</span></span>

7.  <span data-ttu-id="46296-115">在“**事务日志备份**”下，单击“**备份设置**”。</span><span class="sxs-lookup"><span data-stu-id="46296-115">Under **Transaction log backups**, click **Backup Settings**.</span></span>

8.  <span data-ttu-id="46296-116">在 " **备份文件夹的网络路径** " 框中，键入为 "事务日志备份" 文件夹创建的共享的网络路径。</span><span class="sxs-lookup"><span data-stu-id="46296-116">In the **Network path to the backup folder** box, type the network path to the share you created for the transaction log backup folder.</span></span>

9.  <span data-ttu-id="46296-117">如果备份文件夹位于主服务器上，请在 " **如果备份文件夹位于主服务器上** " 中键入备份文件夹的本地路径，请在 "文件夹" 框中键入本地路径。</span><span class="sxs-lookup"><span data-stu-id="46296-117">If the backup folder is located on the primary server, type the local path to the backup folder in the **If the backup folder is located on the primary server, type a local path to the folder** box.</span></span> <span data-ttu-id="46296-118"> (如果备份文件夹不在主服务器上，可以将此框保留为空。 ) </span><span class="sxs-lookup"><span data-stu-id="46296-118">(If the backup folder is not on the primary server, you can leave this box empty.)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="46296-119">如果主服务器上的 SQL Server 服务帐户在本地系统帐户下运行，则必须在主服务器上创建备份文件夹，并指定该文件夹的本地路径。</span><span class="sxs-lookup"><span data-stu-id="46296-119">If the SQL Server service account on your primary server runs under the local system account, you must create your backup folder on the primary server and specify a local path to that folder.</span></span>

    
    </div>

10. <span data-ttu-id="46296-120">配置“**删除文件，如果其保留时间超过**”和“**在以下时间内没有执行备份时报警**”参数。</span><span class="sxs-lookup"><span data-stu-id="46296-120">Configure the **Delete files older than** and **Alert if no backup occurs within** parameters.</span></span>

11. <span data-ttu-id="46296-121">查看“**备份作业**”下的“**计划**”框中所列的备份计划。</span><span class="sxs-lookup"><span data-stu-id="46296-121">Look at the backup schedule listed in the **Schedule** box under **Backup job**.</span></span> <span data-ttu-id="46296-122">若要自定义安装的计划，请单击 " **计划**"，然后根据需要调整 SQL Server 代理计划。</span><span class="sxs-lookup"><span data-stu-id="46296-122">To customize the schedule for your installation, click **Schedule**, and adjust the SQL Server Agent schedule, as required.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="46296-123">使用您用于主数据库的相同设置。</span><span class="sxs-lookup"><span data-stu-id="46296-123">Use the same settings that you used for the primary database.</span></span>

    
    </div>

12. <span data-ttu-id="46296-124">在 " **压缩**" 下，选择 " **使用默认服务器设置**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="46296-124">Under **Compression**, select **Use the default server setting**, and click **OK**.</span></span>

13. <span data-ttu-id="46296-125">在“**辅助服务器实例和数据库**”下，单击“**添加**”。</span><span class="sxs-lookup"><span data-stu-id="46296-125">Under **Secondary server instances and databases**, click **Add**.</span></span>

14. <span data-ttu-id="46296-126">单击 " **连接**"，并连接到已配置为辅助服务器的 SQL Server 实例。</span><span class="sxs-lookup"><span data-stu-id="46296-126">Click **Connect**, and connect to the instance of SQL Server that you have configured as your secondary server.</span></span>

15. <span data-ttu-id="46296-127">在“**辅助数据库**”框中，从列表中选择“**mgc**”数据库。</span><span class="sxs-lookup"><span data-stu-id="46296-127">In the **Secondary Database** box, select the **mgc** database from the list.</span></span>

16. <span data-ttu-id="46296-128">在 " **初始化辅助数据库** " 选项卡上，选择 " **否，辅助数据库已初始化**"。</span><span class="sxs-lookup"><span data-stu-id="46296-128">On the **Initialize Secondary database** tab, select the option **No, the secondary database is initialized**.</span></span>

17. <span data-ttu-id="46296-129">在 " **复制** 文件" 选项卡上，在 " **复制的文件的目标文件夹**" 中，键入应将事务日志备份复制到其中的文件夹的路径，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="46296-129">On the **Copy Files** tab, in **Destination folder for copied files**, type the path of the folder into which the transaction logs backups should be copied, and click **OK**.</span></span> <span data-ttu-id="46296-130">此文件夹通常位于辅助服务器上。</span><span class="sxs-lookup"><span data-stu-id="46296-130">This folder is often located on the secondary server.</span></span>

18. <span data-ttu-id="46296-131">打开 " **脚本配置** " 下拉列表，然后选择 " **对新查询进行脚本配置" 窗口**。</span><span class="sxs-lookup"><span data-stu-id="46296-131">Open the **Script Configuration** drop-down list, and select **Script Configuration to New Query Window**.</span></span>

19. <span data-ttu-id="46296-132">在 "新建查询" 窗口的 " **数据库属性**" 中，单击 **"确定"** 开始配置过程。</span><span class="sxs-lookup"><span data-stu-id="46296-132">In the new query window, in **Database Properties**, click **OK** to begin the configuration process.</span></span>

20. <span data-ttu-id="46296-133">选择并运行查询的前半部分 (查看第 18) 行：- \* \* \* \* \* \* 结束：要在主 \* \* \* \* \* \* 目录中运行的脚本：。</span><span class="sxs-lookup"><span data-stu-id="46296-133">Select and run the first half of the query (see step 18) up to the line: -- \*\*\*\*\*\* End: Script to be run at Primary: \*\*\*\*\*\*.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="46296-134">必须手动运行此脚本，因为 SQL Server Management Studio 不支持 SQL Server 日志传送配置中的多个主数据库。</span><span class="sxs-lookup"><span data-stu-id="46296-134">Manually running this script is necessary because SQL Server Management Studio does not support multiple primary databases in a SQL Server Log Shipping configuration.</span></span>

    
    </div>

21. <span data-ttu-id="46296-135">选择 " **取消** " 以关闭日志文件传输配置面板，并建立工作设置，以便在故障转移) 时正确实现主数据库和镜像 (数据库的日志文件传送。</span><span class="sxs-lookup"><span data-stu-id="46296-135">Select **Cancel** to close the Log File shipping configuration panel and to establish a working setup that correctly implements the log file shipping for both the primary and mirrored database (in case of failover).</span></span>

22. <span data-ttu-id="46296-136">将主持久聊天数据库手动故障恢复到主数据库。</span><span class="sxs-lookup"><span data-stu-id="46296-136">Manually fail back the primary Persistent Chat database to the primary.</span></span> <span data-ttu-id="46296-137">这可通过使用 Lync Server 命令行管理程序和 **CsDatabaseFailover** cmdlet 来完成。</span><span class="sxs-lookup"><span data-stu-id="46296-137">This is done by using the Lync Server Management Shell, and the **Invoke-CsDatabaseFailover** cmdlet.</span></span> <span data-ttu-id="46296-138">有关详细信息，请参阅在 [Lync server 2013 中部署 SQL 镜像以获得后端服务器高可用性](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)的 "使用 Lync Server Management Shell cmdlet"。</span><span class="sxs-lookup"><span data-stu-id="46296-138">For details, see "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="46296-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46296-139">See Also</span></span>


[<span data-ttu-id="46296-140">在 Lync Server 2013 中针对后端服务器高可用性部署 SQL 镜像</span><span class="sxs-lookup"><span data-stu-id="46296-140">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)  
[<span data-ttu-id="46296-141">在 Lync Server 2013 中针对后端服务器高可用性部署 SQL 镜像</span><span class="sxs-lookup"><span data-stu-id="46296-141">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)  
  

<span data-ttu-id="46296-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46296-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

