---
title: Lync Server 2013：定义转换规则
description: Lync Server 2013：定义翻译规则。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining translation rules
ms:assetid: 4f6b975a-77e6-474c-9171-b139d84138c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398322(v=OCS.15)
ms:contentKeyID: 48184093
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0c59225c8dc74d7d97bf3536c7b7073bc977925
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430908"
---
# <a name="defining-translation-rules-in-lync-server-2013"></a><span data-ttu-id="040a5-103">在 Lync Server 2013 中定义转换规则</span><span class="sxs-lookup"><span data-stu-id="040a5-103">Defining translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="040a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="040a5-104">

<span> </span></span></span>

<span data-ttu-id="040a5-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="040a5-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="040a5-106">Lync Server 2013 企业版语音路由基于规范化为164格式的电话号码进行呼叫。</span><span class="sxs-lookup"><span data-stu-id="040a5-106">Lync Server 2013 Enterprise Voice routes calls based on phone numbers normalized to E.164 format.</span></span> <span data-ttu-id="040a5-107">这意味着，所有已拨的字符串都必须规范化为 RNL 格式，以便执行反向数字查找 () ，以便可以将其转换为匹配的 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="040a5-107">This means that all dialed strings must be normalized to E.164 format for the purpose of performing reverse number lookup (RNL) so they can be translated to their matching SIP URI.</span></span> <span data-ttu-id="040a5-108">Lync Server 2013 提供操作被呼叫的 ID 和来电显示演示文稿的功能。</span><span class="sxs-lookup"><span data-stu-id="040a5-108">Lync Server 2013 provides the ability to manipulate the called ID and the caller ID presentation.</span></span>

<span data-ttu-id="040a5-109">本部分讨论如何操纵已调用的 ID 和来电显示 ID。</span><span class="sxs-lookup"><span data-stu-id="040a5-109">This section discusses how to manipulate the called ID and caller ID.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="040a5-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="040a5-110">In This Section</span></span>

  - [<span data-ttu-id="040a5-111">Lync Server 2013 中的呼叫者 ID 演示文稿</span><span class="sxs-lookup"><span data-stu-id="040a5-111">Caller ID presentation in Lync Server 2013</span></span>](lync-server-2013-caller-id-presentation.md)

  - [<span data-ttu-id="040a5-112">Lync Server 2013 中名为 "ID 演示文稿"</span><span class="sxs-lookup"><span data-stu-id="040a5-112">Called ID presentation in Lync Server 2013</span></span>](lync-server-2013-called-id-presentation.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="040a5-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="040a5-113">See Also</span></span>


[<span data-ttu-id="040a5-114">在 Lync Server 2013 中定义规范化规则</span><span class="sxs-lookup"><span data-stu-id="040a5-114">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)  
  

<span data-ttu-id="040a5-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="040a5-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

