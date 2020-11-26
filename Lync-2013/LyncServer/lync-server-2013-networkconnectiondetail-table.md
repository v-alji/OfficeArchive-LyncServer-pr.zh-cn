---
title: Lync Server 2013： NetworkConnectionDetail 表
description: Lync Server 2013： NetworkConnectionDetail 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: NetworkConnectionDetail table
ms:assetid: b48cc9a6-5232-48b5-bd20-53b68229336b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205185(v=OCS.15)
ms:contentKeyID: 48185170
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dcd0f429999b6629826a9f9369d154afe3c1af2f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445489"
---
# <a name="networkconnectiondetail-table-in-lync-server-2013"></a><span data-ttu-id="f34ab-103">Lync Server 2013 中的 NetworkConnectionDetail 表</span><span class="sxs-lookup"><span data-stu-id="f34ab-103">NetworkConnectionDetail table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f34ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f34ab-104">

<span> </span></span></span>

<span data-ttu-id="f34ab-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="f34ab-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="f34ab-106">NetworkConnectionDetail 表将网络连接类型映射到 "体验质量" 数据库中其他位置使用的网络连接标识符。</span><span class="sxs-lookup"><span data-stu-id="f34ab-106">The NetworkConnectionDetail table maps network connection types to the network connection identifiers used elsewhere in the Quality of Experience database.</span></span> <span data-ttu-id="f34ab-107">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="f34ab-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f34ab-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="f34ab-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="f34ab-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="f34ab-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="f34ab-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="f34ab-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="f34ab-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="f34ab-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f34ab-112"><strong>NetworkConnectionDetailKey</strong></span><span class="sxs-lookup"><span data-stu-id="f34ab-112"><strong>NetworkConnectionDetailKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f34ab-113">tinyint</span><span class="sxs-lookup"><span data-stu-id="f34ab-113">tinyint</span></span></p></td>
<td><p><span data-ttu-id="f34ab-114">Primary</span><span class="sxs-lookup"><span data-stu-id="f34ab-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="f34ab-115">网络连接类型的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f34ab-115">Unique identifier for the network connection type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f34ab-116"><strong>NetworkConnectionDetail</strong></span><span class="sxs-lookup"><span data-stu-id="f34ab-116"><strong>NetworkConnectionDetail</strong></span></span></p></td>
<td><p><span data-ttu-id="f34ab-117">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="f34ab-117">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="f34ab-118">唯一</span><span class="sxs-lookup"><span data-stu-id="f34ab-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="f34ab-119">与 NetworkConnectionDetailKey 对应的网络连接类型。</span><span class="sxs-lookup"><span data-stu-id="f34ab-119">Network connection type that corresponds to the NetworkConnectionDetailKey.</span></span> <span data-ttu-id="f34ab-120">允许的值包括：</span><span class="sxs-lookup"><span data-stu-id="f34ab-120">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="f34ab-121">0--有线</span><span class="sxs-lookup"><span data-stu-id="f34ab-121">0 -- Wired</span></span></p></li>
<li><p><span data-ttu-id="f34ab-122">1--WiFi</span><span class="sxs-lookup"><span data-stu-id="f34ab-122">1 -- WiFi</span></span></p></li>
<li><p><span data-ttu-id="f34ab-123">2--以太网</span><span class="sxs-lookup"><span data-stu-id="f34ab-123">2 -- Ethernet</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="f34ab-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f34ab-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

