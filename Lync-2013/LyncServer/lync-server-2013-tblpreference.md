---
title: Lync Server 2013：tblPreference
description: Lync Server 2013： tblPreference。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPreference
ms:assetid: f94eb128-f782-42ff-a568-ed3529573bc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615052(v=OCS.15)
ms:contentKeyID: 48185913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86e8b81a6af93e9bf1d7673e54492579a1bed08e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441373"
---
# <a name="tblpreference-in-lync-server-2013"></a><span data-ttu-id="8e48f-103">Lync Server 2013 中的 tblPreference</span><span class="sxs-lookup"><span data-stu-id="8e48f-103">tblPreference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e48f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e48f-104">

<span> </span></span></span>

<span data-ttu-id="8e48f-105">_**主题上次修改时间：** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="8e48f-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="8e48f-106">tblPreference 包含用户的客户端首选项。</span><span class="sxs-lookup"><span data-stu-id="8e48f-106">tblPreference contains the users’ client preferences.</span></span> <span data-ttu-id="8e48f-107">这通常由 Lync 2013 之前的客户端使用。</span><span class="sxs-lookup"><span data-stu-id="8e48f-107">This is generally used by clients previous to Lync 2013.</span></span>

### <a name="columns"></a><span data-ttu-id="8e48f-108">多</span><span class="sxs-lookup"><span data-stu-id="8e48f-108">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e48f-109">列</span><span class="sxs-lookup"><span data-stu-id="8e48f-109">Column</span></span></th>
<th><span data-ttu-id="8e48f-110">类型</span><span class="sxs-lookup"><span data-stu-id="8e48f-110">Type</span></span></th>
<th><span data-ttu-id="8e48f-111">说明</span><span class="sxs-lookup"><span data-stu-id="8e48f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e48f-112">prefLabel</span><span class="sxs-lookup"><span data-stu-id="8e48f-112">prefLabel</span></span></p></td>
<td><p><span data-ttu-id="8e48f-113">nvarchar (255) ，not null</span><span class="sxs-lookup"><span data-stu-id="8e48f-113">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="8e48f-114">带格式的标签，如： &lt; 用户 sip uri &gt; | 用户名。 &lt;首选项集 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="8e48f-114">Label with a format such as: &lt;user sip uri&gt;|username.&lt;preference set&gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e48f-115">prefSeqID</span><span class="sxs-lookup"><span data-stu-id="8e48f-115">prefSeqID</span></span></p></td>
<td><p><span data-ttu-id="8e48f-116">int，not null</span><span class="sxs-lookup"><span data-stu-id="8e48f-116">int, not null</span></span></p></td>
<td><p><span data-ttu-id="8e48f-117">用于进行版本控制)  (每个标签的序列号。</span><span class="sxs-lookup"><span data-stu-id="8e48f-117">A sequential number (per label) for versioning purposes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e48f-118">prefContent</span><span class="sxs-lookup"><span data-stu-id="8e48f-118">prefContent</span></span></p></td>
<td><p><span data-ttu-id="8e48f-119">nvarchar (max) </span><span class="sxs-lookup"><span data-stu-id="8e48f-119">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="8e48f-120">编码内容。</span><span class="sxs-lookup"><span data-stu-id="8e48f-120">Encoded content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e48f-121">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="8e48f-121">lastModifiedBy</span></span></p></td>
<td><p><span data-ttu-id="8e48f-122">int，not null</span><span class="sxs-lookup"><span data-stu-id="8e48f-122">int, not null</span></span></p></td>
<td><p><span data-ttu-id="8e48f-123">已更新首选项的主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="8e48f-123">ID of the principal that updated the preference.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="8e48f-124">密钥</span><span class="sxs-lookup"><span data-stu-id="8e48f-124">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e48f-125">列</span><span class="sxs-lookup"><span data-stu-id="8e48f-125">Column</span></span></th>
<th><span data-ttu-id="8e48f-126">说明</span><span class="sxs-lookup"><span data-stu-id="8e48f-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e48f-127">&lt;prefLabel, prefSeqID&gt;</span><span class="sxs-lookup"><span data-stu-id="8e48f-127">&lt;prefLabel, prefSeqID&gt;</span></span></p></td>
<td><p><span data-ttu-id="8e48f-128">主键。</span><span class="sxs-lookup"><span data-stu-id="8e48f-128">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8e48f-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e48f-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

