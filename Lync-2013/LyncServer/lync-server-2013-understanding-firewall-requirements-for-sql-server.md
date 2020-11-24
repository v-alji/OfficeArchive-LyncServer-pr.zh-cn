---
title: Lync Server 2013：了解 SQL Server 的防火墙要求
description: Lync Server 2013：了解 SQL Server 的防火墙要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding firewall requirements for SQL Server
ms:assetid: 31d7df2c-589f-465e-be74-cf6767db190d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425818(v=OCS.15)
ms:contentKeyID: 48183781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c434474b36ced0fe64b9398f7d0e6136ff523a93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392263"
---
# <a name="understanding-firewall-requirements-for-sql-server-with-lync-server-2013"></a><span data-ttu-id="99b8f-103">了解 SQL Server 与 Lync Server 2013 一起使用时的防火墙要求</span><span class="sxs-lookup"><span data-stu-id="99b8f-103">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99b8f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99b8f-104">

<span> </span></span></span>

<span data-ttu-id="99b8f-105">_**主题上次修改时间：** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="99b8f-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="99b8f-106">对于标准版部署，将在 Lync Server 2013 设置期间自动创建防火墙例外。</span><span class="sxs-lookup"><span data-stu-id="99b8f-106">For a Standard Edition deployment, firewall exceptions are created automatically during Lync Server 2013 Setup.</span></span> <span data-ttu-id="99b8f-107">但是，对于企业版部署，你必须在 SQL Server 后端服务器上手动配置防火墙例外。</span><span class="sxs-lookup"><span data-stu-id="99b8f-107">However, for Enterprise Edition deployments, you must configure the firewall exceptions manually on the SQL Server Back End Server.</span></span> <span data-ttu-id="99b8f-108">TCP/IP 协议允许为给定的 IP 地址使用一次给定的端口。</span><span class="sxs-lookup"><span data-stu-id="99b8f-108">The TCP/IP protocol allows for a given port to be used once for a given IP address.</span></span> <span data-ttu-id="99b8f-109">这意味着对于基于 SQL Server 的服务器，你可以为默认的 TCP 端口1433分配默认的数据库实例。</span><span class="sxs-lookup"><span data-stu-id="99b8f-109">This means that for the SQL Server-based server you can assign the default database instance the default TCP port 1433.</span></span> <span data-ttu-id="99b8f-110">对于任何其他实例，你将需要使用 SQL Server 配置管理器分配唯一的和未使用的端口。</span><span class="sxs-lookup"><span data-stu-id="99b8f-110">For any other instances you will need to use the SQL Server Configuration Manager to assign unique and unused ports.</span></span> <span data-ttu-id="99b8f-111">本主题包括：</span><span class="sxs-lookup"><span data-stu-id="99b8f-111">This topic covers:</span></span>

  - <span data-ttu-id="99b8f-112">使用默认实例时防火墙异常的要求</span><span class="sxs-lookup"><span data-stu-id="99b8f-112">Requirements for a firewall exception when using the default instance</span></span>

  - <span data-ttu-id="99b8f-113">SQL Server Browser 服务的防火墙例外要求</span><span class="sxs-lookup"><span data-stu-id="99b8f-113">Requirements for a firewall exception for the SQL Server Browser service</span></span>

  - <span data-ttu-id="99b8f-114">使用命名实例时静态侦听端口的要求</span><span class="sxs-lookup"><span data-stu-id="99b8f-114">Requirements for static listening ports when using named instances</span></span>

<div>

## <a name="requirements-for-a-firewall-exception-when-using-the-default-instance"></a><span data-ttu-id="99b8f-115">使用默认实例时防火墙异常的要求</span><span class="sxs-lookup"><span data-stu-id="99b8f-115">Requirements for a Firewall Exception When Using the Default Instance</span></span>

<span data-ttu-id="99b8f-116">如果在部署 Lync Server 2013 时对任何数据库使用 SQL Server 默认实例，则以下防火墙规则要求用于帮助确保从前端池到 SQL Server 默认实例的通信。</span><span class="sxs-lookup"><span data-stu-id="99b8f-116">If you are using the SQL Server default instance for any database when deploying Lync Server 2013, the following firewall rule requirements are used to help ensure communication from the Front End pool to the SQL Server default instance.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99b8f-117">协议</span><span class="sxs-lookup"><span data-stu-id="99b8f-117">Protocol</span></span></th>
<th><span data-ttu-id="99b8f-118">端口</span><span class="sxs-lookup"><span data-stu-id="99b8f-118">Port</span></span></th>
<th><span data-ttu-id="99b8f-119">方向</span><span class="sxs-lookup"><span data-stu-id="99b8f-119">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99b8f-120">TCP</span><span class="sxs-lookup"><span data-stu-id="99b8f-120">TCP</span></span></p></td>
<td><p><span data-ttu-id="99b8f-121">1433</span><span class="sxs-lookup"><span data-stu-id="99b8f-121">1433</span></span></p></td>
<td><p><span data-ttu-id="99b8f-122">入站到 SQL Server</span><span class="sxs-lookup"><span data-stu-id="99b8f-122">Inbound to SQL Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-a-firewall-exception-for-the-sql-server-browser-service"></a><span data-ttu-id="99b8f-123">SQL Server Browser 服务的防火墙例外要求</span><span class="sxs-lookup"><span data-stu-id="99b8f-123">Requirements for a Firewall Exception for the SQL Server Browser Service</span></span>

