---
title: Lync Server 2013：配置故障转移路由
description: Lync Server 2013：配置故障转移路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a failover route
ms:assetid: 76e48df4-3b78-4fb7-b1f7-c1e604b81bad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398581(v=OCS.15)
ms:contentKeyID: 48184542
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7cfc45276931685a2d42103b1b7f1d5015dcd7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433519"
---
# <a name="configuring-a-failover-route-in-lync-server-2013"></a><span data-ttu-id="8924f-103">在 Lync Server 2013 中配置故障转移路由</span><span class="sxs-lookup"><span data-stu-id="8924f-103">Configuring a failover route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8924f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8924f-104">

<span> </span></span></span>

<span data-ttu-id="8924f-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="8924f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="8924f-p101">以下示例显示在 Dallas-GW1 因维护而关闭或因其他原因不可用时，管理员如何定义故障转移路由以供使用。下面的表显示了所需的配置更改。</span><span class="sxs-lookup"><span data-stu-id="8924f-p101">The following example shows how an administrator can define a failover route for use if the Dallas-GW1 is down for maintenance or is otherwise unavailable. The following tables illustrate the required configuration change.</span></span>

### <a name="table-1-user-policy"></a><span data-ttu-id="8924f-p102">表 1. 用户策略</span><span class="sxs-lookup"><span data-stu-id="8924f-p102">Table 1. User Policy</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8924f-110">用户策略</span><span class="sxs-lookup"><span data-stu-id="8924f-110">User policy</span></span></th>
<th><span data-ttu-id="8924f-111">电话用法</span><span class="sxs-lookup"><span data-stu-id="8924f-111">Phone usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8924f-112">默认呼叫策略</span><span class="sxs-lookup"><span data-stu-id="8924f-112">Default Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="8924f-113">Local</span><span class="sxs-lookup"><span data-stu-id="8924f-113">Local</span></span></p>
<p><span data-ttu-id="8924f-114">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="8924f-114">GlobalPSTNHopoff</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8924f-115">Redmond 本地策略</span><span class="sxs-lookup"><span data-stu-id="8924f-115">Redmond Local Policy</span></span></p></td>
<td><p><span data-ttu-id="8924f-116">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="8924f-116">RedmondLocal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8924f-117">Dallas 呼叫策略</span><span class="sxs-lookup"><span data-stu-id="8924f-117">Dallas Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="8924f-118">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="8924f-118">DallasUsers</span></span></p>
<p><span data-ttu-id="8924f-119">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="8924f-119">GlobalPSTNHopoff</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-2-routes"></a><span data-ttu-id="8924f-p103">表 2. 路由</span><span class="sxs-lookup"><span data-stu-id="8924f-p103">Table 2. Routes</span></span>

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
<th><span data-ttu-id="8924f-122">路由名称</span><span class="sxs-lookup"><span data-stu-id="8924f-122">Route name</span></span></th>
<th><span data-ttu-id="8924f-123">号码模式</span><span class="sxs-lookup"><span data-stu-id="8924f-123">Number pattern</span></span></th>
<th><span data-ttu-id="8924f-124">电话用法</span><span class="sxs-lookup"><span data-stu-id="8924f-124">Phone usage</span></span></th>
<th><span data-ttu-id="8924f-125">中继</span><span class="sxs-lookup"><span data-stu-id="8924f-125">Trunk</span></span></th>
<th><span data-ttu-id="8924f-126">网关</span><span class="sxs-lookup"><span data-stu-id="8924f-126">Gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8924f-127">Redmond 本地路由</span><span class="sxs-lookup"><span data-stu-id="8924f-127">Redmond Local Route</span></span></p></td>
<td><p><span data-ttu-id="8924f-128">^\+1 (425 | 206 | 253) # A2\d {7}) $</span><span class="sxs-lookup"><span data-stu-id="8924f-128">^\+1(425|206|253)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="8924f-129">Local</span><span class="sxs-lookup"><span data-stu-id="8924f-129">Local</span></span></p>
<p><span data-ttu-id="8924f-130">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="8924f-130">RedmondLocal</span></span></p></td>
<td><p><span data-ttu-id="8924f-131">Trunk1</span><span class="sxs-lookup"><span data-stu-id="8924f-131">Trunk1</span></span></p>
<p><span data-ttu-id="8924f-132">Trunk2</span><span class="sxs-lookup"><span data-stu-id="8924f-132">Trunk2</span></span></p></td>
<td><p><span data-ttu-id="8924f-133">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="8924f-133">Red-GW1</span></span></p>
<p><span data-ttu-id="8924f-134">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="8924f-134">Red-GW2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8924f-135">Dallas 本地路由</span><span class="sxs-lookup"><span data-stu-id="8924f-135">Dallas Local Route</span></span></p></td>
<td><p><span data-ttu-id="8924f-136">^\+1 (972 | 214 | 469) # A2\d {7}) $</span><span class="sxs-lookup"><span data-stu-id="8924f-136">^\+1(972|214|469)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="8924f-137">Local</span><span class="sxs-lookup"><span data-stu-id="8924f-137">Local</span></span></p></td>
<td><p><span data-ttu-id="8924f-138">Trunk3</span><span class="sxs-lookup"><span data-stu-id="8924f-138">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="8924f-139">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="8924f-139">Dallas-GW1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8924f-140">通用路由</span><span class="sxs-lookup"><span data-stu-id="8924f-140">Universal Route</span></span></p></td>
<td><p><span data-ttu-id="8924f-141">^\+？ ( \d \* ) $</span><span class="sxs-lookup"><span data-stu-id="8924f-141">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="8924f-142">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="8924f-142">GlobalPSTNHopoff</span></span></p></td>
<td><p><span data-ttu-id="8924f-143">Trunk1</span><span class="sxs-lookup"><span data-stu-id="8924f-143">Trunk1</span></span></p>
<p><span data-ttu-id="8924f-144">Trunk2</span><span class="sxs-lookup"><span data-stu-id="8924f-144">Trunk2</span></span></p>
<p><span data-ttu-id="8924f-145">Trunk3</span><span class="sxs-lookup"><span data-stu-id="8924f-145">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="8924f-146">Red-GW1</span><span class="sxs-lookup"><span data-stu-id="8924f-146">Red-GW1</span></span></p>
<p><span data-ttu-id="8924f-147">Red-GW2</span><span class="sxs-lookup"><span data-stu-id="8924f-147">Red-GW2</span></span></p>
<p><span data-ttu-id="8924f-148">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="8924f-148">Dallas-GW1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8924f-149">Dallas 用户路由</span><span class="sxs-lookup"><span data-stu-id="8924f-149">Dallas Users Route</span></span></p></td>
<td><p><span data-ttu-id="8924f-150">^\+？ ( \d \* ) $</span><span class="sxs-lookup"><span data-stu-id="8924f-150">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="8924f-151">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="8924f-151">DallasUsers</span></span></p></td>
<td><p><span data-ttu-id="8924f-152">Trunk3</span><span class="sxs-lookup"><span data-stu-id="8924f-152">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="8924f-153">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="8924f-153">Dallas-GW1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8924f-p104">在表 1 中，名为 GlobalPSTNHopoff 的电话用法添加到 Dallas Calling Policy 中的 DallasUsers 电话用法的后面。这样，当 DallasUsers 电话用法的路由不可用时，具有 Dallas Calling Policy 的呼叫就可以使用针对 GlobalPSTNHopoff 电话用法配置的路由。</span><span class="sxs-lookup"><span data-stu-id="8924f-p104">In Table 1, a phone usage of GlobalPSTNHopoff is added after the DallasUsers phone usage in the Dallas Calling Policy. This enables calls with the Dallas Calling policy to use routes that are configured for the GlobalPSTNHopoff phone usage if a route for the DallasUsers phone usage is unavailable.</span></span>

<span data-ttu-id="8924f-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8924f-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

