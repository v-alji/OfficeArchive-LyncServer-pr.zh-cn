---
title: Lync Server 2013：用于通讯簿管理的 Get-CsWebServiceConfiguration
description: Lync Server 2013：用于通讯簿管理的 Get-CsWebServiceConfiguration。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsWebServiceConfiguration for Address Book management
ms:assetid: 0b223733-5224-47d1-9b47-2109e6f135c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429692(v=OCS.15)
ms:contentKeyID: 48183372
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb22d7607f9ac18cda9c8653374ae86839b033e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427941"
---
# <a name="get-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="ef284-103">Lync Server 2013 中的通讯簿管理 Get-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef284-103">Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef284-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef284-104">

<span> </span></span></span>

<span data-ttu-id="ef284-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ef284-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ef284-106">哪些人可以运行此 cmdlet：默认情况下，授权以下组的成员在本地运行 Get-CsWebServiceConfiguration cmdlet： RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="ef284-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsWebServiceConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="ef284-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="ef284-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsWebServiceConfiguration"}

<span data-ttu-id="ef284-108">Get-CsWebServiceConfiguration 返回您的组织中当前使用的 Web 服务配置的信息。</span><span class="sxs-lookup"><span data-stu-id="ef284-108">Get-CsWebServiceConfiguration returns information of the Web Services configuration currently in use in your organization.</span></span> <span data-ttu-id="ef284-109">通讯簿服务感兴趣是通讯组列表扩展功能的状态。</span><span class="sxs-lookup"><span data-stu-id="ef284-109">Of interest to the Address Book Services is the status of Distribution List Expansion function.</span></span> <span data-ttu-id="ef284-110">如果属性 EnableGroupExpansion 为 True，则您的组织当前允许组扩展。</span><span class="sxs-lookup"><span data-stu-id="ef284-110">If the attribute EnableGroupExpansion is True, your organization currently allows group expansion.</span></span>

<span data-ttu-id="ef284-111">例如：</span><span class="sxs-lookup"><span data-stu-id="ef284-111">For example:</span></span>

    Get-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="ef284-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ef284-112">See Also</span></span>


[<span data-ttu-id="ef284-113">CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef284-113">Get-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWebServiceConfiguration)  
  

<span data-ttu-id="ef284-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef284-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

