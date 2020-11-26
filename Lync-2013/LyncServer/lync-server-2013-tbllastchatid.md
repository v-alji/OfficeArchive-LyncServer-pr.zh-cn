---
title: Lync Server 2013：tblLastChatId
description: Lync Server 2013： tblLastChatId。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastChatId
ms:assetid: 17a4ffbe-cca9-4ec5-ae46-38a15274889a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558616(v=OCS.15)
ms:contentKeyID: 48183513
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69e80a735e70c8a03441038f5e58eb93e0af1f82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444425"
---
# <a name="tbllastchatid-in-lync-server-2013"></a><span data-ttu-id="59f72-103">Lync Server 2013 中的 tblLastChatId</span><span class="sxs-lookup"><span data-stu-id="59f72-103">tblLastChatId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="59f72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="59f72-104">

<span> </span></span></span>

<span data-ttu-id="59f72-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="59f72-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="59f72-106">tblLastChatId 包含在 tblChat) 表中为每个用户生成 (和使用的最后一个聊天 ID。</span><span class="sxs-lookup"><span data-stu-id="59f72-106">tblLastChatId contains the last chat ID that was generated (and used in the tblChat table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="59f72-107">多</span><span class="sxs-lookup"><span data-stu-id="59f72-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59f72-108">列</span><span class="sxs-lookup"><span data-stu-id="59f72-108">Column</span></span></th>
<th><span data-ttu-id="59f72-109">类型</span><span class="sxs-lookup"><span data-stu-id="59f72-109">Type</span></span></th>
<th><span data-ttu-id="59f72-110">说明</span><span class="sxs-lookup"><span data-stu-id="59f72-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59f72-111">a</span><span class="sxs-lookup"><span data-stu-id="59f72-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="59f72-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="59f72-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="59f72-113"> (聊天室的节点 ID-仅键入) 。</span><span class="sxs-lookup"><span data-stu-id="59f72-113">Node ID (chat room-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59f72-114">lastChatID</span><span class="sxs-lookup"><span data-stu-id="59f72-114">lastChatID</span></span></p></td>
<td><p><span data-ttu-id="59f72-115">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="59f72-115">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="59f72-116">上次使用的聊天 ID。</span><span class="sxs-lookup"><span data-stu-id="59f72-116">Last used chat ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="59f72-117">标示</span><span class="sxs-lookup"><span data-stu-id="59f72-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59f72-118">列</span><span class="sxs-lookup"><span data-stu-id="59f72-118">Column</span></span></th>
<th><span data-ttu-id="59f72-119">说明</span><span class="sxs-lookup"><span data-stu-id="59f72-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59f72-120">&lt;lastChatID&gt;</span><span class="sxs-lookup"><span data-stu-id="59f72-120">&lt;nodeID, lastChatID&gt;</span></span></p></td>
<td><p><span data-ttu-id="59f72-121">主键 (只有一个参数就足以处理) 。</span><span class="sxs-lookup"><span data-stu-id="59f72-121">Primary key (just nodeID is sufficient for processing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59f72-122">a</span><span class="sxs-lookup"><span data-stu-id="59f72-122">nodeID</span></span></p></td>
<td><p><span data-ttu-id="59f72-123">带有 tblNode 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="59f72-123">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="59f72-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="59f72-124">See Also</span></span>


[<span data-ttu-id="59f72-125">Lync Server 2013 中的 tblChat</span><span class="sxs-lookup"><span data-stu-id="59f72-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)  
  

<span data-ttu-id="59f72-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="59f72-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

