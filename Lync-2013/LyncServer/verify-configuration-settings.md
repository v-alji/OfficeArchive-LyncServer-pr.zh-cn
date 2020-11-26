---
title: 验证配置设置
description: 验证配置设置。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify configuration settings
ms:assetid: 51c2d1d9-63f7-43ab-88ca-b8913da7cede
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204885(v=OCS.15)
ms:contentKeyID: 48184111
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7bb1135e95dafe51e906768fe0f4f0d57bf2d6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423342"
---
# <a name="verify-configuration-settings"></a><span data-ttu-id="593b2-103">验证配置设置</span><span class="sxs-lookup"><span data-stu-id="593b2-103">Verify configuration settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="593b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="593b2-104">

<span> </span></span></span>

<span data-ttu-id="593b2-105">_**主题上次修改时间：** 2012-09-06_</span><span class="sxs-lookup"><span data-stu-id="593b2-105">_**Topic Last Modified:** 2012-09-06_</span></span>

<span data-ttu-id="593b2-106">你可以通过在中央管理存储所在的内部计算机上运行 Lync Server 2013 **CsManagementStoreReplicationStatus** cmdlet，或在已加入的任何域的计算机上安装了 lync Server 2013 核心组件 ( # A0) 来验证配置信息到边缘服务器的复制。</span><span class="sxs-lookup"><span data-stu-id="593b2-106">You can validate the replication of configuration information to the Edge server by running the Lync Server 2013 **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located, or on any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span>

<span data-ttu-id="593b2-107">初始结果可能表明状态为 "False"，而不是 "True" 用于复制。</span><span class="sxs-lookup"><span data-stu-id="593b2-107">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="593b2-108">如果是这样，请运行 **CsManagementStoreReplication** cmdlet 并等待复制完成，然后再再次运行 **Get CsManagementStoreReplicationStatus** 。</span><span class="sxs-lookup"><span data-stu-id="593b2-108">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="593b2-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="593b2-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

