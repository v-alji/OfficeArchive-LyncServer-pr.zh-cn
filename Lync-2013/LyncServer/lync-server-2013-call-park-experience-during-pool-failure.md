---
title: Lync Server 2013：池故障期间的呼叫寄存体验
description: Lync Server 2013：在池故障期间调用寄存体验。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park experience during pool failure
ms:assetid: f6303e69-8771-492a-9e8b-c3d7ba231309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205383(v=OCS.15)
ms:contentKeyID: 48185831
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b97a0af13d378b0753979c32b6d5ffe7a525cf0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435696"
---
# <a name="call-park-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="0f256-103">池故障期间 Lync Server 2013 中的呼叫寄存体验</span><span class="sxs-lookup"><span data-stu-id="0f256-103">Call Park experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0f256-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0f256-104">

<span> </span></span></span>

<span data-ttu-id="0f256-105">_**主题上次修改时间：** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="0f256-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="0f256-106">当前端池因计划外事件而不可用时，已暂停但尚未检索的通话将断开连接。</span><span class="sxs-lookup"><span data-stu-id="0f256-106">When a Front End pool becomes unavailable due an unplanned incident, calls that have been parked but not yet retrieved are disconnected.</span></span> <span data-ttu-id="0f256-107">在故障转移到备份池的过程中，用户将被重定向到备份池并处于复原模式。</span><span class="sxs-lookup"><span data-stu-id="0f256-107">During failover to a backup pool, users are redirected to the backup pool and are in resiliency mode.</span></span> <span data-ttu-id="0f256-108">在弹性模式下，用户不能寄存呼叫，但可以将呼叫置于保持状态，并将其转移。</span><span class="sxs-lookup"><span data-stu-id="0f256-108">While in resiliency mode, users cannot park calls, but they can place calls on hold and transfer them.</span></span> <span data-ttu-id="0f256-109">故障转移完成后，可以再次按正常方式暂停和检索呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f256-109">When failover is complete, calls can again be parked and retrieved as usual.</span></span> <span data-ttu-id="0f256-110">在故障回复期间，用户不能寄存呼叫，直到他们退出恢复模式。</span><span class="sxs-lookup"><span data-stu-id="0f256-110">During failback, users cannot park calls until they are out of resiliency mode.</span></span>

<span data-ttu-id="0f256-111">在灾难恢复期间，已作为故障转移过程的一部分被重定向到备份池的用户将使用在备份池中部署的 "呼叫驻留" 应用程序。</span><span class="sxs-lookup"><span data-stu-id="0f256-111">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park application that is deployed in the backup pool.</span></span> <span data-ttu-id="0f256-112">因此，被重定向到备份池的用户使用为备份池中的 "呼叫驻留" 应用程序配置的 "呼叫寄存" 设置。</span><span class="sxs-lookup"><span data-stu-id="0f256-112">Therefore, users who are redirected to the backup pool use the call park settings that are configured for the Call Park application in the backup pool.</span></span>

<span data-ttu-id="0f256-113">下表总结了灾难恢复阶段的通话寄存体验。</span><span class="sxs-lookup"><span data-stu-id="0f256-113">The following table summarizes the Call Park experience through the phases of disaster recovery.</span></span>

### <a name="user-experience-during-disaster-recovery"></a><span data-ttu-id="0f256-114">灾难恢复期间的用户体验</span><span class="sxs-lookup"><span data-stu-id="0f256-114">User Experience During Disaster Recovery</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f256-115">通话状态</span><span class="sxs-lookup"><span data-stu-id="0f256-115">Call state</span></span></th>
<th><span data-ttu-id="0f256-116">出现停机时</span><span class="sxs-lookup"><span data-stu-id="0f256-116">When outage occurs</span></span></th>
<th><span data-ttu-id="0f256-117">故障转移期间</span><span class="sxs-lookup"><span data-stu-id="0f256-117">During failover</span></span></th>
<th><span data-ttu-id="0f256-118">故障回复期间</span><span class="sxs-lookup"><span data-stu-id="0f256-118">During failback</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f256-119">通话尚未停用</span><span class="sxs-lookup"><span data-stu-id="0f256-119">Call not yet parked</span></span></p></td>
<td><p><span data-ttu-id="0f256-120">通话保持连接，但无法停用。</span><span class="sxs-lookup"><span data-stu-id="0f256-120">Call remains connected, but cannot be parked.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="0f256-121">在故障转移期间，当用户处于复原模式时，无法停止呼叫，但可以将呼叫置于保持状态并进行转移。</span><span class="sxs-lookup"><span data-stu-id="0f256-121">During failover, call cannot be parked while users are in resiliency mode, but can be put on hold and transferred.</span></span></p></li>
<li><p><span data-ttu-id="0f256-122">故障转移完成后，可以停用和检索呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f256-122">When failover completes, call can be parked and retrieved.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="0f256-123">在故障回复期间，当用户处于复原模式时，无法停止呼叫，但可以将呼叫置于保持状态并进行转移。</span><span class="sxs-lookup"><span data-stu-id="0f256-123">During failback, call cannot be parked while users are in resiliency mode, but can be put on hold and transferred.</span></span></p></li>
<li><p><span data-ttu-id="0f256-124">当故障回复完成时，可以停用和检索呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f256-124">When failback completes, call can be parked and retrieved.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f256-125">呼叫已暂停，但尚未检索</span><span class="sxs-lookup"><span data-stu-id="0f256-125">Call parked, but not yet retrieved</span></span></p></td>
<td><p><span data-ttu-id="0f256-126">通话断开。</span><span class="sxs-lookup"><span data-stu-id="0f256-126">Call is disconnected.</span></span></p></td>
<td><p><span data-ttu-id="0f256-127">通话处于此状态。</span><span class="sxs-lookup"><span data-stu-id="0f256-127">No calls in this state.</span></span></p></td>
<td><p><span data-ttu-id="0f256-128">通话保持停用。</span><span class="sxs-lookup"><span data-stu-id="0f256-128">Call remains parked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f256-129">已检索寄存通话</span><span class="sxs-lookup"><span data-stu-id="0f256-129">Parked call already retrieved</span></span></p></td>
<td><p><span data-ttu-id="0f256-130">通话保持连接。</span><span class="sxs-lookup"><span data-stu-id="0f256-130">Call remains connected.</span></span></p></td>
<td><p><span data-ttu-id="0f256-131">通话保持连接。</span><span class="sxs-lookup"><span data-stu-id="0f256-131">Call remains connected.</span></span></p></td>
<td><p><span data-ttu-id="0f256-132">通话保持连接。</span><span class="sxs-lookup"><span data-stu-id="0f256-132">Call remains connected.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0f256-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0f256-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

