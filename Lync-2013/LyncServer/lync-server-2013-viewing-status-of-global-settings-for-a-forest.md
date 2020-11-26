---
title: Lync Server 2013：查看林全局设置的状态
description: Lync Server 2013：查看林的全局设置状态。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View status of global settings for a forest
ms:assetid: 2ab0f2f1-9908-4e6f-aff3-d6b3cc474b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747889(v=OCS.15)
ms:contentKeyID: 63969590
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9f722ea66f6c54c816703bd1af1d3def57bbd84
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443907"
---
# <a name="view-status-of-global-settings-for-a-forest-in-lync-server-2013"></a><span data-ttu-id="d2607-103">查看 Lync Server 2013 中的林全局设置的状态</span><span class="sxs-lookup"><span data-stu-id="d2607-103">View status of global settings for a forest in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2607-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2607-104">

<span> </span></span></span>

<span data-ttu-id="d2607-105">_**主题上次修改时间：** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="d2607-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="d2607-106">管理员应每月查看 Lync Server 2013 部署的全局设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-106">Administrators should review the global settings for a Lync Server 2013 deployment monthly.</span></span> <span data-ttu-id="d2607-107">目标是针对一组已知的配置查看实施的设置-基准配置，以帮助确保设置有效，并确定是否应更新基准文档。</span><span class="sxs-lookup"><span data-stu-id="d2607-107">The objective would be to review implemented settings against a set of known configurations—a baseline configuration to help guarantee that settings are valid and to determine whether the baseline documentation should be updated.</span></span> <span data-ttu-id="d2607-108">对全局设置所做的更改应通过更改控制过程实现，该过程应包括记录新设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-108">Changes to global setting should be implemented through a Change Control process which should include documenting the new settings.</span></span>

<span data-ttu-id="d2607-109">应查看的全局设置将在以下部分中介绍：</span><span class="sxs-lookup"><span data-stu-id="d2607-109">Global settings that should be reviewed are described in the following sections:</span></span>

<div>

## <a name="check-general-settings"></a><span data-ttu-id="d2607-110">检查常规设置</span><span class="sxs-lookup"><span data-stu-id="d2607-110">Check general settings</span></span>

<span data-ttu-id="d2607-111">检查 "常规" 设置，包括支持的会话初始协议 (Lync Server 2013 的 SIP) 域。</span><span class="sxs-lookup"><span data-stu-id="d2607-111">Check general settings, including the supported Session Initiation Protocol (SIP) domains for Lync Server 2013.</span></span>

<span data-ttu-id="d2607-112">SIP 域信息可通过使用 Windows PowerShell 和 **CsSipDomain** cmdlet 返回。</span><span class="sxs-lookup"><span data-stu-id="d2607-112">SIP domain information can be returned by using Windows PowerShell and the **Get-CsSipDomain** cmdlet.</span></span> <span data-ttu-id="d2607-113">若要返回此信息，请运行 `Get-CsSipDomain` Windows PowerShell 命令。</span><span class="sxs-lookup"><span data-stu-id="d2607-113">To return this information, run the `Get-CsSipDomain` Windows PowerShell command.</span></span>

<span data-ttu-id="d2607-114">对于所有授权 SIP 域，Get-CsSipDomain 将返回类似以下内容的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-114">Get-CsSipDomain will return information similar to this for all the authorized SIP domains:</span></span>

<span data-ttu-id="d2607-115">标识名称 IsDefault</span><span class="sxs-lookup"><span data-stu-id="d2607-115">Identity Name IsDefault</span></span>

<span data-ttu-id="d2607-116">\-------- ---- ---------</span><span class="sxs-lookup"><span data-stu-id="d2607-116">\-------- ---- ---------</span></span>

<span data-ttu-id="d2607-117">fabrikam.com fabrikam.com True</span><span class="sxs-lookup"><span data-stu-id="d2607-117">fabrikam.com fabrikam.com True</span></span>

<span data-ttu-id="d2607-118">na.fabrikam.com na.fabrikam.com False</span><span class="sxs-lookup"><span data-stu-id="d2607-118">na.fabrikam.com na.fabrikam.com False</span></span>

<span data-ttu-id="d2607-119">如果 IsDefault 属性设置为 True，则相应的域是默认 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="d2607-119">If the IsDefault property is set to True, the corresponding domain is your default SIP domain.</span></span> <span data-ttu-id="d2607-120">你可以使用 Set-CsSipDomain cmdlet 更改你的组织的默认 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="d2607-120">You can use the Set-CsSipDomain cmdlet to change the default SIP domain for your organization.</span></span> <span data-ttu-id="d2607-121">但是，不能只是删除默认 SIP 域，因为这样做将不使用默认域。</span><span class="sxs-lookup"><span data-stu-id="d2607-121">However, you can't just delete the default SIP domain because that would leave you without a default domain.</span></span> <span data-ttu-id="d2607-122">如果想要删除 fabrikam.com 域 (如前面的示例) 所示），则必须首先将 na.fabrikam.com 配置为默认域。</span><span class="sxs-lookup"><span data-stu-id="d2607-122">If you wanted to delete the fabrikam.com domain (as shown in the previous example), you would first have to configure na.fabrikam.com to be your default domain.</span></span>

</div>

<div>

## <a name="check-meeting-settings"></a><span data-ttu-id="d2607-123">检查会议设置</span><span class="sxs-lookup"><span data-stu-id="d2607-123">Check meeting settings</span></span>

<span data-ttu-id="d2607-124">会议设置包括会议策略定义和在会议中参与匿名用户的支持。</span><span class="sxs-lookup"><span data-stu-id="d2607-124">Meeting settings include meeting policy definitions and support for participation of anonymous users in meetings.</span></span>

<span data-ttu-id="d2607-125">可使用 Windows PowerShell 和 **CsMeetingConfiguration** cmdlet 检索会议配置设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-125">Meeting configuration settings can be retrieved by using Windows PowerShell and the **Get-CsMeetingConfiguration** cmdlet.</span></span> <span data-ttu-id="d2607-126">例如，以下命令将返回有关全局会议配置设置的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-126">For example, this command returns information about the global meeting configuration settings:</span></span>

