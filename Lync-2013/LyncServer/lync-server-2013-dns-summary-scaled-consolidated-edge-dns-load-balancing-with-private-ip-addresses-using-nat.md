---
title: Lync Server 2013：DNS 摘要 - 扩展的合并边缘（使用 NAT 通过专用 IP 地址进行 DNS 负载平衡）
description: Lync Server 2013：使用 NAT 的 DNS 摘要-缩放后的合并边缘、使用专用 IP 地址的 DNS 负载平衡。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: 11bc7b84-91cf-48f9-ad0e-06ad30b46a2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398201(v=OCS.15)
ms:contentKeyID: 48183447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2eef3029323c1c2f798fddc721df832a932524c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437705"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="72099-103">Lync Server 2013 中的 DNS 摘要 - 扩展的合并边缘（使用 NAT 通过专用 IP 地址进行 DNS 负载平衡）</span><span class="sxs-lookup"><span data-stu-id="72099-103">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72099-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72099-104">

<span> </span></span></span>

<span data-ttu-id="72099-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="72099-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="72099-106">与证书和端口的远程2013访问的 DNS 记录要求相当直接。</span><span class="sxs-lookup"><span data-stu-id="72099-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="72099-107">此外，许多记录是可选的，具体取决于您配置运行 Lync 2013 的客户端的方式以及是否启用联盟。</span><span class="sxs-lookup"><span data-stu-id="72099-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="72099-108">有关 Lync 2013 DNS 要求的详细信息，请参阅 [确定 Lync Server 2013 的 DNS 要求](lync-server-2013-determine-dns-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="72099-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="72099-109">有关配置 Lync 2013 客户端的自动配置的详细信息，请参阅 [确定 Lync Server 2013 的 DNS 要求](lync-server-2013-determine-dns-requirements.md)时，请参阅 "没有拆分大脑 Dns 的自动配置" 部分。</span><span class="sxs-lookup"><span data-stu-id="72099-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="72099-110">下表列出了支持单个统一边缘拓扑图中所示的单个统一边缘拓扑所需的 DNS 记录的摘要。</span><span class="sxs-lookup"><span data-stu-id="72099-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="72099-111">请注意，仅当自动配置 Lync 2013 客户端时，才需要某些 DNS 记录。</span><span class="sxs-lookup"><span data-stu-id="72099-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="72099-112">如果你计划使用组策略对象 (Gpo) 配置 Lync 客户端，则不需要关联的记录。</span><span class="sxs-lookup"><span data-stu-id="72099-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="72099-113">重要提示： Edge 服务器网络适配器要求</span><span class="sxs-lookup"><span data-stu-id="72099-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="72099-114">为避免路由问题，请验证边缘服务器中是否至少有两个网络适配器，并且是否仅在与外部接口关联的网络适配器上设置默认网关。</span><span class="sxs-lookup"><span data-stu-id="72099-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="72099-115">例如，如缩放后的合并边缘方案图中所示，在 [Lync Server 2013 中使用 NAT 进行 DNS 负载平衡](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)，默认网关将指向外部防火墙。</span><span class="sxs-lookup"><span data-stu-id="72099-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md), the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="72099-116">可以在每个边缘服务器中配置两个网络适配器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="72099-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="72099-117">**网络适配器 1-节点 1 (内部接口)**</span><span class="sxs-lookup"><span data-stu-id="72099-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="72099-118">已分配172.25.33.10 的内部接口。</span><span class="sxs-lookup"><span data-stu-id="72099-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="72099-119">未定义默认网关。</span><span class="sxs-lookup"><span data-stu-id="72099-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="72099-120">请确保从网络中有一条路由，该网络包含指向运行 Lync Server 2013 或 Lync Server 2013 客户端的服务器的任何网络的边缘内部接口 (例如从172.25.33.0 到 192.168.10.0) 。</span><span class="sxs-lookup"><span data-stu-id="72099-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="72099-121">**网络适配器 1-节点 2 (内部接口)**</span><span class="sxs-lookup"><span data-stu-id="72099-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="72099-122">已分配172.25.33.11 的内部接口。</span><span class="sxs-lookup"><span data-stu-id="72099-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="72099-123">未定义默认网关。</span><span class="sxs-lookup"><span data-stu-id="72099-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="72099-124">请确保从网络中有一条路由，该网络包含指向运行 Lync Server 2013 或 Lync Server 2013 客户端的服务器的任何网络的边缘内部接口 (例如从172.25.33.0 到 192.168.10.0) 。</span><span class="sxs-lookup"><span data-stu-id="72099-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="72099-125">**网络适配器2节点 1 (外部接口)**</span><span class="sxs-lookup"><span data-stu-id="72099-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="72099-126">将三个专用 IP 地址分配给此网络适配器，例如10.45.16.10 用于访问边缘，10.45.16.20 用于 Web 会议边缘，10.45.16.30 AV 边缘。</span><span class="sxs-lookup"><span data-stu-id="72099-126">Three private IP addresses are assigned to this network adapter, for example 10.45.16.10 for Access Edge, 10.45.16.20 for Web Conferencing Edge, 10.45.16.30 for AV Edge.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="72099-127">虽然不推荐使用所有三个边缘服务接口的单个 IP 地址，但也有可能。</span><span class="sxs-lookup"><span data-stu-id="72099-127">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="72099-128">虽然这会保存 IP 地址，但它需要每个服务的不同端口号。</span><span class="sxs-lookup"><span data-stu-id="72099-128">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="72099-129">默认端口号为 443/TCP，这可确保大多数远程防火墙都允许流量。</span><span class="sxs-lookup"><span data-stu-id="72099-129">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="72099-130">将端口值更改为 (（) 例如，访问边缘的 5061/tcp）、Web 会议边缘的 444/tcp 和 AV 边缘的 443/TCP 对于远程用户来说，其背后的防火墙不允许通过 5061/TCP 和 444/TCP 的流量，这可能会导致出现问题。</span><span class="sxs-lookup"><span data-stu-id="72099-130">Changing the port values to (for example) 5061/TCP for the Access Edge, 444/TCP for the Web Conferencing Edge and 443/TCP for the AV Edge might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="72099-131">此外，由于能够筛选 IP 地址，三个不同的 IP 地址使疑难解答变得更轻松。</span><span class="sxs-lookup"><span data-stu-id="72099-131">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="72099-132">访问边缘公共 IP 地址是将默认网关设置为集成路由器 (10.45.16.1) 的主要地址。</span><span class="sxs-lookup"><span data-stu-id="72099-132">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="72099-133">Web 会议和 A/V 边缘专用 IP 地址是 Windows Server 中 **本地连接属性** 的 **internet 协议版本 4 (tcp/IPv4)** 和 **INTERNET 协议版本 6 (tcp/IPv6)** 的 "**高级**" 部分中的其他 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="72099-133">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

  - <span data-ttu-id="72099-134">**网络适配器2节点 2 (外部接口)**</span><span class="sxs-lookup"><span data-stu-id="72099-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="72099-135">将三个专用 IP 地址分配给此网络适配器，例如10.45.16.11 用于访问边缘，10.45.16.21 用于 Web 会议边缘，10.45.16.31 AV 边缘。</span><span class="sxs-lookup"><span data-stu-id="72099-135">Three private IP addresses are assigned to this network adapter, for example 10.45.16.11 for Access Edge, 10.45.16.21 for Web Conferencing Edge, 10.45.16.31 for AV Edge.</span></span>
    
    <span data-ttu-id="72099-136">访问边缘公共 IP 地址是将默认网关设置为集成路由器 (10.45.16.1) 的主要地址。</span><span class="sxs-lookup"><span data-stu-id="72099-136">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="72099-137">Web 会议和 A/V 边缘专用 IP 地址是 Windows Server 中 **本地连接属性** 的 **internet 协议版本 4 (tcp/IPv4)** 和 **INTERNET 协议版本 6 (tcp/IPv6)** 的 "**高级**" 部分中的其他 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="72099-137">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="72099-138">配置具有两个网络适配器的 Edge 服务器是两个选项之一。</span><span class="sxs-lookup"><span data-stu-id="72099-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="72099-139">另一种选择是将一个网络适配器用于内部端，将三个网络适配器用于边缘服务器的外部端。</span><span class="sxs-lookup"><span data-stu-id="72099-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="72099-140">此选项的主要优点是每个边缘服务器服务有一个不同的网络适配器，并且在需要故障排除时有可能更简洁的数据收集</span><span class="sxs-lookup"><span data-stu-id="72099-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-example"></a><span data-ttu-id="72099-141">缩放后的合并边缘、使用 NAT 使用专用 IP 地址的 DNS 负载平衡 (示例) 的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="72099-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72099-142">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="72099-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="72099-143">FQDN/DNS 记录</span><span class="sxs-lookup"><span data-stu-id="72099-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="72099-144">IP 地址/FQDN</span><span class="sxs-lookup"><span data-stu-id="72099-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="72099-145">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="72099-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72099-146">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="72099-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="72099-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-148">131.107.155.10 和 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="72099-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="72099-149">对于启用了 Lync 的用户， (Contoso) 的访问边缘外部接口对所有 SIP 域重复</span><span class="sxs-lookup"><span data-stu-id="72099-149">Access Edge external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72099-150">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="72099-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="72099-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-152">131.107.155.20 和 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="72099-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="72099-153">网络会议边缘外部界面</span><span class="sxs-lookup"><span data-stu-id="72099-153">Web Conferencing Edge external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72099-154">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="72099-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="72099-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-156">131.107.155.30 和 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="72099-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="72099-157">A/V 边缘外部接口</span><span class="sxs-lookup"><span data-stu-id="72099-157">A/V Edge external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72099-158">外部 DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="72099-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="72099-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-161">访问边缘外部接口。</span><span class="sxs-lookup"><span data-stu-id="72099-161">Access Edge external interface.</span></span> <span data-ttu-id="72099-162">需要将 Lync 2013 和 Lync 2010 客户端的自动配置用于外部工作。</span><span class="sxs-lookup"><span data-stu-id="72099-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="72099-163">根据需要对启用了 Lync 的用户的所有 SIP 域重复此操作。</span><span class="sxs-lookup"><span data-stu-id="72099-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72099-164">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="72099-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="72099-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-167">SIP 访问边缘外部接口。</span><span class="sxs-lookup"><span data-stu-id="72099-167">SIP Access Edge external interface.</span></span> <span data-ttu-id="72099-168">对于称为 "允许的 SIP 域" 的联盟合作伙伴，自动 DNS 发现所必需 () 以前版本中的 "增强联盟"。</span><span class="sxs-lookup"><span data-stu-id="72099-168">Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="72099-169">根据需要对启用了 Lync 的用户的所有 SIP 域重复此操作</span><span class="sxs-lookup"><span data-stu-id="72099-169">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72099-170">内部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="72099-170">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="72099-171">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="72099-171">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="72099-172">172.25.33.10 和 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="72099-172">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="72099-173">统一边缘内部接口</span><span class="sxs-lookup"><span data-stu-id="72099-173">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="72099-174">联盟所需的记录</span><span class="sxs-lookup"><span data-stu-id="72099-174">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72099-175">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="72099-175">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="72099-176">FQDN</span><span class="sxs-lookup"><span data-stu-id="72099-176">FQDN</span></span></th>
