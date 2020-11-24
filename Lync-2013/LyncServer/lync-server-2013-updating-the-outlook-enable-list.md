---
title: Lync Server 2013：更新 Outlook 启用列表
description: Lync Server 2013：更新 Outlook 启用列表。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Updating the Outlook enable list
ms:assetid: 5db120dc-52f9-4dde-acb9-3824ae245086
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215438(v=OCS.15)
ms:contentKeyID: 48242739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96edc327fa1b63d5da95eb6ea36a2296659910d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392259"
---
# <a name="updating-the-outlook-enable-list-in-lync-server-2013"></a>在 Lync Server 2013 中更新 Outlook 启用列表

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-01-07_

你可以通过在 Outlook 的加载项管理列表中创建一个策略来确保始终为用户启用适用于 Microsoft Lync 2013 的联机会议加载项。 "外接程序管理列表" 策略包含在组策略管理控制台的 Office 管理模板文件中。 它将在 HKCU \\ 软件 \\ 策略 " \\ Microsoft \\ Office \\ 15.0 \\ Outlook15 \\ 弹性 \\ AddinList" 下创建一个注册表项。 你可以将 ucaddin.dll 的值添加到此项，并配置 ucaddin.dll 值以使其始终处于启用状态，以便用户无法手动禁用它。

<div>

## <a name="to-add-ucaddindll-to-the-outlook-add-in-list"></a>将 ucaddin.dll 添加到 Outlook 外接程序列表

  - AddinList 注册表项位于 "HKCU \\ 软件 \\ 策略 \\ Microsoft \\ Office \\ 15.0 \\ Outlook15 \\ 弹性 AddinList" 下 \\ ，请添加以下值：
    
      - 注册表类型 = REG \_ SZ
    
      - Name = ucaddin.dll
    
      - 值 = 1 (指定外接程序始终处于启用状态，并且不能由最终用户管理) 

</div>

</div>

<span> </span>

</div>

</div>

</div>

