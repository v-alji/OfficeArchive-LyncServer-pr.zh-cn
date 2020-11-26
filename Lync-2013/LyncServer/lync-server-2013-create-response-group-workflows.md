---
title: Lync Server 2013：创建响应组工作流
description: Lync Server 2013：创建响应组工作流。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Response Group workflows
ms:assetid: 41272258-728d-42bd-b4d4-2a499734c720
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425918(v=OCS.15)
ms:contentKeyID: 48183954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7082295eeca45c4dac76d68ef54b5c32fafb25d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431587"
---
# <a name="create-response-group-workflows-in-lync-server-2013"></a><span data-ttu-id="ad571-103">在 Lync Server 2013 中创建响应组工作流</span><span class="sxs-lookup"><span data-stu-id="ad571-103">Create Response Group workflows in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad571-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad571-104">

<span> </span></span></span>

<span data-ttu-id="ad571-105">_**主题上次修改时间：** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="ad571-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="ad571-p101">工作流定义了从电话响铃到有人接听电话这段时间内呼叫的行为。工作流指定用于保留呼叫的队列，并指定用于智能寻线的路由方法或用于互动响应组的问题和答案。工作流还定义了诸如欢迎消息、保持音乐、工作时间和假日等设置。</span><span class="sxs-lookup"><span data-stu-id="ad571-p101">A workflow defines the behavior of a call from the time that the phone rings to the time that someone answers the call. The workflow specifies the queue to use for holding the call, and specifies the routing method to use for hunt groups or the questions and answers to use for interactive response groups. A workflow also defines settings such as a welcome message, music on hold, business hours, and holidays.</span></span>

<span data-ttu-id="ad571-109">使用 "响应组配置" 工具创建工作流。</span><span class="sxs-lookup"><span data-stu-id="ad571-109">You use the Response Group Configuration Tool to create workflows.</span></span> <span data-ttu-id="ad571-110">您可以从 Lync Server 控制面板的 "响应组" 页面访问 "响应组配置" 工具。</span><span class="sxs-lookup"><span data-stu-id="ad571-110">You can access the Response Group Configuration Tool from the Response Group page of Lync Server Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ad571-111">必须先创建代理组和队列，然后再创建使用这些组和队列的工作流。</span><span class="sxs-lookup"><span data-stu-id="ad571-111">You must create agent groups and queues before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ad571-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="ad571-112">In This Section</span></span>

  - [<span data-ttu-id="ad571-113">在 Lync Server 2013 中创建或修改查寻组工作流</span><span class="sxs-lookup"><span data-stu-id="ad571-113">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="ad571-114">在 Lync Server 2013 中设计互动语音响应呼叫流</span><span class="sxs-lookup"><span data-stu-id="ad571-114">Design interactive voice response call flows in Lync Server 2013</span></span>](lync-server-2013-design-interactive-voice-response-call-flows.md)

  - [<span data-ttu-id="ad571-115">在 Lync Server 2013 中创建或修改互动工作流</span><span class="sxs-lookup"><span data-stu-id="ad571-115">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="ad571-116">相关部分</span><span class="sxs-lookup"><span data-stu-id="ad571-116">Related Sections</span></span>

  - [<span data-ttu-id="ad571-117">在 Lync Server 2013 中创建响应组代理组</span><span class="sxs-lookup"><span data-stu-id="ad571-117">Create Response Group agent groups Lync Server 2013</span></span>](lync-server-2013-create-response-group-agent-groups.md)

  - [<span data-ttu-id="ad571-118">在 Lync Server 2013 中创建响应组队列</span><span class="sxs-lookup"><span data-stu-id="ad571-118">Create Response Group queues in Lync Server 2013</span></span>](lync-server-2013-create-response-group-queues.md)

<span data-ttu-id="ad571-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad571-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

