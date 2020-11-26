---
title: Lync Server 2013：对 Lync 客户端使用双因素身份验证
description: Lync Server 2013：使用 Lync 客户端的双重身份验证。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using two-factor authentication with Lync client
ms:assetid: d4136e61-c3ab-4b26-85c8-c1b2c24f5ee3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn338071(v=OCS.15)
ms:contentKeyID: 55115593
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbfde1d04d4e641c8fbe4817ffce214df891b565
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438685"
---
# <a name="using-two-factor-authentication-with-lync-client-and-lync-server-2013"></a><span data-ttu-id="5704d-103">将双因素身份验证与 Lync 客户端和 Lync Server 2013 结合使用</span><span class="sxs-lookup"><span data-stu-id="5704d-103">Using two-factor authentication with Lync client and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5704d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5704d-104">

<span> </span></span></span>

<span data-ttu-id="5704d-105">_**主题上次修改时间：** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="5704d-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="5704d-106">本主题介绍了如何利用 Lync 2013 客户端的双重身份验证。</span><span class="sxs-lookup"><span data-stu-id="5704d-106">This topic described how to take advantage of two-factor authentication with Lync 2013 client.</span></span>

<div>

## <a name="sign-in-to-lync-2013-for-the-first-time"></a><span data-ttu-id="5704d-107">第一次登录 Lync 2013</span><span class="sxs-lookup"><span data-stu-id="5704d-107">Sign in to Lync 2013 for the first time</span></span>

<span data-ttu-id="5704d-108">在安装 Lync 2013 时，通常会自动配置您的 Lync 登录信息。</span><span class="sxs-lookup"><span data-stu-id="5704d-108">Your Lync sign-in information is usually configured automatically when Lync 2013 is installed.</span></span> <span data-ttu-id="5704d-109">但首次使用 Lync 时，您可能必须手动启动客户端。</span><span class="sxs-lookup"><span data-stu-id="5704d-109">But the first time you use Lync, you might have to manually start the client.</span></span>

<span data-ttu-id="5704d-110">**首次登录 Lync**</span><span class="sxs-lookup"><span data-stu-id="5704d-110">**To sign in to Lync for the first time**</span></span>

1.  <span data-ttu-id="5704d-111">登录到您的组织的网络。</span><span class="sxs-lookup"><span data-stu-id="5704d-111">Log on to your organization’s network.</span></span>

2.  <span data-ttu-id="5704d-112">选择 " **启动** \> **所有程序**" \> **Microsoft Lync \> Lync 2013**。</span><span class="sxs-lookup"><span data-stu-id="5704d-112">Select **Start** \> **All Programs** \> **Microsoft Lync \> Lync 2013**.</span></span>
    
    <span data-ttu-id="5704d-113">您应看到 Lync 登录屏幕。</span><span class="sxs-lookup"><span data-stu-id="5704d-113">You should see the Lync sign-in screen.</span></span>
    
      - <span data-ttu-id="5704d-114">如果登录地址框已经填充，请确认显示的地址是否正确。</span><span class="sxs-lookup"><span data-stu-id="5704d-114">If the sign-in address box is already filled in, confirm that the address shown is correct.</span></span>
    
      - <span data-ttu-id="5704d-115">如果不正确，或者如果该框为空，请输入您的 Lync 登录地址 (这通常与您的电子邮件地址相同) 。</span><span class="sxs-lookup"><span data-stu-id="5704d-115">If it’s not correct, or if the box is empty, enter your Lync sign-in address (this is usually the same as your email address).</span></span>
    
      - <span data-ttu-id="5704d-116">如果显示空密码框，请添加您的密码。</span><span class="sxs-lookup"><span data-stu-id="5704d-116">If an empty password box is displayed, add your password.</span></span>

3.  <span data-ttu-id="5704d-117">选择“登录”。</span><span class="sxs-lookup"><span data-stu-id="5704d-117">Select **Sign-in**.</span></span>

</div>

<div>

## <a name="sign-out-of-lync"></a><span data-ttu-id="5704d-118">注销 Lync</span><span class="sxs-lookup"><span data-stu-id="5704d-118">Sign out of Lync</span></span>

