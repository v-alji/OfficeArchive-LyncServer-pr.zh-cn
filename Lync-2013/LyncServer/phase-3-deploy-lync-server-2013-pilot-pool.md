---
title: 第3阶段：部署 Lync Server 2013 试验池
description: 第3阶段：部署 Lync Server 2013 试验池。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Phase 3: Deploy Lync Server 2013 pilot pool'
ms:assetid: f12b1517-fb56-4ded-8323-57aa9fc9ea48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205367(v=OCS.15)
ms:contentKeyID: 48185778
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f72f0cdd2e7d3b9e29891a4adc0ab0551539f465
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438454"
---
# <a name="phase-3-deploy-lync-server-2013-pilot-pool"></a><span data-ttu-id="9a041-103">第3阶段：部署 Lync Server 2013 试验池</span><span class="sxs-lookup"><span data-stu-id="9a041-103">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a041-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a041-104">

<span> </span></span></span>

<span data-ttu-id="9a041-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="9a041-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="9a041-106">本部分介绍了部署 Lync Server 2013 的引导池所需的步骤。</span><span class="sxs-lookup"><span data-stu-id="9a041-106">This section covers the steps required to deploy a pilot pool of Lync Server 2013.</span></span> <span data-ttu-id="9a041-107">Lync Server 2013 的部署需要使用拓扑生成器来定义你的拓扑和要部署的组件，为部署 Lync Server 2013 组件准备环境，在第一台前端服务器上发布拓扑设计，然后为你的部署安装并配置该组件的 Lync Server 2013 软件。</span><span class="sxs-lookup"><span data-stu-id="9a041-107">The deployment of Lync Server 2013 requires using Topology Builder to define your topology and the components you want to deploy, preparing your environment for deployment of the Lync Server 2013 components, publishing your topology design on the first Front End Server, and then installing and configuring Lync Server 2013 software for the components for your deployment.</span></span> <span data-ttu-id="9a041-108">完成后，您的 Lync Server 2013 试验池部署将与现有 Lync Server 2010 池共存。</span><span class="sxs-lookup"><span data-stu-id="9a041-108">When completed, your Lync Server 2013 pilot pool deployment will coexist with an existing Lync Server 2010 pool.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9a041-109">本节内容</span><span class="sxs-lookup"><span data-stu-id="9a041-109">In This Section</span></span>

  - [<span data-ttu-id="9a041-110">为 Lync Server 准备 Active Directory</span><span class="sxs-lookup"><span data-stu-id="9a041-110">Prepare Active Directory for Lync Server</span></span>](prepare-active-directory-for-lync-server.md)

  - [<span data-ttu-id="9a041-111">从现有部署下载拓扑</span><span class="sxs-lookup"><span data-stu-id="9a041-111">Download topology from existing deployment</span></span>](download-topology-from-existing-deployment.md)

  - [<span data-ttu-id="9a041-112">部署 Lync Server 2013 试验池</span><span class="sxs-lookup"><span data-stu-id="9a041-112">Deploy Lync Server 2013 pilot pool</span></span>](deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="9a041-113">验证试点池与旧池的共存情况</span><span class="sxs-lookup"><span data-stu-id="9a041-113">Verify pilot pool coexistence with legacy pool</span></span>](verify-pilot-pool-coexistence-with-legacy-pool.md)

  - [<span data-ttu-id="9a041-114">将试点池连接到旧 Edge Server</span><span class="sxs-lookup"><span data-stu-id="9a041-114">Connect pilot pool to legacy Edge Servers</span></span>](connect-pilot-pool-to-legacy-edge-servers.md)

  - [<span data-ttu-id="9a041-115">配置 XMPP 网关访问策略和证书</span><span class="sxs-lookup"><span data-stu-id="9a041-115">Configure XMPP gateway access policies and certificates</span></span>](configure-xmpp-gateway-access-policies-and-certificates.md)

<span data-ttu-id="9a041-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a041-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

