---
title: Lync Server 2013：EndpointSubnet 表
description: Lync Server 2013： EndpointSubnet 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: EndpointSubnet table
ms:assetid: d62e51d6-2117-4c41-adce-08f8d9d75ce0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398933(v=OCS.15)
ms:contentKeyID: 48185514
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63e7d3c908a55ae866ed8e330cc8742b9f6a0096
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428662"
---
# <a name="endpointsubnet-table-in-lync-server-2013"></a><span data-ttu-id="9a84a-103">Lync Server 2013 中的 EndpointSubnet 表</span><span class="sxs-lookup"><span data-stu-id="9a84a-103">EndpointSubnet table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a84a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a84a-104">

<span> </span></span></span>

<span data-ttu-id="9a84a-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="9a84a-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="9a84a-106">EndpointSubnet 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="9a84a-106">The EndpointSubnet table is a supporting table.</span></span> <span data-ttu-id="9a84a-107">每条记录表示一个从终结点捕获的子网。</span><span class="sxs-lookup"><span data-stu-id="9a84a-107">Each record represents one subnet captured from endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a84a-108"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="9a84a-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="9a84a-109"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="9a84a-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="9a84a-110"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="9a84a-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="9a84a-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="9a84a-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a84a-112"><strong>SubnetIP</strong></span><span class="sxs-lookup"><span data-stu-id="9a84a-112"><strong>SubnetIP</strong></span></span></p></td>
<td><p><span data-ttu-id="9a84a-113">int</span><span class="sxs-lookup"><span data-stu-id="9a84a-113">int</span></span></p></td>
<td><p><span data-ttu-id="9a84a-114">主、外部</span><span class="sxs-lookup"><span data-stu-id="9a84a-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="9a84a-115">子网的整数表示形式。</span><span class="sxs-lookup"><span data-stu-id="9a84a-115">Integer representation for the subnet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a84a-116"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="9a84a-116"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="9a84a-117">datetime</span><span class="sxs-lookup"><span data-stu-id="9a84a-117">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="9a84a-118">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="9a84a-118">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9a84a-119">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a84a-119">


</div>

<span> </span>

</div>

</div>

</span></span></div>

