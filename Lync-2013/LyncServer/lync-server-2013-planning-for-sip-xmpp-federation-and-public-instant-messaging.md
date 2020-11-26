---
title: 计划 SIP、XMPP 联盟和公共即时消息
description: 规划 SIP、XMPP 联盟和公共即时消息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for SIP, XMPP federation, and public instant messaging
ms:assetid: 3b234d92-b9ff-4b1d-910e-084c6f17e751
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204825(v=OCS.15)
ms:contentKeyID: 48183918
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c28c9c75310c884ea00117be2458384d408daae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424420"
---
# <a name="planning-for-sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="e58ff-103">在 Lync Server 2013 中规划 SIP、XMPP 联盟和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="e58ff-103">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e58ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e58ff-104">

<span> </span></span></span>

<span data-ttu-id="e58ff-105">_**主题上次修改时间：** 2013-10-28_</span><span class="sxs-lookup"><span data-stu-id="e58ff-105">_**Topic Last Modified:** 2013-10-28_</span></span>

<span data-ttu-id="e58ff-106">可以将 Edge 服务器配置为允许内部和外部用户访问合作伙伴组织或服务的联系人。</span><span class="sxs-lookup"><span data-stu-id="e58ff-106">Edge Servers can be configured to allow your internal and external users access to contacts at partner organizations or services.</span></span> <span data-ttu-id="e58ff-107">联合身份验证（如这些合作伙伴协议），可向组织中的组织中的联系人提供以下任何或所有联系人：</span><span class="sxs-lookup"><span data-stu-id="e58ff-107">Federations, as these partner agreements are known, can provide any or all of the following to the contacts in your organization on the partner federation or contacts in the partner federation to yours:</span></span>

  - <span data-ttu-id="e58ff-108">即时消息和状态</span><span class="sxs-lookup"><span data-stu-id="e58ff-108">Instant messaging and presence</span></span>

  - <span data-ttu-id="e58ff-109">协作和会议，例如 Web 会议</span><span class="sxs-lookup"><span data-stu-id="e58ff-109">Collaboration and conferencing, for example – Web conferencing</span></span>

  - <span data-ttu-id="e58ff-110">音频会议和/或视频会议</span><span class="sxs-lookup"><span data-stu-id="e58ff-110">Audio conferencing, video conferencing, or both</span></span>

<span data-ttu-id="e58ff-111">在某些情况下，通信（例如即时消息 (IM) 和状态在 Microsoft Lync Server 2013 和可扩展消息和状态协议 (XMPP) 联系人，仅支持对等用户和联盟合作伙伴的联系人。</span><span class="sxs-lookup"><span data-stu-id="e58ff-111">In some cases the communication, for example instant messaging (IM) and presence between a Microsoft Lync Server 2013 and an extensible messaging and presence protocol (XMPP) contact, is peer-to-peer only - supporting only you and the contact at the federated partner.</span></span> <span data-ttu-id="e58ff-112">在其他情况下（如 Lync 服务器、Lync server 2010 至 Lync Server 2013 联盟），可以邀请多个参与者加入对话。</span><span class="sxs-lookup"><span data-stu-id="e58ff-112">In other cases, such as a Lync Server, Lync Server 2010 to Lync Server 2013 federation, multiple participants can be invited to join into the conversation.</span></span>

<div>

## <a name="lync-server-and-office-communications-server-federation"></a><span data-ttu-id="e58ff-113">Lync Server 和 Office 通信服务器联合</span><span class="sxs-lookup"><span data-stu-id="e58ff-113">Lync Server and Office Communications Server Federation</span></span>

<span data-ttu-id="e58ff-114">Microsoft Lync Server 2013、Lync Server 2010 和 Office 通信服务器之间的联盟支持对等通信和多方通信。</span><span class="sxs-lookup"><span data-stu-id="e58ff-114">Federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server supports peer-to-peer and multi-party communications.</span></span> <span data-ttu-id="e58ff-115">对等对话可以升级到多方对话，从而允许进行临时会议。</span><span class="sxs-lookup"><span data-stu-id="e58ff-115">Peer-to-peer conversations can be escalated to multi-party conversations, allowing for ad hoc meetings.</span></span> <span data-ttu-id="e58ff-116">会议-网络会议或音频/视频/视频会议-可以安排在您的组织内以及与您联盟的合作伙伴中的联系人之间包括联系人。</span><span class="sxs-lookup"><span data-stu-id="e58ff-116">Meetings – Web conferencing or audio/visual conferences – can be scheduled to include contacts inside your organization as well as contacts in partners that you federate with.</span></span>

