---
title: Lync Server 2013：用户视图
description: Lync Server 2013：用户视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User view
ms:assetid: 796f77e6-1da6-4969-b18b-3537209a1fe4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688100(v=OCS.15)
ms:contentKeyID: 49733699
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa606887e8050a51f1e5a87656bb74a7cd58bbc3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439156"
---
# <a name="user-view-in-lync-server-2013"></a><span data-ttu-id="a7ab4-103">Lync Server 2013 中的用户视图</span><span class="sxs-lookup"><span data-stu-id="a7ab4-103">User view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7ab4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7ab4-104">

<span> </span></span></span>

<span data-ttu-id="a7ab4-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a7ab4-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a7ab4-106">"用户" 视图存储与在数据库中具有记录的通话或会话中参与的用户的相关信息。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-106">The User view stores information about users who have been involved in calls or sessions that have records in the database.</span></span> <span data-ttu-id="a7ab4-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7ab4-108">列</span><span class="sxs-lookup"><span data-stu-id="a7ab4-108">Column</span></span></th>
<th><span data-ttu-id="a7ab4-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="a7ab4-109">Data Type</span></span></th>
<th><span data-ttu-id="a7ab4-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="a7ab4-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7ab4-111">UserId</span><span class="sxs-lookup"><span data-stu-id="a7ab4-111">UserId</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-112">int</span><span class="sxs-lookup"><span data-stu-id="a7ab4-112">int</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-113">标识此用户的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-113">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ab4-114">UserUri</span><span class="sxs-lookup"><span data-stu-id="a7ab4-114">UserUri</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-115">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="a7ab4-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-116">用户的 Uri。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-116">Uri of the user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7ab4-117">TenantKey</span><span class="sxs-lookup"><span data-stu-id="a7ab4-117">TenantKey</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-118">标识符</span><span class="sxs-lookup"><span data-stu-id="a7ab4-118">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-119">用户的租户。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-119">Tenant of user.</span></span> <span data-ttu-id="a7ab4-120">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-120">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7ab4-121">UriType</span><span class="sxs-lookup"><span data-stu-id="a7ab4-121">UriType</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a7ab4-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a7ab4-123">用户 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-123">Type of user URI.</span></span> <span data-ttu-id="a7ab4-124">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="a7ab4-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a7ab4-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7ab4-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

