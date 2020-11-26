---
title: Lync Server 2013：调用寄存应用程序 cmdlet
description: Lync Server 2013：调用寄存应用程序 cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park application cmdlets
ms:assetid: 30cc001f-b29e-4d44-bad7-65e1133e67b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415639(v=OCS.15)
ms:contentKeyID: 48183764
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25d37e8cfad022e9e8478e68f158e1838bdcca5b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435717"
---
# <a name="call-park-application-cmdlets-in-lync-server-2013"></a><span data-ttu-id="c9a08-103">在 Lync Server 2013 中调用寄存应用程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c9a08-103">Call Park application cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9a08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9a08-104">

<span> </span></span></span>

<span data-ttu-id="c9a08-105">_**主题上次修改时间：** 2012-03-21_</span><span class="sxs-lookup"><span data-stu-id="c9a08-105">_**Topic Last Modified:** 2012-03-21_</span></span>

<span data-ttu-id="c9a08-106">呼叫驻留应用程序允许用户将呼叫置于保持状态，然后从其他电话检索该呼叫。</span><span class="sxs-lookup"><span data-stu-id="c9a08-106">Call Park application allows a user to place a call on hold, then retrieve that call from a different phone.</span></span> <span data-ttu-id="c9a08-107">使用这些 cmdlet 配置呼叫寄存轨道式和呼叫寄存应用程序的设置。</span><span class="sxs-lookup"><span data-stu-id="c9a08-107">Use these cmdlets to configure settings for call park orbits and the Call Park application.</span></span>

<div>

## <a name="call-park-application-cmdlets"></a><span data-ttu-id="c9a08-108">呼叫寄存应用程序 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c9a08-108">Call Park Application Cmdlets</span></span>

<span data-ttu-id="c9a08-109">以下 cmdlet 可用于管理呼叫驻留应用程序。</span><span class="sxs-lookup"><span data-stu-id="c9a08-109">The following cmdlets can be used to manage Call Park application.</span></span>

<span data-ttu-id="c9a08-110">**呼叫寄存应用程序**</span><span class="sxs-lookup"><span data-stu-id="c9a08-110">**Call Park Application**</span></span>

  - <span></span>  
    <span data-ttu-id="c9a08-111">[CsCallParkOrbit](https://technet.microsoft.com/library/Gg398554(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-111">[Get-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398554(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="c9a08-112">[新-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398936(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-112">[New-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398936(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="c9a08-113">[Remove-CsCallParkOrbit](https://technet.microsoft.com/library/Gg412901(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-113">[Remove-CsCallParkOrbit](https://technet.microsoft.com/library/Gg412901(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="c9a08-114">[Set-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398796(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-114">[Set-CsCallParkOrbit](https://technet.microsoft.com/library/Gg398796(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="c9a08-115">[Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/library/Gg412836(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-115">[Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/library/Gg412836(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="c9a08-116">[CsCpsConfiguration](https://technet.microsoft.com/library/Gg398948(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-116">[Get-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398948(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="c9a08-117">[新-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412919(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-117">[New-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412919(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="c9a08-118">[Remove-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398358(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-118">[Remove-CsCpsConfiguration](https://technet.microsoft.com/library/Gg398358(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="c9a08-119">[Set-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412721(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="c9a08-119">[Set-CsCpsConfiguration](https://technet.microsoft.com/library/Gg412721(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c9a08-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c9a08-120">See Also</span></span>


[<span data-ttu-id="c9a08-121">Lync Server PowerShell 博客</span><span class="sxs-lookup"><span data-stu-id="c9a08-121">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="c9a08-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9a08-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

