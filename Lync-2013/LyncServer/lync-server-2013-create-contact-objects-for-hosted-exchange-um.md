---
title: Lync Server 2013：为托管 Exchange UM 创建联系人对象
description: Lync Server 2013：为托管 Exchange UM 创建联系人对象。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create contact objects for hosted Exchange UM
ms:assetid: a39be52f-488a-4523-ad5f-ce1f0d681959
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412765(v=OCS.15)
ms:contentKeyID: 48185045
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9760e2a39b5182f9b5194e364e059bddc6a63d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431972"
---
# <a name="create-contact-objects-for-hosted-exchange-um-in-lync-server-2013"></a><span data-ttu-id="04b09-103">在 Lync Server 2013 中为托管 Exchange UM 创建联系人对象</span><span class="sxs-lookup"><span data-stu-id="04b09-103">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04b09-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04b09-104">

<span> </span></span></span>

<span data-ttu-id="04b09-105">_**主题上次修改时间：** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="04b09-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="04b09-106">以下过程介绍了如何为托管 Exchange 统一消息 (UM)  (AA) 或订阅者访问 (SA) 联系人对象创建自动助理。</span><span class="sxs-lookup"><span data-stu-id="04b09-106">The following procedure explains how to create Auto Attendant (AA) or Subscriber Access (SA) contact objects for hosted Exchange Unified Messaging (UM).</span></span>

<span data-ttu-id="04b09-107">有关详细信息，请参阅规划文档中 [Lync Server 2013 中的托管 Exchange 联系人对象管理](lync-server-2013-hosted-exchange-contact-object-management.md) 。</span><span class="sxs-lookup"><span data-stu-id="04b09-107">For details, see [Hosted Exchange Contact object management in Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="04b09-108">有关配置联系人对象的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="04b09-108">For details about configuring contact objects, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="04b09-109">New-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="04b09-109">New-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExUmContact)

  - [<span data-ttu-id="04b09-110">Set-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="04b09-110">Set-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExUmContact)

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="04b09-111">在 Lync Server 2013 中可以为托管 Exchange UM 启用联系人对象之前，必须部署适用于它们的托管语音邮件策略。</span><span class="sxs-lookup"><span data-stu-id="04b09-111">Before Lync Server 2013 contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="04b09-112">有关详细信息，请参阅 <A href="lync-server-2013-hosted-voice-mail-policies.md">Lync Server 2013 中的托管语音邮件策略</A>。</span><span class="sxs-lookup"><span data-stu-id="04b09-112">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-aa-or-sa-contact-objects-for-hosted-exchange-um"></a><span data-ttu-id="04b09-113">为托管 Exchange UM 创建 AA 或 SA 联系人对象</span><span class="sxs-lookup"><span data-stu-id="04b09-113">To create AA or SA contact objects for hosted Exchange UM</span></span>

1.  <span data-ttu-id="04b09-114">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="04b09-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="04b09-115">运行 New-CsExUmContact cmdlet 以创建你的部署所需的任何联系人对象。</span><span class="sxs-lookup"><span data-stu-id="04b09-115">Run the New-CsExUmContact cmdlet to create any contact objects required for your deployment.</span></span> <span data-ttu-id="04b09-116">例如，运行以下内容创建 AA 和 SA 联系人对象：</span><span class="sxs-lookup"><span data-stu-id="04b09-116">For example, run the following to create an AA and an SA contact object:</span></span>
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumaa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101" -AutoAttendant $True
       ```
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumsa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101"
       ```
    
    <span data-ttu-id="04b09-117">这些示例设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="04b09-117">These examples set the following parameters:</span></span>
    
      - <span data-ttu-id="04b09-118">**SipAddress** 指定 contact 对象的 SIP 地址。</span><span class="sxs-lookup"><span data-stu-id="04b09-118">**SipAddress** specifies the SIP address of the contact object.</span></span> <span data-ttu-id="04b09-119">这必须是尚未用于配置 Active Directory 域服务中的用户或联系人对象的地址。</span><span class="sxs-lookup"><span data-stu-id="04b09-119">This must be an address that has not already been used to configure a user or contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="04b09-120">此值必须采用 "sip：" 格式， \<*SIP address*\> 如前面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="04b09-120">This value must be in the format “sip:\<*SIP address*\>“ as shown in the previous examples.</span></span>
    
      - <span data-ttu-id="04b09-121">**RegistrarPool** 指定运行注册服务的池 (FQDN) 的完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="04b09-121">**RegistrarPool** specifies the fully qualified domain name (FQDN) of the pool on which the Registrar service is running.</span></span>
        
        <div class=" ">
        

        > [!NOTE]  
        > <span data-ttu-id="04b09-122">在 Lync Server 2013 之前，无法将 Exchange UM 联系人对象移到属于 Lync Server 2013 部署的池。</span><span class="sxs-lookup"><span data-stu-id="04b09-122">Exchange UM contact objects cannot be moved to pools that are part of Lync Server 2013 deployments prior to Lync Server 2013.</span></span>

        
        </div>
    
      - <span data-ttu-id="04b09-123">**OU** 指定此联系人对象将位于的 Active Directory 组织单位。</span><span class="sxs-lookup"><span data-stu-id="04b09-123">**OU** specifies the Active Directory organizational unit where this contact object will be located.</span></span>
    
      - <span data-ttu-id="04b09-124">**DisplayNumber** 指定 contact 对象的电话号码。</span><span class="sxs-lookup"><span data-stu-id="04b09-124">**DisplayNumber** specifies the telephone number of the contact object.</span></span> <span data-ttu-id="04b09-125">每个联系人对象的电话号码必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="04b09-125">The phone number for each contact object must be unique.</span></span>
    
      - <span data-ttu-id="04b09-126">自动 **助理** 指定联系人对象是否为自动助理。</span><span class="sxs-lookup"><span data-stu-id="04b09-126">**AutoAttendant** specifies whether the Contact object is an Auto Attendant.</span></span> <span data-ttu-id="04b09-127">自动助理提供一组语音提示，允许呼叫者在电话系统中导航，并联系他们想要联系的对方。</span><span class="sxs-lookup"><span data-stu-id="04b09-127">Auto Attendant provides a set of voice prompts that allow callers to navigate the phone system and reach the party that they want to contact.</span></span> <span data-ttu-id="04b09-128">值为 **False** (此参数的默认) 表示订阅者访问联系人对象。</span><span class="sxs-lookup"><span data-stu-id="04b09-128">A value of **False** (the default) for this parameter indicates a Subscriber Access contact object.</span></span>

<span data-ttu-id="04b09-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04b09-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

