---
title: Lync Server 2013：媒体视图
description: Lync Server 2013： "媒体" 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media view
ms:assetid: 1a7b2e59-082e-4188-98ae-48ae9bd3494a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687981(v=OCS.15)
ms:contentKeyID: 49733570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74643986b12a30b1055a46a37febf90eeb70c514
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446035"
---
# <a name="media-view-in-lync-server-2013"></a><span data-ttu-id="59179-103">Lync Server 2013 中的 "媒体" 视图</span><span class="sxs-lookup"><span data-stu-id="59179-103">Media view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="59179-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="59179-104">

<span> </span></span></span>

<span data-ttu-id="59179-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="59179-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="59179-106">媒体视图存储对等会话中使用的一种媒体类型的相关信息。</span><span class="sxs-lookup"><span data-stu-id="59179-106">The Media view stores information about one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="59179-107">如果使用多个媒体类型，则表中的多个记录将表示一个会话。</span><span class="sxs-lookup"><span data-stu-id="59179-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span> <span data-ttu-id="59179-108">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="59179-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="59179-109">不应使用 "媒体" 视图计算会话的媒体持续时间。</span><span class="sxs-lookup"><span data-stu-id="59179-109">The Media view should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="59179-110">此视图包含会话中媒体交换的信号详细信息。</span><span class="sxs-lookup"><span data-stu-id="59179-110">This view contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="59179-111">媒体交换由邀请请求完成，并且 StartTime 指示发送邀请的时间。邀请时间不一定意味着媒体开始时间，因为媒体仅在接受会话后才开始。</span><span class="sxs-lookup"><span data-stu-id="59179-111">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the session is accepted.</span></span>



</div>

<span data-ttu-id="59179-112">媒体视图在 [Lync Server 2013 的 SessionDetails 视图](lync-server-2013-sessiondetails-view.md) 中包含所有列，此外还包含下面列出的列。</span><span class="sxs-lookup"><span data-stu-id="59179-112">The Media view contains all of the columns in the [SessionDetails view in Lync Server 2013](lync-server-2013-sessiondetails-view.md) in addition the ones listed below.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59179-113">列</span><span class="sxs-lookup"><span data-stu-id="59179-113">Column</span></span></th>
<th><span data-ttu-id="59179-114">数据类型</span><span class="sxs-lookup"><span data-stu-id="59179-114">Data Type</span></span></th>
<th><span data-ttu-id="59179-115">详细信息</span><span class="sxs-lookup"><span data-stu-id="59179-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59179-116"><strong>媒体</strong></span><span class="sxs-lookup"><span data-stu-id="59179-116"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="59179-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="59179-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="59179-118">媒体类型。</span><span class="sxs-lookup"><span data-stu-id="59179-118">Media type.</span></span> <span data-ttu-id="59179-119">有关详细信息，请参阅 <a href="lync-server-2013-medialist-table.md">Lync Server 2013 中的 MediaList 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="59179-119">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59179-120"><strong>MediaStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="59179-120"><strong>MediaStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="59179-121">datetime</span><span class="sxs-lookup"><span data-stu-id="59179-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="59179-122">媒体请求发出的时间。</span><span class="sxs-lookup"><span data-stu-id="59179-122">Time that a media request was sent out.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59179-123"><strong>MediaEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="59179-123"><strong>MediaEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="59179-124">datetime</span><span class="sxs-lookup"><span data-stu-id="59179-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="59179-125">会话的结束时间。</span><span class="sxs-lookup"><span data-stu-id="59179-125">End time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="59179-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="59179-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

