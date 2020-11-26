---
title: Lync Server 2013：用于通讯簿管理的 New-CsClientPolicy
description: Lync Server 2013：用于通讯簿管理的 New-CsClientPolicy。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsClientPolicy for Address Book management
ms:assetid: ef4415fc-82c4-4dc8-97d1-37a084553343
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429726(v=OCS.15)
ms:contentKeyID: 48185771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12c14534c7af447f30a01b1bbbd1679a8375c705
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425107"
---
# <a name="new-csclientpolicy-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="caf30-103">Lync Server 2013 中的通讯簿管理 New-CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="caf30-103">New-CsClientPolicy for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="caf30-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="caf30-104">

<span> </span></span></span>

<span data-ttu-id="caf30-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="caf30-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="caf30-106">哪些人可以运行此 cmdlet：默认情况下，已授权以下组的成员运行 New-CsClientPolicy cmdlet： RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="caf30-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsClientPolicy cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="caf30-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="caf30-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsClientPolicy"}

<span data-ttu-id="caf30-108">Cmdlet New-CsClientPolicy 为 Lync Server 2013 中提供的功能定义了大量设置，用于设置客户端。</span><span class="sxs-lookup"><span data-stu-id="caf30-108">The cmdlet New-CsClientPolicy defines a large number of settings for provisioning clients for features that are available in Lync Server 2013.</span></span> <span data-ttu-id="caf30-109">对于通讯簿服务，参数 AddressBookAvailability 是重要的。</span><span class="sxs-lookup"><span data-stu-id="caf30-109">For the Address Book Service, the parameter AddressBookAvailability is of interest.</span></span> <span data-ttu-id="caf30-110">此参数直接影响客户端可用的选项，有三种可能的选项：</span><span class="sxs-lookup"><span data-stu-id="caf30-110">This parameter, which directly impacts the options available to clients, has three possible options:</span></span>

  - <span data-ttu-id="caf30-111">WebSearchAndFileDownload</span><span class="sxs-lookup"><span data-stu-id="caf30-111">WebSearchAndFileDownload</span></span>

  - <span data-ttu-id="caf30-112">WebSearchOnly</span><span class="sxs-lookup"><span data-stu-id="caf30-112">WebSearchOnly</span></span>

  - <span data-ttu-id="caf30-113">FileDownloadOnly</span><span class="sxs-lookup"><span data-stu-id="caf30-113">FileDownloadOnly</span></span>

<span data-ttu-id="caf30-114">定义后，它决定了客户端如何访问通讯簿。</span><span class="sxs-lookup"><span data-stu-id="caf30-114">When defined, it determines how the Address Book is accessed by clients.</span></span> <span data-ttu-id="caf30-115">如果定义此参数，则必须定义其中一个选项。</span><span class="sxs-lookup"><span data-stu-id="caf30-115">If you define this parameter, you must define one of the options.</span></span> <span data-ttu-id="caf30-116">如果不修改此设置，则默认 WebSearchAndFileDownload 保持有效。</span><span class="sxs-lookup"><span data-stu-id="caf30-116">If you do not modify this setting, the default WebSearchAndFileDownload remains in effect.</span></span>

<span data-ttu-id="caf30-117">例如：</span><span class="sxs-lookup"><span data-stu-id="caf30-117">For example:</span></span>

    New-CsClientPolicy -Identity RedmondClientPolicy -DisableCalendarPresence $True -DisablePhonePresence $True -DisplayPhoto "PhotosFromADOnly" -AddressBookAvailability "WebSearchOnly"

<div>

## <a name="see-also"></a><span data-ttu-id="caf30-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="caf30-118">See Also</span></span>


[<span data-ttu-id="caf30-119">新-Set-csclientpolicy</span><span class="sxs-lookup"><span data-stu-id="caf30-119">New-CsClientPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy)  
  

<span data-ttu-id="caf30-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="caf30-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

