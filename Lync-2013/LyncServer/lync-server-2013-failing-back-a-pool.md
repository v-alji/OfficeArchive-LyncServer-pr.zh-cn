---
title: Lync Server 2013：对池进行故障回复
description: Lync Server 2013：退回池失败。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428326"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a>在 Lync Server 2013 中对池进行故障回复

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-11-01_

在遇到灾难的池重新联机 (也就是说，在此示例) 中，请执行以下步骤将部署还原为正常的工作状态。

请注意，故障回复过程需要几分钟才能完成。  作为参考，对于用户数为 20,000 的池而言，预期最多需要 60 分钟。

1.  通过键入以下 cmdlet 对最初驻留在 Pool1 中的用户进行故障回复，并已故障转移到 Pool2：
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

无需执行其他步骤。 如果您通过中央管理服务器进行了故障转移，您可以将其保留在 Pool2 中。

</div>

<span> </span>

</div>

</div>

</div>

