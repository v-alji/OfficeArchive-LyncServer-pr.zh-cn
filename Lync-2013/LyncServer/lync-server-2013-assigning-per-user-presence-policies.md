---
title: Lync Server 2013：分配每用户状态策略
description: Lync Server 2013：分配每用户状态策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user presence policies
ms:assetid: fd1097b7-248d-4b78-8c43-456b03257c18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182614(v=OCS.15)
ms:contentKeyID: 48185955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c3d4b4bda0c4bb85065d546fdbb4b2578db0e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392426"
---
# <a name="assigning-per-user-presence-policies-in-lync-server-2013"></a><span data-ttu-id="a89e5-103">在 Lync Server 2013 中分配每用户状态策略</span><span class="sxs-lookup"><span data-stu-id="a89e5-103">Assigning per-user presence policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a89e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a89e5-104">

<span> </span></span></span>

<span data-ttu-id="a89e5-105">_**主题上次修改时间：** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="a89e5-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="a89e5-106">状态策略是一组影响状态的限制和限制。</span><span class="sxs-lookup"><span data-stu-id="a89e5-106">A presence policy is a set of limits and restrictions that affect presence.</span></span> <span data-ttu-id="a89e5-107">下表描述了 Lync Server 2013 中可用的状态策略设置。</span><span class="sxs-lookup"><span data-stu-id="a89e5-107">The following table describes the presence policy settings available in Lync Server 2013.</span></span>

### <a name="presence-policy-settings"></a><span data-ttu-id="a89e5-108">状态策略设置</span><span class="sxs-lookup"><span data-stu-id="a89e5-108">Presence Policy Settings</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a89e5-109">XML 名称</span><span class="sxs-lookup"><span data-stu-id="a89e5-109">XML name</span></span></th>
<th><span data-ttu-id="a89e5-110">显示名称</span><span class="sxs-lookup"><span data-stu-id="a89e5-110">Display name</span></span></th>
<th><span data-ttu-id="a89e5-111">说明</span><span class="sxs-lookup"><span data-stu-id="a89e5-111">Description</span></span></th>
<th><span data-ttu-id="a89e5-112">类型</span><span class="sxs-lookup"><span data-stu-id="a89e5-112">Type</span></span></th>
<th><span data-ttu-id="a89e5-113">值</span><span class="sxs-lookup"><span data-stu-id="a89e5-113">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a89e5-114">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="a89e5-114">CategorySubscriptions</span></span></p></td>
<td><p><span data-ttu-id="a89e5-115">订阅者类别订阅的最大数量</span><span class="sxs-lookup"><span data-stu-id="a89e5-115">Maximum Number of Subscriber Category Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="a89e5-116">限制订阅者类别订阅数。</span><span class="sxs-lookup"><span data-stu-id="a89e5-116">Limits the number of subscriber category subscriptions.</span></span> <span data-ttu-id="a89e5-117">例如，当 Communicator 订阅用户的状态时，它将为每个联系人卡片、日历数据、便笺、服务和状态类别获取类别订阅。</span><span class="sxs-lookup"><span data-stu-id="a89e5-117">For example, when Communicator subscribes to a user’s presence, it obtains a category subscription for each of the contact card, calendar data, notes, services, and state categories.</span></span></p>
<p><span data-ttu-id="a89e5-118">设置为0表示用户或联系人对象不能由其他人订阅。</span><span class="sxs-lookup"><span data-stu-id="a89e5-118">A setting of 0 means that the user or contact object cannot be subscribed to by others.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="a89e5-119">如果设置为较高的数字，此设置可能会对性能产生重大影响，并且平均用户有大量用户订阅其状态。</span><span class="sxs-lookup"><span data-stu-id="a89e5-119">This setting can have a significant impact on performance if it is set to a high number, and the average user has a large number of users subscribing to his or her presence.</span></span>


