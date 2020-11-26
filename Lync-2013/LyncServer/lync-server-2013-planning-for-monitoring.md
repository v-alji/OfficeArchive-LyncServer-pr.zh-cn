---
title: Lync Server 2013：规划监控
description: Lync Server 2013：规划监视。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for monitoring
ms:assetid: 26cead5a-183c-42f1-a4b0-0e8d61c6159d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204752(v=OCS.15)
ms:contentKeyID: 48183671
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8ee78f06423bc167e26455d399ce2dd16f24262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442927"
---
# <a name="planning-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="8c9a0-103">在 Lync Server 2013 中规划监控</span><span class="sxs-lookup"><span data-stu-id="8c9a0-103">Planning for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c9a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c9a0-104">

<span> </span></span></span>

<span data-ttu-id="8c9a0-105">_**主题上次修改时间：** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="8c9a0-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="8c9a0-106">Microsoft Lync Server 2013 中的 "监视" 服务为管理员收集组织中发生的通信会话的使用情况、趋势和质量数据提供了一种方法。</span><span class="sxs-lookup"><span data-stu-id="8c9a0-106">The monitoring service in Microsoft Lync Server 2013 provides a way for administrators to collect usage, trend, and quality of service data for the communication sessions that take place in their organization.</span></span> <span data-ttu-id="8c9a0-107">Lync Server 2013 中的监控不再需要单独的服务器角色;而是将监视服务内置于每个前端服务器。</span><span class="sxs-lookup"><span data-stu-id="8c9a0-107">Monitoring in Lync Server 2013 no longer requires a separate server role; instead, the monitoring service is built into each Front End server.</span></span> <span data-ttu-id="8c9a0-108">但是，默认情况下，在 Lync Server 2013 中未启用监视功能。</span><span class="sxs-lookup"><span data-stu-id="8c9a0-108">However, by default monitoring is not enabled in Lync Server 2013.</span></span> <span data-ttu-id="8c9a0-109">本文档将帮助你确定是否应在你的组织中启用监视。</span><span class="sxs-lookup"><span data-stu-id="8c9a0-109">This document will help you determine whether or not monitoring should be enabled in your organization.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8c9a0-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="8c9a0-110">In This Section</span></span>

  - [<span data-ttu-id="8c9a0-111">Lync Server 2013 中的监视概述</span><span class="sxs-lookup"><span data-stu-id="8c9a0-111">Overview of monitoring in Lync Server 2013</span></span>](lync-server-2013-overview-of-monitoring.md)

  - [<span data-ttu-id="8c9a0-112">在 Lync Server 2013 中定义组织的监控要求</span><span class="sxs-lookup"><span data-stu-id="8c9a0-112">Defining your requirements for monitoring in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-monitoring.md)

  - [<span data-ttu-id="8c9a0-113">在 Lync Server 2013 中启用监视</span><span class="sxs-lookup"><span data-stu-id="8c9a0-113">Enabling monitoring in Lync Server 2013</span></span>](lync-server-2013-enabling-monitoring.md)

  - [<span data-ttu-id="8c9a0-114">访问 Lync Server 2013 中的监视数据</span><span class="sxs-lookup"><span data-stu-id="8c9a0-114">Accessing monitoring data in Lync Server 2013</span></span>](lync-server-2013-accessing-monitoring-data.md)

  - [<span data-ttu-id="8c9a0-115">Lync Server 2013 中用于监控的组件和拓扑</span><span class="sxs-lookup"><span data-stu-id="8c9a0-115">Components and topologies for monitoring in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-monitoring.md)

  - [<span data-ttu-id="8c9a0-116">Lync Server 2013 中监控的部署清单</span><span class="sxs-lookup"><span data-stu-id="8c9a0-116">Deployment checklist for monitoring in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-monitoring.md)

<span data-ttu-id="8c9a0-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c9a0-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

