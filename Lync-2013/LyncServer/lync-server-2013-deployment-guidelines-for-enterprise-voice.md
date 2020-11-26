---
title: Lync Server 2013：企业语音部署准则
description: Lync Server 2013：企业语音的部署指南。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment guidelines for Enterprise Voice
ms:assetid: 8985bd93-7613-4cef-9c89-51df6049ed9b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398694(v=OCS.15)
ms:contentKeyID: 48184733
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cd847f674ad4b04698be0f54f8fbd490b13d689
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429690"
---
# <a name="deployment-guidelines-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="ca184-103">Lync Server 2013 中的企业语音部署准则</span><span class="sxs-lookup"><span data-stu-id="ca184-103">Deployment guidelines for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ca184-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ca184-104">

<span> </span></span></span>

<span data-ttu-id="ca184-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="ca184-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="ca184-106">本主题介绍了规划部署 Lync Server 2013 和企业语音工作负荷时需要考虑的先决条件和其他指南。</span><span class="sxs-lookup"><span data-stu-id="ca184-106">This topic describes prerequisites and other guidelines to consider when you are planning to deploy Lync Server 2013 and the Enterprise Voice workload.</span></span>

<div>

## <a name="deployment-prerequisites"></a><span data-ttu-id="ca184-107">部署先决条件</span><span class="sxs-lookup"><span data-stu-id="ca184-107">Deployment Prerequisites</span></span>

