---
title: Lync Server 2013：用于通讯簿管理的 Update-CsAddressBook
description: Lync Server 2013：用于通讯簿管理的 Update-CsAddressBook。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Update-CsAddressBook for Address Book management
ms:assetid: 0ffd2ef8-201c-44aa-8c64-1c7b0eaa7d48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429695(v=OCS.15)
ms:contentKeyID: 48183428
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4adc7f94e2f31f64f6517b8cdf9bbcb0649f6c8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392261"
---
# <a name="update-csaddressbook-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="18a2a-103">Lync Server 2013 中的通讯簿管理 Update-CsAddressBook</span><span class="sxs-lookup"><span data-stu-id="18a2a-103">Update-CsAddressBook for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18a2a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18a2a-104">

<span> </span></span></span>

<span data-ttu-id="18a2a-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="18a2a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="18a2a-106">哪些人可以运行此 cmdlet：默认情况下，授权以下组的成员在本地运行 Update-CsAddressBook cmdlet： RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="18a2a-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Update-CsAddressBook cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="18a2a-107">若要返回所有基于角色的访问控制列表 (RBAC) 角色已将此 cmdlet 分配给 (包括你自己创建的任何自定义 RBAC 角色) ，请从 Windows PowerShell 提示符处运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="18a2a-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Update-CsAddressBook"}

<span data-ttu-id="18a2a-108">Update-CsAddressBook cmdlet 替换 Office 通信服务器中的 **abserver.exe-syncNow** 命令。</span><span class="sxs-lookup"><span data-stu-id="18a2a-108">The Update-CsAddressBook cmdlet replaces the **abserver.exe –syncNow** command from Office Communications Server.</span></span> <span data-ttu-id="18a2a-109">该 cmdlet 的用途是立即启动同步，而不是等待计划的时间。</span><span class="sxs-lookup"><span data-stu-id="18a2a-109">The cmdlet’s purpose is to initiate a synchronization immediately rather than waiting for the scheduled time.</span></span> <span data-ttu-id="18a2a-110">第一个示例命令将更新组织中的所有通讯簿。</span><span class="sxs-lookup"><span data-stu-id="18a2a-110">The first example command updates all Address Books in the organization.</span></span> <span data-ttu-id="18a2a-111">第二个更新仅更新与已定义服务器相关联的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="18a2a-111">The second updates only the Address Book associated with the defined server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="18a2a-112">在 Lync Server 2013 中，Lync Server 用户复制程序将从 Active Directory 中获取更改，并根据配置的间隔更新 Lync Server 用户数据库。</span><span class="sxs-lookup"><span data-stu-id="18a2a-112">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="18a2a-113">Lync Server 用户复制程序还将在无需运行 CSAddressBook 的情况下快速将更改传播到 RTCab 数据库。</span><span class="sxs-lookup"><span data-stu-id="18a2a-113">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="18a2a-114">只有当通讯簿文件下载已启用时，管理员才需要运行 CSAddressBook 更新。</span><span class="sxs-lookup"><span data-stu-id="18a2a-114">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>



</div>

<span data-ttu-id="18a2a-115">例如：</span><span class="sxs-lookup"><span data-stu-id="18a2a-115">For example:</span></span>

   ```PowerShell
    Update-CsAddressBook
   ```

   ```PowerShell
    Update-CsAddressBook -Fqdn atl-abs-001.contoso.com
   ```

<div>

## <a name="see-also"></a><span data-ttu-id="18a2a-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18a2a-116">See Also</span></span>


[<span data-ttu-id="18a2a-117">Update-CsAddressBook</span><span class="sxs-lookup"><span data-stu-id="18a2a-117">Update-CsAddressBook</span></span>](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook)  
  

<span data-ttu-id="18a2a-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18a2a-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

