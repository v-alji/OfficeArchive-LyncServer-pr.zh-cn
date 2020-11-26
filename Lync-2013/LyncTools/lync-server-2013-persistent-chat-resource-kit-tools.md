---
title: Lync Server 2013 持久聊天资源工具包工具
description: Lync Server 2013 持久聊天资源工具包工具。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Persistent Chat Resource Kit Tools
ms:assetid: 7a34d2ba-eb25-4e22-92d1-b9baf81b102c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945599(v=OCS.15)
ms:contentKeyID: 51541423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 336e81c97da73da47eee654161a7d8d8956f9edb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438416"
---
# <a name="lync-server-2013-persistent-chat-resource-kit-tools"></a><span data-ttu-id="1ad7c-103">Lync Server 2013 持久聊天资源工具包工具</span><span class="sxs-lookup"><span data-stu-id="1ad7c-103">Lync Server 2013 Persistent Chat Resource Kit Tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1ad7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1ad7c-104">

<span> </span></span></span>

<span data-ttu-id="1ad7c-105">_**主题上次修改时间：** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="1ad7c-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="1ad7c-106">Lync Server 2013 持久聊天资源工具包工具可帮助部署和管理 Lync Server 2013 持久聊天服务器的 IT 管理员更轻松地执行日常任务。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-106">The Lync Server 2013 Persistent Chat Resource Kit tools help to make routine tasks easier for IT administrators who deploy and manage Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="1ad7c-107">除了安装说明，本主题还介绍了每个工具的用途以及它的使用示例。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-107">In addition to installation instructions, this topic describes the purpose of each tool, and examples of its use.</span></span>

<div>

## <a name="installation-of-the-resource-kit-tools"></a><span data-ttu-id="1ad7c-108">安装资源管理包工具</span><span class="sxs-lookup"><span data-stu-id="1ad7c-108">Installation of the Resource Kit Tools</span></span>

<span data-ttu-id="1ad7c-109">若要安装 Lync Server 2013、资源工具包工具，请下载 **PersistentChatReskit.msi**。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-109">To install the Lync Server 2013, Resource Kit Tools, download **PersistentChatReskit.msi**.</span></span> <span data-ttu-id="1ad7c-110">运行 **PersistentChatReskit.msi** 以执行简单安装。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-110">Run **PersistentChatReskit.msi** to do a simple installation.</span></span> <span data-ttu-id="1ad7c-111">.Msi 将在以下路径中安装所有工具： \\ **程序文件 \\ Microsoft Lync Server 2013 \\ 持久聊天服务器资源工具包**。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-111">The .msi installs all the tools in the following path: \\**Program Files\\ Microsoft Lync Server 2013\\Persistent Chat Server Resource Kit**.</span></span> <span data-ttu-id="1ad7c-112">属于自包含可执行文件的工具位于此文件夹中。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-112">Tools that are self-contained executables are in this folder.</span></span> <span data-ttu-id="1ad7c-113">也有文件的工具位于它们自己的子文件夹中。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-113">Tools that also have files are in their own subfolders.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1ad7c-114">安装 Lync Server 2013 和资源工具包工具后，必须安装<STRONG>PsExec.exe</STRONG>并将<STRONG>PsExec.exe</STRONG>复制到以下路径： \\ <STRONG>程序文件 \ Microsoft Lync Server 2013 \ 持久聊天服务器资源 Kit\ChatStressTool</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-114">After installing the Lync Server 2013, Resource Kit Tools, you must install <STRONG>PsExec.exe</STRONG> and copy <STRONG>PsExec.exe</STRONG> to the following path: \\<STRONG>Program Files\ Microsoft Lync Server 2013\Persistent Chat Server Resource Kit\ChatStressTool</STRONG>.</span></span> <span data-ttu-id="1ad7c-115">如果不复制 <STRONG>PsExec.exe</STRONG>，持久聊天应力工具将引发错误异常，并且不会正确执行。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-115">If you do not copy <STRONG>PsExec.exe</STRONG>, the Persistent Chat Stress Tool will throw an error exception, and not perform correctly.</span></span> <span data-ttu-id="1ad7c-116">在运行该工具之前，请确保满足此先决条件要求。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-116">Make sure that you meet this prerequisite requirement prior to running the tool.</span></span> <span data-ttu-id="1ad7c-117">有关安装 <STRONG>PsExec.exe</STRONG>的详细信息，请参阅 <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A> 。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-117">For details about installing <STRONG>PsExec.exe</STRONG>, see <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A>.</span></span>



</div>

</div>

<div>

## <a name="supported-environments"></a><span data-ttu-id="1ad7c-118">支持的环境</span><span class="sxs-lookup"><span data-stu-id="1ad7c-118">Supported Environments</span></span>

<span data-ttu-id="1ad7c-119">为获得最佳性能，Lync Server 2013、资源工具包工具应安装在相同的环境中，并具有 Lync Server 2013 所需的相同规范。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-119">For optimal performance, the Lync Server 2013, Resource Kit Tools should be installed in the same environment and with the same specifications that are required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="resource-kit-tools-overview"></a><span data-ttu-id="1ad7c-120">资源管理包工具概述</span><span class="sxs-lookup"><span data-stu-id="1ad7c-120">Resource Kit Tools Overview</span></span>

