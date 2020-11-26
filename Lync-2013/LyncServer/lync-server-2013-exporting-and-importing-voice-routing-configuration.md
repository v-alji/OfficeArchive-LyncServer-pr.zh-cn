---
title: Lync Server 2013：导出和导入语音路由配置
description: Lync Server 2013：导出和导入 "语音路由配置"。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting and importing voice routing configuration
ms:assetid: c9b78622-5725-43b0-9ee1-5b82b1e1c8eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398836(v=OCS.15)
ms:contentKeyID: 48185398
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a94a9c02672debae9f5b30e3a1a96856050d6ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428354"
---
# <a name="exporting-and-importing-voice-routing-configuration-in-lync-server-2013"></a><span data-ttu-id="8ff00-103">在 Lync Server 2013 中导出和导入语音路由配置</span><span class="sxs-lookup"><span data-stu-id="8ff00-103">Exporting and importing voice routing configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ff00-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ff00-104">

<span> </span></span></span>

<span data-ttu-id="8ff00-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8ff00-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8ff00-106">如果要在不发布的情况下保存语音路由配置，请按照以下步骤使用 Lync Server 控制面板配置导出和导入命令来保存和检索你的语音路由配置的快照。</span><span class="sxs-lookup"><span data-stu-id="8ff00-106">If you want to save your voice routing configuration without publishing it, follow these steps to use the Lync Server Control Panel configuration export and import commands to save and retrieve a snapshot of your voice routing configuration.</span></span> <span data-ttu-id="8ff00-107">当您导入 "语音路由配置" 文件 () ，但在此期间对服务器上的语音路由配置进行了更改，则 Lync Server 控制面板中的 " **语音路由** " 组中的页面将指示有未提交的语音路由更改。</span><span class="sxs-lookup"><span data-stu-id="8ff00-107">When you import a voice routing configuration file (.vcfg), but changes have been made to the voice routing configuration on the server in the meantime, the pages in the **Voice Routing** group in Lync Server Control Panel will indicate that there are uncommitted changes to voice routing.</span></span> <span data-ttu-id="8ff00-108">这些未提交的更改是两种需要调节的配置之间的差异。</span><span class="sxs-lookup"><span data-stu-id="8ff00-108">Those uncommitted changes are the differences between the two configurations that require reconciliation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8ff00-109">如果你对 " <STRONG>语音路由</STRONG> " 组内任何页面上的设置进行了任何未提交的更改，则所做的更改将保存在导出的语音配置文件中 ( vcfg) 。</span><span class="sxs-lookup"><span data-stu-id="8ff00-109">If you have made any uncommitted changes to the settings on any page within the <STRONG>Voice Routing</STRONG> group, the changes are saved in the exported voice configuration file (.vcfg).</span></span> <span data-ttu-id="8ff00-110">这使你可以在发布更改之前，在多个 Lync Server 控制面板会话期间进行语音路由配置更改。</span><span class="sxs-lookup"><span data-stu-id="8ff00-110">This enables you to make voice routing configuration changes during multiple Lync Server Control Panel sessions before you publish the changes.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8ff00-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="8ff00-111">In This Section</span></span>

  - [<span data-ttu-id="8ff00-112">在 Lync Server 2013 中导出语音路由配置文件</span><span class="sxs-lookup"><span data-stu-id="8ff00-112">Export a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-export-a-voice-route-configuration-file.md)

  - [<span data-ttu-id="8ff00-113">在 Lync Server 2013 中导入语音路由配置文件</span><span class="sxs-lookup"><span data-stu-id="8ff00-113">Import a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-import-a-voice-route-configuration-file.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="8ff00-114">相关部分</span><span class="sxs-lookup"><span data-stu-id="8ff00-114">Related Sections</span></span>

<span data-ttu-id="8ff00-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ff00-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

