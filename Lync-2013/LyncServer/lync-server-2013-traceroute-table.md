---
title: Lync Server 2013： TraceRoute 表
description: Lync Server 2013： TraceRoute 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440834"
---
# <a name="traceroute-table-in-lync-server-2013"></a><span data-ttu-id="3cfc9-103">Lync Server 2013 中的 TraceRoute 表</span><span class="sxs-lookup"><span data-stu-id="3cfc9-103">TraceRoute table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3cfc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3cfc9-104">

<span> </span></span></span>

<span data-ttu-id="3cfc9-105">_**主题上次修改时间：** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="3cfc9-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="3cfc9-106">TraceRoute 表包含来自呼叫的路由信息。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-106">The TraceRoute table contains routing information from calls.</span></span> <span data-ttu-id="3cfc9-107">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cfc9-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="3cfc9-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="3cfc9-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="3cfc9-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cfc9-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3cfc9-113">datetime</span><span class="sxs-lookup"><span data-stu-id="3cfc9-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-114">主、外部</span><span class="sxs-lookup"><span data-stu-id="3cfc9-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-115">通话开始的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-115">Date and time that the call began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cfc9-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="3cfc9-117">int</span><span class="sxs-lookup"><span data-stu-id="3cfc9-117">int</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-118">主、外部</span><span class="sxs-lookup"><span data-stu-id="3cfc9-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-119">用于区分可能在同一日期和同一时间开始的多个通话的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-119">Unique identifier used to distinguish between multiple calls that might have begun on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cfc9-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="3cfc9-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="3cfc9-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-122">主、外部</span><span class="sxs-lookup"><span data-stu-id="3cfc9-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-123">表示通话中使用的视频线路类型。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="3cfc9-124">允许的值包括：</span><span class="sxs-lookup"><span data-stu-id="3cfc9-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3cfc9-125">0-音频</span><span class="sxs-lookup"><span data-stu-id="3cfc9-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="3cfc9-126">1-视频</span><span class="sxs-lookup"><span data-stu-id="3cfc9-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="3cfc9-127">2-全景视频</span><span class="sxs-lookup"><span data-stu-id="3cfc9-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="3cfc9-128">3-应用程序/桌面共享</span><span class="sxs-lookup"><span data-stu-id="3cfc9-128">3 – Application/Desktop sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cfc9-129"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-129"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="3cfc9-130">bit</span><span class="sxs-lookup"><span data-stu-id="3cfc9-130">bit</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-131">Primary</span><span class="sxs-lookup"><span data-stu-id="3cfc9-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-132">发出呼叫的终结点。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-132">Endpoint that placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cfc9-133"><strong>跳</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-133"><strong>Hop</strong></span></span></p></td>
<td><p><span data-ttu-id="3cfc9-134">int</span><span class="sxs-lookup"><span data-stu-id="3cfc9-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3cfc9-135">网络跃点/</span><span class="sxs-lookup"><span data-stu-id="3cfc9-135">Network hop/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cfc9-136"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-136"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="3cfc9-137">int</span><span class="sxs-lookup"><span data-stu-id="3cfc9-137">int</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-138">外表</span><span class="sxs-lookup"><span data-stu-id="3cfc9-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3cfc9-139">IP 地址的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-139">Unique identifier for the IP address.</span></span> <span data-ttu-id="3cfc9-140">IP 地址信息存储在 <a href="lync-server-2013-ipaddress-table.md">Lync Server 2013 的 "IPAddress" 表中</a>。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-140">IP address information is stored in the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cfc9-141"><strong>RTT</strong></span><span class="sxs-lookup"><span data-stu-id="3cfc9-141"><strong>RTT</strong></span></span></p></td>
<td><p><span data-ttu-id="3cfc9-142">int</span><span class="sxs-lookup"><span data-stu-id="3cfc9-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3cfc9-143">往返时间。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-143">Roundtrip time.</span></span> <span data-ttu-id="3cfc9-144">往返时间测量语音数据包到达其目标所需的时间量，然后发送发送回收到通知的时间。</span><span class="sxs-lookup"><span data-stu-id="3cfc9-144">The roundtrip time measures the amount of time it takes for a voice packet to reach its destination and then send back notification that it was received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3cfc9-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3cfc9-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

