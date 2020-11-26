---
title: Lync Server 2013：Phones 表
description: Lync Server 2013：手机表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Phones table
ms:assetid: 41cb356d-9cc8-42b6-ac23-98a61b25aadc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425923(v=OCS.15)
ms:contentKeyID: 48183996
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c62fffecd2442b79aefde77eb037dca4bffc9d4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437110"
---
# <a name="phones-table-in-lync-server-2013"></a><span data-ttu-id="274b8-103">Lync Server 2013 中的 Phones 表</span><span class="sxs-lookup"><span data-stu-id="274b8-103">Phones table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="274b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="274b8-104">

<span> </span></span></span>

<span data-ttu-id="274b8-105">_**主题上次修改时间：** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="274b8-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="274b8-106">"电话" 表是支持表。</span><span class="sxs-lookup"><span data-stu-id="274b8-106">The Phones table is a supporting table.</span></span> <span data-ttu-id="274b8-107">表中的每条记录存储了在具有数据库中的记录的 VoIP 呼叫中涉及的一个电话号码的相关信息。</span><span class="sxs-lookup"><span data-stu-id="274b8-107">Each record in the table stores information about one phone number involved in VoIP calls that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="274b8-108">列</span><span class="sxs-lookup"><span data-stu-id="274b8-108">Column</span></span></th>
<th><span data-ttu-id="274b8-109">数据类型</span><span class="sxs-lookup"><span data-stu-id="274b8-109">Data Type</span></span></th>
<th><span data-ttu-id="274b8-110">键/索引</span><span class="sxs-lookup"><span data-stu-id="274b8-110">Key/Index</span></span></th>
<th><span data-ttu-id="274b8-111">详细信息</span><span class="sxs-lookup"><span data-stu-id="274b8-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="274b8-112"><strong>PhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="274b8-112"><strong>PhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="274b8-113">int</span><span class="sxs-lookup"><span data-stu-id="274b8-113">int</span></span></p></td>
<td><p><span data-ttu-id="274b8-114">Primary</span><span class="sxs-lookup"><span data-stu-id="274b8-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="274b8-115">标识此电话的唯一号码。</span><span class="sxs-lookup"><span data-stu-id="274b8-115">Unique number identifying this phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="274b8-116"><strong>PhoneUri</strong></span><span class="sxs-lookup"><span data-stu-id="274b8-116"><strong>PhoneUri</strong></span></span></p></td>
<td><p><span data-ttu-id="274b8-117">nvarchar (450) </span><span class="sxs-lookup"><span data-stu-id="274b8-117">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="274b8-118">电话号码。</span><span class="sxs-lookup"><span data-stu-id="274b8-118">Phone number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="274b8-119"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="274b8-119"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="274b8-120">从中</span><span class="sxs-lookup"><span data-stu-id="274b8-120">dateTime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="274b8-121">时间戳 (仅供内部使用) 。</span><span class="sxs-lookup"><span data-stu-id="274b8-121">Time stamp (for internal use only).</span></span></p>
<p><span data-ttu-id="274b8-122">此字段是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="274b8-122">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="274b8-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="274b8-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

