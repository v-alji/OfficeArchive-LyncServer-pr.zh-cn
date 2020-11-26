---
title: Lync Server 2013：定义您的移动要求
description: Lync Server 2013：定义移动性要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your mobility requirements
ms:assetid: b7608335-cdeb-4aae-8e4b-d80c55f0d62b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690039(v=OCS.15)
ms:contentKeyID: 48185226
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fbc1a443946f0c879397f41628cfe788b428ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430894"
---
# <a name="defining-your-mobility-requirements-for-lync-server-2013"></a><span data-ttu-id="c2af4-103">定义您的 Lync Server 2013 移动要求</span><span class="sxs-lookup"><span data-stu-id="c2af4-103">Defining your mobility requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2af4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2af4-104">

<span> </span></span></span>

<span data-ttu-id="c2af4-105">_**主题上次修改时间：** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="c2af4-105">_**Topic Last Modified:** 2013-02-14_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="c2af4-106">在 Lync Server 2013 移动功能的规划阶段中，当你使用 Lync 2010 移动版和 Lync 2013 移动客户端时，应做出决定以确定你的部署步骤。</span><span class="sxs-lookup"><span data-stu-id="c2af4-106">During the planning phase for the Lync Server 2013 mobility feature, when you are using Lync 2010 Mobile and Lync 2013 Mobile clients, you make decisions that determine your deployment steps.</span></span>

