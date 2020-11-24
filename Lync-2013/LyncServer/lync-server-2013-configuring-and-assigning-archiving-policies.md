---
title: Lync Server 2013：配置和分配存档策略
description: Lync Server 2013：配置和分配存档策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring and assigning Archiving policies
ms:assetid: acd18ea8-c7f1-4178-871a-cd3b75bdaa8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205175(v=OCS.15)
ms:contentKeyID: 48185121
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebe08715433e04e56758c7fb09b331065fbd6f44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392161"
---
# <a name="configuring-and-assigning-archiving-policies-in-lync-server-2013"></a><span data-ttu-id="ff52e-103">在 Lync Server 2013 中配置和分配存档策略</span><span class="sxs-lookup"><span data-stu-id="ff52e-103">Configuring and assigning Archiving policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff52e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff52e-104">

<span> </span></span></span>

<span data-ttu-id="ff52e-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="ff52e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="ff52e-106">在 Lync Server 2013 中，你可以使用策略为托管于 Lync Server 2013 的用户启用和禁用内部通信和外部通信的存档。</span><span class="sxs-lookup"><span data-stu-id="ff52e-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users who are homed on Lync Server 2013.</span></span> <span data-ttu-id="ff52e-107">这包括以下存档策略：</span><span class="sxs-lookup"><span data-stu-id="ff52e-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="ff52e-108">部署 Lync Server 2013 时默认创建的全局策略。</span><span class="sxs-lookup"><span data-stu-id="ff52e-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="ff52e-109">可创建和使用的可选网站级和用户级策略，用于指定如何为特定网站或用户实现存档。</span><span class="sxs-lookup"><span data-stu-id="ff52e-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="ff52e-110">你在部署存档时最初设置存档策略，但你可以在部署后更改、添加和删除策略。</span><span class="sxs-lookup"><span data-stu-id="ff52e-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="ff52e-111">在 Lync Server 2013 控制面板中，你可以使用 "**存档和监视**" 组的 "**存档策略**" 页面管理全局级别、网站级别和用户级别的策略。</span><span class="sxs-lookup"><span data-stu-id="ff52e-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ff52e-112">若要控制存档的实现，必须指定存档配置中的选项，例如，是存档 IM 还是会议、使用关键模式和清除选项。</span><span class="sxs-lookup"><span data-stu-id="ff52e-112">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="ff52e-113">默认情况下，全局存档配置或任何网站或池存档配置中均未启用任何选项。</span><span class="sxs-lookup"><span data-stu-id="ff52e-113">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="ff52e-114">应在存档配置中指定所有适当的选项，然后才能在存档策略中启用内部或外部通信的存档。</span><span class="sxs-lookup"><span data-stu-id="ff52e-114">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="ff52e-115">有关详细信息，请参阅在 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 中为你的组织、网站和池在操作文档中管理存档配置选项</A> 。</span><span class="sxs-lookup"><span data-stu-id="ff52e-115">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="ff52e-116">如果你将 Lync Server 存储与 Exchange 2013 存储集成，则 Exchange 用户策略将优先于 Lync Server 2013 存档策略，但仅适用于托管了 Exchange 2013 的用户在 In-Place 保留的邮箱。</span><span class="sxs-lookup"><span data-stu-id="ff52e-116">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies but only for those users who are homed on Exchange 2013 who have had their mailboxes put on In-Place Hold.</span></span>



</div>

<span data-ttu-id="ff52e-117">有关如何实施策略的详细信息（包括策略的层次结构），请参阅规划文档、部署文档或操作文档中的在 [Lync Server 2013 中的存档的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="ff52e-117">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span> <span data-ttu-id="ff52e-118">有关如何在部署后管理策略的详细信息，请参阅在操作文档中 [管理 Lync Server 2013 中的内部和外部通信的存档](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md) 。</span><span class="sxs-lookup"><span data-stu-id="ff52e-118">For details about how to manage policies after deployment, see [Managing the Archiving of internal and external communications in Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md) in the Operations documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ff52e-119">本节内容</span><span class="sxs-lookup"><span data-stu-id="ff52e-119">In This Section</span></span>

  - [<span data-ttu-id="ff52e-120">在 Lync Server 2013 中配置用于存档的全局策略</span><span class="sxs-lookup"><span data-stu-id="ff52e-120">Configuring the global policy for Archiving in Lync Server 2013</span></span>](lync-server-2013-configuring-the-global-policy-for-archiving.md)

  - [<span data-ttu-id="ff52e-121">在 Lync Server 2013 中设置用于存档的网站策略</span><span class="sxs-lookup"><span data-stu-id="ff52e-121">Setting up site policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-setting-up-site-policies-for-archiving.md)

  - [<span data-ttu-id="ff52e-122">为 Lync Server 2013 中的用户设置存档策略</span><span class="sxs-lookup"><span data-stu-id="ff52e-122">Setting up Archiving policies for users in Lync Server 2013</span></span>](lync-server-2013-setting-up-archiving-policies-for-users.md)

<span data-ttu-id="ff52e-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff52e-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

