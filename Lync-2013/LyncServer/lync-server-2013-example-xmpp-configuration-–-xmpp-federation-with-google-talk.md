---
title: 示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟
description: 示例 XMPP 配置-XMPP 联盟与 Google 通话。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428447"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a><span data-ttu-id="3f46a-103">Lync Server 2013 中的示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="3f46a-103">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f46a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f46a-104">

<span> </span></span></span>

<span data-ttu-id="3f46a-105">_**主题上次修改时间：** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="3f46a-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="3f46a-106">部署 XMPP 代理的示例配置定义了与 Google 通话的联盟。</span><span class="sxs-lookup"><span data-stu-id="3f46a-106">An example configuration for deploying the XMPP Proxy defines a federation with Google Talk.</span></span>

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a><span data-ttu-id="3f46a-107">示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟</span><span class="sxs-lookup"><span data-stu-id="3f46a-107">Example XMPP configuration – XMPP federation with Google Talk</span></span>

1.  <span data-ttu-id="3f46a-108">在前端服务器上，打开 "Lync Server 部署向导"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-108">On the Front End Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="3f46a-109">单击 " **安装** 或 **更新 lync 服务器系统**"，然后单击 " **设置** " 或 " **删除 lync server 组件**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-109">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="3f46a-110">再次单击 " **运行**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-110">Click **Run Again**.</span></span>

2.  <span data-ttu-id="3f46a-111">在 " **安装 Lync 服务器组件**" 中，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-111">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="3f46a-112">"摘要" 屏幕将显示执行时的操作。</span><span class="sxs-lookup"><span data-stu-id="3f46a-112">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="3f46a-113">部署完成后，单击 " **查看日志** " 以查看可用的日志文件。</span><span class="sxs-lookup"><span data-stu-id="3f46a-113">After the deployment is complete, click **View Log** to view available log files.</span></span> <span data-ttu-id="3f46a-114">单击 " **完成** " 以完成部署。</span><span class="sxs-lookup"><span data-stu-id="3f46a-114">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="3f46a-115">在边缘服务器上，打开 "Lync Server 部署向导"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-115">On the Edge Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="3f46a-116">单击 " **安装** 或 **更新 lync 服务器系统**"，然后单击 " **设置** " 或 " **删除 lync server 组件**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-116">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="3f46a-117">再次单击 " **运行**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-117">Click **Run Again**.</span></span>

4.  <span data-ttu-id="3f46a-118">将 Google 通话添加为 XMPP 允许合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="3f46a-118">Add Google Talk as an XMPP allowed partner.</span></span> <span data-ttu-id="3f46a-119">Google 谈话目前仅支持服务器到服务器 XMPP 联合身份验证的 TCP 连接，并且仅支持服务器回拨以进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="3f46a-119">Google Talk currently only supports unencrypted, TCP connections for server-to-server XMPP federation and only supports Server Dialback for identity verification.</span></span> <span data-ttu-id="3f46a-120"> (参阅 <http://xmpp.org/extensions/xep-0220.html>) 。</span><span class="sxs-lookup"><span data-stu-id="3f46a-120">(See <http://xmpp.org/extensions/xep-0220.html>).</span></span>
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  <span data-ttu-id="3f46a-121">若要启用边缘联盟，请键入以下内容：</span><span class="sxs-lookup"><span data-stu-id="3f46a-121">To enable Edge Federation, type the following:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  <span data-ttu-id="3f46a-122">在 " **安装 Lync 服务器组件**" 中，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-122">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="3f46a-123">"摘要" 屏幕将显示执行时的操作。</span><span class="sxs-lookup"><span data-stu-id="3f46a-123">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="3f46a-124">部署完成后，单击 " **查看日志** " 以查看可用的日志文件。</span><span class="sxs-lookup"><span data-stu-id="3f46a-124">After the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="3f46a-125">单击 " **完成** " 以完成部署。</span><span class="sxs-lookup"><span data-stu-id="3f46a-125">Click **Finish** to complete the deployment.</span></span>

7.  <span data-ttu-id="3f46a-126">在边缘服务器上的 "Lync Server 部署向导" 中，在 " **步骤3：请求、安装或分配证书**" 旁边，再次单击 " **运行**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-126">On the Edge Server, in the Lync Server Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="3f46a-127">如果你是首次部署 Edge 服务器，你将看到 "运行"，而不是再次运行。</span><span class="sxs-lookup"><span data-stu-id="3f46a-127">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

8.  <span data-ttu-id="3f46a-128">在“**可用的证书任务**”页上，单击“**创建新的证书请求**”。</span><span class="sxs-lookup"><span data-stu-id="3f46a-128">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

9.  <span data-ttu-id="3f46a-129">在 " **证书请求** " 页面上，单击 " **外部边缘证书**"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-129">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

10. <span data-ttu-id="3f46a-130">在 " **延迟或立即请求** " 页面上，选中 " **立即准备请求，但稍后发送"** 复选框。</span><span class="sxs-lookup"><span data-stu-id="3f46a-130">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

11. <span data-ttu-id="3f46a-131">在 " **证书请求文件** " 页面上，键入请求要保存到的文件的完整路径和文件名 (例如，c： \\ cert \_ 外部 \_ edge) 。</span><span class="sxs-lookup"><span data-stu-id="3f46a-131">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

12. <span data-ttu-id="3f46a-132">在 " **指定备用证书模板** " 页面上，若要使用默认 web 台模板之外的模板，请选中 " **为所选证书颁发机构使用备用证书模板** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="3f46a-132">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

13. <span data-ttu-id="3f46a-133">在 " **名称和安全设置** " 页面上，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="3f46a-133">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="3f46a-134">在 " **友好名称**" 中，键入证书的显示名称</span><span class="sxs-lookup"><span data-stu-id="3f46a-134">In **Friendly name**, type a display name for the certificate</span></span>
    
    2.  <span data-ttu-id="3f46a-135">在 " **位长度**" 中，指定位长度 (通常是 **2048** 的默认值) </span><span class="sxs-lookup"><span data-stu-id="3f46a-135">In **Bit length**, specify the bit length (typically, the default of **2048**)</span></span>
    
    3.  <span data-ttu-id="3f46a-136">验证已选中 "将 **证书私钥标记为可导出** " 复选框</span><span class="sxs-lookup"><span data-stu-id="3f46a-136">Verify that the **Mark certificate private key as exportable** check box is selected</span></span>

14. <span data-ttu-id="3f46a-137">在 " **组织信息** " 页面上，键入组织和组织单位的名称 (例如，部门或部门) </span><span class="sxs-lookup"><span data-stu-id="3f46a-137">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department)</span></span>

