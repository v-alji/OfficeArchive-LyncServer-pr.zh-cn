---
title: Lync Server 2013：IIS 配置
description: Lync Server 2013： IIS 配置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS configuration
ms:assetid: b458babf-bf64-43f0-8a8e-612f5096b63c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412871(v=OCS.15)
ms:contentKeyID: 48185169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 901aca7bf5ff8824b54e93754569a6ef5defc10e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427430"
---
# <a name="iis-configuration-in-lync-server-2013"></a><span data-ttu-id="3038e-103">Lync Server 2013 中的 IIS 配置</span><span class="sxs-lookup"><span data-stu-id="3038e-103">IIS configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3038e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3038e-104">

<span> </span></span></span>

<span data-ttu-id="3038e-105">_**主题上次修改时间：** 2014-02-17_</span><span class="sxs-lookup"><span data-stu-id="3038e-105">_**Topic Last Modified:** 2014-02-17_</span></span>

<span data-ttu-id="3038e-106">若要成功完成此过程，你应作为本地管理员和域用户至少登录到服务器。</span><span class="sxs-lookup"><span data-stu-id="3038e-106">To successfully complete this procedure, you should be logged on to the server minimally as a local administrator and a domain user.</span></span>

<span data-ttu-id="3038e-107">在池中配置和安装 Lync Server 2013、标准版或第一个前端服务器的前端服务器之前，请为 Internet 信息服务 (IIS) 安装和配置服务器角色和 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="3038e-107">Before you configure and install the Front End Server for Lync Server 2013, Standard Edition or the first Front End Server in a pool, you install and configure the server role and Web Services for Internet Information Services (IIS).</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="3038e-108">如果你的组织要求在除系统驱动器之外的驱动器上查找 IIS 和所有 Web 服务，你可以在初始安装 Lync Server 2013 管理工具时，在 "设置" 对话框中更改 Lync Server 2013 文件的安装位置路径。</span><span class="sxs-lookup"><span data-stu-id="3038e-108">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box when you initially install the Lync Server 2013 Administrative tools.</span></span> <span data-ttu-id="3038e-109">在安装 IIS 之前安装 "管理工具"。</span><span class="sxs-lookup"><span data-stu-id="3038e-109">You install the Administrative tools before installing IIS.</span></span> <span data-ttu-id="3038e-110">如果将安装文件安装到此路径（包括 OCSCore.msi），则会将其他 Lync Server 2013 文件也部署到此驱动器。</span><span class="sxs-lookup"><span data-stu-id="3038e-110">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span> <span data-ttu-id="3038e-111">有关 dtails，请参阅 <A href="lync-server-2013-install-lync-server-administrative-tools.md">安装 Lync Server 2013 管理工具</A>。</span><span class="sxs-lookup"><span data-stu-id="3038e-111">For dtails, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A>.</span></span> <span data-ttu-id="3038e-112">有关如何重新定位 Windows Server Manager 在安装 IIS 时部署的 INETPUB 的详细信息，请参阅 <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> 。</span><span class="sxs-lookup"><span data-stu-id="3038e-112">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>



</div>

<span data-ttu-id="3038e-113">下表指示所需的 IIS 7.5 角色服务。</span><span class="sxs-lookup"><span data-stu-id="3038e-113">The following table indicates the required IIS 7.5 role services.</span></span>