<span data-ttu-id="d2607-127">Get-CsMeetingConfiguration –还可以在网站范围内配置身份 "全局" 会议配置设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-127">Get-CsMeetingConfiguration –Identity "Global"Meeting configuration settings can also be configured at the site scope.</span></span> <span data-ttu-id="d2607-128">因此，你可能需要使用以下命令，该命令将返回有关所有会议配置设置的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-128">Because of that, you might want to use the following command, which returns information about all the meeting configuration settings:</span></span>

`Get-CsMeetingConfiguration`

<span data-ttu-id="d2607-129">**CsMeetingConfiguration** cmdlet 返回类似于以下内容的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-129">The **Get-CsMeetingConfiguration** cmdlet returns information similar to the following:</span></span>

<span data-ttu-id="d2607-130">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-130">Identity : Global</span></span>

<span data-ttu-id="d2607-131">PstnCallersBypassLobby： True</span><span class="sxs-lookup"><span data-stu-id="d2607-131">PstnCallersBypassLobby : True</span></span>

<span data-ttu-id="d2607-132">EnableAssignedConferenceType： True</span><span class="sxs-lookup"><span data-stu-id="d2607-132">EnableAssignedConferenceType : True</span></span>

<span data-ttu-id="d2607-133">DesignateAsPresenter：公司</span><span class="sxs-lookup"><span data-stu-id="d2607-133">DesignateAsPresenter : Company</span></span>

<span data-ttu-id="d2607-134">AssignedConferenceTypeByDefault： True</span><span class="sxs-lookup"><span data-stu-id="d2607-134">AssignedConferenceTypeByDefault : True</span></span>

<span data-ttu-id="d2607-135">AdmitAnonymousUsersByDefault： True</span><span class="sxs-lookup"><span data-stu-id="d2607-135">AdmitAnonymousUsersByDefault : True</span></span>

<span data-ttu-id="d2607-136">同样， **AdmitAnonymousUsersByDefault** 列表中的最后一个项目可启用或禁用匿名用户参与会议的能力。</span><span class="sxs-lookup"><span data-stu-id="d2607-136">Again, the final item in the list, **AdmitAnonymousUsersByDefault**, enables or disables the ability of anonymous users to participate in meetings.</span></span>

<span data-ttu-id="d2607-137">检查会议配置设置时，你可能会发现将当前设置与默认等效项进行比较非常有用。</span><span class="sxs-lookup"><span data-stu-id="d2607-137">When checking meeting configuration settings, you might find it useful to compare the current settings against the default equivalents.</span></span> <span data-ttu-id="d2607-138">可以通过运行以下命令来查看默认会议配置设置：</span><span class="sxs-lookup"><span data-stu-id="d2607-138">You can view the default meeting configuration settings by running the following command:</span></span>

