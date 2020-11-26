---
title: Lync Server 2013：Roles 表
description: Lync Server 2013： Roles 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Roles table
ms:assetid: e8eb8a10-26b5-488b-bc8c-f9ef93f98bdb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399043(v=OCS.15)
ms:contentKeyID: 48185893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d16f9483fc97145d82faf7e8f1175772f10f9a4b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442353"
---
# <a name="roles-table-in-lync-server-2013"></a><span data-ttu-id="b2b11-103">Lync Server 2013 中的 Roles 表</span><span class="sxs-lookup"><span data-stu-id="b2b11-103">Roles table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2b11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2b11-104">

<span> </span></span></span>

<span data-ttu-id="b2b11-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b2b11-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b2b11-106">Roles 表是一个静态表，它存储了可能的会议角色（如与会者和演示者）的列表。</span><span class="sxs-lookup"><span data-stu-id="b2b11-106">The Roles table is a static table that stores the list of possible conference roles, such as attendee and presenter.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2b11-107">列</span><span class="sxs-lookup"><span data-stu-id="b2b11-107">Column</span></span></th>
<th><span data-ttu-id="b2b11-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="b2b11-108">Data Type</span></span></th>
<th><span data-ttu-id="b2b11-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="b2b11-109">Key/Index</span></span></th>
<th><span data-ttu-id="b2b11-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="b2b11-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2b11-111"><strong>RoleId</strong></span><span class="sxs-lookup"><span data-stu-id="b2b11-111"><strong>RoleId</strong></span></span></p></td>
<td><p><span data-ttu-id="b2b11-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="b2b11-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b2b11-113">Primary</span><span class="sxs-lookup"><span data-stu-id="b2b11-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2b11-114"><strong>角色</strong></span><span class="sxs-lookup"><span data-stu-id="b2b11-114"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="b2b11-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b2b11-115">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b2b11-116">允许的值：</span><span class="sxs-lookup"><span data-stu-id="b2b11-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="b2b11-117">0-未知</span><span class="sxs-lookup"><span data-stu-id="b2b11-117">0 - Unknown</span></span></p></li>
<li><p><span data-ttu-id="b2b11-118">1-演示者</span><span class="sxs-lookup"><span data-stu-id="b2b11-118">1 - Presenter</span></span></p></li>
<li><p><span data-ttu-id="b2b11-119">2-与会者</span><span class="sxs-lookup"><span data-stu-id="b2b11-119">2 - Attendee</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="b2b11-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2b11-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

