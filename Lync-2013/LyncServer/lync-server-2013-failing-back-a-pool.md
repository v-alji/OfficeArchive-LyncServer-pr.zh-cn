---
title: Lync Server 2013：对池进行故障回复
description: Lync Server 2013：退回池失败。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428326"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a><span data-ttu-id="31a85-103">在 Lync Server 2013 中对池进行故障回复</span><span class="sxs-lookup"><span data-stu-id="31a85-103">Failing back a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31a85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31a85-104">

<span> </span></span></span>

<span data-ttu-id="31a85-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="31a85-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="31a85-106">在遇到灾难的池重新联机 (也就是说，在此示例) 中，请执行以下步骤将部署还原为正常的工作状态。</span><span class="sxs-lookup"><span data-stu-id="31a85-106">After the pool that experienced the disaster is back online (that is, Pool1 in this example), take the following steps to restore your deployment to regular working status.</span></span>

<span data-ttu-id="31a85-107">请注意，故障回复过程需要几分钟才能完成。</span><span class="sxs-lookup"><span data-stu-id="31a85-107">Note that the failback process takes several minute to complete.</span></span>  <span data-ttu-id="31a85-108">作为参考，对于用户数为 20,000 的池而言，预期最多需要 60 分钟。</span><span class="sxs-lookup"><span data-stu-id="31a85-108">For reference, it is expected to take up to 60 minutes for a pool of 20,000 users.</span></span>

1.  <span data-ttu-id="31a85-109">通过键入以下 cmdlet 对最初驻留在 Pool1 中的用户进行故障回复，并已故障转移到 Pool2：</span><span class="sxs-lookup"><span data-stu-id="31a85-109">Fail back the users who were originally homed in Pool1 and have been failed over to Pool2 by typing the following cmdlet:</span></span>
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

<span data-ttu-id="31a85-110">无需执行其他步骤。</span><span class="sxs-lookup"><span data-stu-id="31a85-110">No other steps are necessary.</span></span> <span data-ttu-id="31a85-111">如果您通过中央管理服务器进行了故障转移，您可以将其保留在 Pool2 中。</span><span class="sxs-lookup"><span data-stu-id="31a85-111">If you failed over the Central Management Server, you can leave it in Pool2.</span></span>

<span data-ttu-id="31a85-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31a85-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

