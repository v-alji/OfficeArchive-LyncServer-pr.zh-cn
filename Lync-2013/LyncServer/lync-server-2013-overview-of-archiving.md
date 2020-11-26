---
title: Lync Server 2013：存档概述
description: Lync Server 2013：存档概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Archiving
ms:assetid: 1e3c2ef1-f561-4f57-8b6a-7d78addc1ed1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204729(v=OCS.15)
ms:contentKeyID: 48183570
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 548d82d6731fd28fafbde5816a7a0dc77a1fcc02
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424826"
---
# <a name="overview-of-archiving-in-lync-server-2013"></a><span data-ttu-id="ac397-103">Lync Server 2013 中的存档概述</span><span class="sxs-lookup"><span data-stu-id="ac397-103">Overview of Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac397-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac397-104">

<span> </span></span></span>

<span data-ttu-id="ac397-105">_**主题上次修改时间：** 2013-09-30_</span><span class="sxs-lookup"><span data-stu-id="ac397-105">_**Topic Last Modified:** 2013-09-30_</span></span>

<span data-ttu-id="ac397-106">Lync Server 2013 中的存档提供了一种存档通过 Lync Server 2013 发送的通信的方式。</span><span class="sxs-lookup"><span data-stu-id="ac397-106">Archiving in Lync Server 2013 provides a way for you to archive communications that are sent through Lync Server 2013.</span></span>

<span data-ttu-id="ac397-107">你可以在初始 Lync Server 2013 部署中实现存档，也可以将其添加到现有部署。</span><span class="sxs-lookup"><span data-stu-id="ac397-107">You can implement Archiving as part of your initial Lync Server 2013 deployment, or you can add it to an existing deployment.</span></span> <span data-ttu-id="ac397-108">若要使用 Lync Server 2013 存档数据库 (SQL Server 数据库) 以存储存档数据，请使用拓扑生成器将数据库添加到拓扑，然后再次发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="ac397-108">To use Lync Server 2013 Archiving databases (SQL Server databases) for storage of archiving data, you use Topology Builder to add the databases to your topology, and then publish the topology again.</span></span> <span data-ttu-id="ac397-109">如果你的所有用户都托管在 Exchange 2013 上，并且其邮箱放在 In-Place 保留，则不必更新拓扑，但只需启用 Microsoft Exchange 集成即可将已存档的数据存储在 Exchange 2013 中。</span><span class="sxs-lookup"><span data-stu-id="ac397-109">If all your users are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, you do not have to update your topology, but only need to enable Microsoft Exchange integration to store archived data in Exchange 2013.</span></span>

<span data-ttu-id="ac397-110">实现存档时，将其配置为指定存档内容。</span><span class="sxs-lookup"><span data-stu-id="ac397-110">When you implement Archiving, you configure it to specify what is archived.</span></span> <span data-ttu-id="ac397-111">默认情况下，不会存档任何内容。</span><span class="sxs-lookup"><span data-stu-id="ac397-111">By default, nothing is archived.</span></span> <span data-ttu-id="ac397-112">使用 Lync Server 2013 控制面板配置和管理存档。</span><span class="sxs-lookup"><span data-stu-id="ac397-112">You configure and manage Archiving by using Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="ac397-113">你可以实现内部通信、外部通信或两者的存档。</span><span class="sxs-lookup"><span data-stu-id="ac397-113">You can implement Archiving for internal communications, external communications, or both.</span></span> <span data-ttu-id="ac397-114">你可以配置整个组织的存档设置，也可以配置特定网站、特定池和特定用户和用户组的存档设置。</span><span class="sxs-lookup"><span data-stu-id="ac397-114">You can configure archiving settings your entire organization and, optionally, for specific sites, specific pools, and specific users and user groups.</span></span> <span data-ttu-id="ac397-115">有关确定组织的相应选项的详细信息，请参阅在规划文档中 [定义 Lync Server 2013 中的存档要求](lync-server-2013-defining-your-requirements-for-archiving.md) 。</span><span class="sxs-lookup"><span data-stu-id="ac397-115">For details about determining the appropriate options for your organization, see [Defining your requirements for Archiving in Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md) in the Planning documentation.</span></span> <span data-ttu-id="ac397-116">有关如何实施存档策略和配置的详细信息以及有关哪些信息可以或无法存档的详细信息，请参阅规划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="ac397-116">For details about how Archiving policies and configurations are implemented, and details about what information can or cannot be archived, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<span data-ttu-id="ac397-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac397-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

