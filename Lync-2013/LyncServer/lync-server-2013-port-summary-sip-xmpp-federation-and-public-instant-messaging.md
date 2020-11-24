---
title: 端口摘要-SIP、XMPP 联盟和公共即时消息
description: 端口摘要-SIP、XMPP 联盟和公共即时消息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - SIP, XMPP federation, and public instant messaging
ms:assetid: ab05bdd6-e9b0-4b1b-9dd9-29ab88e8befe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618373(v=OCS.15)
ms:contentKeyID: 49105660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c58dbf7bdd56b4678d56f96a11332219bb40c17
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391826"
---
# <a name="port-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="ab232-103">端口摘要-Lync Server 2013 中的 SIP、XMPP 联盟和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="ab232-103">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab232-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab232-104">

<span> </span></span></span>

<span data-ttu-id="ab232-105">_**主题上次修改时间：** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="ab232-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="ab232-106">与 Microsoft Lync Server 2013、Lync Server 2010 和 Office 通信服务器的联盟的端口、协议和防火墙要求与已部署的边缘服务器的身份验证要求类似。</span><span class="sxs-lookup"><span data-stu-id="ab232-106">Port, protocol and firewall requirements for federation with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server are similar to those for the deployed Edge Server.</span></span> <span data-ttu-id="ab232-107">客户通过 TLS/SIP/TCP 443 上的访问边缘服务发起通信。</span><span class="sxs-lookup"><span data-stu-id="ab232-107">Clients initiate communication with the Access Edge service over TLS/SIP/TCP 443.</span></span> <span data-ttu-id="ab232-108">但是，联盟伙伴将通过 MTLS/SIP/TCP 5061 发起与访问边缘服务的通信。</span><span class="sxs-lookup"><span data-stu-id="ab232-108">Federated partners however, will initiate communications to the Access Edge service over MTLS/SIP/TCP 5061.</span></span>

