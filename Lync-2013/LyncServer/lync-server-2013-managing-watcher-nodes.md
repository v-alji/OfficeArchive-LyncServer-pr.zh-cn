---
title: Lync Server 2013：管理观察程序节点
description: Lync Server 2013：管理观察程序节点。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing watcher nodes
ms:assetid: 66deaf49-a71f-4a6e-ada0-ea8b688ee921
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688078(v=OCS.15)
ms:contentKeyID: 49733674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1795b09bbca73d8157cf796ceeaaeafb9cc2ebc5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425827"
---
# <a name="managing-watcher-nodes-in-lync-server-2013"></a><span data-ttu-id="52446-103">在 Lync Server 2013 中管理观察程序节点</span><span class="sxs-lookup"><span data-stu-id="52446-103">Managing watcher nodes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52446-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52446-104">

<span> </span></span></span>

<span data-ttu-id="52446-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="52446-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="52446-106">除了修改在观察程序节点上执行的合成事务，管理员还可以使用 **CsWatcherNodeConfiguration** cmdlet 执行两个其他重要任务：启用和禁用 "观察程序" 节点，以及将观察程序节点配置为在运行其测试时使用内部 url 或外部 url。</span><span class="sxs-lookup"><span data-stu-id="52446-106">In addition to modifying the synthetic transactions that are executed on a watcher node, administrators can also use the **Set-CsWatcherNodeConfiguration** cmdlet to carry out two other important tasks: enabling and disabling the watcher node, and configuring the watcher node to use either internal URLs or external URLs when running its tests.</span></span>

<span data-ttu-id="52446-107">默认情况下，观察程序节点设计为定期运行其所有启用的合成事务。</span><span class="sxs-lookup"><span data-stu-id="52446-107">By default, watcher nodes are designed to periodically run all their enabled synthetic transactions.</span></span> <span data-ttu-id="52446-108">但是，有时可能需要暂停这些交易。</span><span class="sxs-lookup"><span data-stu-id="52446-108">Sometimes, however, you may need to suspend those transactions.</span></span> <span data-ttu-id="52446-109">例如，如果观察程序节点暂时与网络断开连接，则没有理由运行合成事务。</span><span class="sxs-lookup"><span data-stu-id="52446-109">For example, if the watcher node is temporarily disconnected from the network, then there is no reason to run the synthetic transactions.</span></span> <span data-ttu-id="52446-110">如果没有网络连接，这些事务将保证失败。</span><span class="sxs-lookup"><span data-stu-id="52446-110">Without network connectivity, those transactions are guaranteed to fail.</span></span> <span data-ttu-id="52446-111">如果要临时禁用观察程序节点，请从 Lync Server Management Shell 运行类似下面的命令：</span><span class="sxs-lookup"><span data-stu-id="52446-111">If you want to temporarily disable a watcher node, run a command similar to this from the Lync Server Management Shell:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -Enabled $False

<span data-ttu-id="52446-112">此命令将禁用观察程序节点 atl-观察程序-001.litwareinc.com 上的合成事务的执行。</span><span class="sxs-lookup"><span data-stu-id="52446-112">This command will disable the execution of synthetic transactions on the watcher node atl-watcher- 001.litwareinc.com.</span></span> <span data-ttu-id="52446-113">若要恢复合成事务的执行，请将 Enabled 属性设置回 True ($True) ：</span><span class="sxs-lookup"><span data-stu-id="52446-113">To resume execution of the synthetic transactions, set the Enabled property back to True ($True):</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -Enabled $True

<div>


> [!NOTE]  
> <span data-ttu-id="52446-114">Enabled 属性可用于打开或关闭观察程序节点。</span><span class="sxs-lookup"><span data-stu-id="52446-114">The Enabled property can be used to turn watcher nodes on or off.</span></span> <span data-ttu-id="52446-115">如果要永久删除观察程序节点，请使用 <STRONG>CsWatcherNodeConfiguration</STRONG> cmdlet：</span><span class="sxs-lookup"><span data-stu-id="52446-115">If you want to permanently delete a watcher node, use the <STRONG>Remove-CsWatcherNodeConfiguration</STRONG> cmdlet:</span></span><BR><span data-ttu-id="52446-116">Remove-CsWatcherNodeConfiguration-身份 "atl-watcher-001.litwareinc.com"</span><span class="sxs-lookup"><span data-stu-id="52446-116">Remove-CsWatcherNodeConfiguration –Identity "atl-watcher-001.litwareinc.com"</span></span><BR><span data-ttu-id="52446-117">该命令将从指定的计算机中删除所有观察程序节点配置设置，这将阻止计算机自动运行合成事务。</span><span class="sxs-lookup"><span data-stu-id="52446-117">That command removes all the watcher node configuration settings from the specified computer, which prevents the computer from automatically running synthetic transactions.</span></span> <span data-ttu-id="52446-118">但是，该命令不会卸载 System Center agent 文件或 Lync Server 2013 系统文件。</span><span class="sxs-lookup"><span data-stu-id="52446-118">However, the command does not uninstall the System Center agent files or the Lync Server 2013 system files.</span></span>



</div>

<span data-ttu-id="52446-119">默认情况下，观察程序节点在进行测试时使用组织的外部 Url。</span><span class="sxs-lookup"><span data-stu-id="52446-119">By default, watcher nodes use an organization's external URLs when conducting their tests.</span></span> <span data-ttu-id="52446-120">但是，观察程序节点也可以配置为使用组织的内部 Url。</span><span class="sxs-lookup"><span data-stu-id="52446-120">However, watcher nodes can also be configured to use the organization's internal URLs.</span></span> <span data-ttu-id="52446-121">这使管理员能够验证位于外围网络内的用户的 URL 访问。</span><span class="sxs-lookup"><span data-stu-id="52446-121">This enables administrators to verify URL access for users located inside the perimeter network.</span></span> <span data-ttu-id="52446-122">若要将观察程序节点配置为使用内部 Url 而不是外部 Url，请将 UseInternalWebUrls 属性设置为 True ($True) ：</span><span class="sxs-lookup"><span data-stu-id="52446-122">To configure a watcher node to use internal URLs instead of external URLs, set the UseInternalWebUrls property to True ($True):</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -UseInternalWebUrls $True

<span data-ttu-id="52446-123">如果将此属性重置为默认值 False ($False) ，则观察程序将使用外部 Url：</span><span class="sxs-lookup"><span data-stu-id="52446-123">If you reset this property to the default value of False ($False), the watcher will then use the external URLs:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-watcher-001.litwareinc.com" -UseInternalWebUrls $False

<span data-ttu-id="52446-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52446-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

