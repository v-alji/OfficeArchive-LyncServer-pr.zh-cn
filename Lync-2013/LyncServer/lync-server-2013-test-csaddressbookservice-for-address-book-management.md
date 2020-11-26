---
title: Lync Server 2013：用于通讯簿管理的 Test-CsAddressBookService
description: Lync Server 2013：用于通讯簿管理的 Test-CsAddressBookService。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookService for Address Book management
ms:assetid: b88cea74-41fd-4c0e-9284-7135bff27a27
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429720(v=OCS.15)
ms:contentKeyID: 48185206
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 345886c68c814534fcbfd4debfd3be8562fae5a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444278"
---
# <a name="test-csaddressbookservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="9f192-103">Lync Server 2013 中的通讯簿管理 Test-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="9f192-103">Test-CsAddressBookService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f192-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f192-104">

<span> </span></span></span>

<span data-ttu-id="9f192-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9f192-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9f192-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员运行 Test-CsAddressBookService cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="9f192-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookService cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="9f192-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="9f192-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

<span data-ttu-id="9f192-108">Lync Server 2013 包含许多用于启动合成命令的 cmdlet，用于确认特定的函数或功能是否正常工作。</span><span class="sxs-lookup"><span data-stu-id="9f192-108">Lync Server 2013 contains a number of cmdlets that initiate synthetic commands to confirm that a specific function or feature is working properly.</span></span> <span data-ttu-id="9f192-109">Test-CsAddressBookService 确认已定义的用户可以通过通讯簿 Web 服务连接和请求本地文件。</span><span class="sxs-lookup"><span data-stu-id="9f192-109">Test-CsAddressBookService confirms that a defined user can connect and request the local files from the Address Book Web service.</span></span>

<span data-ttu-id="9f192-110">例如：</span><span class="sxs-lookup"><span data-stu-id="9f192-110">For example:</span></span>

    Test-CsAddressBookService -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a><span data-ttu-id="9f192-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9f192-111">See Also</span></span>


[<span data-ttu-id="9f192-112">Test-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="9f192-112">Test-CsAddressBookService</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService)  
  

<span data-ttu-id="9f192-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f192-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

