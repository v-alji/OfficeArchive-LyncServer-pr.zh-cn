---
title: 配置 Lync Server 2013 方案
description: 配置 Lync Server 2013 方案。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Lync Server 2013 Scenarios
ms:assetid: 6705346b-1512-4af3-85e4-64dfa6ee6f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945596(v=OCS.15)
ms:contentKeyID: 51541420
ms.date: 12/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4a5b7bd271191067779ac358807cc54918b16bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440071"
---
# <a name="configure-lync-server-2013-scenarios"></a><span data-ttu-id="99ac5-103">配置 Lync Server 2013 方案</span><span class="sxs-lookup"><span data-stu-id="99ac5-103">Configure Lync Server 2013 Scenarios</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99ac5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99ac5-104">

<span> </span></span></span>

<span data-ttu-id="99ac5-105">_**主题上次修改时间：** 2016-12-28_</span><span class="sxs-lookup"><span data-stu-id="99ac5-105">_**Topic Last Modified:** 2016-12-28_</span></span>

<span data-ttu-id="99ac5-106">若要运行 Lync Server 2013 应力和性能工具 (LyncPerfTool) ，必须首先为将要执行的方案配置 Lync Server 2013 拓扑。</span><span class="sxs-lookup"><span data-stu-id="99ac5-106">To run the Lync Server 2013 Stress and Performance Tool (LyncPerfTool), the Lync Server 2013 topology must first be configured for the scenarios that will be executed.</span></span> <span data-ttu-id="99ac5-107">如果未配置 Lync Server 2013 或配置不正确，则在大多数情况下，负载模拟将失败。</span><span class="sxs-lookup"><span data-stu-id="99ac5-107">If Lync Server 2013 is not configured or is configured incorrectly, load simulation will fail in most cases.</span></span> <span data-ttu-id="99ac5-108">使用 Lync Server 2013 应力和性能工具，我们提供了示例 Lync Server Management Shell 脚本和基本资源文件，可用作配置 Lync Server 2013 的起始点。</span><span class="sxs-lookup"><span data-stu-id="99ac5-108">With the Lync Server 2013 Stress and Performance Tool, we have provided example Lync Server Management Shell scripts and basic resource files that can be used as a starting point for configuring Lync Server 2013.</span></span> <span data-ttu-id="99ac5-109">本主题介绍所提供的 Windows PowerShell 示例。</span><span class="sxs-lookup"><span data-stu-id="99ac5-109">This topic describes the Windows PowerShell examples provided.</span></span> <span data-ttu-id="99ac5-110">请注意，本主题的目标不是介绍如何在一般情况下配置 Lync Server 2013 的目标。</span><span class="sxs-lookup"><span data-stu-id="99ac5-110">Note that it is not the goal of this topic to describe how to configure Lync Server 2013 in general.</span></span> <span data-ttu-id="99ac5-111">有关在 Lync Server 2013 中使用 Windows PowerShell 的详细信息，请参阅 Lync Server Management Shell 文档 <https://technet.microsoft.com/library/gg398474.aspx> 。</span><span class="sxs-lookup"><span data-stu-id="99ac5-111">For details about working with Windows PowerShell in Lync Server 2013, see the Lync Server Management Shell documentation at <https://technet.microsoft.com/library/gg398474.aspx>.</span></span>

<div>

## <a name="about-running-lync-server-management-shell-scripts"></a><span data-ttu-id="99ac5-112">关于运行 Lync Server 命令行管理程序脚本</span><span class="sxs-lookup"><span data-stu-id="99ac5-112">About Running Lync Server Management Shell Scripts</span></span>

