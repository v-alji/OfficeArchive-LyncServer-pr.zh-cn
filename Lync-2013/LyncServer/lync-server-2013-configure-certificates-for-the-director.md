---
title: Lync Server 2013：为控制器配置证书
description: Lync Server 2013：配置 Director 的证书。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure certificates for the Director
ms:assetid: 22988186-15ae-43b1-92f4-0adb3b75a7fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398296(v=OCS.15)
ms:contentKeyID: 48183612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cadc3f51b036120e21c3f1e6201f872aacafef69
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434009"
---
# <a name="configure-certificates-for-the-director-in-lync-server-2013"></a><span data-ttu-id="325a2-103">在 Lync Server 2013 中为控制器配置证书</span><span class="sxs-lookup"><span data-stu-id="325a2-103">Configure certificates for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="325a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="325a2-104">

<span> </span></span></span>

<span data-ttu-id="325a2-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="325a2-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="325a2-106">当你运行证书向导时，请确保你使用的帐户是已为你将使用的证书模板类型分配了相应权限的组的成员。</span><span class="sxs-lookup"><span data-stu-id="325a2-106">When you run the Certificate Wizard, ensure that you are logged in using an account that is a member of a group that has been assigned the appropriate permissions for the type of certificate template you will use.</span></span> <span data-ttu-id="325a2-107">默认情况下，Lync Server 2013 证书请求将使用 Web 服务器证书模板。</span><span class="sxs-lookup"><span data-stu-id="325a2-107">By default, a Lync Server 2013 certificate request will use the Web Server certificate template.</span></span> <span data-ttu-id="325a2-108">如果您使用的帐户是 RTCUniversalServerAdmins 组的成员以使用此模板申请证书，请验证该组是否已分配使用该模板所需的注册权限。</span><span class="sxs-lookup"><span data-stu-id="325a2-108">If you use an account that is a member of the RTCUniversalServerAdmins group to request a certificate using this template, verify that the group has been assigned the Enroll permissions required to use that template.</span></span>



</div>

<span data-ttu-id="325a2-109">每个控制器都需要默认证书、web 内部证书和 web 外部证书。</span><span class="sxs-lookup"><span data-stu-id="325a2-109">Each Director requires a default certificate, a web internal certificate, and a web external certificate.</span></span> <span data-ttu-id="325a2-110">有关控制器的证书要求的详细信息，请参阅规划文档中 [Lync Server 2013 内部服务器的证书要求](lync-server-2013-certificate-requirements-for-internal-servers.md) 。</span><span class="sxs-lookup"><span data-stu-id="325a2-110">For details about the certificate requirements for Directors, see [Certificate requirements for internal servers in Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) in the Planning documentation.</span></span>

<span data-ttu-id="325a2-111">使用以下过程配置控制器证书。</span><span class="sxs-lookup"><span data-stu-id="325a2-111">Use the following procedure to configure Director certificates.</span></span> <span data-ttu-id="325a2-112">对每个导演重复该过程。</span><span class="sxs-lookup"><span data-stu-id="325a2-112">Repeat the procedure for each Director.</span></span> <span data-ttu-id="325a2-113">此过程的步骤介绍了如何从由组织部署的内部企业根证书颁发机构 (CA 以及脱机请求处理) 配置证书。</span><span class="sxs-lookup"><span data-stu-id="325a2-113">The steps of this procedure describe how to configure a certificate from an Internal Enterprise Root certification authority (CA) deployed by your organization and with offline request processing.</span></span> <span data-ttu-id="325a2-114">有关从外部 CA 获取证书的详细信息，请与您的支持团队联系。</span><span class="sxs-lookup"><span data-stu-id="325a2-114">For details about obtaining certificates from an external CA, contact your support team.</span></span>

<div>

## <a name="to-configure-certificates-for-the-director-or-director-pool"></a><span data-ttu-id="325a2-115">为 Director 或控制器池配置证书</span><span class="sxs-lookup"><span data-stu-id="325a2-115">To configure certificates for the Director or Director pool</span></span>

1.  <span data-ttu-id="325a2-116">在 Lync Server 部署向导的 " **步骤3：请求、安装或分配证书**" 旁边，单击 " **运行**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-116">In the Lync Server Deployment Wizard, next to **Step 3: Request, Install or Assign Certificates**, click **Run**.</span></span>

2.  <span data-ttu-id="325a2-117">在“**证书向导**”页上，单击“**请求**”。</span><span class="sxs-lookup"><span data-stu-id="325a2-117">On the **Certificate Wizard** page, click **Request**.</span></span>

3.  <span data-ttu-id="325a2-118">在 " **证书请求** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-118">On the **Certificate Request** page, click **Next**.</span></span>

