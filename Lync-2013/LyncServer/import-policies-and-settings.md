---
title: 导入策略和设置
description: 导入策略和设置。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Import policies and settings
ms:assetid: b25decee-2ee5-4836-b370-454411d39252
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205178(v=OCS.15)
ms:contentKeyID: 48185147
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e014b7e8f0498742104118eec9eb313394ae6a94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439602"
---
# <a name="import-policies-and-settings"></a><span data-ttu-id="dd820-103">导入策略和设置</span><span class="sxs-lookup"><span data-stu-id="dd820-103">Import policies and settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd820-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd820-104">

<span> </span></span></span>

<span data-ttu-id="dd820-105">_**主题上次修改时间：** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="dd820-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="dd820-106">将 Office 通信服务器 2007 R2 拓扑信息与 Lync Server 2013 试验池合并后，您需要运行 Lync Server 2013 Management Shell cmdlet 将 Office 通信服务器 2007 R2 策略和配置设置迁移到 Lync Server 2013 试验池。</span><span class="sxs-lookup"><span data-stu-id="dd820-106">After you merge your Office Communications Server 2007 R2 topology information with your Lync Server 2013 pilot pool, you need to run a Lync Server 2013 Management Shell cmdlet to migrate your Office Communications Server 2007 R2 policies and configuration settings to your Lync Server 2013 pilot pool.</span></span>

<span data-ttu-id="dd820-107">**CsLegacyConfiguration** cmdlet 将策略、语音路由、拨号计划、Communicator Web Access url 和电话拨入访问号码导入 Lync Server 2013。</span><span class="sxs-lookup"><span data-stu-id="dd820-107">The **Import-CsLegacyConfiguration** cmdlet imports policies, voice routes, dial plans, Communicator Web Access URLs, and dial-in access numbers to Lync Server 2013.</span></span>

<div>

## <a name="to-migrate-policies-and-settings"></a><span data-ttu-id="dd820-108">迁移策略和设置</span><span class="sxs-lookup"><span data-stu-id="dd820-108">To migrate policies and settings</span></span>

1.  <span data-ttu-id="dd820-109">在 Lync Server 2013 前端服务器上，启动 Lync Server 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="dd820-109">On the Lync Server 2013 Front End server, start the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="dd820-110">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="dd820-110">At the command line, type the following:</span></span>
    
        Import-CsLegacyConfiguration
    
    <span data-ttu-id="dd820-111">导入策略后，请使用下面的过程在 Lync Server 控制面板中查看导入的策略。</span><span class="sxs-lookup"><span data-stu-id="dd820-111">After the policies are imported, use the procedure that follows to see the imported policies in the Lync Server Control Panel .</span></span>

</div>

<div>

## <a name="to-view-imported-policies"></a><span data-ttu-id="dd820-112">查看导入的策略</span><span class="sxs-lookup"><span data-stu-id="dd820-112">To view imported policies</span></span>

1.  <span data-ttu-id="dd820-113">打开 "Lync Server 2013 控制面板"。</span><span class="sxs-lookup"><span data-stu-id="dd820-113">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="dd820-114">单击 " **语音路由** "，然后查看导入的策略。</span><span class="sxs-lookup"><span data-stu-id="dd820-114">Click **Voice Routing** and view the imported policies.</span></span>

3.  <span data-ttu-id="dd820-115">单击 " **会议** " 并查看导入的策略。</span><span class="sxs-lookup"><span data-stu-id="dd820-115">Click **Conferencing** and view the imported policies.</span></span>

4.  <span data-ttu-id="dd820-116">单击 " **联盟和外部访问** " 并查看导入的策略。</span><span class="sxs-lookup"><span data-stu-id="dd820-116">Click **Federation and External Access** and view the imported policies.</span></span>

5.  <span data-ttu-id="dd820-117">单击 " **监视和存档** "，然后查看导入的策略。</span><span class="sxs-lookup"><span data-stu-id="dd820-117">Click **Monitoring and Archiving** and view the imported policies.</span></span>

<span data-ttu-id="dd820-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd820-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

