---
title: Lync Server 2013：定义边缘拓扑
description: Lync Server 2013：定义边缘拓扑。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define your edge topology
ms:assetid: 787b23f1-8fa0-4c37-abf2-c516c5dd66f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398591(v=OCS.15)
ms:contentKeyID: 48184562
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd4aa16ca23d24f0edd92189216030ef926fc841
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431034"
---
# <a name="define-your-edge-topology-in-lync-server-2013"></a><span data-ttu-id="10a52-103">在 Lync Server 2013 中定义边缘拓扑</span><span class="sxs-lookup"><span data-stu-id="10a52-103">Define your edge topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10a52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10a52-104">

<span> </span></span></span>

<span data-ttu-id="10a52-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="10a52-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="10a52-106">必须使用拓扑生成器构建拓扑，并且必须至少设置一个内部前端池或标准版服务器，然后才能部署 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-106">You must use Topology Builder to build your topology and you must set up at least one internal Front End pool or Standard Edition server before you can deploy your Edge Server.</span></span> <span data-ttu-id="10a52-107">使用以下过程定义单个边缘服务器的边缘拓扑，然后使用在 [Lync server 2013 中发布拓扑](lync-server-2013-publish-your-topology.md) 中的过程并 [导出 lync server 2013 拓扑，并将其复制到外部媒体以进行边缘安装](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) 以发布拓扑，并使其可供边缘服务器使用。</span><span class="sxs-lookup"><span data-stu-id="10a52-107">Use the following procedure to define the edge topology for a single Edge Server, and then use the procedures in [Publish your topology in Lync Server 2013](lync-server-2013-publish-your-topology.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) to publish the topology and make it available to your Edge Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="10a52-108">内部边缘接口和外部边缘接口必须使用同一类型的负载平衡。</span><span class="sxs-lookup"><span data-stu-id="10a52-108">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="10a52-109">您不能在一个边缘接口上使用 DNS 负载平衡的同时，在另一个边缘接口上使用硬件负载平衡。</span><span class="sxs-lookup"><span data-stu-id="10a52-109">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="10a52-110">若要在添加或删除服务器角色时成功发布、启用或禁用拓扑，您必须以 RTCUniversalServerAdmins 和域管理员组成员的用户身份登录。</span><span class="sxs-lookup"><span data-stu-id="10a52-110">To successfully publish, enable, or disable a topology when adding or removing a server role, you must be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="10a52-111">你还可以授予将服务器角色添加到用户帐户所需的管理员权限和权限。</span><span class="sxs-lookup"><span data-stu-id="10a52-111">You can also grant the administrator rights and permissions required for adding server roles to a user account.</span></span> <span data-ttu-id="10a52-112">有关详细信息，请参阅在标准版服务器或企业版服务器部署文档中 [Lync Server 2013 中的 "委派设置权限](lync-server-2013-delegate-setup-permissions.md) "。</span><span class="sxs-lookup"><span data-stu-id="10a52-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="10a52-113">对于其他配置更改，仅需要 RTCUniversalServerAdmins 组中的成员身份。</span><span class="sxs-lookup"><span data-stu-id="10a52-113">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<span data-ttu-id="10a52-114">如果你在定义和发布内部拓扑时定义了 edge 拓扑，并且你以前定义的边缘拓扑不需要进行任何更改，则无需定义它并再次发布它。</span><span class="sxs-lookup"><span data-stu-id="10a52-114">If you defined your edge topology when you defined and published your internal topology, and no changes are required to the edge topology that you previously defined, you do not need to do define it and publish it again.</span></span> <span data-ttu-id="10a52-115">仅当需要对 edge 拓扑进行更改时，请使用以下过程。</span><span class="sxs-lookup"><span data-stu-id="10a52-115">Use the following procedure only if you need to make changes to your edge topology.</span></span> <span data-ttu-id="10a52-116">你必须将以前定义和发布的拓扑提供给你的边缘服务器，你可以通过使用 [导出 Lync Server 2013 拓扑中的过程并将其复制到外部媒体进行边缘安装](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="10a52-116">You must make the previously defined and published topology available to your Edge Servers, which you do by using the procedure in [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="10a52-117">不能从边缘服务器运行拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="10a52-117">You cannot run Topology Builder from an Edge Server.</span></span> <span data-ttu-id="10a52-118">必须从前端服务器或标准版服务器运行它。</span><span class="sxs-lookup"><span data-stu-id="10a52-118">You must run it from your Front End Server or Standard Edition servers.</span></span>



</div>

<span data-ttu-id="10a52-119">定义边缘服务器拓扑的过程在拓扑生成器中完成。</span><span class="sxs-lookup"><span data-stu-id="10a52-119">The process to define your Edge Server topology is done in Topology Builder.</span></span> <span data-ttu-id="10a52-120">下面列出了你计划和配置的三种主要类型的边缘服务器拓扑：</span><span class="sxs-lookup"><span data-stu-id="10a52-120">The three primary types of Edge Server topologies that you plan and configure are listed below:</span></span>

  - <span data-ttu-id="10a52-121">定义单个边缘服务器的拓扑</span><span class="sxs-lookup"><span data-stu-id="10a52-121">To define the Topology for a Single Edge Server</span></span>

  - <span data-ttu-id="10a52-122">定义负载平衡的边缘服务器池的拓扑</span><span class="sxs-lookup"><span data-stu-id="10a52-122">To define the Topology for a Load Balanced Edge Server Pool</span></span>

  - <span data-ttu-id="10a52-123">定义硬件负载平衡的边缘池的拓扑</span><span class="sxs-lookup"><span data-stu-id="10a52-123">To define the Topology for a Hardware Load Balanced Edge Pool</span></span>

<div>

## <a name="to-define-the-topology-for-a-single-edge-server"></a><span data-ttu-id="10a52-124">定义单个边缘服务器的拓扑</span><span class="sxs-lookup"><span data-stu-id="10a52-124">To define the topology for a single Edge Server</span></span>

1.  <span data-ttu-id="10a52-125">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-125">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="10a52-126">在控制台树中，展开要在其中部署边缘服务器的网站。</span><span class="sxs-lookup"><span data-stu-id="10a52-126">In the console tree, expand the site in which you want to deploy an Edge Server.</span></span>

3.  <span data-ttu-id="10a52-127">右键单击 " **边缘池**"，然后单击 " **新建边缘池**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-127">Right-click **Edge pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="10a52-128">在 " **定义新的边缘池**" 中，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-128">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="10a52-129">在 " **定义边缘池 FQDN**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-129">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-130">在 " **池 FQDN**" 中，键入边缘服务器内部接口 (FQDN) 的完全限定的域名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-130">In **Pool FQDN**, type the fully qualified domain name (FQDN) of the internal interface for the Edge Server.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="10a52-131">您指定的名称必须与服务器上配置的计算机名相同。</span><span class="sxs-lookup"><span data-stu-id="10a52-131">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="10a52-132">默认情况下，未加入域的计算机的计算机名是一个短名称，而不是 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-132">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="10a52-133">拓扑生成器使用 FQDN，而不是短名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-133">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="10a52-134">因此，您必须在要部署为域外边缘服务器的计算机的名称上配置 DNS 后缀。</span><span class="sxs-lookup"><span data-stu-id="10a52-134">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="10a52-135">分配您的 Lync Server、边缘服务器和池的 FQDN 时，只使用标准字符（包括 A–Z、a–z、0–9 和连字符）。</span><span class="sxs-lookup"><span data-stu-id="10a52-135">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="10a52-136">不要使用 Unicode 字符或下划线。</span><span class="sxs-lookup"><span data-stu-id="10a52-136">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="10a52-137">当必须将 FQDN 分配给证书) 中的 SN 时，外部 DNS 和公共 Ca 通常不支持 FQDN 中的非标准字符 (。</span><span class="sxs-lookup"><span data-stu-id="10a52-137">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="10a52-138">有关向计算机名添加 DNS 后缀的详细信息，请参阅 <A href="lync-server-2013-configure-dns-for-edge-support.md">在 Lync Server 2013 中为 edge 支持配置 DNS</A>。</span><span class="sxs-lookup"><span data-stu-id="10a52-138">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-139">单击 " **单计算机池**"，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-139">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="10a52-140">在 " **选择功能**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-140">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-141">如果你计划为 SIP Access 服务使用单个 FQDN 和 IP 地址，Lync Server 2013 Web 会议服务和 A/V 边缘服务，请选中 " **使用单个 FQDN 和 Ip 地址** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="10a52-141">If you plan to use a single FQDN and IP address for the SIP Access service, Lync Server 2013 Web Conferencing service, and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="10a52-142">如果你计划启用联盟，请选中 " **为此边缘池启用联盟" (端口 5061)** 复选框。</span><span class="sxs-lookup"><span data-stu-id="10a52-142">If you plan to enable federation select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-143">你可以选择此选项，但你的组织中只能为联盟发布一个 Edge 池或边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-143">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="10a52-144">联盟用户（包括公共即时消息 (IM) 用户的所有访问权限，请访问同一 Edge 池或单层服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-144">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="10a52-145">例如，如果你的部署包括在纽约部署的 Edge 池或单层服务器，并且在伦敦部署了一个，并且你在纽约的 Edge 池或单层服务器上启用了联合身份验证支持，则联盟用户的信号流量将通过纽约的 Edge 池或单边服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-145">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="10a52-146">这同样适用于 London 用户的通信，尽管 London 内部用户呼叫 London 联盟用户时将使用 London 池或边缘服务器路由 A/V 流量。</span><span class="sxs-lookup"><span data-stu-id="10a52-146">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-147">如果你计划支持针对你的部署的可扩展消息和状态协议 (XMPP) ，请选中 " **启用 XMPP 联合身份验证 (端口 5269")** 复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-147">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="10a52-148">在 " **选择 IP 选项**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-148">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-149">**在内部接口上启用 ipv4**：如果要将 ipv4 地址应用到边缘服务器或边缘池内部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-149">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="10a52-150">**在内部接口上启用 ipv6**：如果要将 ipv6 地址应用到边缘服务器或边缘池内部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-150">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="10a52-151">**在外部接口上启用 ipv4**：如果要将 ipv4 地址应用到边缘服务器或边缘池外部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-151">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="10a52-152">**在外部接口上启用 ipv6**：如果要将 ipv6 地址应用到边缘服务器或边缘池外部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-152">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="10a52-153">你还可以将 Edge 服务器或边缘池配置为使用外部 IP 地址的网络地址转换地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-153">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="10a52-154">要执行此操作，请选中该复选框 **此边缘池的外部 IP 地址由 NAT 转换**。</span><span class="sxs-lookup"><span data-stu-id="10a52-154">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

8.  <span data-ttu-id="10a52-155">在 **外部 fqdn** 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-155">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-156">如果在 " **选择" 功能中选择** 使用单个 FQDN 和 IP 地址进行 sip 访问、Web 会议服务和 a/V 边缘服务，请在 " **sip 访问**" 中键入外部 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-156">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-157">如果选择此选项，则必须为每个 edge 服务指定不同的端口号 (推荐的端口设置：5061用于访问边缘服务，444用于 Web 会议 Edge 服务，443用于 A/V 边缘服务) 。</span><span class="sxs-lookup"><span data-stu-id="10a52-157">If you choose this option, you must specify a different port number for each of the edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="10a52-158">选择此选项可帮助防止潜在的连接问题，并简化配置，因为你可以使用相同的端口号 (例如，443) 所有三个服务。</span><span class="sxs-lookup"><span data-stu-id="10a52-158">Selecting this option can help prevent potential connectivity issues, and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-159">如果在 **"选择" 功能** 中未选择使用单个 FQDN 和 IP 地址，请键入 **SIP 访问**、 **Web 会议** 和 **音频视频** 的外部 fqdn，并保留默认端口。</span><span class="sxs-lookup"><span data-stu-id="10a52-159">If in **Select features** you did not chose to use a single FQDN and IP Address, type the External FQDNs for **SIP Access**, **Web Conferencing** and **Audio Video**, keeping the default ports.</span></span>

9.  <span data-ttu-id="10a52-160">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-160">Click **Next**.</span></span>

10. <span data-ttu-id="10a52-161">在 " **定义内部 IP 地址**" 中，在 " **内部 IPv4 地址** " 和 " **内部 IPv6 地址** " 中键入边缘服务器的 IP 地址，这适合你的要求。</span><span class="sxs-lookup"><span data-stu-id="10a52-161">In **Define the Internal IP address**, type the IP address of your Edge Server in **Internal IPv4 address** and **Internal IPv6 address** as is appropriate for your requirements.</span></span> <span data-ttu-id="10a52-162">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-162">Click **Next**.</span></span>

11. <span data-ttu-id="10a52-163">在 " **定义外部 IP 地址**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-163">In **Define the External IP address**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-164">如果你选择对 SIP 访问、Web 会议服务和 A/V 边缘服务使用单个 FQDN 和 IP 地址，请在 **SIP access** 中键入 Edge 服务器的外部 IPv4 地址，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-164">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="10a52-165">如果您选择使用 IPv6 地址，请在 " **SIP 访问**" 中键入边缘服务器的外部 IPv6 地址，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-165">If you chose to use IPv6 addresses, type the external IPv6 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="10a52-166">如果未选择使用单个 FQDN 和 IP 地址进行 SIP 访问、Web 会议服务和 A/V 边缘服务，请在 **SIP 访问**、 **Web 会议** 和 **a/v 会议** 中键入边缘服务器的外部 IPv4 地址，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-166">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="10a52-167">如果你选择使用 IPv6 地址，但未选择对 SIP 访问、Web 会议服务和 A/V 边缘服务使用单个 FQDN 和 IP 地址，请在 " **Sip 访问**"、" **web 会议**" 和 " **a/v" 会议** 中键入边缘服务器的外部 IPv6 地址，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-167">If you chose to use IPv6 addresses and did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-168">如果你没有选择启用和分配 IPv6 寻址，则不会看到此对话框。</span><span class="sxs-lookup"><span data-stu-id="10a52-168">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

        
        </div>

12. <span data-ttu-id="10a52-169">如果您选择使用 NAT，则会显示一个对话框。</span><span class="sxs-lookup"><span data-stu-id="10a52-169">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="10a52-170">在 **A/V 边缘服务的公共 ipv4 地址** 中，键入要由 NAT 转换的公共 ipv4 地址，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-170">In **Public IPv4 address for the A/V Edge service**, type the public IPv4 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-171">这应该是 A/V 边缘服务的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-171">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

13. <span data-ttu-id="10a52-172">如果您选择使用 NAT 和 IPv6 地址，则会出现一个对话框。</span><span class="sxs-lookup"><span data-stu-id="10a52-172">If you chose to use NAT and IPv6 addresses, a dialog box appears.</span></span> <span data-ttu-id="10a52-173">在 **A/V 边缘服务的公共 ipv6 地址** 中，键入要由 NAT 转换的公共 ipv6 地址，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-173">In **Public IPv6 address for the A/V Edge service**, type the public IPv6 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-174">这应该是 A/V 边缘服务的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-174">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

14. <span data-ttu-id="10a52-175">在 " **定义下一跃点**" 的 " **下一跃点" 池中**，选择内部池的名称，该名称可以是前端池，也可以是标准版池。</span><span class="sxs-lookup"><span data-stu-id="10a52-175">In **Define the next hop**, in **Next hop pool**, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="10a52-176">或者，如果你的部署包含 Director，请选择 Director。</span><span class="sxs-lookup"><span data-stu-id="10a52-176">Or, if your deployment includes a Director, select the Director.</span></span> <span data-ttu-id="10a52-177">然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-177">Then, click **Next**.</span></span>

15. <span data-ttu-id="10a52-178">在 **关联前端池** 中，通过选择要使用此 edge 服务器与受支持的外部用户通信的内部池的名称，指定一个或多个内部池（这些内部池可以包括前端池和标准版服务器）与此边缘服务器关联。</span><span class="sxs-lookup"><span data-stu-id="10a52-178">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pools that are to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-179">对于 A/V 流量，只能将一个负载平衡的边缘池或单个边缘服务器与每个内部池相关联。</span><span class="sxs-lookup"><span data-stu-id="10a52-179">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="10a52-180">如果你已有与边缘池或边缘服务器关联的内部池，则会显示一条警告，指示内部池已关联到边缘池或边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-180">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="10a52-181">如果你选择的池已与另一 Edge 服务器关联，则它将更改关联。</span><span class="sxs-lookup"><span data-stu-id="10a52-181">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

16. <span data-ttu-id="10a52-182">单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="10a52-182">Click **Finish**.</span></span>

17. <span data-ttu-id="10a52-183">发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="10a52-183">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-dns-load-balanced-edge-server-pool"></a><span data-ttu-id="10a52-184">定义 DNS 负载平衡的边缘服务器池的拓扑</span><span class="sxs-lookup"><span data-stu-id="10a52-184">To define the topology for a DNS load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="10a52-185">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-185">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="10a52-186">在控制台树中，展开要在其中部署边缘服务器的网站。</span><span class="sxs-lookup"><span data-stu-id="10a52-186">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="10a52-187">右键单击 " **边缘池**"，然后单击 " **新建边缘池**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-187">Right-click **Edge Pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="10a52-188">在 " **定义新的边缘池**" 中，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-188">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="10a52-189">在 " **定义边缘池 FQDN**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-189">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-190">在 " **池 FQDN**" 中，键入 (FQDN) 的完全限定的域名，以获取边缘池的内部连接。</span><span class="sxs-lookup"><span data-stu-id="10a52-190">In **Pool FQDN**, type the fully qualified domain name (FQDN) for the internal connection of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="10a52-191">为池指定的名称必须是内部边缘池名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-191">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="10a52-192">必须将其定义为 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-192">This must be defined as a FQDN.</span></span> <span data-ttu-id="10a52-193">拓扑生成器使用 FQDN，而不是短名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-193">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="10a52-194">分配您的 Lync Server、边缘服务器和池的 FQDN 时，只使用标准字符（包括 A–Z、a–z、0–9 和连字符）。</span><span class="sxs-lookup"><span data-stu-id="10a52-194">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="10a52-195">不要使用 Unicode 字符或下划线。</span><span class="sxs-lookup"><span data-stu-id="10a52-195">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="10a52-196">当必须将 FQDN 分配给证书) 中的 SN 时，外部 DNS 和公共 Ca 通常不支持 FQDN 中的非标准字符 (。</span><span class="sxs-lookup"><span data-stu-id="10a52-196">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-197">单击 " **多台计算机池**"，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-197">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="10a52-198">在 " **选择功能**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-198">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-199">如果你计划将单个 FQDN 和 IP 地址用于 SIP 访问，请使用 Lync Server 2013 Web 会议服务和 A/V 边缘服务，选中 " **使用单个 FQDN 和 Ip 地址** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="10a52-199">If you plan to use a single FQDN and IP address for the SIP access, Lync Server 2013 Web Conferencing service and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="10a52-200">如果你计划启用联盟，请选中 " **为此边缘池启用联盟" (端口 5061)** 复选框。</span><span class="sxs-lookup"><span data-stu-id="10a52-200">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span> <span data-ttu-id="10a52-201">单击 "**下一步**"</span><span class="sxs-lookup"><span data-stu-id="10a52-201">Click **Next**</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-202">你可以选择此选项，但你的组织中只能为联盟发布一个 Edge 池或边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-202">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="10a52-203">联盟用户（包括公共即时消息 (IM) 用户的所有访问权限，请访问同一 Edge 池或单层服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-203">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="10a52-204">例如，如果部署中有一个边缘池或单个边缘服务器部署在纽约，另一个部署在伦敦，并对纽约的边缘池或单个边缘服务器启用联盟支持，则联盟用户的信号流量将通过纽约的边缘池或单个边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-204">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="10a52-205">这同样适用于 London 用户的通信，尽管 London 内部用户呼叫 London 联盟用户时将使用 London 池或边缘服务器路由 A/V 流量。</span><span class="sxs-lookup"><span data-stu-id="10a52-205">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-206">如果你计划支持针对你的部署的可扩展消息和状态协议 (XMPP) ，请选中 " **启用 XMPP 联合身份验证 (端口 5269")** 复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-206">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="10a52-207">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-207">Click **Next**.</span></span>

