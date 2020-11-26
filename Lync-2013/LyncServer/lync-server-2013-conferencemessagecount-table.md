---
title: Lync Server 2013：ConferenceMessageCount 表
description: Lync Server 2013： ConferenceMessageCount 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount table
ms:assetid: 78569dbf-5217-42fa-ba1a-4380f56e2a3d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398590(v=OCS.15)
ms:contentKeyID: 48184570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 271b654c09ab1aef194eb613e660de208aea1534
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434450"
---
# <a name="conferencemessagecount-table-in-lync-server-2013"></a><span data-ttu-id="e9caa-103">Lync Server 2013 中的 ConferenceMessageCount 表</span><span class="sxs-lookup"><span data-stu-id="e9caa-103">ConferenceMessageCount table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9caa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9caa-104">

<span> </span></span></span>

<span data-ttu-id="e9caa-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e9caa-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e9caa-106">此表中的每条记录表示一个 IM 会议中的一个用户，包括该用户发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="e9caa-106">Each record in this table represents one user in one IM conference and includes the number of messages sent by that user.</span></span> <span data-ttu-id="e9caa-107">每个会议都由该表中的多条记录表示;每个用户一条记录。</span><span class="sxs-lookup"><span data-stu-id="e9caa-107">Each conference is represented by multiple records in this table; one record for each user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9caa-108">列</span><span class="sxs-lookup"><span data-stu-id="e9caa-108">Column</span></span></th>
<th><span data-ttu-id="e9caa-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="e9caa-109">Data Type</span></span></th>
<th><span data-ttu-id="e9caa-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="e9caa-110">Key/Index</span></span></th>
<th><span data-ttu-id="e9caa-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="e9caa-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9caa-112"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="e9caa-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e9caa-113">datetime</span><span class="sxs-lookup"><span data-stu-id="e9caa-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="e9caa-114">主、外部</span><span class="sxs-lookup"><span data-stu-id="e9caa-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e9caa-115">会议实例的时间。</span><span class="sxs-lookup"><span data-stu-id="e9caa-115">Time of conference instance.</span></span> <span data-ttu-id="e9caa-116">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="e9caa-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="e9caa-117">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="e9caa-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9caa-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e9caa-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e9caa-119">int</span><span class="sxs-lookup"><span data-stu-id="e9caa-119">int</span></span></p></td>
<td><p><span data-ttu-id="e9caa-120">主、外部</span><span class="sxs-lookup"><span data-stu-id="e9caa-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e9caa-121">标识会议实例的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="e9caa-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="e9caa-122">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会议实例。</span><span class="sxs-lookup"><span data-stu-id="e9caa-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="e9caa-123">有关详细信息，请参阅 <a href="lync-server-2013-conferences-table.md">Lync Server 2013 中</a> 的 "会议" 表。</span><span class="sxs-lookup"><span data-stu-id="e9caa-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9caa-124"><strong>UserId</strong></span><span class="sxs-lookup"><span data-stu-id="e9caa-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="e9caa-125">int</span><span class="sxs-lookup"><span data-stu-id="e9caa-125">int</span></span></p></td>
<td><p><span data-ttu-id="e9caa-126">外表</span><span class="sxs-lookup"><span data-stu-id="e9caa-126">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e9caa-127">标识此用户的唯一号码，从 <a href="lync-server-2013-users-table.md">Lync Server 2013 的 "用户" 表中</a>引用。</span><span class="sxs-lookup"><span data-stu-id="e9caa-127">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9caa-128"><strong>MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="e9caa-128"><strong>MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="e9caa-129">smallint</span><span class="sxs-lookup"><span data-stu-id="e9caa-129">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e9caa-130">此用户在此会议期间发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="e9caa-130">The number of messages sent by this user during this conference.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e9caa-131">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9caa-131">


</div>

<span> </span>

</div>

</div>

</span></span></div>

