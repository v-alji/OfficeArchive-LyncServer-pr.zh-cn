---
title: Lync Server 2013：测试副本服务
description: Lync Server 2013：测试副本服务。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the replica service
ms:assetid: 4ff2cc91-0036-4c5a-9792-7bf43d8ce18d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727303(v=OCS.15)
ms:contentKeyID: 63969600
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a61751b95115da3d6519f20f52262b7159ffcbfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440974"
---
# <a name="testing-the-replica-service-in-lync-server-2013"></a><span data-ttu-id="def24-103">在 Lync Server 2013 中测试副本服务</span><span class="sxs-lookup"><span data-stu-id="def24-103">Testing the replica service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="def24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="def24-104">

<span> </span></span></span>

<span data-ttu-id="def24-105">_**主题上次修改时间：** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="def24-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="def24-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="def24-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="def24-107">每天</span><span class="sxs-lookup"><span data-stu-id="def24-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="def24-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="def24-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="def24-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="def24-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="def24-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="def24-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="def24-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="def24-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="def24-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 <strong>CsReplica</strong> cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="def24-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsReplica</strong> cmdlet.</span></span> <span data-ttu-id="def24-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="def24-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsReplica&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="def24-114">说明</span><span class="sxs-lookup"><span data-stu-id="def24-114">Description</span></span>

<span data-ttu-id="def24-115">**CsReplica** cmdlet 验证是否在本地计算机上运行 Lync Server 2013 副本服务。</span><span class="sxs-lookup"><span data-stu-id="def24-115">The **Test-CsReplica** cmdlet verifies that the Lync Server 2013 replica service is running on the local computer.</span></span> <span data-ttu-id="def24-116">**CsReplica** cmdlet 执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="def24-116">The **Test-CsReplica** cmdlet performs such tasks as:</span></span>

  - <span data-ttu-id="def24-117">检查复制器代理和集中式日志记录代理服务的状态</span><span class="sxs-lookup"><span data-stu-id="def24-117">checking the status of the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="def24-118">验证是否已在 Windows 防火墙中打开所需的端口</span><span class="sxs-lookup"><span data-stu-id="def24-118">verifying that the required ports were opened in the Windows Firewall</span></span>

  - <span data-ttu-id="def24-119">确保有必要的 Active Directory 和本地计算机安全组。</span><span class="sxs-lookup"><span data-stu-id="def24-119">making sure that the necessary Active Directory and local computer security groups exist.</span></span>

<span data-ttu-id="def24-120">请注意，此 cmdlet 必须在本地运行。</span><span class="sxs-lookup"><span data-stu-id="def24-120">Note that this cmdlet must be run locally.</span></span> <span data-ttu-id="def24-121">也就是说，它必须在运行副本服务的同一台计算机上运行。</span><span class="sxs-lookup"><span data-stu-id="def24-121">That is, it must be run on the same computer where the replica service is running.</span></span> <span data-ttu-id="def24-122">没有用于针对远程服务器运行 **CsReplica** cmdlet 的选项。</span><span class="sxs-lookup"><span data-stu-id="def24-122">There are no options for running the **Test-CsReplica** cmdlet against a remote server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="def24-123">运行测试</span><span class="sxs-lookup"><span data-stu-id="def24-123">Running the test</span></span>

<span data-ttu-id="def24-124">示例1中所示的命令将测试本地计算机上的 Lync Server 2013 副本服务。</span><span class="sxs-lookup"><span data-stu-id="def24-124">The command shown in Example 1 tests the Lync Server 2013 replica service on the local computer.</span></span> <span data-ttu-id="def24-125">在此示例中，Verbose 参数用于保证有关测试的信息-包括测试的最终故障或成功的测试的位置-显示在屏幕上。</span><span class="sxs-lookup"><span data-stu-id="def24-125">In this example the Verbose parameter is used to guarantee that information about the test – including the eventual failure or success of the test and the location of the report generated by the test – is displayed on screen.</span></span>

    Test-CsReplica -Verbose

<span data-ttu-id="def24-126">示例2是示例1中所示命令的变体。</span><span class="sxs-lookup"><span data-stu-id="def24-126">Example 2 is a variation of the command shown in Example 1.</span></span> <span data-ttu-id="def24-127">在这种情况下，包含报表参数，以便为测试生成的报表指定文件夹路径和名称。</span><span class="sxs-lookup"><span data-stu-id="def24-127">In this case, the Report parameter is included to specify a folder path and name for the report generated by the test.</span></span> <span data-ttu-id="def24-128">如果未指定报表路径，将为报表提供一个类似于以下内容的自动生成的名称：</span><span class="sxs-lookup"><span data-stu-id="def24-128">If you do not specify a report path the report will be given an auto-generated name similar to this:</span></span>

