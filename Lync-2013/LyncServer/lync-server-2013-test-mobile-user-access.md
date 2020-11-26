---
title: Lync Server 2013：测试移动用户访问
description: Lync Server 2013：测试移动用户访问。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile user access
ms:assetid: 81d97420-428b-41b7-91ef-185d572d3456
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767947(v=OCS.15)
ms:contentKeyID: 63969624
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e99a05e6ef9fe925126026452823e5edcc100ede
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441240"
---
# <a name="test-mobile-user-access-in-lync-server-2013"></a><span data-ttu-id="13122-103">在 Lync Server 2013 中测试移动用户访问权限</span><span class="sxs-lookup"><span data-stu-id="13122-103">Test mobile user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13122-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13122-104">

<span> </span></span></span>

<span data-ttu-id="13122-105">_**主题上次修改时间：** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="13122-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13122-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="13122-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="13122-107">每月</span><span class="sxs-lookup"><span data-stu-id="13122-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13122-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="13122-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="13122-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="13122-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13122-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="13122-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="13122-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="13122-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="13122-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsMcxConference cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="13122-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxConference cmdlet.</span></span> <span data-ttu-id="13122-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="13122-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="13122-114">说明</span><span class="sxs-lookup"><span data-stu-id="13122-114">Description</span></span>

<span data-ttu-id="13122-115">移动服务使移动设备用户可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="13122-115">The Mobility Service enables mobile device users to do such things as:</span></span>

1.  <span data-ttu-id="13122-116">Exchange 即时消息和状态信息。</span><span class="sxs-lookup"><span data-stu-id="13122-116">Exchange instant messages and presence information.</span></span>

2.  <span data-ttu-id="13122-117">在内部存储和检索语音邮件，而不是无线提供商。</span><span class="sxs-lookup"><span data-stu-id="13122-117">Store and retrieve voice mail internally instead of with their wireless provider.</span></span>

3.  <span data-ttu-id="13122-118">利用 Lync 服务器功能，例如通过工作电话和拨出式会议进行呼叫。</span><span class="sxs-lookup"><span data-stu-id="13122-118">Take advantage of Lync Server capabilities such as Call via Work and dial-out conferencing.</span></span> <span data-ttu-id="13122-119">Test-CsMcxConference cmdlet 提供一种快速简便的方式来验证用户是否可以使用移动设备加入和参与 Lync Server 会议。</span><span class="sxs-lookup"><span data-stu-id="13122-119">The Test-CsMcxConference cmdlet provides a quick and easy way to verify that users can join and participate in Lync Server conferences by using a mobile device.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="13122-120">运行测试</span><span class="sxs-lookup"><span data-stu-id="13122-120">Running the test</span></span>

<span data-ttu-id="13122-121">若要运行此检查，必须为每个帐户 (包含帐户名称和密码) 的对象创建三个 Windows PowerShell 凭据对象。</span><span class="sxs-lookup"><span data-stu-id="13122-121">To run this check, you must create three Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="13122-122">然后，当你调用 Test-CsMcxConference 时，必须包含这些凭据对象和两个帐户的 SIP 地址，如下例所示：</span><span class="sxs-lookup"><span data-stu-id="13122-122">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsMcxConference as shown in the following example:</span></span>

    $organizerCred = Get-Credential "litwareinc\kenmyer"
    $user1Cred = Get-Credential "litwareinc\packerman"
    $user2Cred = Get-Credential "litwareinc\adelaney"
    
    Test-CsMcxConference -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -OrganizerSipAddress "sip:kenmyer@litwareinc.com" -OrganizerCredential $organizerCred -UserSipAddress "sip:pilar@litwareinc.com" -UserCredential $user1Cred -User2SipAddress "sip:adelaney@litwareinc.com" -User2Credential $user2Cred