<span data-ttu-id="5704d-119">使用完 Lync 后，您可以从 "文件" 菜单中关闭显示、注销会话或退出程序。</span><span class="sxs-lookup"><span data-stu-id="5704d-119">When you’re finished using Lync, you can close the display, sign out of your session, or exit from the program, all from the File menu.</span></span> <span data-ttu-id="5704d-120">下表说明了这些选项之间的差异。</span><span class="sxs-lookup"><span data-stu-id="5704d-120">The following table explains the differences in the options.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5704d-121">选项</span><span class="sxs-lookup"><span data-stu-id="5704d-121">Option</span></span></th>
<th><span data-ttu-id="5704d-122">执行的结果</span><span class="sxs-lookup"><span data-stu-id="5704d-122">What it does</span></span></th>
<th><span data-ttu-id="5704d-123">如何执行</span><span class="sxs-lookup"><span data-stu-id="5704d-123">How to perform it</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5704d-124">关闭</span><span class="sxs-lookup"><span data-stu-id="5704d-124">Close</span></span></p></td>
<td><p><span data-ttu-id="5704d-125">关闭 Lync 显示，但让使用你的用户 ID 标识的 Lync 会话继续运行。</span><span class="sxs-lookup"><span data-stu-id="5704d-125">Closes your Lync display but lets the Lync session identified with your user ID continue to run.</span></span> <span data-ttu-id="5704d-126">因此，您可以继续接收通知并与其他人互动。</span><span class="sxs-lookup"><span data-stu-id="5704d-126">This is so you can continue to get notifications and interact with others.</span></span></p>
<p><span data-ttu-id="5704d-127">你可以随时通过单击任务栏上的 Lync 图标或屏幕底部的通知区域来恢复显示。</span><span class="sxs-lookup"><span data-stu-id="5704d-127">You can get the display back at any time by clicking the Lync icon on the taskbar or the notification area at the bottom of your screen.</span></span></p></td>
<td><p><span data-ttu-id="5704d-128">在 Lync 主窗口中，执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="5704d-128">On the Lync main window, do one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="5704d-129">选择 " <strong>选项</strong> " 按钮，然后选择 " <strong>文件</strong> &gt; <strong>关闭</strong>"。</span><span class="sxs-lookup"><span data-stu-id="5704d-129">Select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Close</strong>.</span></span></p></li>
<li><p><span data-ttu-id="5704d-130">单击窗口右上角的“关闭”<strong></strong>按钮 (X)。</span><span class="sxs-lookup"><span data-stu-id="5704d-130">Click the <strong>Close</strong> button (X) in the upper-right corner of the window.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5704d-131">注销</span><span class="sxs-lookup"><span data-stu-id="5704d-131">Sign out</span></span></p></td>
<td><p><span data-ttu-id="5704d-132">结束与你的用户 ID 相关联的 Lync 会话，但 Lync 会继续在后台运行。</span><span class="sxs-lookup"><span data-stu-id="5704d-132">Ends the Lync session associated with your user ID, but Lync continues to run in the background.</span></span> <span data-ttu-id="5704d-133">注销时，登录窗口将会出现。</span><span class="sxs-lookup"><span data-stu-id="5704d-133">When you sign out, the sign-in window will appear.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="5704d-p105">注销时选择“删除我的登录信息”<STRONG></STRONG>以从计算机中删除您的登录 ID 和密码记录。这样做使支持人员可以更轻松地解决登录问题。还通过使未经授权的用户难以使用您的凭据登录来帮助确保您的登录信息更安全。</span><span class="sxs-lookup"><span data-stu-id="5704d-p105">Select <STRONG>Delete my sign-in information</STRONG> when you sign out to remove the record of your logon ID and password from the computer. Doing this might make it easier for support people to troubleshoot sign-in issues. It can also help ensure your sign-in information is more secure by making it difficult for unauthorized users to log on with your credentials.</span></span>


</div></td>
<td><p><span data-ttu-id="5704d-137">在 Lync 主窗口中，选择 " <strong>选项</strong> " 按钮，然后选择 " <strong>文件</strong> &gt; <strong>注销"</strong>。</span><span class="sxs-lookup"><span data-stu-id="5704d-137">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Sign Out</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5704d-138">退出</span><span class="sxs-lookup"><span data-stu-id="5704d-138">Exit</span></span></p></td>
<td><p><span data-ttu-id="5704d-139">结束 Lync 会话并在计算机上关闭 Lync。</span><span class="sxs-lookup"><span data-stu-id="5704d-139">Ends your Lync session and shuts down Lync on your computer.</span></span> <span data-ttu-id="5704d-140">退出后，如果要重新启动 Lync，请选择 " <strong>启动</strong> &gt; <strong>所有程序</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>"。</span><span class="sxs-lookup"><span data-stu-id="5704d-140">After exiting, if you want to restart Lync, select <strong>Start</strong> &gt; <strong>All Programs</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>.</span></span></p></td>
<td><p><span data-ttu-id="5704d-141">在 Lync 主窗口中，选择 " <strong>选项</strong> " 按钮，然后选择 " <strong>文件</strong> &gt; <strong>退出</strong>"。</span><span class="sxs-lookup"><span data-stu-id="5704d-141">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Exit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sign-in-to-lync-with-a-smart-card"></a><span data-ttu-id="5704d-142">使用智能卡登录 Lync</span><span class="sxs-lookup"><span data-stu-id="5704d-142">Sign in to Lync with a Smart Card</span></span>

