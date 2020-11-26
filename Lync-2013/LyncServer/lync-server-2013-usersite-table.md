---
title: Lync Server 2013：UserSite 表
description: Lync Server 2013： UserSite 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserSite table
ms:assetid: 1c2a3cf2-dc05-472e-8097-a31f3a1aafcb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398256(v=OCS.15)
ms:contentKeyID: 48183552
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e0fb3149b9378bbfd3f14da8176eed226e4f57f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436109"
---
# <a name="usersite-table-in-lync-server-2013"></a><span data-ttu-id="f87c2-103">Lync Server 2013 中的 UserSite 表</span><span class="sxs-lookup"><span data-stu-id="f87c2-103">UserSite table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f87c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f87c2-104">

<span> </span></span></span>

<span data-ttu-id="f87c2-105">_**主题上次修改时间：** 2010-11-09_</span><span class="sxs-lookup"><span data-stu-id="f87c2-105">_**Topic Last Modified:** 2010-11-09_</span></span>

<span data-ttu-id="f87c2-106">UserSite 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="f87c2-106">The UserSite table is a supporting table.</span></span> <span data-ttu-id="f87c2-107">每条记录表示网络配置设置中定义的一个用户网站。</span><span class="sxs-lookup"><span data-stu-id="f87c2-107">Each record represents one user site defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f87c2-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="f87c2-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="f87c2-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="f87c2-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="f87c2-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="f87c2-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="f87c2-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="f87c2-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f87c2-112"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="f87c2-112"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f87c2-113">int</span><span class="sxs-lookup"><span data-stu-id="f87c2-113">int</span></span></p></td>
<td><p><span data-ttu-id="f87c2-114">Primary</span><span class="sxs-lookup"><span data-stu-id="f87c2-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="f87c2-115">标识用户网站的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="f87c2-115">Unique number identifying the user site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f87c2-116"><strong>UserSiteName</strong></span><span class="sxs-lookup"><span data-stu-id="f87c2-116"><strong>UserSiteName</strong></span></span></p></td>
<td><p><span data-ttu-id="f87c2-117">nvarchar (128) </span><span class="sxs-lookup"><span data-stu-id="f87c2-117">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="f87c2-118">唯一</span><span class="sxs-lookup"><span data-stu-id="f87c2-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="f87c2-119">用户网站的名称。</span><span class="sxs-lookup"><span data-stu-id="f87c2-119">User site’s name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f87c2-120"><strong>RegionKey</strong></span><span class="sxs-lookup"><span data-stu-id="f87c2-120"><strong>RegionKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f87c2-121">int</span><span class="sxs-lookup"><span data-stu-id="f87c2-121">int</span></span></p></td>
<td><p><span data-ttu-id="f87c2-122">外表</span><span class="sxs-lookup"><span data-stu-id="f87c2-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f87c2-123">从 <a href="lync-server-2013-region-table.md">Lync Server 2013 中的区域表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="f87c2-123">Referenced from <a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f87c2-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f87c2-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

