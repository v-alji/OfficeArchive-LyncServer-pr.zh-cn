---
title: Lync Server 2013： Active Directory cmdlet
description: Lync Server 2013： Active Directory cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory cmdlets
ms:assetid: 313d73cb-f3db-4bc4-8708-de4da1d719c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415640(v=OCS.15)
ms:contentKeyID: 48183769
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c5e87cda24d5517b9c4501523fd06804ea20020
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439469"
---
# <a name="active-directory-cmdlets-in-lync-server-2013"></a><span data-ttu-id="d7745-103">Lync Server 2013 中的 Active Directory cmdlet</span><span class="sxs-lookup"><span data-stu-id="d7745-103">Active Directory cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7745-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7745-104">

<span> </span></span></span>

<span data-ttu-id="d7745-105">_**主题上次修改时间：** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="d7745-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="d7745-106">Active Directory cmdlet 通常由安装程序使用，并且很少会由管理员直接调用。</span><span class="sxs-lookup"><span data-stu-id="d7745-106">The Active Directory cmdlets are typically used by Setup, and will rarely be called directly by an administrator.</span></span> <span data-ttu-id="d7745-107">但是，管理员可以使用这些 cmdlet 准备 (或 unprepare) Microsoft Lync Server 2013 的域或林，并安装所需的 Active Directory 架构文件。</span><span class="sxs-lookup"><span data-stu-id="d7745-107">However, administrators can use these cmdlets to prepare (or unprepare) a domain or forest for Microsoft Lync Server 2013, and to install the required Active Directory schema files.</span></span>

<div>

## <a name="active-directory-cmdlets"></a><span data-ttu-id="d7745-108">Active Directory Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d7745-108">Active Directory Cmdlets</span></span>

<span data-ttu-id="d7745-109">以下是与管理 Lync Server 2013 Active Directory 设置直接相关的 cmdlet 的列表：</span><span class="sxs-lookup"><span data-stu-id="d7745-109">The following is a list of cmdlets that relate directly to managing Lync Server 2013 Active Directory settings:</span></span>

<span data-ttu-id="d7745-110">**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="d7745-110">**Active Directory**</span></span>

  - <span></span>  
    <span data-ttu-id="d7745-111">[Disable-CsAdDomain](https://technet.microsoft.com/library/Gg398785(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-111">[Disable-CsAdDomain](https://technet.microsoft.com/library/Gg398785(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d7745-112">[Enable-CsAdDomain](https://technet.microsoft.com/library/Gg412764(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-112">[Enable-CsAdDomain](https://technet.microsoft.com/library/Gg412764(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d7745-113">[CsAdDomain](https://technet.microsoft.com/library/Gg398453(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-113">[Get-CsAdDomain](https://technet.microsoft.com/library/Gg398453(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d7745-114">[Disable-CsAdForest](https://technet.microsoft.com/library/Gg398122(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-114">[Disable-CsAdForest](https://technet.microsoft.com/library/Gg398122(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d7745-115">[Enable-CsAdForest](https://technet.microsoft.com/library/Gg425713(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-115">[Enable-CsAdForest](https://technet.microsoft.com/library/Gg425713(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d7745-116">[CsAdForest](https://technet.microsoft.com/library/Gg412995(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-116">[Get-CsAdForest](https://technet.microsoft.com/library/Gg412995(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="d7745-117">[CsAdServerSchema](https://technet.microsoft.com/library/Gg413070(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-117">[Get-CsAdServerSchema](https://technet.microsoft.com/library/Gg413070(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="d7745-118">[安装-CsAdServerSchema](https://technet.microsoft.com/library/Gg398681(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d7745-118">[Install-CsAdServerSchema](https://technet.microsoft.com/library/Gg398681(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d7745-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d7745-119">See Also</span></span>


[<span data-ttu-id="d7745-120">Lync Server PowerShell 博客</span><span class="sxs-lookup"><span data-stu-id="d7745-120">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="d7745-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7745-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

