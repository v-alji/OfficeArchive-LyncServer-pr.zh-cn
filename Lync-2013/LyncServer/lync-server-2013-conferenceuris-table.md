---
title: Lync Server 2013：ConferenceUris 表
description: Lync Server 2013： ConferenceUris 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceUris table
ms:assetid: b1721d52-3c65-45ea-8997-06af8fef93fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412854(v=OCS.15)
ms:contentKeyID: 48185160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a142aa9ad1fe4d3ae92aa3e21aa9eee505457cbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434387"
---
# <a name="conferenceuris-table-in-lync-server-2013"></a><span data-ttu-id="10a1b-103">Lync Server 2013 中的 ConferenceUris 表</span><span class="sxs-lookup"><span data-stu-id="10a1b-103">ConferenceUris table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10a1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10a1b-104">

<span> </span></span></span>

<span data-ttu-id="10a1b-105">_**主题上次修改时间：** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="10a1b-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="10a1b-106">ConfereneUris 表是一个支持表，用于存储参与数据库中记录的会议会话的各种会议 Uri 的列表。</span><span class="sxs-lookup"><span data-stu-id="10a1b-106">The ConfereneUris table is a supporting table that stores a list of the various conference URIs that have participated in conference sessions recorded in the database.</span></span> <span data-ttu-id="10a1b-107">表中的每条记录表示一个会议 URI。</span><span class="sxs-lookup"><span data-stu-id="10a1b-107">Each record in the table represents one conference URI.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10a1b-108">列</span><span class="sxs-lookup"><span data-stu-id="10a1b-108">Column</span></span></th>
<th><span data-ttu-id="10a1b-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="10a1b-109">Data Type</span></span></th>
<th><span data-ttu-id="10a1b-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="10a1b-110">Key/Index</span></span></th>
<th><span data-ttu-id="10a1b-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="10a1b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10a1b-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="10a1b-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="10a1b-113">datetime</span><span class="sxs-lookup"><span data-stu-id="10a1b-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="10a1b-114">Primary</span><span class="sxs-lookup"><span data-stu-id="10a1b-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="10a1b-115">时间戳，内部使用。</span><span class="sxs-lookup"><span data-stu-id="10a1b-115">Time stamp, Internal used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a1b-116"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="10a1b-116"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="10a1b-117">int</span><span class="sxs-lookup"><span data-stu-id="10a1b-117">int</span></span></p></td>
<td><p><span data-ttu-id="10a1b-118">Primary</span><span class="sxs-lookup"><span data-stu-id="10a1b-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="10a1b-119">标识此会议 URI 的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="10a1b-119">Unique number identifying this conference URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a1b-120"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="10a1b-120"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="10a1b-121">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="10a1b-121">nvarchar(450)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="10a1b-122">会议 URI。</span><span class="sxs-lookup"><span data-stu-id="10a1b-122">Conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a1b-123"><strong>检查</strong></span><span class="sxs-lookup"><span data-stu-id="10a1b-123"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="10a1b-124">int</span><span class="sxs-lookup"><span data-stu-id="10a1b-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="10a1b-125">ConferenceUri 的校验和。</span><span class="sxs-lookup"><span data-stu-id="10a1b-125">Checksum of ConferenceUri.</span></span> <span data-ttu-id="10a1b-126">用于提高数据库搜索的速度。</span><span class="sxs-lookup"><span data-stu-id="10a1b-126">Used to increases the speed of database searches.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a1b-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="10a1b-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="10a1b-128">int</span><span class="sxs-lookup"><span data-stu-id="10a1b-128">int</span></span></p></td>
<td><p><span data-ttu-id="10a1b-129">外表</span><span class="sxs-lookup"><span data-stu-id="10a1b-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="10a1b-130">URI 类型，例如会议：用于即时消息会议的聊天或会议：音频-音频/视频会议的视频。</span><span class="sxs-lookup"><span data-stu-id="10a1b-130">URI type, such as conf:chat for IM conference, or conf:audio-video for audio/video conference.</span></span> <span data-ttu-id="10a1b-131">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 表中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="10a1b-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> table for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="10a1b-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10a1b-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

