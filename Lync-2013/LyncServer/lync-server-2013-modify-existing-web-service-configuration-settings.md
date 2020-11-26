---
title: Lync Server 2013：修改现有 Web 服务配置设置
description: Lync Server 2013：修改现有 Web 服务配置设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify existing Web Service configuration settings
ms:assetid: bd9c7aa5-d31c-4fab-b31d-8baae26b1296
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182580(v=OCS.15)
ms:contentKeyID: 48185272
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 455ddf60d171fe584115d646b16f63595285a906
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445755"
---
# <a name="modify-existing-web-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="aae55-103">在 Lync Server 2013 中修改现有的 Web 服务配置设置</span><span class="sxs-lookup"><span data-stu-id="aae55-103">Modify existing Web Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aae55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aae55-104">

<span> </span></span></span>

<span data-ttu-id="aae55-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="aae55-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="aae55-106">你可以使用 **Web 服务** 页面配置用于访问 Lync Server 2013 相关 web 服务器和 web 服务的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="aae55-106">You can use the **Web Service** page to configure the authentication methods for accessing Lync Server 2013 related web servers and Web Services.</span></span>

<span data-ttu-id="aae55-107">按照以下步骤修改现有的 Web 服务策略。</span><span class="sxs-lookup"><span data-stu-id="aae55-107">Follow these steps to modify an existing Web Service policy.</span></span>

<div>

## <a name="to-modify-existing-web-service-configuration-settings"></a><span data-ttu-id="aae55-108">修改现有的 Web 服务配置设置</span><span class="sxs-lookup"><span data-stu-id="aae55-108">To modify existing Web service configuration settings</span></span>

1.  <span data-ttu-id="aae55-109">从属于 RTCUniversalServerAdmins 组成员的用户帐户 (或具有等效的用户权限) 或分配给 CsServerAdministrator 或 CsAdministrator 角色，请登录到你部署 Lync Server 2013 的网络中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="aae55-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="aae55-110">打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。</span><span class="sxs-lookup"><span data-stu-id="aae55-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="aae55-111">有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="aae55-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="aae55-112">在左侧导航栏中，单击“安全性”，然后单击“Web 服务”。</span><span class="sxs-lookup"><span data-stu-id="aae55-112">In the left navigation bar, click **Security** and then click **Web Service**.</span></span>

4.  <span data-ttu-id="aae55-113">在“Web 服务”页上，单击某个配置，再单击“编辑”，然后单击“显示详细信息”。</span><span class="sxs-lookup"><span data-stu-id="aae55-113">On the **Web Service** page, click a configuration, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="aae55-114">在“编辑 Web 服务设置”的“集成 Windows 身份验证”中，选择“协商”、“集成 Windows 身份验证”或“无”。</span><span class="sxs-lookup"><span data-stu-id="aae55-114">In **Edit Web Service Setting**, in **Integrated Windows authentication**, select **Negotiate**, **Integrated Windows authentication**, or **None**.</span></span>

6.  <span data-ttu-id="aae55-115">根据环境中的客户端功能和支持情况，选择下列一项或多项：</span><span class="sxs-lookup"><span data-stu-id="aae55-115">Select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="aae55-116">**启用 PIN 身份验证**，允许使用 PIN 号对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="aae55-116">**Enable PIN Authentication** to enable clients to be authenticated using PIN numbers.</span></span>
    
      - <span data-ttu-id="aae55-117">**启用证书身份验证**，可使池中的服务器向客户端颁发证书。</span><span class="sxs-lookup"><span data-stu-id="aae55-117">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>
    
      - <span data-ttu-id="aae55-118">**启用证书链下载**，让具有身份验证证书的服务器下载该证书的证书链。</span><span class="sxs-lookup"><span data-stu-id="aae55-118">**Enable certificate chain download** to have servers presented with an authentication certificate download the certificate chain for that certificate.</span></span>

7.  <span data-ttu-id="aae55-119">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="aae55-119">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="aae55-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aae55-120">See Also</span></span>


[<span data-ttu-id="aae55-121">在 Lync Server 2013 "控制面板" 中配置身份验证</span><span class="sxs-lookup"><span data-stu-id="aae55-121">Configuring authentication in the Lync Server 2013 Control Panel</span></span>](lync-server-2013-configuring-authentication-in-the-lync-server-control-panel.md)  
  

<span data-ttu-id="aae55-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aae55-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

