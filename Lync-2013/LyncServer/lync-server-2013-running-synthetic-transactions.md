---
title: Lync Server 2013：运行合成事务
description: Lync Server 2013：运行合成事务。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running synthetic transactions
ms:assetid: 2b56c7bd-8956-4fa1-8232-1876b959b258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720911(v=OCS.15)
ms:contentKeyID: 63969593
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26b0c26024f361dac196319eaf849c1847033cc9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442178"
---
# <a name="running-synthetic-transactions-in-lync-server-2013"></a>在 Lync Server 2013 中运行合成事务

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2014-08-18_

综合事务通常通过两种方式进行。 你可以使用 CsHealthMonitoringConfiguration cmdlet 为其每个注册机构池设置测试用户。 这些测试用户是已预配置为与综合事务一起使用的一对用户。  (通常是测试帐户，而不是属于实际用户的帐户。 ) 配置了针对池的测试用户，则可以针对该池运行合成事务，而无需指定 (的标识并提供用于) 测试所涉及的用户帐户的凭据。

或者，你可以使用实际的用户帐户运行综合事务。 例如，如果两个用户无法交换即时消息，你可以使用这两个用户帐户运行合成事务 (而不是一对测试帐户) ，然后尝试诊断并解决该问题。 如果你决定使用实际的用户帐户执行合成事务，则必须为每个用户提供登录名和密码。

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中配置观察程序节点测试用户和配置设置](lync-server-2013-configuring-watcher-node-test-users-and-configuration-settings.md)  
[Lync Server 2013 中的综合事务的特殊设置说明](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

