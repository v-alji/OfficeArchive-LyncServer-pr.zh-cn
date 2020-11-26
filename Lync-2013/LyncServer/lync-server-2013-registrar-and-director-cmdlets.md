---
title: Lync Server 2013：注册机构和控制器 cmdlet
description: Lync Server 2013：注册机构和控制器 cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registrar and Director cmdlets
ms:assetid: 327c08ab-7e1e-47c0-b280-a001722c116f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415641(v=OCS.15)
ms:contentKeyID: 48183813
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a0cd1775e2fc4e83e3507cbbea588b57550b8cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436543"
---
# <a name="registrar-and-director-cmdlets-in-lync-server-2013"></a><span data-ttu-id="85d96-103">Lync Server 2013 中的注册机构和主管 cmdlet</span><span class="sxs-lookup"><span data-stu-id="85d96-103">Registrar and Director cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85d96-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85d96-104">

<span> </span></span></span>

<span data-ttu-id="85d96-105">_**主题上次修改时间：** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="85d96-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="85d96-106">注册机构和控制器用于对登录请求进行身份验证，并维护有关用户状态和可用性的信息。</span><span class="sxs-lookup"><span data-stu-id="85d96-106">Registrars and Directors are used to authenticate logon requests and to maintain information about user status and availability.</span></span> <span data-ttu-id="85d96-107">注册机构和控制器 cmdlet 使你能够管理这些服务器的配置设置。</span><span class="sxs-lookup"><span data-stu-id="85d96-107">The Registrar and Director cmdlets enable you to manage configuration settings for these servers.</span></span>

<div>

## <a name="registrar-and-director-cmdlets"></a><span data-ttu-id="85d96-108">注册机构和控制器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="85d96-108">Registrar and Director Cmdlets</span></span>

<span data-ttu-id="85d96-109">以下是与管理注册机构和董事直接相关的 cmdlet 的列表：</span><span class="sxs-lookup"><span data-stu-id="85d96-109">The following is a list of cmdlets that relate directly to managing Registrars and Directors:</span></span>

<span data-ttu-id="85d96-110">**注册机构和董事**</span><span class="sxs-lookup"><span data-stu-id="85d96-110">**Registrars and Directors**</span></span>

  - <span></span>  
    <span data-ttu-id="85d96-111">[Set-CsDirector](https://technet.microsoft.com/library/Gg398565(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-111">[Set-CsDirector](https://technet.microsoft.com/library/Gg398565(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85d96-112">[Reset-CsPoolRegistrarState](https://technet.microsoft.com/library/JJ619172(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-112">[Reset-CsPoolRegistrarState](https://technet.microsoft.com/library/JJ619172(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85d96-113">[Set-CsRegistrar](https://technet.microsoft.com/library/Gg398993(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-113">[Set-CsRegistrar](https://technet.microsoft.com/library/Gg398993(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85d96-114">[CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398483(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-114">[Get-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398483(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85d96-115">[新-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg425893(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-115">[New-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg425893(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85d96-116">[Remove-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398482(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-116">[Remove-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398482(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85d96-117">[Set-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398764(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-117">[Set-CsRegistrarConfiguration](https://technet.microsoft.com/library/Gg398764(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85d96-118">[Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85d96-118">[Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="85d96-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85d96-119">See Also</span></span>


[<span data-ttu-id="85d96-120">Lync Server PowerShell 博客</span><span class="sxs-lookup"><span data-stu-id="85d96-120">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="85d96-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85d96-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

