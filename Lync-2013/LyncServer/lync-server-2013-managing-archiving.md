---
title: Lync Server 2013：管理存档
description: Lync Server 2013：管理存档。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013 Archiving
ms:assetid: 48c6cc8c-c2c1-4534-9a8a-fd5eb738076a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520990(v=OCS.15)
ms:contentKeyID: 48184003
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c7010645f36a7144ea508447d2c628bc8feacb0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425974"
---
# <a name="managing-lync-server-2013-archiving"></a><span data-ttu-id="5cbb9-103">管理 Lync Server 2013 存档</span><span class="sxs-lookup"><span data-stu-id="5cbb9-103">Managing Lync Server 2013 Archiving</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5cbb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5cbb9-104">

<span> </span></span></span>

<span data-ttu-id="5cbb9-105">_**主题上次修改时间：** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="5cbb9-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="5cbb9-106">为组织部署存档时，请在部署期间指定初始配置。</span><span class="sxs-lookup"><span data-stu-id="5cbb9-106">When you deploy Archiving for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="5cbb9-107">但是，有时你可能希望更改为日常管理实现存档支持的方式，或者满足你的组织中的新要求。</span><span class="sxs-lookup"><span data-stu-id="5cbb9-107">However, there may be times when you want to change how you implement archiving support for day-to-day management or to meet new requirements in your organization.</span></span> <span data-ttu-id="5cbb9-108">例如，你可能需要为组织中的特定网站、池或用户设置不同的存档支持。</span><span class="sxs-lookup"><span data-stu-id="5cbb9-108">For example, you may need to set up archiving support differently for a specific site, pool, or users within your organization.</span></span> <span data-ttu-id="5cbb9-109">对于驻留在 Lync Server 2013 上的用户，你可以创建和自定义存档策略和配置。</span><span class="sxs-lookup"><span data-stu-id="5cbb9-109">For users homed on Lync Server 2013, you do this be creating and customizing archiving policies and configurations.</span></span> <span data-ttu-id="5cbb9-110">如果使用 Microsoft Exchange 集成，还必须配置 Exchange 2013 设置。</span><span class="sxs-lookup"><span data-stu-id="5cbb9-110">If you use Microsoft Exchange integration, you must also configure Exchange 2013 settings.</span></span> <span data-ttu-id="5cbb9-111">本部分提供了使你能够更改存档部署的信息和过程。</span><span class="sxs-lookup"><span data-stu-id="5cbb9-111">This section provides information and procedures to enable you to make changes to your Archiving deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5cbb9-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="5cbb9-112">In This Section</span></span>

  - [<span data-ttu-id="5cbb9-113">在 Lync Server 2013 中存档的工作方式</span><span class="sxs-lookup"><span data-stu-id="5cbb9-113">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)

  - [<span data-ttu-id="5cbb9-114">在 Lync Server 2013 中管理内部和外部通信的存档</span><span class="sxs-lookup"><span data-stu-id="5cbb9-114">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)

  - [<span data-ttu-id="5cbb9-115">管理您的组织、网站和池的 Lync Server 2013 中的存档配置选项</span><span class="sxs-lookup"><span data-stu-id="5cbb9-115">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)

  - [<span data-ttu-id="5cbb9-116">在 Lync Server 2013 中更改存档数据库选项</span><span class="sxs-lookup"><span data-stu-id="5cbb9-116">Changing Archiving database options in Lync Server 2013</span></span>](lync-server-2013-changing-archiving-database-options.md)

  - [<span data-ttu-id="5cbb9-117">从 Lync Server 2013 导出已存档的数据</span><span class="sxs-lookup"><span data-stu-id="5cbb9-117">Exporting archived data from Lync Server 2013</span></span>](lync-server-2013-exporting-archived-data.md)

<span data-ttu-id="5cbb9-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5cbb9-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

