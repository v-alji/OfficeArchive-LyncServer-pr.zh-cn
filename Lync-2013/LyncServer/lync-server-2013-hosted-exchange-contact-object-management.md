---
title: Lync Server 2013：托管 Exchange 联系人对象管理
description: Lync Server 2013：托管 Exchange 联系人对象管理。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Contact object management
ms:assetid: eead9d76-bc4f-4c1c-9779-683cb7a88410
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412978(v=OCS.15)
ms:contentKeyID: 48185748
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 691bcea10d3a4f8b523c6565f384d6c4c9a2a2a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427614"
---
# <a name="hosted-exchange-contact-object-management-in-lync-server-2013"></a><span data-ttu-id="e7612-103">Lync Server 2013 中的托管 Exchange 联系人对象管理</span><span class="sxs-lookup"><span data-stu-id="e7612-103">Hosted Exchange Contact object management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7612-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7612-104">

<span> </span></span></span>

<span data-ttu-id="e7612-105">_**主题上次修改时间：** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="e7612-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="e7612-106">您需要为您的跨平台部署中的每个自动助理号码和订户访问号码配置联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e7612-106">You need to configure a Contact object for each auto-attendant number and subscriber access number in your cross-premises deployment.</span></span>

<span data-ttu-id="e7612-107">为了与托管 Exchange UM 集成，ocsumutil.exe 无法用于管理联系人对象，因为它依赖于 Active Directory Exchange UM 设置。</span><span class="sxs-lookup"><span data-stu-id="e7612-107">For integration with hosted Exchange UM, ocsumutil.exe cannot be used to manage Contact objects, because it depends on Active Directory Exchange UM settings.</span></span> <span data-ttu-id="e7612-108">在跨平台部署中，Lync Server 2013 和托管 Exchange UM 安装在单独的林中，它们之间不受信任。</span><span class="sxs-lookup"><span data-stu-id="e7612-108">In a cross-premises deployment, Lync Server 2013 and hosted Exchange UM are installed in separate forests with no trust between them.</span></span> <span data-ttu-id="e7612-109">出于安全原因，Lync Server 2013 管理员无法直接访问 Exchange UM Active Directory 设置。</span><span class="sxs-lookup"><span data-stu-id="e7612-109">For security reasons, Lync Server 2013 administrators have no direct access to Exchange UM Active Directory settings.</span></span> <span data-ttu-id="e7612-110">因此，Lync Server 2013 提供了一种不同的模型来管理共享 SIP 地址空间中的联系人对象，该 *共享 SIP 地址空间* 可同时用于 Lync Server 2013 和托管 Exchange UM 服务。</span><span class="sxs-lookup"><span data-stu-id="e7612-110">As a result, Lync Server 2013 provides a different model for managing Contact objects in a *shared SIP address space* that is accessible to both Lync Server 2013 and the hosted Exchange UM service.</span></span>

<div>

## <a name="hosted-contact-object-workflow"></a><span data-ttu-id="e7612-111">托管联系人对象工作流</span><span class="sxs-lookup"><span data-stu-id="e7612-111">Hosted Contact Object Workflow</span></span>

<span data-ttu-id="e7612-112">以下是使用托管的 Exchange 租户管理员管理联系人对象的常规步骤：</span><span class="sxs-lookup"><span data-stu-id="e7612-112">The following are the general steps for working with your hosted Exchange tenant administrator to manage contact objects:</span></span>

1.  <span data-ttu-id="e7612-113">Exchange 管理员请求 Exchange UM 订阅者访问和自动助理联系人对象的电话号码。</span><span class="sxs-lookup"><span data-stu-id="e7612-113">The Exchange administrator requests phone numbers for the Exchange UM subscriber access and auto-attendant Contact objects.</span></span>

2.  <span data-ttu-id="e7612-114">Lync Server 2013 管理员为每个电话号码创建一个 Contact 对象，并为每个 Contact 对象分配一个托管语音邮件策略。</span><span class="sxs-lookup"><span data-stu-id="e7612-114">The Lync Server 2013 administrator creates a Contact object for each phone number and assigns a hosted voice mail policy to each Contact object.</span></span>

3.  <span data-ttu-id="e7612-115">Lync Server 2013 管理员向 Exchange 管理员提供电话号码。</span><span class="sxs-lookup"><span data-stu-id="e7612-115">The Lync Server 2013 administrator provides the phone numbers to the Exchange administrator.</span></span>