<span data-ttu-id="1ad7c-121">下面是 Lync Server 2013 持久聊天资源工具包中提供的工具。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-121">Here are the tools that are provided in the Lync Server 2013 Persistent Chat Resource Kit.</span></span> <span data-ttu-id="1ad7c-122">下节提供了每个工具的说明，包括要求和示例用法。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-122">The following section provides a description of each tool, including requirements and example usage.</span></span>

  - <span data-ttu-id="1ad7c-123">AffCheck</span><span class="sxs-lookup"><span data-stu-id="1ad7c-123">AffCheck</span></span>

  - <span data-ttu-id="1ad7c-124">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="1ad7c-124">ChatMonitoringSummary</span></span>

  - <span data-ttu-id="1ad7c-125">ChatStress 工具</span><span class="sxs-lookup"><span data-stu-id="1ad7c-125">ChatStress Tool</span></span>

  - <span data-ttu-id="1ad7c-126">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="1ad7c-126">ChatUpgradeVerifier</span></span>

  - <span data-ttu-id="1ad7c-127">ChatUsageReport</span><span class="sxs-lookup"><span data-stu-id="1ad7c-127">ChatUsageReport</span></span>

  - <span data-ttu-id="1ad7c-128">ScheduleADSyncforPrincipal</span><span class="sxs-lookup"><span data-stu-id="1ad7c-128">ScheduleADSyncforPrincipal</span></span>

</div>

<div>

## <a name="affcheck"></a><span data-ttu-id="1ad7c-129">AffCheck</span><span class="sxs-lookup"><span data-stu-id="1ad7c-129">AffCheck</span></span>

<div>

## <a name="description"></a><span data-ttu-id="1ad7c-130">说明</span><span class="sxs-lookup"><span data-stu-id="1ad7c-130">Description</span></span>

<span data-ttu-id="1ad7c-131">AffCheck 工具可确认持久的聊天后端数据库用户和组从属记录是否与 Active Directory 域服务的记录相匹配。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-131">The AffCheck tool confirms that the Persistent Chat back-end database user and group affiliation records match that of Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="1ad7c-132">要求</span><span class="sxs-lookup"><span data-stu-id="1ad7c-132">Requirements</span></span>

<span data-ttu-id="1ad7c-133">该工具随加入域的计算机上的 PersistentChatResKit 安装程序一起安装。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-133">The tool is installed with the PersistentChatResKit installer on a domain joined machine.</span></span>

<span data-ttu-id="1ad7c-134">运行该工具的用户帐户必须对持久的聊天后端数据库和 Active Directory 域服务具有读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-134">The user account under which the tool is run must have Read access to the Persistent Chat back-end database and Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="1ad7c-135">用法</span><span class="sxs-lookup"><span data-stu-id="1ad7c-135">Usage</span></span>

<span data-ttu-id="1ad7c-136">根据配置文件中的说明配置 AffCheck.exe.config 文件，并不带命令行参数运行 AffCheck 工具。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-136">Configure the AffCheck.exe.config file according to the instructions in the config file and run the AffCheck tool without command-line parameters.</span></span> <span data-ttu-id="1ad7c-137">下面是默认 AffCheck.exe.config 的内容。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-137">Following are the contents of the default AffCheck.exe.config.</span></span>

