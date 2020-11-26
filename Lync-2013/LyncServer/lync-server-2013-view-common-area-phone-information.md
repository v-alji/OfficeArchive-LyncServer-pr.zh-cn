---
title: Lync Server 2013：查看常见的区域电话信息
description: Lync Server 2013：查看常见的区域电话信息。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View common area phone information
ms:assetid: e652240c-6a3f-4be7-a083-32f24c08e655
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994081(v=OCS.15)
ms:contentKeyID: 51803992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4debe9a76118ac0bf1ca711426ce5487009a053
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443375"
---
# <a name="view-common-area-phone-information-in-lync-server-2013"></a>在 Lync Server 2013 中查看常见的区域电话信息

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-20_

你可以使用 **CsCommonAreaPhone** cmdlet 查看配置为在你的组织中使用的公共区域电话的相关信息。 如果在没有任何参数的情况下使用，此 cmdlet 将返回有关所有公共区域电话的信息。 可选参数提供不同的筛选信息的方式。 例如，您可以返回在指定组织单位 (OU) 或指定大楼内所有联系人对象中具有联系人对象的所有公共区域电话。 有关 **CsCommonAreaPhone** 参数的详细信息，请参阅 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)。

从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行 **CsCommonAreaPhone** 。

<div>


<div>

## <a name="viewing-information-about-all-your-common-area-phones"></a>查看有关所有常用区域电话的信息

  - 若要查看有关所有常用区域电话的信息，请在 Lync Server 命令行管理程序中键入以下命令，然后按 Enter：
    
        Get-CsCommonAreaPhone
    
    您将获得类似以下内容的信息：
    
        Identity           : CN=Building 14 Lobby,OU=Redmond,
                             DC=litwareinc,DC=com
        RegistrarPool      : atl-cs-001.litwareinc.com
        Enabled            : True
        SipAddress         : sip:4714e34b-9781-421d-b07a-
                             52056b5b4a56@litwareinc.com
        ClientPolicy       :
        PinPolicy          :
        VoicePolicy        :
        MobilityPolicy     :
        GroupChatPolicy    :
        ConferencingPolicy :
        LineURI            : tel:+14255550712
        DisplayNumber      : 1-425-555-0712
        DisplayName        : Building 14 Lobby
        Description        :
        ExUmEnabled        : False

</div>

有关详细信息，请参阅 [CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone) Cmdlet 的帮助主题。

</div>

</div>

<span> </span>

</div>

</div>

</div>

