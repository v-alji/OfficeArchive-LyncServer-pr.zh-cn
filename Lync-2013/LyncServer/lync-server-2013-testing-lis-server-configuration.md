---
title: Lync Server 2013：测试 .LIS 服务器配置
description: Lync Server 2013：测试 .LIS 服务器配置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing LIS server configuration
ms:assetid: 6b06e7ab-522f-41a2-878b-e89cd4e3c6da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690129(v=OCS.15)
ms:contentKeyID: 63969614
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4d16d2ce48e3e5bb89e863f02902d05ce77bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392089"
---
# <a name="testing-lis-server-configuration-in-lync-server-2013"></a><span data-ttu-id="651ba-103">在 Lync Server 2013 中测试 .LIS 服务器配置</span><span class="sxs-lookup"><span data-stu-id="651ba-103">Testing LIS server configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="651ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="651ba-104">

<span> </span></span></span>

<span data-ttu-id="651ba-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="651ba-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="651ba-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="651ba-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="651ba-107">每天</span><span class="sxs-lookup"><span data-stu-id="651ba-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="651ba-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="651ba-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="651ba-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="651ba-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="651ba-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="651ba-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="651ba-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="651ba-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="651ba-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsLisConfiguration cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="651ba-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsLisConfiguration cmdlet.</span></span> <span data-ttu-id="651ba-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="651ba-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="651ba-114">说明</span><span class="sxs-lookup"><span data-stu-id="651ba-114">Description</span></span>

<span data-ttu-id="651ba-115">Test-CsLisConfiguration cmdlet 验证你是否能够联系 .LIS web 服务。</span><span class="sxs-lookup"><span data-stu-id="651ba-115">The Test-CsLisConfiguration cmdlet verifies your ability to contact the LIS web service.</span></span> <span data-ttu-id="651ba-116">如果可以联系到 web 服务，则会将测试视为成功，无论是否可以找到任何特定位置。</span><span class="sxs-lookup"><span data-stu-id="651ba-116">If the web service can be contacted, then the test will be considered a success, regardless of whether any specific locations can be found.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="651ba-117">运行测试</span><span class="sxs-lookup"><span data-stu-id="651ba-117">Running the test</span></span>

