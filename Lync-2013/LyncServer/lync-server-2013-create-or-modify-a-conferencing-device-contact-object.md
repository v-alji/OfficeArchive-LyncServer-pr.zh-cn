---
title: Lync Server 2013：创建或修改会议设备联系人对象
description: Lync Server 2013：创建或修改会议设备联系人对象。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 853ee1c7dfda2fda99431b8cc1a5210a51f39a4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392027"
---
# <a name="create-or-modify-a-conferencing-device-contact-object-in-lync-server-2013"></a>在 Lync Server 2013 中创建或修改会议设备联系人对象

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-10-02_

若要创建会议会议室对象，请首先创建一个 Active Directory 用户帐户来表示该设备。 然后，使用 **CsMeetingRoom** cmdlet 使该帐户能够充当会议设备。 如果需要更改现有会议设备的属性，请使用 **CsMeetingRoom** cmdlet。

这些 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。

<div>


> [!NOTE]  
> 有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> 。



</div>

<div>


<div>

## <a name="creating-a-conferencing-device"></a>创建会议设备

  - 在创建表示新会议设备的 Active Directory 用户帐户后，通过使用 **enable-CsMeetingRoom** cmdlet 启用它。 请确保包含) 会议设备标识、b) 房间帐户所在的注册机构池和 c) 分配给该帐户的 SIP 地址。 例如：
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="modifying-a-conferencing-device"></a>修改会议设备

  - 若要修改现有会议设备的属性值，请使用 **CsMeetingRoom** cmdlet。 例如，以下命令将更新与会议设备关联 (LineUri) 的电话号码：
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

</div>

有关详细信息，请参阅 [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) Cmdlet 和 [CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) cmdlet 的帮助主题。

</div>

</div>

<span> </span>

</div>

</div>

</div>

