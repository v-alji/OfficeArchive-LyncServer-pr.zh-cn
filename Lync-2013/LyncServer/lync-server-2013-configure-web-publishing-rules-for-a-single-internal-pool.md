---
title: Lync Server 2013：为单个内部池配置 Web 发布规则
description: Lync Server 2013：为单个内部池配置 web 发布规则。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure web publishing rules for a single internal pool
ms:assetid: 86ff4b2a-1ba9-46a2-a175-8b19e00a49dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429712(v=OCS.15)
ms:contentKeyID: 48184725
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45015c90fdac92fb488affc871f2cfaf9d7506a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433533"
---
# <a name="configure-web-publishing-rules-for-a-single-internal-pool-in-lync-server-2013"></a><span data-ttu-id="fc943-103">在 Lync Server 2013 中为单个内部池配置 Web 发布规则</span><span class="sxs-lookup"><span data-stu-id="fc943-103">Configure web publishing rules for a single internal pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc943-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc943-104">

<span> </span></span></span>

<span data-ttu-id="fc943-105">_**主题上次修改时间：** 2014-07-07_</span><span class="sxs-lookup"><span data-stu-id="fc943-105">_**Topic Last Modified:** 2014-07-07_</span></span>

<span data-ttu-id="fc943-106">Microsoft Forefront 威胁管理网关2010和 Internet Information Server 应用程序请求路由 (IIS ARR) 使用 web 发布规则将内部资源（如会议 URL）发布到 Internet 上的用户。</span><span class="sxs-lookup"><span data-stu-id="fc943-106">Microsoft Forefront Threat Management Gateway 2010 and Internet Information Server Application Request Routing (IIS ARR) uses web publishing rules to publish internal resources, such as a meeting URL, to users on the Internet.</span></span>

<span data-ttu-id="fc943-107">除了虚拟目录的 Web 服务 Url 之外，还必须为简单 Url、LyncDiscover URL 和 Office Web Apps 服务器创建发布规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-107">In addition to the Web Services URLs for the virtual directories, you must also create publishing rules for simple URLs, the LyncDiscover URL, and the Office Web Apps Server.</span></span> <span data-ttu-id="fc943-108">对于每个简单的 URL，必须在指向该简单 URL 的反向代理上创建单个规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-108">For each simple URL, you must create an individual rule on the reverse proxy that points to that simple URL.</span></span>

<span data-ttu-id="fc943-109">如果你要部署移动版并使用自动发现，你需要为外部自动发现服务 URL 创建发布规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-109">If you are deploying mobility and using automatic discovery, you need to create a publishing rule for the external Autodiscover Service URL.</span></span> <span data-ttu-id="fc943-110">自动发现还需要用于你的 Director 池和前端池的外部 Lync Server Web Services URL 的发布规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-110">Automatic discovery also requires publishing rules for the external Lync Server Web Services URL for your Director pool and Front End pool.</span></span> <span data-ttu-id="fc943-111">有关创建用于自动发现的 web 发布规则的详细信息，请参阅 [在 Lync Server 2013 中配置反向代理以进行移动](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)。</span><span class="sxs-lookup"><span data-stu-id="fc943-111">For details about creating the web publishing rules for automatic discovery, see [Configuring the reverse proxy for mobility in Lync Server 2013](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md).</span></span>

<span data-ttu-id="fc943-112">使用以下过程创建 web 发布规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-112">Use the following procedures to create web publishing rules.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fc943-113">这些过程假设你已安装了标准版 Forefront 威胁管理网关 (TMG) 2010 或已使用应用程序请求路由 (IIS ARR) 扩展安装和配置了 Internet 信息服务器。</span><span class="sxs-lookup"><span data-stu-id="fc943-113">These procedures assume that you have installed the Standard Edition of Forefront Threat Management Gateway (TMG) 2010 or have installed and configured Internet Information Server with the Application request Routing (IIS ARR) extension.</span></span> <span data-ttu-id="fc943-114">您使用的是 TMG 或 IIS ARR。</span><span class="sxs-lookup"><span data-stu-id="fc943-114">You use either TMG or IIS ARR.</span></span>



</div>

<div>

## <a name="to-create-a-web-server-publishing-rule-on-the-computer-running-tmg-2010"></a><span data-ttu-id="fc943-115">在运行 TMG 2010 的计算机上创建 web 服务器发布规则</span><span class="sxs-lookup"><span data-stu-id="fc943-115">To create a web server publishing rule on the computer running TMG 2010</span></span>

1.  <span data-ttu-id="fc943-116">单击 " **开始**"，选择 " **程序**"，选择 " **Microsoft Forefront tmg**"，然后单击 " **Forefront tmg 管理**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-116">Click **Start**, select **Programs**, select **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="fc943-117">在左窗格中，展开 " **服务器名**"，右键单击 " **防火墙策略**"，选择 " **新建**"，然后单击 "网站 **发布规则**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-117">In the left pane, expand **ServerName**, right-click **Firewall Policy**, select **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="fc943-118">在 " **欢迎使用新 Web 发布规则** " 页面上，键入发布规则 (的显示名称，例如，LyncServerWebDownloadsRule) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-118">On the **Welcome to the New Web Publishing Rule** page, type a display name for the publishing rule (for example, LyncServerWebDownloadsRule).</span></span>

