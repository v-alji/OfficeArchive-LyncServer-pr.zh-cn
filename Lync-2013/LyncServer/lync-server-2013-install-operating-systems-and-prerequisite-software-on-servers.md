---
title: 在服务器上安装操作系统和必备软件
description: 在服务器上安装操作系统和必备软件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install operating systems and prerequisite software on servers
ms:assetid: 055991e0-5aeb-43fc-a7ba-d4b02316d73b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398103(v=OCS.15)
ms:contentKeyID: 48183288
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2bae9e57db9c2f1d3f3bde7ce9cc7071b73aa01d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427171"
---
# <a name="install-operating-systems-and-prerequisite-software-on-servers-for-lync-server-2013"></a><span data-ttu-id="2b604-103">在服务器上安装适用于 Lync Server 2013 的操作系统和必备软件</span><span class="sxs-lookup"><span data-stu-id="2b604-103">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b604-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b604-104">

<span> </span></span></span>

<span data-ttu-id="2b604-105">_**主题上次修改时间：** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="2b604-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="2b604-106">设置硬件和系统基础结构后，除了要部署的每台服务器上的所有其他必备软件外，还需要安装相应的 Windows 操作系统和更新。</span><span class="sxs-lookup"><span data-stu-id="2b604-106">After you have set up the hardware and system infrastructure, you need to install the appropriate Windows operating systems and updates, in addition to all other prerequisite software on each server that you are deploying.</span></span> <span data-ttu-id="2b604-107">这包括每个 Lync Server 2013 服务器角色以及运行你的部署所需的任何其他基础结构服务器或运行 SQL Server 的服务器。</span><span class="sxs-lookup"><span data-stu-id="2b604-107">This includes each Lync Server 2013 server role and any additional infrastructure servers or servers running SQL Server that are required for your deployment.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="2b604-108">本部分介绍安装内部服务器的操作系统和必备软件。</span><span class="sxs-lookup"><span data-stu-id="2b604-108">This section describes installation of operating systems and prerequisite software for internal servers.</span></span> <span data-ttu-id="2b604-109">如果要部署边缘服务器以支持外部用户访问，还需要为这些服务器安装操作系统和必备软件，包括边缘服务器和反向代理服务器。</span><span class="sxs-lookup"><span data-stu-id="2b604-109">If you are deploying Edge Servers to support external user access, you also need to install operating systems and prerequisite software for those servers, including Edge Servers and reverse proxy servers.</span></span> <span data-ttu-id="2b604-110">有关准备服务器以支持外部用户访问的详细信息，请参阅部署文档中 <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Lync Server 2013 的外围网络中的服务器安装准备</A> 。</span><span class="sxs-lookup"><span data-stu-id="2b604-110">For details about preparing servers to support external user access, see <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Preparing for installation of servers in the perimeter network for Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="install-windows-operating-systems-on-servers"></a><span data-ttu-id="2b604-111">在服务器上安装 Windows 操作系统</span><span class="sxs-lookup"><span data-stu-id="2b604-111">Install Windows Operating Systems on Servers</span></span>

