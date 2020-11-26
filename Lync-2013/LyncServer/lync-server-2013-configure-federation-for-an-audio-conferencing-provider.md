---
title: Lync Server 2013：为音频会议提供商配置联盟
description: Lync Server 2013：为音频会议提供商配置联盟。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure federation for an audio conferencing provider
ms:assetid: 08dedcce-0d3f-45da-8282-cf2634a41665
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn510996(v=OCS.15)
ms:contentKeyID: 60595883
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c74654224c42618768d881a95031d58be4d55df5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434051"
---
# <a name="configure-federation-for-an-audio-conferencing-provider-in-lync-server-2013"></a>在 Lync Server 2013 中配置音频会议提供商的联盟

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-07-24_

如果你想要在混合 (部署中使用音频会议提供商 (ACP) 本地 lync Server 与 Lync Online) ，你需要在本地 Lync 部署和 ACP 合作伙伴之间配置联盟作为允许的伙伴服务器。 您可以通过向本地部署的联盟域列表添加 ACP 合作伙伴域和边缘服务器（可称为访问代理）来配置联盟。 然后，ACP 合作伙伴需要将您的本地边缘服务器池的 FQDN 添加到允许的联盟域列表。 联系你的 ACP 提供商以获取其他 detailsYour ACP 合作伙伴，然后需要将本地边缘服务器池的 FQDN 添加到其允许的联盟域列表。

  - **将 ACP 域和边缘服务器添加为允许的联盟域**
    
    若要将 ACP 域作为允许的伙伴服务器添加 (允许的联盟域) ，请按照在 [Lync Server 2013 中配置对允许的外部域的支持](lync-server-2013-configure-support-for-allowed-external-domains.md)中的步骤操作。 对于边缘服务器，请添加 ACP 合作伙伴的边缘服务器的 FQDN。 您可能需要联系 ACP 合作伙伴，获得其边缘服务器的 FQDN，ACP 也可能称之为访问代理。

  - **向 ACP 合作伙伴提供您的边缘服务器池的 FQDN**
    
    ACP 合作伙伴需要将您的边缘服务器池的 FQDN 添加到允许的联盟域列表，以便配置联盟，将您的本地域添加为允许的合作伙伴服务器。

</div>

<span> </span>

</div>

</div>

</div>

