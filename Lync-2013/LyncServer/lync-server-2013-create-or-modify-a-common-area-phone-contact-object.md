---
title: Lync Server 2013：创建或修改公共的区域电话联系人对象
description: Lync Server 2013：创建或修改公共的区域电话联系人对象。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a common area phone Contact object
ms:assetid: eec33ad1-e4f2-49b2-91d6-d5a9d2e1714b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994083(v=OCS.15)
ms:contentKeyID: 51803995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5ede23f495a63b2d556b556817d4171a08723
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431839"
---
# <a name="create-or-modify-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="ebcce-103">在 Lync Server 2013 中创建或修改公用的 "区域电话联系人" 对象</span><span class="sxs-lookup"><span data-stu-id="ebcce-103">Create or modify a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ebcce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ebcce-104">

<span> </span></span></span>

<span data-ttu-id="ebcce-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="ebcce-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="ebcce-106">若要为所有公共区域电话创建 Active Directory 域服务联系人对象，请使用 **CsCommonAreaPhone** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebcce-106">To create Active Directory Domain Services contact objects for all your common area phones, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="ebcce-107">此 cmdlet 可以创建新的联系人对象以与普通的区域电话配合使用，也可以将现有联系人对象与新的通用区域电话相关联。</span><span class="sxs-lookup"><span data-stu-id="ebcce-107">This cmdlet can either create new contact objects for use with common area phones, or it can associate existing contact objects with a new common area phone.</span></span> <span data-ttu-id="ebcce-108">若要修改与常见的区域电话相关联的联系人对象的属性，请使用 **CsCommonAreaPhone** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebcce-108">To modify the properties of the contact objects associated with common area phones, use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="ebcce-109">" **设置-CsCommonAreaPhone** " 的可选参数使你能够更改项目，例如联系人的 Active Directory 显示名称或行统一资源标识符 (URI) 与该电话相关联，并启用和禁用与 Lync Server 一起使用的帐户。</span><span class="sxs-lookup"><span data-stu-id="ebcce-109">Optional parameters for **Set-CsCommonAreaPhone** enable you to change items, such as the contact’s Active Directory display name or the line Uniform Resource Identifier (URI) associated with the phone, and enable and disable the account for use with Lync Server.</span></span> <span data-ttu-id="ebcce-110">有关所有可用修改的详细信息，请参阅 [CsCommonAreaPhone 设置](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone)的参数部分。</span><span class="sxs-lookup"><span data-stu-id="ebcce-110">For details about all the available modifications, see the Parameters section at [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone).</span></span> <span data-ttu-id="ebcce-111">有关 **新的 CsCommonAreaPhone** 参数的详细信息，请参阅 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone)。</span><span class="sxs-lookup"><span data-stu-id="ebcce-111">For details about **New-CsCommonAreaPhone** parameters, see [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone).</span></span>

<span data-ttu-id="ebcce-112">你可以从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行这两个 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebcce-112">You can run these two cmdlets from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ebcce-113">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="ebcce-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="creating-a-common-area-phone-contact-object"></a><span data-ttu-id="ebcce-114">创建通用的 "区域电话联系人" 对象</span><span class="sxs-lookup"><span data-stu-id="ebcce-114">Creating a common area phone contact object</span></span>

  - <span data-ttu-id="ebcce-115">若要创建新的通用区域电话联系人对象，请使用 **CsCommonAreaPhone** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebcce-115">To create a new common area phone contact object, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="ebcce-116">创建联系人对象时，至少必须提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="ebcce-116">At a minimum, you must supply the following information when creating a contact object:</span></span>
    
      - <span data-ttu-id="ebcce-117">**LineUri**：分配给公共区域电话的电话号码。</span><span class="sxs-lookup"><span data-stu-id="ebcce-117">**LineUri**: The telephone number assigned to the common area phone.</span></span> <span data-ttu-id="ebcce-118">请注意，在指定电话号码时，必须使用 E：164格式。</span><span class="sxs-lookup"><span data-stu-id="ebcce-118">Note that you must use the E.164 format when specifying the phone number.</span></span>
    
      - <span data-ttu-id="ebcce-119">**RegistrarPool**：将托管联系人对象的注册机构池的完全限定的域名 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="ebcce-119">**RegistrarPool**: The fully qualified domain name (FQDN) of the Registrar pool that will host the contact object.</span></span>
    
      - <span data-ttu-id="ebcce-120">**OU**：将在其中创建联系人对象的 Active Directory 容器的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="ebcce-120">**OU**: Distinguished name of the Active Directory container where the contact object will be created.</span></span>
    
    <span data-ttu-id="ebcce-121">我们还建议你提供 Active Directory 域服务的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ebcce-121">We also recommend that you provide an Active Directory Domain Services display name.</span></span> <span data-ttu-id="ebcce-122">否则，你将需要使用 GUID 来指定电话标识。</span><span class="sxs-lookup"><span data-stu-id="ebcce-122">Otherwise, you will need to use a GUID to specify the phone Identity.</span></span> <span data-ttu-id="ebcce-123">例如：</span><span class="sxs-lookup"><span data-stu-id="ebcce-123">For example:</span></span>
    
        New-CsCommonAreaPhone -LineUri "tel:+12065551219" -RegistrarPool "atl-cs-001.litwareinc.com" -OU "OU=Phones,dc=litwareinc,dc=com" -DisplayName "Lobby"

</div>

<div>

## <a name="modifying-a-common-area-phone-contact-object"></a><span data-ttu-id="ebcce-124">修改公共的 "区域电话联系人" 对象</span><span class="sxs-lookup"><span data-stu-id="ebcce-124">Modifying a common area phone contact object</span></span>

  - <span data-ttu-id="ebcce-125">若要修改现有的公共区域电话的属性，请使用 **CsCommonAreaPhone** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebcce-125">To modify the properties of an existing common area phone, contact object use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="ebcce-126">例如，此命令通过 DisplayName 大厅配置公共区域手机的 SIP 地址：</span><span class="sxs-lookup"><span data-stu-id="ebcce-126">For example, this command configures the SIP address for the common area phone with the DisplayName Lobby:</span></span>
    
        Set-CsCommonAreaPhone -Identity "Lobby" -SipAddress "sip:lobby@litwareinc.com"

</div>

<span data-ttu-id="ebcce-127">有关详细信息，请参阅 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) Cmdlet 和 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="ebcce-127">For details, see the Help topics for the [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) cmdlet and the [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) cmdlet.</span></span>

<span data-ttu-id="ebcce-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ebcce-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

