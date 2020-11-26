---
title: Lync Server 2013：在全局级别配置存档选项
description: Lync Server 2013：在全局级别配置存档选项。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options at the global level
ms:assetid: bfe415f7-2abf-41ee-a1cb-cf48b2d59c0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205233(v=OCS.15)
ms:contentKeyID: 48185303
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44b8939ec95d00afa2aa7632f4555bc6fef89834
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433337"
---
# <a name="configuring-archiving-options-at-the-global-level-in-lync-server-2013"></a><span data-ttu-id="a5d9e-103">在 Lync Server 2013 的全局级别配置存档选项</span><span class="sxs-lookup"><span data-stu-id="a5d9e-103">Configuring Archiving options at the global level in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5d9e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5d9e-104">

<span> </span></span></span>

<span data-ttu-id="a5d9e-105">_**主题上次修改时间：** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="a5d9e-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="a5d9e-106">将存档添加到拓扑并发布拓扑时，Lync Server 将为存档创建全局配置。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-106">When you add Archiving to your topology and publish the topology, Lync Server creates a global configuration for Archiving.</span></span> <span data-ttu-id="a5d9e-107">默认情况下，全局配置中不启用任何存档选项。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-107">By default, no Archiving options are enabled in the global configuration.</span></span> <span data-ttu-id="a5d9e-108">除非您自己设置站点或池配置（这将重写全局配置），否则全局配置将控制要为整个部署启用的选项。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-108">The global configuration controls which options are enabled for your entire deployment, unless you set up site or pool configurations, which override the global configuration.</span></span>

<span data-ttu-id="a5d9e-109">有关存档配置的工作原理的详细信息（包括全局、网站和池配置的层次结构），请参阅规划文档、部署文档或操作文档中的 [存档在 Lync Server 2013 中的工作原理](lync-server-2013-how-archiving-works.md) 。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-109">For details about how Archiving configurations work, including the hierarchy for global, site, and pool configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a5d9e-110">在启用存档之前，应在存档配置中指定所有适当的选项。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span>



</div>

<div>

## <a name="to-configure-archiving-options-at-the-global-level"></a><span data-ttu-id="a5d9e-111">在全局级别配置存档选项</span><span class="sxs-lookup"><span data-stu-id="a5d9e-111">To configure archiving options at the global level</span></span>

1.  <span data-ttu-id="a5d9e-112">使用分配给 CsArchivingAdministrator 或 CsAdministrator 角色的用户帐户，登录到内部部署中的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a5d9e-113">打开一个浏览器窗口，然后输入管理员 URL 以打开 Lync Server 2013 控制面板。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-113">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="a5d9e-114">有关可用于启动 Lync Server 2013 控制面板的不同方法的详细信息，请参阅 [打开 Lync server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-114">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a5d9e-115">在左侧导航栏中，单击“监控和存档”，然后单击“存档配置”。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="a5d9e-116">在“**存档配置**”页上，单击“**全局**”，再单击“**编辑**”，然后单击“**显示详细信息**”。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-116">On the **Archiving Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="a5d9e-117">在“**编辑存档设置 - 全局**”的“**存档设置**”下拉列表中，选择下列存档选项之一：</span><span class="sxs-lookup"><span data-stu-id="a5d9e-117">In **Edit Archiving Setting - Global**, in the **Archiving setting** drop-down list, select one of the following archiving options:</span></span>
    
      - <span data-ttu-id="a5d9e-118">**禁用存档**</span><span class="sxs-lookup"><span data-stu-id="a5d9e-118">**Disable archiving**</span></span>
    
      - <span data-ttu-id="a5d9e-119">**存档 IM 会话**</span><span class="sxs-lookup"><span data-stu-id="a5d9e-119">**Archive IM sessions**</span></span>
    
      - <span data-ttu-id="a5d9e-120">**存档 IM 和 Web 会议会话**</span><span class="sxs-lookup"><span data-stu-id="a5d9e-120">**Archive IM and web conferencing sessions**</span></span>

6.  <span data-ttu-id="a5d9e-121">另请在“**编辑存档设置 - 全局**”页中，执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="a5d9e-121">Also on the **Edit Archiving Setting – Global** page, do the following:</span></span>
    
      - <span data-ttu-id="a5d9e-122">要在存档不可用时阻止活动，请选中“**存档失败时阻止即时消息 (IM) 或 Web 会议会话**”复选框。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-122">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="a5d9e-123">若要使用 Microsoft Exchange Server 存储存档数据，请单击 " **Microsoft exchange 集成** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-123">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="a5d9e-124">若要启用数据清除，请选中“**启用存档数据清除**”复选框，然后执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="a5d9e-124">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="a5d9e-125">要指定在特定的天数之后清除，请单击“**在最长期限（天）后清除导出的存档数据和存储的存档数据**”，然后指定天数。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-125">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="a5d9e-126">要限制仅清除已导出的存档数据，请单击“**仅清除导出的存档数据**”。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-126">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

7.  <span data-ttu-id="a5d9e-127">单击“**提交**”。</span><span class="sxs-lookup"><span data-stu-id="a5d9e-127">Click **Commit**.</span></span>

<span data-ttu-id="a5d9e-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5d9e-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