8.  <span data-ttu-id="10a52-208">在 " **选择 IP 选项**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-208">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-209">**在内部接口上启用 ipv4**：如果要将 ipv4 地址应用到边缘服务器或边缘池内部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-209">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="10a52-210">**在内部接口上启用 ipv6**：如果要将 ipv6 地址应用到边缘服务器或边缘池内部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-210">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="10a52-211">**在外部接口上启用 ipv4**：如果要将 ipv4 地址应用到边缘服务器或边缘池外部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-211">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="10a52-212">**在外部接口上启用 ipv6**：如果要将 ipv6 地址应用到边缘服务器或边缘池外部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-212">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="10a52-213">你还可以将 Edge 服务器或边缘池配置为使用外部 IP 地址的网络地址转换地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-213">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="10a52-214">要执行此操作，请选中该复选框 **此边缘池的外部 IP 地址由 NAT 转换**。</span><span class="sxs-lookup"><span data-stu-id="10a52-214">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

9.  <span data-ttu-id="10a52-215">在 **外部 fqdn** 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-215">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-216">如果在 " **选择" 功能中选择** 使用单个 FQDN 和 IP 地址进行 sip 访问、Web 会议服务和 a/V 边缘服务，请在 " **sip 访问**" 中键入外部 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-216">If in **Select features** you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-217">如果选择此选项，则必须为每个 Edge 服务指定不同的端口号 (推荐的端口设置：5061用于访问边缘服务，444用于 Web 会议 Edge 服务，443用于 A/V 边缘服务) 。</span><span class="sxs-lookup"><span data-stu-id="10a52-217">If you choose this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="10a52-218">通过选择此选项，你可以帮助防止潜在的连接问题，并简化配置，因为你可以使用相同的端口号 (例如，443) 所有三个服务。</span><span class="sxs-lookup"><span data-stu-id="10a52-218">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-219">如果在 " **选择" 功能** 中未选择使用单个 FQDN 和 IP 地址，请在 " **SIP 访问**" 中键入您为 edge 池的公共对开面选择的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-219">If in **Select features** you did not chose to use a single FQDN and IP Address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="10a52-220">在 " **Web 会议**" 中，键入为边缘池的公共面向面选择的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-220">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="10a52-221">在 " **音频/视频**" 中，键入为边缘池的公共面向面选择的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-221">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="10a52-222">使用默认端口。</span><span class="sxs-lookup"><span data-stu-id="10a52-222">Use the default ports.</span></span>

