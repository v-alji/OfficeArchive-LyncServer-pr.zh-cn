---
title: Lync Server 2013： SIPResponseMetaData 表
description: Lync Server 2013： SIPResponseMetaData 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIPResponseMetaData table
ms:assetid: cf723737-4a75-4352-829b-f4954aa59716
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205294(v=OCS.15)
ms:contentKeyID: 48185510
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 402cff331f81a9b46028d76de69deeaace8d5ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444621"
---
# <a name="sipresponsemetadata-table-in-lync-server-2013"></a><span data-ttu-id="31a19-103">Lync Server 2013 中的 SIPResponseMetaData 表</span><span class="sxs-lookup"><span data-stu-id="31a19-103">SIPResponseMetaData table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31a19-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31a19-104">

<span> </span></span></span>

<span data-ttu-id="31a19-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="31a19-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="31a19-106">SIPResponseMetaDataTable 包含 SIP 响应代码列表以及每个代码的分类和定义。</span><span class="sxs-lookup"><span data-stu-id="31a19-106">The SIPResponseMetaDataTable contains a list of SIP response codes and the classification and definition of each of those codes.</span></span> <span data-ttu-id="31a19-107">系统会生成这些代码，以响应影响 SIP 设备和 SIP 通信会话的事件;例如，在 SIP 设备发出请求时，将生成响应代码403，但服务器拒绝接受该请求。</span><span class="sxs-lookup"><span data-stu-id="31a19-107">These codes are generated in response to events affecting SIP devices and SIP communication sessions; for example, the response code 403 is generated when a SIP device makes a request, but the server declines to honor that request.</span></span>

<span data-ttu-id="31a19-108">此表是在 Microsoft Lync Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="31a19-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31a19-109">列</span><span class="sxs-lookup"><span data-stu-id="31a19-109">Column</span></span></th>
<th><span data-ttu-id="31a19-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="31a19-110">Data Type</span></span></th>
<th><span data-ttu-id="31a19-111">键/索引</span><span class="sxs-lookup"><span data-stu-id="31a19-111">Key/Index</span></span></th>
<th><span data-ttu-id="31a19-112">详细信息</span><span class="sxs-lookup"><span data-stu-id="31a19-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31a19-113"><strong>ResponseCode</strong></span><span class="sxs-lookup"><span data-stu-id="31a19-113"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="31a19-114">int</span><span class="sxs-lookup"><span data-stu-id="31a19-114">int</span></span></p></td>
<td><p><span data-ttu-id="31a19-115">Primary</span><span class="sxs-lookup"><span data-stu-id="31a19-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="31a19-116">表示 SIP 响应代码的数值。</span><span class="sxs-lookup"><span data-stu-id="31a19-116">Numeric value that represents the SIP response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31a19-117"><strong>种类</strong></span><span class="sxs-lookup"><span data-stu-id="31a19-117"><strong>Class</strong></span></span></p></td>
<td><p><span data-ttu-id="31a19-118">int</span><span class="sxs-lookup"><span data-stu-id="31a19-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31a19-119">响应代码的常规分类。</span><span class="sxs-lookup"><span data-stu-id="31a19-119">General classification for the response code.</span></span> <span data-ttu-id="31a19-120">分类包括：</span><span class="sxs-lookup"><span data-stu-id="31a19-120">Classifications include:</span></span></p>
<ul>
<li><p><span data-ttu-id="31a19-121">1-信息答复</span><span class="sxs-lookup"><span data-stu-id="31a19-121">1 – Informational Responses</span></span></p></li>
<li><p><span data-ttu-id="31a19-122">2–成功的答复</span><span class="sxs-lookup"><span data-stu-id="31a19-122">2 – Successful Responses</span></span></p></li>
<li><p><span data-ttu-id="31a19-123">3-重定向响应</span><span class="sxs-lookup"><span data-stu-id="31a19-123">3 – Redirection Responses</span></span></p></li>
<li><p><span data-ttu-id="31a19-124">4-客户端故障响应</span><span class="sxs-lookup"><span data-stu-id="31a19-124">4 – Client Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="31a19-125">5--服务器故障响应</span><span class="sxs-lookup"><span data-stu-id="31a19-125">5 -- Server Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="31a19-126">6-全球故障回复</span><span class="sxs-lookup"><span data-stu-id="31a19-126">6 – Global Failure Response</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31a19-127"><strong>说明</strong></span><span class="sxs-lookup"><span data-stu-id="31a19-127"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="31a19-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="31a19-128">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="31a19-129">SIP 响应代码的说明。</span><span class="sxs-lookup"><span data-stu-id="31a19-129">Description of the SIP response code.</span></span> <span data-ttu-id="31a19-130">例如，响应代码181具有以下说明：</span><span class="sxs-lookup"><span data-stu-id="31a19-130">For example, response code 181 has the following description:</span></span></p>
<p><span data-ttu-id="31a19-131">正在转发呼叫</span><span class="sxs-lookup"><span data-stu-id="31a19-131">Call Is Being Forwarded</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="31a19-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31a19-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

