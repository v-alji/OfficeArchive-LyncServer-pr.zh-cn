---
title: Lync Server 2013： (CDR) 中调用详细录制
description: Lync Server 2013： (CDR) 中调用详细信息录制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call detail recording (CDR)
ms:assetid: 67726075-c77c-4191-a64f-a1cf5c7bcbb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688079(v=OCS.15)
ms:contentKeyID: 49733675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 590f99fd0b8649ffb3c4df039488dc54a8f3b7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435773"
---
# <a name="call-detail-recording-cdr-in-lync-server-2013"></a><span data-ttu-id="bbbbb-103"> (Lync Server 2013 中的 CDR) 呼叫详细记录</span><span class="sxs-lookup"><span data-stu-id="bbbbb-103">Call detail recording (CDR) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bbbbb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bbbbb-104">

<span> </span></span></span>

<span data-ttu-id="bbbbb-105">_**主题上次修改时间：** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="bbbbb-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="bbbbb-106">呼叫详细信息记录 (CDR) 记录了有关对等活动（包括即时消息、IP 语音 (VoIP) 呼叫、应用程序共享、文件传输和会议）的使用和诊断信息。</span><span class="sxs-lookup"><span data-stu-id="bbbbb-106">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities, including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings.</span></span> <span data-ttu-id="bbbbb-107">使用数据可以用于计算投资回报率 (ROI)，诊断数据可以用于解决对等活动和会议中遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="bbbbb-107">The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span> <span data-ttu-id="bbbbb-108">安装 Lync Server 2013 时，你还将安装用于 CDR 的全局配置设置的预定义集合。</span><span class="sxs-lookup"><span data-stu-id="bbbbb-108">When you install Lync Server 2013, you will also install a predefined collection of global configuration settings for CDR.</span></span> <span data-ttu-id="bbbbb-109">使用本节中的过程可配置 CDR。</span><span class="sxs-lookup"><span data-stu-id="bbbbb-109">Use the topics in this section to configure CDR.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bbbbb-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="bbbbb-110">In This Section</span></span>

  - [<span data-ttu-id="bbbbb-111">查看 Lync Server 2013 中的 CDR 配置信息</span><span class="sxs-lookup"><span data-stu-id="bbbbb-111">View CDR configuration information in Lync Server 2013</span></span>](lync-server-2013-view-cdr-configuration-information.md)

  - [<span data-ttu-id="bbbbb-112">在 Lync Server 2013 中启用呼叫详细记录</span><span class="sxs-lookup"><span data-stu-id="bbbbb-112">Enable call detail recording in Lync Server 2013</span></span>](lync-server-2013-enable-call-detail-recording.md)

  - [<span data-ttu-id="bbbbb-113">在 Lync Server 2013 中创建或修改 CDR 配置设置的集合</span><span class="sxs-lookup"><span data-stu-id="bbbbb-113">Create or modify a collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="bbbbb-114">删除 Lync Server 2013 中的现有 CDR 配置设置集合</span><span class="sxs-lookup"><span data-stu-id="bbbbb-114">Delete an existing collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="bbbbb-115">在 Lync Server 2013 中手动清除 "呼叫详细信息记录" 和 "体验质量" 数据库</span><span class="sxs-lookup"><span data-stu-id="bbbbb-115">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>](lync-server-2013-manually-purging-the-call-detail-recording-and-quality-of-experience-databases.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bbbbb-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bbbbb-116">See Also</span></span>


[<span data-ttu-id="bbbbb-117">在 Lync Server 2013 中配置 "呼叫详细记录" 和 "体验质量" 设置</span><span class="sxs-lookup"><span data-stu-id="bbbbb-117">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md)  
  

<span data-ttu-id="bbbbb-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bbbbb-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

