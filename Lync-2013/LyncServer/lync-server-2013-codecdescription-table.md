---
title: Lync Server 2013： CodecDescription 表
description: Lync Server 2013： CodecDescription 表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CodecDescription table
ms:assetid: 3598acb8-7ea6-4748-8417-149c971c32a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204797(v=OCS.15)
ms:contentKeyID: 48183802
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b96ce75ee5ea4d1093314aa9e9543dd155a5eace
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434716"
---
# <a name="codecdescription-table-in-lync-server-2013"></a><span data-ttu-id="39c88-103">Lync Server 2013 中的 CodecDescription 表</span><span class="sxs-lookup"><span data-stu-id="39c88-103">CodecDescription table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39c88-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39c88-104">

<span> </span></span></span>

<span data-ttu-id="39c88-105">_**主题上次修改时间：** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="39c88-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="39c88-106">CodecDescription 表将唯一的编解码器标识符映射到相应的编解码器。</span><span class="sxs-lookup"><span data-stu-id="39c88-106">The CodecDescription table maps unique codec identifiers to their corresponding codec.</span></span> <span data-ttu-id="39c88-107">编解码器用于为传输和广播编码数字信号，然后解码这些信号以进行播放。</span><span class="sxs-lookup"><span data-stu-id="39c88-107">Codecs are used to encode digital signals for transmission and broadcast, and then to decode those signals for playback.</span></span> <span data-ttu-id="39c88-108">此表是在 Microsoft Lync Server 2013 中引入的</span><span class="sxs-lookup"><span data-stu-id="39c88-108">This table was introduced in Microsoft Lync Server 2013</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39c88-109"><strong>列</strong></span><span class="sxs-lookup"><span data-stu-id="39c88-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="39c88-110"><strong>数据类型</strong></span><span class="sxs-lookup"><span data-stu-id="39c88-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="39c88-111"><strong>键/索引</strong></span><span class="sxs-lookup"><span data-stu-id="39c88-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="39c88-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="39c88-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c88-113"><strong>CodecDescriptionKey</strong></span><span class="sxs-lookup"><span data-stu-id="39c88-113"><strong>CodecDescriptionKey</strong></span></span></p></td>
<td><p><span data-ttu-id="39c88-114">smallint</span><span class="sxs-lookup"><span data-stu-id="39c88-114">smallint</span></span></p></td>
<td><p><span data-ttu-id="39c88-115">Primary</span><span class="sxs-lookup"><span data-stu-id="39c88-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="39c88-116">分配给编解码器的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="39c88-116">Unique identifier assigned to the codec.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c88-117"><strong>CodecDescription</strong></span><span class="sxs-lookup"><span data-stu-id="39c88-117"><strong>CodecDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="39c88-118">varchar (256) </span><span class="sxs-lookup"><span data-stu-id="39c88-118">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="39c88-119">唯一</span><span class="sxs-lookup"><span data-stu-id="39c88-119">Unique</span></span></p></td>
<td><p><span data-ttu-id="39c88-120">与 CodecDescriptionKey 对应的编解码器的唯一说明。</span><span class="sxs-lookup"><span data-stu-id="39c88-120">Unique description of the codec corresponding to the CodecDescriptionKey.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="39c88-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39c88-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

