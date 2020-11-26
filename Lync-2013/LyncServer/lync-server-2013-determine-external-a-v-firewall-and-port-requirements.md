---
title: Lync Server 2013：确定外部 A/V 防火墙和端口要求
description: Lync Server 2013：确定外部 A/V 防火墙和端口要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine external A/V firewall and port requirements
ms:assetid: 3b849dc7-175d-40d1-820d-80e6ade6d332
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425882(v=OCS.15)
ms:contentKeyID: 48183872
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 38c2a8c1e8e332a4a1e65adb87a1e962e82941c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429512"
---
# <a name="determine-external-av-firewall-and-port-requirements-for-lync-server-2013"></a><span data-ttu-id="2a873-103">确定 Lync Server 2013 的外部 A/V 防火墙和端口要求</span><span class="sxs-lookup"><span data-stu-id="2a873-103">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a873-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a873-104">

<span> </span></span></span>

<span data-ttu-id="2a873-105">_**主题上次修改时间：** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="2a873-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="2a873-106">音频/视频 (A/V) 通信可能是一种复杂的。</span><span class="sxs-lookup"><span data-stu-id="2a873-106">Audio/Video (A/V) communication can be a complex.</span></span> <span data-ttu-id="2a873-107">由于在 A/V 中使用的协议的性质以及客户端和服务器使用这些协议的方式，因此有一个特殊的部分可以帮助解释客户端和服务器版本之间的差异。</span><span class="sxs-lookup"><span data-stu-id="2a873-107">Because of the nature of protocols used in A/V and how clients and servers use the protocols, a special section is warranted to explain the differences between client and server versions.</span></span>

