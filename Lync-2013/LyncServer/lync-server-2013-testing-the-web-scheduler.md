---
title: Lync Server 2013：测试 Web 计划程序
description: Lync Server 2013：测试 Web 计划程序。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the Web scheduler
ms:assetid: 58e34058-1afa-42e3-9096-c4ea1954c237
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727304(v=OCS.15)
ms:contentKeyID: 63969603
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6512bf074078005eac66d1e4f5cd3d8ba2dc4bc7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439721"
---
# <a name="testing-the-web-scheduler-in-lync-server-2013"></a><span data-ttu-id="98a05-103">在 Lync Server 2013 中测试 Web 计划程序</span><span class="sxs-lookup"><span data-stu-id="98a05-103">Testing the Web scheduler in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98a05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98a05-104">

<span> </span></span></span>

<span data-ttu-id="98a05-105">_**主题上次修改时间：** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="98a05-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98a05-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="98a05-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="98a05-107">每天</span><span class="sxs-lookup"><span data-stu-id="98a05-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a05-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="98a05-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="98a05-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="98a05-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a05-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="98a05-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="98a05-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="98a05-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="98a05-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 <strong>CsWebScheduler</strong> cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="98a05-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWebScheduler</strong> cmdlet.</span></span> <span data-ttu-id="98a05-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="98a05-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebScheduler&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="98a05-114">说明</span><span class="sxs-lookup"><span data-stu-id="98a05-114">Description</span></span>

<span data-ttu-id="98a05-115">**CsWebScheduler** cmdlet 使你能够确定特定用户是否可以使用 Web 计划程序安排会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-115">The **Test-CsWebScheduler** cmdlet enables you to determine whether a specific user can schedule a meeting using the Web Scheduler.</span></span> <span data-ttu-id="98a05-116">Web 计划程序允许未运行 Outlook 的用户安排联机会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-116">The Web Scheduler enables users who are not running Outlook to schedule online meetings.</span></span> <span data-ttu-id="98a05-117">在其他内容中，此新功能 (，它包含在 Microsoft Lync Server 2010 资源工具包中随附的 Web 计划程序工具中的功能，) 使用户能够：</span><span class="sxs-lookup"><span data-stu-id="98a05-117">Among other things, this new feature (which incorporates the functionality found in the Web Scheduler tool that was included with the Microsoft Lync Server 2010 resource kit) enables users to:</span></span>

  - <span data-ttu-id="98a05-118">安排新的联机会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-118">Schedule a new online meeting.</span></span>

  - <span data-ttu-id="98a05-119">列出他或她安排的所有会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-119">List all meetings that he or she has scheduled.</span></span>

  - <span data-ttu-id="98a05-120">查看/修改现有会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-120">View/modify an existing meeting.</span></span>

  - <span data-ttu-id="98a05-121">删除现有会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-121">Delete an existing meeting.</span></span>

  - <span data-ttu-id="98a05-122">使用预配置的 SMTP 邮件服务器向会议参与者发送电子邮件邀请。</span><span class="sxs-lookup"><span data-stu-id="98a05-122">Send an email invitation to meeting participants by using a preconfigured SMTP mail server.</span></span>

  - <span data-ttu-id="98a05-123">加入现有会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-123">Join an existing conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="98a05-124">运行测试</span><span class="sxs-lookup"><span data-stu-id="98a05-124">Running the test</span></span>

<span data-ttu-id="98a05-125">以下示例验证 pool atl-cs-001.litwareinc.com 的 Web 计划程序。</span><span class="sxs-lookup"><span data-stu-id="98a05-125">The following example verifies the Web Scheduler for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="98a05-126">仅当为池 atl-cs-001.litwareinc.com 定义了测试用户时，此命令才会运行。</span><span class="sxs-lookup"><span data-stu-id="98a05-126">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="98a05-127">如果有，则该命令将确定第一个测试用户是否可以使用 Web 计划程序安排联机会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-127">If they have, then the command will determine whether the first test user can schedule an online meeting using the Web Scheduler.</span></span>

<span data-ttu-id="98a05-128">如果未定义测试用户，则该命令将失败，因为它不会知道哪个用户登录。</span><span class="sxs-lookup"><span data-stu-id="98a05-128">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="98a05-129">如果尚未为池定义测试用户，则必须在尝试登录时包含该命令应使用的 UserSipAddress 参数和用户凭据。</span><span class="sxs-lookup"><span data-stu-id="98a05-129">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user the command should use when trying to log on.</span></span>

    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="98a05-130">下一个示例中所示的命令将测试特定用户 (litwareinc \\ kenmeyer) 的功能，以使用 Web 计划程序安排联机会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-130">The commands shown in the next example test the ability of a specific user (litwareinc\\kenmeyer) to schedule an online meeting using the Web scheduler.</span></span> <span data-ttu-id="98a05-131">若要执行此操作，示例中的第一个命令使用了 **Get 凭据** Cmdlet 创建 Windows PowerShell 命令行界面凭据对象，该对象包含用户 Ken Meyer 的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="98a05-131">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Ken Meyer.</span></span> <span data-ttu-id="98a05-132"> (由于登录名 litwareinc \\ kenmeyer 作为参数包含，因此 "Windows PowerShell 凭据请求" 对话框仅要求管理员输入 Ken Meyer 帐户的密码。 ) 结果凭据对象将存储在名为 $cred 1 的变量中。</span><span class="sxs-lookup"><span data-stu-id="98a05-132">(Because the logon name litwareinc\\kenmeyer is included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Ken Meyer account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="98a05-133">然后，第二个命令将检查此用户是否可以登录到 pool atl-cs-001.litwareinc.com 和安排联机会议。</span><span class="sxs-lookup"><span data-stu-id="98a05-133">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and schedule an online meeting.</span></span> <span data-ttu-id="98a05-134">若要运行此任务， **CsWebScheduler** cmdlet 将与三个参数一起调用： TargetFqdn (注册机构池的 FQDN) ;UserCredential (包含 Pilar Ackerman 的用户凭据的 Windows PowerShell 对象) ;和 UserSipAddress (与提供的用户凭据) 对应的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="98a05-134">To run this task, the **Test-CsWebScheduler** cmdlet is called, together with three parameters: TargetFqdn (the FQDN of the Registrar pool); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebScheduler -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="98a05-135">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="98a05-135">Determining success or failure</span></span>

