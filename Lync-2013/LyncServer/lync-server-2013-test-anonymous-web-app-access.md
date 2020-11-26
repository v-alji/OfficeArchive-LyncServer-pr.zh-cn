---
title: Lync Server 2013：测试匿名 Web 应用访问
description: Lync Server 2013：测试匿名 Web 应用访问权限。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test anonymous Web App access
ms:assetid: 92f691cd-e05e-4bab-beb5-251d4b837a19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767949(v=OCS.15)
ms:contentKeyID: 63969630
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c33840912fefcaeef069e14773cfefd0834a8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441268"
---
# <a name="test-anonymous-web-app-access-in-lync-server-2013"></a><span data-ttu-id="3e091-103">在 Lync Server 2013 中测试匿名 Web 应用访问</span><span class="sxs-lookup"><span data-stu-id="3e091-103">Test anonymous Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e091-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e091-104">

<span> </span></span></span>

<span data-ttu-id="3e091-105">_**主题上次修改时间：** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="3e091-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e091-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="3e091-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="3e091-107">每月</span><span class="sxs-lookup"><span data-stu-id="3e091-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e091-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="3e091-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="3e091-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e091-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e091-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="3e091-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="3e091-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="3e091-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="3e091-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsWebAppAnonymous cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="3e091-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="3e091-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="3e091-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebAppAnonymous&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="3e091-114">说明</span><span class="sxs-lookup"><span data-stu-id="3e091-114">Description</span></span>

<span data-ttu-id="3e091-115">Test-CsWebAppAnonymous cmdlet 验证匿名用户是否可以使用 Lync Web App 加入 Lync Server 会议。</span><span class="sxs-lookup"><span data-stu-id="3e091-115">The Test-CsWebAppAnonymous cmdlet verifies that an anonymous user can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="3e091-116">运行 cmdlet 时，Test-CsWebAppAnonymous 与 Web 票证服务联系以获取匿名用户的 Web 票证。</span><span class="sxs-lookup"><span data-stu-id="3e091-116">When you run the cmdlet, Test-CsWebAppAnonymous contacts the Web Ticket service to obtain a web ticket for the anonymous user.</span></span> <span data-ttu-id="3e091-117">如果 cmdlet 成功获取此票证，Test-CsWebAppAnonymous 将与 Lync Server 联系并尝试建立单独的会议，以便发送即时消息、应用程序共享和数据协作。</span><span class="sxs-lookup"><span data-stu-id="3e091-117">If the cmdlet succeeds in obtaining this ticket, Test-CsWebAppAnonymous will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="3e091-118">请注意，Test-CsWebAppAnonymous 仅验证用于创建这些会议的 Api 和连接。</span><span class="sxs-lookup"><span data-stu-id="3e091-118">Note that Test-CsWebAppAnonymous only verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="3e091-119">该 cmdlet 实际上不会创建和执行任何会议。</span><span class="sxs-lookup"><span data-stu-id="3e091-119">The cmdlet does not actually create and conduct any conferences.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="3e091-120">运行测试</span><span class="sxs-lookup"><span data-stu-id="3e091-120">Running the test</span></span>

<span data-ttu-id="3e091-121">可以使用一对预配置的测试帐户或已启用 Lync Server 的任何两个用户的帐户运行 Test-CsWebAppAnonymous cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e091-121">The Test-CsWebAppAnonymous cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="3e091-122">若要使用测试帐户运行此检查，只需指定正在测试的 Lync Server 池的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="3e091-122">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="3e091-123">例如：</span><span class="sxs-lookup"><span data-stu-id="3e091-123">For example:</span></span>

    Test-CsWebAppAnonymous -TargetFqdn atl-cs-001.litwareinc.com

<span data-ttu-id="3e091-124">若要使用实际的用户帐户运行此检查，必须为每个帐户 (包含帐户名称和密码) 的对象创建两个 Lync Server Management Shell 凭据对象。</span><span class="sxs-lookup"><span data-stu-id="3e091-124">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="3e091-125">然后，当你调用 Test-CsWebAppAnonymous 时，你必须包含这些凭据对象和两个帐户的 SIP 地址：</span><span class="sxs-lookup"><span data-stu-id="3e091-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebAppAnonymous:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1

<span data-ttu-id="3e091-126">有关详细信息，请参阅 Test-CsWebAppAnonymous cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="3e091-126">For more information, see the help topic for the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="3e091-127">请注意，Test-CsWebAppAnonymous 已弃用，无法在 Lync Server 2013 上使用。</span><span class="sxs-lookup"><span data-stu-id="3e091-127">Note that Test-CsWebAppAnonymous is deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="3e091-128">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="3e091-128">Determining success or failure</span></span>

<span data-ttu-id="3e091-129">如果 Test-CsWebAppAnonymous 可以将匿名用户加入其会议，cmdlet 将返回测试结果成功：</span><span class="sxs-lookup"><span data-stu-id="3e091-129">If Test-CsWebAppAnonymous can join the anonymous user to his or her conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="3e091-130">目标 Fqdn：</span><span class="sxs-lookup"><span data-stu-id="3e091-130">Target Fqdn :</span></span>

