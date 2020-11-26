---
title: Lync Server 2013：使用 Lync-Skype 连接作为最终用户
description: Lync Server 2013：将 Lync-Skype 连接作为最终用户使用。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Lync-Skype connectivity as an end user
ms:assetid: ad22f731-118c-4349-8790-b1a72941cbdd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440175(v=OCS.15)
ms:contentKeyID: 57793365
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd669a5cf0b15f7fb2d411e4456553f5469d9f96
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438916"
---
# <a name="using-lync-skype-connectivity-in-lync-server-2013-as-an-end-user"></a><span data-ttu-id="47020-103">在 Lync Server 2013 中使用 Lync-Skype 连接作为最终用户</span><span class="sxs-lookup"><span data-stu-id="47020-103">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47020-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47020-104">

<span> </span></span></span>

<span data-ttu-id="47020-105">_**主题上次修改时间：** 2016-12-27_</span><span class="sxs-lookup"><span data-stu-id="47020-105">_**Topic Last Modified:** 2016-12-27_</span></span>

<span data-ttu-id="47020-106">Lync-Skype 连接使 Skype 用户和 Lync 用户能够将彼此添加为联系人、交换即时消息和进行音频和视频通话。</span><span class="sxs-lookup"><span data-stu-id="47020-106">Lync-Skype Connectivity enables Skype users and Lync users to add each other as contacts, exchange instant messages and make audio and video calls.</span></span> <span data-ttu-id="47020-107">当 Skype 用户添加 Lync 用户时，Skype 用户将在 Skype 中创建一个联系人，其中包含会话初始协议 (SIP) 统一资源标识符 (与 Lync 用户的 URI) 。</span><span class="sxs-lookup"><span data-stu-id="47020-107">When a Skype user adds a Lync user, a Skype user will create a contact in Skype containing the session initiation protocol (SIP) uniform resource identifier (URI) of the Lync user.</span></span> <span data-ttu-id="47020-108">相反，当 Lync 用户添加 Skype 联系人时，Lync 用户将在 Lync 中创建一个联系人，该联系人将包含 Skype 用户 (MSA) 的 Microsoft 帐户，而不是 Skype 用户名。</span><span class="sxs-lookup"><span data-stu-id="47020-108">Conversely, when a Lync user adds a Skype contact, the Lync user will create a contact in Lync that will contain the Microsoft Account (MSA) of the Skype user, and not the Skype user name.</span></span>