<span data-ttu-id="1ad7c-138">**AffCheck.exe.config：**</span><span class="sxs-lookup"><span data-stu-id="1ad7c-138">**AffCheck.exe.config:**</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <appSettings>
        <!--Domain Controller IP Address-->
        <add key="LDAP" value="LDAP://0.0.0.0/"/>
        
        <!-- Domain DN  This is case sensitive, it must match exactly-->
        <add key="DomainComponent" value ="DC=DOMAIN,DC=COM"/>
        
        <!--Domain Administrator Login and Password-->
        <add key="DomainLogin" value="DOMAIN\Administrator"/>
        <add key="DomainPassword" value ="password"/>
        
        <!-- Connection string to Group Chat Database-->
        <add key="ConnectionString" value="data source=SQL_SERVER\INSTANCE;initial catalog=DATABASE_NAME;integrated security=SSPI"/>
        
        <!--Check group affiliations-->
        <add key="CheckGroups" value="true"/>
        
        <!--Check user affilations-->
        <add key="CheckUsers" value="true"/>
        
        <!--List all affiliations if there is a mismatch between database and active directory-->
        <add key="ListAffiliations" value="true"/>
    
        <!--If you need to offset the results of the number of affilations in AD(can be negative to add to AD parent count)-->
        <add key="Offset" value ="0"/>
    
        <!--If you need to ignore certain parents, provide a semi colon delimitted list.-->
        <add key="Ignore" value ="DC=uatest,DC=test,DC=contoso,DC=com;DC=test,DC=contoso,DC=com"/>
      </appSettings>
    </configuration>
  ```
</div>

</div>

<div>

## <a name="chatmonitoringsummary"></a><span data-ttu-id="1ad7c-139">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="1ad7c-139">ChatMonitoringSummary</span></span>

<div>

## <a name="description"></a><span data-ttu-id="1ad7c-140">说明</span><span class="sxs-lookup"><span data-stu-id="1ad7c-140">Description</span></span>

<span data-ttu-id="1ad7c-141">PersistentChatMonitoringSummary 工具将持久聊天监视信息从监视数据库移动到指定的 CSV 日志文件中。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-141">The PersistentChatMonitoringSummary tool moves Persistent Chat monitoring information from the monitoring database into a specified CSV log file.</span></span>

<span data-ttu-id="1ad7c-142">CSV 文件将包含按会话总数、成功会话、意外失败、预期失败和意外故障（如诊断 ID、失败数和失败说明）细分的持久聊天会话的细目。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-142">The CSV file will contain a breakdown of Persistent Chat sessions by number of total sessions, successful sessions, unexpected failures, expected failures, and a breakdown of the unexpected failures by diagnostic ID, number of failures, and failure description.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="1ad7c-143">要求</span><span class="sxs-lookup"><span data-stu-id="1ad7c-143">Requirements</span></span>

<span data-ttu-id="1ad7c-144">在有权访问监视数据库的已加入域的计算机上安装持久聊天资源工具包工具。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-144">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Monitoring database.</span></span>

<span data-ttu-id="1ad7c-145">运行该工具的用户帐户必须具有对监视数据库的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-145">The user account under which the tool runs must have Read access to the Monitoring database.</span></span>

<span data-ttu-id="1ad7c-146">文件 PersistentChatMonitoringSummary.exe.config 中必须包含一个 \<connectionStrings\> 定义监视数据库的连接字符串的节。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-146">The file, PersistentChatMonitoringSummary.exe.config, must contain a \<connectionStrings\> section that defines the connection string to the Monitoring database.</span></span> <span data-ttu-id="1ad7c-147">它还必须包含将为其收集监视数据的 PersistentChatEndpointUri 的键，以及将生成的 CSV 文件的位置的文件路径。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-147">It must also contain a key for the PersistentChatEndpointUri that the monitoring data will be gathered for, and a file path to a location for the CSV file that will be generated.</span></span> <span data-ttu-id="1ad7c-148">有关示例，请参阅已安装的配置文件。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-148">Refer to the installed config file for examples.</span></span> <span data-ttu-id="1ad7c-149">文件必须与工具位于同一目录中。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-149">The file must be located in the same directory as the tool.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="1ad7c-150">用法</span><span class="sxs-lookup"><span data-stu-id="1ad7c-150">Usage</span></span>

```Batch
    PersistentChatMonitoringSummary [-StartDateTime <date>] [-EndDateTime <date>]
```

<span data-ttu-id="1ad7c-151">这些参数定义数据的选择：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-151">These parameters define the selection of data:</span></span>

<span data-ttu-id="1ad7c-152">**StartDateTime：** （可选）指定选择期的开始日期。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-152">**StartDateTime:** Optionally specifies the start date of the selection period.</span></span> <span data-ttu-id="1ad7c-153">默认： 1/1/1753 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="1ad7c-153">Default: 1/1/1753 12:00:00 AM</span></span>

<span data-ttu-id="1ad7c-154">**EndDateTime：** （可选）指定选择期的最后一个日期。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-154">**EndDateTime:** Optionally specifies the last date of the selection period.</span></span> <span data-ttu-id="1ad7c-155">默认：现在</span><span class="sxs-lookup"><span data-stu-id="1ad7c-155">Default: Now</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="1ad7c-156">示例</span><span class="sxs-lookup"><span data-stu-id="1ad7c-156">Example</span></span>

```Batch
    C:\Users\Administrator.VDOMAIN>Desktop\PersistentChatMonitoringSummary.exe
    Reading database connection information, Persistent Chat endpoint uri, and csv output path information from the application config file...
    Connecting to Monitoring database with connection string specified in the application config file...
    Gathering Persistent Chat Session Summary information between "1/1/1753 12:00:00 AM" and "11/19/2012 10:11:25 AM" for Persistent Chat Endpoint Uri "persistentChatEndpointUri@domain.com"...
    Press enter to continue or hit ctr-c if these settings are incorrect...
    
    The summary information about Persistent Chat sessions from the Monitoring database has been output to C:\PersistentChatMonitoring_dd4ace24-4c8a-4a3d-8fd4-591bdfacf47b.csv
    Press enter to exit...
