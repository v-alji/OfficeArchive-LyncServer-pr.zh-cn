---
title: Lync Server 2013：持久聊天服务器的容量规划
description: Lync Server 2013：持久聊天服务器的容量规划。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Persistent Chat Server
ms:assetid: 7a850cd5-c789-4795-a8ff-083be21ae784
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615006(v=OCS.15)
ms:contentKeyID: 48184580
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f78f9f3666fb272b808ef36da2d3010f451d0079
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435556"
---
# <a name="capacity-planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="d8c2d-103">Lync Server 2013 中持久聊天服务器的容量规划</span><span class="sxs-lookup"><span data-stu-id="d8c2d-103">Capacity planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8c2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8c2d-104">

<span> </span></span></span>

<span data-ttu-id="d8c2d-105">_**主题上次修改时间：** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="d8c2d-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="d8c2d-106">持久聊天服务器可以执行可持续进行的多用户实时聊天，以便将来检索和搜索。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-106">Persistent Chat Server can perform multi-user real-time chat that can persist for future retrieval and search.</span></span> <span data-ttu-id="d8c2d-107">与在用户邮箱中保存的组内即时消息 (IM) 的不同，如果已配置对话历史记录，则持久聊天服务器会话将保持打开状态，并将内容保存在服务器上，以及消息、文件、Url 和其他属于正在进行的对话的数据。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-107">Unlike group instant messaging (IM) that is saved in a user’s mailbox if conversation history is configured, a Persistent Chat Server session stays open longer, and the content is saved on a server, along with the messages, files, URLs, and other data that are part of an ongoing conversation.</span></span>

<span data-ttu-id="d8c2d-108">容量规划是准备部署持久聊天服务器的重要部分。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-108">Capacity planning is an important part of preparing to deploy Persistent Chat Server.</span></span> <span data-ttu-id="d8c2d-109">本主题提供了有关受支持的持久聊天服务器拓扑和容量计划表的详细信息，可用于为你的部署确定最佳配置。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-109">This topic provides details about supported Persistent Chat Server topologies and capacity planning tables that you can use to determine the best configuration for your deployment.</span></span> <span data-ttu-id="d8c2d-110">它还介绍了如何最好地管理在高峰时段需要更大容量的持久聊天服务器部署。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-110">It also describes how to best manage Persistent Chat Server deployments that require greater capacity at peak times.</span></span>

<span data-ttu-id="d8c2d-111">若要下载持久聊天服务器，请参阅 "Microsoft Lync Server 13 持久聊天服务器" [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539) 。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-111">To download Persistent Chat Server, see "Microsoft Lync Server 13 Persistent Chat Server" at [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539).</span></span>

