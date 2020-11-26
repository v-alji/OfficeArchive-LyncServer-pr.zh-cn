---
title: Lync Server 2013：端口摘要-公共即时消息连接
description: Lync Server 2013：端口摘要-公共即时消息连接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Public instant messaging connectivity
ms:assetid: f46756ec-1401-4ca2-a4a4-5cd28bcfdc7f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618376(v=OCS.15)
ms:contentKeyID: 49105663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4137b5f92e043dc15dc9aa1f0b9593b4d9f7c2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424273"
---
# <a name="port-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="eb3ca-103">端口摘要-Lync Server 2013 中的公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="eb3ca-103">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb3ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb3ca-104">

<span> </span></span></span>

<span data-ttu-id="eb3ca-105">_**主题上次修改时间：** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="eb3ca-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="eb3ca-106">若要为支持公共即时消息连接所需的端口和协议配置防火墙，请首先注意 SIP/MTLS/TCP 5061 是双向的，以确保公共 IM 提供商联系 Lync 客户端的能力或 Lync 联系公共 IM 联系人。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-106">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="eb3ca-107">Windows Live Messenger 可参与 Lync 客户端的音频/视频通信。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-107">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="eb3ca-108">此帐户适用于通常在防火墙上支持 Lync 客户端作为外部用户的防火墙端口和协议配置。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-108">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="eb3ca-109">Lync 比以往更多，是一种强大的工具，用于跨组织和全球各地的人员进行连接。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-109">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="eb3ca-110">与 Windows Live Messenger 的联盟不需要除 Lync 标准客户端访问许可证 (CAL) 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-110">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="eb3ca-111">Skype 联盟将添加到此列表，使 Lync 用户可以通过 IM 和语音与成百上千人联系。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-111">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="eb3ca-112">与 Messenger 客户联系人的联盟将于2013年3月15日（中国大陆除外）正式结束。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-112">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="eb3ca-113">Skype 将成为以前使用 Messenger 的联盟用户的联合身份验证客户端。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-113">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="eb3ca-114">防火墙摘要-公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="eb3ca-114">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb3ca-115">角色/协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="eb3ca-115">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="eb3ca-116">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="eb3ca-116">Source IP address</span></span></th>
<th><span data-ttu-id="eb3ca-117">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="eb3ca-117">Destination IP address</span></span></th>
<th><span data-ttu-id="eb3ca-118">备注</span><span class="sxs-lookup"><span data-stu-id="eb3ca-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb3ca-119">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="eb3ca-119">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-120">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="eb3ca-120">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-121">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="eb3ca-121">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-122">对于使用 SIP 的联盟和公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-122">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb3ca-123">Access/SIP (MTLS) /TCP/5061</span><span class="sxs-lookup"><span data-stu-id="eb3ca-123">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-124">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="eb3ca-124">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-125">公共 IM 连接合作伙伴</span><span class="sxs-lookup"><span data-stu-id="eb3ca-125">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-126">对于使用 SIP 的联盟和公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-126">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb3ca-127">Access/SIP (TLS) /TCP/443</span><span class="sxs-lookup"><span data-stu-id="eb3ca-127">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-128">客户端</span><span class="sxs-lookup"><span data-stu-id="eb3ca-128">Clients</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-129">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="eb3ca-129">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-130">外部用户访问的客户端到服务器 SIP 通信。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-130">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb3ca-131">A/V/RTP/TCP/50000-59999</span><span class="sxs-lookup"><span data-stu-id="eb3ca-131">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-132">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="eb3ca-132">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-133">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="eb3ca-133">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-134">如果配置了公用 IM 连接，则用于带有 Windows Live Messenger 的 A/V 会话。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-134">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb3ca-135">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="eb3ca-135">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-136">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="eb3ca-136">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-137">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="eb3ca-137">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-138">对于具有 Windows Live Messenger 的公共 IM 连接，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-138">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb3ca-139">A/V/STUN、MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="eb3ca-139">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-140">实时 Messenger 客户端</span><span class="sxs-lookup"><span data-stu-id="eb3ca-140">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-141">Edge 服务器访问接口</span><span class="sxs-lookup"><span data-stu-id="eb3ca-141">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="eb3ca-142">对于具有 Windows Live Messenger 的公共 IM 连接，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="eb3ca-142">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="eb3ca-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb3ca-143">See Also</span></span>


[<span data-ttu-id="eb3ca-144">Lync Server 2013 中的外部用户访问方案</span><span class="sxs-lookup"><span data-stu-id="eb3ca-144">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="eb3ca-145">确定 Lync Server 2013 的外部 A/V 防火墙和端口要求</span><span class="sxs-lookup"><span data-stu-id="eb3ca-145">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="eb3ca-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb3ca-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