<span data-ttu-id="ab232-109">若要为支持公共即时消息连接所需的端口和协议配置防火墙，请首先注意 SIP/MTLS/TCP 5061 是双向的，以确保公共 IM 提供商联系 Lync 客户端的能力或 Lync 联系公共 IM 联系人。</span><span class="sxs-lookup"><span data-stu-id="ab232-109">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="ab232-110">Windows Live Messenger 可参与 Lync 客户端的音频/视频通信。</span><span class="sxs-lookup"><span data-stu-id="ab232-110">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="ab232-111">此帐户适用于通常在防火墙上支持 Lync 客户端作为外部用户的防火墙端口和协议配置。</span><span class="sxs-lookup"><span data-stu-id="ab232-111">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="ab232-112">Lync 比以往更多，是一种强大的工具，用于跨组织和全球各地的人员进行连接。</span><span class="sxs-lookup"><span data-stu-id="ab232-112">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="ab232-113">与 Windows Live Messenger 的联盟不需要除 Lync 标准客户端访问许可证 (CAL) 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="ab232-113">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="ab232-114">Skype 联盟将添加到此列表，使 Lync 用户可以通过 IM 和语音与成百上千人联系。</span><span class="sxs-lookup"><span data-stu-id="ab232-114">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="ab232-115">与 Messenger 客户联系人的联盟将于2013年3月15日（中国大陆除外）正式结束。</span><span class="sxs-lookup"><span data-stu-id="ab232-115">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="ab232-116">Skype 将成为以前使用 Messenger 的联盟用户的联合身份验证客户端。</span><span class="sxs-lookup"><span data-stu-id="ab232-116">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<span data-ttu-id="ab232-117">为可扩展消息和状态协议定义的端口和协议 () XMPP 在 Edge 服务器上部署的代理服务器允许从 XMPP 联盟合作伙伴到边缘服务器的通信，还允许从边缘服务器到 XMPP 联盟合作伙伴的通信。</span><span class="sxs-lookup"><span data-stu-id="ab232-117">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="ab232-118">规则还在面向内部的防火墙上定义，从前端服务器或前端池到边缘服务器或边缘池。</span><span class="sxs-lookup"><span data-stu-id="ab232-118">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary---sip-federation"></a><span data-ttu-id="ab232-119">防火墙摘要-SIP 联盟</span><span class="sxs-lookup"><span data-stu-id="ab232-119">Firewall Summary - SIP Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab232-120">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="ab232-120">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="ab232-121">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="ab232-121">Source IP address</span></span></th>
<th><span data-ttu-id="ab232-122">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="ab232-122">Destination IP address</span></span></th>
<th><span data-ttu-id="ab232-123">备注</span><span class="sxs-lookup"><span data-stu-id="ab232-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab232-124">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="ab232-124">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="ab232-125">Access Edge 服务公共 IP 地址</span><span class="sxs-lookup"><span data-stu-id="ab232-125">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="ab232-126">任意</span><span class="sxs-lookup"><span data-stu-id="ab232-126">Any</span></span></p></td>
<td><p><span data-ttu-id="ab232-127">对于使用 SIP 的联盟和公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="ab232-127">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="ab232-128">防火墙摘要-公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="ab232-128">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab232-129">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="ab232-129">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="ab232-130">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="ab232-130">Source IP address</span></span></th>
<th><span data-ttu-id="ab232-131">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="ab232-131">Destination IP address</span></span></th>
<th><span data-ttu-id="ab232-132">备注</span><span class="sxs-lookup"><span data-stu-id="ab232-132">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab232-133">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="ab232-133">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="ab232-134">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="ab232-134">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="ab232-135">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="ab232-135">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="ab232-136">对于使用 SIP 的联盟和公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="ab232-136">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab232-137">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="ab232-137">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="ab232-138">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="ab232-138">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="ab232-139">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="ab232-139">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="ab232-140">对于使用 SIP 的联盟和公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="ab232-140">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab232-141">Access/SIP (TLS) /TCP/443</span><span class="sxs-lookup"><span data-stu-id="ab232-141">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="ab232-142">客户端</span><span class="sxs-lookup"><span data-stu-id="ab232-142">Clients</span></span></p></td>
<td><p><span data-ttu-id="ab232-143">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="ab232-143">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="ab232-144">外部用户访问的客户端到服务器 SIP 通信。</span><span class="sxs-lookup"><span data-stu-id="ab232-144">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab232-145">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="ab232-145">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="ab232-146">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="ab232-146">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="ab232-147">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="ab232-147">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="ab232-148">如果配置了公用 IM 连接，则用于带有 Windows Live Messenger 的 A/V 会话。</span><span class="sxs-lookup"><span data-stu-id="ab232-148">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab232-149">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="ab232-149">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="ab232-150">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="ab232-150">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="ab232-151">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="ab232-151">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="ab232-152">对于具有 Windows Live Messenger 的公共 IM 连接，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="ab232-152">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab232-153">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="ab232-153">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="ab232-154">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="ab232-154">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="ab232-155">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="ab232-155">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="ab232-156">对于具有 Windows Live Messenger 的公共 IM 连接，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="ab232-156">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="ab232-157">防火墙摘要-可扩展消息和状态协议 (XMPP) </span><span class="sxs-lookup"><span data-stu-id="ab232-157">Firewall Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab232-158">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="ab232-158">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="ab232-159">源 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="ab232-159">Source (IP address)</span></span></th>
<th><span data-ttu-id="ab232-160">目标 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="ab232-160">Destination (IP address)</span></span></th>
<th><span data-ttu-id="ab232-161">备注</span><span class="sxs-lookup"><span data-stu-id="ab232-161">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab232-162">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="ab232-162">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="ab232-163">任意</span><span class="sxs-lookup"><span data-stu-id="ab232-163">Any</span></span></p></td>
<td><p><span data-ttu-id="ab232-164">Access Edge 服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="ab232-164">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="ab232-165">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="ab232-165">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="ab232-166">允许与联盟 XMPP 合作伙伴的 Edge 服务器 XMPP 代理通信</span><span class="sxs-lookup"><span data-stu-id="ab232-166">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab232-167">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="ab232-167">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="ab232-168">Access Edge 服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="ab232-168">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="ab232-169">任意</span><span class="sxs-lookup"><span data-stu-id="ab232-169">Any</span></span></p></td>
<td><p><span data-ttu-id="ab232-170">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="ab232-170">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="ab232-171">允许从 Edge 服务器 XMPP 代理到联合 XMPP 合作伙伴的通信</span><span class="sxs-lookup"><span data-stu-id="ab232-171">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab232-172">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="ab232-172">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="ab232-173">任意</span><span class="sxs-lookup"><span data-stu-id="ab232-173">Any</span></span></p></td>
<td><p><span data-ttu-id="ab232-174">内部边缘服务器接口 IP</span><span class="sxs-lookup"><span data-stu-id="ab232-174">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="ab232-175">从前端服务器或前端池中的 XMPP 网关到边缘服务器的内部 XMPP 流量</span><span class="sxs-lookup"><span data-stu-id="ab232-175">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ab232-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ab232-176">See Also</span></span>


[<span data-ttu-id="ab232-177">Lync Server 2013 中的外部用户访问方案</span><span class="sxs-lookup"><span data-stu-id="ab232-177">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="ab232-178">确定 Lync Server 2013 的外部 A/V 防火墙和端口要求</span><span class="sxs-lookup"><span data-stu-id="ab232-178">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  


[<span data-ttu-id="ab232-179">在 Lync Server 2013 中管理组织的 XMPP 联盟伙伴</span><span class="sxs-lookup"><span data-stu-id="ab232-179">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="ab232-180"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab232-180"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