### <a name="iis-75-role-services"></a><span data-ttu-id="3038e-114">IIS 7.5 角色服务</span><span class="sxs-lookup"><span data-stu-id="3038e-114">IIS 7.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3038e-115">角色标题</span><span class="sxs-lookup"><span data-stu-id="3038e-115">Role Heading</span></span></th>
<th><span data-ttu-id="3038e-116">角色服务</span><span class="sxs-lookup"><span data-stu-id="3038e-116">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3038e-117">已安装常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-117">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="3038e-118">静态内容</span><span class="sxs-lookup"><span data-stu-id="3038e-118">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-119">已安装常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-119">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="3038e-120">默认文档</span><span class="sxs-lookup"><span data-stu-id="3038e-120">Default document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-121">已安装常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-121">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="3038e-122">HTTP 错误</span><span class="sxs-lookup"><span data-stu-id="3038e-122">HTTP errors</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-123">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-123">Application development</span></span></p></td>
<td><p><span data-ttu-id="3038e-124">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="3038e-124">ASP.NET</span></span></p>
<p><span data-ttu-id="3038e-125">Windows Server 2012 还需要 ASP。 NET 4。5</span><span class="sxs-lookup"><span data-stu-id="3038e-125">Windows Server 2012 also requires ASP.NET4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-126">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-126">Application development</span></span></p></td>
<td><p><span data-ttu-id="3038e-127">.NET 扩展性</span><span class="sxs-lookup"><span data-stu-id="3038e-127">.NET extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-128">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-128">Application development</span></span></p></td>
<td><p><span data-ttu-id="3038e-129">Internet Server API (ISAPI) 扩展</span><span class="sxs-lookup"><span data-stu-id="3038e-129">Internet Server API (ISAPI) extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-130">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-130">Application development</span></span></p></td>
<td><p><span data-ttu-id="3038e-131">ISAPI 筛选器</span><span class="sxs-lookup"><span data-stu-id="3038e-131">ISAPI filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-132">运行状况和诊断</span><span class="sxs-lookup"><span data-stu-id="3038e-132">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="3038e-133">HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="3038e-133">HTTP logging</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-134">运行状况和诊断</span><span class="sxs-lookup"><span data-stu-id="3038e-134">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="3038e-135">日志记录工具</span><span class="sxs-lookup"><span data-stu-id="3038e-135">Logging tools</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-136">运行状况和诊断</span><span class="sxs-lookup"><span data-stu-id="3038e-136">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="3038e-137">跟踪</span><span class="sxs-lookup"><span data-stu-id="3038e-137">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-138">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-138">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-139">默认情况下， (安装和启用匿名身份验证) </span><span class="sxs-lookup"><span data-stu-id="3038e-139">Anonymous authentication (installed and enabled by default)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-140">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-140">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-141">Windows 身份验证</span><span class="sxs-lookup"><span data-stu-id="3038e-141">Windows authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-142">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-142">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-143">客户端证书映射身份验证</span><span class="sxs-lookup"><span data-stu-id="3038e-143">Client Certificate Mapping authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-144">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-144">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-145">请求筛选</span><span class="sxs-lookup"><span data-stu-id="3038e-145">Request filtering</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-146">性能</span><span class="sxs-lookup"><span data-stu-id="3038e-146">Performance</span></span></p></td>
<td><p><span data-ttu-id="3038e-147">静态内容压缩</span><span class="sxs-lookup"><span data-stu-id="3038e-147">Static content compression</span></span></p>
<p><span data-ttu-id="3038e-148">动态内容压缩</span><span class="sxs-lookup"><span data-stu-id="3038e-148">Dynamic content compression</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-149">管理工具</span><span class="sxs-lookup"><span data-stu-id="3038e-149">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="3038e-150">IIS 管理控制台</span><span class="sxs-lookup"><span data-stu-id="3038e-150">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-151">管理工具</span><span class="sxs-lookup"><span data-stu-id="3038e-151">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="3038e-152">IIS 管理脚本和工具</span><span class="sxs-lookup"><span data-stu-id="3038e-152">IIS Management Scripts and Tools</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3038e-153">在 Windows Server 2008 R2 SP1 x64 操作系统上，你可以使用 Windows PowerShell 2.0。</span><span class="sxs-lookup"><span data-stu-id="3038e-153">On the Windows Server 2008 R2 SP1 x64 operating system, you can use Windows PowerShell 2.0.</span></span> <span data-ttu-id="3038e-154">必须首先导入 ServerManager 模块，然后安装 IIS 7.5 角色和角色服务。</span><span class="sxs-lookup"><span data-stu-id="3038e-154">You must first import the ServerManager module, and then install the IIS 7.5 role and role services.</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Scripting-Tools, Web-Windows-Auth, Web-Asp-Net, Web-Log-Libraries, Web-Http-Tracing, Web-Stat-Compression, Web-Dyn-Compression, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Errors, Web-Http-Logging, Web-Net-Ext, Web-Client-Auth, Web-Filtering, Web-Mgmt-Console
   ```

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="3038e-155">默认情况下，使用 IIS 服务器角色安装匿名身份验证。</span><span class="sxs-lookup"><span data-stu-id="3038e-155">Anonymous authentication is installed by default with the IIS server role.</span></span> <span data-ttu-id="3038e-156">在安装 IIS 之后，您可以管理匿名身份验证。</span><span class="sxs-lookup"><span data-stu-id="3038e-156">You can manage anonymous authentication after the installation of IIS.</span></span> <span data-ttu-id="3038e-157">有关详细信息，请参阅 "启用匿名身份验证 (IIS 7) " <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A> 。</span><span class="sxs-lookup"><span data-stu-id="3038e-157">For details, see “Enable Anonymous Authentication (IIS 7)” at <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A>.</span></span>



</div>

<span data-ttu-id="3038e-158">下表指示 Windows Server 2012 和 Windows Server 2012 R2 所需的 IIS 8.0 和 IIS 8.5 角色服务。</span><span class="sxs-lookup"><span data-stu-id="3038e-158">The following table indicates the required IIS 8.0 and IIS 8.5 role services for Windows Server 2012 and Windows Server 2012 R2.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="3038e-159">对于 Windows Server 2012 和 Windows Server 2012 R2，Add-WindowsFeature cmdlet 已替换为 Install-WindowsFeature cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3038e-159">For Windows Server 2012 and Windows Server 2012 R2, the Add-WindowsFeature cmdlet has been replaced by the Install-WindowsFeature cmdlet.</span></span> <span data-ttu-id="3038e-160">有关详细信息，请参阅 <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">安装-add-windowsfeature</A>。</span><span class="sxs-lookup"><span data-stu-id="3038e-160">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-WindowsFeature</A>.</span></span>



</div>

### <a name="iis-80-and-iis-85-role-services"></a><span data-ttu-id="3038e-161">IIS 8.0 和 IIS 8.5 角色服务</span><span class="sxs-lookup"><span data-stu-id="3038e-161">IIS 8.0 and IIS 8.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3038e-162">角色标题</span><span class="sxs-lookup"><span data-stu-id="3038e-162">Role Heading</span></span></th>
<th><span data-ttu-id="3038e-163">角色服务</span><span class="sxs-lookup"><span data-stu-id="3038e-163">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3038e-164"> (IIS) 的 Web 服务器</span><span class="sxs-lookup"><span data-stu-id="3038e-164">Web Server (IIS)</span></span></p></td>
<td><p><span data-ttu-id="3038e-165">Web 服务器</span><span class="sxs-lookup"><span data-stu-id="3038e-165">Web Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-166">常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-166">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-167">默认文档</span><span class="sxs-lookup"><span data-stu-id="3038e-167">Default Document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-168">常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-168">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-169">目录浏览</span><span class="sxs-lookup"><span data-stu-id="3038e-169">Directory Browsing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-170">常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-170">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-171">HTTP 错误</span><span class="sxs-lookup"><span data-stu-id="3038e-171">HTTP Errors</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-172">常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-172">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-173">静态内容</span><span class="sxs-lookup"><span data-stu-id="3038e-173">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-174">常见的 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="3038e-174">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-175">HTTP 重定向</span><span class="sxs-lookup"><span data-stu-id="3038e-175">HTTP Redirection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-176">运行状况和诊断</span><span class="sxs-lookup"><span data-stu-id="3038e-176">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="3038e-177">HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="3038e-177">HTTP Logging</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-178">运行状况和诊断</span><span class="sxs-lookup"><span data-stu-id="3038e-178">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="3038e-179">日志记录工具</span><span class="sxs-lookup"><span data-stu-id="3038e-179">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-180">运行状况和诊断</span><span class="sxs-lookup"><span data-stu-id="3038e-180">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="3038e-181">请求监视器</span><span class="sxs-lookup"><span data-stu-id="3038e-181">Request Monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-182">运行状况和诊断</span><span class="sxs-lookup"><span data-stu-id="3038e-182">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="3038e-183">跟踪</span><span class="sxs-lookup"><span data-stu-id="3038e-183">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-184">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-184">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-185">请求筛选</span><span class="sxs-lookup"><span data-stu-id="3038e-185">Request Filtering</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-186">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-186">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-187">基本身份验证</span><span class="sxs-lookup"><span data-stu-id="3038e-187">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-188">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-188">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-189">客户端证书映射身份验证</span><span class="sxs-lookup"><span data-stu-id="3038e-189">Client Certificate Mapping Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-190">安全性</span><span class="sxs-lookup"><span data-stu-id="3038e-190">Security</span></span></p></td>
<td><p><span data-ttu-id="3038e-191">Windows 身份验证</span><span class="sxs-lookup"><span data-stu-id="3038e-191">Windows Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-192">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-192">Application Development</span></span></p></td>
<td><p><span data-ttu-id="3038e-193">.Net 扩展性3。5</span><span class="sxs-lookup"><span data-stu-id="3038e-193">.Net Extensibility 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-194">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-194">Application Development</span></span></p></td>
<td><p><span data-ttu-id="3038e-195">.Net 扩展性4。5</span><span class="sxs-lookup"><span data-stu-id="3038e-195">.Net Extensibility 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-196">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-196">Application Development</span></span></p></td>
<td><p><span data-ttu-id="3038e-197">ASP.Net 3。5</span><span class="sxs-lookup"><span data-stu-id="3038e-197">ASP.Net 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-198">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-198">Application Development</span></span></p></td>
<td><p><span data-ttu-id="3038e-199">ASP.Net 4。5</span><span class="sxs-lookup"><span data-stu-id="3038e-199">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-200">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-200">Application Development</span></span></p></td>
<td><p><span data-ttu-id="3038e-201">ISAPI 扩展</span><span class="sxs-lookup"><span data-stu-id="3038e-201">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-202">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-202">Application Development</span></span></p></td>
<td><p><span data-ttu-id="3038e-203">ISAPI 筛选器</span><span class="sxs-lookup"><span data-stu-id="3038e-203">ISAPI Filters</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-204">应用程序开发</span><span class="sxs-lookup"><span data-stu-id="3038e-204">Application Development</span></span></p></td>
<td><p><span data-ttu-id="3038e-205">服务器端包含</span><span class="sxs-lookup"><span data-stu-id="3038e-205">Server Side Includes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-206">管理工具</span><span class="sxs-lookup"><span data-stu-id="3038e-206">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="3038e-207">IIS 管理控制台</span><span class="sxs-lookup"><span data-stu-id="3038e-207">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-208">管理工具</span><span class="sxs-lookup"><span data-stu-id="3038e-208">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="3038e-209">IIS 6 元数据库兼容性</span><span class="sxs-lookup"><span data-stu-id="3038e-209">IIS 6 Metabase compatibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-210">管理工具</span><span class="sxs-lookup"><span data-stu-id="3038e-210">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="3038e-211">IIS 管理脚本和工具</span><span class="sxs-lookup"><span data-stu-id="3038e-211">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-212">.Net 3.5 框架功能</span><span class="sxs-lookup"><span data-stu-id="3038e-212">.Net 3.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-213">.Net 3.5 Framework</span><span class="sxs-lookup"><span data-stu-id="3038e-213">.Net 3.5 Framework</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-214">.Net 4.5 框架功能</span><span class="sxs-lookup"><span data-stu-id="3038e-214">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-215">.Net Framework 4。5</span><span class="sxs-lookup"><span data-stu-id="3038e-215">.Net Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-216">.Net 4.5 框架功能</span><span class="sxs-lookup"><span data-stu-id="3038e-216">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-217">ASP.Net 4。5</span><span class="sxs-lookup"><span data-stu-id="3038e-217">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-218">.Net 4.5 框架功能</span><span class="sxs-lookup"><span data-stu-id="3038e-218">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-219">HTTP 激活</span><span class="sxs-lookup"><span data-stu-id="3038e-219">HTTP Activation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-220">.Net 4.5 框架功能</span><span class="sxs-lookup"><span data-stu-id="3038e-220">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="3038e-221">TCP 端口共享</span><span class="sxs-lookup"><span data-stu-id="3038e-221">TCP Port Sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-222">后台智能传送服务</span><span class="sxs-lookup"><span data-stu-id="3038e-222">Background Intelligent Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="3038e-223">IIS 服务器扩展</span><span class="sxs-lookup"><span data-stu-id="3038e-223">IIS Server Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-224">墨迹和手写服务</span><span class="sxs-lookup"><span data-stu-id="3038e-224">Ink and Handwriting Services</span></span></p></td>
<td><p><span data-ttu-id="3038e-225">墨迹和手写服务</span><span class="sxs-lookup"><span data-stu-id="3038e-225">Ink and Handwriting Services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-226">媒体基础</span><span class="sxs-lookup"><span data-stu-id="3038e-226">Media Foundation</span></span></p></td>
<td><p><span data-ttu-id="3038e-227">媒体基础</span><span class="sxs-lookup"><span data-stu-id="3038e-227">Media Foundation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-228">用户界面和基础结构</span><span class="sxs-lookup"><span data-stu-id="3038e-228">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="3038e-229">图形管理工具和基础结构</span><span class="sxs-lookup"><span data-stu-id="3038e-229">Graphical Management Tools and Infrastructure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-230">用户界面和基础结构</span><span class="sxs-lookup"><span data-stu-id="3038e-230">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="3038e-231">桌面体验</span><span class="sxs-lookup"><span data-stu-id="3038e-231">Desktop Experience</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-232">用户界面和基础结构</span><span class="sxs-lookup"><span data-stu-id="3038e-232">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="3038e-233">服务器图形 Shell</span><span class="sxs-lookup"><span data-stu-id="3038e-233">Server Graphical Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-234">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="3038e-234">Windows Identity Foundation 3.5</span></span></p></td>
<td><p><span data-ttu-id="3038e-235">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="3038e-235">Windows Identity Foundation 3.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3038e-236">Windows 进程激活服务</span><span class="sxs-lookup"><span data-stu-id="3038e-236">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="3038e-237">流程模型</span><span class="sxs-lookup"><span data-stu-id="3038e-237">Process Model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3038e-238">Windows 进程激活服务</span><span class="sxs-lookup"><span data-stu-id="3038e-238">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="3038e-239">配置 Api</span><span class="sxs-lookup"><span data-stu-id="3038e-239">Configuration APIs</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3038e-240">在 Windows Server 2012 和 Windows Server 2012 R2 中，你可以使用 Windows PowerShell 3.0 来安装 IIS 要求。</span><span class="sxs-lookup"><span data-stu-id="3038e-240">In Windows Server 2012 and Windows Server 2012 R2, you can use Windows PowerShell 3.0 to install the IIS Requirements.</span></span> <span data-ttu-id="3038e-241">使用 Windows PowerShell 3.0 中的 ServerManager 模块，请键入：</span><span class="sxs-lookup"><span data-stu-id="3038e-241">Using the ServerManager module in Windows PowerShell 3.0, type:</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-Framework-45-Core, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Console, Web-Mgmt-Compat, Windows-Identity-Foundation, Server-Media-Foundation, BITS -Source D:\sources\sxs
   ```

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="3038e-242">Windows Server 2012 的新增功能是-Source 参数，用于定义可在何处找到 Windows Server 2012 源媒体。</span><span class="sxs-lookup"><span data-stu-id="3038e-242">New with Windows Server 2012 is the –Source parameter that defines where the Windows Server 2012 source media can be found.</span></span> <span data-ttu-id="3038e-243">媒体可以定义为 DVD 驱动器 (例如，D:\Sources\Sxs) 或网络共享，以便媒体文件已复制 (例如， \\ fileserver\windows2012\sources\Sxs) 。</span><span class="sxs-lookup"><span data-stu-id="3038e-243">The media can be defined as a DVD drive (for example, D:\Sources\Sxs), or to a network share that the media files have been copied (for example, \\fileserver\windows2012\sources\Sxs).</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3038e-244">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3038e-244">See Also</span></span>


[<span data-ttu-id="3038e-245">Lync Server 2013 中前端池和 Standard Edition 服务器的 IIS 要求</span><span class="sxs-lookup"><span data-stu-id="3038e-245">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)  
  

<span data-ttu-id="3038e-246"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3038e-246"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