<span data-ttu-id="3e091-131">结果：成功</span><span class="sxs-lookup"><span data-stu-id="3e091-131">Result : Success</span></span>

<span data-ttu-id="3e091-132">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="3e091-132">Latency : 00:00:00</span></span>

<span data-ttu-id="3e091-133">错误消息：</span><span class="sxs-lookup"><span data-stu-id="3e091-133">Error Message :</span></span>

<span data-ttu-id="3e091-134">自检</span><span class="sxs-lookup"><span data-stu-id="3e091-134">Diagnosis :</span></span>

<span data-ttu-id="3e091-135">如果匿名用户无法加入必要的会议，则测试结果将标记为 "失败"。</span><span class="sxs-lookup"><span data-stu-id="3e091-135">If the anonymous user can't join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="3e091-136">通常 Test-CsWebAppAnonymous 还会报告详细的错误消息和诊断：</span><span class="sxs-lookup"><span data-stu-id="3e091-136">Typically Test-CsWebAppAnonymous will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="3e091-137">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3e091-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3e091-138">结果：失败</span><span class="sxs-lookup"><span data-stu-id="3e091-138">Result : Failure</span></span>

<span data-ttu-id="3e091-139">延迟：00：00：05.9746266</span><span class="sxs-lookup"><span data-stu-id="3e091-139">Latency : 00:00:05.9746266</span></span>

<span data-ttu-id="3e091-140">错误消息：未收到 Web-Ticket 服务的响应</span><span class="sxs-lookup"><span data-stu-id="3e091-140">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="3e091-141">诊断： HTTP 请求未通过客户端授权</span><span class="sxs-lookup"><span data-stu-id="3e091-141">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="3e091-142">身份验证方案 "Ntlm"。</span><span class="sxs-lookup"><span data-stu-id="3e091-142">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="3e091-143">的身份验证</span><span class="sxs-lookup"><span data-stu-id="3e091-143">The authentication</span></span>

<span data-ttu-id="3e091-144">从服务器收到的标头是 "协商，NTLM"。</span><span class="sxs-lookup"><span data-stu-id="3e091-144">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="3e091-145">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="3e091-145">Reasons why the test might have failed</span></span>

<span data-ttu-id="3e091-146">Test-CsWebAppAnonymous 故障通常会绕过用户身份验证错误：你必须使用有效的用户帐户运行测试，即使 cmdlet 检查匿名用户连接到 Lync 服务器的能力。</span><span class="sxs-lookup"><span data-stu-id="3e091-146">Test-CsWebAppAnonymous failures usually revolve around user authentication errors: you must run the test using a valid user account even though the cmdlet is checking the ability of an anonymous user to connect to Lync Server.</span></span> <span data-ttu-id="3e091-147">如果 Test-CsWebAppAnonymous 失败，应验证指定用户是否具有有效的 Lync Server 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="3e091-147">If Test-CsWebAppAnonymous fails, you should verify that the specified user has valid a Lync Server user account.</span></span> <span data-ttu-id="3e091-148">您可以使用类似下面的命令检索 Lync 服务器帐户信息：</span><span class="sxs-lookup"><span data-stu-id="3e091-148">You can retrieve Lync Server account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="3e091-149">如果 Enabled 属性不等于 True 或命令失败，则意味着用户没有有效的 Lync 服务器帐户。</span><span class="sxs-lookup"><span data-stu-id="3e091-149">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.</span></span>

<span data-ttu-id="3e091-150">你还应验证运行 cmdlet 时提供的密码是否为有效密码。</span><span class="sxs-lookup"><span data-stu-id="3e091-150">You should also verify that the password that you supplied when you run the cmdlet is a valid password.</span></span>

<span data-ttu-id="3e091-151">Office Web Apps 服务器的配置问题也可能导致 Test-CsWebAppAnonymous 失败;如果你收到以下诊断，通常会出现这种情况：</span><span class="sxs-lookup"><span data-stu-id="3e091-151">Configuration problems with Office Web Apps Server can also cause Test-CsWebAppAnonymous to fail; that will often be the case if you receive the following diagnosis:</span></span>

<span data-ttu-id="3e091-152">通过客户端身份验证方案 "Ntlm" 对 HTTP 请求进行了未经授权。</span><span class="sxs-lookup"><span data-stu-id="3e091-152">The HTTP request is unauthorized with client authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="3e091-153">从服务器收到的身份验证标头是 "协商，NTLM"。</span><span class="sxs-lookup"><span data-stu-id="3e091-153">The authentication header received from the server was 'Negotiate,NTLM'.</span></span>

<span data-ttu-id="3e091-154">有关诊断和解决 Office Web Apps 服务器问题的详细信息，请参阅博客文章 [Office Web Apps server 2013-计算机始终报告为 "不正常](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy)"。</span><span class="sxs-lookup"><span data-stu-id="3e091-154">For more information on diagnosing and resolving Office Web Apps Server problems see the blog post [Office Web Apps Server 2013 - machines are always reported as Unhealthy](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).</span></span>

<span data-ttu-id="3e091-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e091-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

