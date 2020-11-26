---
title: Lync Server 2013：安装 Lync 会议室系统管理 Web 门户
description: Lync Server 2013：安装 Lync 会议室系统管理 Web 门户。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427003"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="375d1-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="375d1-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="375d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="375d1-104">

<span> </span></span></span>

<span data-ttu-id="375d1-105">_**主题上次修改时间：** 2015-04-09_</span><span class="sxs-lookup"><span data-stu-id="375d1-105">_**Topic Last Modified:** 2015-04-09_</span></span>

<span data-ttu-id="375d1-106">您可以从 Microsoft 下载中心下载 Microsoft Lync 会议室系统管理 Web 门户 [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) 。</span><span class="sxs-lookup"><span data-stu-id="375d1-106">You can download the Microsoft Lync Room System Administrative Web Portal from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044).</span></span>

<span data-ttu-id="375d1-107">若要安装 Lync 会议室系统管理 Web 门户，请使用以下步骤。</span><span class="sxs-lookup"><span data-stu-id="375d1-107">To install the Lync Room System Administrative Web Portal, use the following steps.</span></span>

1.  <span data-ttu-id="375d1-108">通过在 Lync Server 命令行管理程序中运行以下 cmdlet 来配置受信任的应用程序端口：</span><span class="sxs-lookup"><span data-stu-id="375d1-108">Configure the Trusted Application Port by running the following cmdlet in Lync Server Management Shell:</span></span>
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  <span data-ttu-id="375d1-109">若要安装会议室门户，请下载 **LyncRoomAdminPortal.exe** ，然后以管理员身份运行。</span><span class="sxs-lookup"><span data-stu-id="375d1-109">To install the Meeting Room Portal, download **LyncRoomAdminPortal.exe** and then run it as an administrator.</span></span>

3.  <span data-ttu-id="375d1-110">打开以下位置中的 Web.config 文件：</span><span class="sxs-lookup"><span data-stu-id="375d1-110">Open the Web.config file from the following location:</span></span>
    
    <span data-ttu-id="375d1-111">% 程序文件% \\ Microsoft Lync Server 2013 \\ Web Components 会议室 \\ 门户 \\ 程序 Int \\ 处理程序</span><span class="sxs-lookup"><span data-stu-id="375d1-111">%Program Files%\\Microsoft Lync Server 2013\\Web Components\\Meeting Room Portal\\Int\\Handler</span></span>\\

4.  <span data-ttu-id="375d1-112">在 Web.Config 文件中，将 PortalUserName 更改为在步骤2中创建的用户名，在 "配置 Lync 会议室系统管理员的先决条件" 部分中， (步骤中的推荐名称是 LRSApp) ：</span><span class="sxs-lookup"><span data-stu-id="375d1-112">In the Web.Config file, change the PortalUserName to the username created in Step 2 under the section “Configuring Prerequisites for Lync Room System Admin Portal” (the recommended name in the step is LRSApp):</span></span>
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  <span data-ttu-id="375d1-113">由于 LRS 管理门户是一个受信任的应用程序，因此无需在门户配置中提供密码。</span><span class="sxs-lookup"><span data-stu-id="375d1-113">Because the LRS Admin Portal is a trusted application, you do not need to provide the password in the portal configuration.</span></span> <span data-ttu-id="375d1-114">如果此用户使用的是非本地注册器，你需要通过在 Web.Config 文件中添加以下行来为其指定注册器：</span><span class="sxs-lookup"><span data-stu-id="375d1-114">If this user is using a different registrar than local registrar, you need to specify the registrar for it by adding the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  <span data-ttu-id="375d1-115">如果使用的端口不是 5061，则需要在 Web.Config 文件中添加以下行：</span><span class="sxs-lookup"><span data-stu-id="375d1-115">If the port used is other than 5061, add the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="375d1-116">验证 Lync 会议室系统管理 Web 门户的安装</span><span class="sxs-lookup"><span data-stu-id="375d1-116">Verifying Installation of the Lync Room System Administrative Web Portal</span></span>

<span data-ttu-id="375d1-117">若要验证 Lync 会议室系统管理 Web 门户的安装，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="375d1-117">To verify installation of the Lync Room System Administrative Web Portal, do the following:</span></span>


1.  <span data-ttu-id="375d1-118">在前端服务器上，浏览至以下 URL：</span><span class="sxs-lookup"><span data-stu-id="375d1-118">On a Front End server, browse to the following URL:</span></span>
    
    <span data-ttu-id="375d1-119"> https:// \<fe-server\> /lrs</span><span class="sxs-lookup"><span data-stu-id="375d1-119">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="375d1-120">你不应该看到任何错误，如下图所示：</span><span class="sxs-lookup"><span data-stu-id="375d1-120">You should not see any errors, as shown in the following image:</span></span>
    
    <span data-ttu-id="375d1-121">![Lync 聊天室系统管理门户登录屏幕](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync 聊天室系统管理门户登录屏幕")</span><span class="sxs-lookup"><span data-stu-id="375d1-121">![Lync Room System Admin Portal Sign In screen](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System Admin Portal Sign In screen")</span></span>

2.  <span data-ttu-id="375d1-122">如果你未看到任何错误，请尝试从拓扑中的任何其他计算机访问以下 URL：</span><span class="sxs-lookup"><span data-stu-id="375d1-122">If you do not see any errors, try accessing the following URL from any other computer in the topology:</span></span>
    
    <span data-ttu-id="375d1-123"> https:// \<fe-server\> /lrs</span><span class="sxs-lookup"><span data-stu-id="375d1-123">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="375d1-124">若要访问页面，你需要添加 DNS 记录，如 "自动客户登录所需的 DNS 记录" 中所述 [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) 。</span><span class="sxs-lookup"><span data-stu-id="375d1-124">To access the page, you will need to add the DNS records as described in “Required DNS Records for Automatic Client Sign-In” at [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056).</span></span>

<span data-ttu-id="375d1-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="375d1-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

