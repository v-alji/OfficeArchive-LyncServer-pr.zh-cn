---
title: Lync Server 2013：Media 表
description: Lync Server 2013： Media 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media table
ms:assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398268(v=OCS.15)
ms:contentKeyID: 48183568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31e30d1f91c59b8e3aa7915fc0d513618d0f709f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425673"
---
# <a name="media-table-in-lync-server-2013"></a><span data-ttu-id="87d09-103">Lync Server 2013 中的 Media 表</span><span class="sxs-lookup"><span data-stu-id="87d09-103">Media table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87d09-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87d09-104">

<span> </span></span></span>

<span data-ttu-id="87d09-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="87d09-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="87d09-106">每条记录表示对等会话中使用的一种媒体类型。</span><span class="sxs-lookup"><span data-stu-id="87d09-106">Each record represents one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="87d09-107">如果使用多个媒体类型，则表中的多个记录将表示一个会话。</span><span class="sxs-lookup"><span data-stu-id="87d09-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="87d09-108">不应使用 Media 表计算会话的媒体持续时间。</span><span class="sxs-lookup"><span data-stu-id="87d09-108">The Media table should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="87d09-109">此表包含会话中媒体交换的信号详细信息。</span><span class="sxs-lookup"><span data-stu-id="87d09-109">This table contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="87d09-110">媒体交换由邀请请求完成，并且 StartTime 指示发送邀请的时间。邀请时间不一定表示媒体开始时间，因为媒体仅在 sessionee 接受会话后才开始。</span><span class="sxs-lookup"><span data-stu-id="87d09-110">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the sessionee accepts the session.</span></span> <span data-ttu-id="87d09-111">"结束时间" 通常表示本次会话的结束时间。</span><span class="sxs-lookup"><span data-stu-id="87d09-111">The EndTime usually means the end time of this session.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87d09-112">列</span><span class="sxs-lookup"><span data-stu-id="87d09-112">Column</span></span></th>
<th><span data-ttu-id="87d09-113">数据类型</span><span class="sxs-lookup"><span data-stu-id="87d09-113">Data Type</span></span></th>
<th><span data-ttu-id="87d09-114">键/索引</span><span class="sxs-lookup"><span data-stu-id="87d09-114">Key/Index</span></span></th>
<th><span data-ttu-id="87d09-115">详细信息</span><span class="sxs-lookup"><span data-stu-id="87d09-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87d09-116"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="87d09-116"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="87d09-117">datetime</span><span class="sxs-lookup"><span data-stu-id="87d09-117">datetime</span></span></p></td>
<td><p><span data-ttu-id="87d09-118">主、外部</span><span class="sxs-lookup"><span data-stu-id="87d09-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="87d09-119">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="87d09-119">Time of session request.</span></span> <span data-ttu-id="87d09-120">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="87d09-120">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="87d09-121">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="87d09-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87d09-122"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="87d09-122"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="87d09-123">int</span><span class="sxs-lookup"><span data-stu-id="87d09-123">int</span></span></p></td>
<td><p><span data-ttu-id="87d09-124">主、外部</span><span class="sxs-lookup"><span data-stu-id="87d09-124">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="87d09-125">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="87d09-125">ID number to identify the session.</span></span> <span data-ttu-id="87d09-126">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="87d09-126">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="87d09-127">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="87d09-127">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87d09-128"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="87d09-128"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="87d09-129">tinyint</span><span class="sxs-lookup"><span data-stu-id="87d09-129">tinyint</span></span></p></td>
<td><p><span data-ttu-id="87d09-130">主、外部</span><span class="sxs-lookup"><span data-stu-id="87d09-130">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="87d09-131">标识此媒体类型的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="87d09-131">Unique number identifying this media type.</span></span> <span data-ttu-id="87d09-132">有关详细信息，请参阅 <a href="lync-server-2013-medialist-table.md">Lync Server 2013 中的 MediaList 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="87d09-132">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87d09-133"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="87d09-133"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="87d09-134">datetime</span><span class="sxs-lookup"><span data-stu-id="87d09-134">datetime</span></span></p></td>
<td><p><span data-ttu-id="87d09-135">Primary</span><span class="sxs-lookup"><span data-stu-id="87d09-135">Primary</span></span></p></td>
<td><p><span data-ttu-id="87d09-136">这是发送媒体请求的时间，而不是真正的媒体开始时间。</span><span class="sxs-lookup"><span data-stu-id="87d09-136">This is the time that a media request was sent out, not the real media start time.</span></span> <span data-ttu-id="87d09-137"><strong>StartTime</strong> 包括会话设置时间。</span><span class="sxs-lookup"><span data-stu-id="87d09-137"><strong>StartTime</strong> includes the session setup time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87d09-138"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="87d09-138"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="87d09-139">datetime</span><span class="sxs-lookup"><span data-stu-id="87d09-139">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="87d09-140">这是会话的结束时间。</span><span class="sxs-lookup"><span data-stu-id="87d09-140">This is the end time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="87d09-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87d09-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