<span data-ttu-id="651ba-118">可以使用预配置的测试帐户运行 Test-CsLisConfguration cmdlet (请参阅设置用于运行 Lync Server 测试的测试帐户) 或为 Lync Server 启用的任何用户的帐户。</span><span class="sxs-lookup"><span data-stu-id="651ba-118">The Test-CsLisConfguration cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="651ba-119">若要使用测试帐户运行此检查，只需指定正在测试的 Lync Server 池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="651ba-119">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="651ba-120">例如：</span><span class="sxs-lookup"><span data-stu-id="651ba-120">For example:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="651ba-121">若要使用实际用户帐户运行此检查，必须首先创建一个包含帐户名称和密码的 Windows PowerShell 凭据对象。</span><span class="sxs-lookup"><span data-stu-id="651ba-121">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="651ba-122">然后，在调用 Test-CsLisConfiguration 时，必须包含该凭据对象和分配给该帐户的 SIP 地址：</span><span class="sxs-lookup"><span data-stu-id="651ba-122">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsLisConfiguration:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="651ba-123">有关详细信息，请参阅 [CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="651ba-123">For more information, see the Help documentation for the [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="651ba-124">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="651ba-124">Determining success or failure</span></span>

<span data-ttu-id="651ba-125">如果 IIS 配置正确，你将收到类似于此的输出，结果属性标记为 **成功：**</span><span class="sxs-lookup"><span data-stu-id="651ba-125">If the LIS is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="651ba-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span><span class="sxs-lookup"><span data-stu-id="651ba-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span></span>

<span data-ttu-id="651ba-127">liservice</span><span class="sxs-lookup"><span data-stu-id="651ba-127">liservice.svc</span></span>

<span data-ttu-id="651ba-128">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="651ba-128">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="651ba-129">结果：成功</span><span class="sxs-lookup"><span data-stu-id="651ba-129">Result : Success</span></span>

<span data-ttu-id="651ba-130">延迟：00：00：06.1616913</span><span class="sxs-lookup"><span data-stu-id="651ba-130">Latency : 00:00:06.1616913</span></span>

<span data-ttu-id="651ba-131">时发生</span><span class="sxs-lookup"><span data-stu-id="651ba-131">Error :</span></span>

<span data-ttu-id="651ba-132">自检</span><span class="sxs-lookup"><span data-stu-id="651ba-132">Diagnosis :</span></span>

<span data-ttu-id="651ba-133">如果指定用户无法登录或注销，则结果将显示为 "失败"，并且将在 "错误" 和 "诊断" 属性中记录其他信息：</span><span class="sxs-lookup"><span data-stu-id="651ba-133">If the specified user can't log on or log off, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="651ba-134">TargetUri :</span><span class="sxs-lookup"><span data-stu-id="651ba-134">TargetUri :</span></span>

<span data-ttu-id="651ba-135">TargetFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="651ba-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="651ba-136">结果：失败</span><span class="sxs-lookup"><span data-stu-id="651ba-136">Result : Failure</span></span>

<span data-ttu-id="651ba-137">延迟：00:00:00</span><span class="sxs-lookup"><span data-stu-id="651ba-137">Latency : 00:00:00</span></span>

<span data-ttu-id="651ba-138">错误：11004，所请求的名称有效，但没有请求的数据</span><span class="sxs-lookup"><span data-stu-id="651ba-138">Error : 11004, The requested name is valid but no data of the requested</span></span>

<span data-ttu-id="651ba-139">已找到类型</span><span class="sxs-lookup"><span data-stu-id="651ba-139">type was found</span></span>

<span data-ttu-id="651ba-140">自检</span><span class="sxs-lookup"><span data-stu-id="651ba-140">Diagnosis :</span></span>

<span data-ttu-id="651ba-141">Test-CsLisConfiguration：在拓扑中找不到匹配的群集。</span><span class="sxs-lookup"><span data-stu-id="651ba-141">Test-CsLisConfiguration : No matching cluster found in topology.</span></span>

<span data-ttu-id="651ba-142">例如，以前的输出包含注释 "在拓扑中找不到匹配的群集"。</span><span class="sxs-lookup"><span data-stu-id="651ba-142">For example, the previous output includes the note “No matching cluster found in topology.”</span></span> <span data-ttu-id="651ba-143">这通常表示边缘服务器存在问题： IIS 使用边缘服务器连接到服务提供商并验证地址。</span><span class="sxs-lookup"><span data-stu-id="651ba-143">That typically indicates a problem with the Edge Server: the LIS using the Edge Server to connect to the service provider and validate addresses.</span></span>

<span data-ttu-id="651ba-144">如果 Test-CsLisConfiguration 失败，则可能需要重新运行测试，这一次包括 Verbose 参数：</span><span class="sxs-lookup"><span data-stu-id="651ba-144">If Test-CsLisConfiguration fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="651ba-145">当包含详细参数时，Test-CsLisConfiguration 将返回它在检查指定用户登录到 Lync Server 的能力时尝试的每个操作的分步帐户。</span><span class="sxs-lookup"><span data-stu-id="651ba-145">When the Verbose parameter is included, Test-CsLisConfiguration will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="651ba-146">例如：</span><span class="sxs-lookup"><span data-stu-id="651ba-146">For example:</span></span>

<span data-ttu-id="651ba-147">呼叫位置信息服务。</span><span class="sxs-lookup"><span data-stu-id="651ba-147">Calling Location Information Service.</span></span>

<span data-ttu-id="651ba-148">服务路径 = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="651ba-148">Service Path = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span></span>

<span data-ttu-id="651ba-149">子网 =</span><span class="sxs-lookup"><span data-stu-id="651ba-149">Subnet =</span></span>

<span data-ttu-id="651ba-150">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="651ba-150">BssId = 5</span></span>

<span data-ttu-id="651ba-151">ChassisId =</span><span class="sxs-lookup"><span data-stu-id="651ba-151">ChassisId =</span></span>

<span data-ttu-id="651ba-152">PortId =</span><span class="sxs-lookup"><span data-stu-id="651ba-152">PortId =</span></span>

<span data-ttu-id="651ba-153">PortIdSubType = 未定义的类型</span><span class="sxs-lookup"><span data-stu-id="651ba-153">PortIdSubType = Undefined Type</span></span>

<span data-ttu-id="651ba-154">Mac</span><span class="sxs-lookup"><span data-stu-id="651ba-154">Mac</span></span>

<span data-ttu-id="651ba-155">异常 "位置信息 Web 服务请求失败，响应代码为 Item400。"</span><span class="sxs-lookup"><span data-stu-id="651ba-155">An exception 'Location Information Web Service request has failed with a response code Item400.'</span></span> <span data-ttu-id="651ba-156">在 STLisConfigurationWorkflow 执行工作流期间发生。</span><span class="sxs-lookup"><span data-stu-id="651ba-156">occurred during Workflow Microsoft.Rtc.SyntheticTrsnactions.Workflows.STLisConfigurationWorkflow execution.</span></span>

<span data-ttu-id="651ba-157">如果你仔细检查以前的输出，你将看到 cmdlet 在尝试调用位置信息服务后失败。</span><span class="sxs-lookup"><span data-stu-id="651ba-157">If you examine the previous output closely, you’ll see that the cmdlet failed after it tried to call the Location Information Service.</span></span> <span data-ttu-id="651ba-158">该调用中使用的参数之一如下所示：</span><span class="sxs-lookup"><span data-stu-id="651ba-158">One of the parameters that were used in that call was this:</span></span>

<span data-ttu-id="651ba-159">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="651ba-159">BssId = 5</span></span>

<span data-ttu-id="651ba-160">这不是基本服务集标识符 (BssID) 的有效值。</span><span class="sxs-lookup"><span data-stu-id="651ba-160">That’s not a valid value for the Basic Service Set Identifier (BssID).</span></span> <span data-ttu-id="651ba-161">相反，BssID 应如下所示：</span><span class="sxs-lookup"><span data-stu-id="651ba-161">Instead, a BssID should resemble this:</span></span>

<span data-ttu-id="651ba-162">12-34-56-78-90-ab</span><span class="sxs-lookup"><span data-stu-id="651ba-162">12-34-56-78-90-ab</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="651ba-163">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="651ba-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="651ba-164">下面是 Test-CsLisConfiguration 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="651ba-164">Here are some common reasons why Test-CsLisConfiguration might fail:</span></span>

  - <span data-ttu-id="651ba-165">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="651ba-165">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="651ba-166">如前面的示例所示，必须正确配置可选参数，否则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="651ba-166">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="651ba-167">重新运行不带可选参数的命令，并查看是否成功。</span><span class="sxs-lookup"><span data-stu-id="651ba-167">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

<span data-ttu-id="651ba-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="651ba-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

