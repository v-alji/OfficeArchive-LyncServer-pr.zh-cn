---
title: Lync Server 2013：在分支站点提供 PSTN 连接
description: Lync Server 2013：在分支站点上提供 PSTN 连接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Providing PSTN connectivity at a branch site
ms:assetid: d78d76fb-2dd1-42cb-b25a-bfaff9650a70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398945(v=OCS.15)
ms:contentKeyID: 48185633
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63cbc03f78a27bda14c2906e31cc68bed5870878
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436732"
---
# <a name="providing-pstn-connectivity-at-a-branch-site-in-lync-server-2013"></a><span data-ttu-id="bae6c-103">在 Lync Server 2013 中在分支站点提供 PSTN 连接</span><span class="sxs-lookup"><span data-stu-id="bae6c-103">Providing PSTN connectivity at a branch site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bae6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bae6c-104">

<span> </span></span></span>

<span data-ttu-id="bae6c-105">_**主题上次修改时间：** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="bae6c-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="bae6c-106">我们建议使用 Microsoft Lync Server 2013、计划工具将分支站点添加到你的拓扑，并在分支站点中设置你的语音基础结构。</span><span class="sxs-lookup"><span data-stu-id="bae6c-106">We recommend using the Microsoft Lync Server 2013, Planning Tool to add branch sites to your topology and to set up your voice infrastructure in branch sites.</span></span>

<span data-ttu-id="bae6c-107">如果你未使用计划工具，请先使用本部分中的主题中的过程（首先）添加分支站点，然后通过定义 IP/公共交换电话网络 (PSTN) 网关和/或通过使用或不使用媒体旁路) 配置 SIP 中继 (来设置你的语音基础结构。</span><span class="sxs-lookup"><span data-stu-id="bae6c-107">If you are not using the Planning Tool, use the procedures in the topics in this section—first, to add the branch sites, and then, to set up your voice infrastructure by defining the IP/public switched telephone network (PSTN) gateway and/or by configuring the SIP trunk (with or without media bypass).</span></span> <span data-ttu-id="bae6c-108">将专用分支 exchange (PBX) 连接到分支站点是另一个选项。</span><span class="sxs-lookup"><span data-stu-id="bae6c-108">Connecting a private branch exchange (PBX) to the branch site is another option.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bae6c-109">如果要提供分支站点弹性，必须在分支站点部署 Survivable 分支装置、Survivable 分支服务器或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="bae6c-109">If you want to provide branch-site resiliency, you must deploy a Survivable Branch Appliance, a Survivable Branch Server, or Standard Edition server at the branch site.</span></span> <span data-ttu-id="bae6c-110">有关详细信息，请参阅部署文档中的使用 Lync Server 2013 或<A href="lync-server-2013-deploying-lync-server.md">部署 Lync server 2013</A>的<A href="lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md">Survivable 分支装置或服务器</A>。</span><span class="sxs-lookup"><span data-stu-id="bae6c-110">For details, see <A href="lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md">Deploying a Survivable Branch Appliance or Server with Lync Server 2013</A> or <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A>, as appropriate, in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bae6c-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="bae6c-111">In This Section</span></span>

  - [<span data-ttu-id="bae6c-112">在 Lync Server 2013 中向拓扑添加分支站点</span><span class="sxs-lookup"><span data-stu-id="bae6c-112">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="bae6c-113">在 Lync Server 2013 中为分支站点定义 PSTN 网关</span><span class="sxs-lookup"><span data-stu-id="bae6c-113">Define a PSTN gateway for a branch site in Lync Server 2013</span></span>](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md)

  - [<span data-ttu-id="bae6c-114">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bae6c-114">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="bae6c-115">在 Lync Server 2013 中配置不使用 "媒体旁路" 的主干</span><span class="sxs-lookup"><span data-stu-id="bae6c-115">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bae6c-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bae6c-116">See Also</span></span>


[<span data-ttu-id="bae6c-117">在 Lync Server 2013 中规划媒体旁路</span><span class="sxs-lookup"><span data-stu-id="bae6c-117">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
[<span data-ttu-id="bae6c-118">在 Lync Server 2013 中规划 PSTN 连接</span><span class="sxs-lookup"><span data-stu-id="bae6c-118">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
  

<span data-ttu-id="bae6c-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bae6c-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

