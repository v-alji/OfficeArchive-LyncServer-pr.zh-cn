---
title: Lync Server 2013：部署高级企业语音功能
description: Lync Server 2013：部署高级企业语音功能。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying advanced Enterprise Voice features
ms:assetid: 286d9c0b-9442-448f-a6e5-95b3034278fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425753(v=OCS.15)
ms:contentKeyID: 48183675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5cab05de60e1df1611a14af1f5239c24402c6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430110"
---
# <a name="deploying-advanced-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="00054-103">在 Lync Server 2013 中部署高级企业语音功能</span><span class="sxs-lookup"><span data-stu-id="00054-103">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00054-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00054-104">

<span> </span></span></span>

<span data-ttu-id="00054-105">_**主题上次修改时间：** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="00054-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="00054-106">为组织配置基本企业语音功能之后，可以选择按照本节中的过程部署一个或多个高级企业语音功能。</span><span class="sxs-lookup"><span data-stu-id="00054-106">After you have configured basic Enterprise Voice functionality for your organization, you can optionally deploy one or more advanced Enterprise Voice features by following the procedures in this section.</span></span>

<span data-ttu-id="00054-107">有关高级企业语音功能的详细信息，请参阅 [适用于 Lync Server 2013 的规划](lync-server-2013-planning.md) 文档的以下部分：</span><span class="sxs-lookup"><span data-stu-id="00054-107">For details about the advanced Enterprise Voice features, see the following sections of the [Planning for Lync Server 2013](lync-server-2013-planning.md) documentation:</span></span>

  - [<span data-ttu-id="00054-108">在 Lync Server 2013 中规划呼叫允许控制</span><span class="sxs-lookup"><span data-stu-id="00054-108">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="00054-109">在 Lync Server 2013 中规划紧急服务 (E9-1-1)</span><span class="sxs-lookup"><span data-stu-id="00054-109">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="00054-110">在 Lync Server 2013 中规划媒体旁路</span><span class="sxs-lookup"><span data-stu-id="00054-110">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

<div>

## <a name="in-this-section"></a><span data-ttu-id="00054-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="00054-111">In This Section</span></span>

  - [<span data-ttu-id="00054-112">关于 Lync Server 2013 中的网络区域、站点和子网</span><span class="sxs-lookup"><span data-stu-id="00054-112">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="00054-113">在 Lync Server 2013 中创建或修改网络区域</span><span class="sxs-lookup"><span data-stu-id="00054-113">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="00054-114">在 Lync Server 2013 中创建或修改网络站点</span><span class="sxs-lookup"><span data-stu-id="00054-114">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="00054-115">在 Lync Server 2013 中将子网与网络站点相关联</span><span class="sxs-lookup"><span data-stu-id="00054-115">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

  - [<span data-ttu-id="00054-116">在 Lync Server 2013 中配置呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="00054-116">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)

  - [<span data-ttu-id="00054-117">在 Lync Server 2013 中配置增强型 9-1-1</span><span class="sxs-lookup"><span data-stu-id="00054-117">Configure Enhanced 9-1-1 in Lync Server 2013</span></span>](lync-server-2013-configure-enhanced-9-1-1.md)

  - [<span data-ttu-id="00054-118">在 Lync Server 2013 中配置媒体绕过</span><span class="sxs-lookup"><span data-stu-id="00054-118">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)

<span data-ttu-id="00054-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00054-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

