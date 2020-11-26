---
title: Lync Server 2013：端口摘要 - 反向代理
description: Lync Server 2013：端口摘要-反向代理。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Reverse proxy
ms:assetid: 59b9ac3c-3e6f-4776-b366-174f0dd1f2eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204932(v=OCS.15)
ms:contentKeyID: 48184251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf07800c91f5a28165eb05e14e2d775758460f50
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442808"
---
# <a name="port-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="b35c7-103">Lync Server 2013 中的端口摘要 - 反向代理</span><span class="sxs-lookup"><span data-stu-id="b35c7-103">Port summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b35c7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b35c7-104">

<span> </span></span></span>

<span data-ttu-id="b35c7-105">_**主题上次修改时间：** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="b35c7-105">_**Topic Last Modified:** 2013-02-15_</span></span>

<span data-ttu-id="b35c7-106">反向代理对防火墙和端口/协议具有最低要求。</span><span class="sxs-lookup"><span data-stu-id="b35c7-106">The reverse proxy has minimal requirements for firewall and port/protocol.</span></span>

  - <span data-ttu-id="b35c7-107">外部防火墙要求是 HTTPS/TCP/443 以及可选的 HTTP/TCP/80。</span><span class="sxs-lookup"><span data-stu-id="b35c7-107">External firewall requirements are the HTTPS/TCP/443 and the optional HTTP/TCP/80.</span></span> <span data-ttu-id="b35c7-108">HTTPS 用于通过反向代理进行 SSL 和 TLS 安全通信。</span><span class="sxs-lookup"><span data-stu-id="b35c7-108">HTTPS is used for SSL and TLS secure communications through the reverse proxy.</span></span> <span data-ttu-id="b35c7-109">如果你选择允许在修改证书时访问自动发现服务的操作可能很难或不会导致成本调整，则使用 HTTP。</span><span class="sxs-lookup"><span data-stu-id="b35c7-109">HTTP is used if you choose to allow access to the Autodiscover Service when modifying certificates might prove difficult or not cost justified.</span></span>

  - <span data-ttu-id="b35c7-110">客户端希望在 HTTPS 上联系 Office Web Apps 服务器。</span><span class="sxs-lookup"><span data-stu-id="b35c7-110">Clients expect to contact the Office Web Apps Server on HTTPS.</span></span> <span data-ttu-id="b35c7-111">Office Web Apps 服务器需要来自 HTTPS/TCP/443 的内部客户端的通信。</span><span class="sxs-lookup"><span data-stu-id="b35c7-111">The Office Web Apps Server expects communication from internal clients on HTTPS/TCP/443.</span></span> <span data-ttu-id="b35c7-112">建议的配置是允许从反向代理到 Office Web Apps 服务器的 HTTPS/TCP/443。</span><span class="sxs-lookup"><span data-stu-id="b35c7-112">The recommended configuration is to allow HTTPS/TCP/443 from the reverse proxy to the Office Web Apps Server.</span></span>

  - <span data-ttu-id="b35c7-113">端口8080用于将流量从反向代理内部接口路由到前端服务器、前端池虚拟 IP (VIP) 或可选 Director 或控制器池 VIP。</span><span class="sxs-lookup"><span data-stu-id="b35c7-113">Port 8080 is used to route traffic from the reverse proxy internal interface to the Front End Server, Front End pool virtual IP (VIP) or the optional Director or Director pool VIP.</span></span> <span data-ttu-id="b35c7-114">对于运行 Lync 的移动设备，如果需要修改外部 web 服务发布规则证书的情况下，需要使用端口 TCP 8080 以找到自动发现服务 (例如，如果你有大量 SIP 域) 。</span><span class="sxs-lookup"><span data-stu-id="b35c7-114">Port TCP 8080 is required for mobile devices running Lync to locate the Autodiscover Service in situations where modifying the external web service publishing rule certificate is undesirable (for example, if you have a large number of SIP domains).</span></span> <span data-ttu-id="b35c7-115">如果你选择用所需的 SAN 条目获取新的证书，则不需要端口 TCP 8080，并且是可选的。</span><span class="sxs-lookup"><span data-stu-id="b35c7-115">If you choose to acquire new certificates with the necessary SAN entries, the port TCP 8080 is not needed and is optional.</span></span>

  - <span data-ttu-id="b35c7-116">端口4443用于从反向代理内部接口到前端服务器的流量、前端池虚拟 IP (VIP) 或可选控制器或控制器池 VIP</span><span class="sxs-lookup"><span data-stu-id="b35c7-116">Port 4443 is used for traffic from the reverse proxy internal interface to the Front End Server, Front End pool virtual IP (VIP) or the optional Director or Director pool VIP</span></span>
    
    <span data-ttu-id="b35c7-117">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span><span class="sxs-lookup"><span data-stu-id="b35c7-117">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span></span>  
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="b35c7-118">不要将4443中的与来自管理中央管理存储角色的标准版服务器或前端池的 TCP 流量的端口4443的内部部署相混淆。</span><span class="sxs-lookup"><span data-stu-id="b35c7-118">Do not confuse the 4443 over TCP from the reverse proxy to the internal deployment for the port 4443 over TCP traffic from the Standard Edition server or the Front End pool that manages the Central Management store role.</span></span>

    
    </div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="b35c7-119">端口和协议详细信息</span><span class="sxs-lookup"><span data-stu-id="b35c7-119">Port and Protocol Details</span></span>

