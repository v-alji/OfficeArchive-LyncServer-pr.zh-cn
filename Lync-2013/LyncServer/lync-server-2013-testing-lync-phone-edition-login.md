---
title: Lync Server 2013：测试 Lync Phone Edition 登录
description: Lync Server 2013：测试 Lync Phone Edition 登录。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Phone Edition login
ms:assetid: 1ccde6bf-9a2d-4fcf-b81f-1bc9fee2cfbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690128(v=OCS.15)
ms:contentKeyID: 63969583
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d21d65676c4f5e0f867c7d9556cdea50419be69b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392081"
---
# <a name="testing-lync-phone-edition-login-in-lync-server-2013"></a><span data-ttu-id="a61f7-103">在 Lync Server 2013 中测试 Lync Phone Edition 登录</span><span class="sxs-lookup"><span data-stu-id="a61f7-103">Testing Lync Phone Edition login in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a61f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a61f7-104">

<span> </span></span></span>

<span data-ttu-id="a61f7-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="a61f7-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a61f7-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="a61f7-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="a61f7-107">每天</span><span class="sxs-lookup"><span data-stu-id="a61f7-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a61f7-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="a61f7-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="a61f7-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a61f7-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a61f7-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="a61f7-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="a61f7-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="a61f7-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="a61f7-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsPhoneBootstrap cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="a61f7-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPhoneBootstrap cmdlet.</span></span> <span data-ttu-id="a61f7-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="a61f7-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPhoneBootstrap&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="a61f7-114">说明</span><span class="sxs-lookup"><span data-stu-id="a61f7-114">Description</span></span>

<span data-ttu-id="a61f7-115">Test-CsPhoneBootstrap cmdlet 使管理员能够验证给定用户（使用电话号码和分配给他/她的 PIN）是否可以从 Lync 2013 Phone 版本兼容的设备登录到系统。</span><span class="sxs-lookup"><span data-stu-id="a61f7-115">The Test-CsPhoneBootstrap cmdlet enables administrators to verify that a given user—using the phone number and PIN assigned to him or her—can log on to the system from a Lync 2013 Phone Edition-compatible device.</span></span> <span data-ttu-id="a61f7-116"> (实际不需要设备来运行测试。 ) </span><span class="sxs-lookup"><span data-stu-id="a61f7-116">(No device is actually needed to run the test.)</span></span>

<span data-ttu-id="a61f7-117">为了使 Test-CsPhoneBootstrap 进行检查，托管要测试的用户帐户的注册者池必须使用 DHCP 才能发现。</span><span class="sxs-lookup"><span data-stu-id="a61f7-117">In order for Test-CsPhoneBootstrap to make its check, the Registrar pool that hosts the user account being tested must be discoverable using DHCP.</span></span> <span data-ttu-id="a61f7-118">若要确定注册机构是否以这种方式被发现，请使用 cmdlet Get-CsRegistrarConfiguration 并检查 EnableDHCPServer 属性的值。</span><span class="sxs-lookup"><span data-stu-id="a61f7-118">To determine whether a Registrar is discoverable in this manner, use the cmdlet Get-CsRegistrarConfiguration and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="a61f7-119">如果此属性设置为 False，则必须使用 Set-CsRegistrarConfiguration 将属性值设置为 True，并使用 DHCP 使注册机构可发现。</span><span class="sxs-lookup"><span data-stu-id="a61f7-119">If this property is set to False, you must use Set-CsRegistrarConfiguration to set the property value to True and make the Registrar discoverable using DHCP.</span></span> <span data-ttu-id="a61f7-120">也可以使用企业 DHCP 服务器并配置 Lync Server 特定的选项来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="a61f7-120">This can also be done by using Enterprise DHCP Server and configuring the Lync Server-specific options.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="a61f7-121">运行测试</span><span class="sxs-lookup"><span data-stu-id="a61f7-121">Running the test</span></span>

<span data-ttu-id="a61f7-122">若要运行 Test-CsPhoneBootstrap cmdlet，必须至少为有效的 Lync 服务器用户提供电话号码和客户端个人识别码 (PIN) 。</span><span class="sxs-lookup"><span data-stu-id="a61f7-122">To run the Test-CsPhoneBootstrap cmdlet, you must, at a minimum, supply the phone number and client personal identification number (PIN) for a valid Lync Server user.</span></span> <span data-ttu-id="a61f7-123">例如，此命令将测试具有电话号码12065551219和引脚0712的用户的登录能力：</span><span class="sxs-lookup"><span data-stu-id="a61f7-123">For example, this command tests the logon ability for the user who has the phone number 12065551219 and the PIN 0712:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712"

