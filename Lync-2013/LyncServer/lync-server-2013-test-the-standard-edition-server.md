---
title: Lync Server 2013：测试 Standard Edition 服务器
description: Lync Server 2013：测试标准版服务器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the Standard Edition server
ms:assetid: b6ef67bb-9665-43e4-b8b3-eac8898eebf6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412890(v=OCS.15)
ms:contentKeyID: 48185220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 35dc13fc01979cc8b293d0647a7886b7d65d7669
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441177"
---
# <a name="test-the-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="18e08-103">在 Lync Server 2013 中测试 Standard Edition 服务器</span><span class="sxs-lookup"><span data-stu-id="18e08-103">Test the Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18e08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18e08-104">

<span> </span></span></span>

<span data-ttu-id="18e08-105">_**主题上次修改时间：** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="18e08-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="18e08-106">以下过程介绍了如何测试标准版服务器的部署。</span><span class="sxs-lookup"><span data-stu-id="18e08-106">The following procedure describes how to test the deployment of a Standard Edition server.</span></span>

<div>

## <a name="to-test-the-deployment-of-a-standard-edition-server"></a><span data-ttu-id="18e08-107">测试标准版服务器的部署</span><span class="sxs-lookup"><span data-stu-id="18e08-107">To test the deployment of a Standard Edition Server</span></span>

1.  <span data-ttu-id="18e08-108">使用 Active Directory 计算机和用户为 Lync server 2013 部署 (的管理员角色添加 Active Directory 用户对象) 将 Lync Server 控制面板安装到 " **CSAdministrator** " 组中。</span><span class="sxs-lookup"><span data-stu-id="18e08-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server Control Panel is installed) to the **CSAdministrator** group.</span></span>

2.  <span data-ttu-id="18e08-109">如果用户对象当前已登录，则注销后重新登录，以注册新的组分配。</span><span class="sxs-lookup"><span data-stu-id="18e08-109">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="18e08-110">用户帐户不能是运行 Lync Server 2013 标准版的服务器的本地管理员。</span><span class="sxs-lookup"><span data-stu-id="18e08-110">The user account cannot be the local administrator of the server running Lync Server 2013, Standard Edition.</span></span> <span data-ttu-id="18e08-111">如果不将相应的用户和组添加到 CsAdministors 组，则在打开 Lync Server 2013 控制面板时将收到错误，其中指出 "未经授权：由于基于角色的访问控制 (RBAC) 授权失败" 的访问被拒绝。 "</span><span class="sxs-lookup"><span data-stu-id="18e08-111">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server 2013 Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

3.  <span data-ttu-id="18e08-112">使用 "管理" 帐户登录到安装了 "Lync Server 控制面板" 的计算机。</span><span class="sxs-lookup"><span data-stu-id="18e08-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="18e08-113">如果出现提示，请启动 Lync Server 控制面板并提供凭据。</span><span class="sxs-lookup"><span data-stu-id="18e08-113">Start Lync Server Control Panel and provide credentials, if prompted.</span></span> <span data-ttu-id="18e08-114">Lync Server 2013 "控制面板" 显示部署信息。</span><span class="sxs-lookup"><span data-stu-id="18e08-114">Lync Server 2013 Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="18e08-115">在左侧导航栏中，单击 " **拓扑**"，然后确认服务状态是带有绿色箭头的计算机图标，并且已部署并联机的每个 Lync server 服务器角色旁边都有一个绿色复选标记。</span><span class="sxs-lookup"><span data-stu-id="18e08-115">In the left navigation bar, click **Topology**, and then confirm that the service status is a computer icon with a green arrow and there is a green check mark next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="18e08-116">在左侧导航栏中，单击 " **用户**"，然后启用 "Lync Server 2013 的两个用户"。</span><span class="sxs-lookup"><span data-stu-id="18e08-116">In the left navigation bar, click **Users**, and then enable the two users for Lync Server 2013.</span></span>

7.  <span data-ttu-id="18e08-117">将一位用户登录到加入域的计算机，另一用户登录到域中的另一台计算机。</span><span class="sxs-lookup"><span data-stu-id="18e08-117">Log one user on to a computer that is joined to the domain, and the other user on to another computer in the domain.</span></span>

8.  <span data-ttu-id="18e08-118">在两台客户端计算机上安装 Lync Server 2013，然后验证这两个用户都可以登录 Lync Server 2013，并且可以互相发送即时消息。</span><span class="sxs-lookup"><span data-stu-id="18e08-118">Install Lync Server 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="18e08-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18e08-119">See Also</span></span>


[<span data-ttu-id="18e08-120">在 Lync Server 2013 中部署客户端和设备</span><span class="sxs-lookup"><span data-stu-id="18e08-120">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="18e08-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18e08-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

