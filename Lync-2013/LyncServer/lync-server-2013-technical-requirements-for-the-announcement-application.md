---
title: Lync Server 2013：通知应用程序的技术要求
description: Lync Server 2013：公告应用程序的技术要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for the Announcement application
ms:assetid: fbd8c204-3765-4b22-a0c9-a781b5126366
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205413(v=OCS.15)
ms:contentKeyID: 48185944
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5019408b79301bbcda3993ceb7d96ee4d9b7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444306"
---
# <a name="technical-requirements-for-the-announcement-application-in-lync-server-2013"></a>Lync Server 2013 中通知应用程序的技术要求

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-11-07_

本部分介绍了公告应用程序的以下技术要求：

  - 硬件要求

  - 软件要求

  - 端口要求

  - 音频文件要求

<div>

## <a name="hardware-requirements"></a>硬件要求

公告应用程序与前端服务器具有相同的硬件要求。 有关硬件要求的详细信息，请参阅支持文档中的 [Lync server 2013 的服务器硬件平台](lync-server-2013-server-hardware-platforms.md) 。

</div>

<div>

## <a name="software-requirements"></a>软件要求

公告应用程序与前端服务器具有相同的操作系统要求和软件先决条件。 有关软件要求的详细信息，请参阅支持文档中的 [Lync server 2013 中的 "服务器和工具操作系统支持](lync-server-2013-server-and-tools-operating-system-support.md) "。

运行公告应用程序的所有前端服务器或标准版服务器必须为运行 Windows Server 2008 R2 的服务器安装 Windows Media Format Runtime，或者为运行 Windows Server 2012 或 Windows Server 2012 R2 的服务器安装 Microsoft Media Foundation。 对于 Windows Server 2008 R2，Windows Media 格式运行时作为 Windows 桌面体验的一部分进行安装。 Windows media 音频需要 windows Media 格式运行时或 Microsoft Media Foundation () 公告应用程序为公告和音乐播放的 .wma。

</div>

<div>

## <a name="port-requirements"></a>端口要求

公告应用程序使用以下端口：

  - **端口 5071**  用于 SIP 侦听请求

<div>


> [!NOTE]  
> 此端口是默认设置，可以通过使用 <STRONG>Set-CsApplicationServer</STRONG> cmdlet 进行更改。 有关此 cmdlet 的详细信息，请参阅 Lync Server Management Shell 文档。



</div>

</div>

<div>

## <a name="audio-file-requirements"></a>音频文件要求

"通知" 应用程序支持波形 ( .wav) 文件格式和 Windows Media 音频 ( 用于音乐和公告的文件格式) 文件格式。 公告应用程序的音频文件要求与响应组应用程序的音频文件相同。 有关详细信息，请参阅 [Lync Server 2013 中的 "响应" 组技术要求](lync-server-2013-technical-requirements-for-response-group.md)。

</div>

</div>

<span> </span>

</div>

</div>

</div>