4.  <span data-ttu-id="e7612-116">Exchange 管理员将电话号码分配给合适的 Exchange UM 拨号计划，以便自动助理和订阅者访问。</span><span class="sxs-lookup"><span data-stu-id="e7612-116">The Exchange administrator assigns the phone numbers to appropriate Exchange UM dial plans for auto attendants and subscriber access.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e7612-117">无需在联系人对象上配置任何 Lync Server 2013 拨号计划设置，就像本地部署一样。</span><span class="sxs-lookup"><span data-stu-id="e7612-117">There is no need to configure any Lync Server 2013 dial plan settings on the Contact objects as there is with on-premises deployments.</span></span>



</div>

</div>

<div>

## <a name="configuring-hosted-contact-objects"></a><span data-ttu-id="e7612-118">配置托管联系人对象</span><span class="sxs-lookup"><span data-stu-id="e7612-118">Configuring Hosted Contact Objects</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e7612-119">在 Lync Server 2013 中可以为托管 Exchange UM 启用联系人对象之前，必须部署适用于它们的托管语音邮件策略。</span><span class="sxs-lookup"><span data-stu-id="e7612-119">Before Lync Server 2013 Contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="e7612-120">策略可以是全局、网站级或每用户范围，只要它适用于要启用的联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e7612-120">The policy can be of global, site-level, or per-user scope, as long as it applies to the contact object you want to enable.</span></span> <span data-ttu-id="e7612-121">有关详细信息，请参阅 <A href="lync-server-2013-hosted-voice-mail-policies.md">Lync Server 2013 中的托管语音邮件策略</A>。</span><span class="sxs-lookup"><span data-stu-id="e7612-121">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="e7612-122">若要在跨平台部署中配置托管的自动助理和订阅者访问联系人对象，必须使用以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e7612-122">To configure hosted auto-attendant and subscriber access Contact objects in a cross-premises deployment, you must use the following cmdlets:</span></span>

  - <span data-ttu-id="e7612-123">**New-CsExUmContact** 为托管 UM 创建新的联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e7612-123">**New-CsExUmContact** creates a new Contact object for hosted UM.</span></span>

  - <span data-ttu-id="e7612-124">**Set-CsExUmContact** 修改托管 Exchange UM 的现有联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e7612-124">**Set-CsExUmContact** modifies an existing Contact object for hosted Exchange UM.</span></span>

<span data-ttu-id="e7612-125">以下示例创建自动助理联系人对象：</span><span class="sxs-lookup"><span data-stu-id="e7612-125">The following example creates an auto-attendant Contact object:</span></span>

    New-CsExUmContact -SipAddress sip:exumaa1@fabrikam.com -RegistrarPool RedmondPool.litwareinc.com -OU "OU=ExUmContacts,DC=litwareinc,DC=com" -DisplayNumber 2065559876 -AutoAttendant $True

<span data-ttu-id="e7612-126">此示例使用 SIP 地址 sip:exumaa1@fabrikam.com 创建新的 Exchange UM 联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e7612-126">This example creates a new Exchange UM Contact object with the SIP address sip:exumaa1@fabrikam.com.</span></span> <span data-ttu-id="e7612-127">Lync Server 2013 注册机构服务正在运行的池的名称为 RedmondPool.litwareinc.com。</span><span class="sxs-lookup"><span data-stu-id="e7612-127">The name of the pool where the Lync Server 2013 Registrar service is running is RedmondPool.litwareinc.com.</span></span> <span data-ttu-id="e7612-128">将存储此信息的 Active Directory 组织单位为 OU = ExUmContacts、DC = litwareinc、DC = com。</span><span class="sxs-lookup"><span data-stu-id="e7612-128">The Active Directory organizational unit where this information will be stored is OU=ExUmContacts,DC=litwareinc,DC=com.</span></span> <span data-ttu-id="e7612-129">联系人对象的电话号码是2065554567。</span><span class="sxs-lookup"><span data-stu-id="e7612-129">The phone number of the Contact object is 2065554567.</span></span> <span data-ttu-id="e7612-130">"可选-自动助理 $True" 参数指定此对象是自动助理联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e7612-130">The optional -AutoAttendant $True parameter specifies that this object is an auto-attendant Contact object.</span></span> <span data-ttu-id="e7612-131">将-自动助理参数设置为 False (默认) 指定订阅者 access 联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e7612-131">Setting the -AutoAttendant parameter to False (the default) specifies a subscriber access Contact object.</span></span>

<span data-ttu-id="e7612-132">有关 New-CsExUmContact 和 Set-CsExUmContact cmdlet 的详细信息，请参阅 Lync Server Management Shell 文档。</span><span class="sxs-lookup"><span data-stu-id="e7612-132">For details about the New-CsExUmContact and Set-CsExUmContact cmdlets, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="e7612-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7612-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

