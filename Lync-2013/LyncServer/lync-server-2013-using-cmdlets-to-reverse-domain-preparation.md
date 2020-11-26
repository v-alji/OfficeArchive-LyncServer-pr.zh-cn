---
title: Lync Server 2013：使用 Cmdlet 反向执行域准备
description: Lync Server 2013：使用 cmdlet 反向域准备。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse domain preparation
ms:assetid: 014dba5d-fcb3-44c9-9d63-ae0755276dac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398071(v=OCS.15)
ms:contentKeyID: 48183227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d26cc97ee934ee959838f38f4e2f52f9bf89566
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439014"
---
# <a name="using-cmdlets-to-reverse-domain-preparation-for-lync-server-2013"></a>使用 Cmdlet 为 Lync Server 2013 反向执行域准备

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-29_

使用 **CsAdDomain** cmdlet 可撤消域准备步骤。

<div>

## <a name="to-use-cmdlets-to-reverse-domain-preparation"></a>使用 cmdlet 反向域准备

1.  以域管理员组的成员身份登录域中的任何服务器。

2.  启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。

3.  运行：
    
        Disable-CsAdDomain [-Domain <Fqdn>] [-DomainController <Fqdn>] [-Force <SwitchParameter>] 
        [-GlobalCatalog <Fqdn>] [-GlobalSettingsDomainController <Fqdn>] 
    
    例如：
    
        Disable-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.net -Force
    
    如果存在 Force 参数，即使已激活域中的一个或多个前端服务器或 A/V 会议服务器，也会回退域准备。 如果 Force 参数不存在，则在激活域中的任何前端服务器或 A/V 会议服务器时，将终止域准备回退。
    
    <div>
    

    > [!NOTE]  
    > 参数 GlobalSettingsDomainController 允许你指示全局设置的存储位置。 如果你的设置存储在系统容器中 (这通常是由于尚未将全局设置迁移到配置容器) 的升级部署，你可以在 Active Directory 林的根中定义域控制器。 如果全局设置存储在“配置”容器中（在新部署或设置已迁移到“配置”容器的升级部署中时通常是这种情况），则定义林中的任何域控制器。 如果不指定此参数，则 cmdlet 假定设置存储在配置容器中，并引用 AD DS 中的任何域控制器 &nbsp; 。

    
    </div>

</div>

<div>

## <a name="see-also"></a>另请参阅


[为 Lync Server 2013 运行域准备](lync-server-2013-running-domain-preparation.md)  


[为 Lync Server 2013 准备域](lync-server-2013-preparing-domains.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

