---
title: Enterprise Edition 前端池部署中的 Lync Server 2013 服务器并置
description: 在企业版前端池部署中使用 Lync Server 2013 服务器 collocation。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server collocation in an Enterprise Edition Front End pool deployment
ms:assetid: 0516b18d-14c0-4237-9279-0f92e341b1bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398102(v=OCS.15)
ms:contentKeyID: 48183287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a937cd2d58e41d56fec3c7898ebcf6725086d51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444908"
---
# <a name="server-collocation-in-an-enterprise-edition-front-end-pool-deployment-for-lync-server-2013"></a><span data-ttu-id="9554e-103">Lync Server 2013 的 Enterprise Edition 前端池部署中的服务器并置</span><span class="sxs-lookup"><span data-stu-id="9554e-103">Server collocation in an Enterprise Edition Front End pool deployment for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9554e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9554e-104">

<span> </span></span></span>

<span data-ttu-id="9554e-105">_**主题上次修改时间：** 2013-11-11_</span><span class="sxs-lookup"><span data-stu-id="9554e-105">_**Topic Last Modified:** 2013-11-11_</span></span>

<span data-ttu-id="9554e-106">本部分介绍了可在 Lync Server 2013 前端池部署中 collocate 的服务器角色、数据库和文件共享。</span><span class="sxs-lookup"><span data-stu-id="9554e-106">This section describes the server roles, databases, and file shares that you can collocate in a Lync Server 2013 Front End pool deployment.</span></span>

<div>

## <a name="server-roles"></a><span data-ttu-id="9554e-107">服务器角色</span><span class="sxs-lookup"><span data-stu-id="9554e-107">Server Roles</span></span>

<span data-ttu-id="9554e-108">在 Lync Server 2013 中，A/V 会议服务、中介服务、监视和存档都在前端服务器上 collocated，但需要进行其他配置才能启用它们。</span><span class="sxs-lookup"><span data-stu-id="9554e-108">In Lync Server 2013, A/V Conferencing service, Mediation service, Monitoring, and Archiving are collocated on the Front End Server, but additional configuration is required to enable them.</span></span> <span data-ttu-id="9554e-109">如果您不想 collocate 前端服务器的中介服务器，则可以在单独的计算机上将其作为独立中介服务器进行部署。</span><span class="sxs-lookup"><span data-stu-id="9554e-109">If you do not want to collocate the Mediation Server with the Front End Server, you can deploy it as a stand-alone Mediation Server on a separate computer.</span></span>

<span data-ttu-id="9554e-110">你可以使用前端服务器 collocate 受信任的应用服务器。</span><span class="sxs-lookup"><span data-stu-id="9554e-110">You can collocate a trusted application server with the Front End Server.</span></span>

<span data-ttu-id="9554e-111">以下服务器角色必须分别部署在单独的计算机上：</span><span class="sxs-lookup"><span data-stu-id="9554e-111">The following server roles must each be deployed on a separate computer:</span></span>

  - <span data-ttu-id="9554e-112">控制器</span><span class="sxs-lookup"><span data-stu-id="9554e-112">Director</span></span>

  - <span data-ttu-id="9554e-113">边缘服务器</span><span class="sxs-lookup"><span data-stu-id="9554e-113">Edge Server</span></span>

  - <span data-ttu-id="9554e-114">如果不 collocated 前端服务器，则为中介服务器 () </span><span class="sxs-lookup"><span data-stu-id="9554e-114">Mediation Server (if not collocated with the Front End Server)</span></span>

  - <span data-ttu-id="9554e-115">Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="9554e-115">Office Web Apps Server</span></span>

<span data-ttu-id="9554e-116">您不能与前端服务器 collocate 持久聊天服务器角色。</span><span class="sxs-lookup"><span data-stu-id="9554e-116">You cannot collocate Persistent Chat server role with the Front End Server.</span></span>

</div>

<div>

## <a name="databases"></a><span data-ttu-id="9554e-117">数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-117">Databases</span></span>

<span data-ttu-id="9554e-118">你可以在同一个数据库服务器上 collocate 以下每个数据库：</span><span class="sxs-lookup"><span data-stu-id="9554e-118">You can collocate each of the following databases on the same database server:</span></span>

  - <span data-ttu-id="9554e-119">后端数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-119">Back-end database</span></span>

  - <span data-ttu-id="9554e-120">监控数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-120">Monitoring database</span></span>

  - <span data-ttu-id="9554e-121">存档数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-121">Archiving database</span></span>

  - <span data-ttu-id="9554e-122">持久聊天数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-122">Persistent Chat database</span></span>

  - <span data-ttu-id="9554e-123">持久聊天合规性数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-123">Persistent Chat compliance database</span></span>

<span data-ttu-id="9554e-124">你可以在 SQL Server 的单个实例中 collocate 任何或所有或所有这些数据库，或者对每个实例使用单独的 SQL Server 实例，但具有以下限制：</span><span class="sxs-lookup"><span data-stu-id="9554e-124">You can collocate any or any or all of these databases in a single instance of SQL Server or use a separate instance of SQL Server for each, with the following limitations:</span></span>

  - <span data-ttu-id="9554e-125">SQL Server 的每个实例只能包含单个后端数据库、单个监视数据库、单个存档数据库、单个持久聊天数据库和单个持久聊天合规性数据库。</span><span class="sxs-lookup"><span data-stu-id="9554e-125">Each instance of SQL Server can contain only a single back-end database, a single Monitoring database, a single Archiving database, a single Persistent Chat database, and a single Persistent Chat compliance database.</span></span>

  - <span data-ttu-id="9554e-126">数据库服务器无法支持多个前端池、一个存档部署和一个监视部署，但它可以支持其中一个，而不管数据库使用的是相同的 SQL Server 实例还是 SQL Server 的单独实例。</span><span class="sxs-lookup"><span data-stu-id="9554e-126">The database server cannot support more than one Front End pool, one Archiving deployment, and one Monitoring deployment, but it can support one of each, regardless of whether the databases use the same instance of SQL Server or separate instances of SQL Server.</span></span>