<span data-ttu-id="5704d-143">某些组织现在使用一个称为双因素身份验证的多步骤登录过程来提高其 Lync 2013 用户的安全性。</span><span class="sxs-lookup"><span data-stu-id="5704d-143">Some organizations now use a multi-step sign-in process, called two-factor authentication, to increase security for their Lync 2013 users.</span></span> <span data-ttu-id="5704d-144">如果你希望使用此选项，则需要 "智能卡" 才能登录 Lync。</span><span class="sxs-lookup"><span data-stu-id="5704d-144">If you’re expected to use this option, you’ll need a “smart card” to sign in to Lync.</span></span> <span data-ttu-id="5704d-145">智能卡分为两种种类，物理和虚拟：</span><span class="sxs-lookup"><span data-stu-id="5704d-145">Smart cards come in two varieties, physical and virtual:</span></span>

  - <span data-ttu-id="5704d-146">**物理**   关于信用卡的大小。</span><span class="sxs-lookup"><span data-stu-id="5704d-146">**Physical**   About the size of a credit card.</span></span> <span data-ttu-id="5704d-147">登录时请将其插入到智能卡读卡器中。</span><span class="sxs-lookup"><span data-stu-id="5704d-147">You insert it into a smart card reader when you log in.</span></span>

  - <span data-ttu-id="5704d-148">**虚拟**   不是物理对象，而是写入计算机上的特殊芯片的电子标识符，其实质上是将智能卡构建到计算机中。</span><span class="sxs-lookup"><span data-stu-id="5704d-148">**Virtual**   Not a physical object, but an electronic identifier that gets written to a special chip on your computer, which in essence builds the smart card into your computer.</span></span> <span data-ttu-id="5704d-149">仅适用于包含 TPM (受信任的平台模块) 芯片的 Windows 8 计算机。</span><span class="sxs-lookup"><span data-stu-id="5704d-149">Available only for use with Windows 8 computers that contain the TPM (Trusted Platform Module) chip.</span></span>

<div>

## <a name="enroll-your-smart-card"></a><span data-ttu-id="5704d-150">注册智能卡</span><span class="sxs-lookup"><span data-stu-id="5704d-150">Enroll your smart card</span></span>

<span data-ttu-id="5704d-151">在您可以使用智能卡登录之前，必须“注册”该卡，也就是说，必须使用卡识别您的用户凭据。</span><span class="sxs-lookup"><span data-stu-id="5704d-151">Before you can sign in with a smart card, the card must be “enrolled”—that is, your user credentials have to be identified with the card.</span></span> <span data-ttu-id="5704d-152">不管是物理智能卡还是虚拟智能卡都是如此。</span><span class="sxs-lookup"><span data-stu-id="5704d-152">This is the case whether the card is physical or virtual.</span></span> <span data-ttu-id="5704d-153">此过程可能已由 Lync Server 管理员执行。</span><span class="sxs-lookup"><span data-stu-id="5704d-153">This process may already been carried out by your Lync Server administrator.</span></span> <span data-ttu-id="5704d-154">如果不确定是否已执行，请与他们确认。</span><span class="sxs-lookup"><span data-stu-id="5704d-154">Check with them if you’re not sure whether that has been done.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5704d-155">由于每个虚拟智能卡仅与安装它的设备相关联，因此需要为你使用的每个 Windows 8 计算机注册一个单独的卡。</span><span class="sxs-lookup"><span data-stu-id="5704d-155">Since each virtual smart card is associated only with the device it’s installed on, a separate card will need to be enrolled for each Windows 8 computer you use.</span></span>



</div>

<span data-ttu-id="5704d-156">**手动注册智能卡**</span><span class="sxs-lookup"><span data-stu-id="5704d-156">**To manually enroll your smart card**</span></span>

1.  <span data-ttu-id="5704d-157">登录到您将运行 Lync 的计算机。</span><span class="sxs-lookup"><span data-stu-id="5704d-157">Log on to the computer you’ll be running Lync on.</span></span>

