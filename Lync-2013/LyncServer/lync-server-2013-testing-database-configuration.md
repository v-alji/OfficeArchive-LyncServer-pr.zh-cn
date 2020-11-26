---
title: Lync Server 2013：测试数据库配置
description: Lync Server 2013：测试数据库配置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing database configuration
ms:assetid: 60f7fcd2-5efe-4791-b159-b0f9bf39a41b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727307(v=OCS.15)
ms:contentKeyID: 63969606
ms.date: 07/07/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b9f88eee99c4a2d523cc84df401dcc1d7b9fe59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441037"
---
# <a name="testing-database-configuration-in-lync-server-2013"></a><span data-ttu-id="c872a-103">在 Lync Server 2013 中测试数据库配置</span><span class="sxs-lookup"><span data-stu-id="c872a-103">Testing database configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c872a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c872a-104">

<span> </span></span></span>

<span data-ttu-id="c872a-105">_**主题上次修改时间：** 2016-07-07_</span><span class="sxs-lookup"><span data-stu-id="c872a-105">_**Topic Last Modified:** 2016-07-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c872a-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="c872a-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c872a-107">每天</span><span class="sxs-lookup"><span data-stu-id="c872a-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c872a-108">测试工具</span><span class="sxs-lookup"><span data-stu-id="c872a-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c872a-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c872a-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c872a-110">需要权限</span><span class="sxs-lookup"><span data-stu-id="c872a-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c872a-111">使用 Lync Server 命令行管理程序本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员，并且需要拥有 SQL Server 的管理员权限。</span><span class="sxs-lookup"><span data-stu-id="c872a-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group, and need to have Administrator privileges on the SQL server.</span></span></p>
<p><span data-ttu-id="c872a-112">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 <strong>CsDatabase</strong> cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="c872a-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDatabase</strong> cmdlet.</span></span> <span data-ttu-id="c872a-113">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="c872a-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDatabase&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c872a-114">说明</span><span class="sxs-lookup"><span data-stu-id="c872a-114">Description</span></span>

<span data-ttu-id="c872a-115">**CsDatabase** cmdlet 验证与一个或多个 Lync Server 2013 数据库的连接。</span><span class="sxs-lookup"><span data-stu-id="c872a-115">The **Test-CsDatabase** cmdlet verifies connectivity to one or more Lync Server 2013 databases.</span></span> <span data-ttu-id="c872a-116">运行时， **CsDatabase** cmdlet 会读取 Lync Server 拓扑，尝试连接到相关数据库，然后返回每次尝试成功或失败的报告。</span><span class="sxs-lookup"><span data-stu-id="c872a-116">When run, the **Test-CsDatabase** cmdlet reads the Lync Server topology, attempts to connect to relevant databases, and then reports back the success or failure of each try.</span></span> <span data-ttu-id="c872a-117">如果可以建立连接，则 cmdlet 还会报告返回有关数据库名称、SQL Server 版本信息以及任何已安装镜像数据库位置的信息。</span><span class="sxs-lookup"><span data-stu-id="c872a-117">If a connection can be made, the cmdlet will also report back such information as the database name, SQL Server version information, and the location of any installed mirror databases.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c872a-118">运行测试</span><span class="sxs-lookup"><span data-stu-id="c872a-118">Running the test</span></span>

<span data-ttu-id="c872a-119">示例1中所示的命令验证中央管理数据库的配置。</span><span class="sxs-lookup"><span data-stu-id="c872a-119">The command shown in Example 1 verifies the configuration of the Central Management database.</span></span>

    Test-CsDatabase -CentralManagementDatabase

<span data-ttu-id="c872a-120">示例2验证计算机 atl-sql-001.litwareinc.com 上安装的所有 Lync Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="c872a-120">Example 2 verifies all the Lync Server databases installed on the computer atl-sql-001.litwareinc.com.</span></span>

    Test-CsDatabase -ConfiguredDatabases -SqlServerFqdn "atl-sql-001.litwareinc.com"

