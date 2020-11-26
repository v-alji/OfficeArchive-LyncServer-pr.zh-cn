---
title: Lync Server 2013：测试服务激活和组权限
description: Lync Server 2013：测试服务激活和组权限。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing service activation and group permissions
ms:assetid: 2c59e603-ba85-40ba-91a7-51c6fd39472e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743833(v=OCS.15)
ms:contentKeyID: 63969594
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116cf939f3110616ce395eb14c7945890bdb89b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440981"
---
# <a name="testing-service-activation-and-group-permissions-in-lync-server-2013"></a><span data-ttu-id="3e02d-103">在 Lync Server 2013 中测试服务激活和组权限</span><span class="sxs-lookup"><span data-stu-id="3e02d-103">Testing service activation and group permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e02d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e02d-104">

<span> </span></span></span>

<span data-ttu-id="3e02d-105">_**主题上次修改时间：** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="3e02d-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e02d-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="3e02d-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="3e02d-107">每天</span><span class="sxs-lookup"><span data-stu-id="3e02d-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e02d-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="3e02d-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="3e02d-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e02d-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e02d-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="3e02d-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="3e02d-111">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="3e02d-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="3e02d-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsTopology cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="3e02d-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTopology cmdlet.</span></span> <span data-ttu-id="3e02d-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="3e02d-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTopology&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="3e02d-114">说明</span><span class="sxs-lookup"><span data-stu-id="3e02d-114">Description</span></span>

<span data-ttu-id="3e02d-115">Test-CsTopology cmdlet 使你能够验证 Lync Server 2013 在全局范围内是否正常工作。</span><span class="sxs-lookup"><span data-stu-id="3e02d-115">The Test-CsTopology cmdlet enables you to verify that Lync Server 2013 is functioning correctly at a global scope.</span></span> <span data-ttu-id="3e02d-116">默认情况下，该 cmdlet 检查整个 Lync 服务器基础结构，验证所需服务是否正在运行以及是否为这些服务以及在安装 Lync Server 时创建的通用安全组设置了相应的权限。</span><span class="sxs-lookup"><span data-stu-id="3e02d-116">By default, the cmdlet checks your whole Lync Server infrastructure, verifying that the required services are running and that the appropriate permissions are set for these services and for the universal security groups that are created when you install Lync Server.</span></span>

<span data-ttu-id="3e02d-117">除了验证 Lync Server 安装的有效性，Test-CsTopology 还允许你检查特定服务的有效性。</span><span class="sxs-lookup"><span data-stu-id="3e02d-117">In addition to verifying the validity of the Lync Server installation, Test-CsTopology also lets you check the validity of a specific service.</span></span> <span data-ttu-id="3e02d-118">例如，此命令将检查 pool atl-cs-001.litwareinc.com 上的 A/V 会议服务器的状态：</span><span class="sxs-lookup"><span data-stu-id="3e02d-118">For example, this command checks the state of the A/V Conferencing Server on the pool atl-cs-001.litwareinc.com:</span></span>

    Test-CsTopology -Service "ConferencingServer:atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="3e02d-119">运行测试</span><span class="sxs-lookup"><span data-stu-id="3e02d-119">Running the test</span></span>

<span data-ttu-id="3e02d-120">默认情况下，Test-CsTopology 在屏幕上显示非常少的输出。</span><span class="sxs-lookup"><span data-stu-id="3e02d-120">By default, Test-CsTopology displays very little output on-screen.</span></span> <span data-ttu-id="3e02d-121">而是将 cmdlet 返回的信息写入 HTML 文件。</span><span class="sxs-lookup"><span data-stu-id="3e02d-121">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="3e02d-122">Report 参数允许你为由 Test CsTopology 生成的 HTML 文件指定文件路径和文件名。</span><span class="sxs-lookup"><span data-stu-id="3e02d-122">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsTopology.</span></span> <span data-ttu-id="3e02d-123">如果不包含报表参数，则 HTML 文件将自动保存到 "用户" 文件夹中，并指定如下名称： ce84964a-c4da-4622-ad34-c54ff3ed361f.html。</span><span class="sxs-lookup"><span data-stu-id="3e02d-123">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="3e02d-124">以下示例命令将运行 Test-CsTopology 并将输出保存到名为 C： \\ LogsComputerTest.html 的文件中 \\ ：</span><span class="sxs-lookup"><span data-stu-id="3e02d-124">The following sample command runs Test-CsTopology and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsTopology -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="3e02d-125">有关详细信息，请参阅 [CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) Cmdlet 的帮助文档。</span><span class="sxs-lookup"><span data-stu-id="3e02d-125">For more information, see the Help documentation for the [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="3e02d-126">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="3e02d-126">Determining success or failure</span></span>

<span data-ttu-id="3e02d-127">与大多数测试 cmdlet 不同，Test-CsTopology 会报告回退成功或失败。</span><span class="sxs-lookup"><span data-stu-id="3e02d-127">Unlike most of the test cmdlets, Test-CsTopology does report back Success or Failure.</span></span> <span data-ttu-id="3e02d-128">部分中，这是因为每次运行 cmdlet 时都必须执行大量的验证检查。</span><span class="sxs-lookup"><span data-stu-id="3e02d-128">In part, that’s due to the large number of verification checks that the cmdlet must make every time that it runs.</span></span> <span data-ttu-id="3e02d-129">而是将数据保存到 HTML 报表，然后可使用 Internet Explorer 查看。</span><span class="sxs-lookup"><span data-stu-id="3e02d-129">Instead, data is saved to an HTML report that can then be viewed by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="3e02d-130">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="3e02d-130">Reasons why the test might have failed</span></span>

<span data-ttu-id="3e02d-131">下面是 Test-CsTopology 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="3e02d-131">Here are some common reasons why Test-CsTopology might fail:</span></span>

  - <span data-ttu-id="3e02d-132">测试计算机上的复制可能不是最新的。</span><span class="sxs-lookup"><span data-stu-id="3e02d-132">Replication might not be up-to-date on the test computer.</span></span> <span data-ttu-id="3e02d-133">你可以通过运行 Get-CsManagementStoreReplicationStatus cmdlet 来检查计算机的当前复制状态：</span><span class="sxs-lookup"><span data-stu-id="3e02d-133">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="3e02d-134">如果复制状态不是最新的，则可以通过使用类似下面的命令手动强制执行复制：</span><span class="sxs-lookup"><span data-stu-id="3e02d-134">If the replication status is not up-to-date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="3e02d-135">可能必须启用拓扑。</span><span class="sxs-lookup"><span data-stu-id="3e02d-135">The topology might have to be enabled.</span></span> <span data-ttu-id="3e02d-136">如果将 Lync Server 拓扑更改 (可能影响本地计算机) 的更改，则必须启用新拓扑。</span><span class="sxs-lookup"><span data-stu-id="3e02d-136">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="3e02d-137">可以通过运行以下命令随时启用拓扑：</span><span class="sxs-lookup"><span data-stu-id="3e02d-137">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="3e02d-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e02d-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

