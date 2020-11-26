---
title: Lync Server 2013：控制器概述
description: Lync Server 2013： Director 概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6686534e22bab5b02a2663789298e4cf7ea582c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424707"
---
# <a name="overview-of-the-director-in-lync-server-2013"></a><span data-ttu-id="fd87b-103">Lync Server 2013 中的控制器概述</span><span class="sxs-lookup"><span data-stu-id="fd87b-103">Overview of the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd87b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd87b-104">

<span> </span></span></span>

<span data-ttu-id="fd87b-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="fd87b-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="fd87b-106">Director 是运行 Lync Server 2013 的服务器，用于验证用户请求，但不会在家任何用户帐户。</span><span class="sxs-lookup"><span data-stu-id="fd87b-106">A Director is a server running Lync Server 2013 that authenticates user requests, but does not home any user accounts.</span></span> <span data-ttu-id="fd87b-107">您也可以在以下两种方案中部署控制器：</span><span class="sxs-lookup"><span data-stu-id="fd87b-107">You optionally can deploy a Director in the following two scenarios:</span></span>

  - <span data-ttu-id="fd87b-108">如果通过部署边缘服务器启用外部用户访问，则还应部署 Director。</span><span class="sxs-lookup"><span data-stu-id="fd87b-108">If you enable access by external users by deploying Edge Servers, you should also deploy a Director.</span></span> <span data-ttu-id="fd87b-109">在此方案中，控制器对外部用户进行身份验证，然后将其流量传递到内部服务器。</span><span class="sxs-lookup"><span data-stu-id="fd87b-109">In this scenario, the Director authenticates the external users, and then passes their traffic on to internal servers.</span></span> <span data-ttu-id="fd87b-110">当使用 Director 对外部用户进行身份验证时，它将从执行这些用户的身份验证的开销中免除前端池服务器。</span><span class="sxs-lookup"><span data-stu-id="fd87b-110">When a Director is used to authenticate external users, it relieves Front End pool servers from the overhead of performing authentication of these users.</span></span> <span data-ttu-id="fd87b-111">它还有助于将内部前端池与恶意流量（如拒绝服务攻击）隔离。</span><span class="sxs-lookup"><span data-stu-id="fd87b-111">It also helps insulate internal Front End pools from malicious traffic such as denial-of-service attacks.</span></span> <span data-ttu-id="fd87b-112">如果网络被此类攻击中的无效外部通信所淹没，则该流量将在 Director 处结束。</span><span class="sxs-lookup"><span data-stu-id="fd87b-112">If the network is flooded with invalid external traffic in such an attack, this traffic ends at the Director.</span></span>

  - <span data-ttu-id="fd87b-113">如果在中心网站上部署多个前端池，则通过向该网站添加 Director，可以简化身份验证请求并提高性能。</span><span class="sxs-lookup"><span data-stu-id="fd87b-113">If you deploy multiple Front End pools at a central site, by adding a Director to that site you can streamline authentication requests and improve performance.</span></span> <span data-ttu-id="fd87b-114">在此方案中，所有请求首先转到 Director，然后将其路由到正确的前端池。</span><span class="sxs-lookup"><span data-stu-id="fd87b-114">In this scenario, all requests go first to the Director, which then routes them to the correct Front End pool.</span></span>

<span data-ttu-id="fd87b-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd87b-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

