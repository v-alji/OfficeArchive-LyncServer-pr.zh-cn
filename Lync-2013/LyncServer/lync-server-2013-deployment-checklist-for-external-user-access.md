---
title: Lync Server 2013：外部用户访问的部署清单
description: Lync Server 2013：用于外部用户访问的部署清单。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for external user access
ms:assetid: 3f55f502-88a0-4315-8783-45a32a0b78ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425910(v=OCS.15)
ms:contentKeyID: 48183947
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a31534d1dcf3ba4dd0bb222de682d247c9683f94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392155"
---
# <a name="deployment-checklist-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="7dc2f-103">Lync Server 2013 中外部用户访问的部署清单</span><span class="sxs-lookup"><span data-stu-id="7dc2f-103">Deployment checklist for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7dc2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7dc2f-104">

<span> </span></span></span>

<span data-ttu-id="7dc2f-105">_**主题上次修改时间：** 2014-02-04_</span><span class="sxs-lookup"><span data-stu-id="7dc2f-105">_**Topic Last Modified:** 2014-02-04_</span></span>

<span data-ttu-id="7dc2f-106">在部署你的外围网络并实现对外部用户的支持之前，你必须已部署 Microsoft Lync Server 2013 内部服务器，包括前端池或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-106">Before you deploy your perimeter network and implement support for external users, you must already have deployed your Microsoft Lync Server 2013 internal servers, including a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="7dc2f-107">如果你计划在内部网络中部署可选控制器，还应在部署 Edge 服务器之前部署它们。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-107">If you plan to deploy the optional Directors in your internal network, you should also deploy them prior to deploying Edge Servers.</span></span> <span data-ttu-id="7dc2f-108">有关 Director 部署过程的详细信息，请参阅规划文档中 [Lync Server 2013 中的 Director 方案](lync-server-2013-scenarios-for-the-director.md) 。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-108">For details about the Director deployment process, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

<span data-ttu-id="7dc2f-109">Microsoft Lync Server 2013 包括便于规划和部署内部服务器和边缘服务器的工具。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-109">Microsoft Lync Server 2013 includes tools to facilitate planning and deployment of both internal servers and Edge Servers.</span></span> <span data-ttu-id="7dc2f-110">拓扑完成后，将生成的拓扑定义发布到生产环境。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-110">After the topology is completed, publish the resulting topology definition to your production environment.</span></span> <span data-ttu-id="7dc2f-111">若要执行此操作，您必须是 " **域管理员** " 组和 " **RTCUniversalServerAdmins** " 组的成员。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-111">To do this, you must be a member of the **Domain Admins** group and the **RTCUniversalServerAdmins** group.</span></span>

  - <span data-ttu-id="7dc2f-112">**规划工具**   Office 通信服务器 2007 R2 包括一个计划工具和一条边缘规划工具，可用于帮助指导拓扑设计。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-112">**Planning Tool**   Office Communications Server 2007 R2 included a Planning Tool and an Edge Planning Tool that you could use to help guide topology design.</span></span> <span data-ttu-id="7dc2f-113">在 Lync Server 2010 中，这两个工具合并到了一个计划工具中，该工具具有额外的功能，例如收集计划的用户计数、语音要求、外部用户访问类型和联盟选项。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-113">In Lync Server 2010, these two tools were combined into a single Planning Tool that has additional features and functionality, such as collecting planned user count, voice requirements, external user access types, and federation options.</span></span> <span data-ttu-id="7dc2f-114">此外，你可以规划基础结构的网络参数，例如 IP 地址、负载平衡器类型和其他外围网络注意事项。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-114">Additionally, you can plan your infrastructure’s network parameters, such as IP addresses, load balancer types and other perimeter network considerations.</span></span>

  - <span data-ttu-id="7dc2f-115">**拓扑生成器**   Lync Server 2013 拓扑生成器可帮助你定义拓扑和组件。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-115">**Topology Builder**   Lync Server 2013 Topology Builder helps you define your topology and components.</span></span> <span data-ttu-id="7dc2f-116">拓扑生成器对于运行 Lync Server 2013 的服务器来说非常重要。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-116">Topology Builder is essential to deploying servers running Lync Server 2013.</span></span> <span data-ttu-id="7dc2f-117">拓扑生成器将结果发布到用于配置组织中运行 Lync Server 2013 的所有服务器的中央管理存储。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-117">Topology Builder publishes the results to a Central Management store that is used to configure all of the servers running Lync Server 2013 in your organization.</span></span> <span data-ttu-id="7dc2f-118">无法在不使用拓扑生成器的情况下在服务器上安装 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-118">You cannot install Lync Server 2013 on servers without using Topology Builder.</span></span>