`New-CsMeetingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d2607-139">上一个命令创建全局会议配置设置的仅内存实例，该实例使用每个属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="d2607-139">The previous command creates an in-memory-only instance of the global meeting configuration settings, an instance that uses the default value for each property.</span></span> <span data-ttu-id="d2607-140">运行命令时，不会创建实际会议配置设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-140">No actual meeting configuration settings are created when you run the command.</span></span> <span data-ttu-id="d2607-141">但是，所有默认属性值都将显示在屏幕上。</span><span class="sxs-lookup"><span data-stu-id="d2607-141">However, all the default property values will be displayed on-screen.</span></span>

</div>

<div>

## <a name="check-edge-servers-and-their-settings"></a><span data-ttu-id="d2607-142">检查边缘服务器及其设置</span><span class="sxs-lookup"><span data-stu-id="d2607-142">Check Edge Servers and their settings</span></span>

<span data-ttu-id="d2607-143">可以使用 Windows PowerShell 检索边缘服务器信息。</span><span class="sxs-lookup"><span data-stu-id="d2607-143">Edge Server information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="d2607-144">此命令将返回有关所有配置为在你的组织中使用的边缘服务器的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-144">This command returns information about all the Edge Servers configured for use in your organization:</span></span>

`Get-CsService -EdgeServer`

<span data-ttu-id="d2607-145">返回的信息包括每台边缘服务器的所有 FQDN 和端口设置：</span><span class="sxs-lookup"><span data-stu-id="d2607-145">The returned information includes all of the FQDN and port settings for each Edge Server:</span></span>

<span data-ttu-id="d2607-146">标识： EdgeServer： dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d2607-146">Identity : EdgeServer: dc.fabrikam.com</span></span>

<span data-ttu-id="d2607-147">注册机构：注册机构： LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d2607-147">Registrar : Registrar: LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="d2607-148">AccessEdgeInternalSipPort：5061</span><span class="sxs-lookup"><span data-stu-id="d2607-148">AccessEdgeInternalSipPort : 5061</span></span>

<span data-ttu-id="d2607-149">AccessEdgeExternalSipPort：5061</span><span class="sxs-lookup"><span data-stu-id="d2607-149">AccessEdgeExternalSipPort : 5061</span></span>

<span data-ttu-id="d2607-150">AccessEdgeClientPort：443</span><span class="sxs-lookup"><span data-stu-id="d2607-150">AccessEdgeClientPort : 443</span></span>

<span data-ttu-id="d2607-151">DataPsomServerPort：8057</span><span class="sxs-lookup"><span data-stu-id="d2607-151">DataPsomServerPort : 8057</span></span>

<span data-ttu-id="d2607-152">DataPsomClientPort：444</span><span class="sxs-lookup"><span data-stu-id="d2607-152">DataPsomClientPort : 444</span></span>

<span data-ttu-id="d2607-153">MediaRelayAuthEdgePort：5062</span><span class="sxs-lookup"><span data-stu-id="d2607-153">MediaRelayAuthEdgePort : 5062</span></span>

<span data-ttu-id="d2607-154">MediaRelayAuthInternalTurnTcpPort：443</span><span class="sxs-lookup"><span data-stu-id="d2607-154">MediaRelayAuthInternalTurnTcpPort : 443</span></span>

<span data-ttu-id="d2607-155">MediaRelayAuthExternalTurnTcpPort：445</span><span class="sxs-lookup"><span data-stu-id="d2607-155">MediaRelayAuthExternalTurnTcpPort : 445</span></span>

<span data-ttu-id="d2607-156">MediaRelayAuthInternalTurnUdpPort：3478</span><span class="sxs-lookup"><span data-stu-id="d2607-156">MediaRelayAuthInternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="d2607-157">MediaRelayAuthExternalTurnUdpPort：3478</span><span class="sxs-lookup"><span data-stu-id="d2607-157">MediaRelayAuthExternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="d2607-158">MediaCommunicationPortStart：50000</span><span class="sxs-lookup"><span data-stu-id="d2607-158">MediaCommunicationPortStart : 50000</span></span>

<span data-ttu-id="d2607-159">MediaComunicationPortCount：10000</span><span class="sxs-lookup"><span data-stu-id="d2607-159">MediaComunicationPortCount : 10000</span></span>

<span data-ttu-id="d2607-160">AccessEdgeExternalFqdn： dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d2607-160">AccessEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d2607-161">DataEdgeExternalFqdn： dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d2607-161">DataEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d2607-162">AVEdgeExternalFqdn :</span><span class="sxs-lookup"><span data-stu-id="d2607-162">AVEdgeExternalFqdn :</span></span>

<span data-ttu-id="d2607-163">InternalInterfaceFqdn :</span><span class="sxs-lookup"><span data-stu-id="d2607-163">InternalInterfaceFqdn :</span></span>

<span data-ttu-id="d2607-164">ExternalMrasFqdn： dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d2607-164">ExternalMrasFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d2607-165">DependentServiceList： {注册机构： LYNC-SE.fabrikam.com，</span><span class="sxs-lookup"><span data-stu-id="d2607-165">DependentServiceList : {Registrar:LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="d2607-166">ConferencingServer： LYNC-SE</span><span class="sxs-lookup"><span data-stu-id="d2607-166">ConferencingServer:LYNC-SE.fabrikam</span></span>

<span data-ttu-id="d2607-167">com，MediationServer： LYNC-SE。</span><span class="sxs-lookup"><span data-stu-id="d2607-167">com, MediationServer:LYNC-SE.</span></span>

<span data-ttu-id="d2607-168">fabrikam.com}</span><span class="sxs-lookup"><span data-stu-id="d2607-168">fabrikam.com}</span></span>

<span data-ttu-id="d2607-169">ServiceId： fabrikam.com-EdgeServer-2</span><span class="sxs-lookup"><span data-stu-id="d2607-169">ServiceId : fabrikam.com-EdgeServer-2</span></span>

<span data-ttu-id="d2607-170">SiteId： site:fabrikam</span><span class="sxs-lookup"><span data-stu-id="d2607-170">SiteId : site:fabrikam.com</span></span>

<span data-ttu-id="d2607-171">PoolFqdn： dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d2607-171">PoolFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d2607-172">版本：5</span><span class="sxs-lookup"><span data-stu-id="d2607-172">Version : 5</span></span>

<span data-ttu-id="d2607-173">角色： EdgeServer</span><span class="sxs-lookup"><span data-stu-id="d2607-173">Role : EdgeServer</span></span>

<div>

## <a name="check-federation-settings"></a><span data-ttu-id="d2607-174">检查联盟设置</span><span class="sxs-lookup"><span data-stu-id="d2607-174">Check federation settings</span></span>

<span data-ttu-id="d2607-175">检查联盟设置，例如是否已配置，如果答案为 "是"，则为 FQDN 和端口。</span><span class="sxs-lookup"><span data-stu-id="d2607-175">Check Federation settings, such as whether it is configured and, if the answer is "yes,", the FQDN and port.</span></span> <span data-ttu-id="d2607-176">通过使用访问边缘配置设置的全局集合启用和禁用联盟。</span><span class="sxs-lookup"><span data-stu-id="d2607-176">Federation is enabled and disabled by using the global collection of Access Edge configuration settings.</span></span> <span data-ttu-id="d2607-177">在其他情况下，这些意味着联盟是在全或全基础上配置的：为整个组织启用联盟或对整个组织禁用联盟</span><span class="sxs-lookup"><span data-stu-id="d2607-177">Among other things, these mean that federation is configured on an all-or-nothing basis: either federation is enabled for the whole organization or federation is disabled for the whole organization</span></span>

<span data-ttu-id="d2607-178">你的访问边缘配置设置可通过使用 Windows PowerShell 返回。</span><span class="sxs-lookup"><span data-stu-id="d2607-178">Your Access Edge configuration settings can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="d2607-179">若要执行此操作，请运行以下 Windows PowerShell 命令：</span><span class="sxs-lookup"><span data-stu-id="d2607-179">To do that, run the following Windows PowerShell command:</span></span>

`Get-CsAccessEdgeConfiguration`

<span data-ttu-id="d2607-180">因此，该命令将返回类似于以下内容的数据：</span><span class="sxs-lookup"><span data-stu-id="d2607-180">In turn, that command will return data similar to this:</span></span>

<span data-ttu-id="d2607-181">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-181">Identity : Global</span></span>

<span data-ttu-id="d2607-182">AllowAnonymousUsers： False</span><span class="sxs-lookup"><span data-stu-id="d2607-182">AllowAnonymousUsers : False</span></span>

<span data-ttu-id="d2607-183">AllowFederatedUsers： False</span><span class="sxs-lookup"><span data-stu-id="d2607-183">AllowFederatedUsers : False</span></span>

<span data-ttu-id="d2607-184">AllowOutsideUsers： False</span><span class="sxs-lookup"><span data-stu-id="d2607-184">AllowOutsideUsers : False</span></span>

<span data-ttu-id="d2607-185">BeClearingHouse： False</span><span class="sxs-lookup"><span data-stu-id="d2607-185">BeClearingHouse : False</span></span>

<span data-ttu-id="d2607-186">EnablePartnerDiscovery： False</span><span class="sxs-lookup"><span data-stu-id="d2607-186">EnablePartnerDiscovery : False</span></span>

<span data-ttu-id="d2607-187">EnableArchivingDisclaimer： False</span><span class="sxs-lookup"><span data-stu-id="d2607-187">EnableArchivingDisclaimer : False</span></span>

<span data-ttu-id="d2607-188">KeepCrlsUpToDateForPeers： True</span><span class="sxs-lookup"><span data-stu-id="d2607-188">KeepCrlsUpToDateForPeers : True</span></span>

<span data-ttu-id="d2607-189">MarkSourceVerifiableOnOutgoingMessages： True</span><span class="sxs-lookup"><span data-stu-id="d2607-189">MarkSourceVerifiableOnOutgoingMessages : True</span></span>

<span data-ttu-id="d2607-190">OutgoingTlsCountForFederatedPartners：4</span><span class="sxs-lookup"><span data-stu-id="d2607-190">OutgoingTlsCountForFederatedPartners : 4</span></span>

<span data-ttu-id="d2607-191">RoutingMethod : UseDnsSrvRouting</span><span class="sxs-lookup"><span data-stu-id="d2607-191">RoutingMethod : UseDnsSrvRouting</span></span>

<span data-ttu-id="d2607-192">如果 **AllowFederatedUsers** 属性设置为 True，则表示已为你的组织启用联盟。</span><span class="sxs-lookup"><span data-stu-id="d2607-192">If the **AllowFederatedUsers** property is set to True, that means that federation is enabled for your organization.</span></span> <span data-ttu-id="d2607-193"> (将 **AllowFederatedUsers** 设置为 True 还意味着，在拆分域方案中，你的本地用户将能够与云用户无缝通信。 ) </span><span class="sxs-lookup"><span data-stu-id="d2607-193">(Setting **AllowFederatedUsers** to True also means that, in a split domain scenario, your on-premises users will be able to communicate seamlessly with your in-the-cloud users.)</span></span>

<span data-ttu-id="d2607-194">若要检索 Edge 服务器的 FQDN 和端口设置，请参阅上一任务 (边缘服务器及其设置) 。</span><span class="sxs-lookup"><span data-stu-id="d2607-194">To retrieve the FQDN and port settings for your Edge Server, see the previous task (Edge Servers and their settings).</span></span>

<span data-ttu-id="d2607-195">在全局范围内启用联盟意味着用户可能与联盟用户进行通信。</span><span class="sxs-lookup"><span data-stu-id="d2607-195">Enabling federation at the global scope only means that users can potentially communicate with federated users.</span></span> <span data-ttu-id="d2607-196">若要确定任何单个用户是否可以与联盟用户进行实际通信，需要检查分配给该用户的外部用户访问策略。</span><span class="sxs-lookup"><span data-stu-id="d2607-196">To determine whether any individual users can actually communicate with federated users requires you to examine the external user access policy assigned to that user.</span></span>

<span data-ttu-id="d2607-197">可使用 Windows PowerShell 返回外部用户访问信息。</span><span class="sxs-lookup"><span data-stu-id="d2607-197">External user access information can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="d2607-198">例如，此命令返回全局外部用户访问策略的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-198">For example, this command returns information for the global external user access policy:</span></span>

`Get-CsExternalAccessPolicy -Identity "Global"`

<span data-ttu-id="d2607-199">此命令返回所有外部用户访问策略的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-199">And this command returns information for all the external user access policies:</span></span>

`Get-CsExternalAccessPolicy`

<span data-ttu-id="d2607-200">返回的信息将如下所示：</span><span class="sxs-lookup"><span data-stu-id="d2607-200">The returned information will resemble this:</span></span>

<span data-ttu-id="d2607-201">标识： False</span><span class="sxs-lookup"><span data-stu-id="d2607-201">Identity : False</span></span>

<span data-ttu-id="d2607-202">介绍</span><span class="sxs-lookup"><span data-stu-id="d2607-202">Description :</span></span>

<span data-ttu-id="d2607-203">EnableFederationAccess： False</span><span class="sxs-lookup"><span data-stu-id="d2607-203">EnableFederationAccess : False</span></span>

<span data-ttu-id="d2607-204">EnablePublicCloudAccess： False</span><span class="sxs-lookup"><span data-stu-id="d2607-204">EnablePublicCloudAccess : False</span></span>

<span data-ttu-id="d2607-205">EnablePublicCloudAccessAudioVideoAccess： False</span><span class="sxs-lookup"><span data-stu-id="d2607-205">EnablePublicCloudAccessAudioVideoAccess : False</span></span>

<span data-ttu-id="d2607-206">EnableOutsideAccess： False</span><span class="sxs-lookup"><span data-stu-id="d2607-206">EnableOutsideAccess : False</span></span>

<span data-ttu-id="d2607-207">如果 **EnableFederationAccess** 设置为 True，则由给定策略管理的用户可以与联盟用户通信。</span><span class="sxs-lookup"><span data-stu-id="d2607-207">If **EnableFederationAccess** is set to True, then users managed by the given policy can communicate with federated users.</span></span>

</div>

</div>

<div>

## <a name="check-archiving-settings"></a><span data-ttu-id="d2607-208">检查存档设置</span><span class="sxs-lookup"><span data-stu-id="d2607-208">Check archiving settings</span></span>

<span data-ttu-id="d2607-209">检查内部和联盟通信的存档设置。在验证内部和外部存档的设置之前，应验证是否已启用存档。</span><span class="sxs-lookup"><span data-stu-id="d2607-209">Check archiving settings for internal and federated communications.Before verifying the settings for internal and external archiving, you should verify that archiving is enabled.</span></span>

<span data-ttu-id="d2607-210">可以使用 Windows PowerShell 和 Get-CsArchivingConfiguration cmdlet 验证存档配置设置：</span><span class="sxs-lookup"><span data-stu-id="d2607-210">Archiving configuration settings can be verified by using Windows PowerShell and the Get-CsArchivingConfiguration cmdlet:</span></span>

`Get-CsArchivingConfiguration -Identity "Global"`

<span data-ttu-id="d2607-211">请注意，也可以在网站范围内配置存档设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-211">Note that archiving settings can also be configured at the site scope.</span></span> <span data-ttu-id="d2607-212">若要返回有关所有存档设置的信息，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="d2607-212">To return information about all the archiving settings, use this command:</span></span>

`Get-CsArchivingConfiguration`

<span data-ttu-id="d2607-213">Get-CsArchivingConfiguration cmdlet 返回与以下内容类似的数据：</span><span class="sxs-lookup"><span data-stu-id="d2607-213">The Get-CsArchivingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="d2607-214">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-214">Identity : Global</span></span>

<span data-ttu-id="d2607-215">EnableArchiving： False</span><span class="sxs-lookup"><span data-stu-id="d2607-215">EnableArchiving : False</span></span>

<span data-ttu-id="d2607-216">EnablePurging： False</span><span class="sxs-lookup"><span data-stu-id="d2607-216">EnablePurging : False</span></span>

<span data-ttu-id="d2607-217">PurgeExportedArchivesOnly： False</span><span class="sxs-lookup"><span data-stu-id="d2607-217">PurgeExportedArchivesOnly : False</span></span>

<span data-ttu-id="d2607-218">BlockOnArchiveFailure： False</span><span class="sxs-lookup"><span data-stu-id="d2607-218">BlockOnArchiveFailure : False</span></span>

<span data-ttu-id="d2607-219">KeepArchivingDataForDays：14</span><span class="sxs-lookup"><span data-stu-id="d2607-219">KeepArchivingDataForDays : 14</span></span>

<span data-ttu-id="d2607-220">PurgeHourOfDay：2</span><span class="sxs-lookup"><span data-stu-id="d2607-220">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="d2607-221">ArchiveDuplicateMessages： True</span><span class="sxs-lookup"><span data-stu-id="d2607-221">ArchiveDuplicateMessages : True</span></span>

<span data-ttu-id="d2607-222">CachePurgingInterval：24</span><span class="sxs-lookup"><span data-stu-id="d2607-222">CachePurgingInterval : 24</span></span>

<span data-ttu-id="d2607-223">如果 EnableArchiving 属性设置为 False，则表示不会存档任何通信会话。</span><span class="sxs-lookup"><span data-stu-id="d2607-223">If the EnableArchiving property is set to False, that means that no communication sessions will be archived.</span></span> <span data-ttu-id="d2607-224">如果只想存档即时消息会话，请使用如下所示的命令来启用 IM 会话的存档：</span><span class="sxs-lookup"><span data-stu-id="d2607-224">If you want to archive instant messaging sessions only, use a command such as the following to enable the archiving of IM sessions:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="d2607-225">若要将会议会话和即时消息会话存档，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="d2607-225">To archive conferencing sessions and instant messaging sessions, use this command:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="d2607-226">如果你想要将当前存档设置与默认设置进行比较，请运行以下 Windows PowerShell 命令：</span><span class="sxs-lookup"><span data-stu-id="d2607-226">If you’d like to compare your current archiving settings with the default settings, run the following Windows PowerShell command:</span></span>

`New-CsArchivingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d2607-227">该命令将创建全局存档配置设置的仅内存内部实例。</span><span class="sxs-lookup"><span data-stu-id="d2607-227">That command creates an in-memory-only instance of the global archiving configuration settings.</span></span> <span data-ttu-id="d2607-228">这不是由 Lync Server 使用的真实设置集合。</span><span class="sxs-lookup"><span data-stu-id="d2607-228">This is not a real collection of settings that is used by Lync Server.</span></span> <span data-ttu-id="d2607-229">但是，它会显示所有存档配置属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="d2607-229">However, it does display the default values for all the archiving configuration properties.</span></span>