2.  <span data-ttu-id="5704d-158">使用 Internet Explorer，浏览到您的组织的“证书颁发机构 Web 注册”页面。</span><span class="sxs-lookup"><span data-stu-id="5704d-158">Using Internet Explorer, browse to your organization’s Certificate Authority Web Enrollment page.</span></span>
    
    <span data-ttu-id="5704d-159">如果尚不具备此资源的 web 地址，请询问您的 Lync Server 管理员。</span><span class="sxs-lookup"><span data-stu-id="5704d-159">Ask your Lync Server administrator for the web address of this resource if you don’t already have it.</span></span> <span data-ttu-id="5704d-160">URL 将如下所示： https://MyCA.\ [公司名称 \] /certsrv。</span><span class="sxs-lookup"><span data-stu-id="5704d-160">The URL will look something like this: https://MyCA.\[yourcompanyname\].com/certsrv.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5704d-161">如果您正在使用 Internet Explorer 10，则可能需要在兼容模式下查看此网站。</span><span class="sxs-lookup"><span data-stu-id="5704d-161">If you’re using Internet Explorer 10, you may need to view this website in Compatibility Mode.</span></span>

    
    </div>

3.  <span data-ttu-id="5704d-162">当系统提示您登录证书页面时，请使用您的域帐户（例如您的计算机的管理员）登录。</span><span class="sxs-lookup"><span data-stu-id="5704d-162">When you’re prompted to log on to the certification page, log on using your domain account (rather than as administrator of your computer).</span></span>

4.  <span data-ttu-id="5704d-163">在网站的“欢迎”页面上，选择“申请证书”。</span><span class="sxs-lookup"><span data-stu-id="5704d-163">On the website Welcome Page, select **Request a certificate**.</span></span>

5.  <span data-ttu-id="5704d-164">单击“高级申请”。</span><span class="sxs-lookup"><span data-stu-id="5704d-164">Select **Advanced Request**.</span></span>

6.  <span data-ttu-id="5704d-165">选择“创建并向此 CA 提交一个申请”，然后单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="5704d-165">Select **Create and submit a request to this CA**, then click **Next**.</span></span>

7.  <span data-ttu-id="5704d-166">现在，您将看到“智能卡注册站”页面。</span><span class="sxs-lookup"><span data-stu-id="5704d-166">Now you’ll see a page called Smart Card Enrollment Station.</span></span> <span data-ttu-id="5704d-167">批准申请以安装 ActiveX 控件，然后填写“高级证书申请”表单，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5704d-167">Approve the request to install the ActiveX control, and then complete the Advanced Certificate Request form as follows:</span></span>
    
    1.  <span data-ttu-id="5704d-168">从“证书模板”下拉列表中选择“智能卡用户”。</span><span class="sxs-lookup"><span data-stu-id="5704d-168">Select **Smartcard user** from the **Certificate Template** dropdown list.</span></span>
    
    2.  <span data-ttu-id="5704d-169">选择“创建新密钥集”。</span><span class="sxs-lookup"><span data-stu-id="5704d-169">Select **Create new key set**.</span></span>
    
    3.  <span data-ttu-id="5704d-170">在智能卡标签上查找制造商信息，然后从“CSP”下拉列表中选择该制造商。</span><span class="sxs-lookup"><span data-stu-id="5704d-170">Find the manufacturer information on the label of your smart card and select that manufacturer from the **CSP** dropdown list.</span></span>
    
    4.  <span data-ttu-id="5704d-171">选择“CSP”作为申请格式（如果尚未选中）。</span><span class="sxs-lookup"><span data-stu-id="5704d-171">Select **CSP** as the Request Format, if it’s not already selected.</span></span>
    
    5.  <span data-ttu-id="5704d-172">从“哈希算法”下拉列表中选择“sha1”（如果尚未选中）。</span><span class="sxs-lookup"><span data-stu-id="5704d-172">Select **sha1** from the Hash Algorithm dropdown list, if it’s not already selected.</span></span>
    
    6.  <span data-ttu-id="5704d-173">为您的证书提供您将识别的名称，然后单击“提交”。</span><span class="sxs-lookup"><span data-stu-id="5704d-173">Give your certificate a name you’ll recognize, and click **Submit**.</span></span>

8.  <span data-ttu-id="5704d-174">现在在连接到注册站的读卡器中插入空智能卡，然后单击“注册”。</span><span class="sxs-lookup"><span data-stu-id="5704d-174">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

