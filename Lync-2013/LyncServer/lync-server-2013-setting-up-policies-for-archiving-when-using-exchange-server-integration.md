---
title: 使用 Exchange Server 集成时设置存档策略
description: 在使用 Exchange Server 集成时设置存档策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up policies for Archiving when using Exchange Server integration
ms:assetid: 8b9b2bad-a4b3-42e1-85a7-04022e9442ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205063(v=OCS.15)
ms:contentKeyID: 48184742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8281d27101c049b1029a2005ed062a934438afc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444719"
---
# <a name="setting-up-policies-for-archiving-in-lync-server-2013-when-using-exchange-server-integration"></a><span data-ttu-id="63e32-103">使用 Exchange Server 集成时，在 Lync Server 2013 中设置存档策略</span><span class="sxs-lookup"><span data-stu-id="63e32-103">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63e32-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63e32-104">

<span> </span></span></span>

<span data-ttu-id="63e32-105">_**主题上次修改时间：** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="63e32-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="63e32-106">如果托管在 Exchange 2013 上的用户将其邮箱放在 In-Place 保留，Exchange In-Place 保留策略控制这些用户的存档。</span><span class="sxs-lookup"><span data-stu-id="63e32-106">If users homed on Exchange 2013 have their mailboxes put on In-Place Hold, Exchange In-Place Hold policies control archiving for those users.</span></span> <span data-ttu-id="63e32-107">如果你针对你的部署使用 Microsoft Exchange 集成，Exchange 2013 策略将覆盖托管在 Exchange 2013 上的用户的 Lync Server 存档策略。</span><span class="sxs-lookup"><span data-stu-id="63e32-107">If you use Microsoft Exchange integration for your deployment, Exchange 2013 policies override Lync Server Archiving policies for users who are homed on Exchange 2013.</span></span> <span data-ttu-id="63e32-108">有关配置 Exchange 存档策略的信息，请参阅 Exchange 2013 文档。</span><span class="sxs-lookup"><span data-stu-id="63e32-108">For information about configuring Exchange Archiving policies, see the Exchange 2013 documentation.</span></span> <span data-ttu-id="63e32-109">有关为驻留在 Lync Server 2013 上的用户设置用户策略的详细信息，请参阅部署文档中的在 [Lync Server 2013 中设置用于存档的用户策略](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="63e32-109">For details about setting up user policies for users homed on Lync Server 2013, see [Setting up user policies for Archiving in Lync Server 2013](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md) in the Deployment documentation.</span></span> <span data-ttu-id="63e32-110">有关策略如何工作的详细信息，请参阅规划文档、部署文档或操作文档中的在 [Lync Server 2013 中的存档的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="63e32-110">For details about how policies work, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="63e32-111">如果在同一林中部署 Exchange 2013 和 Lync Server 2013，Exchange 2013 In-Place 保留策略控制存档。</span><span class="sxs-lookup"><span data-stu-id="63e32-111">If you deploy Exchange 2013 and Lync Server 2013 in the same forest, your Exchange 2013 In-Place Hold policies control archiving.</span></span> <span data-ttu-id="63e32-112">如果在单独的目录林中部署 Exchange 2013 和 Lync Server 2013，请参阅在 <A href="lync-server-2013-deployment-checklist-for-archiving.md">Lync server 2013 中的存档部署清单中的</A>"部署 Lync 服务器和 Microsoft Exchange 其他林中"。</span><span class="sxs-lookup"><span data-stu-id="63e32-112">If you deploy Exchange 2013 and Lync Server 2013 in separate forests, see “Deploying Lync Server and Microsoft Exchange in Different Forests” in <A href="lync-server-2013-deployment-checklist-for-archiving.md">Deployment checklist for Archiving in Lync Server 2013</A>.</span></span>



<span data-ttu-id="63e32-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63e32-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

