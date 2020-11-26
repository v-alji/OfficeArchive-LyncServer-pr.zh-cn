---
title: Lync Server 2013：用于通讯簿管理的 Get-CsService
description: Lync Server 2013：用于通讯簿管理的 Get-CsService。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsService for Address Book management
ms:assetid: 373b717d-5efa-4c36-a899-a23a5bd922b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429698(v=OCS.15)
ms:contentKeyID: 48183853
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e46173429988d87022c13fab33e3778279dd0e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427983"
---
# <a name="get-csservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="9413b-103">Lync Server 2013 中的通讯簿管理 Get-CsService</span><span class="sxs-lookup"><span data-stu-id="9413b-103">Get-CsService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9413b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9413b-104">

<span> </span></span></span>

<span data-ttu-id="9413b-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9413b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9413b-106">哪些人可以运行此 cmdlet：默认情况下，授权以下组的成员在本地运行 Get-CsService cmdlet： RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="9413b-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsService cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="9413b-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="9413b-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsService"}

<span data-ttu-id="9413b-108">Get-CsService 可检索和显示基础结构的已定义 Web 服务的当前配置非常有用。</span><span class="sxs-lookup"><span data-stu-id="9413b-108">Get-CsService is valuable to retrieve and display the current configuration of your infrastructure’s defined Web Services.</span></span> <span data-ttu-id="9413b-109">通过定义池的完全限定的域名 (FQDN) 和参数 Web 服务器，cmdlet 将返回由服务器提供的基于 web 的服务，包括通讯簿处理程序和通讯组列表扩展 Uri。</span><span class="sxs-lookup"><span data-stu-id="9413b-109">By defining the pool’s fully qualified domain name (FQDN) and the parameter WebServer, the cmdlet returns the web-based services offered by your server, including the Address Book handler and distribution list expansion URIs.</span></span>

<span data-ttu-id="9413b-110">例如：</span><span class="sxs-lookup"><span data-stu-id="9413b-110">For example:</span></span>

    Get-CsService -PoolFqdn "fe01.contoso.net" -WebServer

<span data-ttu-id="9413b-111">此 cmdlet 返回以下内容：</span><span class="sxs-lookup"><span data-stu-id="9413b-111">This cmdlet returns the following:</span></span>

<span data-ttu-id="9413b-112">标识： Web 站点:pool01</span><span class="sxs-lookup"><span data-stu-id="9413b-112">Identity : WebServer:pool01.contoso.net</span></span>

<span data-ttu-id="9413b-113">:Dc01：</span><span class="sxs-lookup"><span data-stu-id="9413b-113">FileStore : FileStore:dc01.contoso.net</span></span>

<span data-ttu-id="9413b-114">UserServer： UserServer:pool01</span><span class="sxs-lookup"><span data-stu-id="9413b-114">UserServer : UserServer:pool01.contoso.net</span></span>

<span data-ttu-id="9413b-115">PrimaryHttpPort：80</span><span class="sxs-lookup"><span data-stu-id="9413b-115">PrimaryHttpPort : 80</span></span>

<span data-ttu-id="9413b-116">PrimaryHttpsPort：443</span><span class="sxs-lookup"><span data-stu-id="9413b-116">PrimaryHttpsPort : 443</span></span>

<span data-ttu-id="9413b-117">ExternalHttpPort：8080</span><span class="sxs-lookup"><span data-stu-id="9413b-117">ExternalHttpPort : 8080</span></span>

<span data-ttu-id="9413b-118">ExternalHttpsPort：4443</span><span class="sxs-lookup"><span data-stu-id="9413b-118">ExternalHttpsPort : 4443</span></span>

<span data-ttu-id="9413b-119">PublishedPrimaryHttpPort：80</span><span class="sxs-lookup"><span data-stu-id="9413b-119">PublishedPrimaryHttpPort : 80</span></span>

<span data-ttu-id="9413b-120">PublishedPrimaryHttpsPort：443</span><span class="sxs-lookup"><span data-stu-id="9413b-120">PublishedPrimaryHttpsPort : 443</span></span>

<span data-ttu-id="9413b-121">PublishedExternalHttpPort：80</span><span class="sxs-lookup"><span data-stu-id="9413b-121">PublishedExternalHttpPort : 80</span></span>

<span data-ttu-id="9413b-122">PublishedExternalHttpsPort：443</span><span class="sxs-lookup"><span data-stu-id="9413b-122">PublishedExternalHttpsPort : 443</span></span>