<span data-ttu-id="e58ff-117">联合身份验证首次出现在 Microsoft Office Live 通信服务器2005中，并且支持一种类型的联盟和直接联盟。</span><span class="sxs-lookup"><span data-stu-id="e58ff-117">Federation first appeared in Microsoft Office Live Communications Server 2005 and supported one kind of federation, Direct Federation.</span></span> <span data-ttu-id="e58ff-118">直接联盟需要你了解联盟伙伴的会话启动协议 (SIP) 域和合作伙伴的边缘服务器的完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="e58ff-118">Direct Federation required you to know the federation partner’s session initiation protocol (SIP) domain and the fully qualified domain name (FQDN) of the partner’s Edge Server.</span></span> <span data-ttu-id="e58ff-119">使用 SP1 的实时通信服务器2005引入了其他联合身份验证类型，所有所需的域名系统 (DNS) SRV 记录由联盟伙伴发布以找到其边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="e58ff-119">Live Communications Server 2005 with SP1 introduced additional federation types, all of which required domain name system (DNS) SRV records to be published by the federated partner to locate their Edge Server.</span></span> <span data-ttu-id="e58ff-120">该版本的术语是：</span><span class="sxs-lookup"><span data-stu-id="e58ff-120">The terminology for that release was:</span></span>

  - <span data-ttu-id="e58ff-121">*打开增强联盟*：接受任何 SIP 域名，并使用 DNS SRV 查找合作伙伴边缘服务器</span><span class="sxs-lookup"><span data-stu-id="e58ff-121">*Open Enhanced Federation*: Accept any SIP domain name and use DNS SRV to locate the partner Edge Server</span></span>

  - <span data-ttu-id="e58ff-122">*增强联盟*：将合作伙伴的 SIP 域名配置为你的组织的联合身份验证合作伙伴，并使用 DNS SRV 查找合作伙伴边缘服务器</span><span class="sxs-lookup"><span data-stu-id="e58ff-122">*Enhanced Federation*: Configure the partner’s SIP domain name as a federation partner for your organization and use DNS SRV to find the partner Edge Server</span></span>

  - <span data-ttu-id="e58ff-123">*直接联盟*：将合作伙伴的 SIP 域名和 FQDN 配置为合作伙伴的边缘服务器</span><span class="sxs-lookup"><span data-stu-id="e58ff-123">*Direct Federation*: Configure the partner’s SIP domain name and the FQDN to the partner’s Edge Server</span></span>

  - <span data-ttu-id="e58ff-124">*服务器允许列表*：接受任何域，使用 DNS SRV 查找托管提供商或公共即时消息 (IM) 连接提供程序的边缘服务器</span><span class="sxs-lookup"><span data-stu-id="e58ff-124">*Server Allow List*: Accept any domain, use DNS SRV to find the Edge Server of a hosting provider or a public instant messaging (IM) connectivity provider</span></span>

<span data-ttu-id="e58ff-125">Microsoft Office 通信服务器2007引入了对联合身份验证类型的更新命名，以便更好地定义每个联合类型实际完成的内容：</span><span class="sxs-lookup"><span data-stu-id="e58ff-125">Microsoft Office Communications Server 2007 introduced updated naming for federation types to better define what each federation type actually accomplished:</span></span>

  - <span data-ttu-id="e58ff-126">开放式增强联盟称为 "已 *发现合作伙伴域*"</span><span class="sxs-lookup"><span data-stu-id="e58ff-126">Open Enhanced Federation became known as *Discovered Partner Domain*</span></span>

  - <span data-ttu-id="e58ff-127">增强联盟被称为 "*允许的伙伴域*"</span><span class="sxs-lookup"><span data-stu-id="e58ff-127">Enhanced Federation became known as *Allowed Partner Domain*</span></span>

  - <span data-ttu-id="e58ff-128">直接联盟被称为 "*允许的伙伴服务器*"</span><span class="sxs-lookup"><span data-stu-id="e58ff-128">Direct Federation became known as *Allowed Partner Server*</span></span>

  - <span data-ttu-id="e58ff-129">服务器允许列表被称为 *托管提供商* 和 *公共 IM 提供商*</span><span class="sxs-lookup"><span data-stu-id="e58ff-129">Server Allow List became known as *Hosting Provider* and *Public IM Provider*</span></span>

