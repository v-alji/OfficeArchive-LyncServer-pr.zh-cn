---
title: Lync Server 2013：部署概述
description: Lync Server 2013：部署概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment overview
ms:assetid: da67555e-f410-4c37-9996-d511f37da8d1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205305(v=OCS.15)
ms:contentKeyID: 48185555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bb3bac4261783a765b64ab2e81adb107599496b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392305"
---
# <a name="deployment-overview-for-lync-server-2013"></a><span data-ttu-id="bf318-103">Lync Server 2013 部署概述</span><span class="sxs-lookup"><span data-stu-id="bf318-103">Deployment overview for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf318-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf318-104">

<span> </span></span></span>

<span data-ttu-id="bf318-105">_**主题上次修改时间：** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="bf318-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="bf318-106">Lync Server 2013 企业版和 Lync Server 2013 标准版之间的主要区别是标准版不支持企业版中包含的高可用性功能。</span><span class="sxs-lookup"><span data-stu-id="bf318-106">The main difference between Lync Server 2013 Enterprise Edition and Lync Server 2013 Standard Edition is that Standard Edition does not support the high availability features included with Enterprise Edition.</span></span> <span data-ttu-id="bf318-107">为了获得高可用性，你需要将多个前端服务器部署到一个池，然后你可以镜像运行 SQL Server 的服务器。</span><span class="sxs-lookup"><span data-stu-id="bf318-107">For high availability, you need to deploy multiple Front End Servers to a pool and then you can mirror the server running SQL Server.</span></span> <span data-ttu-id="bf318-108">使用企业版，您可以选择 collocate 或定义独立的中介服务器。</span><span class="sxs-lookup"><span data-stu-id="bf318-108">With Enterprise Edition you can choose to collocate or define a stand-alone Mediation Server.</span></span> <span data-ttu-id="bf318-109">监视服务器和存档服务器可以使用运行 SQL Server 的独立服务器。</span><span class="sxs-lookup"><span data-stu-id="bf318-109">The Monitoring Server and Archiving Server can use a stand-alone server running SQL Server.</span></span> <span data-ttu-id="bf318-110">或者，他们可以在数据库服务器上为前端服务器和池运行 SQL Server 实例。</span><span class="sxs-lookup"><span data-stu-id="bf318-110">Or, they can have instances of SQL Server running on the database server for the Front End Servers and pools.</span></span>

<span data-ttu-id="bf318-111">运行 Lync Server 2013 标准版的服务器适用于从组织的主部署中删除的较小组织和远程位置。</span><span class="sxs-lookup"><span data-stu-id="bf318-111">Servers running Lync Server 2013 Standard Edition are intended for smaller organizations and remote locations, which are geographically removed from the organization’s main deployment.</span></span> <span data-ttu-id="bf318-112">在灾难情况下，将两个标准版服务器服务器结合在一起以进行故障转移，从而支持最多5000用户。</span><span class="sxs-lookup"><span data-stu-id="bf318-112">Two Standard Edition server servers paired together for failover in case of disaster can support up to 5,000 users.</span></span> <span data-ttu-id="bf318-113">不能像企业版中的前端服务器那样对标准版服务器进行池化。</span><span class="sxs-lookup"><span data-stu-id="bf318-113">You cannot pool Standard Edition servers like you can Front End Servers in Enterprise Edition.</span></span> <span data-ttu-id="bf318-114">此外，标准版使用的 SQL Server 数据库是运行 SQL Server Express 的 collocated 服务器，设计用于处理标准版服务器工作负荷。</span><span class="sxs-lookup"><span data-stu-id="bf318-114">Also, the SQL Server database that Standard Edition uses is a collocated server running SQL Server Express that is designed to handle Standard Edition server workloads.</span></span> <span data-ttu-id="bf318-115">这并不是说所有角色必须驻留在标准版服务器上。</span><span class="sxs-lookup"><span data-stu-id="bf318-115">This is not to say that all roles must reside on a Standard Edition server.</span></span> <span data-ttu-id="bf318-116">你可以有独立的中介服务器和边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="bf318-116">You can have stand-alone Mediation Servers and Edge Servers.</span></span> <span data-ttu-id="bf318-117">用于中央管理存储的 SQL Server 数据库和适用于 Lync Server 2013 的用途必须驻留在标准版服务器 collocated 上，并与运行 SQL Server 的服务器配合。</span><span class="sxs-lookup"><span data-stu-id="bf318-117">The SQL Server database for the Central Management store and for the purposes of Lync Server 2013 must reside on the Standard Edition server collocated with the server running SQL Server.</span></span> <span data-ttu-id="bf318-118">监视服务器和存档服务器将独立服务器与 SQL Server 数据库结合使用。</span><span class="sxs-lookup"><span data-stu-id="bf318-118">The Monitoring Server and Archiving Server use a stand-alone server with the SQL Server database.</span></span>

<span data-ttu-id="bf318-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf318-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

