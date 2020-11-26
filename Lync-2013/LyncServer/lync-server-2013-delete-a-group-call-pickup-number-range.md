---
title: Lync Server 2013：删除组呼叫装货号码范围
description: Lync Server 2013：删除组呼叫装货号码范围。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Group Call Pickup number range
ms:assetid: 521891f3-7a5d-45de-92dc-d57025453159
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945629(v=OCS.15)
ms:contentKeyID: 51541475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b40d423b64d29300741c55433864128897c3ac8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430705"
---
# <a name="delete-a-group-call-pickup-number-range-in-lync-server-2013"></a><span data-ttu-id="37cce-103">在 Lync Server 2013 中删除组呼叫装货号码范围</span><span class="sxs-lookup"><span data-stu-id="37cce-103">Delete a Group Call Pickup number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37cce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37cce-104">

<span> </span></span></span>

<span data-ttu-id="37cce-105">_**主题上次修改时间：** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="37cce-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="37cce-106">使用以下过程删除组呼叫装货号码范围。</span><span class="sxs-lookup"><span data-stu-id="37cce-106">Use the following procedure to delete a Group Call Pickup number range.</span></span>

<div>

## <a name="to-delete-a-call-pickup-group-number-range"></a><span data-ttu-id="37cce-107">删除呼叫装货组号范围</span><span class="sxs-lookup"><span data-stu-id="37cce-107">To delete a call pickup group number range</span></span>

1.  <span data-ttu-id="37cce-108">以 RTCUniversalServerAdmins 组成员的身份或必要的用户权限登录到安装了 Lync Server 管理外壳的计算机，如在 [Lync Server 2013 中的 "委派设置权限](lync-server-2013-delegate-setup-permissions.md)" 中所述。</span><span class="sxs-lookup"><span data-stu-id="37cce-108">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="37cce-109">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="37cce-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="37cce-110">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="37cce-110">At the command line, type:</span></span>
    
        Remove-CsCallParkOrbit -Identity "<group number range name>" 
    
    <span data-ttu-id="37cce-111">例如：</span><span class="sxs-lookup"><span data-stu-id="37cce-111">For example:</span></span>
    
        Remove-CsCallParkOrbit -Identity "Redmond call pickup"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="37cce-112">有关更多选项的详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>。</span><span class="sxs-lookup"><span data-stu-id="37cce-112">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="37cce-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="37cce-113">See Also</span></span>


[<span data-ttu-id="37cce-114">在 Lync Server 2013 中创建或修改呼叫寄存的轨道范围</span><span class="sxs-lookup"><span data-stu-id="37cce-114">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)  


[<span data-ttu-id="37cce-115">Remove-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="37cce-115">Remove-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit)  
[<span data-ttu-id="37cce-116">CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="37cce-116">Get-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCallParkOrbit)  
  

<span data-ttu-id="37cce-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37cce-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

