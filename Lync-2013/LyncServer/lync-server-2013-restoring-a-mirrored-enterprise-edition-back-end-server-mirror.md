---
title: 还原镜像的企业版后端服务器-镜像
description: 还原镜像的企业版后端服务器-镜像。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a mirrored Enterprise Edition Back End Server - mirror
ms:assetid: 4b3c8eae-6f1f-4377-b39b-6699e725c517
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945626(v=OCS.15)
ms:contentKeyID: 51541471
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 011c0aaa10ffed6fef7d579dbc16993fd3341070
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436235"
---
# <a name="restoring-a-mirrored-enterprise-edition-back-end-server-in-lync-server-2013---mirror"></a><span data-ttu-id="4aa2d-103">在 Lync Server 2013 中还原镜像的企业版后端服务器-镜像</span><span class="sxs-lookup"><span data-stu-id="4aa2d-103">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4aa2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4aa2d-104">

<span> </span></span></span>

<span data-ttu-id="4aa2d-105">_**主题上次修改时间：** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="4aa2d-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="4aa2d-106">如果在镜像配置中有企业版后端服务器且只有镜像失败，请按照本部分中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-106">If you have an Enterprise Edition Back End Server in a mirrored configuration and only the mirror fails, follow the procedures in this section.</span></span> <span data-ttu-id="4aa2d-107">如果主数据库和镜像均失败，请参阅 [在 Lync Server 2013 中还原企业版后端服务器](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md)。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-107">If both the primary database and mirror fail, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span></span> <span data-ttu-id="4aa2d-108">如果只有主服务器出现故障，请参阅 [在 Lync server 2013 中还原镜像的企业版后端服务器-主要](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md)。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-108">If only the primary fails, see [Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md).</span></span> <span data-ttu-id="4aa2d-109">如果托管中央管理存储的数据库失败，请参阅 [在 Lync server 2013 中还原托管中央管理存储的服务器](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-109">If the database hosting the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span> <span data-ttu-id="4aa2d-110">如果不是后端服务器的企业版成员服务器出现故障，请参阅 [在 Lync server 2013 中还原企业版成员服务器](lync-server-2013-restoring-an-enterprise-edition-member-server.md)。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-110">If an Enterprise Edition member server that is not the Back End Server fails, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="4aa2d-111">我们建议你先拍摄系统的映像副本，然后再开始还原。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-111">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="4aa2d-112">你可以将此映像用作回退点，以防在还原过程中出现问题。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-112">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="4aa2d-113">您可能希望在安装操作系统和 SQL Server 后获取图像副本，并还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-113">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>

<div>

## <a name="to-restore-an-enterprise-edition-back-end-server-mirror-database"></a><span data-ttu-id="4aa2d-114">还原企业版后端服务器镜像数据库</span><span class="sxs-lookup"><span data-stu-id="4aa2d-114">To restore an Enterprise Edition Back End Server Mirror Database</span></span>

1.  <span data-ttu-id="4aa2d-115">从作为 RTCUniversalServerAdmins 组成员的用户帐户登录到前端服务器。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-115">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

2.  <span data-ttu-id="4aa2d-116">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="4aa2d-117">卸载镜像。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-117">Uninstall mirroring.</span></span> <span data-ttu-id="4aa2d-118">首先，键入以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="4aa2d-118">First, type the following cmdlet:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn <PrimaryServerFqdn> -SqlInstanceName <SQLInstance> -verbose
    
    <span data-ttu-id="4aa2d-119">例如：</span><span class="sxs-lookup"><span data-stu-id="4aa2d-119">For example:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn server4.contoso.com -SqlInstanceName archinst -verbose
    
    <span data-ttu-id="4aa2d-120">对此服务器上的所有数据库类型执行此操作。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-120">Do this for all database types on this server.</span></span>

4.  <span data-ttu-id="4aa2d-121">创建具有相同的完全限定域名的干净或新服务器 (FQDN)  (DB1.contoso.com) 作为故障计算机，安装操作系统，然后还原或重新注册证书。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-121">Create a clean or new server that has the same fully qualified domain name (FQDN) (DB1.contoso.com) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span> <span data-ttu-id="4aa2d-122">此服务器将作为新镜像运行。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-122">This server will function as the new mirror.</span></span>

5.  <span data-ttu-id="4aa2d-123">从 RTCUniversalServerAdmins 组成员的用户帐户登录到新服务器。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-123">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the new server.</span></span>

6.  <span data-ttu-id="4aa2d-124">安装 SQL Server 2012 或 SQL Server 2008 R2，使实例名称与失败之前保持相同。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-124">Install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>

7.  <span data-ttu-id="4aa2d-125">从作为 RTCUniversalServerAdmins 组成员的用户帐户登录到前端服务器。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-125">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

8.  <span data-ttu-id="4aa2d-126">使用拓扑生成器安装镜像数据库。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-126">Use Topology Builder to install the mirror database.</span></span> <span data-ttu-id="4aa2d-127">执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="4aa2d-127">Perform the following:</span></span>
    
      - <span data-ttu-id="4aa2d-128">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-128">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="4aa2d-129">右键单击 "Lync Server 2013" 节点，单击 " **拓扑结构**"，然后单击 " **安装数据库**"。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-129">Right-click the Lync Server 2013 node, click **Topology**, and then click **Install Database**.</span></span>
    
      - <span data-ttu-id="4aa2d-130">按照 **安装数据库** 向导操作。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-130">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="4aa2d-131">在 " **创建数据库** " 页面上，选择要重新创建的数据库。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-131">On the **Create databases** page, select the databases that you want to recreate.</span></span>
    
      - <span data-ttu-id="4aa2d-132">按照向导中的步骤操作，直到出现 " **创建镜像" 数据库** 的提示。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-132">Follow the wizard until a prompt of **Create Mirror Database** appears.</span></span> <span data-ttu-id="4aa2d-133">选择要安装的数据库并完成此过程。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-133">Select the database that you want to install and complete this process.</span></span>
        
        <div>
        

        > [!TIP]
        > <span data-ttu-id="4aa2d-134">你可以使用 <STRONG>CsMirrorDatabase</STRONG> cmdlet 配置镜像，而不是运行拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-134">Instead of running Topology Builder, you can use the <STRONG>Install-CsMirrorDatabase</STRONG> cmdlet to configure mirroring.</span></span> <span data-ttu-id="4aa2d-135">有关详细信息，请参阅 Lync Server Management Shell 文档。</span><span class="sxs-lookup"><span data-stu-id="4aa2d-135">For details, see the Lync Server Management Shell documentation.</span></span>

        
        <span data-ttu-id="4aa2d-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4aa2d-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

