---
title: Lync Server 2013：自动客户端登录的 DNS 要求
description: Lync Server 2013：自动客户端登录的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for automatic client sign-in
ms:assetid: 3bcd4bb3-a022-4ffa-b005-1a95ad2b1796
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425884(v=OCS.15)
ms:contentKeyID: 48183873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2247c955e0a563a22fb5d0ec20735291a836cdfc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392351"
---
# <a name="dns-requirements-for-automatic-client-sign-in-in-lync-server-2013"></a><span data-ttu-id="ed263-103">Lync Server 2013 中自动客户端登录的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="ed263-103">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ed263-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ed263-104">

<span> </span></span></span>

<span data-ttu-id="ed263-105">_**主题上次修改时间：** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="ed263-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="ed263-106">本部分介绍了域名系统 (了自动客户端登录所需的 DNS) 记录。</span><span class="sxs-lookup"><span data-stu-id="ed263-106">This section explains the Domain Name System (DNS) records that are required for automatic client sign-in.</span></span> <span data-ttu-id="ed263-107">部署标准版服务器或前端池时，可以将客户端配置为使用自动发现登录到相应的标准版服务器或前端池。</span><span class="sxs-lookup"><span data-stu-id="ed263-107">When you deploy your Standard Edition servers or Front End pools, you can configure your clients to use automatic discovery to sign in to the appropriate Standard Edition server or Front End pool.</span></span> <span data-ttu-id="ed263-108">如果您计划要求客户手动连接到 Lync Server 2013，则可以跳过本主题。</span><span class="sxs-lookup"><span data-stu-id="ed263-108">If you plan to require your clients to connect manually to Lync Server 2013, you can skip this topic.</span></span>

<span data-ttu-id="ed263-109">若要支持自动客户端登录，必须：</span><span class="sxs-lookup"><span data-stu-id="ed263-109">To support automatic client sign-in, you must:</span></span>

  - <span data-ttu-id="ed263-110">指定单个服务器或池以分发和验证客户端登录请求。</span><span class="sxs-lookup"><span data-stu-id="ed263-110">Designate a single server or pool to distribute and authenticate client sign-in requests.</span></span> <span data-ttu-id="ed263-111">这可以是组织中托管用户的现有服务器或池，也可以指定专用服务器或池用于托管无用户的此用途。</span><span class="sxs-lookup"><span data-stu-id="ed263-111">This can be an existing server or pool in your organization that hosts users, or you can designate a dedicated server or pool for this purpose that hosts no users.</span></span> <span data-ttu-id="ed263-112">为了获得高可用性，建议你为此函数指定一个前端池。</span><span class="sxs-lookup"><span data-stu-id="ed263-112">For high availability, we recommend that you designate a Front End pool for this function.</span></span>

  - <span data-ttu-id="ed263-113">创建内部 DNS SRV 记录以支持此服务器或池的自动客户端登录。</span><span class="sxs-lookup"><span data-stu-id="ed263-113">Create an internal DNS SRV record to support automatic client sign-in for this server or pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ed263-114">在以下记录要求中，SIP 域指的是分配给用户的 SIP Uri 的主机部分。</span><span class="sxs-lookup"><span data-stu-id="ed263-114">In the following record requirements, SIP domain refers to the host portion of the SIP URIs assigned to users.</span></span> <span data-ttu-id="ed263-115">例如，如果 SIP Uri 的形式是 \* @contoso，则 contoso.com 是 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="ed263-115">For example, if SIP URIs are of the form \*@contoso.com, contoso.com is the SIP domain.</span></span> <span data-ttu-id="ed263-116">SIP 域通常与内部 Active Directory 域不同。</span><span class="sxs-lookup"><span data-stu-id="ed263-116">The SIP domain is often different from the internal Active Directory domain.</span></span> <span data-ttu-id="ed263-117">组织还可以支持多个 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="ed263-117">An organization can also support multiple SIP domains.</span></span>

    
    </div>

<span data-ttu-id="ed263-118">若要为你的客户端启用自动配置，你必须创建内部 DNS SRV 记录，将以下记录之一映射到由 Lync 客户端分发登录请求的前端池或标准版服务器的完全限定的域名 (FQDN) ：</span><span class="sxs-lookup"><span data-stu-id="ed263-118">To enable automatic configuration for your clients, you must create an internal DNS SRV record that maps one of the following records to the fully qualified domain name (FQDN) of the Front End pool or Standard Edition server that distributes sign-in requests from Lync clients:</span></span>

  - <span data-ttu-id="ed263-119">\_sipinternaltls。 \_tcp-out.\<domain\></span><span class="sxs-lookup"><span data-stu-id="ed263-119">\_sipinternaltls.\_tcp.\<domain\></span></span> <span data-ttu-id="ed263-120">-用于内部 TLS 连接</span><span class="sxs-lookup"><span data-stu-id="ed263-120">- for internal TLS connections</span></span>

