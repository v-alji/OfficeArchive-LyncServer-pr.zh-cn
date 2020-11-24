---
title: Lync Server 2013：设置用于存档的存储
description: Lync Server 2013：设置用于存档的存储。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up storage for Archiving
ms:assetid: f751245c-743e-454f-8325-968ae5e3de71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205392(v=OCS.15)
ms:contentKeyID: 48185858
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7ee431b17b31c49ace7fae1f90d79ec6de2ada4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391813"
---
# <a name="setting-up-storage-for-archiving-in-lync-server-2013"></a><span data-ttu-id="3dd60-103">在 Lync Server 2013 中设置用于存档的存储</span><span class="sxs-lookup"><span data-stu-id="3dd60-103">Setting up storage for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3dd60-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3dd60-104">

<span> </span></span></span>

<span data-ttu-id="3dd60-105">_**主题上次修改时间：** 2013-12-17_</span><span class="sxs-lookup"><span data-stu-id="3dd60-105">_**Topic Last Modified:** 2013-12-17_</span></span>

<span data-ttu-id="3dd60-106">Lync Server 2013 的存档存储包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="3dd60-106">Archiving storage for Lync Server 2013 includes the following:</span></span>

  - <span data-ttu-id="3dd60-107">**数据存储**   存储 IM 内容需要数据存储。</span><span class="sxs-lookup"><span data-stu-id="3dd60-107">**Data storage**   Data storage is required to store IM content.</span></span>

  - <span data-ttu-id="3dd60-108">**文件存储**   需要文件存储才能存储会议 (会议) 内容数据存储和文件存储。</span><span class="sxs-lookup"><span data-stu-id="3dd60-108">**File storage**   File storage is required to store conferencing (meeting) content data storage and file storage.</span></span>

<div>

## <a name="setting-up-data-storage"></a><span data-ttu-id="3dd60-109">设置数据存储</span><span class="sxs-lookup"><span data-stu-id="3dd60-109">Setting Up Data Storage</span></span>

<span data-ttu-id="3dd60-110">在 Lync Server 2013 中设置用于存档的数据存储的要求取决于您希望存储存档数据的方式：</span><span class="sxs-lookup"><span data-stu-id="3dd60-110">Requirements for setting up data storage for Archiving in Lync Server 2013 depend on how you want to store archiving data:</span></span>

  - <span data-ttu-id="3dd60-111">将 Lync Server 2013 存档与 Exchange 部署集成，以使用 Exchange 存储存储存档数据。</span><span class="sxs-lookup"><span data-stu-id="3dd60-111">Integrate Lync Server 2013 Archiving with your Exchange deployment to store Archiving data using Exchange storage.</span></span>

  - <span data-ttu-id="3dd60-112">设置单独的 SQL Server 数据库服务器以存储存档数据。</span><span class="sxs-lookup"><span data-stu-id="3dd60-112">Set up separate SQL Server database servers to store Archiving data.</span></span>

<div>

## <a name="setting-up-exchange-storage-for-archiving-data"></a><span data-ttu-id="3dd60-113">设置用于存档数据的 Exchange 存储</span><span class="sxs-lookup"><span data-stu-id="3dd60-113">Setting Up Exchange Storage for Archiving Data</span></span>

<span data-ttu-id="3dd60-114">设置用于存储存档数据的 Exchange 需要 Exchange 部署运行 Exchange 2013。</span><span class="sxs-lookup"><span data-stu-id="3dd60-114">Setting up Exchange for storage of Archiving data requires that your Exchange deployment is running Exchange 2013.</span></span> <span data-ttu-id="3dd60-115">此外，用户邮箱必须托管在 Exchange 2013 服务器上，并且其邮箱必须置于 In-Place 保留状态。</span><span class="sxs-lookup"><span data-stu-id="3dd60-115">Additionally, user mailboxes must be homed on the Exchange 2013 server and their mailboxes must be put on In-Place Hold.</span></span> <span data-ttu-id="3dd60-116">有关配置 Exchange 2013 的详细信息，请参阅 Exchange 产品文档。</span><span class="sxs-lookup"><span data-stu-id="3dd60-116">For details about configuring Exchange 2013, see the Exchange product documentation.</span></span>

</div>

<div>

## <a name="setting-up-sql-server-database-servers-for-storage-of-archiving-data"></a><span data-ttu-id="3dd60-117">设置用于存储存档数据的 SQL Server 数据库服务器</span><span class="sxs-lookup"><span data-stu-id="3dd60-117">Setting Up SQL Server Database Servers for Storage of Archiving Data</span></span>

<span data-ttu-id="3dd60-118">Lync Server 2013 中的存档需要 SQL Server 数据库软件存储已存档的数据，除非你将部署与 Exchange 集成。</span><span class="sxs-lookup"><span data-stu-id="3dd60-118">Archiving in Lync Server 2013 requires the SQL Server database software to store the archived data, unless you integrate your deployment with Exchange.</span></span>

