---
title: Lync Server 2013：用于通讯簿管理的 New-CsAddressBookConfiguration
description: Lync Server 2013：用于通讯簿管理的 New-CsAddressBookConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsAddressBookConfiguration for Address Book management
ms:assetid: a58ddc8c-ae04-4141-b69e-e45374a67d72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429718(v=OCS.15)
ms:contentKeyID: 48184985
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c85d85fefe701456ad253f1afc69b73093b30996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445447"
---
# <a name="new-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="0a66c-103">Lync Server 2013 中的通讯簿管理 New-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a66c-103">New-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a66c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a66c-104">

<span> </span></span></span>

<span data-ttu-id="0a66c-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0a66c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0a66c-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 New-CsAddressBookConfiguration cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="0a66c-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="0a66c-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="0a66c-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsAddressBookConfiguration"}

<span data-ttu-id="0a66c-108">New-CsAddressBookConfiguration cmdlet 创建新配置以管理通讯簿的行为。</span><span class="sxs-lookup"><span data-stu-id="0a66c-108">The New-CsAddressBookConfiguration cmdlet creates a new configuration to manage the behavior of the Address book.</span></span> <span data-ttu-id="0a66c-109">特定于此 cmdlet 的功能是定义通讯簿服务是否创建客户端下载文件，以及如何使用规范化规则，在合并新的完整文件之前保留增量和精简的增量文件的时间、增量文件大小、创建完整的文件通讯簿所需的时间以及内部应用于同步用户数据库中的信息。</span><span class="sxs-lookup"><span data-stu-id="0a66c-109">Specific to this cmdlet is the ability to define if the Address Book Service creates the client download files, how and if normalization rules are used, how long to retain delta and compact delta files, delta file size before incorporating a new full file creation, what time of day the full file Address Book is created, and what the internal should be for synchronization of information in the User database.</span></span>

<span data-ttu-id="0a66c-110">例如：</span><span class="sxs-lookup"><span data-stu-id="0a66c-110">For example:</span></span>

    New-CsAddressBookConfiguration -Identity site:Redmond -KeepDuration 15 -SynchronizePollingInterval 00:10:00

<div>

## <a name="see-also"></a><span data-ttu-id="0a66c-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a66c-111">See Also</span></span>


[<span data-ttu-id="0a66c-112">新-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a66c-112">New-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsAddressBookConfiguration)  
  

<span data-ttu-id="0a66c-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a66c-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