<span data-ttu-id="47020-109">**什么是 MSA？**</span><span class="sxs-lookup"><span data-stu-id="47020-109">**What is an MSA?**</span></span> <span data-ttu-id="47020-110">Skype 用户必须使用 Microsoft 帐户登录 Skype (以前称为 Windows Live ID) 才能与 Lync 联系人通信。</span><span class="sxs-lookup"><span data-stu-id="47020-110">Skype users must sign in to Skype with a Microsoft account (previously called Windows Live ID) in order to communicate with Lync contacts.</span></span> <span data-ttu-id="47020-111">Microsoft 帐户包含电子邮件地址和密码的组合，您也可以使用该电子邮件地址和密码登录到服务，例如 Microsoft OneDrive 存储技术、Windows Phone、Microsoft Xbox LIVE online 游戏服务、Microsoft Outlook 消息传递和协作客户端 (，以及以前的基于 Microsoft Hotmail web 的电子邮件服务或 Windows Live Messenger) 。</span><span class="sxs-lookup"><span data-stu-id="47020-111">A Microsoft account consists of the combination of an email address and a password, which you can also use to sign in to services such as Microsoft OneDrive storage technology, Windows Phone, Microsoft Xbox LIVE online game service, and Microsoft Outlook messaging and collaboration client (and, previously, Microsoft Hotmail web-based e-mail service or Windows Live Messenger).</span></span> <span data-ttu-id="47020-112">如果您使用电子邮件地址和密码登录这些或其他服务，则您已经拥有 Microsoft 帐户。</span><span class="sxs-lookup"><span data-stu-id="47020-112">If you use an email address and a password to sign in to these or other services, you already have a Microsoft account.</span></span> <span data-ttu-id="47020-113">有关创建 Microsoft 帐户的详细信息，请参阅中的 Microsoft 帐户注册页面 [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061) 。</span><span class="sxs-lookup"><span data-stu-id="47020-113">For details about creating a Microsoft Account, see the Microsoft account sign-up page at [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061).</span></span> <span data-ttu-id="47020-114">你可以通过各种应用程序和服务将现有 Skype 帐户与 Microsoft 帐户合并，以便进行单一登录。</span><span class="sxs-lookup"><span data-stu-id="47020-114">You can merge your existing Skype account with your Microsoft account for single sign-on, across a variety of applications and services.</span></span> <span data-ttu-id="47020-115">帐户合并后，Skype 用户可以向 Lync 用户发送联系人请求。</span><span class="sxs-lookup"><span data-stu-id="47020-115">Once the account is merged a Skype user can send a contact request to Lync users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="47020-116">为了让 Lync 和 Skype 用户完全通信，必须满足以下要求：</span><span class="sxs-lookup"><span data-stu-id="47020-116">In order for Lync and Skype users to fully communicate with each other, the following requirements must be met:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="47020-117">Skype 用户必须使用 Microsoft 帐户 (MSA) 登录到其 Skype 客户端。</span><span class="sxs-lookup"><span data-stu-id="47020-117">Skype users must be logged into their Skype client with a Microsoft Account (MSA).</span></span></P>
> <LI>
> <P><span data-ttu-id="47020-118">Lync 用户必须通过其 Lync 管理员启用公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="47020-118">Lync users must be enabled for public IM connectivity by their Lync administrator.</span></span></P>
> <LI>
> <P><span data-ttu-id="47020-119">当 Skype 用户添加 Lync 联系人时，请验证 word Lync 是否显示在联系人姓名下方。</span><span class="sxs-lookup"><span data-stu-id="47020-119">When a Skype user adds a Lync contact, verify that the word Lync appears below the contact’s name.</span></span> <span data-ttu-id="47020-120">这表示已找到 Lync URI。</span><span class="sxs-lookup"><span data-stu-id="47020-120">This indicates that a Lync URI has been found.</span></span></P>
> <LI>
> <P><span data-ttu-id="47020-121">当 Skype 用户添加 Lync 联系人，并且为该 Lync 域返回零个搜索结果时，PIC 设置过程可能尚未完成，或者 Lync 域尚未设置。</span><span class="sxs-lookup"><span data-stu-id="47020-121">When a Skype user adds a Lync contact and zero search results are returned for that Lync domain, the PIC provisioning process may not have completed, or the Lync domain has not yet been set up.</span></span></P>
> <LI>
> <P><span data-ttu-id="47020-122">根据 Lync 和 Skype 用户的隐私设置，IM、视频和联机状态可能不起作用，直到每位用户都接受新联系人。</span><span class="sxs-lookup"><span data-stu-id="47020-122">Depending on the privacy settings of the Lync and Skype users, IM, video, and presence may not work until the new contacts are accepted by each user.</span></span></P></LI></UL>



</div>

<span data-ttu-id="47020-123">**将 Skype 联系人添加到 Lync 2013**</span><span class="sxs-lookup"><span data-stu-id="47020-123">**To add a Skype contact to Lync 2013**</span></span>

1.  <span data-ttu-id="47020-124">从 Lync 中，单击 " **添加联系人"，添加不在我的组织中的联系人**。</span><span class="sxs-lookup"><span data-stu-id="47020-124">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="47020-125">从可用的联系人提供商列表中，选择 " **Skype**"。</span><span class="sxs-lookup"><span data-stu-id="47020-125">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="47020-126">在 " **IM 地址** " 字段中，输入 Microsoft 帐户 (Skype 用户的 MSA) 。</span><span class="sxs-lookup"><span data-stu-id="47020-126">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user.</span></span>

