---
title: Lync Server 2013：测试将推送通知发送到智能手机
description: Lync Server 2013：测试将推送通知发送到智能电话。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test push notifications to smart phones
ms:assetid: 8f5ca7d1-1ccb-4cb0-b417-730559e79b6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767948(v=OCS.15)
ms:contentKeyID: 63969626
ms.date: 03/15/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b92ef444a5331c9a673fd2db506631554e96eea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441226"
---
# <a name="test-push-notifications-to-smart-phones-in-lync-server-2013"></a><span data-ttu-id="2de92-103">在 Lync Server 2013 中测试指向智能电话的推送通知</span><span class="sxs-lookup"><span data-stu-id="2de92-103">Test push notifications to smart phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2de92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2de92-104">

<span> </span></span></span>

<span data-ttu-id="2de92-105">_**主题上次修改时间：** 2017-03-15_</span><span class="sxs-lookup"><span data-stu-id="2de92-105">_**Topic Last Modified:** 2017-03-15_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2de92-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="2de92-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="2de92-107">每月</span><span class="sxs-lookup"><span data-stu-id="2de92-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de92-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="2de92-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="2de92-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2de92-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de92-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="2de92-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="2de92-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="2de92-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="2de92-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsMcxPushNotification cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="2de92-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="2de92-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="2de92-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxPushNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="2de92-114">说明</span><span class="sxs-lookup"><span data-stu-id="2de92-114">Description</span></span>

<span data-ttu-id="2de92-115">推送通知服务 (Apple 推送通知服务和 Microsoft 推送通知服务) 可以向移动设备（如 Iphone 和 Windows 电话）发送有关事件（如新的即时消息或新语音邮件）的通知，即使这些设备上的 Lync 客户端当前已暂停或在后台运行也是如此。</span><span class="sxs-lookup"><span data-stu-id="2de92-115">The push notification service (Apple Push Notification Service and Microsoft Push Notification Service) can send notifications about events such as new instant messages or new voice mail to mobile devices such as iPhones and Windows Phones, even if the Lync client on those devices is currently suspended or running in the background.</span></span> <span data-ttu-id="2de92-116">推送通知服务是在 Microsoft 服务器上运行的基于云的服务。</span><span class="sxs-lookup"><span data-stu-id="2de92-116">The push notification service is a cloud-based service that is running on Microsoft servers.</span></span> <span data-ttu-id="2de92-117">为了利用推送通知，你必须能够连接到推送通知交换所并进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="2de92-117">In order to take advantage of push notifications, you must be able to connect to, and be authenticated by, the push notification clearinghouse.</span></span> <span data-ttu-id="2de92-118">Test-CsMcxPushNotification cmdlet 使管理员能够验证推送通知请求是否可以通过 Edge 服务器路由到推送通知交换所。</span><span class="sxs-lookup"><span data-stu-id="2de92-118">The Test-CsMcxPushNotification cmdlet enables administrators to verify that push notification requests can be routed through your Edge server to the push notification clearinghouse.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="2de92-119">运行测试</span><span class="sxs-lookup"><span data-stu-id="2de92-119">Running the test</span></span>

<span data-ttu-id="2de92-120">若要测试推送通知服务，请调用 Test-CsMcxPushNotification cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2de92-120">To test the push notification service, call the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="2de92-121">请确保指定 Edge 服务器的完全限定的域名：</span><span class="sxs-lookup"><span data-stu-id="2de92-121">Make sure that you specify the fully qualified domain name of your Edge server:</span></span>

    Test-CsMcxPushNotification -AccessEdgeFqdn "atl-edge-001.litwareinc.com"

