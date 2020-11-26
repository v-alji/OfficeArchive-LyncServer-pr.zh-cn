---
title: Lync Server 2013：构建边缘和控制器拓扑
description: Lync Server 2013：构建边缘和控制器拓扑。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Building an edge and Director topology
ms:assetid: 11e5759e-d69f-4c39-8994-f467c279c558
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398202(v=OCS.15)
ms:contentKeyID: 48183451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcb2d422136cf0a421c68ebc2adba50f03c5cc85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435934"
---
# <a name="building-an-edge-and-director-topology-in-lync-server-2013"></a><span data-ttu-id="af046-103">在 Lync Server 2013 中构建边缘和控制器拓扑</span><span class="sxs-lookup"><span data-stu-id="af046-103">Building an edge and Director topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af046-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af046-104">

<span> </span></span></span>

<span data-ttu-id="af046-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="af046-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="af046-106">构建拓扑涉及以下规划和部署任务：</span><span class="sxs-lookup"><span data-stu-id="af046-106">Building the topology involves the following planning and deployment tasks:</span></span>

  - <span data-ttu-id="af046-107">**规划**   你需要为你的组织定义合适的拓扑，并确定部署该拓扑所需的组件。</span><span class="sxs-lookup"><span data-stu-id="af046-107">**Planning**   You need to define an appropriate topology for your organization and identify the components required to deploy it.</span></span> <span data-ttu-id="af046-108">这些是规划流程中的标准步骤。</span><span class="sxs-lookup"><span data-stu-id="af046-108">These are standard steps in the planning process.</span></span> <span data-ttu-id="af046-109">Lync Server 2013 提供的 Microsoft Lync Server 2013、计划工具使你能够轻松地开始规划过程，以及如何在你的要求和计划完成后轻松进行更改。</span><span class="sxs-lookup"><span data-stu-id="af046-109">The Microsoft Lync Server 2013, Planning Tool provided with Lync Server 2013 makes it easy to start the planning process, as well as including the ability to easily make changes as your requirements and plans are finalized.</span></span>

  - <span data-ttu-id="af046-110">**部署**   使用拓扑生成器定义的拓扑对于部署任何 Lync Server 2013 服务器都是必需的。</span><span class="sxs-lookup"><span data-stu-id="af046-110">**Deployment**   The topology that you define using Topology Builder is essential to the deployment of any Lync Server 2013 server.</span></span> <span data-ttu-id="af046-111">如果你未通过在计划工作中使用拓扑生成器来完成定义和发布拓扑，则必须先完成它并发布拓扑，然后再部署你的 Edge 服务器。</span><span class="sxs-lookup"><span data-stu-id="af046-111">If you do not finish defining and publishing your topology by using Topology Builder as part of your planning efforts, you must complete it and publish the topology before you deploy your Edge Servers.</span></span>

<span data-ttu-id="af046-112">只有在部署了至少一个内部池后才能部署 Edge 服务器组件，并且必须安装拓扑生成器才能部署内部池。</span><span class="sxs-lookup"><span data-stu-id="af046-112">You cannot deploy Edge Server components until you have deployed at least one internal pool, and you must install Topology Builder to deploy an internal pool.</span></span> <span data-ttu-id="af046-113">本节不介绍拓扑生成器的安装，因为它是内部池安装过程的一部分。</span><span class="sxs-lookup"><span data-stu-id="af046-113">This section does not cover installation of Topology Builder because that is part of the installation process for the internal pool.</span></span>

<span data-ttu-id="af046-114">有关这些工具的详细信息，请参阅 [Lync Server 2013 中的外部用户访问的部署清单](lync-server-2013-deployment-checklist-for-external-user-access.md)。</span><span class="sxs-lookup"><span data-stu-id="af046-114">For details about these tools, see [Deployment checklist for external user access in Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="af046-115">如果你以前使用拓扑生成器定义完整拓扑（包括边缘拓扑），则可以跳过 <A href="lync-server-2013-define-your-edge-topology.md">在 Lync server 2013 中定义 edge 拓扑</A> 并在此部分中的 <A href="lync-server-2013-publish-your-topology.md">Lync server 2013 任务中发布你的拓扑</A> ，但你需要完成 <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">导出 Lync Server 2013 拓扑并将其复制到外部媒体以进行边缘安装</A> 任务。</span><span class="sxs-lookup"><span data-stu-id="af046-115">If you previously used Topology Builder to define a complete topology, including the edge topology, you do can skip the <A href="lync-server-2013-define-your-edge-topology.md">Define your edge topology in Lync Server 2013</A> and <A href="lync-server-2013-publish-your-topology.md">Publish your topology in Lync Server 2013</A> tasks in this section, but you do need to complete the <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A> task.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="af046-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="af046-116">In This Section</span></span>

  - [<span data-ttu-id="af046-117">在 Lync Server 2013 中定义边缘拓扑</span><span class="sxs-lookup"><span data-stu-id="af046-117">Define your edge topology in Lync Server 2013</span></span>](lync-server-2013-define-your-edge-topology.md)

  - [<span data-ttu-id="af046-118">针对 Lync Server 2013 在拓扑中定义可选控制器拓扑</span><span class="sxs-lookup"><span data-stu-id="af046-118">Define optional Director topologies in your topology for Lync Server 2013</span></span>](lync-server-2013-define-optional-director-topologies-in-your-topology.md)

  - [<span data-ttu-id="af046-119">在 Lync Server 2013 中发布拓扑</span><span class="sxs-lookup"><span data-stu-id="af046-119">Publish your topology in Lync Server 2013</span></span>](lync-server-2013-publish-your-topology.md)

  - [<span data-ttu-id="af046-120">导出 Lync Server 2013 拓扑并将其复制到外部媒体以用于边缘安装</span><span class="sxs-lookup"><span data-stu-id="af046-120">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

<span data-ttu-id="af046-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af046-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

