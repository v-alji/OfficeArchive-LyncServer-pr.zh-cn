---
title: Lync Server 2013 支持的池配对选项和最佳做法
description: Lync Server 2013 支持的池配对选项和最佳做法。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported pool pairing options and best practices
ms:assetid: 142caf34-0f20-47f3-9d32-ce25ab622fad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204697(v=OCS.15)
ms:contentKeyID: 48183478
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76d0f8331c0b6998008efff8af70ae3c4b43a9c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441415"
---
# <a name="supported-pool-pairing-options-and-best-practices-for-lync-server-2013"></a><span data-ttu-id="0a71a-103">支持 Lync Server 2013 的池配对选项和最佳做法</span><span class="sxs-lookup"><span data-stu-id="0a71a-103">Supported pool pairing options and best practices for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a71a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a71a-104">

<span> </span></span></span>

<span data-ttu-id="0a71a-105">_**主题上次修改时间：** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="0a71a-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="0a71a-106">对两个数据中心之间的距离没有限制，包括彼此配对的前端池。</span><span class="sxs-lookup"><span data-stu-id="0a71a-106">There is no restriction on the distance between two data centers that are to include Front End pools paired with each other.</span></span> <span data-ttu-id="0a71a-107">我们建议你在同一世界地区使用两个数据中心，并在它们之间使用高速链接。</span><span class="sxs-lookup"><span data-stu-id="0a71a-107">We recommend that you use two data centers in the same world region, with high-speed links between them.</span></span> <span data-ttu-id="0a71a-108">最好将两个数据中心分开，以避免一次灾难碰到这两个数据中心。</span><span class="sxs-lookup"><span data-stu-id="0a71a-108">It is best if the two data centers are separated enough to avoid a single disaster hitting both at the same time.</span></span>

<span data-ttu-id="0a71a-109">可以在世界各地有两个数据中心，但由于数据复制中的延迟，可能会导致更高的数据丢失。</span><span class="sxs-lookup"><span data-stu-id="0a71a-109">Having two data centers across world regions is possible, but could incur higher data loss due to latency in data replication.</span></span>

<span data-ttu-id="0a71a-110">当您计划对池进行配对时，必须谨记仅支持以下配对法：</span><span class="sxs-lookup"><span data-stu-id="0a71a-110">When you plan which pools to pair, you must keep in mind that only the following pairings are supported:</span></span>

  - <span data-ttu-id="0a71a-111">Enterprise Edition 池仅能与其他 Enterprise Edition 池进行配对。</span><span class="sxs-lookup"><span data-stu-id="0a71a-111">Enterprise Edition pools can be paired only with other Enterprise Edition pools.</span></span> <span data-ttu-id="0a71a-112">同样，Standard Edition 池仅能与其他 Standard Edition 池进行配对。</span><span class="sxs-lookup"><span data-stu-id="0a71a-112">Similarly, Standard Edition pools can be paired only with other Standard Edition pools.</span></span>

  - <span data-ttu-id="0a71a-113">物理池仅能与其他物理池配对。</span><span class="sxs-lookup"><span data-stu-id="0a71a-113">Physical pools can be paired only with other physical pools.</span></span> <span data-ttu-id="0a71a-114">同样，虚拟池仅能与其他虚拟池配对。</span><span class="sxs-lookup"><span data-stu-id="0a71a-114">Similarly, virtual pools can be paired only with other virtual pools.</span></span>

  - <span data-ttu-id="0a71a-115">配对的池必须运行相同的操作系统。</span><span class="sxs-lookup"><span data-stu-id="0a71a-115">Pools that are paired together must be running the same operating system.</span></span>

<span data-ttu-id="0a71a-p104">拓扑生成器和拓扑验证都不会阻止以不遵循这些建议的方式对两个池进行配对。例如，拓扑生成器允许您将 Enterprise Edition 池与 Standard Edition 池进行配对。但是，不支持进行这些类型的配对。</span><span class="sxs-lookup"><span data-stu-id="0a71a-p104">Neither Topology Builder nor topology validation will prohibit pairing two pools in a way that does not follow these recommendations. For example, Topology Builder allows you to pair an Enterprise Edition pool with a Standard Edition pool. However, these types of pairings are not supported.</span></span>

<span data-ttu-id="0a71a-119">每个池中的每个池都应具有在发生灾难时为来自两个池的所有用户提供服务的容量。</span><span class="sxs-lookup"><span data-stu-id="0a71a-119">Each pool in a pair should have the capacity to serve all users from both pools in the event of a disaster.</span></span>

<span data-ttu-id="0a71a-120">如果你对企业版池进行了配对，你也可以在后端服务器上实现高可用性，但对于标准版池，只有灾难恢复措施可用。</span><span class="sxs-lookup"><span data-stu-id="0a71a-120">If you pair Enterprise Edition pools, you can also implement high availability on the Back End Servers, but for pairs of Standard Edition pools only the disaster recovery measures are available.</span></span>

<span data-ttu-id="0a71a-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a71a-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