15. <span data-ttu-id="3f46a-138">在 " **地理信息** " 页面上，指定位置信息</span><span class="sxs-lookup"><span data-stu-id="3f46a-138">On the **Geographical Information** page, specify the location information</span></span>

16. <span data-ttu-id="3f46a-139">在 " **主题名称/主题备用名称** " 页面上，将显示要由向导自动填充的信息。</span><span class="sxs-lookup"><span data-stu-id="3f46a-139">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="3f46a-140">如果需要其他主题备用名称，请在接下来的两个步骤中进行指定</span><span class="sxs-lookup"><span data-stu-id="3f46a-140">If additional subject alternative names are needed, you specify them in the next two steps</span></span>

17. <span data-ttu-id="3f46a-141">在 " **使用者备用名称 (SANs)** " 页面上的 "SIP 域设置" 中，选中 "域" 复选框以添加 SIP。</span><span class="sxs-lookup"><span data-stu-id="3f46a-141">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.</span></span> <span data-ttu-id="3f46a-142">\<sipdomain\> 输入到 "主题备用名称" 列表。</span><span class="sxs-lookup"><span data-stu-id="3f46a-142">\<sipdomain\> entry to the subject alternative names list.</span></span>

18. <span data-ttu-id="3f46a-143">在 " **配置其他主题备用名称** " 页面上，指定所需的任何其他主题备用名称。</span><span class="sxs-lookup"><span data-stu-id="3f46a-143">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="3f46a-144">如果 XMPP 代理已安装，则默认情况下会在 SAN 条目中填充域名 (如 contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="3f46a-144">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="3f46a-145">如果需要更多条目，请在此步骤中添加这些条目。</span><span class="sxs-lookup"><span data-stu-id="3f46a-145">If you require more entries, add them in this step.</span></span>

    
    </div>

19. <span data-ttu-id="3f46a-146">在 " **请求摘要** " 页面上，查看要用于生成请求的证书信息。</span><span class="sxs-lookup"><span data-stu-id="3f46a-146">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

20. <span data-ttu-id="3f46a-147">命令完成运行后，您可以 **查看日志**，或单击 " **下一步** " 继续。</span><span class="sxs-lookup"><span data-stu-id="3f46a-147">After the commands finish running, you can **View Log**, or click **Next** to continue.</span></span>

21. <span data-ttu-id="3f46a-148">在 "**证书请求文件**" 页面上，您可以通过单击 "查看或退出证书向导"，**通过单击 "\*\*\*\*查看**" 或 "退出证书向导" 来查看生成的证书签名请求 (CSR) 文件</span><span class="sxs-lookup"><span data-stu-id="3f46a-148">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

22. <span data-ttu-id="3f46a-149">将请求文件复制并提交到公共证书颁发机构。</span><span class="sxs-lookup"><span data-stu-id="3f46a-149">Copy the request file and submit to your public certification authority.</span></span>

23. <span data-ttu-id="3f46a-150">接收、导入和分配公共证书后，必须停止并重新启动 Edge 服务器服务。</span><span class="sxs-lookup"><span data-stu-id="3f46a-150">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="3f46a-151">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft lync server 2013**"，然后单击 " **Lync server 命令行管理** 程序"。</span><span class="sxs-lookup"><span data-stu-id="3f46a-151">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**..</span></span> <span data-ttu-id="3f46a-152">在 Lync Server 命令行管理器中，键入：</span><span class="sxs-lookup"><span data-stu-id="3f46a-152">In the Lync Server Management Shell, type:</span></span>
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. <span data-ttu-id="3f46a-153">若要为 XMPP 联盟配置 DNS，请将以下 SRV 记录添加到外部 DNS： \_ XMPP-server。 \_tcp-out.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="3f46a-153">To configure DNS for XMPP federation, you add the following SRV record to external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="3f46a-154">SRV 记录将解析为 Edge 服务器的访问边缘 FQDN，其端口值为5269</span><span class="sxs-lookup"><span data-stu-id="3f46a-154">The SRV record will resolve to the access edge FQDN of the Edge server, with a port value of 5269</span></span>

25. <span data-ttu-id="3f46a-155">通过在前端服务器上打开 Lync Server 管理外壳并键入以下内容来配置新的外部访问策略以启用所有用户：</span><span class="sxs-lookup"><span data-stu-id="3f46a-155">Configure a new External Access Policy to enable all users by opening the Lync Server Management Shell on a Front End Server and typing:</span></span>
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

<span data-ttu-id="3f46a-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f46a-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

