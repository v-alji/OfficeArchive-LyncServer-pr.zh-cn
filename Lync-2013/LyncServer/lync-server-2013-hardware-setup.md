---
title: Lync Server 2013：硬件安装
description: Lync Server 2013：硬件设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware setup
ms:assetid: 37a9f295-cde3-4beb-9a6a-2580082798ab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425852(v=OCS.15)
ms:contentKeyID: 48183834
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e798ce32c1f89bba40ad9245426492b0489e7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427689"
---
# <a name="hardware-setup-for-lync-server-2013"></a><span data-ttu-id="afa54-103">Lync Server 2013 的硬件安装</span><span class="sxs-lookup"><span data-stu-id="afa54-103">Hardware setup for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="afa54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="afa54-104">

<span> </span></span></span>

<span data-ttu-id="afa54-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="afa54-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="afa54-106">在需要用于实现拓扑的基础结构中设置硬件和其他组件需要在拓扑生成器中发布拓扑之前执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="afa54-106">Setting up the hardware and other components required in the infrastructure that you need to implement your topology requires that, prior to publishing your topology in Topology Builder, you do the following:</span></span>

  - <span data-ttu-id="afa54-107">在使用拓扑生成器创建和保存的拓扑设计中，为每个组件安装硬件，包括运行 Lync Server 2013、数据库服务器、运行 Internet 信息服务的服务器 (IIS) 和反向代理服务器的所有所需 (计算机，如) 、网络适配器、硬件负载平衡器和存储设备 (（如文件服务器) ）。</span><span class="sxs-lookup"><span data-stu-id="afa54-107">Install the hardware for each component in the topology design that you created and saved by using Topology Builder, including all required computers (servers running Lync Server 2013, database servers, servers running Internet Information Services (IIS), and reverse proxy servers, as appropriate), network adapters, hardware load balancers, and storage devices (such as file servers).</span></span> <span data-ttu-id="afa54-108">确认已遵循网络适配器的号码和速度建议。</span><span class="sxs-lookup"><span data-stu-id="afa54-108">Confirm that you have followed the recommendations for the number and speed for network adapters.</span></span> <span data-ttu-id="afa54-109">如果你要使用硬件负载平衡器，请确保你拥有来自供应商的适当信息，以便将其配置为与 Lync Server 2013 配合使用。</span><span class="sxs-lookup"><span data-stu-id="afa54-109">If you will be using hardware load balancers, make sure that you have the proper information from the vendor to configure them for use with Lync Server 2013.</span></span> <span data-ttu-id="afa54-110">如果你将使用文件服务器或其他服务器来承载 Lync Server 所需的文件共享，请确保服务器可用，并且已准备好配置文件共享。</span><span class="sxs-lookup"><span data-stu-id="afa54-110">If you will be using a file server or other server to house the file share required by Lync Server, make sure that the server is available and ready for the configuration of the file share.</span></span> <span data-ttu-id="afa54-111">有关如何定义拓扑以指定部署所需的组件的详细信息，请参阅 [在 Lync Server 2013 中定义和配置拓扑](lync-server-2013-defining-and-configuring-the-topology.md)。</span><span class="sxs-lookup"><span data-stu-id="afa54-111">For details about how to define a topology that specifies the components needed for your deployment, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span> <span data-ttu-id="afa54-112">有关服务器硬件要求的详细信息，请参阅支持文档中的 [Lync Server 2013 支持的硬件](lync-server-2013-supported-hardware.md) 。</span><span class="sxs-lookup"><span data-stu-id="afa54-112">For details about hardware requirements for servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="afa54-113">请确保网络基础结构满足要求。</span><span class="sxs-lookup"><span data-stu-id="afa54-113">Make sure that the networking infrastructure meets requirements.</span></span> <span data-ttu-id="afa54-114">有关详细信息，请参阅规划文档中 [Lync Server 2013 的网络基础结构要求](lync-server-2013-network-infrastructure-requirements.md) 。</span><span class="sxs-lookup"><span data-stu-id="afa54-114">For details, see [Network infrastructure requirements for Lync Server 2013](lync-server-2013-network-infrastructure-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="afa54-115">设置 Active Directory 域服务。</span><span class="sxs-lookup"><span data-stu-id="afa54-115">Set up Active Directory Domain Services.</span></span> <span data-ttu-id="afa54-116">设置 AD DS 包括准备 AD DS 和定义要在 AD DS 中部署的所有组件。</span><span class="sxs-lookup"><span data-stu-id="afa54-116">Setting up AD DS includes preparing AD DS and defining all components that you want to deploy in AD DS.</span></span> <span data-ttu-id="afa54-117">有关准备 AD DS 的详细信息，请参阅部署文档中的 [准备适用于 Lync Server 2013 的 Active Directory 域服务](lync-server-2013-preparing-active-directory-domain-services.md) 。</span><span class="sxs-lookup"><span data-stu-id="afa54-117">For details about preparing AD DS, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="afa54-118">设置创建文件共享所需的权限。</span><span class="sxs-lookup"><span data-stu-id="afa54-118">Set up the required permissions for creating the file share.</span></span> <span data-ttu-id="afa54-119">在发布拓扑时，由 Lync Server 2013 使用文件共享的权限会自动配置为拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="afa54-119">Permissions for use of file shares by Lync Server 2013 are automatically configured by Topology Builder when you publish your topology.</span></span> <span data-ttu-id="afa54-120">但是，用于发布拓扑的用户帐户必须具有 "完全控制" (文件共享上的 "读取/写入/修改") ，以便拓扑生成器配置所需的权限。</span><span class="sxs-lookup"><span data-stu-id="afa54-120">However, the user account used to publish the topology must have full control (read/write/modify) on the file share in order for Topology Builder to configure the required permissions.</span></span> <span data-ttu-id="afa54-121">若要确保可在拓扑生成器发布过程中正确管理文件共享，应将用户所属的用户或域组作为文件共享所在的计算机上的本地管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="afa54-121">To make sure that the file share can be managed properly during the Topology Builder publishing process, the user or domain group that the user is a member of should be made a member of the local Administrators group on the machine where the file share is located.</span></span> <span data-ttu-id="afa54-122">在多域方案中，域 A 用户或组应成为文件共享所在的域 B 中计算机上的本地管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="afa54-122">In a multi-domain scenario, Domain A user or group should be made a member of the local Administrators group on the machine in Domain B where the file share will be located.</span></span>
    
    <span data-ttu-id="afa54-123">有关使用分布式文件系统中的文件共享更新 (DFS) 的详细信息，请参阅 [为 Lync Server 2013 配置文件存储](lync-server-2013-configure-dfs-file-storage.md)。</span><span class="sxs-lookup"><span data-stu-id="afa54-123">For details about updating using file shares in a Distributed File System (DFS), see [Configure file storage for Lync Server 2013](lync-server-2013-configure-dfs-file-storage.md).</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="afa54-124">Lync Server 2013 的文件共享无法在前端服务器上找到。</span><span class="sxs-lookup"><span data-stu-id="afa54-124">The file share for Lync Server 2013, Enterprise Edition cannot be located on the Front End Server.</span></span>

    
    </div>

  - <span data-ttu-id="afa54-125">安装和设置用于 Web 服务的硬件负载平衡器。</span><span class="sxs-lookup"><span data-stu-id="afa54-125">Install and set up the hardware load balancer for Web Services.</span></span> <span data-ttu-id="afa54-126">通过域名系统 (DNS) 负载平衡，你仍然需要对这些池使用硬件负载平衡器，但仅适用于 HTTP/HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="afa54-126">With Domain Name System (DNS) load balancing deployed, you still need to also use hardware load balancers for these pools, but only for HTTP/HTTPS traffic.</span></span> <span data-ttu-id="afa54-127">硬件负载平衡器用于来自端口443和80的客户端的 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="afa54-127">The hardware load balancer is used for HTTPS traffic from clients over ports 443 and 80.</span></span> <span data-ttu-id="afa54-128">虽然您仍需要这些池的硬件负载平衡器，但它们的设置和管理主要用于 HTTP/HTTPS 流量，这些流量习惯于硬件负载平衡器的管理员。</span><span class="sxs-lookup"><span data-stu-id="afa54-128">Although you still need hardware load balancers for these pools, their setup and administration will be primarily for HTTP/HTTPS traffic, which the administrators of the hardware load balancers are accustomed to.</span></span>

<span data-ttu-id="afa54-129">完成本主题中所述的所有准备任务后，在发布拓扑之前，您还需要：</span><span class="sxs-lookup"><span data-stu-id="afa54-129">After you complete all of the preparation tasks as described in this topic, but prior to publishing the topology, you also need to:</span></span>

  - [<span data-ttu-id="afa54-130">在服务器上安装适用于 Lync Server 2013 的操作系统和必备软件</span><span class="sxs-lookup"><span data-stu-id="afa54-130">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>](lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md)

  - [<span data-ttu-id="afa54-131">为 Lync Server 2013 配置 IIS</span><span class="sxs-lookup"><span data-stu-id="afa54-131">Configure IIS for Lync Server 2013</span></span>](lync-server-2013-configure-iis.md)

  - [<span data-ttu-id="afa54-132">为 Lync Server 2013 配置 SQL Server</span><span class="sxs-lookup"><span data-stu-id="afa54-132">Configure SQL Server for Lync Server 2013</span></span>](lync-server-2013-configure-sql-server-for-lync-server.md)

  - [<span data-ttu-id="afa54-133">在 Lync Server 2013 中配置前端池或 Standard Edition 服务器的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="afa54-133">Configure DNS records in Lync Server 2013 for a Front End pool or Standard Edition server</span></span>](lync-server-2013-configure-dns-records-for-a-front-end-pool-or-standard-edition-server.md)

<span data-ttu-id="afa54-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="afa54-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

