---
title: 使用第三方 PSTN 网关或 PBX 时的呼叫允许控制
description: 使用第三方 PSTN 网关或 PBX 呼叫许可控制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control with a third-party PSTN gateway or PBX
ms:assetid: 95dc4ceb-bcad-48ee-86ec-af911727f853
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398762(v=OCS.15)
ms:contentKeyID: 48184850
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aaab42992047ecedcc00ea1ecf5cf69023e51097
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435798"
---
# <a name="call-admission-control-in-lync-server-2013-with-a-third-party-pstn-gateway-or-pbx"></a><span data-ttu-id="5e341-103">使用第三方 PSTN 网关或 PBX 时 Lync Server 2013 中的呼叫允许控制</span><span class="sxs-lookup"><span data-stu-id="5e341-103">Call admission control in Lync Server 2013 with a third-party PSTN gateway or PBX</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5e341-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5e341-104">

<span> </span></span></span>

<span data-ttu-id="5e341-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="5e341-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="5e341-106">本主题举例说明如何在中介服务器的网关接口与第三方公用电话交换网 (PSTN) 网关或专用交换机 (PBX) 之间的链接上部署呼叫允许控制 (CAC)。</span><span class="sxs-lookup"><span data-stu-id="5e341-106">This topic describes examples of how call admission control (CAC) can be deployed on the link between the Mediation Server’s gateway interface and a third-party public switched telephone network (PSTN) gateway or private branch exchange (PBX).</span></span>

<div>

## <a name="case-1-cac-between-the-mediation-server-and-a-pstn-gateway"></a><span data-ttu-id="5e341-107">示例 1：中介服务器与 PSTN 网关之间的 CAC</span><span class="sxs-lookup"><span data-stu-id="5e341-107">Case 1: CAC between the Mediation Server and a PSTN gateway</span></span>

<span data-ttu-id="5e341-108">可以在从中介服务器的网关接口连接到第三方 PBX 或 PSTN 网关的 WAN 链路上部署 CAC。</span><span class="sxs-lookup"><span data-stu-id="5e341-108">CAC can be deployed on the WAN link from the Mediation Server’s gateway interface to a third-party PBX or PSTN gateway.</span></span>

<span data-ttu-id="5e341-109">**示例 1：中介服务器与 PSTN 网关之间的 CAC**</span><span class="sxs-lookup"><span data-stu-id="5e341-109">**Case 1: CAC between the Mediation Server and a PSTN gateway**</span></span>

<span data-ttu-id="5e341-110">![示例 1：中介服务器与 PSTN 网关之间的 CAC](images/Gg398762.4bebf9ee-2732-4ea6-bbe5-0269b2903d8c(OCS.15).jpg "示例 1：中介服务器与 PSTN 网关之间的 CAC")</span><span class="sxs-lookup"><span data-stu-id="5e341-110">![Case 1: CAC between Mediation Server PSTN Gateway](images/Gg398762.4bebf9ee-2732-4ea6-bbe5-0269b2903d8c(OCS.15).jpg "Case 1: CAC between Mediation Server PSTN Gateway")</span></span>

<span data-ttu-id="5e341-111">在此示例中，在中介服务器和 PSTN 网关之间应用 CAC。</span><span class="sxs-lookup"><span data-stu-id="5e341-111">In this example, CAC is applied between the Mediation Server and a PSTN gateway.</span></span> <span data-ttu-id="5e341-112">如果网络站点1中的 Lync 客户端用户通过网络站点2中的 PSTN 网关放置 PSTN 呼叫，则媒体将通过 WAN 链接进行流动。</span><span class="sxs-lookup"><span data-stu-id="5e341-112">If a Lync client user at Network Site 1 places a PSTN call through the PSTN gateway in Network Site 2, the media flows through the WAN link.</span></span> <span data-ttu-id="5e341-113">因此，将对每个 PSTN 会话执行以下两个 CAC 检查：</span><span class="sxs-lookup"><span data-stu-id="5e341-113">Therefore, two CAC checks are performed for each PSTN session:</span></span>

  - <span data-ttu-id="5e341-114">在 Lync 客户端应用程序和中介服务器之间</span><span class="sxs-lookup"><span data-stu-id="5e341-114">Between the Lync client application and the Mediation Server</span></span>

  - <span data-ttu-id="5e341-115">在中介服务器和 PSTN 网关之间</span><span class="sxs-lookup"><span data-stu-id="5e341-115">Between the Mediation Server and the PSTN gateway</span></span>