<span data-ttu-id="9554e-127">你可以将文件共享与数据库 collocate，如本节后面部分所述。</span><span class="sxs-lookup"><span data-stu-id="9554e-127">You can collocate a file share with the databases, as described later in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9554e-128">在 Lync Server 2013 中，你可以选择将存档存储与部署中的部分或所有用户的 Exchange 2013 存储进行集成。</span><span class="sxs-lookup"><span data-stu-id="9554e-128">In Lync Server 2013, you have the option of integrating Archiving storage with Exchange 2013 storage for some or all users in your deployment.</span></span> <span data-ttu-id="9554e-129">不能在 Exchange 存储所在的服务器上部署任何运行 Lync Server 或组件的服务器。</span><span class="sxs-lookup"><span data-stu-id="9554e-129">You cannot deploy any servers running Lync Server or components on the same servers as the Exchange storage.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9554e-130">尽管支持 collocation 数据库，但数据库的大小可以快速增长。</span><span class="sxs-lookup"><span data-stu-id="9554e-130">Although collocation of databases is supported, the size of the databases can grow quickly.</span></span> <span data-ttu-id="9554e-131">例如，当你考虑将存档数据库与其他数据库 collocating 时，请注意，如果你要对超过几个用户的邮件进行存档，则存档数据库所需的磁盘空间可能会变得非常大。</span><span class="sxs-lookup"><span data-stu-id="9554e-131">For example, when you consider collocating the Archiving database with other databases, be aware that if you are archiving the messages of more than a few users, the disk space needed by the Archiving database can grow very large.</span></span> <span data-ttu-id="9554e-132">出于此原因，我们不建议 collocating 多个数据库，尤其是存档数据库、持久聊天数据库或与后端数据库的持久聊天合规性数据库。</span><span class="sxs-lookup"><span data-stu-id="9554e-132">For this reason, we do not recommend collocating multiple databases, especially the Archiving database, the Persistent Chat database, or the Persistent Chat compliance database with the back-end database.</span></span>



</div>

</div>

<div>

## <a name="file-share"></a><span data-ttu-id="9554e-133">文件共享</span><span class="sxs-lookup"><span data-stu-id="9554e-133">File Share</span></span>

<span data-ttu-id="9554e-134">文件共享可以是单独的服务器，也可以在同一台服务器上 collocated，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9554e-134">The file share can be a separate server or can be collocated on the same server as any or all of the following:</span></span>

  - <span data-ttu-id="9554e-135">数据库服务器，包括企业版前端池的后端服务器</span><span class="sxs-lookup"><span data-stu-id="9554e-135">Database server, including the Back End Server of an Enterprise Edition Front End pool</span></span>

  - <span data-ttu-id="9554e-136">存档数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-136">Archiving database</span></span>

  - <span data-ttu-id="9554e-137">监控数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-137">Monitoring database</span></span>

  - <span data-ttu-id="9554e-138">持久聊天数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-138">Persistent Chat database</span></span>

  - <span data-ttu-id="9554e-139">持久聊天合规性数据库</span><span class="sxs-lookup"><span data-stu-id="9554e-139">Persistent Chat compliance database</span></span>

<span data-ttu-id="9554e-140">单个文件共享可用于多个前端池，标准版服务器 (同一网站中的所有) 。</span><span class="sxs-lookup"><span data-stu-id="9554e-140">A single file share can be used for multiple Front End pools, Standard Edition servers (all in the same site).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9554e-141">在 Lync Server 2013 中，监视和存档将 Lync Server 文件共享用作前端服务器。</span><span class="sxs-lookup"><span data-stu-id="9554e-141">In Lync Server 2013, Monitoring and Archiving use the Lync Server file share as the Front End Server.</span></span>



</div>

</div>

<div>

## <a name="other-components"></a><span data-ttu-id="9554e-142">其他组件</span><span class="sxs-lookup"><span data-stu-id="9554e-142">Other Components</span></span>

<span data-ttu-id="9554e-143">不能 collocate 不是 Lync Server 2013 组件的反向代理服务器，但如果你希望支持使用任何 Lync Server 2013 服务器角色的联盟用户共享 web 内容，则你的部署中需要使用该服务器。</span><span class="sxs-lookup"><span data-stu-id="9554e-143">You cannot collocate a reverse proxy server, which is not a Lync Server 2013 component, but is required in your deployment if you want to support sharing of web content for federated users with any Lync Server 2013 server role.</span></span> <span data-ttu-id="9554e-144">但是，你可以通过在你的组织中针对其他应用程序使用的现有反向代理服务器上配置支持，从而实现 Lync Server 2013 部署的反向代理支持。</span><span class="sxs-lookup"><span data-stu-id="9554e-144">You can, however, implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span>

<span data-ttu-id="9554e-145">不能 collocate 任何 Exchange 统一消息 (UM) 组件或具有任何 SharePoint Server 角色的 SharePoint 组件。</span><span class="sxs-lookup"><span data-stu-id="9554e-145">You cannot collocate any Exchange Unified Messaging (UM) component or SharePoint component with any SharePoint Server role.</span></span>

<span data-ttu-id="9554e-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9554e-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

