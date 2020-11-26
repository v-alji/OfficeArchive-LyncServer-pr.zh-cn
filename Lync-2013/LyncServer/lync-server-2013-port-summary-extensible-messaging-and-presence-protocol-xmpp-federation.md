---
title: 端口摘要-可扩展消息和状态协议 (XMPP) 联合身份验证
description: 端口摘要-可扩展消息和状态协议 (XMPP) 联盟。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442801"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="c6d5f-103">端口摘要-可扩展消息和状态协议 (XMPP 在 Lync Server 2013 中) 联盟</span><span class="sxs-lookup"><span data-stu-id="c6d5f-103">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c6d5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c6d5f-104">

<span> </span></span></span>

<span data-ttu-id="c6d5f-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="c6d5f-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="c6d5f-106">为可扩展消息和状态协议定义的端口和协议 () XMPP 在 Edge 服务器上部署的代理服务器允许从 XMPP 联盟合作伙伴到边缘服务器的通信，还允许从边缘服务器到 XMPP 联盟合作伙伴的通信。</span><span class="sxs-lookup"><span data-stu-id="c6d5f-106">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="c6d5f-107">规则还在面向内部的防火墙上定义，从前端服务器或前端池到边缘服务器或边缘池。</span><span class="sxs-lookup"><span data-stu-id="c6d5f-107">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="c6d5f-108">可扩展消息和状态协议的防火墙摘要</span><span class="sxs-lookup"><span data-stu-id="c6d5f-108">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6d5f-109">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="c6d5f-109">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="c6d5f-110">源 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="c6d5f-110">Source (IP address)</span></span></th>
<th><span data-ttu-id="c6d5f-111">目标 (IP 地址) </span><span class="sxs-lookup"><span data-stu-id="c6d5f-111">Destination (IP address)</span></span></th>
<th><span data-ttu-id="c6d5f-112">备注</span><span class="sxs-lookup"><span data-stu-id="c6d5f-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6d5f-113">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c6d5f-113">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-114">任意</span><span class="sxs-lookup"><span data-stu-id="c6d5f-114">Any</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-115">Access Edge 服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="c6d5f-115">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-116">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="c6d5f-116">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="c6d5f-117">允许与联盟 XMPP 合作伙伴的 Edge 服务器 XMPP 代理通信</span><span class="sxs-lookup"><span data-stu-id="c6d5f-117">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d5f-118">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="c6d5f-118">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-119">Access Edge 服务接口 IP 地址</span><span class="sxs-lookup"><span data-stu-id="c6d5f-119">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-120">任意</span><span class="sxs-lookup"><span data-stu-id="c6d5f-120">Any</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-121">适用于 XMPP 的标准服务器到服务器通信端口。</span><span class="sxs-lookup"><span data-stu-id="c6d5f-121">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="c6d5f-122">允许从 Edge 服务器 XMPP 代理到联合 XMPP 合作伙伴的通信</span><span class="sxs-lookup"><span data-stu-id="c6d5f-122">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d5f-123">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="c6d5f-123">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-124">任意</span><span class="sxs-lookup"><span data-stu-id="c6d5f-124">Any</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-125">内部边缘服务器接口 IP</span><span class="sxs-lookup"><span data-stu-id="c6d5f-125">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="c6d5f-126">从前端服务器或前端池中的 XMPP 网关到边缘服务器的内部 XMPP 流量</span><span class="sxs-lookup"><span data-stu-id="c6d5f-126">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c6d5f-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6d5f-127">See Also</span></span>


[<span data-ttu-id="c6d5f-128">Lync Server 2013 中的示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="c6d5f-128">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="c6d5f-129">在 Lync Server 2013 中管理组织的 XMPP 联盟伙伴</span><span class="sxs-lookup"><span data-stu-id="c6d5f-129">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="c6d5f-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c6d5f-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