```

</div>

</div>

<div>

## <a name="persistent-chat-stress-tool"></a><span data-ttu-id="1ad7c-157">持久聊天应力工具</span><span class="sxs-lookup"><span data-stu-id="1ad7c-157">Persistent Chat Stress Tool</span></span>

<div>

## <a name="description"></a><span data-ttu-id="1ad7c-158">说明</span><span class="sxs-lookup"><span data-stu-id="1ad7c-158">Description</span></span>

<span data-ttu-id="1ad7c-159">持久聊天功能强大的工具提供了一种简单的方法来模拟持久聊天的使用，以测试实际性能，包括各种用户模型以更好地适应预期的使用方案。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-159">The Persistent Chat Stress tool provides an easy way to simulate usage of Persistent Chat to test real-world performance, including varied user models to better fit your expected usage scenarios.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="1ad7c-160">要求</span><span class="sxs-lookup"><span data-stu-id="1ad7c-160">Requirements</span></span>

<span data-ttu-id="1ad7c-161">在有权访问持久的聊天后端数据库的已加入域的计算机上安装持久聊天资源工具包工具。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-161">Install the Persistent Chat Resource Kit tools onto a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="1ad7c-162">除了此 *控制器* 计算机外，你还需要多个 *加载程序* 计算机。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-162">In addition to this *controller* machine, you will need several *loader* machines.</span></span> <span data-ttu-id="1ad7c-163">对于用户模型中的每个10K 用户，加载程序计算机上至少需要4GB 的可用内存。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-163">For every 10K users in your user model, you will need at least 4GB of free RAM on a loader machine.</span></span> <span data-ttu-id="1ad7c-164">例如，80K 用户的运行将需要跨所有加载程序计算机的 RAM 的32GB。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-164">For example, a run with 80K users will require about 32GB of RAM spread across all loader machines.</span></span> <span data-ttu-id="1ad7c-165">建议您至少拥有三个加载器计算机，而不考虑预期的负载。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-165">We recommend that you have at least three loader machines, regardless of expected load.</span></span>

<span data-ttu-id="1ad7c-166">加载程序计算机必须安装 .NET 4.5 框架以及安装 Visual c + + 2012 可再发行组件。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-166">Loader machines must have the .NET 4.5 Framework as well as the Visual C++ 2012 Redistributable installed.</span></span>

</div>

<div>

## <a name="configuration"></a><span data-ttu-id="1ad7c-167">配置</span><span class="sxs-lookup"><span data-stu-id="1ad7c-167">Configuration</span></span>

<span data-ttu-id="1ad7c-168">将 ChatStressTool 文件复制到可从所有加载程序计算机访问的共享文件夹中。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-168">Copy ChatStressTool files into a shared folder accessible from all loader machines.</span></span>

<span data-ttu-id="1ad7c-169">创建要在压力运行中使用的用户和频道：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-169">Create users and channels for use in the stress run:</span></span>

  - <span data-ttu-id="1ad7c-170">创建任意多个用户作为你的用户模型调用，为 Lync 启用它们，并将其持久聊天策略设置为 "已启用"。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-170">Create as many users as your user model calls for, enable them for Lync, and set their Persistent Chat policy to Enabled.</span></span>

  - <span data-ttu-id="1ad7c-171">为您的压力信道创建一个类别，然后根据该类别的需要创建任意多个房间。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-171">Create a category for your stress channels, and then create as many rooms as are needed under that category.</span></span> <span data-ttu-id="1ad7c-172">类别应在其 **允许** 列表中包含所有压力用户， (通过添加其 OU) 的方式，而压力房间应具有 " **打开**" 隐私设置。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-172">The category should have all stress users in its **Allowed** list (by way of adding their OU), and stress rooms should have a privacy setting of **Open**.</span></span>

  - <span data-ttu-id="1ad7c-173">我们建议您创建额外的压力房间。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-173">We recommend creating extra stress rooms.</span></span> <span data-ttu-id="1ad7c-174">你可以通过以下 Windows PowerShell 命令行界面命令创建50000聊天室：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-174">You can create 50,000 rooms with the following Windows PowerShell command-line interface command:</span></span>
    ```Powershell
        for ($i = 0; $i -le 50000; $i++) { New-CsPersistentChatRoom -Category <parent category> -Name "StressChan_$i" -Privacy Open }
    ```    

<span data-ttu-id="1ad7c-175">编辑配置文件以适合你的拓扑：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-175">Edit the configuration files to fit your topology:</span></span>

<span data-ttu-id="1ad7c-176">在 **LoaderProcess.exe.config** 中，将 "controller.contoso.com" 更改为控制器计算机的完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-176">In **LoaderProcess.exe.config**, change “controller.contoso.com” to the controller machine’s fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="1ad7c-177">在 **StressLauncher.exe.config 中：**</span><span class="sxs-lookup"><span data-stu-id="1ad7c-177">In **StressLauncher.exe.config:**</span></span>

1.  <span data-ttu-id="1ad7c-178">将 "LoaderBinary" 设置值更改为共享文件夹的路径。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-178">Change the “LoaderBinary” setting value to the shared folder’s path.</span></span>

2.  <span data-ttu-id="1ad7c-179">将 "AdminUser"/"AdminPassword" 更改为具有对加载程序计算机的管理员访问权限的凭据。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-179">Change “AdminUser”/”AdminPassword” to credentials that have admin access to loader machines.</span></span>

3.  <span data-ttu-id="1ad7c-180">将 "ChannelCategory" 更改为在其下创建了应力信道的类别的名称。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-180">Change “ChannelCategory” to the name of the category that stress channels have been created under.</span></span>

4.  <span data-ttu-id="1ad7c-181">将 "UserNamePattern" 和 "UserPasswordPattern" 更改为与你的压力用户凭据匹配的模板。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-181">Change “UserNamePattern” and “UserPasswordPattern” to a template that matches your stress user credentials.</span></span> <span data-ttu-id="1ad7c-182">{0} 将替换为用户的索引号。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-182">{0} is replaced with the user’s index number.</span></span>

5.  <span data-ttu-id="1ad7c-183">将 "域" 更改为测试拓扑的 SIP 域。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-183">Change “Domain” to the SIP domain of your test topology.</span></span>

6.  <span data-ttu-id="1ad7c-184">将 "ConnectionString" 更改为持久的聊天后端数据库的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-184">Change “ConnectionString” to a connection string for your Persistent Chat back-end database.</span></span>

7.  <span data-ttu-id="1ad7c-185">将 "UserIndexStart" 更改为第一个压力用户的索引。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-185">Change “UserIndexStart” to the index of the first stress user.</span></span>

8.  <span data-ttu-id="1ad7c-186">将 "LyncFQDN" 更改为你的前端池的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-186">Change “LyncFQDN” to the FQDN of your Front End pool.</span></span>

9.  <span data-ttu-id="1ad7c-187">修改 "计算机" 列表以包括所有加载程序计算机的计算机名称。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-187">Modify the “Machines” list to include machine names for all of your loader machines.</span></span>

10. <span data-ttu-id="1ad7c-188">更改服务终结点的 baseAddress (默认为 "controller.contoso.com" ) 控制器计算机的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-188">Change the baseAddress of the service endpoint (default is “controller.contoso.com”) to the FQDN of your controller machine.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="1ad7c-189">用法</span><span class="sxs-lookup"><span data-stu-id="1ad7c-189">Usage</span></span>

<span data-ttu-id="1ad7c-190">配置完成后，在控制器计算机上打开 StressLauncher.exe。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-190">After configuration is complete, open StressLauncher.exe on the controller machine.</span></span> <span data-ttu-id="1ad7c-191">您可以以任何用户的身份启动 StressLauncher。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-191">You can launch StressLauncher as any user.</span></span> <span data-ttu-id="1ad7c-192">在加载程序计算机上启动的加载程序进程所下的凭据必须在配置文件中指定。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-192">The credentials under which the loader processes start on the loader machines must be specified in the config file.</span></span> <span data-ttu-id="1ad7c-193">你还必须提供对持久的聊天后端数据库具有读取访问权限的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-193">You also must give a connection string that has Read access to the Persistent Chat back-end database.</span></span> <span data-ttu-id="1ad7c-194">如果此连接字符串使用集成的 Windows 身份验证，则必须以具有此访问权限的用户的身份启动 StressLauncher。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-194">If this connection string uses integrated Windows authentication, you must launch StressLauncher as a user that has this access.</span></span>

<span data-ttu-id="1ad7c-195">根据需要更改用户模型设置。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-195">Alter the user model settings as needed.</span></span> <span data-ttu-id="1ad7c-196">单击 " **开始加载** " 以启动 "运行"。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-196">Click **Start Load** to initiate a run.</span></span> <span data-ttu-id="1ad7c-197">一分钟后，用户将开始登录，进度栏将开始填充。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-197">After a minute or so, users will start being signed in, and the progress bar will begin to fill.</span></span> <span data-ttu-id="1ad7c-198">此时，控制器计算机可以正常工作并采取性能测量。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-198">At this point, you may can the controller machine working and take performance measurements.</span></span>

</div>

</div>

<div>

## <a name="chatupgradeverifier"></a><span data-ttu-id="1ad7c-199">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="1ad7c-199">ChatUpgradeVerifier</span></span>

<div>

## <a name="description"></a><span data-ttu-id="1ad7c-200">说明</span><span class="sxs-lookup"><span data-stu-id="1ad7c-200">Description</span></span>

<span data-ttu-id="1ad7c-201">ChatUpgradeVerifier 是一种持久的聊天特定数据库比较工具。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-201">ChatUpgradeVerifier is a Persistent Chat specific database comparison tool.</span></span> <span data-ttu-id="1ad7c-202">该工具比较了群组聊天 2007 R2 或群组聊天2010数据库 (2007/2010Db) ) 的持久聊天2013数据库 (2013Db。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-202">The tool compares either the Group Chat 2007 R2 or Group Chat 2010 Database (2007/2010Db) to the Persistent Chat 2013 Database (2013Db).</span></span>

<span data-ttu-id="1ad7c-203">在 2007/2010Db 中，该工具将逐个检查、每个类别、持久聊天室和外接程序，以查看它是否出现在2013Db 中。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-203">The tool will check, one by one, each category, Persistent Chat room, and add-in in 2007/2010Db to see if it appears in the 2013Db.</span></span> <span data-ttu-id="1ad7c-204">比较包括检查类别、聊天室或外接程序上的所有设置、类别范围内的任何主体，以及类别或聊天室上某个角色中的任何主体。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-204">The comparison includes checking all settings on the category, chat room, or add-in, any principals in scope on the category, and any principal in a role on either the category or the chat room.</span></span> <span data-ttu-id="1ad7c-205">如果2013Db 中未正确显示某个类别或聊天室，则差异将输出到冲突文件。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-205">If a category or a chat room does not appear correctly in the 2013Db, the differences will be output to a conflicts file.</span></span> <span data-ttu-id="1ad7c-206">如果在升级后，将更改 2007/2010Db，然后此工具运行，则会有一个与冲突文件的差异输出。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-206">If, after the upgrade has occurred, the 2007/2010Db is changed and then this tool is run, there will be a differences output to the conflicts file.</span></span> <span data-ttu-id="1ad7c-207">请注意，此应用程序仅是数据库比较工具，不会验证升级过程。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-207">Note that this application is a database comparison tool only and does not validate the upgrade process.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="1ad7c-208">要求</span><span class="sxs-lookup"><span data-stu-id="1ad7c-208">Requirements</span></span>

<span data-ttu-id="1ad7c-209">在有权访问持久聊天后端数据库的已加入域的计算机上安装持久聊天资源工具包工具 (以前版本和当前版本的持久聊天) 。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-209">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end databases (previous and current versions for Persistent Chat).</span></span>

<span data-ttu-id="1ad7c-210">运行该工具的用户帐户必须具有对持久聊天数据库的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-210">The user account under which the tool runs must have Read access to the Persistent Chat databases.</span></span>

<span data-ttu-id="1ad7c-211">ChatUpgradeVerifier.exe.config 文件必须包含 GroupChat2007R2Db 参数或 GroupChat2010Db 参数，并将连接字符串指向相应的群组聊天数据库 (Groupchat 2007R2 或 2010) 。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-211">The ChatUpgradeVerifier.exe.config file must contain either the GroupChat2007R2Db parameter or the GroupChat2010Db parameter, with a connection string to the appropriate Group Chat database (either Groupchat 2007R2 or 2010).</span></span> <span data-ttu-id="1ad7c-212">它还必须包含 PersistentChat2013Db 参数，并将连接字符串连接到持久聊天2013数据库。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-212">It must also contain a PersistentChat2013Db parameter, with a connection string to the Persistent Chat 2013 database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="1ad7c-213">用法</span><span class="sxs-lookup"><span data-stu-id="1ad7c-213">Usage</span></span>

<span data-ttu-id="1ad7c-214">不带任何参数运行 **ChatUpgradeVerifier** 。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-214">Run **ChatUpgradeVerifier** without any parameters.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="1ad7c-215">示例</span><span class="sxs-lookup"><span data-stu-id="1ad7c-215">Example</span></span>

<span data-ttu-id="1ad7c-216">![运行 ChatUpgradeVerifier.exe。](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "运行 ChatUpgradeVerifier.exe。")</span><span class="sxs-lookup"><span data-stu-id="1ad7c-216">![Running ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Running ChatUpgradeVerifier.exe.")</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-usage-report"></a><span data-ttu-id="1ad7c-217">持续聊天使用情况报告</span><span class="sxs-lookup"><span data-stu-id="1ad7c-217">Persistent Chat Usage Report</span></span>

<div>

## <a name="description"></a><span data-ttu-id="1ad7c-218">说明</span><span class="sxs-lookup"><span data-stu-id="1ad7c-218">Description</span></span>

<span data-ttu-id="1ad7c-219">ChatUsageReport 工具生成持久聊天服务使用的 HTML 报告。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-219">The ChatUsageReport tool generates an HTML report of Persistent Chat service usage.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="1ad7c-220">要求</span><span class="sxs-lookup"><span data-stu-id="1ad7c-220">Requirements</span></span>

<span data-ttu-id="1ad7c-221">在有权访问持久聊天后端数据库的已加入域的计算机上安装持久聊天资源工具包工具。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-221">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="1ad7c-222">运行该工具的用户帐户必须具有对持久聊天后端数据库的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-222">The user account under which the tool is run must have Read access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="1ad7c-223">ChatUsageReport.exe.config 中，文件必须包含 \<connectionStrings\> 定义与持久的聊天后端数据库的连接字符串的节。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-223">The file, ChatUsageReport.exe.config, must contain a \<connectionStrings\> section defining the connection string to the Persistent Chat back-end database.</span></span> <span data-ttu-id="1ad7c-224">默认配置文件的内容包含在此处，供你参考。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-224">The contents of the default config file are included here, for your reference.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="1ad7c-225">用法</span><span class="sxs-lookup"><span data-stu-id="1ad7c-225">Usage</span></span>

```Powershell
    ChatUsageReport [-StartDate {date}] [-EndDate {date}] [-TopActiveUsers {n}] [-TopActiveRooms {n}] [-LeastActiveRooms {n}] [-RoomsInactiveSince {Date}] [-OutputFolder {path}]
