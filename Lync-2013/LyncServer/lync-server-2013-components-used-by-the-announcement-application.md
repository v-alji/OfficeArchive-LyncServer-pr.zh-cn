---
title: Lync Server 2013：通知应用程序使用的组件
description: Lync Server 2013：公告应用程序使用的组件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by the Announcement application
ms:assetid: 7b1a0281-cf31-459d-a734-5f10a129089c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398608(v=OCS.15)
ms:contentKeyID: 48184595
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5338ad097c814d5c6435bd89dbf7cfa8680feb8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391942"
---
# <a name="components-used-by-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="ffc75-103">Lync Server 2013 中的通知应用程序使用的组件</span><span class="sxs-lookup"><span data-stu-id="ffc75-103">Components used by the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffc75-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffc75-104">

<span> </span></span></span>

<span data-ttu-id="ffc75-105">_**主题上次修改时间：** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="ffc75-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="ffc75-106">在 Lync Server 2013 中，公告应用程序是响应组应用程序的一个组件。</span><span class="sxs-lookup"><span data-stu-id="ffc75-106">In Lync Server 2013, the Announcement application is a component of the Response Group application.</span></span> <span data-ttu-id="ffc75-107">部署企业语音时，将自动安装通知应用程序并与响应组应用程序一起激活。</span><span class="sxs-lookup"><span data-stu-id="ffc75-107">When you deploy Enterprise Voice, the Announcement application is automatically installed and activated along with the Response Group application.</span></span> <span data-ttu-id="ffc75-108">本部分介绍支持公告应用程序的组件。</span><span class="sxs-lookup"><span data-stu-id="ffc75-108">This section describes the components that support the Announcement application.</span></span>

<div>

## <a name="announcement-application-components"></a><span data-ttu-id="ffc75-109">公告应用程序组件</span><span class="sxs-lookup"><span data-stu-id="ffc75-109">Announcement Application Components</span></span>

<span data-ttu-id="ffc75-110">以下 Lync Server 组件支持公告应用程序：</span><span class="sxs-lookup"><span data-stu-id="ffc75-110">The following Lync Server components support the Announcement application:</span></span>

  - <span data-ttu-id="ffc75-111">**应用程序服务**   应用程序服务提供了用于部署、托管和管理统一通信应用程序的平台。</span><span class="sxs-lookup"><span data-stu-id="ffc75-111">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications.</span></span> <span data-ttu-id="ffc75-112">应用程序服务将自动安装在前端池和每个标准版服务器上的每个前端服务器上。</span><span class="sxs-lookup"><span data-stu-id="ffc75-112">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="ffc75-113">**响应组应用程序**   响应组应用程序是由应用程序服务托管的统一通信应用程序之一。</span><span class="sxs-lookup"><span data-stu-id="ffc75-113">**Response Group application**   The Response Group application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="ffc75-114">如果将未分配的电话号码范围配置为路由到公告，则需要响应组应用程序来路由对电话号码的呼叫。</span><span class="sxs-lookup"><span data-stu-id="ffc75-114">When an unassigned phone number range is configured to route to an announcement, the Response Group application is required to route the calls made to the phone number.</span></span> <span data-ttu-id="ffc75-115">如果所有范围都配置为路由到 Exchange 统一消息 (UM) ，则不需要 (响应组应用程序。 ) </span><span class="sxs-lookup"><span data-stu-id="ffc75-115">(Response Group application is not required if all the ranges are configured to route to Exchange Unified Messaging (UM).)</span></span>

  - <span data-ttu-id="ffc75-116">**音频文件**   音频文件用于公告。</span><span class="sxs-lookup"><span data-stu-id="ffc75-116">**Audio files**   Audio files are used for the announcements.</span></span>

  - <span data-ttu-id="ffc75-117">**文件存储**   "通知" 应用程序使用文件存储来存储其音频文件。</span><span class="sxs-lookup"><span data-stu-id="ffc75-117">**File Store**   The Announcement application uses File Store to store its audio files.</span></span>

  - <span data-ttu-id="ffc75-118">**Lync Server "控制面板"**   可以使用 Lync Server "控制面板" 配置 "未分配的号码" 表。</span><span class="sxs-lookup"><span data-stu-id="ffc75-118">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the unassigned number table.</span></span>

  - <span data-ttu-id="ffc75-119">**Lync Server 命令行管理**   程序  你可以使用 Lync Server Management Shell cmdlet 配置公告设置和 "未分配的号码" 表。</span><span class="sxs-lookup"><span data-stu-id="ffc75-119">**Lync Server Management Shell**   You can use Lync Server Management Shell cmdlets to configure Announcement settings and the unassigned number table.</span></span>

<span data-ttu-id="ffc75-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffc75-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