<span data-ttu-id="99b8f-124">SQL Server Browser 服务将查找数据库实例，并将配置实例 (命名或配置为使用的默认) 的端口进行通信。</span><span class="sxs-lookup"><span data-stu-id="99b8f-124">The SQL Server Browser service will locate database instances and communicate the port that the instance (named or default) is configured to use.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99b8f-125">协议</span><span class="sxs-lookup"><span data-stu-id="99b8f-125">Protocol</span></span></th>
<th><span data-ttu-id="99b8f-126">端口</span><span class="sxs-lookup"><span data-stu-id="99b8f-126">Port</span></span></th>
<th><span data-ttu-id="99b8f-127">方向</span><span class="sxs-lookup"><span data-stu-id="99b8f-127">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99b8f-128">UDP</span><span class="sxs-lookup"><span data-stu-id="99b8f-128">UDP</span></span></p></td>
<td><p><span data-ttu-id="99b8f-129">1434</span><span class="sxs-lookup"><span data-stu-id="99b8f-129">1434</span></span></p></td>
<td><p><span data-ttu-id="99b8f-130">封</span><span class="sxs-lookup"><span data-stu-id="99b8f-130">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-static-listening-ports-when-using-named-instances"></a><span data-ttu-id="99b8f-131">使用命名实例时静态侦听端口的要求</span><span class="sxs-lookup"><span data-stu-id="99b8f-131">Requirements for Static Listening Ports When Using Named Instances</span></span>

<span data-ttu-id="99b8f-132">在支持 Lync Server 2013 的数据库的 SQL Server 配置中使用命名实例时，可使用 SQL Server 配置管理器配置静态端口。</span><span class="sxs-lookup"><span data-stu-id="99b8f-132">When using named instances in the SQL Server configuration for databases supporting Lync Server 2013, you configure static ports by using SQL Server Configuration Manager.</span></span> <span data-ttu-id="99b8f-133">将静态端口分配给每个命名实例后，将为防火墙中的每个静态端口创建例外。</span><span class="sxs-lookup"><span data-stu-id="99b8f-133">After the static ports have been assigned to each named instance, you create exceptions for each static port in the firewall.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99b8f-134">协议</span><span class="sxs-lookup"><span data-stu-id="99b8f-134">Protocol</span></span></th>
<th><span data-ttu-id="99b8f-135">端口</span><span class="sxs-lookup"><span data-stu-id="99b8f-135">Port</span></span></th>
<th><span data-ttu-id="99b8f-136">方向</span><span class="sxs-lookup"><span data-stu-id="99b8f-136">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99b8f-137">TCP</span><span class="sxs-lookup"><span data-stu-id="99b8f-137">TCP</span></span></p></td>
<td><p><span data-ttu-id="99b8f-138">静态定义</span><span class="sxs-lookup"><span data-stu-id="99b8f-138">Statically defined</span></span></p></td>
<td><p><span data-ttu-id="99b8f-139">封</span><span class="sxs-lookup"><span data-stu-id="99b8f-139">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sql-server-documentation"></a><span data-ttu-id="99b8f-140">SQL Server 文档</span><span class="sxs-lookup"><span data-stu-id="99b8f-140">SQL Server Documentation</span></span>

<span data-ttu-id="99b8f-141">Microsoft SQL Server 2012 文档提供有关如何配置数据库的防火墙访问的详细指南。</span><span class="sxs-lookup"><span data-stu-id="99b8f-141">Microsoft SQL Server 2012 documentation provides detailed guidance on how to configure firewall access for databases.</span></span> <span data-ttu-id="99b8f-142">有关 Microsoft SQL Server 2012 的详细信息，请参阅 "配置 Windows 防火墙以允许 SQL Server 访问" [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031) 。</span><span class="sxs-lookup"><span data-stu-id="99b8f-142">For details about Microsoft SQL Server 2012, see “Configuring the Windows Firewall to Allow SQL Server Access” at [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031).</span></span>

<span data-ttu-id="99b8f-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99b8f-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