<span data-ttu-id="2b604-112">在要部署的每台服务器上，安装相应的 Windows 操作系统，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2b604-112">On each server that you are deploying, install the appropriate Windows operating system as follows:</span></span>

  - <span data-ttu-id="2b604-113">**运行 Lync Server 2013 的服务器**   有关运行 Lync Server 2013 的服务器的操作系统要求的详细信息，请参阅支持文档中 [Lync server 2013 中的 "服务器和工具操作系统支持](lync-server-2013-server-and-tools-operating-system-support.md) "。</span><span class="sxs-lookup"><span data-stu-id="2b604-113">**Servers running Lync Server 2013**   For details about the operating system requirements for servers running Lync Server 2013, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="2b604-114">**数据库服务器**   有关数据库服务器的操作系统要求的详细信息，包括后端数据库、存档数据库和监视数据库，请参阅 SQL Server 文档。</span><span class="sxs-lookup"><span data-stu-id="2b604-114">**Database servers**   For details about operating system requirements for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server documentation.</span></span> <span data-ttu-id="2b604-115">有关 SQL Server 2012，请参阅中的 SQL Server 2012 联机丛书 [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。</span><span class="sxs-lookup"><span data-stu-id="2b604-115">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="2b604-116">如果在 Windows Server 2008 R2 上使用 SP1 安装 Lync Server 2013 &nbsp; &nbsp; ，则必须首先安装 Microsoft 知识库文章2646886中所述的更新： "修复：当模块调用 IIS 7.5 中的 InsertEntityBody 方法时出现堆损坏"，时间<A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp 为; kbid = 2646886</A>。</span><span class="sxs-lookup"><span data-stu-id="2b604-116">If you are installing Lync Server 2013 on Windows Server&nbsp;2008&nbsp;R2 with SP1, you must first install the update described in the Microsoft Knowledge Based article 2646886, “FIX: Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5”, at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=2646886</A>.</span></span><BR><span data-ttu-id="2b604-117">你还必须修改注册表，如知识库文章中所述，在 <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Windows server 2012 R2 中安装的 Lync Server 2013 前端服务器中记录事件 id 32402、61045</A>。</span><span class="sxs-lookup"><span data-stu-id="2b604-117">You must also modify the registry as described in the KB article, <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Event IDs 32402, 61045 are logged in Lync Server 2013 Front End servers that are installed in Windows Server 2012 R2</A>.</span></span>



</div>

</div>

<div>

## <a name="install-windows-update-on-servers"></a><span data-ttu-id="2b604-118">在服务器上安装 Windows 更新</span><span class="sxs-lookup"><span data-stu-id="2b604-118">Install Windows Update on Servers</span></span>

<span data-ttu-id="2b604-119">在每台服务器上安装 Windows 更新中的以下更新：</span><span class="sxs-lookup"><span data-stu-id="2b604-119">Install the following updates from Windows Update on each server:</span></span>

  - <span data-ttu-id="2b604-120">**运行 Lync Server 2013 的服务器的 Windows 更新**   有关运行 Lync Server 2013 的服务器所需的 Windows 更新更新的详细信息，请参阅规划文档中 [Lync Server 2013 的其他软件要求](lync-server-2013-additional-software-requirements.md) 。</span><span class="sxs-lookup"><span data-stu-id="2b604-120">**Windows Update for servers running Lync Server 2013**   For details about the updates from Windows Update that are required for servers running Lync Server 2013, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="2b604-121">**数据库服务器**   有关数据库服务器（包括后端数据库、存档数据库和监视数据库）所需的 Windows 更新更新的详细信息，请参阅 SQL Server 2012 文档。</span><span class="sxs-lookup"><span data-stu-id="2b604-121">**Database servers**   For details about the updates from Windows Update that are required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation.</span></span> <span data-ttu-id="2b604-122">有关 SQL Server 2012，请参阅中的 SQL Server 2012 联机丛书 [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。</span><span class="sxs-lookup"><span data-stu-id="2b604-122">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

</div>

<div>

## <a name="install-other-prerequisite-software-on-servers"></a><span data-ttu-id="2b604-123">在服务器上安装其他必备软件</span><span class="sxs-lookup"><span data-stu-id="2b604-123">Install Other Prerequisite Software on Servers</span></span>

<span data-ttu-id="2b604-124">Lync Server 2013 要求在服务器上安装以下其他软件：</span><span class="sxs-lookup"><span data-stu-id="2b604-124">Lync Server 2013 requires the installation of the following additional software on servers:</span></span>

  - <span data-ttu-id="2b604-125">**运行 Lync Server 2013 的服务器的必备软件**   运行 Lync Server 2013 的服务器的其他必备软件必备条件取决于要部署的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="2b604-125">**Prerequisite software for servers running Lync Server 2013**   The additional software prerequisites for servers running Lync Server 2013 depend on the server role being deployed.</span></span> <span data-ttu-id="2b604-126">有关每台服务器的特定软件要求的详细信息，请参阅规划文档中 [Lync server 2013 的其他软件要求](lync-server-2013-additional-software-requirements.md) 。</span><span class="sxs-lookup"><span data-stu-id="2b604-126">For details about the specific software requirements for each server, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="2b604-127">**Windows Identity Foundation**   Lync Server 2013 需要安装 Windows Identity Foundation 才能支持服务器到服务器的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="2b604-127">**Windows Identity Foundation**   Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server-to-server authentication scenarios.</span></span> <span data-ttu-id="2b604-128">若要验证是否已在计算机上安装，请转到 "控制面板"，单击 " **程序和功能**"， **查看已安装的更新**，然后查看 " **Microsoft Windows**"。</span><span class="sxs-lookup"><span data-stu-id="2b604-128">To verify that it has already been installed on your computer, go to Control Panel, click **Programs and Features**, **View installed updates**, and look under **Microsoft Windows**.</span></span> <span data-ttu-id="2b604-129">有关安装 Windows Identity Foundation 的详细信息，请参阅 [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) 。</span><span class="sxs-lookup"><span data-stu-id="2b604-129">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="2b604-130">**Microsoft .Net Framework 4.5**   Lync Server 2013 需要64位版本的 Microsoft .NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="2b604-130">**Microsoft .NET Framework 4.5**   The 64-bit edition of Microsoft .NET Framework 4.5 is required for Lync Server 2013.</span></span>

  - <span data-ttu-id="2b604-131">**数据库服务器的必备软件**   有关数据库服务器（包括后端数据库、存档数据库和监视数据库）所需的 Windows 更新的详细信息，请参阅 SQL Server 2012 文档 [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) 。</span><span class="sxs-lookup"><span data-stu-id="2b604-131">**Prerequisite software for database servers**   For details about the Windows Update required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="2b604-132">Lync Server 2013 会在每个标准版服务器以及运行本地配置存储所在的 Lync Server 2013 的每台服务器上自动安装 Microsoft SQL Server 2012 Express。</span><span class="sxs-lookup"><span data-stu-id="2b604-132">Lync Server 2013 automatically installs Microsoft SQL Server 2012 Express on each Standard Edition server and each server running Lync Server 2013 on which the local configuration store is located.</span></span>

    
    </div>

  - <span data-ttu-id="2b604-133">**Windows Media 格式运行时**   将部署会议的所有前端服务器和标准版服务器必须安装 Windows Media Format Runtime。</span><span class="sxs-lookup"><span data-stu-id="2b604-133">**Windows Media Format Runtime**   All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed.</span></span> <span data-ttu-id="2b604-134">若要运行 windows Media 音频 ( .wma) 文件（呼叫寄存、公告和响应组应用程序为公告和音乐播放），需要 Windows Media 格式运行时。</span><span class="sxs-lookup"><span data-stu-id="2b604-134">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="2b604-135">对于 Windows Server 2012 和 Windows Server 2012 R2 Windows Media 格式运行时与 Microsoft Media Foundation 一起安装。</span><span class="sxs-lookup"><span data-stu-id="2b604-135">For Windows Server 2012 and Windows Server 2012 R2 the Windows Media Format Runtime installs with Microsoft Media Foundation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="2b604-136">对于 Windows Server &nbsp; 2008 和 Windows server &nbsp; 2008 &nbsp; R2 Windows Media 格式运行时作为 windows 桌面体验的一部分进行安装。</span><span class="sxs-lookup"><span data-stu-id="2b604-136">For Windows Server&nbsp;2008 and Windows Server&nbsp;2008&nbsp;R2 the Windows Media Format Runtime installs as part of the Windows Desktop Experience.</span></span> <span data-ttu-id="2b604-137">建议在安装 Lync Server 2013 之前安装 Windows 桌面体验。</span><span class="sxs-lookup"><span data-stu-id="2b604-137">It is recommended that you install Windows Desktop Experience before you install Lync Server 2013.</span></span> <span data-ttu-id="2b604-138">如果 Lync Server 2013 在服务器上找不到此软件，它将提示您安装它，然后必须重新启动服务器才能完成安装。</span><span class="sxs-lookup"><span data-stu-id="2b604-138">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

    
    <span data-ttu-id="2b604-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b604-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

