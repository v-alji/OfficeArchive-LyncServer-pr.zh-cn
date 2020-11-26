---
title: Lync Server 2013：控制器的软硬件要求
description: Lync Server 2013： Director 的硬件和软件要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardware and software requirements for the Director
ms:assetid: 747b701e-7f97-46fe-91c5-1e8d9addf9f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398560(v=OCS.15)
ms:contentKeyID: 48184517
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dd868a3a566f1d89b4ada5a16695f8eb02b3b21
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427738"
---
# <a name="hardware-and-software-requirements-for-the-director-in-lync-server-2013"></a><span data-ttu-id="79bf7-103">Lync Server 2013 中控制器的软硬件要求</span><span class="sxs-lookup"><span data-stu-id="79bf7-103">Hardware and software requirements for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79bf7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79bf7-104">

<span> </span></span></span>

<span data-ttu-id="79bf7-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="79bf7-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="79bf7-106">本部分详细介绍了 Director 的硬件和软件要求，以及 Director 支持的 collocation 方案。</span><span class="sxs-lookup"><span data-stu-id="79bf7-106">This section details the hardware and software requirements for the Director, and the supported collocation scenarios for the Director.</span></span>

<div>

## <a name="hardware-requirements-for-the-director"></a><span data-ttu-id="79bf7-107">控制器的硬件要求</span><span class="sxs-lookup"><span data-stu-id="79bf7-107">Hardware Requirements for the Director</span></span>

<span data-ttu-id="79bf7-108">下表列出了 Director 的硬件要求：</span><span class="sxs-lookup"><span data-stu-id="79bf7-108">The following table lists the hardware requirements for the Director:</span></span>

### <a name="hardware-requirements-for-the-director"></a><span data-ttu-id="79bf7-109">控制器的硬件要求</span><span class="sxs-lookup"><span data-stu-id="79bf7-109">Hardware Requirements for the Director</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79bf7-110">硬件组件</span><span class="sxs-lookup"><span data-stu-id="79bf7-110">Hardware component</span></span></th>
<th><span data-ttu-id="79bf7-111">最低要求</span><span class="sxs-lookup"><span data-stu-id="79bf7-111">Minimum requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79bf7-112">CPU</span><span class="sxs-lookup"><span data-stu-id="79bf7-112">CPU</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="79bf7-113">64位处理器、四核、2.0 GHz 或更高版本</span><span class="sxs-lookup"><span data-stu-id="79bf7-113">64-bit processor, quad-core, 2.0 GHz or higher</span></span></p></li>
<li><p><span data-ttu-id="79bf7-114">64位双处理器、双核、2.0 GHz 或更高版本</span><span class="sxs-lookup"><span data-stu-id="79bf7-114">64-bit dual processor, dual-core, 2.0 GHz or higher</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79bf7-115">内存</span><span class="sxs-lookup"><span data-stu-id="79bf7-115">Memory</span></span></p></td>
<td><p><span data-ttu-id="79bf7-116">4 gb (GB) </span><span class="sxs-lookup"><span data-stu-id="79bf7-116">4 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79bf7-117">磁盘</span><span class="sxs-lookup"><span data-stu-id="79bf7-117">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="79bf7-118">10K RPM 硬盘 (硬盘) </span><span class="sxs-lookup"><span data-stu-id="79bf7-118">10K RPM hard disk drive (HDD)</span></span></p></li>
<li><p><span data-ttu-id="79bf7-119">高性能固态驱动器 (SSD) 性能等于或优于 10K RPM 的 HDD</span><span class="sxs-lookup"><span data-stu-id="79bf7-119">High-performance solid state drive (SSD) with performance equal to or better than 10K RPM HDD</span></span></p></li>
<li><p><span data-ttu-id="79bf7-120">2倍的 RAID 10 (数据库数据文件的带区镜像和镜像) 15K RPM 磁盘</span><span class="sxs-lookup"><span data-stu-id="79bf7-120">2x RAID 10 (striped and mirrored) 15K RPM disks for database data files</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79bf7-121">网络</span><span class="sxs-lookup"><span data-stu-id="79bf7-121">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="79bf7-122"> (建议的 Gbps) 网络适配器 (Gbps 的每秒千兆位千兆位，) </span><span class="sxs-lookup"><span data-stu-id="79bf7-122">Dual 1 gigabit per second (Gbps) network adapters (recommended)</span></span></p></li>
<li><p><span data-ttu-id="79bf7-123"> (支持单个 1 Gbps 网络适配器) </span><span class="sxs-lookup"><span data-stu-id="79bf7-123">Single 1 Gbps network adapter (supported)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="software-requirements-for-the-director"></a><span data-ttu-id="79bf7-124">董事的软件要求</span><span class="sxs-lookup"><span data-stu-id="79bf7-124">Software Requirements for the Director</span></span>

<span data-ttu-id="79bf7-125">Director 角色只能部署在运行 Lync Server 2013 企业版的服务器上。</span><span class="sxs-lookup"><span data-stu-id="79bf7-125">The Director role can be deployed only on servers running Lync Server 2013 Enterprise Edition.</span></span>

<span data-ttu-id="79bf7-126">控制器需要以下64位操作系统之一：</span><span class="sxs-lookup"><span data-stu-id="79bf7-126">One of the following 64-bit operating systems is required for the Directors:</span></span>

  - <span data-ttu-id="79bf7-127">Windows Server 2008 R2 标准操作系统，Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="79bf7-127">The Windows Server 2008 R2 Standard operating system with Service Pack 1</span></span>

  - <span data-ttu-id="79bf7-128">Windows Server 2008 R2 企业版操作系统 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="79bf7-128">The Windows Server 2008 R2 Enterprise operating system with Service Pack 1</span></span>

  - <span data-ttu-id="79bf7-129">Windows Server 2008 R2 Datacenter 操作系统 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="79bf7-129">The Windows Server 2008 R2 Datacenter operating system with Service Pack 1</span></span>

  - <span data-ttu-id="79bf7-130">Windows Server 2012 标准操作系统</span><span class="sxs-lookup"><span data-stu-id="79bf7-130">The Windows Server 2012 Standard operating system</span></span>

  - <span data-ttu-id="79bf7-131">Windows Server 2012 Datacenter 操作系统</span><span class="sxs-lookup"><span data-stu-id="79bf7-131">The Windows Server 2012 Datacenter operating system</span></span>

<span data-ttu-id="79bf7-132">Lync Server 2013 还要求安装以下程序和更新，详细信息请参阅 [Lync Server 2013 中的其他服务器支持和要求](lync-server-2013-additional-server-support-and-requirements.md)主题。</span><span class="sxs-lookup"><span data-stu-id="79bf7-132">Lync Server 2013 also requires installation of the following programs and updates detailed in the topic [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md).</span></span>

</div>

<div>

## <a name="supported-collocation"></a><span data-ttu-id="79bf7-133">支持的 Collocation</span><span class="sxs-lookup"><span data-stu-id="79bf7-133">Supported Collocation</span></span>

<span data-ttu-id="79bf7-134">Director 服务器角色不能与 Lync Server 2013 中的任何其他服务器角色 collocated。</span><span class="sxs-lookup"><span data-stu-id="79bf7-134">The Director server role cannot be collocated with any other server role in Lync Server 2013.</span></span> <span data-ttu-id="79bf7-135">但是，如果您不部署 Director，前端服务器将承担该角色。</span><span class="sxs-lookup"><span data-stu-id="79bf7-135">However, if you do not deploy a Director, the Front End Servers will assume the role.</span></span>

<span data-ttu-id="79bf7-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79bf7-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