10. <span data-ttu-id="10a52-223">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-223">Click **Next**.</span></span>

11. <span data-ttu-id="10a52-224">在 " **定义此池中的计算机**" 中，单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-224">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="10a52-225">在 " **内部 FQDN 和 IP 地址**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-225">In **Internal FQDN and IP address**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-226">在 " **内部 IPv4 地址**" 中，键入 IPv4 地址和 **内部 IPv6 地址** ，以适合你希望在此池中创建的第一个边缘服务器的要求。</span><span class="sxs-lookup"><span data-stu-id="10a52-226">In **Internal IPv4 address**, type the IPv4 address and **Internal IPv6 address** as is appropriate for your requirements for the first Edge Server that you want to create in this pool.</span></span>
    
      - <span data-ttu-id="10a52-227">在 " **内部 FQDN**" 中，键入要在此池中创建的第一个边缘服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-227">In **Internal FQDN**, type the FQDN of the first Edge Server that you want to create in this pool.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-228">指定的名称必须与在服务器上配置的计算机名称相同。</span><span class="sxs-lookup"><span data-stu-id="10a52-228">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="10a52-229">默认情况下，未加入域的计算机的计算机名称为短名称，而不是 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-229">By default, the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="10a52-230">拓扑生成器使用 FQDN，而不是短名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-230">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="10a52-231">因此，您必须在要部署为域外边缘服务器的计算机的名称上配置 DNS 后缀。</span><span class="sxs-lookup"><span data-stu-id="10a52-231">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="10a52-232">在分配 Lync 服务器、Edge 服务器、池和数组的 Fqdn 时，只能使用标准字符 (包括 A-Z、a – z、0–9和连字符) 。</span><span class="sxs-lookup"><span data-stu-id="10a52-232">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, pools, and arrays.</span></span> <span data-ttu-id="10a52-233">不要使用 Unicode 字符或下划线。</span><span class="sxs-lookup"><span data-stu-id="10a52-233">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="10a52-234">当必须将 FQDN 分配给证书) 中的 SN 时，外部 DNS 和公共 Ca 通常不支持 FQDN 中的非标准字符 (。</span><span class="sxs-lookup"><span data-stu-id="10a52-234">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="10a52-235">有关向计算机名添加 DNS 后缀的详细信息，请参阅 <A href="lync-server-2013-configure-dns-for-edge-support.md">在 Lync Server 2013 中为 edge 支持配置 DNS</A>。</span><span class="sxs-lookup"><span data-stu-id="10a52-235">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>

13. <span data-ttu-id="10a52-236">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-236">Click **Next**.</span></span>

14. <span data-ttu-id="10a52-237">在 " **定义外部 IP 地址**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-237">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-238">如果你选择对 SIP 访问、Web 会议服务和 A/V 边缘服务使用单个 FQDN 和 IP 地址，请在 **SIP access** 中键入边缘服务器的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-238">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="10a52-239">如果你未选择使用单个 FQDN 和 IP 地址进行 SIP 访问、Web 会议服务和 A/V 会议服务，请键入为此 Edge 池服务器的公共对开面选择的 IP 地址以进行 **Sip 访问**。</span><span class="sxs-lookup"><span data-stu-id="10a52-239">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="10a52-240">在 " **Web 会议**" 中，键入您为此 Edge 池服务器的公共对开面选择的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-240">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="10a52-241">在 **A/V 会议** 中，键入为此 Edge 池服务器的公共对开面选择的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-241">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

15. <span data-ttu-id="10a52-242">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-242">Click **Next**.</span></span>

16. <span data-ttu-id="10a52-243">如果您选择启用 IPv6 地址，请在 " **定义外部 IP 地址**" 中执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-243">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-244">如果你选择对 SIP 访问、Web 会议服务和 A/V 边缘服务使用单个 FQDN 和 IP 地址，请在 **SIP access** 中键入边缘服务器的外部 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-244">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="10a52-245">如果您没有选择使用单个 FQDN 和 IP 地址进行 SIP 访问、Web 会议服务和 A/V 会议服务，请键入为该 Edge 池服务器的公共对开面选择的 IPv6 地址以进行 **Sip 访问**。</span><span class="sxs-lookup"><span data-stu-id="10a52-245">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="10a52-246">在 **Web 会议** 中，键入你为此 Edge 池服务器的公共对开面选择的 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-246">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="10a52-247">在 **A/V 会议** 中，键入你为此 Edge 池服务器的公共对开面选择的 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-247">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-248">如果你没有选择启用和分配 IPv6 寻址，则不会看到此对话框。</span><span class="sxs-lookup"><span data-stu-id="10a52-248">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

17. <span data-ttu-id="10a52-249">单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="10a52-249">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-250">现在，你将在 " <STRONG>定义此池中的计算机</STRONG> " 对话框中的池中看到你创建的第一个 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-250">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

18. <span data-ttu-id="10a52-251">在 " **定义此池中的计算机**" 中，单击 " **添加**"，然后为要添加到 Edge 池的第二边缘服务器重复步骤11到步骤14。</span><span class="sxs-lookup"><span data-stu-id="10a52-251">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to you Edge pool.</span></span>

19. <span data-ttu-id="10a52-252">重复步骤11至14后，在 "**定义此池中的计算机"** 中单击 "**下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-252">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-253">此时，你可以看到池中的两个边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-253">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

20. <span data-ttu-id="10a52-254">如果您选择使用 NAT，则会显示一个对话框。</span><span class="sxs-lookup"><span data-stu-id="10a52-254">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="10a52-255">在 " **公共 IP 地址**" 中，根据需要通过 NAT 翻译) 地址键入公共 IPv4 和 IPv6 (，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-255">In **Public IP address**, type the public IPv4 and IPv6 (as appropriate) addresses to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-256">这应该是 A/V 边缘的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-256">This should be the external IP Address of the A/V Edge.</span></span>

    
    </div>

21. <span data-ttu-id="10a52-257">在 " **定义下一跃点**" 下的 " **下一跃点池** " 列表中，选择内部池的名称，该名称可以是前端池，也可以是标准版池。</span><span class="sxs-lookup"><span data-stu-id="10a52-257">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="10a52-258">或者，如果你的部署包含 Director，请选择 Director 的名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-258">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="10a52-259">然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-259">Then, click **Next**.</span></span>

22. <span data-ttu-id="10a52-260">在 " **关联前端池**" 中，指定一个或多个内部池（其中包括要与此边缘服务器关联的前端池和标准版服务器），方法是选择要使用此 edge 服务器与受支持的外部用户通信的内部池 (s 的名称) 。</span><span class="sxs-lookup"><span data-stu-id="10a52-260">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-261">对于 A/V 流量，只能将一个负载平衡的边缘池或单个边缘服务器与每个内部池相关联。</span><span class="sxs-lookup"><span data-stu-id="10a52-261">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="10a52-262">如果你已有与边缘池或边缘服务器关联的内部池，则会显示一条警告，指示内部池已关联到边缘池或边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-262">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="10a52-263">如果你选择的池已与另一 Edge 服务器关联，则它将更改关联。</span><span class="sxs-lookup"><span data-stu-id="10a52-263">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

23. <span data-ttu-id="10a52-264">单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="10a52-264">Click **Finish**.</span></span>

24. <span data-ttu-id="10a52-265">发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="10a52-265">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-hardware-load-balanced-edge-server-pool"></a><span data-ttu-id="10a52-266">定义硬件负载平衡的边缘服务器池的拓扑</span><span class="sxs-lookup"><span data-stu-id="10a52-266">To define the topology for a hardware load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="10a52-267">启动拓扑生成器：单击 " **开始**"，单击 " **所有程序**"，单击 " **Microsoft Lync server 2013**"，然后单击 " **Lync server 拓扑生成器**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-267">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="10a52-268">在控制台树中，展开要在其中部署边缘服务器的网站。</span><span class="sxs-lookup"><span data-stu-id="10a52-268">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="10a52-269">右键单击 " **边缘池**"，然后选择 " **新建边缘池**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-269">Right-click **Edge Pools**, and then select **New Edge Pool**.</span></span>

4.  <span data-ttu-id="10a52-270">在 " **定义新的边缘池**" 中，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-270">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="10a52-271">在 " **定义边缘池 FQDN**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-271">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-272">在 " **fqdn**" 中，键入你为 Edge 池的内部方选择的完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="10a52-272">In **FQDN**, type the fully qualified domain name (FQDN) you have chosen for the internal side of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="10a52-273">为池指定的名称必须是内部边缘池名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-273">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="10a52-274">必须将其定义为 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-274">This must be defined as a FQDN.</span></span> <span data-ttu-id="10a52-275">拓扑生成器使用 FQDN，而不是短名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-275">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="10a52-276">分配您的 Lync Server、边缘服务器和池的 FQDN 时，只使用标准字符（包括 A–Z、a–z、0–9 和连字符）。</span><span class="sxs-lookup"><span data-stu-id="10a52-276">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="10a52-277">不要使用 Unicode 字符或下划线。</span><span class="sxs-lookup"><span data-stu-id="10a52-277">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="10a52-278">当必须将 FQDN 分配给证书) 中的 SN 时，外部 DNS 和公共 Ca 通常不支持 FQDN 中的非标准字符 (。</span><span class="sxs-lookup"><span data-stu-id="10a52-278">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
    <!-- end list -->
    
      - <span data-ttu-id="10a52-279">单击 " **多台计算机池**"，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-279">Click **Multiple computer pool**, and then **Next**.</span></span>

6.  <span data-ttu-id="10a52-280">在 " **选择功能** " 中，执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-280">In **Select features** do the following:</span></span>
    
      - <span data-ttu-id="10a52-281">如果你计划为 SIP access 服务、Lync Server Web 会议服务和 A/V 边缘服务使用单个 FQDN 和 IP 地址，请选中 " **使用单个 FQDN & IP 地址** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="10a52-281">If you plan to use a single FQDN and IP address for the SIP access service, Lync Server Web Conferencing service, and A/V Edge service, select the **Use a single FQDN & IP Address** check box.</span></span>
    
      - <span data-ttu-id="10a52-282">如果你计划启用联盟，请选中 " **为此边缘池启用联盟" (端口 5061)** 复选框。</span><span class="sxs-lookup"><span data-stu-id="10a52-282">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-283">你可以选择此选项，但你的组织中只能有一个 Edge 池或边缘服务器可在外部针对联盟进行发布。</span><span class="sxs-lookup"><span data-stu-id="10a52-283">You can select this option, but only one Edge pool or Edge Server in your organization may be published externally for federation.</span></span> <span data-ttu-id="10a52-284">联盟用户（包括公共即时消息 (IM) 用户的所有访问权限，请访问同一 Edge 池或单层服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-284">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="10a52-285">例如，如果部署中有一个边缘池或单个边缘服务器部署在纽约，另一个部署在伦敦，并对纽约的边缘池或单个边缘服务器启用联盟支持，则联盟用户的信号流量将通过纽约的边缘池或单个边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-285">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="10a52-286">这同样适用于 London 用户的通信，尽管 London 内部用户呼叫 London 联盟用户时将使用 London 池或边缘服务器路由 A/V 流量。</span><span class="sxs-lookup"><span data-stu-id="10a52-286">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-287">如果你计划支持针对你的部署的可扩展消息和状态协议 (XMPP) ，请选中 " **启用 XMPP 联合身份验证 (端口 5269")** 复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-287">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="10a52-288">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-288">Click **Next**.</span></span>