<span data-ttu-id="d2607-230">你还可以使用此命令返回存档服务器的 FQDN：</span><span class="sxs-lookup"><span data-stu-id="d2607-230">You can also use this command to return the FQDN of your Archiving servers:</span></span>

`Get-CsService -ArchivingServer`

<span data-ttu-id="d2607-231">验证已启用存档后，您可以查看存档策略以确定是否正在存档内部和外部通信会话。</span><span class="sxs-lookup"><span data-stu-id="d2607-231">After you have verified that archiving is enabled, you can then view your archiving policies to determine whether internal and external communication sessions are being archived.</span></span>

<span data-ttu-id="d2607-232">可以使用 Get-CsArchivingPolicy cmdlet 检索存档策略信息。</span><span class="sxs-lookup"><span data-stu-id="d2607-232">Archiving policy information can be retrieved by using the Get-CsArchivingPolicy cmdlet.</span></span> <span data-ttu-id="d2607-233">例如，此命令返回有关全局存档策略的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-233">For example, this command returns information about the global archiving policy:</span></span>

`Get-CsArchivingPolicy -Identity "Global"`

<span data-ttu-id="d2607-234">由于还可以在网站和每用户范围内配置存档策略，因此你可能还希望使用此命令，该命令将返回有关所有存档策略的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-234">Because archiving policies can also be configured at the site and the per-user scope, you might also want to use this command, which returns information about all the archiving policies:</span></span>

