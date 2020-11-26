---
title: Lync Server 2013：使用媒体旁路配置主干
description: Lync Server 2013：使用 "媒体绕过" 配置中继。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trunk with media bypass
ms:assetid: 99d729ea-5a4c-4ff2-a4a3-93a24368da6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398792(v=OCS.15)
ms:contentKeyID: 48184959
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51bd58a685e1f4c222a863c21022b3c9dc7c70d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434159"
---
# <a name="configure-a-trunk-with-media-bypass-in-lync-server-2013"></a><span data-ttu-id="5d077-103">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d077-103">Configure a trunk with media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d077-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d077-104">

<span> </span></span></span>

<span data-ttu-id="5d077-105">_**主题上次修改时间：** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="5d077-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="5d077-106">执行以下步骤可配置启用媒体旁路的中继。</span><span class="sxs-lookup"><span data-stu-id="5d077-106">Follow these steps to configure a trunk with media bypass enabled.</span></span> <span data-ttu-id="5d077-107">若要在禁用媒体旁路的情况下配置主干，请参阅 [在 Lync Server 2013 中不使用媒体旁路配置主干](lync-server-2013-configure-a-trunk-without-media-bypass.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-107">To configure a trunk with media bypass disabled, see [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md).</span></span> <span data-ttu-id="5d077-108">当您想要最大程度地减少已部署中介服务器的数量时，媒体绕过非常有用。</span><span class="sxs-lookup"><span data-stu-id="5d077-108">Media bypass is useful when you want to minimize the number of Mediation Servers deployed.</span></span> <span data-ttu-id="5d077-109">通常，将在中心网站上部署中介服务器池，并且它将控制分支站点上的网关。</span><span class="sxs-lookup"><span data-stu-id="5d077-109">Typically, a Mediation Server pool will be deployed at a central site, and it will control gateways at branch sites.</span></span> <span data-ttu-id="5d077-110">启用媒体旁路后，来自分支站点中客户端的公用电话交换网 (PSTN) 呼叫的媒体可直接通过这些站点中的网关流动。</span><span class="sxs-lookup"><span data-stu-id="5d077-110">Enabling media bypass allows media for public switched telephone network (PSTN) calls from clients at branch sites to flow directly through the gateways at those sites.</span></span> <span data-ttu-id="5d077-111">必须正确配置 Lync Server 2013 出站呼叫路由和企业语音策略，以便将来自分支站点的客户端的 PSTN 呼叫路由到相应的网关。</span><span class="sxs-lookup"><span data-stu-id="5d077-111">Lync Server 2013 outbound call routes and Enterprise Voice policies must be properly configured so that PSTN calls from clients at a branch site are routed to the appropriate gateway.</span></span>

