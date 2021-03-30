---
title: Lync Server 2013：设置 Lync 联盟
description: Lync Server 2013：设置 Lync 联合。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392372"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a>在 Lync Server 2013 中设置 Lync 联盟

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间** ：2014-03-27_

如果已部署 Edge 服务器，则直接添加联合方案功能。 如果尚未设置边缘服务器，必须先进行设置。 有关详细信息，请参阅部署文档中的规划文档和在[Lync Server 2013](lync-server-2013-deploying-external-user-access.md)中部署外部用户访问中的规划 Lync Server [2013](lync-server-2013-planning-for-external-user-access.md)中的外部用户访问。

<div>


> [!NOTE]  
> 如果您打算设置 XMPP 联合身份验证、Lync 联合身份验证或公共即时消息连接的任意组合，您可以同时部署它们，也可以一次部署一个。 如果您通过拓扑生成器和 Lync Server 命令行管理程序配置选项，然后在为一种、两种或所有三种联合身份验证类型配置选项后，在 Edge 服务器上运行部署向导，您可以减少所需的步骤数。



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>在拓扑生成器和部署向导中设置 Lync 联合身份验证

1.  在前端服务器上，打开"拓扑生成器"。 展开"边缘池"，然后右键单击 Edge 服务器或边缘服务器池。 选择"编辑属性"。

2.  在"常规"下的"编辑属性"中，选择"启用此 Edge 池 (端口 5061) 。 单击“确定”。

3.  单击"操作"，选择"拓扑"，然后选择"发布"。 当系统提示发布拓扑时，请单击"下一步"。 完成发布后，单击"完成"。

4.  在 Edge 服务器上，打开 Lync Server 部署向导。 单击"安装或更新 Lync Server System"，然后单击"设置或删除 Lync Server 组件"。 再次单击"运行"。

5.  在"设置 Lync Server 组件"中，单击"下一步"。 摘要屏幕将在执行操作时显示操作。 部署完成后，单击"查看日志"以查看可用的日志文件。 单击"完成"完成部署。
    
    <div>
    

    > [!IMPORTANT]  
    > 可以选择此选项，但只能将组织中一个 Edge 池或 Edge Server 发布到外部进行联合身份验证。 联合用户的所有访问（包括公共即时消息 (即时消息) 用户）通过同一边缘池或单个边缘服务器。 例如，如果部署包括一个 Edge 池或一个部署于纽约且一个部署于伦敦的边缘服务器，并且你启用对纽约 Edge 池或单个 Edge Server 的联合身份验证支持，则联合用户的信号流量将经过纽约 Edge 池或单个边缘服务器。 这同样适用于 London 用户的通信，尽管 London 内部用户呼叫 London 联盟用户时将使用 London 池或边缘服务器路由 A/V 流量。

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>配置与合作伙伴联合

