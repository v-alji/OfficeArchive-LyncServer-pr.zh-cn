---
title: Lync Server 2013 服务器硬件平台
description: Lync Server 2013 服务器硬件平台。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server hardware platforms
ms:assetid: c964c1c0-0153-472b-88ad-a38866e0df0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398835(v=OCS.15)
ms:contentKeyID: 48185395
ms.date: 07/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d55deec50994d70cf305b794662a630c16c3af14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441870"
---
# <a name="server-hardware-platforms-for-lync-server-2013"></a><span data-ttu-id="8298d-103">Lync Server 2013 的服务器硬件平台</span><span class="sxs-lookup"><span data-stu-id="8298d-103">Server hardware platforms for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8298d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8298d-104">

<span> </span></span></span>

<span data-ttu-id="8298d-105">_**主题上次修改时间：** 2016-07-28_</span><span class="sxs-lookup"><span data-stu-id="8298d-105">_**Topic Last Modified:** 2016-07-28_</span></span>

<span data-ttu-id="8298d-106">Lync Server 2013 服务器角色和运行 Lync Server 管理工具的计算机需要64位硬件。</span><span class="sxs-lookup"><span data-stu-id="8298d-106">Lync Server 2013 server roles and computers running Lync Server administrative tools require 64-bit hardware.</span></span>

<span data-ttu-id="8298d-107">用于 Lync Server 2013 部署的特定硬件可能会有所不同，具体取决于大小和使用要求。</span><span class="sxs-lookup"><span data-stu-id="8298d-107">The specific hardware used for Lync Server 2013 deployment can vary, depending on size and usage requirements.</span></span> <span data-ttu-id="8298d-108">本节介绍推荐的硬件。</span><span class="sxs-lookup"><span data-stu-id="8298d-108">This section describes the recommended hardware.</span></span> <span data-ttu-id="8298d-109">虽然是建议（不是要求），但是使用不满足这些建议的硬件可能会导致重大性能问题和其他问题。</span><span class="sxs-lookup"><span data-stu-id="8298d-109">Although these are recommendations, not requirements, using hardware that does not meet these recommendations may result in significant performance issues and other issues.</span></span>

<div>

## <a name="recommended-hardware-platform"></a><span data-ttu-id="8298d-110">推荐的硬件平台</span><span class="sxs-lookup"><span data-stu-id="8298d-110">Recommended Hardware Platform</span></span>

<span data-ttu-id="8298d-111">为了获得最佳性能，我们建议你在具有满足下表中的要求的硬件的服务器上运行 Lync 服务器。</span><span class="sxs-lookup"><span data-stu-id="8298d-111">For best performance, we recommend that you run Lync Server on servers with hardware that meets the requirements in the following table.</span></span> <span data-ttu-id="8298d-112">如果使用性能不足的硬件，可能会遇到功能问题或性能下降。</span><span class="sxs-lookup"><span data-stu-id="8298d-112">If you use less powerful hardware, you may experience functionality problems or poor performance.</span></span> <span data-ttu-id="8298d-113">请注意，这些硬件要求比以前版本的 Lync Server 更高，主要是因为在 Lync Server 2013 中，所有前端服务器都运行 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="8298d-113">Note that these hardware requirements are higher than those of previous versions of Lync Server, primarily because in Lync Server 2013, all Front End Servers run SQL Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8298d-114">NIC 组合受支持，并且对于 Lync 服务器而言应该是透明的。</span><span class="sxs-lookup"><span data-stu-id="8298d-114">NIC teaming is supported and should be transparent to Lync Server.</span></span> <span data-ttu-id="8298d-115">有关详细信息，请参阅 <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">通信服务器或 Lync 服务器和网络适配器分组</A>。</span><span class="sxs-lookup"><span data-stu-id="8298d-115">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">Communications Server or Lync Server and network adapter teaming</A>.</span></span>



</div>

