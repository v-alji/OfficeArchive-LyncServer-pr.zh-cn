---
title: Lync Server 2013：测试位置策略
description: Lync Server 2013：测试位置策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing location policy
ms:assetid: 23d06fd3-31ee-4480-ba1e-d179a55b8b14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690127(v=OCS.15)
ms:contentKeyID: 63969591
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4efc7ac6f3beef875ce1496b19b875ff252b145b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392087"
---
# <a name="testing-location-policy-in-lync-server-2013"></a><span data-ttu-id="b2246-103">在 Lync Server 2013 中测试位置策略</span><span class="sxs-lookup"><span data-stu-id="b2246-103">Testing location policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2246-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2246-104">

<span> </span></span></span>

<span data-ttu-id="b2246-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="b2246-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2246-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="b2246-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b2246-107">每天</span><span class="sxs-lookup"><span data-stu-id="b2246-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2246-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="b2246-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b2246-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2246-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2246-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="b2246-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b2246-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="b2246-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b2246-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsLocationPolicy cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="b2246-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsLocationPolicy cmdlet.</span></span> <span data-ttu-id="b2246-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="b2246-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLocationPolicy&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b2246-114">说明</span><span class="sxs-lookup"><span data-stu-id="b2246-114">Description</span></span>

<span data-ttu-id="b2246-115">Test-CsLocationPolicy cmdlet 验证是否已向用户分配了位置策略。</span><span class="sxs-lookup"><span data-stu-id="b2246-115">The Test-CsLocationPolicy cmdlet verifies that a location policy is assigned to a user.</span></span> <span data-ttu-id="b2246-116">位置策略用于应用与 E9-1-1 功能和客户端位置相关的设置。</span><span class="sxs-lookup"><span data-stu-id="b2246-116">The location policy is used to apply settings that relate to E9-1-1 functionality and client location.</span></span> <span data-ttu-id="b2246-117">位置策略确定用户是否已启用 E9-1，如果答案是 "是"，则是紧急呼叫的行为。</span><span class="sxs-lookup"><span data-stu-id="b2246-117">The location policy determines whether a user is enabled for E9-1-1, and, if the answer is "yes,", what the behavior is of an emergency call.</span></span> <span data-ttu-id="b2246-118">例如，你可以使用位置策略来定义在美国) 中 (911 的紧急电话、是否应自动通知企业安全以及如何路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="b2246-118">For example, you can use the location policy to define what number makes up an emergency call (911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="b2246-119">你可以测试用户或网络子网上的位置策略。</span><span class="sxs-lookup"><span data-stu-id="b2246-119">You can test location policies on users or on network subnets.</span></span> <span data-ttu-id="b2246-120">如果针对子网 () 指定子网参数的值来运行测试，则 cmdlet 将尝试解析该子网的位置策略。</span><span class="sxs-lookup"><span data-stu-id="b2246-120">If you run the test against a subnet (by specifying a value for the Subnet parameter), the cmdlet will attempt to resolve the location policy for that subnet.</span></span> <span data-ttu-id="b2246-121">如果未向子网分配位置策略，将检索已配置用户的位置策略。</span><span class="sxs-lookup"><span data-stu-id="b2246-121">If no location policy is assigned to the subnet, the location policy for the configured user will be retrieved.</span></span> <span data-ttu-id="b2246-122">如果成功检索子网策略，则输出将包括以子网 tagid 开头的 LocationPolicyTagID 值。</span><span class="sxs-lookup"><span data-stu-id="b2246-122">If the subnet policy is retrieved successfully, the output will include a LocationPolicyTagID value that begins with subnet-tagid.</span></span> <span data-ttu-id="b2246-123">如果找不到子网的位置策略，LocationPolicyTagID 将以用户 tagid 开头。</span><span class="sxs-lookup"><span data-stu-id="b2246-123">If a location policy for the subnet was not found, the LocationPolicyTagID will begin with user-tagid.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b2246-124">运行测试</span><span class="sxs-lookup"><span data-stu-id="b2246-124">Running the test</span></span>

<span data-ttu-id="b2246-125">可以使用预配置的测试帐户运行 Test-CsLocationPolicy cmdlet (请参阅设置用于运行 Lync Server 测试的测试帐户) 或为 Lync Server 启用的任何用户的帐户。</span><span class="sxs-lookup"><span data-stu-id="b2246-125">The Test-CsLocationPolicy cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="b2246-126">若要使用测试帐户运行此检查，只需指定正在测试的 Lync Server 池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b2246-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="b2246-127">例如：</span><span class="sxs-lookup"><span data-stu-id="b2246-127">For example:</span></span>

    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="b2246-128">若要使用实际用户帐户运行此检查，必须首先创建一个包含帐户名称和密码的 Windows PowerShell 凭据对象。</span><span class="sxs-lookup"><span data-stu-id="b2246-128">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="b2246-129">然后，在调用 Test-CsLocationPolicy 时，必须包含该凭据对象和分配给该帐户的 SIP 地址：</span><span class="sxs-lookup"><span data-stu-id="b2246-129">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsLocationPolicy:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="b2246-130">有关详细信息，请参阅 [CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Test-CsLocationPolicy) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="b2246-130">For more information, see the Help documentation for the [Test-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Test-CsLocationPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b2246-131">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="b2246-131">Determining success or failure</span></span>

<span data-ttu-id="b2246-132">如果指定用户具有有效的位置策略，则会收到与此类似的输出，结果属性标记为 **成功：**</span><span class="sxs-lookup"><span data-stu-id="b2246-132">If the specified user has a valid location policy, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="b2246-133">EnhancedEmergencyServicesEnabled： true</span><span class="sxs-lookup"><span data-stu-id="b2246-133">EnhancedEmergencyServicesEnabled : true</span></span>

<span data-ttu-id="b2246-134">LocationPolicyTagID：用户-tagid</span><span class="sxs-lookup"><span data-stu-id="b2246-134">LocationPolicyTagID : user-tagid</span></span>

<span data-ttu-id="b2246-135">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2246-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b2246-136">结果：成功</span><span class="sxs-lookup"><span data-stu-id="b2246-136">Result : Success</span></span>

<span data-ttu-id="b2246-137">延迟：00：00：06.8630376</span><span class="sxs-lookup"><span data-stu-id="b2246-137">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="b2246-138">时发生</span><span class="sxs-lookup"><span data-stu-id="b2246-138">Error :</span></span>

<span data-ttu-id="b2246-139">自检</span><span class="sxs-lookup"><span data-stu-id="b2246-139">Diagnosis :</span></span>

<span data-ttu-id="b2246-140">如果找不到指定用户的有效位置策略，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="b2246-140">If a valid location policy cannot be found for the specified user, then Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="b2246-141">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2246-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b2246-142">结果：失败</span><span class="sxs-lookup"><span data-stu-id="b2246-142">Result : Failure</span></span>

<span data-ttu-id="b2246-143">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="b2246-143">Latency : 00:00:00</span></span>

<span data-ttu-id="b2246-144">错误：404，未找到</span><span class="sxs-lookup"><span data-stu-id="b2246-144">Error : 404, Not Found</span></span>

<span data-ttu-id="b2246-145">诊断： ErrorCode = 4005，Source = atl-cs-001.litwareinc.com，</span><span class="sxs-lookup"><span data-stu-id="b2246-145">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="b2246-146">原因 = 没有为 SIP 启用目标 URI，或者没有为其启用目标 URI</span><span class="sxs-lookup"><span data-stu-id="b2246-146">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="b2246-147">并存.</span><span class="sxs-lookup"><span data-stu-id="b2246-147">exist.</span></span>

<span data-ttu-id="b2246-148">Microsoft DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="b2246-148">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="b2246-149">以前的输出表明由于指定用户无效而导致测试失败：帐户不存在或尚未为 Lync Server 启用用户。</span><span class="sxs-lookup"><span data-stu-id="b2246-149">The previous output states that the test failed because the specified user is not valid: either the account does not exist or the user has not been enabled for Lync Server.</span></span> <span data-ttu-id="b2246-150">你可以验证帐户的有效性，并通过运行如下命令确定是否已为 nm-ocs-14-3 启用该帐户：</span><span class="sxs-lookup"><span data-stu-id="b2246-150">You can verify the validity of an account, and determine whether or not that account has been enabled for nm-ocs-14-3rd, by running a command similar to this:</span></span>

    Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="b2246-151">如果 Test-CsLocationPolicy 失败，则可能需要重新运行测试，这一次包括 Verbose 参数：</span><span class="sxs-lookup"><span data-stu-id="b2246-151">If Test-CsLocationPolicy fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsLocationPolicy -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="b2246-152">包括详细参数时，Test-CsLocationPolicy 将返回它在验证位置策略时尝试的每个操作的分步帐户。</span><span class="sxs-lookup"><span data-stu-id="b2246-152">When the Verbose parameter is included, Test-CsLocationPolicy will return a step-by-step account of each action it tried when verifying the location policy.</span></span> <span data-ttu-id="b2246-153">例如，此输出表明 Lync Server 无法登录测试用户，可能是因为提供了无效密码：</span><span class="sxs-lookup"><span data-stu-id="b2246-153">For example, this output indicates that Lync Server couldn't log on the test user, probably because an invalid password was supplied:</span></span>

<span data-ttu-id="b2246-154">正在发送注册请求：</span><span class="sxs-lookup"><span data-stu-id="b2246-154">Sending Registration request :</span></span>

<span data-ttu-id="b2246-155">目标 Fqdn = atl-cs-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2246-155">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="b2246-156">用户 Sip 地址 = sip:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b2246-156">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="b2246-157">注册机构端口 = 5061</span><span class="sxs-lookup"><span data-stu-id="b2246-157">Registrar Port = 5061</span></span>

<span data-ttu-id="b2246-158">已选择身份验证类型 "IWA"。</span><span class="sxs-lookup"><span data-stu-id="b2246-158">Auth Type 'IWA' is selected.</span></span>

<span data-ttu-id="b2246-159">对 sip/atl-cs-001 的注册命中率 litwareinc</span><span class="sxs-lookup"><span data-stu-id="b2246-159">Registration hit against sip/atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b2246-160">"Register" 活动在 "0.0601795" 秒内完成。</span><span class="sxs-lookup"><span data-stu-id="b2246-160">'Register' activity completed in '0.0601795' secs.</span></span>

<span data-ttu-id="b2246-161">"登录被拒绝" 异常。</span><span class="sxs-lookup"><span data-stu-id="b2246-161">An exception 'The log on was denied.</span></span> <span data-ttu-id="b2246-162">检查使用的凭据是否正确，帐户是否处于活动状态。 '</span><span class="sxs-lookup"><span data-stu-id="b2246-162">Check that the correct credentials are being used and the account is active.'</span></span> <span data-ttu-id="b2246-163">在工作流期间发生。</span><span class="sxs-lookup"><span data-stu-id="b2246-163">occurred during the Workflow.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b2246-164">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="b2246-164">Reasons why the test might have failed</span></span>

<span data-ttu-id="b2246-165">下面是 Test-CsLocationPolicy 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="b2246-165">Here are some common reasons why Test-CsLocationPolicy might fail:</span></span>

  - <span data-ttu-id="b2246-166">您指定的用户帐户无效。</span><span class="sxs-lookup"><span data-stu-id="b2246-166">You specified a user account that is not valid.</span></span> <span data-ttu-id="b2246-167">你可以通过运行类似如下所示的命令来验证用户帐户是否存在：</span><span class="sxs-lookup"><span data-stu-id="b2246-167">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="b2246-168">用户帐户有效，但当前没有为 Lync Server 启用该帐户。</span><span class="sxs-lookup"><span data-stu-id="b2246-168">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="b2246-169">若要验证是否已启用 Lync Server 的用户帐户，请运行类似如下的命令：</span><span class="sxs-lookup"><span data-stu-id="b2246-169">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="b2246-170">如果 Enabled 属性设置为 False，则表示当前未对 Lync Server 启用用户。</span><span class="sxs-lookup"><span data-stu-id="b2246-170">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="b2246-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2246-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

