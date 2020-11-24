---
title: Lync Server 2013：会议的基于位置的路由的配置
description: Lync Server 2013：为会议 Location-Based 路由的配置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392418"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="e2a02-103">Lync Server 2013 中会议的基于位置的路由的配置</span><span class="sxs-lookup"><span data-stu-id="e2a02-103">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2a02-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2a02-104">

<span> </span></span></span>

<span data-ttu-id="e2a02-105">_**主题上次修改时间：** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="e2a02-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="e2a02-106">Location-Based 路由会议应用程序依赖于 Lync Server 2013 的配置 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="e2a02-106">The Location-Based Routing Conferencing application relies on the configuration of Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="e2a02-107">主要配置如下：</span><span class="sxs-lookup"><span data-stu-id="e2a02-107">The main configurations are the following:</span></span>

  - <span data-ttu-id="e2a02-108">加入会议的参与者的位置基于其网络站点进行确定。</span><span class="sxs-lookup"><span data-stu-id="e2a02-108">The location of participants joining a meeting is determined based on their network site.</span></span> <span data-ttu-id="e2a02-109">必须在 Lync Server 中定义网络网站及其关联的网络子网，才能强制 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="e2a02-109">A network site and its associated network subnets must be defined in Lync Server in order to enforce Location-Based Routing.</span></span>

  - <span data-ttu-id="e2a02-110">若要强制 Location-Based 路由会议，必须为 Lync 参与者启用 Location-Based 路由。</span><span class="sxs-lookup"><span data-stu-id="e2a02-110">To enforce Location-Based Routing of meetings, Lync participants must be enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="e2a02-111">若要强制 Location-Based 路由 PSTN 终结点加入会议，必须为 Location-Based 路由配置用于连接 PSTN 终结点的 SIP 中继。</span><span class="sxs-lookup"><span data-stu-id="e2a02-111">To enforce Location-Based Routing of PSTN endpoints joining meetings, the SIP trunk used to connect the PSTN endpoints must be configured for Location-Based Routing.</span></span>

