---
title: 配置用户配置文件
description: 配置用户配置文件。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure User Profile
ms:assetid: 52713245-e502-4539-a238-66ff1aca26b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945594(v=OCS.15)
ms:contentKeyID: 51541419
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 682297da43797dd2d774094e85e8688ef3c64d98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443675"
---
# <a name="configure-user-profile"></a><span data-ttu-id="f7218-103">配置用户配置文件</span><span class="sxs-lookup"><span data-stu-id="f7218-103">Configure User Profile</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7218-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7218-104">

<span> </span></span></span>

<span data-ttu-id="f7218-105">_**主题上次修改时间：** 2018-10-11_</span><span class="sxs-lookup"><span data-stu-id="f7218-105">_**Topic Last Modified:** 2018-10-11_</span></span>

<span data-ttu-id="f7218-106">可使用 Lync Server 2013 应力和性能工具包中包含的工具创建和配置可用于运行负载模拟的测试用户帐户。</span><span class="sxs-lookup"><span data-stu-id="f7218-106">The tools included in the Lync Server 2013 Stress and Performance Tool package enable you to create and configure test user accounts that you can use to run load simulations.</span></span> <span data-ttu-id="f7218-107">使用 Lync Server 2013 用户创建工具创建用户。</span><span class="sxs-lookup"><span data-stu-id="f7218-107">Use the Lync Server 2013 User Creation Tool to create the users.</span></span> <span data-ttu-id="f7218-108"> (有关详细信息，请参阅 [创建用户和联系人](create-users-and-contacts.md)。 ) 创建用户后，请使用 Lync Server 2013 加载配置工具配置用户配置文件。</span><span class="sxs-lookup"><span data-stu-id="f7218-108">(For details, see [Create Users and Contacts](create-users-and-contacts.md).) After users are created, configure the user profiles by using the Lync Server 2013 Load Configuration Tool.</span></span>

<div>

## <a name="running-the-lync-server-2013-load-configuration-tool"></a><span data-ttu-id="f7218-109">运行 Lync Server 2013 加载配置工具</span><span class="sxs-lookup"><span data-stu-id="f7218-109">Running the Lync Server 2013 Load Configuration Tool</span></span>

