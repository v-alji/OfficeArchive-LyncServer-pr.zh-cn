---
title: Lync Server 2013：为用户分配组呼叫装货号码
description: Lync Server 2013：为用户分配组呼叫装货号码。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign Group Call Pickup numbers to users
ms:assetid: b8e79275-8e7e-4799-b908-f34f61df22f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945647(v=OCS.15)
ms:contentKeyID: 51541508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d550b4556af427e11e99ffb26fb2a6c34d019490
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438342"
---
# <a name="assign-group-call-pickup-numbers-to-users-in-lync-server-2013"></a>向 Lync Server 2013 中的用户分配组呼叫的装货号码

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-01-30_

将组呼叫挑选组号码添加到 "呼叫公园轨道" 表后，您可以将组分配给用户。 使用辅助扩展功能激活 (SEFAUtil ) 资源工具包工具将呼叫装货组分配给用户。

<div>


> [!NOTE]  
> 在混合部署中，不要向处于联机状态的用户分配组呼叫装货组。 处于联机状态的用户不能参与组呼叫装货。 也就是说，他们的呼叫无法由其他用户应答，他们也无法应答对其他用户的呼叫。



</div>

<div>

## <a name="to-assign-a-group-call-pickup-group-to-a-user"></a>将组呼叫装货组分配给用户

1.  使用管理员权限登录安装了 SEFAUtil 工具的计算机。

2.  在该命令行处，运行：
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    例如：
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中为用户启用组呼叫装货](lync-server-2013-enable-group-call-pickup-for-users.md)  
[在 Lync Server 2013 中禁用用户的组呼叫装货](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