<span data-ttu-id="a61f7-124">若要进行更全面的检查，您还可以包括用户的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="a61f7-124">For a more comprehensive check, you can also include the user’s SIP address.</span></span> <span data-ttu-id="a61f7-125">在这种情况下，电话号码、客户端 PIN 和 SIP 地址必须全部有效才能使测试成功：</span><span class="sxs-lookup"><span data-stu-id="a61f7-125">In that case, the phone number, client PIN, and SIP address must all be valid for the test to succeed:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -UserSipAddress "sip:kenmyer@litwareinc.com"

<span data-ttu-id="a61f7-126">有关详细信息，请参阅 [CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="a61f7-126">For more information, see the Help documentation for the [Test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="a61f7-127">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="a61f7-127">Determining success or failure</span></span>

<span data-ttu-id="a61f7-128">如果指定用户能够连接到 Lync Server，你将收到类似于此的输出，结果属性标记为 " **成功"：**</span><span class="sxs-lookup"><span data-stu-id="a61f7-128">If the specified user was able to connect to Lync Server, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="a61f7-129">TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/</span><span class="sxs-lookup"><span data-stu-id="a61f7-129">TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/</span></span>

<span data-ttu-id="a61f7-130">CertProvisioningService</span><span class="sxs-lookup"><span data-stu-id="a61f7-130">CertProvisioningService.svc</span></span>

<span data-ttu-id="a61f7-131">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a61f7-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a61f7-132">结果：成功</span><span class="sxs-lookup"><span data-stu-id="a61f7-132">Result : Success</span></span>

<span data-ttu-id="a61f7-133">延迟：00：00：06.3981276</span><span class="sxs-lookup"><span data-stu-id="a61f7-133">Latency : 00:00:06.3981276</span></span>

<span data-ttu-id="a61f7-134">时发生</span><span class="sxs-lookup"><span data-stu-id="a61f7-134">Error :</span></span>

<span data-ttu-id="a61f7-135">自检</span><span class="sxs-lookup"><span data-stu-id="a61f7-135">Diagnosis :</span></span>

<span data-ttu-id="a61f7-136">如果指定的用户无法建立连接，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="a61f7-136">If the specified user was not able to make a connection, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="a61f7-137">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a61f7-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a61f7-138">结果：失败</span><span class="sxs-lookup"><span data-stu-id="a61f7-138">Result : Failure</span></span>

<span data-ttu-id="a61f7-139">延迟：00：00：04.1993845</span><span class="sxs-lookup"><span data-stu-id="a61f7-139">Latency : 00:00:04.1993845</span></span>

<span data-ttu-id="a61f7-140">错误：错误-未收到 Web-Ticket 服务的响应。</span><span class="sxs-lookup"><span data-stu-id="a61f7-140">Error : ERROR - No response received for Web-Ticket service.</span></span>

<span data-ttu-id="a61f7-141">自检</span><span class="sxs-lookup"><span data-stu-id="a61f7-141">Diagnosis :</span></span>

<span data-ttu-id="a61f7-142">以前的输出表明测试失败的原因是 Web 票证服务未响应。</span><span class="sxs-lookup"><span data-stu-id="a61f7-142">The previous output states that the test failed because the Web Ticket service did not respond.</span></span> <span data-ttu-id="a61f7-143">这可能是由于服务本身有问题，也可能是由于 SIP 地址、电话号码或客户 PIN 传递到了 CsPhoneBootstrap。</span><span class="sxs-lookup"><span data-stu-id="a61f7-143">This could be due to a problem with the service itself, or it might be due to the SIP address, phone number, or client PIN passed to Test-CsPhoneBootstrap.</span></span> <span data-ttu-id="a61f7-144">你可以使用类似下面的命令验证用户的 SIP 地址和电话号码：</span><span class="sxs-lookup"><span data-stu-id="a61f7-144">You can verify the user’s SIP address and phone number by using a command similar to this one:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, LineUri

<span data-ttu-id="a61f7-145">你可以通过使用命令验证用户是否具有有效的 PIN，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a61f7-145">And you can verify that the user has a valid PIN by using a command as follows:</span></span>

    Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="a61f7-146">如果 Test-CsPhoneBootstrap 失败，则可能需要重新运行测试，这一次包括 Verbose 参数：</span><span class="sxs-lookup"><span data-stu-id="a61f7-146">If Test-CsPhoneBootstrap fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -Verbose

<span data-ttu-id="a61f7-147">当包含详细参数时，Test-CsPhoneBootstrap 将返回它在检查指定用户登录到 Lync Server 的能力时尝试的每个操作的分步帐户。</span><span class="sxs-lookup"><span data-stu-id="a61f7-147">When the Verbose parameter is included, Test-CsPhoneBootstrap will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="a61f7-148">例如，下面是一个失败登录的部分输出，其中包含错误 PIN 的会话：</span><span class="sxs-lookup"><span data-stu-id="a61f7-148">For example, here is a portion of the output for an unsuccessful logon, a session in which an incorrect PIN was included:</span></span>

<span data-ttu-id="a61f7-149">将 PIN 验证与电话 \\ 分机：12065551219针：0712配合使用</span><span class="sxs-lookup"><span data-stu-id="a61f7-149">Using PIN auth with Phone\\Ext : 12065551219 Pin : 0712</span></span>

<span data-ttu-id="a61f7-150">无法获取 web 票证</span><span class="sxs-lookup"><span data-stu-id="a61f7-150">Could not get web ticket</span></span>

<span data-ttu-id="a61f7-151">选中</span><span class="sxs-lookup"><span data-stu-id="a61f7-151">CHECK :</span></span>

<span data-ttu-id="a61f7-152">\- Web 服务 url 有效且 web 服务正常运行</span><span class="sxs-lookup"><span data-stu-id="a61f7-152">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="a61f7-153">\- 如果使用 PhoneNo \\ PIN 进行身份验证，请确保它们与用户 uri 匹配</span><span class="sxs-lookup"><span data-stu-id="a61f7-153">\- If using PhoneNo\\PIN to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="a61f7-154">\- 如果使用 NTLM \\ Kerberos 身份验证，请确保提供有效的凭据</span><span class="sxs-lookup"><span data-stu-id="a61f7-154">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="a61f7-155">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="a61f7-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="a61f7-156">下面是 Test-CsPhoneBootstrap 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="a61f7-156">Here are some common reasons why Test-CsPhoneBootstrap might fail:</span></span>

  - <span data-ttu-id="a61f7-157">您可能指定了一个无效的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="a61f7-157">You might have specified a SIP address that is not valid.</span></span> <span data-ttu-id="a61f7-158">你可以使用以下命令验证 SIP 地址是否正确：</span><span class="sxs-lookup"><span data-stu-id="a61f7-158">You can verify that a SIP address is correct by using a command such as this one:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="a61f7-159">您可能指定了一个无效的 PIN 码。</span><span class="sxs-lookup"><span data-stu-id="a61f7-159">You might have specified a PIN that is not valid.</span></span> <span data-ttu-id="a61f7-160">虽然您无法检索用户的 PIN 码，但您可以通过使用类似下面的命令验证用户是否至少拥有 PIN 码：</span><span class="sxs-lookup"><span data-stu-id="a61f7-160">Although you can't retrieve the user’s PIN number, you can verify that the user at least has a PIN number by using a command similar to this:</span></span>
    
        Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="a61f7-161">您可能指定了一个无效的电话号码。</span><span class="sxs-lookup"><span data-stu-id="a61f7-161">You might have specified a phone number that is not valid.</span></span> <span data-ttu-id="a61f7-162">你可以使用类似如下的命令验证用户的电话：</span><span class="sxs-lookup"><span data-stu-id="a61f7-162">You can verify a user’s phone by using a command similar to the following:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object LineUri

  - <span data-ttu-id="a61f7-163">注册机构池不是启用 DHCP 的。</span><span class="sxs-lookup"><span data-stu-id="a61f7-163">The Registrar pool is not DHCP-enabled.</span></span> <span data-ttu-id="a61f7-164">若要确定注册机构池是否已为 DHCP 启用，请运行 Get-CsRegistrarConfiguration cmdlet 并检查 EnableDHCPServer 属性的值。</span><span class="sxs-lookup"><span data-stu-id="a61f7-164">To determine whether your Registrar pool is enabled for DHCP, run the Get-CsRegistrarConfiguration cmdlet and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="a61f7-165">例如：</span><span class="sxs-lookup"><span data-stu-id="a61f7-165">For example:</span></span>
    
        Get-CsRegistrarConfiguration -Identity "global"

<span data-ttu-id="a61f7-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a61f7-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

