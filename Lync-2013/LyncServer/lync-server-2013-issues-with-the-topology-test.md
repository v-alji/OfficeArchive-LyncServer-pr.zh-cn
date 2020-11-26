---
title: Lync Server 2013：拓扑测试问题
description: Lync Server 2013：拓扑测试问题。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the topology test
ms:assetid: 821e8916-7b5d-4f64-8fb0-e5cc392ec1bb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205045(v=OCS.15)
ms:contentKeyID: 48184670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a0f24942844bcf371eff94ee04c8faafcf513d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426709"
---
# <a name="issues-with-the-topology-test-in-lync-server-2013"></a>Lync Server 2013 中的拓扑测试问题

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-21_

与 **CsTopology** cmdlet 类似，最佳做法分析器为你提供一种验证 Lync Server 2013 在全局级别正常运行的方法。 默认情况下，最佳做法分析器（如 cmdlet）将检查整个 Lync Server 2013 基础结构，验证所需服务是否正在运行，以及是否为这些服务以及在安装 Lync Server 2013 时创建的通用安全组设置了相应的用户权限和权限。

除了验证 Lync 服务器的整体有效性 **外，测试 CsTopology** 还检查特定服务的有效性。 有关使用 cmdlet 测试特定服务的详细信息，请参阅 Lync Server Management Shell 文档中的 [Test CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) 。 使用以下信息来帮助解决拓扑问题。

<div>


> [!NOTE]  
> 根据你的边缘服务器的配置和任何相关的外围网络设置（包括防火墙设置和权限），最佳做法分析器可能无法访问和扫描你的边缘服务器。 如果你在扫描中包含 Edge 服务器，并且报表指示访问边缘服务器时出现问题，请清除 " <STRONG>边缘服务器</STRONG> " 复选框，然后再次运行扫描以防止问题显示在报表中。



</div>

<div>

## <a name="resolving-issues-with-your-topology"></a>解决拓扑中的问题

如果拓扑测试发现拓扑出现问题，这些问题可能是由发布或启用拓扑时出现的问题导致的。

当你对拓扑进行更改时，所做的更改仅在已发布和已启用时生效。 必须使用拓扑生成器进行拓扑更改。 在进行更改后，您可以使用拓扑生成器发布和启用这些更改。

发布更改时，新信息 (例如，新网站或新服务器角色) 会写入中央管理存储。 但是，这些新 (或新修改的) 对象不会立即连接拓扑。 仅当启用已更新的拓扑时，对象才会加入拓扑。 如果你选择拓扑生成器中的 "发布" 选项，则会执行这两个步骤：将发布更改 (也就是说，它们将写入到中央管理存储) ，然后启用新拓扑。

默认情况下，RTCUniversalServerAdmins 组的成员有权运行 **CsTopology** Cmdlet 和 **Enable-CsTopology** cmdlet。 但是，如果尚未委派设置权限，则必须以域管理员身份登录才能运行 **Publish-CsTopology**。 若要为 RTCUniversalServerAdmins 提供实际使用 **CsTopology** cmdlet 的权限，必须在包含运行 Lync Server 服务的计算机的每个 Active Directory 容器上运行 **授予 CsSetupPermission** cmdlet。 若要授予 RTCUniversalServerAdmins 使用 **Enable CsTopology** cmdlet 的权利，必须针对包含运行 Lync Server 服务的计算机的每个 Active Directory 域服务容器运行 **CsSetupPermission** cmdlet。 请注意，这适用于使用拓扑生成器启用和发布拓扑。 如果您没有使用 " **设置 CsSetupPermission**" 委派权限，则只有域管理员可以通过拓扑生成器启用和发布拓扑。

</div>

</div>

<span> </span>

</div>

</div>

</div>

