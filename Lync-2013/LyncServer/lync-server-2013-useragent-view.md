---
title: Lync Server 2013： UserAgent 视图
description: Lync Server 2013： UserAgent 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent view
ms:assetid: b986f76f-f16e-4e5e-96cb-6e8f7f9b42ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721862(v=OCS.15)
ms:contentKeyID: 49733795
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc5ef2ec01b50f3714dca3690d0844286baaef5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439049"
---
# <a name="useragent-view-in-lync-server-2013"></a><span data-ttu-id="4d6fa-103">Lync Server 2013 中的 UserAgent 视图</span><span class="sxs-lookup"><span data-stu-id="4d6fa-103">UserAgent view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d6fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d6fa-104">

<span> </span></span></span>

<span data-ttu-id="4d6fa-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="4d6fa-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="4d6fa-106">UserAgent 视图存储有关在数据库中具有记录的会话中涉及的用户代理的信息。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-106">The UserAgent View stores information about the user agents that have been involved in sessions that have records in the database.</span></span> <span data-ttu-id="4d6fa-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d6fa-108">列</span><span class="sxs-lookup"><span data-stu-id="4d6fa-108">Column</span></span></th>
<th><span data-ttu-id="4d6fa-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="4d6fa-109">Data Type</span></span></th>
<th><span data-ttu-id="4d6fa-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="4d6fa-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d6fa-111">UserAgentKey</span><span class="sxs-lookup"><span data-stu-id="4d6fa-111">UserAgentKey</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-112">int</span><span class="sxs-lookup"><span data-stu-id="4d6fa-112">int</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-113">标识此用户代理的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-113">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d6fa-114">UserAgent</span><span class="sxs-lookup"><span data-stu-id="4d6fa-114">UserAgent</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="4d6fa-115">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-116">用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-116">User agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d6fa-117">UAType</span><span class="sxs-lookup"><span data-stu-id="4d6fa-117">UAType</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-118">smallint</span><span class="sxs-lookup"><span data-stu-id="4d6fa-118">smallint</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-119">用户代理的类型。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-119">Type of user agent.</span></span> <span data-ttu-id="4d6fa-120">有关详细信息，请参阅 <a href="lync-server-2013-useragent-table.md">Lync Server 2013 中的 UserAgent 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-120">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d6fa-121">UACategory</span><span class="sxs-lookup"><span data-stu-id="4d6fa-121">UACategory</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-122">nvarchar (64) </span><span class="sxs-lookup"><span data-stu-id="4d6fa-122">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="4d6fa-123">用户代理所属的类别。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-123">Category that the user agent belongs to.</span></span> <span data-ttu-id="4d6fa-124">例如，Conferencing_Attendant_1 .0 的用户代理属于 UACategory CAA。</span><span class="sxs-lookup"><span data-stu-id="4d6fa-124">For example, the user agent Conferencing_Attendant_1.0 belongs to the UACategory CAA.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4d6fa-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d6fa-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