`Get-CsArchivingPolicy`

<span data-ttu-id="d2607-235">从 Get-CsArchivingPolicy 收到的信息将与以下内容类似：</span><span class="sxs-lookup"><span data-stu-id="d2607-235">The information that you receive from Get-CsArchivingPolicy will resemble this:</span></span>

<span data-ttu-id="d2607-236">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-236">Identity : Global</span></span>

<span data-ttu-id="d2607-237">介绍</span><span class="sxs-lookup"><span data-stu-id="d2607-237">Description :</span></span>

<span data-ttu-id="d2607-238">ArchiveInternal： False</span><span class="sxs-lookup"><span data-stu-id="d2607-238">ArchiveInternal : False</span></span>

<span data-ttu-id="d2607-239">ArchiveExternal： False</span><span class="sxs-lookup"><span data-stu-id="d2607-239">ArchiveExternal : False</span></span>

<span data-ttu-id="d2607-240">请注意，默认情况下，存档策略中禁用内部和外部存档。</span><span class="sxs-lookup"><span data-stu-id="d2607-240">Note that, by default, both internal and external archiving are disabled in an archiving policy.</span></span>

</div>

<div>

## <a name="check-cdr-settings"></a><span data-ttu-id="d2607-241">检查 CDR 设置</span><span class="sxs-lookup"><span data-stu-id="d2607-241">Check CDR settings</span></span>

