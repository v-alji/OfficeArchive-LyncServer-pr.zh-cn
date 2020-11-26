---
title: 将拉伸的持久聊天服务器池用于灾难恢复
description: 使用延长的持久聊天服务器池进行灾难恢复。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using a stretched Persistent Chat Server pool for disaster recovery
ms:assetid: 74c5287e-d70d-490a-9adc-ab419917ddd9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205007(v=OCS.15)
ms:contentKeyID: 48184506
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b83a7226f7b9a49a2676b6222505f53247bd5abf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436088"
---
# <a name="using-a-stretched-persistent-chat-server-pool-for-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="31e06-103">在 Lync Server 2013 中将拉伸的持久聊天服务器池用于灾难恢复</span><span class="sxs-lookup"><span data-stu-id="31e06-103">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31e06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31e06-104">

<span> </span></span></span>

<span data-ttu-id="31e06-105">_**主题上次修改时间：** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="31e06-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="31e06-106">持久聊天服务器的灾难恢复解决方案是在延长的持久聊天服务器池中构建的。</span><span class="sxs-lookup"><span data-stu-id="31e06-106">The disaster recovery solution for Persistent Chat Server is built on a stretched Persistent Chat Server pool.</span></span> <span data-ttu-id="31e06-107">这类似于 Lync Server 2010 中的大都市网站复原;但是， (VLAN) 不需要扩展的虚拟局域网。</span><span class="sxs-lookup"><span data-stu-id="31e06-107">This is similar to metropolitan site resiliency in Lync Server 2010; however, there is no requirement for a stretched virtual local area network (VLAN).</span></span> <span data-ttu-id="31e06-108">通过拉伸持久聊天服务器池，你基本上可以在拓扑中逻辑地配置一个池，但实际上是将服务器放在两个不同数据中心的池中。</span><span class="sxs-lookup"><span data-stu-id="31e06-108">By stretching Persistent Chat Server pool, you essentially configure one pool in the topology logically, but you physically place the servers in the pool in two different data centers.</span></span> <span data-ttu-id="31e06-109">以相同的方式为数据库配置 SQL Server 镜像，并在同一数据中心部署数据库和镜像。</span><span class="sxs-lookup"><span data-stu-id="31e06-109">Configure SQL Server mirroring for the database in the same way, and deploy the database and the mirror in the same data center.</span></span> <span data-ttu-id="31e06-110">需要在辅助数据中心中配置一个备份数据库（在灾难恢复期间，用可选镜像来提供高可用性）。</span><span class="sxs-lookup"><span data-stu-id="31e06-110">You need to configure a backup database in the secondary data center (with an optional mirror to provide high availability during disaster recovery).</span></span> <span data-ttu-id="31e06-111">这是在灾难恢复期间用于故障转移的备份数据库。</span><span class="sxs-lookup"><span data-stu-id="31e06-111">This is the backup database used for failover during disaster recovery.</span></span>

<span data-ttu-id="31e06-112">有关如何配置 SQL Server 镜像以获得高可用性的详细信息，请参阅 [Lync Server 2013 中的 SQL server 镜像](lync-server-2013-sql-server-mirroring.md)。</span><span class="sxs-lookup"><span data-stu-id="31e06-112">For details about how to configure SQL Server mirroring for high availability, see [SQL Server mirroring in Lync Server 2013](lync-server-2013-sql-server-mirroring.md).</span></span> <span data-ttu-id="31e06-113">有关故障恢复数据库以进行灾难恢复的详细信息，请参阅 [在 Lync server 2013 中为持久聊天服务器主数据库设置 Sql Server 日志传送](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md) ，以及 [在 lync server 2013 中的主镜像和日志传送辅助数据库之间设置 Sql server 日志传送](lync-server-2013-set-up-log-shipping-secondary-database.md)。</span><span class="sxs-lookup"><span data-stu-id="31e06-113">For details about failing over the database for disaster recovery, see [Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md) and [Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013](lync-server-2013-set-up-log-shipping-secondary-database.md).</span></span>

<span data-ttu-id="31e06-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31e06-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

