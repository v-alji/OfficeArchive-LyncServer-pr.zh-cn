---
title: Lync Server 2013：还原监视或存档数据
description: Lync Server 2013：还原监视或存档数据。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring monitoring or archiving data
ms:assetid: 60118526-13bb-4b03-803e-6ffae219d436
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202175(v=OCS.15)
ms:contentKeyID: 51541483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 169a5da2d606b97c7cd3f59d6cbae3d4c584e6e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442521"
---
# <a name="restoring-monitoring-or-archiving-data-in-lync-server-2013"></a><span data-ttu-id="2f577-103">在 Lync Server 2013 中还原监视或存档数据</span><span class="sxs-lookup"><span data-stu-id="2f577-103">Restoring monitoring or archiving data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f577-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f577-104">

<span> </span></span></span>

<span data-ttu-id="2f577-105">_**主题上次修改时间：** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="2f577-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="2f577-106">恢复监视和存档数据无需在失败后获取 Lync 服务器并运行。</span><span class="sxs-lookup"><span data-stu-id="2f577-106">Restoring monitoring and archiving data is not required to get Lync Server up and running after a failure.</span></span> <span data-ttu-id="2f577-107">但是，如果监视和存档数据对你的组织至关重要，你将希望在重新创建数据库后还原数据。</span><span class="sxs-lookup"><span data-stu-id="2f577-107">However, if monitoring and archiving data is critical to your organization, you will want to restore the data after you re-create the databases.</span></span>

<span data-ttu-id="2f577-108">以下过程介绍了如何使用 SQL Server Management Studio 还原存档或监视数据。</span><span class="sxs-lookup"><span data-stu-id="2f577-108">The following procedure describes how to use SQL Server Management Studio to restore archiving or monitoring data.</span></span>

<div>

## <a name="to-restore-monitoring-or-archiving-data-from-a-backup-file"></a><span data-ttu-id="2f577-109">还原对备份文件中的数据进行监视或存档</span><span class="sxs-lookup"><span data-stu-id="2f577-109">To restore monitoring or archiving data from a backup file</span></span>

1.  <span data-ttu-id="2f577-110">以本地计算机上管理员组的成员或具有同等用户权限的组的成员身份登录到要还原的服务器。</span><span class="sxs-lookup"><span data-stu-id="2f577-110">Log on to the server that you are restoring as a member of the Administrators group on the local computer or a group with equivalent user rights.</span></span>

2.  <span data-ttu-id="2f577-111">打开 SQL Server Management Studio：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft sql Server 2012** " 或 " **microsoft sql server 2008 R2**"，然后单击 " **SQL server management Studio**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-111">Open SQL Server Management Studio: click **Start**, click **All Programs**, click **Microsoft SQL Server 2012** or **Microsoft SQL Server 2008 R2**, and then click **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="2f577-112">在 " **连接到服务器**" 中，通过至少提供服务器的名称和身份验证信息，连接到 SQL Server 实例。</span><span class="sxs-lookup"><span data-stu-id="2f577-112">In **Connect to Server**, connect to the SQL Server instance by providing at least the name of the server and the authentication information.</span></span>

4.  <span data-ttu-id="2f577-113">在 **对象资源管理器** 中，右键单击 " **数据库**"，然后单击 " **还原数据库**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-113">In **Object Explorer**, right-click **Databases**, and then click **Restore Database**.</span></span>

5.  <span data-ttu-id="2f577-114">在 " **选择页面**" 下，单击 " **常规**"，然后在 " **到数据库** " 中选择数据库名称，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2f577-114">Under **Select a page**, click **General**, and then in **To database** select the database name as follows:</span></span>
    
      - <span data-ttu-id="2f577-115">对于存档数据库，请选择 " **LcsLog**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-115">For an Archiving database, select **LcsLog**.</span></span>
    
      - <span data-ttu-id="2f577-116">有关 (CDR) 数据库的通话详细信息录制，请选择 " **LcsCDR**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-116">For a call detail recording (CDR) database, select **LcsCDR**.</span></span>
    
      - <span data-ttu-id="2f577-117">有关 (QoE) 数据库的体验质量，请选择 " **QoEMetrics**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-117">For a Quality of Experience (QoE) database, select **QoEMetrics**.</span></span>

6.  <span data-ttu-id="2f577-118">单击 " **从设备**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-118">Click **From device**.</span></span>

7.  <span data-ttu-id="2f577-119">在 " **选择要还原的备份集**" 下，单击备份文件，然后单击 " **还原**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-119">Under **Select the backup sets to restore**, click the backup file, and then click **Restore**.</span></span>

8.  <span data-ttu-id="2f577-120">在 " **选择页面**" 下，单击 " **选项**"，验证数据文件路径和日志路径是否位于正确的文件夹中，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="2f577-120">Under **Select a page**, click **Options**, verify that the data file path and log path are in the correct folder, and then click **OK**.</span></span>

</div>

<div>

## <a name="to-make-sure-that-access-control-lists-acls-are-correct"></a><span data-ttu-id="2f577-121">确保 (Acl) 的访问控制列表正确无误</span><span class="sxs-lookup"><span data-stu-id="2f577-121">To make sure that access control lists (ACLs) are correct</span></span>

1.  <span data-ttu-id="2f577-122">展开 " **数据库**"，展开 "存档" 或 "监视数据库"，展开 " **安全性**"，然后展开 " **用户**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-122">Expand **Databases**, expand the archiving or monitoring database, expand **Security**, and then expand **Users**.</span></span>

2.  <span data-ttu-id="2f577-123">验证域组 RTCComponentUniversalServices 是否作为用户存在。</span><span class="sxs-lookup"><span data-stu-id="2f577-123">Verify that the domain group RTCComponentUniversalServices exists as a user.</span></span>

3.  <span data-ttu-id="2f577-124">如果 " **用户**" 下不存在 RTCComponentUniversalServices，请执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="2f577-124">If RTCComponentUniversalServices does not exist under **Users**, do the following:</span></span>
    
    1.  <span data-ttu-id="2f577-125">右键单击 " **用户**"，然后单击 " **新建用户**"。</span><span class="sxs-lookup"><span data-stu-id="2f577-125">Right-click **Users**, and then click **New User**.</span></span>
    
    2.  <span data-ttu-id="2f577-126">在 " **登录名**" 中，键入缺少的组名 RTCComponentUniversalServices。</span><span class="sxs-lookup"><span data-stu-id="2f577-126">In **Login name**, type the missing group name, RTCComponentUniversalServices.</span></span>
    
    3.  <span data-ttu-id="2f577-127">在 " **数据库角色成员身份**" 下，选择 " **ServerRole** " 权限，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="2f577-127">Under **Database role membership**, select the **ServerRole** permission, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2f577-128">不需要重新启动存档或监视服务。</span><span class="sxs-lookup"><span data-stu-id="2f577-128">You do not need to restart the archiving or monitoring service.</span></span>

    
    <span data-ttu-id="2f577-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f577-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

