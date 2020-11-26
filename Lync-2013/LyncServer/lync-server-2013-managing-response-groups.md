---
title: Lync Server 2013：管理响应组
description: Lync Server 2013：管理响应组。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing response groups
ms:assetid: 5a804d7d-3c1a-4647-a0e0-d5c4c8c23b73
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520996(v=OCS.15)
ms:contentKeyID: 48184222
ms.date: 02/01/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 138ece386d55895893402e5a1fdead58790504f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437208"
---
# <a name="managing-response-groups-in-lync-server-2013"></a><span data-ttu-id="cfcfd-103">在 Lync Server 2013 中管理响应组</span><span class="sxs-lookup"><span data-stu-id="cfcfd-103">Managing response groups in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cfcfd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cfcfd-104">

<span> </span></span></span>

<span data-ttu-id="cfcfd-105">_**主题上次修改时间：** 2018-02-01_</span><span class="sxs-lookup"><span data-stu-id="cfcfd-105">_**Topic Last Modified:** 2018-02-01_</span></span>

<span data-ttu-id="cfcfd-106">响应组是一种呼叫管理功能，可让你对对特定区域（如帮助桌面）的呼叫进行排队，然后将呼叫路由到指定的一组人员（称为 *代理*）。</span><span class="sxs-lookup"><span data-stu-id="cfcfd-106">Response groups are a call management feature that enables you to queue calls that are made to a specific area, such as a Help Desk, and then route the calls to a designated group of people, called *agents*.</span></span>

<span data-ttu-id="cfcfd-107">若要管理响应组，请配置代理组、队列和工作流，以便在工程师应答它之前定义呼叫发生的时间。</span><span class="sxs-lookup"><span data-stu-id="cfcfd-107">To manage response groups, you configure agent groups, queues, and workflows, which define what happens to a call from the time it is placed until an agent answers it.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cfcfd-108">如果你的响应组部署中的单个池中有300个以上的工作流，最好使用 Lync Server Management Shell cmdlet 创建工作流。</span><span class="sxs-lookup"><span data-stu-id="cfcfd-108">If you have more than 300 workflows in a single pool in your Response Group deployment, it is better to use Lync Server Management Shell cmdlets to create the workflows.</span></span> <span data-ttu-id="cfcfd-109">如果使用 "响应组配置" 工具为具有超过300个工作流的池创建工作流，则该网页需要花费很长时间才能加载。</span><span class="sxs-lookup"><span data-stu-id="cfcfd-109">If you use the Response Group Configuration Tool to create workflows for a pool that has more than 300 workflows, the webpage takes a long time to load.</span></span> <span data-ttu-id="cfcfd-110">通过队列间接与工作流关联的代理数也会在页面加载时产生比例影响。</span><span class="sxs-lookup"><span data-stu-id="cfcfd-110">The number of agents that are indirectly associated with workflows through the queues also has a proportional effect on page loading.</span></span>



</div>

<span data-ttu-id="cfcfd-111">本部分中的主题提供了可执行的任务的分步过程，可用于在部署中自定义和维护响应组应用程序</span><span class="sxs-lookup"><span data-stu-id="cfcfd-111">Topics in this section provide step-by-step procedures for tasks that you can perform to customize and maintain the Response Group application in your deployment</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cfcfd-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="cfcfd-112">In This Section</span></span>

  - [<span data-ttu-id="cfcfd-113">在 Lync Server 2013 中管理响应组代理组</span><span class="sxs-lookup"><span data-stu-id="cfcfd-113">Managing Response Group agent groups in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-agent-groups.md)

  - [<span data-ttu-id="cfcfd-114">在 Lync Server 2013 中管理响应组队列</span><span class="sxs-lookup"><span data-stu-id="cfcfd-114">Managing Response Group queues in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-queues.md)

  - [<span data-ttu-id="cfcfd-115">在 Lync Server 2013 中管理响应组工作流</span><span class="sxs-lookup"><span data-stu-id="cfcfd-115">Managing Response Group workflows in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-workflows.md)

  - [<span data-ttu-id="cfcfd-116">在 Lync Server 2013 中管理应用程序级别的 "响应" 组设置</span><span class="sxs-lookup"><span data-stu-id="cfcfd-116">Managing application-level Response Group settings in Lync Server 2013</span></span>](lync-server-2013-managing-application-level-response-group-settings.md)

  - [<span data-ttu-id="cfcfd-117">将响应组移动到 Lync Server 2013 中的新池</span><span class="sxs-lookup"><span data-stu-id="cfcfd-117">Moving response groups to a new pool in Lync Server 2013</span></span>](lync-server-2013-moving-response-groups-to-a-new-pool.md)

  - [<span data-ttu-id="cfcfd-118">灾难期间在 Lync Server 2013 中管理响应组</span><span class="sxs-lookup"><span data-stu-id="cfcfd-118">Managing response groups in Lync Server 2013 during a disaster</span></span>](lync-server-2013-managing-response-groups-during-a-disaster.md)

<span data-ttu-id="cfcfd-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cfcfd-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