</div></td>
<td><p><span data-ttu-id="a89e5-120">整型</span><span class="sxs-lookup"><span data-stu-id="a89e5-120">Integer</span></span></p></td>
<td><p><span data-ttu-id="a89e5-121">0-3000</span><span class="sxs-lookup"><span data-stu-id="a89e5-121">0-3000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89e5-122">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="a89e5-122">PromptedSubscribers</span></span></p></td>
<td><p><span data-ttu-id="a89e5-123">排队状态订阅警报的最大数量</span><span class="sxs-lookup"><span data-stu-id="a89e5-123">Maximum Number of Queued Presence Subscription Alerts</span></span></p></td>
<td><p><span data-ttu-id="a89e5-124">限制 "提示订阅者" 表中的条目数。</span><span class="sxs-lookup"><span data-stu-id="a89e5-124">Limits the number of entries in the prompted subscribers table.</span></span> <span data-ttu-id="a89e5-125">此设置确定可为给定用户排队的最大提示数。</span><span class="sxs-lookup"><span data-stu-id="a89e5-125">This setting determines the maximum number of prompts that can be queued for a given user.</span></span> <span data-ttu-id="a89e5-126">例如，当用户 A 订阅用户 B 的状态时，用户 B 会收到一条提示，指示用户 A 现在已订阅用户 B，并且在用户 B 的 "提示订阅者" 表中创建了确认提示。</span><span class="sxs-lookup"><span data-stu-id="a89e5-126">For example, when user A subscribes to user B’s presence, user B receives a prompt that user A is now subscribed to user B, and an acknowledgement prompt is created in user B’s prompted subscribers table.</span></span> <span data-ttu-id="a89e5-127">在用户 B 接受或确认订阅后，将从用户 B 的 "提示订阅者" 表中删除确认提示。</span><span class="sxs-lookup"><span data-stu-id="a89e5-127">After user B accepts, or acknowledges, the subscription, the acknowledgement prompt is removed from user B’s prompted subscribers table.</span></span></p>
<p><span data-ttu-id="a89e5-128">设置为0意味着当有人订阅他或她的状态时，不会提示用户。</span><span class="sxs-lookup"><span data-stu-id="a89e5-128">A setting of 0 means that the user is not prompted when someone subscribes to his or her presence.</span></span></p></td>
<td><p><span data-ttu-id="a89e5-129">整型或标记</span><span class="sxs-lookup"><span data-stu-id="a89e5-129">Integer or Token</span></span></p></td>
<td><p><span data-ttu-id="a89e5-130">0-500</span><span class="sxs-lookup"><span data-stu-id="a89e5-130">0-500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a89e5-131">默认情况下，当你部署 Lync Server 时， **默认策略** 和 **服务： "中等** 状态" 策略已安装。</span><span class="sxs-lookup"><span data-stu-id="a89e5-131">By default, the **Default Policy** and **Service: Medium** presence policies are installed when you deploy Lync Server.</span></span> <span data-ttu-id="a89e5-132">下表介绍了这两种状态策略的特定设置。</span><span class="sxs-lookup"><span data-stu-id="a89e5-132">The following table describes the specific settings of the two presence policies.</span></span>

### <a name="presence-policies"></a><span data-ttu-id="a89e5-133">状态策略</span><span class="sxs-lookup"><span data-stu-id="a89e5-133">Presence Policies</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a89e5-134">策略名称</span><span class="sxs-lookup"><span data-stu-id="a89e5-134">Policy name</span></span></th>
<th><span data-ttu-id="a89e5-135">说明</span><span class="sxs-lookup"><span data-stu-id="a89e5-135">Description</span></span></th>
<th><span data-ttu-id="a89e5-136">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="a89e5-136">CategorySubscriptions</span></span></th>
<th><span data-ttu-id="a89e5-137">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="a89e5-137">PromptedSubscribers</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a89e5-138">默认策略</span><span class="sxs-lookup"><span data-stu-id="a89e5-138">Default Policy</span></span></p></td>
<td><p><span data-ttu-id="a89e5-139">适用于典型用户的策略。</span><span class="sxs-lookup"><span data-stu-id="a89e5-139">Policy for typical users.</span></span> <span data-ttu-id="a89e5-140">这是默认的状态策略。</span><span class="sxs-lookup"><span data-stu-id="a89e5-140">This is the default presence policy.</span></span></p></td>
<td><p><span data-ttu-id="a89e5-141">1000</span><span class="sxs-lookup"><span data-stu-id="a89e5-141">1000</span></span></p></td>
<td><p><span data-ttu-id="a89e5-142">200</span><span class="sxs-lookup"><span data-stu-id="a89e5-142">200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a89e5-143">服务：中等</span><span class="sxs-lookup"><span data-stu-id="a89e5-143">Service: Medium</span></span></p></td>
<td><p><span data-ttu-id="a89e5-144">需要更多用户才能订阅对象状态的应用程序的策略。</span><span class="sxs-lookup"><span data-stu-id="a89e5-144">Policy for applications that require more users to subscribe to the object’s presence.</span></span></p></td>
<td><p><span data-ttu-id="a89e5-145">1000</span><span class="sxs-lookup"><span data-stu-id="a89e5-145">1000</span></span></p></td>
<td><p><span data-ttu-id="a89e5-146">0</span><span class="sxs-lookup"><span data-stu-id="a89e5-146">0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a89e5-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a89e5-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

