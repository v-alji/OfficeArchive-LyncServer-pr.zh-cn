---
title: Lync Server 2013：基于位置的路由的客户端和服务器支持
description: Lync Server 2013：客户端和服务器支持 Location-Based 路由。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client and server support for Location-Based Routing
ms:assetid: 26c2ca3d-026d-4dd7-94fa-15ebb4406953
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994024(v=OCS.15)
ms:contentKeyID: 51803933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20dca7444f58ee62dbc36edbb7d9e1c976a97807
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434898"
---
# <a name="client-and-server-support-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="4cc29-103">Lync Server 2013 中基于位置的路由的客户端和服务器支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-103">Client and server support for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cc29-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cc29-104">

<span> </span></span></span>

<span data-ttu-id="4cc29-105">_**主题上次修改时间：** 2013-06-18_</span><span class="sxs-lookup"><span data-stu-id="4cc29-105">_**Topic Last Modified:** 2013-06-18_</span></span>

<span data-ttu-id="4cc29-106">Location-Based 路由由 Lync Server 强制执行。</span><span class="sxs-lookup"><span data-stu-id="4cc29-106">Location-Based Routing is enforced by Lync Server.</span></span> <span data-ttu-id="4cc29-107">Lync 服务器可以标识用户从公司网络中连接的网络站点。</span><span class="sxs-lookup"><span data-stu-id="4cc29-107">Lync Server can identify the network sites where users are connecting from within the corporate network.</span></span> <span data-ttu-id="4cc29-108">由于远程用户位于企业网络外，其位置将被视为未知。</span><span class="sxs-lookup"><span data-stu-id="4cc29-108">Since remote users are outside the corporate network, their location is considered to be unknown.</span></span>

<div>

## <a name="lync-server-support"></a><span data-ttu-id="4cc29-109">Lync Server 支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-109">Lync Server Support</span></span>

<span data-ttu-id="4cc29-110">Location-Based 路由要求在给定拓扑中的所有前端池和标准版服务器上部署 Lync Server 2013 CU1。</span><span class="sxs-lookup"><span data-stu-id="4cc29-110">Location-Based Routing requires that Lync Server 2013 CU1 is deployed on all Front End pools and Standard Edition servers in a given topology.</span></span> <span data-ttu-id="4cc29-111">如果未在拓扑中的某些 Lync 组件上安装 Lync Server 2013 CU1 Location-Based，则无法完全强制执行路由限制。</span><span class="sxs-lookup"><span data-stu-id="4cc29-111">If Lync Server 2013 CU1 is not installed on certain Lync components in the topology, Location-Based Routing restrictions cannot be fully enforced.</span></span>

<span data-ttu-id="4cc29-112">下表标识 Location-Based 路由支持的服务器角色和版本的组合。</span><span class="sxs-lookup"><span data-stu-id="4cc29-112">The following table identifies the combination of server roles and versions that is supported for Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cc29-113">池版本</span><span class="sxs-lookup"><span data-stu-id="4cc29-113">Pool version</span></span></th>
<th><span data-ttu-id="4cc29-114">中介服务器版本</span><span class="sxs-lookup"><span data-stu-id="4cc29-114">Mediation Server version</span></span></th>
<th><span data-ttu-id="4cc29-115">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-115">Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-116">Lync Server 2013，2013 2 月累积更新</span><span class="sxs-lookup"><span data-stu-id="4cc29-116">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="4cc29-117">Lync Server 2013，2013 2 月累积更新</span><span class="sxs-lookup"><span data-stu-id="4cc29-117">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="4cc29-118">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-118">yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cc29-119">Lync Server 2013，2013 2 月累积更新</span><span class="sxs-lookup"><span data-stu-id="4cc29-119">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="4cc29-120">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cc29-120">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="4cc29-121">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-121">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-122">Lync Server 2013，2013 2 月累积更新</span><span class="sxs-lookup"><span data-stu-id="4cc29-122">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="4cc29-123">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4cc29-123">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="4cc29-124">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-124">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cc29-125">Lync Server 2013，2013 2 月累积更新</span><span class="sxs-lookup"><span data-stu-id="4cc29-125">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="4cc29-126">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4cc29-126">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="4cc29-127">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-127">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-128">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cc29-128">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="4cc29-129">任意</span><span class="sxs-lookup"><span data-stu-id="4cc29-129">any</span></span></p></td>
<td><p><span data-ttu-id="4cc29-130">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-130">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cc29-131">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4cc29-131">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="4cc29-132">任意</span><span class="sxs-lookup"><span data-stu-id="4cc29-132">any</span></span></p></td>
<td><p><span data-ttu-id="4cc29-133">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-133">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-134">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4cc29-134">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="4cc29-135">任意</span><span class="sxs-lookup"><span data-stu-id="4cc29-135">any</span></span></p></td>
<td><p><span data-ttu-id="4cc29-136">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-136">no</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="4cc29-137">Lync 客户端支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-137">Lync Client Support</span></span>

