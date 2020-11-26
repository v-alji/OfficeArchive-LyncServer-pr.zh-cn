---
title: Lync Server 2013：查看常见的区域电话信息
description: Lync Server 2013：查看常见的区域电话信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View common area phone information
ms:assetid: e652240c-6a3f-4be7-a083-32f24c08e655
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994081(v=OCS.15)
ms:contentKeyID: 51803992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4debe9a76118ac0bf1ca711426ce5487009a053
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443375"
---
# <a name="view-common-area-phone-information-in-lync-server-2013"></a><span data-ttu-id="00ed1-103">在 Lync Server 2013 中查看常见的区域电话信息</span><span class="sxs-lookup"><span data-stu-id="00ed1-103">View common area phone information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00ed1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00ed1-104">

<span> </span></span></span>

<span data-ttu-id="00ed1-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="00ed1-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="00ed1-106">你可以使用 **CsCommonAreaPhone** cmdlet 查看配置为在你的组织中使用的公共区域电话的相关信息。</span><span class="sxs-lookup"><span data-stu-id="00ed1-106">You can view information about the common area phones configured for use in your organization by using the **Get-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="00ed1-107">如果在没有任何参数的情况下使用，此 cmdlet 将返回有关所有公共区域电话的信息。</span><span class="sxs-lookup"><span data-stu-id="00ed1-107">Used without any parameters, this cmdlet returns information about all your common area phones.</span></span> <span data-ttu-id="00ed1-108">可选参数提供不同的筛选信息的方式。</span><span class="sxs-lookup"><span data-stu-id="00ed1-108">Optional parameters provide different ways for you to filter information.</span></span> <span data-ttu-id="00ed1-109">例如，您可以返回在指定组织单位 (OU) 或指定大楼内所有联系人对象中具有联系人对象的所有公共区域电话。</span><span class="sxs-lookup"><span data-stu-id="00ed1-109">For example, you can return all the common area phones that have contact objects in a specified organizational unit (OU) or all the contacts objects located in a specified building.</span></span> <span data-ttu-id="00ed1-110">有关 **CsCommonAreaPhone** 参数的详细信息，请参阅 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)。</span><span class="sxs-lookup"><span data-stu-id="00ed1-110">For details about **Get-CsCommonAreaPhone** parameters, see [Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone).</span></span>

<span data-ttu-id="00ed1-111">从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行 **CsCommonAreaPhone** 。</span><span class="sxs-lookup"><span data-stu-id="00ed1-111">Run **Get-CsCommonAreaPhone** either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


<div>

## <a name="viewing-information-about-all-your-common-area-phones"></a><span data-ttu-id="00ed1-112">查看有关所有常用区域电话的信息</span><span class="sxs-lookup"><span data-stu-id="00ed1-112">Viewing Information about All Your Common Area Phones</span></span>

  - <span data-ttu-id="00ed1-113">若要查看有关所有常用区域电话的信息，请在 Lync Server 命令行管理程序中键入以下命令，然后按 Enter：</span><span class="sxs-lookup"><span data-stu-id="00ed1-113">To view information about all your common area phones, type the following command in the Lync Server Management Shell, and then press Enter:</span></span>
    
        Get-CsCommonAreaPhone
    
    <span data-ttu-id="00ed1-114">您将获得类似以下内容的信息：</span><span class="sxs-lookup"><span data-stu-id="00ed1-114">You’ll get information similar to this:</span></span>
    
        Identity           : CN=Building 14 Lobby,OU=Redmond,
                             DC=litwareinc,DC=com
        RegistrarPool      : atl-cs-001.litwareinc.com
        Enabled            : True
        SipAddress         : sip:4714e34b-9781-421d-b07a-
                             52056b5b4a56@litwareinc.com
        ClientPolicy       :
        PinPolicy          :
        VoicePolicy        :
        MobilityPolicy     :
        GroupChatPolicy    :
        ConferencingPolicy :
        LineURI            : tel:+14255550712
        DisplayNumber      : 1-425-555-0712
        DisplayName        : Building 14 Lobby
        Description        :
        ExUmEnabled        : False

</div>

<span data-ttu-id="00ed1-115">有关详细信息，请参阅 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone) Cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="00ed1-115">For details, see the Help topic for the [Get-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone) cmdlet.</span></span>

<span data-ttu-id="00ed1-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00ed1-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

