---
title: Lync Server 2013：用于通讯簿管理的 Get-CsAddressBookConfiguration
description: Lync Server 2013：用于通讯簿管理的 Get-CsAddressBookConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsAddressBookConfiguration for Address Book management
ms:assetid: bd62f916-caf3-4e10-ada4-631bbb331ef1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429721(v=OCS.15)
ms:contentKeyID: 48185264
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91b96aead7b7038464f3166691a5952b9ff850dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427976"
---
# <a name="get-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="20345-103">Lync Server 2013 中的通讯簿管理 Get-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="20345-103">Get-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20345-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20345-104">

<span> </span></span></span>

<span data-ttu-id="20345-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="20345-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="20345-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 Get-CsAddressBookConfiguration cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="20345-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="20345-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="20345-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsAddressBookConfiguration"}

<span data-ttu-id="20345-108">Cmdlet Get-CsAddressBookConfiguration 返回有关已存在的配置的信息。</span><span class="sxs-lookup"><span data-stu-id="20345-108">The cmdlet Get-CsAddressBookConfiguration returns information about a configuration that already exists.</span></span>

<span data-ttu-id="20345-109">例如：</span><span class="sxs-lookup"><span data-stu-id="20345-109">For example:</span></span>

    Get-CsAddressBookConfiguration -Identity site:Redmond

<span data-ttu-id="20345-110">将 Get-CsAddressBookConfiguration 和 Set-CsAddressBookConfiguration 的功能结合起来，管理员可以定义要修改的配置，然后应用修改。</span><span class="sxs-lookup"><span data-stu-id="20345-110">Combining the functionality of Get-CsAddressBookConfiguration and Set-CsAddressBookConfiguration allows the administrator to define which configurations to modify and then apply the modifications.</span></span> <span data-ttu-id="20345-111">例如，下面的组合：</span><span class="sxs-lookup"><span data-stu-id="20345-111">For example, this combined:</span></span>

    Get-CsAddressBookConfiguration -Filter site:* | Set-CsAddressBookConfiguration -RunTimeOfDay 23:00

<span data-ttu-id="20345-112">返回所有网站中的所有配置，并对配置应用23:00 小时的 RunTimeOfDay。</span><span class="sxs-lookup"><span data-stu-id="20345-112">Returns all configurations in all sites and applies the RunTimeOfDay of 23:00 hours to the configurations.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="20345-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="20345-113">See Also</span></span>


[<span data-ttu-id="20345-114">CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="20345-114">Get-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAddressBookConfiguration)  
  

<span data-ttu-id="20345-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20345-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