8.  <span data-ttu-id="10a52-289">在 " **选择 IP 选项**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-289">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-290">**在内部接口上启用 ipv4**：如果要将 ipv4 地址应用到边缘服务器或边缘池内部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-290">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="10a52-291">**在内部接口上启用 ipv6**：如果要将 ipv6 地址应用到边缘服务器或边缘池内部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-291">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="10a52-292">**在外部接口上启用 ipv4**：如果要将 ipv4 地址应用到边缘服务器或边缘池外部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-292">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="10a52-293">**在外部接口上启用 ipv6**：如果要将 ipv6 地址应用到边缘服务器或边缘池外部接口，请选中该复选框</span><span class="sxs-lookup"><span data-stu-id="10a52-293">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="10a52-294"><STRONG>不要</STRONG> 选择 " <STRONG>通过 NAT 转换边缘池的外部 IP 地址</STRONG> " 复选框。</span><span class="sxs-lookup"><span data-stu-id="10a52-294"><STRONG>Do Not</STRONG> select the <STRONG>The external IP address of the Edge pool is translated by NAT</STRONG> check box.</span></span> <span data-ttu-id="10a52-295">使用硬件负载平衡时，不支持 (NAT) 的网络地址转换。</span><span class="sxs-lookup"><span data-stu-id="10a52-295">Network address translation (NAT) is not supported when you are using hardware load balancing.</span></span>

    
    </div>

