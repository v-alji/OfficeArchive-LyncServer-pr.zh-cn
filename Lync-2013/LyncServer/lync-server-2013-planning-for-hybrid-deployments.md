---
title: Lync Server 2013：规划混合部署
description: Lync Server 2013：规划混合部署。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424546"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="ad124-103">规划 Lync Server 2013 混合部署</span><span class="sxs-lookup"><span data-stu-id="ad124-103">Planning for Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad124-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad124-104">

<span> </span></span></span>

<span data-ttu-id="ad124-105">_**主题上次修改时间** ：2016-05-25_</span><span class="sxs-lookup"><span data-stu-id="ad124-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="ad124-106">规划混合部署时，应考虑用户和网络基础结构的以下要求。</span><span class="sxs-lookup"><span data-stu-id="ad124-106">You should consider the following requirements for users and your network infrastructure while planning for a hybrid deployment.</span></span>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="ad124-107">基础结构要求</span><span class="sxs-lookup"><span data-stu-id="ad124-107">Infrastructure Requirements</span></span>

<span data-ttu-id="ad124-108">必须在环境中配置以下各项，才能实现和部署混合部署。</span><span class="sxs-lookup"><span data-stu-id="ad124-108">You must have the following configured in your environment in order to implement and deploy a hybrid deployment.</span></span>

  - <span data-ttu-id="ad124-109">启用了 Skype for Business Online 的 Microsoft 365 或 Office 365 组织。</span><span class="sxs-lookup"><span data-stu-id="ad124-109">A Microsoft 365 or Office 365 organization with Skype for Business Online enabled.</span></span> <span data-ttu-id="ad124-110">请注意，只能将单个租户用于本地部署的混合配置。</span><span class="sxs-lookup"><span data-stu-id="ad124-110">Note that you can use only a single tenant for a hybrid configuration with your on-premises deployment.</span></span>

  - <span data-ttu-id="ad124-111">在受支持的拓扑中 (Skype for Business Server) Lync Server 的单个本地部署。</span><span class="sxs-lookup"><span data-stu-id="ad124-111">A single on-premises deployment (infrastructure) of Skype for Business Server or Lync Server that is deployed in a supported topology.</span></span> <span data-ttu-id="ad124-112">请参阅拓扑要求。</span><span class="sxs-lookup"><span data-stu-id="ad124-112">See Topology Requirements.</span></span>
    
    <span data-ttu-id="ad124-113">有关为混合配置 Lync Server 2013 或 Lync Server 2010 部署的信息，请参阅 [配置 Lync Server 2013 混合部署](lync-server-2013-configuring-hybrid-deployments.md)。</span><span class="sxs-lookup"><span data-stu-id="ad124-113">For information about configuring your Lync Server 2013 or Lync Server 2010 deployment for hybrid, see [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span></span>

  - <span data-ttu-id="ad124-114">Skype for Business Server 2015 管理工具。</span><span class="sxs-lookup"><span data-stu-id="ad124-114">Skype for Business Server 2015 administrative tools.</span></span> <span data-ttu-id="ad124-115">如果您使用的是 Lync Server 2013 或 Lync Server 2010，您可以使用 Lync Server 2013 管理工具。</span><span class="sxs-lookup"><span data-stu-id="ad124-115">If you are using Lync Server 2013 or Lync Server 2010, you can use the Lync Server 2013 administrative tools.</span></span>

  - <span data-ttu-id="ad124-116">若要支持 Microsoft 365 或 Office 365 的单一登录，以便用户可以使用与本地相同的登录凭据登录 Office，可以使用 Azure Active Directory (AAD) Connect 的密码同步功能。</span><span class="sxs-lookup"><span data-stu-id="ad124-116">To support Single Sign-on with Microsoft 365 or Office 365 so that users can use the same login credentials for signing in to Office as they do on-premises, you can use the password sync features of Azure Active Directory (AAD) Connect.</span></span> <span data-ttu-id="ad124-117">还可使用 Active Directory 联合身份验证服务 (AD FS) Microsoft 365 或 Office 365 进行单一登录。</span><span class="sxs-lookup"><span data-stu-id="ad124-117">You can also use Active Directory Federation Services (AD FS) for single sign-on with Microsoft 365 or Office 365.</span></span>
    
    <span data-ttu-id="ad124-118">有关详细信息，请参阅 [将本地标识与 Azure Active Directory 集成](https://go.microsoft.com/fwlink/p/?linkid=619754)。</span><span class="sxs-lookup"><span data-stu-id="ad124-118">For more information, see [Integrating your on-premises identities with Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span></span>

  - <span data-ttu-id="ad124-119">单个目录同步解决方案，使本地和联机 Active Directory 对象保持同步。</span><span class="sxs-lookup"><span data-stu-id="ad124-119">A single directory synchronization solution to keep your on-premises and online Active Directory objects synchronized.</span></span> <span data-ttu-id="ad124-120">有关目录同步的详细信息，请参阅 [目录集成工具](https://go.microsoft.com/fwlink/p/?linkid=530320)。</span><span class="sxs-lookup"><span data-stu-id="ad124-120">For details about Directory Synchronization, see [Directory Integration Tools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span></span>

</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="ad124-121">Lync 客户端支持</span><span class="sxs-lookup"><span data-stu-id="ad124-121">Lync Client Support</span></span>

<span data-ttu-id="ad124-122">Lync 客户端支持的功能以及本地和联机环境中提供的功能存在一些差异。</span><span class="sxs-lookup"><span data-stu-id="ad124-122">There are some differences in the features supported in Lync clients, as well as the features available in on-premises and online environments.</span></span> <span data-ttu-id="ad124-123">在决定希望将用户归到组织中何处之前，您可以查看 Lync Server 的各种配置的客户端支持。</span><span class="sxs-lookup"><span data-stu-id="ad124-123">Before you decide where you want to home users in your organization, you can view the client support for the various configurations of Lync Server.</span></span> <span data-ttu-id="ad124-124">Lync 混合部署中的 Skype for Business Online 支持以下客户端：</span><span class="sxs-lookup"><span data-stu-id="ad124-124">The following clients are supported with Skype for Business Online in a Lync hybrid deployment:</span></span>

  - <span data-ttu-id="ad124-125">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ad124-125">Lync 2010</span></span>

  - <span data-ttu-id="ad124-126">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="ad124-126">Lync 2013</span></span>

  - <span data-ttu-id="ad124-127">Lync Windows 应用商店应用</span><span class="sxs-lookup"><span data-stu-id="ad124-127">Lync Windows Store app</span></span>

  - <span data-ttu-id="ad124-128">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="ad124-128">Lync Web App</span></span>

  - <span data-ttu-id="ad124-129">Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="ad124-129">Lync Mobile</span></span>

  - <span data-ttu-id="ad124-130">Lync for Mac 2011</span><span class="sxs-lookup"><span data-stu-id="ad124-130">Lync for Mac 2011</span></span>

  - <span data-ttu-id="ad124-131">Lync Room System</span><span class="sxs-lookup"><span data-stu-id="ad124-131">Lync Room System</span></span>

  - <span data-ttu-id="ad124-132">Lync Basic 2013</span><span class="sxs-lookup"><span data-stu-id="ad124-132">Lync Basic 2013</span></span>

<span data-ttu-id="ad124-133">有关客户端支持的详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="ad124-133">For details about client support, see the following topics:</span></span>

  - [<span data-ttu-id="ad124-134">Lync Online 客户端</span><span class="sxs-lookup"><span data-stu-id="ad124-134">Clients for Lync Online</span></span>](https://go.microsoft.com/fwlink/?linkid=281902)

  - [<span data-ttu-id="ad124-135">Lync Server 2013 的客户端比较表</span><span class="sxs-lookup"><span data-stu-id="ad124-135">Client comparison tables for Lync Server 2013</span></span>](lync-server-2013-desktop-client-comparison-tables.md)

  - [<span data-ttu-id="ad124-136">Lync Server 2013 的移动客户端比较表</span><span class="sxs-lookup"><span data-stu-id="ad124-136">Mobile client comparison tables for Lync Server 2013</span></span>](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="ad124-137">拓扑要求</span><span class="sxs-lookup"><span data-stu-id="ad124-137">Topology Requirements</span></span>

<span data-ttu-id="ad124-138">若要配置与 Skype for Business Online 的混合部署，需要具有以下受支持的拓扑之一：</span><span class="sxs-lookup"><span data-stu-id="ad124-138">To configure your deployment for hybrid with Skype for Business Online, you need to have one of the following supported topologies:</span></span>

  - <span data-ttu-id="ad124-139">Skype for Business Server 2015 部署，所有服务器运行 Skype for Business Server 2015。</span><span class="sxs-lookup"><span data-stu-id="ad124-139">A Skype for Business Server 2015 deployment with all servers running Skype for Business Server 2015.</span></span>

  - <span data-ttu-id="ad124-140">Lync Server 2013 部署，所有服务器运行 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="ad124-140">A Lync Server 2013 deployment with all servers running Lync Server 2013.</span></span>

  - <span data-ttu-id="ad124-141">Lync Server 2010 部署，其所有服务器运行 Lync Server 2010，具有最新的累积更新。</span><span class="sxs-lookup"><span data-stu-id="ad124-141">A Lync Server 2010 deployment with all servers running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="ad124-142">联合边缘服务器和联合边缘服务器中的下一跃点服务器必须运行具有最新累积更新的 Lync Server 2010。</span><span class="sxs-lookup"><span data-stu-id="ad124-142">The federation Edge Server and next hop server from the federation Edge Server must be running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="ad124-143">Skype for Business Server 2015 或 Lync Server 2013 管理工具必须安装在至少一台服务器或管理工作站上。</span><span class="sxs-lookup"><span data-stu-id="ad124-143">The Skype for Business Server 2015 or Lync Server 2013 Administrative Tools must be installed on at least one server or management workstation.</span></span>

  - <span data-ttu-id="ad124-144">混合 Lync Server 2013 和 Skype for Business Server 2015 部署，在运行 Skype for Business Server 2015 的至少一个站点中具有以下服务器角色：</span><span class="sxs-lookup"><span data-stu-id="ad124-144">A mixed Lync Server 2013 and Skype for Business Server 2015 deployment with the following server roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="ad124-145">至少一个企业版池或 Standard Edition 服务器 </span><span class="sxs-lookup"><span data-stu-id="ad124-145">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="ad124-146">与 SIP 联盟关联的控制器池（如果存在）</span><span class="sxs-lookup"><span data-stu-id="ad124-146">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="ad124-147">与 SIP 联盟关联的边缘池</span><span class="sxs-lookup"><span data-stu-id="ad124-147">The Edge Pool associated with SIP federation</span></span>

  - <span data-ttu-id="ad124-148">在运行 Skype for Business Server 2015 的至少一个站点中混合部署 Lync Server 2010 和 Skype for Business Server 2015，其中具有以下服务器角色：</span><span class="sxs-lookup"><span data-stu-id="ad124-148">A mixed Lync Server 2010 and Skype for Business Server 2015 deployment with the following servers roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="ad124-149">至少一个企业版池或 Standard Edition 服务器 </span><span class="sxs-lookup"><span data-stu-id="ad124-149">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="ad124-150">与 SIP 联盟关联的控制器池（如果存在）</span><span class="sxs-lookup"><span data-stu-id="ad124-150">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="ad124-151">与站点的 SIP 联盟关联的边缘池</span><span class="sxs-lookup"><span data-stu-id="ad124-151">The Edge Pool associated with SIP federation for the Site</span></span>

  - <span data-ttu-id="ad124-152">在至少一个运行 Lync Server 2013 的站点中混合部署具有以下服务器角色的 Lync Server 2010 和 Lync Server 2013：</span><span class="sxs-lookup"><span data-stu-id="ad124-152">A mixed Lync Server 2010 and Lync Server 2013 deployment with the following server roles in at least one site running Lync Server 2013:</span></span>
    
      - <span data-ttu-id="ad124-153">站点中至少一个企业版池或 Standard Edition 服务器</span><span class="sxs-lookup"><span data-stu-id="ad124-153">At least one Enterprise Pool or Standard Edition server in the site</span></span>
    
      - <span data-ttu-id="ad124-154">与 SIP 联盟关联的控制器池（如果站点中存在）</span><span class="sxs-lookup"><span data-stu-id="ad124-154">The Director Pool associated with SIP federation, if it exists in the site</span></span>
    
      - <span data-ttu-id="ad124-155">与站点的 SIP 联盟关联的边缘池</span><span class="sxs-lookup"><span data-stu-id="ad124-155">The Edge Pool associated with SIP federation for the site</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ad124-156">所有用户管理（包括用户在本地和 UNRESOLVED_TOKEN_VAL (skypeforbusiness) Online 之间移动）都需要使用最新安装的管理工具版本完成。</span><span class="sxs-lookup"><span data-stu-id="ad124-156">All user management, including user moves between on-premises and UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, needs to be done using the latest installed version of the administrative tools.</span></span> <span data-ttu-id="ad124-157">必须在能够连接到现有本地部署和 Internet 的单独服务器上安装管理工具。</span><span class="sxs-lookup"><span data-stu-id="ad124-157">The administrative tools must be installed on a separate server that has connect access to the existing on-premises deployment and to the Internet.</span></span> <span data-ttu-id="ad124-158">将用户从本地部署移动到 UNRESOLVED_TOKEN_VAL (skype16_online) 的 <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet 必须从连接到本地部署的管理工具运行。</span><span class="sxs-lookup"><span data-stu-id="ad124-158">The <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet to move users from your on-premises deployment to UNRESOLVED_TOKEN_VAL(skype16_online) must be run from the administrative tools connected to your on-premises deployment.</span></span>



</div>

<span data-ttu-id="ad124-159">有关支持的拓扑的详细信息，请参阅 Lync [Server 2013](lync-server-2013-supported-topologies.md)中支持的拓扑和 [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)企业混合部署的参考拓扑。</span><span class="sxs-lookup"><span data-stu-id="ad124-159">For more information about supported topologies, see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md), and [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments](https://go.microsoft.com/fwlink/p/?linkid=398709).</span></span>

<span data-ttu-id="ad124-160">有关混合部署和将 PowerShell 连接到 Lync Online 的故障排除信息，请参阅 [Lync Online：Lync PowerShell 和混合故障排除](https://go.microsoft.com/fwlink/p/?linkid=306718)。</span><span class="sxs-lookup"><span data-stu-id="ad124-160">For troubleshooting information about hybrid deployments and connecting PowerShell to Lync Online, see [Lync Online: Lync PowerShell and Hybrid Troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span></span>

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a><span data-ttu-id="ad124-161">允许/阻止联合列表的要求</span><span class="sxs-lookup"><span data-stu-id="ad124-161">Requirements for Federation Allowed/Blocked Lists</span></span>

<span data-ttu-id="ad124-p108">允许域列表包括已配置合作伙伴“边缘”完全限定域名 (FQDN) 的域。这些域有时也称 *允许的合作伙伴服务器* 或 *直接联盟合作伙伴*。您应熟悉开放联盟和封闭联盟（在本地部署中分别称为 *合作伙伴发现* 和 *允许的合作伙伴域列表*）之间的差异。</span><span class="sxs-lookup"><span data-stu-id="ad124-p108">The Allowed domains list includes domains that have a partner Edge fully qualified domain name (FQDN) configured. These are sometimes referred to as *allowed partner servers* or *direct federation partners*. You should be familiar with the difference between Open Federation and Closed Federation, referred to as *partner discovery* and *allowed partner domain list*, respectively, in on-premises deployments.</span></span>

<span data-ttu-id="ad124-165">必须满足以下要求才能成功配置混合部署：</span><span class="sxs-lookup"><span data-stu-id="ad124-165">The following requirements must be met to successfully configure a hybrid deployment:</span></span>

  - <span data-ttu-id="ad124-166">必须为本地部署和 Microsoft 365 或 Office 365 组织配置相同的域匹配。</span><span class="sxs-lookup"><span data-stu-id="ad124-166">Domain matching must be configured the same for your on-premises deployment and your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="ad124-167">如果在本地部署中启用了合作伙伴发现，则必须为您的联机租户配置开放联盟。</span><span class="sxs-lookup"><span data-stu-id="ad124-167">If partner discovery is enabled on the on-premises deployment, then open federation must be configured for your online tenant.</span></span> <span data-ttu-id="ad124-168">如果未启用合作伙伴发现，则必须为您的联机租户配置封闭联盟。</span><span class="sxs-lookup"><span data-stu-id="ad124-168">If partner discovery is not enabled, then closed federation must be configured for your online tenant.</span></span>

  - <span data-ttu-id="ad124-169">本地部署中的阻止域列表必须与您的联机租户的阻止域列表完全匹配。</span><span class="sxs-lookup"><span data-stu-id="ad124-169">The Blocked domains list in the on-premises deployment must exactly match the Blocked domains list for your online tenant.</span></span>

  - <span data-ttu-id="ad124-170">本地部署中的允许域列表必须与您的联机租户的允许域列表完全匹配。</span><span class="sxs-lookup"><span data-stu-id="ad124-170">The Allowed domains list in the on-premises deployment must exactly match the Allowed domains list for your online tenant.</span></span>

  - <span data-ttu-id="ad124-171">必须为联机租户的外部通信启用联合，该外部通信是使用 Lync Online 控制面板配置的。</span><span class="sxs-lookup"><span data-stu-id="ad124-171">Federation must be enabled for the external communications for the online tenant, which is configured by using the Lync Online Control Panel.</span></span>

</div>

<div>

## <a name="dns-settings"></a><span data-ttu-id="ad124-172">DNS 设置</span><span class="sxs-lookup"><span data-stu-id="ad124-172">DNS Settings</span></span>

<span data-ttu-id="ad124-173">为混合部署创建 DNS 记录时，所有 Lync 外部 DNS 记录应指向本地基础结构。</span><span class="sxs-lookup"><span data-stu-id="ad124-173">When creating DNS records for hybrid deployments, all Lync external DNS records should point to the on-premises infrastructure.</span></span> <span data-ttu-id="ad124-174">有关所需 DNS 记录的详细信息，请参阅域名系统 (DNS) [Lync Server 2013 的要求](lync-server-2013-domain-name-system-dns-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ad124-174">For details on required DNS records, please refer to [Domain Name System (DNS) requirements for Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span></span>

<span data-ttu-id="ad124-175">此外，您还需要确保下表中所述的 DNS 解析在您的本地部署中正常运行：</span><span class="sxs-lookup"><span data-stu-id="ad124-175">Additionally you need to ensure that the DNS resolution described in the following table works in your on-premises deployment:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad124-176">DNS 记录</span><span class="sxs-lookup"><span data-stu-id="ad124-176">DNS record</span></span></p></td>
<td><p><span data-ttu-id="ad124-177">解析者</span><span class="sxs-lookup"><span data-stu-id="ad124-177">Resolvable by</span></span></p></td>
<td><p><span data-ttu-id="ad124-178">DNS 要求</span><span class="sxs-lookup"><span data-stu-id="ad124-178">DNS requirement</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad124-179">_sipfederationtls._tcp 的 DNS SRV 记录。 &lt;sipdomain.com 解析为 Access Edge 外部 IP 帐户的所有受支持的 &gt; SIP () </span><span class="sxs-lookup"><span data-stu-id="ad124-179">DNS SRV record for _sipfederationtls._tcp.&lt;sipdomain.com&gt; for all supported SIP domains resolving to Access Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="ad124-180">边缘服务器</span><span class="sxs-lookup"><span data-stu-id="ad124-180">Edge server(s)</span></span></p></td>
<td><p><span data-ttu-id="ad124-p111">在混合配置中启用联盟通信。边缘服务器需要知道在什么位置为 SIP 域路由分布在本地设备和在线设备上的联盟流量。</span><span class="sxs-lookup"><span data-stu-id="ad124-p111">Enable federated communication in a hybrid configuration. The Edge Server needs to know where to route federated traffic for the SIP domain that is split between on premises and online.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad124-183">边缘 Web 会议服务 FQDN 的 DNS A 记录，例如解析为 Web 会议边缘外部 IP 的 webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ad124-183">DNS A record(s) for Edge Web Conferencing Service FQDN, e.g. webcon.contoso.com resolving to Web Conferencing Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="ad124-184">已连接到用户计算机的内部公司网络</span><span class="sxs-lookup"><span data-stu-id="ad124-184">Internal corporate network connected users’ computers</span></span></p></td>
<td><p><span data-ttu-id="ad124-p112">让在线用户能够在本地托管会议中演示或查看内容。内容包括 PowerPoint 文件、白板、轮询和共享笔记。</span><span class="sxs-lookup"><span data-stu-id="ad124-p112">Enable online users to present or view content in on-premises hosted meetings. Content includes PowerPoint files, whiteboards, polls, and shared notes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad124-187">根据 DNS 在您的组织中如何配置，您可能需要将这些记录添加到内部托管 DNS 区域，以便相应的 SIP 域能够提供对这些记录的内部 DNS 解析。</span><span class="sxs-lookup"><span data-stu-id="ad124-187">Depending on how DNS is configured in your organization, you may need to add these records to the internal hosted DNS zone for the corresponding SIP domain(s) to provide internal DNS resolution to these records.</span></span>

</div>

<div>

## <a name="firewall-considerations"></a><span data-ttu-id="ad124-188">防火墙注意事项</span><span class="sxs-lookup"><span data-stu-id="ad124-188">Firewall Considerations</span></span>

<span data-ttu-id="ad124-p113">您的网络上的计算机必须能够执行标准 Internet DNS 查找。如果这些计算机可以连接标准 Internet 站点，表明您的网络符合此要求。</span><span class="sxs-lookup"><span data-stu-id="ad124-p113">Computers on your network must be able to perform standard Internet DNS lookups. If these computers can reach standard Internet sites, your network meets this requirement.</span></span>

<span data-ttu-id="ad124-191">根据数据中心Microsoft Online Services的位置，还必须将网络防火墙设备配置为接受基于通配符域名的连接，例如 (来自 \* .outlook.com) 的所有流量。</span><span class="sxs-lookup"><span data-stu-id="ad124-191">Depending on the location of your Microsoft Online Services data center, you must also configure your network firewall devices to accept connections based on wildcard domain names (for example, all traffic from \*.outlook.com).</span></span> <span data-ttu-id="ad124-192">如果组织的防火墙不支持通配符名称配置，必须手动确定要允许的 IP 地址范围和指定的端口。</span><span class="sxs-lookup"><span data-stu-id="ad124-192">If your organization’s firewalls do not support wildcard name configurations, you will have to manually determine the IP address ranges that you would like to allow and the specified ports.</span></span>

<span data-ttu-id="ad124-193">请参阅帮助主题 [Office 365 URL 和 IP 地址范围](https://go.microsoft.com/fwlink/p/?linkid=252942)。</span><span class="sxs-lookup"><span data-stu-id="ad124-193">Refer to the Help topic [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=252942).</span></span>

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a><span data-ttu-id="ad124-194">端口和协议要求</span><span class="sxs-lookup"><span data-stu-id="ad124-194">Port and Protocol Requirements</span></span>

<span data-ttu-id="ad124-195">除了内部 Lync Server 2013 通信的端口要求外，还必须配置以下端口。</span><span class="sxs-lookup"><span data-stu-id="ad124-195">In addition to the port requirements for internal Lync Server 2013 communication, you must also configure the following ports.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad124-196">协议/端口</span><span class="sxs-lookup"><span data-stu-id="ad124-196">Protocol / Port</span></span></th>
<th><span data-ttu-id="ad124-197">应用程序</span><span class="sxs-lookup"><span data-stu-id="ad124-197">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad124-198">TCP 443</span><span class="sxs-lookup"><span data-stu-id="ad124-198">TCP 443</span></span></p></td>
<td><p><span data-ttu-id="ad124-199">打开入站</span><span class="sxs-lookup"><span data-stu-id="ad124-199">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="ad124-200">Active Directory 联合身份验证服务 (联合服务器角色) </span><span class="sxs-lookup"><span data-stu-id="ad124-200">Active Directory Federation Services (federation server role)</span></span></p>
<p><span data-ttu-id="ad124-201">有关详细信息，请参阅了解 <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">AD FS 角色服务</a>。</span><span class="sxs-lookup"><span data-stu-id="ad124-201">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span></span></p></li>
<li><p><span data-ttu-id="ad124-202">Active Directory 联合身份验证服务 (代理服务器角色) </span><span class="sxs-lookup"><span data-stu-id="ad124-202">Active Directory Federation Services (proxy server role)</span></span></p></li>
<li><p><span data-ttu-id="ad124-203">Microsoft Online Services 门户</span><span class="sxs-lookup"><span data-stu-id="ad124-203">Microsoft Online Services Portal</span></span></p></li>
<li><p><span data-ttu-id="ad124-204">我的公司门户</span><span class="sxs-lookup"><span data-stu-id="ad124-204">My Company Portal</span></span></p></li>
<li><p><span data-ttu-id="ad124-205">Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="ad124-205">Outlook Web App</span></span></p></li>
<li><p><span data-ttu-id="ad124-206">Lync 客户端 (从本地 Lync Server 与 Lync Online 通信) </span><span class="sxs-lookup"><span data-stu-id="ad124-206">Lync client (communication to Lync Online from on-premises Lync Server)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad124-207">TCP 80 和 443</span><span class="sxs-lookup"><span data-stu-id="ad124-207">TCP 80 and 443</span></span></p></td>
<td><p><span data-ttu-id="ad124-208">打开入站</span><span class="sxs-lookup"><span data-stu-id="ad124-208">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="ad124-209">Microsoft Online Services 目录同步工具</span><span class="sxs-lookup"><span data-stu-id="ad124-209">Microsoft Online Services Directory Synchronization Tool</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad124-210">TCP 5061</span><span class="sxs-lookup"><span data-stu-id="ad124-210">TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="ad124-211">在边缘服务器上打开入站/出站</span><span class="sxs-lookup"><span data-stu-id="ad124-211">Open inbound/outbound on the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad124-212">PSOM/TLS 443</span><span class="sxs-lookup"><span data-stu-id="ad124-212">PSOM/TLS 443</span></span></p></td>
<td><p><span data-ttu-id="ad124-213">为数据共享会话打开入站/出站</span><span class="sxs-lookup"><span data-stu-id="ad124-213">Open inbound/outbound for data sharing sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad124-214">STUN/TCP 443</span><span class="sxs-lookup"><span data-stu-id="ad124-214">STUN/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="ad124-215">为音频、视频、应用程序共享会话打开入站/出站</span><span class="sxs-lookup"><span data-stu-id="ad124-215">Open inbound/outbound for audio, video, application sharing sessions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad124-216">STUN/UDP 3478</span><span class="sxs-lookup"><span data-stu-id="ad124-216">STUN/UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="ad124-217">为音频和视频会话打开入站/出站</span><span class="sxs-lookup"><span data-stu-id="ad124-217">Open inbound/outbound for audio and video sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad124-218">RTP/TCP 50000-59999</span><span class="sxs-lookup"><span data-stu-id="ad124-218">RTP/TCP 50000-59999</span></span></p></td>
<td><p><span data-ttu-id="ad124-219">为音频和视频会话打开出站</span><span class="sxs-lookup"><span data-stu-id="ad124-219">Open outbound for audio and video sessions</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a><span data-ttu-id="ad124-220">用户帐户和数据</span><span class="sxs-lookup"><span data-stu-id="ad124-220">User Accounts and Data</span></span>

<span data-ttu-id="ad124-221">在 Lync Server 2013 混合部署中，必须先在本地部署中创建希望位于 Lync Online 的任何用户，以便用户帐户在 Active Directory 域服务中创建。</span><span class="sxs-lookup"><span data-stu-id="ad124-221">In a Lync Server 2013 hybrid deployment, any user that you want to home in Lync Online must first be created in the on-premises deployment, so that the user account is created in Active Directory Domain Services.</span></span> <span data-ttu-id="ad124-222">然后，你可以将用户移动到 Skype for Business Online，这将移动用户的联系人列表。</span><span class="sxs-lookup"><span data-stu-id="ad124-222">You can then move the user to Skype for Business Online, which will move the user’s contact list.</span></span>

<span data-ttu-id="ad124-223">当您使用 AD FS 和 Dirsync 在您的 Lync 本地和 Lync Online 部署之间同步用户帐户时，您需要在您的本地和联机 Lync 部署之间同步您组织中所有 Lync 用户的 AD 帐户，即使用户未移动到 Lync Online。</span><span class="sxs-lookup"><span data-stu-id="ad124-223">When you synchronize user accounts between your Lync on-premises and Lync Online deployments with AD FS and Dirsync, you need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="ad124-224">如果未同步所有用户，则组织中本地和联机用户之间的通信可能无法按预期工作。</span><span class="sxs-lookup"><span data-stu-id="ad124-224">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ad124-225">如果用户是使用 Microsoft 365 管理中心的联机门户创建的，则用户帐户不会与本地 Active Directory 同步，并且该用户不会存在于本地 Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="ad124-225">If the user is created by using the online portal for Microsoft 365 admin center, the user account will not be synchronized with on-premises Active Directory, and the user will not exist in the on-premises Active Directory.</span></span> <span data-ttu-id="ad124-226">如果您已经在 Lync Online 中创建用户，并且想要配置与本地 Lync Server 的混合，请参阅在 <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013</A>中将用户从 Lync Online 移动到本地 Lync。</span><span class="sxs-lookup"><span data-stu-id="ad124-226">If you have already created users in Lync Online, and want to configure hybrid with an on-premises Lync Server, see <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="ad124-227">规划混合部署时还应考虑以下用户相关的问题。</span><span class="sxs-lookup"><span data-stu-id="ad124-227">You should also consider the following user-related issues when planning for a hybrid deployment.</span></span>

  - <span data-ttu-id="ad124-228">**用户联系人**   Lync Online 用户的联系人限制为 250。</span><span class="sxs-lookup"><span data-stu-id="ad124-228">**User contacts**   The limit for contacts for Lync Online users is 250.</span></span> <span data-ttu-id="ad124-229">当帐户移动到 Lync Online 时，将从用户联系人列表中删除超过此数目的所有联系人。</span><span class="sxs-lookup"><span data-stu-id="ad124-229">Any contacts beyond that number will be removed from the user’s contact list when the account is moved to Lync Online.</span></span>

  - <span data-ttu-id="ad124-230">**即时消息和状态**   用户联系人列表、组和访问控制列表 (ACL) 将与用户帐户一起迁移。</span><span class="sxs-lookup"><span data-stu-id="ad124-230">**Instant Messaging and Presence**   User contact lists, groups, and access control lists (ACLs) are migrated with the user account.</span></span>

  - <span data-ttu-id="ad124-231">**会议数据、会议内容和计划的会议**   此内容不会与用户帐户一起迁移。</span><span class="sxs-lookup"><span data-stu-id="ad124-231">**Conferencing data, meeting content, and scheduled meetings**   This content is not migrated with the user account.</span></span> <span data-ttu-id="ad124-232">用户必须在其帐户迁移到 Lync Online 之后重新安排会议。</span><span class="sxs-lookup"><span data-stu-id="ad124-232">Users must reschedule meetings after their accounts are migrated to Lync Online.</span></span>

</div>

<div>

## <a name="user-policies-and-features"></a><span data-ttu-id="ad124-233">用户策略和功能</span><span class="sxs-lookup"><span data-stu-id="ad124-233">User Policies and Features</span></span>

  - <span data-ttu-id="ad124-234">在 Lync Server 2013 混合环境中，用户可以在本地或联机启用即时消息、语音和会议，但不能同时启用这两者。</span><span class="sxs-lookup"><span data-stu-id="ad124-234">In a Lync Server 2013 hybrid environment, users can be enabled for Instant Messaging, voice, and meetings either on-premises or online, but not both simultaneously.</span></span>

  - <span data-ttu-id="ad124-235">**Lync 客户端**    某些用户在移动到 Lync Online 时可能需要新的客户端版本。</span><span class="sxs-lookup"><span data-stu-id="ad124-235">**Lync Client**    Some users may require a new client version when they are moved to Lync Online.</span></span> <span data-ttu-id="ad124-236">对于 Office Communications Server 2007 R2，在迁移到 Lync Online 之前，必须将用户移动到 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="ad124-236">For Office Communications Server 2007 R2, users must be moved to a Lync Server 2013 pool prior to migration to Lync Online.</span></span>
    
    <span data-ttu-id="ad124-237">有关客户端支持的详细信息，请参阅 [Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) 的客户端和支持的 [Lync 客户端和网络端口配置](https://go.microsoft.com/fwlink/p/?linkid=281901)。</span><span class="sxs-lookup"><span data-stu-id="ad124-237">For more information about client support, see [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span></span>

  - <span data-ttu-id="ad124-238">**本地策略和配置 (非用户)**   联机策略和本地策略需要单独的配置。</span><span class="sxs-lookup"><span data-stu-id="ad124-238">**On-premises policies and configuration (non-user)**   Online and on-premises policies require separate configuration.</span></span> <span data-ttu-id="ad124-239">无法设置适用于二者的全局策略。</span><span class="sxs-lookup"><span data-stu-id="ad124-239">You cannot set global policies that apply to both.</span></span>

<span data-ttu-id="ad124-240"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad124-240"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
