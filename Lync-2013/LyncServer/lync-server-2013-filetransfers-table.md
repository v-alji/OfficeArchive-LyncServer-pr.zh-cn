---
title: Lync Server 2013：FileTransfers 表
description: Lync Server 2013： FileTransfers 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers table
ms:assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398353(v=OCS.15)
ms:contentKeyID: 48184118
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccde45fa3743a809499273676d567846ef292ecc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428165"
---
# <a name="filetransfers-table-in-lync-server-2013"></a><span data-ttu-id="888b6-103">Lync Server 2013 中的 FileTransfers 表</span><span class="sxs-lookup"><span data-stu-id="888b6-103">FileTransfers table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="888b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="888b6-104">

<span> </span></span></span>

<span data-ttu-id="888b6-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="888b6-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="888b6-106">每条记录表示一个文件传输会话。</span><span class="sxs-lookup"><span data-stu-id="888b6-106">Each record represents one file transfer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="888b6-107">列</span><span class="sxs-lookup"><span data-stu-id="888b6-107">Column</span></span></th>
<th><span data-ttu-id="888b6-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="888b6-108">Data Type</span></span></th>
<th><span data-ttu-id="888b6-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="888b6-109">Key/Index</span></span></th>
<th><span data-ttu-id="888b6-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="888b6-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="888b6-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-112">datetime</span><span class="sxs-lookup"><span data-stu-id="888b6-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="888b6-113">主、外部</span><span class="sxs-lookup"><span data-stu-id="888b6-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="888b6-114">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="888b6-114">Time of session request.</span></span> <span data-ttu-id="888b6-115">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="888b6-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="888b6-116">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="888b6-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888b6-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-118">int</span><span class="sxs-lookup"><span data-stu-id="888b6-118">int</span></span></p></td>
<td><p><span data-ttu-id="888b6-119">主、外部</span><span class="sxs-lookup"><span data-stu-id="888b6-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="888b6-120">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="888b6-120">ID number to identify the session.</span></span> <span data-ttu-id="888b6-121">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="888b6-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="888b6-122">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="888b6-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888b6-123"><strong>文件名</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-123"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-124">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="888b6-124">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="888b6-125">文件的名称。</span><span class="sxs-lookup"><span data-stu-id="888b6-125">Name of the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888b6-126"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-126"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-127">标识符</span><span class="sxs-lookup"><span data-stu-id="888b6-127">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="888b6-128">唯一标识符，用于区分涉及相同文件名的文件传输。</span><span class="sxs-lookup"><span data-stu-id="888b6-128">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888b6-129"><strong>票证</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-129"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-130">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="888b6-130">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="888b6-131">Primary</span><span class="sxs-lookup"><span data-stu-id="888b6-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="888b6-132">用于标识要与此邮件关联的每个后续消息。</span><span class="sxs-lookup"><span data-stu-id="888b6-132">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888b6-133"><strong>容纳</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-133"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-134">bit</span><span class="sxs-lookup"><span data-stu-id="888b6-134">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="888b6-135">可以为 TRUE 或 NULL。</span><span class="sxs-lookup"><span data-stu-id="888b6-135">Can be TRUE or NULL.</span></span> <span data-ttu-id="888b6-136">如果为 TRUE，则 "拒绝" 和 "取消" 将为 NULL。</span><span class="sxs-lookup"><span data-stu-id="888b6-136">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="888b6-137"><strong>&</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-137"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-138">bit</span><span class="sxs-lookup"><span data-stu-id="888b6-138">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="888b6-139">可以为 TRUE 或 NULL。</span><span class="sxs-lookup"><span data-stu-id="888b6-139">Can be TRUE or NULL.</span></span> <span data-ttu-id="888b6-140">如果为 TRUE，则 "接受" 和 "取消" 将为 NULL。</span><span class="sxs-lookup"><span data-stu-id="888b6-140">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="888b6-141"><strong>取消</strong></span><span class="sxs-lookup"><span data-stu-id="888b6-141"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="888b6-142">bit</span><span class="sxs-lookup"><span data-stu-id="888b6-142">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="888b6-143">可以为 TRUE 或 NULL。</span><span class="sxs-lookup"><span data-stu-id="888b6-143">Can be TRUE or NULL.</span></span> <span data-ttu-id="888b6-144">如果为 TRUE，则 "接受" 和 "拒绝" 将为 NULL。</span><span class="sxs-lookup"><span data-stu-id="888b6-144">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="888b6-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="888b6-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

