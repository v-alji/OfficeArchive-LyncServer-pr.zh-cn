---
title: Lync Server 2013：呼叫寄存容量规划
description: Lync Server 2013：通话寄存的容量规划。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Call Park
ms:assetid: 75520310-760a-4b1b-bcc1-4d724d13f87a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416493(v=OCS.15)
ms:contentKeyID: 48184529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053a6dabad9d10540e84e9e4f43de09057c295f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392419"
---
# <a name="capacity-planning-for-call-park-in-lync-server-2013"></a><span data-ttu-id="fcf7d-103">Lync Server 2013 中的呼叫寄存容量规划</span><span class="sxs-lookup"><span data-stu-id="fcf7d-103">Capacity planning for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fcf7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fcf7d-104">

<span> </span></span></span>

<span data-ttu-id="fcf7d-105">_**主题上次修改时间：** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="fcf7d-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="fcf7d-106">下表介绍了可用作容量规划要求基础的 "呼叫驻留" 用户模型。</span><span class="sxs-lookup"><span data-stu-id="fcf7d-106">The following table describes the Call Park user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="fcf7d-107">请记住，对于灾难恢复容量规划，配对池的每个池都应该能够处理两个池中的呼叫驻留服务的工作负荷。</span><span class="sxs-lookup"><span data-stu-id="fcf7d-107">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services in both pools.</span></span>



</div>

### <a name="call-park-user-model"></a><span data-ttu-id="fcf7d-108">呼叫寄存用户模型</span><span class="sxs-lookup"><span data-stu-id="fcf7d-108">Call Park User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcf7d-109">指标</span><span class="sxs-lookup"><span data-stu-id="fcf7d-109">Metric</span></span></th>
<th><span data-ttu-id="fcf7d-110">每个前端池 (有8个前端服务器) </span><span class="sxs-lookup"><span data-stu-id="fcf7d-110">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="fcf7d-111">每台 Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="fcf7d-111">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcf7d-112">寄存速率</span><span class="sxs-lookup"><span data-stu-id="fcf7d-112">Park rate</span></span></p></td>
<td><p><span data-ttu-id="fcf7d-113">每分钟 8 个</span><span class="sxs-lookup"><span data-stu-id="fcf7d-113">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="fcf7d-114">每分钟 1 个</span><span class="sxs-lookup"><span data-stu-id="fcf7d-114">1 per minute</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcf7d-115">取回寄存呼叫的速率</span><span class="sxs-lookup"><span data-stu-id="fcf7d-115">Retrieve parked call rate</span></span></p></td>
<td><p><span data-ttu-id="fcf7d-116">每分钟 8 个</span><span class="sxs-lookup"><span data-stu-id="fcf7d-116">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="fcf7d-117">每分钟 1 个</span><span class="sxs-lookup"><span data-stu-id="fcf7d-117">1 per minute</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcf7d-118">平均寄存持续时间</span><span class="sxs-lookup"><span data-stu-id="fcf7d-118">Average park duration</span></span></p></td>
<td><p><span data-ttu-id="fcf7d-119">60 秒</span><span class="sxs-lookup"><span data-stu-id="fcf7d-119">60 seconds</span></span></p></td>
<td><p><span data-ttu-id="fcf7d-120">60 秒</span><span class="sxs-lookup"><span data-stu-id="fcf7d-120">60 seconds</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fcf7d-121">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fcf7d-121">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