<span data-ttu-id="e2a02-112">有关部署和配置 Lync Server 2013 Location-Based 路由的其他信息，请参阅配置 [基于位置的路由](lync-server-2013-configuring-location-based-routing.md)。</span><span class="sxs-lookup"><span data-stu-id="e2a02-112">For additional information on deploying and configuring Lync Server 2013 Location-Based Routing, please refer Configuring [Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a><span data-ttu-id="e2a02-113">启用 Location-Based 路由会议应用程序</span><span class="sxs-lookup"><span data-stu-id="e2a02-113">Enabling the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="e2a02-114">默认情况下，Location-Based "路由会议" 应用程序处于禁用状态。</span><span class="sxs-lookup"><span data-stu-id="e2a02-114">The Location-Based Routing Conferencing application is disabled by default.</span></span> <span data-ttu-id="e2a02-115">在启用此应用程序之前，您需要确定要为该应用程序分配的适当优先级。</span><span class="sxs-lookup"><span data-stu-id="e2a02-115">Before enabling this application, you need to determine the right priority to assign for the application.</span></span> <span data-ttu-id="e2a02-116">若要确定此优先级，请在 Lync Server 命令行管理程序中运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e2a02-116">To determine this priority, run the following cmdlet in Lync Server Management Shell:</span></span>

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

<span data-ttu-id="e2a02-117">在此 cmdlet 中， \<Pool FQDN\> 是要启用 Location-Based 路由会议应用程序的池。</span><span class="sxs-lookup"><span data-stu-id="e2a02-117">In this cmdlet, \<Pool FQDN\> is the pool in which the Location-Based Routing Conferencing application is to be enabled.</span></span>

<span data-ttu-id="e2a02-118">此 cmdlet 将返回由 Lync Server 托管的应用程序的列表及其每个应用程序的优先级值。</span><span class="sxs-lookup"><span data-stu-id="e2a02-118">This cmdlet will return the list of the applications hosted by Lync Server and the priority value for each of them.</span></span> <span data-ttu-id="e2a02-119">需要为 Location-Based 路由会议应用程序分配比 "UdcAgent" 应用程序更大的优先级值，并小于 "DefaultRouting"、"ExumRouting" 和 "OutboundRouting" 应用程序。</span><span class="sxs-lookup"><span data-stu-id="e2a02-119">The Location-Based Routing Conferencing application needs to be assigned a priority value larger than the “UdcAgent” application and smaller than the “DefaultRouting”, “ExumRouting” and “OutboundRouting” applications.</span></span> <span data-ttu-id="e2a02-120">我们建议你为 Location-Based 路由会议应用程序分配一个比 "UdcAgent" 应用程序优先级值更高的优先级值。</span><span class="sxs-lookup"><span data-stu-id="e2a02-120">We recommend that you assign the Location-Based Routing Conferencing application a priority value that is one point higher than the priority value of the “UdcAgent” application.</span></span>

<span data-ttu-id="e2a02-121">例如，如果 "UdcAgent" 应用程序的优先级值为 "2"，"DefaultRouting" 应用程序的优先级值为 "8"，"ExumRouting" 应用程序的优先级值为 "9"，"OutboundRouting" 应用程序的优先级值为 "10"，则你应该为 Location-Based 路由会议应用程序分配优先级值 "3"。</span><span class="sxs-lookup"><span data-stu-id="e2a02-121">For example, if the “UdcAgent” application has a priority value of “2”, the “DefaultRouting” application has a priority value of “8”, the “ExumRouting” application has a priority value of “9” and the “OutboundRouting” application has a priority value of “10” then you should assign the Location-Based Routing Conferencing application a priority value of “3”.</span></span> <span data-ttu-id="e2a02-122">这样做将按以下顺序设定应用程序的优先级：其他应用程序（优先级：0 到 1）、“UdcAgent”（优先级：2）、基于位置的路由会议应用程序（优先级：3）、其他应用程序（优先级：4 到 8）、“DefaultRouting”（优先级：9）、“ExumRouting”（优先级：10）和“OutboundRouting”（优先级：11）。</span><span class="sxs-lookup"><span data-stu-id="e2a02-122">Doing so would place the priority of the applications in the following order: Other applications (Priorities: 0 to 1), “UdcAgent” (Priority: 2), Location-Based Routing Conferencing application (Priority: 3), other applications (Priorities: 4 to 8), “DefaultRouting” (Priority: 9), “ExumRouting” (Priority: 10) and “OutboundRouting” (Priority: 11).</span></span>

<span data-ttu-id="e2a02-123">找到 Location-Based 路由会议应用程序的正确优先级值后，为每个 Front-End 池或标准版服务器键入以下 cmdlet，以便为 Location-Based 路由启用的家庭用户：</span><span class="sxs-lookup"><span data-stu-id="e2a02-123">After you find the correct priority value for the Location-Based Routing Conferencing application, type the following cmdlet for each Front-End pool or Standard Edition Server that homes users enabled for Location-Based Routing:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="e2a02-124">例如：</span><span class="sxs-lookup"><span data-stu-id="e2a02-124">For example:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="e2a02-125">使用此 cmdlet 后，重启池中的所有前端服务器或 Location-Based 路由会议应用程序已启用的标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="e2a02-125">After using this cmdlet, restart all Front End servers in the pool or the Standard Edition Servers where the Location-Based Routing Conferencing application has been enabled.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e2a02-126">Location-Based 路由 enforcements 到会议或咨询式传输，直到适用的池中的所有前端服务器或标准版服务器重新启动后才会强制执行。</span><span class="sxs-lookup"><span data-stu-id="e2a02-126">Location-Based Routing enforcements to conferences or consultative transfers won’t be enforced until all the Front End Servers in the applicable pools or the Standard Edition Servers are restarted.</span></span>



</div>

<span data-ttu-id="e2a02-127">一旦已成功启用 Location-Based 路由会议应用程序并重新启动所有适用的 Lync 服务器，将监视所有已启用了 Location-Based 路由的 Lync 用户组织的会议，以防止 PSTN 免绕过</span><span class="sxs-lookup"><span data-stu-id="e2a02-127">Once the Location-Based Routing Conferencing application has been successfully enabled and all applicable Lync servers have been restarted, all conferences organized by Lync users enabled for Location-Based Routing will be monitored to prevent PSTN toll bypass</span></span>

<span data-ttu-id="e2a02-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2a02-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