<span data-ttu-id="5e341-116">这同时适用于网络站点 1 中的客户端接收的传入 PSTN 呼叫，以及网络站点 1 中的客户端应用程序发送的传出 PSTN 呼叫。</span><span class="sxs-lookup"><span data-stu-id="5e341-116">This works for both incoming PSTN calls to a client in Network Site 1, and for outgoing PSTN calls originating from a client application in Network Site 1.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="5e341-117">请确保 PSTN 网关所属的 IP 子网已配置并与网络站点 2 相关联。</span><span class="sxs-lookup"><span data-stu-id="5e341-117">Make sure that the IP subnet that the PSTN gateway belongs to is configured and associated with Network Site 2.</span></span><BR><span data-ttu-id="5e341-118">确保将中介服务器的两个接口所属的 IP 子网配置和与网络站点1相关联。</span><span class="sxs-lookup"><span data-stu-id="5e341-118">Make sure that the IP subnet that both interfaces of the Mediation Server belong to is configured and associated with Network Site 1.</span></span><BR><span data-ttu-id="5e341-119">有关详细信息，请参阅 <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">在 Lync Server 2013 中将子网与网络站点关联</A>。</span><span class="sxs-lookup"><span data-stu-id="5e341-119">For details, see <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">Associate a subnet with a network site in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="case-2-cac-between-the-mediation-server-and-a-third-party-pbx-with-media-termination-point"></a><span data-ttu-id="5e341-120">情况2：中介服务器和具有媒体终结点的第三方 PBX 之间的 CAC</span><span class="sxs-lookup"><span data-stu-id="5e341-120">Case 2: CAC between the Mediation Server and a third-party PBX with Media Termination Point</span></span>

<span data-ttu-id="5e341-121">此配置与示例 1 类似。</span><span class="sxs-lookup"><span data-stu-id="5e341-121">This configuration is similar to Case 1.</span></span> <span data-ttu-id="5e341-122">在这两种情况下，中介服务器都知道在 WAN 链接的另一端终止媒体的设备，并将中介服务器上的 PSTN 网关或 PBX 的 IP 地址配置为下一跃点 (MTP) 。</span><span class="sxs-lookup"><span data-stu-id="5e341-122">In both the cases, the Mediation Server knows what device terminates media at the opposite end of the WAN link, and the IP address of the PSTN gateway or PBX with Media Termination Point (MTP) is configured on the Mediation Server as the next hop.</span></span>

<span data-ttu-id="5e341-123">**示例 2：中介服务器与具有 MTP 的第三方 PBX 之间的 CAC**</span><span class="sxs-lookup"><span data-stu-id="5e341-123">**Case 2: CAC between the Mediation Server and a third-party PBX with MTP**</span></span>

<span data-ttu-id="5e341-124">![示例 2：中介服务器与具有 MTP 的 PBX 之间的 CAC](images/Gg398762.1c0b5263-c053-4cca-842f-85dd670760c8(OCS.15).jpg "示例 2：中介服务器与具有 MTP 的 PBX 之间的 CAC")</span><span class="sxs-lookup"><span data-stu-id="5e341-124">![Case 2: CAC between Mediation Server PBX with MTP](images/Gg398762.1c0b5263-c053-4cca-842f-85dd670760c8(OCS.15).jpg "Case 2: CAC between Mediation Server PBX with MTP")</span></span>

