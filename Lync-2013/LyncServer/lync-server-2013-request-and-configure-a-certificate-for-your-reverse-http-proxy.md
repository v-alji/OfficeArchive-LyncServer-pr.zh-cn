---
title: 为 HTTP 反向代理请求和配置证书
description: 为反向 HTTP 代理请求和配置证书。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Request and configure a certificate for your reverse HTTP proxy
ms:assetid: 4b70991e-5f10-40a3-b069-0b227c3a3a0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429704(v=OCS.15)
ms:contentKeyID: 48184085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdeaa080e3ccb6a9895e18a6ac02084e99a1e33e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442745"
---
# <a name="request-and-configure-a-certificate-for-your-reverse-http-proxy-in-lync-server-2013"></a><span data-ttu-id="94d2d-103">在 Lync Server 2013 中为 HTTP 反向代理请求和配置证书</span><span class="sxs-lookup"><span data-stu-id="94d2d-103">Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="94d2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="94d2d-104">

<span> </span></span></span>

<span data-ttu-id="94d2d-105">_**主题上次修改时间：** 2014-02-14_</span><span class="sxs-lookup"><span data-stu-id="94d2d-105">_**Topic Last Modified:** 2014-02-14_</span></span>

<span data-ttu-id="94d2d-106">对于向运行 Microsoft Lync Server 2013 的内部服务器颁发服务器证书的 CA 基础结构，在运行 Microsoft Forefront 威胁管理网关2010或 IIS ARR 的服务器上，你需要安装根证书颁发机构 (CA) 证书。</span><span class="sxs-lookup"><span data-stu-id="94d2d-106">You need to install the root certification authority (CA) certificate on the server running Microsoft Forefront Threat Management Gateway 2010 or IIS ARR for the CA infrastructure that issued the server certificates to the internal servers running Microsoft Lync Server 2013.</span></span>

<span data-ttu-id="94d2d-107">您还必须在反向代理服务器上安装公共 web 服务器证书。</span><span class="sxs-lookup"><span data-stu-id="94d2d-107">You also must install a public web server certificate on your reverse proxy server.</span></span> <span data-ttu-id="94d2d-108">此证书的主题备用名称应包含已发布的外部完全限定的域名， (Fqdn) 为远程访问启用用户的每个池的 Fqdn，以及将在该 Edge 基础结构中使用的所有控制器或控制器池的外部 Fqdn。</span><span class="sxs-lookup"><span data-stu-id="94d2d-108">This certificate’s subject alternative names should contain the published external fully qualified domain names (FQDNs) of each pool that is home to users enabled for remote access, and the external FQDNs of all Directors or Director pools that will be used within that Edge infrastructure.</span></span> <span data-ttu-id="94d2d-109">主题备用名称还必须包含会议简单 URL、拨入式简单 URL，如果你要部署移动应用程序并计划使用自动发现，请按下表所示使用 "外部自动发现服务" URL。</span><span class="sxs-lookup"><span data-stu-id="94d2d-109">The subject alternative name must also contain the meeting simple URL, the dial-in simple URL, and, if you are deploying mobile applications and plan to use automatic discovery, the external Autodiscover Service URL as shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="94d2d-110">值</span><span class="sxs-lookup"><span data-stu-id="94d2d-110">Value</span></span></th>
<th><span data-ttu-id="94d2d-111">示例</span><span class="sxs-lookup"><span data-stu-id="94d2d-111">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94d2d-112">主题名称</span><span class="sxs-lookup"><span data-stu-id="94d2d-112">Subject name</span></span></p></td>
<td><p><span data-ttu-id="94d2d-113">池 FQDN</span><span class="sxs-lookup"><span data-stu-id="94d2d-113">Pool FQDN</span></span></p></td>
<td><p><span data-ttu-id="94d2d-114">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d2d-114">webext.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d2d-115">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="94d2d-115">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="94d2d-116">池 FQDN</span><span class="sxs-lookup"><span data-stu-id="94d2d-116">Pool FQDN</span></span></p></td>
<td><p><span data-ttu-id="94d2d-117">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d2d-117">webext.contoso.com</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="94d2d-118">主题名称还必须存在于 "主题备用名称" 中。</span><span class="sxs-lookup"><span data-stu-id="94d2d-118">The subject name must also be present in the subject alternative name.</span></span>