### <a name="firewall-details-for-reverse-proxy-server-external-interface"></a><span data-ttu-id="b35c7-120">反向代理服务器的防火墙详细信息：外部接口</span><span class="sxs-lookup"><span data-stu-id="b35c7-120">Firewall Details for Reverse Proxy Server: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b35c7-121">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="b35c7-121">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="b35c7-122">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="b35c7-122">Source IP Address</span></span></th>
<th><span data-ttu-id="b35c7-123">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="b35c7-123">Destination IP Address</span></span></th>
<th><span data-ttu-id="b35c7-124">注释</span><span class="sxs-lookup"><span data-stu-id="b35c7-124">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b35c7-125">HTTP/TCP/80</span><span class="sxs-lookup"><span data-stu-id="b35c7-125">HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="b35c7-126">任意</span><span class="sxs-lookup"><span data-stu-id="b35c7-126">Any</span></span></p></td>
<td><p><span data-ttu-id="b35c7-127">反向代理侦听器</span><span class="sxs-lookup"><span data-stu-id="b35c7-127">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="b35c7-128">如果用户输入 http://publishedSiteFQDN， (可选) 重定向到 HTTPS &lt; &gt; 。</span><span class="sxs-lookup"><span data-stu-id="b35c7-128">(Optional) Redirection to HTTPS if user enters http://&lt;publishedSiteFQDN&gt;.</span></span></p>
<p><span data-ttu-id="b35c7-129">如果在组织不希望修改外部 Web 服务发布规则证书的情况下，使用适用于会议的 Office Web Apps 和适用于运行 Lync 的移动设备的自动发现服务，也需要使用此参数。</span><span class="sxs-lookup"><span data-stu-id="b35c7-129">Also required if using Office Web Apps for conferencing and the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b35c7-130">HTTPS/TCP/443</span><span class="sxs-lookup"><span data-stu-id="b35c7-130">HTTPS/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="b35c7-131">任意</span><span class="sxs-lookup"><span data-stu-id="b35c7-131">Any</span></span></p></td>
<td><p><span data-ttu-id="b35c7-132">反向代理侦听器</span><span class="sxs-lookup"><span data-stu-id="b35c7-132">Reverse proxy listener</span></span></p></td>
<td><p><span data-ttu-id="b35c7-133">通讯簿下载，通讯簿 Web 查询服务，自动发现，客户端更新，会议内容，设备更新，组扩展，适用于会议的 Office Web Apps，电话拨入式会议和会议。</span><span class="sxs-lookup"><span data-stu-id="b35c7-133">Address book downloads, Address Book Web Query service, Autodiscover, client updates, meeting content, device updates, group expansion, Office Web Apps for conferencing, dial-in conferencing, and meetings.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-details-for-reverse-proxy-server-internal-interface"></a><span data-ttu-id="b35c7-134">反向代理服务器的防火墙详细信息：内部接口</span><span class="sxs-lookup"><span data-stu-id="b35c7-134">Firewall Details for Reverse Proxy Server: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b35c7-135">协议/TCP 或 UDP/端口</span><span class="sxs-lookup"><span data-stu-id="b35c7-135">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="b35c7-136">源 IP 地址</span><span class="sxs-lookup"><span data-stu-id="b35c7-136">Source IP Address</span></span></th>
<th><span data-ttu-id="b35c7-137">目标 IP 地址</span><span class="sxs-lookup"><span data-stu-id="b35c7-137">Destination IP Address</span></span></th>
<th><span data-ttu-id="b35c7-138">注释</span><span class="sxs-lookup"><span data-stu-id="b35c7-138">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b35c7-139">HTTP/TCP/8080</span><span class="sxs-lookup"><span data-stu-id="b35c7-139">HTTP/TCP/8080</span></span></p></td>
<td><p><span data-ttu-id="b35c7-140">内部反向代理接口</span><span class="sxs-lookup"><span data-stu-id="b35c7-140">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="b35c7-141">前端服务器、前端池、导演、控制器池</span><span class="sxs-lookup"><span data-stu-id="b35c7-141">Front End Server, Front End pool, Director, Director pool</span></span></p></td>
<td><p><span data-ttu-id="b35c7-142">如果在组织不希望修改外部 web 服务发布规则证书的情况下使用运行 Lync 的移动设备的自动发现服务，则为必需。</span><span class="sxs-lookup"><span data-stu-id="b35c7-142">Required if using the Autodiscover Service for mobile devices running Lync in situations where the organization does not want to modify the external web service publishing rule certificate.</span></span></p>
<p><span data-ttu-id="b35c7-143">发送到反向代理外部接口上的端口80的流量将从反向代理内部接口重定向到端口8080上的池，以便池 Web 服务可以将其与内部 Web 流量区分开。</span><span class="sxs-lookup"><span data-stu-id="b35c7-143">Traffic sent to port 80 on the reverse proxy external interface is redirected to a pool on port 8080 from the reverse proxy internal interface so that the pool Web Services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b35c7-144">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="b35c7-144">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="b35c7-145">内部反向代理接口</span><span class="sxs-lookup"><span data-stu-id="b35c7-145">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="b35c7-146">前端服务器、前端池、导演、控制器池</span><span class="sxs-lookup"><span data-stu-id="b35c7-146">Front End Server, Front End pool, Director, Director pool</span></span></p></td>
<td><p><span data-ttu-id="b35c7-147">发送到反向代理外部接口上的端口443的流量将从反向代理内部接口重定向到端口4443上的池，以便池 web 服务可以将其与内部 web 流量区分开。</span><span class="sxs-lookup"><span data-stu-id="b35c7-147">Traffic sent to port 443 on the reverse proxy external interface is redirected to a pool on port 4443 from the reverse proxy internal interface so that the pool web services can distinguish it from internal web traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b35c7-148">HTTPS/TCP/443</span><span class="sxs-lookup"><span data-stu-id="b35c7-148">HTTPS/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="b35c7-149">内部反向代理接口</span><span class="sxs-lookup"><span data-stu-id="b35c7-149">Internal reverse proxy interface</span></span></p></td>
<td><p><span data-ttu-id="b35c7-150">适用于会议的 Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="b35c7-150">Office Web Apps for conferencing</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="b35c7-151">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b35c7-151">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

