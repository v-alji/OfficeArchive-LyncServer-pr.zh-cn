---
title: 删除后端服务器上的 SQL Server 实例和数据库
description: 删除后端服务器上的 SQL Server 实例和数据库。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove SQL Server instances and databases on the Back End Server
ms:assetid: 32457df9-7dd9-4fca-9362-ea4de26b0296
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688016(v=OCS.15)
ms:contentKeyID: 49733606
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c87426a3496e6def2ad65775f5dadb1a0141ae3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392467"
---
# <a name="remove-sql-server-instances-and-databases-on-the-back-end-server"></a><span data-ttu-id="b4196-103">删除后端服务器上的 SQL Server 实例和数据库</span><span class="sxs-lookup"><span data-stu-id="b4196-103">Remove SQL Server instances and databases on the Back End Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4196-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4196-104">

<span> </span></span></span>

<span data-ttu-id="b4196-105">_**主题上次修改时间：** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="b4196-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="b4196-106">删除依赖于这些服务器的运行 Lync Server 2010 的服务器后，或者在将运行 Lync Server 2010 的服务器重新配置为使用另一个数据库之后，删除 Microsoft SQL Server 数据库和实例。</span><span class="sxs-lookup"><span data-stu-id="b4196-106">You remove the Microsoft SQL Server databases and instances after you remove the servers running Lync Server 2010 that are dependent on them, or after you reconfigure the servers running Lync Server 2010 to use another database.</span></span> <span data-ttu-id="b4196-107">如果你在终止当前 SQL Server 或以某种方式重新配置运行 Lync Server 2010 的当前服务器，以使数据库过时或不可用，则需要执行本主题中的过程。</span><span class="sxs-lookup"><span data-stu-id="b4196-107">You need to perform the procedure in this topic when you retire the current SQL Server or reconfigure the current server running Lync Server 2010 in such a way that it renders the databases obsolete or unavailable.</span></span>

<span data-ttu-id="b4196-108">若要删除存档服务器或监视服务器的数据库或实例，必须首先删除服务器角色。</span><span class="sxs-lookup"><span data-stu-id="b4196-108">To remove the databases or instances for the Archiving Server or Monitoring Server, you must first remove the server role.</span></span> <span data-ttu-id="b4196-109">同样，若要删除前端池的实例或数据库，必须首先删除或重新配置从属服务器角色。</span><span class="sxs-lookup"><span data-stu-id="b4196-109">Similarly, to remove the instances or databases for Front End pool, you must first remove or reconfigure the dependent server role.</span></span> <span data-ttu-id="b4196-110">这些过程不区分 collocated 数据库或服务器的单独实例。</span><span class="sxs-lookup"><span data-stu-id="b4196-110">These procedures make no distinction between collocated databases or separate instances for servers.</span></span> <span data-ttu-id="b4196-111">数据库的 collocation 不会影响这些过程。</span><span class="sxs-lookup"><span data-stu-id="b4196-111">The procedures are unaffected by the collocation of databases.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b4196-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="b4196-112">In This Section</span></span>

  - [<span data-ttu-id="b4196-113">删除前端池的 SQL Server 数据库</span><span class="sxs-lookup"><span data-stu-id="b4196-113">Remove the SQL Server database for a Front End pool</span></span>](remove-the-sql-server-database-for-a-front-end-pool.md)

  - [<span data-ttu-id="b4196-114">删除监控服务器的 SQL Server 数据库</span><span class="sxs-lookup"><span data-stu-id="b4196-114">Remove the SQL Server database for a Monitoring server</span></span>](remove-the-sql-server-database-for-a-monitoring-server.md)

  - [<span data-ttu-id="b4196-115">删除存档服务器的 SQL Server 数据库</span><span class="sxs-lookup"><span data-stu-id="b4196-115">Remove the SQL Server database for an Archiving server</span></span>](remove-the-sql-server-database-for-an-archiving-server.md)

<span data-ttu-id="b4196-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4196-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

