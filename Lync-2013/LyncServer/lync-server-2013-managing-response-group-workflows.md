---
title: Lync Server 2013：管理响应组工作流
description: Lync Server 2013：管理响应组工作流。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Response Group workflows
ms:assetid: 42cfccdd-2844-4875-b4e3-813e1df15f08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520986(v=OCS.15)
ms:contentKeyID: 48183974
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2223fed2b5b030a2c92e0b958ae8545a7717f848
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437222"
---
# <a name="managing-response-group-workflows-in-lync-server-2013"></a><span data-ttu-id="8e263-103">在 Lync Server 2013 中管理响应组工作流</span><span class="sxs-lookup"><span data-stu-id="8e263-103">Managing Response Group workflows in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e263-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e263-104">

<span> </span></span></span>

<span data-ttu-id="8e263-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="8e263-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="8e263-106">响应组工作流定义通话的行为，从电话响铃到工程师应答呼叫的时间。</span><span class="sxs-lookup"><span data-stu-id="8e263-106">A Response Group workflow defines the behavior of a call from the time that the phone rings to the time that an agent answers the call.</span></span> <span data-ttu-id="8e263-107">工作流包括 "队列" 和 "路由" 信息，其中包括查寻组或交互式语音响应 (IVR) 信息。</span><span class="sxs-lookup"><span data-stu-id="8e263-107">The workflow includes queue and routing information, and includes either hunt group or interactive voice response (IVR) information.</span></span>

<span data-ttu-id="8e263-108">本部分中的主题确定设计 IVR 工作流的最佳做法，并介绍如何创建或修改工作流以及如何删除工作组。</span><span class="sxs-lookup"><span data-stu-id="8e263-108">Topics in this section identify best practices for designing IVR workflows, and explain how to create customized business hours and holiday sets, how to create or modify workflows, and how to delete workgroups.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8e263-109">本节内容</span><span class="sxs-lookup"><span data-stu-id="8e263-109">In This Section</span></span>

  - [<span data-ttu-id="8e263-110">在 Lync Server 2013 中设计互动语音响应呼叫流</span><span class="sxs-lookup"><span data-stu-id="8e263-110">Design interactive voice response call flows in Lync Server 2013</span></span>](lync-server-2013-design-interactive-voice-response-call-flows.md)

  - [<span data-ttu-id="8e263-111"> (可选) 在 Lync Server 2013 中定义响应组工作时间</span><span class="sxs-lookup"><span data-stu-id="8e263-111">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)

  - [<span data-ttu-id="8e263-112"> (可选) 在 Lync Server 2013 中定义 "响应组" 假日集</span><span class="sxs-lookup"><span data-stu-id="8e263-112">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [<span data-ttu-id="8e263-113">在 Lync Server 2013 中创建或修改工作流</span><span class="sxs-lookup"><span data-stu-id="8e263-113">Create or modify a workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-workflow.md)

  - [<span data-ttu-id="8e263-114">在 Lync Server 2013 中删除工作流</span><span class="sxs-lookup"><span data-stu-id="8e263-114">Delete a workflow in Lync Server 2013</span></span>](lync-server-2013-delete-a-workflow.md)

<span data-ttu-id="8e263-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e263-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