<span data-ttu-id="2de92-122">有关详细信息，请参阅 [CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="2de92-122">For more information, see the help topic for the [Test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="2de92-123">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="2de92-123">Determining success or failure</span></span>

<span data-ttu-id="2de92-124">如果 Test-CsMcxPushNotification 成功，cmdlet 将返回测试结果成功：</span><span class="sxs-lookup"><span data-stu-id="2de92-124">If Test-CsMcxPushNotification succeeds the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="2de92-125">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="2de92-125">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="2de92-126">结果：成功</span><span class="sxs-lookup"><span data-stu-id="2de92-126">Result : Success</span></span>

<span data-ttu-id="2de92-127">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="2de92-127">Latency : 00:00:00</span></span>

<span data-ttu-id="2de92-128">时发生</span><span class="sxs-lookup"><span data-stu-id="2de92-128">Error :</span></span>

<span data-ttu-id="2de92-129">自检</span><span class="sxs-lookup"><span data-stu-id="2de92-129">Diagnosis :</span></span>

<span data-ttu-id="2de92-130">如果 Test-CsMcxPushNotification 无法连接到推送通知交换所，则 cmdlet 通常不会返回失败的测试结果。</span><span class="sxs-lookup"><span data-stu-id="2de92-130">If Test-CsMcxPushNotification is unable to connect to the push notification clearinghouse the cmdlet will typically not return a test result of Failure.</span></span> <span data-ttu-id="2de92-131">相反，此命令通常完全失败。</span><span class="sxs-lookup"><span data-stu-id="2de92-131">Instead the command will usually fail completely.</span></span> <span data-ttu-id="2de92-132">例如：</span><span class="sxs-lookup"><span data-stu-id="2de92-132">For example:</span></span>

<span data-ttu-id="2de92-133">Test-CsMcxPushNotification：从网络收到 504 (服务器超时) 响应，操作失败。</span><span class="sxs-lookup"><span data-stu-id="2de92-133">Test-CsMcxPushNotification : A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="2de92-134">有关详细信息，请参阅异常详细信息。</span><span class="sxs-lookup"><span data-stu-id="2de92-134">See the exception details for more information.</span></span>

<span data-ttu-id="2de92-135">在第一行：1个字符：27</span><span class="sxs-lookup"><span data-stu-id="2de92-135">At line:1 char:27</span></span>

<span data-ttu-id="2de92-136">\+Test-CsMcxPushNotification \< \< \< \< AccessEdgeFqdn lyncedge.mydomain.com</span><span class="sxs-lookup"><span data-stu-id="2de92-136">\+ Test-CsMcxPushNotification \<\<\<\< -AccessEdgeFqdn lyncedge.mydomain.com</span></span>

<span data-ttu-id="2de92-137">\+ CategoryInfo： OperationStopped： (： ) \[ Test-CsMcxPushNotification \] 、FailureResponseException</span><span class="sxs-lookup"><span data-stu-id="2de92-137">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], FailureResponseException</span></span>

<span data-ttu-id="2de92-138">\+ FullyQualifiedErrorId： WorkflowNotCompleted、SyntheticTransactions TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="2de92-138">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="2de92-139">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="2de92-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="2de92-140">如果推送通知服务失败通常表示与边缘服务器通信的问题，或者与推送通知交换所进行通信的问题。</span><span class="sxs-lookup"><span data-stu-id="2de92-140">If the push notification service fails that usually indicates either problems communicating with your Edge server, or problems communicating with the Push Notification Clearing House.</span></span> <span data-ttu-id="2de92-141">如果在运行 Test CsMcxPushNotification 时遇到问题，您应执行的第一件事是验证边缘服务器是否正常工作。</span><span class="sxs-lookup"><span data-stu-id="2de92-141">If you encounter problems when you run Test-CsMcxPushNotification, the first thing that you should do is verify that your Edge server is working correctly.</span></span> <span data-ttu-id="2de92-142">执行此操作的一种方法是使用 Test-CsAVEdgeConnectivity cmdlet：</span><span class="sxs-lookup"><span data-stu-id="2de92-142">One way to do that is to use the Test-CsAVEdgeConnectivity cmdlet:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsAVEdgeConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="2de92-143">此检查将验证指定用户是否可以连接到边缘服务器。</span><span class="sxs-lookup"><span data-stu-id="2de92-143">This check verifies that a specified user can connect to the Edge server.</span></span>

<span data-ttu-id="2de92-144">如果边缘服务器似乎正常工作，则这通常意味着你无法连接到推送通知 clearinghouse。</span><span class="sxs-lookup"><span data-stu-id="2de92-144">If the Edge server seems to be working correctly, that often means that you are unable to connect to the push notification clearinghouse.</span></span> <span data-ttu-id="2de92-145">反过来，这通常意味着你未正确配置 clearinghouse URI 或你没有指向此 URL 的 DNS SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="2de92-145">In turn, that typically means that you either have not configured the clearinghouse URI correctly or that you do not have a DNS SRV record that points to this URL.</span></span> <span data-ttu-id="2de92-146">你可以通过运行以下命令来验证 URI 是否已设置为正确的值 (sip:push@push.lync.com) ：</span><span class="sxs-lookup"><span data-stu-id="2de92-146">You can verify that the URI is set to the correct value (sip:push@push.lync.com) by running this command:</span></span>

    Get-CsMcxConfiguration

<span data-ttu-id="2de92-147">如果 PushNotificationProxyUri 属性设置为 sip:push@push.lync.com 以外的任何其他内容，则可以使用 Set-McxConfiguration cmdlet 更正该问题。</span><span class="sxs-lookup"><span data-stu-id="2de92-147">If the PushNotificationProxyUri property is set to anything other than sip:push@push.lync.com then you can correct that problem by using the Set-McxConfiguration cmdlet.</span></span> <span data-ttu-id="2de92-148">例如，此命令在整个组织中正确设置 URI：</span><span class="sxs-lookup"><span data-stu-id="2de92-148">For example, this command correctly sets the URI throughout your organization:</span></span>

    Get-CsMcxConfiguration | Set-CsMcxConfiguration -PushNotificationProxyUri "sip:push@push.lync.com"

<span data-ttu-id="2de92-149">有关详细信息，请参阅 [CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="2de92-149">For more information, see the help topic for the [Set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) cmdlet.</span></span>

<span data-ttu-id="2de92-150">如果 URI 配置正确，则下一步应该是验证你是否具有解析为 SIP 域和边缘服务器的 DNS SRV 记录。</span><span class="sxs-lookup"><span data-stu-id="2de92-150">If the URI is configured correctly, your next step should be to verify that you have a DNS SRV record that resolves to your SIP domain and your Edge server.</span></span> <span data-ttu-id="2de92-151">有关如何配置这些记录的详细信息，请参阅移动性的帮助主题 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="2de92-151">For more information about how to configure these records, see the help topic DNS Requirements for Mobility.</span></span> <span data-ttu-id="2de92-152">请注意，以下错误消息通常表示 DNS 记录的问题：</span><span class="sxs-lookup"><span data-stu-id="2de92-152">Note that the following error message usually indicates a problem with DNS records:</span></span>

<span data-ttu-id="2de92-153">从网络收到 504 (服务器超时) 响应，操作失败。</span><span class="sxs-lookup"><span data-stu-id="2de92-153">A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="2de92-154">有关详细信息，请参阅异常详细信息。</span><span class="sxs-lookup"><span data-stu-id="2de92-154">See the exception details for more information.</span></span>

<span data-ttu-id="2de92-155">也可能 Test-CsMcxConfiguration 将失败，并出现以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="2de92-155">It’s also possible that Test-CsMcxConfiguration will fail with this error message:</span></span>

<span data-ttu-id="2de92-156">Test-CsMcxPushNotification：推送通知请求被拒绝。</span><span class="sxs-lookup"><span data-stu-id="2de92-156">Test-CsMcxPushNotification : Push Notification request was rejected.</span></span>

<span data-ttu-id="2de92-157">在第一行：1个字符：27</span><span class="sxs-lookup"><span data-stu-id="2de92-157">At line:1 char:27</span></span>

<span data-ttu-id="2de92-158">\+ Test-CsMcxPushNotification \<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="2de92-158">\+ Test-CsMcxPushNotification \<\<\<\<</span></span>

<span data-ttu-id="2de92-159">\+ CategoryInfo： OperationStopped： (： ) \[ Test-CsMcxPushNotification \] 、SyntheticTransactionException</span><span class="sxs-lookup"><span data-stu-id="2de92-159">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], SyntheticTransactionException</span></span>

<span data-ttu-id="2de92-160">\+ FullyQualifiedErrorId： WorkflowNotCompleted、SyntheticTransactions TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="2de92-160">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

<span data-ttu-id="2de92-161">如果启用了 URL 筛选并阻止了 http：和 https：前缀，则通常会出现 "推送通知请求被拒绝" 消息。</span><span class="sxs-lookup"><span data-stu-id="2de92-161">The “Push notification request was rejected” message typically occurs if you have enabled URL filtering and are blocking the http: and https: prefixes.</span></span> <span data-ttu-id="2de92-162">你可以使用类似如下的命令确定被阻止的前缀：</span><span class="sxs-lookup"><span data-stu-id="2de92-162">You can determine which prefixes are being blocked by using a command similar to the following:</span></span>

```PowerShell 
 (Get-CsImFilterConfiguration -Identity Global).Prefixes
```

<span data-ttu-id="2de92-163">如果结果中显示了 "http：" 或 "https："，则必须将其从 "阻止的前缀" 列表中删除，"推送通知" 才能正常工作。</span><span class="sxs-lookup"><span data-stu-id="2de92-163">If http: or https: appear in the results, you must remove them from the blocked prefix list for push notifications to work.</span></span> <span data-ttu-id="2de92-164">这可以通过使用以下类似命令来实现：</span><span class="sxs-lookup"><span data-stu-id="2de92-164">That can be done by using commands similar to these:</span></span>

    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="http:"}
    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="https:"}

<span data-ttu-id="2de92-165">有关详细信息，请参阅 [CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration)cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="2de92-165">For more information, see the help topic for the [Set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration)cmdlet.</span></span>

<span data-ttu-id="2de92-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2de92-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

