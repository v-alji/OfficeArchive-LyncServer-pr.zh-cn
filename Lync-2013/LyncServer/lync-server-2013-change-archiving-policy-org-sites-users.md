---
title: Lync Server 2013：更改存档策略以启用或禁用组织、网站或用户的内部或外部通信的存档
description: Lync Server 2013：更改存档策略以启用或禁用组织、网站或用户的内部或外部通信的存档。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435178"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a>在 Lync Server 2013 中更改存档策略以启用或禁用组织、网站或用户的内部或外部通信的存档

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-23_

在 Lync Server 2013 中，你可以使用策略为托管于 Lync Server 2013 的用户启用和禁用内部通信和外部通信的存档。 这包括以下存档策略：

  - 部署 Lync Server 2013 时默认创建的全局策略。

  - 可创建和使用的可选网站级和用户级策略，用于指定如何为特定网站或用户实现存档。

你在部署存档时最初设置存档策略，但你可以在部署后更改、添加和删除策略。 在 Lync Server 2013 控制面板中，你可以使用 "**存档和监视**" 组的 "**存档策略**" 页面管理全局级别、网站级别和用户级别的策略。 如果你将 Lync Server 存储与 Exchange 2013 存储集成，Exchange 用户策略将优先于 Lync Server 2013 存档策略。

有关如何实施策略的详细信息（包括策略的层次结构），请参阅规划文档、部署文档或操作文档中的在 [Lync Server 2013 中的存档的工作原理](lync-server-2013-how-archiving-works.md) 。

<div>


> [!NOTE]  
> 如果为你的部署启用了 Microsoft Exchange 集成，Exchange 策略将控制是否为托管于 Exchange 2013 的用户启用存档，并将其邮箱置于 In-Place 保留。 有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。<BR>在启用存档之前，应在存档配置中指定所有适当的选项。 有关详细信息，请参阅在 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 中为你的组织、网站和池在操作文档中管理存档配置选项</A> 。



</div>

<div>

## <a name="to-change-an-archiving-policy"></a>更改存档策略

1.  使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。

2.  打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。 有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。

3.  在左侧导航栏中，单击“监控和存档”，然后单击“存档策略”。

4.  在策略列表中，执行下列操作之一：
    
      - 若要更改整个部署的策略，请单击策略列表中的“**全局**”，再单击“**编辑**”，然后单击“**显示详细信息**”。
    
      - 若要更改单个站点的策略，请单击策略列表中的站点名称，再单击“**编辑**”，然后单击“**显示详细信息**”。
    
      - 若要更改单个用户或用户组的策略，请单击策略列表中的用户或用户组的名称，再单击“**编辑**”，然后单击“**显示详细信息**”。

5.  在“**编辑存档策略**”页中，执行下列操作：
    
      - 若要为策略启用或禁用内部存档，请选中或清除“**存档内部通信**”复选框。
    
      - 若要为策略启用或禁用外部存档，请选中或清除“**存档外部通信**”复选框。

6.  单击“**提交**”。
    
    <div>
    

    > [!IMPORTANT]  
    > 用户策略的设置仅适用于要应用该策略的特定用户和用户组。 有关详细信息，请参阅 <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">将存档策略应用于 Lync Server 2013 中的用户</A>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a>使用 Windows PowerShell Cmdlet 启用和禁用存档

可以使用 **CsArchivingPolicy** cmdlet 在内部和外部通信会话) 启用和禁用存档 (。 此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。 有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a>启用内部通信会话的存档

  - 若要启用内部通信会话的存档，请将 **ArchiveInternal** 属性的值设置为 True ($True) 。 例如：
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a>启用外部通信会话的存档

  - 若要启用外部通信会话的存档，请将 **ArchiveExternal** 属性的值设置为 True ($True) 。 例如：
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a>启用内部和外部通信会话的存档

  - 若要同时启用内部和外部通信会话的存档，请将 **ArchiveInternal** 和 **ArchiveExternal** 属性设置为 True：
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a>禁用存档

  - 若要完全禁用存档，请将 **ArchiveInternal** 和 **ArchiveExternal** 属性设置为 False ($False) 。 例如：
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

有关详细信息，请参阅 [CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet 的帮助主题。

</div>

<div>

## <a name="see-also"></a>另请参阅


[在 Lync Server 2013 中管理内部和外部通信的存档](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