9.  <span data-ttu-id="10a52-296">在 **外部 fqdn** 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-296">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-297">如果在 " **选择" 功能中选择** 使用单个 FQDN 和 IP 地址进行 sip 访问、Web 会议服务和 a/V 边缘服务，请在 " **sip 访问**" 中键入外部 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-297">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-298">如果你选择此选项，则必须为每个 Edge 服务指定不同的端口号 (推荐的端口设置：5061用于访问边缘服务，444用于 Web 会议 Edge 服务，443适用于 A/V 边缘服务) 。</span><span class="sxs-lookup"><span data-stu-id="10a52-298">If you choose to select this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="10a52-299">通过选择此选项，你可以帮助防止潜在的连接问题，并简化配置，因为你可以使用相同的端口号 (例如，443) 所有三个服务。</span><span class="sxs-lookup"><span data-stu-id="10a52-299">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="10a52-300">如果在 " **选择" 功能** 中未选择使用单个 FQDN 和 IP 地址，请在 " **SIP 访问**" 中键入您为 edge 池的公共对开面选择的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-300">If in **Select features** you did not chose to use a single FQDN and IP address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="10a52-301">在 " **Web 会议**" 中，键入为边缘池的公共面向面选择的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-301">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="10a52-302">在 " **音频/视频**" 中，键入为边缘池的公共面向面选择的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="10a52-302">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="10a52-303">使用默认端口。</span><span class="sxs-lookup"><span data-stu-id="10a52-303">Use the default ports.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="10a52-304">这些将是池 (VIP) Fqdn 的面向公众的虚拟 IP。</span><span class="sxs-lookup"><span data-stu-id="10a52-304">These will be the publicly facing virtual IP (VIP) FQDNs for the pool.</span></span>

        
        </div>

