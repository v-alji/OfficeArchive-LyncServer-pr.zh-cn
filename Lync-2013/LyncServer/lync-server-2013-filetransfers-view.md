---
title: Lync Server 2013： FileTransfers 视图
description: Lync Server 2013： FileTransfers 视图。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428151"
---
# <a name="filetransfers-view-in-lync-server-2013"></a><span data-ttu-id="cb8f1-103">Lync Server 2013 中的 FileTransfers 视图</span><span class="sxs-lookup"><span data-stu-id="cb8f1-103">FileTransfers view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb8f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb8f1-104">

<span> </span></span></span>

<span data-ttu-id="cb8f1-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="cb8f1-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="cb8f1-106">FileTransfer 视图存储有关对等文件传输会话的信息。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-106">The FileTransfer view stores information about peer-to-peer file transfer sessions.</span></span> <span data-ttu-id="cb8f1-107">此视图已在 Microsoft Lync Server 2013 中引入。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cb8f1-108">FileTransfers 视图包含 <A href="lync-server-2013-sessiondetails-view.md">Lync Server 2013 的 SessionDetails 视图</A> 中的所有列以及下面列出的列。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-108">The FileTransfers view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8f1-109">列</span><span class="sxs-lookup"><span data-stu-id="cb8f1-109">Column</span></span></th>
<th><span data-ttu-id="cb8f1-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="cb8f1-110">Data Type</span></span></th>
<th><span data-ttu-id="cb8f1-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="cb8f1-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb8f1-112"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="cb8f1-112"><strong>FileName</strong></span></span></p></td>
<td><p><span data-ttu-id="cb8f1-113">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cb8f1-113">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cb8f1-114">已传输的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-114">Name of the file transferred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8f1-115"><strong>票证</strong></span><span class="sxs-lookup"><span data-stu-id="cb8f1-115"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="cb8f1-116">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="cb8f1-116">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="cb8f1-117">用于标识要与此邮件关联的每个后续消息。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-117">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb8f1-118"><strong>FileIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="cb8f1-118"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="cb8f1-119">标识符</span><span class="sxs-lookup"><span data-stu-id="cb8f1-119">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="cb8f1-120">唯一标识符，用于区分涉及相同文件名的文件传输。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-120">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8f1-121"><strong>容纳</strong></span><span class="sxs-lookup"><span data-stu-id="cb8f1-121"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="cb8f1-122">bit</span><span class="sxs-lookup"><span data-stu-id="cb8f1-122">bit</span></span></p></td>
<td><p><span data-ttu-id="cb8f1-123">可以为 TRUE 或 NULL。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-123">Can be TRUE or NULL.</span></span> <span data-ttu-id="cb8f1-124">如果为 TRUE，则 "拒绝" 和 "取消" 将为 NULL。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-124">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb8f1-125"><strong>&</strong></span><span class="sxs-lookup"><span data-stu-id="cb8f1-125"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="cb8f1-126">bit</span><span class="sxs-lookup"><span data-stu-id="cb8f1-126">bit</span></span></p></td>
<td><p><span data-ttu-id="cb8f1-127">可以为 TRUE 或 NULL。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-127">Can be TRUE or NULL.</span></span> <span data-ttu-id="cb8f1-128">如果为 TRUE，则 "接受" 和 "取消" 将为 NULL。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-128">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb8f1-129"><strong>取消</strong></span><span class="sxs-lookup"><span data-stu-id="cb8f1-129"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="cb8f1-130">bit</span><span class="sxs-lookup"><span data-stu-id="cb8f1-130">bit</span></span></p></td>
<td><p><span data-ttu-id="cb8f1-131">可以为 TRUE 或 NULL。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-131">Can be TRUE or NULL.</span></span> <span data-ttu-id="cb8f1-132">如果为 TRUE，则 "接受" 和 "拒绝" 将为 NULL。</span><span class="sxs-lookup"><span data-stu-id="cb8f1-132">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cb8f1-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb8f1-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