4.  <span data-ttu-id="47020-127">在 " **添加到联系人组** " 下拉框中，选择要将用户添加到的联系人组。</span><span class="sxs-lookup"><span data-stu-id="47020-127">In the **Add to contact group** dropdown box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="47020-128">在 " **设置私人关系** " 下拉框中，选择相应的联系人设置，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="47020-128">In the **Set privacy relationship** dropdown box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="47020-129">用户现在将在 Lync 中显示为联系人。</span><span class="sxs-lookup"><span data-stu-id="47020-129">The user will now appear as a contact in Lync.</span></span> <span data-ttu-id="47020-130">选择用户，右键单击用户名，然后单击 " **查看联系人卡片** " 以查看用户属性。</span><span class="sxs-lookup"><span data-stu-id="47020-130">Select the user, right-click the user name, and click **See Contact Card** to view the user properties.</span></span> <span data-ttu-id="47020-131">您现在可以与新添加的 Skype 用户建立音频或视频通话。</span><span class="sxs-lookup"><span data-stu-id="47020-131">You can now establish an audio or video call with the newly added Skype user.</span></span>

<span data-ttu-id="47020-132">有关对联系人的支持的其他信息，请参阅 [在 Lync 中添加联系人](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a)。</span><span class="sxs-lookup"><span data-stu-id="47020-132">For additional information on support for contacts, see [Add a contact in Lync](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a).</span></span>

<span data-ttu-id="47020-133">当 Skype 用户的 Microsoft 帐户使用自定义域名（如 <strong>bob@contoso.com</strong> ）时，lync 用户可以通过两种方式将该 Microsoft 帐户添加到 Lync：</span><span class="sxs-lookup"><span data-stu-id="47020-133">When a Skype user’s Microsoft account uses a custom domain name, such as <strong>bob@contoso.com</strong> , a Lync user can add that Microsoft account to Lync in two ways:</span></span>

1.  <span data-ttu-id="47020-134">使用 " **添加联系人** " 图标，或</span><span class="sxs-lookup"><span data-stu-id="47020-134">Use the **Add a Contact** icon, or</span></span>

2.  <span data-ttu-id="47020-135">使用 " **查找联系人" 或 "会议室" 或 "拨打号码** " 字段。</span><span class="sxs-lookup"><span data-stu-id="47020-135">Use the **Find someone or a room, or a dial a number** field.</span></span>

<span data-ttu-id="47020-136">在每个实例中，Lync 用户必须按以下格式输入 Skype 用户的电子邮件： <strong>用户 (域名) @msn .com</strong> 。</span><span class="sxs-lookup"><span data-stu-id="47020-136">In each instance, the Lync user must enter the Skype user’s email in the following format: <strong>user(domain name)@msn.com</strong> .</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="47020-137">对于使用以下域名的 Microsoft 帐户，不需要执行此步骤： <STRONG>@live .com、@hotmail .com 或 @outlook .com</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="47020-137">This step is not required for Microsoft accounts that use the following domain names: <STRONG>@live.com, @hotmail.com or @outlook.com</STRONG>.</span></span> <span data-ttu-id="47020-138">有关受支持的自定义域名称的详细信息，请参阅 <A href="https://support.microsoft.com/kb/897567">支持的公共 IM 域</A>。</span><span class="sxs-lookup"><span data-stu-id="47020-138">For more information on supported custom domain names, see <A href="https://support.microsoft.com/kb/897567">Supported public IM domains</A>.</span></span>



</div>

<span data-ttu-id="47020-139">**使用自定义域名时将 Skype 联系人添加到 Lync**</span><span class="sxs-lookup"><span data-stu-id="47020-139">**To add a Skype contact to Lync when using a custom domain name**</span></span>

1.  <span data-ttu-id="47020-140">从 Lync 中，单击 " **添加联系人"，添加不在我的组织中的联系人**。</span><span class="sxs-lookup"><span data-stu-id="47020-140">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="47020-141">从可用的联系人提供商列表中，选择 " **Skype**"。</span><span class="sxs-lookup"><span data-stu-id="47020-141">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="47020-142">在 " **IM 地址** " 字段中，输入 Microsoft 帐户 (的 Skype 用户的 MSA) ，格式为 " <strong>用户 (域名) @msn .com</strong>"。</span><span class="sxs-lookup"><span data-stu-id="47020-142">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user in the format <strong>user(domain name)@msn.com</strong>.</span></span> <span data-ttu-id="47020-143">因此对于用户 bob@contoso.com，该条目将为 <strong> bob (contoso.com) @msn .com <strong> 。</span><span class="sxs-lookup"><span data-stu-id="47020-143">So for user bob@contoso.com, the entry would be <strong>bob(contoso.com)@msn.com<strong> .</span></span>

