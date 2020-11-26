---
title: 验证配置设置的复制
description: 验证配置设置的复制。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Validate replication of configuration settings
ms:assetid: 81a3c21d-b28a-4287-adac-11791e8db56d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205042(v=OCS.15)
ms:contentKeyID: 48184663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26d8e9326da8b865f4e2ca3181975fb899300636
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446533"
---
# <a name="validate-replication-of-configuration-settings"></a><span data-ttu-id="3f7a6-103">验证配置设置的复制</span><span class="sxs-lookup"><span data-stu-id="3f7a6-103">Validate replication of configuration settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f7a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f7a6-104">

<span> </span></span></span>

<span data-ttu-id="3f7a6-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="3f7a6-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="3f7a6-106">你可以通过在中央管理存储所在的内部计算机上运行 Lync Server 2013 cmdlet，或者在安装了 Lync Server 2013 核心组件的任何加入域的计算机上运行 Lync Server for **CsManagementStoreReplicationStatus** cmdlet 来验证配置信息到边缘服务器的复制。</span><span class="sxs-lookup"><span data-stu-id="3f7a6-106">You can validate the replication of configuration information to the Edge Server by running the Lync Server 2013 **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located or any domain joined computer on which Lync Server 2013 Core Components is installed.</span></span>

<span data-ttu-id="3f7a6-107">初始结果可能表明状态为 "False"，而不是 "True" 用于复制。</span><span class="sxs-lookup"><span data-stu-id="3f7a6-107">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="3f7a6-108">如果是这样，请运行 **CsManagementStoreReplication** cmdlet 并留出时间，以便在再次运行 **CsManagementStoreReplicationStatus** cmdlet 之前完成复制。</span><span class="sxs-lookup"><span data-stu-id="3f7a6-108">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** cmdlet again.</span></span>

<span data-ttu-id="3f7a6-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f7a6-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

