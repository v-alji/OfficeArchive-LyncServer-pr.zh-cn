---
title: Lync Server 2013：准备域
description: Lync Server 2013：准备域。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing domains
ms:assetid: 8eea541c-5f9d-4afc-92a8-a31d6f742544
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398721(v=OCS.15)
ms:contentKeyID: 48184816
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7700bbdd10a96949f892858ae03da8de60d86a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424161"
---
# <a name="preparing-domains-for-lync-server-2013"></a><span data-ttu-id="85514-103">为 Lync Server 2013 准备域</span><span class="sxs-lookup"><span data-stu-id="85514-103">Preparing domains for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85514-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85514-104">

<span> </span></span></span>

<span data-ttu-id="85514-105">_**主题上次修改时间：** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="85514-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="85514-106">域准备是为 Lync Server 2013 准备 Active Directory 域服务的最后一步。</span><span class="sxs-lookup"><span data-stu-id="85514-106">Domain preparation is the final step in preparing Active Directory Domain Services for Lync Server 2013.</span></span> <span data-ttu-id="85514-107">域准备步骤将向通用组添加必要的访问控制项 (ACE)，这些访问控制项将授予承载和管理域中用户的权限。</span><span class="sxs-lookup"><span data-stu-id="85514-107">The domain preparation step adds the necessary access control entries (ACEs) to universal groups that grant permissions to host and manage users within the domain.</span></span> <span data-ttu-id="85514-108">域准备过程将在域根和以下三个内置容器中创建 ACE：“用户”、“计算机”和“域控制器”。</span><span class="sxs-lookup"><span data-stu-id="85514-108">Domain preparation creates ACEs on the domain root and three built-in containers: User, Computers, and Domain Controllers.</span></span>

<span data-ttu-id="85514-109">可以在要部署 Lync Server 的域中的任何计算机上运行域准备。</span><span class="sxs-lookup"><span data-stu-id="85514-109">You can run domain preparation on any computer in the domain where you are deploying Lync Server.</span></span> <span data-ttu-id="85514-110">你必须准备将托管 Lync Server 或用户的每个域。</span><span class="sxs-lookup"><span data-stu-id="85514-110">You must prepare every domain that will host Lync Server or users.</span></span>

<span data-ttu-id="85514-111">如果已禁用权限继承或已禁用身份验证用户权限在你的组织中被禁用，则必须在域准备期间执行其他步骤。</span><span class="sxs-lookup"><span data-stu-id="85514-111">If permissions inheritance is disabled or authenticated user permissions are disabled in your organization, you must perform additional steps during domain preparation.</span></span> <span data-ttu-id="85514-112">有关详细信息，请参阅 [在 Lync Server 2013 中准备锁定的 Active Directory 域服务](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="85514-112">For details, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md).</span></span>

<span data-ttu-id="85514-113">如果你的组织使用组织单位 (OU) 而不是) 的三个内置容器 (（用户、计算机和域控制器），则必须向 "已验证用户" 组的 Ou 授予 "读取" 访问权限。</span><span class="sxs-lookup"><span data-stu-id="85514-113">If your organization uses organizational units (OU) instead of the three built-in containers (that is, Users, Computers, and Domain Controllers), you must grant read access to the OUs for the Authenticated Users group.</span></span> <span data-ttu-id="85514-114">域准备需要对容器的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="85514-114">Read access to the containers is required for domain preparation.</span></span> <span data-ttu-id="85514-115">如果 "经过身份验证的用户组" 对 OU 没有 "读取" 访问权限，请运行 **CsOuPermission** cmdlet，如下代码示例所示，为每个 OU 授予读取权限。</span><span class="sxs-lookup"><span data-stu-id="85514-115">If the Authenticated Users group does not have read access to the OU, run the **Grant-CsOuPermission** cmdlet as illustrated in the following code examples to grant read permissions for each OU.</span></span>

   ```PowerShell
    Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU > 
   ```

   ```PowerShell
    Grant-CsOuPermission -ObjectType "user","contact",inetOrgPerson" -OU "ou=Redmond,dc=contoso,dc=net"
   ```

<span data-ttu-id="85514-116">有关 **CsOuPermission** cmdlet 的详细信息，请参阅 Lync Server Management Shell 文档。</span><span class="sxs-lookup"><span data-stu-id="85514-116">For details about the **Grant-CsOuPermission** cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div class="">


> [!TIP]  
> <span data-ttu-id="85514-117">有关在域根和 "用户"、"计算机" 和 "域控制器" 容器中创建的 Ace 的详细信息，请参阅 <A href="lync-server-2013-changes-made-by-domain-preparation.md">Lync Server 2013 中的域准备所做的更改</A>。</span><span class="sxs-lookup"><span data-stu-id="85514-117">For details about the ACEs created on the domain root and in the Users, Computers, and Domain Controllers containers, see <A href="lync-server-2013-changes-made-by-domain-preparation.md">Changes made by domain preparation in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="85514-118">本节内容</span><span class="sxs-lookup"><span data-stu-id="85514-118">In This Section</span></span>

  - [<span data-ttu-id="85514-119">为 Lync Server 2013 运行域准备</span><span class="sxs-lookup"><span data-stu-id="85514-119">Running domain preparation for Lync Server 2013</span></span>](lync-server-2013-running-domain-preparation.md)

  - [<span data-ttu-id="85514-120">使用 Cmdlet 为 Lync Server 2013 反向执行域准备</span><span class="sxs-lookup"><span data-stu-id="85514-120">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)

<span data-ttu-id="85514-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85514-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