<span data-ttu-id="c872a-121">在示例3中，仅对计算机 atl-sql-001.litwareinc.com 上安装的存档数据库执行验证。</span><span class="sxs-lookup"><span data-stu-id="c872a-121">In Example 3, verification is performed only for the Archiving database installed on the computer atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="c872a-122">请注意，SqlInstanceName 参数包含在) 存档数据库所在的位置 (Archinst 指定 SQL Server 实例。</span><span class="sxs-lookup"><span data-stu-id="c872a-122">Note that the SqlInstanceName parameter is included to specify the SQL Server instance (Archinst) where the Archiving database is located.</span></span>

    Test-CsDatabase -DatabaseType "Archiving" -SqlServerFqdn "atl-sql-001.litwareinc.com" -SqlInstanceName "archinst"

<span data-ttu-id="c872a-123">示例4中所示的命令验证本地计算机上安装的数据库。</span><span class="sxs-lookup"><span data-stu-id="c872a-123">The command shown in Example 4 verifies the databases installed on the local computer.</span></span>

    Test-CsDatabase -LocalService

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c872a-124">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="c872a-124">Determining success or failure</span></span>

<span data-ttu-id="c872a-125">如果数据库连接配置正确，您将收到与此类似的输出，其中 "成功" 属性标记为 **True**：</span><span class="sxs-lookup"><span data-stu-id="c872a-125">If database connectivity is configured correctly, you'll receive output similar to this, with the Succeed property marked as **True**:</span></span>

<span data-ttu-id="c872a-126">SqlServerFqdn： atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c872a-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="c872a-127">SqlInstanceName： rtc</span><span class="sxs-lookup"><span data-stu-id="c872a-127">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c872a-128">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c872a-128">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c872a-129">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c872a-129">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c872a-130">DatabaseName： xds</span><span class="sxs-lookup"><span data-stu-id="c872a-130">DatabaseName : xds</span></span>

<span data-ttu-id="c872a-131">数据源</span><span class="sxs-lookup"><span data-stu-id="c872a-131">DataSource :</span></span>

<span data-ttu-id="c872a-132">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-132">SQLServerVersion :</span></span>

<span data-ttu-id="c872a-133">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="c872a-133">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="c872a-134">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-134">InstalledVersion :</span></span>

<span data-ttu-id="c872a-135">成功： True</span><span class="sxs-lookup"><span data-stu-id="c872a-135">Succeed : True</span></span>

<span data-ttu-id="c872a-136">SqlServerFqdn： atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c872a-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="c872a-137">SqlInstanceName： rtc</span><span class="sxs-lookup"><span data-stu-id="c872a-137">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c872a-138">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c872a-138">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c872a-139">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c872a-139">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c872a-140">DatabaseName： .lis</span><span class="sxs-lookup"><span data-stu-id="c872a-140">DatabaseName : lis</span></span>

<span data-ttu-id="c872a-141">数据源</span><span class="sxs-lookup"><span data-stu-id="c872a-141">DataSource :</span></span>

<span data-ttu-id="c872a-142">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-142">SQLServerVersion :</span></span>

<span data-ttu-id="c872a-143">ExpectedVersion : 3.1.1</span><span class="sxs-lookup"><span data-stu-id="c872a-143">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="c872a-144">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-144">InstalledVersion :</span></span>

<span data-ttu-id="c872a-145">成功： True</span><span class="sxs-lookup"><span data-stu-id="c872a-145">Succeed : True</span></span>

<span data-ttu-id="c872a-146">如果数据库配置正确但仍可用，则 "成功" 字段将显示为 **False**，并且将提供其他警告和信息：</span><span class="sxs-lookup"><span data-stu-id="c872a-146">If the database is configured correctly but still available, the Succeed field will be shown as **False**, and additional warnings and information will be provided:</span></span>

<span data-ttu-id="c872a-147">SqlServerFqdn： atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c872a-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="c872a-148">SqlInstanceName： rtc</span><span class="sxs-lookup"><span data-stu-id="c872a-148">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c872a-149">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c872a-149">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c872a-150">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c872a-150">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c872a-151">DatabaseName： xds</span><span class="sxs-lookup"><span data-stu-id="c872a-151">DatabaseName : xds</span></span>

<span data-ttu-id="c872a-152">数据源</span><span class="sxs-lookup"><span data-stu-id="c872a-152">DataSource :</span></span>

<span data-ttu-id="c872a-153">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-153">SQLServerVersion :</span></span>

<span data-ttu-id="c872a-154">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="c872a-154">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="c872a-155">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-155">InstalledVersion :</span></span>

<span data-ttu-id="c872a-156">成功： False</span><span class="sxs-lookup"><span data-stu-id="c872a-156">Succeed : False</span></span>

<span data-ttu-id="c872a-157">SqlServerFqdn： atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c872a-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c872a-158">SqlInstanceName： rtc</span><span class="sxs-lookup"><span data-stu-id="c872a-158">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c872a-159">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c872a-159">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c872a-160">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c872a-160">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c872a-161">DatabaseName： .lis</span><span class="sxs-lookup"><span data-stu-id="c872a-161">DatabaseName : lis</span></span>

<span data-ttu-id="c872a-162">数据源</span><span class="sxs-lookup"><span data-stu-id="c872a-162">DataSource :</span></span>

<span data-ttu-id="c872a-163">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-163">SQLServerVersion :</span></span>

<span data-ttu-id="c872a-164">ExpectedVersion : 3.1.1</span><span class="sxs-lookup"><span data-stu-id="c872a-164">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="c872a-165">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="c872a-165">InstalledVersion :</span></span>

<span data-ttu-id="c872a-166">成功： False</span><span class="sxs-lookup"><span data-stu-id="c872a-166">Succeed : False</span></span>

<span data-ttu-id="c872a-167">警告： Test-CsDatabase 遇到错误。</span><span class="sxs-lookup"><span data-stu-id="c872a-167">WARNING: Test-CsDatabase encountered errors.</span></span> <span data-ttu-id="c872a-168">请参阅日志文件获取</span><span class="sxs-lookup"><span data-stu-id="c872a-168">Consult the log file for a</span></span>

<span data-ttu-id="c872a-169">详细分析，并确保所有错误 (2) 和警告 (0) 已解决</span><span class="sxs-lookup"><span data-stu-id="c872a-169">detailed analysis, and to make sure that all errors (2) and warnings (0) are addressed</span></span>

<span data-ttu-id="c872a-170">然后再继续。</span><span class="sxs-lookup"><span data-stu-id="c872a-170">before continuing.</span></span>

<span data-ttu-id="c872a-171">警告：可以在以下位置找到详细结果</span><span class="sxs-lookup"><span data-stu-id="c872a-171">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="c872a-172">"C： \\ 用户 \\ 测试 \\ AppData \\ 本地 \\ 温度 \\ 2 \\ 测试-CsDatabase-b18d488a-8044-4679-bbf2-</span><span class="sxs-lookup"><span data-stu-id="c872a-172">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsDatabase-b18d488a-8044-4679-bbf2-</span></span>

<span data-ttu-id="c872a-173">04d593cce8e6.html "。</span><span class="sxs-lookup"><span data-stu-id="c872a-173">04d593cce8e6.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c872a-174">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="c872a-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="c872a-175">下面是 **测试 CsDatabase** 可能失败的一些常见原因：</span><span class="sxs-lookup"><span data-stu-id="c872a-175">Here are some common reasons why **Test-CsDatabase** might fail:</span></span>

  - <span data-ttu-id="c872a-176">提供的参数值不正确。</span><span class="sxs-lookup"><span data-stu-id="c872a-176">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="c872a-177">如果使用，则必须正确配置可选参数，否则测试将失败。</span><span class="sxs-lookup"><span data-stu-id="c872a-177">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="c872a-178">重新运行不带可选参数的命令，并查看是否成功。</span><span class="sxs-lookup"><span data-stu-id="c872a-178">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="c872a-179">如果数据库配置错误或尚未部署，此命令将失败。</span><span class="sxs-lookup"><span data-stu-id="c872a-179">This command will fail if the database is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c872a-180">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c872a-180">See Also</span></span>


[<span data-ttu-id="c872a-181">Get-CsDatabaseMirrorState</span><span class="sxs-lookup"><span data-stu-id="c872a-181">Get-CsDatabaseMirrorState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDatabaseMirrorState)  
[<span data-ttu-id="c872a-182">CsService</span><span class="sxs-lookup"><span data-stu-id="c872a-182">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="c872a-183">Get-CsUserDatabaseState</span><span class="sxs-lookup"><span data-stu-id="c872a-183">Get-CsUserDatabaseState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserDatabaseState)  
  

<span data-ttu-id="c872a-184"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c872a-184"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

