---
title: Lync Server 2013 池故障转移和池故障回复的恢复时间
description: Lync Server 2013 池故障转移和池故障回复的恢复时间。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Recovery time for pool failover and pool failback
ms:assetid: 902c658f-8442-4d0d-b3ad-bf795ecd550d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205079(v=OCS.15)
ms:contentKeyID: 48184786
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bb09c32ac4d062358a511464dc21aa7346ee034
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436676"
---
# <a name="recovery-time-for-pool-failover-and-pool-failback-in-lync-server-2013"></a><span data-ttu-id="e39ca-103">Lync Server 2013 中的池故障转移和池故障回复的恢复时间</span><span class="sxs-lookup"><span data-stu-id="e39ca-103">Recovery time for pool failover and pool failback in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e39ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e39ca-104">

<span> </span></span></span>

<span data-ttu-id="e39ca-105">_**主题上次修改时间：** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="e39ca-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="e39ca-106">对于池故障转移和池故障回复，针对恢复时间目标的工程目标 (RTO) 是30分钟。</span><span class="sxs-lookup"><span data-stu-id="e39ca-106">For pool failover and pool failback, the engineering target for recovery time objective (RTO) is 30 minutes.</span></span> <span data-ttu-id="e39ca-107">这是发生故障转移所需的时间，在管理员确定存在灾难并启动故障转移过程之后。</span><span class="sxs-lookup"><span data-stu-id="e39ca-107">This is the time required for the failover to happen, after administrators have determined there was a disaster and initiated the failover procedures.</span></span> <span data-ttu-id="e39ca-108">此时间不包括管理员评估情况并作出决策所需的时间，也不包括用户在故障转移完成后再次登录所需的时间。</span><span class="sxs-lookup"><span data-stu-id="e39ca-108">It does not include the time for administrators to assess the situation and make a decision, nor does it include the time for users to sign in again after failover is complete.</span></span>

<span data-ttu-id="e39ca-109">对于池故障转移和池故障回复，针对恢复点目标的工程目标 (RPO) 为30分钟。</span><span class="sxs-lookup"><span data-stu-id="e39ca-109">For pool failover and pool failback, the engineering target for recovery point objective (RPO) is 30 minutes.</span></span> <span data-ttu-id="e39ca-110">这表示测量可能因灾难、因备份服务的复制延迟丢失的数据的时间。</span><span class="sxs-lookup"><span data-stu-id="e39ca-110">This represents the time measure of data that could be lost due to the disaster, due to replication latency of the Backup Service.</span></span> <span data-ttu-id="e39ca-111">例如，如果池在 10:00 A.M. 停止，RPO 为30分钟，则在 9:30 A.M. 之间写入到池中的数据将被写入。</span><span class="sxs-lookup"><span data-stu-id="e39ca-111">For example, if a pool goes down at 10:00 A.M., and the RPO is 30 minutes, data written to the pool between 9:30 A.M.</span></span> <span data-ttu-id="e39ca-112">和10:00 （可能尚未复制到备份池），将丢失。</span><span class="sxs-lookup"><span data-stu-id="e39ca-112">and 10:00 A.M.might not have replicated to the backup pool, and would be lost.</span></span>

<span data-ttu-id="e39ca-113">本文档中的所有 RTO 和 RPO 数字均假定两个数据中心位于同一在两个网站间具有高速度、低延迟传输的世界区域中。</span><span class="sxs-lookup"><span data-stu-id="e39ca-113">All RTO and RPO numbers in this document assume that the two data centers are located within the same world region with high-speed, low-latency transport between the two sites.</span></span> <span data-ttu-id="e39ca-114">这些数字是针对具有 40,000 个同时活动的用户和 200,000 个已启用有关预定义的用户模型（在该模型中，数据复制没有备份日志）的 Lync 的用户的池测量而来的。</span><span class="sxs-lookup"><span data-stu-id="e39ca-114">These numbers are measured for a pool with 40,000 concurrently active users and 200,000 users enabled for Lync with respect to a pre-defined user model where there is no backlog in data replication.</span></span> <span data-ttu-id="e39ca-115">这些数字可能根据测试和验证性能发生改变。</span><span class="sxs-lookup"><span data-stu-id="e39ca-115">They are subject to change based on performance testing and validation.</span></span>

<span data-ttu-id="e39ca-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e39ca-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

