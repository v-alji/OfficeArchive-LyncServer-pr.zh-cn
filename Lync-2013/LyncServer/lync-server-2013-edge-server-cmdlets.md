---
title: Lync Server 2013： Edge 服务器 cmdlet
description: Lync Server 2013： Edge 服务器 cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edge Server cmdlets
ms:assetid: 1a5427f4-a0d1-4652-8135-91333158ffc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415635(v=OCS.15)
ms:contentKeyID: 48183534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b73172331ddcde76672cccda682669f71dd7262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391734"
---
# <a name="edge-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="5c53c-103">Lync Server 2013 中的 Edge 服务器 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5c53c-103">Edge Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c53c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c53c-104">

<span> </span></span></span>

<span data-ttu-id="5c53c-105">_**主题上次修改时间：** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="5c53c-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="5c53c-106">通过 Edge 服务器，你可以将 Microsoft Lync Server 2013 的功能扩展到未登录到内部网络的用户。</span><span class="sxs-lookup"><span data-stu-id="5c53c-106">Edge Servers provide a way for you to extend the capabilities of Microsoft Lync Server 2013 to people who are not logged on to your internal network.</span></span> <span data-ttu-id="5c53c-107">例如，如果您有通过 Internet （而不是通过内部网络）登录到 Lync Server 2013 的已通过身份验证的远程用户，则需要设置运行 Lync Server Access Edge 服务的边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="5c53c-107">For example, if you have remote users -- authenticated users who log on to Lync Server 2013 over the Internet rather than through the internal network -- you will need to set up an Edge Server that runs the Lync Server Access Edge service.</span></span> <span data-ttu-id="5c53c-108">此外，如果你想要与另一个组织建立联盟，或者你希望向用户提供与具有公共即时消息服务（如 Yahoo \! 、AOL 或 MSN）的帐户进行通信的权限，则需要 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="5c53c-108">Additionally, Edge Servers are required if you want to establish federation with another organization or if you want to give your users the right to communicate with people who have accounts with a public instant messaging service such as Yahoo\!, AOL, or MSN.</span></span>

<div>


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="5c53c-109">从2012年9月1日起，，Microsoft Lync 公共 IM 连接用户订阅许可证 ( "PIC USL" ) 不再可用于购买新的或续订协议。</span><span class="sxs-lookup"><span data-stu-id="5c53c-109">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="5c53c-110">具有活动许可证的客户将能够继续与 Yahoo！进行联盟</span><span class="sxs-lookup"><span data-stu-id="5c53c-110">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="5c53c-111">Messenger，直到服务关闭日期。</span><span class="sxs-lookup"><span data-stu-id="5c53c-111">Messenger until the service shut down date.</span></span> <span data-ttu-id="5c53c-112">AOL 和 Yahoo！的有效期结束日期为2014年6月</span><span class="sxs-lookup"><span data-stu-id="5c53c-112">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="5c53c-113">已宣布。</span><span class="sxs-lookup"><span data-stu-id="5c53c-113">has been announced.</span></span> <span data-ttu-id="5c53c-114">有关详细信息，请参阅 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 中的公共即时消息连接支持</A>。</span><span class="sxs-lookup"><span data-stu-id="5c53c-114">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="5c53c-115">PIC USL 是 Lync Server 或 Office 通信服务器与 Yahoo！联合所需的每个每个用户每月订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="5c53c-115">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="5c53c-116">Messenger.</span><span class="sxs-lookup"><span data-stu-id="5c53c-116">Messenger.</span></span> <span data-ttu-id="5c53c-117">Microsoft 提供此服务的能力已作为对 Yahoo！的支持，它的底层协议被向下缠绕。</span><span class="sxs-lookup"><span data-stu-id="5c53c-117">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="5c53c-118">Lync 比以往更多，是一种强大的工具，用于跨组织和全球各地的人员进行连接。</span><span class="sxs-lookup"><span data-stu-id="5c53c-118">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="5c53c-119">与 Windows Live Messenger 的联盟不需要除 Lync 标准 CAL 之外的其他用户/设备许可证。</span><span class="sxs-lookup"><span data-stu-id="5c53c-119">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="5c53c-120">Skype 联盟将添加到此列表，使 Lync 用户可以通过 IM 和语音与成百上千人联系。</span><span class="sxs-lookup"><span data-stu-id="5c53c-120">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<div>

## <a name="edge-server-cmdlets"></a><span data-ttu-id="5c53c-121">Edge 服务器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5c53c-121">Edge Server Cmdlets</span></span>

<span data-ttu-id="5c53c-122">以下是与管理边缘服务器直接相关的 cmdlet 的列表：</span><span class="sxs-lookup"><span data-stu-id="5c53c-122">The following is a list of cmdlets that relate directly to managing Edge Servers:</span></span>

<span data-ttu-id="5c53c-123">**边缘服务器**</span><span class="sxs-lookup"><span data-stu-id="5c53c-123">**Edge Server**</span></span>

  - <span></span>  
    <span data-ttu-id="5c53c-124">[CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-124">[Get-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg398574(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5c53c-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-125">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5c53c-126">[CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-126">[Get-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg413008(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5c53c-127">[新-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-127">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5c53c-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-128">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="5c53c-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-129">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5c53c-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-130">[Test-CsAVEdgeConnectivity](https://technet.microsoft.com/library/JJ205138(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="5c53c-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5c53c-131">[Set-CsEdgeServer](https://technet.microsoft.com/library/Gg398859(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5c53c-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c53c-132">See Also</span></span>


[<span data-ttu-id="5c53c-133">Lync Server PowerShell 博客</span><span class="sxs-lookup"><span data-stu-id="5c53c-133">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="5c53c-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c53c-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