<span data-ttu-id="def24-129">C： \\ 用户 \\ 管理员。 Litwareinc \\ AppData \\ 本地 \\ 临时 \\ 1 \\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span><span class="sxs-lookup"><span data-stu-id="def24-129">C:\\Users\\Administrator.Litwareinc\\AppData\\Local\\Temp\\1\\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span></span>

    Test-CsReplica -Verbose -Report C:\Logs\ReplicaTest.html

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="def24-130">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="def24-130">Determining success or failure</span></span>

<span data-ttu-id="def24-131">在此处插入节正文。</span><span class="sxs-lookup"><span data-stu-id="def24-131">Insert section body here.</span></span>

<span data-ttu-id="def24-132">详细：创建新日志文件 "C： \\ 用户 \\ 测试 \\ AppData \\ 本地 \\ 临时 \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml"。</span><span class="sxs-lookup"><span data-stu-id="def24-132">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="def24-133">详细：创建新日志文件 "C： \\ 用户 \\ 测试 \\ AppData \\ 本地 \\ 临时 \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml"。</span><span class="sxs-lookup"><span data-stu-id="def24-133">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="def24-134">详细： "Test-CsReplica" 处理已成功完成。</span><span class="sxs-lookup"><span data-stu-id="def24-134">VERBOSE: "Test-CsReplica" processing has completed successfully.</span></span>

<span data-ttu-id="def24-135">详细：可在 "C： \\ 用户 \\ 测试 \\ AppData \\ 本地 \\ 临时 \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml" 处找到详细结果。</span><span class="sxs-lookup"><span data-stu-id="def24-135">VERBOSE: Detailed results can be found at "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="def24-136">详细：创建新日志文件</span><span class="sxs-lookup"><span data-stu-id="def24-136">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="def24-137">"C： \\ 用户 \\ 测试 \\ AppData \\ 本地 \\ 温度 \\ 2 \\ 测试-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="def24-137">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="def24-138">d3bd0e4a083.xml "。</span><span class="sxs-lookup"><span data-stu-id="def24-138">d3bd0e4a083.xml".</span></span>

<span data-ttu-id="def24-139">详细：创建新日志文件</span><span class="sxs-lookup"><span data-stu-id="def24-139">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="def24-140">"C： \\ 用户 \\ 测试 \\ AppData \\ 本地 \\ 温度 \\ 2 \\ 测试-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="def24-140">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="def24-141">d3bd0e4a083.html "。</span><span class="sxs-lookup"><span data-stu-id="def24-141">d3bd0e4a083.html".</span></span>

<span data-ttu-id="def24-142">警告： Test-CsReplica 失败。</span><span class="sxs-lookup"><span data-stu-id="def24-142">WARNING: Test-CsReplica failed.</span></span>

<span data-ttu-id="def24-143">警告：可以在以下位置找到详细结果</span><span class="sxs-lookup"><span data-stu-id="def24-143">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="def24-144">"C： \\ 用户 \\ 测试 \\ AppData \\ 本地 \\ 温度 \\ 2 \\ 测试-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="def24-144">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="def24-145">d3bd0e4a083.html "。</span><span class="sxs-lookup"><span data-stu-id="def24-145">d3bd0e4a083.html".</span></span>

<span data-ttu-id="def24-146">Test-CsReplica：命令执行失败：请求的注册表访问不是</span><span class="sxs-lookup"><span data-stu-id="def24-146">Test-CsReplica : Command execution failed: Requested registry access is not</span></span>

<span data-ttu-id="def24-147">有.</span><span class="sxs-lookup"><span data-stu-id="def24-147">allowed.</span></span>

<span data-ttu-id="def24-148">在第1行：1个字符：1</span><span class="sxs-lookup"><span data-stu-id="def24-148">At line:1 char:1</span></span>

<span data-ttu-id="def24-149">\+ Test-CsReplica-详细</span><span class="sxs-lookup"><span data-stu-id="def24-149">\+ Test-CsReplica -Verbose</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="def24-150">\+ CategoryInfo： InvalidOperation： (： ) \[ Test-CsReplica \] ，Security</span><span class="sxs-lookup"><span data-stu-id="def24-150">\+ CategoryInfo : InvalidOperation: (:) \[Test-CsReplica\], Security</span></span>

