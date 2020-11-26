---
title: Lync Server 2013 证书基础结构要求
description: Lync Server 2013 证书基础结构要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure requirements
ms:assetid: 0051aa23-0bbe-4e72-9f29-e01c6bcc6190
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398066(v=OCS.15)
ms:contentKeyID: 48183219
ms.date: 06/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02c7e69f272c29f0ba9386f403db326b4d39bbff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435409"
---
# <a name="certificate-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="a0526-103">Lync Server 2013 的证书基础结构要求</span><span class="sxs-lookup"><span data-stu-id="a0526-103">Certificate infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0526-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0526-104">

<span> </span></span></span>

<span data-ttu-id="a0526-105">_**主题上次修改时间：** 2016-06-23_</span><span class="sxs-lookup"><span data-stu-id="a0526-105">_**Topic Last Modified:** 2016-06-23_</span></span>

<span data-ttu-id="a0526-106">Lync Server 2013 需要 (PKI) 的公钥基础结构，以支持 TLS 和相互 TLS (MTLS) 连接。</span><span class="sxs-lookup"><span data-stu-id="a0526-106">Lync Server 2013 requires a public key infrastructure (PKI) to support TLS and mutual TLS (MTLS) connections.</span></span>

<span data-ttu-id="a0526-107">Lync 服务器出于以下目的使用证书：</span><span class="sxs-lookup"><span data-stu-id="a0526-107">Lync Server uses certificates for the following purposes:</span></span>

  - <span data-ttu-id="a0526-108">客户端和服务器之间的 TLS 连接</span><span class="sxs-lookup"><span data-stu-id="a0526-108">TLS connections between client and server</span></span>

  - <span data-ttu-id="a0526-109">服务器之间的 MTLS 连接</span><span class="sxs-lookup"><span data-stu-id="a0526-109">MTLS connections between servers</span></span>

  - <span data-ttu-id="a0526-110">使用自动发现伙伴 DNS 的联盟</span><span class="sxs-lookup"><span data-stu-id="a0526-110">Federation using automatic DNS discovery of partners</span></span>

  - <span data-ttu-id="a0526-111">远程用户访问即时消息 (IM)</span><span class="sxs-lookup"><span data-stu-id="a0526-111">Remote user access for instant messaging (IM)</span></span>

  - <span data-ttu-id="a0526-112">外部用户访问音频/视频 (A/V) 会话、应用程序共享和会议</span><span class="sxs-lookup"><span data-stu-id="a0526-112">External user access to audio/video (A/V) sessions, application sharing, and conferencing</span></span>

  - <span data-ttu-id="a0526-113">使用 Web 服务的自动发现的移动请求</span><span class="sxs-lookup"><span data-stu-id="a0526-113">Mobile requests using automatic discovery of Web Services</span></span>

