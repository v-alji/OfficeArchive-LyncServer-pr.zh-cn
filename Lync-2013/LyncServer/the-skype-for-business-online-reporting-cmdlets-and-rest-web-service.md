---
title: Skype for Business Online 报告 cmdlet 和 REST web 服务
description: Skype for Business Online 报告 cmdlet 和 REST web 服务。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: The Skype for Business Online reporting cmdlets and REST web service
ms:assetid: cadd73a7-c08a-4102-b73a-ccb3ad4987bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362845(v=OCS.15)
ms:contentKeyID: 56563409
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2160e0910d42f811ec8b03fa50450d5f73c59b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423405"
---
# <a name="the-skype-for-business-online-reporting-cmdlets-and-rest-web-service"></a>Skype for Business Online 报告 cmdlet 和 REST web 服务

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-09-05_

通过结合报告功能，Skype for Business Online 提供对五个 Windows PowerShell cmdlet 的访问权限，可帮助生成这些报告，并且管理员也可以使用这些 cmdlet 返回自定义报告数据。 Skype for Business Online 还包括 REST (Representational 状态转移) ，可供开发人员用于检索自定义报告信息。

管理员可用的报告 cmdlet 包括：

  - CsActiveUserReport，提供有关活动用户数的信息 (也就是说，已登录到 Skype for Business Online 并参与至少一个会议或对等通信会话的用户) 。

  - CsAVConferenceTimeReport，它提供有关) 用户在音频/视频会议上花费的 (时间量的信息。

  - CsConferenceReport，提供有关用户参与的会议的数量和类型的信息。

  - CsP2PAVTimeReport，它提供有关在中的 (时间量的信息，) 用户在包含音频和/或视频的对等会话中花费的时间。

  - CsP2PSessionReport，提供有关用户参与的对等会话的数量和类型的信息。

大多数管理员将使用 Microsoft 365 管理中心提供的报表：不仅是自动生成的报表，还提供了数据的图形表示形式，这些数据通常更容易解释报告 cmdlet 返回的原始数字值。 但是，熟悉 Windows PowerShell 的管理员可以使用报告 cmdlet 从 Lync Online 报告中返回不容易提供的数据。 例如，报告 cmdlet 返回有关会话持续时间的信息， (每个会话持续) 的时间量（以分钟为单位）。 使用 Lync Online 报表不提供单个会话持续时间。 同样，在 "每日" 视图中，Lync Online 报表仅显示之前14天的信息。 如果想要查看其他日期的每日总计 (例如，四个月前的日期) 你可以使用报告 cmdlet 执行此操作。

管理员还可能对 [使用 Excel 检索 Office 365 报告数据](https://msdn.microsoft.com/library/dn781442.aspx)的文章感兴趣，其中介绍了如何使用 Microsoft Excel 中的 OData 数据查询功能来创建自定义 Office 365 报表。 自定义报表使你能够决定 (哪些数据以及从 Office 365 报告服务中返回多少数据) 。 自定义报表还允许你执行如下操作：指定应如何对数据进行排序和分组，并提供对不在管理中心中显示的信息的访问权限。

具有开发背景的管理员可以使用 REST web 服务获取未在 Skype for Business Online 管理中心中显示的信息。 REST 服务类似于 SOAP 服务，因为每种技术都提供了一种在客户端和服务器之间传输 XML 数据的方法。 但是，REST 服务至少具有与 SOAP 服务相比的两个优势。 对于一个，REST 使用称为 ATOM 供稿格式的标准化格式执行 XML 数据传输。 相比之下，传输数据时使用非标准格式的 SOAP。 此外，REST 能够跨阻止 "获取" 和 "发布" 等 HTTP 谓词的网络传输数据。

<div>

## <a name="see-also"></a>另请参阅


[Lync Online 报告](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))  


[Office 365 报告 Web 服务](https://msdn.microsoft.com/library/office/jj984325.aspx)  
[了解 Office 365 Reporting Web 服务](https://msdn.microsoft.com/library/office/jj984321.aspx)  
[Exchange Online 报告 Cmdlet](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)  
[使用 Excel 检索 Office 365 报告数据](https://msdn.microsoft.com/library/dn781442.aspx)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

