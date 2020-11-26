---
title: Lync Server 2013：执行 ABC 前端池故障转移
description: Lync Server 2013：执行 ABC 前端池故障转移。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Performing an ABC Front End pool failover
ms:assetid: 81ecd26d-49e3-4c72-a66e-02748efb513b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945637(v=OCS.15)
ms:contentKeyID: 51541489
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0c1aa7a18bc1f1126bcb942a0b3a21283637dcb6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445013"
---
# <a name="performing-an-abc-front-end-pool-failover-in-lync-server-2013"></a><span data-ttu-id="46a75-103">在 Lync Server 2013 中执行 ABC 前端池故障转移</span><span class="sxs-lookup"><span data-stu-id="46a75-103">Performing an ABC Front End pool failover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46a75-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46a75-104">

<span> </span></span></span>

<span data-ttu-id="46a75-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="46a75-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="46a75-106">本部分中的两个主题介绍在 Lync Server 2013 中执行 ABC 池故障转移的过程，其中有成对的 Lync Server 前端池 A 和 B，并且池 A 不可恢复。</span><span class="sxs-lookup"><span data-stu-id="46a75-106">The two topics in this section describe the procedure for performing an ABC pool failover in Lync Server 2013, where there are paired Lync Server Front End pools A and B, and pool A becomes unrecoverable.</span></span> <span data-ttu-id="46a75-107">使用此过程，使用新的完全限定的域名 (FQDN) 创建新的前端池 C。</span><span class="sxs-lookup"><span data-stu-id="46a75-107">Using this procedure, you create a new Front End pool C with a new fully qualified domain name (FQDN).</span></span> <span data-ttu-id="46a75-108">池 C 由故障池 A 中的信息构造。该过程还包括将池 B 和 C 配对到一起。</span><span class="sxs-lookup"><span data-stu-id="46a75-108">Pool C is constructed from the information from failed pool A. The procedure also includes pairing together pools B and C.</span></span>

  - [<span data-ttu-id="46a75-109">Lync Server 2013 中的 ABC 池故障转移的备份先决条件</span><span class="sxs-lookup"><span data-stu-id="46a75-109">Backup prerequisites for ABC pool failover in Lync Server 2013</span></span>](lync-server-2013-backup-prerequisites-for-abc-pool-failover.md)

  - [<span data-ttu-id="46a75-110">Lync Server 2013 中的前端池 ABC 故障转移过程</span><span class="sxs-lookup"><span data-stu-id="46a75-110">Front End pool ABC failover procedure in Lync Server 2013</span></span>](lync-server-2013-front-end-pool-abc-failover-procedure.md)

<span data-ttu-id="46a75-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46a75-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

