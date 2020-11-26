---
title: Lync Server 2013：在 Lync Server 中设置用于存档的用户策略
description: Lync Server 2013：在 Lync Server 中设置用于存档的用户策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up user policies for Archiving in Lync Server
ms:assetid: 22d6cc76-6b5c-4a8c-bb8a-7996450ec085
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204742(v=OCS.15)
ms:contentKeyID: 48183626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e33abf6cf16c9c1367162aa8beee91874f4c725
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441625"
---
# <a name="setting-up-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="a85be-103">在 Lync Server 2013 中设置用于存档的用户策略</span><span class="sxs-lookup"><span data-stu-id="a85be-103">Setting up user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a85be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a85be-104">

<span> </span></span></span>

<span data-ttu-id="a85be-105">_**主题上次修改时间：** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="a85be-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="a85be-106">为驻留在 Lync Server 2013 上的特定用户启用或禁用存档需要创建和配置一个或多个用户策略，然后将相应的策略应用到特定用户或用户组。</span><span class="sxs-lookup"><span data-stu-id="a85be-106">Enabling or disabling Archiving for specific users homed on Lync Server 2013 requires creating and configuring one or more user policies, and then applying the appropriate policy to specific users or user groups.</span></span> <span data-ttu-id="a85be-107">用户策略替代网站和全局策略，但仅适用于驻留在 Lync Server 2013 上的用户。</span><span class="sxs-lookup"><span data-stu-id="a85be-107">User policies override site and global policies, but only for users homed on Lync Server 2013.</span></span>

<span data-ttu-id="a85be-108">用户始终驻留在 Lync Server 中。</span><span class="sxs-lookup"><span data-stu-id="a85be-108">Users are always homed in Lync Server.</span></span> <span data-ttu-id="a85be-109">如果启用了 Microsoft Exchange 集成，则邮箱位于 Microsoft Exchange Server 2013 中的用户不需要在 Lync Server 托管中拥有其存档策略。</span><span class="sxs-lookup"><span data-stu-id="a85be-109">If Microsoft Exchange integration is enabled, users whose mailboxes are in Microsoft Exchange Server 2013 don’t need to have their Archiving policies in Lync Server managed.</span></span> <span data-ttu-id="a85be-110">这些具有存档的用户将由 Exchange In-Place 保留进行管理。</span><span class="sxs-lookup"><span data-stu-id="a85be-110">These users with Archiving will be managed by Exchange In-Place Hold.</span></span>

<span data-ttu-id="a85be-111">有关存档策略的工作原理的详细信息（包括全局、网站和用户策略的层次结构），请参阅规划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="a85be-111">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a85be-112">如果为你的部署启用了 Microsoft Exchange 集成，Exchange In-Place 保留策略控制是否为托管在 Exchange 2013 上的用户启用存档。</span><span class="sxs-lookup"><span data-stu-id="a85be-112">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013.</span></span> <span data-ttu-id="a85be-113">这些用户的存档要求他们将邮箱放在 In-Place 保留。</span><span class="sxs-lookup"><span data-stu-id="a85be-113">Archiving for these users requires that they have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="a85be-114">有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="a85be-114">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="a85be-115">在启用存档之前，应在存档配置中指定所有适当的选项。</span><span class="sxs-lookup"><span data-stu-id="a85be-115">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="a85be-116">有关详细信息，请参阅部署文档中 <A href="lync-server-2013-configuring-archiving-options.md">Lync Server 2013 中的 "配置存档选项</A> "。</span><span class="sxs-lookup"><span data-stu-id="a85be-116">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a85be-117">本节内容</span><span class="sxs-lookup"><span data-stu-id="a85be-117">In This Section</span></span>

  - [<span data-ttu-id="a85be-118">在 Lync Server 2013 中创建和配置用于存档的用户策略</span><span class="sxs-lookup"><span data-stu-id="a85be-118">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-creating-and-configuring-user-policies-for-archiving-in-lync-server.md)

  - [<span data-ttu-id="a85be-119">将 Lync 服务器存档策略应用于 Lync Server 2013 中的用户</span><span class="sxs-lookup"><span data-stu-id="a85be-119">Applying a Lync Server Archiving policy to a user in Lync Server 2013</span></span>](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md)

<span data-ttu-id="a85be-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a85be-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

