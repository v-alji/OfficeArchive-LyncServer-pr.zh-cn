---
title: Lync Server 2013：反向代理的配置要求
description: Lync Server 2013：反向代理的配置要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration requirements for reverse proxy
ms:assetid: c37d688a-28e4-4822-80cc-6add59c71052
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945651(v=OCS.15)
ms:contentKeyID: 51541518
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75f3f5b9437ba4518e3feffc193853b446b702d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392417"
---
# <a name="configuration-requirements-for-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="fdafe-103">Lync Server 2013 中反向代理的配置要求</span><span class="sxs-lookup"><span data-stu-id="fdafe-103">Configuration requirements for reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fdafe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fdafe-104">

<span> </span></span></span>

<span data-ttu-id="fdafe-105">_**主题上次修改时间：** 2013-03-05_</span><span class="sxs-lookup"><span data-stu-id="fdafe-105">_**Topic Last Modified:** 2013-03-05_</span></span>

<span data-ttu-id="fdafe-106">Lync Server 2013 对来自外部客户端的通信的一些要求，这些要求随后传递到托管在 Director、Director 池、前端服务器或前端池上的外部 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="fdafe-106">Lync Server 2013 imposes a few requirements on communications from the external client that are then passed on to the external Web services hosted on the Director, Director pool, Front End Server or Front End pool.</span></span> <span data-ttu-id="fdafe-107">如果你向用户提供会议，则反向代理还负责发布 Office Web Apps 服务器。</span><span class="sxs-lookup"><span data-stu-id="fdafe-107">The reverse proxy is also responsible for publishing the Office Web Apps Server, if you are offering conferencing to your users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fdafe-108">Lync Server 2013 不指定必须使用的特定反向代理。</span><span class="sxs-lookup"><span data-stu-id="fdafe-108">Lync Server 2013 does not specify a particular reverse proxy that you must use.</span></span> <span data-ttu-id="fdafe-109">Lync Server 2013 仅定义反向代理必须能够执行的操作要求。</span><span class="sxs-lookup"><span data-stu-id="fdafe-109">Lync Server 2013 only defines operational requirements that the reverse proxy must be able to do.</span></span> <span data-ttu-id="fdafe-110">通常，你的基础结构中已部署的反向代理可能能够满足这些要求。</span><span class="sxs-lookup"><span data-stu-id="fdafe-110">Typically, the reverse proxy that you already have deployed in your infrastructure may be able to meet the requirements.</span></span>



</div>

<div>

## <a name="reverse-proxy-requirements"></a><span data-ttu-id="fdafe-111">反向代理要求</span><span class="sxs-lookup"><span data-stu-id="fdafe-111">Reverse Proxy Requirements</span></span>

