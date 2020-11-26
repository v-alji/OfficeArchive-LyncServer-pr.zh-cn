---
title: 为持久聊天服务器配置高可用性和灾难恢复
description: 为高可用性和灾难恢复配置持久聊天服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server for high availability and disaster recovery
ms:assetid: eebc581c-e3a0-4b69-8a43-80b607b4d8f2
ms:mtpsurl: https://technet.microsoft.com/library/JJ205364(v=OCS.15)
ms:contentKeyID: 48185760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13935f2ec690deb7f896c13d185680ce1122a892
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432784"
---
# <a name="configuring-persistent-chat-server-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="f822f-103">在 Lync Server 2013 中为持久聊天服务器配置高可用性和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="f822f-103">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f822f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f822f-104">

<span> </span></span></span>

<span data-ttu-id="f822f-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="f822f-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="f822f-106">Lync Server 2013、持久聊天服务器服务使用 *扩展池* 配置进行灾难恢复。</span><span class="sxs-lookup"><span data-stu-id="f822f-106">The Lync Server 2013, Persistent Chat Server services use a *stretched pool* configuration for disaster recovery.</span></span> <span data-ttu-id="f822f-107">延伸池是一种池，它具有在两个物理数据中心之间分布但位于单个逻辑 Lync 服务器网站内的计算机。</span><span class="sxs-lookup"><span data-stu-id="f822f-107">A stretched pool is a pool that has computers that are distributed between two physical data centers, but are within a single logical Lync Server site.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f822f-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="f822f-108">In This Section</span></span>

  - [<span data-ttu-id="f822f-109">Lync Server 2013 持久聊天服务器所需的资源</span><span class="sxs-lookup"><span data-stu-id="f822f-109">Required resources for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-required-resources-for-persistent-chat-server.md)

  - [<span data-ttu-id="f822f-110">在 Lync Server 2013 中使用拓扑生成器配置高可用性和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="f822f-110">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-topology-builder-to-configure-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="f822f-111">在 Lync Server 2013 中将拉伸的持久聊天服务器池用于灾难恢复</span><span class="sxs-lookup"><span data-stu-id="f822f-111">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-a-stretched-persistent-chat-server-pool-for-disaster-recovery.md)

  - [<span data-ttu-id="f822f-112">Lync Server 2013 中的 SQL Server 镜像</span><span class="sxs-lookup"><span data-stu-id="f822f-112">SQL Server mirroring in Lync Server 2013</span></span>](lync-server-2013-sql-server-mirroring.md)

  - [<span data-ttu-id="f822f-113">在 Lync Server 2013 中为持久聊天服务器主数据库设置 SQL Server 日志传送</span><span class="sxs-lookup"><span data-stu-id="f822f-113">Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database</span></span>](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md)

  - [<span data-ttu-id="f822f-114">在 Lync Server 2013 中在主镜像和日志传送辅助数据库之间设置 SQL Server 日志传送</span><span class="sxs-lookup"><span data-stu-id="f822f-114">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>](lync-server-2013-set-up-log-shipping-secondary-database.md)

<span data-ttu-id="f822f-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f822f-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

