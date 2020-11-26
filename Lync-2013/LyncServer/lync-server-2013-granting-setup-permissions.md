---
title: Lync Server 2013：授予安装权限
description: Lync Server 2013：授予设置权限。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting setup permissions
ms:assetid: 15982bfe-6844-44f6-815a-72dcaf0e4d21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398225(v=OCS.15)
ms:contentKeyID: 48183491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5523494219d07907caeefc1bd139c41856effa54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427894"
---
# <a name="granting-setup-permissions-in-lync-server-2013"></a><span data-ttu-id="22097-103">在 Lync Server 2013 中授予安装权限</span><span class="sxs-lookup"><span data-stu-id="22097-103">Granting setup permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22097-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22097-104">

<span> </span></span></span>

<span data-ttu-id="22097-105">_**主题上次修改时间：** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="22097-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="22097-106">你可以使用 **CsSetupPermission** cmdlet 向指定的 Active Directory 组织 (单位) 的 RTCUniversalServerAdmins 组添加读取、写入、ReadSPN 和 WriteSPN 权限。</span><span class="sxs-lookup"><span data-stu-id="22097-106">You can use the **Grant-CsSetupPermission** cmdlet to add Read, Write, ReadSPN, and WriteSPN permissions to the RTCUniversalServerAdmins group for a specified Active Directory organizational unit (OU).</span></span> <span data-ttu-id="22097-107">然后，该 OU 中的 RTCUniversalServerAdmins 组的成员可以在指定域中安装运行 Lync Server 2013 的服务器，而不是域管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="22097-107">Then members of the RTCUniversalServerAdmins group in that OU can install servers running Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="22097-108">使用 **CsSetupPermission** cmdlet 验证你通过使用 **CsSetupPermission** cmdlet 设置的权限。</span><span class="sxs-lookup"><span data-stu-id="22097-108">Use the **Test-CsSetupPermission** cmdlet to verify the permissions you set up by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<span data-ttu-id="22097-109">你可以使用 **CsSetupPermission** cmdlet 删除你使用 **CsSetupPermission** cmdlet 授予的权限。</span><span class="sxs-lookup"><span data-stu-id="22097-109">You can use the **Revoke-CsSetupPermission** cmdlet to remove permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-setup-permissions"></a><span data-ttu-id="22097-110">授予设置权限</span><span class="sxs-lookup"><span data-stu-id="22097-110">To grant setup permissions</span></span>

1.  <span data-ttu-id="22097-111">在要授予设置权限的域中登录到运行 Lync Server 2013 的计算机。</span><span class="sxs-lookup"><span data-stu-id="22097-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant setup permissions.</span></span> <span data-ttu-id="22097-112">如果 OU 位于不同的子域中，请使用作为域管理员组成员或企业管理员组成员的帐户。</span><span class="sxs-lookup"><span data-stu-id="22097-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="22097-113">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="22097-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="22097-114">运行：</span><span class="sxs-lookup"><span data-stu-id="22097-114">Run:</span></span>
    
        Grant-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="22097-115">你可以将 ComputerOu 参数指定为相对于指定域的默认命名上下文 (例如，CN = 计算机) 。</span><span class="sxs-lookup"><span data-stu-id="22097-115">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="22097-116">或者，你可以将此参数指定为 (DN) 的完整 OU 可分辨名称 (例如 "CN = 计算机，DC = Contoso，DC = com" ) 。</span><span class="sxs-lookup"><span data-stu-id="22097-116">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="22097-117">在后一种情况下，你必须指定与你指定的域一致的 OU DN。</span><span class="sxs-lookup"><span data-stu-id="22097-117">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="22097-118">如果不指定 Domain 参数，则默认值为本地域。</span><span class="sxs-lookup"><span data-stu-id="22097-118">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-setup-permissions"></a><span data-ttu-id="22097-119">验证设置权限</span><span class="sxs-lookup"><span data-stu-id="22097-119">To verify setup permissions</span></span>

1.  <span data-ttu-id="22097-120">在要验证使用 **CsSetupPermission** cmdlet 授予的设置权限的域中，登录到运行 Lync Server 2013 的计算机。</span><span class="sxs-lookup"><span data-stu-id="22097-120">Log on to a computer running Lync Server 2013 in the domain where you want to verify setup permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="22097-121">如果 OU 位于不同的子域中，请使用作为域管理员组成员或企业管理员组成员的帐户。</span><span class="sxs-lookup"><span data-stu-id="22097-121">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="22097-122">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="22097-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="22097-123">运行：</span><span class="sxs-lookup"><span data-stu-id="22097-123">Run:</span></span>
    
        Test-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="22097-124">你可以将 ComputerOu 参数指定为相对于指定域的默认命名上下文 (例如，CN = 计算机) 。</span><span class="sxs-lookup"><span data-stu-id="22097-124">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="22097-125">或者，你可以将此参数指定为 (DN) 的完整 OU 可分辨名称 (例如 "CN = 计算机，DC = Contoso，DC = com" ) 。</span><span class="sxs-lookup"><span data-stu-id="22097-125">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="22097-126">在后一种情况下，你必须指定与你指定的域一致的 OU DN。</span><span class="sxs-lookup"><span data-stu-id="22097-126">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="22097-127">如果不指定 Domain 参数，则默认值为本地域。</span><span class="sxs-lookup"><span data-stu-id="22097-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-setup-permissions"></a><span data-ttu-id="22097-128">撤销设置权限</span><span class="sxs-lookup"><span data-stu-id="22097-128">To revoke setup permissions</span></span>

1.  <span data-ttu-id="22097-129">在要吊销 **CsSetupPermission** cmdlet 授予的设置权限的域中，登录到运行 Lync Server 2013 的计算机。</span><span class="sxs-lookup"><span data-stu-id="22097-129">Log on to a computer running Lync Server 2013 in the domain where you want to revoke setup permissions that were granted by the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="22097-130">如果 OU 位于不同的子域中，请使用作为域管理员组成员或企业管理员组成员的帐户。</span><span class="sxs-lookup"><span data-stu-id="22097-130">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="22097-131">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="22097-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="22097-132">运行：</span><span class="sxs-lookup"><span data-stu-id="22097-132">Run:</span></span>
    
        Revoke-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="22097-133">你可以将 ComputerOu 参数指定为相对于指定域的默认命名上下文 (例如，CN = 计算机) 。</span><span class="sxs-lookup"><span data-stu-id="22097-133">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="22097-134">或者，你可以将此参数指定为 (DN) 的完整 OU 可分辨名称 (例如 "CN = 计算机，DC = Contoso，DC = com" ) 。</span><span class="sxs-lookup"><span data-stu-id="22097-134">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="22097-135">在后一种情况下，你必须指定与你指定的域一致的 OU DN。</span><span class="sxs-lookup"><span data-stu-id="22097-135">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="22097-136">如果不指定 Domain 参数，则默认值为本地域。</span><span class="sxs-lookup"><span data-stu-id="22097-136">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="22097-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22097-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

