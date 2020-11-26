---
title: Lync Server 2013：测试语音路由
description: Lync Server 2013：测试语音路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice routing
ms:assetid: d3aae909-fef6-440f-b144-0b62dc82bf5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398915(v=OCS.15)
ms:contentKeyID: 48185444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e641e68ccecfe7d1d0e64dc9eb1b1f5016e68e22
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441149"
---
# <a name="test-voice-routing-in-lync-server-2013"></a><span data-ttu-id="98ae8-103">在 Lync Server 2013 中测试语音路由</span><span class="sxs-lookup"><span data-stu-id="98ae8-103">Test voice routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98ae8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98ae8-104">

<span> </span></span></span>

<span data-ttu-id="98ae8-105">_**主题上次修改时间：** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="98ae8-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="98ae8-106">你可以使用 Lync Server 控制面板 " **测试语音路由** " 选项卡来配置测试用例方案。</span><span class="sxs-lookup"><span data-stu-id="98ae8-106">You can use the Lync Server Control Panel **Test Voice Routing** tab to configure test case scenarios.</span></span> <span data-ttu-id="98ae8-107">若要定义测试用例，请指定用于测试指定电话号码的拨号计划、语音策略、PSTN 使用和语音路由。</span><span class="sxs-lookup"><span data-stu-id="98ae8-107">To define a test case, you specify the dial plan, voice policy, PSTN usage, and voice route against which to test a specified phone number.</span></span>

<span data-ttu-id="98ae8-108">在实际部署你的语音路由配置之前，我们建议你在不同的电话号码上测试它，以确保结果是你所期望的。</span><span class="sxs-lookup"><span data-stu-id="98ae8-108">Before you actually deploy your voice routing configuration, we recommend that you test it on various phone numbers to make sure that the results are what you're expecting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="98ae8-109">你可以使用 " <STRONG>导出测试用例</STRONG> " 和 " <STRONG>导入测试用</STRONG> 例" 命令来保存语音路由测试案例并将其导入以在另一台计算机上使用。</span><span class="sxs-lookup"><span data-stu-id="98ae8-109">You can use the <STRONG>Export test cases</STRONG> and <STRONG>Import test cases</STRONG> commands to save voice routing test cases and import them for use on another computer.</span></span>



</div>

<div>


> [!WARNING]  
> <span data-ttu-id="98ae8-110">如果您删除了 "语音路由" 配置的任何部分，如拨号计划、语音策略、语音路由或电话使用，您应该查看和更新您的语音路由测试案例。</span><span class="sxs-lookup"><span data-stu-id="98ae8-110">If you delete any part of your voice routing configuration, such as a dial plan, voice policy, voice route, or phone usage, you should review and update your voice routing test cases.</span></span> <span data-ttu-id="98ae8-111">Lync Server 控制面板将不会向你提示由于配置发生更改而不再有效的测试案例。</span><span class="sxs-lookup"><span data-stu-id="98ae8-111">The Lync Server Control Panel will not alert you to test cases that are no longer valid due to changed configurations.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="98ae8-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="98ae8-112">In This Section</span></span>

  - [<span data-ttu-id="98ae8-113">在 Lync Server 2013 中创建语音路由测试用例</span><span class="sxs-lookup"><span data-stu-id="98ae8-113">Create a voice routing test case in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-routing-test-case.md)

  - [<span data-ttu-id="98ae8-114">在 Lync Server 2013 中导出语音路由测试用例</span><span class="sxs-lookup"><span data-stu-id="98ae8-114">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)

  - [<span data-ttu-id="98ae8-115">在 Lync Server 2013 中导入语音路由测试用例</span><span class="sxs-lookup"><span data-stu-id="98ae8-115">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)

  - [<span data-ttu-id="98ae8-116">在 Lync Server 2013 中运行语音路由测试</span><span class="sxs-lookup"><span data-stu-id="98ae8-116">Running voice routing tests in Lync Server 2013</span></span>](lync-server-2013-running-voice-routing-tests.md)

<span data-ttu-id="98ae8-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98ae8-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

