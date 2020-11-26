---
title: Lync Server 2013：测试应用程序共享
description: Lync Server 2013：测试应用程序共享。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing application sharing
ms:assetid: 8d21db9b-10d1-4b43-b057-0deb1df1c205
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727310(v=OCS.15)
ms:contentKeyID: 63969629
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f857908e374239b4054985b88951cd12720ed418
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441072"
---
# <a name="testing-application-sharing-in-lync-server-2013"></a><span data-ttu-id="8e0eb-103">在 Lync Server 2013 中测试应用程序共享</span><span class="sxs-lookup"><span data-stu-id="8e0eb-103">Testing application sharing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e0eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e0eb-104">

<span> </span></span></span>

<span data-ttu-id="8e0eb-105">_**主题上次修改时间：** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="8e0eb-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e0eb-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="8e0eb-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="8e0eb-107">每天</span><span class="sxs-lookup"><span data-stu-id="8e0eb-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e0eb-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="8e0eb-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="8e0eb-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8e0eb-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e0eb-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="8e0eb-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="8e0eb-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="8e0eb-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsASConference cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsASConference cmdlet.</span></span> <span data-ttu-id="8e0eb-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="8e0eb-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsASConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="8e0eb-114">说明</span><span class="sxs-lookup"><span data-stu-id="8e0eb-114">Description</span></span>

<span data-ttu-id="8e0eb-115">**CsASConference** cmdlet 验证一对测试用户是否可以参与包括应用程序共享的联机会议。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-115">The **Test-CsASConference** cmdlet verifies that a pair of test users can participate in an online conference that includes application sharing.</span></span> <span data-ttu-id="8e0eb-116">为此，cmdlet 向 Lync Server 2013 注册两个用户，然后使用其中一个用户帐户创建包括应用程序共享的新会议。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-116">To do this, the cmdlet registers the two users with Lync Server 2013, and then it uses one of the user accounts to create a new conference that includes applications sharing.</span></span> <span data-ttu-id="8e0eb-117">然后，cmdlet 验证第二个用户是否可以加入该会议。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-117">The cmdlet then verifies that the second user is able to join that conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="8e0eb-118">运行测试</span><span class="sxs-lookup"><span data-stu-id="8e0eb-118">Running the test</span></span>

<span data-ttu-id="8e0eb-119">示例1中所示的命令验证是否可以在 pool atl-cs-001.litwareinc.com 上执行应用程序共享会议。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-119">The command shown in Example 1 verifies that an Application Sharing conference can be conducted on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="8e0eb-120">此命令假设你为指定的池配置了一对测试用户。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-120">This command assumes that you have configured a pair of test users for the specified pool.</span></span> <span data-ttu-id="8e0eb-121">如果不存在这样的测试用户，该命令将失败。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-121">If no such test users exist, the command will fail.</span></span>

    Test-CsASConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="8e0eb-122">示例2测试联接启动器服务在池 atl-cs-001.litwareinc.com 上参与应用程序共享会议的能力。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-122">Example 2 tests the ability of the Join Launcher service to participate in an Application Sharing conference on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="8e0eb-123">请注意，此命令仅测试服务本身;您无需任何移动设备即可运行该命令。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-123">Note that this command tests only the service itself; you do not need any mobile devices in order to run the command.</span></span>

    Test-CsASConference -TargetFqdn "atl-cs-001.litwareinc.com" -TestJoinLauncher 

<span data-ttu-id="8e0eb-124">示例2中所示的命令测试一对用户 (litwareinc \\ pilar 和 litwareinc \\ kenmyer) 登录 Lync Server 2013，然后执行应用程序共享会议。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-124">The commands shown in Example 2 test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then conduct an Application Sharing conference.</span></span> <span data-ttu-id="8e0eb-125">为此，示例中的第一个命令使用 Get-Credential cmdlet 创建 Windows PowerShell 命令行界面凭据对象，该对象包含用户 Pilar Ackerman 的名称和密码。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-125">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object containing the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="8e0eb-126"> (由于登录名 litwareinc pilar 已 \\ 包含为参数，因此 "Windows PowerShell 凭据请求" 对话框仅要求管理员输入 Pilar Ackerman 帐户的密码。 ) 结果凭据对象将存储在名为 $cred 1 的变量中。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-126">(Because the logon name, litwareinc\\pilar, has been included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credential object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="8e0eb-127">第二个命令执行相同操作，这一次返回 Ken Myer 帐户的凭据对象。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-127">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="8e0eb-128">使用凭据对象，第三个命令确定这两个用户是否可以登录 Lync Server 2013 并执行应用程序共享会议。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-128">With the credential objects in hand, the third command determines whether or not these two users can log on to Lync Server 2013 and conduct an Application Sharing conference.</span></span> <span data-ttu-id="8e0eb-129">若要执行此任务， **CsASConference** cmdlet 与以下参数一起调用： TargetFqdn (注册机构池的 FQDN) ;SenderSipAddress (第一个测试用户) 的 SIP 地址;SenderCredential (包含此同一用户的凭据的 Windows PowerShell 对象) ;ReceiverSipAddress (其他测试用户) 的 SIP 地址;和 ReceiverCredential (包含其他测试用户) 凭据的 Windows PowerShell 对象。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-129">To carry out this task, the **Test-CsASConference** cmdlet is called, along with the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object containing the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object containing the credentials for the other test user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar" 
    $cred2 = Get-Credential "litwareinc\kenmyer" 
    Test-CsASConference -TargetFqdn atl-cs-001.litwareinc.com -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $cred1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="8e0eb-130">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="8e0eb-130">Determining success or failure</span></span>

