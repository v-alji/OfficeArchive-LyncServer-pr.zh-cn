---
title: Lync Server 2013：tblLastInviteId
description: Lync Server 2013： tblLastInviteId。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblLastInviteId
ms:assetid: 222b3508-5963-4ddc-b4f3-e8412767e61b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558625(v=OCS.15)
ms:contentKeyID: 48183608
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5a13cfc7edc29ea20c95f7f4d587b0cfb84eb73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444418"
---
# <a name="tbllastinviteid-in-lync-server-2013"></a><span data-ttu-id="183e6-103">Lync Server 2013 中的 tblLastInviteId</span><span class="sxs-lookup"><span data-stu-id="183e6-103">tblLastInviteId in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="183e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="183e6-104">

<span> </span></span></span>

<span data-ttu-id="183e6-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="183e6-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="183e6-106">tblLastInviteId 包含在 tblPrincipalInvites) 表中为每个用户生成 (和使用的最后一个邀请 ID。</span><span class="sxs-lookup"><span data-stu-id="183e6-106">tblLastInviteId contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.</span></span>

### <a name="columns"></a><span data-ttu-id="183e6-107">多</span><span class="sxs-lookup"><span data-stu-id="183e6-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="183e6-108">列</span><span class="sxs-lookup"><span data-stu-id="183e6-108">Column</span></span></th>
<th><span data-ttu-id="183e6-109">类型</span><span class="sxs-lookup"><span data-stu-id="183e6-109">Type</span></span></th>
<th><span data-ttu-id="183e6-110">说明</span><span class="sxs-lookup"><span data-stu-id="183e6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="183e6-111">prinID</span><span class="sxs-lookup"><span data-stu-id="183e6-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="183e6-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="183e6-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="183e6-113">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="183e6-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="183e6-114">lastInviteID</span><span class="sxs-lookup"><span data-stu-id="183e6-114">lastInviteID</span></span></p></td>
<td><p><span data-ttu-id="183e6-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="183e6-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="183e6-116">上次使用的邀请 ID。</span><span class="sxs-lookup"><span data-stu-id="183e6-116">Last used invite ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="183e6-117">标示</span><span class="sxs-lookup"><span data-stu-id="183e6-117">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="183e6-118">列</span><span class="sxs-lookup"><span data-stu-id="183e6-118">Column</span></span></th>
<th><span data-ttu-id="183e6-119">说明</span><span class="sxs-lookup"><span data-stu-id="183e6-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="183e6-120">prinID</span><span class="sxs-lookup"><span data-stu-id="183e6-120">prinID</span></span></p></td>
<td><p><span data-ttu-id="183e6-121">主键。</span><span class="sxs-lookup"><span data-stu-id="183e6-121">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="183e6-122">prinID</span><span class="sxs-lookup"><span data-stu-id="183e6-122">prinID</span></span></p></td>
<td><p><span data-ttu-id="183e6-123">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="183e6-123">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="183e6-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="183e6-124">See Also</span></span>


[<span data-ttu-id="183e6-125">Lync Server 2013 中的 tblPrincipalInvites</span><span class="sxs-lookup"><span data-stu-id="183e6-125">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)  
  

<span data-ttu-id="183e6-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="183e6-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

