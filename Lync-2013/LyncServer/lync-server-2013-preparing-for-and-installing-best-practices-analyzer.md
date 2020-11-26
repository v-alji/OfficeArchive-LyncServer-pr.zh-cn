---
title: Lync Server 2013：准备和安装最佳做法分析器
description: Lync Server 2013：准备和安装最佳做法分析器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing for and installing Best Practices Analyzer
ms:assetid: 550613dd-dc08-482e-9980-a3fe187cd162
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591347(v=OCS.15)
ms:contentKeyID: 48184149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 005c5ac372a3564e74af549832830ebae899e9d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424140"
---
# <a name="preparing-for-and-installing-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="0e55b-103">在 Lync Server 2013 中准备和安装最佳做法分析器</span><span class="sxs-lookup"><span data-stu-id="0e55b-103">Preparing for and installing Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e55b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e55b-104">

<span> </span></span></span>

<span data-ttu-id="0e55b-105">_**主题上次修改时间：** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="0e55b-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="0e55b-106">必须作为管理员组的成员登录才能执行本主题中所述的任务。</span><span class="sxs-lookup"><span data-stu-id="0e55b-106">You must be logged on as a member of the Administrators group to perform the tasks that are described in this topic.</span></span>

<div>

## <a name="system-requirements-for-best-practices-analyzer-installation"></a><span data-ttu-id="0e55b-107">最佳做法分析器安装的系统要求</span><span class="sxs-lookup"><span data-stu-id="0e55b-107">System Requirements for Best Practices Analyzer Installation</span></span>

<span data-ttu-id="0e55b-108">若要运行 Lync Server 2013、最佳做法分析程序来扫描你的环境，计算机必须运行以下任一操作系统的64位版本：</span><span class="sxs-lookup"><span data-stu-id="0e55b-108">To run Lync Server 2013, Best Practices Analyzer to scan your environment, the computer must be running a 64-bit edition of one of the following operating systems:</span></span>

  - <span data-ttu-id="0e55b-109">Windows Server 2008 R2 Service Pack 1 (SP1) 标准操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-109">Windows Server 2008 R2 with Service Pack 1 (SP1) Standard operating system</span></span>

  - <span data-ttu-id="0e55b-110">Windows Server 2008 R2 与 SP1 企业版操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-110">Windows Server 2008 R2 with SP1 Enterprise operating system</span></span>

  - <span data-ttu-id="0e55b-111">Windows Server 2008 R2 与 SP1 Datacenter 操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-111">Windows Server 2008 R2 with SP1 Datacenter operating system</span></span>

  - <span data-ttu-id="0e55b-112">Windows Server 2012 Datacenter 操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-112">Windows Server 2012 Datacenter operating system</span></span>

  - <span data-ttu-id="0e55b-113">Windows Server 2012 标准操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-113">Windows Server 2012 Standard operating system</span></span>

  - <span data-ttu-id="0e55b-114">Windows Server 2012 企业版操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-114">Windows Server 2012 Enterprise operating system</span></span>

  - <span data-ttu-id="0e55b-115">Windows Server 2012 R2 Datacenter 操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-115">Windows Server 2012 R2 Datacenter operating system</span></span>

  - <span data-ttu-id="0e55b-116">Windows Server 2012 R2 标准操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-116">Windows Server 2012 R2 Standard operating system</span></span>

  - <span data-ttu-id="0e55b-117">Windows Server 2012 R2 企业版操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-117">Windows Server 2012 R2 Enterprise operating system</span></span>

  - <span data-ttu-id="0e55b-118">Windows 8 操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-118">Windows 8 operating system</span></span>

  - <span data-ttu-id="0e55b-119">Windows 7 操作系统</span><span class="sxs-lookup"><span data-stu-id="0e55b-119">Windows 7 operating system</span></span>

