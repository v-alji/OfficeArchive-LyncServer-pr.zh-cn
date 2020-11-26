---
title: Lync Server 2013：企业语音的软件先决条件
description: Lync Server 2013：企业语音的软件先决条件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Software prerequisites for Enterprise Voice
ms:assetid: 41172119-9631-46c7-9d9f-386d951c650b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425916(v=OCS.15)
ms:contentKeyID: 48183960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23d21f40e275431f0384448341aa25ecb628ebf9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441604"
---
# <a name="software-prerequisites-for-enterprise-voice-in-lync-server-2013"></a>Lync Server 2013 中企业语音的软件先决条件

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-03_

验证要在其中部署企业语音的基础结构是否满足以下软件先决条件：

  - Lync Server 2013 标准版或企业版已安装并在您的网络上运行。

  - 所有边缘服务器都在你的外围网络中部署和运行，包括运行 Access Edge 服务的边缘服务器、A/V 边缘服务、Web 会议边缘服务和反向代理。

  - Microsoft Exchange Server 2007 Service Pack 3 (SP3) ，Microsoft Exchange Server 2010 或 Microsoft Exchange Server 2013 是与 Lync Server 集成 Exchange 统一消息以及向 Lync 终结点提供丰富通知和呼叫日志信息所必需的。

  - 已为 Lync Server 创建并启用了一个或多个用户。

  - Lync 客户端和设备已成功部署。

  - 拓扑生成器安装在网络上的服务器上。

<div>

## <a name="next-steps-verify-security-and-configuration-prerequisites"></a>后续步骤：验证安全和配置先决条件

验证企业语音的软件先决条件后，您可以使用文档来继续准备部署企业语音：

1.  按照 [在 Lync Server 2013 中的企业语音的安全和配置先决条件](lync-server-2013-security-and-configuration-prerequisites-for-enterprise-voice.md)中所述，验证安全、用户配置和硬件 perquisites。

2.  安装中介服务器，如在 [Lync server 2013 中安装中介服务器的文件](lync-server-2013-install-the-files-for-mediation-server.md)中所述，但 *仅* 当你希望部署独立的中介服务器或池时，因为在 Collocated 时，将中介服务器作为前端池或标准版服务器部署过程的一部分安装。

3.  配置主干连接以为用户提供 PSTN 连接，如在 [Lync Server 2013 中配置中继](lync-server-2013-configuring-trunks.md)中所述。

</div>

</div>

<span> </span>

</div>

</div>

</div>

