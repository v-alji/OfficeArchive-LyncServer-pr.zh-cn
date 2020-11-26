---
title: Lync Server 2013：保护 IIS
description: Lync Server 2013：保护 IIS。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Protecting IIS in Lync Server 2013
ms:assetid: a67171a6-6703-4e09-abb3-35d335bb674e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518332(v=OCS.15)
ms:contentKeyID: 62625492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51161f221c7235aad04850fdccc5d5e9db5cb579
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436837"
---
# <a name="protecting-iis-in-lync-server-2013"></a>在 Lync Server 2013 中保护 IIS

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-12-05_

在 Microsoft Office 通信服务器2007和 Microsoft Office 通信服务器 2007 R2 中， (IIS) 的 Internet 信息服务在标准用户帐户下运行。 这可能会导致问题：如果该密码已过期，则可能会丢失 Web 服务，这种问题通常很难诊断。 为了帮助避免密码过期，Microsoft Lync Server 2013 使你能够为不存在的计算机创建计算机帐户 () 该计算机可以充当运行 IIS 的网站中的所有计算机的身份验证主体。 由于这些帐户使用 Kerberos 身份验证协议，因此称为 Kerberos 帐户，并且新的身份验证过程称为 Kerberos Web 身份验证。 使您可以使用单个帐户管理所有 IIS 服务器。

若要在此身份验证主体下运行服务器，必须首先使用 New-CsKerberosAccount cmdlet 创建计算机帐户;然后，将此帐户分配给一个或多个网站。 执行分配后，将通过运行 Enable-CsTopology cmdlet 来启用帐户与 Lync Server 2013 网站之间的关联。 在其他情况下，这会在 Active Directory 域服务 (AD DS) 中创建所需的服务主体名称 (SPN) 。 SPN 为客户端应用程序提供了一种查找特定服务的方法。 有关详细信息，请参阅操作文档中的 " [新建-CsKerberosAccount](https://docs.microsoft.com/powershell/module/skype/New-CsKerberosAccount) "。

<div>

## <a name="best-practices"></a>最佳做法

为了帮助提高 IIS 的安全性，我们建议你为 IIS 实现 Kerberos 帐户。 如果不实现 Kerberos 帐户，IIS 将在标准用户帐户下运行。

</div>

</div>

<span> </span>

</div>

</div>

</div>