10. <span data-ttu-id="10a52-305">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-305">Click **Next**.</span></span>

11. <span data-ttu-id="10a52-306">在 " **定义此池中的计算机**" 中，单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-306">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="10a52-307">在 " **定义外部 IP 地址**" 中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-307">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-308">如果你选择对 SIP 访问、Web 会议服务和 A/V 边缘服务使用单个 FQDN 和 IP 地址，请在 **Sip 访问** 中键入 edge 服务器的外部 IPv4 地址。 **sip 访问** 中的边缘服务器的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-308">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**.external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="10a52-309">如果你未选择使用单个 FQDN 和 IP 地址进行 SIP 访问、Web 会议服务和 A/V 会议服务，请键入为此 Edge 池服务器的公共对开面选择的 IP 地址以进行 **Sip 访问**。</span><span class="sxs-lookup"><span data-stu-id="10a52-309">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="10a52-310">在 " **Web 会议**" 中，键入您为此 Edge 池服务器的公共对开面选择的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-310">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="10a52-311">在 **A/V 会议** 中，键入为此 Edge 池服务器的公共对开面选择的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-311">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

13. <span data-ttu-id="10a52-312">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-312">Click **Next**.</span></span>

14. <span data-ttu-id="10a52-313">如果您选择启用 IPv6 地址，请在 " **定义外部 IP 地址**" 中执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="10a52-313">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="10a52-314">如果你选择对 SIP 访问、Web 会议服务和 A/V 边缘服务使用单个 FQDN 和 IP 地址，请在 **SIP access** 中键入边缘服务器的外部 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-314">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="10a52-315">如果您没有选择使用单个 FQDN 和 IP 地址进行 SIP 访问、Web 会议服务和 A/V 会议服务，请键入为该 Edge 池服务器的公共对开面选择的 IPv6 地址以进行 **Sip 访问**。</span><span class="sxs-lookup"><span data-stu-id="10a52-315">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="10a52-316">在 **Web 会议** 中，键入你为此 Edge 池服务器的公共对开面选择的 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-316">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="10a52-317">在 **A/V 会议** 中，键入你为此 Edge 池服务器的公共对开面选择的 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="10a52-317">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-318">如果你没有选择启用和分配 IPv6 寻址，则不会看到此对话框。</span><span class="sxs-lookup"><span data-stu-id="10a52-318">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

