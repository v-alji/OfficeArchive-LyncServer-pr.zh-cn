---
title: Lync Server 2013：呼叫允许控制的部署清单
description: Lync Server 2013：用于呼叫许可控制的部署核对清单。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for call admission control
ms:assetid: 7e56a169-3e63-44ab-bf28-1fdeb52381c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398631(v=OCS.15)
ms:contentKeyID: 48184621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea5b16d41228faf01637e7e0d78f5ce56f950a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391749"
---
# <a name="deployment-checklist-for-call-admission-control-in-lync-server-2013"></a>Lync Server 2013 中呼叫允许控制的部署清单

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-08_

要有效地为呼叫许可控制计划 (CAC) ，您需要考虑以下事项：

  - 部署 CAC 的先决条件。

  - 在部署之前必须进行的 CAC 和配置决策所需的信息。

<div>

## <a name="deployment-prerequisites-for-call-admission-control"></a>呼叫许可控制的部署先决条件

在部署 "呼叫许可控制" 之前，您必须已部署了 Lync Server 2013 内部服务器，包括 "前端" 池或标准版服务器。

</div>

<div>

## <a name="information-requirements-for-call-admission-control"></a>呼叫许可控制的信息要求

下表总结了部署 "呼叫许可控制" 所需的信息。

### <a name="information-requirements-for-call-admission-control-deployment"></a>呼叫许可控制部署的信息要求

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>信息</th>
<th>所需信息摘要</th>
<th>文档</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>您的组织所需的 Lync 服务器功能</p></td>
<td><ul>
<li><p>您的组织支持的功能</p></li>
<li><p>为单个用户启用的功能</p></li>
</ul></td>
<td><p><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">在 Lync Server 2013 中定义呼叫允许控制要求</a></p></td>
</tr>
<tr class="even">
<td><p>要部署的拓扑和组件</p></td>
<td><ul>
<li><p>CAC 相关组件将作为 Lync Server 2013 的一部分自动安装</p></li>
</ul></td>
<td><p><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">在 Lync Server 2013 中定义呼叫允许控制要求</a></p></td>
</tr>
<tr class="odd">
<td><p>系统要求</p></td>
<td><ul>
<li><p>硬件要求</p></li>
<li><p>软件要求</p></li>
<li><p>Collocation 要求</p></li>
</ul></td>
<td><p><a href="lync-server-2013-determining-your-system-requirements.md">确定 Lync Server 2013 的系统要求</a></p></td>
</tr>
<tr class="even">
<td><p>基础结构要求</p></td>
<td><ul>
<li><p>CAC 不需要特定的基础结构要求</p></li>
</ul></td>
<td><p><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Lync Server 2013 中呼叫允许控制的基础结构要求</a></p></td>
</tr>
<tr class="odd">
<td><p>网络接口要求</p></td>
<td><ul>
<li><p>内部和外部接口信息</p></li>
<li><p>路由信息 (包括有关在 <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a> Microsoft Lync Server 团队的客户响应频道中的 NextHop 博客的信息) </p></li>
</ul></td>
<td><p><a href="lync-server-2013-deploying-external-user-access.md">在 Lync Server 2013 中部署外部用户访问</a></p></td>
</tr>
<tr class="even">
<td><p>部署策略</p></td>
<td><ul>
<li><p>部署序列</p></li>
<li><p>工作组或域</p></li>
<li><p>安全性</p></li>
<li><p>监视和审核</p></li>
<li><p>硬件注意事项</p></li>
</ul></td>
<td><p><a href="lync-server-2013-best-practices-for-call-admission-control.md">Lync Server 2013 中呼叫允许控制的最佳做法</a></p></td>
</tr>
<tr class="odd">
<td><p>部署过程</p></td>
<td><ul>
<li><p>先决条件</p></li>
<li><p>信息要求</p></li>
<li><p>流程和过程</p></li>
</ul></td>
<td><p><a href="lync-server-2013-configure-call-admission-control.md">在 Lync Server 2013 中配置呼叫许可控制</a></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

