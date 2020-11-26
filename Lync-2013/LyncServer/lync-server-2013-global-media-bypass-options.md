---
title: Lync Server 2013：全局媒体绕过选项
description: Lync Server 2013：全局媒体绕过选项。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Global media bypass options
ms:assetid: 1bd35f90-8587-48a1-b0c2-095a4053fc77
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398255(v=OCS.15)
ms:contentKeyID: 48183551
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e69a776c13171d74666a202108fa4b5c72e224d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427906"
---
# <a name="global-media-bypass-options-in-lync-server-2013"></a><span data-ttu-id="7ad50-103">Lync Server 2013 中的全局媒体绕过选项</span><span class="sxs-lookup"><span data-stu-id="7ad50-103">Global media bypass options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ad50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ad50-104">

<span> </span></span></span>

<span data-ttu-id="7ad50-105">_**主题上次修改时间：** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="7ad50-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7ad50-106">本主题假定你已将任何中继的媒体旁路配置到对等 (在 Internet 电话服务提供商) 的公共交换电话网络 (PSTN) 网关、IP PBX 或会话边界控制器 (SBC) 的特定网站或服务（你希望媒体绕过中介服务器）。</span><span class="sxs-lookup"><span data-stu-id="7ad50-106">This topic assumes that you have already configured media bypass for any trunks to a peer (a public switched telephone network (PSTN) gateway, an IP-PBX, or a Session Border Controller (SBC) at an Internet Telephony Service Provider) for a specific site or service for which you want media to bypass the Mediation Server.</span></span>



</div>

<span data-ttu-id="7ad50-p101">除了为与对等方关联的各个中继连接启用媒体旁路功能外，还必须在全局范围内启用媒体旁路功能。全局媒体旁路设置可以指定始终为对 PSTN 的呼叫尝试媒体旁路，或者指定通过将子网映射到网络站点和网络区域来使用媒体旁路，这与呼叫允许控制（另一高级语音功能）所执行的操作类似。同时启用媒体旁路和呼叫允许控制后，在确定是否使用媒体旁路时，会自动使用为呼叫允许控制指定的网络区域、网络站点和子网信息。这意味着，启用呼叫允许控制后无法指定始终为对 PSTN 的呼叫尝试媒体旁路。</span><span class="sxs-lookup"><span data-stu-id="7ad50-p101">In addition to enabling media bypass for individual trunk connections associated with a peer, you must also enable media bypass globally. Global media bypass settings can either specify that media bypass is always attempted for calls to the PSTN, or that media bypass is employed by using the mapping of subnets to network sites and network regions—similar to what is done by call admission control, another advanced voice feature. When media bypass and call admission control are both enabled, then the network region, network site, and subnet information that is specified for call admission control is automatically used when determining whether to employ media bypass. This means that you cannot specify that media bypass is always attempted for calls to the PSTN when call admission control is enabled.</span></span>

<span data-ttu-id="7ad50-111">本主题介绍了如何将 Lync Server 控制面板和 Lync Server Management Shell 一起使用来配置全局媒体绕过设置。</span><span class="sxs-lookup"><span data-stu-id="7ad50-111">This topic describes how to use Lync Server Control Panel and Lync Server Management Shell together to configure global media bypass settings.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7ad50-112">使用这些步骤配置媒体旁路时，假定客户端和中介服务器对等方（例如，SIP 中继提供商的 PSTN 网关、IP-PBX 或 SBC）之间的连接工作正常。</span><span class="sxs-lookup"><span data-stu-id="7ad50-112">When you use these steps to configure media bypass, the assumption is that you have good connectivity between clients and the Mediation Server peer (for example, a PSTN gateway, an IP-PBX, or an SBC at a SIP trunking provider).</span></span> <span data-ttu-id="7ad50-113">如果链接上有任何带宽限制，则媒体旁路无法应用于呼叫。</span><span class="sxs-lookup"><span data-stu-id="7ad50-113">If there are any bandwidth limitations on the link, media bypass cannot be applied to the call.</span></span> <span data-ttu-id="7ad50-114">媒体旁路将不会与每个 PSTN 网关、IP-PBX 和 SBC 进行交互操作。</span><span class="sxs-lookup"><span data-stu-id="7ad50-114">Media bypass will not interoperate with every PSTN gateway, IP-PBX, and SBC.</span></span> <span data-ttu-id="7ad50-115">Microsoft 与认证合作伙伴一起对一组 PSTN 网关和 SBC 进行了测试，另外也对 Cisco IP-PBX 进行了一些测试。</span><span class="sxs-lookup"><span data-stu-id="7ad50-115">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="7ad50-116">只有在统一通信中列出的产品和版本才支持媒体绕开互操作性计划-Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A> 。</span><span class="sxs-lookup"><span data-stu-id="7ad50-116">Media bypass is supported only with products and versions listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A>.</span></span>



</div>

<div>

## <a name="next-steps-choose-global-media-bypass-settings"></a><span data-ttu-id="7ad50-117">后续步骤：选择全局媒体绕过设置</span><span class="sxs-lookup"><span data-stu-id="7ad50-117">Next Steps: Choose Global Media Bypass Settings</span></span>

<span data-ttu-id="7ad50-118">在针对特定网站或服务对等方的任何中继连接上启用了媒体旁路后，请使用以下内容之一：</span><span class="sxs-lookup"><span data-stu-id="7ad50-118">After you have enabled media bypass on any trunk connections to a peer for specific sites or services, use the following content to either:</span></span>

  - <span data-ttu-id="7ad50-119">按 "在 [Lync server 2013 中配置媒体旁路](lync-server-2013-configure-media-bypass-to-always-bypass-the-mediation-server.md)" 中所述，始终启用媒体绕过，以始终绕过中介服务器。</span><span class="sxs-lookup"><span data-stu-id="7ad50-119">Enable media bypass always, as described in [Configure media bypass in Lync Server 2013 to always bypass the Mediation Server](lync-server-2013-configure-media-bypass-to-always-bypass-the-mediation-server.md).</span></span>

  - <span data-ttu-id="7ad50-120">或者，将媒体旁路配置为使用网站和区域信息，如在 [Lync Server 2013 中配置媒体绕过全局设置以使用网站和区域信息](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="7ad50-120">Or, configure media bypass to use site and region information, as described in [Configure media bypass global settings in Lync Server 2013 to use site and region information](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7ad50-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ad50-121">See Also</span></span>


[<span data-ttu-id="7ad50-122">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ad50-122">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="7ad50-123">在 Lync Server 2013 中将子网与网络站点相关联</span><span class="sxs-lookup"><span data-stu-id="7ad50-123">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)  


[<span data-ttu-id="7ad50-124">在 Lync Server 2013 中配置媒体绕过</span><span class="sxs-lookup"><span data-stu-id="7ad50-124">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)  
[<span data-ttu-id="7ad50-125">Lync Server 2013 中的媒体绕过和中介服务器</span><span class="sxs-lookup"><span data-stu-id="7ad50-125">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)  
  

<span data-ttu-id="7ad50-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ad50-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