<span data-ttu-id="3dd60-119">对于 SQL Server 存档数据库，必须在将托管存档数据库的计算机上安装 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="3dd60-119">For SQL Server archiving databases, you must install SQL Server on the computer that will host the Archiving database.</span></span> <span data-ttu-id="3dd60-120">你可以使用用于前端池的后端数据库的相同 SQL 实例。</span><span class="sxs-lookup"><span data-stu-id="3dd60-120">You can use the same SQL instance that you use for the back-end database of a Front End pool.</span></span> <span data-ttu-id="3dd60-121">为了获得最佳性能，你应该在独立于中央管理存储的计算机上部署存档数据库。</span><span class="sxs-lookup"><span data-stu-id="3dd60-121">For best performance, you should deploy the Archiving database on a computer that is separate from the Central Management store.</span></span> <span data-ttu-id="3dd60-122">有关 collocating Lync Server 2013 组件的详细信息，请参阅支持文档中的 [Lync server 2013 中的 "支持的服务器 collocation](lync-server-2013-supported-server-collocation.md) "。</span><span class="sxs-lookup"><span data-stu-id="3dd60-122">For details about collocating Lync Server 2013 components, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

<span data-ttu-id="3dd60-123">每个数据库服务器都必须运行受支持的 SQL Server 版本。</span><span class="sxs-lookup"><span data-stu-id="3dd60-123">Each database server must be running a supported version of SQL Server.</span></span> <span data-ttu-id="3dd60-124">有关受支持的版本的详细信息，请参阅规划文档中 [Lync Server 2013 中存档的技术要求](lync-server-2013-technical-requirements-for-archiving.md) 。</span><span class="sxs-lookup"><span data-stu-id="3dd60-124">For details about the supported versions, see [Technical requirements for Archiving in Lync Server 2013](lync-server-2013-technical-requirements-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="3dd60-125">在部署和启用存档之前，必须设置 SQL Server 平台。</span><span class="sxs-lookup"><span data-stu-id="3dd60-125">You must set up the SQL Server platforms prior to deploying and enabling Archiving.</span></span> <span data-ttu-id="3dd60-126">如果用于发布拓扑的帐户具有适当的管理员权限，则可在发布拓扑时创建存档数据库 (LcsLog)。</span><span class="sxs-lookup"><span data-stu-id="3dd60-126">If the account to be used to publish the topology has the appropriate administrator rights and permissions, you can create the Archiving database (LcsLog) when you publish your topology.</span></span> <span data-ttu-id="3dd60-127">你还可以稍后创建数据库，包括安装过程的一部分。</span><span class="sxs-lookup"><span data-stu-id="3dd60-127">You can also create the database later, including as part of the installation procedure.</span></span> <span data-ttu-id="3dd60-128">有关 SQL Server 的详细信息，请参阅 SQL Server 技术中心 [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) 。</span><span class="sxs-lookup"><span data-stu-id="3dd60-128">For details about SQL Server, see the SQL Server TechCenter at [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3dd60-129">确保 SQL Server 代理服务启动类型为 "自动"，并且 SQL Server 代理服务正在为持有存档数据库的 SQL 实例运行，因此默认的存档 SQL Server 维护作业可以按其计划在 SQL Server 代理服务的控制下运行。</span><span class="sxs-lookup"><span data-stu-id="3dd60-129">Ensure that the SQL Server Agent Service Startup Type is Automatic and the SQL Server Agent Service is running for the SQL Instance which is holding the Archiving database, so that the Default Archiving SQL Server Maintenance Job can run on its scheduled basis under the control of the SQL Server Agent Service.</span></span>



</div>

</div>

</div>

<div>

## <a name="setting-up-file-storage"></a><span data-ttu-id="3dd60-130">设置文件存储</span><span class="sxs-lookup"><span data-stu-id="3dd60-130">Setting Up File Storage</span></span>

<span data-ttu-id="3dd60-131">存档使用您在设置前端池或标准版服务器时指定的 Lync Server 2013 文件共享。</span><span class="sxs-lookup"><span data-stu-id="3dd60-131">Archiving uses the Lync Server 2013 file share that you specified when you set up your Front End pool or Standard Edition server.</span></span> <span data-ttu-id="3dd60-132">您不能更改用于存档的文件共享。</span><span class="sxs-lookup"><span data-stu-id="3dd60-132">You cannot change the file share used for Archiving.</span></span> <span data-ttu-id="3dd60-133">有关受支持的文件存储系统的详细信息，请参阅支持文档中的 [Lync Server 2013 中的文件存储支持](lync-server-2013-file-storage-support.md) 。</span><span class="sxs-lookup"><span data-stu-id="3dd60-133">For details about supported file storage systems, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="3dd60-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3dd60-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

