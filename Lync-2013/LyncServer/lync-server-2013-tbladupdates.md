---
title: Lync Server 2013：tblADUpdates
description: Lync Server 2013： tblADUpdates。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADUpdates
ms:assetid: ba19fa16-4d2d-4635-ac32-f93e09469546
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615033(v=OCS.15)
ms:contentKeyID: 48185227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ab4418a10eac283d0f39d09b1c1fe15a32b2e68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444481"
---
# <a name="tbladupdates-in-lync-server-2013"></a><span data-ttu-id="6a062-103">Lync Server 2013 中的 tblADUpdates</span><span class="sxs-lookup"><span data-stu-id="6a062-103">tblADUpdates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a062-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a062-104">

<span> </span></span></span>

<span data-ttu-id="6a062-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="6a062-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="6a062-106">tblADUpdates 包含后续 Active Directory 同步步骤尚未处理的 Active Directory 域服务更改。</span><span class="sxs-lookup"><span data-stu-id="6a062-106">tblADUpdates contains Active Directory Domain Services changes that have not yet been processed by the later Active Directory Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="6a062-107">多</span><span class="sxs-lookup"><span data-stu-id="6a062-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a062-108">列</span><span class="sxs-lookup"><span data-stu-id="6a062-108">Column</span></span></th>
<th><span data-ttu-id="6a062-109">类型</span><span class="sxs-lookup"><span data-stu-id="6a062-109">Type</span></span></th>
<th><span data-ttu-id="6a062-110">说明</span><span class="sxs-lookup"><span data-stu-id="6a062-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a062-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="6a062-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="6a062-112">GUID，not null</span><span class="sxs-lookup"><span data-stu-id="6a062-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="6a062-113">已更改对象的主体 GUID。</span><span class="sxs-lookup"><span data-stu-id="6a062-113">Principal GUID of the object that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a062-114">prinADPath</span><span class="sxs-lookup"><span data-stu-id="6a062-114">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="6a062-115">nvarchar (384) ，not null</span><span class="sxs-lookup"><span data-stu-id="6a062-115">nvarchar (384), not null</span></span></p></td>
<td><p><span data-ttu-id="6a062-116">对象的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="6a062-116">Distinguished name of the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a062-117">prinAttributesChanged</span><span class="sxs-lookup"><span data-stu-id="6a062-117">prinAttributesChanged</span></span></p></td>
<td><p><span data-ttu-id="6a062-118">位，not null</span><span class="sxs-lookup"><span data-stu-id="6a062-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="6a062-119">如果对象的至少一个属性发生更改，则为 True。</span><span class="sxs-lookup"><span data-stu-id="6a062-119">True if at least one attribute of the object changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a062-120">prinMembersChanged</span><span class="sxs-lookup"><span data-stu-id="6a062-120">prinMembersChanged</span></span></p></td>
<td><p><span data-ttu-id="6a062-121">位，not null</span><span class="sxs-lookup"><span data-stu-id="6a062-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="6a062-122">如果成员身份已更改，则为 True。</span><span class="sxs-lookup"><span data-stu-id="6a062-122">True if the membership changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a062-123">prinAffiliationsChanged</span><span class="sxs-lookup"><span data-stu-id="6a062-123">prinAffiliationsChanged</span></span></p></td>
<td><p><span data-ttu-id="6a062-124">位，not null</span><span class="sxs-lookup"><span data-stu-id="6a062-124">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="6a062-125">未使用。</span><span class="sxs-lookup"><span data-stu-id="6a062-125">Not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a062-126">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="6a062-126">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="6a062-127">位，not null</span><span class="sxs-lookup"><span data-stu-id="6a062-127">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="6a062-128">如果对象已删除，则为 True。</span><span class="sxs-lookup"><span data-stu-id="6a062-128">True if the object was deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a062-129">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="6a062-129">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="6a062-130">datetime，not null</span><span class="sxs-lookup"><span data-stu-id="6a062-130">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="6a062-131">插入行的时间戳。</span><span class="sxs-lookup"><span data-stu-id="6a062-131">Time stamp of when the row was inserted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6a062-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a062-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

