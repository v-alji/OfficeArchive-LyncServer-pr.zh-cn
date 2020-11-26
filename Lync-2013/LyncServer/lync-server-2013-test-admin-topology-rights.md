---
title: Lync Server 2013：测试管理员拓扑权限
description: Lync Server 2013：测试管理员拓扑权限。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin topology rights
ms:assetid: 0c03b7fd-449a-47ad-8263-ce811164cbce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767943(v=OCS.15)
ms:contentKeyID: 63969575
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22d713297d0e944c7acbc5efcb11b21ea1b26639
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441275"
---
# <a name="test-admin-topology-rights-in-lync-server-2013"></a><span data-ttu-id="42409-103">Lync Server 2013 中的测试管理员拓扑权限</span><span class="sxs-lookup"><span data-stu-id="42409-103">Test admin topology rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42409-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42409-104">

<span> </span></span></span>

<span data-ttu-id="42409-105">_**主题上次修改时间：** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="42409-105">_**Topic Last Modified:** 2016-12-08_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42409-106">验证计划</span><span class="sxs-lookup"><span data-stu-id="42409-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="42409-107">初始 Lync Server 部署后。</span><span class="sxs-lookup"><span data-stu-id="42409-107">After initial Lync Server deployment.</span></span> <span data-ttu-id="42409-108">如果出现权限相关问题，则根据需要。</span><span class="sxs-lookup"><span data-stu-id="42409-108">As needed if permission-related issues arise.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42409-109">测试工具</span><span class="sxs-lookup"><span data-stu-id="42409-109">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="42409-110">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="42409-110">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42409-111">需要权限</span><span class="sxs-lookup"><span data-stu-id="42409-111">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="42409-112">当使用 Lync Server 命令行管理程序在本地运行时，用户必须是 RTCUniversalServerAdmins 安全组的成员。</span><span class="sxs-lookup"><span data-stu-id="42409-112">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="42409-113">使用 Windows PowerShell 的远程实例运行时，必须向用户分配具有运行 Test-CsSetupPermission cmdlet 权限的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="42409-113">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="42409-114">若要查看可使用此 cmdlet 的所有 RBAC 角色的列表，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="42409-114">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsSetupPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="42409-115">说明</span><span class="sxs-lookup"><span data-stu-id="42409-115">Description</span></span>

