---
title: Lync Server 2013：启用 Lync-Skype 连接
description: Lync Server 2013：启用 Lync-Skype 连接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Lync-Skype connectivity
ms:assetid: 34c4db3e-582f-41fb-85c4-3438ae02f09f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440170(v=OCS.15)
ms:contentKeyID: 57793361
ms.date: 12/16/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f31856299b05af7d6b8e934d6e9784d1571b7e29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428799"
---
# <a name="enabling-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="1f8cd-103">在 Lync Server 2013 中启用 Lync-Skype 连接</span><span class="sxs-lookup"><span data-stu-id="1f8cd-103">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f8cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f8cd-104">

<span> </span></span></span>

<span data-ttu-id="1f8cd-105">_**主题上次修改时间：** 2014-12-16_</span><span class="sxs-lookup"><span data-stu-id="1f8cd-105">_**Topic Last Modified:** 2014-12-16_</span></span>

<span data-ttu-id="1f8cd-106">提交预配请求后，你可以专注于 Lync Server 环境和配置 Lync-Skype 连接所需的管理任务。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-106">After you have submitted the provisioning request, you can focus on the Lync Server environment and administrative tasks required to configure Lync-Skype connectivity.</span></span> <span data-ttu-id="1f8cd-107">在此部分中，我们假设 Lync Server 管理员已部署 Lync Server 和配置的外部访问权限。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-107">In this section, we assume that the Lync Server administrator has deployed Lync Server and configured external access.</span></span> <span data-ttu-id="1f8cd-108">有关配置 Lync Server 的外部访问的其他信息，请参阅在 [lync server 2013 中规划外部用户访问](lync-server-2013-planning-for-external-user-access.md) 和 [在 lync Server 2013 中部署外部用户访问](lync-server-2013-deploying-external-user-access.md)。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-108">For additional information on configuring external access for Lync Server, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md).</span></span>

<span data-ttu-id="1f8cd-109">若要为 Lync-Skype 连接准备 Lync Server 环境，Lync Server 管理员必须完成以下三个任务：</span><span class="sxs-lookup"><span data-stu-id="1f8cd-109">To prepare the Lync Server environment for Lync-Skype connectivity, the Lync Server administrator must complete the following three tasks:</span></span>

<div>

## <a name="1-configure-federation-and-pic"></a><span data-ttu-id="1f8cd-110">1 \。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-110">1\.</span></span> <span data-ttu-id="1f8cd-111">配置联盟和 PIC</span><span class="sxs-lookup"><span data-stu-id="1f8cd-111">Configure Federation and PIC</span></span>

<span data-ttu-id="1f8cd-112">必须使用联盟才能使 Skype 用户能够与组织中的 Lync 用户通信。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-112">Federation is required to enable Skype users to communicate with Lync users in your organization.</span></span> <span data-ttu-id="1f8cd-113">公共即时消息连接 (PIC) 是一种联盟类，必须将其配置为使 Lync 用户能够与 Skype 用户通信。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-113">Public Instant Messaging Connectivity (PIC) is a class of federation, and it must be configured to enable your Lync users to communicate with Skype users.</span></span> <span data-ttu-id="1f8cd-114">联盟和 PIC 是使用 Lync Server 控制面板配置的，如下所示。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-114">Federation and PIC are configured by using the Lync Server Control Panel, shown below.</span></span>

<span data-ttu-id="1f8cd-115">![显示 PIC](images/Dn440170.451b94e3-0b38-488c-835f-1f25690e8074(OCS.15).jpg "显示 PIC")</span><span class="sxs-lookup"><span data-stu-id="1f8cd-115">![Showing PIC](images/Dn440170.451b94e3-0b38-488c-835f-1f25690e8074(OCS.15).jpg "Showing PIC")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1f8cd-116">Live Communication Server 2005 SP1 或 Office Communications Server 2007 不再支持 PIC 联盟。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-116">PIC federation is no longer supported by Live Communication Server 2005 SP1 or by Office Communications Server 2007.</span></span> <span data-ttu-id="1f8cd-117">PIC 联盟支持的平台包括 Lync Server 2013、Lync Server 2010 和 Office 通信服务器 2007 R2。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-117">The supported platforms for PIC federation include Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2.</span></span>



</div>

</div>

<div>

