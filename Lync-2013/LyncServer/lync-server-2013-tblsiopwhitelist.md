---
title: Lync Server 2013：tblSiopWhiteList
description: Lync Server 2013： tblSiopWhiteList。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblSiopWhiteList
ms:assetid: 05fc1df4-32eb-4d46-9d1c-e0b607091142
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558607(v=OCS.15)
ms:contentKeyID: 48183310
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbb58c0818a6f36959732f210b8eb53bbfe223d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391788"
---
# <a name="tblsiopwhitelist-in-lync-server-2013"></a><span data-ttu-id="926f4-103">Lync Server 2013 中的 tblSiopWhiteList</span><span class="sxs-lookup"><span data-stu-id="926f4-103">tblSiopWhiteList in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="926f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="926f4-104">

<span> </span></span></span>

<span data-ttu-id="926f4-105">_**主题上次修改时间：** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="926f4-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="926f4-106">tblSiopWhiteList 是可与节点相关联的注册外接程序的列表。</span><span class="sxs-lookup"><span data-stu-id="926f4-106">tblSiopWhiteList is the list of registered add-ins that can be associated with nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="926f4-107">多</span><span class="sxs-lookup"><span data-stu-id="926f4-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="926f4-108">列</span><span class="sxs-lookup"><span data-stu-id="926f4-108">Column</span></span></th>
<th><span data-ttu-id="926f4-109">类型</span><span class="sxs-lookup"><span data-stu-id="926f4-109">Type</span></span></th>
<th><span data-ttu-id="926f4-110">说明</span><span class="sxs-lookup"><span data-stu-id="926f4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="926f4-111">siopID</span><span class="sxs-lookup"><span data-stu-id="926f4-111">siopID</span></span></p></td>
<td><p><span data-ttu-id="926f4-112">GUID，not null</span><span class="sxs-lookup"><span data-stu-id="926f4-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="926f4-113">外接程序的 GUID。</span><span class="sxs-lookup"><span data-stu-id="926f4-113">GUID of the add-in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="926f4-114">siopName</span><span class="sxs-lookup"><span data-stu-id="926f4-114">siopName</span></span></p></td>
<td><p><span data-ttu-id="926f4-115">nvarchar (50) ，not null</span><span class="sxs-lookup"><span data-stu-id="926f4-115">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="926f4-116">显示-外接程序的名称。</span><span class="sxs-lookup"><span data-stu-id="926f4-116">Display-name of the add-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="926f4-117">siopUrl</span><span class="sxs-lookup"><span data-stu-id="926f4-117">siopUrl</span></span></p></td>
<td><p><span data-ttu-id="926f4-118">nvarchar (255) ，not null</span><span class="sxs-lookup"><span data-stu-id="926f4-118">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="926f4-119">外接程序的 URL。</span><span class="sxs-lookup"><span data-stu-id="926f4-119">URL of the add-in.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="926f4-120">密钥</span><span class="sxs-lookup"><span data-stu-id="926f4-120">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="926f4-121">列</span><span class="sxs-lookup"><span data-stu-id="926f4-121">Column</span></span></th>
<th><span data-ttu-id="926f4-122">说明</span><span class="sxs-lookup"><span data-stu-id="926f4-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="926f4-123">siopID</span><span class="sxs-lookup"><span data-stu-id="926f4-123">siopID</span></span></p></td>
<td><p><span data-ttu-id="926f4-124">主键。</span><span class="sxs-lookup"><span data-stu-id="926f4-124">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="926f4-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="926f4-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

