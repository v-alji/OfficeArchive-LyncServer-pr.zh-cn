---
title: Lync Server 2013： IPAddress 表
description: Lync Server 2013： IPAddress 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPAddress table
ms:assetid: 8ec018b9-158e-4bbe-ad46-869e60315555
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205077(v=OCS.15)
ms:contentKeyID: 48184771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6d987281fc310a3a179fa99f2aae51b0764349dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392185"
---
# <a name="ipaddress-table-in-lync-server-2013"></a><span data-ttu-id="605d0-103">Lync Server 2013 中的 IPAddress 表</span><span class="sxs-lookup"><span data-stu-id="605d0-103">IPAddress table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="605d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="605d0-104">

<span> </span></span></span>

<span data-ttu-id="605d0-105">_**主题上次修改时间：** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="605d0-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="605d0-106">IPAddress 表将 IP 地址映射到 "体验质量" 数据库中其他位置使用的唯一 IP 地址标识符。</span><span class="sxs-lookup"><span data-stu-id="605d0-106">The IPAddress table maps IP addresses to the unique IP address identifiers used elsewhere in the Quality of Experience database.</span></span> <span data-ttu-id="605d0-107">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="605d0-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="605d0-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="605d0-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="605d0-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="605d0-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="605d0-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="605d0-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="605d0-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="605d0-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="605d0-112"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="605d0-112"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="605d0-113">int</span><span class="sxs-lookup"><span data-stu-id="605d0-113">int</span></span></p></td>
<td><p><span data-ttu-id="605d0-114">Primary</span><span class="sxs-lookup"><span data-stu-id="605d0-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="605d0-115">指定 IP 地址的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="605d0-115">Unique identifier for the specified IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="605d0-116"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="605d0-116"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="605d0-117">varchar(50)</span><span class="sxs-lookup"><span data-stu-id="605d0-117">varchar(50)</span></span></p></td>
<td><p><span data-ttu-id="605d0-118">唯一</span><span class="sxs-lookup"><span data-stu-id="605d0-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="605d0-119">唯一 IP 地址 (例如，映射到 IpAddressKey 的 189.168.1.1) 。</span><span class="sxs-lookup"><span data-stu-id="605d0-119">Unique IP address (for example, 189.168.1.1) that maps to the IpAddressKey.</span></span> <span data-ttu-id="605d0-120">这可能是 IPv4 地址或 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="605d0-120">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="605d0-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="605d0-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