<span data-ttu-id="c2af4-107">下面是您必须考虑的决策：</span><span class="sxs-lookup"><span data-stu-id="c2af4-107">Here are the decisions that you must consider:</span></span>

  - <span data-ttu-id="c2af4-108">**是否要使用 Lync 移动客户端的自动发现？**</span><span class="sxs-lookup"><span data-stu-id="c2af4-108">**Do you want to use automatic discovery for Lync mobile clients?**</span></span>
    
    <span data-ttu-id="c2af4-109">如果你想要支持自动发现，你需要创建新的内部和外部域名系统 (DNS) 记录，将主题备用名称添加到前端服务器、控制器和反向代理上的证书，以及修改反向代理上的现有发布规则。</span><span class="sxs-lookup"><span data-stu-id="c2af4-109">If you want to support automatic discovery, you need to create new internal and external Domain Name System (DNS) records, add subject alternative names to certificates on the Front End Servers, Directors, and reverse proxy, and modify the existing publishing rules on the reverse proxy.</span></span> <span data-ttu-id="c2af4-110">有关详细信息，请参阅 [Lync Server 2013 中的移动技术要求](lync-server-2013-technical-requirements-for-mobility.md)。</span><span class="sxs-lookup"><span data-stu-id="c2af4-110">For details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span> <span data-ttu-id="c2af4-111">通过自动发现，用户可以从公司网络内部或外部的任何位置自动查找 Lync Server 2013 Web 服务，而无需在移动设备设置中输入 Url。</span><span class="sxs-lookup"><span data-stu-id="c2af4-111">With automatic discovery, users can automatically locate Lync Server 2013 Web Services from anywhere inside or outside the corporate network, without entering URLs in their mobile device settings.</span></span>
    
    <span data-ttu-id="c2af4-112">如果您使用手动设置而不是自动搜索，则移动用户需要在其移动设备上手动输入以下 Url：</span><span class="sxs-lookup"><span data-stu-id="c2af4-112">If you use manual settings instead of automatic discovery, mobile users need to manually enter the following URLs in their mobile devices:</span></span>
    
      - <span data-ttu-id="c2af4-113"> https:// \<ExtPoolFQDN\> /Autodiscover/autodiscoverservice.svc/Root 用于外部访问</span><span class="sxs-lookup"><span data-stu-id="c2af4-113">https://\<ExtPoolFQDN\>/Autodiscover/autodiscoverservice.svc/Root for external access</span></span>
    
      - <span data-ttu-id="c2af4-114"> https:// \<IntPoolFQDN\> /AutoDiscover/autodiscoverservice .svc/Root for 内部访问</span><span class="sxs-lookup"><span data-stu-id="c2af4-114">https://\<IntPoolFQDN\>/AutoDiscover/ autodiscoverservice.svc/Root for internal access</span></span>
    
    <span data-ttu-id="c2af4-115">强烈建议使用自动发现。</span><span class="sxs-lookup"><span data-stu-id="c2af4-115">We strongly recommend using automatic discovery.</span></span> <span data-ttu-id="c2af4-116">手动设置的主要用途是进行故障排除。</span><span class="sxs-lookup"><span data-stu-id="c2af4-116">The primary use of manual settings is for troubleshooting.</span></span>

  - <span data-ttu-id="c2af4-117">**如果你决定支持自动发现，你是否愿意使用每个 SIP 域的使用者备用名称更新反向代理的证书？**</span><span class="sxs-lookup"><span data-stu-id="c2af4-117">**If you decide to support automatic discovery, are you willing to update certificates on the reverse proxy with subject alternative names for each SIP domain?**</span></span>
    
    <span data-ttu-id="c2af4-118">如果您有多个 SIP 域，则在反向代理服务器上更新公共证书可能会非常昂贵。</span><span class="sxs-lookup"><span data-stu-id="c2af4-118">If you have many SIP domains, updating public certificates on the reverse proxy can become very expensive.</span></span> <span data-ttu-id="c2af4-119">如果是这种情况，你可以选择实现自动发现，以便初始自动发现服务请求在端口80上使用 HTTP，而不是在端口443上使用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c2af4-119">If this is the case, you can choose to implement automatic discovery so that the initial Autodiscover Service request uses HTTP on port 80, instead of using HTTPS on port 443.</span></span> <span data-ttu-id="c2af4-120">但是，这不是推荐的方法。</span><span class="sxs-lookup"><span data-stu-id="c2af4-120">However, this is not the recommended approach.</span></span> <span data-ttu-id="c2af4-121">如果你决定选择这种替代方法，则无需更新反向代理的证书，但你需要在端口80上为 HTTP 创建 web 发布规则。</span><span class="sxs-lookup"><span data-stu-id="c2af4-121">If you decide to choose this alternative, you do not need to update the certificates on the reverse proxy, but you need to create a web publishing rule for HTTP on port 80.</span></span> <span data-ttu-id="c2af4-122">有关更多详细信息，请参阅 [Lync Server 2013 中的移动技术要求](lync-server-2013-technical-requirements-for-mobility.md)。</span><span class="sxs-lookup"><span data-stu-id="c2af4-122">For more details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="c2af4-123">**是否希望同时支持企业网络内部和外部的 Lync 移动客户端，或者仅支持企业网络内的客户端？**</span><span class="sxs-lookup"><span data-stu-id="c2af4-123">**Do you want to support Lync mobile clients both internal and external to the corporate network, or support clients only inside the corporate network?**</span></span>
    
    <span data-ttu-id="c2af4-124">如果您希望支持您的网络内部和外部的移动客户端，则移动设备可从任何位置访问移动功能。</span><span class="sxs-lookup"><span data-stu-id="c2af4-124">If you want to support mobile clients internal and external to your network, mobile devices can access mobility features from any location.</span></span> <span data-ttu-id="c2af4-125">默认配置是支持企业网络内部和外部的客户端。</span><span class="sxs-lookup"><span data-stu-id="c2af4-125">The default configuration is to support clients both internal and external to the corporate network.</span></span>
    
    <span data-ttu-id="c2af4-126">尽管默认配置允许移动客户端通信转到外部网站，但你可以将移动客户端流量限制到内部公司网络。</span><span class="sxs-lookup"><span data-stu-id="c2af4-126">Although the default configuration enables mobile client traffic to go through the external site, you can restrict mobile client traffic to the internal corporate network.</span></span> <span data-ttu-id="c2af4-127">将流量限制到内部网络时，用户只能在其移动设备上使用 Lync mobile 应用程序，而不是在网络内部。</span><span class="sxs-lookup"><span data-stu-id="c2af4-127">When you restrict the traffic to the internal network, users can use Lync mobile applications on their mobile devices only when they are inside the network.</span></span>
    
    <span data-ttu-id="c2af4-128">对于支持使用 Mcx 移动服务和 Lync 2010 Mobile 进行移动的部署，请运行 **CsMcxConfiguration** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2af4-128">For deployments that support mobility using the Mcx mobility service and Lync 2010 Mobile, you run the **Set-CsMcxConfiguration** cmdlet.</span></span> <span data-ttu-id="c2af4-129">若要设置仅供内部使用的移动，请使用类似于以下内容的命令：</span><span class="sxs-lookup"><span data-stu-id="c2af4-129">To set mobility for internal use only, you would use a command similar to the following:</span></span>
    
        Set-CsMcxConfiguration -Identity site:Redmond -ExposedWebURL Internal
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c2af4-130">UCWA 不需要额外的配置。</span><span class="sxs-lookup"><span data-stu-id="c2af4-130">There are no additional configurations required for UCWA.</span></span> <span data-ttu-id="c2af4-131">UCWA 没有等效的仅内部配置。</span><span class="sxs-lookup"><span data-stu-id="c2af4-131">UCWA does not have an equivalent internal-only configuration.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c2af4-132">如果您使用的是 Lync Server 2013 &nbsp; 前端服务器或前端池，并且没有<STRONG>you do not have</STRONG>任何 Lync Server 2010 &nbsp; 前端服务器或前端池，则不<STRONG>需要基于 cookie 的持久性</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="c2af4-132">If you are using a Lync Server 2013&nbsp;Front End Server or Front End pools and <STRONG>you do not have</STRONG> any Lync Server 2010&nbsp;Front End Servers or Front End pools, <STRONG>there is no requirement for cookie-based persistence</STRONG>.</span></span> <span data-ttu-id="c2af4-133">如果需要保留任何 Lync Server 2010 &nbsp; 前端服务器或前端池，同样的规则在 Lync Server 2010 中仍适用于基于 cookie 的持久性。</span><span class="sxs-lookup"><span data-stu-id="c2af4-133">If you need to retain any Lync Server 2010&nbsp;Front End Servers or Front End pools, the same rules still apply as in Lync Server 2010 for cookie-based persistence.</span></span>

    
    </div>

  - <span data-ttu-id="c2af4-134">**是否要支持 Apple iOS 设备和 Windows phone 的推送通知？**</span><span class="sxs-lookup"><span data-stu-id="c2af4-134">**Do you want to support push notifications for Apple iOS devices and Windows Phones?**</span></span>
    
    <span data-ttu-id="c2af4-135">如果你支持推送通知，受支持的 Apple iOS 设备和 Windows phone 将收到当移动应用程序处于非活动状态时发生的事件通知。</span><span class="sxs-lookup"><span data-stu-id="c2af4-135">If you support push notifications, supported Apple iOS devices and Windows Phones receive a notification of events that occur when the mobile application is inactive.</span></span> <span data-ttu-id="c2af4-136">你必须将 Edge 服务器配置为与基于云的 Lync Server 推送通知服务具有联合身份验证关系，该服务位于 Lync Online 数据中心，并运行 cmdlet 以启用推送通知。</span><span class="sxs-lookup"><span data-stu-id="c2af4-136">You must configure your Edge Server to have a federation relationship with the cloud-based Lync Server Push Notification Service, which is located in the Lync Online datacenter, and run a cmdlet to enable push notifications.</span></span>
    
    <span data-ttu-id="c2af4-137">如果你想要通过你的 Wi-Fi 网络支持推送通知，除了支持移动设备提供商的3G 或数据网络上的推送通知之外，你必须打开企业 Wi-Fi 网络上的出站端口5223。</span><span class="sxs-lookup"><span data-stu-id="c2af4-137">If you want to support push notifications over your Wi-Fi network, in addition to supporting push notifications over the mobile device providers' 3G or data networks, you must open port 5223 outbound on your enterprise Wi-Fi network.</span></span> <span data-ttu-id="c2af4-138">通过 Wi-Fi 网络支持推送通知，支持仅使用具有较低室内接收的 Wi-Fi 和移动设备的移动设备。</span><span class="sxs-lookup"><span data-stu-id="c2af4-138">Supporting push notifications over the Wi-Fi network supports mobile devices that use only Wi-Fi and mobile devices that have poor indoor reception.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c2af4-139">仅当支持运行 Lync 2010 移动客户端的 Apple 设备时，才需要打开端口 TCP 5223。</span><span class="sxs-lookup"><span data-stu-id="c2af4-139">Opening port TCP 5223 is required only when supporting Apple devices running the Lync 2010 Mobile client.</span></span>

    
    </div>
    
    <span data-ttu-id="c2af4-140">如果不支持推送通知，Apple mobile 设备和 Windows phone 的用户将无法找到有关在移动应用程序处于非活动状态时出现的事件（如即时消息邀请或错过的消息）。</span><span class="sxs-lookup"><span data-stu-id="c2af4-140">If you do not support push notifications, users of Apple mobile devices and Windows Phones will not find out about events—such as instant message invitations or missed messages—that occur when the mobile application is inactive.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c2af4-141">Apple 设备上的 Lync 2013 移动客户端不需要推送通知。</span><span class="sxs-lookup"><span data-stu-id="c2af4-141">Lync 2013 Mobile clients on Apple devices do not require push notification.</span></span> <span data-ttu-id="c2af4-142">Windows Phone 上的 Lync 2013 移动客户端使用推送通知。</span><span class="sxs-lookup"><span data-stu-id="c2af4-142">The Lync 2013 Mobile clients on Windows Phone use push notification.</span></span> <span data-ttu-id="c2af4-143">对推送通知和推送通知 clearinghouse 的规划对于 Windows Phone 上的 Lync Mobile 和不能运行 Lync 2013 移动客户端的 Apple 设备保持相同。</span><span class="sxs-lookup"><span data-stu-id="c2af4-143">Planning for push notification and the push notification clearinghouse remain the same for Lync Mobile on Windows Phone and Apple devices that are not able to run the Lync 2013 Mobile client.</span></span>

    
    </div>

  - <span data-ttu-id="c2af4-144">**是否希望所有用户都可以访问移动功能，或者是否希望能够指定哪些用户有权访问这些功能？**</span><span class="sxs-lookup"><span data-stu-id="c2af4-144">**Do you want all users to have access to mobility features, or do you want to be able to specify which users have access to these features?**</span></span>
    
    <span data-ttu-id="c2af4-145">此表介绍了 Lync Server 2013 中的用户可用的功能。</span><span class="sxs-lookup"><span data-stu-id="c2af4-145">The table describes features available to users in Lync Server 2013.</span></span> <span data-ttu-id="c2af4-146">默认值允许通过工作呼叫，允许通过 IP (VoIP) 上进行语音通话，并启用移动性。</span><span class="sxs-lookup"><span data-stu-id="c2af4-146">The defaults allow Call via Work, allow Voice over IP (VoIP), and enable Mobility.</span></span> <span data-ttu-id="c2af4-147">下面是可用选项的完整集：</span><span class="sxs-lookup"><span data-stu-id="c2af4-147">Here is the full set of available options:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c2af4-148">功能/参数名称/作用域 (策略参数名称可能不同) </span><span class="sxs-lookup"><span data-stu-id="c2af4-148">Feature/Parameter Name/Scope (Policy parameter names may not be the same)</span></span></th>
    <th><span data-ttu-id="c2af4-149">说明</span><span class="sxs-lookup"><span data-stu-id="c2af4-149">Description</span></span></th>
    <th><span data-ttu-id="c2af4-150">新增</span><span class="sxs-lookup"><span data-stu-id="c2af4-150">Introduced</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c2af4-151">支持移动性</span><span class="sxs-lookup"><span data-stu-id="c2af4-151">Enable Mobility</span></span></p>
    <p><span data-ttu-id="c2af4-152">参数名称： <code>EnableMobility</code></span><span class="sxs-lookup"><span data-stu-id="c2af4-152">Parameter Name : <code>EnableMobility</code></span></span></p>
    <p><span data-ttu-id="c2af4-153">范围：全局/网站/用户</span><span class="sxs-lookup"><span data-stu-id="c2af4-153">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-154">管理设置若要控制已安装 Lync Mobile 的给定范围内的用户，如果该策略设置为 False，用户将无法登录到客户端。</span><span class="sxs-lookup"><span data-stu-id="c2af4-154">Administrative setting to control users in a given scope that have the Lync Mobile installed, If the policy is set to False, the user would not be able to sign into the client.</span></span></p>
    <p><span data-ttu-id="c2af4-155">默认设置为 True。</span><span class="sxs-lookup"><span data-stu-id="c2af4-155">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-156">Lync Server 2010 的累积更新：11月2011</span><span class="sxs-lookup"><span data-stu-id="c2af4-156">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c2af4-157">启用外部语音</span><span class="sxs-lookup"><span data-stu-id="c2af4-157">Enable Outside Voice</span></span></p>
    <p><span data-ttu-id="c2af4-158">参数名称： <code>EnableOutsideVoice</code></span><span class="sxs-lookup"><span data-stu-id="c2af4-158">Parameter Name : <code>EnableOutsideVoice</code></span></span></p>
    <p><span data-ttu-id="c2af4-159">范围：全局/网站/用户</span><span class="sxs-lookup"><span data-stu-id="c2af4-159">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-160">控制用户通过工作进行呼叫的能力，该功能使用户能够使用其工作电话号码而不是移动电话号码拨打和接听电话。</span><span class="sxs-lookup"><span data-stu-id="c2af4-160">Controls a user’s ability to use Call Via Work, a feature that enables users to make and receive calls by using their work number instead of their mobile number.</span></span> <span data-ttu-id="c2af4-161">如果设置为 False，用户将无法通过其移动设备使用其工作电话来拨打或接听电话。</span><span class="sxs-lookup"><span data-stu-id="c2af4-161">If set to False, the user will not be able to make or receive calls by using their work number from their mobile device.</span></span></p>
    <p><span data-ttu-id="c2af4-162">默认设置为 True</span><span class="sxs-lookup"><span data-stu-id="c2af4-162">The default setting is True</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-163">Lync Server 2010 的累积更新：11月2011</span><span class="sxs-lookup"><span data-stu-id="c2af4-163">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c2af4-164">支持 IP 音频和视频</span><span class="sxs-lookup"><span data-stu-id="c2af4-164">Enable IP Audio and Video</span></span></p>
    <p><span data-ttu-id="c2af4-165">参数名称： <code>EnableIPAudioVideo</code></span><span class="sxs-lookup"><span data-stu-id="c2af4-165">Parameter Name : <code>EnableIPAudioVideo</code></span></span></p>
    <p><span data-ttu-id="c2af4-166">范围：全局/网站/用户</span><span class="sxs-lookup"><span data-stu-id="c2af4-166">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-167">控制用户是否可以使用 VoIP 在其移动设备上进行语音或视频通话。</span><span class="sxs-lookup"><span data-stu-id="c2af4-167">Controls whether a user can use VoIP to make or receive voice or video calls on their mobile device.</span></span> <span data-ttu-id="c2af4-168">如果设置为 False，用户将无法在其设备上进行或接收 VoIP 或视频通话。</span><span class="sxs-lookup"><span data-stu-id="c2af4-168">If set to False, the user will not be able to make or receive VoIP or video calls on their device.</span></span></p>
    <p><span data-ttu-id="c2af4-169">默认设置为 True。</span><span class="sxs-lookup"><span data-stu-id="c2af4-169">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-170">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2af4-170">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c2af4-171">IP 音频需要 WiFi</span><span class="sxs-lookup"><span data-stu-id="c2af4-171">Require WiFi for IP Audio</span></span></p>
    <p><span data-ttu-id="c2af4-172">参数名称： <code>RequireWiFiForIPAudio</code></span><span class="sxs-lookup"><span data-stu-id="c2af4-172">Parameter Name : <code>RequireWiFiForIPAudio</code></span></span></p>
    <p><span data-ttu-id="c2af4-173">范围：全局/网站/用户</span><span class="sxs-lookup"><span data-stu-id="c2af4-173">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-174">此设置定义客户是否需要在 WiFi 上通过 VoIP 而不是手机网络数据网络进行呼叫。</span><span class="sxs-lookup"><span data-stu-id="c2af4-174">This setting defines whether the client will be required to make and receive calls over VoIP on WiFi instead of the cellular data network.</span></span> <span data-ttu-id="c2af4-175">如果设置为 True，则用户仅在连接到 WiFi 网络时才能拨打和接听 VoIP 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c2af4-175">If set to True, the user can make and receive VoIP calls only when connected to a WiFi network.</span></span></p>
    <p><span data-ttu-id="c2af4-176">默认设置为 False。</span><span class="sxs-lookup"><span data-stu-id="c2af4-176">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-177">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2af4-177">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c2af4-178">IP 视频需要 WiFi</span><span class="sxs-lookup"><span data-stu-id="c2af4-178">Require WiFi for IP Video</span></span></p>
    <p><span data-ttu-id="c2af4-179">参数名称： <code>RequireWiFiForIPVideo</code></span><span class="sxs-lookup"><span data-stu-id="c2af4-179">Parameter Name : <code>RequireWiFiForIPVideo</code></span></span></p>
    <p><span data-ttu-id="c2af4-180">范围：全局/网站/用户</span><span class="sxs-lookup"><span data-stu-id="c2af4-180">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-181">此设置定义客户是否需要在 Wi-Fi 上（而不是在手机网络数据网络上）拨打和接收视频呼叫。</span><span class="sxs-lookup"><span data-stu-id="c2af4-181">This setting defines whether the client will be required to make and receive video calls on Wi-Fi instead of on the cellular data network.</span></span> <span data-ttu-id="c2af4-182">如果设置为 True，则用户仅在连接到 Wi-Fi 网络时才能发出和接收视频呼叫。</span><span class="sxs-lookup"><span data-stu-id="c2af4-182">If set to True, the user can make and receive video calls only when connected to a Wi-Fi network.</span></span></p>
    <p><span data-ttu-id="c2af4-183">默认设置为 False。</span><span class="sxs-lookup"><span data-stu-id="c2af4-183">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="c2af4-184">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2af4-184">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="c2af4-185">有关可以配置的策略设置以及如何管理策略的说明，请参阅 [CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy)、 [CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy)、 [CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy)、 [赠与 CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) 和 [Remove-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy)。</span><span class="sxs-lookup"><span data-stu-id="c2af4-185">For a description of the policy settings that you can configure, and how to manage the policies, see [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy), [Set-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy), [Get-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy), [Grant-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) and [Remove-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy).</span></span>

  - <span data-ttu-id="c2af4-186">**您是否希望未启用企业语音的用户能够使用单击加入加入会议？**</span><span class="sxs-lookup"><span data-stu-id="c2af4-186">**Do you want users who are not enabled for Enterprise Voice to be able to use Click to Join to join conferences?**</span></span>
    
    <span data-ttu-id="c2af4-187">若要让用户能够访问移动功能并通过工作进行呼叫，必须为企业语音启用这些功能。</span><span class="sxs-lookup"><span data-stu-id="c2af4-187">For users to have access to mobility features and Call via Work, they must be enabled for Enterprise Voice.</span></span> <span data-ttu-id="c2af4-188">但是，未启用企业语音的用户可以通过单击其移动设备上的链接来加入会议，前提是这些用户已分配适当的语音策略。</span><span class="sxs-lookup"><span data-stu-id="c2af4-188">However, users who are not enabled for Enterprise Voice can join conferences by clicking the link on their mobile device, if they have an appropriate voice policy assigned to them.</span></span> <span data-ttu-id="c2af4-189">你可以为这些用户分配特定的语音策略，或者确保存在适用于它们的全局策略或网站级别策略。</span><span class="sxs-lookup"><span data-stu-id="c2af4-189">You can either assign a specific voice policy to these users or make sure that a global policy or site-level policy exists that applies to them.</span></span> <span data-ttu-id="c2af4-190">您分配的语音政策必须具有公共交换电话网络 (PSTN) 使用情况记录和路由，用于定义用户可拨出以加入会议的区域。</span><span class="sxs-lookup"><span data-stu-id="c2af4-190">The voice policy that you assign must have public switched telephone network (PSTN) usage records and routes that define the areas to which users can dial out to join a conference.</span></span> <span data-ttu-id="c2af4-191">有关设置语音策略、PSTN 使用记录和路由的详细信息，请参阅 [在 Lync Server 2013 中配置语音策略、pstn 使用记录和语音路由](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)。</span><span class="sxs-lookup"><span data-stu-id="c2af4-191">For details about setting voice policy, PSTN usage records, and routes, see [Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c2af4-192">希望使用 "单击以加入" 的移动用户以及相关的 PSTN 使用记录和语音路由，因为单击移动设备上的链接将导致来自 Lync Server 2013 的出站呼叫。</span><span class="sxs-lookup"><span data-stu-id="c2af4-192">Mobile users who want to use Click to Join require a voice policy, along with the related PSTN usage records and voice routes, because clicking the link on the mobile device results in an outbound call from Lync Server 2013.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="c2af4-193">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2af4-193">See Also</span></span>


[<span data-ttu-id="c2af4-194">Lync Server 2013 中的移动性技术要求</span><span class="sxs-lookup"><span data-stu-id="c2af4-194">Technical requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-mobility.md)  


[<span data-ttu-id="c2af4-195">在 Lync Server 2013 中配置语音策略、PSTN 使用记录和语音路由</span><span class="sxs-lookup"><span data-stu-id="c2af4-195">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)  
  

<span data-ttu-id="c2af4-196"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2af4-196"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

