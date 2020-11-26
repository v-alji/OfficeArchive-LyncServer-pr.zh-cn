---
title: 验证是否已从旧版池中删除所有 Exchange UM 联系人对象
description: 验证是否已从旧版池中删除所有 Exchange UM 联系人对象。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440134"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a>验证是否已从旧版池中删除所有 Exchange UM 联系人对象

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-26_

使用 **OCSUmUtil** 工具或 **CsExumContact** cmdlet 验证 Exchange UM 联系人对象是否已从旧版 Office 通信服务器 2007 R2 池中删除。 **OCSUmUtil** 位于以下文件夹中：

% 程序文件% \\ 常用文件% \\ Lync Server 2013 \\ 支持 \\OcsUMUtil.exe

**OCSUmUtil** 必须从具有以下内容的用户帐户运行：

  - RTCUniversalServerAdmins 和 RTCUniversalUserAdmins 组中的成员身份 (包括读取 Exchange Server 统一消息设置的权限) 

  - 在指定组织单位 (OU) 容器中创建联系人对象的域权限

有关使用 **CsExumContact** cmdlet 的详细信息，请参阅 Lync Server Management Shell 文档中的 [CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) 。

</div>

<span> </span>

</div>

</div>

</div>