4.  <span data-ttu-id="47020-144">在 " **添加到联系人组** " 下拉列表框中，选择要将用户添加到的联系人组。</span><span class="sxs-lookup"><span data-stu-id="47020-144">In the **Add to contact group** drop-down list box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="47020-145">在 " **设置私人关系** " 下拉列表框中，选择适当的联系人设置，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="47020-145">In the **Set privacy relationship** drop-down list box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="47020-146">Lync 用户还可以使用 " **查找某人或聊天室"，或者** 在 Lync 中拨打号码域，然后添加类似于以下 <strong>用户 (域名) @msn</strong> 的地址。</span><span class="sxs-lookup"><span data-stu-id="47020-146">A Lync user can also use the **Find someone or a room, or dial a number** field in Lync, and add an address that resembles the following <strong>user(domain name)@msn.com</strong> .</span></span> <span data-ttu-id="47020-147">因此对于 bob@contoso.com Microsoft 帐户，该条目将为 <strong>bob (contoso.com) @msn .com</strong> 。</span><span class="sxs-lookup"><span data-stu-id="47020-147">So for the bob@contoso.com Microsoft account, the entry would be <strong>bob(contoso.com)@msn.com</strong> .</span></span>

7.  <span data-ttu-id="47020-148">按照此过程前面的步骤4和步骤5将联系人添加到联系人组并选择相应的私人关系。</span><span class="sxs-lookup"><span data-stu-id="47020-148">Follow steps 4 and 5 earlier in this procedure to add the contact to a contact group and to select the appropriate privacy relationship.</span></span>

<span data-ttu-id="47020-149">**将 Lync 联系人添加到 Skype**</span><span class="sxs-lookup"><span data-stu-id="47020-149">**To add a Lync contact to Skype**</span></span>

1.  <span data-ttu-id="47020-150">登录 Skype。</span><span class="sxs-lookup"><span data-stu-id="47020-150">Sign in to Skype.</span></span> <span data-ttu-id="47020-151">Skype 用户必须使用 Microsoft 帐户 (MSA) 登录到其 Skype 客户端。</span><span class="sxs-lookup"><span data-stu-id="47020-151">The Skype user must be logged into their Skype client with a Microsoft Account (MSA).</span></span>

2.  <span data-ttu-id="47020-152">选择 "添加联系人" 图标。</span><span class="sxs-lookup"><span data-stu-id="47020-152">Select the Add Contacts icon.</span></span>

3.  <span data-ttu-id="47020-153">输入 Lync 用户的 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="47020-153">Enter the SIP URI of the Lync user.</span></span> <span data-ttu-id="47020-154">例如，bob@contoso.com。</span><span class="sxs-lookup"><span data-stu-id="47020-154">For example, bob@contoso.com.</span></span>

4.  <span data-ttu-id="47020-155">当 Skype 在搜索结果中找到匹配项时，请在 Lync 用户的名称下方查找 word **lync** 。</span><span class="sxs-lookup"><span data-stu-id="47020-155">When Skype finds the match in the search results, look for the word **Lync** below the Lync user’s name.</span></span> <span data-ttu-id="47020-156">这表示 Skype 已成功找到 Lync 客户端的 SIP URI。</span><span class="sxs-lookup"><span data-stu-id="47020-156">This indicates Skype successfully located the Lync client’s SIP URI.</span></span> <span data-ttu-id="47020-157">单击名称。</span><span class="sxs-lookup"><span data-stu-id="47020-157">Click the name.</span></span>

5.  <span data-ttu-id="47020-158">在窗口的右上角，单击 "添加到联系人"。</span><span class="sxs-lookup"><span data-stu-id="47020-158">In the top right corner of the window, click Add to Contacts.</span></span>

