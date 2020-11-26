---
title: 查看 Lync Server 2010 池中的当前用户
description: 查看 Lync Server 2010 池中的当前用户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View current users in Lync Server 2010 pool
ms:assetid: c0986800-8ee4-4d50-9e9c-39f7c4e67bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721870(v=OCS.15)
ms:contentKeyID: 49733804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55d328bf03c34db632f239bd9d3221ef942cd463
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438748"
---
# <a name="view-current-users-in-lync-server-2010-pool"></a><span data-ttu-id="af120-103">查看 Lync Server 2010 池中的当前用户</span><span class="sxs-lookup"><span data-stu-id="af120-103">View current users in Lync Server 2010 pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af120-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af120-104">

<span> </span></span></span>

<span data-ttu-id="af120-105">_**主题上次修改时间：** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="af120-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="af120-106">在了解你可以在池之间移动用户的各种方法之前，我们必须首先确定旧版 Lync Server 2010 池中存在哪些用户。</span><span class="sxs-lookup"><span data-stu-id="af120-106">Prior to learning the various ways you can move users between pools, we must first determine what users exist in the legacy Lync Server 2010 pool.</span></span> <span data-ttu-id="af120-107">在下面的图像中，"注册机构池" 列标识为旧版 Lync Server 2010 池配置的六个用户。</span><span class="sxs-lookup"><span data-stu-id="af120-107">In the image below, the Registrar pool column identifies six users who are configured for the legacy Lync Server 2010 pool.</span></span> <span data-ttu-id="af120-108">这些是我们将迁移到 Lync Server 2013 池的测试用户。</span><span class="sxs-lookup"><span data-stu-id="af120-108">These are the test users we will move to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="af120-109">**若要查看 Lync Server 2010 池中的用户列表**</span><span class="sxs-lookup"><span data-stu-id="af120-109">**To see the list of users in the Lync Server 2010 pool**</span></span>

1.  <span data-ttu-id="af120-110">使用属于 RTCUniversalServerAdmins 组成员的帐户或 CsAdministrator 或 CsUserAdministrator 管理角色的成员登录到 Lync Server 2010 前端服务器。</span><span class="sxs-lookup"><span data-stu-id="af120-110">Log on to the Lync Server 2010 Front End Server with an account that is a member of the RTCUniversalServerAdmins group or a member of the CsAdministrator or CsUserAdministrator administrative role.</span></span>

2.  <span data-ttu-id="af120-111">打开“Lync Server 控制面板”。</span><span class="sxs-lookup"><span data-stu-id="af120-111">Open **Lync Server Control Panel**.</span></span>

3.  <span data-ttu-id="af120-112">依次单击“用户”、“搜索”和“查找”。</span><span class="sxs-lookup"><span data-stu-id="af120-112">Click **Users**, click Search, and then click **Find**.</span></span>

<span data-ttu-id="af120-113">**Lync Server 15 "控制面板"**</span><span class="sxs-lookup"><span data-stu-id="af120-113">**The Lync Server 15 Control Panel**</span></span>

<span data-ttu-id="af120-114">![Lync Server 控制面板，"移动用户" 对话框](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server 控制面板，"移动用户" 对话框")</span><span class="sxs-lookup"><span data-stu-id="af120-114">![Lync Server Control Panel, Move User dialog](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server Control Panel, Move User dialog")</span></span>

<span data-ttu-id="af120-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af120-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