<span data-ttu-id="ca184-108">若要在部署企业语音时获得最佳体验，请确保你的 IT 基础结构、网络和系统满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="ca184-108">For an optimum experience when deploying Enterprise Voice, make sure that your IT infrastructure, network, and systems meet the following prerequisites:</span></span>

  - <span data-ttu-id="ca184-109">Lync Server 2013 标准版或企业版已安装并在您的网络上运行。</span><span class="sxs-lookup"><span data-stu-id="ca184-109">Lync Server 2013 Standard Edition or Enterprise Edition is installed and operational on your network.</span></span>

  - <span data-ttu-id="ca184-110">所有边缘服务器都在你的外围网络中部署并运行，包括具有访问边缘服务的边缘服务器、A/V 边缘服务、Web 会议边缘服务和反向代理。</span><span class="sxs-lookup"><span data-stu-id="ca184-110">All Edge Servers are deployed and operational in your perimeter network, including Edge Servers with Access Edge service, A/V Edge service, Web Conferencing Edge service, and a reverse proxy.</span></span>

  - <span data-ttu-id="ca184-111">已为 Lync Server 创建并启用了一个或多个用户。</span><span class="sxs-lookup"><span data-stu-id="ca184-111">One or more users have been created and enabled for Lync Server.</span></span>

  - <span data-ttu-id="ca184-112">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 或最新的 service pack 或 Microsoft Exchange Server 2010 已安装。</span><span class="sxs-lookup"><span data-stu-id="ca184-112">Microsoft Exchange Server 2007 Service Pack 1 (SP1) or latest service pack, or Microsoft Exchange Server 2010 is installed.</span></span> <span data-ttu-id="ca184-113">将 Exchange 统一消息 (UM) 与 Lync Server 进行集成，并向客户端终结点提供丰富通知和调用日志信息，需要其中一项。</span><span class="sxs-lookup"><span data-stu-id="ca184-113">One of these is required for integrating Exchange Unified Messaging (UM) with Lync Server and to provide rich notifications and call log information to client endpoints.</span></span>

  - <span data-ttu-id="ca184-114">为要启用企业语音的每位用户指定、正常化和复制到 **msRTCSIP** 属性的唯一主要电话号码。</span><span class="sxs-lookup"><span data-stu-id="ca184-114">A unique primary phone number has been designated, normalized, and copied to the **msRTCSIP-line** attribute for each user who is to be enabled for Enterprise Voice.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ca184-115">Lync Server 支持 E-164 号码和非直接向内拨号 () 号码。</span><span class="sxs-lookup"><span data-stu-id="ca184-115">Lync Server supports E.164 numbers and non-Direct Inward Dialing (DID) numbers.</span></span> <span data-ttu-id="ca184-116">未完成的数字可以采用<STRONG> &lt; E-164、 &gt; ext = &lt; extension &gt; </STRONG>或数字字符串表示，要求专用扩展在整个企业中唯一。</span><span class="sxs-lookup"><span data-stu-id="ca184-116">Non-DID numbers can be represented in the format <STRONG>&lt;E.164&gt;;ext=&lt;extension&gt;</STRONG> or as a string of digits, with the requirement that the private extension is unique across the enterprise.</span></span> <span data-ttu-id="ca184-117">例如，1001的私密号码可以表示为 <STRONG>+ 1425550100; ext = 1001</STRONG>，或 <STRONG>1001</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="ca184-117">For example, a private number of 1001 can be represented as <STRONG>+1425550100;ext=1001</STRONG>, or as <STRONG>1001</STRONG>.</span></span> <span data-ttu-id="ca184-118">当表示为 <STRONG>1001</STRONG>时，预期是此专用号码在整个企业中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ca184-118">When represented as <STRONG>1001</STRONG>, the expectation is that this private number is unique across the enterprise.</span></span>

    
    </div>

  - <span data-ttu-id="ca184-119">部署企业语音的管理员应是 RTCUniversalServerAdmins 组的成员。</span><span class="sxs-lookup"><span data-stu-id="ca184-119">Administrators who deploy Enterprise Voice should be members of the RTCUniversalServerAdmins group.</span></span>

  - <span data-ttu-id="ca184-120">至少已成功部署 Office Communicator 2007。</span><span class="sxs-lookup"><span data-stu-id="ca184-120">At a minimum, Office Communicator 2007 is successfully deployed.</span></span> <span data-ttu-id="ca184-121">若要使用此版本的新功能，请部署 Lync 2013。</span><span class="sxs-lookup"><span data-stu-id="ca184-121">To use features new to this release, Lync 2013 is deployed.</span></span>

  - <span data-ttu-id="ca184-122">使用 Microsoft 或第三方证书颁发机构 (CA) 基础结构部署和配置 (MKI) 的托管密钥基础结构。</span><span class="sxs-lookup"><span data-stu-id="ca184-122">Managed key infrastructure (MKI) is deployed and configured, using either a Microsoft or a third-party certification authority (CA) infrastructure.</span></span>

  - <span data-ttu-id="ca184-123">安装中介服务器的每台计算机都必须：</span><span class="sxs-lookup"><span data-stu-id="ca184-123">Each computer on which you install Mediation Server must be:</span></span>
    
      - <span data-ttu-id="ca184-124">域的成员服务器，并准备好使用 Active Directory 域服务。</span><span class="sxs-lookup"><span data-stu-id="ca184-124">A member server of a domain, and prepared for Active Directory Domain Services.</span></span> <span data-ttu-id="ca184-125">有关 Active Directory 域服务的准备过程，请参阅部署文档中的 [准备适用于 Lync Server 2013 的 Active Directory 域服务](lync-server-2013-preparing-active-directory-domain-services.md) 。</span><span class="sxs-lookup"><span data-stu-id="ca184-125">For Active Directory Domain Services preparation procedures, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="ca184-126">运行下列操作系统之一：</span><span class="sxs-lookup"><span data-stu-id="ca184-126">Running one of the following operating systems:</span></span>
        
          - <span></span>  
            <span data-ttu-id="ca184-127">Windows Server 2008 标准操作系统的64位版本</span><span class="sxs-lookup"><span data-stu-id="ca184-127">The 64-bit edition of the Windows Server 2008 Standard operating system</span></span>
        
          - <span></span>  
            <span data-ttu-id="ca184-128">Windows Server 2008 企业版操作系统的64位版本</span><span class="sxs-lookup"><span data-stu-id="ca184-128">The 64-bit edition of the Windows Server 2008 Enterprise operating system</span></span>

  - <span data-ttu-id="ca184-129">如果到公共交换电话网络的连接 (PSTN) 或专用分支 exchange (PBX) 是由时间段多路复用 (TDM) 连接，则可以使用一个或多个 PSTN 网关进行部署。</span><span class="sxs-lookup"><span data-stu-id="ca184-129">If the connection to the public switched telephone network (PSTN) or private branch exchange (PBX) is by means of a Time Division Multiplexing (TDM) connection, one or more PSTN gateways are available for deployment.</span></span> <span data-ttu-id="ca184-130"> (如果通过 SIP 中继连接，则不需要 PSTN 网关。 ) </span><span class="sxs-lookup"><span data-stu-id="ca184-130">(If the connection is by means of a SIP trunk, a PSTN gateway is not required.)</span></span>

</div>

<div>

## <a name="power-network-or-telephone-service-outages"></a><span data-ttu-id="ca184-131">电源、网络或电话服务中断</span><span class="sxs-lookup"><span data-stu-id="ca184-131">Power, Network, or Telephone Service Outages</span></span>

