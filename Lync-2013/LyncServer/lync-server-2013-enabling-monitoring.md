---
title: Lync Server 2013：启用监视
description: Lync Server 2013：启用监视。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling monitoring
ms:assetid: 244df419-d0a8-4b1d-aedd-a92114172ab6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687994(v=OCS.15)
ms:contentKeyID: 49733584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d8995042bdc9b121dc5253940104bb167567ddcc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392201"
---
# <a name="enabling-monitoring-in-lync-server-2013"></a><span data-ttu-id="0c3a5-103">在 Lync Server 2013 中启用监视</span><span class="sxs-lookup"><span data-stu-id="0c3a5-103">Enabling monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c3a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c3a5-104">

<span> </span></span></span>

<span data-ttu-id="0c3a5-105">_**主题上次修改时间：** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="0c3a5-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="0c3a5-106">虽然统一的数据收集代理会在每个前端服务器上自动安装和激活，但这并不意味着你在完成安装 Microsoft Lync Server 2013 后将自动开始收集监视数据。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-106">Although the unified data collection agents are automatically installed and activated on each Front End server, that does not mean that you will automatically begin to collect monitoring data the moment you finish installing Microsoft Lync Server 2013.</span></span> <span data-ttu-id="0c3a5-107">你必须执行两项操作：你必须将前端服务器/前端池与监视数据库相关联，并且必须在全局范围和/或网站范围内启用 "呼叫详细记录" (CDR) 和/或体验 (QoE) 监视。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-107">Instead, you must do two things: you must associate your Front End servers/Front End pools with a monitoring database, and you must enable call detail recording (CDR) and/or Quality of Experience (QoE) monitoring at the global scope and/or the site scope.</span></span>

<span data-ttu-id="0c3a5-108">有关将前端服务器或前端池与监视数据库关联的分步说明，请参阅部署指南中的主题将 [监视存储与 Lync Server 2013 中的前端池相关联](lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md) 。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-108">For step-by-step instructions on associating Front End servers or Front End pools with a monitoring database, see the topic [Associating a monitoring store with a Front End pool in Lync Server 2013](lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md) in the Deployment guide.</span></span> <span data-ttu-id="0c3a5-109">在创建这些关联后，在新的 Lync Server 拓扑发布后，你仍然无法收集监视数据。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-109">After these associations have been made, and after your new Lync Server topology has been published, you will still not be able to collect monitoring data.</span></span> <span data-ttu-id="0c3a5-110">这是因为，默认情况下，在安装 Lync Server 2013 时，将禁用 CDR 和 QoE 数据收集。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-110">That's because, by default, both CDR and QoE data collection is disabled when you install Lync Server 2013.</span></span>

<span data-ttu-id="0c3a5-111">若要开始数据收集，您将需要启用 CDR 和/或 QoE 监控。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-111">In order to begin data collection you will need to enable CDR and/or QoE monitoring.</span></span> <span data-ttu-id="0c3a5-112"> (注意，你无需同时启用 CDR 和 QoE 监视;如果你愿意，可以启用一种类型的监视，同时保留另一种类型。 ) 在全局范围内启用 CDR 监视在 Lync Server Management Shell 中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="0c3a5-112">(Note that you do not have to enable both CDR and QoE monitoring; if you prefer, you can enable one type of monitoring while leaving the other type disabled.) To enable CDR monitoring at the global scope run the following command from within the Lync Server Management Shell:</span></span>

    Set-CsCdrConfiguration -Identity "global" -EnableCDR $True

<span data-ttu-id="0c3a5-113">或者，您可以从 Lync Server 2013 控制面板中启用 CDR 监视。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-113">Alternatively, you can enable CDR monitoring from within the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="0c3a5-114">在 Lync Server "控制面板" 中，完成以下过程：</span><span class="sxs-lookup"><span data-stu-id="0c3a5-114">From within the Lync Server Control Panel, complete the following procedure:</span></span>

1.  <span data-ttu-id="0c3a5-115">单击“**监控**”。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-115">Click **Monitoring**.</span></span>

2.  <span data-ttu-id="0c3a5-116">在“**呼叫详细记录**”选项卡上，双击“**全局**”设置。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-116">On the **Call Detail Recording** tab, double-click the **Global** setting.</span></span>

3.  <span data-ttu-id="0c3a5-117">在“**编辑呼叫详细记录(CDR)设置**”窗格中，选择“**启用 CDR 监控**”，然后单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-117">In the **Edit Call Detail Recording (CDR) Setting** pane, select **Enable monitoring of CDRs** and then click **Commit**.</span></span>

<span data-ttu-id="0c3a5-118">若要在全局范围内启用 QoE 监视，请从 Lync Server Management Shell 中运行此命令：</span><span class="sxs-lookup"><span data-stu-id="0c3a5-118">To enable QoE monitoring at the global scope, run this command from within the Lync Server Management Shell:</span></span>

    Set-CsQoEConfiguration -Identity "global" -EnableQoE $True

<span data-ttu-id="0c3a5-119">如果您愿意，也可以从 Lync Server 控制面板中启用 QoE 监控。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-119">If you prefer, you can also enable QoE monitoring from within the Lync Server Control Panel.</span></span> <span data-ttu-id="0c3a5-120">从控制面板中，完成以下过程：</span><span class="sxs-lookup"><span data-stu-id="0c3a5-120">From within the Control Panel, complete the following procedure:</span></span>

1.  <span data-ttu-id="0c3a5-121">单击“**监控**”。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-121">Click **Monitoring**.</span></span>

2.  <span data-ttu-id="0c3a5-122">在“**用户体验质量数据**”选项卡上，双击“**全局**”设置。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-122">On the **Quality of Experience Data** tab, double-click the **Global** setting.</span></span>

3.  <span data-ttu-id="0c3a5-123">在“**编辑体验质量(QoE)设置**”窗格中，选择“**启用 QoE 数据监控**”，然后单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-123">In the **Edit Quality of Experience (QoE) Setting** pane, select **Enable monitoring of QoE data** and then click **Commit**.</span></span>

<span data-ttu-id="0c3a5-124">您已看到，上面的示例在全局范围启用监控；即，它们在贵组织内启用 CDR 和 QoE 监控。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-124">As noted, the preceding examples enable monitoring at the global scope; that is, they enable CDR and QoE monitoring throughout your organization.</span></span> <span data-ttu-id="0c3a5-125">您也可以在站点范围创建单独的 CDR 和 QoE 配置设置，然后有选择地为每个站点启用或禁用监控。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-125">Alternatively, you can create separate CDR and QoE configuration settings at the site scope, and then selectively enable or disable monitoring for each site.</span></span> <span data-ttu-id="0c3a5-126">例如，可以为您的 Redmond 站点启用 CDR 监控，而为您的 Dublin 站点禁用 CDR 监控。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-126">For example, you could enable CDR monitoring for your Redmond site, yet disable CDR monitoring for your Dublin site.</span></span> <span data-ttu-id="0c3a5-127">有关管理监视配置设置的详细信息，请参阅部署指南主题 [配置 Lync Server 2013 中的 "呼叫详细记录" 和 "体验质量" 设置](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="0c3a5-127">For more information on managing your monitoring configuration settings, see the Deployment guide topic [Configuring call detail recording and Quality of Experience settings in Lync Server 2013](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md).</span></span>

<span data-ttu-id="0c3a5-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c3a5-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

