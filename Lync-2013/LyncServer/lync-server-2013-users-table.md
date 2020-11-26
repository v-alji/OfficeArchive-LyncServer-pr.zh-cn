---
title: Lync Server 2013：Users 表
description: Lync Server 2013： Users 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436179"
---
# <a name="users-table-in-lync-server-2013"></a><span data-ttu-id="74b0f-103">Lync Server 2013 中的 Users 表</span><span class="sxs-lookup"><span data-stu-id="74b0f-103">Users table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74b0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74b0f-104">

<span> </span></span></span>

<span data-ttu-id="74b0f-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="74b0f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="74b0f-106">"用户" 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="74b0f-106">The Users table is a supporting table.</span></span> <span data-ttu-id="74b0f-107">表中的每条记录存储有关在数据库中具有记录的通话或会话中涉及的一个用户的信息。</span><span class="sxs-lookup"><span data-stu-id="74b0f-107">Each record in the table stores information about one user involved in calls or sessions that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74b0f-108">列</span><span class="sxs-lookup"><span data-stu-id="74b0f-108">Column</span></span></th>
<th><span data-ttu-id="74b0f-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="74b0f-109">Data Type</span></span></th>
<th><span data-ttu-id="74b0f-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="74b0f-110">Key/Index</span></span></th>
<th><span data-ttu-id="74b0f-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="74b0f-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74b0f-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="74b0f-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="74b0f-113">datetime</span><span class="sxs-lookup"><span data-stu-id="74b0f-113">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="74b0f-114">供内部使用的时间戳。</span><span class="sxs-lookup"><span data-stu-id="74b0f-114">Time stamp for internal use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74b0f-115"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="74b0f-115"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="74b0f-116">int</span><span class="sxs-lookup"><span data-stu-id="74b0f-116">int</span></span></p></td>
<td><p><span data-ttu-id="74b0f-117">Primary</span><span class="sxs-lookup"><span data-stu-id="74b0f-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="74b0f-118">标识此用户的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="74b0f-118">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74b0f-119"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="74b0f-119"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="74b0f-120">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="74b0f-120">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="74b0f-121">用户 URI。</span><span class="sxs-lookup"><span data-stu-id="74b0f-121">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74b0f-122"><strong>TenantId</strong></span><span class="sxs-lookup"><span data-stu-id="74b0f-122"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="74b0f-123">int</span><span class="sxs-lookup"><span data-stu-id="74b0f-123">int</span></span></p></td>
<td><p><span data-ttu-id="74b0f-124">外表</span><span class="sxs-lookup"><span data-stu-id="74b0f-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="74b0f-125">此用户的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="74b0f-125">This user’s Tenant ID.</span></span> <span data-ttu-id="74b0f-126">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="74b0f-126">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74b0f-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="74b0f-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="74b0f-128">int</span><span class="sxs-lookup"><span data-stu-id="74b0f-128">int</span></span></p></td>
<td><p><span data-ttu-id="74b0f-129">外表</span><span class="sxs-lookup"><span data-stu-id="74b0f-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="74b0f-130">此用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="74b0f-130">This user’s URI type.</span></span> <span data-ttu-id="74b0f-131">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="74b0f-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="74b0f-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74b0f-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