4.  <span data-ttu-id="325a2-119">在 " **延迟或立即请求** " 页面上，接受默认将 **请求立即发送到联机证书颁发机构** 选项，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-119">On the **Delayed or Immediate Requests** page, accept the default **Send the request immediately to an online certification authority** option, and then click **Next**.</span></span>

5.  <span data-ttu-id="325a2-120">在 " **选择证书颁发机构 (CA)** " 页面上，单击要使用的内部 Windows 证书颁发机构，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-120">On the **Choose a Certification Authority (CA)** page, click the internal Windows certification authority that you want to use, and then click **Next**.</span></span>

6.  <span data-ttu-id="325a2-121">在 " **证书颁发机构帐户** " 页面上，指定要使用的备用凭据（如果您登录的帐户没有足够的权限申请证书），然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-121">On the **Certification Authority Account** page, specify alternate credentials to be used if the account you are logged on with does not have sufficient authority to request the certificate, and then click **Next**.</span></span>

7.  <span data-ttu-id="325a2-122">在 " **指定备用证书模板** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-122">On the **Specify Alternate Certificate Template** page, click **Next**.</span></span>

8.  <span data-ttu-id="325a2-123">在 " **名称和安全设置** " 页面上，您可以指定一个 **友好名称**，接受2048位密钥长度，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-123">On the **Name and Security Settings** page, you can specify a **Friendly Name**, accept the 2048-bit key length, and then click **Next**.</span></span>

9.  <span data-ttu-id="325a2-124">在 " **组织信息** " 页面上，选择 "指定组织信息"，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-124">On the **Organization Information** page, optionally specify organization information, and then click **Next**.</span></span>

10. <span data-ttu-id="325a2-125">在 " **地理信息** " 页面上，选择 "指定地理信息"，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-125">On the **Geographical Information** page, optionally specify geographical information, and then click **Next**.</span></span>

11. <span data-ttu-id="325a2-126">在 " **主题名称/主题备用名称** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-126">On the **Subject Name / Subject Alternative Names** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="325a2-127">"主题备用名称" 列表应包含要在其上安装 Director 的计算机的名称 (如果单个控制器) 或控制器池名称以及为组织配置的简单 URL 名称。</span><span class="sxs-lookup"><span data-stu-id="325a2-127">The subject alternative name list should contain the name of the computer on which you are installing the Director (if a single Director) or the Director pool name, and the simple URL names configured for the organization.</span></span>

    
    </div>

12. <span data-ttu-id="325a2-128">在 " **(SANs) 的主题备用名称上的 SIP 域设置** " 页面上，为希望 Director 控制其处理的所有域选择 **已配置的 SIP 域** ，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-128">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the **Configured SIP Domains** for all domains that you want the Director to handle, and then click **Next**.</span></span>

13. <span data-ttu-id="325a2-129">在 " **配置其他主题备用名称** " 页面上，添加任何其他所需的主题备用名称，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-129">On the **Configure Additional Subject Alternative Names** page, add any additional required subject alternative names, and then click **Next**.</span></span>

14. <span data-ttu-id="325a2-130">在 " **证书申请摘要** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-130">On the **Certificate Request Summary** page, click **Next**.</span></span>

15. <span data-ttu-id="325a2-131">在 " **执行命令** " 页面上，在命令完成运行后单击 " **下一步** "。</span><span class="sxs-lookup"><span data-stu-id="325a2-131">On the **Executing Commands** page, click **Next** after the commands have finished running.</span></span>

16. <span data-ttu-id="325a2-132">在 " **联机证书请求状态** " 页面上，单击 " **完成**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-132">On the **Online Certificate Request Status** page, click **Finish**.</span></span>

17. <span data-ttu-id="325a2-133">在 " **证书分配** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-133">On the **Certificate Assignment** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="325a2-134">如果想要查看证书，请双击列表中的证书。</span><span class="sxs-lookup"><span data-stu-id="325a2-134">if you want to view the certificate, double-click the certificate in the list.</span></span>

    
    </div>

18. <span data-ttu-id="325a2-135">在 " **证书分配摘要** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-135">On the **Certificate Assignment Summary** page, click **Next**.</span></span>

19. <span data-ttu-id="325a2-136">在 " **执行命令** " 页面上，在命令完成运行后单击 " **完成** "。</span><span class="sxs-lookup"><span data-stu-id="325a2-136">On the **Executing Commands** page, click **Finish** after the commands have finished running.</span></span>

20. <span data-ttu-id="325a2-137">在 " **证书向导** " 页面上，单击 " **关闭**"。</span><span class="sxs-lookup"><span data-stu-id="325a2-137">On the **Certificate Wizard** page, click **Close**.</span></span>

<span data-ttu-id="325a2-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="325a2-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