</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d2d-119">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="94d2d-119">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="94d2d-120">如果部署了 Director，则可选的 Director Web 服务 () </span><span class="sxs-lookup"><span data-stu-id="94d2d-120">Optional Director Web Services (if Director is deployed)</span></span></p></td>
<td><p><span data-ttu-id="94d2d-121">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d2d-121">webdirext.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d2d-122">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="94d2d-122">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="94d2d-123">会议简单 URL</span><span class="sxs-lookup"><span data-stu-id="94d2d-123">Meeting simple URL</span></span></p>



> [!NOTE]
> <span data-ttu-id="94d2d-124">所有会议简单 Url 必须位于主题备用名称中。</span><span class="sxs-lookup"><span data-stu-id="94d2d-124">All meeting simple URLs must be in the subject alternative name.</span></span> <span data-ttu-id="94d2d-125">每个 SIP 域必须至少有一个活动会议简单 URL。</span><span class="sxs-lookup"><span data-stu-id="94d2d-125">Each SIP domain must have at least one active meeting simple URL.</span></span>

</td>
<td><p><span data-ttu-id="94d2d-126">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d2d-126">meet.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d2d-127">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="94d2d-127">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="94d2d-128">拨入简单 URL</span><span class="sxs-lookup"><span data-stu-id="94d2d-128">Dial-in simple URL</span></span></p></td>
<td><p><span data-ttu-id="94d2d-129">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d2d-129">dialin.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d2d-130">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="94d2d-130">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="94d2d-131">Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="94d2d-131">Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="94d2d-132">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d2d-132">officewebapps01.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d2d-133">使用者替代名称</span><span class="sxs-lookup"><span data-stu-id="94d2d-133">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="94d2d-134">外部自动发现服务 URL</span><span class="sxs-lookup"><span data-stu-id="94d2d-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="94d2d-135">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d2d-135">lyncdiscover.contoso.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="94d2d-136">如果你还在使用 Microsoft Exchange Server，你还需要为 Exchange 自动发现和 web 服务 Url 配置反向代理规则。</span><span class="sxs-lookup"><span data-stu-id="94d2d-136">If you are also using Microsoft Exchange Server you will also need to configure reverse proxy rules for the Exchange autodiscover and web services URLs.</span></span>

</td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]
> <span data-ttu-id="94d2d-137">如果内部部署包含多个标准版服务器或前端池，则必须为每个外部 web 场 FQDN 配置 web 发布规则，并且你将需要每个外部 web 场 FQDN 的证书和 web 侦听器，或者你必须获取一个证书，其主题备用名称中包含所有池使用的名称，并将其分配给 web 侦听器。，并在多个 web 发布规则之间共享它。</span><span class="sxs-lookup"><span data-stu-id="94d2d-137">If your internal deployment consists of more than one Standard Edition server or Front End pool, you must configure web publishing rules for each external web farm FQDN and you will either need a certificate and web listener for each, or you must obtain a certificate whose subject alternative name contains the names used by all of the pools, assign it to a web listener, and share it among multiple web publishing rules.</span></span>



</div>

<div>

## <a name="create-a-certificate-request"></a><span data-ttu-id="94d2d-138">创建证书请求</span><span class="sxs-lookup"><span data-stu-id="94d2d-138">Create a Certificate Request</span></span>

