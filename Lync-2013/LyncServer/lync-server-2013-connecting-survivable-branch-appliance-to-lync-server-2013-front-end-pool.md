---
title: 将 Survivable Branch Appliance 连接到 Lync Server 2013 前端池
description: 将 Survivable 分支装置连接到 Lync Server 2013 前端池。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool
ms:assetid: 3c7ca33f-5295-4d82-9152-41d8bc6f35cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688026(v=OCS.15)
ms:contentKeyID: 49733616
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ef917d3db6a1d653ac716d6c078e1df240fb31d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432259"
---
# <a name="connecting-survivable-branch-appliance-to-lync-server-2013-front-end-pool"></a><span data-ttu-id="822b3-103">将 Survivable Branch Appliance 连接到 Lync Server 2013 前端池</span><span class="sxs-lookup"><span data-stu-id="822b3-103">Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="822b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="822b3-104">

<span> </span></span></span>

<span data-ttu-id="822b3-105">_**主题上次修改时间：** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="822b3-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="822b3-106">每个 Survivable 分支装置 (SBA) 都与一个前端池相关联，后者充当 SBA 的备份注册机构。</span><span class="sxs-lookup"><span data-stu-id="822b3-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool, which serves as a backup Registrar for the SBA.</span></span> <span data-ttu-id="822b3-107">当前端池升级到 Lync Server 2013 时，在升级前端池时，SBA 必须与前端池解除关联。</span><span class="sxs-lookup"><span data-stu-id="822b3-107">When the Front End pool is upgraded to Lync Server 2013, the SBA must be disassociated from the Front End pool while the Front End pool is upgraded.</span></span> <span data-ttu-id="822b3-108">升级前端池后，SBA 可以与前端池 reassociated。</span><span class="sxs-lookup"><span data-stu-id="822b3-108">After the Front End pool is upgraded, the SBA can be reassociated with the Front End pool.</span></span> <span data-ttu-id="822b3-109">这包括从拓扑生成器的拓扑中删除 SBA，然后再次将 SBA 添加到拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="822b3-109">This involves deleting the SBA from the topology in Topology Builder and then adding the SBA, again, to Topology Builder.</span></span> <span data-ttu-id="822b3-110">在从拓扑结构中删除 SBA 之前，必须将驻留在 SBA 上的用户移动到另一个前端池。</span><span class="sxs-lookup"><span data-stu-id="822b3-110">Users homed on the SBA must be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="822b3-111">将 SBA 添加回拓扑后，这些用户可以移回 SBA。</span><span class="sxs-lookup"><span data-stu-id="822b3-111">After the SBA is added back to the topology, those users can be moved back to the SBA.</span></span>

<span data-ttu-id="822b3-112">下面总结了这些步骤：</span><span class="sxs-lookup"><span data-stu-id="822b3-112">These steps are summarized below:</span></span>

1.  <span data-ttu-id="822b3-113">将驻留在 SBA 上的分支用户移到另一个前端池。</span><span class="sxs-lookup"><span data-stu-id="822b3-113">Move branch users homed on SBA to another Front End pool.</span></span>

2.  <span data-ttu-id="822b3-114">从拓扑中删除 SBA，以将现有的前端池与备份注册机构解除关联。</span><span class="sxs-lookup"><span data-stu-id="822b3-114">Remove SBA from your topology to disassociate the existing Front End pool as the backup Registrar.</span></span>

3.  <span data-ttu-id="822b3-115">将前端池升级到 Microsoft Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="822b3-115">Upgrade Front End pool to Microsoft Lync Server 2013.</span></span>

4.  <span data-ttu-id="822b3-116">将 SBA 添加回拓扑。</span><span class="sxs-lookup"><span data-stu-id="822b3-116">Add SBA back into your topology.</span></span>

5.  <span data-ttu-id="822b3-117">将新的前端池与 SBA 作为备份注册机构相关联。</span><span class="sxs-lookup"><span data-stu-id="822b3-117">Associate the new Front End pool to the SBA as a backup Registrar.</span></span>

6.  <span data-ttu-id="822b3-118">将分支用户移回 SBA。</span><span class="sxs-lookup"><span data-stu-id="822b3-118">Move branch users back to the SBA.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="822b3-119">本节内容</span><span class="sxs-lookup"><span data-stu-id="822b3-119">In This Section</span></span>

  - [<span data-ttu-id="822b3-120">将 Lync Server 2013 Survivable Branch Appliance 分支站点添加到您的拓扑</span><span class="sxs-lookup"><span data-stu-id="822b3-120">Add Lync Server 2013 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology.md)

  - [<span data-ttu-id="822b3-121">将 Lync Server 2010 Survivable Branch Appliance 分支站点添加到您的拓扑</span><span class="sxs-lookup"><span data-stu-id="822b3-121">Add Lync Server 2010 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2010-survivable-branch-appliance-branch-site-to-your-topology.md)

<span data-ttu-id="822b3-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="822b3-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

