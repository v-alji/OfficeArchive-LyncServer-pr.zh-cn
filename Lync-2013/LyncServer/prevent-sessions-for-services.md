---
title: 阻止服务的会话
description: 阻止服务的会话。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 4b541c72-cdc1-4f86-a5a8-c43c24f41d8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688049(v=OCS.15)
ms:contentKeyID: 49733642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a452f8091716daa0a15967e2a278e82c5bc8c4f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438461"
---
# <a name="prevent-sessions-for-services"></a><span data-ttu-id="0bcca-103">阻止服务的会话</span><span class="sxs-lookup"><span data-stu-id="0bcca-103">Prevent sessions for services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0bcca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0bcca-104">

<span> </span></span></span>

<span data-ttu-id="0bcca-105">_**主题上次修改时间：** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="0bcca-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="0bcca-106">你可以使用 Microsoft Lync Server 2010 控制面板阻止在特定计算机上运行的所有 Lync Server 2010 服务的新会话或阻止特定 Lync Server 2010 服务的新会话。</span><span class="sxs-lookup"><span data-stu-id="0bcca-106">You can use Microsoft Lync Server 2010 Control Panel to prevent new sessions for all the Lync Server 2010 services running on a specific computer or to prevent new sessions for a specific Lync Server 2010 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="0bcca-107">阻止计算机上所有 Lync Server 服务的新会话</span><span class="sxs-lookup"><span data-stu-id="0bcca-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="0bcca-108">从属于 RTCUniversalServerAdmins 组成员的用户帐户 (或具有等效的用户权限) 或分配给 CsServerAdministrator 或 CsAdministrator 角色，请登录到你部署 Lync Server 2013 的网络中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="0bcca-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="0bcca-109">打开“Lync Server 控制面板”。</span><span class="sxs-lookup"><span data-stu-id="0bcca-109">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="0bcca-110">在左侧导航栏中，单击 " **拓扑** "，然后单击 " **状态**"。</span><span class="sxs-lookup"><span data-stu-id="0bcca-110">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="0bcca-111">在 " **状态** " 页面上，根据需要对列表进行排序或搜索以查找运行要阻止新会话的服务的计算机，然后单击该计算机。</span><span class="sxs-lookup"><span data-stu-id="0bcca-111">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="0bcca-112">单击 " **操作**"。</span><span class="sxs-lookup"><span data-stu-id="0bcca-112">Click **Action**.</span></span>

6.  <span data-ttu-id="0bcca-113">单击 " **阻止所有服务的新会话**"。</span><span class="sxs-lookup"><span data-stu-id="0bcca-113">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="0bcca-114">阻止特定服务的新会话</span><span class="sxs-lookup"><span data-stu-id="0bcca-114">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="0bcca-115">从属于 RTCUniversalServerAdmins 组成员的用户帐户 (或具有等效的用户权限) 或分配给 CsServerAdministrator 或 CsAdministrator 角色，请登录到你部署 Lync Server 2013 的网络中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="0bcca-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="0bcca-116">打开“Lync Server 控制面板”。</span><span class="sxs-lookup"><span data-stu-id="0bcca-116">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="0bcca-117">在左侧导航栏中，单击 " **拓扑** "，然后单击 " **状态**"。</span><span class="sxs-lookup"><span data-stu-id="0bcca-117">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="0bcca-118">在 " **状态** " 页面上，根据需要对列表进行排序或搜索以查找运行要启动或停止的服务的计算机，然后单击它。</span><span class="sxs-lookup"><span data-stu-id="0bcca-118">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="0bcca-119">单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="0bcca-119">Click **Properties**.</span></span>

6.  <span data-ttu-id="0bcca-120">对服务列表进行排序（如有必要），然后单击要阻止新会话的服务。</span><span class="sxs-lookup"><span data-stu-id="0bcca-120">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="0bcca-121">单击 " **操作**"。</span><span class="sxs-lookup"><span data-stu-id="0bcca-121">Click **Action**.</span></span>

8.  <span data-ttu-id="0bcca-122">单击 " **阻止新的服务会话**"。</span><span class="sxs-lookup"><span data-stu-id="0bcca-122">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="0bcca-123">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="0bcca-123">Click **Close**.</span></span>

<span data-ttu-id="0bcca-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0bcca-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

