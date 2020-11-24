---
title: Lync Server 2013：规划远程呼叫控制
description: Lync Server 2013：规划远程呼叫控制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for remote call control
ms:assetid: 688a0328-1aa7-449f-b5f7-98c876112ed2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558658(v=OCS.15)
ms:contentKeyID: 48184371
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e3a089a806683098a948d235559bbcb16224bdde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392505"
---
# <a name="planning-for-remote-call-control-in-lync-server-2013"></a>在 Lync Server 2013 中规划远程呼叫控制

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-09-05_

在 Lync Server 2013 中，对远程呼叫控制方案的支持允许用户通过在其台式计算机上使用 Lync 2013 来控制其专用分支 exchange (PBX) 手机。 本部分介绍了部署远程呼叫控制的远程呼叫控制功能和要求。

通过 PBX 和 Lync Server 2013 之间的集成，用户可以使用 Lync 2013 用户界面 (UI) 以下列方式控制其 PBX 手机上的呼叫：

<div>


> [!NOTE]  
> 最终，承载用户 PBX 电话的 PBX 的功能决定了该用户可以使用的远程呼叫控制功能。



</div>

  - 进行拨出通话

  - 接听来电

  - 使用即时消息应答传入呼叫
    
    <div>
    

    > [!NOTE]  
    > 也就是说，当呼叫者的电话号码可以与组织的全球通讯簿中的即时消息地址相关联， (GAL) 、被呼叫者的 Lync 联系人列表中或联盟伙伴的组织中。

    
    </div>

  - 转移来电

  - 转发来电

  - 通话暂候

  - 在多个并发通话之间切换

  - 接听通话中的第二个呼叫 (即呼叫等待) 

  - Multifrequency (DTMF) 数字的拨号音

  - 在对话窗口中，在 Microsoft Office OneNote 笔记记录程序中键入备注

此外，当用户启用 "远程呼叫控制" 时，Lync 2013 向用户提供以下调用信息：

  - 当呼叫者的电话号码位于启用远程呼叫控制的用户的 Microsoft Office Outlook 消息和协作客户端、Lync 联系人列表或组织的 GAL 的联系人列表中时，按名称标识呼叫者。

  - 过去拨入和拨出的电话，它们保存在 Outlook 的 "对话历史记录" 文件夹中。

  - 未接来电通知将发送到用户的 Outlook 收件箱文件夹，但仅当接收来电时，才会生成 Lync。

<div>

## <a name="remote-call-control-and-enterprise-voice"></a>远程通话控制和企业语音

虽然远程呼叫控制功能与企业语音功能不同，并且不能同时启用用户，但企业语音还提供了一种可供启用远程呼叫控制的用户使用的功能子集。 如果部署了企业语音，则启用远程呼叫控制的用户可以使用 Lync 访问下列企业语音功能：

  - 拨打和接听其他 Lync 客户端的音频电话

  - 加入由已启用企业语音的用户创建的会议的音频部分

</div>

<div>

## <a name="in-this-section"></a>本节内容

  - [Lync Server 2013 中远程呼叫控制的部署任务](lync-server-2013-deployment-tasks-for-remote-call-control.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

