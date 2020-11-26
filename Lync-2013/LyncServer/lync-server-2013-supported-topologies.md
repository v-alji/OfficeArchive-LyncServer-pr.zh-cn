---
title: Lync Server 2013 支持的拓扑
description: Lync Server 2013 支持的拓扑。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported topologies
ms:assetid: 3475d430-0394-491b-a09b-ba85bd62be70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425833(v=OCS.15)
ms:contentKeyID: 48183832
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39c19577fbda7e377e145abfd473d2cf8e6d4a1a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441429"
---
# <a name="supported-topologies-in-lync-server-2013"></a><span data-ttu-id="83806-103">Lync Server 2013 中支持的拓扑</span><span class="sxs-lookup"><span data-stu-id="83806-103">Supported topologies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83806-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83806-104">

<span> </span></span></span>

<span data-ttu-id="83806-105">_**主题上次修改时间：** 2014-01-14_</span><span class="sxs-lookup"><span data-stu-id="83806-105">_**Topic Last Modified:** 2014-01-14_</span></span>

<span data-ttu-id="83806-106">Lync Server 2013 支持在组织内部部署网站，并使用 Lync Online 部署（称为混合部署）集成本地部署。</span><span class="sxs-lookup"><span data-stu-id="83806-106">Lync Server 2013 supports deployment of sites on premises in an organization and integration of on-premises deployments with Lync Online deployments, which is known as a hybrid deployment.</span></span> <span data-ttu-id="83806-107">在混合部署中，某些用户在本地托管，某些用户是在线托管的。</span><span class="sxs-lookup"><span data-stu-id="83806-107">In a hybrid deployment, some users are homed on-premises and some users are homed online.</span></span>

<span data-ttu-id="83806-108">对于本地部署，Lync Server 2013 支持部署一个或多个可缩放的网站，以满足高可用性和位置要求。</span><span class="sxs-lookup"><span data-stu-id="83806-108">For on-premises deployments, Lync Server 2013 supports deployment of one or more sites that can be scaled to meet high availability and location requirements.</span></span> <span data-ttu-id="83806-109">你可以组织这些网站及其组件，以满足你的组织的访问权限和复原要求。</span><span class="sxs-lookup"><span data-stu-id="83806-109">You can structure these sites and their components to meet the access and resiliency requirements of your organization.</span></span>

