---
title: Lync Server 2013：MediaList 表
description: Lync Server 2013： MediaList 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaList table
ms:assetid: 1f440590-c1bc-483e-b7bc-6cc763847768
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398279(v=OCS.15)
ms:contentKeyID: 48183579
ms.date: 07/12/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e54535cd4a081657e7dcd59446cf65aaa3af7cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445923"
---
# <a name="medialist-table-in-lync-server-2013"></a><span data-ttu-id="1cadd-103">Lync Server 2013 中的 MediaList 表</span><span class="sxs-lookup"><span data-stu-id="1cadd-103">MediaList table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1cadd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1cadd-104">

<span> </span></span></span>

<span data-ttu-id="1cadd-105">_**主题上次修改时间：** 2016-07-12_</span><span class="sxs-lookup"><span data-stu-id="1cadd-105">_**Topic Last Modified:** 2016-07-12_</span></span>

<span data-ttu-id="1cadd-106">MediaList 表是一个静态表，用于存储各种媒体类型的列表。</span><span class="sxs-lookup"><span data-stu-id="1cadd-106">The MediaList table is a static table that stores the list of various media types.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1cadd-107">列</span><span class="sxs-lookup"><span data-stu-id="1cadd-107">Column</span></span></th>
<th><span data-ttu-id="1cadd-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="1cadd-108">Data Type</span></span></th>
<th><span data-ttu-id="1cadd-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="1cadd-109">Key/Index</span></span></th>
<th><span data-ttu-id="1cadd-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="1cadd-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cadd-111"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="1cadd-111"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="1cadd-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="1cadd-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1cadd-113">Primary</span><span class="sxs-lookup"><span data-stu-id="1cadd-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="1cadd-114">值：1-7</span><span class="sxs-lookup"><span data-stu-id="1cadd-114">Values: 1-7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cadd-115"><strong>媒体</strong></span><span class="sxs-lookup"><span data-stu-id="1cadd-115"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="1cadd-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1cadd-116">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1cadd-117">MediaID 与媒体值的静态映射：</span><span class="sxs-lookup"><span data-stu-id="1cadd-117">Static mapping of MediaID and Media values:</span></span></p>
<ul>
<li><p><span data-ttu-id="1cadd-118">1-IM</span><span class="sxs-lookup"><span data-stu-id="1cadd-118">1 – IM</span></span></p></li>
<li><p><span data-ttu-id="1cadd-119">2 - 文件传输</span><span class="sxs-lookup"><span data-stu-id="1cadd-119">2 – File Transfer</span></span></p></li>
<li><p><span data-ttu-id="1cadd-120">3 – 远程协助</span><span class="sxs-lookup"><span data-stu-id="1cadd-120">3 – Remote Assistance</span></span></p></li>
<li><p><span data-ttu-id="1cadd-121">4 – 应用程序共享</span><span class="sxs-lookup"><span data-stu-id="1cadd-121">4 – Application Sharing</span></span></p></li>
<li><p><span data-ttu-id="1cadd-122">5-音频</span><span class="sxs-lookup"><span data-stu-id="1cadd-122">5 – Audio</span></span></p></li>
<li><p><span data-ttu-id="1cadd-123">6-视频</span><span class="sxs-lookup"><span data-stu-id="1cadd-123">6 – Video</span></span></p></li>
<li><p><span data-ttu-id="1cadd-124">7 – 应用程序邀请</span><span class="sxs-lookup"><span data-stu-id="1cadd-124">7 – App Invite</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1cadd-125">如果你尝试确定 LcsCDR.SessionDetailsView.MediaTypes 中的值的形式类型，则需要使用以下加入代码段：</span><span class="sxs-lookup"><span data-stu-id="1cadd-125">If you are trying to determine the modality type for the values in LcsCDR.SessionDetailsView.MediaTypes, then you need to use the following Join snippet:</span></span>

    LEFT JOIN on Media.MediaId = MediaList.MediaId

<span data-ttu-id="1cadd-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1cadd-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

