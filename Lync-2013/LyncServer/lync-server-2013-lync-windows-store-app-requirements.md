---
title: Lync Server 2013： Lync Windows 应用商店应用要求
description: Lync Server 2013： Lync Windows 应用商店应用要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Windows Store app requirements
ms:assetid: 5f2e0a40-8450-4f61-b6f6-913fc1906020
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ823129(v=OCS.15)
ms:contentKeyID: 50120200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17e8705a55625bcf0ad099ead1000a82c994d867
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426163"
---
# <a name="lync-windows-store-app-requirements-for-lync-server-2013"></a>Lync Server 2013 的 lync Windows 应用商店应用要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-12-03_

具有 Lync Server 的本地部署的组织必须满足以下要求才能支持 Lync Windows 应用商店应用。

<div>


> [!NOTE]  
> 对于 Lync Server 2010，请运行 Lync Server 2010 的累积更新： <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2670352"> https://go.microsoft.com/fwlink/?linkid=3052&amp kbid = 2670352</A>) 或更高版本，请参阅所有服务器上的 "2 月 (2012"。 若要使用户能够加入会议，请运行 Lync Server 2010 的累积更新：年10月 2012 (在服务器上提供<A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2737915"> https://go.microsoft.com/fwlink/?linkid=3052&amp ; kbid = 2737915</A>) 。



</div>

  - 在服务器上启用自动发现、Lync Web App 和 Web 票证服务。

  - 在前端服务器或前端池上启用证书身份验证。  (前端服务器或前端池中的用户注册过程通常称为注册机构。 ) 有关详细信息，请参阅 [在 Lync Server 2013 中创建注册机构配置设置](lync-server-2013-create-registrar-configuration-settings.md)。

  - 为自动发现服务 (CNAME) 资源记录发布 DNS 别名。

  - 不再需要确保证书吊销列表 (CRL) 分发点 (CDP) 颁发给 Lync 服务器的证书指向的是 HTTP 资源，而不是 LDAP 资源。 但是，请确保客户端计算机安装了最新的 Windows 更新。

  - 配置企业中的 HTTP 代理以允许 Lync server 相关的 HTTP 流量。  为自动发现、Lync Web App 和 WebTicket 服务添加例外（如有必要）。

  - 在客户端上，安装 Windows 8.1 和最新版本的 Lync Windows 应用商店应用以修复通常在使用多个域时出现的登录问题 (例如，当 SIP URI **userA@domainZ.com** ，而 Edge 服务器 **sip.domainX.com**) 。

如果你的组织订阅了 Lync Online 或 Microsoft 365，并且你使用的是你自己的域名，则必须执行一些额外的步骤来设置你的网络以自动发现 Lync 服务器。 在移动设备上，Lync Windows 应用商店应用和 Lync 的网络配置要求相同。

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中部署 Lync Windows 应用商店应用](lync-server-2013-deploying-lync-windows-store-app.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>