<span data-ttu-id="d2607-242">查看呼叫详细记录 (对等、会议和语音呼叫详细录制的 CDR) 设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-242">Check Call Detail Record (CDR) settings for peer-to-peer, conferencing, and Voice call detail recording.</span></span> <span data-ttu-id="d2607-243">可通过使用 **CsCdrConfiguration** cmdlet 返回有关 CDR 设置的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d2607-243">Detailed information about your CDR settings can be returned by using the **Get-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="d2607-244">例如，此命令返回有关 CDR 配置设置的全局集合的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-244">For example, this command returns information about the global collection of CDR configuration settings:</span></span>

`Get-CsCdrConfiguration -Identity "Global"`

<span data-ttu-id="d2607-245">由于 CDR 也可以在网站范围内配置，因此你可能还希望运行此命令，该命令将返回有关所有 CDR 配置设置的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-245">Because CDR can also be configured at the site scope, you might also want to run this command, which returns information about all the CDR configuration settings:</span></span>

`Get-CsCdrConfiguration`

<span data-ttu-id="d2607-246">对于每个 CDR 配置设置，Get-CsCdrConfiguration cmdlet 将返回类似以下内容的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-246">The Get-CsCdrConfiguration cmdlet returns information similar to this for each collection of CDR configuration settings:</span></span>

<span data-ttu-id="d2607-247">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-247">Identity : Global</span></span>

<span data-ttu-id="d2607-248">EnableCDR： True</span><span class="sxs-lookup"><span data-stu-id="d2607-248">EnableCDR : True</span></span>

<span data-ttu-id="d2607-249">EnablePurging： True</span><span class="sxs-lookup"><span data-stu-id="d2607-249">EnablePurging : True</span></span>

<span data-ttu-id="d2607-250">KeepCallDetailForDays：60</span><span class="sxs-lookup"><span data-stu-id="d2607-250">KeepCallDetailForDays : 60</span></span>

<span data-ttu-id="d2607-251">KeepErrorReportForDays：60</span><span class="sxs-lookup"><span data-stu-id="d2607-251">KeepErrorReportForDays : 60</span></span>

<span data-ttu-id="d2607-252">PurgeHourOfDay：2</span><span class="sxs-lookup"><span data-stu-id="d2607-252">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="d2607-253">通过使用 Get-CsQoEConfiguration cmdlet，可以为 QoE 监视返回类似信息。</span><span class="sxs-lookup"><span data-stu-id="d2607-253">Similar information can be returned for QoE monitoring by using the Get-CsQoEConfiguration cmdlet.</span></span> <span data-ttu-id="d2607-254">例如，此命令返回有关 QoE 配置设置的全局集合的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-254">For example, this command returns information about the global collection of QoE configuration settings:</span></span>

`Get-QoEConfiguration -Identity "Global"`

<span data-ttu-id="d2607-255">该信息将如下所示：</span><span class="sxs-lookup"><span data-stu-id="d2607-255">That information will resemble this:</span></span>

<span data-ttu-id="d2607-256">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-256">Identity : Global</span></span>

<span data-ttu-id="d2607-257">ExternalConsumerIssuedCertId :</span><span class="sxs-lookup"><span data-stu-id="d2607-257">ExternalConsumerIssuedCertId :</span></span>

<span data-ttu-id="d2607-258">EnablePurging： True</span><span class="sxs-lookup"><span data-stu-id="d2607-258">EnablePurging : True</span></span>

<span data-ttu-id="d2607-259">KeepQoEDataForDays：60</span><span class="sxs-lookup"><span data-stu-id="d2607-259">KeepQoEDataForDays : 60</span></span>

<span data-ttu-id="d2607-260">PurgeHourOfDay：1</span><span class="sxs-lookup"><span data-stu-id="d2607-260">PurgeHourOfDay : 1</span></span>

<span data-ttu-id="d2607-261">EnableExternalConsumer： False</span><span class="sxs-lookup"><span data-stu-id="d2607-261">EnableExternalConsumer : False</span></span>

<span data-ttu-id="d2607-262">ExternalConsumerName :</span><span class="sxs-lookup"><span data-stu-id="d2607-262">ExternalConsumerName :</span></span>

<span data-ttu-id="d2607-263">ExternalConsumerURL :</span><span class="sxs-lookup"><span data-stu-id="d2607-263">ExternalConsumerURL :</span></span>

<span data-ttu-id="d2607-264">EnableQoE： True</span><span class="sxs-lookup"><span data-stu-id="d2607-264">EnableQoE : True</span></span>

<span data-ttu-id="d2607-265">如果要将当前 CDR 设置与默认的 CDR 设置进行比较，可以通过运行以下命令来查看默认值：</span><span class="sxs-lookup"><span data-stu-id="d2607-265">If you want to compare your current CDR settings with the default CDR settings, the default values can be reviewed by running this command:</span></span>

`New-CsCdrConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d2607-266">同样，可以使用以下命令检索 QoE 监视的默认值：</span><span class="sxs-lookup"><span data-stu-id="d2607-266">Likewise, the default values for QoE monitoring can be retrieved by using this command:</span></span>

`New-CsQoEConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d2607-267">您也可以通过运行以下命令返回监视服务器的 FQDN：</span><span class="sxs-lookup"><span data-stu-id="d2607-267">You can also return the FQDN of your Monitoring servers by running this command:</span></span>

`Get-CsService -MonitoringServer`

</div>

<div>

## <a name="check-voice-settings"></a><span data-ttu-id="d2607-268">检查语音设置</span><span class="sxs-lookup"><span data-stu-id="d2607-268">Check voice settings</span></span>

<span data-ttu-id="d2607-269">语音设置通常对管理员非常重要，因为它包含在语音策略和语音路由中：语音策略包含确定向单个用户显示的功能的设置 (例如转发或转移) 呼叫的功能，而语音路由 (决定) 呼叫是否通过 PSTN 路由。</span><span class="sxs-lookup"><span data-stu-id="d2607-269">The voice settings typically important to administrators are contained in voice policies and voice routes: voice policies contain the settings that determine the capabilities exposed to individual users (such as the ability to forward or transfer calls), while voice routes determine how (and if) calls are routed across the PSTN.</span></span>

