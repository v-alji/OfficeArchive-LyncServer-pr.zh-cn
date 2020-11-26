---
title: Lync Server 2013：为 Lync Server 添加和启用用户帐户
description: Lync Server 2013：为 Lync Server 添加和启用用户帐户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add and enable user account for Lync Server
ms:assetid: 1edd1c1c-307d-450b-abea-33aaf56bdf13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520961(v=OCS.15)
ms:contentKeyID: 48183578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f70ae2da122a0db3986a75677c1d29234fbe0e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439371"
---
# <a name="add-and-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="4146f-103">为 Lync Server 2013 添加和启用用户帐户</span><span class="sxs-lookup"><span data-stu-id="4146f-103">Add and enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4146f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4146f-104">

<span> </span></span></span>

<span data-ttu-id="4146f-105">_**主题上次修改时间：** 2012-11-02_</span><span class="sxs-lookup"><span data-stu-id="4146f-105">_**Topic Last Modified:** 2012-11-02_</span></span>

<span data-ttu-id="4146f-106">启用 Active Directory 用户和计算机中的用户帐户后，您可以使用 Lync Server 控制面板通过将 Active Directory 用户添加到 Lync Server 来创建和启用新的 Lync Server 2013 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="4146f-106">After enabling a user account in Active Directory Users and Computers, you can use Lync Server Control Panel to create and enable new Lync Server 2013 user accounts by adding an Active Directory user to Lync Server.</span></span>

<div>

## <a name="to-add-and-enable-a-new-lync-server-user"></a><span data-ttu-id="4146f-107">添加和启用新的 Lync 服务器用户</span><span class="sxs-lookup"><span data-stu-id="4146f-107">To add and enable a new Lync Server user</span></span>

1.  <span data-ttu-id="4146f-108">使用分配给 CsUserAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="4146f-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4146f-109">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="4146f-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4146f-110">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="4146f-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4146f-111">在左导航栏中，单击“用户”。</span><span class="sxs-lookup"><span data-stu-id="4146f-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="4146f-112">单击 " **启用用户**"。</span><span class="sxs-lookup"><span data-stu-id="4146f-112">Click **Enable users**.</span></span>

5.  <span data-ttu-id="4146f-113">在 " **新建 Lync Server 用户** " 对话框中，单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="4146f-113">On the **New Lync Server User** dialog, click **Add**.</span></span>

6.  <span data-ttu-id="4146f-114">在 " **搜索用户** " 框中，键入所需 Active Directory 用户帐户的全部或部分名称、显示名称、名字、姓氏、安全帐户管理器 (SAM) 帐户名称、电子邮件地址、用户主体名称 (UPN) 或电话号码，然后单击 " **查找**"。</span><span class="sxs-lookup"><span data-stu-id="4146f-114">In the **Search users** box, type all or the first portion of the name, display name, first name, last name, Security Accounts Manager (SAM) account name, email address, User Principal Name (UPN), or phone number of the Active Directory user account that you want, and then click **Find**.</span></span>

7.  <span data-ttu-id="4146f-115">在表中，选择要添加到 Lync Server 的帐户，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="4146f-115">In the table, select the account you want to add to Lync Server, and then click **OK**.</span></span>

8.  <span data-ttu-id="4146f-116">将用户分配到池，指定任何其他详细信息，并将策略分配给所需的用户，然后单击 " **启用**"。</span><span class="sxs-lookup"><span data-stu-id="4146f-116">Assign the user to a pool, specify any additional details, and assign the policies to the user you want, and then click **Enable**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4146f-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4146f-117">See Also</span></span>


[<span data-ttu-id="4146f-118">禁用或重新启用 Lync Server 2013 的用户帐户</span><span class="sxs-lookup"><span data-stu-id="4146f-118">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="4146f-119">从 Lync Server 2013 中删除用户帐户</span><span class="sxs-lookup"><span data-stu-id="4146f-119">Remove a user account from Lync Server 2013</span></span>](lync-server-2013-remove-a-user-account-from-lync-server.md)  


[<span data-ttu-id="4146f-120">启用和禁用 Lync Server 2013 的用户</span><span class="sxs-lookup"><span data-stu-id="4146f-120">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="4146f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4146f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