```
<span data-ttu-id="1ad7c-226">这些参数定义数据的选择：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-226">These parameters define the selection of data:</span></span>

<span data-ttu-id="1ad7c-227">开始 **日期：**（可选）指定选择期的 UTC 开始日期。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-227">**StartDate:** Optionally specifies the UTC start date of the selection period.</span></span> <span data-ttu-id="1ad7c-228">默认：最早日期</span><span class="sxs-lookup"><span data-stu-id="1ad7c-228">Default: Earliest Date</span></span>

<span data-ttu-id="1ad7c-229">**结束日期：** （可选）指定选择期的 UTC 结束日期。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-229">**EndDate:** Optionally specifies the UTC end date of the selection period.</span></span> <span data-ttu-id="1ad7c-230">默认：现在</span><span class="sxs-lookup"><span data-stu-id="1ad7c-230">Default: Now</span></span>

<span data-ttu-id="1ad7c-231">这些参数定义数据的显示方式和显示方式：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-231">These parameters define how and what data is displayed:</span></span>

<span data-ttu-id="1ad7c-232">**TopActiveUsers：** 如果指定此选项，则报表将包括 n 个最活跃的用户，包括用户在所选期间的聊天室中发布的消息数。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-232">**TopActiveUsers:** If this is specified, the report will include the n most active users in terms of the number of messages the user has posted in the chat room for the selected period.</span></span> <span data-ttu-id="1ad7c-233">默认值：10</span><span class="sxs-lookup"><span data-stu-id="1ad7c-233">Default: 10</span></span>

<span data-ttu-id="1ad7c-234">**TopActiveRooms：** 如果指定此选项，则报表将包含 n 个最活跃的聊天室，其中包含在所选期间的会议室中发布的消息数。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-234">**TopActiveRooms:** If this is specified, the report will include the n most active chat rooms in terms of the number of messages posted in the room for the selected period.</span></span> <span data-ttu-id="1ad7c-235">默认值：10</span><span class="sxs-lookup"><span data-stu-id="1ad7c-235">Default: 10</span></span>

<span data-ttu-id="1ad7c-236">**LeastActiveRooms：** 如果指定此选项，则报告将包括 n 个最少活动聊天室，条件是所选期间的聊天室中发布的消息数。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-236">**LeastActiveRooms:** If this is specified, the report will include the n least active chat rooms in terms of the number of messages posted in the chat room for the selected period.</span></span> <span data-ttu-id="1ad7c-237">会议室将至少发布一封邮件。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-237">Rooms will have at least one message posted.</span></span> <span data-ttu-id="1ad7c-238">默认值：10</span><span class="sxs-lookup"><span data-stu-id="1ad7c-238">Default: 10</span></span>

<span data-ttu-id="1ad7c-239">**RoomsInactiveSince：** 如果指定此项，报表将包含自指定日期后处于非活动状态的聊天室的列表。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-239">**RoomsInactiveSince:** If this is specified, the report will include a list of chat rooms that have been inactive since the specified date.</span></span> <span data-ttu-id="1ad7c-240">默认：整个时间</span><span class="sxs-lookup"><span data-stu-id="1ad7c-240">Default: Entire Time</span></span>

<span data-ttu-id="1ad7c-241">**OutputFolder：** 将放置 ChatUsageReport.html 和图形图像的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-241">**OutputFolder:** The folder where the ChatUsageReport.html and the graph images will be placed.</span></span> <span data-ttu-id="1ad7c-242">这必须在配置文件或命令行中定义。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-242">This must be defined in the config file or on the command line.</span></span>

<span data-ttu-id="1ad7c-243">所有命令行参数值也可以在与该工具位于同一目录中的 ChatUsageReport.exe.config 文件中指定。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-243">All of the command line parameter values can also be specified in the ChatUsageReport.exe.config file that is located in the same directory as the tool.</span></span> <span data-ttu-id="1ad7c-244">如果在配置文件和命令行中均指定了任何值，则命令行值将替代配置文件值。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-244">If any value is specified in both the config file and the command line, the command line value will override the config file value.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="1ad7c-245">输出</span><span class="sxs-lookup"><span data-stu-id="1ad7c-245">Output</span></span>

<span data-ttu-id="1ad7c-246">报表将始终包含以下输出：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-246">The report will always include the following output:</span></span>

  - <span data-ttu-id="1ad7c-247">按所选期间的邮件投递次数排名前 n 位的最活跃聊天室。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-247">Top n most active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="1ad7c-248">按所选期间的邮件投递次数排名前 n 位的最活跃的用户。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-248">Top n most active users by number of message posts for selected period.</span></span>

  - <span data-ttu-id="1ad7c-249">按所选期间的邮件投递次数，最少有 n 个活动聊天室。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-249">Top n least active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="1ad7c-250">在数据库的整个生命周期内或自指定日期起不活动的聊天室。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-250">Chat rooms that are inactive for the entire life of the database, or since the specified date.</span></span>

  - <span data-ttu-id="1ad7c-251">所选期间的每日消息发布趋势。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-251">Daily message post trend for selected period.</span></span>

  - <span data-ttu-id="1ad7c-252">所选期间的每周邮件发布趋势。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-252">Weekly message post trend for selected period.</span></span>

  - <span data-ttu-id="1ad7c-253">所选期间的每月消息发布趋势。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-253">Monthly message post trend for selected period.</span></span>

  - <span data-ttu-id="1ad7c-254">所选期间的总邮件帖子。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-254">Total message posts for selected period.</span></span>

  - <span data-ttu-id="1ad7c-255">已启用的会议室的总数。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-255">Total number of enabled rooms.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="1ad7c-256">示例</span><span class="sxs-lookup"><span data-stu-id="1ad7c-256">Example</span></span>

<span data-ttu-id="1ad7c-257">以下示例为2001年生成一个使用报表，并将报表放置在 ChatUsageReport.exe.config 中指定的 OutputFolder 中。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-257">The following example generates a usage report for the entire year 2001 and places the report in the OutputFolder specified in the ChatUsageReport.exe.config.</span></span>

```Powershell
    ChatUsageReport -RoomsInactiveSince 06-20-2010
