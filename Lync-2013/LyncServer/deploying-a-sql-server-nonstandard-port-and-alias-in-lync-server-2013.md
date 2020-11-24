---
title: 在 Lync Server 2013 中部署一个 SQL Server 非标准端口和别名。
description: 在 Lync Server 2013 中部署 SQL Server 非标准端口和别名。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a SQL Server nonstandard port and alias in Lync Server 2013
ms:assetid: 2da92c1f-250e-407a-8651-fb2aec76aeb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn776290(v=OCS.15)
ms:contentKeyID: 62634609
ms.date: 09/17/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da76db2b946a47e13fe3549d7184b0b12894a83a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391856"
---
# <a name="deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="ab040-103">在 Lync Server 2013 中部署一个 SQL Server 非标准端口和别名。</span><span class="sxs-lookup"><span data-stu-id="ab040-103">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab040-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab040-104">

<span> </span></span></span>

<span data-ttu-id="ab040-105">_**主题上次修改时间：** 2015-09-16_</span><span class="sxs-lookup"><span data-stu-id="ab040-105">_**Topic Last Modified:** 2015-09-16_</span></span>

<span data-ttu-id="ab040-106">Microsoft Lync Server 2013 支持在 SQL Server 中使用非标准端口和别名。</span><span class="sxs-lookup"><span data-stu-id="ab040-106">Microsoft Lync Server 2013 supports using a non-standard port and alias in SQL Server.</span></span> <span data-ttu-id="ab040-107">使用 SQL Server 非标准端口和别名可提高安全性，并为 Lync 部署创建更灵活的环境。</span><span class="sxs-lookup"><span data-stu-id="ab040-107">Using a SQL Server non-standard port and an alias increases security and creates a more flexible environment for the Lync deployment.</span></span> <span data-ttu-id="ab040-108">这些步骤只是妥善保护 Lync Server 2013 环境的一个步骤。</span><span class="sxs-lookup"><span data-stu-id="ab040-108">These steps are only a single step in properly securing your Lync Server 2013 environment.</span></span> <span data-ttu-id="ab040-109">应采取其他步骤来减少 Lync Server 2013 实现的受攻击面。</span><span class="sxs-lookup"><span data-stu-id="ab040-109">Additional steps should be taken to reduce the attack surface of a Lync Server 2013 implementation.</span></span>

<span data-ttu-id="ab040-110">以下文章介绍了在 Lync Server 2013 中设置 SQL Server 非标准端口和别名所需的步骤。</span><span class="sxs-lookup"><span data-stu-id="ab040-110">The following article describes the steps required to setup a SQL Server non-standard port and alias in Lync Server 2013.</span></span>

<div>

## <a name="deploying-a-sql-server-non-standard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="ab040-111">在 Lync Server 2013 中部署 SQL Server 非标准端口和别名</span><span class="sxs-lookup"><span data-stu-id="ab040-111">Deploying a SQL Server Non-Standard Port and Alias in Lync Server 2013</span></span>

<span data-ttu-id="ab040-112">Lync Server 2013 拓扑生成器支持在配置 Lync Server 2013 时使用 SQL Server 别名作为完全限定的域名 (FQDN) ，而不是实际的 SQL Server FQDN。</span><span class="sxs-lookup"><span data-stu-id="ab040-112">Lync Server 2013 Topology Builder supports using a SQL Server alias as the Fully Qualified Domain Name (FQDN) instead of the actual SQL Server FQDN when configuring Lync Server 2013.</span></span> <span data-ttu-id="ab040-113">这允许对任何恶意攻击者隐藏实际的 SQL Server FQDN。</span><span class="sxs-lookup"><span data-stu-id="ab040-113">This allows the actual SQL Server FQDN to be hidden from any malicious attacker.</span></span> <span data-ttu-id="ab040-114">此外，使用非标准端口遮盖实际端口，攻击者试图在标准端口1433上攻击数据库，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-114">In addition, using a non-standard port obscures the actual port from any would be attacker attempting to attack the database on the standard port 1433, as shown in the following figure.</span></span>