<span data-ttu-id="83806-110">Lync Server 2013 内部部署包含以下内容：</span><span class="sxs-lookup"><span data-stu-id="83806-110">A Lync Server 2013 on-premises deployment consists of the following:</span></span>

  - <span data-ttu-id="83806-111">你的部署必须包含至少一个中心网站 (也称为数据中心) 。</span><span class="sxs-lookup"><span data-stu-id="83806-111">Your deployment must include at least one central site (also known as a data center).</span></span> <span data-ttu-id="83806-112">每个中心网站必须包含至少一个企业版前端池或一个标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-112">Each central site must contain at least one Enterprise Edition Front End pool or one Standard Edition server.</span></span> <span data-ttu-id="83806-113">其中包括以下内容：</span><span class="sxs-lookup"><span data-stu-id="83806-113">These consist of the following:</span></span>
    
      - <span data-ttu-id="83806-114">企业版前端池（由一个或多个前端服务器组成），它包含一个或多个前端服务器 (通常是至少两个前端服务器的可伸缩性) 和一个单独的后端服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-114">Enterprise Edition Front End pool, which consists of one or more Front End Servers (typically, at least two Front End Servers for scalability) and a separate Back End Server.</span></span> <span data-ttu-id="83806-115">前端池最多可以包含十二个前端服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-115">A Front End pool can contain a maximum of twelve Front End Servers.</span></span> <span data-ttu-id="83806-116">对于多个前端服务器，需要负载平衡。</span><span class="sxs-lookup"><span data-stu-id="83806-116">Load balancing is required for multiple Front End Servers.</span></span> <span data-ttu-id="83806-117">对于 SIP 流量，我们建议采用 DNS 负载平衡，但硬件负载平衡也受支持。</span><span class="sxs-lookup"><span data-stu-id="83806-117">For SIP traffic, we recommend DNS load balancing, but hardware load balancing is also supported.</span></span> <span data-ttu-id="83806-118">如果你对 SIP 流量使用 DNS 负载平衡，你仍然需要用于 HTTP 流量的硬件负载平衡器。</span><span class="sxs-lookup"><span data-stu-id="83806-118">If you use DNS load balancing for SIP traffic, you still need a hardware load balancer for HTTP traffic.</span></span> <span data-ttu-id="83806-119">我们建议 SQL Server 镜像以实现数据库的高可用性。</span><span class="sxs-lookup"><span data-stu-id="83806-119">We recommend SQL Server mirroring for high availability of databases.</span></span> <span data-ttu-id="83806-120">后端数据库需要单独的实例，但你可以将存档数据库、监视数据库、持久聊天数据库和持久聊天合规性数据库 collocate。</span><span class="sxs-lookup"><span data-stu-id="83806-120">The back-end database requires a separate instance, but you can collocate the archiving database, monitoring database, persistent chat database, and persistent chat compliance database with it.</span></span> <span data-ttu-id="83806-121">Lync Server 2013 支持对部署中的文件共享使用共享群集。</span><span class="sxs-lookup"><span data-stu-id="83806-121">Lync Server 2013 supports the use of a shared cluster for the file shares in your deployment.</span></span> <span data-ttu-id="83806-122">有关数据库存储要求的详细信息，请参阅 [Lync Server 2013 中的数据库软件支持](lync-server-2013-database-software-support.md)。</span><span class="sxs-lookup"><span data-stu-id="83806-122">For details about database storage requirements, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md).</span></span> <span data-ttu-id="83806-123">有关文件存储要求的详细信息，请参阅 [Lync Server 2013 中的文件存储支持](lync-server-2013-file-storage-support.md)。</span><span class="sxs-lookup"><span data-stu-id="83806-123">For details about file storage requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md).</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="83806-124">如果您 collocate Lync Server 数据库，我们强烈建议评估可能影响可用性和性能的所有因素。</span><span class="sxs-lookup"><span data-stu-id="83806-124">If you collocate Lync Server databases, we highly recommend assessing all factors that might affect availability and performance.</span></span> <span data-ttu-id="83806-125">若要验证故障转移功能，建议您测试所有故障转移方案。</span><span class="sxs-lookup"><span data-stu-id="83806-125">To verify failover capabilities, we recommend testing all failover scenarios.</span></span>

        
        </div>
    
      - <span data-ttu-id="83806-126">标准版服务器，其中包括 collocated SQL Server Express 数据库。</span><span class="sxs-lookup"><span data-stu-id="83806-126">Standard Edition server, which includes a collocated SQL Server Express database.</span></span>

  - <span data-ttu-id="83806-127">您的部署还可以有一个或多个与中央站点相关联的分支站点。</span><span class="sxs-lookup"><span data-stu-id="83806-127">Your deployment can also have one or more branch sites associated with a central site.</span></span>

