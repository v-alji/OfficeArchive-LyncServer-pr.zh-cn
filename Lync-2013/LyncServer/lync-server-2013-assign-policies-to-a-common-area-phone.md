---
title: Lync Server 2013：为公共区域电话分配策略
description: Lync Server 2013：为公共区域电话分配策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign policies to a common area phone
ms:assetid: f0554fd1-b237-49b3-9eb4-26f4b91f5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994082(v=OCS.15)
ms:contentKeyID: 51803993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe437ec87ba30eff834239db2b4815adb2d5718c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438314"
---
# <a name="assign-policies-in-lync-server-2013-to-a-common-area-phone"></a><span data-ttu-id="acb72-103">在 Lync Server 2013 中将策略分配到常见的区域电话</span><span class="sxs-lookup"><span data-stu-id="acb72-103">Assign policies in Lync Server 2013 to a common area phone</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="acb72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="acb72-104">

<span> </span></span></span>

<span data-ttu-id="acb72-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="acb72-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="acb72-106">为常见的区域电话创建策略后 (有关详细信息，请参阅 [在 Lync Server 2013) 中创建语音策略和配置 PSTN 使用记录](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md) ，您可以使用 Windows PowerShell 和相应的 **Grant** cmdlet 将该策略分配到公共的区域电话。</span><span class="sxs-lookup"><span data-stu-id="acb72-106">After you create your policy for common area phones (for details, see [Create a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), you can assign the policy to a common area phone by using Windows PowerShell and the appropriate **Grant-Cs** cmdlet.</span></span> <span data-ttu-id="acb72-107">这些 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="acb72-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="acb72-108">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="acb72-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="assigning-a-policy-to-a-single-common-area-phone"></a><span data-ttu-id="acb72-109">向单个公共区域电话分配策略</span><span class="sxs-lookup"><span data-stu-id="acb72-109">Assigning a Policy to a Single Common Area Phone</span></span>

  - <span data-ttu-id="acb72-110">以下命令将每用户语音策略 RedmondVoice 分配给具有标识建筑物14会议厅的通用区域电话。</span><span class="sxs-lookup"><span data-stu-id="acb72-110">The following command assigns the per-user voice policy RedmondVoice to the common area phone that has the Identity Building 14 Lobby.</span></span>
    
        Grant-CsVoicePolicy -Identity "Building 14 Lobby" -PolicyName "RedmondVoicePolicy"

</div>

<div>

## <a name="assigning-a-policy-to-multiple-common-area-phones"></a><span data-ttu-id="acb72-111">向多个公共区域电话分配策略</span><span class="sxs-lookup"><span data-stu-id="acb72-111">Assigning a Policy to Multiple Common Area Phones</span></span>

  - <span data-ttu-id="acb72-112">在此示例中，每用户语音策略 RedmondVoice 分配给所有配置为在组织中使用的常用区域电话。</span><span class="sxs-lookup"><span data-stu-id="acb72-112">In this example, the per-user voice policy RedmondVoice is assigned to all the common area phones configured for use in the organization.</span></span>
    
        Get-CsCommonAreaPhone | Grant-CsVoicePolicy  -PolicyName "RedmondVoicePolicy"

</div>

<span data-ttu-id="acb72-113">有关详细信息，请参阅 [授权 CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy)的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="acb72-113">For details, see the Help topics for the [Grant-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="acb72-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="acb72-114">See Also</span></span>


[<span data-ttu-id="acb72-115">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="acb72-115">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="acb72-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="acb72-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

