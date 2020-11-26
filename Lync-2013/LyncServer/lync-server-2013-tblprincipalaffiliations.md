---
title: Lync Server 2013：tblPrincipalAffiliations
description: Lync Server 2013： tblPrincipalAffiliations。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441366"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a><span data-ttu-id="f51c6-103">Lync Server 2013 中的 tblPrincipalAffiliations</span><span class="sxs-lookup"><span data-stu-id="f51c6-103">tblPrincipalAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f51c6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f51c6-104">

<span> </span></span></span>

<span data-ttu-id="f51c6-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="f51c6-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="f51c6-106">tblPrincipalAffiliations 包含描述位置中的成员身份的主体成员，包括 Active directory 域服务安全组，位于 Active Directory 容器中的域中。</span><span class="sxs-lookup"><span data-stu-id="f51c6-106">tblPrincipalAffiliations contains the principal affiliations that describe memberships in locations, including Active Directory Domain Services security groups, in Active Directory containers, in domains.</span></span>

### <a name="columns"></a><span data-ttu-id="f51c6-107">多</span><span class="sxs-lookup"><span data-stu-id="f51c6-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f51c6-108">列</span><span class="sxs-lookup"><span data-stu-id="f51c6-108">Column</span></span></th>
<th><span data-ttu-id="f51c6-109">类型</span><span class="sxs-lookup"><span data-stu-id="f51c6-109">Type</span></span></th>
<th><span data-ttu-id="f51c6-110">说明</span><span class="sxs-lookup"><span data-stu-id="f51c6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f51c6-111">principalID</span><span class="sxs-lookup"><span data-stu-id="f51c6-111">principalID</span></span></p></td>
<td><p><span data-ttu-id="f51c6-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="f51c6-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f51c6-113">关联主体的 ID。</span><span class="sxs-lookup"><span data-stu-id="f51c6-113">ID of the affiliated principal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f51c6-114">affiliationID</span><span class="sxs-lookup"><span data-stu-id="f51c6-114">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="f51c6-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="f51c6-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f51c6-116">表示隶属关系的承担者的 ID。</span><span class="sxs-lookup"><span data-stu-id="f51c6-116">ID of the principal representing the affiliation.</span></span> <span data-ttu-id="f51c6-117">除了系统用户类型外，每个主体 () 也具有自身附属关系。</span><span class="sxs-lookup"><span data-stu-id="f51c6-117">Each principal (except system-user-types) has a self-affiliation as well.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f51c6-118">食指</span><span class="sxs-lookup"><span data-stu-id="f51c6-118">index</span></span></p></td>
<td><p><span data-ttu-id="f51c6-119">int，not null</span><span class="sxs-lookup"><span data-stu-id="f51c6-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f51c6-120">食指.</span><span class="sxs-lookup"><span data-stu-id="f51c6-120">Index.</span></span> <span data-ttu-id="f51c6-121">自隶属关系的值是-1，对于其他隶属关系，在每个 &lt; principalID、affiliationId 存储桶中，它将按从1开始递增 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="f51c6-121">The value for self-affiliations is -1, and for the other affiliations it increases sequentially from 1 within each &lt;principalID, affiliationId&gt; bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f51c6-122">updatedBy</span><span class="sxs-lookup"><span data-stu-id="f51c6-122">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="f51c6-123">int，not null</span><span class="sxs-lookup"><span data-stu-id="f51c6-123">int, not null</span></span></p></td>
<td><p><span data-ttu-id="f51c6-124">已进行最新更新的主体。</span><span class="sxs-lookup"><span data-stu-id="f51c6-124">Principal that did the latest update.</span></span> <span data-ttu-id="f51c6-125">这通常是1，这意味着 Active Directory 同步。</span><span class="sxs-lookup"><span data-stu-id="f51c6-125">This is usually 1, which means Active Directory Sync.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="f51c6-126">标示</span><span class="sxs-lookup"><span data-stu-id="f51c6-126">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f51c6-127">多</span><span class="sxs-lookup"><span data-stu-id="f51c6-127">Columns</span></span></th>
<th><span data-ttu-id="f51c6-128">说明</span><span class="sxs-lookup"><span data-stu-id="f51c6-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f51c6-129">&lt;principalID、index、affiliationID&gt;</span><span class="sxs-lookup"><span data-stu-id="f51c6-129">&lt;principalID, index, affiliationID&gt;</span></span></p></td>
<td><p><span data-ttu-id="f51c6-130">主键。</span><span class="sxs-lookup"><span data-stu-id="f51c6-130">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f51c6-131">principalID</span><span class="sxs-lookup"><span data-stu-id="f51c6-131">principalID</span></span></p></td>
<td><p><span data-ttu-id="f51c6-132">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="f51c6-132">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f51c6-133">affiliationID</span><span class="sxs-lookup"><span data-stu-id="f51c6-133">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="f51c6-134">TblPrincipal 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="f51c6-134">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f51c6-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f51c6-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

