---
title: Lync Server 2013：用于通讯簿管理的 Set-CsWebServiceConfiguration
description: Lync Server 2013：用于通讯簿管理的 Set-CsWebServiceConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set-CsWebServiceConfiguration for Address Book management
ms:assetid: 79d0edf5-23f3-4845-a7b7-e11b5a928bab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429709(v=OCS.15)
ms:contentKeyID: 48184572
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37dcd7676829c5a91e05667fa0ae0d74dc6f7dc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423993"
---
# <a name="set-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="b4968-103">Lync Server 2013 中的通讯簿管理 Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4968-103">Set-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4968-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4968-104">

<span> </span></span></span>

<span data-ttu-id="b4968-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b4968-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b4968-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 Set-CsWebServiceConfiguration cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="b4968-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="b4968-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="b4968-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsWebServiceConfiguration"}

<span data-ttu-id="b4968-108">Set-CsWebServiceConfiguration cmdlet 允许管理员在 Web 服务的配置中重新定义现有属性。</span><span class="sxs-lookup"><span data-stu-id="b4968-108">The Set-CsWebServiceConfiguration cmdlet allows the administrator to redefine an existing attribute in the configuration of the Web Services.</span></span>

<span data-ttu-id="b4968-109">例如：</span><span class="sxs-lookup"><span data-stu-id="b4968-109">For example:</span></span>

    Set-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $True

<div>

## <a name="see-also"></a><span data-ttu-id="b4968-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b4968-110">See Also</span></span>


[<span data-ttu-id="b4968-111">Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4968-111">Set-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)  
  

<span data-ttu-id="b4968-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4968-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