<span data-ttu-id="2a873-108">使用以下 A/V 防火墙和端口表确定防火墙要求和要打开的端口。</span><span class="sxs-lookup"><span data-stu-id="2a873-108">Use the following A/V Firewall and Port table to determine firewall requirements and which ports to open.</span></span> <span data-ttu-id="2a873-109">然后，查看网络地址转换 (NAT) 术语，因为 NAT 可以采用多种不同的方式实现。</span><span class="sxs-lookup"><span data-stu-id="2a873-109">Then, review the network address translation (NAT) terminology because NAT can be implemented in many different ways.</span></span> <span data-ttu-id="2a873-110">有关防火墙端口设置的详细示例，请参阅 [Lync Server 2013 中用于外部用户访问的方案](lync-server-2013-scenarios-for-external-user-access.md)中的参考体系结构。</span><span class="sxs-lookup"><span data-stu-id="2a873-110">For a detailed example of firewall port settings, see the reference architectures in [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

### <a name="general-protocol-usage-for-udp-and-tcp-in-audiovideo-and-media-traffic"></a><span data-ttu-id="2a873-111">音频/视频和媒体流量中的 UDP 和 TCP 的常规协议用法</span><span class="sxs-lookup"><span data-stu-id="2a873-111">General Protocol Usage for UDP and TCP in Audio/Video and Media Traffic</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a873-112">音频/视频传输</span><span class="sxs-lookup"><span data-stu-id="2a873-112">Audio/Video Transport</span></span></th>
<th><span data-ttu-id="2a873-113">使用</span><span class="sxs-lookup"><span data-stu-id="2a873-113">Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a873-114">UDP</span><span class="sxs-lookup"><span data-stu-id="2a873-114">UDP</span></span></p></td>
<td><p><span data-ttu-id="2a873-115">音频和视频的首选传输层协议</span><span class="sxs-lookup"><span data-stu-id="2a873-115">Preferred transport layer protocol for audio and video</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a873-116">TCP</span><span class="sxs-lookup"><span data-stu-id="2a873-116">TCP</span></span></p></td>
<td><p><span data-ttu-id="2a873-117">音频和视频的回退传输层协议</span><span class="sxs-lookup"><span data-stu-id="2a873-117">Fallback transport layer protocol for audio and video</span></span></p>
<p><span data-ttu-id="2a873-118">Office 通信服务器的应用程序共享所需的传输层协议 2007 R2、Lync Server 2010 和 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a873-118">Required transport layer protocol for application sharing to Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013</span></span></p>
<p><span data-ttu-id="2a873-119">将文件传输到 Lync Server 2010 和 Lync Server 2013 所需的传输层协议</span><span class="sxs-lookup"><span data-stu-id="2a873-119">Required transport layer protocol for file transfer to Lync Server 2010 and Lync Server 2013</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="external-av-firewall-port-requirements-for-external-user-access"></a><span data-ttu-id="2a873-120">外部用户访问的外部 A/V 防火墙端口要求</span><span class="sxs-lookup"><span data-stu-id="2a873-120">External A/V Firewall Port Requirements for External User Access</span></span>

<span data-ttu-id="2a873-121">无论客户端的版本或联合合作伙伴的版本如何，防火墙端口对外部 (和内部) SIP 和会议界面的要求都是一致的。</span><span class="sxs-lookup"><span data-stu-id="2a873-121">The firewall port requirements for external (and internal) SIP and conferencing interfaces are consistent, regardless of the version of your client or the version of the federation partner.</span></span>

<span data-ttu-id="2a873-122">音频/视频边缘外部界面同样不成立。</span><span class="sxs-lookup"><span data-stu-id="2a873-122">The same is not true for the Audio/Video Edge external interface.</span></span> <span data-ttu-id="2a873-123">对于使用 Office 通信服务器2007的联盟，A/V 边缘服务要求外部防火墙规则允许50000至59999端口范围内的 RTP/TCP 和 RTP/UDP 流量双向流动。</span><span class="sxs-lookup"><span data-stu-id="2a873-123">For federation with Office Communications Server 2007, the A/V Edge service requires that external firewall rules allow RTP/TCP and RTP/UDP traffic in the 50,000 through 59,999 port range to flow in both directions.</span></span> <span data-ttu-id="2a873-124">上表假设 Lync Server 2013 是主联合身份验证伙伴，并且配置为与列出的其他联合合作伙伴类型之一进行通信。</span><span class="sxs-lookup"><span data-stu-id="2a873-124">The previous table assumes that Lync Server 2013 is the primary federation partner and it is being configured to communicate with one of the other federation partner types listed.</span></span>

<span data-ttu-id="2a873-125">配置 50000-59999 的音频/视频端口范围必须考虑到端口范围将包含用于与联合身份验证伙伴通信的源端口。</span><span class="sxs-lookup"><span data-stu-id="2a873-125">Configuring the Audio/Video port range of 50,000-59,999 must take into account that the port range will contain the source ports for communications to federation partners.</span></span> <span data-ttu-id="2a873-126">在详细信息中，请考虑从联合身份验证伙伴发起通信。</span><span class="sxs-lookup"><span data-stu-id="2a873-126">In detail, consider that a communication is initiated from a federation partner.</span></span> <span data-ttu-id="2a873-127">从59999范围内的 A/V 边缘服务端口进行的通信将连接到合作伙伴的 A/V 边缘服务的预期端口 TCP 443。</span><span class="sxs-lookup"><span data-stu-id="2a873-127">The communication from the A/V Edge service ports in the 50,000-59,999 range will connect to the expected port TCP 443 of the partner’s A/V Edge service.</span></span> <span data-ttu-id="2a873-128">相反，到 A/V 边缘服务端口 TCP 443 的入站流量将具有59999中的源端口。</span><span class="sxs-lookup"><span data-stu-id="2a873-128">Conversely, inbound traffic to your A/V Edge service port TCP 443 will have a source port in the range of 50,000-59,999.</span></span>

<span data-ttu-id="2a873-129">防火墙管理的不同防火墙和策略可能只需要配置目标规则，也可能需要配置源和目标。</span><span class="sxs-lookup"><span data-stu-id="2a873-129">Different firewalls and policies for firewall administration may require only destination rules to be configured, or they may require both source and destination to be configured.</span></span> <span data-ttu-id="2a873-130">如果您的要求仅适用于目的地端口，音频/视频要求如下：</span><span class="sxs-lookup"><span data-stu-id="2a873-130">If your requirements are for destination ports only, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a873-131">源 IP</span><span class="sxs-lookup"><span data-stu-id="2a873-131">Source IP</span></span></th>
<th><span data-ttu-id="2a873-132">目标 IP</span><span class="sxs-lookup"><span data-stu-id="2a873-132">Destination IP</span></span></th>
<th><span data-ttu-id="2a873-133">目标端口</span><span class="sxs-lookup"><span data-stu-id="2a873-133">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a873-134">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-134">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-135">任意</span><span class="sxs-lookup"><span data-stu-id="2a873-135">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-136">TCP 443</span><span class="sxs-lookup"><span data-stu-id="2a873-136">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a873-137">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-137">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-138">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-138">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-139">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="2a873-139">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a873-140">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-140">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-141">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-141">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-142">TCP 443</span><span class="sxs-lookup"><span data-stu-id="2a873-142">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a873-143">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-143">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-144">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-144">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-145">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="2a873-145">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a873-146">如果你的策略需要入站和出站防火墙规则定义，音频/视频要求如下：</span><span class="sxs-lookup"><span data-stu-id="2a873-146">If your policies require both inbound and outbound firewall rule definitions, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a873-147">源 IP</span><span class="sxs-lookup"><span data-stu-id="2a873-147">Source IP</span></span></th>
<th><span data-ttu-id="2a873-148">目标 IP</span><span class="sxs-lookup"><span data-stu-id="2a873-148">Destination IP</span></span></th>
<th><span data-ttu-id="2a873-149">源端口</span><span class="sxs-lookup"><span data-stu-id="2a873-149">Source Port</span></span></th>
<th><span data-ttu-id="2a873-150">目标端口</span><span class="sxs-lookup"><span data-stu-id="2a873-150">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a873-151">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-151">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-152">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-152">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-153">TCP 50,000-59,999</span><span class="sxs-lookup"><span data-stu-id="2a873-153">TCP 50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="2a873-154">TCP 443</span><span class="sxs-lookup"><span data-stu-id="2a873-154">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a873-155">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-155">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-156">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-156">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-157">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="2a873-157">UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="2a873-158">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="2a873-158">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a873-159">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-159">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-160">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-160">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-161">任意</span><span class="sxs-lookup"><span data-stu-id="2a873-161">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-162">TCP 443</span><span class="sxs-lookup"><span data-stu-id="2a873-162">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a873-163">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-163">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-164">A/V 边缘服务接口</span><span class="sxs-lookup"><span data-stu-id="2a873-164">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="2a873-165">任何</span><span class="sxs-lookup"><span data-stu-id="2a873-165">Any</span></span></p></td>
<td><p><span data-ttu-id="2a873-166">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="2a873-166">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="2a873-167">Microsoft Office 通信服务器2007需要稍有不同的配置。</span><span class="sxs-lookup"><span data-stu-id="2a873-167">Microsoft Office Communications Server 2007 requires a slightly different configuration.</span></span> <span data-ttu-id="2a873-168">TCP 和 UDP 端口范围59999必须打开入站和出站。</span><span class="sxs-lookup"><span data-stu-id="2a873-168">The TCP and UDP port range of 50,000-59,999 must be open inbound and outbound.</span></span> <span data-ttu-id="2a873-169">此要求仅适用于 Office Communicator 2007。</span><span class="sxs-lookup"><span data-stu-id="2a873-169">This requirement is only for Office Communicator 2007.</span></span> <span data-ttu-id="2a873-170">Office 通信服务器 2007 R2、Lync Server 2010 和 Lync Server 2013 仅要求 TCP 范围 50000-59999 打开出站。</span><span class="sxs-lookup"><span data-stu-id="2a873-170">Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013 only require TCP range 50,000-59,999 open outbound.</span></span>



</div>

</div>

<div>

## <a name="nat-requirements-for-the-edge-service"></a><span data-ttu-id="2a873-171">Edge 服务的 NAT 要求</span><span class="sxs-lookup"><span data-stu-id="2a873-171">NAT requirements for the Edge service</span></span>

<span data-ttu-id="2a873-172">如果你选择为 Edge 服务配置不可路由的专用 IP 地址，则以下 NAT 要求适用：</span><span class="sxs-lookup"><span data-stu-id="2a873-172">The following NAT requirements apply if you choose to configure non-routable private IP addresses for the Edge service:</span></span>

  - <span data-ttu-id="2a873-173">NAT 仅可与 DNS 负载平衡配合使用。</span><span class="sxs-lookup"><span data-stu-id="2a873-173">NAT can only be used with DNS load-balancing.</span></span> <span data-ttu-id="2a873-174">NAT 在硬件负载平衡 (HLB) Edge 拓扑中不受支持。</span><span class="sxs-lookup"><span data-stu-id="2a873-174">NAT is not supported with a hardware load balancing (HLB) Edge topology.</span></span>

  - <span data-ttu-id="2a873-175">NAT 仅可在外部边缘接口上使用。</span><span class="sxs-lookup"><span data-stu-id="2a873-175">NAT can only be used on the external Edge interface.</span></span> <span data-ttu-id="2a873-176">NAT 在内部边缘接口上不受支持。</span><span class="sxs-lookup"><span data-stu-id="2a873-176">NAT is not supported on the internal Edge interface.</span></span>

  - <span data-ttu-id="2a873-177">对于传入和传出通信，NAT 必须是对称的。</span><span class="sxs-lookup"><span data-stu-id="2a873-177">NAT must be symmetric for incoming and outgoing traffic.</span></span>
    
  - <span data-ttu-id="2a873-178">对于来自 Internet 的流量，NAT 必须将目标 IP 地址从 A/V 边缘服务的支持 NAT 的公共 IP 地址更改为其外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="2a873-178">For traffic from the Internet, NAT must change the destination IP address from the NAT-enabled public IP address of the A/V Edge service to its external IP address.</span></span> <span data-ttu-id="2a873-179">源 IP 地址必须保持不变，以便 A/V 边缘服务可以找到最佳媒体路径。</span><span class="sxs-lookup"><span data-stu-id="2a873-179">The source IP address must remain intact, so that the A/V Edge service can find the optimal media path.</span></span>
  
  <span data-ttu-id="2a873-180">例如，在下图中的入站方向上，公共 IP 地址131.107.155.30 已更改为外部 (专用) IP 地址10.45.16.10。</span><span class="sxs-lookup"><span data-stu-id="2a873-180">For example, in the inbound direction in the figure below, the public IP address 131.107.155.30 was changed to the external (private) IP address 10.45.16.10.</span></span> <span data-ttu-id="2a873-181">源 IP 地址保持不变。</span><span class="sxs-lookup"><span data-stu-id="2a873-181">The source IP address remained unchanged.</span></span>
  
  - <span data-ttu-id="2a873-182">对于从 A/V 边缘服务到 Internet 的流量，NAT 必须将源 IP 地址从 A/V 边缘服务的外部 IP 地址更改为启用 NAT 的公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="2a873-182">For traffic from the A/V Edge service to the Internet, NAT must change the source IP address from the external IP address of the A/V Edge service to the NAT-enabled public IP address.</span></span>

<span data-ttu-id="2a873-183">例如，在下图中的出站方向上，外部 (专用) IP 地址10.45.16.10 已更改为公共 IP 地址131.107.155.30。</span><span class="sxs-lookup"><span data-stu-id="2a873-183">For example, in the outbound direction in the figure below, the external (private) IP address 10.45.16.10 was changed to the public IP address 131.107.155.30.</span></span>

<span data-ttu-id="2a873-184">**下图显示了 NAT 如何更改入站流量的目标 IP 地址和出站流量的源 IP 地址。**</span><span class="sxs-lookup"><span data-stu-id="2a873-184">**The figure below shows how NAT changes the destination IP address for inbound traffic and the source IP Address for outbound traffic.**</span></span>

<span data-ttu-id="2a873-185">![更改目标/源 IP 地址](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "更改目标/源 IP 地址")</span><span class="sxs-lookup"><span data-stu-id="2a873-185">![Changing destination/source IP addresses](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Changing destination/source IP addresses")</span></span>

<span data-ttu-id="2a873-186">关键点是：</span><span class="sxs-lookup"><span data-stu-id="2a873-186">The key points are:</span></span>

  - <span data-ttu-id="2a873-187">入站到运行 A/V 边缘服务的服务器的通信，源 IP 地址不会更改，但目标 IP 地址会从131.107.155.30 更改为10.45.16.10 的已转换 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="2a873-187">Traffic that is inbound to the server running the A/V Edge service, the source IP address does not change but the destination IP address changes from 131.107.155.30 to the translated IP address of 10.45.16.10.</span></span>

  - <span data-ttu-id="2a873-188">从运行 A/V 边缘服务的服务器传出的流量返回到工作站，源 IP 地址从服务器的公共 IP 地址更改为运行 A/V 边缘服务的服务器的公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="2a873-188">Traffic that is outbound from the server running the A/V Edge service back to the workstation, the source IP address changes from the server’s public IP address to the public IP address of the server running the A/V Edge service.</span></span> <span data-ttu-id="2a873-189">目标 IP 将保留工作站的公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="2a873-189">The destination IP remains the workstation’s public IP address.</span></span> <span data-ttu-id="2a873-190">数据包离开第一个 NAT 设备出站后，NAT 设备上的规则会将运行 A/V 边缘服务的服务器的源 IP 地址更改为其公共 IP 地址 (10.45.16.10) 到其公共 IP 地址 (131.107.155.30) 。</span><span class="sxs-lookup"><span data-stu-id="2a873-190">After the packet leaves the first NAT device outbound, the rule on the NAT device changes the source IP address of the server running the A/V Edge service external interface IP address (10.45.16.10) to its public IP address (131.107.155.30).</span></span>

<span data-ttu-id="2a873-191"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a873-191"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

