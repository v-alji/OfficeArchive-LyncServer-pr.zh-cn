---
title: Lync Server 2013：tblComplianceData
description: Lync Server 2013： tblComplianceData。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444474"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a><span data-ttu-id="e16c1-103">Lync Server 2013 中的 tblComplianceData</span><span class="sxs-lookup"><span data-stu-id="e16c1-103">tblComplianceData in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e16c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e16c1-104">

<span> </span></span></span>

<span data-ttu-id="e16c1-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="e16c1-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="e16c1-106">tblComplianceData 包含尚未由合规性适配器处理的合规性事件。</span><span class="sxs-lookup"><span data-stu-id="e16c1-106">tblComplianceData contains the compliance events that have not been processed by the compliance adapter yet.</span></span>

### <a name="columns"></a><span data-ttu-id="e16c1-107">多</span><span class="sxs-lookup"><span data-stu-id="e16c1-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e16c1-108">列</span><span class="sxs-lookup"><span data-stu-id="e16c1-108">Column</span></span></th>
<th><span data-ttu-id="e16c1-109">类型</span><span class="sxs-lookup"><span data-stu-id="e16c1-109">Type</span></span></th>
<th><span data-ttu-id="e16c1-110">说明</span><span class="sxs-lookup"><span data-stu-id="e16c1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e16c1-111">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="e16c1-111">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="e16c1-112">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="e16c1-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="e16c1-113">事件 ID。</span><span class="sxs-lookup"><span data-stu-id="e16c1-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e16c1-114">entryDate</span><span class="sxs-lookup"><span data-stu-id="e16c1-114">entryDate</span></span></p></td>
<td><p><span data-ttu-id="e16c1-115">smalldatetime，not null</span><span class="sxs-lookup"><span data-stu-id="e16c1-115">smalldatetime, not null</span></span></p></td>
<td><p><span data-ttu-id="e16c1-116">插入 (的时间可能会在未来的 cmplType = 9 中，因为在该情况下该项只是占位符) 。</span><span class="sxs-lookup"><span data-stu-id="e16c1-116">Time of insertion (may be far in the future for cmplType=9 because the entry is just a placeholder in that case).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e16c1-117">cmplType</span><span class="sxs-lookup"><span data-stu-id="e16c1-117">cmplType</span></span></p></td>
<td><p><span data-ttu-id="e16c1-118">int，not null</span><span class="sxs-lookup"><span data-stu-id="e16c1-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="e16c1-119">合规性事件的类型：</span><span class="sxs-lookup"><span data-stu-id="e16c1-119">Type of compliance event:</span></span></p>
<ul>
<li><p><span data-ttu-id="e16c1-120">1：聊天</span><span class="sxs-lookup"><span data-stu-id="e16c1-120">1: Chat</span></span></p></li>
<li><p><span data-ttu-id="e16c1-121">2： Backchat</span><span class="sxs-lookup"><span data-stu-id="e16c1-121">2: Backchat</span></span></p></li>
<li><p><span data-ttu-id="e16c1-122">3：文件下载</span><span class="sxs-lookup"><span data-stu-id="e16c1-122">3: File download</span></span></p></li>
<li><p><span data-ttu-id="e16c1-123">4：文件上载</span><span class="sxs-lookup"><span data-stu-id="e16c1-123">4: File upload</span></span></p></li>
<li><p><span data-ttu-id="e16c1-124">9：临时文件传输</span><span class="sxs-lookup"><span data-stu-id="e16c1-124">9: Provisional file transfer</span></span></p></li>
<li><p><span data-ttu-id="e16c1-125">10：与 "替换")  (的聊天删除</span><span class="sxs-lookup"><span data-stu-id="e16c1-125">10: Chat deletion (with replace)</span></span></p></li>
<li><p><span data-ttu-id="e16c1-126">11：聊天清除</span><span class="sxs-lookup"><span data-stu-id="e16c1-126">11: Chat purging</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e16c1-127">cmplTime</span><span class="sxs-lookup"><span data-stu-id="e16c1-127">cmplTime</span></span></p></td>
<td><p><span data-ttu-id="e16c1-128">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="e16c1-128">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="e16c1-129">事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="e16c1-129">Time stamp for the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e16c1-130">cmplChannelUri</span><span class="sxs-lookup"><span data-stu-id="e16c1-130">cmplChannelUri</span></span></p></td>
<td><p><span data-ttu-id="e16c1-131">nvarchar (255) ，not null</span><span class="sxs-lookup"><span data-stu-id="e16c1-131">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="e16c1-132">通道统一资源标识符 (URI) 。</span><span class="sxs-lookup"><span data-stu-id="e16c1-132">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e16c1-133">cmplChatID</span><span class="sxs-lookup"><span data-stu-id="e16c1-133">cmplChatID</span></span></p></td>
<td><p><span data-ttu-id="e16c1-134">bigint</span><span class="sxs-lookup"><span data-stu-id="e16c1-134">bigint</span></span></p></td>
<td><p><span data-ttu-id="e16c1-135">聊天 ID (对应于 tblChat chatId 表) 。</span><span class="sxs-lookup"><span data-stu-id="e16c1-135">Chat ID (corresponding to tblChat.chatId table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e16c1-136">cmplUserID</span><span class="sxs-lookup"><span data-stu-id="e16c1-136">cmplUserID</span></span></p></td>
<td><p><span data-ttu-id="e16c1-137">int，not null</span><span class="sxs-lookup"><span data-stu-id="e16c1-137">int, not null</span></span></p></td>
<td><p><span data-ttu-id="e16c1-138">标牌的主体 ID (对应于 tblPrincipal prinID 表) 。</span><span class="sxs-lookup"><span data-stu-id="e16c1-138">Principal ID of the poster (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e16c1-139">cmplUserUri</span><span class="sxs-lookup"><span data-stu-id="e16c1-139">cmplUserUri</span></span></p></td>
<td><p><span data-ttu-id="e16c1-140">nvarchar (255) ，not null</span><span class="sxs-lookup"><span data-stu-id="e16c1-140">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="e16c1-141">用户 URI。</span><span class="sxs-lookup"><span data-stu-id="e16c1-141">User URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e16c1-142">cmplMessage</span><span class="sxs-lookup"><span data-stu-id="e16c1-142">cmplMessage</span></span></p></td>
<td><p><span data-ttu-id="e16c1-143">nvarchar (max) </span><span class="sxs-lookup"><span data-stu-id="e16c1-143">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="e16c1-144"> (编码的消息取决于 cmplType) 。</span><span class="sxs-lookup"><span data-stu-id="e16c1-144">Message (encoding depends on cmplType).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="e16c1-145">密钥</span><span class="sxs-lookup"><span data-stu-id="e16c1-145">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e16c1-146">列</span><span class="sxs-lookup"><span data-stu-id="e16c1-146">Column</span></span></th>
<th><span data-ttu-id="e16c1-147">说明</span><span class="sxs-lookup"><span data-stu-id="e16c1-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e16c1-148">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="e16c1-148">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="e16c1-149">主键。</span><span class="sxs-lookup"><span data-stu-id="e16c1-149">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e16c1-150">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e16c1-150">


</div>

<span> </span>

</div>

</div>

</span></span></div>

