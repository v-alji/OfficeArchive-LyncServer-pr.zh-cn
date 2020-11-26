---
title: DNS 摘要-可扩展消息和状态协议 (XMPP) 联合身份验证
description: DNS 摘要-可扩展消息和状态协议 (XMPP) 联盟。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 0f720a2a-8ab5-43cc-882a-ab595ed3cec7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618368(v=OCS.15)
ms:contentKeyID: 49105655
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b8088e30c93faa52c575fefa97e572ed20b6ad9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437733"
---
# <a name="dns-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="d4e9e-103">DNS 摘要-可扩展消息和状态协议 (XMPP 在 Lync Server 2013 中) 联盟</span><span class="sxs-lookup"><span data-stu-id="d4e9e-103">DNS summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4e9e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4e9e-104">

<span> </span></span></span>

<span data-ttu-id="d4e9e-105">_**主题上次修改时间：** 2014-04-08_</span><span class="sxs-lookup"><span data-stu-id="d4e9e-105">_**Topic Last Modified:** 2014-04-08_</span></span>

<span data-ttu-id="d4e9e-106">若要配置可扩展消息和状态协议 (XMPP) 对于你的部署，你将在外部 DNS 服务器中创建两个域名系统 (DNS) 记录，该 DNS 服务器会将记录解析为 Edge 服务器或边缘池的访问边缘服务。</span><span class="sxs-lookup"><span data-stu-id="d4e9e-106">To configure extensible messaging and presence protocol (XMPP) for your deployment, you create two Domain Name System (DNS) records in an external DNS server that will resolve the records to the Access Edge service of your Edge Server or Edge pool.</span></span>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="d4e9e-107">可扩展消息和状态协议的 DNS 摘要</span><span class="sxs-lookup"><span data-stu-id="d4e9e-107">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4e9e-108">位置/类型/端口</span><span class="sxs-lookup"><span data-stu-id="d4e9e-108">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="d4e9e-109">FQDN</span><span class="sxs-lookup"><span data-stu-id="d4e9e-109">FQDN</span></span></th>
<th><span data-ttu-id="d4e9e-110">IP 地址/FQDN 主机记录</span><span class="sxs-lookup"><span data-stu-id="d4e9e-110">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="d4e9e-111">映射到/批注</span><span class="sxs-lookup"><span data-stu-id="d4e9e-111">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4e9e-112">外部 DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="d4e9e-112">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="d4e9e-113">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d4e9e-113">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d4e9e-114">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d4e9e-114">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d4e9e-115">"访问边缘服务" 或 "边缘池" 上的 XMPP 代理外部接口。对于启用了 Lync 的用户，通过全局策略、用户所在的网站策略或应用到启用了 Lync 的用户的用户策略，可以为所有内部 SIP 域重复此操作。</span><span class="sxs-lookup"><span data-stu-id="d4e9e-115">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="d4e9e-116">还必须在 XMPP 联盟合作伙伴策略中配置允许的 XMPP 域。</span><span class="sxs-lookup"><span data-stu-id="d4e9e-116">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="d4e9e-117">有关其他详细信息，请参阅 <strong>另请参阅</strong> 中的主题</span><span class="sxs-lookup"><span data-stu-id="d4e9e-117">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4e9e-118">外部 DNS/A</span><span class="sxs-lookup"><span data-stu-id="d4e9e-118">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="d4e9e-119">xmpp.contoso.com (例如) </span><span class="sxs-lookup"><span data-stu-id="d4e9e-119">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="d4e9e-120">边缘服务器上的访问边缘服务的 IP 地址或托管 XMPP 代理的边缘池的 IP 地址</span><span class="sxs-lookup"><span data-stu-id="d4e9e-120">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="d4e9e-121">指向托管 XMPP 代理服务的访问边缘服务或边缘池。</span><span class="sxs-lookup"><span data-stu-id="d4e9e-121">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="d4e9e-122">通常，你创建的 SRV 记录将指向此主机 (A 或 AAAA) 记录</span><span class="sxs-lookup"><span data-stu-id="d4e9e-122">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d4e9e-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d4e9e-123">See Also</span></span>


[<span data-ttu-id="d4e9e-124">在 Lync Server 2013 中设置 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="d4e9e-124">Setting up XMPP federation in Lync Server 2013</span></span>](lync-server-2013-setting-up-xmpp-federation.md)  


[<span data-ttu-id="d4e9e-125">确定 Lync Server 2013 的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="d4e9e-125">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  
  

<span data-ttu-id="d4e9e-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4e9e-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

