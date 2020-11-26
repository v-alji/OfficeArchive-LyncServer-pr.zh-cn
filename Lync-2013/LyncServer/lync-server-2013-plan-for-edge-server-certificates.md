---
title: Lync Server 2013：规划边缘服务器证书
description: Lync Server 2013：规划边缘服务器证书。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Plan for Edge Server certificates
ms:assetid: f1dfe220-2398-4ac8-ba4c-206c8c0cbc50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413010(v=OCS.15)
ms:contentKeyID: 48185798
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22ec3743256fe3e4c55dba0f6357a85b1ad81cd0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437128"
---
# <a name="plan-for-edge-server-certificates-in-lync-server-2013"></a><span data-ttu-id="db858-103">在 Lync Server 2013 中规划边缘服务器证书</span><span class="sxs-lookup"><span data-stu-id="db858-103">Plan for Edge Server certificates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db858-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db858-104">

<span> </span></span></span>

<span data-ttu-id="db858-105">_**主题上次修改时间：** 2012-11-05_</span><span class="sxs-lookup"><span data-stu-id="db858-105">_**Topic Last Modified:** 2012-11-05_</span></span>

<span data-ttu-id="db858-106">在 Lync Server 2013 中简化了为 Edge 创建证书。</span><span class="sxs-lookup"><span data-stu-id="db858-106">Certificate creation for Edge is simplified in Lync Server 2013.</span></span>

<span data-ttu-id="db858-107">**边缘服务器的流程图**</span><span class="sxs-lookup"><span data-stu-id="db858-107">**Certificates Flow Chart for Edge Server**</span></span>

<span data-ttu-id="db858-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span><span class="sxs-lookup"><span data-stu-id="db858-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span></span>

<span data-ttu-id="db858-109">创建单个公共证书，确保你具有为证书定义的可导出私钥，并使用证书向导将其分配给以下 Edge 服务器外部接口：</span><span class="sxs-lookup"><span data-stu-id="db858-109">Create a single public certificate, ensure that you have an exportable private key defined for the certificate, and assign it to the following Edge Server external interfaces using the certificate wizard:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="db858-110">Lync Server 不支持通配符证书，除非使用反向代理汇总简单的 Url。</span><span class="sxs-lookup"><span data-stu-id="db858-110">Wildcard certificates are not supported in Lync Server, except where used to summarize the Simple URLs through the reverse proxy.</span></span> <span data-ttu-id="db858-111">你必须为你的部署提供的每个 SIP 域名、Web 会议 Edge 服务、A/V 边缘服务和 XMPP 域定义不同的主题替换名称 (SANs) 。</span><span class="sxs-lookup"><span data-stu-id="db858-111">You must define distinct subject alternate names (SANs) for each SIP domain name, Web Conferencing Edge service, A/V Edge service and XMPP domain offered by your deployment.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="db858-112">在 Lync Server 2013 中引入，在当前证书过期时间之前暂存音频/视频身份验证证书需要额外的计划。</span><span class="sxs-lookup"><span data-stu-id="db858-112">Introduced in Lync Server 2013, staging Audio/Video Authentication certificates in advance of the expiration time of the current certificate requires some additional planning.</span></span> <span data-ttu-id="db858-113">对于外部边缘接口，而不是一个具有多个用途的证书，你将需要两个证书，一个证书分配给 "访问边缘服务" 和 "Web 会议边缘" 服务，另一个证书用于 A/V 边缘服务。</span><span class="sxs-lookup"><span data-stu-id="db858-113">Instead of one certificate with multiple purposes for the external Edge interface, you will require two certificates, one assigned to the Access Edge service and Web Conferencing Edge service, and one certificate for the A/V Edge service.</span></span> <span data-ttu-id="db858-114">有关其他详细信息，请参阅 <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">在 CsCertificate 中使用-滚在 Lync Server 2013 中暂存 AV 和 OAuth 证书</A></span><span class="sxs-lookup"><span data-stu-id="db858-114">For additional details, see <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</A></span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="db858-115">在边缘服务器池的事件中，将带有私钥的证书导出到每个边缘服务器，并将证书分配给每个 Edge 服务器服务。</span><span class="sxs-lookup"><span data-stu-id="db858-115">In the event of a pool of Edge Servers, you export the certificate with the private key to each Edge Server and assign the certificate to each Edge Server service.</span></span> <span data-ttu-id="db858-116">对内部边缘服务器证书执行相同操作，导出具有私钥的证书并分配给每个内部边缘接口。</span><span class="sxs-lookup"><span data-stu-id="db858-116">Do the same for the internal Edge Server certificate, exporting the certificate with the private key and assigning to each internal Edge interface.</span></span>



