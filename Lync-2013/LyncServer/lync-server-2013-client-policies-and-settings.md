---
title: Lync Server 2013：客户端策略和设置
description: Lync Server 2013：客户端策略和设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client policies and settings
ms:assetid: c3ee47c0-7e20-47ec-809a-f4502d939586
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412966(v=OCS.15)
ms:contentKeyID: 48185330
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 608eefe293942c978270a7841fdd3a8f88876d1a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434863"
---
# <a name="client-policies-and-settings-in-lync-server-2013"></a><span data-ttu-id="7e522-103">Lync Server 2013 中的客户端策略和设置</span><span class="sxs-lookup"><span data-stu-id="7e522-103">Client policies and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7e522-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7e522-104">

<span> </span></span></span>

<span data-ttu-id="7e522-105">_**主题上次修改时间：** 2012-06-18_</span><span class="sxs-lookup"><span data-stu-id="7e522-105">_**Topic Last Modified:** 2012-06-18_</span></span>

<span data-ttu-id="7e522-106">本主题概述了可在 Lync Server 2013 中配置的客户端相关设置和策略。</span><span class="sxs-lookup"><span data-stu-id="7e522-106">This topic provides an overview of the client-related settings and policies that you can configure in Lync Server 2013.</span></span> <span data-ttu-id="7e522-107">Lync Server 2013 包括以下用于管理和配置客户端的工具：</span><span class="sxs-lookup"><span data-stu-id="7e522-107">Lync Server 2013 includes the following tools for managing and configuring clients:</span></span>

  - <span data-ttu-id="7e522-108">**Lync Server 2013 控制面板**   用于管理和配置服务器、用户、客户端和设备的基于 web 的图形用户界面。</span><span class="sxs-lookup"><span data-stu-id="7e522-108">**Lync Server 2013 Control Panel**   A web-based graphical user interface for managing and configuring servers, users, clients, and devices.</span></span>

  - <span data-ttu-id="7e522-109">**Lync Server 命令行管理**   程序  具有一组丰富的 Windows PowerShell 命令行界面 cmdlet 和若干预定义脚本的管理界面。</span><span class="sxs-lookup"><span data-stu-id="7e522-109">**Lync Server Management Shell**   A management interface with a rich set of Windows PowerShell command-line interface cmdlets and a number of pre-defined scripts.</span></span>

  - <span data-ttu-id="7e522-110">**Lync 2013 组策略**    可使用 Office 组策略管理模板为客户端配置的一组策略。</span><span class="sxs-lookup"><span data-stu-id="7e522-110">**Lync 2013 Group Policy**    A set of policies that you can configure for clients by using the Office Group Policy Administrative Template.</span></span> <span data-ttu-id="7e522-111">必须先配置某些客户端引导策略，然后才能部署 Lync 2013 客户端。</span><span class="sxs-lookup"><span data-stu-id="7e522-111">Certain client bootstrapping policies must be configured before you deploy Lync 2013 clients.</span></span> <span data-ttu-id="7e522-112">Lync 2010 中的其他可选设置继续在 Lync 2013 中生效。</span><span class="sxs-lookup"><span data-stu-id="7e522-112">Other optional settings from Lync 2010 continue to be honored in Lync 2013.</span></span>

<span data-ttu-id="7e522-113">本部分介绍了对 Lync Server 2013 中的客户端相关设置的更改。</span><span class="sxs-lookup"><span data-stu-id="7e522-113">This section describes changes to client-related settings in Lync Server 2013.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7e522-114">本部分内容</span><span class="sxs-lookup"><span data-stu-id="7e522-114">In this Section</span></span>

  - <span></span>  
    [<span data-ttu-id="7e522-115">Lync 2013 的新增和更改的设置</span><span class="sxs-lookup"><span data-stu-id="7e522-115">New and changed settings for Lync 2013</span></span>](lync-server-2013-new-and-changed-settings-for-lync-2013.md)

  - <span></span>  
    [<span data-ttu-id="7e522-116">Lync 2013 的组策略设置</span><span class="sxs-lookup"><span data-stu-id="7e522-116">Group Policy settings for Lync 2013</span></span>](lync-server-2013-group-policy-settings-for-lync-2013.md)

<span data-ttu-id="7e522-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7e522-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