<span data-ttu-id="4cc29-138">下表标识 Location-Based 路由支持的客户端。</span><span class="sxs-lookup"><span data-stu-id="4cc29-138">The following table identifies the clients that Location-Based Routing supports.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cc29-139">客户端类型</span><span class="sxs-lookup"><span data-stu-id="4cc29-139">Client type</span></span></th>
<th><span data-ttu-id="4cc29-140">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-140">Supported</span></span></th>
<th><span data-ttu-id="4cc29-141">详细信息</span><span class="sxs-lookup"><span data-stu-id="4cc29-141">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-142">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4cc29-142">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="4cc29-143">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-143">yes</span></span></p></td>
<td><p><span data-ttu-id="4cc29-144">包括 Lync 2013 二月2013累积更新</span><span class="sxs-lookup"><span data-stu-id="4cc29-144">Including Lync 2013 February 2013 Cumulative Update</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cc29-145">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4cc29-145">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4cc29-146">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-146">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-147">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4cc29-147">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="4cc29-148">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-148">no</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cc29-149">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="4cc29-149">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="4cc29-150">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-150">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-151">Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="4cc29-151">Lync Attendant</span></span></p></td>
<td><p><span data-ttu-id="4cc29-152">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-152">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cc29-153">适用于 Windows 8 的 Lync</span><span class="sxs-lookup"><span data-stu-id="4cc29-153">Lync for Windows 8</span></span></p></td>
<td><p><span data-ttu-id="4cc29-154">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-154">no</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cc29-155">Lync Mobile 2013</span><span class="sxs-lookup"><span data-stu-id="4cc29-155">Lync Mobile 2013</span></span></p></td>
<td><p><span data-ttu-id="4cc29-156">不支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-156">no</span></span></p></td>
<td><p><span data-ttu-id="4cc29-157">如果启用了 Location-Based 路由的用户使用，则必须为 Lync Mobile 2013 客户端禁用 VoIP。</span><span class="sxs-lookup"><span data-stu-id="4cc29-157">VoIP must be disabled for Lync Mobile 2013 clients if used by users with Location-Based Routing enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cc29-158">Lync Mobile 2010</span><span class="sxs-lookup"><span data-stu-id="4cc29-158">Lync Mobile 2010</span></span></p></td>
<td><p><span data-ttu-id="4cc29-159">支持</span><span class="sxs-lookup"><span data-stu-id="4cc29-159">yes</span></span></p></td>
<td> </td>
</tr>
</tbody>
</table>

  

<div>


> [!NOTE]  
> <span data-ttu-id="4cc29-160">若要禁用 Lync Mobile 2013 客户端的 VoIP，请为启用了基于位置的路由的所有用户的设置（IP 音频/视频）分配移动策略。</span><span class="sxs-lookup"><span data-stu-id="4cc29-160">To disable VoIP for Lync Mobile 2013 clients, assign a mobility policy with the setting, IP Audio/Video, disabled for all users enabled for Location Based Routing.</span></span> <span data-ttu-id="4cc29-161">有关移动策略的详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>。</span><span class="sxs-lookup"><span data-stu-id="4cc29-161">For more details about mobility policy, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4cc29-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4cc29-162">See Also</span></span>


[<span data-ttu-id="4cc29-163">在 Lync Server 2013 中规划基于位置的路由</span><span class="sxs-lookup"><span data-stu-id="4cc29-163">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="4cc29-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cc29-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

