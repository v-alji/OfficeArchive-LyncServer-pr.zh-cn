---
title: Lync Server 2013： UserStatistics 表
description: Lync Server 2013： UserStatistics 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserStatistics table
ms:assetid: cfaf803b-1679-4169-92d3-533fad3e56ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721893(v=OCS.15)
ms:contentKeyID: 49733827
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75b34fa3c34af4cc9cf2cacc6ae7feb4d217114c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436095"
---
# <a name="userstatistics-table-in-lync-server-2013"></a><span data-ttu-id="874cf-103">Lync Server 2013 中的 UserStatistics 表</span><span class="sxs-lookup"><span data-stu-id="874cf-103">UserStatistics table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="874cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="874cf-104">

<span> </span></span></span>

<span data-ttu-id="874cf-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="874cf-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="874cf-106">UserStatistics 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="874cf-106">The UserStatistics table is a supporting table.</span></span> <span data-ttu-id="874cf-107">表中的每条记录存储有关系统的单个用户使用情况的信息。</span><span class="sxs-lookup"><span data-stu-id="874cf-107">Each record in the table stores information about an individual user’s usage of the system.</span></span> <span data-ttu-id="874cf-108">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="874cf-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="874cf-109">列</span><span class="sxs-lookup"><span data-stu-id="874cf-109">Column</span></span></th>
<th><span data-ttu-id="874cf-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="874cf-110">Data Type</span></span></th>
<th><span data-ttu-id="874cf-111">键/索引</span><span class="sxs-lookup"><span data-stu-id="874cf-111">Key/Index</span></span></th>
<th><span data-ttu-id="874cf-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="874cf-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="874cf-113"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="874cf-113"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="874cf-114">int</span><span class="sxs-lookup"><span data-stu-id="874cf-114">int</span></span></p></td>
<td><p><span data-ttu-id="874cf-115">Primary</span><span class="sxs-lookup"><span data-stu-id="874cf-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="874cf-116">标识此用户的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="874cf-116">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="874cf-117"><strong>LastLogInTime</strong></span><span class="sxs-lookup"><span data-stu-id="874cf-117"><strong>LastLogInTime</strong></span></span></p></td>
<td><p><span data-ttu-id="874cf-118">datetime</span><span class="sxs-lookup"><span data-stu-id="874cf-118">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="874cf-119">上次登录用户的时间。</span><span class="sxs-lookup"><span data-stu-id="874cf-119">Last time the user logged in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="874cf-120"><strong>LastConfOrganizedTime</strong></span><span class="sxs-lookup"><span data-stu-id="874cf-120"><strong>LastConfOrganizedTime</strong></span></span></p></td>
<td><p><span data-ttu-id="874cf-121">datetime</span><span class="sxs-lookup"><span data-stu-id="874cf-121">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="874cf-122">上次用户组织会议的时间。</span><span class="sxs-lookup"><span data-stu-id="874cf-122">Last time the user organized a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="874cf-123"><strong>LastCallOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="874cf-123"><strong>LastCallOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="874cf-124">datetime</span><span class="sxs-lookup"><span data-stu-id="874cf-124">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="874cf-125">上次用户遇到通话失败的时间。</span><span class="sxs-lookup"><span data-stu-id="874cf-125">Last time the user experienced a call failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="874cf-126"><strong>LastConfOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="874cf-126"><strong>LastConfOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="874cf-127">datetime</span><span class="sxs-lookup"><span data-stu-id="874cf-127">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="874cf-128">上次用户遇到作为会议组织者的呼叫失败的时间。</span><span class="sxs-lookup"><span data-stu-id="874cf-128">Last time the user experienced a call failure as a conference organizer.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="874cf-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="874cf-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

