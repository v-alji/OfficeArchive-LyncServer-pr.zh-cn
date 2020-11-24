---
title: Lync Server 2013：Subnet 表
description: Lync Server 2013：子网表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Subnet table
ms:assetid: 76f5c995-96c8-4aa3-bc30-1d74991d7c42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398582(v=OCS.15)
ms:contentKeyID: 48184544
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30c04ddf897e0a62551709b30211ba724a75cbf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391810"
---
# <a name="subnet-table-in-lync-server-2013"></a><span data-ttu-id="aa0f3-103">Lync Server 2013 中的 Subnet 表</span><span class="sxs-lookup"><span data-stu-id="aa0f3-103">Subnet table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aa0f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aa0f3-104">

<span> </span></span></span>

<span data-ttu-id="aa0f3-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="aa0f3-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="aa0f3-106">子网表是支持表。</span><span class="sxs-lookup"><span data-stu-id="aa0f3-106">The Subnet table is a supporting table.</span></span> <span data-ttu-id="aa0f3-107">每条记录表示网络配置设置中定义的一个子网。</span><span class="sxs-lookup"><span data-stu-id="aa0f3-107">Each record represents one subnet defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa0f3-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="aa0f3-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="aa0f3-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="aa0f3-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa0f3-112"><strong>SubnetIP</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-112"><strong>SubnetIP</strong></span></span></p></td>
<td><p><span data-ttu-id="aa0f3-113">int</span><span class="sxs-lookup"><span data-stu-id="aa0f3-113">int</span></span></p></td>
<td><p><span data-ttu-id="aa0f3-114">主、外部</span><span class="sxs-lookup"><span data-stu-id="aa0f3-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="aa0f3-115">子网 IP 的整数表示形式。</span><span class="sxs-lookup"><span data-stu-id="aa0f3-115">Integer representation for the subnet IP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa0f3-116"><strong>SubnetMask</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-116"><strong>SubnetMask</strong></span></span></p></td>
<td><p><span data-ttu-id="aa0f3-117">int</span><span class="sxs-lookup"><span data-stu-id="aa0f3-117">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="aa0f3-118">子网掩码。</span><span class="sxs-lookup"><span data-stu-id="aa0f3-118">Subnet mask.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa0f3-119"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-119"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="aa0f3-120">int</span><span class="sxs-lookup"><span data-stu-id="aa0f3-120">int</span></span></p></td>
<td><p><span data-ttu-id="aa0f3-121">外表</span><span class="sxs-lookup"><span data-stu-id="aa0f3-121">Foreign</span></span></p></td>
<td><p><span data-ttu-id="aa0f3-122">从 <a href="lync-server-2013-usersite-table.md">Lync Server 2013 中的 UserSite 表</a>引用。</span><span class="sxs-lookup"><span data-stu-id="aa0f3-122">Referenced from the <a href="lync-server-2013-usersite-table.md">UserSite table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa0f3-123"><strong>SubnetDescription</strong></span><span class="sxs-lookup"><span data-stu-id="aa0f3-123"><strong>SubnetDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="aa0f3-124">nvarchar (512) </span><span class="sxs-lookup"><span data-stu-id="aa0f3-124">nvarchar(512)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="aa0f3-125">子网的说明。</span><span class="sxs-lookup"><span data-stu-id="aa0f3-125">The description for the subnet.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="aa0f3-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aa0f3-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

