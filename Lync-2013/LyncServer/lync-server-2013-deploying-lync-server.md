---
title: Lync Server 2013：部署 Lync Server
description: Lync Server 2013：部署 Lync 服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Server 2013
ms:assetid: b76795a4-4e71-4c70-a5c0-d1197fa8028c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412892(v=OCS.15)
ms:contentKeyID: 48185197
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 569b1e8b07954f04ee7e4f73de51494ece27157e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429928"
---
# <a name="deploying-lync-server-2013"></a><span data-ttu-id="a3314-103">部署 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3314-103">Deploying Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3314-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3314-104">

<span> </span></span></span>

<span data-ttu-id="a3314-105">_**主题上次修改时间：** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="a3314-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="a3314-106">Lync Server 2013 的部署过程由你决定要安装的 Lync Server 拓扑和组件决定，包括你是要部署前端池还是标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="a3314-106">Your deployment process for Lync Server 2013 is determined by the Lync Server topology and components you decide to install, including whether you want to deploy a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="a3314-107">本节中的主题帮助你确定要部署的环境，并指导你完成部署过程。</span><span class="sxs-lookup"><span data-stu-id="a3314-107">The topics in this section help you determine what environment you want to deploy and guide you through the deployment process.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a3314-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="a3314-108">In This Section</span></span>

  - [<span data-ttu-id="a3314-109">Lync Server 2013 部署概述</span><span class="sxs-lookup"><span data-stu-id="a3314-109">Deployment overview for Lync Server 2013</span></span>](lync-server-2013-deployment-overview.md)

  - [<span data-ttu-id="a3314-110">Lync Server 2013 的系统要求</span><span class="sxs-lookup"><span data-stu-id="a3314-110">System requirements for Lync Server 2013</span></span>](lync-server-2013-system-requirements.md)

  - [<span data-ttu-id="a3314-111">为 Lync Server 2013 准备基础结构和系统</span><span class="sxs-lookup"><span data-stu-id="a3314-111">Preparing the infrastructure and systems for Lync Server 2013</span></span>](lync-server-2013-preparing-the-infrastructure-and-systems.md)

  - [<span data-ttu-id="a3314-112">在 Lync Server 2013 中定义和配置拓扑</span><span class="sxs-lookup"><span data-stu-id="a3314-112">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)

  - [<span data-ttu-id="a3314-113">在 Lync Server 2013 中完成和实施拓扑设计</span><span class="sxs-lookup"><span data-stu-id="a3314-113">Finalizing and implementing the topology design in Lync Server 2013</span></span>](lync-server-2013-finalizing-and-implementing-the-topology-design.md)

  - [<span data-ttu-id="a3314-114">为 Lync Server 2013 设置前端服务器和前端池</span><span class="sxs-lookup"><span data-stu-id="a3314-114">Setting up Front End Servers and Front End pools for Lync Server 2013</span></span>](lync-server-2013-setting-up-front-end-servers-and-front-end-pools.md)

  - [<span data-ttu-id="a3314-115">将 Lync Server 2013 Standard Edition 部署到现有 Lync Server 2013 Enterprise 中</span><span class="sxs-lookup"><span data-stu-id="a3314-115">Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise</span></span>](lync-server-2013-deploying-lync-server-2013-standard-edition-into-an-existing-lync-server-2013-enterprise.md)

  - [<span data-ttu-id="a3314-116">在 Lync Server 2013 中添加服务器角色</span><span class="sxs-lookup"><span data-stu-id="a3314-116">Adding server roles in Lync Server 2013</span></span>](lync-server-2013-adding-server-roles.md)

  - [<span data-ttu-id="a3314-117">在 Lync Server 2013 中设置 Kerberos 身份验证</span><span class="sxs-lookup"><span data-stu-id="a3314-117">Setting up Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-setting-up-kerberos-authentication.md)

<span data-ttu-id="a3314-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3314-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