<span data-ttu-id="ed263-121">你只需要为前端池或标准版服务器创建单个 SRV 记录，或者将分发登录请求。</span><span class="sxs-lookup"><span data-stu-id="ed263-121">You only need to create a single SRV record for the Front End pool or Standard Edition server or that will distribute sign-in requests.</span></span>

<span data-ttu-id="ed263-122">下表显示了虚构公司 Contoso 所需的一些示例记录，它支持 contoso.com 和 retail.contoso.com 的 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="ed263-122">The following table shows some example records required for the fictitious company Contoso, which supports SIP domains of contoso.com and retail.contoso.com.</span></span>

### <a name="example-of-dns-records-required-for-automatic-client-sign-in-with-multiple-sip-domains"></a><span data-ttu-id="ed263-123">自动客户端登录多个 SIP 域所需的 DNS 记录示例</span><span class="sxs-lookup"><span data-stu-id="ed263-123">Example of DNS Records Required for Automatic Client Sign-in with Multiple SIP Domains</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed263-124">用于分发登录请求的前端池的 FQDN</span><span class="sxs-lookup"><span data-stu-id="ed263-124">FQDN of Front End pool used to distribute sign-in requests</span></span></th>
<th><span data-ttu-id="ed263-125">SIP 域</span><span class="sxs-lookup"><span data-stu-id="ed263-125">SIP domain</span></span></th>
<th><span data-ttu-id="ed263-126">DNS SRV 记录</span><span class="sxs-lookup"><span data-stu-id="ed263-126">DNS SRV record</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed263-127">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ed263-127">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ed263-128">contoso.com</span><span class="sxs-lookup"><span data-stu-id="ed263-128">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ed263-129">通过端口5061映射到 pool01.contoso.com 的 _sipinternaltls 域的 SRV 记录。 _tcp</span><span class="sxs-lookup"><span data-stu-id="ed263-129">An SRV record for _sipinternaltls._tcp.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed263-130">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ed263-130">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ed263-131">retail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ed263-131">retail.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="ed263-132">将 _sipinternaltls 映射到 pool01.contoso.com 的端口5061上的 _tcp 的 SRV 域的 SRV 记录</span><span class="sxs-lookup"><span data-stu-id="ed263-132">An SRV record for _sipinternaltls._tcp.retail.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="ed263-133">默认情况下，DNS 记录的查询将遵循用户名和 SRV 记录中的域之间的严格域名匹配。</span><span class="sxs-lookup"><span data-stu-id="ed263-133">By default, queries for DNS records adhere to strict domain name matching between the domain in the user name and the SRV record.</span></span> <span data-ttu-id="ed263-134">如果你希望客户端 DNS 查询改为使用后缀匹配，则可以配置 DisableStrictDNSNaming 组策略。</span><span class="sxs-lookup"><span data-stu-id="ed263-134">If you prefer that client DNS queries use suffix matching instead, you can configure the DisableStrictDNSNaming Group Policy.</span></span> <span data-ttu-id="ed263-135">有关详细信息，请参阅规划文档中的 <A href="lync-server-2013-planning-for-clients-and-devices.md">Lync Server 2013 中的客户端和设备规划</A> 。</span><span class="sxs-lookup"><span data-stu-id="ed263-135">For details, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="example-of-the-certificates-and-dns-records-required-for-automatic-client-sign-in"></a><span data-ttu-id="ed263-136">自动客户端所需的证书和 DNS 记录示例 Sign-In</span><span class="sxs-lookup"><span data-stu-id="ed263-136">Example of the Certificates and DNS Records Required for Automatic Client Sign-In</span></span>

<span data-ttu-id="ed263-137">此示例使用上表中的相同示例名称。</span><span class="sxs-lookup"><span data-stu-id="ed263-137">This example uses the same example names in the preceding table.</span></span> <span data-ttu-id="ed263-138">Contoso 组织支持 contoso.com 和 retail.contoso.com 的 SIP 域，并且其所有用户都具有以下形式之一的 SIP URI：</span><span class="sxs-lookup"><span data-stu-id="ed263-138">The Contoso organization supports the SIP domains of contoso.com and retail.contoso.com, and all of its users have a SIP URI in one of the following forms:</span></span>

  - <span data-ttu-id="ed263-139">\<user\>@retail contoso.com</span><span class="sxs-lookup"><span data-stu-id="ed263-139">\<user\>@retail.contoso.com</span></span>

  - <span data-ttu-id="ed263-140">\<user\>@contoso .com</span><span class="sxs-lookup"><span data-stu-id="ed263-140">\<user\>@contoso.com</span></span>

<span data-ttu-id="ed263-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ed263-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

