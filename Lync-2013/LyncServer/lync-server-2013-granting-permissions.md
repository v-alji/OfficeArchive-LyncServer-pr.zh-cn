---
title: Lync Server 2013：授予权限
description: Lync Server 2013：授予权限。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting permissions
ms:assetid: d1c9ea66-bd07-480e-99a0-011108f97e42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398901(v=OCS.15)
ms:contentKeyID: 48185446
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4bdb2b1ef39b85caa89c7597f455e6e4fc08e44e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392346"
---
# <a name="granting-permissions-in-lync-server-2013"></a><span data-ttu-id="216de-103">在 Lync Server 2013 中授予权限</span><span class="sxs-lookup"><span data-stu-id="216de-103">Granting permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="216de-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="216de-104">

<span> </span></span></span>

<span data-ttu-id="216de-105">_**主题上次修改时间：** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="216de-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="216de-106">对于设置，你可以为特定 Active Directory 组织 (单位的 RTCUniversalServerAdmins 通用组授予权限) ，从而允许该 OU 中的 RTCUniversalServerAdmins 组成员在指定域中安装 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="216de-106">For setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain.</span></span> <span data-ttu-id="216de-107">为 OU 授予权限时，授予以下权限：</span><span class="sxs-lookup"><span data-stu-id="216de-107">When you grant permissions for an OU, the following permissions are granted:</span></span>

  - <span data-ttu-id="216de-108">继续</span><span class="sxs-lookup"><span data-stu-id="216de-108">Read</span></span>

  - <span data-ttu-id="216de-109">记录</span><span class="sxs-lookup"><span data-stu-id="216de-109">Write</span></span>

  - <span data-ttu-id="216de-110">ReadSPN</span><span class="sxs-lookup"><span data-stu-id="216de-110">ReadSPN</span></span>

  - <span data-ttu-id="216de-111">WriteSPN</span><span class="sxs-lookup"><span data-stu-id="216de-111">WriteSPN</span></span>

<span data-ttu-id="216de-112">对于 "管理"，你可以向指定的 Ou 添加权限，以便林准备创建的 RTC 通用组的成员可以访问 Ou，而无需成为域管理员组的成员。</span><span class="sxs-lookup"><span data-stu-id="216de-112">For administration, you can add permissions to specified OUs so that members of the RTC universal groups created by forest preparation can access the OUs without needing to be members of the Domain Admins group.</span></span> <span data-ttu-id="216de-113">添加到指定 OU 的权限与 **Enable CsAdDomain** cmdlet 添加到计算机和用户 OU 容器的权限相同。</span><span class="sxs-lookup"><span data-stu-id="216de-113">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users OU containers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="216de-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="216de-114">In This Section</span></span>

  - [<span data-ttu-id="216de-115">在 Lync Server 2013 中授予安装权限</span><span class="sxs-lookup"><span data-stu-id="216de-115">Granting setup permissions in Lync Server 2013</span></span>](lync-server-2013-granting-setup-permissions.md)

  - [<span data-ttu-id="216de-116">在 Lync Server 2013 中授予组织单位权限</span><span class="sxs-lookup"><span data-stu-id="216de-116">Granting organizational unit permissions in Lync Server 2013</span></span>](lync-server-2013-granting-organizational-unit-permissions.md)

<span data-ttu-id="216de-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="216de-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

