---
title: Lync Server 2013：其他软件要求
description: Lync Server 2013：其他软件要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Additional software requirements
ms:assetid: 87b318e3-03ae-41f7-af5e-29bb294f6af0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398686(v=OCS.15)
ms:contentKeyID: 48184731
ms.date: 12/09/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbc36f23a2246c9d653e47954064182c756f0dff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443151"
---
# <a name="additional-software-requirements-for-lync-server-2013"></a><span data-ttu-id="89e43-103">Lync Server 2013 的其他软件要求</span><span class="sxs-lookup"><span data-stu-id="89e43-103">Additional software requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89e43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89e43-104">

<span> </span></span></span>

<span data-ttu-id="89e43-105">_**主题上次修改时间：** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="89e43-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="89e43-106">除了服务器平台的硬件和操作系统要求之外，Lync Server 2013 还需要在部署的服务器上安装其他软件。</span><span class="sxs-lookup"><span data-stu-id="89e43-106">In addition to the hardware and operating system requirements for server platforms, Lync Server 2013 requires the installation of additional software on the servers that you deploy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="89e43-107">有关运行 Lync Server 的服务器的平台要求的详细信息，请参阅 Lync server <A href="lync-server-2013-server-hardware-platforms.md">2013 的服务器硬件平台</A> 和 <A href="lync-server-2013-server-and-tools-operating-system-support.md">lync server 2013 中的服务器和工具操作系统支持</A>。</span><span class="sxs-lookup"><span data-stu-id="89e43-107">For details about the platform requirements for servers running Lync Server, see <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A> and <A href="lync-server-2013-server-and-tools-operating-system-support.md">Server and tools operating system support in Lync Server 2013</A>.</span></span> <span data-ttu-id="89e43-108">有关客户端计算机和设备的系统要求的详细信息，请参阅规划文档中 <A href="lync-server-2013-planning-for-clients-and-devices.md">Lync Server 2013 中的客户端和设备规划</A> 。</span><span class="sxs-lookup"><span data-stu-id="89e43-108">For details about system requirements for client computers and devices, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span> <span data-ttu-id="89e43-109">有关管理工具的软件要求的详细信息，请参阅 <A href="lync-server-2013-administrative-tools-software-requirements.md">Lync Server 2013 中的管理工具软件要求</A>。</span><span class="sxs-lookup"><span data-stu-id="89e43-109">For details about software requirements for administrative tools, see <A href="lync-server-2013-administrative-tools-software-requirements.md">Administrative tools software requirements in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="additional-software-necessary-for-all-internal-server-roles"></a><span data-ttu-id="89e43-110">所有内部服务器角色所需的其他软件</span><span class="sxs-lookup"><span data-stu-id="89e43-110">Additional Software Necessary for All Internal Server Roles</span></span>

<span data-ttu-id="89e43-111">本部分列出了所有内部服务器角色所必需的软件，这些角色是除 Edge 服务器之外的所有 Lync Server 服务器角色。</span><span class="sxs-lookup"><span data-stu-id="89e43-111">This section lists software necessary on all internal server roles, which are all Lync Server server roles except for Edge Server.</span></span> <span data-ttu-id="89e43-112">有关 Edge 服务器和边缘池的要求将在本主题的 " **其他软件适用于边缘服务器**" 下列出。</span><span class="sxs-lookup"><span data-stu-id="89e43-112">The requirements for the Edge Servers and Edge pools are listed later in this topic under **Additional Software for Edge Servers**.</span></span>

</div>

<div>

## <a name="windows-powershell-30"></a><span data-ttu-id="89e43-113">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="89e43-113">Windows PowerShell 3.0</span></span>

<span data-ttu-id="89e43-114">运行 Lync Server 2013 的每台服务器必须安装正确版本的 Windows PowerShell 3.0。</span><span class="sxs-lookup"><span data-stu-id="89e43-114">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="89e43-115">有关详细信息，请参阅 [安装 Lync Server 2013 的 Windows PowerShell 3.0](lync-server-2013-installing-windows-powershell-3-0.md)。</span><span class="sxs-lookup"><span data-stu-id="89e43-115">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

</div>

<div>

## <a name="microsoft-net-framework-45"></a><span data-ttu-id="89e43-116">Microsoft .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="89e43-116">Microsoft .NET Framework 4.5</span></span>

