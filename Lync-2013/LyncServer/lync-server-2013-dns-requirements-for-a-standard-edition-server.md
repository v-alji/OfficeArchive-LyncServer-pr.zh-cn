---
title: Lync Server 2013：Standard Edition 服务器的 DNS 要求
description: Lync Server 2013：标准版服务器的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392352"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="80db4-103">Lync Server 2013 中 Standard Edition 服务器的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="80db4-103">DNS requirements for a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80db4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80db4-104">

<span> </span></span></span>

<span data-ttu-id="80db4-105">_**主题上次修改时间** ：2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="80db4-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="80db4-106">本部分介绍域名系统 (DNS) 部署标准版服务器所需的记录。</span><span class="sxs-lookup"><span data-stu-id="80db4-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="80db4-107">标准版服务器的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="80db4-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="80db4-108">下表指定 Lync Server 2013 Standard Edition 服务器部署的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="80db4-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80db4-109">部署方案</span><span class="sxs-lookup"><span data-stu-id="80db4-109">Deployment scenario</span></span></th>
<th><span data-ttu-id="80db4-110">DNS 要求</span><span class="sxs-lookup"><span data-stu-id="80db4-110">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80db4-111">Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="80db4-111">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="80db4-112">内部 A 记录，用于将服务器的 FQDN (FQDN) 到其 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="80db4-112">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80db4-113">自动客户端登录</span><span class="sxs-lookup"><span data-stu-id="80db4-113">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="80db4-114">对于每个支持的 SIP 域，_sipinternaltls._tcp 的 SRV 记录。 &lt;通过端口 5061 的域，该域映射到标准版服务器的 FQDN，该服务器对客户端登录请求进行身份验证和 &gt; 重定向。</span><span class="sxs-lookup"><span data-stu-id="80db4-114">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="80db4-115">有关详细信息，请参阅 <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013</a>中客户端自动登录的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="80db4-115">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80db4-116">通过统一通信通过统一通信发现 (UC) 设备</span><span class="sxs-lookup"><span data-stu-id="80db4-116">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="80db4-117">名称为 ucupdates-r2 的内部 A 记录。 &lt;SIP 域，解析为托管设备更新 Web &gt; 服务的标准版本服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="80db4-117">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="80db4-118">如果 UC 设备已打开，但用户从未登录到该设备，则 A 记录允许设备发现托管设备更新 Web 服务的服务器并获取更新。</span><span class="sxs-lookup"><span data-stu-id="80db4-118">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="80db4-119">否则，设备在用户首次登录时通过带内预配获取服务器信息。</span><span class="sxs-lookup"><span data-stu-id="80db4-119">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span> <span data-ttu-id="80db4-120">有关详细信息，请参阅 <a href="lync-server-2013-device-update-web-service.md">操作文档中的 Lync Server 2013</a> 中的设备更新 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="80db4-120">For details, see <a href="lync-server-2013-device-update-web-service.md">Device Update Web service in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80db4-121">支持 HTTP 流量的反向代理</span><span class="sxs-lookup"><span data-stu-id="80db4-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="80db4-122">外部 A 记录，用于将外部 Web 场 FQDN 解析为反向代理的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="80db4-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="80db4-123">客户端和 UC 设备使用此记录连接到反向代理。</span><span class="sxs-lookup"><span data-stu-id="80db4-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="80db4-124">有关详细信息，请参阅规划文档中的确定 <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013</a> 的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="80db4-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="80db4-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80db4-125">See Also</span></span>


[<span data-ttu-id="80db4-126">Lync Server 2013 中自动客户端登录的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="80db4-126">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[<span data-ttu-id="80db4-127">确定 Lync Server 2013 的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="80db4-127">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="80db4-128">Lync Server 2013 中的设备更新 Web 服务</span><span class="sxs-lookup"><span data-stu-id="80db4-128">Device Update Web service in Lync Server 2013</span></span>](lync-server-2013-device-update-web-service.md)  
  

<span data-ttu-id="80db4-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80db4-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

