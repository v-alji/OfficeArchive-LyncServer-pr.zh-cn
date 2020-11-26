---
title: Lync Server 2013 可伸缩性
description: Lync Server 2013 可伸缩性。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability
ms:assetid: 46fa0cb5-1507-4a12-ad3f-ba64585e2dc4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417160(v=OCS.15)
ms:contentKeyID: 48183995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28cd5820755ffd1eb863ed6f2369b5756a7ae3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442115"
---
# <a name="scalability-with-lync-server-2013"></a><span data-ttu-id="b8443-103">Lync Server 2013 可伸缩性</span><span class="sxs-lookup"><span data-stu-id="b8443-103">Scalability with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8443-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8443-104">

<span> </span></span></span>

<span data-ttu-id="b8443-105">_**主题上次修改时间：** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="b8443-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="b8443-106">Lync Server 在两个版本的企业版和标准版中提供。</span><span class="sxs-lookup"><span data-stu-id="b8443-106">Lync Server is offered in two editions, Enterprise Edition and Standard Edition.</span></span> <span data-ttu-id="b8443-107">不同版本主要适用于不同规模的组织。</span><span class="sxs-lookup"><span data-stu-id="b8443-107">The different editions are intended primarily for different sizes of organizations.</span></span> <span data-ttu-id="b8443-108">如下表所示，这两个版本都支持除高可用性和灾难恢复之外的所有工作负荷中的所有功能。</span><span class="sxs-lookup"><span data-stu-id="b8443-108">As shown in the following table, both editions support all functionality in all workloads, except for high availability and disaster recovery.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8443-109">功能</span><span class="sxs-lookup"><span data-stu-id="b8443-109">Feature</span></span></th>
<th><span data-ttu-id="b8443-110">在企业版中受支持？</span><span class="sxs-lookup"><span data-stu-id="b8443-110">Supported in Enterprise Edition?</span></span></th>
<th><span data-ttu-id="b8443-111">在标准版中受支持？</span><span class="sxs-lookup"><span data-stu-id="b8443-111">Supported in Standard Edition?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8443-112">即时消息 (IM) 和状态</span><span class="sxs-lookup"><span data-stu-id="b8443-112">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="b8443-113">是</span><span class="sxs-lookup"><span data-stu-id="b8443-113">Yes</span></span></p></td>
<td><p><span data-ttu-id="b8443-114">是</span><span class="sxs-lookup"><span data-stu-id="b8443-114">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8443-115">网络会议</span><span class="sxs-lookup"><span data-stu-id="b8443-115">Conferencing</span></span></p></td>
<td><p><span data-ttu-id="b8443-116">是</span><span class="sxs-lookup"><span data-stu-id="b8443-116">Yes</span></span></p></td>
<td><p><span data-ttu-id="b8443-117">是</span><span class="sxs-lookup"><span data-stu-id="b8443-117">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8443-118">A/V 会议</span><span class="sxs-lookup"><span data-stu-id="b8443-118">A/V conferencing</span></span></p></td>
<td><p><span data-ttu-id="b8443-119">是</span><span class="sxs-lookup"><span data-stu-id="b8443-119">Yes</span></span></p></td>
<td><p><span data-ttu-id="b8443-120">是</span><span class="sxs-lookup"><span data-stu-id="b8443-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8443-121">电话拨入式会议</span><span class="sxs-lookup"><span data-stu-id="b8443-121">Dial-in conferencing</span></span></p></td>
<td><p><span data-ttu-id="b8443-122">是</span><span class="sxs-lookup"><span data-stu-id="b8443-122">Yes</span></span></p></td>
<td><p><span data-ttu-id="b8443-123">是</span><span class="sxs-lookup"><span data-stu-id="b8443-123">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8443-124">企业语音</span><span class="sxs-lookup"><span data-stu-id="b8443-124">Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="b8443-125">是</span><span class="sxs-lookup"><span data-stu-id="b8443-125">Yes</span></span></p></td>
<td><p><span data-ttu-id="b8443-126">是</span><span class="sxs-lookup"><span data-stu-id="b8443-126">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8443-127">Virtualization</span><span class="sxs-lookup"><span data-stu-id="b8443-127">Virtualization</span></span></p></td>
<td><p><span data-ttu-id="b8443-128">是</span><span class="sxs-lookup"><span data-stu-id="b8443-128">Yes</span></span></p></td>
<td><p><span data-ttu-id="b8443-129">是</span><span class="sxs-lookup"><span data-stu-id="b8443-129">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8443-130">高可用性、故障切换和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="b8443-130">High availability, failover, and disaster recovery</span></span></p></td>
<td><p><span data-ttu-id="b8443-131">是</span><span class="sxs-lookup"><span data-stu-id="b8443-131">Yes</span></span></p></td>
<td><p><span data-ttu-id="b8443-132">否</span><span class="sxs-lookup"><span data-stu-id="b8443-132">No</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b8443-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8443-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