9.  <span data-ttu-id="5704d-175">出现提示时，输入您的个人标识号 (PIN)，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5704d-175">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5704d-176">如果您的技术支持人员未向您提供用于注册智能卡的特殊 PIN，请使用默认智能卡 PIN 值 12345678。</span><span class="sxs-lookup"><span data-stu-id="5704d-176">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

10. <span data-ttu-id="5704d-177">选择可在首次使用智能卡时强制用户（您）更改 PIN 的选项。</span><span class="sxs-lookup"><span data-stu-id="5704d-177">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

11. <span data-ttu-id="5704d-178">现在在连接到注册站的读卡器中插入空智能卡，然后单击“注册”。</span><span class="sxs-lookup"><span data-stu-id="5704d-178">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

12. <span data-ttu-id="5704d-179">出现提示时，输入您的个人标识号 (PIN)，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5704d-179">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5704d-180">如果您的技术支持人员未向您提供用于注册智能卡的特殊 PIN，请使用默认智能卡 PIN 值 12345678。</span><span class="sxs-lookup"><span data-stu-id="5704d-180">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

13. <span data-ttu-id="5704d-181">选择可在首次使用智能卡时强制用户（您）更改 PIN 的选项。</span><span class="sxs-lookup"><span data-stu-id="5704d-181">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

14. <span data-ttu-id="5704d-182">单击“确定”以确认显示的证书包含您的信息。</span><span class="sxs-lookup"><span data-stu-id="5704d-182">Click **OK** to confirm that the certificate displayed has your information on it.</span></span>

15. <span data-ttu-id="5704d-183">看到已颁发证书的通知后，单击“安装此证书”以完成注册过程。</span><span class="sxs-lookup"><span data-stu-id="5704d-183">Once you see the notice that the certificate has been issued, click **Install this certificate** to complete the enrollment process.</span></span>

</div>

<div>

## <a name="sign-in-to-lync-with-your-smart-card-credentials"></a><span data-ttu-id="5704d-184">通过智能卡凭据登录 Lync</span><span class="sxs-lookup"><span data-stu-id="5704d-184">Sign in to Lync with your smart card credentials</span></span>

<span data-ttu-id="5704d-185">首次使用智能卡之前，建议在 Lync 登录页面上单击 " **删除我的登录信息** "。</span><span class="sxs-lookup"><span data-stu-id="5704d-185">Before you use your smart card for the first time, it’s recommended that you click **Delete my sign-in info** on the Lync sign-in page.</span></span> <span data-ttu-id="5704d-186">这样做可清除您的计算机上存储的任何登录凭据，并消除可能的错误源。</span><span class="sxs-lookup"><span data-stu-id="5704d-186">Doing this clears any sign-in credentials stored on your computer, and eliminates a possible source of error.</span></span>

<span data-ttu-id="5704d-187">**若要通过智能卡凭据登录 Lync**</span><span class="sxs-lookup"><span data-stu-id="5704d-187">**To sign in to Lync with your smart card credentials**</span></span>

1.  <span data-ttu-id="5704d-188">启动 Lync 客户端。</span><span class="sxs-lookup"><span data-stu-id="5704d-188">Start the Lync client.</span></span>

2.  <span data-ttu-id="5704d-189">在“登录”屏幕上，在“登录地址”框中键入您的登录用户帐户名称，然后单击“登录”。</span><span class="sxs-lookup"><span data-stu-id="5704d-189">On the Sign in screen, type your sign in user account name in the **Sign-in address** box, and then click **Sign In**.</span></span>

3.  <span data-ttu-id="5704d-190">如果您正在使用虚拟智能卡，请跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="5704d-190">If you are using a virtual smart card, skip this step.</span></span>
    
    <span data-ttu-id="5704d-191">如果您正在使用物理智能卡，请在出现提示时在您的智能卡读卡器中插入智能卡，然后当检测到卡时单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5704d-191">If you are using a physical smart card, insert the smart card into your smart card reader and prompted to do so, and then click **OK** when the card is detected.</span></span>

4.  <span data-ttu-id="5704d-192">为您的智能卡键入 PIN 号码，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="5704d-192">Type in the PIN number you for your smart card and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5704d-193">如果您的支持人员未向您提供智能卡 PIN 号码，请使用默认值 12345678。</span><span class="sxs-lookup"><span data-stu-id="5704d-193">If you were not assigned a smart card PIN number by your support person, use the default value, which is 12345678.</span></span>

    
    <span data-ttu-id="5704d-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5704d-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

