---
title: Lync Server 2013：tblComplianceParticipant
description: Lync Server 2013： tblComplianceParticipant。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceParticipant
ms:assetid: 5d7e0dea-74f7-46d1-badf-b94abc8f066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558655(v=OCS.15)
ms:contentKeyID: 48184262
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1385b0a635f003a72de93f10f72642314ad7ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444453"
---
# <a name="tblcomplianceparticipant-in-lync-server-2013"></a><span data-ttu-id="4b6da-103">Lync Server 2013 中的 tblComplianceParticipant</span><span class="sxs-lookup"><span data-stu-id="4b6da-103">tblComplianceParticipant in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b6da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b6da-104">

<span> </span></span></span>

<span data-ttu-id="4b6da-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="4b6da-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="4b6da-106">tblComplianceParticipant 包含每个频道和每台服务器的当前参与者。</span><span class="sxs-lookup"><span data-stu-id="4b6da-106">tblComplianceParticipant contains the current participants per channel and per server.</span></span>

### <a name="columns"></a><span data-ttu-id="4b6da-107">多</span><span class="sxs-lookup"><span data-stu-id="4b6da-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b6da-108">列</span><span class="sxs-lookup"><span data-stu-id="4b6da-108">Column</span></span></th>
<th><span data-ttu-id="4b6da-109">类型</span><span class="sxs-lookup"><span data-stu-id="4b6da-109">Type</span></span></th>
<th><span data-ttu-id="4b6da-110">说明</span><span class="sxs-lookup"><span data-stu-id="4b6da-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b6da-111">channelUri</span><span class="sxs-lookup"><span data-stu-id="4b6da-111">channelUri</span></span></p></td>
<td><p><span data-ttu-id="4b6da-112">nvarchar (255) ，not null</span><span class="sxs-lookup"><span data-stu-id="4b6da-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="4b6da-113">通道统一资源标识符 (URI) 。</span><span class="sxs-lookup"><span data-stu-id="4b6da-113">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b6da-114">userId</span><span class="sxs-lookup"><span data-stu-id="4b6da-114">userId</span></span></p></td>
<td><p><span data-ttu-id="4b6da-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="4b6da-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="4b6da-116">参与者的主体 ID (对应于 tblPrincipal prinID 表) 。</span><span class="sxs-lookup"><span data-stu-id="4b6da-116">Principal ID of the participant (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b6da-117">joinedAt</span><span class="sxs-lookup"><span data-stu-id="4b6da-117">joinedAt</span></span></p></td>
<td><p><span data-ttu-id="4b6da-118">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="4b6da-118">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="4b6da-119">联接事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="4b6da-119">Time stamp of the joining event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b6da-120">partedAt</span><span class="sxs-lookup"><span data-stu-id="4b6da-120">partedAt</span></span></p></td>
<td><p><span data-ttu-id="4b6da-121">bigint</span><span class="sxs-lookup"><span data-stu-id="4b6da-121">bigint</span></span></p></td>
<td><p><span data-ttu-id="4b6da-122">如果参与者仍处于加入，则为 Null。</span><span class="sxs-lookup"><span data-stu-id="4b6da-122">Null if participant is still joined.</span></span> <span data-ttu-id="4b6da-123">如果 not null，则通道的时间戳会留下事件。</span><span class="sxs-lookup"><span data-stu-id="4b6da-123">The time stamp of the channel leaving event if not null.</span></span></p>
<p><span data-ttu-id="4b6da-124">这些条目最终会在所有翻译人员处理该事件时被删除。</span><span class="sxs-lookup"><span data-stu-id="4b6da-124">These entries are eventually removed when all translators process the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b6da-125">userUri</span><span class="sxs-lookup"><span data-stu-id="4b6da-125">userUri</span></span></p></td>
<td><p><span data-ttu-id="4b6da-126">nvarchar (255) ，not null</span><span class="sxs-lookup"><span data-stu-id="4b6da-126">nvarchar(255), not null</span></span></p></td>
<td><p><span data-ttu-id="4b6da-127">用户 URI。</span><span class="sxs-lookup"><span data-stu-id="4b6da-127">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b6da-128">serverID</span><span class="sxs-lookup"><span data-stu-id="4b6da-128">serverID</span></span></p></td>
<td><p><span data-ttu-id="4b6da-129">int</span><span class="sxs-lookup"><span data-stu-id="4b6da-129">int</span></span></p></td>
<td><p><span data-ttu-id="4b6da-130">服务器标识 (，tblServerIdentity serverID table) 中所示。</span><span class="sxs-lookup"><span data-stu-id="4b6da-130">Server identity (as in tblServerIdentity.serverID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b6da-131">标识符</span><span class="sxs-lookup"><span data-stu-id="4b6da-131">sessionId</span></span></p></td>
<td><p><span data-ttu-id="4b6da-132">bigint</span><span class="sxs-lookup"><span data-stu-id="4b6da-132">bigint</span></span></p></td>
<td><p><span data-ttu-id="4b6da-133">服务器会话。</span><span class="sxs-lookup"><span data-stu-id="4b6da-133">Server session.</span></span> <span data-ttu-id="4b6da-134">这是每次启动聊天服务时生成的随机数字。</span><span class="sxs-lookup"><span data-stu-id="4b6da-134">This is a random number generated each time a Chat service starts.</span></span> <span data-ttu-id="4b6da-135">它用于为识别孤立参与者的目的而区分会话。</span><span class="sxs-lookup"><span data-stu-id="4b6da-135">It is used to differentiate sessions for the purpose of identifying orphaned participants.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="4b6da-136">密钥</span><span class="sxs-lookup"><span data-stu-id="4b6da-136">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b6da-137">列</span><span class="sxs-lookup"><span data-stu-id="4b6da-137">Column</span></span></th>
<th><span data-ttu-id="4b6da-138">说明</span><span class="sxs-lookup"><span data-stu-id="4b6da-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b6da-139">&lt;channelUri、userId、joinedAt&gt;</span><span class="sxs-lookup"><span data-stu-id="4b6da-139">&lt;channelUri, userId, joinedAt&gt;</span></span></p></td>
<td><p><span data-ttu-id="4b6da-140">主键。</span><span class="sxs-lookup"><span data-stu-id="4b6da-140">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4b6da-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b6da-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

