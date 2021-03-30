---
title: Lync Server 2013：标准版服务器的 DNS 要求
description: Lync Server 2013：标准版服务器的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391830"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="58048-103">Lync Server 2013 中标准版服务器的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="58048-103">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58048-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58048-104">

<span> </span></span></span>

<span data-ttu-id="58048-105">_**主题上次修改时间** ：2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="58048-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="58048-106">本部分介绍域名系统 (DNS) 部署标准版服务器所需的记录。</span><span class="sxs-lookup"><span data-stu-id="58048-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="58048-107">标准版服务器的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="58048-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="58048-108">下表指定 Lync Server 2013 Standard Edition 服务器部署的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="58048-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>

### <a name="dns-requirements-for-a-standard-edition-server"></a><span data-ttu-id="58048-109">标准版服务器的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="58048-109">DNS Requirements for a Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58048-110">部署方案</span><span class="sxs-lookup"><span data-stu-id="58048-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="58048-111">DNS 要求</span><span class="sxs-lookup"><span data-stu-id="58048-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58048-112">Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="58048-112">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="58048-113">内部 A 记录，用于将服务器的 FQDN (FQDN) 到其 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="58048-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58048-114">自动客户端登录</span><span class="sxs-lookup"><span data-stu-id="58048-114">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="58048-115">对于每个支持的 SIP 域，_sipinternaltls._tcp 的 SRV 记录。 &lt;通过端口 5061 的域，该域映射到标准版服务器的 FQDN，该服务器对客户端登录请求进行身份验证和 &gt; 重定向。</span><span class="sxs-lookup"><span data-stu-id="58048-115">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="58048-116">有关详细信息，请参阅 <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013</a>中客户端自动登录的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="58048-116">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58048-117">通过统一通信通过统一通信发现 (UC) 设备</span><span class="sxs-lookup"><span data-stu-id="58048-117">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="58048-118">名称为 ucupdates-r2 的内部 A 记录。 &lt;SIP 域，解析为托管设备更新 Web &gt; 服务的标准版本服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="58048-118">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="58048-119">如果 UC 设备已打开，但用户从未登录到该设备，则 A 记录允许设备发现托管设备更新 Web 服务的服务器并获取更新。</span><span class="sxs-lookup"><span data-stu-id="58048-119">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="58048-120">否则，设备在用户首次登录时通过带内预配获取服务器信息。</span><span class="sxs-lookup"><span data-stu-id="58048-120">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58048-121">支持 HTTP 流量的反向代理</span><span class="sxs-lookup"><span data-stu-id="58048-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="58048-122">外部 A 记录，用于将外部 Web 场 FQDN 解析为反向代理的外部 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="58048-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="58048-123">客户端和 UC 设备使用此记录连接到反向代理。</span><span class="sxs-lookup"><span data-stu-id="58048-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="58048-124">有关详细信息，请参阅规划文档中的确定 <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013</a> 的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="58048-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="58048-125">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58048-125">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

