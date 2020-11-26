---
title: Lync Server 2013：管理呼叫许可控制
description: Lync Server 2013：管理呼叫许可控制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing call admission control
ms:assetid: b0bd4783-6f47-408d-b010-2e30f9bc1770
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721851(v=OCS.15)
ms:contentKeyID: 49733784
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a1c01bff6d1dce48dea314b6704cc0f5ff7d6b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425960"
---
# <a name="managing-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="fdc3b-103">在 Lync Server 2013 中管理呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="fdc3b-103">Managing call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fdc3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fdc3b-104">

<span> </span></span></span>

<span data-ttu-id="fdc3b-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="fdc3b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="fdc3b-106">呼叫允许控制 (CAC) 根据可用网络带宽确定是否允许建立实时通信会话（如语音呼叫或视频呼叫）。</span><span class="sxs-lookup"><span data-stu-id="fdc3b-106">Call admission control (CAC) determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="fdc3b-107">使用以下过程管理 Lync Server 2013 环境的不同 CAC 功能。</span><span class="sxs-lookup"><span data-stu-id="fdc3b-107">Use the following procedures to manage different CAC features for your Lync Server 2013 environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fdc3b-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="fdc3b-108">In This Section</span></span>

  - [<span data-ttu-id="fdc3b-109">在 Lync Server 2013 中启用呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="fdc3b-109">Enabling call admission control in Lync Server 2013</span></span>](lync-server-2013-enabling-call-admission-control.md)

  - [<span data-ttu-id="fdc3b-110">管理 Lync Server 2013 中的网络带宽策略配置文件</span><span class="sxs-lookup"><span data-stu-id="fdc3b-110">Managing network bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-managing-network-bandwidth-policy-profiles.md)

  - [<span data-ttu-id="fdc3b-111">Lync Server 2013 中的网络区域</span><span class="sxs-lookup"><span data-stu-id="fdc3b-111">Network regions in Lync Server 2013</span></span>](lync-server-2013-network-regions.md)

  - [<span data-ttu-id="fdc3b-112">Lync Server 2013 中的网络区域路由</span><span class="sxs-lookup"><span data-stu-id="fdc3b-112">Network region routes in Lync Server 2013</span></span>](lync-server-2013-network-region-routes.md)

  - [<span data-ttu-id="fdc3b-113">Lync Server 2013 中的网站呼叫许可控制</span><span class="sxs-lookup"><span data-stu-id="fdc3b-113">Call admission control for sites in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-for-sites.md)

  - [<span data-ttu-id="fdc3b-114">在 Lync Server 2013 中启用和禁用媒体旁路</span><span class="sxs-lookup"><span data-stu-id="fdc3b-114">Enabling and disabling media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-media-bypass.md)

  - [<span data-ttu-id="fdc3b-115">在 Lync Server 2013 中链接网络区域</span><span class="sxs-lookup"><span data-stu-id="fdc3b-115">Linking network regions in Lync Server 2013</span></span>](lync-server-2013-linking-network-regions.md)

  - [<span data-ttu-id="fdc3b-116">在 Lync Server 2013 中管理网络子网</span><span class="sxs-lookup"><span data-stu-id="fdc3b-116">Managing network subnets in Lync Server 2013</span></span>](lync-server-2013-managing-network-subnets.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fdc3b-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fdc3b-117">See Also</span></span>


[<span data-ttu-id="fdc3b-118">Lync Server 2013 中的呼叫许可控制概述</span><span class="sxs-lookup"><span data-stu-id="fdc3b-118">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)  
  

<span data-ttu-id="fdc3b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fdc3b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

