---
title: 创建用户和联系人
description: 创建用户和联系人。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Create Users and Contacts
ms:assetid: 04b24d07-2864-463d-b508-544c2674c4ab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945587(v=OCS.15)
ms:contentKeyID: 51541412
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e45bb1aa737dd8287be15ae72ece2e35a346af1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446510"
---
# <a name="create-users-and-contacts"></a><span data-ttu-id="ee74d-103">创建用户和联系人</span><span class="sxs-lookup"><span data-stu-id="ee74d-103">Create Users and Contacts</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee74d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee74d-104">

<span> </span></span></span>

<span data-ttu-id="ee74d-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="ee74d-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="ee74d-106">您必须使用 Lync Server 2013 用户预配工具 ( # A0) 来创建用户和联系人，以便为压力和性能负载测试做好准备。</span><span class="sxs-lookup"><span data-stu-id="ee74d-106">You must use the Lync Server 2013 User Provisioning Tool (UserProvisioningTool.exe) to create users and contacts in preparation for stress and performance load testing.</span></span>

<span data-ttu-id="ee74d-107">下面是您在阅读本主题时可能会发现的术语和定义的列表。</span><span class="sxs-lookup"><span data-stu-id="ee74d-107">Here is a list of terms and definitions that you might find useful as you read through this topic.</span></span>

  - <span data-ttu-id="ee74d-108">组织单位-Active Directory 域服务组织单位 (OU) 。</span><span class="sxs-lookup"><span data-stu-id="ee74d-108">Organizational Unit – The Active Directory Domain Services organizational unit (OU).</span></span>

  - <span data-ttu-id="ee74d-109">联合/跨池–将启用用户与其他即时消息 (IM) 服务的用户进行通信的用户，如 Internet 服务的 MSN 网络、AOL®和 Yahoo \! ®。</span><span class="sxs-lookup"><span data-stu-id="ee74d-109">Federated / Cross Pool – Users who will be enabled to communicate with users from other Instant Messaging (IM) services, such as MSN network of Internet services, AOL®, and Yahoo\!®.</span></span>

  - <span data-ttu-id="ee74d-110">通讯组列表-包含 Active Directory 域服务用户列表的 Active Directory 域服务中的对象，用于启动与一组用户的通信。</span><span class="sxs-lookup"><span data-stu-id="ee74d-110">Distribution Lists – The objects in Active Directory Domain Services that contain a list of Active Directory Domain Services users, used for launching communications with groups of people.</span></span>

  - <span data-ttu-id="ee74d-111">位置信息服务-Lync Server 2013 服务（在每个电话上启用和配置时）支持检索增强 9-1-1 (E9) 服务的物理位置。</span><span class="sxs-lookup"><span data-stu-id="ee74d-111">Location Info Service – The Lync Server 2013 service that, when enabled and configured per phone, enables retrieval of physical location for Enhanced 9-1-1 (E9-1-1) services.</span></span>

  - <span data-ttu-id="ee74d-112">美国电话号码–分配给用户的电话号码，以及用于路由入站和出站呼叫和反向号码查找 (RNL) 的 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="ee74d-112">U.S. Phone Numbers – The phone numbers that are assigned to users, in addition to the SIP URI that is used for routing inbound and outbound calls and reverse number lookup (RNL).</span></span>

<div>

## <a name="create-users-and-contacts-by-using-userprovisioningtoolexe"></a><span data-ttu-id="ee74d-113">使用 UserProvisioningTool.exe 创建用户和联系人</span><span class="sxs-lookup"><span data-stu-id="ee74d-113">Create Users and Contacts by Using UserProvisioningTool.exe</span></span>

<span data-ttu-id="ee74d-114">必须使用 Lync Server 用户预配工具为负载模拟创建用户和联系人。</span><span class="sxs-lookup"><span data-stu-id="ee74d-114">You must use the Lync Server User Provisioning Tool to create users and contacts for load simulation.</span></span> <span data-ttu-id="ee74d-115">Lync server 用户预配工具随 Lync Server 压力和性能工具程序包一起安装。</span><span class="sxs-lookup"><span data-stu-id="ee74d-115">The Lync Server User Provisioning Tool is installed with the Lync Server Stress and Performance Tool package.</span></span> <span data-ttu-id="ee74d-116">请确保程序包安装程序 ( # A0) 已在前端服务器或标准版服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="ee74d-116">Be sure that the package installer (CapacityPlanningTool.msi) has been run on the Front End Server or the Standard Edition server.</span></span> <span data-ttu-id="ee74d-117">通过在 \\ 前端服务器或标准版服务器上的% InstalledDirectory% LyncStressAndPerfTool LyncStress) 运行文件 UserProvisioningTool.exe (启动 Lync Server 用户预配工具。</span><span class="sxs-lookup"><span data-stu-id="ee74d-117">Start the Lync Server User Provisioning Tool by running the file UserProvisioningTool.exe (located at %InstalledDirectory%LyncStressAndPerfTool\\LyncStress) on the Front End Server or on the Standard Edition server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ee74d-118">您必须作为域管理员安全组的成员登录才能运行 UserProvisioningTool.exe。</span><span class="sxs-lookup"><span data-stu-id="ee74d-118">You must be logged on as a member of the Domain Admins security group in order to run UserProvisioningTool.exe.</span></span> <span data-ttu-id="ee74d-119">需要从此上下文中运行，因为 UserProvisioningTool.exe 将创建和配置新的 Active Directory 域服务用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-119">It is necessary to run from this context because UserProvisioningTool.exe will be creating and configuring new Active Directory Domain Services users.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="ee74d-120">当您创建 (10000 或更多) 的大量用户时，请从高端计算机运行 UserProvisioningTool.exe。</span><span class="sxs-lookup"><span data-stu-id="ee74d-120">When you create a significant number of users (10,000 or more), run UserProvisioningTool.exe from a high-end computer.</span></span> <span data-ttu-id="ee74d-121">请注意，在创建用户时，域控制器也会遇到高负载。</span><span class="sxs-lookup"><span data-stu-id="ee74d-121">Note that the domain controller will also experience high load while the users are being created.</span></span>



</div>

<span data-ttu-id="ee74d-122">当 Lync Server 用户预配工具打开时，单击 " **配置** "，然后选择 " **加载配置**"。</span><span class="sxs-lookup"><span data-stu-id="ee74d-122">When the Lync Server User Provisioning Tool opens, click **Configuration** and select **Load Configuration**.</span></span> <span data-ttu-id="ee74d-123">若要开始配置用户和联系人，请加载程序包中包含的默认文件 SampleData.xml。</span><span class="sxs-lookup"><span data-stu-id="ee74d-123">To begin configuring users and contacts, load the default file that is included in the package, SampleData.xml.</span></span> <span data-ttu-id="ee74d-124">这将预填充包含你的系统需要修订的示例数据的字段。</span><span class="sxs-lookup"><span data-stu-id="ee74d-124">This will prepopulate the fields with example data that you'll need to revise for your system.</span></span> <span data-ttu-id="ee74d-125">如果你有一个已预配置的 XML 文件，该文件已包含自定义设置，请改为加载该文件。</span><span class="sxs-lookup"><span data-stu-id="ee74d-125">If you have a preconfigured XML file that already contains customized settings, load that file instead.</span></span> <span data-ttu-id="ee74d-126">填写 Lync Server 用户预配工具中的字段，如下部分所述。</span><span class="sxs-lookup"><span data-stu-id="ee74d-126">Fill in the fields in the Lync Server User Provisioning Tool, as described in the following sections.</span></span>

<span data-ttu-id="ee74d-127">![“创建用户”选项卡。](images/JJ945587.80d3c17b-7482-4818-8381-1eff8717d2fe(OCS.15).jpg "“创建用户”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="ee74d-127">![User Creation tab.](images/JJ945587.80d3c17b-7482-4818-8381-1eff8717d2fe(OCS.15).jpg "User Creation tab.")</span></span>

<span data-ttu-id="ee74d-128">若要配置服务器选项，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ee74d-128">To configure server options, follow these steps.</span></span>

1.  <span data-ttu-id="ee74d-129">在 " **前端池 FQDN**" 中，键入要在其中托管用户的标准版服务器或前端池 (FQDN) 的完全限定的域名称。</span><span class="sxs-lookup"><span data-stu-id="ee74d-129">In **Front End Pool FQDN**, type the fully qualified domain name (FQDN) of the Standard Edition server or Front End pool where you want to host the users.</span></span>

2.  <span data-ttu-id="ee74d-130">在 " **用户名前缀**" 中，键入要用于为测试目的生成用户名的前缀。</span><span class="sxs-lookup"><span data-stu-id="ee74d-130">In **User Name Prefix**, type a prefix that you want to use to build user names for testing purposes.</span></span>

3.  <span data-ttu-id="ee74d-131">在 " **密码**" 中，指定将应用于所有测试用户帐户的密码。</span><span class="sxs-lookup"><span data-stu-id="ee74d-131">In **Password**, specify a password that will be applied for all of the test user accounts.</span></span>

4.  <span data-ttu-id="ee74d-132">在 **SIP 域** 中，键入用于测试用户的 SIP Uri (统一资源标识符) 的域名。</span><span class="sxs-lookup"><span data-stu-id="ee74d-132">In **SIP Domain**, type the domain name to be used for test users’ SIP URIs (Uniform Resource Identifiers).</span></span>

5.  <span data-ttu-id="ee74d-133">在 " **帐户域**" 中，键入您的当前 Active Directory 域服务域的域名，您希望在该域中创建测试用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-133">In **Account Domain**, type the domain name of your current Active Directory Domain Services domain, under which you want to create the test users.</span></span>

6.  <span data-ttu-id="ee74d-134">在 " **组织单位**" 中，键入要在其中创建用户对象的 Active Directory 域服务 OU 的名称。</span><span class="sxs-lookup"><span data-stu-id="ee74d-134">In **Organizational Unit**, type the name of the Active Directory Domain Services OU where you want to create the User objects.</span></span> <span data-ttu-id="ee74d-135">如果该 OU 不存在，将创建它。</span><span class="sxs-lookup"><span data-stu-id="ee74d-135">If the OU does not exist, it will be created.</span></span>

7.  <span data-ttu-id="ee74d-136">在 " **电话区号**" 中，键入将用于测试用户帐户的三位数区域代码。</span><span class="sxs-lookup"><span data-stu-id="ee74d-136">In **Phone Area Code**, type the three-digit area code that will be used for test user accounts.</span></span> <span data-ttu-id="ee74d-137">请确保电话区号与 Active Directory 域服务中的任何其他用户区域代码不冲突。</span><span class="sxs-lookup"><span data-stu-id="ee74d-137">Be sure that phone area code does not conflict with any other users’ area codes in Active Directory Domain Services.</span></span>

8.  <span data-ttu-id="ee74d-138">如果要启用企业语音的测试用户，请选中 " **启用语音** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="ee74d-138">Select the **Voice Enabled** check box if you want to enable the test users for Enterprise Voice.</span></span>

9.  <span data-ttu-id="ee74d-139">在 " **用户数**" 中，指定要创建的测试用户总数。</span><span class="sxs-lookup"><span data-stu-id="ee74d-139">In **Number of Users**, specify the total number of test users that you want to create.</span></span>

10. <span data-ttu-id="ee74d-140">在 " **开始索引**" 中，指定将用作用户名前缀的后缀的起始编号。</span><span class="sxs-lookup"><span data-stu-id="ee74d-140">In **Start Index**, specify the starting number that will be used as suffix to the user name prefix.</span></span>

<div>

## <a name="create-users-button"></a><span data-ttu-id="ee74d-141">"创建用户" 按钮</span><span class="sxs-lookup"><span data-stu-id="ee74d-141">Create Users Button</span></span>

<span data-ttu-id="ee74d-142">单击 "创建用户" 按钮时，它将验证所有输入参数。</span><span class="sxs-lookup"><span data-stu-id="ee74d-142">When you click on the Create Users button, it will validate all the input parameters.</span></span>

  - <span data-ttu-id="ee74d-143">如果存在任何验证错误，它将提示你更正这些输入值。</span><span class="sxs-lookup"><span data-stu-id="ee74d-143">If there are any validation errors, it will prompt you to correct those input values.</span></span>

  - <span data-ttu-id="ee74d-144">如果所有输入值都是正确的，它将在 Active Directory 域服务中开始创建用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-144">If all the input values are correct, it will start creating users in Active Directory Domain Services.</span></span> <span data-ttu-id="ee74d-145">将在此窗体底部显示一个进度栏。</span><span class="sxs-lookup"><span data-stu-id="ee74d-145">A progress bar will appear at the bottom of this form.</span></span> <span data-ttu-id="ee74d-146">我们建议您不要在进度栏处于活动状态时关闭应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee74d-146">We recommend that you do not close the application while the progress bar is active.</span></span>

<span data-ttu-id="ee74d-147">用户创建过程速度较慢。</span><span class="sxs-lookup"><span data-stu-id="ee74d-147">User Creation is a slow process.</span></span> <span data-ttu-id="ee74d-148">这可能需要几分钟时间。</span><span class="sxs-lookup"><span data-stu-id="ee74d-148">It can take several minutes.</span></span> <span data-ttu-id="ee74d-149">如果用户数量非常大，流程甚至可能需要几个小时。</span><span class="sxs-lookup"><span data-stu-id="ee74d-149">If the number of users is very large, the process could even take a few hours.</span></span> <span data-ttu-id="ee74d-150">如果用户已存在，则会用任何更改更新这些用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-150">If the users already exist, they are updated with any changes.</span></span> <span data-ttu-id="ee74d-151">你可以通过登录为区域中的一个用户来验证用户是否已创建。</span><span class="sxs-lookup"><span data-stu-id="ee74d-151">You can validate that the users were created by logging on as one of the users in the range.</span></span> <span data-ttu-id="ee74d-152">使用用户前缀、用户编号和 @sipDomain 作为用户名 (例如，LyncUser10@contoso.net) 和指定的密码。</span><span class="sxs-lookup"><span data-stu-id="ee74d-152">Use the user prefix, user number, and @sipDomain as the user name (for example, LyncUser10@contoso.net), along with the specified password.</span></span>

</div>

<div>

## <a name="delete-users-button"></a><span data-ttu-id="ee74d-153">"删除用户" 按钮</span><span class="sxs-lookup"><span data-stu-id="ee74d-153">Delete Users Button</span></span>

<span data-ttu-id="ee74d-154">单击 "删除用户" 按钮时，它将验证所有输入参数。</span><span class="sxs-lookup"><span data-stu-id="ee74d-154">When you click on Delete Users button, it will validate all the input parameters.</span></span>

  - <span data-ttu-id="ee74d-155">如果存在任何验证错误，它将提示你更正这些输入值。</span><span class="sxs-lookup"><span data-stu-id="ee74d-155">If there are any validation errors, it will prompt you to correct those input values.</span></span>

  - <span data-ttu-id="ee74d-156">如果所有输入值都是正确的，它将在 Active Directory 域服务中开始禁用和删除用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-156">If all the input values are correct, it will start disabling and deleting users in Active Directory Domain Services.</span></span> <span data-ttu-id="ee74d-157">将在此窗体底部显示一个进度栏。</span><span class="sxs-lookup"><span data-stu-id="ee74d-157">A progress bar will appear at the bottom of this form.</span></span> <span data-ttu-id="ee74d-158">我们建议您不要在进度栏处于活动状态时关闭应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee74d-158">We recommend that you do not close the application while the progress bar is active.</span></span>

<div>


> [!NOTE]  
> <OL>
> <LI>
> <P><span data-ttu-id="ee74d-159">仅支持美国格式的电话号码。</span><span class="sxs-lookup"><span data-stu-id="ee74d-159">Only U.S.-formatted phone numbers are supported.</span></span> <span data-ttu-id="ee74d-160">电话号码始终分配给用户，由 UserProvisioningTool.exe 创建的所有用户均可用于企业语音。</span><span class="sxs-lookup"><span data-stu-id="ee74d-160">Phone numbers are always assigned to users, and all users created by UserProvisioningTool.exe are enabled for Enterprise Voice.</span></span> <span data-ttu-id="ee74d-161">使用电话号码的任何方案（如会议自动助理或 UC PSTN 呼叫）均可使用此电话号码正确路由呼叫。</span><span class="sxs-lookup"><span data-stu-id="ee74d-161">Any scenarios that use the phone number, such as Conferencing Auto Attendant or UC-PSTN calls, use this phone number to properly route calls.</span></span> <span data-ttu-id="ee74d-162">出于此原因，每个用户都必须有唯一的电话号码。</span><span class="sxs-lookup"><span data-stu-id="ee74d-162">For this reason, every user must have a unique phone number.</span></span> <span data-ttu-id="ee74d-163">如果你必须创建两次用户，该命令将失败，除非你使用不同的区号，或者使用 <STRONG>Disable-move-csuser</STRONG> cmdlet 禁用了以前的用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-163">If you have to create users twice, the command will fail unless you use a different area code, or if the previous users have been disabled by using the <STRONG>Disable-CsUser</STRONG> cmdlet.</span></span></P>
> <LI>
> <P><span data-ttu-id="ee74d-164">在创建联系人之前，必须首先完成从 "用户" 选项卡执行的用户复制。如果你刚刚创建了用户，则必须等到 Lync Server 复制完成，并填充数据库中的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-164">Before you create contacts, you must first complete user replication, performed from the Users tab. If you have just created your users, you must wait until Lync Server replication completes and populates the user accounts in the database.</span></span> <span data-ttu-id="ee74d-165">如果用户尚未完成复制，您将看到一个错误。</span><span class="sxs-lookup"><span data-stu-id="ee74d-165">If the users have not finished replicating, you will see an error.</span></span> <span data-ttu-id="ee74d-166">如果 Lync Server 2013 前端服务已启动，或在最后一位用户上成功运行 <STRONG>move-csuser</STRONG> cmdlet，你将知道用户已完成复制的时间。</span><span class="sxs-lookup"><span data-stu-id="ee74d-166">You will know when users have finished replicating if Lync Server 2013 Front End service has started, or by successfully running the <STRONG>Get-CsUser</STRONG> cmdlet on the last user.</span></span></P></LI></OL>



</div>

</div>

</div>

<div>

## <a name="contacts-creation-tab"></a><span data-ttu-id="ee74d-167">"创建联系人" 选项卡</span><span class="sxs-lookup"><span data-stu-id="ee74d-167">Contacts Creation Tab</span></span>

<span data-ttu-id="ee74d-168">通过 "联系人创建" 选项卡，你可以指定用户联系人的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ee74d-168">The Contacts Creation tab enables you to specify details for users’ contacts.</span></span>

<span data-ttu-id="ee74d-169">![“创建联系人”选项卡。](images/JJ945587.7508726e-83e6-4878-8edd-114543d9af24(OCS.15).jpg "“创建联系人”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="ee74d-169">![Contacts Creation tab.](images/JJ945587.7508726e-83e6-4878-8edd-114543d9af24(OCS.15).jpg "Contacts Creation tab.")</span></span>

<span data-ttu-id="ee74d-170">要配置用户的联系人，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ee74d-170">To configure users’ contacts, follow these steps.</span></span>

1.  <span data-ttu-id="ee74d-171">在 "每个用户的平均联系人" 中，指定为每个用户在联系人列表中填写的联系人的平均数量。</span><span class="sxs-lookup"><span data-stu-id="ee74d-171">In Average Contacts per User, specify the average number of contacts to populate in contact lists for each of the users.</span></span>

2.  <span data-ttu-id="ee74d-172">如果要为每位用户创建同等数量的联系人，请选中 "固定" 复选框。</span><span class="sxs-lookup"><span data-stu-id="ee74d-172">Select the Fixed check box if you want to create an equal number of contacts for every user.</span></span> <span data-ttu-id="ee74d-173">如果想要更改为用户创建的联系人数量，请清除该复选框。</span><span class="sxs-lookup"><span data-stu-id="ee74d-173">If you want to vary the number of contacts created for users, clear the check box.</span></span>

3.  <span data-ttu-id="ee74d-174">在 "每个用户的平均联系人组" 中，指定每个用户的联系人组数。</span><span class="sxs-lookup"><span data-stu-id="ee74d-174">In Average Contact Groups per User, specify the number of contact groups per user.</span></span> <span data-ttu-id="ee74d-175">此号码必须小于每位用户的平均联系人数。</span><span class="sxs-lookup"><span data-stu-id="ee74d-175">This number must be smaller than Average Contacts per User.</span></span>

4.  <span data-ttu-id="ee74d-176">在 "联盟/跨库联系人百分比" 中，指定一个介于0和100之间的数字。</span><span class="sxs-lookup"><span data-stu-id="ee74d-176">In Federated / Cross Pool Contacts Percentage, specify a number between 0 and 100.</span></span> <span data-ttu-id="ee74d-177">此联系人的百分比将与联盟用户一起创建。</span><span class="sxs-lookup"><span data-stu-id="ee74d-177">This percentage of contacts will be created with the federated users.</span></span>

5.  <span data-ttu-id="ee74d-178">在 "联盟/跨池" 用户前缀中，指定将添加到本地用户的联系人列表中的联盟用户的用户名。</span><span class="sxs-lookup"><span data-stu-id="ee74d-178">In Federated / Cross Pool User Prefix, specify the username for federated users that will be added to the contact lists of local users.</span></span>

6.  <span data-ttu-id="ee74d-179">在 "联合/跨池用户 SIP" 域中，指定联盟用户的 SIP 域名称。</span><span class="sxs-lookup"><span data-stu-id="ee74d-179">In Federated / Cross Pool User SIP Domain, specify the SIP Domain Name of the federated users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee74d-180">创建联系人时，不应登录任何用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-180">None of the users should be signed in when creating contacts.</span></span>

    
    </div>

7.  <span data-ttu-id="ee74d-181">在 "用户创建" 选项卡中，验证参数是否正确。</span><span class="sxs-lookup"><span data-stu-id="ee74d-181">In User Creation tab, verify that the parameters are correct.</span></span> <span data-ttu-id="ee74d-182">将在 "用户创建" 选项卡上获取要为其创建联系人的用户的范围。</span><span class="sxs-lookup"><span data-stu-id="ee74d-182">The range of users for which contacts will be created is obtained from the User Creation tab.</span></span>

8.  <span data-ttu-id="ee74d-183">单击 "创建联系人" 以开始创建联系人。</span><span class="sxs-lookup"><span data-stu-id="ee74d-183">Click Create Contacts to begin the contact creation.</span></span> <span data-ttu-id="ee74d-184">此过程可能需要几分钟。</span><span class="sxs-lookup"><span data-stu-id="ee74d-184">This process can take several minutes.</span></span> <span data-ttu-id="ee74d-185">完成后，将出现一个对话框，其中显示 "操作已成功完成" 消息。</span><span class="sxs-lookup"><span data-stu-id="ee74d-185">After it completes, a dialog box will appear with the message, "Operation Completed Successfully."</span></span> <span data-ttu-id="ee74d-186">你可以通过以用户 "创建" 选项卡上创建的用户身份登录来验证已创建的联系人。</span><span class="sxs-lookup"><span data-stu-id="ee74d-186">You can validate the contacts that were created by logging on as a user that was created from the User Creation tab.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee74d-187">创建联系人后，此工具将重新启动目标池中的所有前端服务器。</span><span class="sxs-lookup"><span data-stu-id="ee74d-187">After the contacts are created, this tool will restart all the Front End Servers in the target pool.</span></span> <span data-ttu-id="ee74d-188">根据此操作创建的联系人数量，可能需要更长的时间 (以2小时为单位才能启动前端服务器) 。</span><span class="sxs-lookup"><span data-stu-id="ee74d-188">It may take longer (up to 2 hours) for the Front End Servers to start, depending on how many contacts were created by this operation.</span></span>

    
    </div>

</div>

<div>

## <a name="distribution-list"></a><span data-ttu-id="ee74d-189">通讯组列表</span><span class="sxs-lookup"><span data-stu-id="ee74d-189">Distribution List</span></span>

<span data-ttu-id="ee74d-190">Lync Server 2013 应力和性能工具的其中一个功能是模拟通讯组列表 (Lync 2013 中的 "DL) 扩展" 功能。</span><span class="sxs-lookup"><span data-stu-id="ee74d-190">One of the features of the Lync Server 2013 Stress and Performance Tool is to simulate the distribution list (DL) expansion feature in Lync 2013.</span></span> <span data-ttu-id="ee74d-191">如果您不打算在 UserProvisioningTool 中启用 DL 扩展，则可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="ee74d-191">If you are not going to enable DL expansion in UserProvisioningTool, you can skip this step.</span></span>

<span data-ttu-id="ee74d-192">![“创建通讯组列表”选项卡。](images/JJ945587.0a1d681b-2aea-4724-90d8-efa8a526f600(OCS.15).jpg "“创建通讯组列表”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="ee74d-192">![Distribution List Creation tab.](images/JJ945587.0a1d681b-2aea-4724-90d8-efa8a526f600(OCS.15).jpg "Distribution List Creation tab.")</span></span>

<span data-ttu-id="ee74d-193">通过 "通讯组列表" 选项卡，你可以创建压力和性能工具将用于通讯组列表扩展功能的 DLs。</span><span class="sxs-lookup"><span data-stu-id="ee74d-193">The Distribution List tab enables you to create DLs that the Stress and Performance Tool will use for Distribution List Expansion feature.</span></span> <span data-ttu-id="ee74d-194">在创建 Dl 之前，必须已安装 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="ee74d-194">Prior to creating DLs, Lync Server 2013 must already be installed.</span></span> <span data-ttu-id="ee74d-195">您必须已运行 Lync Server 2013 ForestPrep。</span><span class="sxs-lookup"><span data-stu-id="ee74d-195">You must have run Lync Server 2013 ForestPrep.</span></span> <span data-ttu-id="ee74d-196">否则，在 Active Directory 域服务架构中不存在 DL 属性，并且该工具将无法创建 Dl。</span><span class="sxs-lookup"><span data-stu-id="ee74d-196">Otherwise, the DL attributes do not exist in the Active Directory Domain Services schema and the tool will not be able to create DLs.</span></span>

<span data-ttu-id="ee74d-197">若要配置通讯组列表，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ee74d-197">To configure distribution lists, follow these steps.</span></span>

1.  <span data-ttu-id="ee74d-198">在 "通讯组列表数量" 中，指定要创建的 DLs 的总数。</span><span class="sxs-lookup"><span data-stu-id="ee74d-198">In Number of Distribution Lists, specify the total number of DLs that you want to create.</span></span> <span data-ttu-id="ee74d-199"> (我们建议您从) 的用户数中开始两倍。</span><span class="sxs-lookup"><span data-stu-id="ee74d-199">(We recommend that you start with twice the number of users).</span></span> <span data-ttu-id="ee74d-200">它们的编号从0到 n-1。</span><span class="sxs-lookup"><span data-stu-id="ee74d-200">They are numbered from 0 to n-1.</span></span>

2.  <span data-ttu-id="ee74d-201">在通讯组列表前缀中，指定 DLs 将具有的前缀。</span><span class="sxs-lookup"><span data-stu-id="ee74d-201">In Distribution List Prefix, specify the prefix that the DLs will have.</span></span> <span data-ttu-id="ee74d-202">例如，如果你指定 100 Dl 和 testDL 的前缀，则将通过 testDL99 将 DLs 命名为 testDL0、testDL1 等。</span><span class="sxs-lookup"><span data-stu-id="ee74d-202">For example if you specify 100 DLs and a prefix of testDL, the DLs will be named testDL0, testDL1, and so on, through testDL99.</span></span>

3.  <span data-ttu-id="ee74d-203">在 Dist 的 "最少成员" 列表中，指定要在每个通讯组列表中添加的用户的最少数量。</span><span class="sxs-lookup"><span data-stu-id="ee74d-203">In Minimum Members in a Dist. List, specify the minimum number of users to add in each Distribution List.</span></span>

4.  <span data-ttu-id="ee74d-204">在 Dist 的最大成员中，指定每个通讯组列表中要添加的最大用户数。</span><span class="sxs-lookup"><span data-stu-id="ee74d-204">In Maximum Members in a Dist. List, specify the maximum number of users to add in each Distribution List.</span></span>

<div>

## <a name="create-distribution-lists-button"></a><span data-ttu-id="ee74d-205">创建通讯组列表按钮</span><span class="sxs-lookup"><span data-stu-id="ee74d-205">Create Distribution Lists Button</span></span>

<span data-ttu-id="ee74d-206">单击 "创建通讯组列表" 按钮时，该工具将查询 Active Directory 域服务以查看是否存在与前缀和号码相匹配的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="ee74d-206">When you click the Create Distribution Lists button, the tool queries Active Directory Domain Services to see if distribution lists matching the prefix and numbers already exist.</span></span> <span data-ttu-id="ee74d-207">该工具将仅创建尚不存在的工具。</span><span class="sxs-lookup"><span data-stu-id="ee74d-207">The tool will create only the ones that do not already exist.</span></span> <span data-ttu-id="ee74d-208">将成员添加到这些新创建的通讯组列表时，将从 "用户创建" 选项卡上指定的范围内选择用户。</span><span class="sxs-lookup"><span data-stu-id="ee74d-208">When adding members to these newly created Distribution Lists, it will pick the users from the range specified on the User Creation tab.</span></span>

</div>

</div>

<div>

## <a name="location-info-service-config-tab"></a><span data-ttu-id="ee74d-209">位置信息服务配置选项卡</span><span class="sxs-lookup"><span data-stu-id="ee74d-209">Location Info Service Config Tab</span></span>

<span data-ttu-id="ee74d-210">Lync Server 2013 应力和性能工具的其中一个功能是为位置信息服务生成虚拟配置文件。</span><span class="sxs-lookup"><span data-stu-id="ee74d-210">One of the features of the Lync Server 2013 Stress and Performance Tool is to generate dummy configuration files for the Location Information Service.</span></span> <span data-ttu-id="ee74d-211">位置信息服务通常对服务器性能没有任何重大影响。</span><span class="sxs-lookup"><span data-stu-id="ee74d-211">The Location Information Service typically does not have any significant performance impact on the servers.</span></span>

<span data-ttu-id="ee74d-212">![“位置信息服务配置”选项卡。](images/JJ945587.52ea4e9e-d50a-4dc9-982b-31ee5ace4578(OCS.15).jpg "“位置信息服务配置”选项卡。")</span><span class="sxs-lookup"><span data-stu-id="ee74d-212">![Location Info Service Config tab.](images/JJ945587.52ea4e9e-d50a-4dc9-982b-31ee5ace4578(OCS.15).jpg "Location Info Service Config tab.")</span></span>

<span data-ttu-id="ee74d-213">如果你选择测试此功能，你可以填写表单中提及的值，然后单击 "生成 IIS 配置文件" 按钮。</span><span class="sxs-lookup"><span data-stu-id="ee74d-213">If you choose to test this feature, you can fill in the values mentioned in the form and then click the Generate LIS Config Files button.</span></span> <span data-ttu-id="ee74d-214">它将生成名为 .LIS \_Subnet.csv、.lis \_Switches.csv、.Lis \_Ports.csv 和 .LISWAP.csv \_ 的 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="ee74d-214">It will generate CSV files called LIS\_Subnet.csv, LIS\_Switches.csv, LIS\_Ports.csv, and LIS\_WAP.csv.</span></span> <span data-ttu-id="ee74d-215">然后，你可以分别使用 **CsLisSubnet** Cmdlet、 **CsLisSwitch** cmdlet、 **CsLisPort** CMDLET 和 **CsWirelessAccessPoint** CMDLET 将这些 CSV 文件导入到 .lis 数据库中。</span><span class="sxs-lookup"><span data-stu-id="ee74d-215">You can then import these CSV files into LIS database by using the **Set-CsLisSubnet** cmdlet, the **Set-CsLisSwitch** cmdlet, the **Set-CsLisPort** cmdlet, and the **Set-CsWirelessAccessPoint** cmdlet, respectively.</span></span>

<span data-ttu-id="ee74d-216"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee74d-216"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

