---
title: Lync Server 2013：配置对存档的支持
description: Lync Server 2013：配置对存档的支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Archiving
ms:assetid: 579283fe-909c-46f2-a0c9-52ca1e7d63d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204905(v=OCS.15)
ms:contentKeyID: 48184187
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4209614ed1248ab0caf3cf438a922d569ba79630
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432630"
---
# <a name="configuring-support-for-archiving-in-lync-server-2013"></a><span data-ttu-id="bd280-103">在 Lync Server 2013 中配置存档支持</span><span class="sxs-lookup"><span data-stu-id="bd280-103">Configuring support for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd280-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd280-104">

<span> </span></span></span>

<span data-ttu-id="bd280-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="bd280-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="bd280-106">将存档添加到你的拓扑并发布新的拓扑后，你需要配置有关在部署中最初实现存档的方式的选项，然后配置一个或多个存档策略来为你的部署启用存档，还可以为特定的网站和用户配置一个或多个存档策略。</span><span class="sxs-lookup"><span data-stu-id="bd280-106">After adding Archiving to your topology and publishing the new topology, you need to configure options for how Archiving is initially implemented in your deployment, and then configure one or more Archiving policies to enable Archiving for your deployment and, optionally, for specific sites and users.</span></span> <span data-ttu-id="bd280-107">您可以使用 Lync Server 2013 控制面板执行此操作。</span><span class="sxs-lookup"><span data-stu-id="bd280-107">You can use Lync Server 2013 Control Panel to do this.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bd280-108">部署后，您可以更改存档设置以禁用或启用存档。</span><span class="sxs-lookup"><span data-stu-id="bd280-108">After deployment, you can change Archiving settings to disable or enable Archiving.</span></span> <span data-ttu-id="bd280-109">有关如何实现对日常管理的存档支持或在部署后满足组织中的新要求的详细信息，请参阅操作文档中的 <A href="lync-server-2013-managing-archiving.md">管理 Lync Server 2013 存档</A> 。</span><span class="sxs-lookup"><span data-stu-id="bd280-109">For details about how to implement archiving support for day-to-day management or to meet new requirements in your organization after deployment, see <A href="lync-server-2013-managing-archiving.md">Managing Lync Server 2013 Archiving</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bd280-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="bd280-110">In This Section</span></span>

  - [<span data-ttu-id="bd280-111">在 Lync Server 2013 中配置存档选项</span><span class="sxs-lookup"><span data-stu-id="bd280-111">Configuring Archiving options in Lync Server 2013</span></span>](lync-server-2013-configuring-archiving-options.md)

  - [<span data-ttu-id="bd280-112">在 Lync Server 2013 中配置和分配存档策略</span><span class="sxs-lookup"><span data-stu-id="bd280-112">Configuring and assigning Archiving policies in Lync Server 2013</span></span>](lync-server-2013-configuring-and-assigning-archiving-policies.md)

  - [<span data-ttu-id="bd280-113">在 Lync Server 2013 中启用或禁用向联盟伙伴发送存档免责声明</span><span class="sxs-lookup"><span data-stu-id="bd280-113">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

<span data-ttu-id="bd280-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd280-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

