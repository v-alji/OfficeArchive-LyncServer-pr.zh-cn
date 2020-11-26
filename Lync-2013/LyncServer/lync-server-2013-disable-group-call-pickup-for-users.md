---
title: Lync Server 2013：为用户禁用组呼叫装货
description: Lync Server 2013：禁用组呼叫用户的分拣。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disable Group Call Pickup for users
ms:assetid: 91b06f9e-2840-45a2-bbb3-6a29179b9a9f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945638(v=OCS.15)
ms:contentKeyID: 51541492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3f5b4542cf7bb8ea5be524d2695701979ec2987
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429103"
---
# <a name="disable-group-call-pickup-for-users-in-lync-server-2013"></a>在 Lync Server 2013 中禁用用户的组呼叫装货

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-01-30_

使用以下过程可禁用用户的组呼叫装货。

<div>


> [!NOTE]  
> 当您为用户禁用组呼叫装货时，分配给该用户的呼叫装货组号码将不会保留。 如果随后想要为该用户重新启用组呼叫装货，则必须使用/enablegrouppickup 参数再次分配呼叫装货组编号。



</div>

<div>

## <a name="to-disable-group-call-pickup-for-a-user"></a>为用户禁用组呼叫装货

1.  使用管理员权限登录安装了 SEFAUtil 工具的计算机。

2.  在该命令行处，运行：
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /disablegrouppickup
    
    例如：
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /disablegrouppickup

</div>

<div>

## <a name="see-also"></a>另请参阅


[向 Lync Server 2013 中的用户分配组呼叫的装货号码](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[在 Lync Server 2013 中为用户启用组呼叫装货](lync-server-2013-enable-group-call-pickup-for-users.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

