---
title: Lync Server 2013：创建或修改工作流
description: Lync Server 2013：创建或修改工作流。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a workflow
ms:assetid: 5ac1c0f3-e82f-40ca-b972-91950e38c05b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520997(v=OCS.15)
ms:contentKeyID: 48184225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053b80e313e497313e613a5f8b16bd5beeabf7ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431727"
---
# <a name="create-or-modify-a-workflow-in-lync-server-2013"></a><span data-ttu-id="81972-103">在 Lync Server 2013 中创建或修改工作流</span><span class="sxs-lookup"><span data-stu-id="81972-103">Create or modify a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81972-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81972-104">

<span> </span></span></span>

<span data-ttu-id="81972-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="81972-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="81972-106">Lync Server 2013 支持两种类型的工作流：查寻组和交互式语音响应 (IVR) 。</span><span class="sxs-lookup"><span data-stu-id="81972-106">Lync Server 2013 supports two types of workflows: hunt group and interactive voice response (IVR).</span></span> <span data-ttu-id="81972-107">创建工作流时，使用 "响应组配置" 工具指定要使用的队列和其他设置，如欢迎消息、保持的音乐、工作时间和响应组应用程序询问呼叫者的问题。</span><span class="sxs-lookup"><span data-stu-id="81972-107">When you create a workflow, you use the Response Group Configuration Tool to specify the queue to use and other settings, such as a welcome message, music on hold, business hours, and questions that the Response Group application asks the caller.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="81972-108">必须先创建代理组和队列，然后再创建使用这些组和队列的工作流。</span><span class="sxs-lookup"><span data-stu-id="81972-108">You must create agent groups and queues before you create a workflow that uses them.</span></span> <span data-ttu-id="81972-109">如果要创建可用于多个工作流的预定义工作时间和假日，则还必须在创建使用它们的工作流之前定义这些工时和假日。</span><span class="sxs-lookup"><span data-stu-id="81972-109">If you want to create predefined business hours and holidays that you can use for multiple workflows, you must also define these hours and holidays before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="81972-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="81972-110">In This Section</span></span>

  - [<span data-ttu-id="81972-111">在 Lync Server 2013 中创建或修改查寻组工作流</span><span class="sxs-lookup"><span data-stu-id="81972-111">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="81972-112">在 Lync Server 2013 中创建或修改互动工作流</span><span class="sxs-lookup"><span data-stu-id="81972-112">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="81972-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="81972-113">See Also</span></span>


[<span data-ttu-id="81972-114">在 Lync Server 2013 中创建或修改代理组</span><span class="sxs-lookup"><span data-stu-id="81972-114">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  
[<span data-ttu-id="81972-115">在 Lync Server 2013 中创建或修改队列</span><span class="sxs-lookup"><span data-stu-id="81972-115">Create or modify a queue in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-queue.md)  
[<span data-ttu-id="81972-116"> (可选) 在 Lync Server 2013 中定义 "响应组" 假日集</span><span class="sxs-lookup"><span data-stu-id="81972-116">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="81972-117"> (可选) 在 Lync Server 2013 中定义响应组工作时间</span><span class="sxs-lookup"><span data-stu-id="81972-117">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  
  

<span data-ttu-id="81972-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81972-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

