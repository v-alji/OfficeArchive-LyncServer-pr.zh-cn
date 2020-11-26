---
title: 删除现有 SIP 中继配置设置的集合
description: 删除 SIP 中继配置设置的现有集合。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of SIP trunk configuration settings
ms:assetid: 3b25f14d-884b-42dd-a866-460d276d3e43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688024(v=OCS.15)
ms:contentKeyID: 49733614
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98acede458d34eb30202d898414b2e17076d32d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430516"
---
# <a name="delete-an-existing-collection-of-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="1cfbf-103">删除 Lync Server 2013 中的现有 SIP 中继配置设置集合</span><span class="sxs-lookup"><span data-stu-id="1cfbf-103">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1cfbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1cfbf-104">

<span> </span></span></span>

<span data-ttu-id="1cfbf-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="1cfbf-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="1cfbf-106">SIP 中继配置设置在服务提供商处定义中介服务器与公共交换电话网络之间的关系和功能 (PSTN) 网关、IP 公共分支 exchange (PBX) 或会话边界控制器 (SBC) 。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="1cfbf-107">这些设置可执行如下所指定内容的操作：</span><span class="sxs-lookup"><span data-stu-id="1cfbf-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="1cfbf-108">是否在中继上启用媒体旁路功能。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="1cfbf-109">发送 RTCP) 数据包的实时传输控制协议 (的条件。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="1cfbf-110"> (SRTP 是否需要安全的实时协议) 加密在每个主干上都是必需的。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="1cfbf-111">安装 Microsoft Lync Server 2013 时，将为你创建一个全局 SIP 中继配置设置集合。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="1cfbf-112">此全局集合设置无法删除。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-112">This global collection of settings cannot be deleted.</span></span> <span data-ttu-id="1cfbf-113">但是，你可以使用 Lync Server 控制面板或 [new-cstrunkconfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet 将全局集合中的属性 "重置" 为其默认值。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-113">However, you can use the Lync Server Control Panel or the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet to "reset" the properties in the global collection to their default values.</span></span> <span data-ttu-id="1cfbf-114">例如，如果已将 Enable3pccRefer 属性设置为 True，则当您重置全局集合时，Enable3pccRefer 属性将还原为其默认值 False。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-114">For example, if you have set the Enable3pccRefer property to True, when you reset the global collection the Enable3pccRefer property will revert to its default value of False.</span></span>

<span data-ttu-id="1cfbf-p103">管理员还可以在站点作用域或服务作用域（针对单个 PSTN 网关）创建自定义中继配置设置；这些自定义设置可以删除。在删除这些自定义设置时，请注意以下事项：</span><span class="sxs-lookup"><span data-stu-id="1cfbf-p103">Administrators can also create custom trunk configuration settings at the site scope or at the service scope (for an individual PSTN gateway); these custom settings can be removed. When removing these custom settings keep the following in mind:</span></span>

  - <span data-ttu-id="1cfbf-p104">如果删除了服务作用域设置，由这些设置管理的 SIP 中继将由应用于这些站点的设置（如果存在）管理。如果站点设置不存在，这些中继随后会由中继配置设置的全局集合管理。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-p104">If you remove service scope settings, then the SIP trunk managed by those settings will be managed by the settings applied to their site, if they exist. If site settings do not exist, those trunks will then be managed by the global collection of trunk configuration settings.</span></span>

  - <span data-ttu-id="1cfbf-119">如果删除了站点作用域设置，由这些设置管理的任何 SIP 中继都将立即由中继配置设置的全局集合管理。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-119">If you remove site-scoped settings then any SIP trunks managed by those settings will now be managed by the global collection of trunk configuration settings.</span></span>

<div>

## <a name="to-remove-trunk-configuration-settings-with-lync-server-control-panel"></a><span data-ttu-id="1cfbf-120">通过 Lync Server 控制面板删除中继配置设置</span><span class="sxs-lookup"><span data-stu-id="1cfbf-120">To remove trunk configuration settings with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="1cfbf-121">在 "Lync Server 控制面板" 中，单击 " **语音路由** "，然后单击 " **中继配置**"。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-121">In Lync Server Control Panel, click **Voice Routing** and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="1cfbf-p105">在“Trunk 配置”选项卡上，选择要删除的 SIP 中继配置设置的集合，单击“编辑”，然后单击“删除”。若要在同一操作中删除多个集合，请单击第一个要删除的集合，然后按住 Ctrl 键并单击任何其他要删除的集合。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-p105">On the **Trunk Configuration** tab, select the collection of SIP trunk configuration settings to be deleted, click **Edit** and then click **Delete**. To delete multiple collections in the same operation, click the first collection to be deleted, then hold down the Ctrl key and click any additional collections that you want to remove.</span></span>

3.  <span data-ttu-id="1cfbf-p106">集合的“状态”属性将更新为“未提交”。若要提交更改和删除集合，请单击“提交”，然后单击“全部提交”。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-p106">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

4.  <span data-ttu-id="1cfbf-126">在“未提交的语音配置设置”对话框中，单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-126">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

5.  <span data-ttu-id="1cfbf-127">在 " **Microsoft Lync Server 2013 控制面板** " 对话框中，单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-127">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

6.  <span data-ttu-id="1cfbf-128">If you change your mind and decide not to delete the collection, click **Commit** and then click **Cancel All Uncommitted Changes**.</span><span class="sxs-lookup"><span data-stu-id="1cfbf-128">If you change your mind and decide not to delete the collection, click **Commit** and then click **Cancel All Uncommitted Changes**.</span></span> <span data-ttu-id="1cfbf-129">当显示 " **Microsoft Lync Server 2013 控制面板** " 对话框时，单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-129">When the **Microsoft Lync Server 2013 Control Panel** dialog box appears, click **OK**.</span></span>

</div>

<div>

## <a name="removing-trunk-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="1cfbf-130">使用 Windows PowerShell Cmdlet 删除中继配置设置</span><span class="sxs-lookup"><span data-stu-id="1cfbf-130">Removing Trunk Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="1cfbf-131">你可以使用 Windows PowerShell 和 **new-cstrunkconfiguration** cmdlet 删除中继配置设置。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-131">You can delete trunk configuration settings by using Windows PowerShell and the **Remove-CsTrunkConfiguration** cmdlet.</span></span> <span data-ttu-id="1cfbf-132">你可以从 Lync Server 2013 命令行管理程序或 Windows PowerShell 的远程会话运行此 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-132">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="1cfbf-133">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-settings"></a><span data-ttu-id="1cfbf-134">删除指定的设置集合</span><span class="sxs-lookup"><span data-stu-id="1cfbf-134">To remove a specified collection of settings</span></span>

  - <span data-ttu-id="1cfbf-135">以下命令将删除应用于 Redmond 站点的中继配置设置：</span><span class="sxs-lookup"><span data-stu-id="1cfbf-135">The following command removes the trunk configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsTrunkConfiguration -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-collections-applied-to-the-site-scope"></a><span data-ttu-id="1cfbf-136">删除适用于站点范围的所有集合</span><span class="sxs-lookup"><span data-stu-id="1cfbf-136">To remove all the collections applied to the site scope</span></span>

  - <span data-ttu-id="1cfbf-137">以下命令将删除应用于服务作用域的所有中继配置设置：</span><span class="sxs-lookup"><span data-stu-id="1cfbf-137">This command removes all the trunk configuration settings applied to the service scope:</span></span>
    
        Get-CsTrunkConfiguration -Filter "service:*" | Remove-CsTrunkConfiguration

</div>

<div>

## <a name="to-remove-all-the-collections-where-media-bypass-is-enabled"></a><span data-ttu-id="1cfbf-138">删除启用了媒体旁路的所有集合</span><span class="sxs-lookup"><span data-stu-id="1cfbf-138">To remove all the collections where media bypass is enabled</span></span>

  - <span data-ttu-id="1cfbf-139">以下命令将删除启用了媒体旁路的所有中继配置设置：</span><span class="sxs-lookup"><span data-stu-id="1cfbf-139">The following command removes all the trunk configuration settings where media bypass has been enabled:</span></span>
    
        Get-CsTrunkConfiguration | Where-Object {$_.EnableBypass -eq $True} | Remove-CsTrunkConfiguration

</div>

<span data-ttu-id="1cfbf-140">有关详细信息，请参阅 [new-cstrunkconfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="1cfbf-140">For more information, see the help topic for the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="1cfbf-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1cfbf-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