<th><span data-ttu-id="72099-177">IP 地址/FQDN 主机记录</span><span class="sxs-lookup"><span data-stu-id="72099-177">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="72099-178">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="72099-178">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72099-179">外部 DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="72099-179">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="72099-180">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-180">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-181">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-181">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-182">SIP 访问边缘外部接口，将联合身份验证自动 DNS 发现到其他潜在的联合合作伙伴，并称为 "允许的 SIP 域" (在以前版本的版本中称为 "增强联盟") 。根据需要对启用了 Lync 的用户的所有 SIP 域重复此操作</span><span class="sxs-lookup"><span data-stu-id="72099-182">SIP Access Edge external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="72099-183">移动和推送通知交换所需要此 SRV 记录</span><span class="sxs-lookup"><span data-stu-id="72099-183">This SRV record is required for mobility and the push notification clearing house</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="72099-184">DNS 摘要-公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="72099-184">DNS Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72099-185">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="72099-185">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="72099-186">FQDN/DNS 记录</span><span class="sxs-lookup"><span data-stu-id="72099-186">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="72099-187">IP 地址/FQDN</span><span class="sxs-lookup"><span data-stu-id="72099-187">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="72099-188">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="72099-188">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72099-189">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="72099-189">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="72099-190">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-190">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-191">Access Edge 服务界面</span><span class="sxs-lookup"><span data-stu-id="72099-191">Access Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="72099-192">对于启用了 Lync 的用户， (Contoso) 的访问边缘外部接口对所有 SIP 域重复</span><span class="sxs-lookup"><span data-stu-id="72099-192">Access Edge external interface (Contoso)Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="72099-193">可扩展消息和状态协议的 DNS 摘要</span><span class="sxs-lookup"><span data-stu-id="72099-193">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72099-194">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="72099-194">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="72099-195">FQDN</span><span class="sxs-lookup"><span data-stu-id="72099-195">FQDN</span></span></th>
<th><span data-ttu-id="72099-196">IP 地址/FQDN 主机记录</span><span class="sxs-lookup"><span data-stu-id="72099-196">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="72099-197">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="72099-197">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72099-198">外部 DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="72099-198">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="72099-199">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-199">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-200">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="72099-200">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="72099-201">"访问边缘服务" 或 "边缘池" 上的 XMPP 代理外部接口。对于启用了 Lync 的用户，通过全局策略、用户所在的网站策略或应用到启用了 Lync 的用户的用户策略，可以为所有内部 SIP 域重复此操作。</span><span class="sxs-lookup"><span data-stu-id="72099-201">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="72099-202">还必须在 XMPP 联盟合作伙伴策略中配置允许的 XMPP 域。</span><span class="sxs-lookup"><span data-stu-id="72099-202">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="72099-203">有关其他详细信息，请参阅 <strong>另请参阅</strong> 中的主题</span><span class="sxs-lookup"><span data-stu-id="72099-203">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72099-204">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="72099-204">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="72099-205">xmpp.contoso.com (例如) </span><span class="sxs-lookup"><span data-stu-id="72099-205">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="72099-206">边缘服务器上的访问边缘服务的 IP 地址或托管 XMPP 代理的边缘池的 IP 地址</span><span class="sxs-lookup"><span data-stu-id="72099-206">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="72099-207">指向托管 XMPP 代理服务的访问边缘服务或边缘池。</span><span class="sxs-lookup"><span data-stu-id="72099-207">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="72099-208">通常，你创建的 SRV 记录将指向此主机 (A 或 AAAA) 记录</span><span class="sxs-lookup"><span data-stu-id="72099-208">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="72099-209">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72099-209">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