<span data-ttu-id="98a05-136">如果正确配置了 web 计划程序，则会收到类似于此的输出，结果属性标记为 " **成功**"：</span><span class="sxs-lookup"><span data-stu-id="98a05-136">If the web scheduler is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="98a05-137">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="98a05-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="98a05-138">目标 Uri： https://atl-cs-001.litwareinc.com。</span><span class="sxs-lookup"><span data-stu-id="98a05-138">Target Uri : https:// atl-cs-001.litwareinc.com.</span></span>

<span data-ttu-id="98a05-139">litwareinc.com:443/Scheduler</span><span class="sxs-lookup"><span data-stu-id="98a05-139">litwareinc.com:443/Scheduler</span></span>

<span data-ttu-id="98a05-140">结果：成功</span><span class="sxs-lookup"><span data-stu-id="98a05-140">Result : Success</span></span>

<span data-ttu-id="98a05-141">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="98a05-141">Latency : 00:00:00</span></span>

<span data-ttu-id="98a05-142">错误消息：</span><span class="sxs-lookup"><span data-stu-id="98a05-142">Error Message :</span></span>

<span data-ttu-id="98a05-143">自检</span><span class="sxs-lookup"><span data-stu-id="98a05-143">Diagnosis :</span></span>

<span data-ttu-id="98a05-144">如果 web 计划程序配置不正确，则结果将显示为 " **失败**"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="98a05-144">If the web scheduler is not configured correctly, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="98a05-145">警告：无法读取给定的完全限定的注册机构端口号</span><span class="sxs-lookup"><span data-stu-id="98a05-145">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="98a05-146"> (FQDN) 的域名。</span><span class="sxs-lookup"><span data-stu-id="98a05-146">domain name (FQDN).</span></span> <span data-ttu-id="98a05-147">使用默认注册器端口号。</span><span class="sxs-lookup"><span data-stu-id="98a05-147">Using default Registrar port number.</span></span> <span data-ttu-id="98a05-148">除了</span><span class="sxs-lookup"><span data-stu-id="98a05-148">Exception:</span></span>

<span data-ttu-id="98a05-149">InvalidOperationException：在拓扑中找不到匹配的群集。</span><span class="sxs-lookup"><span data-stu-id="98a05-149">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="98a05-150">看</span><span class="sxs-lookup"><span data-stu-id="98a05-150">at</span></span>

<span data-ttu-id="98a05-151">SipSyntheticTransaction. TryRetri 的 SyntheticTransactions</span><span class="sxs-lookup"><span data-stu-id="98a05-151">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="98a05-152">eveRegistrarPortFromTopology (Int32& registrarPortNumber) </span><span class="sxs-lookup"><span data-stu-id="98a05-152">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="98a05-153">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="98a05-153">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="98a05-154">目标 Uri：</span><span class="sxs-lookup"><span data-stu-id="98a05-154">Target Uri :</span></span>

<span data-ttu-id="98a05-155">结果：失败</span><span class="sxs-lookup"><span data-stu-id="98a05-155">Result : Failure</span></span>

<span data-ttu-id="98a05-156">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="98a05-156">Latency : 00:00:00</span></span>

<span data-ttu-id="98a05-157">错误消息：在拓扑中找不到匹配的群集。</span><span class="sxs-lookup"><span data-stu-id="98a05-157">Error Message : No matching cluster found in topology.</span></span>

<span data-ttu-id="98a05-158">自检</span><span class="sxs-lookup"><span data-stu-id="98a05-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="98a05-159">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="98a05-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="98a05-160">下面是 **测试 CsWebScheduler** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="98a05-160">Here are some common reasons why **Test-CsWebScheduler** might fail:</span></span>

  - <span data-ttu-id="98a05-161">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="98a05-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="98a05-162">如果使用，则必须正确配置可选参数，否则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="98a05-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="98a05-163">重新运行不带可选参数的命令，并查看是否成功。</span><span class="sxs-lookup"><span data-stu-id="98a05-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="98a05-164">如果 Web 计划程序配置错误或尚未部署，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="98a05-164">This command will fail if the Web Scheduler is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="98a05-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98a05-165">See Also</span></span>


[<span data-ttu-id="98a05-166">Set-CsWebServer</span><span class="sxs-lookup"><span data-stu-id="98a05-166">Set-CsWebServer</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServer)  
  

<span data-ttu-id="98a05-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98a05-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

