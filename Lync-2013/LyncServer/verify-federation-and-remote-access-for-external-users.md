---
title: 验证联盟和外部用户的远程访问
description: 验证外部用户的联盟和远程访问。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify federation and remote access for external users
ms:assetid: a383fefb-c428-4462-93fd-15ba540fa867
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688163(v=OCS.15)
ms:contentKeyID: 49733768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ac36f2e1b6c5ddfd889810ba2a3ab4d82b7ae33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446470"
---
# <a name="verify-federation-and-remote-access-for-external-users"></a><span data-ttu-id="b26b7-103">验证联盟和外部用户的远程访问</span><span class="sxs-lookup"><span data-stu-id="b26b7-103">Verify federation and remote access for external users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b26b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b26b7-104">

<span> </span></span></span>

<span data-ttu-id="b26b7-105">_**主题上次修改时间：** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="b26b7-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="b26b7-106">将联盟路由转换为 Lync Server 2013 Edge 服务器之后，你应该执行一些功能测试以验证联合身份验证是否按预期执行。</span><span class="sxs-lookup"><span data-stu-id="b26b7-106">After transitioning the federation route to the Lync Server 2013 Edge Server, you should perform some functional tests to verify that federation performs as expected.</span></span> <span data-ttu-id="b26b7-107">外部用户访问的测试应包括您的组织支持的每种类型的外部用户，包括以下任何或所有类型的外部用户。</span><span class="sxs-lookup"><span data-stu-id="b26b7-107">Tests for external user access should include each type of external user that your organization supports, including any or all of the following.</span></span>

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a><span data-ttu-id="b26b7-108">测试外部用户和外部访问的连接性</span><span class="sxs-lookup"><span data-stu-id="b26b7-108">Test Connectivity of External Users and External access</span></span>

  - <span data-ttu-id="b26b7-109">至少一个联盟域中的用户、Lync Server 2013 上的内部用户以及 Lync Server 2010 上的用户。</span><span class="sxs-lookup"><span data-stu-id="b26b7-109">Users from at least one federated domain, an internal user on Lync Server 2013, and a user on Lync Server 2010.</span></span> <span data-ttu-id="b26b7-110">测试即时消息 (IM) 、状态、音频/视频 (A/V) 和桌面共享。</span><span class="sxs-lookup"><span data-stu-id="b26b7-110">Test instant messaging (IM), presence, audio/video (A/V), and desktop sharing.</span></span>

  - <span data-ttu-id="b26b7-111">您的组织支持 (和已完成的设置的每个公共 IM 服务提供商的用户) 与 Lync Server 2013 上的用户通信以及 Lync Server 2010 上的用户。</span><span class="sxs-lookup"><span data-stu-id="b26b7-111">Users of each public IM service provider that your organization supports (and for which provisioning has been completed) communicating with a user on Lync Server 2013 and a user on Lync Server 2010.</span></span>

  - <span data-ttu-id="b26b7-112">验证匿名用户是否能够加入会议。</span><span class="sxs-lookup"><span data-stu-id="b26b7-112">Verify that anonymous users are able to join conferences.</span></span>

  - <span data-ttu-id="b26b7-113">在 Lync Server 2010 上托管的用户使用远程用户访问 (从 intranet 外部登录 Lync Server 2010，但没有与 Lync server 2013 上的用户以及 Lync Server 2010 上的用户进行 VPN) 。</span><span class="sxs-lookup"><span data-stu-id="b26b7-113">A user hosted on Lync Server 2010 using remote user access (logging into Lync Server 2010 from outside the intranet but without VPN) with a user on Lync Server 2013, and a user on Lync Server 2010.</span></span> <span data-ttu-id="b26b7-114">测试即时消息、状态、A/V 和桌面共享。</span><span class="sxs-lookup"><span data-stu-id="b26b7-114">Test IM, presence, A/V, and desktop sharing.</span></span>

  - <span data-ttu-id="b26b7-115">在 Lync Server 2013 上托管的用户使用远程用户访问 (从 intranet 外部登录 Lync Server 2013，但没有与 Lync server 2013 上的用户以及 Lync Server 2010 上的用户进行 VPN) 。</span><span class="sxs-lookup"><span data-stu-id="b26b7-115">A user hosted on Lync Server 2013 using remote user access (logging into Lync Server 2013 from outside the intranet but without VPN) with a user on Lync Server 2013, and a user on Lync Server 2010.</span></span> <span data-ttu-id="b26b7-116">测试即时消息、状态、A/V 和桌面共享。</span><span class="sxs-lookup"><span data-stu-id="b26b7-116">Test IM, presence, A/V, and desktop sharing.</span></span>

<span data-ttu-id="b26b7-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b26b7-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