<span data-ttu-id="ab040-115">![黑客不知道要攻击的端口号。](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "黑客不知道要攻击的端口号。")</span><span class="sxs-lookup"><span data-stu-id="ab040-115">![A hacker doesn't know the port number to attack.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "A hacker doesn't know the port number to attack.")</span></span>

<span data-ttu-id="ab040-116">为了成功确定 Lync Server 2013 正在使用的端口与 SQL Server 通信，攻击者需要扫描所有端口以获取端口信息。</span><span class="sxs-lookup"><span data-stu-id="ab040-116">In order to be successful in determining the port Lync Server 2013 is using to communicate with SQL Server, the attacker would need to scan all ports to obtain the port information.</span></span> <span data-ttu-id="ab040-117">由攻击者进行的端口扫描增加了安全检测和停止指令的机会。</span><span class="sxs-lookup"><span data-stu-id="ab040-117">A port scan by an attacker increases the chances that security can detect and stop the instruction.</span></span> <span data-ttu-id="ab040-118">除了使用非标准端口增加安全性外，你还可以使用 SQL Server 别名为部署提供灵活性。</span><span class="sxs-lookup"><span data-stu-id="ab040-118">In addition to adding increased security with a non-standard port, you can also use a SQL Server alias to provide flexibility for the deployment.</span></span> <span data-ttu-id="ab040-119">这非常有用，以便减少需要更改 SQL Server 名称的情况下的配置更改。</span><span class="sxs-lookup"><span data-stu-id="ab040-119">This is valuable in order to reduce configuration changes in situations where a SQL Server name change is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ab040-120">SQL Server 提供两种容错方法 (故障转移群集和镜像) 。</span><span class="sxs-lookup"><span data-stu-id="ab040-120">SQL Server provides two fault tolerance methods (Failover Clustering and Mirroring).</span></span> <span data-ttu-id="ab040-121">使用 SQL Server 非标准端口和使用 Lync Server 2013 的别名均支持这两种 SQL Server 容错方法。</span><span class="sxs-lookup"><span data-stu-id="ab040-121">Both SQL Server fault tolerance methods are supported using a SQL Server non-standard port and alias with Lync Server 2013.</span></span> <span data-ttu-id="ab040-122">如果池使用的 SQL Server 后端位于镜像配置中，则 SQL Server 后端服务器上的 SQL 浏览器服务应在数据库故障转移到镜像 SQL Server 时运行，以便连接到镜像数据库。</span><span class="sxs-lookup"><span data-stu-id="ab040-122">If the SQL Server backend used by the pool is in a mirrored configuration, then the SQL browser service on the SQL Server backend servers should be running for Front End servers to connect to the mirrored database when the databases are failed over to the mirrored SQL Server.</span></span>



</div>

<span data-ttu-id="ab040-123">在从拓扑生成器内部配置 SQL Server 数据库连接时，或者在使用 Install-CsDatabase cmdlet 时，不可能显式定义 SQL Server 非标准端口号并将其与 SQL 实例关联。</span><span class="sxs-lookup"><span data-stu-id="ab040-123">When configuring SQL Server database connectivity from within Topology Builder, or when using the Install-CsDatabase cmdlet, it’s not possible to explicitly define a SQL Server non-standard port number and associate it with a SQL instance.</span></span> <span data-ttu-id="ab040-124">若要设置非标准端口，需要使用 SQL Server 和 Windows Server 实用工具。</span><span class="sxs-lookup"><span data-stu-id="ab040-124">To set a non-standard port, you’ll need to use SQL Server and Windows Server utilities.</span></span>

<span data-ttu-id="ab040-125">若要设置用于 Lync Server 2013 的 SQL Server 非标准端口和别名，您需要完成三个主要步骤。</span><span class="sxs-lookup"><span data-stu-id="ab040-125">To set up a SQL Server non-standard port and alias for use with Lync Server 2013, you will need to complete three primary steps.</span></span> <span data-ttu-id="ab040-126">这些步骤如下：</span><span class="sxs-lookup"><span data-stu-id="ab040-126">These steps are:</span></span>

  - <span data-ttu-id="ab040-127">确认 Lync Server 2013 已应用最新的更新。</span><span class="sxs-lookup"><span data-stu-id="ab040-127">Confirm that Lync Server 2013 has the Latest Updates Applied.</span></span>

  - <span data-ttu-id="ab040-128">设置 SQL Server 非标准端口和别名。</span><span class="sxs-lookup"><span data-stu-id="ab040-128">Setup the SQL Server Non-Standard Port and Alias.</span></span>

  - <span data-ttu-id="ab040-129">使用拓扑生成器使用 SQL Server 别名配置 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="ab040-129">Configure Lync Server 2013 with the SQL Server alias using Topology Builder.</span></span>

  - <span data-ttu-id="ab040-130">发布拓扑，并验证数据库。</span><span class="sxs-lookup"><span data-stu-id="ab040-130">Publish the Topology, and Verify the Database.</span></span>

<div>

## <a name="confirm-that-lync-server-2013-has-the-latest-updates-applied"></a><span data-ttu-id="ab040-131">确认 Lync Server 2013 已应用最新的更新</span><span class="sxs-lookup"><span data-stu-id="ab040-131">Confirm that Lync Server 2013 has the Latest Updates Applied</span></span>

<span data-ttu-id="ab040-132">将 Lync Server 2013 保持最新非常重要。</span><span class="sxs-lookup"><span data-stu-id="ab040-132">It is important to keep Lync Server 2013 up to date.</span></span> <span data-ttu-id="ab040-133">若要查看有关如何应用的最新更新和信息，请参阅 [Lync Server 2013 更新](https://support.microsoft.com/kb/2809243)。</span><span class="sxs-lookup"><span data-stu-id="ab040-133">To check for the most recent updates and information on how to apply them, see [Updates for Lync Server 2013](https://support.microsoft.com/kb/2809243).</span></span>

</div>

<div>

## <a name="setup-the-sql-server-non-standard-port-and-alias"></a><span data-ttu-id="ab040-134">设置 SQL Server 非标准端口和别名</span><span class="sxs-lookup"><span data-stu-id="ab040-134">Setup the SQL Server Non-Standard Port and Alias</span></span>

<span data-ttu-id="ab040-135">必须先在数据库实例上设置 SQL Server 非标准端口和别名，然后才能从 Lync Server 2013 拓扑生成器中引用它。</span><span class="sxs-lookup"><span data-stu-id="ab040-135">The SQL Server non-standard port and alias must be set up on the database instance before it can be referenced from Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="ab040-136">若要设置 SQL Server 非标准端口和别名，您将必须完成三个主要步骤。</span><span class="sxs-lookup"><span data-stu-id="ab040-136">To set up a SQL Server non-standard port and alias, you will have to complete three primary steps.</span></span> <span data-ttu-id="ab040-137">这些步骤如下所示：</span><span class="sxs-lookup"><span data-stu-id="ab040-137">These steps are as follows:</span></span>

  - <span data-ttu-id="ab040-138">更改默认的 TCP/IP 协议值。</span><span class="sxs-lookup"><span data-stu-id="ab040-138">Change the Default TCP/IP Protocol Values.</span></span>

  - <span data-ttu-id="ab040-139">创建和配置 SQL Server 别名。</span><span class="sxs-lookup"><span data-stu-id="ab040-139">Create and Configure a SQL Server Alias.</span></span>

  - <span data-ttu-id="ab040-140">创建域名系统 (DNS) 规范名称 (CNAME) 资源记录。</span><span class="sxs-lookup"><span data-stu-id="ab040-140">Create a Domain Name System (DNS) Canonical Name (CNAME) Resource Record.</span></span>

<span data-ttu-id="ab040-141">**修改默认 TCP/IP 协议值**</span><span class="sxs-lookup"><span data-stu-id="ab040-141">**Modify the Default TCP/IP Protocol Values**</span></span>

1.  <span data-ttu-id="ab040-142">选择 " **开始**"，然后选择 " **SQL Server 配置管理器**"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-142">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-143">![SQL Server Management Studio 图标](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "SQL Server Management Studio 图标")</span><span class="sxs-lookup"><span data-stu-id="ab040-143">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="ab040-144">在导航窗格中，选择展开 **Sql server 实例**，选择展开 " **Sql server 网络配置**"，然后 **\<instance name\>** 选择 "协议"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-144">In the navigation pane, choose to expand the **SQL Server instance**, choose to expand **SQL Server Network Configuration**, and choose **Protocols for \<instance name\>**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-145">![导航到 TCP/IP 属性](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "导航到 TCP/IP 属性")</span><span class="sxs-lookup"><span data-stu-id="ab040-145">![Navigate to TCP/IP Properties](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navigate to TCP/IP Properties")</span></span>

3.  <span data-ttu-id="ab040-146">在右窗格中，右键单击 " **tcp/ip**"，然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="ab040-146">In the right pane, right-click **TCP/IP**, and select **Properties**.</span></span> <span data-ttu-id="ab040-147">将显示 "TCP/IP 属性" 对话框。</span><span class="sxs-lookup"><span data-stu-id="ab040-147">The TCP/IP Properties dialog box is displayed.</span></span>

4.  <span data-ttu-id="ab040-148">选择 " **IP 地址** " 选项卡。"IP 地址" 选项卡显示服务器上的所有活动 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="ab040-148">Select the **IP Addresses** tab. The IP Addresses tab shows all of the active IP addresses on the server.</span></span> <span data-ttu-id="ab040-149">这些格式的格式为 IP1、IP2、最高 IPAll，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-149">These are in the format IP1, IP2, up to IPAll, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-150">![打开 TCP/IP 属性。](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "打开 TCP/IP 属性。")</span><span class="sxs-lookup"><span data-stu-id="ab040-150">![Open TCP/IP properties.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Open TCP/IP properties.")</span></span>

5.  <span data-ttu-id="ab040-151">清除所有 IP 地址的 " **TCP 动态端口** " 字段。</span><span class="sxs-lookup"><span data-stu-id="ab040-151">Clear the **TCP Dynamic Ports** field for all IP addresses.</span></span> <span data-ttu-id="ab040-152">如果该字段包含零个字符，则表示 SQL Server 正在侦听动态端口。</span><span class="sxs-lookup"><span data-stu-id="ab040-152">If the field contains a zero character, then it means SQL Server is listening on dynamic ports.</span></span> <span data-ttu-id="ab040-153">请确保这些字段已清除且不包含零。</span><span class="sxs-lookup"><span data-stu-id="ab040-153">Make sure these fields are cleared and do not contain a zero.</span></span>

6.  <span data-ttu-id="ab040-154">对于 Lync 服务器将用于连接到数据库的 IP 地址，请确保 " **已启用** " 设置为 **"是"**，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-154">For the IP address that Lync Server will be using to connect to the database, make sure that **Enabled** is set to **Yes**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-155">![对于正确 IP 将“启用”设置为“是”。](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "对于正确 IP 将“启用”设置为“是”。")</span><span class="sxs-lookup"><span data-stu-id="ab040-155">![Set enabled as Yes for the correct IP.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Set enabled as Yes for the correct IP.")</span></span>

7.  <span data-ttu-id="ab040-156">在对话框底部的 " **IPAll** " 部分中，在 " **TCP 端口** " 字段中输入所需的端口，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-156">In the **IPAll** section at the bottom of the dialog, enter the desired port in the **TCP Port** field, as shown in the following figure.</span></span> <span data-ttu-id="ab040-157">在此示例中，我们使用端口50062，但你可以使用49152和65535之间的任何端口。</span><span class="sxs-lookup"><span data-stu-id="ab040-157">In this example, we use port 50062, but you can use any port between 49152 and 65535.</span></span> <span data-ttu-id="ab040-158">这些端口分配给动态和专用用途，这可确保您不会与 Lync Server 2013 部署中使用的其他端口发生冲突。</span><span class="sxs-lookup"><span data-stu-id="ab040-158">These are the ports assigned to dynamic and private use, and this ensures you won’t conflict with other ports being used in the Lync Server 2013 deployment.</span></span>
    
    <span data-ttu-id="ab040-159">![在 IPAll 部分中设置端口。](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "在 IPAll 部分中设置端口。")</span><span class="sxs-lookup"><span data-stu-id="ab040-159">![Set port in IPAll section.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Set port in IPAll section.")</span></span>

8.  <span data-ttu-id="ab040-160">选择 **"确定"** 以退出 "tcp/ip 属性" 对话框。</span><span class="sxs-lookup"><span data-stu-id="ab040-160">Choose **OK** to exit the TCP/IP Properties dialog.</span></span>

9.  <span data-ttu-id="ab040-161">通过在 SQL Server 配置管理器的左窗格中选择 " **Sql Server 服务** "，重新启动 sql server 实例。</span><span class="sxs-lookup"><span data-stu-id="ab040-161">Restart the SQL Server instance by selecting **SQL Server Services** in the left pane of SQL Server Configuration Manager.</span></span> <span data-ttu-id="ab040-162">然后右键单击右窗格中的 " **SQL Server \<instance name\>** "，然后选择 "**重启**"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-162">Then right-click **SQL Server \<instance name\>** in the right pane, and select **Restart**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-163">![针对实例重置 SQL Server 服务。](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "针对实例重置 SQL Server 服务。")</span><span class="sxs-lookup"><span data-stu-id="ab040-163">![Reset the SQL Server service for instance.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Reset the SQL Server service for instance.")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ab040-164">请确保更新防火墙设置以适应新的 SQL Server 端口。</span><span class="sxs-lookup"><span data-stu-id="ab040-164">Make sure you update your firewall settings to accommodate the new SQL Server port.</span></span>



</div>

<span data-ttu-id="ab040-165">**创建和配置 SQL Server 别名**</span><span class="sxs-lookup"><span data-stu-id="ab040-165">**Create and Configure a SQL Server Alias**</span></span>

1.  <span data-ttu-id="ab040-166">选择 " **开始**"，然后选择 " **SQL Server 配置管理器**"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-166">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-167">![SQL Server Management Studio 图标](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "SQL Server Management Studio 图标")</span><span class="sxs-lookup"><span data-stu-id="ab040-167">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="ab040-168">在左窗格中，选择展开 " **Sql Server 实例**"，选择展开 " **sql Native Client \<version\> 配置**"，然后选择 " **别名**"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-168">In the left pane, choose to expand **SQL Server instance**, choose to expand **SQL Native Client \<version\> Configuration**, and then choose **Aliases**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-169">![SQL Server 配置管理器中的别名。](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "SQL Server 配置管理器中的别名。")</span><span class="sxs-lookup"><span data-stu-id="ab040-169">![Aliases in SQL Server Configuration Manager.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliases in SQL Server Configuration Manager.")</span></span>

3.  <span data-ttu-id="ab040-170">右键单击 " **别名**"，然后选择 " **新建别名 ...**"。</span><span class="sxs-lookup"><span data-stu-id="ab040-170">Right-click **Aliases**, and select **New Alias…**.</span></span>

4.  <span data-ttu-id="ab040-171">输入 **别名名称**、 **端口号**、 **协议** 和 **服务器**，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-171">Enter the **Alias Name**, **Port Number**, **Protocol**, and **Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-172">![创建新别名](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "创建新别名")</span><span class="sxs-lookup"><span data-stu-id="ab040-172">![Creating a new alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Creating a new alias")</span></span>
    
    <div>
    

    > [!CAUTION]  
    > <span data-ttu-id="ab040-173">请确保输入与上一步骤中使用的非标准端口，因为该端口是 SQL Server 将侦听的端口。</span><span class="sxs-lookup"><span data-stu-id="ab040-173">Make sure to enter the same non-standard port you used in the previous step since that is the port SQL Server will be listening on.</span></span> <span data-ttu-id="ab040-174">如果配置的别名连接到错误的 SQL Server FQDN 或实例，请禁用并重新启用关联的网络协议。</span><span class="sxs-lookup"><span data-stu-id="ab040-174">If a configured alias is connecting to the wrong SQL Server FQDN or Instance, disable and then re-enable the associated network protocol.</span></span> <span data-ttu-id="ab040-175">执行此操作将清除任何缓存的连接信息，并允许客户端正确连接。</span><span class="sxs-lookup"><span data-stu-id="ab040-175">Doing this clears any cached connection information and allows the client to connect correctly.</span></span>

    
    </div>

<span data-ttu-id="ab040-176">**创建 DNS CNAME 资源记录**</span><span class="sxs-lookup"><span data-stu-id="ab040-176">**Create a DNS CNAME Resource Record**</span></span>

1.  <span data-ttu-id="ab040-177">登录到管理 DNS 的计算机。</span><span class="sxs-lookup"><span data-stu-id="ab040-177">Sign into the computer managing DNS.</span></span>

2.  <span data-ttu-id="ab040-178">选择 " **开始**"，然后选择 " **服务器管理器**"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-178">Select **Start**, and choose **Server Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-179">![打开服务器管理器](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "打开服务器管理器")</span><span class="sxs-lookup"><span data-stu-id="ab040-179">![Opening Server Manager](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Opening Server Manager")</span></span>

3.  <span data-ttu-id="ab040-180">选择 " **工具** " 下拉列表，然后选择 " **DNS**"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-180">Choose the **Tools** drop-down, and select **DNS**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-181">![从服务器管理器打开 DNS。](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "从服务器管理器打开 DNS。")</span><span class="sxs-lookup"><span data-stu-id="ab040-181">![Opening DNS from Server Manager.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Opening DNS from Server Manager.")</span></span>

4.  <span data-ttu-id="ab040-182">在左窗格中，展开 "服务器名称" 节点，展开 "正向查找区域" 节点，然后选择相关域。</span><span class="sxs-lookup"><span data-stu-id="ab040-182">In the left pane, expand the server name node, expand the Forward Lookup Zones node, and choose the relevant domain.</span></span>

5.  <span data-ttu-id="ab040-183">右键单击域，然后选择 " **新建别名 (CNAME) ...**"，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-183">Right-click the domain, and select **New Alias (CNAME)…**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-184">![选择创建新的别名 CNAME 的选项](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "选择创建新的别名 CNAME 的选项")</span><span class="sxs-lookup"><span data-stu-id="ab040-184">![Selecting option to create a new alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selecting option to create a new alias CNAME")</span></span>

6.  <span data-ttu-id="ab040-185">为 **SQL Server** 输入 **别名名称** 和 FQDN，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-185">Enter the **Alias Name** and the **FQDN for SQL Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-186">![填写 "新建别名 CNAME" 对话框。](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "填写 "新建别名 CNAME" 对话框。")</span><span class="sxs-lookup"><span data-stu-id="ab040-186">![Filling in the new alias CNAME dialog.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Filling in the new alias CNAME dialog.")</span></span>

7.  <span data-ttu-id="ab040-187">选择 **"确定"** 保存 CNAME 并在 DNS 管理器中查看。</span><span class="sxs-lookup"><span data-stu-id="ab040-187">Choose **OK** to save the CNAME and view it in DNS Manager.</span></span>

</div>

<div>

## <a name="validate-database-connectivity"></a><span data-ttu-id="ab040-188">验证数据库连接</span><span class="sxs-lookup"><span data-stu-id="ab040-188">Validate Database Connectivity</span></span>

<span data-ttu-id="ab040-189">有多种不同的方法可确保其正常工作。</span><span class="sxs-lookup"><span data-stu-id="ab040-189">There are many different ways to make sure it is working.</span></span> <span data-ttu-id="ab040-190">你希望确保 SQL Server 数据库使用别名在指定的端口上侦听。</span><span class="sxs-lookup"><span data-stu-id="ab040-190">You want to make sure that the SQL Server database is listening on the specified port using the alias.</span></span> <span data-ttu-id="ab040-191">可使用 **netstat** 和 **telnet** 命令完成快速检查。</span><span class="sxs-lookup"><span data-stu-id="ab040-191">A quick check can be completed using the **netstat** and **telnet** commands.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ab040-192">"Telnet 客户端" 是 Windows Server 附带的一项功能，必须安装。</span><span class="sxs-lookup"><span data-stu-id="ab040-192">Telnet Client is a Feature that comes with Windows Server but that must be installed.</span></span> <span data-ttu-id="ab040-193">可通过打开服务器管理器并从 "管理" 菜单中选择 "添加角色和功能" 来安装 Windows Server 功能。</span><span class="sxs-lookup"><span data-stu-id="ab040-193">A Windows Server Feature can be installed by opening Server Manager and selecting Add Roles and Features from the Manage menu.</span></span>



</div>

<span data-ttu-id="ab040-194">**使用 netstat 和 telnet 验证数据库连接**</span><span class="sxs-lookup"><span data-stu-id="ab040-194">**Use netstat and telnet to verify database connectivity**</span></span>

1.  <span data-ttu-id="ab040-195">选择 " **开始**"，然后键入 **cmd** 以打开命令提示符。</span><span class="sxs-lookup"><span data-stu-id="ab040-195">Select **Start**, and type **cmd** to open a command prompt.</span></span>

2.  <span data-ttu-id="ab040-196">键入 **netstat-a-f**，并确认 SQL Server 使用正确的端口运行，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="ab040-196">Type **netstat -a -f**, and confirm that SQL Server is running with the correct port, as shown in the following figure.</span></span>
    
    <span data-ttu-id="ab040-197">![使用 netstat 验证端口。](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "使用 netstat 验证端口。")</span><span class="sxs-lookup"><span data-stu-id="ab040-197">![Using netstat to verify port.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Using netstat to verify port.")</span></span>

3.  <span data-ttu-id="ab040-198">键入 **telnet \<alias name\> \<port \#\>** 以确认与 SQL Server 实例的连接。</span><span class="sxs-lookup"><span data-stu-id="ab040-198">Type **telnet \<alias name\> \<port \#\>** to confirm the connection to the SQL Server instance.</span></span> <span data-ttu-id="ab040-199">如果连接成功，telnet 将连接，您不会看到错误。</span><span class="sxs-lookup"><span data-stu-id="ab040-199">If the connection is successful, telnet will connect and you shouldn’t see an error.</span></span> <span data-ttu-id="ab040-200">这表明 SQL Server 实例在具有正确别名的正确端口上侦听。</span><span class="sxs-lookup"><span data-stu-id="ab040-200">This shows that the SQL Server instance is listening on the correct port with the correct alias.</span></span> <span data-ttu-id="ab040-201">如果连接到 SQL Server 数据库时出现问题，telnet 将显示一条错误消息，指出无法建立连接。</span><span class="sxs-lookup"><span data-stu-id="ab040-201">If there’s a problem connecting to the SQL Server database, then telnet shows an error that the connection cannot be made.</span></span> <span data-ttu-id="ab040-202">现在，你已在数据库服务器上检查了数据库连接，你可以通过网络) 从 Lync Server (执行相同的操作，并确保没有任何防火墙阻止访问。</span><span class="sxs-lookup"><span data-stu-id="ab040-202">Now that you have checked database connectivity on the database server, you can do the same thing from Lync Server (over the network) and make sure there aren’t any firewalls blocking access along the way.</span></span>

</div>

<div>

## <a name="conclusion"></a><span data-ttu-id="ab040-203">结论</span><span class="sxs-lookup"><span data-stu-id="ab040-203">Conclusion</span></span>

<span data-ttu-id="ab040-204">配置 SQL Server 别名后，您可以在拓扑生成器工具中使用它来创建 Lync Server 2013 拓扑。</span><span class="sxs-lookup"><span data-stu-id="ab040-204">Once the SQL Server alias has been configured, you can use it to create a Lync Server 2013 topology in the Topology Builder tool.</span></span> <span data-ttu-id="ab040-205">有关拓扑的详细信息，请参阅 [在 Lync Server 2013 中定义和配置拓扑](lync-server-2013-defining-and-configuring-the-topology.md)。</span><span class="sxs-lookup"><span data-stu-id="ab040-205">For more information about topologies, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ab040-206">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ab040-206">See Also</span></span>


<span data-ttu-id="ab040-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md)  
[Lync Server 2013 中的安全规划](lync-server-2013-planning-for-security.md)</span><span class="sxs-lookup"><span data-stu-id="ab040-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md) 
[Planning for security in Lync Server 2013](lync-server-2013-planning-for-security.md)</span></span>  
[<span data-ttu-id="ab040-208">在 Lync Server 2013 中定义和配置拓扑</span><span class="sxs-lookup"><span data-stu-id="ab040-208">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)  
[<span data-ttu-id="ab040-209">部署 Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab040-209">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="ab040-210"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab040-210"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

