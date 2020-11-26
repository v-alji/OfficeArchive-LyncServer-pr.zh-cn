---
title: Lync Server 2013：配置中继
description: Lync Server 2013：配置中继。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring trunks
ms:assetid: 0c339511-a185-484e-94f0-dbe918b7e48a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398170(v=OCS.15)
ms:contentKeyID: 48183389
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07d9503cd38419a7145796a6edf8484a14cdeb53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432462"
---
# <a name="configuring-trunks-in-lync-server-2013"></a><span data-ttu-id="7ecb9-103">在 Lync Server 2013 中配置中继</span><span class="sxs-lookup"><span data-stu-id="7ecb9-103">Configuring trunks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ecb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ecb9-104">

<span> </span></span></span>

<span data-ttu-id="7ecb9-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="7ecb9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="7ecb9-106">作为企业语音部署的一部分，你可以在中介服务器和一个或多个以下对等的一个或多个对等之间配置主干，以便为组织中的企业语音客户端和设备提供公共交换电话网络 (PSTN) 连接：</span><span class="sxs-lookup"><span data-stu-id="7ecb9-106">As part of Enterprise Voice deployment, you can configure a trunk between a Mediation Server and one or more of the following peers to provide public switched telephone network (PSTN) connectivity for Enterprise Voice clients and devices in your organization:</span></span>

  - <span data-ttu-id="7ecb9-107">到 Internet 电话服务提供商 (ITSP) 的 SIP 中继连接</span><span class="sxs-lookup"><span data-stu-id="7ecb9-107">SIP trunk connection to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="7ecb9-108">PSTN 网关</span><span class="sxs-lookup"><span data-stu-id="7ecb9-108">PSTN gateway</span></span>

  - <span data-ttu-id="7ecb9-109">专用交换机 (PBX)</span><span class="sxs-lookup"><span data-stu-id="7ecb9-109">Private branch exchange (PBX)</span></span>

<span data-ttu-id="7ecb9-110">有关详细信息，请参阅规划文档中的 [Lync Server 2013 中的 "规划 PSTN 连接](lync-server-2013-planning-for-pstn-connectivity.md) "。</span><span class="sxs-lookup"><span data-stu-id="7ecb9-110">For details, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) in the Planning documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7ecb9-111">在开始中继配置之前，验证已创建拓扑，并且中介服务器及其对等已配置并与另一个关联。</span><span class="sxs-lookup"><span data-stu-id="7ecb9-111">Before you begin trunk configuration, verify that the topology has been created and that the Mediation Server and its peer have been configured and associated with one another.</span></span> <span data-ttu-id="7ecb9-112">有关详细信息，请参阅部署文档中 <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Lync Server 2013 的拓扑生成器中的 "定义网关</A> "。</span><span class="sxs-lookup"><span data-stu-id="7ecb9-112">For details, see <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Define a gateway in Topology Builder in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="7ecb9-113">作为主干配置的一部分，你可以启用 Lync Server 2013 媒体绕过功能，这使媒体能够绕过中介服务器。</span><span class="sxs-lookup"><span data-stu-id="7ecb9-113">As a part of trunk configuration, you can enable the Lync Server 2013 media bypass feature, which enables media to bypass the Mediation Server.</span></span> <span data-ttu-id="7ecb9-114">中继可以使用或不启用媒体旁路进行配置，但我们强烈建议你启用它。</span><span class="sxs-lookup"><span data-stu-id="7ecb9-114">Trunks can be configured either with or without media bypass enabled, but we strongly recommend that you enable it.</span></span> <span data-ttu-id="7ecb9-115">有关详细信息，请参阅规划文档中的在 <A href="lync-server-2013-planning-for-media-bypass.md">Lync Server 2013 中规划媒体旁路</A> 。</span><span class="sxs-lookup"><span data-stu-id="7ecb9-115">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7ecb9-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="7ecb9-116">In This Section</span></span>

  - [<span data-ttu-id="7ecb9-117">Lync Server 2013 中的多个中继支持</span><span class="sxs-lookup"><span data-stu-id="7ecb9-117">Multiple trunk support in Lync Server 2013</span></span>](lync-server-2013-multiple-trunk-support.md)

  - [<span data-ttu-id="7ecb9-118">Lync Server 2013 中的中继间路由</span><span class="sxs-lookup"><span data-stu-id="7ecb9-118">Inter-trunk routing in Lync Server 2013</span></span>](lync-server-2013-inter-trunk-routing.md)

  - [<span data-ttu-id="7ecb9-119">在 Lync Server 2013 中查看中继配置信息</span><span class="sxs-lookup"><span data-stu-id="7ecb9-119">View trunk configuration information in Lync Server 2013</span></span>](lync-server-2013-view-trunk-configuration-information.md)

  - [<span data-ttu-id="7ecb9-120">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ecb9-120">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="7ecb9-121">在 Lync Server 2013 中配置不使用 "媒体旁路" 的主干</span><span class="sxs-lookup"><span data-stu-id="7ecb9-121">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

  - [<span data-ttu-id="7ecb9-122">在 Lync Server 2013 中创建新的主干配置设置集合</span><span class="sxs-lookup"><span data-stu-id="7ecb9-122">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-a-new-collection-of-trunk-configuration-settings.md)

  - [<span data-ttu-id="7ecb9-123">删除 Lync Server 2013 中的现有 SIP 中继配置设置集合</span><span class="sxs-lookup"><span data-stu-id="7ecb9-123">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="7ecb9-124">在 Lync Server 2013 中修改 SIP 中继配置设置</span><span class="sxs-lookup"><span data-stu-id="7ecb9-124">Modify SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-modify-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="7ecb9-125">在 Lync Server 2013 中测试 SIP 中继配置设置</span><span class="sxs-lookup"><span data-stu-id="7ecb9-125">Test SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-test-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="7ecb9-126">在 Lync Server 2013 中查看有关单个 SIP 中继的信息</span><span class="sxs-lookup"><span data-stu-id="7ecb9-126">View information about individual SIP trunks in Lync Server 2013</span></span>](lync-server-2013-view-information-about-individual-sip-trunks.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7ecb9-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ecb9-127">See Also</span></span>


[<span data-ttu-id="7ecb9-128">在 Lync Server 2013 的拓扑生成器中定义网关</span><span class="sxs-lookup"><span data-stu-id="7ecb9-128">Define a gateway in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-gateway-in-topology-builder.md)  


[<span data-ttu-id="7ecb9-129">在 Lync Server 2013 中规划 PSTN 连接</span><span class="sxs-lookup"><span data-stu-id="7ecb9-129">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
[<span data-ttu-id="7ecb9-130">在 Lync Server 2013 中规划媒体旁路</span><span class="sxs-lookup"><span data-stu-id="7ecb9-130">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="7ecb9-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ecb9-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

