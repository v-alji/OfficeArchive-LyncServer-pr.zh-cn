---
title: Lync Server 2013：tblActivePeers
description: Lync Server 2013： tblActivePeers。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblActivePeers
ms:assetid: b50c3f4a-bab6-4cb9-b40e-016cf1a9c607
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615030(v=OCS.15)
ms:contentKeyID: 48185176
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f274f82a280883e38e8e02409305982b64c18e4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392010"
---
# <a name="tblactivepeers-in-lync-server-2013"></a><span data-ttu-id="e1def-103">Lync Server 2013 中的 tblActivePeers</span><span class="sxs-lookup"><span data-stu-id="e1def-103">tblActivePeers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1def-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1def-104">

<span> </span></span></span>

<span data-ttu-id="e1def-105">_**主题上次修改时间：** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="e1def-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="e1def-106">tblActivePeers 包含聊天服务之间的当前点对点连接。</span><span class="sxs-lookup"><span data-stu-id="e1def-106">tblActivePeers contains the current peer-to-peer connections between chat services.</span></span>

### <a name="columns"></a><span data-ttu-id="e1def-107">多</span><span class="sxs-lookup"><span data-stu-id="e1def-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1def-108">列</span><span class="sxs-lookup"><span data-stu-id="e1def-108">Column</span></span></th>
<th><span data-ttu-id="e1def-109">类型</span><span class="sxs-lookup"><span data-stu-id="e1def-109">Type</span></span></th>
<th><span data-ttu-id="e1def-110">说明</span><span class="sxs-lookup"><span data-stu-id="e1def-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1def-111">aplServerID</span><span class="sxs-lookup"><span data-stu-id="e1def-111">aplServerID</span></span></p></td>
<td><p><span data-ttu-id="e1def-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="e1def-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="e1def-113">已发布条目的服务器的 ID。</span><span class="sxs-lookup"><span data-stu-id="e1def-113">ID of the server that posted the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1def-114">aplPeerID</span><span class="sxs-lookup"><span data-stu-id="e1def-114">aplPeerID</span></span></p></td>
<td><p><span data-ttu-id="e1def-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="e1def-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="e1def-116">过帐服务器连接到的对等的 ID。</span><span class="sxs-lookup"><span data-stu-id="e1def-116">ID of the peer that the posting server is connected to.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="e1def-117">标示</span><span class="sxs-lookup"><span data-stu-id="e1def-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1def-118">列</span><span class="sxs-lookup"><span data-stu-id="e1def-118">Column</span></span></th>
<th><span data-ttu-id="e1def-119">说明</span><span class="sxs-lookup"><span data-stu-id="e1def-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1def-120">&lt;aplServerID, aplPeerID&gt;</span><span class="sxs-lookup"><span data-stu-id="e1def-120">&lt;aplServerID, aplPeerID&gt;</span></span></p></td>
<td><p><span data-ttu-id="e1def-121">主键。</span><span class="sxs-lookup"><span data-stu-id="e1def-121">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1def-122">aplServerID</span><span class="sxs-lookup"><span data-stu-id="e1def-122">aplServerID</span></span></p></td>
<td><p><span data-ttu-id="e1def-123">TblServerIdentity 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="e1def-123">Foreign key with lookup in tblServerIdentity.serverID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1def-124">aplPeerID</span><span class="sxs-lookup"><span data-stu-id="e1def-124">aplPeerID</span></span></p></td>
<td><p><span data-ttu-id="e1def-125">TblServerIdentity 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="e1def-125">Foreign key with lookup in tblServerIdentity.serverID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e1def-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1def-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

