---
title: Lync Server 2013：组呼叫装货的容量规划
description: Lync Server 2013：组呼叫装货的容量规划。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Group Call Pickup
ms:assetid: 0d654a19-6cf0-4118-903d-ec2c4e519253
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ984297(v=OCS.15)
ms:contentKeyID: 51476680
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12648c57d1036a0ed27c60ef6399bf570c5dcd3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435570"
---
# <a name="capacity-planning-for-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="801f0-103">Lync Server 2013 中组呼叫装货的容量规划</span><span class="sxs-lookup"><span data-stu-id="801f0-103">Capacity planning for Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="801f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="801f0-104">

<span> </span></span></span>

<span data-ttu-id="801f0-105">_**主题上次修改时间：** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="801f0-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="801f0-106">下表介绍了组呼叫装货用户模型，您可以将其用作容量规划要求的基础。</span><span class="sxs-lookup"><span data-stu-id="801f0-106">The following table describes the Group Call Pickup user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="801f0-107">组呼叫分拣基于呼叫寄存应用程序。</span><span class="sxs-lookup"><span data-stu-id="801f0-107">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="801f0-108">请记住，对于灾难恢复容量规划，配对池的每个池都应该能够处理呼叫驻留服务的工作负荷，包括组呼叫在两个池中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="801f0-108">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services, including Group Call Pickup, in both pools.</span></span>



</div>

### <a name="group-call-pickup-user-model"></a><span data-ttu-id="801f0-109">组呼叫装货用户模型</span><span class="sxs-lookup"><span data-stu-id="801f0-109">Group Call Pickup User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="801f0-110">指标</span><span class="sxs-lookup"><span data-stu-id="801f0-110">Metric</span></span></th>
<th><span data-ttu-id="801f0-111">每个前端池 (有8个前端服务器) </span><span class="sxs-lookup"><span data-stu-id="801f0-111">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="801f0-112">每台 Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="801f0-112">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="801f0-113">建议的每组用户数</span><span class="sxs-lookup"><span data-stu-id="801f0-113">Recommended number of users per group</span></span></p></td>
<td><p><span data-ttu-id="801f0-114">50</span><span class="sxs-lookup"><span data-stu-id="801f0-114">50</span></span></p></td>
<td><p><span data-ttu-id="801f0-115">50</span><span class="sxs-lookup"><span data-stu-id="801f0-115">50</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="801f0-116">建议的组数</span><span class="sxs-lookup"><span data-stu-id="801f0-116">Recommended number of groups</span></span></p></td>
<td><p><span data-ttu-id="801f0-117">500</span><span class="sxs-lookup"><span data-stu-id="801f0-117">500</span></span></p></td>
<td><p><span data-ttu-id="801f0-118">60</span><span class="sxs-lookup"><span data-stu-id="801f0-118">60</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="801f0-119">针对组内呼叫应答启用的每个池的最大用户数</span><span class="sxs-lookup"><span data-stu-id="801f0-119">Maximum number of users per pool enabled for Group Call Pickup</span></span></p></td>
<td><p><span data-ttu-id="801f0-120">25,000</span><span class="sxs-lookup"><span data-stu-id="801f0-120">25,000</span></span></p></td>
<td><p><span data-ttu-id="801f0-121">3,000</span><span class="sxs-lookup"><span data-stu-id="801f0-121">3,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="801f0-122">每个池每分钟针对组内呼叫应答启用的所有用户的最大传入呼叫速率</span><span class="sxs-lookup"><span data-stu-id="801f0-122">Maximum rate of incoming calls to total users enabled for Group Call Pickup per pool per minute</span></span></p></td>
<td><p><span data-ttu-id="801f0-123">500</span><span class="sxs-lookup"><span data-stu-id="801f0-123">500</span></span></p></td>
<td><p><span data-ttu-id="801f0-124">60</span><span class="sxs-lookup"><span data-stu-id="801f0-124">60</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="801f0-125">每个池每分钟用户使用组内呼叫应答检索的最大呼叫速率</span><span class="sxs-lookup"><span data-stu-id="801f0-125">Maximum rate of calls retrieved by users with Group Call Pickup per pool per minute</span></span></p></td>
<td><p><span data-ttu-id="801f0-126">200</span><span class="sxs-lookup"><span data-stu-id="801f0-126">200</span></span></p></td>
<td><p><span data-ttu-id="801f0-127">二十五</span><span class="sxs-lookup"><span data-stu-id="801f0-127">25</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="801f0-128">对于少于八个前端服务器的前端池，按线性计算指标。</span><span class="sxs-lookup"><span data-stu-id="801f0-128">For Front End pools that have fewer than eight Front End Servers, calculate the metrics linearly.</span></span> <span data-ttu-id="801f0-129">例如，如果您的前端池有一个前端服务器，请将最大负载计算为表中显示的值1/8。</span><span class="sxs-lookup"><span data-stu-id="801f0-129">For example, if your Front End pool has one Front End Server, calculate the maximum load as 1/8 of the values shown in the table.</span></span></P>
> <LI>
> <P><span data-ttu-id="801f0-130">只要不超过每个池的最大用户数，您就可以增加或减少建议的组数以及每组用户数。</span><span class="sxs-lookup"><span data-stu-id="801f0-130">You can increase or decrease the recommended number of users per group and number of groups as long as you do not exceed the maximum number of users per pool.</span></span> <span data-ttu-id="801f0-131">例如，你的标准版服务器可以拥有每组25个用户的120组，因为为组呼叫挑选启用的用户数仍在用户模型中最大 (，120组数25用户3000是已启用组呼叫挑选) 的用户。</span><span class="sxs-lookup"><span data-stu-id="801f0-131">For example, your Standard Edition server can have 120 groups with 25 users per group because the number of users enabled for Group Call Pickup is still within the user model maximum (that is, 120 groups times 25 users is 3,000 users enabled for Group Call Pickup).</span></span></P></LI></UL><span data-ttu-id="801f0-132">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="801f0-132">



</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