<span data-ttu-id="7dc2f-119">如果你在计划过程中设计了 edge 拓扑，包括运行拓扑生成器以定义边缘拓扑，则可以使用这些结果开始边缘服务器部署。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-119">If you designed your edge topology during your planning process, including running Topology Builder to define your edge topology, you can use those results to start your Edge Server deployment.</span></span> <span data-ttu-id="7dc2f-120">如果你之前未完成构建 edge 拓扑或想要更改以前指定的信息，则必须先完成拓扑生成器运行，然后再继续执行其他部署步骤。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-120">If you did not finish building your edge topology earlier or you want to change the information you previously specified, you must finish running Topology Builder before proceeding with other deployment steps.</span></span> <span data-ttu-id="7dc2f-121">有关如何构建拓扑的详细信息，请参阅 [Lync Server 2013 中的外部用户访问方案](lync-server-2013-scenarios-for-external-user-access.md)。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-121">For details about how to build your topology, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="7dc2f-122">有关规划工具和拓扑生成器的详细信息，请参阅在规划文档中 [开始 Lync Server 2013 的规划过程](lync-server-2013-beginning-the-planning-process.md) 。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-122">For details about the Planning Tool and Topology Builder, see [Beginning the planning process for Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in the Planning documentation.</span></span>

<span data-ttu-id="7dc2f-123">下表提供了边缘服务器部署过程的概述。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-123">The following table provides an overview of the Edge Server deployment process.</span></span> <span data-ttu-id="7dc2f-124">若要查看在部署外部用户访问之前必须制定的规划决策，请参阅 [Lync Server 2013 中的外部用户访问方案](lync-server-2013-scenarios-for-external-user-access.md)。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-124">To review the planning decisions that must be made before deploying external user access, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="7dc2f-125">下表中的信息重点介绍新的部署。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-125">The information in the following table focuses on a new deployment.</span></span> <span data-ttu-id="7dc2f-126">如果你已在 Lync Server 2010、Office 通信服务器 2007 R2 或 Office 通信服务器2007环境中部署了 Edge 服务器，请参阅 <A href="migration.md">迁移</A> 以了解有关迁移到 Lync Server 2013 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-126">If you have deployed Edge Servers in a Lync Server 2010, Office Communications Server 2007 R2 or Office Communications Server 2007 environment, see the <A href="migration.md">Migration</A> for details about migrating to Lync Server 2013.</span></span> <span data-ttu-id="7dc2f-127">Office 通信服务器 2007 R2 之前的任何版本均不支持迁移，包括 Office 通信服务器2007、实时通信服务器2005和实时通信服务器2003。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-127">Migration is not supported from any version prior to Office Communications Server 2007 R2, including Office Communications Server 2007, Live Communications Server 2005, and Live Communications Server 2003.</span></span>



</div>

<span data-ttu-id="7dc2f-128">若要提高边缘服务器性能和安全性以及便于部署，请在部署外围网络和边缘服务器时应用以下最佳做法：</span><span class="sxs-lookup"><span data-stu-id="7dc2f-128">To enhance Edge Server performance and security, and to facilitate deployment, apply the following best practices when you deploy your perimeter network and Edge Servers:</span></span>

  - <span data-ttu-id="7dc2f-129">只有在组织内部对 Lync Server 2013 进行了测试和验证后，才部署 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-129">Deploy Edge Servers only after you have tested and verified operation of Lync Server 2013 inside your organization.</span></span>

  - <span data-ttu-id="7dc2f-130">我们建议你在工作组而不是域中部署边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-130">We recommend that you deploy Edge Servers in a workgroup rather than a domain.</span></span> <span data-ttu-id="7dc2f-131">这样做会简化安装，并保留 Active Directory 域服务 (AD DS) 外围网络。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-131">Doing so simplifies installation and keeps Active Directory Domain Services (AD DS) out of the perimeter network.</span></span> <span data-ttu-id="7dc2f-132">在外围网络中查找 AD DS 可能会带来严重的安全风险。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-132">Locating AD DS in the perimeter network can present a significant security risk.</span></span>

  - <span data-ttu-id="7dc2f-133">支持将 Edge 服务器联接到完全位于外围网络的域，但不建议这样做。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-133">Joining an Edge Server to a domain located entirely in the perimeter network is supported but not recommended.</span></span> <span data-ttu-id="7dc2f-134">作为内部域的一部分的边缘服务器违反受信任网络边界，其中 Internet 最少受信任，外围网络比 Internet 更受信任，并且内部网络最受信任。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-134">An Edge Server as part of the internal domain violates trusted network boundaries, where the Internet is least trusted, perimeter network is more trusted than the Internet, and the internal network is most trusted.</span></span> <span data-ttu-id="7dc2f-135">作为域成员的边缘服务器会自动成为最受信任网络的一部分，但驻留在不太受信任的网络中 (外围) 。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-135">An Edge server as a member of the domain is automatically a part of the most trusted network, but resides in a less trusted network (the perimeter).</span></span>

<div>

## <a name="deployment-process-for-edge-servers"></a><span data-ttu-id="7dc2f-136">边缘服务器的部署过程</span><span class="sxs-lookup"><span data-stu-id="7dc2f-136">Deployment Process for Edge Servers</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7dc2f-137">阶段</span><span class="sxs-lookup"><span data-stu-id="7dc2f-137">Phase</span></span></th>
<th><span data-ttu-id="7dc2f-138">步骤</span><span class="sxs-lookup"><span data-stu-id="7dc2f-138">Steps</span></span></th>
<th><span data-ttu-id="7dc2f-139">权限</span><span class="sxs-lookup"><span data-stu-id="7dc2f-139">Permissions</span></span></th>
<th><span data-ttu-id="7dc2f-140">文档</span><span class="sxs-lookup"><span data-stu-id="7dc2f-140">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dc2f-141">创建适当的边缘拓扑，并确定相应的组件。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-141">Create the appropriate edge topology and determine the appropriate components.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7dc2f-142">运行拓扑生成器以配置边缘服务器设置，并创建和发布拓扑，然后使用 Lync Server Management Shell 导出拓扑配置文件。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-142">Run Topology Builder to configure Edge Server settings and create and publish the topology, and then use Lync Server Management Shell to export the topology configuration file.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7dc2f-143"><strong>域管理员</strong> 组和 <strong>RTCUniversalServerAdmins</strong> 或 <strong>CsAdmins</strong> 组</span><span class="sxs-lookup"><span data-stu-id="7dc2f-143"><strong>Domain Admins</strong> group and <strong>RTCUniversalServerAdmins</strong> or <strong>CsAdmins</strong> group</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="7dc2f-144">你可以使用属于本地用户组的成员的帐户定义拓扑，但发布拓扑需要一个帐户，该帐户是 <STRONG>域管理员</STRONG> 组和 <STRONG>RTCUniversalServerAdmins</STRONG> 组的成员。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-144">You can define a topology using an account that is a member of the local users group, but publishing a topology requires an account that is a member of the <STRONG>Domain Admins</STRONG> group and the <STRONG>RTCUniversalServerAdmins</STRONG> group.</span></span>


</div></td>
<td><p><span data-ttu-id="7dc2f-145">在部署文档的<a href="lync-server-2013-building-an-edge-and-director-topology.md">Lync Server 2013 中构建边缘和控制器拓扑</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-145"><a href="lync-server-2013-building-an-edge-and-director-topology.md">Building an edge and Director topology in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dc2f-146">准备设置。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-146">Prepare for setup.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="7dc2f-147">确保满足系统先决条件。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-147">Ensure that system prerequisites are met.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-148">配置 (IPv4 和 IPv6 的 IP 地址（如果在每台边缘服务器上对内部和面向公众的网络接口使用) ）。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-148">Configure IP addresses (IPv4 and IPv6, if used) for both internal and public facing network interfaces on each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-149"> (IPv4 和 IPv6) 的主机 A 和 AAAA 配置内部和外部 DNS 记录，包括在计算机上配置 DNS 后缀以将其部署为 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-149">Configure internal and external DNS records (host A and AAAA for IPv4 and IPv6), including configuring the DNS suffix on the computer to be deployed as an Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-150"> (可选) 创建和安装公共证书。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-150">(Optional) Create and install public certificates.</span></span> <span data-ttu-id="7dc2f-151">获取证书所需的时间取决于颁发证书的证书颁发机构 (CA) 颁发证书。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-151">The time required to obtain certificates depends on which certification authority (CA) issues the certificate.</span></span> <span data-ttu-id="7dc2f-152">如果此时不执行此步骤，则必须在安装边缘服务器期间执行此操作。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-152">If you do not perform this step at this point, you must do it during Edge Server installation.</span></span> <span data-ttu-id="7dc2f-153">无法启动 Edge 服务器服务，直到获得并安装证书。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-153">The Edge Server services cannot be started until certificates are obtained and installed.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-154">如果你的部署支持与 Windows Live、AOL 或 Yahoo！的通信，则预配对公共 IM 连接的支持</span><span class="sxs-lookup"><span data-stu-id="7dc2f-154">Provision support for public IM connectivity, if your deployment is to support communications with Windows Live, AOL, or Yahoo!</span></span> <span data-ttu-id="7dc2f-155">那些.</span><span class="sxs-lookup"><span data-stu-id="7dc2f-155">users.</span></span></p>
<div>

> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="7dc2f-156">从2012年9月1日起，，Microsoft Lync 公共 IM 连接用户订阅许可证 ( "PIC USL" ) 不再可用于购买新的或续订协议。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-156">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="7dc2f-157">具有活动许可证的客户将能够继续与 Yahoo！进行联盟</span><span class="sxs-lookup"><span data-stu-id="7dc2f-157">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="7dc2f-158">Messenger，直到服务关闭日期。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-158">Messenger until the service shut down date.</span></span> <span data-ttu-id="7dc2f-159">AOL 和 Yahoo！的有效期结束日期为2014年6月</span><span class="sxs-lookup"><span data-stu-id="7dc2f-159">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="7dc2f-160">已宣布。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-160">has been announced.</span></span> <span data-ttu-id="7dc2f-161">有关详细信息，请参阅 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 中的公共即时消息连接支持</A>。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-161">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="7dc2f-162">PIC USL 是 Lync Server 或 Office 通信服务器与 Yahoo！联合所需的每个每个用户每月订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-162">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="7dc2f-163">Messenger.</span><span class="sxs-lookup"><span data-stu-id="7dc2f-163">Messenger.</span></span> <span data-ttu-id="7dc2f-164">Microsoft 提供此服务的能力已作为对 Yahoo！的支持，它的底层协议被向下缠绕。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-164">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="7dc2f-165">Lync 比以往更多，是一种强大的工具，用于跨组织和全球各地的人员进行连接。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-165">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="7dc2f-166">与 Windows Live Messenger 的联盟不需要除 Lync 标准 CAL 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-166">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="7dc2f-167">Skype 联盟将添加到此列表，使 Lync 用户可以通过 IM 和语音与成百上千人联系。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-167">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


</div></li>
<li><p><span data-ttu-id="7dc2f-168">预配支持 Office 通信服务器2007、Office 通信服务器 2007 R2、Lync Server 2010 合作伙伴的 XMPP 和联合支持，如果你的部署将使用这些</span><span class="sxs-lookup"><span data-stu-id="7dc2f-168">Provision support for XMPP and federation support for Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 partners, if your deployment will use these</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-169">配置防火墙。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-169">Configure firewalls.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="7dc2f-170">根据您的组织的需要</span><span class="sxs-lookup"><span data-stu-id="7dc2f-170">As appropriate to your organization</span></span></p></td>
<td><p><span data-ttu-id="7dc2f-171">准备在部署文档中<a href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Lync Server 2013 的外围网络中安装服务器</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-171"><a href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Preparing for installation of servers in the perimeter network for Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dc2f-172">设置反向代理。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-172">Set up reverse proxy.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7dc2f-173">设置反向代理 (例如，对于 Microsoft Forefront 威胁管理网关2010或 Microsoft Internet 安全和加速 (在外围网络中具有 Service Pack 1) 的 ISA) Server，获取必要的公共证书，并在反向代理服务器上配置 web 发布规则。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-173">Set up the reverse proxy (for example, for Microsoft Forefront Threat Management Gateway 2010 or Microsoft Internet Security and Acceleration (ISA) Server with Service Pack 1) in the perimeter network, obtain the necessary public certificates, and configure the web publishing rules on the reverse proxy server.</span></span></p>
<p><span data-ttu-id="7dc2f-174">如果你计划移动服务并在前端池或标准版服务器上部署移动服务，请为移动服务准备反向代理。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-174">Prepare the reverse proxy for Mobility services if you have planned for Mobility and are deploying the Mobility services on the Front End pool or Standard Edition server.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7dc2f-175"><strong>管理员</strong> 组或反向代理管理员</span><span class="sxs-lookup"><span data-stu-id="7dc2f-175"><strong>Administrators</strong> group or Reverse Proxy administrator</span></span></p></td>
<td><p><span data-ttu-id="7dc2f-176">在部署文档中<a href="lync-server-2013-setting-up-reverse-proxy-servers.md">为 Lync Server 2013 设置反向代理服务器</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-176"><a href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dc2f-177">设置 Director (可选) 。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-177">Setup a Director (optional).</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7dc2f-178"> (可选) 在内部网络中安装和配置一个或多个控制器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-178">(Optional) Install and configure one or more Directors in the internal network.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7dc2f-179"><strong>管理员</strong> 组</span><span class="sxs-lookup"><span data-stu-id="7dc2f-179"><strong>Administrators</strong> group</span></span></p></td>
<td><p><span data-ttu-id="7dc2f-180">在部署文档的<a href="lync-server-2013-setting-up-the-director.md">Lync Server 2013 中设置 Director</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-180"><a href="lync-server-2013-setting-up-the-director.md">Setting up the Director in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dc2f-181">设置边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-181">Set up Edge Servers.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="7dc2f-182">安装必备软件。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-182">Install prerequisite software.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-183">将导出的拓扑配置文件传输到每台边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-183">Transport the exported topology configuration file to each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-184">在每台边缘服务器上安装 Lync Server 2013 软件。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-184">Install the Lync Server 2013 software on each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-185">配置边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-185">Configure the Edge Servers.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-186">为每个边缘服务器请求和安装证书。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-186">Request and install certificates for each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-187">启动边缘服务器服务。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-187">Start the Edge Server services.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="7dc2f-188"><strong>管理员</strong> 组</span><span class="sxs-lookup"><span data-stu-id="7dc2f-188"><strong>Administrators</strong> group</span></span></p></td>
<td><p><span data-ttu-id="7dc2f-189">在部署文档的<a href="lync-server-2013-setting-up-edge-servers.md">Lync Server 2013 中设置边缘服务器</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-189"><a href="lync-server-2013-setting-up-edge-servers.md">Setting up Edge Servers in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dc2f-190">为外部用户访问配置部署。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-190">Configure deployment for external user access.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="7dc2f-191">根据适用) ，使用 Lync Server 控制面板配置对以下每个 (的支持：</span><span class="sxs-lookup"><span data-stu-id="7dc2f-191">Use the Lync Server Control Panel to configure support for each of the following (as applicable):</span></span></p>
<ul>
<li><p><span data-ttu-id="7dc2f-192">媒体中继</span><span class="sxs-lookup"><span data-stu-id="7dc2f-192">Media relay</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-193">联盟路线</span><span class="sxs-lookup"><span data-stu-id="7dc2f-193">Federation route</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-194">远程用户访问</span><span class="sxs-lookup"><span data-stu-id="7dc2f-194">Remote user access</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-195">与 Lync Server、Office 通信服务器和实时通信服务器的联盟</span><span class="sxs-lookup"><span data-stu-id="7dc2f-195">Federation with Lync Server, Office Communications Server and Live Communications Server</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-196">公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="7dc2f-196">Public IM connectivity</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-197">XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="7dc2f-197">XMPP federation</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-198">匿名用户</span><span class="sxs-lookup"><span data-stu-id="7dc2f-198">Anonymous users</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="7dc2f-199">将远程用户访问、联盟、公共 IM 连接、XMPP 和匿名用户支持 (的用户帐户配置为适用) </span><span class="sxs-lookup"><span data-stu-id="7dc2f-199">Configure user accounts for remote user access, federation, public IM connectivity, XMPP and anonymous user support (as applicable)</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="7dc2f-200">分配给<strong>CSAdministrator</strong>角色的<strong>RTCUniversalServerAdmins</strong>组或用户帐户</span><span class="sxs-lookup"><span data-stu-id="7dc2f-200"><strong>RTCUniversalServerAdmins</strong> group or user account that is assigned to the <strong>CSAdministrator</strong> role</span></span></p></td>
<td><p><span data-ttu-id="7dc2f-201">在部署文档中<a href="lync-server-2013-configuring-support-for-external-user-access.md">配置 Lync Server 2013 中外部用户访问的支持</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-201"><a href="lync-server-2013-configuring-support-for-external-user-access.md">Configuring support for external user access in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dc2f-202">验证边缘服务器配置。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-202">Verify your Edge Server configuration.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="7dc2f-203">验证服务器连接和来自内部服务器的配置数据的复制。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-203">Verify server connectivity and replication of configuration data from internal servers.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-204">验证外部用户是否可以连接，包括远程用户、联盟域中的用户、公共 IM 用户以及匿名用户（根据你的部署情况）。</span><span class="sxs-lookup"><span data-stu-id="7dc2f-204">Verify that external users can connect, including remote users, users in federated domains, public IM users, and anonymous users, as appropriate to your deployment.</span></span></p></li>
<li><p><span data-ttu-id="7dc2f-205">使用 Lync Server 远程连接分析器验证配置和通信 <a href="https://www.testocsconnectivity.com" class="uri">https://www.testocsconnectivity.com</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-205">Verify configuration and communication using the Lync Server Remote Connectivity Analyzer <a href="https://www.testocsconnectivity.com" class="uri">https://www.testocsconnectivity.com</a></span></span></p></li>
<li><p><span data-ttu-id="7dc2f-206">解决配置和通信问题</span><span class="sxs-lookup"><span data-stu-id="7dc2f-206">Troubleshoot configuration and communication difficulties</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="7dc2f-207">有关复制的验证，请 <strong>RTCUniversalServerAdmins</strong> 组或分配给 <strong>CSAdministrator</strong> 角色的用户帐户</span><span class="sxs-lookup"><span data-stu-id="7dc2f-207">For verification of replication, <strong>RTCUniversalServerAdmins</strong> group or user account that is assigned to the <strong>CSAdministrator</strong> role</span></span></p>
<p><span data-ttu-id="7dc2f-208">对于用户连接，您支持的每种类型的外部用户访问的用户</span><span class="sxs-lookup"><span data-stu-id="7dc2f-208">For verification of user connectivity, a user for each type of external user access that you support</span></span></p>
<p><span data-ttu-id="7dc2f-209">远程用户</span><span class="sxs-lookup"><span data-stu-id="7dc2f-209">Remote users</span></span></p></td>
<td><p><span data-ttu-id="7dc2f-210">在部署文档的<a href="lync-server-2013-verifying-your-edge-deployment.md">Lync Server 2013 中验证 edge 部署</a></span><span class="sxs-lookup"><span data-stu-id="7dc2f-210"><a href="lync-server-2013-verifying-your-edge-deployment.md">Verifying your edge deployment in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr><span data-ttu-id="7dc2f-211">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7dc2f-211">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

