---
title: Lync Server 2013：规划混合部署
description: Lync Server 2013：规划混合部署。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424546"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a>规划 Lync Server 2013 混合部署

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间** ：2016-05-25_

规划混合部署时，应考虑用户和网络基础结构的以下要求。

<div>

## <a name="infrastructure-requirements"></a>基础结构要求

必须在环境中配置以下各项，才能实现和部署混合部署。

  - 启用了 Skype for Business Online 的 Microsoft 365 或 Office 365 组织。 请注意，只能将单个租户用于本地部署的混合配置。

  - 在受支持的拓扑中 (Skype for Business Server) Lync Server 的单个本地部署。 请参阅拓扑要求。
    
    有关为混合配置 Lync Server 2013 或 Lync Server 2010 部署的信息，请参阅 [配置 Lync Server 2013 混合部署](lync-server-2013-configuring-hybrid-deployments.md)。

  - Skype for Business Server 2015 管理工具。 如果您使用的是 Lync Server 2013 或 Lync Server 2010，您可以使用 Lync Server 2013 管理工具。

  - 若要支持 Microsoft 365 或 Office 365 的单一登录，以便用户可以使用与本地相同的登录凭据登录 Office，可以使用 Azure Active Directory (AAD) Connect 的密码同步功能。 还可使用 Active Directory 联合身份验证服务 (AD FS) Microsoft 365 或 Office 365 进行单一登录。
    
    有关详细信息，请参阅 [将本地标识与 Azure Active Directory 集成](https://go.microsoft.com/fwlink/p/?linkid=619754)。

  - 单个目录同步解决方案，使本地和联机 Active Directory 对象保持同步。 有关目录同步的详细信息，请参阅 [目录集成工具](https://go.microsoft.com/fwlink/p/?linkid=530320)。

</div>

<div>

## <a name="lync-client-support"></a>Lync 客户端支持

Lync 客户端支持的功能以及本地和联机环境中提供的功能存在一些差异。 在决定希望将用户归到组织中何处之前，您可以查看 Lync Server 的各种配置的客户端支持。 Lync 混合部署中的 Skype for Business Online 支持以下客户端：

  - Lync 2010

  - Lync 2013

  - Lync Windows 应用商店应用

  - Lync Web App

  - Lync Mobile

  - Lync for Mac 2011

  - Lync Room System

  - Lync Basic 2013

有关客户端支持的详细信息，请参阅以下主题：

  - [Lync Online 客户端](https://go.microsoft.com/fwlink/?linkid=281902)

  - [Lync Server 2013 的客户端比较表](lync-server-2013-desktop-client-comparison-tables.md)

  - [Lync Server 2013 的移动客户端比较表](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a>拓扑要求

若要配置与 Skype for Business Online 的混合部署，需要具有以下受支持的拓扑之一：

  - Skype for Business Server 2015 部署，所有服务器运行 Skype for Business Server 2015。

  - Lync Server 2013 部署，所有服务器运行 Lync Server 2013。

  - Lync Server 2010 部署，其所有服务器运行 Lync Server 2010，具有最新的累积更新。
    
      - 联合边缘服务器和联合边缘服务器中的下一跃点服务器必须运行具有最新累积更新的 Lync Server 2010。
    
      - Skype for Business Server 2015 或 Lync Server 2013 管理工具必须安装在至少一台服务器或管理工作站上。

  - 混合 Lync Server 2013 和 Skype for Business Server 2015 部署，在运行 Skype for Business Server 2015 的至少一个站点中具有以下服务器角色：
    
      - 至少一个企业版池或 Standard Edition 服务器 
    
      - 与 SIP 联盟关联的控制器池（如果存在）
    
      - 与 SIP 联盟关联的边缘池

  - 在运行 Skype for Business Server 2015 的至少一个站点中混合部署 Lync Server 2010 和 Skype for Business Server 2015，其中具有以下服务器角色：
    
      - 至少一个企业版池或 Standard Edition 服务器 
    
      - 与 SIP 联盟关联的控制器池（如果存在）
    
      - 与站点的 SIP 联盟关联的边缘池

  - 在至少一个运行 Lync Server 2013 的站点中混合部署具有以下服务器角色的 Lync Server 2010 和 Lync Server 2013：
    
      - 站点中至少一个企业版池或 Standard Edition 服务器
    
      - 与 SIP 联盟关联的控制器池（如果站点中存在）
    
      - 与站点的 SIP 联盟关联的边缘池

<div>


> [!IMPORTANT]  
> 所有用户管理（包括用户在本地和 UNRESOLVED_TOKEN_VAL (skypeforbusiness) Online 之间移动）都需要使用最新安装的管理工具版本完成。 必须在能够连接到现有本地部署和 Internet 的单独服务器上安装管理工具。 将用户从本地部署移动到 UNRESOLVED_TOKEN_VAL (skype16_online) 的 <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet 必须从连接到本地部署的管理工具运行。



</div>

有关支持的拓扑的详细信息，请参阅 Lync [Server 2013](lync-server-2013-supported-topologies.md)中支持的拓扑和 [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)企业混合部署的参考拓扑。

有关混合部署和将 PowerShell 连接到 Lync Online 的故障排除信息，请参阅 [Lync Online：Lync PowerShell 和混合故障排除](https://go.microsoft.com/fwlink/p/?linkid=306718)。

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a>允许/阻止联合列表的要求

允许域列表包括已配置合作伙伴“边缘”完全限定域名 (FQDN) 的域。这些域有时也称 *允许的合作伙伴服务器* 或 *直接联盟合作伙伴*。您应熟悉开放联盟和封闭联盟（在本地部署中分别称为 *合作伙伴发现* 和 *允许的合作伙伴域列表*）之间的差异。

必须满足以下要求才能成功配置混合部署：

  - 必须为本地部署和 Microsoft 365 或 Office 365 组织配置相同的域匹配。 如果在本地部署中启用了合作伙伴发现，则必须为您的联机租户配置开放联盟。 如果未启用合作伙伴发现，则必须为您的联机租户配置封闭联盟。

  - 本地部署中的阻止域列表必须与您的联机租户的阻止域列表完全匹配。

  - 本地部署中的允许域列表必须与您的联机租户的允许域列表完全匹配。

  - 必须为联机租户的外部通信启用联合，该外部通信是使用 Lync Online 控制面板配置的。

</div>

<div>

## <a name="dns-settings"></a>DNS 设置

为混合部署创建 DNS 记录时，所有 Lync 外部 DNS 记录应指向本地基础结构。 有关所需 DNS 记录的详细信息，请参阅域名系统 (DNS) [Lync Server 2013 的要求](lync-server-2013-domain-name-system-dns-requirements.md)。

此外，您还需要确保下表中所述的 DNS 解析在您的本地部署中正常运行：


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>DNS 记录</p></td>
<td><p>解析者</p></td>
<td><p>DNS 要求</p></td>
</tr>
<tr class="even">
<td><p>_sipfederationtls._tcp 的 DNS SRV 记录。 &lt;sipdomain.com 解析为 Access Edge 外部 IP 帐户的所有受支持的 &gt; SIP () </p></td>
<td><p>边缘服务器</p></td>
<td><p>在混合配置中启用联盟通信。边缘服务器需要知道在什么位置为 SIP 域路由分布在本地设备和在线设备上的联盟流量。</p></td>
</tr>
<tr class="odd">
<td><p>边缘 Web 会议服务 FQDN 的 DNS A 记录，例如解析为 Web 会议边缘外部 IP 的 webcon.contoso.com</p></td>
<td><p>已连接到用户计算机的内部公司网络</p></td>
<td><p>让在线用户能够在本地托管会议中演示或查看内容。内容包括 PowerPoint 文件、白板、轮询和共享笔记。</p></td>
</tr>
</tbody>
</table>


根据 DNS 在您的组织中如何配置，您可能需要将这些记录添加到内部托管 DNS 区域，以便相应的 SIP 域能够提供对这些记录的内部 DNS 解析。

</div>

<div>

## <a name="firewall-considerations"></a>防火墙注意事项

您的网络上的计算机必须能够执行标准 Internet DNS 查找。如果这些计算机可以连接标准 Internet 站点，表明您的网络符合此要求。

根据数据中心Microsoft Online Services的位置，还必须将网络防火墙设备配置为接受基于通配符域名的连接，例如 (来自 \* .outlook.com) 的所有流量。 如果组织的防火墙不支持通配符名称配置，必须手动确定要允许的 IP 地址范围和指定的端口。

请参阅帮助主题 [Office 365 URL 和 IP 地址范围](https://go.microsoft.com/fwlink/p/?linkid=252942)。

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a>端口和协议要求

除了内部 Lync Server 2013 通信的端口要求外，还必须配置以下端口。


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>协议/端口</th>
<th>应用程序</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TCP 443</p></td>
<td><p>打开入站</p>
<ul>
<li><p>Active Directory 联合身份验证服务 (联合服务器角色) </p>
<p>有关详细信息，请参阅了解 <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">AD FS 角色服务</a>。</p></li>
<li><p>Active Directory 联合身份验证服务 (代理服务器角色) </p></li>
<li><p>Microsoft Online Services 门户</p></li>
<li><p>我的公司门户</p></li>
<li><p>Outlook Web App</p></li>
<li><p>Lync 客户端 (从本地 Lync Server 与 Lync Online 通信) </p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>TCP 80 和 443</p></td>
<td><p>打开入站</p>
<ul>
<li><p>Microsoft Online Services 目录同步工具</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>TCP 5061</p></td>
<td><p>在边缘服务器上打开入站/出站</p></td>
</tr>
<tr class="even">
<td><p>PSOM/TLS 443</p></td>
<td><p>为数据共享会话打开入站/出站</p></td>
</tr>
<tr class="odd">
<td><p>STUN/TCP 443</p></td>
<td><p>为音频、视频、应用程序共享会话打开入站/出站</p></td>
</tr>
<tr class="even">
<td><p>STUN/UDP 3478</p></td>
<td><p>为音频和视频会话打开入站/出站</p></td>
</tr>
<tr class="odd">
<td><p>RTP/TCP 50000-59999</p></td>
<td><p>为音频和视频会话打开出站</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a>用户帐户和数据

在 Lync Server 2013 混合部署中，必须先在本地部署中创建希望位于 Lync Online 的任何用户，以便用户帐户在 Active Directory 域服务中创建。 然后，你可以将用户移动到 Skype for Business Online，这将移动用户的联系人列表。

当您使用 AD FS 和 Dirsync 在您的 Lync 本地和 Lync Online 部署之间同步用户帐户时，您需要在您的本地和联机 Lync 部署之间同步您组织中所有 Lync 用户的 AD 帐户，即使用户未移动到 Lync Online。 如果未同步所有用户，则组织中本地和联机用户之间的通信可能无法按预期工作。

<div>


> [!IMPORTANT]  
> 如果用户是使用 Microsoft 365 管理中心的联机门户创建的，则用户帐户不会与本地 Active Directory 同步，并且该用户不会存在于本地 Active Directory 中。 如果您已经在 Lync Online 中创建用户，并且想要配置与本地 Lync Server 的混合，请参阅在 <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013</A>中将用户从 Lync Online 移动到本地 Lync。



</div>

规划混合部署时还应考虑以下用户相关的问题。

  - **用户联系人**   Lync Online 用户的联系人限制为 250。 当帐户移动到 Lync Online 时，将从用户联系人列表中删除超过此数目的所有联系人。

  - **即时消息和状态**   用户联系人列表、组和访问控制列表 (ACL) 将与用户帐户一起迁移。

  - **会议数据、会议内容和计划的会议**   此内容不会与用户帐户一起迁移。 用户必须在其帐户迁移到 Lync Online 之后重新安排会议。

</div>

<div>

## <a name="user-policies-and-features"></a>用户策略和功能

  - 在 Lync Server 2013 混合环境中，用户可以在本地或联机启用即时消息、语音和会议，但不能同时启用这两者。

  - **Lync 客户端**    某些用户在移动到 Lync Online 时可能需要新的客户端版本。 对于 Office Communications Server 2007 R2，在迁移到 Lync Online 之前，必须将用户移动到 Lync Server 2013 池。
    
    有关客户端支持的详细信息，请参阅 [Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) 的客户端和支持的 [Lync 客户端和网络端口配置](https://go.microsoft.com/fwlink/p/?linkid=281901)。

  - **本地策略和配置 (非用户)**   联机策略和本地策略需要单独的配置。 无法设置适用于二者的全局策略。

</div>

</div>

<span> </span>

</div>

</div>

</div>