<span data-ttu-id="99ac5-113">我们提供了可用于准备运行负载模拟的 Lync Server Management Shell 脚本示例。</span><span class="sxs-lookup"><span data-stu-id="99ac5-113">We have provided example Lync Server Management Shell scripts that may be used in preparation for running load simulation.</span></span> <span data-ttu-id="99ac5-114">由于脚本适用于负载模拟，因此它们很简单且许可，因此可能不适合生产。</span><span class="sxs-lookup"><span data-stu-id="99ac5-114">Because the scripts are intended for load simulation, they are simple and permissive, and therefore may not be appropriate for production.</span></span> <span data-ttu-id="99ac5-115">所有脚本都是示例，在某些情况下，必须对其进行修改以反映你的拓扑。</span><span class="sxs-lookup"><span data-stu-id="99ac5-115">All scripts are examples and must be reviewed, and, in some cases, modified to reflect your topology.</span></span> <span data-ttu-id="99ac5-116">因此，我们预计响应组服务 (RGS) 方案需要进行修改以指定分配给代理组的代理。</span><span class="sxs-lookup"><span data-stu-id="99ac5-116">At a minimum, we expect that the Response Group Service (RGS) scenario would need to be modified to specify the agents that are assigned to the agent groups.</span></span> <span data-ttu-id="99ac5-117">但是，你可以选择不模拟此加载。</span><span class="sxs-lookup"><span data-stu-id="99ac5-117">However, you have the option to not simulate this load.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="99ac5-118">请注意查看和理解所提供的示例。</span><span class="sxs-lookup"><span data-stu-id="99ac5-118">Take care in reviewing and understanding the examples provided.</span></span> <span data-ttu-id="99ac5-119">脚本将覆盖拓扑中的任何现有设置。</span><span class="sxs-lookup"><span data-stu-id="99ac5-119">Scripts will overwrite any existing settings in the topology.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="99ac5-120">有关使用 Windows PowerShell 和 Lync Server 命令行管理程序的详细信息，请参阅 Lync Server 2013 中的 Windows PowerShell 博客 <A href="https://go.microsoft.com/fwlink/?linkid=203150">https://go.microsoft.com/fwlink/?LinkId=203150</A> 。</span><span class="sxs-lookup"><span data-stu-id="99ac5-120">For details about using Windows PowerShell and the Lync Server Management Shell, see the Lync Server 2013 Windows PowerShell Blog at <A href="https://go.microsoft.com/fwlink/?linkid=203150">https://go.microsoft.com/fwlink/?LinkId=203150</A>.</span></span>



</div>

</div>

<div>

## <a name="stress-and-performance-tool-client-version-monikers"></a><span data-ttu-id="99ac5-121">压力和性能工具客户端版本名字对象</span><span class="sxs-lookup"><span data-stu-id="99ac5-121">Stress and Performance Tool Client Version Monikers</span></span>

<span data-ttu-id="99ac5-122">如果您已更改默认值的设置，您可能需要配置客户端版本检查策略。</span><span class="sxs-lookup"><span data-stu-id="99ac5-122">You may need to configure the Client Version Check policy if you have changed the settings from the default values.</span></span> <span data-ttu-id="99ac5-123">有关详细信息，请参阅 "配置支持的客户端版本" <https://technet.microsoft.com/library/gg412832(v=ocs.15).aspx> 。</span><span class="sxs-lookup"><span data-stu-id="99ac5-123">For details, see “Configuring supported client versions” at <https://technet.microsoft.com/library/gg412832(v=ocs.15).aspx>.</span></span> <span data-ttu-id="99ac5-124">在与 Lync Server 2013 通信时，Lync Server 2013 应力和性能工具默认使用以下用户代理版本：</span><span class="sxs-lookup"><span data-stu-id="99ac5-124">The Lync Server 2013 Stress and Performance Tool uses the following User Agent Versions by default when communicating with Lync Server 2013:</span></span>

  - <span data-ttu-id="99ac5-125">LSPT/15.0.0.0 (Lync Server 2013 应力和性能工具) </span><span class="sxs-lookup"><span data-stu-id="99ac5-125">LSPT/15.0.0.0 (Lync Server 2013 Stress and Performance Tool)</span></span>

  - <span data-ttu-id="99ac5-126">OCPHONE/.0.522</span><span class="sxs-lookup"><span data-stu-id="99ac5-126">OCPHONE/.0.522</span></span>

<span data-ttu-id="99ac5-127">这些适用于移动 (LyncPerfTool 中的 UCWA) 客户端：</span><span class="sxs-lookup"><span data-stu-id="99ac5-127">These are for the Mobility (UCWA) client in LyncPerfTool:</span></span>

  - <span data-ttu-id="99ac5-128">Ucwa Perf 工具/Web 会议</span><span class="sxs-lookup"><span data-stu-id="99ac5-128">Ucwa Perf Tool/Web Conference</span></span>

  - <span data-ttu-id="99ac5-129">Ucwa Perf 工具/移动版</span><span class="sxs-lookup"><span data-stu-id="99ac5-129">Ucwa Perf Tool/Mobile</span></span>

<span data-ttu-id="99ac5-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99ac5-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