<span data-ttu-id="13122-123">有关详细信息，请参阅 [CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="13122-123">For more information, see the help topic for the [Test-CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="13122-124">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="13122-124">Determining success or failure</span></span>

<span data-ttu-id="13122-125">如果检查成功，Test-CsMcxConference 将报告成功的测试结果：</span><span class="sxs-lookup"><span data-stu-id="13122-125">If the check succeeds, Test-CsMcxConference will report a test result of Success:</span></span>

<span data-ttu-id="13122-126">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="13122-126">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="13122-127">目标 Uri： http://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="13122-127">Target Uri : http://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="13122-128">结果：成功</span><span class="sxs-lookup"><span data-stu-id="13122-128">Result : Success</span></span>

<span data-ttu-id="13122-129">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="13122-129">Latency : 00:00:00</span></span>

<span data-ttu-id="13122-130">错误消息：</span><span class="sxs-lookup"><span data-stu-id="13122-130">Error Message :</span></span>

<span data-ttu-id="13122-131">自检</span><span class="sxs-lookup"><span data-stu-id="13122-131">Diagnosis :</span></span>

<span data-ttu-id="13122-132">如果检查失败 Test-CsMcxConference 将报告失败的测试结果。</span><span class="sxs-lookup"><span data-stu-id="13122-132">If the check is unsuccessful Test-CsMcxConference will report a test result of Failure.</span></span> <span data-ttu-id="13122-133">此测试结果通常附带详细的错误消息和诊断。</span><span class="sxs-lookup"><span data-stu-id="13122-133">This test result will typically be accompanied by a detailed error message and diagnosis.</span></span> <span data-ttu-id="13122-134">例如：</span><span class="sxs-lookup"><span data-stu-id="13122-134">For example:</span></span>

<span data-ttu-id="13122-135">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="13122-135">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="13122-136">目标 Uri： https://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="13122-136">Target Uri : https://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="13122-137">结果：失败</span><span class="sxs-lookup"><span data-stu-id="13122-137">Result : Failure</span></span>

<span data-ttu-id="13122-138">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="13122-138">Latency : 00:00:00</span></span>

<span data-ttu-id="13122-139">错误消息：未收到 Web-Ticket 服务的响应。</span><span class="sxs-lookup"><span data-stu-id="13122-139">Error Message : No response received for Web-Ticket service.</span></span>

<span data-ttu-id="13122-140">内部异常： HHTP 请求未通过客户端授权</span><span class="sxs-lookup"><span data-stu-id="13122-140">Inner Exception:The HHTP request is unauthorized with client</span></span>

<span data-ttu-id="13122-141">协商方案 "Ntlm"。</span><span class="sxs-lookup"><span data-stu-id="13122-141">negotiation scheme 'Ntlm'.</span></span> <span data-ttu-id="13122-142">收到的身份验证标头</span><span class="sxs-lookup"><span data-stu-id="13122-142">The authentication header received</span></span>

<span data-ttu-id="13122-143">来自服务器的 "协商"。</span><span class="sxs-lookup"><span data-stu-id="13122-143">from the server was 'Negotiate'.</span></span>

<span data-ttu-id="13122-144">内部异常：远程服务器返回错误： (401) </span><span class="sxs-lookup"><span data-stu-id="13122-144">Inner Exception:The remote server returned an error: (401)</span></span>

<span data-ttu-id="13122-145">便.</span><span class="sxs-lookup"><span data-stu-id="13122-145">Unauthorized.</span></span>

<span data-ttu-id="13122-146">自检</span><span class="sxs-lookup"><span data-stu-id="13122-146">Diagnosis :</span></span>

<span data-ttu-id="13122-147">内部诊断： X 毫秒-服务器-Fqdb： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="13122-147">Inner Diagnosis:X-MS-server-Fqdb : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="13122-148">Cache-Control： private</span><span class="sxs-lookup"><span data-stu-id="13122-148">Cache-Control : private</span></span>

<span data-ttu-id="13122-149">内容类型：文本/html;字符集 = utf-8。</span><span class="sxs-lookup"><span data-stu-id="13122-149">Content-Type : text/html; charset=utf-8.</span></span>

<span data-ttu-id="13122-150">服务器： Microsoft-IIS/8。5</span><span class="sxs-lookup"><span data-stu-id="13122-150">Server : Microsoft-IIS/8.5</span></span>

<span data-ttu-id="13122-151">WWW-Authenticate：协商，NTLM</span><span class="sxs-lookup"><span data-stu-id="13122-151">WWW-Authenticate : Negotiate,NTLM</span></span>

<span data-ttu-id="13122-152">X-通过： ASP.NET</span><span class="sxs-lookup"><span data-stu-id="13122-152">X-Powered-By : ASP.NET</span></span>

<span data-ttu-id="13122-153">X-内容类型-选项： nosniff</span><span class="sxs-lookup"><span data-stu-id="13122-153">X-Content-Type-Options : nosniff</span></span>

<span data-ttu-id="13122-154">日期：星期三，28五月 2014 19:22:19 GMT</span><span class="sxs-lookup"><span data-stu-id="13122-154">Date : Wed, 28 May 2014 19:22:19 GMT</span></span>

<span data-ttu-id="13122-155">内容长度：6305</span><span class="sxs-lookup"><span data-stu-id="13122-155">Content-Length : 6305</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="13122-156">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="13122-156">Reasons why the test might have failed</span></span>

<span data-ttu-id="13122-157">如果 Test-CsMcxConference 失败，应首先验证移动服务是否正在运行且可访问。</span><span class="sxs-lookup"><span data-stu-id="13122-157">If Test-CsMcxConference fails you should begin by verifying that the mobility service is running and can be accessed.</span></span> <span data-ttu-id="13122-158">可通过使用 web 浏览器验证是否可以访问 Lync Server 池的移动服务 URL 来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="13122-158">That can be done by using a web browser to verify that the mobility service URL for your Lync Server pool can be accessed.</span></span> <span data-ttu-id="13122-159">例如，此命令将验证 pool atl-cs-001.litwareinc.com 的 URL：</span><span class="sxs-lookup"><span data-stu-id="13122-159">For example, this command verifies the URL for the pool atl-cs-001.litwareinc.com:</span></span>

`https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc`

<span data-ttu-id="13122-160">如果可以访问移动服务，则应验证测试用户是否具有有效的 Lync 服务器帐户。</span><span class="sxs-lookup"><span data-stu-id="13122-160">If the mobility service can be accessed you should then verify that your test users have valid Lync Server accounts.</span></span> <span data-ttu-id="13122-161">你可以使用类似下面的命令检索帐户信息：</span><span class="sxs-lookup"><span data-stu-id="13122-161">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="13122-162">如果 Enabled 属性不等于 True 或命令失败，则意味着用户没有有效的 Lync 服务器帐户。你还应验证每个用户帐户是否已启用移动。</span><span class="sxs-lookup"><span data-stu-id="13122-162">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.You should also verify that each user account is enabled for mobility.</span></span> <span data-ttu-id="13122-163">若要执行此操作，请首先确定分配给该帐户的移动策略：</span><span class="sxs-lookup"><span data-stu-id="13122-163">To do that, first determine the mobility policy that is assigned to the account:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

<span data-ttu-id="13122-164">了解策略名称后，请使用 Get-CsMobilityPolicy cmdlet 验证有问题的策略 (例如，RedmondMobilityPolicy) 将 EnableMobility 属性设置为 True：</span><span class="sxs-lookup"><span data-stu-id="13122-164">After you know the policy name, use the Get-CsMobilityPolicy cmdlet to verify that the policy in question (for example, RedmondMobilityPolicy) has the EnableMobility property set to True:</span></span>

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

<span data-ttu-id="13122-165">如果你在运行 Test-CsMcxConference 时收到 "身份验证头" 错误消息，这通常意味着你未指定有效的用户帐户，请验证用户名和密码，然后再次尝试测试。</span><span class="sxs-lookup"><span data-stu-id="13122-165">If you receive an “authentication header” error message when you run Test-CsMcxConference that often means that you have not specified a valid user account, Verify the user name and password and then try the test again.</span></span> <span data-ttu-id="13122-166">如果您确信用户帐户有效，请使用 Get-CsWebServiceConfiguration cmdlet 并检查 UseWindowsAuth 属性的值。</span><span class="sxs-lookup"><span data-stu-id="13122-166">If you are convinced that the user account is valid, then use the Get-CsWebServiceConfiguration cmdlet and check the value of the UseWindowsAuth property.</span></span> <span data-ttu-id="13122-167">这将告诉你在你的组织中启用了哪些身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="13122-167">That will tell you which authentication methods are enabled in your organization.</span></span>

<span data-ttu-id="13122-168">有关如何解决移动服务问题的更多提示，请参阅分步 [解决外部 Lync 移动性连接问题](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx)的博客文章。</span><span class="sxs-lookup"><span data-stu-id="13122-168">For more tips about how to troubleshoot the mobility service, see the blog post [Troubleshooting External Lync Mobility Connectivity Issues Step-by-Step](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span></span>

<span data-ttu-id="13122-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13122-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

