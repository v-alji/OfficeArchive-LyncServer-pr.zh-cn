---
title: Lync Server 2013：还原数据和设置
description: Lync Server 2013：还原数据和设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring data and settings
ms:assetid: b07f5dd7-7bed-4819-8cb5-617f5acd478e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202185(v=OCS.15)
ms:contentKeyID: 51541503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694b1e362d729d354b08367d31c47e8ca866dd91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442528"
---
# <a name="restoring-data-and-settings-in-lync-server-2013"></a><span data-ttu-id="7cd1b-103">在 Lync Server 2013 中还原数据和设置</span><span class="sxs-lookup"><span data-stu-id="7cd1b-103">Restoring data and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7cd1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7cd1b-104">

<span> </span></span></span>

<span data-ttu-id="7cd1b-105">_**主题上次修改时间：** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="7cd1b-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="7cd1b-106">如果你已使用配对池实现灾难恢复拓扑，并且其中一个前端池已关闭，并且你需要快速将服务还原到你的用户，请参阅 [在 Lync Server 2013 中故障转移池](lync-server-2013-failing-over-a-pool.md)。</span><span class="sxs-lookup"><span data-stu-id="7cd1b-106">If you have implemented a disaster recovery topology with paired pools, and one of those Front End pools has gone down and you need to quickly restore service to your users, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="7cd1b-107">否则，请使用以下主题中的信息以及 [Lync server 2013 的备份和还原工作表](lync-server-2013-backup-and-restoration-worksheets.md)中的工作表，以在出现故障或中断后还原 Lync Server。</span><span class="sxs-lookup"><span data-stu-id="7cd1b-107">Otherwise, use the information in the following topics, along with the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md), to restore Lync Server after a failure or outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7cd1b-108">若要减少停机时间和潜在的数据丢失，请仅在故障排除过程无法有效识别和更正问题时执行本文档中所述的还原过程。</span><span class="sxs-lookup"><span data-stu-id="7cd1b-108">To reduce downtime and potential data loss, perform the restoration procedures described in this document only if troubleshooting procedures are not effective in identifying and correcting the problem.</span></span> <span data-ttu-id="7cd1b-109">在故障排除过程中，请尝试在关闭并重新启动服务器时尽量减少对其他服务器和组件的影响。</span><span class="sxs-lookup"><span data-stu-id="7cd1b-109">During troubleshooting, try to minimize the impact on other servers and components as you shut down and restart servers.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7cd1b-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="7cd1b-110">In This Section</span></span>

  - [<span data-ttu-id="7cd1b-111">准备还原 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cd1b-111">Preparing to restore Lync Server 2013</span></span>](lync-server-2013-preparing-to-restore-lync-server.md)

  - [<span data-ttu-id="7cd1b-112">在 Lync Server 2013 中还原标准版服务器</span><span class="sxs-lookup"><span data-stu-id="7cd1b-112">Restoring a Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-restoring-a-standard-edition-server.md)

  - [<span data-ttu-id="7cd1b-113">在 Lync Server 2013 中还原托管中央管理存储的服务器</span><span class="sxs-lookup"><span data-stu-id="7cd1b-113">Restoring the server hosting the Central Management store in Lync Server 2013</span></span>](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)

  - [<span data-ttu-id="7cd1b-114">在 Lync Server 2013 中还原企业版后端服务器</span><span class="sxs-lookup"><span data-stu-id="7cd1b-114">Restoring an Enterprise Edition Back End Server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md)

  - [<span data-ttu-id="7cd1b-115">在 Lync Server 2013 中还原企业版成员服务器</span><span class="sxs-lookup"><span data-stu-id="7cd1b-115">Restoring an Enterprise Edition member server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-member-server.md)

  - [<span data-ttu-id="7cd1b-116">在 Lync Server 2013 中还原 Lync 服务器池</span><span class="sxs-lookup"><span data-stu-id="7cd1b-116">Restoring a Lync Server pool in Lync Server 2013</span></span>](lync-server-2013-restoring-a-lync-server-pool.md)

  - [<span data-ttu-id="7cd1b-117">在 Lync Server 2013 中执行 ABC 前端池故障转移</span><span class="sxs-lookup"><span data-stu-id="7cd1b-117">Performing an ABC Front End pool failover in Lync Server 2013</span></span>](lync-server-2013-performing-an-abc-front-end-pool-failover.md)

  - [<span data-ttu-id="7cd1b-118">在 Lync Server 2013 中还原文件存储</span><span class="sxs-lookup"><span data-stu-id="7cd1b-118">Restoring a file store in Lync Server 2013</span></span>](lync-server-2013-restoring-a-file-store.md)

  - [<span data-ttu-id="7cd1b-119">在 Lync Server 2013 中还原监视或存档数据</span><span class="sxs-lookup"><span data-stu-id="7cd1b-119">Restoring monitoring or archiving data in Lync Server 2013</span></span>](lync-server-2013-restoring-monitoring-or-archiving-data.md)

  - [<span data-ttu-id="7cd1b-120">在 Lync Server 2013 中还原永久聊天数据</span><span class="sxs-lookup"><span data-stu-id="7cd1b-120">Restoring Persistent Chat data in Lync Server 2013</span></span>](lync-server-2013-restoring-persistent-chat-data.md)

<span data-ttu-id="7cd1b-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7cd1b-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

