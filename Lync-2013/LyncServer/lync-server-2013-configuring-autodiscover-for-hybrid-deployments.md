---
title: Lync Server 2013：配置混合部署的自动发现
description: Lync Server 2013：配置混合部署的自动发现。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Autodiscover for hybrid deployments
ms:assetid: ca605e62-181c-42ca-80a1-e37e610f8277
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945653(v=OCS.15)
ms:contentKeyID: 51541521
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e6797e3f6b77e3016f6cef87f2a930f5a7c1fce6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433302"
---
# <a name="configuring-autodiscover-in-lync-server-2013-for-hybrid-deployments"></a><span data-ttu-id="58b97-103">在 Lync Server 2013 中为混合部署配置自动发现</span><span class="sxs-lookup"><span data-stu-id="58b97-103">Configuring Autodiscover in Lync Server 2013 for hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58b97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58b97-104">

<span> </span></span></span>

<span data-ttu-id="58b97-105">_**主题上次修改时间：** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="58b97-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="58b97-106">混合部署是使用 Microsoft Lync Online 云服务和本地部署的配置。</span><span class="sxs-lookup"><span data-stu-id="58b97-106">Hybrid Deployments are configurations that use both the Microsoft Lync Online cloud service and the on premises deployment.</span></span> <span data-ttu-id="58b97-107">在此类型的配置中，自动发现服务必须能够找到用户实际所在的位置。</span><span class="sxs-lookup"><span data-stu-id="58b97-107">In this type of configuration, the Autodiscover service must be able to locate where the user is actually located.</span></span> <span data-ttu-id="58b97-108">也就是说，"自动发现" 帮助查找用户帐户和托管用户帐户的服务器所在的位置，无论该帐户是在本地部署还是在 Lync Online 部署中。</span><span class="sxs-lookup"><span data-stu-id="58b97-108">That is to say, Autodiscover aids in finding the user account and where the server that hosts the user’s account is, regardless if it is in the on premises deployment or in the Lync Online deployment.</span></span>

<span data-ttu-id="58b97-109">例如，如果用户的帐户托管在 Lync Online 中的服务器上，则在称为 " *发现*" 的过程中，尝试查找用户的操作将如下所示：</span><span class="sxs-lookup"><span data-stu-id="58b97-109">For example, if a user’s account is hosted on a server in Lync Online, the attempt to locate the user will happen as follows, in a process known as *discoverability*:</span></span>

  - <span data-ttu-id="58b97-110">用户启动到本地部署的连接尝试 **contoso.com**。</span><span class="sxs-lookup"><span data-stu-id="58b97-110">User initiates a connection attempt to the on premises deployment, **contoso.com**.</span></span>

  - <span data-ttu-id="58b97-111">该尝试将发送到 lyncdiscover.contoso.com，它是与自动发现服务关联的 DNS 名称。</span><span class="sxs-lookup"><span data-stu-id="58b97-111">The attempt is sent to lyncdiscover.contoso.com, the DNS name associated with the Autodiscover service.</span></span>

  - <span data-ttu-id="58b97-112">自动发现指在 contoso.com 本地部署中假定的注册机构池，并提供有关用户在 Lync Online 中托管的实际主服务器的信息。</span><span class="sxs-lookup"><span data-stu-id="58b97-112">Autodiscover refers to the assumed registrar pool at the contoso.com on premises deployment and is given information on the user’s actual home server hosted in Lync Online.</span></span> <span data-ttu-id="58b97-113">然后，自动发现将向用户发送 **lync.com** 联机自动发现服务的引用。</span><span class="sxs-lookup"><span data-stu-id="58b97-113">Autodiscover then sends the user a referral to the **lync.com** online Autodiscover service.</span></span>

  - <span data-ttu-id="58b97-114">用户启动到 lync.com online 自动发现服务的连接尝试，并且能够找到用户的帐户和用户的主服务器。</span><span class="sxs-lookup"><span data-stu-id="58b97-114">The user initiates a connection attempt to the lync.com online Autodiscover service and is able to locate the user’s account and the user’s home server.</span></span>

<span data-ttu-id="58b97-115">若要使客户能够发现用户主服务器所在的部署，你必须使用新的统一资源定位器（ (URL) ）配置自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="58b97-115">To enable clients to discover the deployment where the user home server is located, you must configure the Autodiscover service with a new uniform resource locator (URL).</span></span> <span data-ttu-id="58b97-116">执行以下操作以配置自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="58b97-116">Do the following to configure the Autodiscover service.</span></span>

<div>

## <a name="configuring-autodiscover-for-hybrid-deployments"></a><span data-ttu-id="58b97-117">配置混合部署的自动发现</span><span class="sxs-lookup"><span data-stu-id="58b97-117">Configuring Autodiscover for Hybrid Deployments</span></span>

1.  <span data-ttu-id="58b97-118">在本主题中， [针对 Lync Server 2013 的自动发现服务要求](lync-server-2013-autodiscover-service-requirements.md)使用 Get-CsHostingProvider 检索 ProxyFQDN 属性的值。</span><span class="sxs-lookup"><span data-stu-id="58b97-118">In the topic, [Autodiscover service requirements for Lync Server 2013](lync-server-2013-autodiscover-service-requirements.md), you use Get-CsHostingProvider to retrieve the value of the attribute ProxyFQDN.</span></span>

2.  <span data-ttu-id="58b97-119">从 Lync Server 命令行管理程序中，键入</span><span class="sxs-lookup"><span data-stu-id="58b97-119">From the Lync Server Management Shell, type</span></span>
    
        Set-CsHostingProvider -Identity [identity] -AutodiscoverUrl https://webdir.online.lync.com/autodiscover/autodisccoverservice.svc/root
    
    <span data-ttu-id="58b97-120">其中 \[ 标识 \] 替换为共享 SIP 地址空间的域名。</span><span class="sxs-lookup"><span data-stu-id="58b97-120">Where \[identity\] is replaced with the domain name of the shared SIP address space.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="58b97-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58b97-121">See Also</span></span>


[<span data-ttu-id="58b97-122">CsHostingProvider</span><span class="sxs-lookup"><span data-stu-id="58b97-122">Get-CsHostingProvider</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostingProvider)  
[<span data-ttu-id="58b97-123">Set-CsHostingProvider</span><span class="sxs-lookup"><span data-stu-id="58b97-123">Set-CsHostingProvider</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostingProvider)  
  

<span data-ttu-id="58b97-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58b97-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