<span data-ttu-id="5e341-125">在此示例中，在中介服务器和 PBX/MTP 之间应用 CAC。</span><span class="sxs-lookup"><span data-stu-id="5e341-125">In this example, CAC is applied between the Mediation Server and the PBX/MTP.</span></span> <span data-ttu-id="5e341-126">如果网络站点1中的 Lync 客户端用户通过位于网络 Site 2 中的 PBX/MTP 放置 PSTN 呼叫，则媒体将通过 WAN 链接进行流动。</span><span class="sxs-lookup"><span data-stu-id="5e341-126">If a Lync client user at the Network Site 1 places a PSTN call through the PBX/MTP located in Network Site 2, the media flows through the WAN link.</span></span> <span data-ttu-id="5e341-127">因此，将对每个 PSTN 会话执行以下两个 CAC 检查：</span><span class="sxs-lookup"><span data-stu-id="5e341-127">Therefore, for each PSTN session two CAC checks are performed:</span></span>

  - <span data-ttu-id="5e341-128">在 Lync 客户端应用程序和中介服务器之间</span><span class="sxs-lookup"><span data-stu-id="5e341-128">Between the Lync client application and the Mediation Server</span></span>

  - <span data-ttu-id="5e341-129">在中介服务器和 PBX/MTP 之间</span><span class="sxs-lookup"><span data-stu-id="5e341-129">Between the Mediation Server and the PBX/MTP</span></span>

<span data-ttu-id="5e341-130">这同时适用于网络站点 1 中的客户端接收的传入 PSTN 呼叫，以及网络站点 1 中的客户端发送的传出 PSTN 呼叫。</span><span class="sxs-lookup"><span data-stu-id="5e341-130">This works for both incoming PSTN calls to a client in Network Site 1, and outgoing PSTN calls originating from a client in Network Site 1.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="5e341-131">请确保 MTP 所属的 IP 子网已配置并与网络站点 2 相关联。</span><span class="sxs-lookup"><span data-stu-id="5e341-131">Make sure that the IP subnet that the MTP belongs to is configured and associated with Network Site 2.</span></span><BR><span data-ttu-id="5e341-132">确保将中介服务器的两个接口所属的 IP 子网配置和与网络站点1相关联。</span><span class="sxs-lookup"><span data-stu-id="5e341-132">Make sure that the IP subnet that both interfaces of the Mediation Server belong to is configured and associated with Network Site 1.</span></span><BR><span data-ttu-id="5e341-133">有关详细信息，请参阅 <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">在 Lync Server 2013 中将子网与网络站点关联</A>。</span><span class="sxs-lookup"><span data-stu-id="5e341-133">For details, see <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">Associate a subnet with a network site in Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="case-3-cac-between-the-mediation-server-and-a-third-party-pbx-without-a-media-termination-point"></a><span data-ttu-id="5e341-134">情况3：在中介服务器与没有媒体终结点的第三方 PBX 之间使用 CAC</span><span class="sxs-lookup"><span data-stu-id="5e341-134">Case 3: CAC between the Mediation Server and a third-party PBX without a Media Termination Point</span></span>

<span data-ttu-id="5e341-135">示例 3 与前两个示例略有不同。</span><span class="sxs-lookup"><span data-stu-id="5e341-135">Case 3 is slightly different from the first two cases.</span></span> <span data-ttu-id="5e341-136">如果在第三方 PBX 上没有 MTP，而对于第三方 PBX 的传出会话请求，则中介服务器不知道媒体将在 PBX 边界内终止的位置。</span><span class="sxs-lookup"><span data-stu-id="5e341-136">If there is no MTP on the third-party PBX, for an outgoing session request to the third-party PBX the Mediation Server does not know where media will terminate in the PBX boundary.</span></span> <span data-ttu-id="5e341-137">在这种情况下，媒体将直接在中介服务器和第三方终结点设备之间流动。</span><span class="sxs-lookup"><span data-stu-id="5e341-137">In this case, the media flows directly between the Mediation Server and the third-party endpoint device.</span></span>

