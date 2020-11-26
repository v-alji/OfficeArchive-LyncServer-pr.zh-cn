---
title: 迁移模拟设备
description: 迁移模拟设备。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63f7f92142fb6a3ced37cded1a223038ec1876d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443830"
---
# <a name="migrate-analog-devices"></a><span data-ttu-id="e89cf-103">迁移模拟设备</span><span class="sxs-lookup"><span data-stu-id="e89cf-103">Migrate analog devices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e89cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e89cf-104">

<span> </span></span></span>

<span data-ttu-id="e89cf-105">_**主题上次修改时间：** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="e89cf-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="e89cf-106">Lync 服务器提供模拟设备的支持。</span><span class="sxs-lookup"><span data-stu-id="e89cf-106">Lync Server provides support for analog devices.</span></span> <span data-ttu-id="e89cf-107">具体说来，受支持的模拟设备是模拟音频电话和模拟传真计算机。</span><span class="sxs-lookup"><span data-stu-id="e89cf-107">Specifically, the supported analog devices are analog audio phones and analog fax machines.</span></span> <span data-ttu-id="e89cf-108">你可以配置合格的网关以支持在 Lync Server 环境中使用模拟设备。</span><span class="sxs-lookup"><span data-stu-id="e89cf-108">You can configure the qualified gateways to support the use of analog devices in your Lync Server environment.</span></span> <span data-ttu-id="e89cf-109">从 Lync Server 2010 迁移到 Lync Server 2013 后，您还必须迁移与模拟设备相关联的联系人对象。</span><span class="sxs-lookup"><span data-stu-id="e89cf-109">After you migrate from Lync Server 2010 to Lync Server 2013, you must also migrate the contact objects associated with the analog devices.</span></span> <span data-ttu-id="e89cf-110">使用 Lync Server Management Shell 首先检索与 Lync Server 2010 模拟设备关联的所有联系人对象，然后将这些对象移动到 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="e89cf-110">Use Lync Server Management Shell to first retrieve all contact objects associated with the Lync Server 2010 analog devices, and then move those objects to the Lync Server 2013 pool.</span></span>

<div>

## <a name="to-migrate-analog-devices"></a><span data-ttu-id="e89cf-111">迁移模拟设备</span><span class="sxs-lookup"><span data-stu-id="e89cf-111">To migrate analog devices</span></span>

1.  <span data-ttu-id="e89cf-112">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="e89cf-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="e89cf-113">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e89cf-113">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  <span data-ttu-id="e89cf-114">验证是否已将所有联系人对象移动到 Lync Server 2013 池。</span><span class="sxs-lookup"><span data-stu-id="e89cf-114">Verify that all contact objects have been moved to the Lync Server 2013 pool.</span></span> <span data-ttu-id="e89cf-115">在命令行中键入：</span><span class="sxs-lookup"><span data-stu-id="e89cf-115">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  <span data-ttu-id="e89cf-116">验证所有联系人对象现在是否与 Lync Server 2013 池相关联。</span><span class="sxs-lookup"><span data-stu-id="e89cf-116">Verify that all the contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="e89cf-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e89cf-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