```
<span data-ttu-id="1ad7c-258">ChatUsageReport.exe.config：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-258">ChatUsageReport.exe.config:</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <connectionStrings>
        <!-- The PersistentChat connection string must be defined in this file. -->
        <add name="PersistentChat" connectionString="Data Source=contoso.com\RTC;Initial Catalog=mgc;Integrated Security=SSPI"/>
      </connectionStrings>
      <appSettings>
        <!-- The OutputFolder must be defined here or on the command line. -->
        <add key="OutputFolder" value="."/>
        <!-- The values below are the same as the application defaults. -->
        <add key="StartDate" value="01/01/0001"/>
        <add key="EndDate" value="12/31/9999"/>
        <add key="TopActiveUsers" value="10"/>
        <add key="TopActiveRooms" value="10"/>
        <add key="LeastActiveRooms" value="10"/>
        <add key="RoomsInactiveSince" value="01/01/0001"/>
      </appSettings>
    </configuration></configuration>
```
</div>

</div>

<div>

## <a name="scheduleadsyncforprincipal"></a><span data-ttu-id="1ad7c-259">ScheduleADSyncForPrincipal</span><span class="sxs-lookup"><span data-stu-id="1ad7c-259">ScheduleADSyncForPrincipal</span></span>

<div>

## <a name="description"></a><span data-ttu-id="1ad7c-260">说明</span><span class="sxs-lookup"><span data-stu-id="1ad7c-260">Description</span></span>