<span data-ttu-id="d2607-270">可以使用 Windows PowerShell 检索语音策略信息。</span><span class="sxs-lookup"><span data-stu-id="d2607-270">Voice policy information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="d2607-271">例如，此命令返回有关全局语音策略的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-271">For example, this command returns information about the global voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global"`

<span data-ttu-id="d2607-272">此命令将返回有关已配置为在组织中使用的所有语音策略的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-272">And this command returns information about all the voice policies configured for use in the organization:</span></span>

`Get-CsVoicePolicy`

<span data-ttu-id="d2607-273">Get-CsVoicePolicy cmdlet 返回的信息如下所示：</span><span class="sxs-lookup"><span data-stu-id="d2607-273">The information returned by the Get-CsVoicePolicy cmdlet resembles the following:</span></span>

<span data-ttu-id="d2607-274">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-274">Identity : Global</span></span>

<span data-ttu-id="d2607-275">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="d2607-275">PstnUsages : {}</span></span>

<span data-ttu-id="d2607-276">介绍</span><span class="sxs-lookup"><span data-stu-id="d2607-276">Description :</span></span>

<span data-ttu-id="d2607-277">AllowSimulRing： True</span><span class="sxs-lookup"><span data-stu-id="d2607-277">AllowSimulRing : True</span></span>

<span data-ttu-id="d2607-278">AllowCallForwarding： True</span><span class="sxs-lookup"><span data-stu-id="d2607-278">AllowCallForwarding : True</span></span>

<span data-ttu-id="d2607-279">AllowPSTNReRouting： True</span><span class="sxs-lookup"><span data-stu-id="d2607-279">AllowPSTNReRouting : True</span></span>

<span data-ttu-id="d2607-280">名称： DefaultPolicy</span><span class="sxs-lookup"><span data-stu-id="d2607-280">Name : DefaultPolicy</span></span>

<span data-ttu-id="d2607-281">EnableDelegation： True</span><span class="sxs-lookup"><span data-stu-id="d2607-281">EnableDelegation : True</span></span>

<span data-ttu-id="d2607-282">EnableTeamCall： True</span><span class="sxs-lookup"><span data-stu-id="d2607-282">EnableTeamCall : True</span></span>

<span data-ttu-id="d2607-283">EnableCallTransfer： True</span><span class="sxs-lookup"><span data-stu-id="d2607-283">EnableCallTransfer : True</span></span>

<span data-ttu-id="d2607-284">EnableCallPark： False</span><span class="sxs-lookup"><span data-stu-id="d2607-284">EnableCallPark : False</span></span>

<span data-ttu-id="d2607-285">EnableMaliciousCallTracing： False</span><span class="sxs-lookup"><span data-stu-id="d2607-285">EnableMaliciousCallTracing : False</span></span>

<span data-ttu-id="d2607-286">EnableBWPolicyOverride： False</span><span class="sxs-lookup"><span data-stu-id="d2607-286">EnableBWPolicyOverride : False</span></span>

<span data-ttu-id="d2607-287">PreventPSTNTollBypass： False</span><span class="sxs-lookup"><span data-stu-id="d2607-287">PreventPSTNTollBypass : False</span></span>

<span data-ttu-id="d2607-288">您还可以创建返回您的语音策略子集的查询。</span><span class="sxs-lookup"><span data-stu-id="d2607-288">You can also create queries that returned a subset of your voice policies.</span></span> <span data-ttu-id="d2607-289">例如，此命令返回允许呼叫转接的所有语音策略：</span><span class="sxs-lookup"><span data-stu-id="d2607-289">For example, this command returns all the voice policies that allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $True}`

<span data-ttu-id="d2607-290">此命令将返回不允许呼叫转接的所有语音策略：</span><span class="sxs-lookup"><span data-stu-id="d2607-290">And this command returns all the voice policies that don’t allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $False}`

<span data-ttu-id="d2607-291">在 Windows PowerShell 中，使用 Get-CsVoiceRouting cmdlet 返回有关语音路由的信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-291">In Windows PowerShell, use the Get-CsVoiceRouting cmdlet to return information about your voice routes:</span></span>

`Get-CsVoiceRoute`

<span data-ttu-id="d2607-292">该命令将为所有语音路线返回如下信息：</span><span class="sxs-lookup"><span data-stu-id="d2607-292">That command returns information such as this for all the voice routes:</span></span>

<span data-ttu-id="d2607-293">标识： LocalRoute</span><span class="sxs-lookup"><span data-stu-id="d2607-293">Identity : LocalRoute</span></span>

<span data-ttu-id="d2607-294">优先级：0</span><span class="sxs-lookup"><span data-stu-id="d2607-294">Priority : 0</span></span>

<span data-ttu-id="d2607-295">介绍</span><span class="sxs-lookup"><span data-stu-id="d2607-295">Description :</span></span>

<span data-ttu-id="d2607-296">NumberPattern： ^ (\\ + 1 \[ 0-9 \] {10}) $</span><span class="sxs-lookup"><span data-stu-id="d2607-296">NumberPattern : ^(\\+1\[0-9\]{10})$</span></span>

<span data-ttu-id="d2607-297">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="d2607-297">PstnUsages : {}</span></span>

<span data-ttu-id="d2607-298">PstnGatewayList : {}</span><span class="sxs-lookup"><span data-stu-id="d2607-298">PstnGatewayList : {}</span></span>

<span data-ttu-id="d2607-299">名称： LocalRoute</span><span class="sxs-lookup"><span data-stu-id="d2607-299">Name : LocalRoute</span></span>

<span data-ttu-id="d2607-300">SuppressCallerId :</span><span class="sxs-lookup"><span data-stu-id="d2607-300">SuppressCallerId :</span></span>

<span data-ttu-id="d2607-301">AlternateCallerId :</span><span class="sxs-lookup"><span data-stu-id="d2607-301">AlternateCallerId :</span></span>

<span data-ttu-id="d2607-302">Lync Server 允许你创建没有 PSTN 使用的语音路由，不指定 PSTN 网关。</span><span class="sxs-lookup"><span data-stu-id="d2607-302">Lync Server allows you to create voice routes that do not have a PSTN usage and do not specify a PSTN gateway.</span></span> <span data-ttu-id="d2607-303">但是，您实际上无法通过没有配置这两个属性值的语音路线路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="d2607-303">However, you can't actually route calls over a voice route that does not have these two property values configured.</span></span> <span data-ttu-id="d2607-304">出于此原因，你可能会发现定期运行此命令非常有用，该命令将返回没有 PSTN 使用的任何语音路由的标识：</span><span class="sxs-lookup"><span data-stu-id="d2607-304">Because of that, you might find it useful to periodically run this command, which returns the identity of any voice route that does not have a PSTN usage:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnUsages -eq $Null} | Select-Object Identity`

