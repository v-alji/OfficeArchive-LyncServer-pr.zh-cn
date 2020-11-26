---
title: Lync Server 2013：为用户设置存档策略
description: Lync Server 2013：为用户设置存档策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Archiving policies for users
ms:assetid: 1bbb45df-0590-4c66-9d65-d25526f57790
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204722(v=OCS.15)
ms:contentKeyID: 48183549
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c18a15c1a0611f49a6fd9a4983f3ce87104332e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444761"
---
# <a name="setting-up-archiving-policies-for-users-in-lync-server-2013"></a><span data-ttu-id="15e90-103">为 Lync Server 2013 中的用户设置存档策略</span><span class="sxs-lookup"><span data-stu-id="15e90-103">Setting up Archiving policies for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15e90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15e90-104">

<span> </span></span></span>

<span data-ttu-id="15e90-105">_**主题上次修改时间：** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="15e90-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="15e90-106">你可以通过为用户创建和配置存档策略，然后将策略应用于特定用户或用户组，为特定用户启用或禁用存档。</span><span class="sxs-lookup"><span data-stu-id="15e90-106">You can enable or disable Archiving for specific users by creating and configuring an Archiving policy for users, and then applying the policy to specific users or user groups.</span></span> <span data-ttu-id="15e90-107">用户策略会覆盖任何全局策略或站点策略。</span><span class="sxs-lookup"><span data-stu-id="15e90-107">User policies override any global policy or site policies.</span></span> <span data-ttu-id="15e90-108">仅当你不使用 Microsoft Exchange 集成时，或者，如果你使用的是 Microsoft Exchange 集成，但某些用户未托管在 Exchange 2013 上，并且其邮箱置于 In-Place 保留状态，则仅适用于存档策略。</span><span class="sxs-lookup"><span data-stu-id="15e90-108">Archiving policies only apply if you do not use Microsoft Exchange integration or, if you do use Microsoft Exchange integration, but have some users who are not homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="15e90-109">有关存档策略的工作原理的详细信息（包括全局、网站和用户策略的层次结构），请参阅 [Lync Server 2013 中的存档如何工作](lync-server-2013-how-archiving-works.md) 规划文档、部署文档或操作文档。</span><span class="sxs-lookup"><span data-stu-id="15e90-109">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="15e90-110">如果为你的部署启用 Microsoft Exchange 集成，Exchange In-Place 保留策略控制是否为托管在 Exchange 2013 上的用户启用存档，并将其邮箱置于 In-Place 保留状态。</span><span class="sxs-lookup"><span data-stu-id="15e90-110">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="15e90-111">有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="15e90-111">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="15e90-112">在存档策略中启用内部或外部通信存档之前，应在存档配置中指定所有相应的选项。</span><span class="sxs-lookup"><span data-stu-id="15e90-112">You should specify all appropriate options in the Archiving configurations before enabling Archiving of internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="15e90-113">有关详细信息，请参阅部署文档中 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 中的 "配置存档选项</A> "。</span><span class="sxs-lookup"><span data-stu-id="15e90-113">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="15e90-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="15e90-114">In This Section</span></span>

  - [<span data-ttu-id="15e90-115">在 Lync Server 2013 中设置用于存档的用户策略</span><span class="sxs-lookup"><span data-stu-id="15e90-115">Setting up user policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md)

  - [<span data-ttu-id="15e90-116">使用 Exchange Server 集成时，在 Lync Server 2013 中设置存档策略</span><span class="sxs-lookup"><span data-stu-id="15e90-116">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</span></span>](lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md)

<span data-ttu-id="15e90-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15e90-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