15. <span data-ttu-id="10a52-319">单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="10a52-319">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-320">现在，你将在 " <STRONG>定义此池中的计算机</STRONG> " 对话框中的池中看到你创建的第一个 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-320">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

16. <span data-ttu-id="10a52-321">在 " **定义此池中的计算机**" 中，单击 " **添加**"，然后为要添加到 Edge 池的第二边缘服务器重复步骤11到步骤14。</span><span class="sxs-lookup"><span data-stu-id="10a52-321">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to your Edge pool.</span></span>

17. <span data-ttu-id="10a52-322">重复步骤11至14后，在 "**定义此池中的计算机"** 中单击 "**下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-322">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-323">此时，你可以看到池中的两个边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-323">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

18. <span data-ttu-id="10a52-324">在 " **定义下一跃点**" 下的 " **下一跃点池** " 列表中，选择内部池的名称，该名称可以是前端池，也可以是标准版池。</span><span class="sxs-lookup"><span data-stu-id="10a52-324">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="10a52-325">或者，如果你的部署包含 Director，请选择 Director 的名称。</span><span class="sxs-lookup"><span data-stu-id="10a52-325">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="10a52-326">然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="10a52-326">Then, click **Next**.</span></span>

19. <span data-ttu-id="10a52-327">在 " **关联前端池**" 中，指定一个或多个内部池（其中包括要与此边缘服务器关联的前端池和标准版服务器），方法是选择要使用此 edge 服务器与受支持的外部用户通信的内部池 (s 的名称) 。</span><span class="sxs-lookup"><span data-stu-id="10a52-327">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="10a52-328">对于 A/V 流量，只能将一个负载平衡的边缘池或单个边缘服务器与每个内部池相关联。</span><span class="sxs-lookup"><span data-stu-id="10a52-328">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="10a52-329">如果你已有与边缘池或边缘服务器关联的内部池，则会显示一条警告，指示内部池已关联到边缘池或边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="10a52-329">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="10a52-330">如果你选择的池已与另一 Edge 服务器关联，则它将更改关联。</span><span class="sxs-lookup"><span data-stu-id="10a52-330">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

20. <span data-ttu-id="10a52-331">单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="10a52-331">Click **Finish**.</span></span>

21. <span data-ttu-id="10a52-332">发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="10a52-332">Publish your topology.</span></span>

<span data-ttu-id="10a52-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10a52-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