<span data-ttu-id="5e341-138">**示例 3：中介服务器与没有 MTP 的第三方 PBX 之间的 CAC**</span><span class="sxs-lookup"><span data-stu-id="5e341-138">**Case 3: CAC between the Mediation Server and a third-party PBX without MTP**</span></span>

<span data-ttu-id="5e341-139">![示例 3：中介服务器与不具有 MTP 的 PBX 之间的 CAC](images/Gg398762.f4bcf800-3a68-4037-bb3f-adb2fdf50d32(OCS.15).jpg "示例 3：中介服务器与不具有 MTP 的 PBX 之间的 CAC")</span><span class="sxs-lookup"><span data-stu-id="5e341-139">![Case 3: CAC between Mediation Server PBX no MTP](images/Gg398762.f4bcf800-3a68-4037-bb3f-adb2fdf50d32(OCS.15).jpg "Case 3: CAC between Mediation Server PBX no MTP")</span></span>

<span data-ttu-id="5e341-140">在此示例中，如果网络站点1上的 Lync 客户端用户通过 PBX 将呼叫与用户进行呼叫，则中介服务器只能在 Lync 客户端应用程序和中介服务器) 之间的代理端 (执行 CAC 检查。</span><span class="sxs-lookup"><span data-stu-id="5e341-140">In this example, if a Lync client user at Network Site 1 places a call to a user through the PBX, the Mediation Server is able to perform CAC checks only on the proxy leg (between the Lync client application and Mediation Server).</span></span> <span data-ttu-id="5e341-141">由于中介服务器在请求会话时没有终结点设备的相关信息，因此在通话建立之前，不能在中介服务器和第三方终结) 点之间的 WAN 链接 (上执行 CAC 检查。</span><span class="sxs-lookup"><span data-stu-id="5e341-141">Because the Mediation Server does not have information about the endpoint device while the session is being requested, CAC checks cannot be performed on the WAN link (between the Mediation Server and the third-party endpoint) prior to call establishment.</span></span> <span data-ttu-id="5e341-142">但是，在建立会话后，中介服务器将为主干上使用的带宽提供便利。</span><span class="sxs-lookup"><span data-stu-id="5e341-142">After the session is established, however, the Mediation Server facilitates in accounting for the bandwidth used on the trunk.</span></span>

<span data-ttu-id="5e341-143">对于源自第三方终结点的调用，有关该终结点设备的信息在会话请求时可用，并且可以在中介服务器的两面上执行 CAC 检查。</span><span class="sxs-lookup"><span data-stu-id="5e341-143">For calls that originate from the third-party endpoint, the information about that endpoint device is available at the time of session request and CAC check can be performed on both the sides of the Mediation Server.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="5e341-144">请确保终结点设备所属的 IP 子网已配置并与网络站点 2 相关联。</span><span class="sxs-lookup"><span data-stu-id="5e341-144">Make sure that the IP subnet that the endpoint devices belong to is configured and associated with Network Site 2.</span></span><BR><span data-ttu-id="5e341-145">确保将中介服务器的两个接口所属的 IP 子网配置和与网络站点1相关联。</span><span class="sxs-lookup"><span data-stu-id="5e341-145">Make sure that the IP subnet that both interfaces of the Mediation Server belong to is configured and associated with Network Site 1.</span></span><BR><span data-ttu-id="5e341-146">有关详细信息，请参阅 <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">在 Lync Server 2013 中将子网与网络站点关联</A>。</span><span class="sxs-lookup"><span data-stu-id="5e341-146">For details, see <A href="lync-server-2013-associate-a-subnet-with-a-network-site.md">Associate a subnet with a network site in Lync Server 2013</A>.</span></span>



<span data-ttu-id="5e341-147"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5e341-147"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

