---
title: Lync Server 2013：通讯簿服务器 cmdlet
description: Lync Server 2013：通讯簿服务器 cmdlet。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Address Book Server cmdlets
ms:assetid: 33da45da-3c57-4d04-9679-f0e5a0cfd37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415643(v=OCS.15)
ms:contentKeyID: 48183793
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4fef903d25f0d2707410e017f4eb280282bbdab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439994"
---
# <a name="address-book-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="eac97-103">Lync Server 2013 中的通讯簿服务器 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eac97-103">Address Book Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eac97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eac97-104">

<span> </span></span></span>

<span data-ttu-id="eac97-105">_**主题上次修改时间：** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="eac97-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="eac97-106">通讯簿服务器是 Active Directory 域服务和 Microsoft Lync Server 2013 之间的媒介。</span><span class="sxs-lookup"><span data-stu-id="eac97-106">Address Book servers are intermediaries between Active Directory Domain Services and Microsoft Lync Server 2013.</span></span> <span data-ttu-id="eac97-107">通讯簿服务器确保存储在 Lync Server 2013 中的用户信息与 Active Directory 中存储的用户信息同步。</span><span class="sxs-lookup"><span data-stu-id="eac97-107">The Address Book server ensures that the user information stored in Lync Server 2013 is in synch with the user information stored in Active Directory.</span></span> <span data-ttu-id="eac97-108">这是通过使用存储在用户数据库中的信息定期同步通讯录文件完成的。</span><span class="sxs-lookup"><span data-stu-id="eac97-108">This is done by periodically synching Address Book files with information stored in the User database.</span></span> <span data-ttu-id="eac97-109">因此，Lync Server 包含许多用于管理通讯簿服务器的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eac97-109">In turn, Lync Server includes a number of cmdlets for managing Address Book servers.</span></span>

<div>

## <a name="address-book-server-cmdlets"></a><span data-ttu-id="eac97-110">通讯簿服务器 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eac97-110">Address Book Server Cmdlets</span></span>

<span data-ttu-id="eac97-111">不能在 Lync Server "控制面板" 中配置通讯簿服务器设置。</span><span class="sxs-lookup"><span data-stu-id="eac97-111">You cannot configure the Address Book Server settings in Lync Server Control Panel.</span></span> <span data-ttu-id="eac97-112">Windows PowerShell 是用于管理这些设置的主要工具。</span><span class="sxs-lookup"><span data-stu-id="eac97-112">Windows PowerShell is the primary tool for managing these settings.</span></span> <span data-ttu-id="eac97-113">以下是与管理通讯簿服务器直接相关的 cmdlet 的列表：</span><span class="sxs-lookup"><span data-stu-id="eac97-113">The following is a list of cmdlets that relate directly to managing the Address Book Server:</span></span>

<span data-ttu-id="eac97-114">**通讯簿服务器**</span><span class="sxs-lookup"><span data-stu-id="eac97-114">**Address Book Server**</span></span>

  - <span></span>  
    <span data-ttu-id="eac97-115">[CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="eac97-116">[新-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-116">[New-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="eac97-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="eac97-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="eac97-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="eac97-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="eac97-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="eac97-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="eac97-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="eac97-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eac97-123">See Also</span></span>


[<span data-ttu-id="eac97-124">Lync Server PowerShell 博客</span><span class="sxs-lookup"><span data-stu-id="eac97-124">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="eac97-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eac97-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

