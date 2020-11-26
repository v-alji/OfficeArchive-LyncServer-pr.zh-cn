---
title: Lync Server 2013：为自动发现服务创建 DNS 记录
description: Lync Server 2013：为自动发现服务创建 DNS 记录。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating DNS records for the Autodiscover Service
ms:assetid: 3756ffe4-c6b1-492d-850e-42a832e06567
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690010(v=OCS.15)
ms:contentKeyID: 48183823
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6903e6b07001289db8b65e8cc962e8d8db4b248b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431510"
---
# <a name="creating-dns-records-for-the-autodiscover-service-in-lync-server-2013"></a>在 Lync Server 2013 中为自动发现服务创建 DNS 记录

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-06-20_

您的 Lync 移动用户将需要您启用自动发现，其中包括创建某些域名系统 (DNS) 记录的部分。 根据你的需要，你需要满足以下要求：

  - 一个内部 DNS 记录，用于支持从你的组织的网络中连接的移动用户。

  - 支持从 Internet 连接的移动用户的外部 DNS 记录或公共 DNS 记录

为什么？ 你需要为每个 SIP 域创建一个内部 DNS 记录和一个外部 DNS 记录。

你创建的 DNS 记录可以是 (主机) 记录或 CNAME 记录。 为帮助你解决此问题，我们将指导你了解如何在下面创建这些内部和外部 DNS 记录。 如果需要进一步阅读有关移动用户的 DNS 要求的详细信息，您可以查看 [Lync Server 2013 中的移动技术要求](lync-server-2013-technical-requirements-for-mobility.md)。

<div>

## <a name="creating-an-internal-dns-cname-record"></a>创建内部 DNS CNAME 记录

1.  要创建内部 DNS 记录，您需要使用域管理员组的成员或 DnsAdmins 组的成员登录到您的网络中的 DNS 服务器上。

2.  打开 "DNS 管理" 管理单元：单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。

3.  在 DNS 服务器的控制台树中，展开用于安装 Lync Server 2013 控制器池和前端池的 Active Directory 域的 " **正向查找区域** "。  (例如，contoso. 本地) 。

4.  检查并查看是否存在针对内部 DNS 记录的控制器池的主机 A (AAAA 是否存在) 记录的主机 A 记录应存在于内部 Web 服务的内部 Web 服务完全限定的域名 (FQDN) 的 FQDN (例如，lyncwebdir01) 。 如果不在这里，你可能不会使用控制器池，并且你将需要为你的前端池或单个服务器 FQDN （如果你的设置）使用 FQDN。

5.  请注意，请检查并查看是否存在针对内部 DNS 记录的前端池的主机 A (AAAA) 记录，主机 A (或 AAAA) 记录应存在于你的前端池的内部 Web 服务 FQDN (例如，lyncwebpool01) 。 如果不是，你需要记下前端服务器或标准版服务器的 FQDN。

