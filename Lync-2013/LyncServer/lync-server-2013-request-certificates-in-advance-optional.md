---
title: Lync Server 2013：提前请求证书（可选）
description: Lync Server 2013：提前请求证书 (可选) 。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Request certificates in advance (optional)
ms:assetid: 9d6d7de6-ff2a-46da-b1b7-a354c8e383e4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412733(v=OCS.15)
ms:contentKeyID: 48184915
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92ac9b68012487d07f25f08649689611117202
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442717"
---
# <a name="request-certificates-in-advance-optional-for-lync-server-2013"></a>为 Lync Server 2013 提前请求证书（可选）

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-21_

所有运行 Lync Server 2013 的内部服务器都需要证书，包括每个企业版前端服务器、标准版服务器、Director、Edge 服务器和独立中介服务器。 尽管推荐内部企业证书颁发机构 (CA) 供内部服务器使用，但你也可以使用公共 CA。 有关证书要求和公用 CA 使用的详细信息，请参阅规划文档中的 [Lync Server 2013 内部服务器的证书要求](lync-server-2013-certificate-requirements-for-internal-servers.md) 。

Lync Server 2013 安装程序包括证书向导，该向导有助于在部署期间请求、分配和安装证书的任务。 如果你想要在安装服务器之前请求证书 (例如，为了在服务器的实际部署期间节省时间) ，你可以通过使用安装了 Lync Server 2013 管理工具的计算机或使用组织中定义的证书请求过程来执行此操作，前提是确保证书可导出并包含所有必需的主题备用名称。 预先申请证书是可选的。 如果不提前请求，则必须将其作为需要证书的每台服务器的设置的一部分进行请求。

此部署文档提供使用证书向导作为安装过程的一部分请求证书的过程，如 "在 lync server [2013 中配置服务器的证书](lync-server-2013-configure-certificates-for-servers.md)" 中所述，在 [lync server 2013 中配置 Director 的证书](lync-server-2013-configure-certificates-for-the-director.md)，并在此部署文档的 [Lync Server 2013 部分中安装中介服务器的文件](lync-server-2013-install-the-files-for-mediation-server.md) 。 如果提前申请证书，则必须根据需要在这些分区中修改证书部署过程，以便导入和分配证书，而不是在部署时请求证书。

<div>


> [!NOTE]  
> Lync Server 2013 包括对从运行 Windows Vista、Windows Server &nbsp; 2008、Windows server &nbsp; 2008 &nbsp; R2 和 windows 7 操作系统以及 Lync Phone Edition 的客户端的连接的 SHA-256 证书的支持。 若要支持使用 SHA-256 的外部访问，外部证书由使用 SHA-256 的公共 CA 颁发。



</div>

</div>

<span> </span>

</div>

</div>

</div>

