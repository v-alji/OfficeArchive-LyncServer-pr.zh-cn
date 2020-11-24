---
title: Lync Server 2013：tblADCookie
description: Lync Server 2013： tblADCookie。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392011"
---
# <a name="tbladcookie-in-lync-server-2013"></a><span data-ttu-id="fd2a0-103">Lync Server 2013 中的 tblADCookie</span><span class="sxs-lookup"><span data-stu-id="fd2a0-103">tblADCookie in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd2a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd2a0-104">

<span> </span></span></span>

<span data-ttu-id="fd2a0-105">_**主题上次修改时间：** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="fd2a0-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="fd2a0-106">tblADCookie 包含当前轻型目录访问协议 (LDAP) 同步 cookie。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-106">tblADCookie contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span>

### <a name="columns"></a><span data-ttu-id="fd2a0-107">多</span><span class="sxs-lookup"><span data-stu-id="fd2a0-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd2a0-108">列</span><span class="sxs-lookup"><span data-stu-id="fd2a0-108">Column</span></span></th>
<th><span data-ttu-id="fd2a0-109">类型</span><span class="sxs-lookup"><span data-stu-id="fd2a0-109">Type</span></span></th>
<th><span data-ttu-id="fd2a0-110">说明</span><span class="sxs-lookup"><span data-stu-id="fd2a0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd2a0-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="fd2a0-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-112">GUID，not null</span><span class="sxs-lookup"><span data-stu-id="fd2a0-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-113">正在监视的域的主体 GUID。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-113">Principal GUID of the domain being monitored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd2a0-114">prinDCHost</span><span class="sxs-lookup"><span data-stu-id="fd2a0-114">prinDCHost</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-115">nvarchar (255) </span><span class="sxs-lookup"><span data-stu-id="fd2a0-115">nvarchar (255)</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-116">用于 Active Directory 域服务同步的当前域控制器 (FQDN) 的完全限定的域名。有信息值。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-116">Fully qualified domain name (FQDN) of the current domain controller used for Active Directory Domain Services Sync. Has informational value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd2a0-117">adcContent</span><span class="sxs-lookup"><span data-stu-id="fd2a0-117">adcContent</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-118"> (二进制) 的图像</span><span class="sxs-lookup"><span data-stu-id="fd2a0-118">image (binary)</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-119">Active Directory 同步 cookie。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-119">Active Directory Sync cookie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd2a0-120">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="fd2a0-120">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-121">datetime</span><span class="sxs-lookup"><span data-stu-id="fd2a0-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-122">带有行更新时间的时间戳。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-122">Time stamp with the row update time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd2a0-123">lockedUntil</span><span class="sxs-lookup"><span data-stu-id="fd2a0-123">lockedUntil</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-124">datetime</span><span class="sxs-lookup"><span data-stu-id="fd2a0-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-125">对行进行更改锁定的时间。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-125">Time until the row is locked for changes.</span></span> <span data-ttu-id="fd2a0-126">这是一种软件互操作机制的一部分，可确保每次只有一个聊天服务执行 Active Directory 同步。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-126">This is part of a software interlock mechanism that ensures that only one of the chat services does the Active Directory Sync at a time.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="fd2a0-127">标示</span><span class="sxs-lookup"><span data-stu-id="fd2a0-127">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd2a0-128"> (s) 的列</span><span class="sxs-lookup"><span data-stu-id="fd2a0-128">Column(s)</span></span></th>
<th><span data-ttu-id="fd2a0-129">说明</span><span class="sxs-lookup"><span data-stu-id="fd2a0-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd2a0-130">prinGuid</span><span class="sxs-lookup"><span data-stu-id="fd2a0-130">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-131">主键。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-131">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd2a0-132">prinGuid</span><span class="sxs-lookup"><span data-stu-id="fd2a0-132">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="fd2a0-133">PrinGuid 表中的 lookup 的外键。</span><span class="sxs-lookup"><span data-stu-id="fd2a0-133">Foreign key with lookup in Principal.prinGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fd2a0-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd2a0-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

