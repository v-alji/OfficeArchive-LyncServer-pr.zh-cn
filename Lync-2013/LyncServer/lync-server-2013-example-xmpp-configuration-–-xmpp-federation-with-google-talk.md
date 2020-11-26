---
title: 示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟
description: 示例 XMPP 配置-XMPP 联盟与 Google 通话。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428447"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a>Lync Server 2013 中的示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-04-22_

部署 XMPP 代理的示例配置定义了与 Google 通话的联盟。

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a>示例 XMPP 配置 –  与 Google Talk 的 XMPP 联盟

1.  在前端服务器上，打开 "Lync Server 部署向导"。 单击 " **安装** 或 **更新 lync 服务器系统**"，然后单击 " **设置** " 或 " **删除 lync server 组件**"。 再次单击 " **运行**"。

2.  在 " **安装 Lync 服务器组件**" 中，单击 " **下一步**"。 "摘要" 屏幕将显示执行时的操作。 部署完成后，单击 " **查看日志** " 以查看可用的日志文件。 单击 " **完成** " 以完成部署。

3.  在边缘服务器上，打开 "Lync Server 部署向导"。 单击 " **安装** 或 **更新 lync 服务器系统**"，然后单击 " **设置** " 或 " **删除 lync server 组件**"。 再次单击 " **运行**"。

4.  将 Google 通话添加为 XMPP 允许合作伙伴。 Google 谈话目前仅支持服务器到服务器 XMPP 联合身份验证的 TCP 连接，并且仅支持服务器回拨以进行身份验证。  (参阅 <http://xmpp.org/extensions/xep-0220.html>) 。
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  若要启用边缘联盟，请键入以下内容：
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  在 " **安装 Lync 服务器组件**" 中，单击 " **下一步**"。 "摘要" 屏幕将显示执行时的操作。 部署完成后，单击 " **查看日志** " 以查看可用的日志文件。 单击 " **完成** " 以完成部署。

7.  在边缘服务器上的 "Lync Server 部署向导" 中，在 " **步骤3：请求、安装或分配证书**" 旁边，再次单击 " **运行**"。
    
    <div>
    

    > [!TIP]
    > 如果你是首次部署 Edge 服务器，你将看到 "运行"，而不是再次运行。

    
    </div>

8.  在“**可用的证书任务**”页上，单击“**创建新的证书请求**”。

9.  在 " **证书请求** " 页面上，单击 " **外部边缘证书**"。

10. 在 " **延迟或立即请求** " 页面上，选中 " **立即准备请求，但稍后发送"** 复选框。

11. 在 " **证书请求文件** " 页面上，键入请求要保存到的文件的完整路径和文件名 (例如，c： \\ cert \_ 外部 \_ edge) 。

12. 在 " **指定备用证书模板** " 页面上，若要使用默认 web 台模板之外的模板，请选中 " **为所选证书颁发机构使用备用证书模板** " 复选框。

13. 在 " **名称和安全设置** " 页面上，执行下列操作：
    
    1.  在 " **友好名称**" 中，键入证书的显示名称
    
    2.  在 " **位长度**" 中，指定位长度 (通常是 **2048** 的默认值) 
    
    3.  验证已选中 "将 **证书私钥标记为可导出** " 复选框

14. 在 " **组织信息** " 页面上，键入组织和组织单位的名称 (例如，部门或部门) 

15. 在 " **地理信息** " 页面上，指定位置信息

16. 在 " **主题名称/主题备用名称** " 页面上，将显示要由向导自动填充的信息。 如果需要其他主题备用名称，请在接下来的两个步骤中进行指定

17. 在 " **使用者备用名称 (SANs)** " 页面上的 "SIP 域设置" 中，选中 "域" 复选框以添加 SIP。 \<sipdomain\> 输入到 "主题备用名称" 列表。

18. 在 " **配置其他主题备用名称** " 页面上，指定所需的任何其他主题备用名称。
    
    <div>
    

    > [!TIP]
    > 如果 XMPP 代理已安装，则默认情况下会在 SAN 条目中填充域名 (如 contoso.com) 。 如果需要更多条目，请在此步骤中添加这些条目。

    
    </div>

19. 在 " **请求摘要** " 页面上，查看要用于生成请求的证书信息。

20. 命令完成运行后，您可以 **查看日志**，或单击 " **下一步** " 继续。

21. 在 "**证书请求文件**" 页面上，您可以通过单击 "查看或退出证书向导"，**通过单击 "****查看**" 或 "退出证书向导" 来查看生成的证书签名请求 (CSR) 文件

22. 将请求文件复制并提交到公共证书颁发机构。

23. 接收、导入和分配公共证书后，必须停止并重新启动 Edge 服务器服务。 启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft lync server 2013**"，然后单击 " **Lync server 命令行管理** 程序"。 在 Lync Server 命令行管理器中，键入：
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. 若要为 XMPP 联盟配置 DNS，请将以下 SRV 记录添加到外部 DNS： \_ XMPP-server。 \_tcp-out.\<domain name\> SRV 记录将解析为 Edge 服务器的访问边缘 FQDN，其端口值为5269

25. 通过在前端服务器上打开 Lync Server 管理外壳并键入以下内容来配置新的外部访问策略以启用所有用户：
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

</div>

</div>

<span> </span>

</div>

</div>

</div>