<span data-ttu-id="ca184-132">如果你所在位置有停机、中断或其他电源、网络或电话服务，并且 Lync Server 和连接到 Lync 服务器的任何设备的声音、即时消息、状态和其他功能可能无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="ca184-132">If there is an outage, disruption, or other degradation of the power, network, or telephone services at your location, the voice, instant messaging, presence, and other features of Lync Server and any device connected to Lync Server may not work properly.</span></span>

</div>

<div>

## <a name="enterprise-voice-depends-on-server-availability-and-voice-client-and-hardware-operability"></a><span data-ttu-id="ca184-133">企业语音取决于服务器可用性和语音客户端和硬件可操作性</span><span class="sxs-lookup"><span data-stu-id="ca184-133">Enterprise Voice Depends on Server Availability and Voice Client and Hardware Operability</span></span>

<span data-ttu-id="ca184-134">与 Lync Server 的语音通信取决于服务器软件的可用性以及连接到服务器软件的语音客户端或硬件电话设备是否正常工作。</span><span class="sxs-lookup"><span data-stu-id="ca184-134">Voice communications with Lync Server depend upon the availability of the server software and the proper functioning of the voice clients or the hardware phone devices connecting to the server software.</span></span>

</div>

<div>

## <a name="alternative-means-of-accessing-emergency-services"></a><span data-ttu-id="ca184-135">访问紧急服务的替代方法</span><span class="sxs-lookup"><span data-stu-id="ca184-135">Alternative Means of Accessing Emergency Services</span></span>

<span data-ttu-id="ca184-136">对于安装语音客户端的那些位置 (例如，运行 Lync 客户端或 Lync 手机版设备的电脑) ，我们建议你保留用于呼叫紧急服务的备份选项 (例如，911或 999) 电源故障、网络连接降低、电话服务中断或可能阻碍 Lync 服务器、Lync 或 Lync Phone Edition 设备运行的其他问题。</span><span class="sxs-lookup"><span data-stu-id="ca184-136">For those locations where you install a voice client (for example, a PC running Lync client or an Lync Phone Edition device), we recommend that you maintain a backup option for users to call emergency services (for example, 911 or 999) in case of a power failure, network connectivity degradation, telephone service outage, or other issue that may inhibit operation of Lync Server, Lync, or Lync Phone Edition devices.</span></span> <span data-ttu-id="ca184-137">此类替代选项可能包括连接到标准的公共交换电话网络线路或手机的电话。</span><span class="sxs-lookup"><span data-stu-id="ca184-137">Such alternative options could include a telephone connected to a standard public switched telephone network line or a cell phone.</span></span>

</div>

<div>

## <a name="emergency-calls-and-multi-line-telephone-systems"></a><span data-ttu-id="ca184-138">紧急呼叫和多行电话系统</span><span class="sxs-lookup"><span data-stu-id="ca184-138">Emergency Calls and Multi-Line Telephone Systems</span></span>

<span data-ttu-id="ca184-139">使用多行电话系统 (MLTS) 可能受美国国家/地区的 MLTS 或联邦法律或其他国家/地区的法律限制，这些国家/地区要求向紧急 (服务提供呼叫者的电话号码、分机和/或物理位置，例如，拨打紧急接入号码（如911或 999) 时）。</span><span class="sxs-lookup"><span data-stu-id="ca184-139">The use of a multiline telephone system (MLTS) may be subject to U.S state or federal laws or the laws of other countries/regions that require the MLTS to provide a caller’s telephone number, extension, and/or physical location to applicable emergency services when a caller is placed to emergency services (for example, when dialing an emergency access number such as 911 or 999).</span></span> <span data-ttu-id="ca184-140">在此版本中，可将 Lync Server 配置为向紧急服务提供商提供呼叫方的物理位置，如在 [Lync Server 2013 中的 "使用紧急服务 (E9-1-1") 中](lync-server-2013-planning-for-emergency-services-e9-1-1.md)所述。</span><span class="sxs-lookup"><span data-stu-id="ca184-140">In this release, Lync Server can be configured to provide a caller’s physical location to an emergency services provider, as described in [Planning for emergency services (E9-1-1) in Lync Server 2013](lync-server-2013-planning-for-emergency-services-e9-1-1.md).</span></span> <span data-ttu-id="ca184-141">遵守 MLTS 法律是 Lync Server、Lync 客户端和 Lync Phone 版设备的买方的唯一责任。</span><span class="sxs-lookup"><span data-stu-id="ca184-141">Compliance with MLTS laws is the sole responsibility of the purchaser of Lync Server, Lync client, and Lync Phone Edition devices.</span></span>

<span data-ttu-id="ca184-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ca184-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