<span data-ttu-id="5d077-112">强烈建议您启用媒体旁路。</span><span class="sxs-lookup"><span data-stu-id="5d077-112">We strongly recommend that you enable media bypass.</span></span> <span data-ttu-id="5d077-113">但是在 SIP 中继上启用媒体旁路之前，请确认您的合格 SIP 中继提供商是否支持媒体旁路且能够满足成功启用方案的要求。</span><span class="sxs-lookup"><span data-stu-id="5d077-113">However, before you enable media bypass on a SIP trunk, confirm that your qualified SIP trunk provider supports media bypass and is able to accommodate the requirements for successfully enabling the scenario.</span></span> <span data-ttu-id="5d077-114">具体而言，提供商必须有您组织内部网络中的服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="5d077-114">Specifically, the provider must have the IP addresses of servers in your organization’s internal network.</span></span> <span data-ttu-id="5d077-115">如果提供程序无法支持此方案，则媒体绕过将不会成功。</span><span class="sxs-lookup"><span data-stu-id="5d077-115">If the provider cannot support this scenario, media bypass will not succeed.</span></span> <span data-ttu-id="5d077-116">有关详细信息，请参阅规划文档中的在 [Lync Server 2013 中规划媒体旁路](lync-server-2013-planning-for-media-bypass.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d077-116">For details, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5d077-117">媒体旁路不能与每个公共交换电话网络（ (PSTN) 网关、IP PBX 和会话边界控制器 (SBC) 进行互操作。</span><span class="sxs-lookup"><span data-stu-id="5d077-117">Media bypass will not interoperate with every public switched telephone network (PSTN) gateway, IP-PBX, and Session Border Controller (SBC).</span></span> <span data-ttu-id="5d077-118">Microsoft 与认证合作伙伴一起对一组 PSTN 网关和 SBC 进行了测试，另外也对 Cisco IP-PBX 进行了一些测试。</span><span class="sxs-lookup"><span data-stu-id="5d077-118">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="5d077-119">只有在统一通信打开的互操作性计划（Lync Server）上列出的产品和版本才支持媒体绕过 <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A> 。</span><span class="sxs-lookup"><span data-stu-id="5d077-119">Media bypass is supported only with products and versions that are listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A>.</span></span>



</div>

<span data-ttu-id="5d077-p104">如下所述的中继组合了一组应用于分配了此中继配置的中继的参数。可以将特定的中继配置的范围限定为全局（没有更特定的站点或池配置的所有中继）、一个站点或一个池。池级别中继配置用于将特定中继配置的范围限定为单个中继。</span><span class="sxs-lookup"><span data-stu-id="5d077-p104">A trunk configuration as described below groups a set of parameters that are applied to trunks assigned this trunk configuration. A particular trunk configuration can be scoped globally (to all trunks that do not have more specific site or pool configuration), or to a site, or to a pool. The pool-level trunk configuration is used to scope a specific trunk configuration to a single trunk.</span></span>

<span id="BKMK_ConfigTrunkMediaBypassSteps"></span>

<div>

## <a name="to-configure-a-trunk-with-media-bypass"></a><span data-ttu-id="5d077-123">配置带媒体旁路的中继</span><span class="sxs-lookup"><span data-stu-id="5d077-123">To configure a trunk with media bypass</span></span>

1.  <span data-ttu-id="5d077-124">以 RTCUniversalServerAdmins 组成员的身份或者以 CsVoiceAdministrator、CsServerAdministrator 或 CsAdministrator 角色成员的身份登录计算机。</span><span class="sxs-lookup"><span data-stu-id="5d077-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="5d077-125">有关详细信息，请参阅 [在 Lync Server 2013 中委派设置权限](lync-server-2013-delegate-setup-permissions.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-125">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="5d077-126">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="5d077-126">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5d077-127">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-127">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5d077-128">在左侧导航栏中，单击“语音路由”，然后单击“Trunk 配置”。</span><span class="sxs-lookup"><span data-stu-id="5d077-128">In the left navigation bar, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

4.  <span data-ttu-id="5d077-129">在“Trunk 配置”页上，使用以下方法之一配置中继：</span><span class="sxs-lookup"><span data-stu-id="5d077-129">On the **Trunk Configuration** page, use one of the following methods to configure a trunk:</span></span>
    
      - <span data-ttu-id="5d077-130">双击某个现有的中继（例如“全局”中继）以显示“编辑 Trunk 配置”对话框。</span><span class="sxs-lookup"><span data-stu-id="5d077-130">Double-click an existing trunk (for example, the **Global** trunk) to display the **Edit Trunk Configuration** dialog box.</span></span>
    
      - <span data-ttu-id="5d077-131">单击“新建”，然后为新的中继配置选择范围：</span><span class="sxs-lookup"><span data-stu-id="5d077-131">Click **New**, and then select a scope for the new trunk configuration:</span></span>
        
          - <span data-ttu-id="5d077-132">**网站主干：** 从 " **选择网站**" 中选择此中继配置的网站，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="5d077-132">**Site trunk:** Choose the site for this trunk configuration from **Select a Site**, and then click **OK**.</span></span> <span data-ttu-id="5d077-133">请注意，如果已经为站点创建了中继配置，则该站点不会显示在“选择站点”中。</span><span class="sxs-lookup"><span data-stu-id="5d077-133">Note that if a trunk configuration has already been created for a site, the site does not appear in **Select a Site**.</span></span> <span data-ttu-id="5d077-134">此中继配置将应用于站点中的所有中继。</span><span class="sxs-lookup"><span data-stu-id="5d077-134">This trunk configuration will be applied to all trunks in the site.</span></span>
        
          - <span data-ttu-id="5d077-135">**池干线：** 选择此中继配置适用的主干的名称。</span><span class="sxs-lookup"><span data-stu-id="5d077-135">**Pool trunk:** Choose the name of the trunk that this trunk configuration applies to.</span></span> <span data-ttu-id="5d077-136">此主干可以是 "根主干" 或 "拓扑生成器" 中定义的任何其他中继。</span><span class="sxs-lookup"><span data-stu-id="5d077-136">This trunk can be the root trunk or any additional trunks defined in Topology Builder.</span></span> <span data-ttu-id="5d077-137">从“选择服务”中，单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5d077-137">From **Select a Service**, click **OK**.</span></span> <span data-ttu-id="5d077-138">请注意，如果已为特定中继创建中继配置，则此中继不会显示在“选择服务”中。</span><span class="sxs-lookup"><span data-stu-id="5d077-138">Note that if a trunk configuration has already been created for a specific trunk, the trunk does not appear in **Select a Service**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5d077-139">选择中继配置的范围后无法更改该范围。</span><span class="sxs-lookup"><span data-stu-id="5d077-139">After you select the scope of the trunk configuration, it cannot be changed.</span></span><BR><span data-ttu-id="5d077-140">“名称”<STRONG></STRONG>字段会使用中继配置的关联站点或服务的名称进行预填充，且不能更改。</span><span class="sxs-lookup"><span data-stu-id="5d077-140">The <STRONG>Name</STRONG> field is prepopulated with the name of the trunk configuration’s associated site or service and cannot be changed.</span></span>

    
    </div>

5.  <span data-ttu-id="5d077-p109">在“支持的最大早期对话数”中指定一个值。这是公用电话交换网 (PSTN) 网关、IP-PBX 或 ITSP 会话边界控制器 (SBC) 可以接收的分叉响应的最大数目，这些响应针对的是发送到中介服务器的邀请。默认值为 20。</span><span class="sxs-lookup"><span data-stu-id="5d077-p109">Specify a value in **Maximum early dialogs supported**. This is the maximum number of forked responses a public switched telephone network (PSTN) gateway, IP-PBX, or ITSP Session Border Controller (SBC) can receive to an INVITE that it sent to the Mediation Server. The default value is 20.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5d077-144">在更改此值之前，请咨询您的服务提供商或设备制造商，以了解有关所用系统功能的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5d077-144">Before you change this value, consult your service provider or equipment manufacturer for details about the capabilities of your system.</span></span>

    
    </div>

6.  <span data-ttu-id="5d077-145">选择以下“加密支持级别”选项之一：</span><span class="sxs-lookup"><span data-stu-id="5d077-145">Select one of the following **Encryption support level** options:</span></span>
    
      - <span data-ttu-id="5d077-146">**必需：** 安全实时传输协议 (SRTP) 加密必须用于帮助保护中介服务器与网关或专用分支 exchange (PBX) 之间的流量。</span><span class="sxs-lookup"><span data-stu-id="5d077-146">**Required:** Secure real-time transport protocol (SRTP) encryption must be used to help protect traffic between the Mediation Server and the gateway or private branch exchange (PBX).</span></span>
    
      - <span data-ttu-id="5d077-147">**可选：** 如果服务提供商或设备制造商支持，则使用 SRTP 加密。</span><span class="sxs-lookup"><span data-stu-id="5d077-147">**Optional:** SRTP encryption will be used if the service provider or equipment manufacturer supports it.</span></span>
    
      - <span data-ttu-id="5d077-148">**不支持：** SRTP 加密不受服务提供商或设备制造商支持，因此不会使用。</span><span class="sxs-lookup"><span data-stu-id="5d077-148">**Not Supported:** SRTP encryption is not supported by the service provider or equipment manufacturer and therefore will not be used.</span></span>

7.  <span data-ttu-id="5d077-149">如果您要绕过中介服务器而通过中继对等方处理媒体，请选中“启用媒体旁路”复选框。</span><span class="sxs-lookup"><span data-stu-id="5d077-149">Select the **Enable media bypass** check box if you want media to bypass the Mediation Server for processing by the trunk peer.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5d077-150">为使媒体旁路功能成功发挥作用，PSTN 网关、IP-PBX 或 ITSP 会话边界控制器必须支持某些功能。</span><span class="sxs-lookup"><span data-stu-id="5d077-150">For media bypass to work successfully, the PSTN gateway, IP-PBX, or ITSP Session Border Controller must support certain capabilities.</span></span> <span data-ttu-id="5d077-151">有关详细信息，请参阅规划文档中的在 <A href="lync-server-2013-planning-for-media-bypass.md">Lync Server 2013 中规划媒体旁路</A> 。</span><span class="sxs-lookup"><span data-stu-id="5d077-151">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>

8.  <span data-ttu-id="5d077-p111">如果存在一个已知的媒体端点（例如 PSTN 网关，其中媒体终端与信号终端具有相同的 IP），则选中“集中式媒体处理”复选框。如果中继没有已知的媒体端点，则清除该复选框。</span><span class="sxs-lookup"><span data-stu-id="5d077-p111">Select the **Centralized media processing** check box if there is a well-known media termination point (for example, a PSTN gateway where the media termination has the same IP as the signaling termination). Clear this check box if the trunk does not have a well-known media termination point.</span></span>

9.  <span data-ttu-id="5d077-154">如果中继对等支持接收来自中介服务器的 SIP，请选中 " **启用发送指向网关** 的请求" 复选框。</span><span class="sxs-lookup"><span data-stu-id="5d077-154">If the trunk peer supports receiving SIP REFER requests from the Mediation Server, select the **Enable sending refer to the gateway** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5d077-155">如果禁用此选项而选中“启用媒体旁路”<STRONG></STRONG>选项，则需要其他设置。</span><span class="sxs-lookup"><span data-stu-id="5d077-155">If you disable this option while the <STRONG>Enable media bypass</STRONG> option is selected, additional settings are required.</span></span> <span data-ttu-id="5d077-156">如果中继对等方不支持接收来自中介服务器的 SIP REFER 请求且启用了媒体旁路，则为了支持媒体旁路的适当条件，还必须运行 <STRONG>Set-CsTrunkConfiguration</STRONG> cmdlet 以禁用活动呼叫和保留呼叫的 RTCP。</span><span class="sxs-lookup"><span data-stu-id="5d077-156">If the trunk peer does not support receiving SIP REFER requests from the Mediation Server and media bypass is enabled, you must also run the <STRONG>Set-CsTrunkConfiguration</STRONG> cmdlet to disable RTCP for active and held calls in order to support proper conditions for media bypass.</span></span> <span data-ttu-id="5d077-157">有关详细信息，请参阅 <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 管理外壳</A> 文档。</span><span class="sxs-lookup"><span data-stu-id="5d077-157">For details, see the <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 Management Shell</A> documentation.</span></span><BR><span data-ttu-id="5d077-158">此外，如果您希望转移的呼叫传输支持媒体旁路，并且网关不支持 SIP REFER 请求，则您可以选择“允许使用第三方呼叫控制的引用”<STRONG></STRONG>。</span><span class="sxs-lookup"><span data-stu-id="5d077-158">Alternatively, you can select <STRONG>Enable refer using third-party-call control</STRONG> if you want transferred calls to be media bypassed, and the gateway does not support SIP REFER requests.</span></span>

    
    </div>

10. <span data-ttu-id="5d077-159">（可选）若要启用中继间路由，请将 PSTN 用法记录关联到此中继配置并进行相应的配置。</span><span class="sxs-lookup"><span data-stu-id="5d077-159">(Optional) To enable inter-trunk routing, associate and configure PSTN usage records to this trunk configuration.</span></span> <span data-ttu-id="5d077-160">与此干线配置关联的 PSTN 用法将应用于所有传入呼叫，该主干不是从 Lync 终结点发起的。</span><span class="sxs-lookup"><span data-stu-id="5d077-160">The PSTN usages associated to this trunk configuration will be applied for all incoming calls through the trunk that is not originating from a Lync endpoint.</span></span> <span data-ttu-id="5d077-161">若要管理与中继配置关联的 PSTN 用法记录，请使用下列方法之一：</span><span class="sxs-lookup"><span data-stu-id="5d077-161">To manage PSTN usage records associated to a trunk configuration, use one of the following methods:</span></span>
    
      - <span data-ttu-id="5d077-162">若要从您的企业语音部署中可用的所有 PSTN 使用记录列表中选择一个或多个记录，请单击 " **选择**"。</span><span class="sxs-lookup"><span data-stu-id="5d077-162">To select one or more records from a list of all PSTN usage records available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="5d077-163">突出显示要与此中继配置关联的记录，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5d077-163">Highlight the records you want to associate with this trunk configuration and then click **OK**.</span></span>
    
      - <span data-ttu-id="5d077-164">要删除此中继配置中的某个 PSTN 用法记录，请选择此记录，并单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="5d077-164">To remove a PSTN usage record from this trunk configuration, select the record and click **Remove**.</span></span>
    
      - <span data-ttu-id="5d077-165">要定义新的 PSTN 用法记录并将其与此中继配置相关联，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="5d077-165">To define a new PSTN usage record and associate it with this trunk configuration, do the following:</span></span>
        
        1.  <span data-ttu-id="5d077-166">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5d077-166">Click **New**.</span></span>
        
        2.  <span data-ttu-id="5d077-167">在“名称”字段中，为记录指定唯一的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="5d077-167">In the **Name** field, specify a descriptive name for the record that is unique.</span></span>
            
            <div>
            

            > [!NOTE]  
            > <span data-ttu-id="5d077-p115">PSTN 用法记录名称在企业语音部署中必须是唯一的。保存记录后，将无法编辑“名称”<STRONG></STRONG>字段。</span><span class="sxs-lookup"><span data-stu-id="5d077-p115">The PSTN usage record name must be unique within the Enterprise Voice deployment. After the record is saved, the <STRONG>Name</STRONG> field cannot be edited.</span></span>

            
            </div>
        
        3.  <span data-ttu-id="5d077-170">使用下列方法之一为此 PSTN 用法记录关联和配置路由：</span><span class="sxs-lookup"><span data-stu-id="5d077-170">Use one of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="5d077-171">若要从您的企业语音部署中的所有可用路由列表中选择一个或多个路由，请单击 " **选择**"。</span><span class="sxs-lookup"><span data-stu-id="5d077-171">To select one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="5d077-172">突出显示要与此 PSTN 用法记录相关联的路由，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5d077-172">Highlight the routes you want to associate with this PSTN usage record, and click **OK**.</span></span>
            
              - <span data-ttu-id="5d077-173">要删除 PSTN 用法记录中的某个路由，请选择此路由，然后单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="5d077-173">To remove a route from the PSTN usage record, select the route, and click **Remove**.</span></span>
            
              - <span data-ttu-id="5d077-174">要定义新路由并将其与此 PSTN 用法记录相关联，请单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5d077-174">To define a new route and associate it to this PSTN usage record, click **New**.</span></span> <span data-ttu-id="5d077-175">有关详细信息，请参阅 [在 Lync Server 2013 中创建语音路由](lync-server-2013-create-a-voice-route.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-175">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="5d077-176">要编辑与此 PSTN 用法记录相关联的路由，请选择此路由，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="5d077-176">To edit a route that is associated with this PSTN usage record, select the route, and click **Show details**.</span></span> <span data-ttu-id="5d077-177">有关详细信息，请参阅 [在 Lync Server 2013 中修改语音路由](lync-server-2013-modify-a-voice-route.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-177">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        4.  <span data-ttu-id="5d077-178">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="5d077-178">Click **OK**.</span></span>
    
      - <span data-ttu-id="5d077-179">要编辑已经与此中继配置相关联的 PSTN 用法记录，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="5d077-179">To edit a PSTN usage record that is already associated with this trunk configuration, do the following:</span></span>
        
        1.  <span data-ttu-id="5d077-180">选择要编辑的 PSTN 用法记录，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="5d077-180">Select the PSTN usage record you want to edit, and click **Show details**.</span></span>
        
        2.  <span data-ttu-id="5d077-181">使用下列方法之一为此 PSTN 用法记录关联和配置路由：</span><span class="sxs-lookup"><span data-stu-id="5d077-181">Use one of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="5d077-182">若要从您的企业语音部署中的所有可用路由列表中选择一个或多个路由，请单击 " **选择**"。</span><span class="sxs-lookup"><span data-stu-id="5d077-182">To select one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="5d077-183">突出显示要与此 PSTN 用法记录相关联的路由，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5d077-183">Highlight the routes you want to associate with this PSTN usage record, and click **OK**.</span></span>
            
              - <span data-ttu-id="5d077-184">要删除 PSTN 用法记录中的某个路由，请选择此路由，然后单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="5d077-184">To remove a route from the PSTN usage record, select the route, and click **Remove**.</span></span>
            
              - <span data-ttu-id="5d077-185">要定义新路由并将其与此 PSTN 用法记录相关联，请单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5d077-185">To define a new route and associate it to this PSTN usage record, click **New**.</span></span> <span data-ttu-id="5d077-186">有关详细信息，请参阅 [在 Lync Server 2013 中创建语音路由](lync-server-2013-create-a-voice-route.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-186">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="5d077-187">要编辑与此 PSTN 用法记录相关联的路由，请选择此路由，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="5d077-187">To edit a route that is associated with this PSTN usage record, select the route, and click **Show details**.</span></span> <span data-ttu-id="5d077-188">有关详细信息，请参阅 [在 Lync Server 2013 中修改语音路由](lync-server-2013-modify-a-voice-route.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-188">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        3.  <span data-ttu-id="5d077-189">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="5d077-189">Click **OK**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5d077-190">根据与正在配置的主干相关联的中介服务器对，关联 PSTN 使用记录非常重要。</span><span class="sxs-lookup"><span data-stu-id="5d077-190">It important to associate PSTN usage records according to the Mediation Server peer that is associated to the trunk being configured.</span></span> <span data-ttu-id="5d077-191">如果中介服务器对等是 PSTN 网关或 (SBC) 的会话边界控制器，强烈建议不要将 trunk 配置与路由到 PSTN 目标或通过 Lync Server 连接的任何其他下游系统的 PSTN 使用记录相关联。</span><span class="sxs-lookup"><span data-stu-id="5d077-191">If the Mediation Server peer is a PSTN gateway or a Session Border Controller (SBC), it is strongly recommended that the trunk configuration is not associated to a PSTN usage record that routes to a PSTN destination or any other downstream systems connected via Lync Server.</span></span>

    
    </div>

11. <span data-ttu-id="5d077-p123">排列 PSTN 用法记录以获得最佳性能。要更改记录在列表中的位置，请选择 PSTN 用法记录，并单击向上箭头或向下箭头。</span><span class="sxs-lookup"><span data-stu-id="5d077-p123">Arrange the PSTN usage records for optimum performance. To change a record’s position in the list, select the PSTN usage record, and click the up or down arrows.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5d077-194">PSTN 用法记录在中继配置中列出的顺序很重要。</span><span class="sxs-lookup"><span data-stu-id="5d077-194">The order in which PSTN usage records are listed in the trunk configuration is significant.</span></span> <span data-ttu-id="5d077-195">Lync 服务器从上到下遍历列表。</span><span class="sxs-lookup"><span data-stu-id="5d077-195">Lync Server traverses the list from top to down.</span></span>

    
    </div>

12. <span data-ttu-id="5d077-196">应选择“启用 RTP 闭锁”为网络地址转换 (NAT) 或防火墙以及支持闭锁的 SBC 后面的客户端启用媒体旁路。</span><span class="sxs-lookup"><span data-stu-id="5d077-196">**Enable RTP Latching** should be selected to enable bypass media for clients behind a network address translation (NAT) or firewall and an SBC that supports latching.</span></span>

13. <span data-ttu-id="5d077-197">应选择 "**启用转发呼叫" 历史记录**，以便为中介服务器的网关对等发送呼叫历史记录信息。</span><span class="sxs-lookup"><span data-stu-id="5d077-197">**Enable forward call history** should be selected to enable sending of call history information to the gateway peer of the Mediation Server.</span></span>

14. <span data-ttu-id="5d077-198">**启用前向 p 声明的标识数据** 应选中以启用 P 声明的标识数据 (PAI) 调用发起方信息，以便在中介服务器端和网关端 (，反之亦然) （如果存在）。</span><span class="sxs-lookup"><span data-stu-id="5d077-198">**Enable forward P-Asserted-Identity data** should be selected to enable the P-Asserted-Identity (PAI) call originator information to be forwarded between the Mediation Server side and gateway side (and vice versa), when present.</span></span>

15. <span data-ttu-id="5d077-199">应选择“启用出站路由故障转移计时器”以启用快速故障转移。</span><span class="sxs-lookup"><span data-stu-id="5d077-199">**Enable outbound routing failover timer** should be selected to enable fast failover.</span></span> <span data-ttu-id="5d077-200">与此中继关联的网关会在 10 秒内发送通知，告知正在处理出站呼叫。</span><span class="sxs-lookup"><span data-stu-id="5d077-200">The gateway associated with this trunk can give notification within 10 seconds that it is processing an outbound call.</span></span> <span data-ttu-id="5d077-201">如果中介服务器未收到此通知，将会重新路由到另一个主干。</span><span class="sxs-lookup"><span data-stu-id="5d077-201">Rerouting to another trunk will occur if this notification is not received by the Mediation Server.</span></span> <span data-ttu-id="5d077-202">在延迟可能推迟响应时间或网关需要花费 10 秒以上的时间才能响应，应禁用快速故障转移。</span><span class="sxs-lookup"><span data-stu-id="5d077-202">On networks where latency may delay the response time or the gateway takes longer than 10 seconds to respond, the fast failover should be disabled.</span></span>

16. <span data-ttu-id="5d077-203">（可选）为中继关联和配置“主叫号码转换规则”。</span><span class="sxs-lookup"><span data-stu-id="5d077-203">(Optional) Associate and configure **calling number translation rules** for the trunk.</span></span> <span data-ttu-id="5d077-204">这些转换规则适用于出站呼叫的主叫号码</span><span class="sxs-lookup"><span data-stu-id="5d077-204">These translation rules apply to the calling number for outbound calls</span></span>
    
      - <span data-ttu-id="5d077-205">若要从您的企业语音部署中可用的所有翻译规则列表中选择一个或多个规则，请单击 " **选择**"。</span><span class="sxs-lookup"><span data-stu-id="5d077-205">To choose one or more rules from a list of all translation rules that are available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="5d077-206">在“选择转换规则”中，单击要与中继关联的规则，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5d077-206">In **Select Translation Rules**, click the rules that you want to associate with the trunk, and then click **OK**.</span></span>
    
      - <span data-ttu-id="5d077-207">要定义新的转换规则并将其与中继相关联，请单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5d077-207">To define a new translation rule and associate it with the trunk, click **New**.</span></span> <span data-ttu-id="5d077-208">有关定义新规则的详细信息，请参阅部署文档中 [Lync Server 2013 中的 "定义翻译规则](lync-server-2013-defining-translation-rules.md) "。</span><span class="sxs-lookup"><span data-stu-id="5d077-208">For details about defining a new rule, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="5d077-209">要编辑已与中继关联的转换规则，请单击相应的规则名称，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="5d077-209">To edit a translation rule that is already associated with the trunk, click the rule name, and then click **Show details**.</span></span> <span data-ttu-id="5d077-210">有关详细信息，请参阅部署文档中 [Lync Server 2013 中的 "定义翻译规则](lync-server-2013-defining-translation-rules.md) "。</span><span class="sxs-lookup"><span data-stu-id="5d077-210">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="5d077-211">要复制现有的转换规则以作为定义新规则的起点，请单击相应的规则名称，再单击“复制”，然后单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="5d077-211">To copy an existing translation rule to use as a starting point for defining a new rule, click the rule name and click **Copy**, and then click **Paste**.</span></span> <span data-ttu-id="5d077-212">有关详细信息，请参阅 [在 Lync Server 2013 中定义翻译规则](lync-server-2013-defining-translation-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-212">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span></span>
    
      - <span data-ttu-id="5d077-213">要从中继删除某个转换规则，请突出显示相应的规则名称，然后单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="5d077-213">To remove a translation rule from the trunk, highlight the rule name and click **Remove**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="5d077-214">如果已在关联的中继对等方上配置了转换规则，则不要将任何转换规则与中继相关联，因为这两种规则可能会发生冲突。</span><span class="sxs-lookup"><span data-stu-id="5d077-214">Do not associate translation rules with a trunk if you have configured translation rules on the associated trunk peer, because the two rules might conflict.</span></span>

    
    </div>

17. <span data-ttu-id="5d077-p131">（可选）为中继关联和配置“被叫号码转换规则”。这些转换规则适用于出站呼叫的被叫号码。</span><span class="sxs-lookup"><span data-stu-id="5d077-p131">(Optional) Associate and configure **called number translation rules** for the trunk. The translation rules apply to the called number in an outbound call.</span></span>
    
      - <span data-ttu-id="5d077-217">若要从您的企业语音部署中可用的所有翻译规则列表中选择一个或多个规则，请单击 " **选择**"。</span><span class="sxs-lookup"><span data-stu-id="5d077-217">To choose one or more rules from a list of all translation rules that are available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="5d077-218">在“选择转换规则”中，单击要与中继关联的规则，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5d077-218">In **Select Translation Rules**, click the rules that you want to associate with the trunk, and then click **OK**.</span></span>
    
      - <span data-ttu-id="5d077-219">要定义新的转换规则并将其与中继相关联，请单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="5d077-219">To define a new translation rule and associate it with the trunk, click **New**.</span></span> <span data-ttu-id="5d077-220">有关定义新规则的详细信息，请参阅部署文档中 [Lync Server 2013 中的 "定义翻译规则](lync-server-2013-defining-translation-rules.md) "。</span><span class="sxs-lookup"><span data-stu-id="5d077-220">For details about defining a new rule, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="5d077-221">要编辑已与中继关联的转换规则，请单击相应的规则名称，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="5d077-221">To edit a translation rule that is already associated with the trunk, click the rule name, and then click **Show details**.</span></span> <span data-ttu-id="5d077-222">有关详细信息，请参阅部署文档中 [Lync Server 2013 中的 "定义翻译规则](lync-server-2013-defining-translation-rules.md) "。</span><span class="sxs-lookup"><span data-stu-id="5d077-222">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="5d077-223">要复制现有的转换规则以作为定义新规则的起点，请单击相应的规则名称，再单击“复制”，然后单击“粘贴”。</span><span class="sxs-lookup"><span data-stu-id="5d077-223">To copy an existing translation rule to use as a starting point for defining a new rule, click the rule name and click **Copy**, and then click **Paste**.</span></span> <span data-ttu-id="5d077-224">有关详细信息，请参阅 [在 Lync Server 2013 中定义翻译规则](lync-server-2013-defining-translation-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="5d077-224">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span></span>
    
      - <span data-ttu-id="5d077-225">要从中继删除某个转换规则，请突出显示相应的规则名称，然后单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="5d077-225">To remove a translation rule from the trunk, highlight the rule name and click **Remove**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="5d077-226">如果已在关联的中继对等方上配置了转换规则，则不要将任何转换规则与中继相关联，因为这两种规则可能会发生冲突。</span><span class="sxs-lookup"><span data-stu-id="5d077-226">Do not associate translation rules with a trunk if you have configured translation rules on the associated trunk peer, because the two rules might conflict.</span></span>

    
    </div>

18. <span data-ttu-id="5d077-p136">确保中继的转换规则按正确的顺序排列。要更改规则在列表中的位置，请突出显示相应的规则名称，然后单击向上箭头或向下箭头。</span><span class="sxs-lookup"><span data-stu-id="5d077-p136">Make sure that the trunk’s translation rules are arranged in the correct order. To change a rule’s position in the list, highlight the rule name and then click the up or down arrow.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="5d077-229">Lync Server 2013 从上到下遍历翻译规则列表，并使用与所拨号码匹配的第一个规则。</span><span class="sxs-lookup"><span data-stu-id="5d077-229">Lync Server 2013 traverses the translation rule list from the top down and uses the first rule that matches the dialed number.</span></span> <span data-ttu-id="5d077-230">如果要配置中继以使拨打号码可以匹配多个转换规则，则确保限制较严格的规则排在限制较宽松的规则上方。</span><span class="sxs-lookup"><span data-stu-id="5d077-230">If you configure a trunk so that a dialed number can match more than one translation rule, be sure that the more restrictive rules are sorted above the less restrictive rules.</span></span> <span data-ttu-id="5d077-231">例如，如果具有与任何 11 位数字相匹配的转换规则和只与以 +1425 开头的 11 位数字相匹配的转换规则，则确保与任何 11 位数字相匹配的规则排在更加严格的规则<EM>下方</EM>。</span><span class="sxs-lookup"><span data-stu-id="5d077-231">For example, if you have included a translation rule that matches any 11-digit number and a translation rule that matches only 11-digit numbers that start with +1425, be sure that the rule that matches any 11-digit number is sorted <EM>below</EM> the more restrictive rule.</span></span>

    
    </div>

19. <span data-ttu-id="5d077-232">完成中继的配置后，单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5d077-232">When you are finished configuring the trunk, click **OK**.</span></span>

20. <span data-ttu-id="5d077-233">在“Trunk 配置”页上，单击“提交”，然后单击“全部提交”。</span><span class="sxs-lookup"><span data-stu-id="5d077-233">On the **Trunk Configuration** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5d077-234">任何时候创建或修改中继配置，都必须运行“全部提交”<STRONG></STRONG>命令以发布配置更改。</span><span class="sxs-lookup"><span data-stu-id="5d077-234">Whenever you create or modify a trunk configuration, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="5d077-235">有关详细信息，请参阅操作文档中的 <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Lync Server 2013 中的 "发布待处理的语音路由配置更改"</A> 。</span><span class="sxs-lookup"><span data-stu-id="5d077-235">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

<span data-ttu-id="5d077-236">配置主干后，通过选择全局媒体绕过选项来继续配置 "绕过媒体"，如部署文档中 [Lync Server 2013 中的全局媒体旁路选项](lync-server-2013-global-media-bypass-options.md) 中所述。</span><span class="sxs-lookup"><span data-stu-id="5d077-236">After you have configured the trunk, continue configuring media bypass by choosing between global media bypass options, as described in [Global media bypass options in Lync Server 2013](lync-server-2013-global-media-bypass-options.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5d077-237">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d077-237">See Also</span></span>


[<span data-ttu-id="5d077-238">在 Lync Server 2013 中配置不使用 "媒体旁路" 的主干</span><span class="sxs-lookup"><span data-stu-id="5d077-238">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  


[<span data-ttu-id="5d077-239">在 Lync Server 2013 中配置媒体绕过</span><span class="sxs-lookup"><span data-stu-id="5d077-239">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)  
[<span data-ttu-id="5d077-240">Lync Server 2013 中的全局媒体绕过选项</span><span class="sxs-lookup"><span data-stu-id="5d077-240">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  


[<span data-ttu-id="5d077-241">在 Lync Server 2013 中定义转换规则</span><span class="sxs-lookup"><span data-stu-id="5d077-241">Defining translation rules in Lync Server 2013</span></span>](lync-server-2013-defining-translation-rules.md)  
  

<span data-ttu-id="5d077-242"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d077-242"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

