---
title: Lync Server 2013： VoIPDetails 视图
description: Lync Server 2013： VoIPDetails 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoIPDetails view
ms:assetid: 14c44736-71ba-4fc5-82c7-1df65bf6261c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687973(v=OCS.15)
ms:contentKeyID: 49733561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ecd34be0c8568eef29d773f088e8503a8065743
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446182"
---
# <a name="voipdetails-view-in-lync-server-2013"></a><span data-ttu-id="6ef85-103">Lync Server 2013 中的 VoIPDetails 视图</span><span class="sxs-lookup"><span data-stu-id="6ef85-103">VoIPDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ef85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ef85-104">

<span> </span></span></span>

<span data-ttu-id="6ef85-105">_**主题上次修改时间：** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="6ef85-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="6ef85-106">VoIPDetails 视图存储有关对等会话的信息，其中至少有一个用户是 VoIP 用户。</span><span class="sxs-lookup"><span data-stu-id="6ef85-106">The VoIPDetails view stores information about peer-to-peer sessions, where at least one user is a VoIP user.</span></span> <span data-ttu-id="6ef85-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="6ef85-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6ef85-108">VoIPDetails 视图包含 <A href="lync-server-2013-sessiondetails-view.md">Lync Server 2013 的 SessionDetails 视图</A> 中的所有列以及下面列出的列。</span><span class="sxs-lookup"><span data-stu-id="6ef85-108">The VoIPDetails view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ef85-109">列</span><span class="sxs-lookup"><span data-stu-id="6ef85-109">Column</span></span></th>
<th><span data-ttu-id="6ef85-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="6ef85-110">Data Type</span></span></th>
<th><span data-ttu-id="6ef85-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="6ef85-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ef85-112"><strong>FromPhone</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-112"><strong>FromPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-113">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="6ef85-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-114">启动会话的用户的电话 URI。</span><span class="sxs-lookup"><span data-stu-id="6ef85-114">Phone URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ef85-115"><strong>ToPhone</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-115"><strong>ToPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-116">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="6ef85-116">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-117">加入会话的用户的电话 URI。</span><span class="sxs-lookup"><span data-stu-id="6ef85-117">Phone URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ef85-118"><strong>DisconnectedByUri</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-118"><strong>DisconnectedByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-119">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="6ef85-119">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-120">断开会话的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="6ef85-120">URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ef85-121"><strong>DisconnectedByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-121"><strong>DisconnectedByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ef85-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-123">断开会话的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="6ef85-123">Type of URI of the user who disconnected the session.</span></span> <span data-ttu-id="6ef85-124">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="6ef85-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ef85-125"><strong>DisconnectedByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-125"><strong>DisconnectedByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ef85-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-127">断开会话的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="6ef85-127">Tenant of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ef85-128"><strong>DisconnectedByPhone</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-128"><strong>DisconnectedByPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-129">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="6ef85-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-130">断开会话的用户的电话 URI。</span><span class="sxs-lookup"><span data-stu-id="6ef85-130">Phone URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ef85-131"><strong>FromMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-131"><strong>FromMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ef85-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-133">启动会话的用户所使用的中介服务器。</span><span class="sxs-lookup"><span data-stu-id="6ef85-133">Mediation Server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ef85-134"><strong>ToMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-134"><strong>ToMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ef85-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-136">加入会话的用户所使用的中介服务器。</span><span class="sxs-lookup"><span data-stu-id="6ef85-136">Mediation Server used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ef85-137"><strong>FromGateway</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-137"><strong>FromGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ef85-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-139">启动会话的用户所使用的网关。</span><span class="sxs-lookup"><span data-stu-id="6ef85-139">Gateway used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ef85-140"><strong>ToGateway</strong></span><span class="sxs-lookup"><span data-stu-id="6ef85-140"><strong>ToGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="6ef85-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6ef85-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="6ef85-142">加入会话的用户所使用的网关。</span><span class="sxs-lookup"><span data-stu-id="6ef85-142">Gateway used by the user who joined the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6ef85-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ef85-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

