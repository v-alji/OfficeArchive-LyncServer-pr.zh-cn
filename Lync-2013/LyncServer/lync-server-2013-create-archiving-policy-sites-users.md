---
title: Lync Server 2013：创建存档策略以启用或禁用特定网站或用户的内部或外部通信的存档
description: Lync Server 2013：创建存档策略以启用或禁用特定网站或用户的内部或外部通信的存档。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431986"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a>在 Lync Server 2013 中创建存档策略，以启用或禁用特定网站或用户的内部或外部通信的存档

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
> 若要控制存档的实现，必须指定存档配置中的选项，例如，是存档 IM 还是会议、使用关键模式和清除选项。 默认情况下，全局存档配置或任何网站或池存档配置中均未启用任何选项。 应在存档配置中指定所有适当的选项，然后才能在存档策略中启用内部或外部通信的存档。 有关详细信息，请参阅在 <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Lync Server 2013 中为你的组织、网站和池在操作文档中管理存档配置选项</A> 。<BR>如果为你的部署启用了 Microsoft Exchange 集成，Exchange 策略将控制是否为托管于 Exchange 2013 的用户启用存档，并将其邮箱置于 In-Place 保留。 有关详细信息，请参阅在部署文档中 <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">使用 Exchange Server 集成时在 Lync Server 2013 中设置存档策略</A> 。



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a>为网站或用户创建存档策略

1.  使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。

2.  打开一个浏览器窗口，然后输入 "管理员" URL 以打开 Lync Server "控制面板"。 有关可用于启动 Lync Server "控制面板" 的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。

3.  在左侧导航栏中，单击“监控和存档”，然后单击“存档策略”。

4.  单击“**新建**”，然后执行以下操作之一：
    
      - 若要创建网站级别的存档策略，请单击 " **网站策略** "，然后在 " **选择网站**" 中，单击要应用策略的网站。
    
      - 若要创建用户级别的存档策略，请单击“**用户策略**”。

5.  在“**新建存档策略**”中，执行下列操作：
    
      - 在“**名称**”中，指定新策略的名称（例如，externalContoso）。
    
      - 在“**说明**”中，提供有关该策略内容的详细信息（例如，Contoso 的外部用户存档策略）。
    
      - 要控制内部用户通信的存档，请选中或清除“**存档内部通信**”复选框。
    
      - 要控制外部用户通信的存档，请选中或清除“**存档外部通信**”复选框。

6.  单击“**提交**”。
    
    <div>
    

    > [!IMPORTANT]
    > 用户策略的设置仅适用于要应用该策略的特定用户和用户组。 有关详细信息，请参阅 <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">将存档策略应用于 Lync Server 2013 中的用户</A>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a>使用 Windows PowerShell Cmdlet 创建存档策略

可以使用 Windows PowerShell 和 **CsArchivingPolicy** cmdlet 创建存档策略。 此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。 有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a>在网站范围内创建新的存档策略

  - 此命令可为 Redmond 站点创建新的存档策略：
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a>在每用户范围内创建新的存档策略

  - 若要在每用户范围内创建新的存档策略，只需在创建策略时指定唯一标识：
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a>要创建允许对内部通信会话进行存档的新存档策略

  - 由于前面的命令中未指定参数（必需的 Identity 参数之外），因此新策略将对其所有属性使用默认值。 若要创建使用其他属性值的策略，只需包括适当的参数和参数值。 例如，若要创建允许存档内部即时消息会话的存档策略，请使用如下所示的命令：
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a>要创建允许对内部和外部通信会话进行存档的新存档策略

  - 可通过包含多个参数来修改多个属性值。 例如，此命令将配置新策略以存档内部和外部即时消息会话：
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

有关详细信息，请参阅 [CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet 的帮助主题。

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

