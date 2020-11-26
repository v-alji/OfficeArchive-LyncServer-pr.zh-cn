---
title: Lync Server 2013：用于通讯簿管理的 Set-CsAddressBookConfiguration
description: Lync Server 2013：用于通讯簿管理的 Set-CsAddressBookConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set-CsAddressBookConfiguration for Address Book management
ms:assetid: 3a64ceb1-9f79-4f3b-bf33-eaf346dbd60d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429700(v=OCS.15)
ms:contentKeyID: 48183913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab7a58510b2bb6232d9908c77cf6b70bbeb927f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444754"
---
# <a name="set-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="8713b-103">Lync Server 2013 中的通讯簿管理 Set-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="8713b-103">Set-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8713b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8713b-104">

<span> </span></span></span>

<span data-ttu-id="8713b-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8713b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8713b-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 Set-CsAddressBookConfiguration cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="8713b-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="8713b-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="8713b-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsAddressBookConfiguration"}

<span data-ttu-id="8713b-108">Set-CsAddressBookConfiguration 与 New-CsAddressBookConfiguration cmdlet 类似，但它用于修改现有配置。</span><span class="sxs-lookup"><span data-stu-id="8713b-108">Set-CsAddressBookConfiguration is similar to the New-CsAddressBookConfiguration cmdlet, except it is used to modify an existing configuration.</span></span>

<span data-ttu-id="8713b-109">例如：</span><span class="sxs-lookup"><span data-stu-id="8713b-109">For example:</span></span>

    Set-CsAddressBookConfiguration -identity site:Redmond -RunTimeOfDay 23:00

<div>

## <a name="see-also"></a><span data-ttu-id="8713b-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8713b-110">See Also</span></span>


[<span data-ttu-id="8713b-111">Set-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="8713b-111">Set-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsAddressBookConfiguration)  
  

<span data-ttu-id="8713b-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8713b-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

