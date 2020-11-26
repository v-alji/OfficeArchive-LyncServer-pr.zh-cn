---
title: Lync Server 2013：DNS 基础结构支持
description: Lync Server 2013： DNS 基础结构支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Domain Name System (DNS) infrastructure support
ms:assetid: 37777c16-94ce-436d-b517-bcf53a564513
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425850(v=OCS.15)
ms:contentKeyID: 48183878
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea65907eba13367fd92e546d62994d10907bf89
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429075"
---
# <a name="dns-infrastructure-support-in-lync-server-2013"></a><span data-ttu-id="250d2-103">Lync Server 2013 中的 DNS 基础结构支持</span><span class="sxs-lookup"><span data-stu-id="250d2-103">DNS infrastructure support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="250d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="250d2-104">

<span> </span></span></span>

<span data-ttu-id="250d2-105">_**主题上次修改时间：** 2013-03-08_</span><span class="sxs-lookup"><span data-stu-id="250d2-105">_**Topic Last Modified:** 2013-03-08_</span></span>

<span data-ttu-id="250d2-106">Lync Server 2013 需要域名系统 (DNS) 并通过以下方式使用它：</span><span class="sxs-lookup"><span data-stu-id="250d2-106">Lync Server 2013 requires Domain Name System (DNS) and uses it in the following ways:</span></span>

  - <span data-ttu-id="250d2-107">发现内部服务器或池以进行服务器至服务器的通信。</span><span class="sxs-lookup"><span data-stu-id="250d2-107">To discover internal servers or pools for server-to-server communications.</span></span>

  - <span data-ttu-id="250d2-108">使客户能够发现用于各种 SIP 事务的前端池或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="250d2-108">To enable clients to discover the Front End pool or Standard Edition server used for various SIP transactions.</span></span>

  - <span data-ttu-id="250d2-109">将会议的简单 Url 与托管这些会议的服务器相关联。</span><span class="sxs-lookup"><span data-stu-id="250d2-109">To associate the simple URLs for conferences with the servers hosting those conferences.</span></span>

  - <span data-ttu-id="250d2-110">若要启用外部服务器和客户端连接到边缘服务器或 HTTP 反向代理以便发送即时消息 (IM) 或会议。</span><span class="sxs-lookup"><span data-stu-id="250d2-110">To enable external servers and clients to connect to Edge Servers or the HTTP reverse proxy for instant messaging (IM) or conferencing.</span></span>

  - <span data-ttu-id="250d2-111">若要启用统一通信 (UC) 未登录的设备以发现运行设备更新 Web 服务的前端池或标准版服务器，获取更新和发送日志。</span><span class="sxs-lookup"><span data-stu-id="250d2-111">To enable unified communications (UC) devices that are not logged in to discover the Front End pool or Standard Edition server running Device Update Web service, obtain updates, and send logs.</span></span>

  - <span data-ttu-id="250d2-112">使移动客户端能够自动发现 Web 服务资源，而无需用户在设备设置中手动输入 Url。</span><span class="sxs-lookup"><span data-stu-id="250d2-112">To enable mobile clients to automatically discover Web Services resources without requiring users to manually enter URLs in device settings.</span></span>

  - <span data-ttu-id="250d2-113">用于 DNS 负载平衡。</span><span class="sxs-lookup"><span data-stu-id="250d2-113">For DNS load balancing.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="250d2-114">Lync Server 2013 不支持 (IDNs) 的国际化域名。</span><span class="sxs-lookup"><span data-stu-id="250d2-114">Lync Server 2013 does not support internationalized domain names (IDNs).</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="250d2-115">您指定的名称必须与服务器上配置的计算机名相同。</span><span class="sxs-lookup"><span data-stu-id="250d2-115">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="250d2-116">默认情况下，未加入到域的计算机的计算机名是一个短名称，而不是完全限定的域名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="250d2-116">By default, the computer name of a computer that is not joined to a domain is a short name, not a fully qualified domain name (FQDN).</span></span> <span data-ttu-id="250d2-117">拓扑生成器使用 FQDN，而不是短名称。</span><span class="sxs-lookup"><span data-stu-id="250d2-117">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="250d2-118">因此，您必须在要部署为域外边缘服务器的计算机的名称上配置 DNS 后缀。</span><span class="sxs-lookup"><span data-stu-id="250d2-118">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="250d2-119">分配您的 Lync Server、边缘服务器和池的 FQDN 时，<STRONG>只使用标准字符</STRONG>（包括 A–Z、a–z、0–9 和连字符）。</span><span class="sxs-lookup"><span data-stu-id="250d2-119"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="250d2-120">不要使用 Unicode 字符或下划线。</span><span class="sxs-lookup"><span data-stu-id="250d2-120">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="250d2-121">外部 DNS 和公共 CA（即，在 FQDN 必须分配给证书中的 SN 时）通常不支持在 FQDN 中使用非标准字符。</span><span class="sxs-lookup"><span data-stu-id="250d2-121">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (that is, when the FQDN must be assigned to the SN in the certificate).</span></span>



<span data-ttu-id="250d2-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="250d2-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

