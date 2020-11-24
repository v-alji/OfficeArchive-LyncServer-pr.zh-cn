---
title: Lync Server 2013：UriTypes 表
description: Lync Server 2013： UriTypes 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UriTypes table
ms:assetid: 77c4dfae-1b29-4e81-ba05-609e61643998
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398587(v=OCS.15)
ms:contentKeyID: 48184553
ms.date: 06/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 97a63173b7ada258e7da22591b28a6a0410e666a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392250"
---
# <a name="uritypes-table-in-lync-server-2013"></a><span data-ttu-id="6bdcf-103">Lync Server 2013 中的 UriTypes 表</span><span class="sxs-lookup"><span data-stu-id="6bdcf-103">UriTypes table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bdcf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bdcf-104">

<span> </span></span></span>

<span data-ttu-id="6bdcf-105">_**主题上次修改时间：** 2015-06-16_</span><span class="sxs-lookup"><span data-stu-id="6bdcf-105">_**Topic Last Modified:** 2015-06-16_</span></span>

<span data-ttu-id="6bdcf-106">UriTypes 表包含在 Microsoft Lync Server 2013 中监视的不同 URI (统一资源标识符) 类型。</span><span class="sxs-lookup"><span data-stu-id="6bdcf-106">The UriTypes Table contains the different URI (Uniform resource identifier) types monitored in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bdcf-107">列</span><span class="sxs-lookup"><span data-stu-id="6bdcf-107">Column</span></span></th>
<th><span data-ttu-id="6bdcf-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="6bdcf-108">Data Type</span></span></th>
<th><span data-ttu-id="6bdcf-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="6bdcf-109">Key/Index</span></span></th>
<th><span data-ttu-id="6bdcf-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="6bdcf-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bdcf-111"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="6bdcf-111"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="6bdcf-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="6bdcf-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="6bdcf-113">Primary</span><span class="sxs-lookup"><span data-stu-id="6bdcf-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="6bdcf-114">分配给 URI 类型的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="6bdcf-114">Unique identifier assigned to a URI type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bdcf-115"><strong>UriType</strong></span><span class="sxs-lookup"><span data-stu-id="6bdcf-115"><strong>UriType</strong></span></span></p></td>
<td><p><span data-ttu-id="6bdcf-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="6bdcf-116">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6bdcf-117">不同 URI 类型的说明。</span><span class="sxs-lookup"><span data-stu-id="6bdcf-117">Descriptions of the different URI types.</span></span> <span data-ttu-id="6bdcf-118">允许的值包括：</span><span class="sxs-lookup"><span data-stu-id="6bdcf-118">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="6bdcf-119">1–电话 Uri</span><span class="sxs-lookup"><span data-stu-id="6bdcf-119">1 – Phone Uri</span></span></p></li>
<li><p><span data-ttu-id="6bdcf-120">0-用户 Uri</span><span class="sxs-lookup"><span data-stu-id="6bdcf-120">0 – User Uri</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="6bdcf-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bdcf-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