6.  知道存在 (或 AAAA) 记录的主机后，在 DNS 服务器的控制台树中，展开您的 SIP 域的 " **正向查找区域** " (例如，contoso.com ") "。

7.  右键单击 SIP 域名称，然后单击 " **新建别名 (CNAME)**"。

8.  在 " **别名名称**" 中，键入 lyncdiscoverinternal 作为内部自动发现服务 URL 的主机名。

9.  在 " **完全限定的域名 (适用于目标主机的 FQDN)** 中，键入或浏览到你的控制器池的内部 WEB 服务 FQDN (例如，lyncwebdir01) ，然后单击 **" 确定 "**。

10. 必须在 Lync Server 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 CNAME 记录。

</div>

<div>

## <a name="creating-an-external-dns-cname-record"></a>创建外部 DNS CNAME 记录

1.  若要创建外部 DNS CNAME 记录，你需要连接到你的公共 DNS 提供商，然后按照我们的步骤操作。 我们无法确切描述你在 DNS 提供商环境中所处的位置，因为可能有不同的管理外部 DNS 的方式，但我们希望这些步骤有所帮助。

2.  使用可在该环境中创建 DNS 记录的帐户登录到您的外部 DNS 提供商。

3.  你应该已为此环境创建了一个 SIP 域。 展开此 SIP 域的 **正向查找区域** ，或者根据所使用的外部 DNS 接口选择它。

4.  你应该已经看到一个主机 A (AAAA) 你的控制器 (池的 AAAA，如 lyncwebexdir01.contoso.com) ，请确认这是。 如果不是，则您可能没有使用控制器池。 如果是这种情况，你需要使用前端池的 FQDN，或者，如果你为 Front-End server 或标准版服务器的单个服务器执行此操作，则需要使用它。

5.  你还需要确认对于你的外部 Web 服务，) 记录的主机 A (AAAA 是否存在) 适用于你的外部 Web 服务的完全限定域名 (FQDN 对于你的前端池 (（如 lyncwebextpool01.contoso.com) ），如果没有前端池，则为你的单服务器 FQDN 的 FQDN。 如前面的步骤所述，如果没有控制器池，则需要以下内容。

6.  现在，按照适用于你的外部 DNS 提供程序的格式，选择用于创建 **新别名 (CNAME)** 的选项 (这可能是菜单选项或链接，具体取决于 DNS 提供商的格式) 。

7.  应该有某种形式的 **别名** 文本框与内部 DNS，应输入 lyncdiscover 作为外部自动发现服务 URL 的主机名。

8.  还应该有某种形式的 **完全限定的域名 (FQDN) 用于目标主机** 文本框，下面是输入 Director 池的外部 WEB 服务 FQDN 的位置 (例如，lyncwebexdir01.contoso.com) 然后单击 "确定" 或 "执行外部 DNS 中的任何操作" 以接受此条目的创建。 如上面的步骤4中所述，如果你没有控制器池，你需要根据需要使用前端池 FQDN 或已设置的单服务器 FQDN。

9.  你将需要在 Lync 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 CNAME 记录。

</div>

<div>

## <a name="creating-an-internal-dns-a-record"></a>创建内部 DNS A 记录

1.  要创建内部 DNS 记录，请使用域管理员组的成员或 DnsAdmins 组的成员登录到您的网络中的 DNS 服务器。

2.  打开 "DNS 管理" 管理单元：单击 " **开始**"，单击 " **管理工具**"，然后单击 " **DNS**"。

3.  对于内部 DNS 记录，请在 DNS 服务器的控制台树中，展开您的 Active Directory 域的 **正向查找区域** (例如，contoso. 本地) 您的 Lync Server 2013 控制器池和前端池的安装位置。

4.  检查并查看是否存在针对内部 DNS 记录的控制器池的主机 A (AAAA 是否存在) 记录的主机 A 记录应存在于内部 Web 服务的内部 Web 服务完全限定的域名 (FQDN) 的 FQDN (例如，lyncwebdir01) 。 如果不在这里，您可能没有使用控制器池，并且您需要使用您的前端池的 IP 地址，甚至是单个服务器 IP 地址（如果您设置了）。

5.  请注意，请检查并查看是否存在针对内部 DNS 记录的前端池的主机 A (AAAA) 记录，主机 A (或 AAAA) 记录应存在于你的前端池的内部 Web 服务 FQDN (例如，lyncwebpool01) 。 如果不是，你需要记下前端服务器或标准版服务器的 IP 地址。

6.  知道存在 (或 AAAA) 记录的主机后，在 DNS 服务器的控制台树中，展开您的 SIP 域的 " **正向查找区域** " (例如，contoso.com ") "。

7.  右键单击 SIP 域名称，然后单击 " **新建主机 (A 或 AAAA)**。

8.  在 " **名称**" 中，键入 lyncdiscoverinternal 作为内部自动发现服务 URL 的主机名。

9.  在 " **IP 地址**" 中，键入 director (的内部 WEB 服务 IP 地址，或者，如果使用负载平衡器，请键入控制器负载平衡器) 的虚拟 IP (VIP) 。 如上面的步骤4所述，如果未使用 Director，可能需要输入前端服务器或标准版服务器的 IP 地址，或者，如果使用负载平衡器，请键入前端池负载平衡器的 VIP。

10. 单击 " **添加主机**"，然后单击 **"确定"**。

11. 若要创建其他 A 或 AAAA 记录，请重复步骤8到步骤10，请记住，你需要在 Lync Server 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 A 或 AAAA 记录。

12. 为 IPv6 创建 (后，AAAA) 记录，请单击 " **完成**"。

</div>

<div>

## <a name="creating-an-external-dns-a-record"></a>创建外部 DNS A 记录

1.  若要创建外部 DNS 记录，请连接到您的公共 DNS 提供商，然后按照我们的步骤进行操作。 我们无法确切描述你在 DNS 提供商环境中所处的位置，因为可能有不同的管理外部 DNS 的方式，但我们希望这些步骤有所帮助。

2.  您需要以可在该环境中创建 DNS 记录的帐户的形式登录。

3.  对于外部 DNS 记录，请在 DNS 服务器的控制台树中，展开您的 SIP 域的 **正向查找区域** (例如，contoso.com) 。 对于外部 DNS 记录，请在 DNS 服务器的控制台树中，展开您的 SIP 域的 **正向查找区域** (例如，contoso.com) 。

4.  你应该已经看到了一个主机 A (AAAA for) 你的控制器池的应用 AAAA (如 lyncwebexdir01.contoso.com) ，因此请确认该地址是否存在以及 IP 地址是什么。 如果不是，则您可能没有使用控制器池。 如果是这种情况，您需要使用您的前端池的 IP 地址，或者，如果对单个服务器执行此操作，请使用您的 Front-End 服务器或标准版服务器。 请记住，你的服务器还可能位于负载平衡器后面，或者使用反向代理。 请记下您的 IP 地址，并按照以下步骤进行操作。

5.  你还需要确认对于你的外部 Web 服务，) 记录的主机 A (AAAA 是否存在) 适用于你的外部 Web 服务的完全限定域名 (FQDN 对于你的前端池 (（如 lyncwebextpool01.contoso.com) ），如果没有前端池，则为单服务器 Lync 安装的 IP 地址。 如前面的步骤所述，如果没有控制器池，则需要以下内容。

6.  现在，按照适用于您的外部 DNS 提供商的格式，选择用于创建 **新主机 a 或 AAAA** 的选项 (此选项可能是菜单选项或链接，具体取决于 DNS 提供商) 的格式。

7.  应存在一个用于输入 **名称** 的位置，键入 lyncdiscover 作为外部自动发现服务 URL 的主机名。

8.  还有一个 **Ip 地址** 文本框，你可以在此处输入你的用于你的 Director 池的 ip (例如，lyncwebexdir01.contoso.com) 池的负载平衡器 (的 ip 或可能导致相同) 的反向代理 ip，然后单击 "确定" 或执行外部 DNS 中的任何操作以接受此条目的创建。 如上面的步骤4中所述，如果你没有控制器池，则需要根据需要使用前端池 IP 地址或已设置的单服务器 IP 地址。

9.  你需要在 Lync 2013 环境支持的每个 SIP 域的正向查找区域中创建新的自动发现 A 或 AAAA 记录。

</div>

</div>

<span> </span>

</div>

</div>

</div>