<span data-ttu-id="e58ff-130">Microsoft Lync Server 2010 根据 Microsoft Lync Online 2010 和 Microsoft Office 365 引入了更窄的托管提供程序的定义，并且它遵守允许的伙伴域联合身份验证类型所定义的同一允许列表。</span><span class="sxs-lookup"><span data-stu-id="e58ff-130">Microsoft Lync Server 2010 introduced a narrower definition of Hosting Provider in accordance with Microsoft Lync Online 2010 and Microsoft Office 365 and also made it subject to the same allowed list defined by the Allowed Partner Domain federation type.</span></span>

<span data-ttu-id="e58ff-131">在 Microsoft Lync Server 2013、Lync Server 2010 和 Office 通信服务器之间启用联盟将使用边缘服务器和反向代理来强制执行所定义的规则和允许的伙伴域。</span><span class="sxs-lookup"><span data-stu-id="e58ff-131">Enabling federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server uses the Edge Servers and reverse proxies to enforce the rules and allowed partner domains that you define.</span></span> <span data-ttu-id="e58ff-132">从规划的角度来看，与其他 Lync 服务器进行联盟，Office 通信服务器需要满足以下要求：</span><span class="sxs-lookup"><span data-stu-id="e58ff-132">From a planning perspective, federating with other Lync Server, Office Communications Server requires the following:</span></span>

  - <span data-ttu-id="e58ff-133">在拓扑生成器中启用联盟。</span><span class="sxs-lookup"><span data-stu-id="e58ff-133">Enable federation in Topology Builder.</span></span> <span data-ttu-id="e58ff-134">有关详细信息，请参阅 [在 Lync Server 2013 中配置 SIP 联合、XMPP 联盟和公共即时消息](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md)的部署主题。</span><span class="sxs-lookup"><span data-stu-id="e58ff-134">For details, see the Deployment topic [Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="e58ff-135">确定联合域发现的要求：</span><span class="sxs-lookup"><span data-stu-id="e58ff-135">Determine your requirements for federated domain discovery:</span></span>
    
      - <span></span>  
        <span data-ttu-id="e58ff-136">若要手动配置联盟，你必须具有合作伙伴的 Edge 服务器和域名的完全限定的域名 (FQDN) ，或者在 Lync Server 控制面板、 **联盟和外部访问** 以及 **SIP 联盟域** 中输入的联机域名。</span><span class="sxs-lookup"><span data-stu-id="e58ff-136">For manual configuration of federation, you must have the fully qualified domain name (FQDN) of the partner’s Edge Server and domain name, or online domain name, which is entered in the Lync Server Control Panel, **Federation and External Access**, **SIP Federated Domains**.</span></span> <span data-ttu-id="e58ff-137">创建 **新** 策略或 **编辑** 现有策略以允许或阻止 FQDN 域。</span><span class="sxs-lookup"><span data-stu-id="e58ff-137">Create a **New** policy or **Edit** an existing policy to either allow or block domains by FQDN.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="e58ff-138">如果合作伙伴更改了其边缘服务器的 IP 地址，则联合身份验证伙伴的边缘服务器的手动配置很容易出现故障。</span><span class="sxs-lookup"><span data-stu-id="e58ff-138">Manual configuration of a federation partner’s Edge Server is prone to failure in the event that the partner changes the IP address of their Edge Server.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="e58ff-139">对于 <STRONG>新 SIP 联盟域</STRONG>，你必须为 Microsoft Lync Online 和 microsoft 365 或 Office 365 提供 <STRONG>域名 (或 FQDN) </STRONG> 。</span><span class="sxs-lookup"><span data-stu-id="e58ff-139">For <STRONG>New SIP Federated Domains</STRONG>, you must provide the <STRONG>Domain name (or FQDN)</STRONG> for Microsoft Lync Online and Microsoft 365 or Office 365.</span></span> <span data-ttu-id="e58ff-140">对于 Microsoft Lync Server 2013、Lync Server 2010 和 Office 通信服务器，你还必须提供 <STRONG> (FQDN 的访问边缘服务) </STRONG></span><span class="sxs-lookup"><span data-stu-id="e58ff-140">For Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server you must also provide an <STRONG>Access Edge service (FQDN)</STRONG></span></span>

        
        </div>
    
      - <span></span>  
        <span data-ttu-id="e58ff-141">对于已发现的合作伙伴联盟（合作伙伴可以在其中发现你的 Edge 服务器），你可以在外部 DNS-sipfederationtls 中创建 SRV 记录 \_ 。 \_tcp.contoso.com-指向端口5061和主机 (边缘服务器的) 记录</span><span class="sxs-lookup"><span data-stu-id="e58ff-141">For discovered partner federation, where partners can discover your Edge Server, you create an SRV record in your external DNS - \_sipfederationtls.\_tcp.contoso.com – which points to the port 5061 and the host (A) record of your Edge Server</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="e58ff-142">如果你在 Windows Phone 或 Apple iPhone、iPad 或其他 Apple 设备上支持 Microsoft Lync 移动客户端，并且使用的是推送通知服务或推送通知服务，则必须为 _tcp _sipfederationtls。</span><span class="sxs-lookup"><span data-stu-id="e58ff-142">If you are supporting Microsoft Lync Mobile clients on either Windows Phone or Apple iPhone, iPad, or other Apple devices and are using the Push Notification Service or Push Notification Service, you must plan for _sipfederationtls._tcp.</span></span> <span data-ttu-id="e58ff-143">&lt;&gt;您有 Lync 移动客户端的每个 sip 域的 SIP 域 SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="e58ff-143">&lt;SIP domain&gt; SRV records for each SIP domain that you have Lync Mobile clients.</span></span> <span data-ttu-id="e58ff-144">Android 和 Nokia Symbian Lync Mobile 不使用推送通知，也不受此要求的制约。</span><span class="sxs-lookup"><span data-stu-id="e58ff-144">Android and Nokia Symbian Lync Mobile do not use push notification and are not subject to this requirement.</span></span>

        
        </div>

  - <span data-ttu-id="e58ff-145">配置外部用户访问策略以支持联盟域</span><span class="sxs-lookup"><span data-stu-id="e58ff-145">Configure external user access policies to support federated domains</span></span>

  - <span data-ttu-id="e58ff-146">打开用于会话初始协议的防火墙端口 (SIP) 、web 会议和音频/视频，以适应您正在启用的联盟或联系人。</span><span class="sxs-lookup"><span data-stu-id="e58ff-146">Open firewall ports for session initiation protocol (SIP), web conferencing and audio/visual to accommodate the federation or contacts that you are enabling.</span></span> <span data-ttu-id="e58ff-147">有关详细信息，请参阅： [确定 Lync Server 2013 的外部 A/V 防火墙和端口要求](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="e58ff-147">For details, see: [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span></span>

<span data-ttu-id="e58ff-148">以下信息将帮助你为与 Microsoft Lync Server 2013 和 Lync Server 2010 的联合定义证书、端口/协议和 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="e58ff-148">The following information will aid you in defining the certificate, port/protocol and DNS requirements for federation with Microsoft Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="e58ff-149">如果已计划或部署 Microsoft Lync Server 2013 Edge 服务器，则为证书、防火墙和端口/协议要求以及 DNS 要求的规划通常是一个直连过程。</span><span class="sxs-lookup"><span data-stu-id="e58ff-149">Planning for certificates, firewall and port/protocol requirements and DNS requirements is generally a straight forward process if you have planned or deployed your Microsoft Lync Server 2013 Edge Servers.</span></span> <span data-ttu-id="e58ff-150">由于联盟是一个使用现有边缘服务器的附加功能，因此规划要求一般由边缘服务器规划和部署来满足。</span><span class="sxs-lookup"><span data-stu-id="e58ff-150">Because federation is an additional feature that uses the existing Edge Server, the planning requirements are generally met by the Edge Server planning and deployment.</span></span> <span data-ttu-id="e58ff-151">你应该使用下表确定满足你的要求，并相应地在端口/协议和 DNS 中进行更改。</span><span class="sxs-lookup"><span data-stu-id="e58ff-151">You should use the following tables to determine that your requirements are met and make changes in port/protocol and DNS accordingly.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="e58ff-152">如果你有一个 Edge 服务器池，并且正在与 Lync Server 2013 或 Lync Server 2010 合作伙伴联盟，那么你可以在边缘服务器的内部和外部面向的方使用 DNS 负载平衡或硬件负载平衡器。</span><span class="sxs-lookup"><span data-stu-id="e58ff-152">If you have a pool of Edge Servers and are federating with Lync Server 2013 or Lync Server 2010 partners, then you can use either DNS load balancing or hardware load balancers on the internal and external facing sides of the Edge Servers.</span></span> <span data-ttu-id="e58ff-153">如果您要与 Office 通信服务器2007或 Office 通信服务器 2007 R2 进行联盟，则硬件负载平衡将在 Edge 服务器的事件中提供故障转移支持。</span><span class="sxs-lookup"><span data-stu-id="e58ff-153">If you are federating with Office Communications Server 2007 or Office Communications Server 2007 R2, hardware load balancing will provide failover support in the event of an Edge Server.</span></span> <span data-ttu-id="e58ff-154">Office 通信服务器2007和 Office 通信服务器 2007 R2 不支持 DNS 负载平衡。</span><span class="sxs-lookup"><span data-stu-id="e58ff-154">Office Communications Server 2007 and Office Communications Server 2007 R2 are not DNS load balancing aware.</span></span> <span data-ttu-id="e58ff-155">合作伙伴边缘服务器将与你的池中的第一个边缘服务器建立通信，以响应。</span><span class="sxs-lookup"><span data-stu-id="e58ff-155">The partner Edge Servers will establish communication with the first Edge Server in your pool that responds.</span></span> <span data-ttu-id="e58ff-156">如果该边缘服务器出现故障，通信不会自动故障转移。</span><span class="sxs-lookup"><span data-stu-id="e58ff-156">If that Edge Server fails, communication does not automatically failover.</span></span>



</div>

<span data-ttu-id="e58ff-157">证书要求通常通过规划所选边缘服务器或池边缘服务器计划的证书来满足。</span><span class="sxs-lookup"><span data-stu-id="e58ff-157">Certificate requirements are typically met through the planning of certificates for your chosen Edge Server or pooled Edge Server plan.</span></span>

</div>

<div>

## <a name="public-instant-messaging-connectivity"></a><span data-ttu-id="e58ff-158">公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="e58ff-158">Public Instant Messaging Connectivity</span></span>

<span data-ttu-id="e58ff-159">公用即时消息连接是一种联盟类，并配置为允许您的内部和外部 Lync Server 2013 用户从以下任何内容添加联系人：</span><span class="sxs-lookup"><span data-stu-id="e58ff-159">Public Instant Messaging Connectivity is a class of federation, and is configured to allow your internal and external Lync Server 2013 users to add contacts from any of the following:</span></span>

  - <span data-ttu-id="e58ff-160">Messenger 联系人</span><span class="sxs-lookup"><span data-stu-id="e58ff-160">Messenger contacts</span></span>

  - <span data-ttu-id="e58ff-161">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="e58ff-161">Yahoo\!</span></span> <span data-ttu-id="e58ff-162">联系人</span><span class="sxs-lookup"><span data-stu-id="e58ff-162">contacts</span></span>

  - <span data-ttu-id="e58ff-163">北美在线 (AOL) 联系人</span><span class="sxs-lookup"><span data-stu-id="e58ff-163">America Online (AOL) contacts</span></span>

<div>


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="e58ff-164">从2012年9月1日起，，Microsoft Lync 公共 IM 连接用户订阅许可证 (PIC USL) 不再可供购买新的或续订协议。</span><span class="sxs-lookup"><span data-stu-id="e58ff-164">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="e58ff-165">具有活动许可证的客户将能够继续与 Yahoo！进行联盟</span><span class="sxs-lookup"><span data-stu-id="e58ff-165">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="e58ff-166">Messenger 直到服务关闭日期 (准确日期仍将决定，但不早于2013年6月) 。</span><span class="sxs-lookup"><span data-stu-id="e58ff-166">Messenger until the service shutdown date (exact date is still to be decided, but no sooner than June 2013).</span></span></P>
> <LI>
> <P><span data-ttu-id="e58ff-167">PIC USL 是 Lync Server 或 Office 通信服务器与 Yahoo！联合所需的每用户、每月订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="e58ff-167">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="e58ff-168">Messenger.</span><span class="sxs-lookup"><span data-stu-id="e58ff-168">Messenger.</span></span> <span data-ttu-id="e58ff-169">Microsoft 提供此服务的能力已由 Yahoo！的支持（将不会续订的底层协议）提供。</span><span class="sxs-lookup"><span data-stu-id="e58ff-169">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="e58ff-170">Lync 比以往更多，是一种强大的工具，用于跨组织和全球各地的人员进行连接。</span><span class="sxs-lookup"><span data-stu-id="e58ff-170">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="e58ff-171">与 Windows Live Messenger 的联盟不需要除 Lync 标准 CAL 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="e58ff-171">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="e58ff-172">Skype 联盟将添加到此列表，使 Lync 用户可以通过 IM 和语音与成百上千人联系。</span><span class="sxs-lookup"><span data-stu-id="e58ff-172">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="e58ff-173">此类联合需要以下规划注意事项：</span><span class="sxs-lookup"><span data-stu-id="e58ff-173">This class of federation requires the following planning considerations:</span></span>

  - <span data-ttu-id="e58ff-174">除了即时消息外，Windows Live Messenger 用户可以与 Lync Server 2013 用户进行对等音频/视频通信。</span><span class="sxs-lookup"><span data-stu-id="e58ff-174">Windows Live Messenger users can have peer-to-peer audio/visual communication with Lync Server 2013 users, in addition to instant messaging.</span></span> <span data-ttu-id="e58ff-175">边缘服务器必须满足特定的端口和协议要求。</span><span class="sxs-lookup"><span data-stu-id="e58ff-175">Your Edge Servers must meet specific port and protocol requirements.</span></span> <span data-ttu-id="e58ff-176">有关详细信息，请参阅 [确定 Lync Server 2013 的外部 A/V 防火墙和端口要求](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e58ff-176">For details, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

  - <span data-ttu-id="e58ff-177">Yahoo 即时消息没有独特的要求，除了通常用于提供联合的典型边缘服务器的规划和部署中。</span><span class="sxs-lookup"><span data-stu-id="e58ff-177">Yahoo instant messaging has no unique requirements, other than those typically used in the planning and deployment of the typical Edge Server that is providing federation.</span></span>

  - <span data-ttu-id="e58ff-178">美洲在线要求分配给 Access Edge 服务的 Edge 服务器证书具有客户端增强型密钥用法 (EKU) 。</span><span class="sxs-lookup"><span data-stu-id="e58ff-178">America Online requires that your Edge Server certificate assigned to the Access Edge service has a client enhanced key usage (EKU).</span></span>

</div>

<div>

## <a name="extensible-messaging-and-presence-protocol-xmpp-federation"></a><span data-ttu-id="e58ff-179">可扩展消息和状态协议 (XMPP) 联合身份验证</span><span class="sxs-lookup"><span data-stu-id="e58ff-179">Extensible Messaging and Presence Protocol (XMPP) Federation</span></span>

<span data-ttu-id="e58ff-180">以前版本的 Lync Server 和 Office 通信服务器提供了可扩展消息和状态协议 (XMPP) 网关，可部署为单独的服务器角色，以便允许与 XMPP 部署进行联盟。</span><span class="sxs-lookup"><span data-stu-id="e58ff-180">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="e58ff-181">在 Microsoft Lync Server 2013 中，XMPP 功能可以部署为功能。</span><span class="sxs-lookup"><span data-stu-id="e58ff-181">In Microsoft Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="e58ff-182">XMPP 功能在两个部分中安装：在边缘服务器上运行的 XMPP 代理和在前端服务器上运行的 XMPP 网关。</span><span class="sxs-lookup"><span data-stu-id="e58ff-182">XMPP functionality is installed in two parts: an XMPP proxy that runs on the Edge Server and the XMPP gateway that runs on the Front End Servers.</span></span>

<span data-ttu-id="e58ff-183">在 [Lync Server 2013 中部署外部用户访问权限](lync-server-2013-deploying-external-user-access.md) 中介绍了 XMPP 的部署和配置在你的防火墙上部署外部用户访问，并通过在防火墙上定义端口和协议规则、配置证书以及添加 DNS 记录。</span><span class="sxs-lookup"><span data-stu-id="e58ff-183">Deployment and configuration of XMPP is covered in [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) You plan for supporting XMPP in your organization by defining port and protocol rules on your firewall, configuration of certificates, and adding DNS records.</span></span> <span data-ttu-id="e58ff-184">本节中的以下主题概述了为部署成功规划 XMPP 联合所需的信息。</span><span class="sxs-lookup"><span data-stu-id="e58ff-184">The following topics in this section summarize the information that you will need to successfully plan XMPP federation for your deployment.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="e58ff-p120">Microsoft 已测试 Lync Server 2013 的 XMPP 功能，并且支持该功能与 Google Talk 进行即时消息传递联盟。对于任何其他 XMPP 系统，请与第三方供应商联系，以确认它们是否支持与 Lync Server 2013 联盟以及获取任何部署或疑难解答建议。</span><span class="sxs-lookup"><span data-stu-id="e58ff-p120">The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.</span></span>



</div>

<div>


> [!IMPORTANT]
> <span data-ttu-id="e58ff-187">对于托管在 survivable 分支设备上的用户，不支持 XMPP 联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="e58ff-187">XMPP federation is not supported for users who are homed on survivable branch appliances.</span></span> <span data-ttu-id="e58ff-188">这适用于查看状态信息和交换 IM 消息。</span><span class="sxs-lookup"><span data-stu-id="e58ff-188">This applies to both seeing presence information and exchanging IM messages.</span></span>



</div>

</div>

<div id="sectionSection3" class="section">

<span data-ttu-id="e58ff-189">以下主题包含为受支持的联合身份验证方案的类型定义证书、防火墙端口和 DNS 条目的指南。</span><span class="sxs-lookup"><span data-stu-id="e58ff-189">In the following topics contain guidance for defining certificates, firewall ports and DNS entries for the types of supported federation scenarios.</span></span>

  - <span></span>  
    [<span data-ttu-id="e58ff-190">证书摘要-Lync Server 2013 中的 SIP、XMPP 联盟和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="e58ff-190">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - <span></span>  
    [<span data-ttu-id="e58ff-191">端口摘要-Lync Server 2013 中的 SIP、XMPP 联盟和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="e58ff-191">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - <span></span>  
    [<span data-ttu-id="e58ff-192">DNS 摘要-Lync Server 2013 中的 SIP、XMPP 联盟和公共即时消息</span><span class="sxs-lookup"><span data-stu-id="e58ff-192">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e58ff-193">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e58ff-193">See Also</span></span>


[<span data-ttu-id="e58ff-194">在 Lync Server 2013 中配置策略以控制联盟用户访问</span><span class="sxs-lookup"><span data-stu-id="e58ff-194">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  


[<span data-ttu-id="e58ff-195">Lync Server 2013 中的外部用户访问方案</span><span class="sxs-lookup"><span data-stu-id="e58ff-195">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="e58ff-196">确定 Lync Server 2013 的外部 A/V 防火墙和端口要求</span><span class="sxs-lookup"><span data-stu-id="e58ff-196">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
[<span data-ttu-id="e58ff-197">确定 Lync Server 2013 的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="e58ff-197">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="e58ff-198">在 Lync Server 2013 中管理您的组织的访问边缘配置</span><span class="sxs-lookup"><span data-stu-id="e58ff-198">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-access-edge-configuration-for-your-organization.md)  
[<span data-ttu-id="e58ff-199">在 Lync Server 2013 中管理组织的 SIP 联盟域</span><span class="sxs-lookup"><span data-stu-id="e58ff-199">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="e58ff-200">在 Lync Server 2013 中管理组织的 SIP 联盟提供程序</span><span class="sxs-lookup"><span data-stu-id="e58ff-200">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
  

<span data-ttu-id="e58ff-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e58ff-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

