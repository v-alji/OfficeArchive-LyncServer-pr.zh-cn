---
title: Lync Server 2013：DeRegisterType 表
description: Lync Server 2013： DeRegisterType 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DeRegisterType table
ms:assetid: 09148118-6209-4fd7-a494-99118689a245
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398142(v=OCS.15)
ms:contentKeyID: 48183346
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afad63c2abeba3e91565e07dac75d0ac6c96ca3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429557"
---
# <a name="deregistertype-table-in-lync-server-2013"></a><span data-ttu-id="f47f3-103">Lync Server 2013 中的 DeRegisterType 表</span><span class="sxs-lookup"><span data-stu-id="f47f3-103">DeRegisterType table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f47f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f47f3-104">

<span> </span></span></span>

<span data-ttu-id="f47f3-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f47f3-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f47f3-106">DeRegisterType 表是一个静态表，用于存储可能的用户取消注册类型的列表，例如 "客户端启动"、"注册过期" 或 "客户端已停止响应"。</span><span class="sxs-lookup"><span data-stu-id="f47f3-106">The DeRegisterType table is a static table that stores the list of possible user de-registers types, such as ‘client initiated’, ‘registration expired’, or ‘client stopped responding.’</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f47f3-107">列</span><span class="sxs-lookup"><span data-stu-id="f47f3-107">Column</span></span></th>
<th><span data-ttu-id="f47f3-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="f47f3-108">Data Type</span></span></th>
<th><span data-ttu-id="f47f3-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="f47f3-109">Key/Index</span></span></th>
<th><span data-ttu-id="f47f3-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="f47f3-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f47f3-111"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="f47f3-111"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="f47f3-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="f47f3-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f47f3-113">Primary</span><span class="sxs-lookup"><span data-stu-id="f47f3-113">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f47f3-114"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="f47f3-114"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="f47f3-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="f47f3-115">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f47f3-116">允许的值：</span><span class="sxs-lookup"><span data-stu-id="f47f3-116">Allowed values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f47f3-117">0--未知</span><span class="sxs-lookup"><span data-stu-id="f47f3-117">0 -- Unknown</span></span></p></li>
<li><p><span data-ttu-id="f47f3-118">1--客户发起的取消注册</span><span class="sxs-lookup"><span data-stu-id="f47f3-118">1 -- Client Initiated Deregistration</span></span></p></li>
<li><p><span data-ttu-id="f47f3-119">2--注册已过期</span><span class="sxs-lookup"><span data-stu-id="f47f3-119">2 -- Registration Expired</span></span></p></li>
<li><p><span data-ttu-id="f47f3-120">3-客户端崩溃</span><span class="sxs-lookup"><span data-stu-id="f47f3-120">3 – Client crashed</span></span></p></li>
<li><p><span data-ttu-id="f47f3-121">4--用户属性已更改</span><span class="sxs-lookup"><span data-stu-id="f47f3-121">4 -- User Attributes Changed</span></span></p></li>
<li><p><span data-ttu-id="f47f3-122">5-首选注册机构已更改</span><span class="sxs-lookup"><span data-stu-id="f47f3-122">5 – Preferred Registrar Changed</span></span></p></li>
<li><p><span data-ttu-id="f47f3-123">6--处于生存模式的旧客户端</span><span class="sxs-lookup"><span data-stu-id="f47f3-123">6 -- Legacy Client In Survival Mode</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="f47f3-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f47f3-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

