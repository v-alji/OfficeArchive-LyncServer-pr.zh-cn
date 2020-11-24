---
title: Lync Server 2013：呼叫寄存使用的组件
description: Lync Server 2013：由呼叫寄存使用的组件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391944"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a><span data-ttu-id="3e526-103">Lync Server 2013 中呼叫寄存使用的组件</span><span class="sxs-lookup"><span data-stu-id="3e526-103">Components used by Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e526-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e526-104">

<span> </span></span></span>

<span data-ttu-id="3e526-105">_**主题上次修改时间：** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="3e526-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="3e526-106">部署企业语音时，将自动安装呼叫寄存应用程序。</span><span class="sxs-lookup"><span data-stu-id="3e526-106">The Call Park application is automatically installed when you deploy Enterprise Voice.</span></span> <span data-ttu-id="3e526-107">通过配置语音策略启用呼叫寄存。</span><span class="sxs-lookup"><span data-stu-id="3e526-107">You enable Call Park by configuring voice policy.</span></span> <span data-ttu-id="3e526-108">以下 Lync Server 2013 组件支持调用寄存应用程序：</span><span class="sxs-lookup"><span data-stu-id="3e526-108">The following Lync Server 2013 components support the Call Park application:</span></span>

  - <span data-ttu-id="3e526-109">**应用程序服务**   应用程序服务提供了用于部署、托管和管理统一通信应用程序（如呼叫驻留应用程序）的平台。</span><span class="sxs-lookup"><span data-stu-id="3e526-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="3e526-110">应用程序服务将自动安装在前端池和每个标准版服务器上的每个前端服务器上。</span><span class="sxs-lookup"><span data-stu-id="3e526-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="3e526-111">**呼叫寄存应用程序**   调用寄存应用程序是由应用程序服务托管的统一通信应用程序之一。</span><span class="sxs-lookup"><span data-stu-id="3e526-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="3e526-112">当您部署企业语音时，它会自动包括在内。</span><span class="sxs-lookup"><span data-stu-id="3e526-112">It is included automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="3e526-113">呼叫公园公园和检索呼叫，并管理呼叫寄存的轨道式。</span><span class="sxs-lookup"><span data-stu-id="3e526-113">Call Park parks and retrieves calls and manages call park orbits.</span></span>

  - <span data-ttu-id="3e526-114">**音乐保留-文件**   如果启用了音乐，则会在呼叫暂停时播放音乐文件。</span><span class="sxs-lookup"><span data-stu-id="3e526-114">**Music-on hold-file**   If music in enabled, the music file is played while a call is parked.</span></span> <span data-ttu-id="3e526-115">安装呼叫寄存应用程序时，将包含默认音乐文件。</span><span class="sxs-lookup"><span data-stu-id="3e526-115">A default music file is included when the Call Park application is installed.</span></span>

  - <span data-ttu-id="3e526-116">**文件存储**   呼叫驻留应用程序使用文件存储来保存自定义音频文件。</span><span class="sxs-lookup"><span data-stu-id="3e526-116">**File Store**   The Call Park application uses File Store to hold custom audio files.</span></span>

  - <span data-ttu-id="3e526-117">**Lync Server "控制面板"**   您可以使用 Lync Server 控制面板配置 "呼叫寄存轨道" 表，并为用户启用呼叫寄存。</span><span class="sxs-lookup"><span data-stu-id="3e526-117">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the call park orbit table and to enable Call Park for users.</span></span>

  - <span data-ttu-id="3e526-118">**Lync Server 命令行管理**   程序  可以使用 Lync Server Management Shell cmdlet 执行所有呼叫寄存应用程序配置。</span><span class="sxs-lookup"><span data-stu-id="3e526-118">**Lync Server Management Shell**   All Call Park application configuration can be performed by using Lync Server Management Shell cmdlets.</span></span>

<span data-ttu-id="3e526-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e526-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

