---
title: Lync Server 2013：名为 "ID 演示文稿"
description: Lync Server 2013：名为 "ID 演示文稿"。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Called ID presentation
ms:assetid: cf6c6af5-3418-411e-a50b-7a9cf8e100d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721892(v=OCS.15)
ms:contentKeyID: 49733826
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b438c7c19bc3c4ad641a8b9f8dac319c9fc2b1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435647"
---
# <a name="called-id-presentation-in-lync-server-2013"></a><span data-ttu-id="e1b95-103">Lync Server 2013 中名为 "ID 演示文稿"</span><span class="sxs-lookup"><span data-stu-id="e1b95-103">Called ID presentation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1b95-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1b95-104">

<span> </span></span></span>

<span data-ttu-id="e1b95-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="e1b95-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="e1b95-106">使用 Lync Server 2010，呼叫方的电话号码 (也就是说，电话号码) 可以从格式转换为中继对等 (的本地拨号格式，即关联网关、专用分支 exchange (PBX) 或 SIP 中继) 。</span><span class="sxs-lookup"><span data-stu-id="e1b95-106">With Lync Server 2010, the called party’s phone number (that is, the phone number called) can be translated from E.164 format to the local dialing format that is required by the trunk peer (that is, the associated gateway, private branch exchange (PBX), or SIP trunk).</span></span> <span data-ttu-id="e1b95-107">为此，必须定义一个或多个转换规则，以便在将请求 URI 路由至中继对等方之前对其执行转换。</span><span class="sxs-lookup"><span data-stu-id="e1b95-107">To do this, you must define one or more translation rules to translate the Request URI before routing it to the trunk peer.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e1b95-108">将一个或多个翻译规则与企业语音中继配置相关联的功能旨在用作在中继对等上配置翻译规则的 <EM>替代方法</EM> 。</span><span class="sxs-lookup"><span data-stu-id="e1b95-108">The ability to associate one or more translation rules with an Enterprise Voice trunk configuration is intended to be used as an <EM>alternative</EM> to configuring translation rules on the trunk peer.</span></span> <span data-ttu-id="e1b95-109">如果你已在中继对等上配置了转换规则，请不要将翻译规则与企业语音中继配置相关联，因为这两个规则可能会发生冲突。</span><span class="sxs-lookup"><span data-stu-id="e1b95-109">Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer because the two rules might conflict.</span></span>



</div>

<span data-ttu-id="e1b95-110">你可以使用以下任一方法来创建或修改翻译规则：</span><span class="sxs-lookup"><span data-stu-id="e1b95-110">You can use either of the following methods to create or modify a translation rule:</span></span>

  - <span data-ttu-id="e1b95-111">使用 " **生成翻译规则** " 工具来指定起始数字、长度、要删除的数字和要添加的数字的值，然后让 Lync Server "控制面板" 为你生成相应的匹配模式和转换规则。</span><span class="sxs-lookup"><span data-stu-id="e1b95-111">Use the **Build a Translation Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.</span></span>

  - <span data-ttu-id="e1b95-112">手动编写正则表达式以定义匹配的模式和转换规则。</span><span class="sxs-lookup"><span data-stu-id="e1b95-112">Write regular expressions manually to define the matching pattern and translation rule.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e1b95-113">有关如何编写正则表达式的信息，请参阅的 ".NET Framework 正则表达式" <A href="https://go.microsoft.com/fwlink/p/?linkid=140927">https://go.microsoft.com/fwlink/p/?linkId=140927</A> 。</span><span class="sxs-lookup"><span data-stu-id="e1b95-113">For information about how to write regular expressions, see ".NET Framework Regular Expressions" at <A href="https://go.microsoft.com/fwlink/p/?linkid=140927">https://go.microsoft.com/fwlink/p/?linkId=140927</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e1b95-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="e1b95-114">In This Section</span></span>

  - [<span data-ttu-id="e1b95-115">使用 Lync Server 2013 中的 "生成翻译规则" 工具创建或修改翻译规则</span><span class="sxs-lookup"><span data-stu-id="e1b95-115">Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md)

  - [<span data-ttu-id="e1b95-116">在 Lync Server 2013 中手动创建或修改翻译规则</span><span class="sxs-lookup"><span data-stu-id="e1b95-116">Create or modify a translation rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-manually.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e1b95-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1b95-117">See Also</span></span>


[<span data-ttu-id="e1b95-118">Lync Server 2013 中的呼叫者 ID 演示文稿</span><span class="sxs-lookup"><span data-stu-id="e1b95-118">Caller ID presentation in Lync Server 2013</span></span>](lync-server-2013-caller-id-presentation.md)  
  

<span data-ttu-id="e1b95-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1b95-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

