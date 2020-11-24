---
title: Lync Server 2013：VideoClientEvent 表
description: Lync Server 2013： VideoClientEvent 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoClientEvent table
ms:assetid: e8ab963b-fe1d-45b3-b9bd-66a5f44c1629
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399039(v=OCS.15)
ms:contentKeyID: 48185891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae73ac2548e838241febe60a2d31f80983b01de5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392434"
---
# <a name="videoclientevent-table-in-lync-server-2013"></a><span data-ttu-id="a0ad7-103">Lync Server 2013 中的 VideoClientEvent 表</span><span class="sxs-lookup"><span data-stu-id="a0ad7-103">VideoClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0ad7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0ad7-104">

<span> </span></span></span>

<span data-ttu-id="a0ad7-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="a0ad7-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="a0ad7-106">每条记录包含视频呼叫中一个终结点的客户端事件。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-106">Each record contains client event for one endpoint in a video call.</span></span> <span data-ttu-id="a0ad7-107">通常，一个通话有两个记录，一个用于呼叫方，另一个用于被呼叫方。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0ad7-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="a0ad7-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="a0ad7-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="a0ad7-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0ad7-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a0ad7-113">datetime</span><span class="sxs-lookup"><span data-stu-id="a0ad7-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-114">Primary</span><span class="sxs-lookup"><span data-stu-id="a0ad7-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-115">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ad7-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="a0ad7-117">int</span><span class="sxs-lookup"><span data-stu-id="a0ad7-117">int</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-118">Primary</span><span class="sxs-lookup"><span data-stu-id="a0ad7-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-119">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ad7-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="a0ad7-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="a0ad7-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-122">Primary</span><span class="sxs-lookup"><span data-stu-id="a0ad7-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-123">从 <a href="lync-server-2013-medialine-table.md">Lync Server 2013 中的 MediaLine 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ad7-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="a0ad7-125">bit</span><span class="sxs-lookup"><span data-stu-id="a0ad7-125">bit</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-126">Primary</span><span class="sxs-lookup"><span data-stu-id="a0ad7-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="a0ad7-127">0：被调用方的数据</span><span class="sxs-lookup"><span data-stu-id="a0ad7-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="a0ad7-128">1：调用方的数据</span><span class="sxs-lookup"><span data-stu-id="a0ad7-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0ad7-129"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-129"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a0ad7-130">会话百分比为 "坏" 状态引发 LowBandwidth 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-130">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="a0ad7-131">可用带宽不足以获得可接受的语音体验。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-131">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0ad7-132"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="a0ad7-132"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="a0ad7-133">会话百分比为 "坏" 状态引发 ReceiveSendQuality 事件的百分比。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-133">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="a0ad7-134">"抖动" 或 "数据包丢失" 方面的网络质量非常严重，影响接收音频的质量。</span><span class="sxs-lookup"><span data-stu-id="a0ad7-134">Network quality in terms of jitter or packet loss is severe and impacts the quality of audio being received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a0ad7-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0ad7-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