<span data-ttu-id="94d2d-139">在反向代理服务器上创建证书请求。</span><span class="sxs-lookup"><span data-stu-id="94d2d-139">You create a certificate request on the reverse proxy.</span></span> <span data-ttu-id="94d2d-140">在另一台计算机上创建一个请求，但必须使用私钥导出签名的证书，并在从公共证书颁发机构收到该证书后将其导入到反向代理。</span><span class="sxs-lookup"><span data-stu-id="94d2d-140">You create a request on another computer, but you must export the signed certificate with the private key and import it onto the reverse proxy once you have received it from the public certification authority.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="94d2d-141"> (CSR) 证书申请或证书签名请求是受信任的公共证书颁发机构 (CA) 对请求的计算机的公钥进行验证和签名的请求。</span><span class="sxs-lookup"><span data-stu-id="94d2d-141">A certificate request or a certificate signing request (CSR) is a request to a trusted public certification authority (CA) to validate and sign the requesting computer’s public key.</span></span> <span data-ttu-id="94d2d-142">当生成证书时，将创建一个公钥和一个私钥。</span><span class="sxs-lookup"><span data-stu-id="94d2d-142">When a certificate is generated, a public key and a private key are created.</span></span> <span data-ttu-id="94d2d-143">仅共享和签名公钥。</span><span class="sxs-lookup"><span data-stu-id="94d2d-143">Only the public key is shared and signed.</span></span> <span data-ttu-id="94d2d-144">正如名称所示，公钥可用于任何公共请求。</span><span class="sxs-lookup"><span data-stu-id="94d2d-144">As the name implies, the public key is made available to any public request.</span></span> <span data-ttu-id="94d2d-145">公钥供客户、服务器和其他申请者使用，这些申请者需要安全地交换信息并验证计算机的标识。</span><span class="sxs-lookup"><span data-stu-id="94d2d-145">The public key is for use by clients, servers and other requesters that need to exchange information securely and validate a computer’s identity.</span></span> <span data-ttu-id="94d2d-146">私钥保持安全，并且仅由创建密钥对的计算机使用，用于解密使用其公钥加密的消息。</span><span class="sxs-lookup"><span data-stu-id="94d2d-146">The private key is kept secured and is used only by the computer that created the key pair to decrypt messages encrypted with its public key.</span></span> <span data-ttu-id="94d2d-147">私钥可用于其他用途。</span><span class="sxs-lookup"><span data-stu-id="94d2d-147">The private key can be used for other purposes.</span></span> <span data-ttu-id="94d2d-148">对于反向代理目的，数据加密是主要用途。</span><span class="sxs-lookup"><span data-stu-id="94d2d-148">For reverse proxy purposes, data encipherment is the primary use.</span></span> <span data-ttu-id="94d2d-149">Secondarily，证书密钥级别的证书身份验证是另一种用途，仅限于验证请求者拥有计算机的公钥，或者你拥有公钥的计算机实际上是它所声明的计算机。</span><span class="sxs-lookup"><span data-stu-id="94d2d-149">Secondarily, the certificate authentication at the certificate key level is another use, and is limited only to validation that a requester has the computer’s public key, or that the computer that you have a public key for is actually the computer that it claims to be.</span></span>



</div>

<div>