<span data-ttu-id="d2607-305">同样，此命令返回尚未配置为具有 PSTN 网关的任何语音路由的标识：</span><span class="sxs-lookup"><span data-stu-id="d2607-305">Similarly, this command returns the identity of any voice route that has not been configured to have a PSTN gateway:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnGatewayList -eq $Null}} | Select-Object Identity`

</div>

<div>

## <a name="check-conferencing-attendant-settings"></a><span data-ttu-id="d2607-306">检查会议助理设置</span><span class="sxs-lookup"><span data-stu-id="d2607-306">Check Conferencing Attendant settings</span></span>

<span data-ttu-id="d2607-307">检查 PSTN 电话拨入式会议的会议助理设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-307">Check conferencing Attendant settings for PSTN dial-in conferencing.</span></span> <span data-ttu-id="d2607-308">只能使用 **CsDialInConferencingConfiguration** cmdlet 来检索会议助理设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-308">Conferencing Attendant settings can only be retrieved by using the **Get-CsDialInConferencingConfiguration** cmdlet.</span></span> <span data-ttu-id="d2607-309">这些设置在 Lync Server "控制面板" 中不可用。</span><span class="sxs-lookup"><span data-stu-id="d2607-309">These settings are not available in the Lync Server Control Panel.</span></span> <span data-ttu-id="d2607-310">若要查看会议助理设置，请使用与以下内容类似的 Windows PowerShell 命令，它可返回全局会议助理设置的全局集合：</span><span class="sxs-lookup"><span data-stu-id="d2607-310">To view your Conferencing Attendant settings, use a Windows PowerShell command similar to the following, which returns the global collection of Conferencing Attendant settings:</span></span>

`Get-CsDialInConferencingConfiguration -Identity "Global"`

<span data-ttu-id="d2607-311">请注意，还可以在网站范围内配置会议助理设置。</span><span class="sxs-lookup"><span data-stu-id="d2607-311">Note that Conferencing Attendant settings can also be configured at the site scope.</span></span> <span data-ttu-id="d2607-312">若要返回有关所有会议助理设置的信息，请改用此命令：</span><span class="sxs-lookup"><span data-stu-id="d2607-312">To return information about all the Conferencing Attendant settings, use this command instead:</span></span>

`Get-CsDialInConferencingConfiguration`

<span data-ttu-id="d2607-313">Get-CsDialInConferencingConfiguration cmdlet 返回与以下内容类似的数据：</span><span class="sxs-lookup"><span data-stu-id="d2607-313">The Get-CsDialInConferencingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="d2607-314">标识：全局</span><span class="sxs-lookup"><span data-stu-id="d2607-314">Identity : Global</span></span>

<span data-ttu-id="d2607-315">EntryExitAnnouncementsType : UseNames</span><span class="sxs-lookup"><span data-stu-id="d2607-315">EntryExitAnnouncementsType : UseNames</span></span>

<span data-ttu-id="d2607-316">EnableNameRecording： True</span><span class="sxs-lookup"><span data-stu-id="d2607-316">EnableNameRecording : True</span></span>

<span data-ttu-id="d2607-317">EntryExitAnnouncementsEnabledByDefault： False</span><span class="sxs-lookup"><span data-stu-id="d2607-317">EntryExitAnnouncementsEnabledByDefault : False</span></span>

<span data-ttu-id="d2607-318">如果 EntryExitAnnouncementsEnabledByDefault 设置为 False，则表示已禁用会议通知。</span><span class="sxs-lookup"><span data-stu-id="d2607-318">If EntryExitAnnouncementsEnabledByDefault is set to False, that means the conferencing announcements are disabled.</span></span> <span data-ttu-id="d2607-319">若要启用进入和退出通知，请运行如下所示的 Windows PowerShell 命令：</span><span class="sxs-lookup"><span data-stu-id="d2607-319">To enable entry and exit announcements, run a Windows PowerShell command similar to this:</span></span>

`Set-CsDialInConferencingConfiguration -Identity "Global" -EntryExitAnnouncementsEnabledByDefault $True`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d2607-320">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2607-320">See Also</span></span>


[<span data-ttu-id="d2607-321">Get-CsSipDomain</span><span class="sxs-lookup"><span data-stu-id="d2607-321">Get-CsSipDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsSipDomain)  
[<span data-ttu-id="d2607-322">Get-CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2607-322">Get-CsMeetingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration)  
[<span data-ttu-id="d2607-323">CsService</span><span class="sxs-lookup"><span data-stu-id="d2607-323">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="d2607-324">CsAccessEdgeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2607-324">Get-CsAccessEdgeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAccessEdgeConfiguration)  
[<span data-ttu-id="d2607-325">CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d2607-325">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="d2607-326">CsArchivingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2607-326">Get-CsArchivingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsArchivingConfiguration)  
[<span data-ttu-id="d2607-327">CsCdrConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2607-327">Get-CsCdrConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration)  
[<span data-ttu-id="d2607-328">CsQoEConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2607-328">Get-CsQoEConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsQoEConfiguration)  
[<span data-ttu-id="d2607-329">CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="d2607-329">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="d2607-330">CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="d2607-330">Get-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoiceRoute)  
[<span data-ttu-id="d2607-331">Get-CsDialInConferencingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2607-331">Get-CsDialInConferencingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingConfiguration)  
  

<span data-ttu-id="d2607-332"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2607-332"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

