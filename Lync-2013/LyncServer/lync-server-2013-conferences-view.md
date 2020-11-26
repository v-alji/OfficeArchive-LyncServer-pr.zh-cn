---
title: Lync Server 2013：会议视图
description: Lync Server 2013： "会议" 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences view
ms:assetid: c0e5c4db-c135-401f-9296-e9a49f6499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721871(v=OCS.15)
ms:contentKeyID: 49733803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee7fbb7c839c351fc9c81716a5800a678980549
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434422"
---
# <a name="conferences-view-in-lync-server-2013"></a><span data-ttu-id="225aa-103">Lync Server 2013 中的 "会议" 视图</span><span class="sxs-lookup"><span data-stu-id="225aa-103">Conferences view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="225aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="225aa-104">

<span> </span></span></span>

<span data-ttu-id="225aa-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="225aa-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="225aa-106">"会议" 视图存储有关会议的信息。</span><span class="sxs-lookup"><span data-stu-id="225aa-106">The Conferences View stores information about the conferences.</span></span> <span data-ttu-id="225aa-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="225aa-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="225aa-108">列</span><span class="sxs-lookup"><span data-stu-id="225aa-108">Column</span></span></th>
<th><span data-ttu-id="225aa-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="225aa-109">Data Type</span></span></th>
<th><span data-ttu-id="225aa-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="225aa-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="225aa-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-112">datetime</span><span class="sxs-lookup"><span data-stu-id="225aa-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="225aa-113">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="225aa-113">Time of session request.</span></span> <span data-ttu-id="225aa-114">与 SessionIdSeq 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="225aa-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="225aa-115">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="225aa-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="225aa-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-117">int</span><span class="sxs-lookup"><span data-stu-id="225aa-117">int</span></span></p></td>
<td><p><span data-ttu-id="225aa-118">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="225aa-118">ID number to identify the session.</span></span> <span data-ttu-id="225aa-119">与 SessionIdTime 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="225aa-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="225aa-120">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="225aa-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="225aa-121"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-121"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-122">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="225aa-122">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="225aa-123">会议的 URI。</span><span class="sxs-lookup"><span data-stu-id="225aa-123">URI for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="225aa-124"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-124"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="225aa-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="225aa-126">会议 URI 的类型。</span><span class="sxs-lookup"><span data-stu-id="225aa-126">Type of the conference URI.</span></span> <span data-ttu-id="225aa-127">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="225aa-127">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="225aa-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-129">标识符</span><span class="sxs-lookup"><span data-stu-id="225aa-129">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="225aa-130">用于定期会议。</span><span class="sxs-lookup"><span data-stu-id="225aa-130">Used for recurring conferences.</span></span> <span data-ttu-id="225aa-131">定期会议的每个实例都具有相同的 ConferenceUri，但具有不同的 ConfInstance。</span><span class="sxs-lookup"><span data-stu-id="225aa-131">Each instance of a recurring conference has the same ConferenceUri but a different ConfInstance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="225aa-132"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-132"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-133">datetime</span><span class="sxs-lookup"><span data-stu-id="225aa-133">datetime</span></span></p></td>
<td><p><span data-ttu-id="225aa-134">会议的开始时间。</span><span class="sxs-lookup"><span data-stu-id="225aa-134">Starting time for the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="225aa-135"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-135"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-136">datetime</span><span class="sxs-lookup"><span data-stu-id="225aa-136">datetime</span></span></p></td>
<td><p><span data-ttu-id="225aa-137">会议的结束时间。</span><span class="sxs-lookup"><span data-stu-id="225aa-137">Ending time for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="225aa-138"><strong>OrganizerUri</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-138"><strong>OrganizerUri</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-139">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="225aa-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="225aa-140">组织会议的用户的 URI。</span><span class="sxs-lookup"><span data-stu-id="225aa-140">URI of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="225aa-141"><strong>OrganizerType</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-141"><strong>OrganizerType</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="225aa-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="225aa-143">组织会议的用户的 URI 类型。</span><span class="sxs-lookup"><span data-stu-id="225aa-143">Type of URI of the user who organized the conference.</span></span> <span data-ttu-id="225aa-144">有关详细信息，请参阅 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 中的 UriTypes 表</a> 。</span><span class="sxs-lookup"><span data-stu-id="225aa-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="225aa-145"><strong>OrganizerTenant</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-145"><strong>OrganizerTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-146">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="225aa-146">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="225aa-147">组织会议的用户的租户。</span><span class="sxs-lookup"><span data-stu-id="225aa-147">Tenant of the user who organized the conference.</span></span> <span data-ttu-id="225aa-148">有关详细信息，请参阅 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 中的租户表</a> 。</span><span class="sxs-lookup"><span data-stu-id="225aa-148">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="225aa-149"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-149"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="225aa-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="225aa-151">托管会议的池的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="225aa-151">Fully qualified domain name of the pool that hosted the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="225aa-152"><strong>旗</strong></span><span class="sxs-lookup"><span data-stu-id="225aa-152"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="225aa-153">smallint</span><span class="sxs-lookup"><span data-stu-id="225aa-153">smallint</span></span></p></td>
<td><p><span data-ttu-id="225aa-154">包含会议属性的位掩码。</span><span class="sxs-lookup"><span data-stu-id="225aa-154">Bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="225aa-155">可能的值：</span><span class="sxs-lookup"><span data-stu-id="225aa-155">Possible values are:</span></span></p>
<p><span data-ttu-id="225aa-156">0X01-合成事务</span><span class="sxs-lookup"><span data-stu-id="225aa-156">0X01 – Synthetic Transaction</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="225aa-157">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="225aa-157">


</div>

<span> </span>

</div>

</div>

</span></span></div>