<span data-ttu-id="f7218-110">要配置用户配置文件，请运行 Lync Server 2013 加载配置工具 ( # A0) 并填写每个选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7218-110">To configure user profiles, run the Lync Server 2013 Load Configuration Tool (UserProfileGenerator.exe) and fill out each of the tabs.</span></span> <span data-ttu-id="f7218-111">对于运行模拟所需的每个客户端计算机，UserProfileGenerator.exe 生成一个目录。</span><span class="sxs-lookup"><span data-stu-id="f7218-111">UserProfileGenerator.exe generates a directory for each of the client computers that you need to run the simulation.</span></span> <span data-ttu-id="f7218-112">每个客户端目录还附带一个脚本来启动 Lync Server 2013 的所有实例（应力和性能工具 ( # A0) ）。</span><span class="sxs-lookup"><span data-stu-id="f7218-112">Each client directory also comes with a script to start all the instances of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f7218-113">在 UserProfileGenerator 中指定的特定于用户的值必须与 Lync Server 2013 用户创建工具中指定的值相匹配， (UserProvisioningTool) 。</span><span class="sxs-lookup"><span data-stu-id="f7218-113">The user-specific values specified in UserProfileGenerator must match the values specified in the Lync Server 2013 User Creation Tool (UserProvisioningTool) for the pool.</span></span>



</div>

<span data-ttu-id="f7218-114">在 Lync Server 2013 加载配置工具的每个选项卡上填写字段，如下部分所述。</span><span class="sxs-lookup"><span data-stu-id="f7218-114">Fill in the fields on each tab of the Lync Server 2013 Load Configuration Tool, as described in the following sections.</span></span>

<div>

## <a name="common-configuration"></a><span data-ttu-id="f7218-115">常见配置</span><span class="sxs-lookup"><span data-stu-id="f7218-115">Common Configuration</span></span>

<span data-ttu-id="f7218-116">下图显示了 Lync Server 2013 加载配置工具的 " **通用配置** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7218-116">The **Common Configuration** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span> <span data-ttu-id="f7218-117">填写 " **通用配置** " 选项卡的字段，如以下步骤中所述。</span><span class="sxs-lookup"><span data-stu-id="f7218-117">Fill in the fields of the **Common Configuration** tab, as described in the following steps.</span></span>

<span data-ttu-id="f7218-118">![“常见配置”选项卡。](images/JJ945594.c68dcc8f-10f2-499e-95a2-fccbcc206c2f(OCS.15).jpg "“常见配置”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="f7218-118">![Common Configuration tab.](images/JJ945594.c68dcc8f-10f2-499e-95a2-fccbcc206c2f(OCS.15).jpg "Common Configuration tab.")</span></span>

1.  <span data-ttu-id="f7218-119">在 " **可用计算机数**" 中，键入或单击要用于运行 LyncPerfTool.exe 的计算机数。</span><span class="sxs-lookup"><span data-stu-id="f7218-119">In **Number of Available Machines**, type or click the number of computers that you want to use to run LyncPerfTool.exe.</span></span> <span data-ttu-id="f7218-120">我们建议你为要模拟的每个4500用户提供一台计算机。</span><span class="sxs-lookup"><span data-stu-id="f7218-120">We recommend that you have one computer for every 4,500 users that you will be simulating.</span></span> <span data-ttu-id="f7218-121">如果你降低负载级别或仅使用可用功能的子集，则该数字可能会有所不同。</span><span class="sxs-lookup"><span data-stu-id="f7218-121">That number may vary if you reduce the load level or if you use only a subset of the available features.</span></span> <span data-ttu-id="f7218-122"> (负载级别在 " **常规方案** " 选项卡上设置。 ) </span><span class="sxs-lookup"><span data-stu-id="f7218-122">(Load levels are set on the **General Scenarios** tab.)</span></span>

2.  <span data-ttu-id="f7218-123">在 " **用户名前缀**" 中，键入用户用户名的前缀。</span><span class="sxs-lookup"><span data-stu-id="f7218-123">In **Prefix for User Names**, type the prefix for the user name of the users.</span></span> <span data-ttu-id="f7218-124">若要登录，统一资源标识符 (URI) 将为： UserPrefix \[ 用户开始索引 ... (用户数-1) \] @User 域。</span><span class="sxs-lookup"><span data-stu-id="f7218-124">To log in, the Uniform Resource Identifier (URI) will be: UserPrefix\[User Start Index…(Number Of Users-1)\]@User Domain.</span></span>

3.  <span data-ttu-id="f7218-125">在 " **为所有用户输入密码**" 中，输入用于创建用户的密码。</span><span class="sxs-lookup"><span data-stu-id="f7218-125">In **Password for All Users**, enter the password that was used for creating the users.</span></span> <span data-ttu-id="f7218-126">如果将此字段保留为空，则用户名将用作密码。</span><span class="sxs-lookup"><span data-stu-id="f7218-126">If you leave this field empty, the username will be used as the password.</span></span>

4.  <span data-ttu-id="f7218-127">在 " **用户开始索引**" 中，单击或键入要配置的第一个用户的索引。</span><span class="sxs-lookup"><span data-stu-id="f7218-127">In **User Start Index**, click or type the index of the first user to be configured.</span></span> <span data-ttu-id="f7218-128">你可以为不同类型或不同级别的负载配置不同的范围，但必须针对要配置的区域运行 UserProfileGenerator.exe 一次。</span><span class="sxs-lookup"><span data-stu-id="f7218-128">You can configure different ranges for different types or levels of load, but you must run UserProfileGenerator.exe once per the range that you want to configure.</span></span>

5.  <span data-ttu-id="f7218-129">在 " **用户数**" 中，单击或键入要配置的用户总数。</span><span class="sxs-lookup"><span data-stu-id="f7218-129">In **Number of Users**, click or type the total number of users you are going to configure.</span></span>

6.  <span data-ttu-id="f7218-130">在 " **用户域**" 中，键入用于 SIP URI 的域。</span><span class="sxs-lookup"><span data-stu-id="f7218-130">In **User Domain**, type the domain used for the SIP URI.</span></span> <span data-ttu-id="f7218-131">这用于构造每个用户的 SIP URI 以登录到 Lync Server 2013 前端服务器或标准版服务器。</span><span class="sxs-lookup"><span data-stu-id="f7218-131">This is used to construct the SIP URI of each user to log on to the Lync Server 2013 Front End Server or Standard Edition server.</span></span> <span data-ttu-id="f7218-132">它可以不同于帐户域。</span><span class="sxs-lookup"><span data-stu-id="f7218-132">It can be different from the account domain.</span></span>

7.  <span data-ttu-id="f7218-133">在 " **帐户域**" 中，键入 Active Directory 域服务域登录。</span><span class="sxs-lookup"><span data-stu-id="f7218-133">In **Account Domain**, type the Active Directory Domain Services domain logon.</span></span>

8.  <span data-ttu-id="f7218-134">输入你希望该工具在所有终结点/用户中记录的每 **秒 (每个实例)** 的最大并发终结点数。</span><span class="sxs-lookup"><span data-stu-id="f7218-134">Enter the maximum number of concurrent endpoints in **Sign In Per Second (per instance)** for which you want the tool to log in all the endpoints/users.</span></span> <span data-ttu-id="f7218-135">建议的费率为 \< = 每秒 2/标准 SKU FE。</span><span class="sxs-lookup"><span data-stu-id="f7218-135">The recommended rate is \<=2 per second/standard SKU FE.</span></span>

9.  <span data-ttu-id="f7218-136">在 " **访问代理服务器" 或 "池 FQDN**" 中，键入希望客户端连接到的服务器 (FQDN) 的完全限定的域名称。</span><span class="sxs-lookup"><span data-stu-id="f7218-136">In **Access Proxy or Pool FQDN**, type the fully qualified domain name (FQDN) of the server that you want the clients to connect to.</span></span> <span data-ttu-id="f7218-137">如果用户在外部登录，请指定访问代理服务器。</span><span class="sxs-lookup"><span data-stu-id="f7218-137">If the users are logging on externally, specify the access proxy.</span></span> <span data-ttu-id="f7218-138">如果用户是内部用户，请指定其池或标准版服务器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f7218-138">If the users are internal, specify the FQDN of their pool or Standard Edition server.</span></span>

10. <span data-ttu-id="f7218-139">在 " **端口**" 中，单击或键入希望用户用于 SIP (的端口（默认值为 5061) ）。</span><span class="sxs-lookup"><span data-stu-id="f7218-139">In **Port**, click or type the port that you want users to use for SIP (the default is 5061).</span></span>

<span data-ttu-id="f7218-140">对于外部网络服务器设置，请指定 " **访问代理服务器" 或 "池 FQDN** " 和 " **端口**"。</span><span class="sxs-lookup"><span data-stu-id="f7218-140">For External Network Server Settings, specify the **Access Proxy or Pool FQDN** and the **Port**.</span></span> <span data-ttu-id="f7218-141">这些设置仅用于外部终结点负载模拟。</span><span class="sxs-lookup"><span data-stu-id="f7218-141">These settings are used only for External endpoints load simulation.</span></span>

</div>

<div>

## <a name="general-scenarios"></a><span data-ttu-id="f7218-142">常规方案</span><span class="sxs-lookup"><span data-stu-id="f7218-142">General Scenarios</span></span>

<span data-ttu-id="f7218-143">下图显示了 Lync Server 2013 加载配置工具的 " **常规方案** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7218-143">The **General Scenarios** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="f7218-144">为要运行的每个常规方案配置负载级别和参数，或保持禁用。</span><span class="sxs-lookup"><span data-stu-id="f7218-144">Configure the load levels and parameters for each of the general scenarios that you want to run, or leave disabled.</span></span>

<span data-ttu-id="f7218-145">![“常规方案”选项卡。](images/JJ945594.4f046d39-b532-4baf-99a6-c89d1d6d1fcc(OCS.15).jpg "“常规方案”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="f7218-145">![General Scenarios tab.](images/JJ945594.4f046d39-b532-4baf-99a6-c89d1d6d1fcc(OCS.15).jpg "General Scenarios tab.")</span></span>

1.  <span data-ttu-id="f7218-146">在包含对等和会议的 **即时消息** 中，为负载级别指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-146">In **Instant Messaging**, which includes peer-to-peer and conferencing, specify the appropriate value for the Load Level.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f7218-147">所有字段的负载级别值 (除位置信息服务) <STRONG>禁用</STRONG>、 <STRONG>低</STRONG>、 <STRONG>中</STRONG>、 <STRONG>高</STRONG>和 <STRONG>自定义</STRONG>之外。</span><span class="sxs-lookup"><span data-stu-id="f7218-147">Load level values for all fields (except Location Information Services) are <STRONG>Disabled</STRONG>, <STRONG>Low</STRONG>, <STRONG>Medium</STRONG>, <STRONG>High</STRONG>, and <STRONG>Custom</STRONG>.</span></span> <span data-ttu-id="f7218-148">选中 "低"、"中"、"高" 或 "自定义" 时，将为每个模态和客户端生成配置。</span><span class="sxs-lookup"><span data-stu-id="f7218-148">When Low, Medium, High, or Custom is selected, configurations will be generated for each modality and client.</span></span> <span data-ttu-id="f7218-149">"高" 将导致为服务器生成的最大支持负载，"中" 对应于60% 的负载，"低" 对应于负载的30%。</span><span class="sxs-lookup"><span data-stu-id="f7218-149">High will result in the maximum supported load to be generated for the server, Medium corresponds to 60 percent of the load, and Low corresponds to 30 percent of the load.</span></span>

    
    </div>

2.  <span data-ttu-id="f7218-150">在仅音频会议的 **音频会议** 中，为负载级别指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-150">In **Audio Conferencing**, which is audio conferencing only, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="f7218-151">对等通话将在本主题后面的 "语音方案" 部分中介绍。</span><span class="sxs-lookup"><span data-stu-id="f7218-151">Peer-to-peer calls are covered in the Voice Scenarios section later in this topic.</span></span> <span data-ttu-id="f7218-152">若要启用 "可查看"，请打开该模态的 " **高级** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7218-152">To enable MultiView, open the **Advanced** tab for that modality.</span></span>

3.  <span data-ttu-id="f7218-153">在 " **应用程序共享**" 中，为负载级别指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-153">In **Application Sharing**, specify the appropriate value for Load Level.</span></span>

4.  <span data-ttu-id="f7218-154">在 **数据协作**（包括数据会议）中，为负载级别指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-154">In **Data Collaboration**, which includes data conferencing, specify the appropriate value for Load Level.</span></span>

5.  <span data-ttu-id="f7218-155">在 **通讯组列表扩展** 中，为加载级别指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-155">In **Distribution List Expansion**, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="f7218-156">还必须单击 " **高级** " 按钮，然后使用在 Lync Server 用户创建工具的 " **通讯组列表** " 选项卡上配置的值相同的字段 ( # A0) 。</span><span class="sxs-lookup"><span data-stu-id="f7218-156">You must also click the **Advanced** button, and then fill in the fields with the same values that you configured on the **Distribution List** tab of the Lync Server User Creation Tool (UserProvisioningTool.exe).</span></span> <span data-ttu-id="f7218-157">有关这些字段的详细信息，请参阅 [创建用户和联系人](create-users-and-contacts.md)</span><span class="sxs-lookup"><span data-stu-id="f7218-157">For details about these fields, see [Create Users and Contacts](create-users-and-contacts.md)</span></span>

6.  <span data-ttu-id="f7218-158">在 " **通讯簿" Web 查询** 中，"通讯簿" 查找服务 (不是通讯簿文件下载) ，请为加载级别指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-158">In **Address Book Web Query**, which is the address book lookup service (not the address book file download), specify the appropriate value for Load Level.</span></span> <span data-ttu-id="f7218-159">若要启用通讯簿下载，请单击相应的 " **高级** " 按钮，然后将 **EnableABSDownload** 设置为 true。</span><span class="sxs-lookup"><span data-stu-id="f7218-159">To enable address book downloads, click the corresponding **Advanced** button, and then set **EnableABSDownload** to true.</span></span>

7.  <span data-ttu-id="f7218-160">在 " **响应组服务**" 中，为负载级别指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-160">In **Response Group Service**, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="f7218-161">您还必须单击相应的 " **高级** " 按钮，然后指定在设置响应组服务代理时已创建的响应组的 uri。</span><span class="sxs-lookup"><span data-stu-id="f7218-161">You must also click the corresponding **Advanced** button, and then specify the URIs of the response groups you have already created when provisioning Response Group Service agents.</span></span> <span data-ttu-id="f7218-162">必须至少指定一个响应组。</span><span class="sxs-lookup"><span data-stu-id="f7218-162">You must specify at least one response group.</span></span> <span data-ttu-id="f7218-163">使用分号分隔多个响应组。</span><span class="sxs-lookup"><span data-stu-id="f7218-163">Use semicolons to separate multiple response groups.</span></span> <span data-ttu-id="f7218-164">将 RGSUriSuffixStartIndex 和 RGSUriSuffixEndIndex 更新为实际值。</span><span class="sxs-lookup"><span data-stu-id="f7218-164">Update RGSUriSuffixStartIndex and RGSUriSuffixEndIndex to the actual values.</span></span>

8.  <span data-ttu-id="f7218-165">在 " **位置信息服务**" 中，为 "负载级别" 选择适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-165">In **Location Information Services**, select the appropriate value for Load Level.</span></span> <span data-ttu-id="f7218-166">必须 **启用** 或 **禁用** 位置信息服务的负载级别。</span><span class="sxs-lookup"><span data-stu-id="f7218-166">The load level for Location Information Services must be **Enabled** or **Disabled**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7218-167">每个方案都有一个位于它旁边的 " <STRONG>高级</STRONG> " 按钮，以及一组支持方案变体的复选框。</span><span class="sxs-lookup"><span data-stu-id="f7218-167">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it, and a set of check boxes that enable variations of the scenarios.</span></span> <span data-ttu-id="f7218-168"><STRONG>临时方式可</STRONG> 生成将在一小时内创建的会议的模拟。</span><span class="sxs-lookup"><span data-stu-id="f7218-168"><STRONG>Ad-hoc</STRONG> means to generate simulation of conferences that will be created throughout the hour.</span></span> <span data-ttu-id="f7218-169"><STRONG>大型</STRONG> 会议意味着将模拟大型会议方案。</span><span class="sxs-lookup"><span data-stu-id="f7218-169"><STRONG>Large Conf</STRONG> means that Large Conference Scenario will be simulated.</span></span> <span data-ttu-id="f7218-170"><STRONG>外部</STRONG> 方式也用于模拟外部用户。</span><span class="sxs-lookup"><span data-stu-id="f7218-170"><STRONG>External</STRONG> means to also simulate external users.</span></span><BR><span data-ttu-id="f7218-171">这些按钮和复选框允许访问特定于每个方案的值，这些值将更改 Lync Server 2013 应力和性能工具 (LyncPerfTool) 的行为，并使自定义设置成为可能。</span><span class="sxs-lookup"><span data-stu-id="f7218-171">These buttons and check boxes allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and make customization possible.</span></span> <span data-ttu-id="f7218-172">对于 " <STRONG>常规方案</STRONG> " 选项卡上的每个方案 (除 "位置信息服务") 的 "加载级别的值" 为 " <STRONG>自定义</STRONG>" 时，将使用 " <STRONG>高级</STRONG> " 对话框中对应的字段计算对话费率。</span><span class="sxs-lookup"><span data-stu-id="f7218-172">For each scenario on the <STRONG>General Scenarios</STRONG> tab (except for Location Information Services), if the value of Load Level is <STRONG>Custom</STRONG>, then the conversation rate will be calculated using the corresponding field in the <STRONG>Advanced</STRONG> dialog box.</span></span> <span data-ttu-id="f7218-173">字段名称不同，具体取决于方案，但字段说明将显示为 "注意：只有从下拉菜单中选择" 自定义 "时，才会使用此号码。</span><span class="sxs-lookup"><span data-stu-id="f7218-173">The field name differs, depending on the scenario, but the field description will state, "NOTE: This number will only be used if Custom is selected from the drop-down menu."</span></span> <span data-ttu-id="f7218-174">通常情况下，" <STRONG>高</STRONG>"、" <STRONG>中</STRONG>" 和 " <STRONG>低</STRONG> " 值将根据每个模式更改每个模式的会话费率以及所有方案的平衡。</span><span class="sxs-lookup"><span data-stu-id="f7218-174">In general, the values <STRONG>High</STRONG>, <STRONG>Medium</STRONG>, and <STRONG>Low</STRONG> will alter the conversation rates per modality in line with the User Model that is a balance of all the scenarios.</span></span> <span data-ttu-id="f7218-175">如果由于预期用法的差异而需要更改每个模态的负载级别，建议使用 <STRONG>自定义</STRONG> 对话费率。</span><span class="sxs-lookup"><span data-stu-id="f7218-175">If there is a need to change the load level per modality due to a difference in expected usage, we recommend using a <STRONG>Custom</STRONG> conversation rate.</span></span><BR>



</div>

</div>

<div>

## <a name="voice-scenarios"></a><span data-ttu-id="f7218-176">语音方案</span><span class="sxs-lookup"><span data-stu-id="f7218-176">Voice Scenarios</span></span>

<span data-ttu-id="f7218-177">下图显示了 Lync Server 2013 加载配置工具的 " **语音方案** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7218-177">The **Voice Scenarios** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="f7218-178">使用 " **语音方案** " 选项卡配置所有语音相关方案。</span><span class="sxs-lookup"><span data-stu-id="f7218-178">Use the **Voice Scenarios** tab to configure all of the voice-related scenarios.</span></span>

<span data-ttu-id="f7218-179">![“语音方案”选项卡。](images/JJ945594.28edf664-da59-40b0-9a0e-196f01e9ca86(OCS.15).jpg "“语音方案”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="f7218-179">![Voice Scenarios tab.](images/JJ945594.28edf664-da59-40b0-9a0e-196f01e9ca86(OCS.15).jpg "Voice Scenarios tab.")</span></span>

1.  <span data-ttu-id="f7218-180">在 **VoIP** 中，单击 " **高级** " 按钮，然后为 " **PhoneAreaCode** " 和 " **LocationProfile** " ("拨号计划) " 字段提供值。</span><span class="sxs-lookup"><span data-stu-id="f7218-180">In **VoIP**, click the **Advanced** button, and then provide values for the **PhoneAreaCode** and **LocationProfile** (dial plan) fields.</span></span> <span data-ttu-id="f7218-181">你还必须为 **负载级别** 指定一个值。</span><span class="sxs-lookup"><span data-stu-id="f7218-181">You must also specify a value for **Load Level**.</span></span> <span data-ttu-id="f7218-182">如果启用了 **VoIP** 和 **UC/PSTN 网关** 的负载级别，则将始终生成一个公共交换电话网络 (PSTN) 到统一通信 (UC) 配置文件，这将模拟外部呼叫。</span><span class="sxs-lookup"><span data-stu-id="f7218-182">If Load Level for **VoIP** and **UC/PSTN Gateway** is Enabled, then a public switched telephone network (PSTN) to unified communications (UC) configuration file will always be generated that will simulate external calls.</span></span>

2.  <span data-ttu-id="f7218-183">在 " **UC/PSTN 网关**" 中，为负载级别指定一个值。</span><span class="sxs-lookup"><span data-stu-id="f7218-183">In **UC/PSTN Gateway**, specify a value for Load Level.</span></span> <span data-ttu-id="f7218-184">如果选择 "**禁用**" 以外的加载级别，则必须通过单击 "中介服务器和 PSTN" 下的 "**添加**" 按钮为 **PSTN 区域代码** 提供值。</span><span class="sxs-lookup"><span data-stu-id="f7218-184">If you select a load level other than **Disabled**, you must supply a value for **PSTN Area Code** by clicking the **Add** button under Mediation Server and PSTN.</span></span> <span data-ttu-id="f7218-185">验证您是否有为该区号配置的路线。</span><span class="sxs-lookup"><span data-stu-id="f7218-185">Verify that you have a route configured for that area code.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f7218-186">你可以使用 Lync Server 控制面板或 Lync Server 命令行管理程序来验证语音路由配置。</span><span class="sxs-lookup"><span data-stu-id="f7218-186">You can use either the Lync Server Control Panel or the Lync Server Management Shell to verify voice route configuration.</span></span>

    
    </div>

3.  <span data-ttu-id="f7218-187">在 **会议助理** 中，为负载级别指定一个值。</span><span class="sxs-lookup"><span data-stu-id="f7218-187">In **Conferencing Attendant**, specify a value for Load Level.</span></span> <span data-ttu-id="f7218-188">选择除 **禁用**) 之外的加载级别 (将启用 " **电话号码** " 字段。</span><span class="sxs-lookup"><span data-stu-id="f7218-188">Selecting a load level (other than **Disabled**) will enable the **Telephone Number** field.</span></span> <span data-ttu-id="f7218-189">输入要使用的自动助理的电话号码。</span><span class="sxs-lookup"><span data-stu-id="f7218-189">Enter the telephone number of the Auto Attendant that you want to use.</span></span> <span data-ttu-id="f7218-190">此外，单击 " **高级** " 按钮，然后为 " **LocationProfile** " 字段指定一个值。</span><span class="sxs-lookup"><span data-stu-id="f7218-190">Also, click the **Advanced** button, and then specify a value for the **LocationProfile** field.</span></span>

4.  <span data-ttu-id="f7218-191">在 " **呼叫寄存服务**" 中，为 **负载级别** 指定适当的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-191">In **Call Park Service**, specify the appropriate value for **Load Level**.</span></span>

5.  <span data-ttu-id="f7218-192">在 **中介服务器和 PSTN** 中，对于要使用的每个中介服务器，您必须拥有单独的 PSTN 模拟器。</span><span class="sxs-lookup"><span data-stu-id="f7218-192">In **Mediation Server and PSTN**, for each Mediation Server that you want to use, you must have a separate PSTN simulator.</span></span> <span data-ttu-id="f7218-193">确定要用作模拟器的客户端后，您需要配置中介服务器以将呼叫路由到您配置的 PSTN 模拟器端口上的该计算机。</span><span class="sxs-lookup"><span data-stu-id="f7218-193">After you have determined which client you are going to use as the simulator, you need to configure your Mediation Server to route calls to that computer on the PSTN Simulator port that you configured.</span></span> <span data-ttu-id="f7218-194">单击 " **添加** " 以配置中介服务器的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-194">Click **Add** to configure the value for the Mediation Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7218-195">每个方案旁边都有一个 " <STRONG>高级</STRONG> " 按钮。</span><span class="sxs-lookup"><span data-stu-id="f7218-195">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="f7218-196">这些按钮允许访问特定于每个方案的值，这些值将更改 Lync Server 2013 应力和性能工具 (LyncPerfTool) 的行为，并启用自定义。</span><span class="sxs-lookup"><span data-stu-id="f7218-196">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="f7218-197">对于 " <STRONG>语音方案</STRONG> " 选项卡上的每个方案，如果 " <STRONG>负载级别</STRONG> " 的值为 " <STRONG>自定义</STRONG>"，则将使用 " <STRONG>高级</STRONG> " 对话框中的相应字段计算对话费率。</span><span class="sxs-lookup"><span data-stu-id="f7218-197">For each scenario on the <STRONG>Voice Scenarios</STRONG> tab, if the value of <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the conversation rate will be calculated by using the corresponding field in the <STRONG>Advanced</STRONG> dialog box.</span></span> <span data-ttu-id="f7218-198">字段名称不同，具体取决于方案，但字段说明将显示为 "注意：只有从下拉菜单中选择" 自定义 "时，才会使用此号码。</span><span class="sxs-lookup"><span data-stu-id="f7218-198">The field name differs, depending on the scenario, but the field description will state, "NOTE: This number will only be used if Custom is selected from the drop-down menu."</span></span>



</div>

</div>

<div>

## <a name="reach"></a><span data-ttu-id="f7218-199">到达</span><span class="sxs-lookup"><span data-stu-id="f7218-199">Reach</span></span>

<span data-ttu-id="f7218-200">在 Lync Server 2013 中，通过 Front-End 服务器上安装的统一通信 Web API (UCWA) 服务器支持会议方案，达到新的体验。</span><span class="sxs-lookup"><span data-stu-id="f7218-200">Reach is a new experience in Lync Server 2013 that supports conferencing scenarios through the Unified Communications Web API (UCWA) server that is installed on the Front-End server.</span></span> <span data-ttu-id="f7218-201">下图显示了 Lync Server 2013 加载配置工具的 " **访问** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7218-201">The **Reach** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="f7218-202">使用 " **转到" 选项卡** 配置所有与访问相关的方案。</span><span class="sxs-lookup"><span data-stu-id="f7218-202">Use the **Reach** tab to configure all the reach-related scenarios.</span></span>

<span data-ttu-id="f7218-203">![“联系”选项卡。](images/JJ945594.65ccf6de-0e8d-47ba-93f3-9dcb39d3fd62(OCS.15).jpg "“联系”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="f7218-203">![Reach tab.](images/JJ945594.65ccf6de-0e8d-47ba-93f3-9dcb39d3fd62(OCS.15).jpg "Reach tab.")</span></span>

1.  <span data-ttu-id="f7218-204">单击 "**常规访问设置**" 旁边的 "**高级**" 按钮。</span><span class="sxs-lookup"><span data-stu-id="f7218-204">Click the **Advanced** button next to **General Reach Settings**.</span></span> <span data-ttu-id="f7218-205">将字段 **UcwaTargetServerUrl** 设置为控制器池虚拟 IP (VIP) 或前端池 VIP。</span><span class="sxs-lookup"><span data-stu-id="f7218-205">Set the field **UcwaTargetServerUrl** to the Director pool virtual IP (VIP) or the Front End pool VIP.</span></span>

2.  <span data-ttu-id="f7218-206">在 " **应用程序共享**"、" **数据协作**" 和 " **IM**" 中，选择适用于 **负载级别** 的值。</span><span class="sxs-lookup"><span data-stu-id="f7218-206">In **Application Sharing**, **Data Collaboration**, and **IM**, select the appropriate value for **Load Level**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7218-207">每个方案旁边都有一个 " <STRONG>高级</STRONG> " 按钮。</span><span class="sxs-lookup"><span data-stu-id="f7218-207">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="f7218-208">这些按钮允许访问特定于每个方案的值，这些值将更改 Lync Server 2013 应力和性能工具 (LyncPerfTool) 的行为，并启用自定义。</span><span class="sxs-lookup"><span data-stu-id="f7218-208">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="f7218-209">对于每个访问情形，如果 <STRONG>负载级别</STRONG> 为 " <STRONG>自定义</STRONG>"，则使用 " <STRONG>ConversationsPerHour</STRONG> " 字段中指定的值，而不是默认值</span><span class="sxs-lookup"><span data-stu-id="f7218-209">For each of the Reach scenarios, if the <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the value specified in the <STRONG>ConversationsPerHour</STRONG> field is used instead of the default</span></span>



</div>

<span data-ttu-id="f7218-210">使用 " **移动** " 选项卡配置所有与移动相关的方案。</span><span class="sxs-lookup"><span data-stu-id="f7218-210">Use the **Mobility** tab to configure all of the mobility-related scenarios.</span></span>

<span data-ttu-id="f7218-211">![“移动性”选项卡。](images/JJ945594.4dd8f3e0-921c-48a5-8b23-2a0330d3c334(OCS.15).jpg "“移动性”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="f7218-211">![Mobility tab.](images/JJ945594.4dd8f3e0-921c-48a5-8b23-2a0330d3c334(OCS.15).jpg "Mobility tab.")</span></span>

1.  <span data-ttu-id="f7218-212">单击 "**移动 (UCWA**" 旁边的 "**高级**" 按钮) 。</span><span class="sxs-lookup"><span data-stu-id="f7218-212">Click the **Advanced** button next to **Mobility (UCWA)**.</span></span> <span data-ttu-id="f7218-213">将字段 **UcwaTargetServerUrl** 设置为控制器池虚拟 IP (VIP) 或前端池 VIP。</span><span class="sxs-lookup"><span data-stu-id="f7218-213">Set the field **UcwaTargetServerUrl** to the Director pool virtual IP (VIP) or the Front End pool VIP.</span></span>

2.  <span data-ttu-id="f7218-214">在 **状态和 P2P 即时消息 \\ 音频** 中，选择适当的 **负载级别** 值以启用移动方案模拟。</span><span class="sxs-lookup"><span data-stu-id="f7218-214">In **Presence and P2P Instant Messaging\\Audio**, select the appropriate value for **Load Level** to enable Mobility Scenario simulation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7218-215">每个方案旁边都有一个 " <STRONG>高级</STRONG> " 按钮。</span><span class="sxs-lookup"><span data-stu-id="f7218-215">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="f7218-216">这些按钮允许访问特定于每个方案的值，这些值将更改 Lync Server 2013 应力和性能工具 (LyncPerfTool) 的行为，并启用自定义。</span><span class="sxs-lookup"><span data-stu-id="f7218-216">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="f7218-217">对于每个访问情形，如果 <STRONG>负载级别</STRONG> 为 " <STRONG>自定义</STRONG>"，则使用 " <STRONG>ConversationsPerHour</STRONG> " 字段中指定的值，而不是默认值。</span><span class="sxs-lookup"><span data-stu-id="f7218-217">For each of the Reach scenarios, if the <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the value specified in the <STRONG>ConversationsPerHour</STRONG> field is used instead of the default.</span></span>



</div>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="f7218-218">摘要</span><span class="sxs-lookup"><span data-stu-id="f7218-218">Summary</span></span>

<span data-ttu-id="f7218-219">下图显示了 Lync Server 2013 加载配置工具的 " **摘要** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f7218-219">The **Summary** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="f7218-220">![“摘要”选项卡。](images/JJ945594.c675e869-8ded-4195-8c2a-68d844fc96ad(OCS.15).jpg "“摘要”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="f7218-220">![Summary tab.](images/JJ945594.c675e869-8ded-4195-8c2a-68d844fc96ad(OCS.15).jpg "Summary tab.")</span></span>

<span data-ttu-id="f7218-221">" **摘要** " 选项卡指示要针对每个方案使用的用户。</span><span class="sxs-lookup"><span data-stu-id="f7218-221">The **Summary** tab indicates which users to use for each of the scenarios.</span></span> <span data-ttu-id="f7218-222">通过选中 " **启用自定义用户范围生成** " 复选框，然后双击包含要自定义的 **用户区域** 的表中的方案，可以手动配置用户编号范围。</span><span class="sxs-lookup"><span data-stu-id="f7218-222">It is possible to manually configure user number ranges by selecting the **Enable Custom User Range Generation** check box, and then double-clicking the scenario in the table that has the **User Range** that you want to customize.</span></span> <span data-ttu-id="f7218-223">检查 ( # A0) 在启动时添加登录延迟，以便包括生成的批处理文件中的延迟以与登录速率对应。</span><span class="sxs-lookup"><span data-stu-id="f7218-223">Check (RunClient.bat) Add sign-in delay when starting, in order to include delays in the generated batch files to correspond with the sign-in rate.</span></span> <span data-ttu-id="f7218-224">这在登录大量用户时避免服务器超载非常有用。</span><span class="sxs-lookup"><span data-stu-id="f7218-224">This is useful to prevent server overload when signing in a large number of users.</span></span> <span data-ttu-id="f7218-225">单击 " **生成文件**"，然后选择要在其中生成配置的文件夹。</span><span class="sxs-lookup"><span data-stu-id="f7218-225">Click **Generate Files**, and select the folder where you want to generate the configuration.</span></span> <span data-ttu-id="f7218-226">当文件创建成功后，将显示与下图类似的对话框。</span><span class="sxs-lookup"><span data-stu-id="f7218-226">A dialog box similar to the following figure will appear when your files have been successfully created.</span></span>

<span data-ttu-id="f7218-227">![确认已创建文件。](images/JJ945594.00dc1e92-bfba-48e7-9568-b97ad864491e(OCS.15).jpg "确认已创建文件。")</span><span class="sxs-lookup"><span data-stu-id="f7218-227">![Acknowledgement that files have been created.](images/JJ945594.00dc1e92-bfba-48e7-9568-b97ad864491e(OCS.15).jpg "Acknowledgement that files have been created.")</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f7218-228">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f7218-228">See Also</span></span>


[<span data-ttu-id="f7218-229">创建用户和联系人</span><span class="sxs-lookup"><span data-stu-id="f7218-229">Create Users and Contacts</span></span>](create-users-and-contacts.md)  
</div>
</div>
<span></span>
</div>
</div>
</div>