4.  <span data-ttu-id="fc943-119">在 " **选择规则操作** " 页面上，选择 " **允许**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-119">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="fc943-120">在 " **发布类型** " 页面上，选择 " **发布单个网站" 或 "负载平衡器**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-120">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="fc943-121">在 " **服务器连接安全** " 页面上，选择 **"使用 SSL 连接到发布的 Web 服务器或服务器场"**。</span><span class="sxs-lookup"><span data-stu-id="fc943-121">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="fc943-122">在 " **内部发布详细信息** " 页面上，在 "内部 **网站名称** " 框中键入托管会议内容和通讯簿内容的内部 web 场的完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-122">On the **Internal Publishing Details** page, type the fully qualified domain name (FQDN) of the internal web farm that hosts your meeting content and Address Book content in the **Internal Site name** box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fc943-123">如果内部服务器是标准版服务器，则该 FQDN 是标准版服务器 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fc943-123">If your internal server is a Standard Edition server, this FQDN is the Standard Edition server FQDN.</span></span> <span data-ttu-id="fc943-124">如果内部服务器是前端池，则该 FQDN 是硬件负载平衡器虚拟 IP (VIP) 负载平衡内部 web 场服务器。</span><span class="sxs-lookup"><span data-stu-id="fc943-124">If your internal server is a Front End pool, this FQDN is a hardware load balancer virtual IP (VIP) that load balances the internal web farm servers.</span></span> <span data-ttu-id="fc943-125">TMG 服务器必须能够将 FQDN 解析为内部 web 服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="fc943-125">The TMG server must be able to resolve the FQDN to the IP address of the internal web server.</span></span> <span data-ttu-id="fc943-126">如果 TMG 服务器无法将 FQDN 解析为正确的 IP 地址，则可以选择 " <STRONG>使用计算机名称或 ip 地址连接到已发布的服务器</STRONG>"，然后在 " <STRONG>计算机名称或</STRONG> <STRONG>ip 地址</STRONG> " 框中键入内部 web 服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="fc943-126">If the TMG server is not able to resolve the FQDN to the proper IP address, you can select <STRONG>Use a computer name or IP address to connect to the published server</STRONG>, and then in the <STRONG>Computer name or</STRONG> <STRONG>IP address</STRONG> box, type the IP address of the internal web server.</span></span> <span data-ttu-id="fc943-127">如果执行此操作，必须确保 TMG 服务器上的端口53处于打开状态，并且它可以访问位于外围网络中的 DNS 服务器。</span><span class="sxs-lookup"><span data-stu-id="fc943-127">If you do this, you must ensure that port 53 is open on the TMG server and that it can reach a DNS server that resides in the perimeter network.</span></span> <span data-ttu-id="fc943-128">您也可以使用本地 hosts 文件中的条目来提供名称解析。</span><span class="sxs-lookup"><span data-stu-id="fc943-128">You can also use entries in the local hosts file to provide name resolution.</span></span>

    
    </div>

8.  <span data-ttu-id="fc943-129">在 " **内部发布详细信息** " 页面上，在 " **路径 (可选)** " 框中，键入 \* */\** _ 作为要发布的文件夹的路径。</span><span class="sxs-lookup"><span data-stu-id="fc943-129">On the **Internal Publishing Details** page, in the **Path (optional)** box, type \**/\** _ as the path of the folder to be published.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fc943-130">在网站发布向导中，只能指定一个路径。</span><span class="sxs-lookup"><span data-stu-id="fc943-130">In the website publishing wizard you can only specify one path.</span></span> <span data-ttu-id="fc943-131">可通过修改规则的属性来添加其他路径。</span><span class="sxs-lookup"><span data-stu-id="fc943-131">Additional paths can be added by modifying the properties of the rule.</span></span>

    
    </div>

9.  <span data-ttu-id="fc943-132">在 "_ \*公用名称详细信息**" 页面上，确认在 "**接受请求**" 下选择了 **此域名**，在 "**公共名称\*\*" 框中键入外部 Web 服务 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fc943-132">On the _ *Public Name Details*\* page, confirm that **This domain name** is selected under **Accept Requests for**, type the external Web Services FQDN, in the **Public Name** box.</span></span>

10. <span data-ttu-id="fc943-133">在 " **选择 Web 侦听器** " 页面上，单击 " **新建** " 以打开 "新建 Web 侦听器定义" 向导。</span><span class="sxs-lookup"><span data-stu-id="fc943-133">On **Select Web Listener** page, click **New** to open the New Web Listener Definition Wizard.</span></span>

11. <span data-ttu-id="fc943-134">在 " **欢迎使用新建 Web 侦听器向导** " 页面上，在 " **web 侦听器名称** " 框中键入 web 侦听器的名称 (例如，LyncServerWebServers) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-134">On the **Welcome to the New Web Listener Wizard** page, type a name for the web listener in the **Web listener name** box (for example, LyncServerWebServers).</span></span>

12. <span data-ttu-id="fc943-135">在 " **客户端连接安全** " 页面上，选择 " **要求与客户端的 SSL 安全连接**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-135">On the **Client Connection Security** page, select **Require SSL secured connections with clients**.</span></span>

13. <span data-ttu-id="fc943-136">在 " **Web 侦听器 IP 地址** " 页面上，选择 " **外部**"，然后单击 " **选择 IP 地址**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-136">On the **Web Listener IP Address** page, select **External**, and then click **Select IP Addresses**.</span></span>

14. <span data-ttu-id="fc943-137">在 " **外部侦听器 IP 选择** " 页面上，选择 **所选网络中 Forefront TMG 计算机上的 "指定 ip 地址**"，选择适当的 ip 地址，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-137">On the **External Listener IP selection** page, select **Specified IP address on the Forefront TMG computer in the selected network**, select the appropriate IP address, click **Add**.</span></span>

15. <span data-ttu-id="fc943-138">在 " **侦听器 SSL 证书** " 页面上，选择 " **为每个 IP 地址分配证书**"，选择与外部 web FQDN 相关联的 IP 地址，然后单击 " **选择证书**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-138">On the **Listener SSL Certificates** page, select **Assign a certificate for each IP address**, select the IP address that is associated with the external web FQDN, and then click **Select Certificate**.</span></span>

16. <span data-ttu-id="fc943-139">在 " **选择证书** " 页面上，选择与步骤9中指定的公共名称相匹配的证书，单击 " **选择**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-139">On the **Select Certificate** page, select the certificate that matches the public names specified in step 9, click **Select**.</span></span>

