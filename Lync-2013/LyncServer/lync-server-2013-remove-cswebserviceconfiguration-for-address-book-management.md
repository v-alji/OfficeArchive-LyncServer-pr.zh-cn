---
title: Lync Server 2013：用于通讯簿管理的 Remove-CsWebServiceConfiguration
description: Lync Server 2013：用于通讯簿管理的 Remove-CsWebServiceConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove-CsWebServiceConfiguration for Address Book management
ms:assetid: 91947cad-5cdd-41b9-83e1-650703c55879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429713(v=OCS.15)
ms:contentKeyID: 48184848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 145cb1cb98bcb4c988a8fdaea74a4eae86d5fc4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436424"
---
# <a name="remove-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="b16d0-103">Lync Server 2013 中的通讯簿管理 Remove-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b16d0-103">Remove-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b16d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b16d0-104">

<span> </span></span></span>

<span data-ttu-id="b16d0-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b16d0-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b16d0-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员在本地运行 Remove-CsWebServiceConfiguration cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="b16d0-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Remove-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="b16d0-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="b16d0-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsWebServiceConfiguration"}

<span data-ttu-id="b16d0-108">Remove-CsWebServiceConfiguration cmdlet 允许管理员删除以前创建的 Web 服务配置。</span><span class="sxs-lookup"><span data-stu-id="b16d0-108">The Remove-CsWebServiceConfiguration cmdlet allows an administrator to remove a previously created Web Services configuration.</span></span> <span data-ttu-id="b16d0-109">Cmdlet 无法删除全局 Web 服务配置。</span><span class="sxs-lookup"><span data-stu-id="b16d0-109">The cmdlet cannot remove the global Web Services configuration.</span></span>

<span data-ttu-id="b16d0-110">例如：</span><span class="sxs-lookup"><span data-stu-id="b16d0-110">For example:</span></span>

    Remove-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="b16d0-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b16d0-111">See Also</span></span>


[<span data-ttu-id="b16d0-112">Remove-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b16d0-112">Remove-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration)  
  

<span data-ttu-id="b16d0-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b16d0-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

