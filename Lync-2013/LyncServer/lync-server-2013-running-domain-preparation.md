---
title: Lync Server 2013：运行域准备
description: Lync Server 2013：运行域准备。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running domain preparation
ms:assetid: 95dab800-1f2c-4506-b36c-99986643b149
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398761(v=OCS.15)
ms:contentKeyID: 48184847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f2c4ebe94d07ed2d1fd9be013cd8e88204312f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442255"
---
# <a name="running-domain-preparation-for-lync-server-2013"></a>为 Lync Server 2013 运行域准备

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-04-16_

你可以使用安装程序或 Lync Server Management Shell cmdlet 准备域。 准备域的 cmdlet 为 **Enable-CsAdDomain**。

域准备是为 Lync Server 2013 准备 Active Directory 域服务的最后一步。

<div>

## <a name="to-use-setup-to-prepare-domains"></a>使用安装程序准备域

1.  以域管理员组的成员身份登录域中的任何服务器。

2.  在 Lync Server 2013 安装文件夹或媒体中，运行 Setup.exe 以启动 Lync Server 部署向导。

3.  单击“**准备 Active Directory**”，然后等待确定部署状态。

4.  在“**步骤 5：准备当前域**”中，单击“**运行**”。

5.  在 " **准备域** " 页面上，单击 " **下一步**"。

6.  在“**正在执行命令**”页上，查找“**任务状态：已完成**”，然后单击“**查看日志**”。

7.  在 " **操作** " 列下，展开 " **域准备**"， **\<Success\>** 在每个任务的末尾查找执行结果，验证域准备是否成功完成，关闭日志，然后单击 " **完成**"。

8.  等待 Active Directory 复制完成或强制复制到林根域控制器的 Active Directory 站点和服务管理单元中列出的所有域控制器。

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-domain"></a>使用 cmdlet 准备域

1.  以域管理员组的成员身份登录域中的任何服务器。

2.  安装 Lync Server Core 组件，如下所示：
    
    1.  在 Lync Server 2013 安装文件夹或媒体中，运行 Setup.exe 以启动 Lync Server 部署向导。
    
    2.  如果系统提示您安装 Microsoft Visual c + + 可再发行组件，请单击 **"是"**。
    
    3.  "Lync Server 2013 设置" 对话框提示你输入安装 Lync Server 文件的位置。 选择默认位置或 **浏览** 到您选择的位置，然后单击 " **安装**"。
    
    4.  在 "许可协议" 页面上，选中 " **我接受许可协议中的条款**"，然后单击 **"确定"**。 安装程序安装 Lync Server 2013 核心组件。

3.  启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。

4.  运行：
    
        Enable-CsAdDomain [-Domain <DomainFQDN>] 
    
    例如：
    
        Enable-CsAdDomain -Domain domain1.contoso.net 
    
    如果不指定 Domain 参数，则默认为本地域。

5.  验证域准备是否成功。 运行：
    
        Get-CsAdDomain [-Domain <Domain FQDN>] [-DomainController <Domain controller FQDN>] [-GlobalCatalog <Global catalog server FQDN>] [-GlobalSettingsDomainController <Domain controller FQDN where global settings are stored>] 
    
    例如：
    
        Get-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.com
    
    <div>
    

    > [!NOTE]  
    > 参数 GlobalSettingsDomainController 允许你指示全局设置的存储位置。 如果你的设置存储在系统容器中 (这通常是由于尚未将全局设置迁移到配置容器) 的升级部署，你可以在 Active Directory 林的根中定义域控制器。 如果全局设置存储在“配置”容器中（在新部署或设置已迁移到“配置”容器的升级部署中时通常是这种情况），则定义林中的任何域控制器。 如果不指定此参数，则 cmdlet 假定设置存储在配置容器中，并引用 AD DS 中的任何域控制器 &nbsp; 。

    
    </div>
    
    如果不指定 **Domain** 参数，则默认为本地域。
    
    如果域准备成功，此 cmdlet 将返回 LC DOMAINSETTINGS 状态的值为 "已 **\_ \_ \_ 准备就绪** "。

</div>

<div>

## <a name="see-also"></a>另请参阅


[使用 Cmdlet 为 Lync Server 2013 反向执行域准备](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)  


[为 Lync Server 2013 准备域](lync-server-2013-preparing-domains.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

