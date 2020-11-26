---
title: Lync Server 2013：通过 System Center Operations Manager 监视 Lync 服务器
description: Lync Server 2013：通过 System Center Operations Manager 监视 Lync 服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Lync 2013 with SCOM
ms:assetid: a74bde92-97ff-4d90-acb9-7a70272f0f31
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720343(v=OCS.15)
ms:contentKeyID: 63969636
ms.date: 05/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ad93c47ab8d157b1e18b4bccc5094408f3d68ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425407"
---
# <a name="monitoring-lync-server-2013-with-system-center-operations-manager"></a><span data-ttu-id="dc505-103">通过 System Center Operations Manager 监视 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc505-103">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc505-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc505-104">

<span> </span></span></span>

<span data-ttu-id="dc505-105">_**主题上次修改时间：** 2015-05-06_</span><span class="sxs-lookup"><span data-stu-id="dc505-105">_**Topic Last Modified:** 2015-05-06_</span></span>

<span data-ttu-id="dc505-106">Lync Server 管理包 (MP) 是监视任何 Lync Server 部署选择的监视解决方案。</span><span class="sxs-lookup"><span data-stu-id="dc505-106">The Lync Server Management Pack (MP) is your monitoring solution of choice for monitoring any Lync Server deployment.</span></span>

<span data-ttu-id="dc505-107">MP 实现传统的事件日志和性能计数器的检测，并在 Lync Server 中启用新可用的检测，例如对多个关键运行状况指标的配对事件 (失败/成功) ，以及完全实现新的合成事务 (Test-Cs \* Windows PowerShell cmdlet) 。</span><span class="sxs-lookup"><span data-stu-id="dc505-107">The MP implements traditional Event Log and Performance counter-based instrumentation and enables newly available instrumentation in Lync Server, such as pair events (failure/success) for several Key Health Indicators, and also fully implements the new Synthetic Transactions (Test-Cs\* Windows PowerShell cmdlets).</span></span>

<span data-ttu-id="dc505-108">您可以在上找到 Lync Server 2013 管理包及其相关文档 [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468) 。</span><span class="sxs-lookup"><span data-stu-id="dc505-108">You can find the Lync Server 2013 Management Pack and its related documentation at [https://go.microsoft.com/fwlink/p/?LinkId=400468](https://go.microsoft.com/fwlink/p/?linkid=400468).</span></span> <span data-ttu-id="dc505-109">如果你运行的是 System Center Operations Manager 2012，则建议这样做。</span><span class="sxs-lookup"><span data-stu-id="dc505-109">This is recommended if you are running System Center Operations Manager 2012.</span></span>

<span data-ttu-id="dc505-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc505-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