## <a name="2-configure-at-least-one-policy-to-support-federated-user-access"></a><span data-ttu-id="1f8cd-118">2 \。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-118">2\.</span></span> <span data-ttu-id="1f8cd-119">配置至少一个策略以支持联盟的用户访问</span><span class="sxs-lookup"><span data-stu-id="1f8cd-119">Configure at least one policy to support federated user access</span></span>

<span data-ttu-id="1f8cd-120">使用 Lync Server 控制面板，管理员必须配置一个或多个外部用户访问策略，以控制 Skype 用户是否可以与内部 Lync Server 用户进行协作。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-120">Using the Lync Server Control Panel, an administrator must configure one or more external user access policies to control whether Skype users can collaborate with internal Lync Server users.</span></span>

<span data-ttu-id="1f8cd-121">![策略](images/Dn440170.8fd46ad1-9749-422c-8c47-c16ac9032cdb(OCS.15).jpg "策略")</span><span class="sxs-lookup"><span data-stu-id="1f8cd-121">![Policies](images/Dn440170.8fd46ad1-9749-422c-8c47-c16ac9032cdb(OCS.15).jpg "Policies")</span></span>

</div>

<div>

## <a name="3-configure-the-skype-pic-provider-setting-for-lync"></a><span data-ttu-id="1f8cd-122">3。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-122">3\.</span></span> <span data-ttu-id="1f8cd-123">配置 Lync 的 Skype PIC 提供商设置</span><span class="sxs-lookup"><span data-stu-id="1f8cd-123">Configure the Skype PIC provider setting for Lync</span></span>

<span data-ttu-id="1f8cd-124">使用 Lync Server 命令行管理程序，管理员必须将 Lync 客户端策略配置为将 Skype 显示为其他 PIC 提供商。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-124">Using the Lync Server Management Shell, an administrator must configure the Lync client policy to display Skype as an additional PIC provider.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1f8cd-125"> (PIC) 服务提供商的公共即时消息连接的用户在你的组织中无法参与 IM 或音频或视频会议，除非你还在本过程的前面部分中配置了至少一个策略 (步骤 2) 以支持公共 IM 连接。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-125">Users of the Public Instant Messaging Connectivity (PIC) service providers can’t participate in IM or audio or video conferences in your organization until you also configure at least one policy (step 2, earlier in this procedure) to support public IM connectivity.</span></span>



</div>