<span data-ttu-id="0e55b-120">计算机还必须运行以下内容：</span><span class="sxs-lookup"><span data-stu-id="0e55b-120">The computer must also be running the following:</span></span>

  - <span data-ttu-id="0e55b-121">Microsoft .NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="0e55b-121">Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="0e55b-122">对于 Lync Server 2013，必须先在服务器上手动安装64位版本的 Microsoft .NET Framework 4.5，然后再安装 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="0e55b-122">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span>

  - <span data-ttu-id="0e55b-123">Lync Server 2013、核心组件。</span><span class="sxs-lookup"><span data-stu-id="0e55b-123">Lync Server 2013, Core Components.</span></span>

  - <span data-ttu-id="0e55b-124">WMI 向后兼容程序包。</span><span class="sxs-lookup"><span data-stu-id="0e55b-124">WMI Backward Compatibility Package.</span></span> <span data-ttu-id="0e55b-125">有关详细信息，请参阅在迁移文档中 [安装 WMI 向后兼容性程序包](install-wmi-backward-compatibility-package.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e55b-125">For details, see [Install WMI Backward Compatibility package](install-wmi-backward-compatibility-package.md) in the Migration documentation.</span></span>

  - <span data-ttu-id="0e55b-126">Windows PowerShell 3.0。</span><span class="sxs-lookup"><span data-stu-id="0e55b-126">Windows PowerShell 3.0.</span></span> <span data-ttu-id="0e55b-127">有关详细信息，请参阅在部署文档中 [安装 Lync Server 2013 的 Windows PowerShell 3.0](lync-server-2013-installing-windows-powershell-3-0.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e55b-127">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) in the Deployment documentation.</span></span>

<span data-ttu-id="0e55b-128">你可以在安装了不运行 Lync Server 2013、Core 组件或 WMI 向后兼容性程序包的受支持操作系统的计算机上安装最佳做法分析器，但你只能在这些计算机上使用最佳做法分析器来查看报表，而不是运行扫描。</span><span class="sxs-lookup"><span data-stu-id="0e55b-128">You can install Best Practices Analyzer on computers with a supported operating system that are not running Lync Server 2013, Core Components or WMI Backward Compatibility Package, but you can use Best Practices Analyzer on those computers only to view reports, not to run scans.</span></span>

</div>

<div>

## <a name="choosing-a-computer-for-installation"></a><span data-ttu-id="0e55b-129">选择计算机进行安装</span><span class="sxs-lookup"><span data-stu-id="0e55b-129">Choosing a Computer for Installation</span></span>

<span data-ttu-id="0e55b-130">我们建议在专用于 Lync Server 2013 管理的计算机上安装 Lync Server 2013 和最佳做法分析器。</span><span class="sxs-lookup"><span data-stu-id="0e55b-130">We recommend that you install Lync Server 2013, Best Practices Analyzer on a computer that is dedicated to Lync Server 2013 management.</span></span> <span data-ttu-id="0e55b-131">可以在运行 Lync Server 2013 或运行 Lync Server 2013 管理工具的管理计算机的服务器上安装该工具。</span><span class="sxs-lookup"><span data-stu-id="0e55b-131">You can install the tool on a server running Lync Server 2013 or an administrative computer running Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="0e55b-132">如果在运行 Lync Server 的服务器上安装该工具，我们建议使用该工具仅扫描该服务器。</span><span class="sxs-lookup"><span data-stu-id="0e55b-132">If you install the tool on a server that is running Lync Server, we recommend that you use the tool to scan only that server.</span></span>

</div>

<div>

## <a name="installing-best-practices-analyzer"></a><span data-ttu-id="0e55b-133">安装最佳做法分析器</span><span class="sxs-lookup"><span data-stu-id="0e55b-133">Installing Best Practices Analyzer</span></span>

<span data-ttu-id="0e55b-134">您可以在下载 Lync Server 2013 的最佳做法分析器 [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539) 。</span><span class="sxs-lookup"><span data-stu-id="0e55b-134">You can download the Best Practices Analyzer for Lync Server 2013 at [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539).</span></span>

<span data-ttu-id="0e55b-135">若要安装最佳做法分析器，请在要安装该工具的计算机上启动 Microsoft 安装程序文件 RtcBPA.msi，然后按照屏幕上的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="0e55b-135">To install Best Practices Analyzer, start the Microsoft Installer file RtcBPA.msi on the computer where you want to install the tool, and then follow the instructions on the screen.</span></span> <span data-ttu-id="0e55b-136">用于安装程序文件的默认位置是 \<system drive\> \\ 程序文件 \\ Lync Server 2013 \\ BPA。</span><span class="sxs-lookup"><span data-stu-id="0e55b-136">The default location for installing the program files is \<system drive\>\\Program Files\\Lync Server 2013\\BPA.</span></span>

<span data-ttu-id="0e55b-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e55b-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

