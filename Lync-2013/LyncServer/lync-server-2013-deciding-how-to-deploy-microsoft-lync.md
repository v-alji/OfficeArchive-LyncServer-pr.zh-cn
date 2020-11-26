---
title: Lync Server 2013：确定如何部署 Microsoft Lync
description: Lync Server 2013：确定如何部署 Microsoft Lync。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431230"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a>确定如何部署 Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-03_

规划 Lync 时，第一个主要决策是如何部署 Microsoft Lync：在本地 Lync Server 2013 或在云中通过 Microsoft 365 或 Office 365 进行 Lync Online。

  - **Lync Server 2013 本地** 版：此选项提供了完整的 Lync 功能集，并提供了配置、自定义和操作部署的绝佳灵活性。 所有服务器都安装在现场并由你的组织维护。 本地部署提供了各种 Lync Server 功能。

  - **云中的 Lync Online** Lync Online 适用于希望基于云的即时消息、状态和会议的成本和灵活性优势的组织，而不牺牲 Lync 服务器的企业级功能。 通过 Lync Online，Microsoft 部署和维护所需的服务器基础结构，并处理持续维护、修补和升级。 本地部署中提供的某些功能在 Lync Online 中不可用。

哪种类型的部署最适合你取决于要部署的工作负荷以及你的组织的地理和业务状态。

<div>

## <a name="lync-server"></a>Lync Server

本地 Lync 服务器部署最适用于以下情况：

  - **完整的企业语音功能**   如果你计划部署完整的企业语音解决方案以替换 PBX 或使用高级呼叫功能，则需要本地 Lync 服务器部署。 本地支持与 PBX 系统和中继的直接连接，以及高级电话功能（如响应组和呼叫寄存）。 Lync Online 目前不支持这些功能。

  - **媒体质量控件**   如果你需要各种媒体质量保证功能（如呼叫许可控制 (CAC) 和服务质量 (QoS) 功能），你将需要内部部署。

  - **持久聊天**   如果你需要为你的组织部署持久聊天，你必须选择本地部署。

  - **第三方服务器应用程序**   只有本地部署才能与使用 Microsoft 统一通信托管 API (UCMA) 的受信任的第三方应用程序配合使用。

  - **需要地区支持的多国/多地区公司**   如果您有多个国家或地区的数据中心，并且需要在区域基础上部署和管理服务器，则最好使用内部部署，因为它提供了这种类型的区域管理功能。

  - **完全控制策略、报告和升级**   使用本地 Lync 服务器部署，你可以访问完整的服务器和客户端策略集、监视和其他报告以及升级计时。 Lync Online 提供了策略设置和报告的子集，并提供了一个限制的有效窗口，可用于接受升级。

</div>

<div>

## <a name="lync-online"></a>Lync Online

如果上述列表中的任何因素对您来说都不重要，则您可能希望选择 Lync Online，以获得更简单的部署和可管理性。 Lync Online 提供了一种强大的 IM、状态和会议功能集，还支持在您的组织中的用户之间通过 IP 进行语音和视频通话。

</div>

</div>

<span> </span>

</div>

</div>

</div>