<span data-ttu-id="d8c2d-112">有关安装持久聊天服务器的详细信息，请参阅在 [Lync server 2013 中安装持久聊天服务器](lync-server-2013-installing-persistent-chat-server.md) 和在部署文档的 [lync Server 2013 中配置持久聊天服务器](lync-server-2013-configuring-persistent-chat-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-112">For details about installing Persistent Chat Server, see [Installing Persistent Chat Server in Lync Server 2013](lync-server-2013-installing-persistent-chat-server.md) and [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="d8c2d-113">支持工具（如 Lync Server 规划工具）可以通过容量规划进一步帮助您。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-113">Support tools, such as Lync Server Planning Tool, can further assist you with capacity planning.</span></span> <span data-ttu-id="d8c2d-114">有关规划工具的详细信息，请参阅规划文档中的 [Lync Server 2013 的规划过程](lync-server-2013-beginning-the-planning-process.md) 。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-114">For details about the Planning Tool, see [Beginning the planning process for Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in the Planning documentation.</span></span>

<div>

## <a name="persistent-chat-server-supported-topologies"></a><span data-ttu-id="d8c2d-115">持久聊天服务器支持的拓扑</span><span class="sxs-lookup"><span data-stu-id="d8c2d-115">Persistent Chat Server Supported Topologies</span></span>

<span data-ttu-id="d8c2d-116">你可以在单服务器或多服务器池中部署持久聊天服务器，并通过单个池或多池拓扑进行部署。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-116">You can deploy Persistent Chat Server in single-server or multiple-server pools, and with single-pool or multiple-pool topology.</span></span>

<span data-ttu-id="d8c2d-117">现在，我们还支持适用于新 Lync Server 2013 部署的标准版服务器上的持久聊天服务器。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-117">We now also support Persistent Chat Server on Standard Edition server for new Lync Server 2013 deployments.</span></span> <span data-ttu-id="d8c2d-118">但是，性能和规模将受到影响，并且由于没有适用于此新部署的高可用性选项，因此我们希望你主要用于概念证明、评估等目的。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-118">However, performance and scale will be affected, and because there is no high availability option for this new deployment, we expect you to use this primarily for the purposes of proof of concept, evaluation, and so on.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d8c2d-119">有关这两种拓扑的其他详细信息，请参阅本文档中的 " <A href="lync-server-2013-planning-for-persistent-chat-server.md">在 lync server 2013 中规划持久聊天服务器</A> " 和 "部署文档" 中的 <A href="lync-server-2013-deploying-persistent-chat-server.md">lync server 2013 中的 "部署持久</A> 聊天服务器"。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-119">For additional details about both topologies, see <A href="lync-server-2013-planning-for-persistent-chat-server.md">Planning for Persistent Chat Server in Lync Server 2013</A> in this documentation set and <A href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="single-server-topology"></a><span data-ttu-id="d8c2d-120">Single-Server 拓扑</span><span class="sxs-lookup"><span data-stu-id="d8c2d-120">Single-Server Topology</span></span>

<span data-ttu-id="d8c2d-121">持久聊天服务器的最低配置和最简单的部署是单个持久聊天服务器前端服务器拓扑。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-121">The minimum configuration and simplest deployment for Persistent Chat Server is a single Persistent Chat Server Front End Server topology.</span></span> <span data-ttu-id="d8c2d-122">此部署需要运行持久聊天服务器的单个服务器 (该服务器可以选择运行合规性服务，前提是启用合规性服务) 、托管 SQL Server 数据库的服务器以及是否需要合规性，SQL Server 数据库存储合规性数据。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-122">This deployment requires a single server that runs Persistent Chat Server (which optionally runs the Compliance service, if compliance is enabled), a server that hosts both the SQL Server database, and if compliance is required, the SQL Server database to store the compliance data.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d8c2d-123">不能将其他服务器添加到在拓扑生成器中作为单服务器部署启动的持久聊天服务器池。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-123">You cannot add additional servers to a Persistent Chat Server pool that is started as a single-server deployment in Topology Builder.</span></span> <span data-ttu-id="d8c2d-124">我们建议使用多服务器池拓扑，即使您使用的是单个服务器也是如此。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-124">We recommend using the multiple-server pool topology, even if you’re using a single server.</span></span> <span data-ttu-id="d8c2d-125">这样，您就可以在以后添加更多的服务器（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-125">This is so that you’ll be able to add more servers later, if it's necessary.</span></span> 


</div>

<span data-ttu-id="d8c2d-126">下图显示了具有合规性的单个持久聊天服务器前端服务器的拓扑的所有必需和可选组件。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-126">The following figure shows all required and optional components of a topology for a single Persistent Chat Server Front End Server with compliance.</span></span>

<span data-ttu-id="d8c2d-127">**单个持久聊天服务器**</span><span class="sxs-lookup"><span data-stu-id="d8c2d-127">**Single Persistent Chat Server**</span></span>

<span data-ttu-id="d8c2d-128">![具有合规性服务的单服务器拓扑](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "具有合规性服务的单服务器拓扑")</span><span class="sxs-lookup"><span data-stu-id="d8c2d-128">![Single server topology with Compliance service](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Single server topology with Compliance service")</span></span>

</div>

<div>

## <a name="multiple-server-topology"></a><span data-ttu-id="d8c2d-129">Multiple-Server 拓扑</span><span class="sxs-lookup"><span data-stu-id="d8c2d-129">Multiple-Server Topology</span></span>

<span data-ttu-id="d8c2d-130">为了提供更大的容量和可靠性，你可以部署多服务器拓扑，如在 [Lync server 2013 中规划持久聊天服务器](lync-server-2013-planning-for-persistent-chat-server.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-130">To provide greater capacity and reliability, you can deploy a multiple-server topology, as described in [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span> <span data-ttu-id="d8c2d-131">多服务器拓扑可以包括多达四个运行持久聊天服务器的活动计算机 (高可用性和灾难恢复配置最多允许八个，但只有四个可以激活，并且剩余四个备用) 。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-131">The multiple-server topology can include as many as four active computers running Persistent Chat Server (high availability and disaster recovery configurations will allow up to eight, but only four can be active and the remaining four on standby).</span></span> <span data-ttu-id="d8c2d-132">每台服务器可支持多达20000并行用户，总共可支持连接到具有4台服务器的持久聊天服务器池的80000个并发用户。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-132">Each server can support as many as 20,000 concurrent users, for a total of 80,000 concurrent users connected to a Persistent Chat Server pool with 4 servers.</span></span> <span data-ttu-id="d8c2d-133">多服务器拓扑与单服务器拓扑相同，不同之处在于多台服务器托管持久聊天服务器，并且可以更高的比例。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-133">A multiple-server topology is the same as the single-server topology except that multiple servers host Persistent Chat Server, and can scale higher.</span></span> <span data-ttu-id="d8c2d-134">运行持久聊天服务器的多台计算机应位于与 Lync Server 和合规性服务相同的 Active Directory 域服务域中。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-134">Multiple computers running Persistent Chat Server should reside in the same Active Directory Domain Services domain as Lync Server and the Compliance service.</span></span>

<span data-ttu-id="d8c2d-135">下图显示多服务器拓扑的所有组件，其中包含运行持久聊天服务器的多台计算机、可选合规性服务和单独的合规性数据库。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-135">The following figure shows all the components of a multiple-server topology with multiple computers running Persistent Chat Server, the optional Compliance service, and a separate compliance database.</span></span>

<span data-ttu-id="d8c2d-136">**多个持久聊天服务器**</span><span class="sxs-lookup"><span data-stu-id="d8c2d-136">**Multiple Persistent Chat Servers**</span></span>

<span data-ttu-id="d8c2d-137">![多服务器拓扑](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "多服务器拓扑")</span><span class="sxs-lookup"><span data-stu-id="d8c2d-137">![Multiple server topology](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Multiple server topology")</span></span>

<span data-ttu-id="d8c2d-138">在四台服务器持久聊天服务器部署（其中80000用户可以同时登录和使用持久聊天）中，每个服务器的20000用户均会平均分配负载。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-138">In a four-server Persistent Chat Server deployment, where 80,000 users can be simultaneously signed in to and using Persistent Chat, the load is distributed evenly at 20,000 users per server.</span></span> <span data-ttu-id="d8c2d-139">如果一台服务器不可用，连接到该服务器的用户将失去其永久聊天服务器的访问权限。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-139">If one server becomes unavailable, the users who are connected to that server will lose their access to Persistent Chat Server.</span></span> <span data-ttu-id="d8c2d-140">断开连接的用户将自动转移到其他服务器，直至不可用服务器恢复为止。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-140">The disconnected users will be automatically transferred to the remaining servers until the unavailable server is restored.</span></span> <span data-ttu-id="d8c2d-141">根据网络上持久聊天流量的数量，此传输可能需要几分钟或更长时间。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-141">Depending on the amount of Persistent Chat traffic on the network, this transfer can take a few minutes or longer.</span></span> <span data-ttu-id="d8c2d-142">由于其余每个服务器都可能托管为多达30000用户，因此我们建议尽快还原不可用的服务器，以避免性能问题。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-142">Because each of the remaining servers might be hosting as many as 30,000 users, we recommend that you restore the unavailable server as quickly as possible to avoid performance issues.</span></span> <span data-ttu-id="d8c2d-143">否则，你可以使用拓扑生成器或 Windows PowerShell cmdlet （ **CsPersistentChatActiveServer**）来使另一个持久聊天服务器可用。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-143">Otherwise, you can make another Persistent Chat Server available by using the Topology Builder or the Windows PowerShell cmdlet, **set-CsPersistentChatActiveServer**.</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-server-capacity-planning"></a><span data-ttu-id="d8c2d-144">持久聊天服务器容量规划</span><span class="sxs-lookup"><span data-stu-id="d8c2d-144">Persistent Chat Server Capacity Planning</span></span>

<span data-ttu-id="d8c2d-145">下表可帮助你对持久聊天服务器进行容量规划。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-145">The following tables can help you with capacity planning for Persistent Chat Server.</span></span> <span data-ttu-id="d8c2d-146">他们对更改各种持久聊天服务器设置有何影响，从而影响容量功能。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-146">They model how changing various Persistent Chat Server settings affect capacity capabilities.</span></span>

<div>

## <a name="planning-your-maximum-capacity-for-persistent-chat-server"></a><span data-ttu-id="d8c2d-147">规划持久聊天服务器的最大容量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-147">Planning Your Maximum Capacity for Persistent Chat Server</span></span>

<span data-ttu-id="d8c2d-148">使用下面的示例表确定可以支持的用户数。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-148">Use the following sample table to determine the number of users you will be able to support.</span></span>

### <a name="persistent-chat-server-pool-maximum-capacity-sample"></a><span data-ttu-id="d8c2d-149">持久聊天服务器池最大容量示例</span><span class="sxs-lookup"><span data-stu-id="d8c2d-149">Persistent Chat Server pool Maximum Capacity Sample</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-150">活动的持久聊天服务实例</span><span class="sxs-lookup"><span data-stu-id="d8c2d-150">Active Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-151"><em>4</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-151"><em>4</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-152">持久聊天服务实例</span><span class="sxs-lookup"><span data-stu-id="d8c2d-152">Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-153"><em>8 (4 必须处于非活动状态。最多只能有4个活动) </em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-153"><em>8 (4 must be inactive; only a maximum of 4 can be active)</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-154">连接的活动用户数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-154">Active users connected</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-155"><em>80,000</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-155"><em>80,000</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-156">设置的用户总数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-156">Total provisioned users</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-157">150,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-157">150,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-158">终结点数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-158">Number of endpoints</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-159">120,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-159">120,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8c2d-160">在前面的示例中，计划支持持久聊天服务器允许的最大用户数： "持久聊天" 服务 (的四个服务器/实例可以有四个更多的被动服务器，运行持久聊天服务器，以实现高可用性和灾难恢复) 和20000用户（每台服务器最多），共80000个活动用户。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-160">In the preceding sample, the plan is to support the maximum number of users that Persistent Chat Server allows: four servers/instances of the Persistent Chat service (can have four more passive servers running Persistent Chat Server for high availability and disaster recovery) and 20,000 users per server, for a total of 80,000 active users.</span></span>

</div>

<div>

## <a name="capacity-planning-for-managing-persistent-chat-room-access"></a><span data-ttu-id="d8c2d-161">管理持久的聊天室访问的容量计划</span><span class="sxs-lookup"><span data-stu-id="d8c2d-161">Capacity Planning for Managing Persistent Chat Room Access</span></span>

<span data-ttu-id="d8c2d-162">下面的示例表可帮助你计划管理持久聊天服务器池中的持久聊天室访问。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-162">The following sample table can help you plan for managing Persistent Chat room access in a Persistent Chat Server pool.</span></span>

### <a name="managing-chat-room-access-sample"></a><span data-ttu-id="d8c2d-163">管理聊天室访问示例</span><span class="sxs-lookup"><span data-stu-id="d8c2d-163">Managing Chat Room Access Sample</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d8c2d-164">小聊天室</span><span class="sxs-lookup"><span data-stu-id="d8c2d-164">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="d8c2d-165">中聊天室</span><span class="sxs-lookup"><span data-stu-id="d8c2d-165">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="d8c2d-166">大聊天室</span><span class="sxs-lookup"><span data-stu-id="d8c2d-166">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="d8c2d-167">总计</span><span class="sxs-lookup"><span data-stu-id="d8c2d-167">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-168">聊天室大小（连接的用户数）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-168">Size of chat rooms (number of users connected)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-169">每个聊天室 30 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-169">30 per room</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-170">每个聊天室 150 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-170">150 per room</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-171">每个聊天室 16,000 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-171">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-172">聊天室</span><span class="sxs-lookup"><span data-stu-id="d8c2d-172">Chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-173">32,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-173">32,000</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-174">1,067</span><span class="sxs-lookup"><span data-stu-id="d8c2d-174">1,067</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-175">10</span><span class="sxs-lookup"><span data-stu-id="d8c2d-175">10</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-176">33,077</span><span class="sxs-lookup"><span data-stu-id="d8c2d-176">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-177">属于大会堂的聊天室百分比</span><span class="sxs-lookup"><span data-stu-id="d8c2d-177">% of rooms that are auditorium</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-178">1%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-178">1%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-179">1%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-179">1%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-180">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-180">50%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-181">开放式聊天室的百分比</span><span class="sxs-lookup"><span data-stu-id="d8c2d-181">% of rooms that are open</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-182">3%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-182">3%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-183">3%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-183">3%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-184">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-184">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-185">开放式聊天室数量（没有明确的成员身份）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-185">Open rooms (no explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-186">960</span><span class="sxs-lookup"><span data-stu-id="d8c2d-186">960</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-187">32</span><span class="sxs-lookup"><span data-stu-id="d8c2d-187">32</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-188">5</span><span class="sxs-lookup"><span data-stu-id="d8c2d-188">5</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-189">997</span><span class="sxs-lookup"><span data-stu-id="d8c2d-189">997</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-190">非开放式聊天室数量（具有明确的成员身份的普通聊天室）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-190">Non-open rooms (regular rooms with explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-191">31,040</span><span class="sxs-lookup"><span data-stu-id="d8c2d-191">31,040</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-192">1.035</span><span class="sxs-lookup"><span data-stu-id="d8c2d-192">1.035</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-193">5</span><span class="sxs-lookup"><span data-stu-id="d8c2d-193">5</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-194">32,080</span><span class="sxs-lookup"><span data-stu-id="d8c2d-194">32,080</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-195">大会堂聊天室数量（有更多的演示者进入）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-195">Auditorium rooms (additional presenters entry)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-196">0</span><span class="sxs-lookup"><span data-stu-id="d8c2d-196">0</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-197">32</span><span class="sxs-lookup"><span data-stu-id="d8c2d-197">32</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-198">5</span><span class="sxs-lookup"><span data-stu-id="d8c2d-198">5</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-199">按直接成员身份管理的聊天室比例</span><span class="sxs-lookup"><span data-stu-id="d8c2d-199">Rooms managed by direct membership</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-200">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-200">50%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-201">10%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-201">10%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-202">0%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-202">0%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-203">用户组管理的聊天室比率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-203">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-204">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-204">50%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-205">90%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-205">90%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-206">100%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-206">100%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-207">开放式聊天室的每个聊天室成员列表中的用户组数量（未明确指定）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-207">User groups in each chat room's membership list for open rooms (not specified explicitly)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-208">0</span><span class="sxs-lookup"><span data-stu-id="d8c2d-208">0</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-209">0</span><span class="sxs-lookup"><span data-stu-id="d8c2d-209">0</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-210">0</span><span class="sxs-lookup"><span data-stu-id="d8c2d-210">0</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-211">非开放式聊天室的每个聊天室成员列表中的用户数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-211">Users in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-212">大约</span><span class="sxs-lookup"><span data-stu-id="d8c2d-212">30</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-213">150</span><span class="sxs-lookup"><span data-stu-id="d8c2d-213">150</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-214">16,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-214">16,000</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-215">非开放式聊天室的每个聊天室成员列表中的用户组数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-215">User groups in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-216">3</span><span class="sxs-lookup"><span data-stu-id="d8c2d-216">3</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-217">5</span><span class="sxs-lookup"><span data-stu-id="d8c2d-217">5</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-218">10</span><span class="sxs-lookup"><span data-stu-id="d8c2d-218">10</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-219">每个聊天室的管理者列表中的用户和用户组数量（开放式和非开放式聊天室）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-219">Users and user groups in each chat room's manager list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-220">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-220">6</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-221">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-221">6</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-222">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-222">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-223">每个大会堂聊天室的演示者列表中的用户和用户组数量（开放式和非开放式聊天室）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-223">Users and user groups in each auditorium chat room's presenters list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-224">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-224">6</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-225">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-225">6</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-226">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-226">6</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-227">所有非开放式聊天室中基于用户的成员实体数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-227">User-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-228">465,600</span><span class="sxs-lookup"><span data-stu-id="d8c2d-228">465,600</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-229">15,520</span><span class="sxs-lookup"><span data-stu-id="d8c2d-229">15,520</span></span></p></td>
<td><p>-</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-230">所有非开放式聊天室中基于用户组的成员实体数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-230">User-group-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-231">46,560</span><span class="sxs-lookup"><span data-stu-id="d8c2d-231">46,560</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-232">4656</span><span class="sxs-lookup"><span data-stu-id="d8c2d-232">4656</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-233">50</span><span class="sxs-lookup"><span data-stu-id="d8c2d-233">50</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-234">所有大会堂聊天室中基于用户和用户组的实体数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-234">Users and user groups based entities across all auditorium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-235">0</span><span class="sxs-lookup"><span data-stu-id="d8c2d-235">0</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-236">192</span><span class="sxs-lookup"><span data-stu-id="d8c2d-236">192</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-237">50</span><span class="sxs-lookup"><span data-stu-id="d8c2d-237">50</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-238">所有聊天室管理者列表中基于用户和用户组的管理者实体数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-238">Users and user groups based manager entities across all chat rooms manager lists</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-239">192,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-239">192,000</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-240">6,400</span><span class="sxs-lookup"><span data-stu-id="d8c2d-240">6,400</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-241">60</span><span class="sxs-lookup"><span data-stu-id="d8c2d-241">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-242">每个聊天室的活动用户数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-242">Active users per chat room</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-243"><em>大约</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-243"><em>30</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-244"><em>150</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-244"><em>150</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-245"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-245"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-246">每个用户的聊天室数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-246">Chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-247"><em>至</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-247"><em>12</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-248"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-248"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-249"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-249"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-250"><em>utf-16</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-250"><em>16</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-251">每个聊天室成员列表中用户组的数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-251">User groups in each chat room’s membership list</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-252"><em>10</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-252"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-253"><em>10</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-253"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-254"><em>岁</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-254"><em>15</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-255">用户组管理的聊天室比率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-255">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-256"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-256"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-257"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-257"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-258"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-258"><em>50%</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-259">所有聊天室中基于用户组的成员实体数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-259">User-group-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-260">155,200</span><span class="sxs-lookup"><span data-stu-id="d8c2d-260">155,200</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-261">5173</span><span class="sxs-lookup"><span data-stu-id="d8c2d-261">5173</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-262">68</span><span class="sxs-lookup"><span data-stu-id="d8c2d-262">68</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-263">所有聊天室中基于用户的成员实体数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-263">User-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-264">465,600</span><span class="sxs-lookup"><span data-stu-id="d8c2d-264">465,600</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-265">77,600</span><span class="sxs-lookup"><span data-stu-id="d8c2d-265">77,600</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-266">72,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-266">72,000</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-267">每个聊天室的管理者、演示者和范围列表中的用户和用户组数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-267">Users and user groups in each chat room's manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-268">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-268">6</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-269">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-269">6</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-270">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-270">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-271">所有聊天室的管理者、演示者和范围列表中的用户和用户组数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-271">Users and user groups across all chat rooms' manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-272">192,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-272">192,000</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-273">6400</span><span class="sxs-lookup"><span data-stu-id="d8c2d-273">6400</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-274">60</span><span class="sxs-lookup"><span data-stu-id="d8c2d-274">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-275">访问控制项数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-275">Access control entries</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-276">704,160</span><span class="sxs-lookup"><span data-stu-id="d8c2d-276">704,160</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-277">26,768</span><span class="sxs-lookup"><span data-stu-id="d8c2d-277">26,768</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-278">160</span><span class="sxs-lookup"><span data-stu-id="d8c2d-278">160</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-279">731,088</span><span class="sxs-lookup"><span data-stu-id="d8c2d-279">731,088</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-280">最大访问控制项数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-280">Maximum access control entries</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="d8c2d-281">2,000,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-281">2,000,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8c2d-282">在前面的示例中，当你根据推荐的指南部署持久聊天服务器时，他们最多可以在启用了合规性的四个服务器池中处理最多80000个活动用户。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-282">In the preceding sample, when you deploy the Persistent Chat Servers according to the recommended guidelines, they can handle up to 80,000 active users across a four-server pool with compliance enabled.</span></span>

<span data-ttu-id="d8c2d-283">该示例显示按小（在任何给定时间具有 30 个活动用户）、中（150 个活动用户）和大（16,000 个活动用户）进行分类的聊天室。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-283">This sample shows chat rooms categorized as small (30 active users at any given time), medium (150 active users), and large (16,000 active users).</span></span> <span data-ttu-id="d8c2d-284">根据以下大小的 "聊天室" 的总数计算：</span><span class="sxs-lookup"><span data-stu-id="d8c2d-284">The number of chat rooms of a certain size is computed based on the total number of:</span></span>

  - <span data-ttu-id="d8c2d-285">系统中的活动用户数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-285">Active users in the system</span></span>

  - <span data-ttu-id="d8c2d-286">给定大小的聊天室中的活动用户数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-286">Active users in chat rooms of the given size</span></span>

  - <span data-ttu-id="d8c2d-287">单个用户加入的给定大小的聊天室数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-287">Chat rooms of the given size that a single user joins</span></span>

<span data-ttu-id="d8c2d-p111">对于每个聊天室，前面的容量规划表将指定与聊天室关联的访问控制项的数量，包括直接分配到聊天室的项。可以使用访问控制列表 (ACL) 控制对单个聊天室的访问，也可以在类别级别控制访问。在 ACL 中，单个访问控制项可以是用户组（例如，安全组、通讯组列表），也可以是单个用户。您可以为聊天室管理者、演示者和成员定义访问控制项。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-p111">For each chat room, the preceding capacity planning table specifies the number of access control entries that are associated with the chat room, including entries that are assigned directly to the chat room. You can control access to individual chat rooms by using access control lists (ACLs). You can also control access at the category level. In an ACL, an individual access control entry can be either a user group—for example, a security group, a distribution list, or a single user. You can define access control entries for chat room managers, presenters, and members.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d8c2d-p112">规划管理聊天室的策略时，请牢记允许的访问控制项总数是 200 万。如果计算出的访问控制项超过 200 万，服务器性能可能会显著降低。为避免这一问题，请尽可能确保您的访问控制项是用户组而非单个用户。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-p112">In planning your strategy for managing chat rooms, keep in mind that the total number of allowed access control entries is 2 million. If the calculated access control entries exceed 2 million, server performance could degrade significantly. To avoid this issue, whenever possible, be sure that your access control entries are user groups instead of individual users.</span></span>



</div>

</div>

<div>

## <a name="capacity-planning-for-managing-chat-room-access-by-invitation"></a><span data-ttu-id="d8c2d-296">通过邀请管理聊天室访问的容量计划</span><span class="sxs-lookup"><span data-stu-id="d8c2d-296">Capacity Planning for Managing Chat Room Access by Invitation</span></span>

<span data-ttu-id="d8c2d-297">当配置为发送邀请时，可以使用以下容量规划表了解持久聊天服务器在持久聊天数据库中创建和存储的邀请数。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-297">You can use the following capacity planning table to understand the number of invitations that Persistent Chat Server creates and stores in the Persistent Chat database when it is configured to send invitations.</span></span> <span data-ttu-id="d8c2d-298">通过使用 Lync Server 控制面板中的 " **聊天室类别设置** " 页面或使用 Windows PowerShell cmdlet **csPersistentChatCategory**，可在类别上管理邀请。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-298">You manage invitations on the Category by using the **Chat Room Category settings** page in the Lync Server Control Panel, or by using the Windows PowerShell cmdlet, **set-csPersistentChatCategory**.</span></span> <span data-ttu-id="d8c2d-299">你可以通过使用从 Lync 客户端 **启动的 csPersistentChatRoom** ，或使用 Windows PowerShell Cmdlet （ **set-csPersistentChatRoom**）在 (聊天室上管理邀请，即使用类别允许的内容) 。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-299">You can manage invitations on a chat room (in line with what the category allows) by using the **Room Management** page launched from the Lync client, or by using a Windows PowerShell cmdlet, **set-csPersistentChatRoom**.</span></span>

<span data-ttu-id="d8c2d-300">下表中的示例数据假定在 50% 聊天室的“**聊天室设置**”页面上，“**邀请**”选项设置为“**是**”。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-300">The sample data in the following table assumes that, on the **Chat room settings** page for 50 percent of all chat rooms, the **Invitations** option is set to **Yes**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d8c2d-301">如果计算出的服务器生成的邀请数量超过 100 万，服务器性能可能会显著降低。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-301">If the calculated value for the number of invitations that is generated by the server exceeds 1 million, server performance could degrade significantly.</span></span> <span data-ttu-id="d8c2d-302">若要避免此问题，请确保将配置为发送邀请的聊天室的数量减到最少，或者限制可加入聊天室的用户数，这些聊天室已配置为发送邀请。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-302">To avoid this issue, be sure that you minimize the number of chat rooms that are configured to send invitations or restrict the number of users who can join chat rooms that have been configured to send invitations.</span></span>



</div>

### <a name="chat-room-access-by-invitation-sample"></a><span data-ttu-id="d8c2d-303">通过邀请的聊天室访问示例</span><span class="sxs-lookup"><span data-stu-id="d8c2d-303">Chat Room Access by Invitation Sample</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d8c2d-304">小聊天室</span><span class="sxs-lookup"><span data-stu-id="d8c2d-304">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="d8c2d-305">中聊天室</span><span class="sxs-lookup"><span data-stu-id="d8c2d-305">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="d8c2d-306">大聊天室</span><span class="sxs-lookup"><span data-stu-id="d8c2d-306">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="d8c2d-307">总计</span><span class="sxs-lookup"><span data-stu-id="d8c2d-307">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-308">可以访问聊天室的用户数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-308">Users who can access chat room</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-309">每个聊天室 30 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-309">30 per room</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-310">每个聊天室 150 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-310">150 per room</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-311">每个聊天室 16,000 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-311">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-312">具有邀请的聊天室百分比</span><span class="sxs-lookup"><span data-stu-id="d8c2d-312">Percentage of rooms that have invitations</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-313">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-313">50%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-314">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-314">50%</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-315">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-315">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-316">配置为发送邀请的聊天室数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-316">Chat rooms configured to send invitations</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-317"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-317"><em>16,000</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-318"><em>533</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-318"><em>533</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-319"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-319"><em>5</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-320">可以访问聊天室的用户数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-320">Users who can access the chat room</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-321"><em>60</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-321"><em>60</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-322"><em>225</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-322"><em>225</em></span></span></p></td>
<td><p><span data-ttu-id="d8c2d-323"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="d8c2d-323"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-324">持久聊天服务器生成的邀请</span><span class="sxs-lookup"><span data-stu-id="d8c2d-324">Invitations generated by Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-325">960,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-325">960,000</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-326">120,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-326">120,000</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-327">80,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-327">80,000</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-328">1,160,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-328">1,160,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-329">允许的最大邀请数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-329">Maximum allowable number of invitations</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="d8c2d-330">2,000,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-330">2,000,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-331">模型 1 - 以每天每个聊天室的预期消息数开始</span><span class="sxs-lookup"><span data-stu-id="d8c2d-331">Model 1 - Start with expected number of messages per room per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-332">每个聊天室的聊天速率（每天）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-332">Chat Rate Per Room (per day)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-333">50</span><span class="sxs-lookup"><span data-stu-id="d8c2d-333">50</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-334">500</span><span class="sxs-lookup"><span data-stu-id="d8c2d-334">500</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-335">100</span><span class="sxs-lookup"><span data-stu-id="d8c2d-335">100</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-336">650</span><span class="sxs-lookup"><span data-stu-id="d8c2d-336">650</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-337">所有聊天室的聊天速率（每秒）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-337">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-338">55.56</span><span class="sxs-lookup"><span data-stu-id="d8c2d-338">55.56</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-339">18.52</span><span class="sxs-lookup"><span data-stu-id="d8c2d-339">18.52</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-340">0.03</span><span class="sxs-lookup"><span data-stu-id="d8c2d-340">0.03</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-341">74</span><span class="sxs-lookup"><span data-stu-id="d8c2d-341">74</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-342">模型 2 - 以每天每个用户发布的消息数开始</span><span class="sxs-lookup"><span data-stu-id="d8c2d-342">Model 2 - Start with number of messages posted per user per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-343">每个用户每天的聊天速率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-343">Chat rate per user per day</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-344">岁</span><span class="sxs-lookup"><span data-stu-id="d8c2d-344">15</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-345">5</span><span class="sxs-lookup"><span data-stu-id="d8c2d-345">5</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-346">0.1</span><span class="sxs-lookup"><span data-stu-id="d8c2d-346">0.1</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-347">名</span><span class="sxs-lookup"><span data-stu-id="d8c2d-347">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-348">每个聊天室的聊天速率（每天）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-348">Chat rate per room (per day)</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-349">38</span><span class="sxs-lookup"><span data-stu-id="d8c2d-349">38</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-350">375</span><span class="sxs-lookup"><span data-stu-id="d8c2d-350">375</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-351">800</span><span class="sxs-lookup"><span data-stu-id="d8c2d-351">800</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-352">1,213</span><span class="sxs-lookup"><span data-stu-id="d8c2d-352">1,213</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-353">所有聊天室的聊天速率（每秒）</span><span class="sxs-lookup"><span data-stu-id="d8c2d-353">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-354">41.67</span><span class="sxs-lookup"><span data-stu-id="d8c2d-354">41.67</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-355">13.89</span><span class="sxs-lookup"><span data-stu-id="d8c2d-355">13.89</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-356">0.28</span><span class="sxs-lookup"><span data-stu-id="d8c2d-356">0.28</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-357">56</span><span class="sxs-lookup"><span data-stu-id="d8c2d-357">56</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="d8c2d-358">持久聊天服务器性能用户模型</span><span class="sxs-lookup"><span data-stu-id="d8c2d-358">Persistent Chat Server Performance User Model</span></span>

<span data-ttu-id="d8c2d-359">下表介绍持久聊天服务器的用户模型。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-359">The following table describes the user model for Persistent Chat Server.</span></span> <span data-ttu-id="d8c2d-360">它提供了容量规划要求的基础，并代表一个在四台服务器上拥有 80,000 个并发用户的典型组织。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-360">It provides the basis for the capacity planning requirements and represents a typical organization with 80,000 concurrent users on four servers.</span></span>

### <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="d8c2d-361">持久聊天服务器性能用户模型</span><span class="sxs-lookup"><span data-stu-id="d8c2d-361">Persistent Chat Server Performance User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-362">连接的活动用户的数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-362">Number of active users connected</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-363">80,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-363">80,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-364">持久聊天服务器服务实例数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-364">Number of Persistent Chat Server service instances</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-365">4</span><span class="sxs-lookup"><span data-stu-id="d8c2d-365">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-366">小聊天室的大小</span><span class="sxs-lookup"><span data-stu-id="d8c2d-366">Size of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-367">30 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-367">30 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-368">中聊天室的大小</span><span class="sxs-lookup"><span data-stu-id="d8c2d-368">Size of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-369">150 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-369">150 users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-370">大聊天室的大小</span><span class="sxs-lookup"><span data-stu-id="d8c2d-370">Size of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-371">16,000 个用户</span><span class="sxs-lookup"><span data-stu-id="d8c2d-371">16,000 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-372">聊天室的总数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-372">Total number of chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-373">33,077</span><span class="sxs-lookup"><span data-stu-id="d8c2d-373">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-374">小聊天室的数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-374">Number of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-375">32,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-375">32,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-376">中聊天室的数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-376">Number of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-377">1,067</span><span class="sxs-lookup"><span data-stu-id="d8c2d-377">1,067</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-378">大聊天室的数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-378">Number of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-379">10</span><span class="sxs-lookup"><span data-stu-id="d8c2d-379">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-380">每个用户的聊天室总数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-380">Total number of chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-381">utf-16</span><span class="sxs-lookup"><span data-stu-id="d8c2d-381">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-382">每个用户的小聊天室数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-382">Number of small chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-383">至</span><span class="sxs-lookup"><span data-stu-id="d8c2d-383">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-384">每个用户的中聊天室数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-384">Number of medium chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-385">2</span><span class="sxs-lookup"><span data-stu-id="d8c2d-385">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-386">每个用户的大聊天室数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-386">Number of large chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-387">2</span><span class="sxs-lookup"><span data-stu-id="d8c2d-387">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-388">每个用户加入的聊天室数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-388">Number of rooms joined per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-389">全</span><span class="sxs-lookup"><span data-stu-id="d8c2d-389">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-390">峰值加入速率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-390">Peak join rate</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-391">10 个/秒</span><span class="sxs-lookup"><span data-stu-id="d8c2d-391">10/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-392">总聊天速率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-392">Total chat rate</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-393">24 个/秒</span><span class="sxs-lookup"><span data-stu-id="d8c2d-393">24/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-394">小聊天室的聊天速率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-394">Chat rate for small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-395">22.22/second</span><span class="sxs-lookup"><span data-stu-id="d8c2d-395">22.22/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-396">中聊天室的聊天速率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-396">Chat rate for medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-397">1.67/second</span><span class="sxs-lookup"><span data-stu-id="d8c2d-397">1.67/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-398">大聊天室的聊天速率</span><span class="sxs-lookup"><span data-stu-id="d8c2d-398">Chat rate for large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-399">~0.15/second</span><span class="sxs-lookup"><span data-stu-id="d8c2d-399">~0.15/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-400">为邀请配置的聊天室的百分比</span><span class="sxs-lookup"><span data-stu-id="d8c2d-400">Percentage of chat rooms configured for invitations</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-401">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-401">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-402">直接成员身份的百分比</span><span class="sxs-lookup"><span data-stu-id="d8c2d-402">Percentage of direct memberships</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-403">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-403">50%</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-404">组成员身份的百分比</span><span class="sxs-lookup"><span data-stu-id="d8c2d-404">Percentage of group memberships</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-405">50%</span><span class="sxs-lookup"><span data-stu-id="d8c2d-405">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-406">Active Directory 域服务中上级隶属关系的平均数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-406">Average number of ancestor affiliations in Active Directory Domain Services</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-407">100 - 200</span><span class="sxs-lookup"><span data-stu-id="d8c2d-407">100 - 200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-408">每个用户的订阅联系人数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-408">Number of subscribed contacts per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-409">80</span><span class="sxs-lookup"><span data-stu-id="d8c2d-409">80</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-410">每个用户的平均终结点数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-410">Average number of endpoints per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-411">1.5</span><span class="sxs-lookup"><span data-stu-id="d8c2d-411">1.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-412">每个终结点的平均可见聊天室数</span><span class="sxs-lookup"><span data-stu-id="d8c2d-412">Average number of visible chat rooms per endpoint</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-413">1.5</span><span class="sxs-lookup"><span data-stu-id="d8c2d-413">1.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-414">每个用户可见的平均聊天室数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-414">Average number of visible chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-415">2.25（一个聊天室为 50%，两个聊天室也为 50%）；最多 6 个聊天室开放，每个监视器一个</span><span class="sxs-lookup"><span data-stu-id="d8c2d-415">2.25 (50% for 1 room and 50% for 2 rooms); Up to 6 rooms open, one per monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-416">每个时间间隔轮询的参与者数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-416">Number of participants polled per interval</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-417">每个可见聊天室 25 个</span><span class="sxs-lookup"><span data-stu-id="d8c2d-417">25 per visible chat room</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-418">轮询间隔时长</span><span class="sxs-lookup"><span data-stu-id="d8c2d-418">Length of polling interval</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-419">5 分钟</span><span class="sxs-lookup"><span data-stu-id="d8c2d-419">5 minutes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-420">每秒钟轮询的参与者数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-420">Number of participants polled per second</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-421">15,000</span><span class="sxs-lookup"><span data-stu-id="d8c2d-421">15,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8c2d-422">每个用户每小时的状态更改数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-422">Number of presence changes per hour per user</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-423">6</span><span class="sxs-lookup"><span data-stu-id="d8c2d-423">6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8c2d-424">每秒钟的状态更改数量</span><span class="sxs-lookup"><span data-stu-id="d8c2d-424">Number of presence changes per second</span></span></p></td>
<td><p><span data-ttu-id="d8c2d-425">133.33</span><span class="sxs-lookup"><span data-stu-id="d8c2d-425">133.33</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d8c2d-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8c2d-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