1.  <span data-ttu-id="1f8cd-126">若要配置联盟和 PIC，请参阅 "启用或禁用联盟和公用 IM 连接" [https://go.microsoft.com/fwlink/p/?LinkId=306063](https://go.microsoft.com/fwlink/p/?linkid=306063) 。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-126">To configure federation and PIC, see "Enable or Disable Federation and Public IM Connectivity" at [https://go.microsoft.com/fwlink/p/?LinkId=306063](https://go.microsoft.com/fwlink/p/?linkid=306063).</span></span>

2.  <span data-ttu-id="1f8cd-127">若要配置至少一个策略以支持联合用户访问，请参阅 "配置用于控制公共用户访问的策略" [https://go.microsoft.com/fwlink/p/?LinkId=306064](https://go.microsoft.com/fwlink/p/?linkid=306064) 。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-127">To configure at least one policy to support federated user access, see "Configure Policies to Control Public User Access" at [https://go.microsoft.com/fwlink/p/?LinkId=306064](https://go.microsoft.com/fwlink/p/?linkid=306064).</span></span>

<span data-ttu-id="1f8cd-128">**编辑现有 Messenger 或 Skype PIC 提供商并为其配置 Skype**</span><span class="sxs-lookup"><span data-stu-id="1f8cd-128">**To edit an existing Messenger or Skype PIC provider and configure it for Skype**</span></span>

1.  <span data-ttu-id="1f8cd-129">从 Lync Server 前端服务器，打开 Lync Server 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-129">From a Lync Server Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="1f8cd-130">运行以下两个命令：</span><span class="sxs-lookup"><span data-stu-id="1f8cd-130">Run the following two commands:</span></span>
    
    `Remove-CsPublicProvider -Identity <identity-name>`
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1f8cd-131">如果你的环境中尚未安装 PIC 提供程序，而是创建新的 PIC 提供商，则无需运行 <STRONG>CsPublicProvider</STRONG> cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-131">If you do not already have a PIC provider in your environment and are creating a new PIC provider then you do not need to run the <STRONG>Remove-CsPublicProvider</STRONG> cmdlet.</span></span>

    
    </div>
    
    `New-CsPublicProvider -ProxyFqdn federation.messenger.msn.com -Enabled 1 -Identity Skype  -VerificationLevel 2 -NameDecorationRoutingDomain msn.com -NameDecorationExcludedDomainList "msn.com,outlook.com,live.com,hotmail.com" -IconUrl "https://images.edge.messenger.live.com/Messenger_16x16.png"`
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1f8cd-132">在 Lync Server 2013 CU5 &amp; 中添加了 Office 2013 SP1 中的 lync 桌面客户端，NameDecorationRoutingDomain 和 NameDecorationExcludedDomainList 改进了 lync 用户添加了 "装饰" 非 Microsoft 域所需的 Skype 联系人以标识和将其路由到 skype (的格式：用户 (contoso.com) @msn .com) 。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-132">Added in Lync Server 2013 CU5 &amp; Lync desktop client in Office 2013 SP1, the NameDecorationRoutingDomain and NameDecorationExcludedDomainList improve the situation where Lync users adding Skype contacts needed to “decorate” non-Microsoft domains to identify and route them to Skype (the format of: user(contoso.com)@msn.com).</span></span> <span data-ttu-id="1f8cd-133">这些新设置可自动格式化用户通过 NameDecorationRoutingDomain（应设为 msn.com）在“添加 Skype 联系人”对话框中输入的地址（如果其不包含 NameDecorationExcludedDomainList 中的域）（我们当前支持 msn.com、live.com、Hotmail.com、outlook.com）。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-133">These new settings will allow automatic formatting of the address user’s enter in the “Add Skype contact” dialog box with the NameDecorationRoutingDomain (which should be set to msn.com) if it does not contain the domains in the NameDecorationExcludedDomainList (we currently can support msn.com, live.com, Hotmail.com, outlook.com).</span></span>

    
    </div>

3.  <span data-ttu-id="1f8cd-134">通过 Lync 客户端，您现在可以选择 Skype 作为 PIC 提供商，并通过指定其 Microsoft 帐户来添加 Skype 客户端。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-134">From a Lync client, you can now select Skype as the PIC provider, and add a Skype client by specifying their Microsoft account.</span></span> <span data-ttu-id="1f8cd-135">此外，已使用其 Microsoft 帐户合并和登录的 Skype 用户可以向 Lync 用户发送联系人请求。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-135">In addition, a Skype user who has merged and logged in with their Microsoft account can send contact request to Lync users.</span></span> <span data-ttu-id="1f8cd-136">有关 Microsoft 帐户的详细信息，请参阅 [什么是 microsoft 帐户？](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account)。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-136">For more information about Microsoft accounts, see [What is a Microsoft account?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span></span> <span data-ttu-id="1f8cd-137">有关将客户端添加到 Lync 的其他信息，请参阅 [在 Lync Server 2013 中使用 Lync-Skype 连接作为最终用户](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-137">For additional information on adding clients to Lync, see [Using Lync-Skype connectivity in Lync Server 2013 as an end user](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span></span>
    
    <span data-ttu-id="1f8cd-138">![添加 Skype 联系人](images/Dn440170.df0e6ed9-2374-4dfa-a815-87281989487c(OCS.15).jpg "添加 Skype 联系人")</span><span class="sxs-lookup"><span data-stu-id="1f8cd-138">![Add Skype Contact](images/Dn440170.df0e6ed9-2374-4dfa-a815-87281989487c(OCS.15).jpg "Add Skype Contact")</span></span>

4.  <span data-ttu-id="1f8cd-139">有关修改托管提供商的详细信息，请参阅 "创建或编辑托管的 SIP 联合提供商" [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065) 。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-139">For detailed information on modifying hosted providers, see "Create or Edit Hosted SIP Federated Providers" at [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065).</span></span>

<span data-ttu-id="1f8cd-140">这将完成必须在服务器上执行的管理任务。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-140">This completes the administrative tasks that must be performed on the server.</span></span> <span data-ttu-id="1f8cd-141">现已为 Lync-Skype 连接设置。</span><span class="sxs-lookup"><span data-stu-id="1f8cd-141">You are now set up for Lync-Skype connectivity.</span></span>

<span data-ttu-id="1f8cd-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f8cd-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