<span data-ttu-id="a0526-114">对于 Lync Server，需要遵守以下常见要求：</span><span class="sxs-lookup"><span data-stu-id="a0526-114">For Lync Server, the following common requirements apply:</span></span>

  - <span data-ttu-id="a0526-115">所有服务器证书都必须支持服务器授权（服务器 EKU）。</span><span class="sxs-lookup"><span data-stu-id="a0526-115">All server certificates must support server authorization (Server EKU).</span></span>

  - <span data-ttu-id="a0526-116">所有服务器证书都必须包含一个 CRL 分发点 (CDP)。</span><span class="sxs-lookup"><span data-stu-id="a0526-116">All server certificates must contain a CRL Distribution Point (CDP).</span></span>

  - <span data-ttu-id="a0526-117">所有证书必须使用操作系统支持的签名算法进行签名。</span><span class="sxs-lookup"><span data-stu-id="a0526-117">All certificates must be signed using a signing algorithm supported by the operating system.</span></span> <span data-ttu-id="a0526-118">Lync Server 2013 支持 SHA-1 和 SHA-1 系列的摘要大小 (224、256、384和512位) ，满足或超过操作系统要求。</span><span class="sxs-lookup"><span data-stu-id="a0526-118">Lync Server 2013 supports the SHA-1 and SHA-2 suite of digest sizes (224, 256, 384 and 512-bit), and meets or exceeds the operating system requirements.</span></span> <span data-ttu-id="a0526-119">有关操作系统支持，请参阅 [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002) 。</span><span class="sxs-lookup"><span data-stu-id="a0526-119">For operating system support, see [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a0526-120">不支持使用 RSASSA-PSS 签名算法，否则可能导致登录错误、呼叫转接问题及其他问题。</span><span class="sxs-lookup"><span data-stu-id="a0526-120">Using the RSASSA-PSS signature algorithm is unsupported, and may lead to errors on login and call forwarding issues, among other problems.</span></span>

    
    </div>

  - <span data-ttu-id="a0526-121">对于运行 Lync Server 的内部服务器，自动注册受支持。</span><span class="sxs-lookup"><span data-stu-id="a0526-121">Auto-enrollment is supported for internal servers running Lync Server.</span></span>

  - <span data-ttu-id="a0526-122">Lync Server Edge 服务器不支持自动注册。</span><span class="sxs-lookup"><span data-stu-id="a0526-122">Auto-enrollment is not supported for Lync Server Edge Servers.</span></span>

  - <span data-ttu-id="a0526-123">将基于 web 的证书请求提交到 Windows Server 2003 CA 时，必须从运行 Windows Server 2003 的计算机或 Windows XP 提交该证书请求。</span><span class="sxs-lookup"><span data-stu-id="a0526-123">When you submit a web-based certificate request to a Windows Server 2003 CA, you must submit it from a computer running either Windows Server 2003 with SP2 or Windows XP.</span></span>
    
    <span data-ttu-id="a0526-124">请注意，虽然 KB922706 提供了对针对 Windows Server 2003 证书服务 web 注册注册 web 证书的问题的支持，但它不能使用 Windows Server 2008、Windows Vista 或 Windows 7 从 Windows Server 2003 CA 申请证书。</span><span class="sxs-lookup"><span data-stu-id="a0526-124">Note that although KB922706 provides support for resolving issues with enrolling web certificates against a Windows Server 2003 Certificate Services web enrollment, it does not make it possible to use Windows Server 2008, Windows Vista, or Windows 7 to request a certificate from a Windows Server 2003 CA.</span></span>

  - <span data-ttu-id="a0526-125">加密密钥长度为 1024、2048 和 4096。</span><span class="sxs-lookup"><span data-stu-id="a0526-125">Encryption key lengths of 1024, 2048, and 4096 are supported.</span></span> <span data-ttu-id="a0526-126">建议使用密钥长度 2048 和更大值。</span><span class="sxs-lookup"><span data-stu-id="a0526-126">Key lengths of 2048 and greater are recommended.</span></span>

  - <span data-ttu-id="a0526-127">默认的摘要式或哈希签名算法是 RSA。</span><span class="sxs-lookup"><span data-stu-id="a0526-127">The default digest, or hash signing, algorithm is RSA.</span></span> <span data-ttu-id="a0526-128">\_还支持 ecdh P256、ecdh \_ P384 和 ecdh \_ P521 算法。</span><span class="sxs-lookup"><span data-stu-id="a0526-128">The ECDH\_P256, ECDH\_P384, and ECDH\_P521 algorithms are also supported.</span></span> 

<div>

## <a name="in-this-section"></a><span data-ttu-id="a0526-129">本节内容</span><span class="sxs-lookup"><span data-stu-id="a0526-129">In This Section</span></span>

  - [<span data-ttu-id="a0526-130">Lync Server 2013 中内部服务器的证书要求</span><span class="sxs-lookup"><span data-stu-id="a0526-130">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="a0526-131">Lync Server 2013 中外部用户访问的证书要求</span><span class="sxs-lookup"><span data-stu-id="a0526-131">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="a0526-132">Lync Server 2013 中持久聊天服务器的证书要求</span><span class="sxs-lookup"><span data-stu-id="a0526-132">Certificate requirements for Persistent Chat server in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="a0526-133">Lync Server 2013 中移动的证书要求</span><span class="sxs-lookup"><span data-stu-id="a0526-133">Certificate requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-mobility.md)

<span data-ttu-id="a0526-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0526-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