17. <span data-ttu-id="fc943-140">在 " **身份验证设置** " 页面上，选择 " **无身份验证**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-140">On the **Authentication Setting** page, select **No Authentication**.</span></span>

18. <span data-ttu-id="fc943-141">在 " **单一登录设置** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-141">On the **Single Sign On Setting** page, click **Next**.</span></span>

19. <span data-ttu-id="fc943-142">在 " **正在完成 Web 侦听器向导** " 页面上，验证 **web 侦听器** 设置是否正确，然后单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-142">On the **Completing the Web Listener Wizard** page, verify that the **Web listener** settings are correct, and then click **Finish**.</span></span>

20. <span data-ttu-id="fc943-143">在 " **身份验证委派** " 页面上，选择 " **无委派"，但客户端可以直接进行身份验证**。</span><span class="sxs-lookup"><span data-stu-id="fc943-143">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly**.</span></span>

21. <span data-ttu-id="fc943-144">在 " **用户设置** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-144">On the **User Set** page, click **Next**.</span></span>

22. <span data-ttu-id="fc943-145">在 " **正在完成新建 Web 发布规则向导** " 页面上，验证 Web 发布规则设置是否正确，然后单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-145">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

23. <span data-ttu-id="fc943-146">单击 "详细信息" 窗格中的 " **应用** " 以保存更改并更新配置。</span><span class="sxs-lookup"><span data-stu-id="fc943-146">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

</div>

<div>

## <a name="to-create-a-web-server-publishing-rule-on-the-computer-running-iis-arr"></a><span data-ttu-id="fc943-147">在运行 IIS ARR 的计算机上创建 web 服务器发布规则</span><span class="sxs-lookup"><span data-stu-id="fc943-147">To create a web server publishing rule on the computer running IIS ARR</span></span>

1.  <span data-ttu-id="fc943-148">将用于反向代理的证书绑定到 HTTPS 协议。</span><span class="sxs-lookup"><span data-stu-id="fc943-148">Bind the certificate that you will use for the reverse proxy to the HTTPS protocol.</span></span> <span data-ttu-id="fc943-149">单击 " **开始**"，选择 " **程序**"，选择 " **管理工具**"，然后单击 " **Internet 信息服务" (IIS) 管理器**。</span><span class="sxs-lookup"><span data-stu-id="fc943-149">Click **Start**, select **Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fc943-150">有关部署和配置 IIS ARR 的其他帮助、屏幕截图和指南可在 NextHop 文章中找到， <A href="https://go.microsoft.com/fwlink/?linkid=293391">使用 IIS arr 作为 Lync Server 2013 的反向代理</A>。</span><span class="sxs-lookup"><span data-stu-id="fc943-150">Additional help, screen shots and guidance on deploying and configuring IIS ARR can be found in the NextHop article <A href="https://go.microsoft.com/fwlink/?linkid=293391">Using IIS ARR as a Reverse Proxy for Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="fc943-151">如果尚未执行此操作，请导入将用于反向代理的证书。</span><span class="sxs-lookup"><span data-stu-id="fc943-151">If you have not already done so, import the certificate that you will use for the reverse proxy.</span></span> <span data-ttu-id="fc943-152">在 " **Internet 信息服务 (IIS) 管理器**" 中，单击控制台左侧大小的反向代理服务器名称。</span><span class="sxs-lookup"><span data-stu-id="fc943-152">In **Internet Information Services (IIS) Manager**, click the reverse proxy server name on the left-hand size of the console.</span></span> <span data-ttu-id="fc943-153">在位于控制台中间的 " **IIS** " 下，找到 " **服务器证书**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-153">In the middle of the console under **IIS** locate **Server Certificates**.</span></span> <span data-ttu-id="fc943-154">右键单击 " **服务器证书** "，然后选择 " **打开功能**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-154">Right-click **Server Certificates** and select **Open feature**.</span></span>

