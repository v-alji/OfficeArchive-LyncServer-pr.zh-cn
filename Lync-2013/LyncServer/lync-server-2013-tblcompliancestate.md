---
title: Lync Server 2013：tblComplianceState
description: Lync Server 2013： tblComplianceState。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceState
ms:assetid: ea82e56c-3cca-4d89-b4e6-6bcaeb1f2830
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615045(v=OCS.15)
ms:contentKeyID: 48185937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6eaf35eee8b4e24ec4d04e607fa77fd91b91e4e8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423510"
---
# <a name="tblcompliancestate-in-lync-server-2013"></a><span data-ttu-id="c4c14-103">Lync Server 2013 中的 tblComplianceState</span><span class="sxs-lookup"><span data-stu-id="c4c14-103">tblComplianceState in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4c14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4c14-104">

<span> </span></span></span>

<span data-ttu-id="c4c14-105">_**主题上次修改时间：** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="c4c14-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="c4c14-106">tblComplianceState 包含池范围的合规性状态信息。</span><span class="sxs-lookup"><span data-stu-id="c4c14-106">tblComplianceState contains pool-wide compliance state information.</span></span>

### <a name="columns"></a><span data-ttu-id="c4c14-107">多</span><span class="sxs-lookup"><span data-stu-id="c4c14-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4c14-108">列</span><span class="sxs-lookup"><span data-stu-id="c4c14-108">Column</span></span></th>
<th><span data-ttu-id="c4c14-109">类型</span><span class="sxs-lookup"><span data-stu-id="c4c14-109">Type</span></span></th>
<th><span data-ttu-id="c4c14-110">说明</span><span class="sxs-lookup"><span data-stu-id="c4c14-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4c14-111">lastProcessedEntryID</span><span class="sxs-lookup"><span data-stu-id="c4c14-111">lastProcessedEntryID</span></span></p></td>
<td><p><span data-ttu-id="c4c14-112">bigint，not null</span><span class="sxs-lookup"><span data-stu-id="c4c14-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="c4c14-113">最新的已处理合规性事件的 ID。</span><span class="sxs-lookup"><span data-stu-id="c4c14-113">ID of the latest processed compliance event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4c14-114">activeServerID</span><span class="sxs-lookup"><span data-stu-id="c4c14-114">activeServerID</span></span></p></td>
<td><p><span data-ttu-id="c4c14-115">int，not null</span><span class="sxs-lookup"><span data-stu-id="c4c14-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="c4c14-116">在数据库上持有独占锁的合规性服务器 ID，或者，如果没有，则为-1。</span><span class="sxs-lookup"><span data-stu-id="c4c14-116">ID of the Compliance server holding the exclusive lock on the database, or -1 if none.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4c14-117">lockExpirationTime</span><span class="sxs-lookup"><span data-stu-id="c4c14-117">lockExpirationTime</span></span></p></td>
<td><p><span data-ttu-id="c4c14-118">datetime2，not null</span><span class="sxs-lookup"><span data-stu-id="c4c14-118">datetime2, not null</span></span></p></td>
<td><p><span data-ttu-id="c4c14-119">如果 activeServerID 不是-1) ，则锁定到期时间 (。</span><span class="sxs-lookup"><span data-stu-id="c4c14-119">Lock expiration time (if activeServerID is not -1).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c4c14-120">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4c14-120">


</div>

<span> </span>

</div>

</div>

</span></span></div>

