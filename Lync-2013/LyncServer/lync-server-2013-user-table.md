---
title: Lync Server 2013：User 表
description: Lync Server 2013：用户表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444166"
---
# <a name="user-table-in-lync-server-2013"></a><span data-ttu-id="58b59-103">Lync Server 2013 中的 User 表</span><span class="sxs-lookup"><span data-stu-id="58b59-103">User table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58b59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58b59-104">

<span> </span></span></span>

<span data-ttu-id="58b59-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="58b59-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="58b59-106">用户表是一个支持表，用于存储参与数据库中记录的会话的各种用户的列表。</span><span class="sxs-lookup"><span data-stu-id="58b59-106">The User table is a supporting table that stores a list of the various users who have participated in sessions recorded in the database.</span></span> <span data-ttu-id="58b59-107">表中的每条记录表示一个用户。</span><span class="sxs-lookup"><span data-stu-id="58b59-107">Each record in the table represents one user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58b59-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="58b59-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="58b59-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="58b59-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58b59-112"><strong>UserKey</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-112"><strong>UserKey</strong></span></span></p></td>
<td><p><span data-ttu-id="58b59-113">int</span><span class="sxs-lookup"><span data-stu-id="58b59-113">int</span></span></p></td>
<td><p><span data-ttu-id="58b59-114">Primary</span><span class="sxs-lookup"><span data-stu-id="58b59-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="58b59-115">标识此用户的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="58b59-115">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58b59-116"><strong>URI</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-116"><strong>URI</strong></span></span></p></td>
<td><p><span data-ttu-id="58b59-117">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="58b59-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="58b59-118">唯一</span><span class="sxs-lookup"><span data-stu-id="58b59-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="58b59-119">URI 字符串。</span><span class="sxs-lookup"><span data-stu-id="58b59-119">URI string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58b59-120"><strong>URIType</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-120"><strong>URIType</strong></span></span></p></td>
<td><p><span data-ttu-id="58b59-121">int</span><span class="sxs-lookup"><span data-stu-id="58b59-121">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="58b59-122">1是未知的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="58b59-122">1 is unknown URI type.</span></span></p>
<p><span data-ttu-id="58b59-123">2是用户 URI。</span><span class="sxs-lookup"><span data-stu-id="58b59-123">2 is user URI.</span></span></p>
<p><span data-ttu-id="58b59-124">4是会议 URI。</span><span class="sxs-lookup"><span data-stu-id="58b59-124">4 is conference URI.</span></span></p>
<p><span data-ttu-id="58b59-125">8是电话 URI。</span><span class="sxs-lookup"><span data-stu-id="58b59-125">8 is phone URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58b59-126"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-126"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="58b59-127">int</span><span class="sxs-lookup"><span data-stu-id="58b59-127">int</span></span></p></td>
<td><p><span data-ttu-id="58b59-128">外表</span><span class="sxs-lookup"><span data-stu-id="58b59-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="58b59-129">用户的租户，从租户表引用。</span><span class="sxs-lookup"><span data-stu-id="58b59-129">Tenant of the user, referenced from tenant table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58b59-130"><strong>LastPoorCallTime</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-130"><strong>LastPoorCallTime</strong></span></span></p></td>
<td><p><span data-ttu-id="58b59-131">datetime</span><span class="sxs-lookup"><span data-stu-id="58b59-131">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="58b59-132">当用户的音频通话较差时的最晚时间戳。</span><span class="sxs-lookup"><span data-stu-id="58b59-132">Latest time stamp when the user had a poor audio call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58b59-133"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="58b59-133"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="58b59-134">datetime</span><span class="sxs-lookup"><span data-stu-id="58b59-134">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="58b59-135">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="58b59-135">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="58b59-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58b59-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