> [!TIP]
> <span data-ttu-id="94d2d-150">如果同时计划 Edge 服务器证书和反向代理证书，应注意两种证书要求之间有很大的相似性。</span><span class="sxs-lookup"><span data-stu-id="94d2d-150">If you plan your Edge Server certificates and your reverse proxy certificates at the same time, you should notice that there is a great deal of similarity between the two certificate requirements.</span></span> <span data-ttu-id="94d2d-151">配置和请求 Edge 服务器证书时，请结合边缘服务器和反向代理主题备用名称。</span><span class="sxs-lookup"><span data-stu-id="94d2d-151">When you configure and request your Edge Server certificate, combine the Edge Server and the reverse proxy subject alternative names.</span></span> <span data-ttu-id="94d2d-152">如果你导出证书和私钥并将导出的文件复制到反向代理，然后导入证书/密钥对并在即将进行的过程中根据需要分配证书/密钥对，则可以为反向代理使用相同的证书。</span><span class="sxs-lookup"><span data-stu-id="94d2d-152">You can use the same certificate for your reverse proxy if you export the certificate and the private key and copy the exported file to the reverse proxy and then import the certificate/key pair and assign it as needed in the upcoming procedures.</span></span> <span data-ttu-id="94d2d-153">请参阅 lync server 2013 中的边缘服务器 &nbsp; <A href="lync-server-2013-plan-for-edge-server-certificates.md">计划</A>和反向代理<A href="lync-server-2013-certificate-summary-reverse-proxy.md">证书摘要-lync Server 2013 中的反向</A>代理服务器证书的证书要求。</span><span class="sxs-lookup"><span data-stu-id="94d2d-153">Refer to the certificate requirements for the Edge Server&nbsp;<A href="lync-server-2013-plan-for-edge-server-certificates.md">Plan for Edge Server certificates in Lync Server 2013</A> and the reverse proxy <A href="lync-server-2013-certificate-summary-reverse-proxy.md">Certificate summary - Reverse proxy in Lync Server 2013</A>.</span></span> <span data-ttu-id="94d2d-154">请确保使用可导出的私钥创建证书。</span><span class="sxs-lookup"><span data-stu-id="94d2d-154">Make sure that you create the certificate with an exportable private key.</span></span> <span data-ttu-id="94d2d-155">使用池边缘服务器创建证书和证书请求时需要具有可导出的私钥，因此这是一种正常做法，在 "Lync Server 部署向导" 中，边缘服务器的证书向导将允许你设置 "设置 <STRONG>私钥可导出</STRONG> " 标志。</span><span class="sxs-lookup"><span data-stu-id="94d2d-155">Creating the certificate and certificate request with an exportable private key is required for pooled Edge Servers, so this is a normal practice and the Certificate Wizard in the Lync Server Deployment Wizard for the Edge Server will allow you to set the <STRONG>Make private key exportable</STRONG> flag.</span></span> <span data-ttu-id="94d2d-156">从公共证书颁发机构收到证书申请后，您将导出证书和私钥。</span><span class="sxs-lookup"><span data-stu-id="94d2d-156">Once you receive the certificate request back from the public certification authority, you will export the certificate and the private key.</span></span> <span data-ttu-id="94d2d-157">有关如何使用私钥创建和导出您的证书的详细信息，请参阅主题为 <A href="lync-server-2013-set-up-certificates-for-the-external-edge-interface.md">Lync Server 2013 的外部边缘界面设置</A> 证书中的 "导出证书并为该池的私钥" 部分。</span><span class="sxs-lookup"><span data-stu-id="94d2d-157">See the section “To export the certificate with the private key for Edge Servers in a pool” in the topic <A href="lync-server-2013-set-up-certificates-for-the-external-edge-interface.md">Set up certificates for the external edge interface for Lync Server 2013</A> for details on how to create and export your certificate with a private key.</span></span> <span data-ttu-id="94d2d-158">证书的扩展名应为 <STRONG>.pfx</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="94d2d-158">The extension of the certificate should be of type <STRONG>.pfx</STRONG>.</span></span>



</div>

<span data-ttu-id="94d2d-159">若要在将分配证书和私钥的计算机上生成证书签名请求，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="94d2d-159">To generate a certificate signing request on the computer where the certificate and private key will be assigned, you do the following:</span></span>

<span data-ttu-id="94d2d-160">**创建证书签名请求**</span><span class="sxs-lookup"><span data-stu-id="94d2d-160">**Creating a certificate signing request**</span></span>