<span data-ttu-id="89e43-117">Lync Server 要求 Microsoft .NET Framework 4.5 位于所有内部服务器角色和任何运行 Lync Server 管理工具或 Microsoft Lync Server 2013 的计算机上的 "规划工具"。</span><span class="sxs-lookup"><span data-stu-id="89e43-117">Lync Server requires Microsoft .NET Framework 4.5 on all internal server roles and on any computer where you will run the Lync Server administrative tools or Microsoft Lync Server 2013, Planning Tool.</span></span> <span data-ttu-id="89e43-118">对于 Lync Server 2013，必须先在服务器上手动安装64位版本的 Microsoft .NET Framework 4.5，然后再安装 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="89e43-118">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="89e43-119">若要手动安装，请从 Microsoft 下载中心下载 Microsoft .NET 4.5 Framework [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="89e43-119">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

<div>

## <a name="installing-microsoft-net-framework-45-on-servers-running-windows-server-2012"></a><span data-ttu-id="89e43-120">在运行 Windows Server 2012 的服务器上安装 Microsoft .NET Framework 4。5</span><span class="sxs-lookup"><span data-stu-id="89e43-120">Installing Microsoft .NET Framework 4.5 on Servers Running Windows Server 2012</span></span>

<span data-ttu-id="89e43-121">在将运行 Lync Server 2013 和 Windows Server 2012 的服务器上安装 Microsoft .NET Framework 4.5 时，必须执行一个附加步骤。</span><span class="sxs-lookup"><span data-stu-id="89e43-121">When you install Microsoft .NET Framework 4.5 on servers that will run Lync Server 2013 and Windows Server 2012, you must perform one additional step.</span></span> <span data-ttu-id="89e43-122">安装 .NET Framework 4.5 后，请使用服务器管理器安装 HTTP 激活。</span><span class="sxs-lookup"><span data-stu-id="89e43-122">After .NET Framework 4.5 is installed, use Server Manager to install HTTP Activation.</span></span>

<span data-ttu-id="89e43-123">**在 Windows Server 2012 上安装 .NET 4.5 HTTP 激活**</span><span class="sxs-lookup"><span data-stu-id="89e43-123">**To Install .NET 4.5 HTTP Activation on Windows Server 2012**</span></span>

1.  <span data-ttu-id="89e43-124">从 " **开始** " 菜单中，单击 " **程序**"，然后单击 " **管理工具**"，然后单击 " **服务器管理器**"。</span><span class="sxs-lookup"><span data-stu-id="89e43-124">From the **Start** menu, click **Programs**, then click **Administrative Tools**, then click **Server Manager**.</span></span>

2.  <span data-ttu-id="89e43-125">在服务器管理器中的 " **功能摘要**" 下，选择 " **添加功能**"。</span><span class="sxs-lookup"><span data-stu-id="89e43-125">In Server Manager, under **Features Summary**, choose **Add Features**.</span></span>

3.  <span data-ttu-id="89e43-126">展开 **.Net Framework 4.5**。</span><span class="sxs-lookup"><span data-stu-id="89e43-126">Expand **.NET Framework 4.5**.</span></span>

4.  <span data-ttu-id="89e43-127">选择 " **WCF 激活** " （如果尚未选中）。</span><span class="sxs-lookup"><span data-stu-id="89e43-127">Select **WCF Activation** if it isn’t already selected.</span></span> <span data-ttu-id="89e43-128">然后选择 " **HTTP 激活**"。</span><span class="sxs-lookup"><span data-stu-id="89e43-128">Then select **HTTP Activation**.</span></span>

5.  <span data-ttu-id="89e43-129">单击 " **下一步** " 并按照提示完成安装。</span><span class="sxs-lookup"><span data-stu-id="89e43-129">Click **Next** and follow the prompts to finish the installation.</span></span>

</div>

</div>

<div>

## <a name="windows-identity-foundation"></a><span data-ttu-id="89e43-130">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="89e43-130">Windows Identity Foundation</span></span>

<span data-ttu-id="89e43-131">Lync Server 2013 中的 **Windows Identity foundation** 需要安装 Windows identity foundation 才能支持服务器到服务器身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="89e43-131">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="89e43-132">Windows Server 2008 R2 和 Windows Server 2012 需要不同的步骤来安装 Windows 识别基础。</span><span class="sxs-lookup"><span data-stu-id="89e43-132">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="89e43-133">从以下列表中选择服务器操作系统：</span><span class="sxs-lookup"><span data-stu-id="89e43-133">Select your server operating system from the following list:</span></span>

  - <span data-ttu-id="89e43-134">Windows server 2008 R2 For Windows Server 2008 R2，请检查它是否已安装在你的计算机上。</span><span class="sxs-lookup"><span data-stu-id="89e43-134">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="89e43-135">若要执行此操作，请转到 " **添加/删除程序**"、" **查看已安装的更新**"，然后在 **windows** 中查找 **(KB974405) 的入门级 windows Identity Foundation**。</span><span class="sxs-lookup"><span data-stu-id="89e43-135">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="89e43-136">有关安装 Windows Identity Foundation 的详细信息，请参阅 [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) 。</span><span class="sxs-lookup"><span data-stu-id="89e43-136">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="89e43-137">Windows server 2012 For Windows Server 2012，可使用 **服务器管理器** 安装 Windows Identity Foundation。</span><span class="sxs-lookup"><span data-stu-id="89e43-137">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="89e43-138">在服务器管理器 " **添加角色和功能" 向导** 中，选择 " **功能**"。</span><span class="sxs-lookup"><span data-stu-id="89e43-138">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="89e43-139">从列表中选择 **Windows Identity Foundation 3.5** 。</span><span class="sxs-lookup"><span data-stu-id="89e43-139">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="89e43-140">单击 " **下一步**"，然后单击 " **安装**"。</span><span class="sxs-lookup"><span data-stu-id="89e43-140">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="additional-software-for-all-front-end-servers-and-standard-edition-servers"></a><span data-ttu-id="89e43-141">适用于所有前端服务器和标准版服务器的其他软件</span><span class="sxs-lookup"><span data-stu-id="89e43-141">Additional Software for All Front End Servers and Standard Edition Servers</span></span>

<span data-ttu-id="89e43-142">所有前端服务器和标准版服务器还必须在特定模块 (IIS) 上运行 Internet 信息服务。</span><span class="sxs-lookup"><span data-stu-id="89e43-142">All Front End Servers and Standard Edition servers must also run Internet Information Services (IIS) with certain modules.</span></span> <span data-ttu-id="89e43-143">此外，所有前端服务器和标准版服务器（可在其中部署会议、呼叫驻留应用程序、公告或响应组）都必须运行 Windows Media 格式运行时。</span><span class="sxs-lookup"><span data-stu-id="89e43-143">Additionally, all Front End Servers and Standard Edition servers where conferencing, Call Park application, Announcement, or Response Groups are deployed must run Windows Media Format Runtime.</span></span>

<div>

## <a name="internet-information-services-iis"></a><span data-ttu-id="89e43-144">Internet 信息服务 (IIS)</span><span class="sxs-lookup"><span data-stu-id="89e43-144">Internet Information Services (IIS)</span></span>

<span data-ttu-id="89e43-145">前端服务器和标准版服务器必须 (IIS) 运行 Internet 信息服务，其中包含以下模块：</span><span class="sxs-lookup"><span data-stu-id="89e43-145">Front End Servers and Standard Edition servers must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="89e43-146">静态内容</span><span class="sxs-lookup"><span data-stu-id="89e43-146">Static Content</span></span>

  - <span data-ttu-id="89e43-147">默认文档</span><span class="sxs-lookup"><span data-stu-id="89e43-147">Default Document</span></span>

  - <span data-ttu-id="89e43-148">HTTP 错误</span><span class="sxs-lookup"><span data-stu-id="89e43-148">HTTP Errors</span></span>

  - <span data-ttu-id="89e43-149">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="89e43-149">ASP.NET</span></span>

  - <span data-ttu-id="89e43-150">.NET 扩展性</span><span class="sxs-lookup"><span data-stu-id="89e43-150">.NET Extensibility</span></span>

  - <span data-ttu-id="89e43-151">Internet Server API (ISAPI) 扩展</span><span class="sxs-lookup"><span data-stu-id="89e43-151">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="89e43-152">ISAPI 筛选器</span><span class="sxs-lookup"><span data-stu-id="89e43-152">ISAPI Filters</span></span>

  - <span data-ttu-id="89e43-153">HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="89e43-153">HTTP Logging</span></span>

  - <span data-ttu-id="89e43-154">日志记录工具</span><span class="sxs-lookup"><span data-stu-id="89e43-154">Logging Tools</span></span>

  - <span data-ttu-id="89e43-155">跟踪</span><span class="sxs-lookup"><span data-stu-id="89e43-155">Tracing</span></span>

  - <span data-ttu-id="89e43-156">Windows 身份验证</span><span class="sxs-lookup"><span data-stu-id="89e43-156">Windows Authentication</span></span>

  - <span data-ttu-id="89e43-157">请求筛选</span><span class="sxs-lookup"><span data-stu-id="89e43-157">Request Filtering</span></span>

  - <span data-ttu-id="89e43-158">静态内容压缩</span><span class="sxs-lookup"><span data-stu-id="89e43-158">Static Content Compression</span></span>

  - <span data-ttu-id="89e43-159">动态内容压缩</span><span class="sxs-lookup"><span data-stu-id="89e43-159">Dynamic Content Compression</span></span>

  - <span data-ttu-id="89e43-160">IIS 管理控制台</span><span class="sxs-lookup"><span data-stu-id="89e43-160">IIS Management Console</span></span>

  - <span data-ttu-id="89e43-161">IIS 管理脚本和工具</span><span class="sxs-lookup"><span data-stu-id="89e43-161">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="89e43-162">匿名身份验证 (在安装 IIS 时默认安装此功能。 ) </span><span class="sxs-lookup"><span data-stu-id="89e43-162">Anonymous Authentication (this is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="89e43-163">客户端证书映射身份验证</span><span class="sxs-lookup"><span data-stu-id="89e43-163">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="windows-media-format-runtime-and-windows-desktop-experience"></a><span data-ttu-id="89e43-164">Windows Media 格式运行时和 Windows 桌面体验</span><span class="sxs-lookup"><span data-stu-id="89e43-164">Windows Media Format Runtime and Windows Desktop Experience</span></span>

<span data-ttu-id="89e43-165">**Windows 桌面体验** 部署会议的所有前端服务器和标准版服务器都必须安装 Windows Media 格式运行时，但 Windows 桌面体验中安装的 windows Server 2012 除外。</span><span class="sxs-lookup"><span data-stu-id="89e43-165">**Windows Desktop Experience** All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed, which, except for Windows Server 2012 is installed as part of the Windows desktop experience.</span></span> <span data-ttu-id="89e43-166">Windows Server 2012 需要 Microsoft Media Foundation。</span><span class="sxs-lookup"><span data-stu-id="89e43-166">Windows Server 2012 requires Microsoft Media Foundation.</span></span> <span data-ttu-id="89e43-167">若要运行 windows Media 音频 ( .wma) 文件（呼叫寄存、公告和响应组应用程序为公告和音乐播放），需要 Windows Media 格式运行时。</span><span class="sxs-lookup"><span data-stu-id="89e43-167">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>

<span data-ttu-id="89e43-168">我们建议你在安装 Lync Server 2013 之前安装 Windows 桌面体验。</span><span class="sxs-lookup"><span data-stu-id="89e43-168">We recommend that you install Windows desktop experience before you install Lync Server 2013.</span></span> <span data-ttu-id="89e43-169">如果 Lync Server 2013 在服务器上找不到此软件，它将提示您安装它，然后必须重新启动服务器才能完成安装。</span><span class="sxs-lookup"><span data-stu-id="89e43-169">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

</div>

</div>

<div>

## <a name="additional-software-for-front-end-servers-and-standard-edition-servers-running-on-windows-server-2012"></a><span data-ttu-id="89e43-170">在 Windows Server 2012 上运行的前端服务器和标准版服务器的附加软件</span><span class="sxs-lookup"><span data-stu-id="89e43-170">Additional Software for Front End Servers and Standard Edition Servers Running on Windows Server 2012</span></span>

<span data-ttu-id="89e43-171">前端服务器需要安装 .NET 3.5，默认情况下不会在 Windows Server 2012 上安装。</span><span class="sxs-lookup"><span data-stu-id="89e43-171">Front End Servers require .NET 3.5, which is not installed by default on Windows Server 2012.</span></span> <span data-ttu-id="89e43-172">若要安装，请将 Windows Server 2012 安装媒体置于驱动器 D 中，然后键入以下内容：</span><span class="sxs-lookup"><span data-stu-id="89e43-172">To install it, put your Windows Server 2012 installation media in Drive D and type the following:</span></span>

    Add-WindowsFeature RSAT-ADDS, Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Compat, Desktop-Experience, Telnet-Client, BITS -Source D:\sources\sxs

<span data-ttu-id="89e43-173">有关在运行 Windows Server 2012 的服务器上安装 .NET 3.5 的详细信息，请参阅 "Microsoft .NET Framework 3.5 部署注意事项" <https://go.microsoft.com/fwlink/p/?linkid=275032> 。</span><span class="sxs-lookup"><span data-stu-id="89e43-173">For details about installing .NET 3.5 on servers running Windows Server 2012, see "Microsoft .NET Framework 3.5 Deployment Considerations" at <https://go.microsoft.com/fwlink/p/?linkid=275032>.</span></span>

</div>

<div>

## <a name="additional-software-for-directors"></a><span data-ttu-id="89e43-174">适用于董事的其他软件</span><span class="sxs-lookup"><span data-stu-id="89e43-174">Additional Software for Directors</span></span>

<span data-ttu-id="89e43-175">控制器必须 (IIS) 运行 Internet 信息服务，并提供以下模块：</span><span class="sxs-lookup"><span data-stu-id="89e43-175">Directors must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="89e43-176">静态内容</span><span class="sxs-lookup"><span data-stu-id="89e43-176">Static Content</span></span>

  - <span data-ttu-id="89e43-177">默认文档</span><span class="sxs-lookup"><span data-stu-id="89e43-177">Default Document</span></span>

  - <span data-ttu-id="89e43-178">HTTP 错误</span><span class="sxs-lookup"><span data-stu-id="89e43-178">HTTP Errors</span></span>

  - <span data-ttu-id="89e43-179">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="89e43-179">ASP.NET</span></span>

  - <span data-ttu-id="89e43-180">.NET 扩展性</span><span class="sxs-lookup"><span data-stu-id="89e43-180">.NET Extensibility</span></span>

  - <span data-ttu-id="89e43-181">Internet Server API (ISAPI) 扩展</span><span class="sxs-lookup"><span data-stu-id="89e43-181">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="89e43-182">ISAPI 筛选器</span><span class="sxs-lookup"><span data-stu-id="89e43-182">ISAPI Filters</span></span>

  - <span data-ttu-id="89e43-183">HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="89e43-183">HTTP Logging</span></span>

  - <span data-ttu-id="89e43-184">日志记录工具</span><span class="sxs-lookup"><span data-stu-id="89e43-184">Logging Tools</span></span>

  - <span data-ttu-id="89e43-185">跟踪</span><span class="sxs-lookup"><span data-stu-id="89e43-185">Tracing</span></span>

  - <span data-ttu-id="89e43-186">Windows 身份验证</span><span class="sxs-lookup"><span data-stu-id="89e43-186">Windows Authentication</span></span>

  - <span data-ttu-id="89e43-187">请求筛选</span><span class="sxs-lookup"><span data-stu-id="89e43-187">Request Filtering</span></span>

  - <span data-ttu-id="89e43-188">静态内容压缩</span><span class="sxs-lookup"><span data-stu-id="89e43-188">Static Content Compression</span></span>

  - <span data-ttu-id="89e43-189">IIS 管理控制台</span><span class="sxs-lookup"><span data-stu-id="89e43-189">IIS Management Console</span></span>

  - <span data-ttu-id="89e43-190">IIS 管理脚本和工具</span><span class="sxs-lookup"><span data-stu-id="89e43-190">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="89e43-191">匿名身份验证 (在安装 IIS 时默认安装此功能。 ) </span><span class="sxs-lookup"><span data-stu-id="89e43-191">Anonymous Authentication (This is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="89e43-192">客户端证书映射身份验证</span><span class="sxs-lookup"><span data-stu-id="89e43-192">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="additional-software-for-persistent-chat-front-end-servers"></a><span data-ttu-id="89e43-193">适用于持久聊天前端服务器的其他软件</span><span class="sxs-lookup"><span data-stu-id="89e43-193">Additional Software for Persistent Chat Front End Servers</span></span>

<span data-ttu-id="89e43-194">持久聊天前端服务器必须运行消息队列 (也称为 MSMQ) ，它是 Windows Server 的一个组件。</span><span class="sxs-lookup"><span data-stu-id="89e43-194">Persistent Chat Front End Servers must run Message Queuing (also known as MSMQ), which is a component of Windows Server.</span></span>

<span data-ttu-id="89e43-195">有关启用 MSMQ 的信息，请 [单击此处。](https://technet.microsoft.com/library/cc771474.aspx)</span><span class="sxs-lookup"><span data-stu-id="89e43-195">For information on enabling MSMQ, [click here.](https://technet.microsoft.com/library/cc771474.aspx)</span></span>

</div>

<div>

## <a name="additional-software-for-edge-servers"></a><span data-ttu-id="89e43-196">适用于边缘服务器的其他软件</span><span class="sxs-lookup"><span data-stu-id="89e43-196">Additional Software for Edge Servers</span></span>

<span data-ttu-id="89e43-197">边缘服务器需要以下软件：</span><span class="sxs-lookup"><span data-stu-id="89e43-197">Edge Servers require the following software:</span></span>

  - <span data-ttu-id="89e43-198">运行 Lync Server 2013 的每台服务器必须安装正确版本的 Windows PowerShell 3.0。</span><span class="sxs-lookup"><span data-stu-id="89e43-198">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="89e43-199">有关详细信息，请参阅 [安装 Lync Server 2013 的 Windows PowerShell 3.0](lync-server-2013-installing-windows-powershell-3-0.md)。</span><span class="sxs-lookup"><span data-stu-id="89e43-199">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

  - <span data-ttu-id="89e43-200">Lync 服务器需要 Microsoft .NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="89e43-200">Lync Server requires Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="89e43-201">对于安装在 Windows Server 2008 R2 上的 Lync Server 2013，必须在安装 Lync Server 2013 之前在服务器上手动安装64位版本的 Microsoft .NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="89e43-201">For Lync Server 2013 installed on Windows Server 2008 R2, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="89e43-202">若要手动安装，请从 Microsoft 下载中心下载 Microsoft .NET 4.5 Framework [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="89e43-202">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

  - <span data-ttu-id="89e43-203">Lync Server 2013 中的 **Windows Identity foundation** 需要安装 Windows identity foundation 才能支持服务器到服务器身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="89e43-203">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="89e43-204">Windows Server 2008 R2 和 Windows Server 2012 需要不同的步骤来安装 Windows 识别基础。</span><span class="sxs-lookup"><span data-stu-id="89e43-204">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="89e43-205">从以下列表中选择服务器操作系统：</span><span class="sxs-lookup"><span data-stu-id="89e43-205">Select your server operating system from the following list:</span></span>
    
      - <span data-ttu-id="89e43-206">Windows server 2008 R2 For Windows Server 2008 R2，请检查它是否已安装在你的计算机上。</span><span class="sxs-lookup"><span data-stu-id="89e43-206">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="89e43-207">若要执行此操作，请转到 " **添加/删除程序**"、" **查看已安装的更新**"，然后在 **windows** 中查找 **(KB974405) 的入门级 windows Identity Foundation**。</span><span class="sxs-lookup"><span data-stu-id="89e43-207">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="89e43-208">有关安装 Windows Identity Foundation 的详细信息，请参阅 [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) 。</span><span class="sxs-lookup"><span data-stu-id="89e43-208">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>
    
      - <span data-ttu-id="89e43-209">Windows server 2012 For Windows Server 2012，可使用 **服务器管理器** 安装 Windows Identity Foundation。</span><span class="sxs-lookup"><span data-stu-id="89e43-209">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="89e43-210">在服务器管理器 " **添加角色和功能" 向导** 中，选择 " **功能**"。</span><span class="sxs-lookup"><span data-stu-id="89e43-210">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="89e43-211">从列表中选择 **Windows Identity Foundation 3.5** 。</span><span class="sxs-lookup"><span data-stu-id="89e43-211">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="89e43-212">单击 " **下一步**"，然后单击 " **安装**"。</span><span class="sxs-lookup"><span data-stu-id="89e43-212">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="do-not-install-layered-socket-providers-on-media-servers"></a><span data-ttu-id="89e43-213">不要在媒体服务器上安装分层套接字提供程序</span><span class="sxs-lookup"><span data-stu-id="89e43-213">Do Not Install Layered Socket Providers on Media Servers</span></span>

<span data-ttu-id="89e43-214">不要在任何前端服务器或独立中介服务器上安装任何 Microsoft Internet 安全和加速 (ISA) 服务器客户端软件或任何其他 Winsock 分层服务提供程序 (LSP) 软件。</span><span class="sxs-lookup"><span data-stu-id="89e43-214">Do not install any Microsoft Internet Security and Acceleration (ISA) Server client software, or any other Winsock Layered Service Providers (LSP) software, on any Front End Servers or stand-alone Mediation Servers.</span></span> <span data-ttu-id="89e43-215">安装此软件可能会导致媒体流量较差。</span><span class="sxs-lookup"><span data-stu-id="89e43-215">Installing this software could cause poor media traffic performance.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="89e43-216">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89e43-216">See Also</span></span>


[<span data-ttu-id="89e43-217">Lync Server 2013 中的管理工具软件要求</span><span class="sxs-lookup"><span data-stu-id="89e43-217">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
  

<span data-ttu-id="89e43-218"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89e43-218"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