### <a name="recommended-hardware-for-front-end-servers-back-end-servers-standard-edition-servers-persistent-chat-servers-and-persistent-chat-store-and-persistent-chat-compliance-store-back-end-server-roles-for-persistent-chat-server"></a><span data-ttu-id="8298d-116">前端服务器、后端服务器、Standard Edition 服务器、持久聊天存储和持久聊天合规性存储（持久聊天服务器的后端服务器角色）的推荐硬件</span><span class="sxs-lookup"><span data-stu-id="8298d-116">Recommended Hardware for Front End Servers, Back End Servers, Standard Edition Servers, Persistent Chat Servers, and Persistent Chat Store and Persistent Chat Compliance Store (Back End Server Roles for Persistent Chat Server)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8298d-117">硬件组件</span><span class="sxs-lookup"><span data-stu-id="8298d-117">Hardware component</span></span></th>
<th><span data-ttu-id="8298d-118">推荐</span><span class="sxs-lookup"><span data-stu-id="8298d-118">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8298d-119">CPU</span><span class="sxs-lookup"><span data-stu-id="8298d-119">CPU</span></span></p></td>
<td><p><span data-ttu-id="8298d-120">64 位双处理器、六核、2.26 GHz 或更快。</span><span class="sxs-lookup"><span data-stu-id="8298d-120">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="8298d-121">Lync Server 服务器角色不支持英特尔安腾处理器。</span><span class="sxs-lookup"><span data-stu-id="8298d-121">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8298d-122">内存</span><span class="sxs-lookup"><span data-stu-id="8298d-122">Memory</span></span></p></td>
<td><p><span data-ttu-id="8298d-123">32 GB。</span><span class="sxs-lookup"><span data-stu-id="8298d-123">32 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8298d-124">磁盘</span><span class="sxs-lookup"><span data-stu-id="8298d-124">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8298d-125">8 个或 8 个以上具有至少 72 GB 可用磁盘空间的 10,000 RPM 硬盘驱动器。</span><span class="sxs-lookup"><span data-stu-id="8298d-125">8 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="8298d-126">其中两个磁盘驱动器应使用 RAID 1，另外六个磁盘驱动器应使用 RAID 10。</span><span class="sxs-lookup"><span data-stu-id="8298d-126">Two of the disks should use RAID 1, and six should use RAID 10.</span></span></p>
<p><span data-ttu-id="8298d-127">- 或</span><span class="sxs-lookup"><span data-stu-id="8298d-127">- OR -</span></span></p></li>
<li><p><span data-ttu-id="8298d-128">性能类似于 8 个 10,000 RPM 机械磁盘驱动器的固态驱动器 (SSD)</span><span class="sxs-lookup"><span data-stu-id="8298d-128">Solid state drives (SSDs) which provide performance similar to 8 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8298d-129">网络</span><span class="sxs-lookup"><span data-stu-id="8298d-129">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8298d-130">1 个双端口网络适配器，1 Gbps 或更高（建议为 2 Gbps，这要求与一个 MAC 地址和一个 IP 地址结合使用）。</span><span class="sxs-lookup"><span data-stu-id="8298d-130">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="8298d-131">前端服务器、后端服务器、Standard Edition 服务器和持久聊天服务器不支持双宿主或多宿主配置。</span><span class="sxs-lookup"><span data-stu-id="8298d-131">Dual or multi-homed configurations are not supported for Front End Servers, Back End Servers, Standard Edition servers, and Persistent Chat Servers.</span></span><BR><span data-ttu-id="8298d-132">ILO/DRAC/更高的连接。未向操作系统公开的连接以及用于监视和管理服务器硬件的连接不构成多穴服务器，因此受支持。</span><span class="sxs-lookup"><span data-stu-id="8298d-132">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="recommended-hardware-for-edge-servers-standalone-mediation-servers-and-directors"></a><span data-ttu-id="8298d-133">边缘服务器、独立中介服务器和控制器的推荐硬件</span><span class="sxs-lookup"><span data-stu-id="8298d-133">Recommended Hardware for Edge Servers, Standalone Mediation Servers, and Directors</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8298d-134">硬件组件</span><span class="sxs-lookup"><span data-stu-id="8298d-134">Hardware component</span></span></th>
<th><span data-ttu-id="8298d-135">推荐</span><span class="sxs-lookup"><span data-stu-id="8298d-135">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8298d-136">CPU</span><span class="sxs-lookup"><span data-stu-id="8298d-136">CPU</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8298d-137">64位双处理器、四核、2.0 千兆位 (GHz) 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="8298d-137">64-bit dual processor, quad-core, 2.0 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="8298d-138">- 或</span><span class="sxs-lookup"><span data-stu-id="8298d-138">- OR -</span></span></p></li>
<li><p><span data-ttu-id="8298d-139">64位4路处理器、双核、2.0 GHz 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="8298d-139">64-bit 4-way processor, dual-core, 2.0 GHz or higher.</span></span></p></li>
</ul>
<p><span data-ttu-id="8298d-140">Lync Server 服务器角色不支持英特尔安腾处理器。</span><span class="sxs-lookup"><span data-stu-id="8298d-140">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8298d-141">内存</span><span class="sxs-lookup"><span data-stu-id="8298d-141">Memory</span></span></p></td>
<td><p><span data-ttu-id="8298d-142">16 gb (GB) 。</span><span class="sxs-lookup"><span data-stu-id="8298d-142">16 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8298d-143">磁盘</span><span class="sxs-lookup"><span data-stu-id="8298d-143">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8298d-144">4个或更多 10000 RPM 硬盘，至少有 72 GB 的可用磁盘空间。</span><span class="sxs-lookup"><span data-stu-id="8298d-144">4 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="8298d-145">磁盘应使用 2x RAID 1 配置。</span><span class="sxs-lookup"><span data-stu-id="8298d-145">The disks should be in a 2x RAID 1 configuration.</span></span></p>
<p><span data-ttu-id="8298d-146">- 或</span><span class="sxs-lookup"><span data-stu-id="8298d-146">- OR -</span></span></p></li>
<li><p><span data-ttu-id="8298d-147">性能类似于 4 个 10,000 RPM 机械磁盘驱动器的固态驱动器 (SSD)。</span><span class="sxs-lookup"><span data-stu-id="8298d-147">Solid state drives (SSDs) which provide performance similar to 4 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8298d-148">网络</span><span class="sxs-lookup"><span data-stu-id="8298d-148">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8298d-149">1 个双端口网络适配器，1 Gbps 或更高（建议为 2 Gbps，这要求与一个 MAC 地址和一个 IP 地址结合使用）。</span><span class="sxs-lookup"><span data-stu-id="8298d-149">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span> <span data-ttu-id="8298d-150">两个网络接口在 Edge 服务器上是必需的，并且在独立中介服务器上受支持。</span><span class="sxs-lookup"><span data-stu-id="8298d-150">2 network interfaces are required on Edge Servers, and are supported on standalone Mediation Servers.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="8298d-151">控制器不支持双穴或多穴配置。</span><span class="sxs-lookup"><span data-stu-id="8298d-151">Dual or multi-homed configurations are not supported for Directors.</span></span><BR><span data-ttu-id="8298d-152">ILO/DRAC/更高的连接。未向操作系统公开的连接以及用于监视和管理服务器硬件的连接不构成多穴服务器，因此受支持。</span><span class="sxs-lookup"><span data-stu-id="8298d-152">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div>
<p><span data-ttu-id="8298d-153">边缘服务器需要两个两个网络接口：双端口网络适配器、1 Gbps 或更高 (版本的网络适配器（共4个），每个配对都包含一个 MAC 地址和一个 IP 地址，总共两对) 。</span><span class="sxs-lookup"><span data-stu-id="8298d-153">Edge Servers will require two network interfaces that are dual-port network adapters, 1 Gbps or higher (or two paired network adapters, for a total of four, each pair being teamed with a single MAC address and a single IP address, for a total of two pairs).</span></span></p>
<p><span data-ttu-id="8298d-154">安装其他网络接口卡 (Nic) 以允许特定 PSTN IP 地址的配置在独立中介服务器上受支持。</span><span class="sxs-lookup"><span data-stu-id="8298d-154">Installation of additional network interface cards (NICs) to allow the configuration of a specific PSTN IP address is supported on standalone Mediation Servers.</span></span></p><span data-ttu-id="8298d-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8298d-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

