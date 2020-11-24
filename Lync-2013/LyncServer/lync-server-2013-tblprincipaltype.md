---
title: Lync Server 2013：tblPrincipalType
description: Lync Server 2013： tblPrincipalType。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba0f607d4499b54b16d7ecf8a4e7de603e874788
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391793"
---
# <a name="tblprincipaltype-in-lync-server-2013"></a><span data-ttu-id="a201c-103">Lync Server 2013 中的 tblPrincipalType</span><span class="sxs-lookup"><span data-stu-id="a201c-103">tblPrincipalType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a201c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a201c-104">

<span> </span></span></span>

<span data-ttu-id="a201c-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="a201c-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="a201c-106">tblPrincipalType 包含用于对 tblPrincipal 表中的内容进行分类的主体类型。</span><span class="sxs-lookup"><span data-stu-id="a201c-106">tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.</span></span>

### <a name="columns"></a><span data-ttu-id="a201c-107">多</span><span class="sxs-lookup"><span data-stu-id="a201c-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a201c-108">列</span><span class="sxs-lookup"><span data-stu-id="a201c-108">Column</span></span></th>
<th><span data-ttu-id="a201c-109">类型</span><span class="sxs-lookup"><span data-stu-id="a201c-109">Type</span></span></th>
<th><span data-ttu-id="a201c-110">说明</span><span class="sxs-lookup"><span data-stu-id="a201c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a201c-111">ptypeID</span><span class="sxs-lookup"><span data-stu-id="a201c-111">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="a201c-112">smallint，not null</span><span class="sxs-lookup"><span data-stu-id="a201c-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="a201c-113">主体类型 ID。</span><span class="sxs-lookup"><span data-stu-id="a201c-113">Principal type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a201c-114">ptypeDesc</span><span class="sxs-lookup"><span data-stu-id="a201c-114">ptypeDesc</span></span></p></td>
<td><p><span data-ttu-id="a201c-115">nvarchar (256) ，not null</span><span class="sxs-lookup"><span data-stu-id="a201c-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="a201c-116">类型的说明。</span><span class="sxs-lookup"><span data-stu-id="a201c-116">Description of the type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a201c-117">ptypeIsSystemUser</span><span class="sxs-lookup"><span data-stu-id="a201c-117">ptypeIsSystemUser</span></span></p></td>
<td><p><span data-ttu-id="a201c-118">位，not null</span><span class="sxs-lookup"><span data-stu-id="a201c-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="a201c-119">如果类型对应于用于内部用途的主体，则为 True。</span><span class="sxs-lookup"><span data-stu-id="a201c-119">True if the type corresponds to the principals that are used for internal purposes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a201c-120">ptypeIsUser</span><span class="sxs-lookup"><span data-stu-id="a201c-120">ptypeIsUser</span></span></p></td>
<td><p><span data-ttu-id="a201c-121">位，not null</span><span class="sxs-lookup"><span data-stu-id="a201c-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="a201c-122">如果类型为用户类型，则为 True。</span><span class="sxs-lookup"><span data-stu-id="a201c-122">True if the type is a user type.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="a201c-123">密钥</span><span class="sxs-lookup"><span data-stu-id="a201c-123">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a201c-124">列</span><span class="sxs-lookup"><span data-stu-id="a201c-124">Column</span></span></th>
<th><span data-ttu-id="a201c-125">说明</span><span class="sxs-lookup"><span data-stu-id="a201c-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a201c-126">ptypeID</span><span class="sxs-lookup"><span data-stu-id="a201c-126">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="a201c-127">主键。</span><span class="sxs-lookup"><span data-stu-id="a201c-127">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="principal-values"></a><span data-ttu-id="a201c-128">主体值</span><span class="sxs-lookup"><span data-stu-id="a201c-128">Principal Values</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a201c-129">ID</span><span class="sxs-lookup"><span data-stu-id="a201c-129">ID</span></span></th>
<th><span data-ttu-id="a201c-130">角色</span><span class="sxs-lookup"><span data-stu-id="a201c-130">Role</span></span></th>
<th><span data-ttu-id="a201c-131">说明</span><span class="sxs-lookup"><span data-stu-id="a201c-131">Description</span></span></th>
<th><span data-ttu-id="a201c-132">用户</span><span class="sxs-lookup"><span data-stu-id="a201c-132">User</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a201c-133">1</span><span class="sxs-lookup"><span data-stu-id="a201c-133">1</span></span></p></td>
<td><p><span data-ttu-id="a201c-134">任意</span><span class="sxs-lookup"><span data-stu-id="a201c-134">Any</span></span></p></td>
<td><p><span data-ttu-id="a201c-135">没有已知类型的泛型主体。</span><span class="sxs-lookup"><span data-stu-id="a201c-135">Generic principal with no known type.</span></span> <span data-ttu-id="a201c-136">未在 tblPrincipal 表中使用。</span><span class="sxs-lookup"><span data-stu-id="a201c-136">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a201c-137">2</span><span class="sxs-lookup"><span data-stu-id="a201c-137">2</span></span></p></td>
<td><p><span data-ttu-id="a201c-138">AnyUser</span><span class="sxs-lookup"><span data-stu-id="a201c-138">AnyUser</span></span></p></td>
<td><p><span data-ttu-id="a201c-139">用户类型的一般主体。</span><span class="sxs-lookup"><span data-stu-id="a201c-139">Generic principal of user type.</span></span> <span data-ttu-id="a201c-140">未在 tblPrincipal 表中使用。</span><span class="sxs-lookup"><span data-stu-id="a201c-140">Not used in tblPrincipal table.</span></span></p></td>
<td><p><span data-ttu-id="a201c-141">是</span><span class="sxs-lookup"><span data-stu-id="a201c-141">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a201c-142">3</span><span class="sxs-lookup"><span data-stu-id="a201c-142">3</span></span></p></td>
<td><p><span data-ttu-id="a201c-143">AnyGroup</span><span class="sxs-lookup"><span data-stu-id="a201c-143">AnyGroup</span></span></p></td>
<td><p><span data-ttu-id="a201c-144">具有组语义的常规主体。</span><span class="sxs-lookup"><span data-stu-id="a201c-144">Generic principal with group semantic.</span></span> <span data-ttu-id="a201c-145">未在 tblPrincipal 表中使用。</span><span class="sxs-lookup"><span data-stu-id="a201c-145">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a201c-146">4</span><span class="sxs-lookup"><span data-stu-id="a201c-146">4</span></span></p></td>
<td><p><span data-ttu-id="a201c-147">SystemUser</span><span class="sxs-lookup"><span data-stu-id="a201c-147">SystemUser</span></span></p></td>
<td><p><span data-ttu-id="a201c-148">持久聊天服务器在内部使用的主体。</span><span class="sxs-lookup"><span data-stu-id="a201c-148">Principal used internally by Persistent Chat Server.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a201c-149">5</span><span class="sxs-lookup"><span data-stu-id="a201c-149">5</span></span></p></td>
<td><p><span data-ttu-id="a201c-150">用户</span><span class="sxs-lookup"><span data-stu-id="a201c-150">User</span></span></p></td>
<td><p><span data-ttu-id="a201c-151">普通用户。</span><span class="sxs-lookup"><span data-stu-id="a201c-151">Regular user.</span></span></p></td>
<td><p><span data-ttu-id="a201c-152">是</span><span class="sxs-lookup"><span data-stu-id="a201c-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a201c-153">个</span><span class="sxs-lookup"><span data-stu-id="a201c-153">8</span></span></p></td>
<td><p><span data-ttu-id="a201c-154">电源</span><span class="sxs-lookup"><span data-stu-id="a201c-154">DC</span></span></p></td>
<td><p><span data-ttu-id="a201c-155">Active Directory 域服务域控制器。</span><span class="sxs-lookup"><span data-stu-id="a201c-155">Active Directory Domain Services domain controller.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a201c-156">db-9</span><span class="sxs-lookup"><span data-stu-id="a201c-156">9</span></span></p></td>
<td><p><span data-ttu-id="a201c-157">团队</span><span class="sxs-lookup"><span data-stu-id="a201c-157">Group</span></span></p></td>
<td><p><span data-ttu-id="a201c-158">Active Directory 安全组。</span><span class="sxs-lookup"><span data-stu-id="a201c-158">Active Directory security group.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a201c-159">10</span><span class="sxs-lookup"><span data-stu-id="a201c-159">10</span></span></p></td>
<td><p><span data-ttu-id="a201c-160">文件夹</span><span class="sxs-lookup"><span data-stu-id="a201c-160">Folder</span></span></p></td>
<td><p><span data-ttu-id="a201c-161">Active Directory 容器或组织单位。</span><span class="sxs-lookup"><span data-stu-id="a201c-161">Active Directory container or organizational unit.</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="a201c-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a201c-162">See Also</span></span>


[<span data-ttu-id="a201c-163">Lync Server 2013 中的 tblPrincipal</span><span class="sxs-lookup"><span data-stu-id="a201c-163">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)  
  

<span data-ttu-id="a201c-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a201c-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