<span data-ttu-id="9413b-123">ReachPrimaryPsomServerPort：8060</span><span class="sxs-lookup"><span data-stu-id="9413b-123">ReachPrimaryPsomServerPort : 8060</span></span>

<span data-ttu-id="9413b-124">ReachExternalPsomServerPort：8061</span><span class="sxs-lookup"><span data-stu-id="9413b-124">ReachExternalPsomServerPort : 8061</span></span>

<span data-ttu-id="9413b-125">AppSharingPortStart：49152</span><span class="sxs-lookup"><span data-stu-id="9413b-125">AppSharingPortStart : 49152</span></span>

<span data-ttu-id="9413b-126">AppSharingPortCount：16383</span><span class="sxs-lookup"><span data-stu-id="9413b-126">AppSharingPortCount : 16383</span></span>

<span data-ttu-id="9413b-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span></span>

<span data-ttu-id="9413b-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span><span class="sxs-lookup"><span data-stu-id="9413b-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span></span>

<span data-ttu-id="9413b-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span><span class="sxs-lookup"><span data-stu-id="9413b-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span></span>

<span data-ttu-id="9413b-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span></span>

<span data-ttu-id="9413b-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span></span>

<span data-ttu-id="9413b-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="9413b-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="9413b-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span><span class="sxs-lookup"><span data-stu-id="9413b-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span></span>

<span data-ttu-id="9413b-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span><span class="sxs-lookup"><span data-stu-id="9413b-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span></span>

<span data-ttu-id="9413b-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="9413b-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="9413b-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span></span>

<span data-ttu-id="9413b-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="9413b-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span></span>

<span data-ttu-id="9413b-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span><span class="sxs-lookup"><span data-stu-id="9413b-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span></span>

<span data-ttu-id="9413b-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span><span class="sxs-lookup"><span data-stu-id="9413b-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span></span>

<span data-ttu-id="9413b-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="9413b-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="9413b-143">MeetExternalUri : https://csweb.contoso.com/Meet</span><span class="sxs-lookup"><span data-stu-id="9413b-143">MeetExternalUri : https://csweb.contoso.com/Meet</span></span>

<span data-ttu-id="9413b-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span><span class="sxs-lookup"><span data-stu-id="9413b-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span></span>

<span data-ttu-id="9413b-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span><span class="sxs-lookup"><span data-stu-id="9413b-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span></span>

<span data-ttu-id="9413b-146">ReachExternalUri : https://csweb.contoso.com/Reach</span><span class="sxs-lookup"><span data-stu-id="9413b-146">ReachExternalUri : https://csweb.contoso.com/Reach</span></span>

<span data-ttu-id="9413b-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span><span class="sxs-lookup"><span data-stu-id="9413b-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span></span>

<span data-ttu-id="9413b-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="9413b-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="9413b-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="9413b-150">ExternalFqdn： csweb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9413b-150">ExternalFqdn : csweb.contoso.com</span></span>

<span data-ttu-id="9413b-151">InternalFqdn： internalweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="9413b-151">InternalFqdn : internalweb.contoso.net</span></span>

<span data-ttu-id="9413b-152">DependentServiceList： {注册:pool01，ConferencingServer:pool01}</span><span class="sxs-lookup"><span data-stu-id="9413b-152">DependentServiceList : {Registrar:pool01.contoso.net, ConferencingServer:pool01.contoso.net}</span></span>

<span data-ttu-id="9413b-153">ServiceId： 1-WebServices-1</span><span class="sxs-lookup"><span data-stu-id="9413b-153">ServiceId : 1-WebServices-1</span></span>

<span data-ttu-id="9413b-154">SiteId：网站：雷德蒙</span><span class="sxs-lookup"><span data-stu-id="9413b-154">SiteId : Site:Redmond</span></span>

<span data-ttu-id="9413b-155">PoolFqdn： pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="9413b-155">PoolFqdn : pool01.contoso.net</span></span>

<span data-ttu-id="9413b-156">版本：5</span><span class="sxs-lookup"><span data-stu-id="9413b-156">Version : 5</span></span>

<span data-ttu-id="9413b-157">角色： Web 还是 Web</span><span class="sxs-lookup"><span data-stu-id="9413b-157">Role : WebServer</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="9413b-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9413b-158">See Also</span></span>


[<span data-ttu-id="9413b-159">CsService</span><span class="sxs-lookup"><span data-stu-id="9413b-159">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="9413b-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9413b-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

