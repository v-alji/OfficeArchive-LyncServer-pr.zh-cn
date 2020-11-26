---
title: Lync Server 2013：tblFileToken
description: Lync Server 2013： tblFileToken。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423526"
---
# <a name="tblfiletoken-in-lync-server-2013"></a><span data-ttu-id="0080f-103">Lync Server 2013 中的 tblFileToken</span><span class="sxs-lookup"><span data-stu-id="0080f-103">tblFileToken in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0080f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0080f-104">

<span> </span></span></span>

<span data-ttu-id="0080f-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="0080f-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="0080f-106">tblFileToken 包含用于文件传输目的的临时令牌。</span><span class="sxs-lookup"><span data-stu-id="0080f-106">tblFileToken contains temporary tokens for file transfer purposes.</span></span>

### <a name="columns"></a><span data-ttu-id="0080f-107">多</span><span class="sxs-lookup"><span data-stu-id="0080f-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0080f-108">列</span><span class="sxs-lookup"><span data-stu-id="0080f-108">Column</span></span></th>
<th><span data-ttu-id="0080f-109">类型</span><span class="sxs-lookup"><span data-stu-id="0080f-109">Type</span></span></th>
<th><span data-ttu-id="0080f-110">说明</span><span class="sxs-lookup"><span data-stu-id="0080f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0080f-111">fileToken</span><span class="sxs-lookup"><span data-stu-id="0080f-111">fileToken</span></span></p></td>
<td><p><span data-ttu-id="0080f-112">nvarchar (50) ，not null</span><span class="sxs-lookup"><span data-stu-id="0080f-112">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="0080f-113">GUID)  (唯一令牌。</span><span class="sxs-lookup"><span data-stu-id="0080f-113">Unique token (a GUID).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0080f-114">fileTokenUserID</span><span class="sxs-lookup"><span data-stu-id="0080f-114">fileTokenUserID</span></span></p></td>
<td><p><span data-ttu-id="0080f-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="0080f-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="0080f-116">传输文件的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="0080f-116">ID of the principal that is transferring the file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0080f-117">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="0080f-117">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="0080f-118">GUID，not null</span><span class="sxs-lookup"><span data-stu-id="0080f-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="0080f-119">聊天室节点的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0080f-119">GUID of the chat room node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0080f-120">fileTokenExpireDate</span><span class="sxs-lookup"><span data-stu-id="0080f-120">fileTokenExpireDate</span></span></p></td>
<td><p><span data-ttu-id="0080f-121">datetime，not null</span><span class="sxs-lookup"><span data-stu-id="0080f-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="0080f-122">过期时间。</span><span class="sxs-lookup"><span data-stu-id="0080f-122">Expiration time.</span></span> <span data-ttu-id="0080f-123"> (令牌将在30分钟后过期，除非已固定 (请参阅本专栏中的以下说明) 。</span><span class="sxs-lookup"><span data-stu-id="0080f-123">(Tokens expire after 30 minutes, unless pinned (see the following descriptions in this column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0080f-124">fileTokenComplianceFileUrl</span><span class="sxs-lookup"><span data-stu-id="0080f-124">fileTokenComplianceFileUrl</span></span></p></td>
<td><p><span data-ttu-id="0080f-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0080f-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0080f-126">为合规性服务使用) 的已传送文件 (的 URL。</span><span class="sxs-lookup"><span data-stu-id="0080f-126">URL of the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0080f-127">fileTokenComplianceThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="0080f-127">fileTokenComplianceThumbnailUrl</span></span></p></td>
<td><p><span data-ttu-id="0080f-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="0080f-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="0080f-129">已传输文件的缩略图的 URL (以获取合规性服务使用) 。</span><span class="sxs-lookup"><span data-stu-id="0080f-129">URL of the thumbnail for the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0080f-130">fileTokenComplianceTime</span><span class="sxs-lookup"><span data-stu-id="0080f-130">fileTokenComplianceTime</span></span></p></td>
<td><p><span data-ttu-id="0080f-131">datetime2</span><span class="sxs-lookup"><span data-stu-id="0080f-131">datetime2</span></span></p></td>
<td><p><span data-ttu-id="0080f-132">用于 (合规性服务使用) 的实际文件传输操作的时间戳。</span><span class="sxs-lookup"><span data-stu-id="0080f-132">Timestamp for the actual file transfer operation (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0080f-133">fileTokenComplianceIsUpload</span><span class="sxs-lookup"><span data-stu-id="0080f-133">fileTokenComplianceIsUpload</span></span></p></td>
<td><p><span data-ttu-id="0080f-134">bit</span><span class="sxs-lookup"><span data-stu-id="0080f-134">bit</span></span></p></td>
<td><p><span data-ttu-id="0080f-135">如果上载，则为 True;如果下载 (以获取合规性服务使用) ，则为 False。</span><span class="sxs-lookup"><span data-stu-id="0080f-135">True if upload; False if download (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0080f-136">fileTokenCompliancePinned</span><span class="sxs-lookup"><span data-stu-id="0080f-136">fileTokenCompliancePinned</span></span></p></td>
<td><p><span data-ttu-id="0080f-137">位，not null</span><span class="sxs-lookup"><span data-stu-id="0080f-137">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="0080f-138">如果标记已固定，则为 True。</span><span class="sxs-lookup"><span data-stu-id="0080f-138">True if token is pinned.</span></span> <span data-ttu-id="0080f-139">它用于在表中保留令牌，直到合规性服务有机会从中检索相关字段。</span><span class="sxs-lookup"><span data-stu-id="0080f-139">It’s used to keep the token in the table until Compliance service has a chance to retrieve the relevant fields from it.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="0080f-140">标示</span><span class="sxs-lookup"><span data-stu-id="0080f-140">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0080f-141">列</span><span class="sxs-lookup"><span data-stu-id="0080f-141">Column</span></span></th>
<th><span data-ttu-id="0080f-142">说明</span><span class="sxs-lookup"><span data-stu-id="0080f-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0080f-143">fileToken</span><span class="sxs-lookup"><span data-stu-id="0080f-143">fileToken</span></span></p></td>
<td><p><span data-ttu-id="0080f-144">主键。</span><span class="sxs-lookup"><span data-stu-id="0080f-144">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0080f-145">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="0080f-145">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="0080f-146">TblNode 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="0080f-146">Foreign key with lookup in tblNode.nodeGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0080f-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0080f-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

