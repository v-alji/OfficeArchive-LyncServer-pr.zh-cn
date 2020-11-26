---
title: Lync Server 2013：用于通讯簿管理的 Test-CsAddressBookWebQuery
description: Lync Server 2013：用于通讯簿管理的 Test-CsAddressBookWebQuery。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookWebQuery for Address Book management
ms:assetid: 977a9c1f-5f4e-4539-9a26-8748b61a57d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429716(v=OCS.15)
ms:contentKeyID: 48184865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7448733ed1477d36b887648154d66c96f9e6d0b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441254"
---
# <a name="test-csaddressbookwebquery-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="99579-103">Lync Server 2013 中的通讯簿管理 Test-CsAddressBookWebQuery</span><span class="sxs-lookup"><span data-stu-id="99579-103">Test-CsAddressBookWebQuery for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99579-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99579-104">

<span> </span></span></span>

<span data-ttu-id="99579-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="99579-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="99579-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员运行 Test-CsAddressBookWebQuery cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="99579-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookWebQuery cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="99579-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="99579-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

<span data-ttu-id="99579-108">与 Test-CsAddressBookService 综合事务类似，Test-CsAddressBookWebQuery 对通讯簿 Web 查询执行查询以确保其正常运行。</span><span class="sxs-lookup"><span data-stu-id="99579-108">Similar to the Test-CsAddressBookService synthetic transaction, Test-CsAddressBookWebQuery performs a query against the Address Book Web Query to ensure that it is operating properly.</span></span> <span data-ttu-id="99579-109">该 cmdlet 将连接到 Web 票证身份验证，并显示在-UserCredential 中指定的凭据。</span><span class="sxs-lookup"><span data-stu-id="99579-109">The cmdlet will connect to the Web Ticket authentication and present the credentials specified in –UserCredential.</span></span> <span data-ttu-id="99579-110">如果经过身份验证，则 cmdlet 将呈现-TargetSipAddress 信息。</span><span class="sxs-lookup"><span data-stu-id="99579-110">If authenticated, the cmdlet then present the –TargetSipAddress information.</span></span> <span data-ttu-id="99579-111">如果该 cmdlet 能够检索有关该联系人的信息，则该 cmdlet 应报告成功。</span><span class="sxs-lookup"><span data-stu-id="99579-111">The cmdlet should report success if it was able to retrieve the information about the contact.</span></span>

<span data-ttu-id="99579-112">例如：</span><span class="sxs-lookup"><span data-stu-id="99579-112">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com" -TargetSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a><span data-ttu-id="99579-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="99579-113">See Also</span></span>


[<span data-ttu-id="99579-114">Test-CsAddressBookWebQuery</span><span class="sxs-lookup"><span data-stu-id="99579-114">Test-CsAddressBookWebQuery</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery)  
  

<span data-ttu-id="99579-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99579-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

