---
title: Lync Server 2013：灾难期间管理响应组
description: Lync Server 2013：在灾难期间管理响应组。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing response groups during a disaster
ms:assetid: 9f14e677-7be8-4f08-88ba-444ec2148ce8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688154(v=OCS.15)
ms:contentKeyID: 49733757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16018f170395e4657daf4405798be05c6da62581
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446057"
---
# <a name="managing-response-groups-in-lync-server-2013-during-a-disaster"></a><span data-ttu-id="5c514-103">灾难期间在 Lync Server 2013 中管理响应组</span><span class="sxs-lookup"><span data-stu-id="5c514-103">Managing response groups in Lync Server 2013 during a disaster</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c514-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c514-104">

<span> </span></span></span>

<span data-ttu-id="5c514-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5c514-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5c514-106">Lync Server 2013 支持在灾难恢复期间在备份池中运行响应组。</span><span class="sxs-lookup"><span data-stu-id="5c514-106">Lync Server 2013 supports running response groups in the backup pool during disaster recovery.</span></span> <span data-ttu-id="5c514-107">本部分介绍了如何在中断期间规划响应组、在中断期间响应组的工作方式，以及故障转移和故障回复响应组所需的步骤。</span><span class="sxs-lookup"><span data-stu-id="5c514-107">This section describes how to plan for response groups during an outage, how response groups work during the outage, and the steps required to fail over and fail back response groups.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5c514-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="5c514-108">In This Section</span></span>

  - [<span data-ttu-id="5c514-109">在 Lync Server 2013 中规划响应组灾难恢复</span><span class="sxs-lookup"><span data-stu-id="5c514-109">Planning for response group disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-group-disaster-recovery.md)

  - [<span data-ttu-id="5c514-110">池故障期间 Lync Server 2013 中的响应组体验</span><span class="sxs-lookup"><span data-stu-id="5c514-110">Response group experience in Lync Server 2013 during pool failure</span></span>](lync-server-2013-response-group-experience-during-pool-failure.md)

  - [<span data-ttu-id="5c514-111">Lync Server 2013 中的响应组灾难恢复过程</span><span class="sxs-lookup"><span data-stu-id="5c514-111">Response group disaster recovery procedures in Lync Server 2013</span></span>](lync-server-2013-response-group-disaster-recovery-procedures.md)

<span data-ttu-id="5c514-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c514-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

