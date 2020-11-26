---
title: Lync Server 2013：配置默认图片选项
description: Lync Server 2013：配置默认图片选项。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring default picture options
ms:assetid: b1c986f0-6400-447a-9e36-78c1c3a4f793
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn205074(v=OCS.15)
ms:contentKeyID: 56280893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6261aca82b4c71eb8e0573e8d2adbfc008e743fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433211"
---
# <a name="configuring-default-picture-options-in-lync-server-2013"></a>在 Lync Server 2013 中配置默认图片选项

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-03-22_

默认情况下，将自动显示用户的图片。 如果用户想要隐藏其图片，可以在 Lync 客户端中选择 " **隐藏我的图片** " 选项。 但是，其他一些 Office 应用程序将忽略此设置。

如果在用户关闭图片时也可能显示图片，则可以为网站或服务更改 Lync 图片显示设置，以便默认情况下不显示用户的图片。 使用以下 Lync Server Management Shell cmdlet，以便用户的图片在客户端中明确选择 " **显示我的图片** " 选项，否则不会显示。

    Set-CsPrivacyConfiguration -DisplayPublishedPhotoDefault $False

有关此 cmdlet 的详细信息，请参阅 Lync Server Management Shell 文档中的 " [设置 CsPrivacyConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration) "。

</div>

<span> </span>

</div>

</div>

</div>