<span data-ttu-id="42409-116">默认情况下，只有域管理员可以启用 Lync Server 拓扑，并对 Lync Server 基础结构进行较大的更改。</span><span class="sxs-lookup"><span data-stu-id="42409-116">By default, only domain administrators can enable a Lync Server topology and make large changes to the Lync Server infrastructure.</span></span> <span data-ttu-id="42409-117">只要您的域管理员和您的 Lync 服务器管理员是同一个，这就不会出现问题。在许多组织中，Lync Server 管理员不拥有对整个域的管理权限。</span><span class="sxs-lookup"><span data-stu-id="42409-117">This won't be a problem as long as your domain administrators and your Lync Server administrators are one and the same.In many organizations Lync Server administrators do not hold administrative rights to the whole domain.</span></span> <span data-ttu-id="42409-118">默认情况下，这意味着这些管理员 (定义为 RTCUniversalServerAdmins 组的成员) 无法进行 Lync 服务器拓扑更改。</span><span class="sxs-lookup"><span data-stu-id="42409-118">By default, that means that these administrators (defined as members of the RTCUniversalServerAdmins group) can't make Lync Server topology changes.</span></span> <span data-ttu-id="42409-119">若要为 RTCUniversalServerAdmins 组的成员授予拓扑更改权限，必须通过使用 [CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) cmdlet 分配所需的 Active Directory 权限。</span><span class="sxs-lookup"><span data-stu-id="42409-119">To give members of the RTCUniversalServerAdmins group the right to make topology changes, you must assign the required Active Directory permissions by using the [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="42409-120">Test-CsSetupPermission cmdlet 验证在指定的 Active Directory 容器上配置安装 Lync Server 或其组件之一所需的权限。</span><span class="sxs-lookup"><span data-stu-id="42409-120">The Test-CsSetupPermission cmdlet verifies that the required permissions that are needed to install Lync Server or one of its components are configured on the specified Active Directory container.</span></span> <span data-ttu-id="42409-121">如果未分配权限，则可以运行 Grant-CsSetupPermission cmdlet 以向 RTCUniversalServerAdmins 组的成员授予安装和启用 Lync Server 的权限。</span><span class="sxs-lookup"><span data-stu-id="42409-121">If the permissions are not assigned, you can then run the Grant-CsSetupPermission cmdlet to give members of the RTCUniversalServerAdmins group the right to install and enable Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="42409-122">有关由授权 CsSetupPermission 分配的权限的详细列表，请参阅博客帖子 <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">授予-CsSetupPermission 和 Grant CsOUPermission</A>。</span><span class="sxs-lookup"><span data-stu-id="42409-122">For a detailed list of permissions assigned by Grant-CsSetupPermission, see the blog post <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">Grant-CsSetupPermission and Grant-CsOUPermission</A>.</span></span>



</div>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="42409-123">运行测试</span><span class="sxs-lookup"><span data-stu-id="42409-123">Running the test</span></span>

<span data-ttu-id="42409-124">若要确定是否为 Active Directory 容器分配了设置权限，请调用 Test-CsSetupPermission cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42409-124">To determine whether setup permissions are assigned for an Active Directory container, call the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="42409-125">指定要检查的容器的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="42409-125">Specify the distinguished name of the container to be checked.</span></span> <span data-ttu-id="42409-126">例如，此命令将验证容器 ou = CsServers、dc = litwareinc、dc = com 的设置权限：</span><span class="sxs-lookup"><span data-stu-id="42409-126">For example, this command verifies setup permissions on the container ou=CsServers,dc=litwareinc,dc=com:</span></span>

    Test-CsSetupPermission -ComputerOU "ou=CsServers,dc=litwareinc,dc=com"

<span data-ttu-id="42409-127">有关详细信息，请参阅 [CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="42409-127">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="42409-128">确定成功还是失败</span><span class="sxs-lookup"><span data-stu-id="42409-128">Determining success or failure</span></span>

<span data-ttu-id="42409-129">如果 Test-CsSetupPermission 确定已在 Active Directory 容器上设置了所需的权限，则 cmdlet 将返回值 True：</span><span class="sxs-lookup"><span data-stu-id="42409-129">If Test-CsSetupPermission determines that the required permissions have already been set on an Active Directory container then the cmdlet will return the value True:</span></span>

<span data-ttu-id="42409-130">True</span><span class="sxs-lookup"><span data-stu-id="42409-130">True</span></span>

<span data-ttu-id="42409-131">如果未设置权限，Test-CsSetupPermission 将返回值 False。</span><span class="sxs-lookup"><span data-stu-id="42409-131">If permissions are not set, Test-CsSetupPermission will return the value False.</span></span> <span data-ttu-id="42409-132">请注意，此值通常会包含在许多警告消息中。</span><span class="sxs-lookup"><span data-stu-id="42409-132">Note that this value will typically be enclosed in many warning messages.</span></span> <span data-ttu-id="42409-133">例如：</span><span class="sxs-lookup"><span data-stu-id="42409-133">For example:</span></span>

<span data-ttu-id="42409-134">警告： (ACE) atl-001 RTCUniversalServerAdmins 中的访问控制项 \\帮助ExtendedRight;尚尚1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span><span class="sxs-lookup"><span data-stu-id="42409-134">WARNING: Access control entry (ACE) atl-cs-001\\RTCUniversalServerAdmins; Allow; ExtendedRight; None; None; 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span></span>

<span data-ttu-id="42409-135">警告： (Ace) 对象 "CN = 计算机，DC = litwareinc，DC = com" 的访问控制条目尚未准备就绪。</span><span class="sxs-lookup"><span data-stu-id="42409-135">WARNING: The access control entries (ACEs) on the object "CN=Computers,DC=litwareinc,DC=com" are not ready.</span></span>

<span data-ttu-id="42409-136">False</span><span class="sxs-lookup"><span data-stu-id="42409-136">False</span></span>

<span data-ttu-id="42409-137">警告： "Test-CsSetupPermission" 处理已完成，但出现警告。</span><span class="sxs-lookup"><span data-stu-id="42409-137">WARNING: "Test-CsSetupPermission" processing has completed with warnings.</span></span> <span data-ttu-id="42409-138">此运行期间录制了 "2" 条警告。</span><span class="sxs-lookup"><span data-stu-id="42409-138">"2" warnings were recorded during this run.</span></span>

<span data-ttu-id="42409-139">警告：可以在 "C： \\ 用户 \\ 管理员 \\ AppData \\ 本地 \\ 临时 \\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html" 处找到详细结果。</span><span class="sxs-lookup"><span data-stu-id="42409-139">WARNING: Detailed results can be found at "C:\\Users\\Admin\\AppData\\Local\\Temp\\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="42409-140">测试可能失败的原因</span><span class="sxs-lookup"><span data-stu-id="42409-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="42409-141">虽然不太常见的例外情况，但如果 Test-CsSetupPermission 失败通常意味着不会为指定的 Active Directory 容器分配设置权限。</span><span class="sxs-lookup"><span data-stu-id="42409-141">Although there are rare exceptions, if Test-CsSetupPermission fails that typically means that setup permissions are not assigned for the specified Active Directory container.</span></span> <span data-ttu-id="42409-142">可以使用 Grant-CsSetupPermission cmdlet 分配这些权限。</span><span class="sxs-lookup"><span data-stu-id="42409-142">Those permissions can be assigned by using the Grant-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="42409-143">例如，此命令向域 litwareinc.com 中的计算机容器授予设置权限：</span><span class="sxs-lookup"><span data-stu-id="42409-143">For example, this command grants setup permissions to the Computers container in the domain litwareinc.com:</span></span>

    Grant-CsSetupPermission -ComputerOU "cn=Computers,dc=litwareinc,dc=com"

<span data-ttu-id="42409-144">有关详细信息，请参阅 [CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="42409-144">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="42409-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42409-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