<span data-ttu-id="8e0eb-131">如果正确配置了应用程序共享，则将收到类似于此的输出，结果属性标记为 " **成功"：**</span><span class="sxs-lookup"><span data-stu-id="8e0eb-131">If application sharing is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="8e0eb-132">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="8e0eb-132">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="8e0eb-133">结果：成功</span><span class="sxs-lookup"><span data-stu-id="8e0eb-133">Result : Success</span></span>

<span data-ttu-id="8e0eb-134">延迟：00:00:01</span><span class="sxs-lookup"><span data-stu-id="8e0eb-134">Latency : 00:00:01</span></span>

<span data-ttu-id="8e0eb-135">错误消息：</span><span class="sxs-lookup"><span data-stu-id="8e0eb-135">Error Message :</span></span>

<span data-ttu-id="8e0eb-136">自检</span><span class="sxs-lookup"><span data-stu-id="8e0eb-136">Diagnosis :</span></span>

<span data-ttu-id="8e0eb-137">如果指定用户无法共享应用程序，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="8e0eb-137">If the specified users can't share applications, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="8e0eb-138">目标 Fqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="8e0eb-138">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="8e0eb-139">结果：失败</span><span class="sxs-lookup"><span data-stu-id="8e0eb-139">Result : Failure</span></span>

<span data-ttu-id="8e0eb-140">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="8e0eb-140">Latency : 00:00:00</span></span>

<span data-ttu-id="8e0eb-141">错误消息：10060，连接尝试失败，因为已连接的参与方</span><span class="sxs-lookup"><span data-stu-id="8e0eb-141">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="8e0eb-142">在一段时间后未正确响应，或者</span><span class="sxs-lookup"><span data-stu-id="8e0eb-142">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="8e0eb-143">已建立连接失败，因为连接的主机已</span><span class="sxs-lookup"><span data-stu-id="8e0eb-143">established connection failed because connected host has</span></span>

<span data-ttu-id="8e0eb-144">无法响应10.188.116.96：5061</span><span class="sxs-lookup"><span data-stu-id="8e0eb-144">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="8e0eb-145">内部异常：连接尝试失败，因为</span><span class="sxs-lookup"><span data-stu-id="8e0eb-145">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="8e0eb-146">已连接方在一段时间后未正确响应</span><span class="sxs-lookup"><span data-stu-id="8e0eb-146">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="8e0eb-147">时间，或已建立的连接失败，因为已连接的主机</span><span class="sxs-lookup"><span data-stu-id="8e0eb-147">time, or established connection failed because connected host</span></span>

<span data-ttu-id="8e0eb-148">无法响应10.188.116.96：5061</span><span class="sxs-lookup"><span data-stu-id="8e0eb-148">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="8e0eb-149">自检</span><span class="sxs-lookup"><span data-stu-id="8e0eb-149">Diagnosis :</span></span>

<span data-ttu-id="8e0eb-150">例如，以前的输出包含 "已连接方" 未正确响应的注释，这通常表示边缘服务器有问题。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-150">For example, the previous output includes the note “the connected party did not properly respond” That typically indicates a problem with the Edge Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="8e0eb-151">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="8e0eb-151">Reasons why the test might have failed</span></span>

<span data-ttu-id="8e0eb-152">下面是 **测试 CsASConference** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="8e0eb-152">Here are some common reasons why **Test-CsASConference** might fail:</span></span>

  - <span data-ttu-id="8e0eb-153">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-153">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="8e0eb-154">如果使用，则必须正确配置可选参数，否则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-154">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="8e0eb-155">重新运行不带可选参数的命令，并查看是否成功。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-155">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="8e0eb-156">如果为测试用户分配了一种阻止其使用应用程序共享的会议策略，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-156">This command will fail if the test users were assigned a conferencing policy that prevents them from using application sharing.</span></span>

  - <span data-ttu-id="8e0eb-157">如果边缘服务器配置错误或尚未部署，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="8e0eb-157">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8e0eb-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8e0eb-158">See Also</span></span>


[<span data-ttu-id="8e0eb-159">Get-CsConferencingPolicy</span><span class="sxs-lookup"><span data-stu-id="8e0eb-159">Get-CsConferencingPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsConferencingPolicy)  
[<span data-ttu-id="8e0eb-160">Test-CsDataConference</span><span class="sxs-lookup"><span data-stu-id="8e0eb-160">Test-CsDataConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsDataConference)  
  

<span data-ttu-id="8e0eb-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e0eb-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

