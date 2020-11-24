---
title: Lync Server 2013：Locations 表
description: Lync Server 2013：位置表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392379"
---
# <a name="locations-table-in-lync-server-2013"></a><span data-ttu-id="fc390-103">Lync Server 2013 中的 Locations 表</span><span class="sxs-lookup"><span data-stu-id="fc390-103">Locations table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc390-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc390-104">

<span> </span></span></span>

<span data-ttu-id="fc390-105">_**主题上次修改时间：** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="fc390-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="fc390-106">每条记录代表紧急呼叫中的一个位置引用，如 E9-1-1 通话。</span><span class="sxs-lookup"><span data-stu-id="fc390-106">Each record represents one location reference in an emergency call, like an E9-1-1 call.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc390-107">列</span><span class="sxs-lookup"><span data-stu-id="fc390-107">Column</span></span></th>
<th><span data-ttu-id="fc390-108">数据类型</span><span class="sxs-lookup"><span data-stu-id="fc390-108">Data Type</span></span></th>
<th><span data-ttu-id="fc390-109">键/索引</span><span class="sxs-lookup"><span data-stu-id="fc390-109">Key/Index</span></span></th>
<th><span data-ttu-id="fc390-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="fc390-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc390-111"><strong>SessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="fc390-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fc390-112">datetime</span><span class="sxs-lookup"><span data-stu-id="fc390-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="fc390-113">主、外部</span><span class="sxs-lookup"><span data-stu-id="fc390-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="fc390-114">会话请求的时间。</span><span class="sxs-lookup"><span data-stu-id="fc390-114">Time of session request.</span></span> <span data-ttu-id="fc390-115">与 <strong>SessionIdSeq</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="fc390-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="fc390-116">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="fc390-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc390-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="fc390-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="fc390-118">int</span><span class="sxs-lookup"><span data-stu-id="fc390-118">int</span></span></p></td>
<td><p><span data-ttu-id="fc390-119">主、外部</span><span class="sxs-lookup"><span data-stu-id="fc390-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="fc390-120">标识会话的 ID 号。</span><span class="sxs-lookup"><span data-stu-id="fc390-120">ID number to identify the session.</span></span> <span data-ttu-id="fc390-121">与 <strong>SessionIdTime</strong> 结合使用以唯一标识会话。</span><span class="sxs-lookup"><span data-stu-id="fc390-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="fc390-122">有关详细信息，请参阅 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 中的对话框表</a> 。</span><span class="sxs-lookup"><span data-stu-id="fc390-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc390-123"><strong>位置</strong></span><span class="sxs-lookup"><span data-stu-id="fc390-123"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="fc390-124">nvarchar (max) </span><span class="sxs-lookup"><span data-stu-id="fc390-124">nvarchar(max)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="fc390-125">紧急电话的位置。</span><span class="sxs-lookup"><span data-stu-id="fc390-125">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fc390-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc390-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