1.  若要设置与另一个 Microsoft Lync Server 2013、Lync Server 2010、Office Communications Server 2007 R2 或 Office Communicator 2007 的成功联合，请从下表中选择联合类型，并定义 DNS SRV 记录、DNS 主机 (A 或 AAAA for IPv6) 并配置适用于联合身份验证类型的策略：
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>联合身份验证类型</th>
    <th>DNS 记录</th>
    <th>策略定义</th>
    <th>注释</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>发现的合作伙伴域</p></td>
    <td><p>配置格式为 _sipfederationtls._tcp 的 SRV 记录。 &lt;外部域名 &gt; 其中，SRV 记录的端口值为 TCP 5061，并且提供此服务的主机 <strong>定义为</strong> sip。 &lt;外部域名 &gt; – Access Edge 服务的 FQDN。 有关创建 SRV 记录的详细信息，请参阅 <a href="lync-server-2013-configure-dns-for-edge-support.md">在 Lync Server 2013</a> 中为边缘支持配置 DNS</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">在 Lync Server 2013 中启用或禁用联盟伙伴发现</a></p></li>
    </ul></td>
    <td><p>以前的版本称为开放增强联合身份验证的这种类型的 <strong>联合</strong>。 此类型的联合身份验证需要创建 SRV 记录，并且允许其他合作伙伴发现你的联合。</p></td>
    </tr>
    <tr class="even">
    <td><p>允许的合作伙伴域</p></td>
    <td><p>配置格式为 _sipfederationtls._tcp 的 SRV 记录。 &lt;外部域名 &gt; 其中，SRV 记录的端口值为 TCP 5061，并且提供此服务的主机 <strong>定义为</strong> sip。 &lt;外部域名 &gt; – Access Edge 服务的 FQDN。 有关创建 SRV 记录的详细信息，请参阅 <a href="lync-server-2013-configure-dns-for-edge-support.md">在 Lync Server 2013</a> 中为边缘支持配置 DNS</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></p></li>
    </ul></td>
    <td><p>以前的版本称为"增强联合身份验证"的此类 <strong>联合</strong>身份验证。 对于此类联合身份验证，SRV 记录的创建是可选的，允许其他合作伙伴发现联合。 当然，这是开放式增强 <strong>联合</strong>身份验证或 <strong>已发现的合作伙伴域</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>允许的合作伙伴服务器</p></td>
    <td><p>在策略中将 SIP 域名和合作伙伴 Edge Server FQDN 配置为联合合作伙伴</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">在 Lync Server 2013 中配置对允许的外部域的支持</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">在 Lync Server 2013 中配置对阻止的外部域的支持</a></p></li>
    </ul></td>
    <td><p>此联合类型是一对一关系的定义，不允许发现其他联合合作伙伴。 显式配置每个联合合作伙伴。 在以前的版本中，这称为直接 <strong>联合</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>托管提供商和公共 IM 提供程序</p></td>
    <td><p>未为此类型的联合身份验证定义特定的 DNS 要求</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">在 Lync Server 2013 中启用或禁用联盟和公共 IM 连接</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">在 Lync Server 2013 中创建或编辑公共 SIP 联盟提供程序</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">在 Lync Server 2013 中创建或编辑托管的 SIP 联盟提供程序</a></p></li>
    </ul></td>
    <td><p>此联合类型定义要为用户配置的服务和托管提供程序。 典型用途包括公共 IM 提供商（如 Windows Live Messenger、Yahoo！ 和 AOL，以及 Lync Online 和 Microsoft 365 等托管提供商</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>从 2012 年 9 月 1 日起，Microsoft Lync 公共 IM 连接用户订阅许可证 ("PIC USL") 不再可用于购买新协议或续订协议。 具有活动许可证的客户将能够继续与 Yahoo！ Messenger，直到服务关闭日期。 AOL 和 Yahoo！ 的结束日期为 2014 年 6 月 已宣布。 有关详细信息，请参阅 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">支持 Lync Server 2013 中的公共即时消息连接</A>。</P>
    > <LI>
    > <P>PIC USL 是 Lync Server 或 Office Communications Server 与 Yahoo！ 联合所需的按用户每月订阅许可证。 Messenger。 Microsoft 提供此服务的能力取决于 Yahoo！ 的支持，而 Yahoo！ 的基础协议正在逐渐减少。</P>
    > <LI>
    > <P>Lync 比以往任何时候都更加强大，是一种强大的工具，用于跨组织和与世界各地的个人进行连接。 与 Windows Live Messenger 联合身份验证不需要除 Lync 标准 CAL 之外的其他用户/设备许可证。 Skype 联合身份验证将添加到此列表，使 Lync 用户能够使用即时消息和语音联系数亿用户。</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  为 IPv6 记录和 DNS SRV (A 或 AAAA 定义和) DNS 主机

3.  使用 Lync Server 控制面板或 Lync Server 命令行管理程序以及相应的 cmdlet 定义和配置任何策略。 有关 Lync Server Management Shell cmdlet 的详细信息，请参阅[Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)中的联合和外部访问 cmdlet
    
    <div>
    

    > [!NOTE]  
    > Lync Room System (LRS) 未显示由联盟 Lync 合作伙伴中的组织者发送的会议的"加入"按钮。 若要在 LRS 上显示会议加入链接，发送组织必须使用以下 cmdlet 启用 TNEF：<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>请注意，这不特定于 LRS。 在这种情况下，Outlook 和 Lync 不会显示"加入"链接，因为不会传输 MAPI 属性，但在 Outlook 中，用户可以打开会议邀请并单击会议 URL。 当 TNEFEnabled 设置为 true Exchange 2013 时，不会删除 MAPI 属性（包括 OnlineMeetingExternalLink）并且提醒上会显示"联接"按钮。

    
    </div>

</div>

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中规划 SIP、XMPP 联合和公共即时消息](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[管理对 Lync Server 2013 的联盟和外部访问](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

