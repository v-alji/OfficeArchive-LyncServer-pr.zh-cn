---
title: Lync Server 2013 备份注册器关系
description: Lync Server 2013 备份注册机构关系。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup Registrar relationships
ms:assetid: 7e078271-84b9-4666-989c-c4507a0cdf4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205033(v=OCS.15)
ms:contentKeyID: 48184631
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7b0bfce6444ae78c2fb792a6d63dba4bf36b1791
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437915"
---
# <a name="backup-registrar-relationships-in-lync-server-2013"></a><span data-ttu-id="dedcf-103">Lync Server 2013 中的备份注册器关系</span><span class="sxs-lookup"><span data-stu-id="dedcf-103">Backup Registrar relationships in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dedcf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dedcf-104">

<span> </span></span></span>

<span data-ttu-id="dedcf-105">_**主题上次修改时间：** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="dedcf-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="dedcf-106">除了提供灾难恢复功能外，两个配对的池彼此用作对方的备份注册器。</span><span class="sxs-lookup"><span data-stu-id="dedcf-106">In addition to providing disaster recovery ability, two paired pools serve as the backup Registrars for each other.</span></span> <span data-ttu-id="dedcf-107">在 Lync Server 2013 中，前端池之间的备份注册机构关系始终是1:1 和互惠。</span><span class="sxs-lookup"><span data-stu-id="dedcf-107">In Lync Server 2013, backup Registrar relationships between Front End pools are always 1:1 and reciprocal.</span></span> <span data-ttu-id="dedcf-108">这意味着如果 P1 是 P2 的备份，则 P2 必须是 P1 的备份，并且两者都不能是任何其他前端池的备份。</span><span class="sxs-lookup"><span data-stu-id="dedcf-108">This means that if P1 is the backup for P2, then P2 must be the backup for P1, and neither can be the backup for any other Front End pool.</span></span> <span data-ttu-id="dedcf-109">这是 Lync Server 2010 的更改，在这种情况下，前端池备份关系可能是多个。</span><span class="sxs-lookup"><span data-stu-id="dedcf-109">This is a change from Lync Server 2010, in which Front End pool backup relationships could be many to one.</span></span>

<span data-ttu-id="dedcf-110">即使两个前端池之间的备份关系必须是1:1 和对称的，每个前端池也可以是任意数量的 Survivable 分支装置的备份注册机构，就像在 Lync Server 2010 中一样。</span><span class="sxs-lookup"><span data-stu-id="dedcf-110">Even though backup relationships between two Front End pools must be 1:1 and symmetrical, each Front End pool can still also be the backup registrar for any number of Survivable Branch Appliances, just as in Lync Server 2010.</span></span>

<span data-ttu-id="dedcf-111">请注意，Lync Server 2013 不会将灾难恢复支持扩展到托管在 Survivable 分支设备上的用户。</span><span class="sxs-lookup"><span data-stu-id="dedcf-111">Note that Lync Server 2013 does not extend disaster recovery support to users homed on a Survivable Branch Appliance.</span></span> <span data-ttu-id="dedcf-112">如果充当 Survivable 分支设备备份的前端池已关闭，则登录到 Survivable 分支设备的用户即使在前端池上的用户故障转移到备份前端池后也会处于复原模式。</span><span class="sxs-lookup"><span data-stu-id="dedcf-112">If a Front End pool that serves as the backup for a Survivable Branch Appliance goes down, users signed into the Survivable Branch Appliance fall into resiliency mode even after users homed on the Front End pool are failed over to the backup Front End pool.</span></span>

<span data-ttu-id="dedcf-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dedcf-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