<span data-ttu-id="1ad7c-261">ScheduleADSyncForPrincipal 是 Microsoft SQL Server 2012 脚本，当连接到持久的聊天后端数据库时，必须直接在 SQL Server Management Studio 内运行。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-261">ScheduleADSyncForPrincipal is a Microsoft SQL Server 2012 script that must be run directly from within SQL Server Management Studio when connected to the Persistent Chat back-end database.</span></span> <span data-ttu-id="1ad7c-262">此脚本使你能够强制持久聊天将用户的记录与 Active Directory 域服务的记录同步，而不是等待计划的同步时间。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-262">This script enables you to force Persistent Chat to synchronize its records of a user with those of Active Directory Domain Services, rather than waiting for the scheduled synchronization time.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="1ad7c-263">要求</span><span class="sxs-lookup"><span data-stu-id="1ad7c-263">Requirements</span></span>

<span data-ttu-id="1ad7c-264">运行脚本的用户帐户必须具有对持久的聊天后端数据库的所有者访问权限。</span><span class="sxs-lookup"><span data-stu-id="1ad7c-264">The user account under which the script is run must have owner access to the Persistent Chat back-end database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="1ad7c-265">用法</span><span class="sxs-lookup"><span data-stu-id="1ad7c-265">Usage</span></span>

<span data-ttu-id="1ad7c-266">以下是默认脚本的内容：</span><span class="sxs-lookup"><span data-stu-id="1ad7c-266">Following are the contents of the default script:</span></span>

```Powershell
    /*
    This script will schedule a principal for a forced AD synchronization cycle
    
    If you're using Sql Server Management Studio, pressing Ctrl+Shift+M will 
    allow you to specify values for the template parameter.
    */
    
        insert into
          tblPrincipalMeta
          (
           prinID
          ,prinAffiliationsDirty
          ,prinAttributesDirty
          ,prinDeleted
          )
          select
            prinID
           ,1
           ,1
           ,0
          from
            tblPrincipal
          where
            prinID not in (select prinID from tblPrincipalMeta) and
            prinID = <PrinID,int,0>
     
        update
          tblPrincipalMeta
        set
          prinAffiliationsDirty = 1
         ,prinAttributesDirty = 1
         ,tryCount = 0
         ,nextTry = null
        where
         prinID = <PrinID,int,0>
```

<span data-ttu-id="1ad7c-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1ad7c-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

