---
title: Lync Server 2013：启用或禁用热 desking
description: Lync Server 2013：启用或禁用热 desking。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable hot desking
ms:assetid: 93a7fed6-f61a-4b41-9336-a8320afa87cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994057(v=OCS.15)
ms:contentKeyID: 51803968
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3fd22c9bf51078324cfe5e215bd154503c2d9b57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391829"
---
# <a name="enable-or-disable-hot-desking-in-lync-server-2013"></a><span data-ttu-id="b1a79-103">在 Lync Server 2013 中启用或禁用热 desking</span><span class="sxs-lookup"><span data-stu-id="b1a79-103">Enable or disable hot desking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1a79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1a79-104">

<span> </span></span></span>

<span data-ttu-id="b1a79-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="b1a79-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="b1a79-106">您可以将公用区域电话设置为 " *热桌面电话*"。</span><span class="sxs-lookup"><span data-stu-id="b1a79-106">You can set up common area phones as *hot-desk phones*.</span></span> <span data-ttu-id="b1a79-107">使用桌面电话，用户可以登录到自己的用户帐户，登录后，使用 Lync Server 功能及其自己的用户配置文件设置。</span><span class="sxs-lookup"><span data-stu-id="b1a79-107">With hot-desk phones, users can log on to their own user account, and, after they are logged on, use Lync Server features and their own user profile settings.</span></span> <span data-ttu-id="b1a79-108">热 desking 通过使用客户端策略进行管理：若要启用或禁用热 desking，您需要修改由您的公共区域电话使用的客户端策略。</span><span class="sxs-lookup"><span data-stu-id="b1a79-108">Hot desking is managed by using client policies: to enable or disable hot desking, you need to modify the client policies that are used by your common area phones.</span></span> <span data-ttu-id="b1a79-109">有关如何确定已分配给您的公共区域电话的会议策略的详细信息，请参阅 [在 Lync Server 2013 中查看常见的区域电话信息](lync-server-2013-view-common-area-phone-information.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a79-109">For details about how to determine the conferencing policies that have been assigned to your common area phones, see [View common area phone information in Lync Server 2013](lync-server-2013-view-common-area-phone-information.md).</span></span>

<span data-ttu-id="b1a79-110">你可以使用 **set-csclientpolicy** Cmdlet 或 **Set-csclientpolicy** cmdlet 的 EnableHotdesking 参数在手机上启用或禁用热 desking，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b1a79-110">You use the EnableHotdesking parameter of the **New-CSClientPolicy** cmdlet or the **Set-CSClientPolicy** cmdlet to enable or disable hot desking on a phone, as follows.</span></span> <span data-ttu-id="b1a79-111">从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行这些 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1a79-111">Run these cmdlets from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="b1a79-112">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="b1a79-112">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="enabling-hot-desking"></a><span data-ttu-id="b1a79-113">启用热 desking</span><span class="sxs-lookup"><span data-stu-id="b1a79-113">Enabling hot desking</span></span>

  - <span data-ttu-id="b1a79-114">若要为公共区域电话启用热 desking，您必须修改已分配给该电话 (或) 的电话集合的客户端策略。</span><span class="sxs-lookup"><span data-stu-id="b1a79-114">To enable hot desking for a common area phone, you must modify the client policy that has been assigned to that phone (or collection of phones).</span></span>
    
    <span data-ttu-id="b1a79-115">标识需要修改的策略后，下一步是使用 **set-csclientpolicy** Cmdlet 将 EnableHotdesking 参数设置为 True。</span><span class="sxs-lookup"><span data-stu-id="b1a79-115">After you have identified the policy that needs to be modified, the next step is to use the **Set-CsClientPolicy** cmdlet to set the EnableHotdesking parameter to True.</span></span> <span data-ttu-id="b1a79-116">例如：</span><span class="sxs-lookup"><span data-stu-id="b1a79-116">For example:</span></span>
    
        Set-CsClientPolicy -Identity "CommonAreaPhonePolicy" - EnableHotdesking $True

  - <span data-ttu-id="b1a79-117">或者，你可以使用 **set-csclientpolicy** cmdlet 创建支持热 desking 的新客户端策略。</span><span class="sxs-lookup"><span data-stu-id="b1a79-117">Alternatively, you can use the **New-CsClientPolicy** cmdlet to create a new client policy that enables hot desking.</span></span> <span data-ttu-id="b1a79-118">例如：</span><span class="sxs-lookup"><span data-stu-id="b1a79-118">For example:</span></span>
    
        New-CsClientPolicy -Identity "NewCommonAreaPhonePolicy" - EnableHotdesking $True

</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b1a79-119">创建此策略后，您必须将其分配给合适的公共区域电话。</span><span class="sxs-lookup"><span data-stu-id="b1a79-119">After this policy has been created, you must assign it to the appropriate common area phones.</span></span> <span data-ttu-id="b1a79-120">有关详细信息，请参阅 <A href="lync-server-2013-assign-policies-to-a-common-area-phone.md">在 Lync Server 2013 中将策略分配给常见的区域电话</A>。</span><span class="sxs-lookup"><span data-stu-id="b1a79-120">For details, see <A href="lync-server-2013-assign-policies-to-a-common-area-phone.md">Assign policies in Lync Server 2013 to a common area phone</A>.</span></span>



</div>

<div>

## <a name="disabling-hot-desking"></a><span data-ttu-id="b1a79-121">禁用热 desking</span><span class="sxs-lookup"><span data-stu-id="b1a79-121">Disabling hot desking</span></span>

  - <span data-ttu-id="b1a79-122">若要为公共区域电话禁用热 desking，请 **将 set-csclientpolicy** Cmdlet 的 EnableHotdesking 参数重置为默认值 False。</span><span class="sxs-lookup"><span data-stu-id="b1a79-122">To disable hot desking for a common area phone, reset the EnableHotdesking parameter of the **Set-CsClientPolicy** cmdlet to the default value of False.</span></span> <span data-ttu-id="b1a79-123">例如：</span><span class="sxs-lookup"><span data-stu-id="b1a79-123">For example:</span></span>
    
        Set-CsClientPolicy -Identity "CommonAreaPhonePolicy" - EnableHotdesking $False

</div>

<span data-ttu-id="b1a79-124">有关详细信息，请参阅 [set-csclientpolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) Cmdlet 和 [Set-csclientpolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="b1a79-124">For details, see the Help topics for the [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) cmdlet and the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) cmdlet.</span></span>

<span data-ttu-id="b1a79-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1a79-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