<span data-ttu-id="fdafe-112">Lync Server 2013 预期执行反向代理的功能操作是：</span><span class="sxs-lookup"><span data-stu-id="fdafe-112">The functional operations that Lync Server 2013 expect a reverse proxy to perform are:</span></span>

  - <span data-ttu-id="fdafe-113">使用安全套接字层 (SSL) 和传输层安全 (TLS) 通过使用从公共证书颁发机构获取的证书连接到 Director、Director pool、前端服务器或前端服务器或前端池的已发布的外部 Web 服务来实现。</span><span class="sxs-lookup"><span data-stu-id="fdafe-113">Use secure socket layer (SSL) and transport layer security (TLS) implemented by using certificates acquired from a public certification authority to connect to the published external Web services of the Director, Director pool, Front End Server or Front End pool.</span></span> <span data-ttu-id="fdafe-114">控制器和前端服务器可以使用硬件负载平衡器在负载平衡的池中。</span><span class="sxs-lookup"><span data-stu-id="fdafe-114">The Director and the Front End Server can be in a load-balanced pool by using hardware load balancers.</span></span>

  - <span data-ttu-id="fdafe-115">可以使用证书进行加密来发布内部网站，或通过未加密的方式发布它们（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="fdafe-115">Able to publish internal Web sites using certificates for encryption, or publish them over an unencrypted means, if needed.</span></span>

  - <span data-ttu-id="fdafe-116">可以通过使用完全限定的域名 (FQDN) 来在外部发布内部托管的网站。</span><span class="sxs-lookup"><span data-stu-id="fdafe-116">Able to publish an internally hosted web site externally by using a fully qualified domain name (FQDN).</span></span>

  - <span data-ttu-id="fdafe-117">能够发布托管网站的所有内容。</span><span class="sxs-lookup"><span data-stu-id="fdafe-117">Able to publish all contents of the hosted web site.</span></span> <span data-ttu-id="fdafe-118">默认情况下，你可以使用 **/ \* *_ 指令，大多数 web 服务器将其识别为表示 "发布 web 服务器上的所有内容"。您也可以修改指令（例如，_*/Uwca/ \***，这意味着 "在虚拟目录 Ucwa 下发布所有内容"。）</span><span class="sxs-lookup"><span data-stu-id="fdafe-118">By default, you can use the **/\**_ directive, which is recognized by most web servers to mean "Publish all content on the web server." You can also modify the directive—for example, _*/Uwca/\***, which means "Publish all content under the virtual directory Ucwa."</span></span>

  - <span data-ttu-id="fdafe-119">必须可配置为需要安全套接字层 (SSL) 和/或传输层安全 (TLS) 与从发布的网站请求内容的客户端连接。</span><span class="sxs-lookup"><span data-stu-id="fdafe-119">Must be configurable to require Secure Sockets Layer (SSL) and/or Transport Layer Security (TLS) connections with clients that request content from a published website.</span></span>

  - <span data-ttu-id="fdafe-120">必须接受 (SAN) 条目的使用者备用名称的证书。</span><span class="sxs-lookup"><span data-stu-id="fdafe-120">Must accept certificates with subject alternative name (SAN) entries.</span></span>

  - <span data-ttu-id="fdafe-121">必须能够允许将证书绑定到侦听器或接口，外部 web 服务 FQDN 将解析该侦听器。</span><span class="sxs-lookup"><span data-stu-id="fdafe-121">Must be able to allow binding of a certificate to a listener or interface through which the external web services FQDN will resolve.</span></span> <span data-ttu-id="fdafe-122">侦听器配置优于接口配置。</span><span class="sxs-lookup"><span data-stu-id="fdafe-122">Listener configurations are preferable to interfaces.</span></span> <span data-ttu-id="fdafe-123">可在一个接口上配置多个侦听器。</span><span class="sxs-lookup"><span data-stu-id="fdafe-123">Many listeners can be configured on a single interface.</span></span>

  - <span data-ttu-id="fdafe-124">必须允许进行主机头处理的配置。</span><span class="sxs-lookup"><span data-stu-id="fdafe-124">Must allow for the configuration of host header handling.</span></span> <span data-ttu-id="fdafe-125">通常，发出请求的客户端发送的原始主机标头必须透明地传递，而不是由反向代理进行修改。</span><span class="sxs-lookup"><span data-stu-id="fdafe-125">Often, the original host header sent by the requesting client must be passed transparently, instead of being modified by the reverse proxy.</span></span>

  - <span data-ttu-id="fdafe-126">从一个外部定义的端口桥接 SSL 和 TLS 流量 (例如，TCP 443) 另一个已定义的端口 (例如，TCP 4443) 。</span><span class="sxs-lookup"><span data-stu-id="fdafe-126">Bridging of SSL and TLS traffic from one externally defined port (for example, TCP 443) to another defined port (for example, TCP 4443).</span></span> <span data-ttu-id="fdafe-127">反向代理可能会在接收时解密数据包，然后在发送时 reencrypt 数据包。</span><span class="sxs-lookup"><span data-stu-id="fdafe-127">The reverse proxy may decrypt the packet on receipt and then reencrypt the packet on sending.</span></span>

  - <span data-ttu-id="fdafe-128">将未加密 TCP 流量从一个端口桥接 (例如，TCP 80) 另一个 (例如，TCP 8080) 。</span><span class="sxs-lookup"><span data-stu-id="fdafe-128">Bridging of unencrypted TCP traffic from one port (for example, TCP 80) to another (for example, TCP 8080).</span></span>

  - <span data-ttu-id="fdafe-129">允许配置或接受 NTLM 身份验证，无身份验证和传递身份验证。</span><span class="sxs-lookup"><span data-stu-id="fdafe-129">Allow configuration of, or accept, NTLM authentication, No authentication and Pass-through authentication.</span></span>

<span data-ttu-id="fdafe-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fdafe-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

