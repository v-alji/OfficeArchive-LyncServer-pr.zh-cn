---
title: Lync Server 2013：tblPrincipalMembers
description: Lync Server 2013： tblPrincipalMembers。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMembers
ms:assetid: 9a3e24cf-6ef7-4b82-99fc-50ba41800b6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615022(v=OCS.15)
ms:contentKeyID: 48184965
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8bbb8be0b83d09b1bd54ea98655558581e6df834
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391805"
---
# <a name="tblprincipalmembers-in-lync-server-2013"></a><span data-ttu-id="56626-103">Lync Server 2013 中的 tblPrincipalMembers</span><span class="sxs-lookup"><span data-stu-id="56626-103">tblPrincipalMembers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56626-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56626-104">

<span> </span></span></span>

<span data-ttu-id="56626-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="56626-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="56626-106">tblPrincipalMembers 包含主体成员身份。</span><span class="sxs-lookup"><span data-stu-id="56626-106">tblPrincipalMembers contains principal memberships.</span></span>

### <a name="columns"></a><span data-ttu-id="56626-107">多</span><span class="sxs-lookup"><span data-stu-id="56626-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56626-108">列</span><span class="sxs-lookup"><span data-stu-id="56626-108">Column</span></span></th>
<th><span data-ttu-id="56626-109">类型</span><span class="sxs-lookup"><span data-stu-id="56626-109">Type</span></span></th>
<th><span data-ttu-id="56626-110">说明</span><span class="sxs-lookup"><span data-stu-id="56626-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56626-111">prinID</span><span class="sxs-lookup"><span data-stu-id="56626-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="56626-112">int，not null</span><span class="sxs-lookup"><span data-stu-id="56626-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="56626-113">主体 ID。</span><span class="sxs-lookup"><span data-stu-id="56626-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56626-114">memberADPath</span><span class="sxs-lookup"><span data-stu-id="56626-114">memberADPath</span></span></p></td>
<td><p><span data-ttu-id="56626-115">nvarchar (384) ，not null</span><span class="sxs-lookup"><span data-stu-id="56626-115">nvarchar (384), not null</span></span></p></td>
<td><p><span data-ttu-id="56626-116">成员的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="56626-116">Distinguished name of a member.</span></span> <span data-ttu-id="56626-117">成员在 tblPrincipal table) 中不必是主体 (。</span><span class="sxs-lookup"><span data-stu-id="56626-117">A member does not have to be a principal (in tblPrincipal table).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="56626-118">标示</span><span class="sxs-lookup"><span data-stu-id="56626-118">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56626-119">列</span><span class="sxs-lookup"><span data-stu-id="56626-119">Column</span></span></th>
<th><span data-ttu-id="56626-120">说明</span><span class="sxs-lookup"><span data-stu-id="56626-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56626-121">&lt;prinID, memberADPath&gt;</span><span class="sxs-lookup"><span data-stu-id="56626-121">&lt;prinID, memberADPath&gt;</span></span></p></td>
<td><p><span data-ttu-id="56626-122">主键。</span><span class="sxs-lookup"><span data-stu-id="56626-122">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56626-123">prinID</span><span class="sxs-lookup"><span data-stu-id="56626-123">prinID</span></span></p></td>
<td><p><span data-ttu-id="56626-124">在 tblPrincipal 中查找的外键。 prinID。</span><span class="sxs-lookup"><span data-stu-id="56626-124">Foreign key with lookup in tblPrincipal.prinID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="56626-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56626-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

