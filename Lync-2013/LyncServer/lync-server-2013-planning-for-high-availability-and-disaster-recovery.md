---
title: Lync Server 2013：规划高可用性和灾难恢复
description: Lync Server 2013：规划高可用性和灾难恢复。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for high availability and disaster recovery
ms:assetid: 15a72073-0336-45dd-b2a0-35e7522c6000
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204703(v=OCS.15)
ms:contentKeyID: 48183497
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6bb5f430201c48738421c4fbe72151ca58173898
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442955"
---
# <a name="planning-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="869c8-103">在 Lync Server 2013 中规划高可用性和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="869c8-103">Planning for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="869c8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="869c8-104">

<span> </span></span></span>

<span data-ttu-id="869c8-105">_**主题上次修改时间：** 2013-10-31_</span><span class="sxs-lookup"><span data-stu-id="869c8-105">_**Topic Last Modified:** 2013-10-31_</span></span>

<span data-ttu-id="869c8-106">与在 Lync Server 2010 中一样，Lync Server 2013 中大多数服务器角色的主高可用性方案都基于服务器冗余（通过池划分）。</span><span class="sxs-lookup"><span data-stu-id="869c8-106">As in Lync Server 2010, the main high availability scheme for most server roles in Lync Server 2013 is based on server redundancy via pooling.</span></span> <span data-ttu-id="869c8-107">如果运行特定服务器角色的服务器发生故障，则池中运行相同角色的其他服务器将承担该服务器的负载。</span><span class="sxs-lookup"><span data-stu-id="869c8-107">If a server running a certain server role fails, the other servers in the pool running the same role take the load of that server.</span></span> <span data-ttu-id="869c8-108">这适用于前端服务器、边缘服务器、中介服务器和控制器。</span><span class="sxs-lookup"><span data-stu-id="869c8-108">This applies to Front End Servers, Edge Servers, Mediation Servers, and Directors.</span></span>

<span data-ttu-id="869c8-109">Lync Server 2013 通过将服务器的地理 dispersement 引入两个数据中心来为前端池添加新的灾难恢复措施，以便在一个整个池或网站停机时提供服务的延续。</span><span class="sxs-lookup"><span data-stu-id="869c8-109">Lync Server 2013 adds new disaster recovery measures for Front End pools by introducing geographical dispersement of your servers into two data centers to provide continuation of service should one entire pool or site go down.</span></span>

<span data-ttu-id="869c8-110">Lync Server 2013 还支持后端数据库的同步 SQL 镜像，从而增强了后端服务器高可用性。</span><span class="sxs-lookup"><span data-stu-id="869c8-110">Lync Server 2013 also enhances Back End Server high availability, by supporting synchronous SQL mirroring for your Back End databases.</span></span>

<span data-ttu-id="869c8-111">本部分介绍这些主要的高可用性和灾难恢复功能，还介绍了为其他服务器角色执行高可用性和灾难恢复时可以采取的步骤。</span><span class="sxs-lookup"><span data-stu-id="869c8-111">This section explains these major high availability and disaster recovery features, and also covers what steps you can take for high availability and disaster recovery for your other server roles as well.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="869c8-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="869c8-112">In This Section</span></span>

  - [<span data-ttu-id="869c8-113">Lync Server 2013 中的前端池灾难恢复</span><span class="sxs-lookup"><span data-stu-id="869c8-113">Front End pool disaster recovery in Lync Server 2013</span></span>](lync-server-2013-front-end-pool-disaster-recovery.md)

  - [<span data-ttu-id="869c8-114">Lync Server 2013 中的边缘服务器灾难恢复</span><span class="sxs-lookup"><span data-stu-id="869c8-114">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)

  - [<span data-ttu-id="869c8-115">在 Lync Server 2013 中规划企业语音恢复能力</span><span class="sxs-lookup"><span data-stu-id="869c8-115">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="869c8-116">Lync Server 2013 中实现灾难恢复的呼叫管理功能</span><span class="sxs-lookup"><span data-stu-id="869c8-116">Call management features for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-call-management-features-for-disaster-recovery.md)

  - [<span data-ttu-id="869c8-117">在 Lync Server 2013 中为持久聊天服务器配置高可用性和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="869c8-117">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="869c8-118">Lync Server 2010 都市站点恢复能力</span><span class="sxs-lookup"><span data-stu-id="869c8-118">Lync Server 2010 metropolitan site resiliency</span></span>](lync-server-2013-compatibility-with-lync-server-2010-metropolitan-site-resiliency.md)

<span data-ttu-id="869c8-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="869c8-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