3.  <span data-ttu-id="fc943-155">在控制台右侧，单击 " **导入 ...**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-155">On the right hand side of the console, click **Import…**.</span></span> <span data-ttu-id="fc943-156">键入带有扩展名的证书的路径和文件名，或单击 " **...** "。</span><span class="sxs-lookup"><span data-stu-id="fc943-156">Type the path and filename of the certificate with the extension, or click **…**</span></span> <span data-ttu-id="fc943-157">浏览证书。</span><span class="sxs-lookup"><span data-stu-id="fc943-157">to browse for the certificate.</span></span> <span data-ttu-id="fc943-158">选择证书，然后单击 " **打开**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-158">Select the certificate and click **Open**.</span></span> <span data-ttu-id="fc943-159">如果在导出证书和私钥) 时分配了密码，则提供用于保护私钥 (的密码。</span><span class="sxs-lookup"><span data-stu-id="fc943-159">Supply the password used to protect the private key (if you assigned a password when exporting the certificate and private key).</span></span> <span data-ttu-id="fc943-160">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="fc943-160">Click **OK**.</span></span> <span data-ttu-id="fc943-161">如果证书导入成功，证书将在控制台中间显示为 " **服务器证书**" 中的条目。</span><span class="sxs-lookup"><span data-stu-id="fc943-161">If the certificate import was successful, the certificate will appear as an entry in the middle of the console as an entry in **Server Certificates**.</span></span>

4.  <span data-ttu-id="fc943-162">分配用于 HTTPS 的证书。</span><span class="sxs-lookup"><span data-stu-id="fc943-162">Assign the certificate for use by HTTPS.</span></span> <span data-ttu-id="fc943-163">在控制台的左侧，选择 IIS 服务器的 **默认网站** 。</span><span class="sxs-lookup"><span data-stu-id="fc943-163">On the left-hand side of the console, select the **Default Web Site** of the IIS server.</span></span> <span data-ttu-id="fc943-164">单击右侧的 " **绑定 ...**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-164">On the right-hand side, click **Bindings…**.</span></span> <span data-ttu-id="fc943-165">在 " **网站绑定** " 对话框中，单击 " **添加 ...**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-165">In the **Site Bindings** dialog, click **Add…**.</span></span> <span data-ttu-id="fc943-166">在 "**类型：**" 下的 "**添加网站绑定**" 对话框中，选择 " **https**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-166">On the **Add Site Binding** dialog under **Type:**, select **https**.</span></span> <span data-ttu-id="fc943-167">选择 "https" 将允许你选择要用于 https 的证书。</span><span class="sxs-lookup"><span data-stu-id="fc943-167">Selecting https will allow you to select the certificate to use for https.</span></span> <span data-ttu-id="fc943-168">在 " **SSL 证书：**" 下，选择为反向代理导入的证书。</span><span class="sxs-lookup"><span data-stu-id="fc943-168">Under **SSL certificate:**, select the certificate that you imported for the reverse proxy.</span></span> <span data-ttu-id="fc943-169">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="fc943-169">Click **OK**.</span></span> <span data-ttu-id="fc943-170">然后单击 " **关闭**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-170">Then, click **Close**.</span></span> <span data-ttu-id="fc943-171">证书现在绑定到安全套接字层的反向代理 (SSL) 和传输层安全 (TLS) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-171">The certificate is now bound to the reverse proxy for secure socket layer (SSL) and transport layer security (TLS).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fc943-172">如果在关闭中间证书缺少的绑定对话框时收到警告，则需要查找并导入公共 CA 根颁发机构证书和任何中间 CA 证书。</span><span class="sxs-lookup"><span data-stu-id="fc943-172">If you receive a warning when closing the Bindings dialogs that intermediate certificates are missing, you need to locate and import the public CA root authority certificate and any intermediate CA certificates.</span></span> <span data-ttu-id="fc943-173">请参阅您请求证书的公共 CA 中的说明，然后按照说明请求和导入证书链。</span><span class="sxs-lookup"><span data-stu-id="fc943-173">Consult the instructions at the public CA that you requested your certificate from and follow the instructions to request and import a certificate chain.</span></span> <span data-ttu-id="fc943-174">如果你从 Edge 服务器导出证书，则可以导出根 CA 证书和与边缘服务器关联的任何中间 CA 证书。</span><span class="sxs-lookup"><span data-stu-id="fc943-174">If you exported the certificate from your Edge Server, you can export the root CA certificate and any intermediate CA certificates associated with the Edge Server.</span></span> <span data-ttu-id="fc943-175">将根 CA 证书导入计算机的 (不要与用户存储) 受信任的根证书颁发机构存储和中间证书混淆到计算机的 "中间证书颁发机构" 存储。</span><span class="sxs-lookup"><span data-stu-id="fc943-175">Import the root CA certificate into the Computer’s (not to be confused with the User store) Trusted Root Certification Authorities store and intermediate certificates into the Computer’s Intermediate Certification Authorities store.</span></span>

    
    </div>

5.  <span data-ttu-id="fc943-176">在控制台左侧的 IIS 服务器名称下，右键单击 " **服务器场** "，然后单击 " **创建服务器场 ...**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-176">On the left-hand side of the console below the IIS server name, right-click **Server Farms** then click **Create Server Farm…**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fc943-177">如果看不到 " <STRONG>服务器场</STRONG> " 节点，则需要安装应用程序请求路由。</span><span class="sxs-lookup"><span data-stu-id="fc943-177">If you do not see the <STRONG>Server Farms</STRONG> node, you need to install Application Request Routing.</span></span> <span data-ttu-id="fc943-178">有关详细信息，请参阅为 <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Lync Server 2013 设置反向代理服务器</A>。</span><span class="sxs-lookup"><span data-stu-id="fc943-178">For details, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="fc943-179">在 "**服务器场名称**" 中的 "**创建服务器场**" 对话框中，键入一个名称 (此名称可以是用于标识用途的友好名称) 第一个 URL。</span><span class="sxs-lookup"><span data-stu-id="fc943-179">On the **Create Server Farm** dialog in **Server farm name**, type the a name (this can be a friendly name for identification purposes) for the first URL.</span></span> <span data-ttu-id="fc943-180">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-180">Click **Next**.</span></span>

6.  <span data-ttu-id="fc943-181">在 "**服务器地址**" 中的 "**添加服务器**" 对话框中，键入您的前端服务器上的外部 web 服务的完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-181">On the **Add Server** dialog in **Server Address**, type the fully qualified domain name (FQDN) of the external web services on your Front End Server.</span></span> <span data-ttu-id="fc943-182">在此处用作示例的名称与在 "反向代理"、" [证书摘要-Lync Server 2013 中的反向代理](lync-server-2013-certificate-summary-reverse-proxy.md)" 的 "计划" 部分中使用的名称相同。</span><span class="sxs-lookup"><span data-stu-id="fc943-182">The names that will be used here for example purposes are the same that are used in the Planning section for the reverse proxy, [Certificate summary - Reverse proxy in Lync Server 2013](lync-server-2013-certificate-summary-reverse-proxy.md).</span></span> <span data-ttu-id="fc943-183">参考反向代理计划，我们键入 FQDN `webext.contoso.com` 。</span><span class="sxs-lookup"><span data-stu-id="fc943-183">Referring to the reverse proxy planning, we type the FQDN `webext.contoso.com`.</span></span> <span data-ttu-id="fc943-184">确认 " **联机** " 旁边的复选框处于选中状态。</span><span class="sxs-lookup"><span data-stu-id="fc943-184">Confirm that the checkbox next to **Online** is selected.</span></span> <span data-ttu-id="fc943-185">单击 " **添加** "，将服务器添加到此配置的 web 服务器池中。</span><span class="sxs-lookup"><span data-stu-id="fc943-185">Click **Add** to add the server to the pool of web servers for this configuration.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="fc943-186">Lync 服务器使用硬件负载平衡器对 HTTP 和 HTTPS 流量进行池控制器和前端服务器的缓冲。</span><span class="sxs-lookup"><span data-stu-id="fc943-186">Lync Server uses hardware load balancers to pool Director and Front End Servers for HTTP and HTTPS traffic.</span></span> <span data-ttu-id="fc943-187">将服务器添加到 IIS ARR 服务器场时，你将仅提供一个 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fc943-187">You will only supply one FQDN when adding a server to the IIS ARR Server Farm.</span></span> <span data-ttu-id="fc943-188">FQDN 将是在非池中的服务器配置中的前端服务器或控制器，或者是为服务器池配置的硬件负载平衡器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fc943-188">The FQDN will be the Front End Server or Director in non-pooled server configurations, or the FQDN of the configured hardware load balancer for server pools.</span></span> <span data-ttu-id="fc943-189">负载平衡 HTTP 和 HTTPS 流量的唯一支持方法是使用硬件负载平衡器。</span><span class="sxs-lookup"><span data-stu-id="fc943-189">The only supported method to load balance HTTP and HTTPS traffic is by using hardware load balancers.</span></span>

    
    </div>

7.  <span data-ttu-id="fc943-190">在 " **添加服务器** " 对话框中，单击 " **高级设置 ...**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-190">On the **Add Server** dialog, click **Advanced settings…**.</span></span> <span data-ttu-id="fc943-191">这将打开一个对话框，用于为已配置的 FQDN 的请求定义应用程序请求路由。</span><span class="sxs-lookup"><span data-stu-id="fc943-191">This opens a dialog to define application request routing for requests to the configured FQDN.</span></span> <span data-ttu-id="fc943-192">目的是在通过 IIS ARR 处理请求时重新定义要使用的端口。</span><span class="sxs-lookup"><span data-stu-id="fc943-192">The purpose is to redefine what port is used when the request is processed by IIS ARR.</span></span>
    
    <span data-ttu-id="fc943-193">默认情况下，目标 HTTP 端口必须定义为8080。</span><span class="sxs-lookup"><span data-stu-id="fc943-193">By default, the destination HTTP port must be defined as 8080.</span></span> <span data-ttu-id="fc943-194">单击当前 **httpsport 80** 的 "下一步" 并将值设置为 **8080**。</span><span class="sxs-lookup"><span data-stu-id="fc943-194">Click next to the current **httpPort 80** and set the value to **8080**.</span></span> <span data-ttu-id="fc943-195">单击当前 **httpsPort 443** 的 "下一步" 并将值设置为 **4443**。</span><span class="sxs-lookup"><span data-stu-id="fc943-195">Click next to the current **httpsPort 443** and set the value to **4443**.</span></span> <span data-ttu-id="fc943-196">在100中保留 **体重** 参数。</span><span class="sxs-lookup"><span data-stu-id="fc943-196">Leave the **weight** parameter at 100.</span></span> <span data-ttu-id="fc943-197">如果需要，您可以在有基线统计信息后重新定义给定规则的权重。</span><span class="sxs-lookup"><span data-stu-id="fc943-197">If needed, you can redefine weights for a given rule once you have baseline statistics.</span></span> <span data-ttu-id="fc943-198">单击 " **完成** " 以完成规则配置的这一部分。</span><span class="sxs-lookup"><span data-stu-id="fc943-198">Click **Finish** to complete this part of the rule configuration.</span></span>

8.  <span data-ttu-id="fc943-199">你可能会看到一个对话框重写规则，通知你 IIS 管理器可以创建 URL 重写规则，以便自动将所有传入请求路由到服务器场。</span><span class="sxs-lookup"><span data-stu-id="fc943-199">You may see a dialog Rewrite Rules that informs you that IIS Manager can create a URL rewrite rule to route all incoming requests to the server farm automatically.</span></span> <span data-ttu-id="fc943-200">单击“**是**”。</span><span class="sxs-lookup"><span data-stu-id="fc943-200">Click **Yes**.</span></span> <span data-ttu-id="fc943-201">您将手动调整规则，但选择 "是" 设置初始配置。。</span><span class="sxs-lookup"><span data-stu-id="fc943-201">You will adjust the rules manually, but selecting Yes sets the initial configuration..</span></span>

9.  <span data-ttu-id="fc943-202">单击刚刚创建的服务器场的名称。</span><span class="sxs-lookup"><span data-stu-id="fc943-202">Click the name of the server farm that you have just created.</span></span> <span data-ttu-id="fc943-203">在 IIS 管理器的 "功能" 视图中的 " **服务器场** " 下，双击 " **缓存**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-203">Under **Server Farm** in IIS Manager Features View, you double-click **Caching**.</span></span> <span data-ttu-id="fc943-204">取消选择 " **启用磁盘缓存**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-204">Deselect **Enable disk cache**.</span></span> <span data-ttu-id="fc943-205">单击右侧的 " **应用** "。</span><span class="sxs-lookup"><span data-stu-id="fc943-205">Click **Apply** on the right-hand side.</span></span>

10. <span data-ttu-id="fc943-206">单击服务器场的名称。</span><span class="sxs-lookup"><span data-stu-id="fc943-206">Click the name of the server farm.</span></span> <span data-ttu-id="fc943-207">在 IIS 管理器的 "功能" 视图中的 " **服务器场** " 下，双击 " **代理**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-207">Under **Server Farm** in IIS Manager Features View, you double-click **Proxy**.</span></span> <span data-ttu-id="fc943-208">在 "代理设置" 页面上，将 **超时 (秒** 的值更改为适合你的部署的值) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-208">On the Proxy settings page change the value for **Time-out (seconds)** to a value appropriate for your deployment.</span></span> <span data-ttu-id="fc943-209">单击 " **应用** " 以保存更改。</span><span class="sxs-lookup"><span data-stu-id="fc943-209">Click **Apply** to save the change.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fc943-210">代理超时值是一个数字，该数字将因部署而异。</span><span class="sxs-lookup"><span data-stu-id="fc943-210">The Proxy Time-out value is a number that will vary from deployment to deployment.</span></span> <span data-ttu-id="fc943-211">应监视你的部署并修改客户端最佳体验的值。</span><span class="sxs-lookup"><span data-stu-id="fc943-211">You should monitor your deployment and modify the value for the best experience for clients.</span></span> <span data-ttu-id="fc943-212">你可以将值设置为低至200。</span><span class="sxs-lookup"><span data-stu-id="fc943-212">You may be able to set the value as low as 200.</span></span> <span data-ttu-id="fc943-213">如果你在你的环境中支持 Lync 移动客户端，则应将此值设置为960以允许来自 Office 365 的推送通知超时，其超时值为900。</span><span class="sxs-lookup"><span data-stu-id="fc943-213">If you are supporting Lync mobile clients in your environment, you should set the value to 960 to allow for push notifications timeout from Office 365 which have a time-out value of 900.</span></span> <span data-ttu-id="fc943-214">很有可能需要增加超时值以避免客户端在值太低时断开连接，或在客户端断开连接后，如果通过代理连接没有断开和清除该号码，则不会减少客户端连接的数量。</span><span class="sxs-lookup"><span data-stu-id="fc943-214">It is very likely that you will need to increase the time-out value to avoid client disconnects when the value is too low or decrease the number if connections through the proxy do not disconnect and clear long after the client has disconnected.</span></span> <span data-ttu-id="fc943-215">监视和基本排列环境的正常情况是确定正确设置对于此值的位置的唯一准确方式。</span><span class="sxs-lookup"><span data-stu-id="fc943-215">Monitoring and base-lining what is normal for your environment is the only accurate means to determine where the right setting is for this value.</span></span>

    
    </div>

11. <span data-ttu-id="fc943-216">单击服务器场的名称。</span><span class="sxs-lookup"><span data-stu-id="fc943-216">Click the name of the server farm.</span></span> <span data-ttu-id="fc943-217">在 IIS 管理器的 "功能" 视图中的 " **服务器场** " 下，双击 " **路由规则**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-217">Under **Server Farm** in IIS Manager Features View, you double-click **Routing Rules**.</span></span> <span data-ttu-id="fc943-218">在 "路由" 下的 "路由规则" 对话框中，清除 "启用 SSL 卸载" 旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="fc943-218">On the Routing Rules dialog under Routing, clear the checkbox next to Enable SSL offloading.</span></span> <span data-ttu-id="fc943-219">如果清除复选框的功能不可用，请选中 " **使用 URL 重写" 复选框以检查传入的请求**。</span><span class="sxs-lookup"><span data-stu-id="fc943-219">If the ability to clear the checkbox is not available, select the checkbox for **Use URL Rewrite to inspect incoming requests**.</span></span> <span data-ttu-id="fc943-220">单击 " **应用** " 以保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="fc943-220">Click **Apply** to save your changes.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="fc943-221">不支持反向代理的 SSL 卸载。</span><span class="sxs-lookup"><span data-stu-id="fc943-221">SSL Offloading by the reverse proxy is not supported.</span></span>

    
    </div>

12. <span data-ttu-id="fc943-222">对每个必须通过反向代理传递的 URL 重复步骤5-11。</span><span class="sxs-lookup"><span data-stu-id="fc943-222">Repeat Steps 5-11 for each URL that must pass through the reverse proxy.</span></span> <span data-ttu-id="fc943-223">常见列表如下所示：</span><span class="sxs-lookup"><span data-stu-id="fc943-223">A common list would be the following:</span></span>
    
      - <span data-ttu-id="fc943-224">前端服务器 Web 服务外部： webext.contoso.com (已通过初始浏览) 进行配置</span><span class="sxs-lookup"><span data-stu-id="fc943-224">Front End Server Web services external: webext.contoso.com (already configured by initial walk through)</span></span>
    
      - <span data-ttu-id="fc943-225">董事的外部 Web 服务主管： webdirext.contoso.com 在部署 Director 时 (可选的) </span><span class="sxs-lookup"><span data-stu-id="fc943-225">Director Web services external for Director: webdirext.contoso.com (Optional if a Director is deployed)</span></span>
    
      - <span data-ttu-id="fc943-226">简单的 URL 开会： meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fc943-226">Simple URL meet: meet.contoso.com</span></span>
    
      - <span data-ttu-id="fc943-227">简单 URL 拨入： dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fc943-227">Simple URL dialin: dialin.contoso.com</span></span>
    
      - <span data-ttu-id="fc943-228">Lync 自动发现 URL： lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fc943-228">Lync Autodiscover URL: lyncdiscover.contoso.com</span></span>
    
      - <span data-ttu-id="fc943-229">Office Web Apps 服务器 URL： officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fc943-229">Office Web Apps Server URL: officewebapps01.contoso.com</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="fc943-230">Office Web Apps 服务器的 URL 将使用不同的 httpsPort 地址。</span><span class="sxs-lookup"><span data-stu-id="fc943-230">The URL for the Office Web Apps Server will use a different httpsPort address.</span></span> <span data-ttu-id="fc943-231">在步骤7中，将 <STRONG>httpsPort</STRONG> 定义为 <STRONG>443</STRONG> ，将 <STRONG>httpsport</STRONG> 定义为端口 <STRONG>80</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="fc943-231">In step 7, you define the <STRONG>httpsPort</STRONG> as <STRONG>443</STRONG> and the <STRONG>httpPort</STRONG> as port <STRONG>80</STRONG>.</span></span> <span data-ttu-id="fc943-232">所有其他配置设置相同。</span><span class="sxs-lookup"><span data-stu-id="fc943-232">All other configuration settings are the same.</span></span>

        
        </div>

13. <span data-ttu-id="fc943-233">在控制台的左侧，单击 IIS 服务器名称。</span><span class="sxs-lookup"><span data-stu-id="fc943-233">On the left-hand side of the console, click the IIS server name.</span></span> <span data-ttu-id="fc943-234">在控制台的中间，找到 " **IIS**" 下的 **URL 重写**。</span><span class="sxs-lookup"><span data-stu-id="fc943-234">In the middle of the console, locate **URL Rewrite** under **IIS**.</span></span> <span data-ttu-id="fc943-235">双击 "URL 重写" 以打开 URL 重写规则配置。</span><span class="sxs-lookup"><span data-stu-id="fc943-235">Double-click URL Rewrite to open the URL Rewrite rules configuration.</span></span> <span data-ttu-id="fc943-236">你应该看到在前面的步骤中创建的每个服务器场的规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-236">You should see rules for each Server Farm that you created in the previous steps.</span></span> <span data-ttu-id="fc943-237">如果未执行此操作，请确认单击了 "Internet 信息服务器管理器" 控制台中 "**起始页**" 节点下方的 **IIS 服务器** 名称。</span><span class="sxs-lookup"><span data-stu-id="fc943-237">If you do not, confirm that you clicked on the **IIS Server** name immediately below the **Start Page** node in the Internet Information Server Manager console.</span></span>

14. <span data-ttu-id="fc943-238">在 " **URL 重写** " 对话框中，使用 webext.contoso.com 作为示例，显示的规则的完整名称为 **ARR \_ webext.contoso.com \_ loadbalance \_ SSL**。</span><span class="sxs-lookup"><span data-stu-id="fc943-238">In the **URL Rewrite** dialog, using webext.contoso.com as an example, the full name of the rule as displayed is **ARR\_webext.contoso.com\_loadbalance\_SSL**.</span></span>
    
      - <span data-ttu-id="fc943-239">双击规则以打开 " **编辑入站规则** " 对话框。</span><span class="sxs-lookup"><span data-stu-id="fc943-239">Double-click the rule to open the **Edit Inbound Rule** dialog.</span></span>
    
      - <span data-ttu-id="fc943-240">单击 "**添加 ...** "</span><span class="sxs-lookup"><span data-stu-id="fc943-240">Click **Add…**</span></span> <span data-ttu-id="fc943-241">在 " **条件** " 对话框中。</span><span class="sxs-lookup"><span data-stu-id="fc943-241">on the **Conditions** dialog.</span></span>
    
      - <span data-ttu-id="fc943-242">在 "**条件输入：** 类型 **{HTTP \_ HOST}**" 中的 "**添加条件**" 中。</span><span class="sxs-lookup"><span data-stu-id="fc943-242">On the **Add Condition** in **Condition input:** type **{HTTP\_HOST}**.</span></span> <span data-ttu-id="fc943-243">在你键入时 (，将显示一个对话框，可让你选择条件) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-243">(As you type, a dialog appears that will let you select the condition).</span></span> <span data-ttu-id="fc943-244">在 " **检查输入字符串：** " 下 **，选择 "匹配模式"**。</span><span class="sxs-lookup"><span data-stu-id="fc943-244">under **Check if input string:** select **Matches the Pattern**.</span></span> <span data-ttu-id="fc943-245">在 **模式输入** 类型中，应选择 " **\* *_. _* 忽略大小写**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-245">In the **Pattern input** type **\**_. _\* Ignore case*\* should be selected.</span></span> <span data-ttu-id="fc943-246">单击“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="fc943-246">Click **OK**.</span></span>
    
      - <span data-ttu-id="fc943-247">在 " **编辑入站规则** " 对话框中向下滚动，找到 " **操作** " 对话框。</span><span class="sxs-lookup"><span data-stu-id="fc943-247">Scroll down in the **Edit Inbound Rule** dialog to locate the **Action** dialog.</span></span> <span data-ttu-id="fc943-248">**操作类型：** 应设置为 **路由到服务器场**， **方案：** 设置为 **https://**， **服务器场：** 设置为应用此规则的 URL。</span><span class="sxs-lookup"><span data-stu-id="fc943-248">**Action Type:** should be set to **Route to Server Farm**, **Scheme:** set to **https://**, **Server farm:** set to the URL that this rule applies to.</span></span> <span data-ttu-id="fc943-249">在此示例中，此示例应设置为 **webext.contoso.com**。</span><span class="sxs-lookup"><span data-stu-id="fc943-249">For this example, this should be set to **webext.contoso.com**.</span></span> <span data-ttu-id="fc943-250">**路径：** 设置为 **/{R： 0}**</span><span class="sxs-lookup"><span data-stu-id="fc943-250">**Path:** is set to **/{R:0}**</span></span>
    
      - <span data-ttu-id="fc943-251">单击 " **应用** " 以保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="fc943-251">Click **Apply** to save your changes.</span></span> <span data-ttu-id="fc943-252">单击 " **返回到规则** " 以返回到 URL 重写规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-252">Click **Back to Rules** to return to the URL Rewrite rules.</span></span>

15. <span data-ttu-id="fc943-253">对已定义的每个 SSL 重写规则（每个服务器场 URL）重复步骤14中定义的过程。</span><span class="sxs-lookup"><span data-stu-id="fc943-253">Repeat the procedure defined in Step 14 for each of the SSL rewrite rules that you have defined, one per Server Farm URL.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="fc943-254">默认情况下，也会创建 HTTP 规则，并使用与 SSL 规则类似的命名表示。</span><span class="sxs-lookup"><span data-stu-id="fc943-254">By default, HTTP rules are created as well and are denoted by the similar naming to the SSL rules.</span></span> <span data-ttu-id="fc943-255">对于我们的当前示例，HTTP 规则将被命名为 <STRONG>ARR_webext _loadbalance</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="fc943-255">For our current example, the HTTP rule would be named <STRONG>ARR_webext.contoso.com_loadbalance</STRONG>.</span></span> <span data-ttu-id="fc943-256">这些规则不需要修改，可以安全地忽略它们。</span><span class="sxs-lookup"><span data-stu-id="fc943-256">No modifications are needed to these rules and they can be safely ignored.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-the-properties-of-the-web-publishing-rule-in-tmg-2010"></a><span data-ttu-id="fc943-257">修改 TMG 2010 中的 web 发布规则的属性</span><span class="sxs-lookup"><span data-stu-id="fc943-257">To modify the properties of the web publishing rule in TMG 2010</span></span>

1.  <span data-ttu-id="fc943-258">单击 " **开始**"，指向 " **程序**"，选择 " **Microsoft Forefront tmg**"，然后单击 " **Forefront tmg 管理**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-258">Click **Start**, point to **Programs**, select **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="fc943-259">在左窗格中，展开 " **服务器名**"，然后单击 " **防火墙策略**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-259">In the left pane, expand **ServerName**, and then click **Firewall Policy**.</span></span>

3.  <span data-ttu-id="fc943-260">在 "详细信息" 窗格中，右键单击您在上一过程中创建的 web 服务器发布规则 (例如，LyncServerExternalRule) "，然后单击" **属性**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-260">In the details pane, right-click the web server publishing rule that you created in the previous procedure (for example, LyncServerExternalRule), and then click **Properties**.</span></span>

4.  <span data-ttu-id="fc943-261">在 " **属性** " 页上的 " **从** " 选项卡上，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="fc943-261">On the **Properties** page, on the **From** tab, do the following:</span></span>
    
      - <span data-ttu-id="fc943-262">在 " **此规则适用于来自这些源的流量** " 列表中，单击 " **任意位置**"，然后单击 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-262">In the **This rule applies to traffic from these sources** list, click **Anywhere**, and then click **Remove**.</span></span>
    
      - <span data-ttu-id="fc943-263">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fc943-263">Click **Add**.</span></span>
    
      - <span data-ttu-id="fc943-264">在 " **添加网络实体**" 中展开 " **网络**"，单击 " **外部**"，单击 " **添加**"，然后单击 " **关闭**"。</span><span class="sxs-lookup"><span data-stu-id="fc943-264">In **Add Network Entities**, expand **Networks**, click **External**, click **Add**, and then click **Close**.</span></span>

5.  <span data-ttu-id="fc943-265">在 " **收件人** " 选项卡上，确保已选中 " **转发原始主机标头，而不是实际的主机头** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="fc943-265">On the **To** tab, ensure that the **Forward the original host header instead of the actual one** check box is selected.</span></span>

6.  <span data-ttu-id="fc943-266">在 " **桥接** " 选项卡上，选中 "将 **请求重定向到 SSL 端口** " 复选框，然后指定端口 **4443**。</span><span class="sxs-lookup"><span data-stu-id="fc943-266">On the **Bridging** tab, select the **Redirect request to SSL port** check box, and then specify port **4443**.</span></span>

7.  <span data-ttu-id="fc943-267">在 " **公共名称** " 选项卡上，添加简单的 url (例如，meet.contoso.com 和 dialin.contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="fc943-267">On the **Public Name** tab, add the simple URLs (for example, meet.contoso.com and dialin.contoso.com).</span></span>

8.  <span data-ttu-id="fc943-268">单击 " **应用** " 以保存更改，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="fc943-268">Click **Apply** to save changes, and then click **OK**.</span></span>

9.  <span data-ttu-id="fc943-269">单击 "详细信息" 窗格中的 " **应用** " 以保存更改并更新配置。</span><span class="sxs-lookup"><span data-stu-id="fc943-269">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

</div>

<div>

## <a name="to-modify-the-properties-of-the-web-publishing-rule-in-iis-arr"></a><span data-ttu-id="fc943-270">在 IIS ARR 中修改 web 发布规则的属性</span><span class="sxs-lookup"><span data-stu-id="fc943-270">To modify the properties of the web publishing rule in IIS ARR</span></span>

1.  <span data-ttu-id="fc943-271">单击 " **开始**"，选择 " **程序**"，选择 " **管理工具**"，然后单击 " **Internet 信息服务" (IIS) 管理器**。</span><span class="sxs-lookup"><span data-stu-id="fc943-271">Click **Start**, select **Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>

2.  <span data-ttu-id="fc943-272">在控制台的左侧，单击 IIS 服务器名称。</span><span class="sxs-lookup"><span data-stu-id="fc943-272">On the left-hand side of the console, click the IIS server name.</span></span>

3.  <span data-ttu-id="fc943-273">在控制台的中间，找到 " **IIS**" 下的 **URL 重写**。</span><span class="sxs-lookup"><span data-stu-id="fc943-273">In the middle of the console, locate **URL Rewrite** under **IIS**.</span></span> <span data-ttu-id="fc943-274">双击 "URL 重写" 以打开 URL 重写规则配置。</span><span class="sxs-lookup"><span data-stu-id="fc943-274">Double-click URL Rewrite to open the URL Rewrite rules configuration.</span></span>

4.  <span data-ttu-id="fc943-275">双击需要修改的规则。</span><span class="sxs-lookup"><span data-stu-id="fc943-275">Double-click the rule that you need to modify.</span></span> <span data-ttu-id="fc943-276">根据需要进行修改， **匹配 URL**、 **条件**、 **服务器变量** 或 **操作**。</span><span class="sxs-lookup"><span data-stu-id="fc943-276">Make your modifications, as needed, in **Match URL**, **Conditions**, **Server Variables** or **Action**.</span></span>

5.  <span data-ttu-id="fc943-277">单击 " **应用** " 以提交所做的更改。</span><span class="sxs-lookup"><span data-stu-id="fc943-277">Click **Apply** to commit your changes.</span></span> <span data-ttu-id="fc943-278">单击 " **返回规则** " 以修改其他规则，或关闭 **IIS 管理器** 控制台（如果你已完成更改）。</span><span class="sxs-lookup"><span data-stu-id="fc943-278">Click **Back to Rules** to modify other rules, or close the **IIS Manager** console if you are done with your changes.</span></span>

<span data-ttu-id="fc943-279"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc943-279"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