6.  <span data-ttu-id="47020-159">新联系人现在已添加到您的联系人列表中，但在接受您的请求之前，您将看到一个问号，而不是状态图标。</span><span class="sxs-lookup"><span data-stu-id="47020-159">The new contact is now added to your contact list, but you’ll see a question mark instead of their status icon until they accept your request.</span></span> <span data-ttu-id="47020-160">当新联系人接受您的请求后，您将能够看到他们处于联机状态、启动 IM 对话以及进行音频和视频通话。</span><span class="sxs-lookup"><span data-stu-id="47020-160">When your new contact accepts your request, you will be able to see when they are online, initiate IM conversations, and make audio and video calls.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="47020-161">Lync Server 管理员必须将 Lync 用户的策略设置配置为允许传入的请求。</span><span class="sxs-lookup"><span data-stu-id="47020-161">The Lync Server administrator must configure the Lync user’s policy settings to allow incoming requests.</span></span> <span data-ttu-id="47020-162">如果不是，Lync 用户将不会收到来自 Skype 用户的联系人请求。</span><span class="sxs-lookup"><span data-stu-id="47020-162">If not, the Lync user will not receive contact requests from the Skype user.</span></span> <span data-ttu-id="47020-163">根据 Lync 用户策略设置的配置，添加 Skype 用户的请求将显示在 Lync 客户端的 " <STRONG>新建</STRONG> " 选项卡上。要开始与 Skype 用户通信，Lync 用户必须将 Skype 用户添加到 "收藏夹" 列表或联系人列表。</span><span class="sxs-lookup"><span data-stu-id="47020-163">Depending on the configuration of the Lync user’s policy settings, the request to add the Skype user will appear on the Lync client’s <STRONG>New</STRONG> tab. To begin communicating with the Skype user, the Lync user must add the Skype user to either the Favorites list or a contact list.</span></span> <span data-ttu-id="47020-164">下图显示了 <STRONG>新</STRONG> 选项卡在 Lync 客户端中的位置。</span><span class="sxs-lookup"><span data-stu-id="47020-164">The image below shows the location of the <STRONG>New</STRONG> tab in the Lync client.</span></span>

    
    </div>

<span data-ttu-id="47020-165">Lync 用户必须配置 Lync 警报，以确保从 Skype 用户发送的请求出现，并由 Lync 用户发现。</span><span class="sxs-lookup"><span data-stu-id="47020-165">A Lync user must configure Lync alerts to ensure that requests sent from a Skype user appear and are discoverable by the Lync user.</span></span> <span data-ttu-id="47020-166">若要配置 Lync 通知，请完成下面的过程。</span><span class="sxs-lookup"><span data-stu-id="47020-166">To configure Lync alerts, complete the procedure that follows.</span></span>

<span data-ttu-id="47020-167">**配置 Lync 通知**</span><span class="sxs-lookup"><span data-stu-id="47020-167">**To configure Lync Alerts**</span></span>

1.  <span data-ttu-id="47020-168">在 Lync 客户端中，单击 " **选项** " 图标。</span><span class="sxs-lookup"><span data-stu-id="47020-168">From the Lync client, click the **Options** icon.</span></span>

2.  <span data-ttu-id="47020-169">选择 " **通知**"。</span><span class="sxs-lookup"><span data-stu-id="47020-169">Select **Alerts**.</span></span>

3.  <span data-ttu-id="47020-170">在 " **常规通知**" 下，选中 " **当某人将我添加到其联系人列表时，请通知我**"。</span><span class="sxs-lookup"><span data-stu-id="47020-170">Under **General alerts**, check **Tell me when someone adds me to his or her contact list**.</span></span>

4.  <span data-ttu-id="47020-171">在 " **未使用 Lync 的联系人**" 下，选择 " **允许邀请"，但阻止所有其他通信**。</span><span class="sxs-lookup"><span data-stu-id="47020-171">Under **Contacts not using Lync**, select **Allow invites but block all other communications**.</span></span>

5.  <span data-ttu-id="47020-172">单击 **"确定"** 关闭 "选项" 窗口。</span><span class="sxs-lookup"><span data-stu-id="47020-172">Click **OK** to close the Options window.</span></span>

<span data-ttu-id="47020-173"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47020-173"></div>

<span> </span>

</div>

</div>

</span></span></div>