<span data-ttu-id="83806-128">本部分介绍 Lync Server 2013 部署的网站和组件。</span><span class="sxs-lookup"><span data-stu-id="83806-128">This section describes the sites and components of a Lync Server 2013 deployment.</span></span> <span data-ttu-id="83806-129">有关 Lync Server 2013 网站、拓扑和组件规划的详细信息，请参阅规划文档中 Lync server 2013 和[Lync server 2013 中的参考拓扑](lync-server-2013-reference-topologies.md)[之前必须了解的拓扑基础知识](lync-server-2013-topology-basics-you-must-know-before-planning.md)。</span><span class="sxs-lookup"><span data-stu-id="83806-129">For details about Lync Server 2013 site, topology, and component planning, see [Topology basics you must know before planning for Lync Server 2013](lync-server-2013-topology-basics-you-must-know-before-planning.md) and [Reference topologies in Lync Server 2013](lync-server-2013-reference-topologies.md) in the Planning documentation.</span></span> <span data-ttu-id="83806-130">有关以前版本的组件集成的详细信息，请参阅 [Lync Server 2013 中支持的迁移路径和共存方案](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md)。</span><span class="sxs-lookup"><span data-stu-id="83806-130">For details about integration of components of previous releases, see [Supported migration paths and coexistence scenarios in Lync Server 2013](lync-server-2013-supported-migration-paths-and-coexistence-scenarios.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="83806-131">前端、Edge、中介和控制器服务器角色不支持延伸池。</span><span class="sxs-lookup"><span data-stu-id="83806-131">Stretched pools are not supported for the Front End, Edge, Mediation, and Director server roles.</span></span>



</div>

<div>

## <a name="central-site-topologies-and-components-on-premises"></a><span data-ttu-id="83806-132">中心网站拓扑和组件 (本地) </span><span class="sxs-lookup"><span data-stu-id="83806-132">Central Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="83806-133">虽然中心站点拓扑必须包括一个前端池或一个标准版服务器，但每个中心网站也可以包含以下内容：</span><span class="sxs-lookup"><span data-stu-id="83806-133">Although a central site topology must include one Front End pool or one Standard Edition server, each central site can also contain the following:</span></span>

  - <span data-ttu-id="83806-134">多个前端池，可以位于同一个域或不同域中。</span><span class="sxs-lookup"><span data-stu-id="83806-134">Multiple Front End pools, which can be in the same domain or different domains.</span></span> <span data-ttu-id="83806-135">但是，前端池中的所有前端服务器和该池的后端服务器必须位于同一个域中。</span><span class="sxs-lookup"><span data-stu-id="83806-135">However, all Front End Servers in a Front End pool, and the Back End Server for that pool, must be in the same domain.</span></span>

  - <span data-ttu-id="83806-136">多个标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-136">Multiple Standard Edition servers.</span></span>

  - <span data-ttu-id="83806-137">Office Web Apps 服务器，可与 Lync Server 2013 中的 Office Web 应用程序一起处理 Microsoft PowerPoint 演示文稿的共享和呈现。</span><span class="sxs-lookup"><span data-stu-id="83806-137">Office Web Apps Server, which is used with Office Web Applications in Lync Server 2013 to handle the sharing and rendering of Microsoft PowerPoint presentations.</span></span>

  - <span data-ttu-id="83806-138">在外围网络中，如果你希望部署支持联盟伙伴、公共 IM 连接、可扩展消息和状态协议 (XMPP) 网关、远程用户访问、参与会议的匿名用户或 Exchange 统一消息 (UM) ，请使用边缘服务器或边缘池。</span><span class="sxs-lookup"><span data-stu-id="83806-138">Edge Server or Edge pool in your perimeter network, if you want your deployment to support federated partners, public IM connectivity, an extensible messaging and presence protocol (XMPP) gateway, remote user access, participation of anonymous users in meetings, or Exchange Unified Messaging (UM).</span></span> <span data-ttu-id="83806-139">您不能与 Edge 服务器 collocate 任何其他服务器角色。</span><span class="sxs-lookup"><span data-stu-id="83806-139">You cannot collocate any other server role with an Edge Server.</span></span> <span data-ttu-id="83806-140">我们建议在适当的情况下提供 DNS 负载平衡，但硬件负载平衡也受支持。</span><span class="sxs-lookup"><span data-stu-id="83806-140">We recommend DNS load balancing, where appropriate, but hardware load balancing is also supported.</span></span> <span data-ttu-id="83806-141">内部边缘接口和外部边缘接口必须使用同一类型的负载平衡。</span><span class="sxs-lookup"><span data-stu-id="83806-141">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="83806-142">您不能在一个边缘接口上使用 DNS 负载平衡的同时，在另一个边缘接口上使用硬件负载平衡。</span><span class="sxs-lookup"><span data-stu-id="83806-142">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span> <span data-ttu-id="83806-143">有关负载平衡要求和支持的详细信息，请参阅部署文档中的 "在 lync server [2013 中规划外部用户访问](lync-server-2013-planning-for-external-user-access.md) " 和 " [在 lync Server 2013 中部署外部用户访问](lync-server-2013-deploying-external-user-access.md) "。</span><span class="sxs-lookup"><span data-stu-id="83806-143">For details about load balancing requirements and support, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="83806-144">中介服务器或池，如果你想要在中心网站上的前端池中支持企业语音或拨入式会议。</span><span class="sxs-lookup"><span data-stu-id="83806-144">Mediation Server or pool, if you want to support Enterprise Voice or dial-in conferencing in a Front End pool at the central site.</span></span> <span data-ttu-id="83806-145">根据部署企业语音支持的方式，你可以 collocate 前端池中的中介服务器 (默认) 或部署独立的中介服务器或池。</span><span class="sxs-lookup"><span data-stu-id="83806-145">Depending on how you deploy Enterprise Voice support, you can collocate the Mediation Server in a Front End pool (the default) or deploy a stand-alone Mediation Server or pool.</span></span> <span data-ttu-id="83806-146">在适当的情况下，你可以使用 DNS、硬件或应用程序负载平衡 () 从中介服务器池的网关对等分配流量，包括 PSTN 网关、IP PBX 或 SIP 中继会话边界控制 (SBC) 。有关规划相应中介服务器拓扑的详细信息，请参阅规划文档中 [Lync server 2013 中的中介服务器部署指南](lync-server-2013-deployment-guidelines-for-mediation-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="83806-146">You can use DNS, hardware, or application load balancing (when appropriate) to distribute traffic from a Mediation Server pool’s gateway peer, including a PSTN gateway, IP-PBX, or SIP trunk Session Border Control (SBC).For details about planning the appropriate Mediation Server topology, see [Deployment guidelines for Mediation Server in Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="83806-147">持久聊天服务器，如果你希望用户能够参与多个基于主题的对话，这些对话会随着时间的推移而保留。</span><span class="sxs-lookup"><span data-stu-id="83806-147">Persistent Chat Server, if you want to users to be able to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="83806-148">为了提供更大的容量和增强的可靠性，你的拓扑可以包括多台运行持久聊天服务器的计算机。</span><span class="sxs-lookup"><span data-stu-id="83806-148">To provide more capacity and increased reliability, your topology can include multiple computers running Persistent Chat Server.</span></span> <span data-ttu-id="83806-149">您不能将持久聊天服务器与企业版池中的其他服务器角色 collocate。</span><span class="sxs-lookup"><span data-stu-id="83806-149">You cannot collocate Persistent Chat Server with other server roles in an Enterprise pool.</span></span> <span data-ttu-id="83806-150">但是，你可以在标准版服务器上 collocate 持久聊天服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-150">However, you can collocate Persistent Chat Server on a Standard Edition server.</span></span> <span data-ttu-id="83806-151">持久聊天需要数据库，并且如果你实现持久聊天合规性数据库，但数据库可以与存档数据库、监视数据库或企业版前端池的后端服务器 collocated。</span><span class="sxs-lookup"><span data-stu-id="83806-151">Persistent chat requires a database and, if you implement persistent chat compliance, a persistent chat compliance database, but the databases can be collocated with the Archiving database, Monitoring database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span> <span data-ttu-id="83806-152">有关规划合适的持久聊天服务器拓扑的详细信息，请参阅规划文档中的在 [Lync server 2013 中规划持久聊天服务器](lync-server-2013-planning-for-persistent-chat-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="83806-152">For details about planning the appropriate Persistent Chat Server topology, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="83806-153">监视：如果你希望支持音频/视频体验的数据收集 (QoE) 并在你的部署中为企业语音和 A/V 会议 (CDR) 调用详细录制。</span><span class="sxs-lookup"><span data-stu-id="83806-153">Monitoring, if you want to support data collection for audio/video Quality of Experience (QoE) and call detail recording (CDR) for Enterprise Voice and A/V conferences in your deployment.</span></span> <span data-ttu-id="83806-154">或者，你可以将 Microsoft System Center Operations Manager 安装 (以前的 Microsoft Operations Manager) ，它使用监视 CDR 和 QoE 数据来生成接近的实时警报，显示调用可靠性和媒体质量的运行状况。</span><span class="sxs-lookup"><span data-stu-id="83806-154">Optionally, you can install the Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which uses Monitoring CDR and QoE data to generate near real-time alerts that show the health of call reliability and media quality.</span></span> <span data-ttu-id="83806-155">监视（部署后）在前端服务器或标准版服务器上 collocated。</span><span class="sxs-lookup"><span data-stu-id="83806-155">Monitoring, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="83806-156">监视需要数据库，但数据库可以与存档数据库、持久聊天数据库、持久聊天合规数据库或企业版前端池的后端服务器 collocated。</span><span class="sxs-lookup"><span data-stu-id="83806-156">Monitoring requires a database, but the database can be collocated with the Archiving database, persistent chat database, persistent chat compliance database, or on the Back End Server of an Enterprise Edition Front End pool.</span></span>

  - <span data-ttu-id="83806-157">存档：如果要存档 IM 通信和会议内容 (，以了解部署中) 的合规性原因。</span><span class="sxs-lookup"><span data-stu-id="83806-157">Archiving, if you want to archive IM communications and meeting content (for compliance reasons) in your deployment.</span></span> <span data-ttu-id="83806-158">存档（部署后）在前端服务器或标准版服务器上 collocated。</span><span class="sxs-lookup"><span data-stu-id="83806-158">Archiving, when deployed, is collocated on Front End Servers or a Standard Edition server.</span></span> <span data-ttu-id="83806-159">存档存储需要部署存档数据库或与 Exchange 2013 存储集成。</span><span class="sxs-lookup"><span data-stu-id="83806-159">Archiving storage requires either deployment of an Archiving database or integration with Exchange 2013 storage.</span></span> <span data-ttu-id="83806-160">如果同时使用这两个（即 *混合模式*），exchange 2013 存储用于存储托管在 Exchange 2013 上的用户的存档数据，而存档数据库用于存档部署中所有其他用户的数据。</span><span class="sxs-lookup"><span data-stu-id="83806-160">If you use both, which is known as *mixed mode*, Exchange 2013 storage is used to store archive data for users who are homed on Exchange 2013, and the Archiving database is used to archive data for all other users in your deployment.</span></span> <span data-ttu-id="83806-161">如果需要存档数据库，可以在监视数据库、持久聊天数据库、持久聊天合规数据库或前端池的后端服务器上 collocated 数据库。</span><span class="sxs-lookup"><span data-stu-id="83806-161">If you require an Archiving database, the database can be collocated on the Monitoring database, persistent chat database, persistent chat compliance database, or on the Back End Server of a Front End pool.</span></span> <span data-ttu-id="83806-162">有关规划相应的存档拓扑的详细信息，请参阅规划文档中的 [在 Lync Server 2013 中规划存档](lync-server-2013-planning-for-archiving.md) 。</span><span class="sxs-lookup"><span data-stu-id="83806-162">For details about planning the appropriate Archiving topology, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="83806-163">Director 或控制器池，如果你想要方便将 Lync Server 2013 用户请求恢复和重定向到用户的主池，它可以是企业版前端池或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-163">Director or Director pool, if you want to facilitate resiliency and redirection of Lync Server 2013 user requests to the user’s home pool, which can be either an Enterprise Edition Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="83806-164">我们建议你在支持外部用户访问的每个中心网站以及你部署一个或多个前端池的每个中心网站中部署 Director 或控制器池。</span><span class="sxs-lookup"><span data-stu-id="83806-164">We recommend that you deploy a Director or Director pool in each central site that supports external user access and in each central site in which you deploy one or more Front End pools.</span></span> <span data-ttu-id="83806-165">每个控制器池最多可包含10个控制器。</span><span class="sxs-lookup"><span data-stu-id="83806-165">Each Director pool can contain a maximum of ten Directors.</span></span> <span data-ttu-id="83806-166">Director 不能与任何其他服务器角色 collocated。</span><span class="sxs-lookup"><span data-stu-id="83806-166">A Director cannot be collocated with any other server role.</span></span> <span data-ttu-id="83806-167">有关规划合适的控制器拓扑的详细信息，请参阅规划文档中 [Lync Server 2013 中的 Director 的方案](lync-server-2013-scenarios-for-the-director.md) 。</span><span class="sxs-lookup"><span data-stu-id="83806-167">For details about planning the appropriate Director topology, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="83806-168">反向代理（不是 Lync Server 2013 组件），但如果您希望支持对联盟用户的 web 内容的共享或支持移动通信，则该代理是必需的。</span><span class="sxs-lookup"><span data-stu-id="83806-168">Reverse proxy, which is not a Lync Server 2013 component, but is required if you want to support sharing of web content for federated users or to support Mobility traffic.</span></span> <span data-ttu-id="83806-169">不能将反向代理服务器与任何 Lync Server 2013 服务器角色 collocate，但你可以通过在用于其他应用程序的组织中的现有反向代理服务器上配置支持来为 Lync Server 2013 部署实现反向代理支持。</span><span class="sxs-lookup"><span data-stu-id="83806-169">You cannot collocate a reverse proxy server with any Lync Server 2013 server role, but you can implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span> <span data-ttu-id="83806-170">有关反向代理服务器的详细信息，请参阅部署文档中 [的 Lync Server 2013 的 "设置反向代理服务器](lync-server-2013-setting-up-reverse-proxy-servers.md) "。</span><span class="sxs-lookup"><span data-stu-id="83806-170">For details about reverse proxy servers, see [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="83806-171">在 Lync Server 2013 中，A/V 会议、监视和存档运行在前端服务器上，不再是单独的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="83806-171">In Lync Server 2013, A/V Conferencing, Monitoring, and Archiving run on Front End Servers and are no longer separate server roles.</span></span>



</div>

<span data-ttu-id="83806-172">您在中心网站上部署的所有前端池和标准版服务器都将共享您为中心网站部署的以下任何内容：</span><span class="sxs-lookup"><span data-stu-id="83806-172">All Front End pools and Standard Edition servers that you deploy at a central site share any of the following that you deploy for the central site:</span></span>

  - <span data-ttu-id="83806-173">导演或控制器池</span><span class="sxs-lookup"><span data-stu-id="83806-173">Director or Director pool</span></span>

  - <span data-ttu-id="83806-174">独立中介服务器或池</span><span class="sxs-lookup"><span data-stu-id="83806-174">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="83806-175">Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="83806-175">Office Web Apps Server</span></span>

  - <span data-ttu-id="83806-176">边缘服务器或边缘池</span><span class="sxs-lookup"><span data-stu-id="83806-176">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="83806-177">持久聊天服务器或池</span><span class="sxs-lookup"><span data-stu-id="83806-177">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="83806-178">监控</span><span class="sxs-lookup"><span data-stu-id="83806-178">Monitoring</span></span>

  - <span data-ttu-id="83806-179">存档</span><span class="sxs-lookup"><span data-stu-id="83806-179">Archiving</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="83806-180">如果你想要支持 Exchange 2013 统一消息的集成，但它不是 Lync Server 2013 网站的组件，则可以使用 Lync Server 2013 部署实现 Exchange UM 服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-180">An Exchange UM Server can be implemented with your Lync Server 2013 deployment if you want to support integration of Exchange 2013 Unified Messaging, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="83806-181">多个中心网站也可以共享在一个中心网站中部署的以下任何内容：</span><span class="sxs-lookup"><span data-stu-id="83806-181">Multiple central sites can also share any of the following that you deploy in one central site:</span></span>

  - <span data-ttu-id="83806-182">独立中介服务器或池</span><span class="sxs-lookup"><span data-stu-id="83806-182">Stand-alone Mediation Server or pool</span></span>

  - <span data-ttu-id="83806-183">边缘服务器或边缘池</span><span class="sxs-lookup"><span data-stu-id="83806-183">Edge Server or Edge pool</span></span>

  - <span data-ttu-id="83806-184">持久聊天服务器或池</span><span class="sxs-lookup"><span data-stu-id="83806-184">Persistent Chat Server or pool</span></span>

  - <span data-ttu-id="83806-185">存档</span><span class="sxs-lookup"><span data-stu-id="83806-185">Archiving</span></span>

  - <span data-ttu-id="83806-186">监控</span><span class="sxs-lookup"><span data-stu-id="83806-186">Monitoring</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="83806-187">Exchange UM 服务器可以通过 Lync Server 2013 部署实现并由多个中心网站共享，但它不是 Lync Server 2013 网站的组件。</span><span class="sxs-lookup"><span data-stu-id="83806-187">An Exchange UM Server can be implemented with your Lync Server 2013 deployment and shared by multiple central sites, but it is not a component of the Lync Server 2013 site.</span></span>



</div>

<span data-ttu-id="83806-188">有关 Lync Server 2013 服务器角色和功能的详细信息，请参阅规划文档中 [Lync server 2013 中的服务器角色](lync-server-2013-server-roles.md) 。</span><span class="sxs-lookup"><span data-stu-id="83806-188">For details about Lync Server 2013 server roles and functionality, see [Server roles in Lync Server 2013](lync-server-2013-server-roles.md) in the Planning documentation.</span></span>

<span data-ttu-id="83806-189">有关 Lync Server 2013 服务器 collocation 支持的摘要，请参阅 [Lync server 2013 中的支持的服务器 collocation](lync-server-2013-supported-server-collocation.md)。</span><span class="sxs-lookup"><span data-stu-id="83806-189">For a summary of Lync Server 2013 server collocation support, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md).</span></span>

<span data-ttu-id="83806-190">除了本部分前面所述的服务器角色和功能之外，Lync Server 2013 还有其他组件和选项，其中包括以下部分或全部选项：</span><span class="sxs-lookup"><span data-stu-id="83806-190">In addition to the server roles and functionality covered previously in this section, Lync Server 2013 has additional components and options, which can include some or all of the following:</span></span>

  - <span data-ttu-id="83806-191">防火墙</span><span class="sxs-lookup"><span data-stu-id="83806-191">Firewalls</span></span>

  - <span data-ttu-id="83806-192">PSTN 网关 (如果部署企业语音) </span><span class="sxs-lookup"><span data-stu-id="83806-192">PSTN gateways (if deploying Enterprise Voice)</span></span>

  - <span data-ttu-id="83806-193">Exchange UM 服务器</span><span class="sxs-lookup"><span data-stu-id="83806-193">Exchange UM Server</span></span>

  - <span data-ttu-id="83806-194">DNS 负载平衡</span><span class="sxs-lookup"><span data-stu-id="83806-194">DNS load balancing</span></span>

  - <span data-ttu-id="83806-195">硬件负载平衡器</span><span class="sxs-lookup"><span data-stu-id="83806-195">Hardware load balancers</span></span>

  - <span data-ttu-id="83806-196">SQL Server 数据库</span><span class="sxs-lookup"><span data-stu-id="83806-196">SQL Server databases</span></span>

  - <span data-ttu-id="83806-197">文件共享</span><span class="sxs-lookup"><span data-stu-id="83806-197">File shares</span></span>

<span data-ttu-id="83806-198">有关所有 Lync Server 2013 功能、组件和选项的详细信息，请参阅规划文档。</span><span class="sxs-lookup"><span data-stu-id="83806-198">For details about all of the Lync Server 2013 features, components, and options, see the Planning documentation.</span></span>

</div>

<div>

## <a name="branch-site-topologies-and-components-on-premises"></a><span data-ttu-id="83806-199">分支站点拓扑和组件 (本地) </span><span class="sxs-lookup"><span data-stu-id="83806-199">Branch Site Topologies and Components (On-Premises)</span></span>

<span data-ttu-id="83806-200">分支站点与中央站点相关联，并且分支站点中的每个 Survivable 分支装置都与关联的中心网站中的企业版前端池或标准版服务器相关联。</span><span class="sxs-lookup"><span data-stu-id="83806-200">A branch site is associated with a central site, and each Survivable Branch Appliance in a branch site is associated with an Enterprise Edition Front End pool or a Standard Edition server in the associated central site.</span></span> <span data-ttu-id="83806-201">分支站点依赖于中心网站查看大多数功能，因此分支网站上的组件仅包含以下内容：</span><span class="sxs-lookup"><span data-stu-id="83806-201">Branch sites depend on the central site for most of their functionality, so components at a branch site contain only the following:</span></span>

  - <span data-ttu-id="83806-202">Survivable 分支设备，它将公共交换电话网络与某些 Lync Server 功能结合 (PSTN) 网关。</span><span class="sxs-lookup"><span data-stu-id="83806-202">A Survivable Branch Appliance, which combines a public switched telephone network (PSTN) gateway with some Lync Server functionality.</span></span> <span data-ttu-id="83806-203">中介服务器可以与 Survivable 分支设备上的注册机构实例 collocated，并且你可以部署独立的中介服务器或中介服务器池。</span><span class="sxs-lookup"><span data-stu-id="83806-203">A Mediation Server can be collocated with the instance of the Registrar on the Survivable Branch Appliance, and you can deploy a stand-alone Mediation Server or pool of Mediation Servers.</span></span>

  - <span data-ttu-id="83806-204">Survivable 分支服务器，它是运行安装了 Lync Server 2013 注册机构和中介服务器软件的 Windows Server 的服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-204">A Survivable Branch Server, which is a server running Windows Server that has Lync Server 2013 Registrar and Mediation Server software installed.</span></span>

  - <span data-ttu-id="83806-205">独立的 PSTN 网关 (不属于 Survivable 分支装置) 和独立中介服务器。</span><span class="sxs-lookup"><span data-stu-id="83806-205">A stand-alone PSTN gateway (not part of the Survivable Branch Appliance) and a stand-alone Mediation Server.</span></span>

<span data-ttu-id="83806-206">Survivable 分支服务器的要求与任何 Lync Server 2013 服务器角色的要求相同。</span><span class="sxs-lookup"><span data-stu-id="83806-206">The requirements for Survivable Branch Servers are the same as the requirements for any Lync Server 2013 server role.</span></span>

<span data-ttu-id="83806-207"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83806-207"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