1.  <span data-ttu-id="94d2d-161">打开 Microsoft 管理控制台 (MMC) 并添加 "证书" 管理单元，然后选择 " **计算机**"，然后展开 " **个人**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-161">Open the Microsoft Management Console (MMC) and add the Certificates snap-in and select **Computers**, then expand **Personal**.</span></span> <span data-ttu-id="94d2d-162">有关如何在 Microsoft 管理控制台 (MMC) 中创建证书控制台的详细信息，请参阅 [https://go.microsoft.com/fwlink/?LinkId=282616](https://go.microsoft.com/fwlink/?linkid=282616) 。</span><span class="sxs-lookup"><span data-stu-id="94d2d-162">For details on how to create a certificates console in the Microsoft Management Console (MMC), see [https://go.microsoft.com/fwlink/?LinkId=282616](https://go.microsoft.com/fwlink/?linkid=282616).</span></span>

2.  <span data-ttu-id="94d2d-163">右键单击 " **证书**"，单击 " **所有任务**"，单击 " **高级操作**"，然后单击 " **创建自定义请求**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-163">Right-click **Certificates**, click **All Tasks**, click **Advanced Operations**, click **Create Custom Request**.</span></span>

3.  <span data-ttu-id="94d2d-164">在 " **证书注册** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-164">On the **Certificate Enrollment** page, click **Next**.</span></span>

4.  <span data-ttu-id="94d2d-165">在 " **选择证书注册策略** " 页面的 " **自定义请求**" 下，选择 " **继续，不包含注册策略**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-165">On the **Select Certificate Enrollment Policy** page under **Custom Request**, select **Proceed without enrollment policy**.</span></span> <span data-ttu-id="94d2d-166">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-166">Click **Next**.</span></span>

5.  <span data-ttu-id="94d2d-167">在 " **自定义请求** " 页面上，选择 " **模板** " **(没有) 旧版密钥的模板**。</span><span class="sxs-lookup"><span data-stu-id="94d2d-167">On the **Custom Request** page, for **Template** select **(No template) Legacy key**.</span></span> <span data-ttu-id="94d2d-168">除非您的证书提供商另有通知，否则请保留 **取消选中默认扩展名** 和 **PKCS \# 10** 上的 **请求格式** 选择。</span><span class="sxs-lookup"><span data-stu-id="94d2d-168">Unless otherwise directed by your certificate provider, leave **Suppress default extensions** unchecked and the **Request format** selection on **PKCS \#10**.</span></span> <span data-ttu-id="94d2d-169">单击" **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-169">Click **Next**.</span></span>

6.  <span data-ttu-id="94d2d-170">在 " **证书信息** " 页面上，单击 " **详细信息**"，然后单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-170">On the **Certificate Information** page, click **Details**, then click **Properties**.</span></span>

7.  <span data-ttu-id="94d2d-171">在 " **证书属性** " 页面上 " **常规** " 选项卡上的 " **友好名称** " 字段中，键入此证书的名称。</span><span class="sxs-lookup"><span data-stu-id="94d2d-171">On the **Certificate Properties** page on the **General** tab in the **Friendly Name** field, type a name for this certificate.</span></span> <span data-ttu-id="94d2d-172">（可选）在 " **说明** " 字段中键入说明。</span><span class="sxs-lookup"><span data-stu-id="94d2d-172">Optionally, type a description in the **Description** field.</span></span> <span data-ttu-id="94d2d-173">管理员通常使用友好名称和描述来标识证书用途，例如 **Lync Server 的反向代理侦听器**。</span><span class="sxs-lookup"><span data-stu-id="94d2d-173">The Friendly Name and description are typically used by the Administrator to identify what the certificate purpose is, such as **Reverse Proxy Listener for Lync Server**.</span></span>

8.  <span data-ttu-id="94d2d-174">选择 "**主题**" 选项卡。在 **类型** 的 "**主题名称**" 下，选择 "主题名称" 类型的 "**公用名**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-174">Select the **Subject** tab. Under **Subject name** for the **Type**, select **Common name** for the Subject name type.</span></span> <span data-ttu-id="94d2d-175">对于 " **值**"，请键入将用于反向代理的主题名称，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-175">For the **Value**, type the subject name that you will use for the reverse proxy, and then click **Add**.</span></span> <span data-ttu-id="94d2d-176">在本主题的表所提供的示例中，主题名称是 webext.contoso.com，并将键入到主题名称的值字段中。</span><span class="sxs-lookup"><span data-stu-id="94d2d-176">In the example provided in the table in this topic, the subject name is webext.contoso.com and would be typed into the Value field for the Subject name.</span></span>

9.  <span data-ttu-id="94d2d-177">在 "**其他名称**" 下的 "**主题**" 选项卡上，从 "**类型**" 下拉列表中选择 " **DNS** "。</span><span class="sxs-lookup"><span data-stu-id="94d2d-177">On the **Subject** tab under **Alternative name**, select **DNS** from the drop down for **Type**.</span></span> <span data-ttu-id="94d2d-178">对于证书上所需的每个已定义的主题备用名称，请键入完全限定的域名，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-178">For each defined subject alternative name that you require on the certificate, type the fully qualified domain name, then click **Add**.</span></span> <span data-ttu-id="94d2d-179">例如，在表中有三个主题可选名称、meet.contoso.com、dialin.contoso.com 和 lyncdiscover.contoso.com。</span><span class="sxs-lookup"><span data-stu-id="94d2d-179">For example, in the table there are three subject alternative names, meet.contoso.com, dialin.contoso.com, and lyncdiscover.contoso.com.</span></span> <span data-ttu-id="94d2d-180">在 " **值** " 字段中，键入 meet.contoso.com，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-180">In the **Value** field, type meet.contoso.com, then click **Add**.</span></span> <span data-ttu-id="94d2d-181">对你需要定义的每个主题的备用名称重复上述操作。</span><span class="sxs-lookup"><span data-stu-id="94d2d-181">Repeat for each subject alternative names that you need to define.</span></span>

10. <span data-ttu-id="94d2d-182">在 " **证书属性** " 页面上，单击 " **扩展** " 选项卡。在此页面上，你将定义 **密钥用法** 中的加密密钥用途以及扩展密钥用法中的扩展密钥用法 **(应用程序策略)**。</span><span class="sxs-lookup"><span data-stu-id="94d2d-182">On the **Certificate Properties** page, click the **Extensions** tab. On this page, you will define the cryptographic key purposes in **Key usage** and the extended key usage in **Extended Key Usage (application policies)**.</span></span>

11. <span data-ttu-id="94d2d-183">单击 " **密钥用法** " 箭头以显示 **可用选项**。</span><span class="sxs-lookup"><span data-stu-id="94d2d-183">Click the **Key usage** arrow to show the **Available options**.</span></span> <span data-ttu-id="94d2d-184">在 "可用选项" 下，单击 " **数字签名**"，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-184">Under Available options, click **Digital signature**, then click **Add**.</span></span> <span data-ttu-id="94d2d-185">单击 " **密钥译码**"，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-185">Click **Key encipherment**, then click **Add**.</span></span> <span data-ttu-id="94d2d-186">如果未选中 " **使这些密钥用法关键** " 的复选框处于未选中状态，请选中该复选框。</span><span class="sxs-lookup"><span data-stu-id="94d2d-186">If the checkbox for **Make these key usages critical** is unchecked, select the checkbox.</span></span>

12. <span data-ttu-id="94d2d-187">单击 " **应用程序策略) 箭头 (的" 扩展密钥用法** "以显示 **可用选项**。</span><span class="sxs-lookup"><span data-stu-id="94d2d-187">Click the **Extended Key Usage (application policies)** arrow to show the **Available options**.</span></span> <span data-ttu-id="94d2d-188">在 "可用选项" 下，单击 " **服务器身份验证**"，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-188">Under Available options, click **Server Authentication**, then click **Add**.</span></span> <span data-ttu-id="94d2d-189">单击 " **客户端身份验证**"，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-189">Click **Client Authentication**, then click **Add**.</span></span> <span data-ttu-id="94d2d-190">如果选中 " **使扩展密钥用法为关键"** 的复选框，请取消选中复选框。</span><span class="sxs-lookup"><span data-stu-id="94d2d-190">If the check box for **Make the Extended Key Usages critical** is checked, unselect the checkbox.</span></span> <span data-ttu-id="94d2d-191">与必须选中的 "密钥用法" 复选框相反 () 必须确保未选中 "扩展密钥用法" 复选框。</span><span class="sxs-lookup"><span data-stu-id="94d2d-191">Contrary to the Key usage checkbox (which must be checked) you must be sure that the Extended Key Usage checkbox is not checked.</span></span>

13. <span data-ttu-id="94d2d-192">在 " **证书属性** " 页上，单击 " **私钥** " 选项卡。单击 " **键选项** " 箭头。</span><span class="sxs-lookup"><span data-stu-id="94d2d-192">On the **Certificate Properties** page, click the **Private Key** tab. Click the **Key options** arrow.</span></span> <span data-ttu-id="94d2d-193">对于 **密钥大小**，请从下拉列表中选择 **2048** 。</span><span class="sxs-lookup"><span data-stu-id="94d2d-193">For **Key size**, select **2048** from the drop down.</span></span> <span data-ttu-id="94d2d-194">如果你在此证书所针对的反向代理以外的计算机上生成此密钥对和 CSR，请选择 " **使私钥可导出**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-194">If you are generating this key pair and CSR on a computer other than the reverse proxy that this certificate is intended for, select **Make private key exportable**.</span></span>
    
    <div>
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg398321.security(OCS.15).gif" title="安全" alt="security" /><span data-ttu-id="94d2d-196">安全说明：</span><span class="sxs-lookup"><span data-stu-id="94d2d-196">Security Note:</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="94d2d-197">当在服务器场中拥有多个反向代理时，通常会建议选择 " <strong>使私钥可导出</strong> "，因为你将把证书和私钥复制到服务器场中的每台计算机。</span><span class="sxs-lookup"><span data-stu-id="94d2d-197">Selecting <strong>Make a private key exportable</strong> is generally advised when you have more than one reverse proxy in a farm because you will copy the certificate and the private key to each machine in the farm.</span></span> <span data-ttu-id="94d2d-198">如果你确实允许可导出的私钥，则必须对证书以及生成它的计算机额外小心。</span><span class="sxs-lookup"><span data-stu-id="94d2d-198">If you do allow for an exportable private key, you must take extra care with the certificate and the computer that it is generated on.</span></span> <span data-ttu-id="94d2d-199">私钥（如受损）将使证书不会被公开，并且可能会将计算机或计算机暴露给外部访问和其他安全漏洞。</span><span class="sxs-lookup"><span data-stu-id="94d2d-199">The private key, if compromised, will render the certificate useless as well as potentially expose the computer or computers to external access and other security vulnerabilities.</span></span></td>
    </tr>
    </tbody>
    </table>
    
    </div>

14. <span data-ttu-id="94d2d-200">在 " **专用密钥** " 选项卡上，单击 " **键类型** " 箭头。</span><span class="sxs-lookup"><span data-stu-id="94d2d-200">On the **Private Key** tab, click the **Key type** arrow.</span></span> <span data-ttu-id="94d2d-201">选择 " **Exchange** " 选项。</span><span class="sxs-lookup"><span data-stu-id="94d2d-201">Select the **Exchange** option.</span></span>

15. <span data-ttu-id="94d2d-202">单击 **"确定"** 保存已设置的 **证书属性** 。</span><span class="sxs-lookup"><span data-stu-id="94d2d-202">Click **OK** to save the **Certificate Properties** that you have set.</span></span>

16. <span data-ttu-id="94d2d-203">在 " **证书注册** " 页面上，单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-203">On the **Certificate Enrollment** page, click **Next**.</span></span>

17. <span data-ttu-id="94d2d-204">在 " **你想要在何处保存脱机请求？** " 页面上，系统将提示你输入 **文件名和用于** 保存证书签名请求的 **文件格式** 。</span><span class="sxs-lookup"><span data-stu-id="94d2d-204">On the **Where do you want to save the offline request?** page, you are prompted for a **File Name** and a **File Format** for saving the certificate signing request.</span></span>

18. <span data-ttu-id="94d2d-205">**在 "文件名输入"** 字段中，键入请求的路径和文件名，或单击 "**浏览**" 以选择文件的位置，然后键入请求的文件名。</span><span class="sxs-lookup"><span data-stu-id="94d2d-205">In the **File Name** entry field, type a path and filename for the request, or click **Browse** to select a location for the file and type the filename for the request.</span></span>

19. <span data-ttu-id="94d2d-206">对于 **文件格式**，请单击 " **基本 64** " 或 " **二进制**"。</span><span class="sxs-lookup"><span data-stu-id="94d2d-206">For **File format**, click either **Base 64** or **Binary**.</span></span> <span data-ttu-id="94d2d-207">选择 " **基本 64** "，除非您被您的证书的供应商指示。</span><span class="sxs-lookup"><span data-stu-id="94d2d-207">Select **Base 64** unless you are instructed otherwise by the vendor for your certificates.</span></span>

20. <span data-ttu-id="94d2d-208">找到您在上一步中保存的请求文件。</span><span class="sxs-lookup"><span data-stu-id="94d2d-208">Locate the request file that you saved in the previous step.</span></span> <span data-ttu-id="94d2d-209">提交到公共证书颁发机构。</span><span class="sxs-lookup"><span data-stu-id="94d2d-209">Submit to your public certification authority.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="94d2d-210">Microsoft 已确定满足统一通信要求的公共 Ca。</span><span class="sxs-lookup"><span data-stu-id="94d2d-210">Microsoft has identified Public CAs that meets the requirements for Unified Communications purposes.</span></span> <span data-ttu-id="94d2d-211">以下知识库文章中将保留列表。</span><span class="sxs-lookup"><span data-stu-id="94d2d-211">A list is maintained in the following knowledge base article.</span></span> <A href="https://go.microsoft.com/fwlink/?linkid=282625">https://go.microsoft.com/fwlink/?LinkId=282625</A>

    
    <span data-ttu-id="94d2d-212"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="94d2d-212"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