<span data-ttu-id="def24-151">除了</span><span class="sxs-lookup"><span data-stu-id="def24-151">Exception</span></span>

<span data-ttu-id="def24-152">\+ FullyQualifiedErrorId： ProcessingFailed、、.Deploy</span><span class="sxs-lookup"><span data-stu-id="def24-152">\+ FullyQualifiedErrorId : ProcessingFailed,Microsoft.Rtc.Management.Deploy</span></span>

<span data-ttu-id="def24-153">。TestReplicaCmdlet</span><span class="sxs-lookup"><span data-stu-id="def24-153">ment.TestReplicaCmdlet</span></span>

<span data-ttu-id="def24-154">PS C： \\ 用户 \\ 测试\></span><span class="sxs-lookup"><span data-stu-id="def24-154">PS C:\\Users\\Testing\></span></span>

<span data-ttu-id="def24-155">PS C： \\ 用户 \\ 测试 \> Test-CsUcwaConference-TargetFqdn "LyncTest"</span><span class="sxs-lookup"><span data-stu-id="def24-155">PS C:\\Users\\Testing\> Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.M</span></span>

<span data-ttu-id="def24-156">icrosoft.com "</span><span class="sxs-lookup"><span data-stu-id="def24-156">icrosoft.com"</span></span>

<span data-ttu-id="def24-157">警告：无法读取给定的完全限定的注册机构端口号</span><span class="sxs-lookup"><span data-stu-id="def24-157">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="def24-158"> (FQDN) 的域名。</span><span class="sxs-lookup"><span data-stu-id="def24-158">domain name (FQDN).</span></span> <span data-ttu-id="def24-159">使用默认注册器端口号。</span><span class="sxs-lookup"><span data-stu-id="def24-159">Using default Registrar port number.</span></span> <span data-ttu-id="def24-160">除了</span><span class="sxs-lookup"><span data-stu-id="def24-160">Exception:</span></span>

<span data-ttu-id="def24-161">InvalidOperationException：在拓扑中找不到匹配的群集。</span><span class="sxs-lookup"><span data-stu-id="def24-161">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="def24-162">看</span><span class="sxs-lookup"><span data-stu-id="def24-162">at</span></span>

<span data-ttu-id="def24-163">SipSyntheticTransaction. TryRetri 的 SyntheticTransactions</span><span class="sxs-lookup"><span data-stu-id="def24-163">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="def24-164">eveRegistrarPortFromTopology (Int32& registrarPortNumber) </span><span class="sxs-lookup"><span data-stu-id="def24-164">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="def24-165">Test-CsUcwaConference：没有分配测试用户</span><span class="sxs-lookup"><span data-stu-id="def24-165">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="def24-166">\[LyncTest.SelfHost.Corp.Microsoft.com \] 。</span><span class="sxs-lookup"><span data-stu-id="def24-166">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="def24-167">验证测试用户配置。</span><span class="sxs-lookup"><span data-stu-id="def24-167">Verify test user configuration.</span></span>

<span data-ttu-id="def24-168">在第1行：1个字符：1</span><span class="sxs-lookup"><span data-stu-id="def24-168">At line:1 char:1</span></span>

<span data-ttu-id="def24-169">\+ Test-CsUcwaConference-TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="def24-169">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="def24-170">\+ CategoryInfo： ResourceUnavailable： (： ) \[ Test-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="def24-170">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="def24-171">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="def24-171">, InvalidOperationException</span></span>

<span data-ttu-id="def24-172">\+ FullyQualifiedErrorId： NotFoundTestUsers、</span><span class="sxs-lookup"><span data-stu-id="def24-172">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="def24-173">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="def24-173">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="def24-174">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="def24-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="def24-175">下面是 **测试 CsReplica** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="def24-175">Here are some common reasons why **Test-CsReplica** might fail:</span></span>

  - <span data-ttu-id="def24-176">复制器代理和集中式日志记录代理服务可能存在更大的问题</span><span class="sxs-lookup"><span data-stu-id="def24-176">There may be a larger problem with the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="def24-177">所需的端口可能未在 Windows 防火墙中打开</span><span class="sxs-lookup"><span data-stu-id="def24-177">The required ports may not be open in the Windows Firewall</span></span>

  - <span data-ttu-id="def24-178">所需的 Active Directory 和本地计算机安全组可能不存在</span><span class="sxs-lookup"><span data-stu-id="def24-178">The necessary Active Directory and local computer security groups may not exist</span></span>

<span data-ttu-id="def24-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="def24-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

