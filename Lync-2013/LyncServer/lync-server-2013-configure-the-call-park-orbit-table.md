---
title: Lync Server 2013：配置呼叫寄存通道表
description: Lync Server 2013：配置 "呼叫公园轨道" 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Call Park orbit table
ms:assetid: e5cc0c19-7b2c-48e7-a21d-cfb23c842f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399020(v=OCS.15)
ms:contentKeyID: 48185666
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce9fb35c2958a426888d83d075064c88ddae4bfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433631"
---
# <a name="configure-the-call-park-orbit-table-in-lync-server-2013"></a><span data-ttu-id="a6179-103">在 Lync Server 2013 中配置呼叫寄存通道表</span><span class="sxs-lookup"><span data-stu-id="a6179-103">Configure the Call Park orbit table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6179-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6179-104">

<span> </span></span></span>

<span data-ttu-id="a6179-105">_**主题上次修改时间：** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="a6179-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="a6179-106">呼叫寄存使用用于停车呼叫的 "轨道"。</span><span class="sxs-lookup"><span data-stu-id="a6179-106">Call Park uses orbits for parking calls.</span></span> <span data-ttu-id="a6179-107">在用户可以停止和检索呼叫之前，必须配置 "呼叫公园轨道" 表。</span><span class="sxs-lookup"><span data-stu-id="a6179-107">Before users can park and retrieve calls, you must configure the Call Park orbit table.</span></span> <span data-ttu-id="a6179-108">你需要指定扩展号码的范围 ("轨道式") 你的组织将为停车调用保留，并通过指定处理每个区域的调用驻留池来定义这些范围的路由。</span><span class="sxs-lookup"><span data-stu-id="a6179-108">You need to specify the ranges of extension numbers (orbits) that your organization will reserve for parking calls and define the routing for those ranges by specifying which Call Park pool handles each range.</span></span> <span data-ttu-id="a6179-109">定义通道范围时，目标是具有足够的通道，以便不会在短时间内重用任何一个通道，但又不能有太多通道，以致于不得不限制用户或其他服务可使用的分机数量。</span><span class="sxs-lookup"><span data-stu-id="a6179-109">When you define orbit ranges, the goal is to have enough orbits so that any one orbit is not reused too quickly, but not so many orbits that you limit the number of extensions available for users or other services.</span></span> <span data-ttu-id="a6179-110">你可以为部署呼叫驻留应用程序的每个 Lync 服务器池创建多个呼叫驻留轨道范围。</span><span class="sxs-lookup"><span data-stu-id="a6179-110">You can create multiple Call Park orbit ranges for each Lync Server pool where the Call Park application is deployed.</span></span> <span data-ttu-id="a6179-111">每个呼叫驻留的 "轨道" 范围必须具有全局唯一名称和一组唯一的扩展。</span><span class="sxs-lookup"><span data-stu-id="a6179-111">Each Call Park orbit range must have a globally unique name and a unique set of extensions.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a6179-p102">每个通道范围包含的通道数通常不超过 100。范围可以更大一点，只要每个范围的通道数小于最大值 10,000 且每个池的通道数小于 50,000。如果范围太小，很快就会重用通道。</span><span class="sxs-lookup"><span data-stu-id="a6179-p102">An orbit range typically encompasses 100 or fewer orbits. Each range can be much larger, as long as it is smaller than the maximum of 10,000 orbits per range and you have fewer than 50,000 orbits per pool. If a range is too small, the orbits are reused more quickly.</span></span>



</div>

<span data-ttu-id="a6179-115">请使用虚拟分机（未向其分配用户或电话的分机）块作为通道范围。</span><span class="sxs-lookup"><span data-stu-id="a6179-115">Use blocks of virtual extensions (extensions that have no user or phone assigned to them) for your orbit ranges.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6179-116">分配直接向内拨号 (在 "呼叫公园轨道" 表中不支持以轨道数字形式) 数字。</span><span class="sxs-lookup"><span data-stu-id="a6179-116">Assigning Direct Inward Dialing (DID) numbers as orbit numbers in the Call Park orbit table is not supported.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a6179-117">本节内容</span><span class="sxs-lookup"><span data-stu-id="a6179-117">In This Section</span></span>

[<span data-ttu-id="a6179-118">在 Lync Server 2013 中创建或修改呼叫寄存的轨道范围</span><span class="sxs-lookup"><span data-stu-id="a6179-118">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

<span data-ttu-id="a6179-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6179-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