</div>

  - <span data-ttu-id="db858-117">确保为证书分配了可导出的私钥</span><span class="sxs-lookup"><span data-stu-id="db858-117">Ensure that you have an exportable private key assigned for the certificate</span></span>

  - <span data-ttu-id="db858-118">Access Edge 服务 (称为 "证书向导" 中的 " **外部 SIP 访问边缘** ") </span><span class="sxs-lookup"><span data-stu-id="db858-118">Access Edge service (referred to as **SIP Access Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="db858-119">网络会议边缘服务 (在证书向导中称为 " **网上会议边缘** ") </span><span class="sxs-lookup"><span data-stu-id="db858-119">Web Conferencing Edge service (referred to as **Web Conferencing Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="db858-120">A/V 身份验证服务 (在证书向导中称为 **a/v 边缘外部**) </span><span class="sxs-lookup"><span data-stu-id="db858-120">A/V Authentication service (referred to as **A/V Edge External** in the certificate wizard)</span></span>

<span data-ttu-id="db858-121">创建具有可导出私钥的单个内部证书，将其复制并分配给每个边缘服务器内部接口：</span><span class="sxs-lookup"><span data-stu-id="db858-121">Create a single internal certificate with exportable private key, copy and assign it to each of the Edge Server internal interfaces:</span></span>

  - <span data-ttu-id="db858-122">边缘服务器 (在证书向导中称为 " **边缘内部** ") </span><span class="sxs-lookup"><span data-stu-id="db858-122">Edge Server (referred to as **Edge Internal** in the certificate wizard)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="db858-123">可以为每个 Edge 服务器服务使用单独和不同的证书。</span><span class="sxs-lookup"><span data-stu-id="db858-123">It is possible to use separate and distinct certificates for each Edge Server service.</span></span> <span data-ttu-id="db858-124">选择单独的证书的一个好理由是您想要对 A/V 边缘服务证书使用新的滚动证书功能。</span><span class="sxs-lookup"><span data-stu-id="db858-124">A good reason to choose separate certificates is if you want to use the new rolling certificate feature for the A/V Edge service certificate.</span></span> <span data-ttu-id="db858-125">在此功能的情况下，建议将 A/V 边缘服务证书与 "访问边缘" 服务分离，并建议使用网络会议边缘服务。</span><span class="sxs-lookup"><span data-stu-id="db858-125">In the case of this feature, decoupling the A/V Edge service certificate from the Access Edge service and Web Conferencing Edge service is recommended.</span></span> <span data-ttu-id="db858-126">如果你选择请求、为每项服务获取和分配单独的证书，你必须请求为 A/V Edge 服务 (导出私钥，这实际上是 A/V 身份验证服务) 并将同一证书分配给每台边缘服务器上的 A/V 边缘外部接口。</span><span class="sxs-lookup"><span data-stu-id="db858-126">If you choose to request, acquire and assign separate certificates for each service, you must request that the private key be exportable for the A/V Edge service (again, this is in actuality the A/V Authentication service) and assign the same certificate to the A/V Edge External interface on each Edge Server.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="db858-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db858-127">See Also</span></span>


[<span data-ttu-id="db858-128">在 CsCertificate 中使用-滚在 Lync Server 2013 中暂存 AV 和 OAuth 证书</span><span class="sxs-lookup"><span data-stu-id="db858-128">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</span></span>](lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  


[<span data-ttu-id="db858-129">Lync Server 2013 中影响边缘服务器规划的更改</span><span class="sxs-lookup"><span data-stu-id="db858-129">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)  
  

<span data-ttu-id="db858-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db858-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

