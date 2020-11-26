---
title: Lync Server 2013：支持的虚拟化技术和已知限制
description: Lync Server 2013：支持的虚拟化技术和已知限制。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported virtualization technologies and known limitations
ms:assetid: 6d3d749d-e840-4c05-afae-d6e69e7616aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204982(v=OCS.15)
ms:contentKeyID: 48184428
ms.date: 02/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 745fa535462d29342f4c0a58674ee6487db42a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423559"
---
# <a name="supported-virtualization-technologies-and-known-limitations-in-lync-server-2013"></a><span data-ttu-id="ebf6b-103">Lync Server 2013 中支持的虚拟化技术和已知限制</span><span class="sxs-lookup"><span data-stu-id="ebf6b-103">Supported virtualization technologies and known limitations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ebf6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ebf6b-104">

<span> </span></span></span>

<span data-ttu-id="ebf6b-105">_**主题上次修改时间：** 2017-02-06_</span><span class="sxs-lookup"><span data-stu-id="ebf6b-105">_**Topic Last Modified:** 2017-02-06_</span></span>

<span data-ttu-id="ebf6b-106">Lync VDI 插件允许针对受支持的虚拟化技术进行音频和视频通话。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-106">The Lync VDI plug-in allows audio and video calling for supported virtualization technologies.</span></span> <span data-ttu-id="ebf6b-107">这将在 [Microsoft lync 2010 白皮书的客户端虚拟化](https://go.microsoft.com/fwlink/?linkid=330447) 中扩展 Microsoft Lync Server 2010 所示的功能。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-107">This extends the functionality outlined for Microsoft Lync Server 2010 in the [Client Virtualization in Microsoft Lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) white paper.</span></span> <span data-ttu-id="ebf6b-108">遵守标准电话规章，还包括对 E911 的支持。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-108">In compliance with standard telephone regulations, support for E911 is also included.</span></span> <span data-ttu-id="ebf6b-109">以下部分介绍 Lync VDI 插件支持的虚拟化技术和已知功能限制。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-109">The following sections describe the virtualization technologies that are supported by the Lync VDI plug-in and the known feature limitations.</span></span>

<div>

## <a name="support-for-virtualization-technologies"></a><span data-ttu-id="ebf6b-110">虚拟化技术支持</span><span class="sxs-lookup"><span data-stu-id="ebf6b-110">Support for Virtualization Technologies</span></span>

<span data-ttu-id="ebf6b-111">Lync VDI 插件支持个人虚拟桌面方案中的完整桌面远程处理，但不支持远程桌面会话方案中的完整桌面远程处理。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-111">The Lync VDI plug-in supports full desktop remoting in the personal virtual desktop scenario, but not in the remote desktop session scenario.</span></span> <span data-ttu-id="ebf6b-112">这些方案可描述如下：</span><span class="sxs-lookup"><span data-stu-id="ebf6b-112">These scenarios can be described as follows:</span></span>

  - <span data-ttu-id="ebf6b-113">**支持：个性化虚拟桌面或虚拟桌面基础结构 (VDI)。**</span><span class="sxs-lookup"><span data-stu-id="ebf6b-113">**Supported: Personalized Virtual Desktops or Virtual Desktop Infrastructure (VDI).**</span></span>   <span data-ttu-id="ebf6b-114">在此方案中，每个用户都登录到可自定义的虚拟桌面，并且能够将文件保存到桌面上，这些文件跨会话持续存在。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-114">In this scenario, each user logs on to a customizable virtual desktop and is able to save files on the desktop that persist across sessions.</span></span> <span data-ttu-id="ebf6b-115">Microsoft 远程桌面服务、VMware 地平线视图和 Citrix XenDesktop 是已测试用于 Lync 的实现。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-115">Microsoft Remote Desktop Services, VMware Horizon View, and Citrix XenDesktop are implementations that have been tested for use with Lync.</span></span> <span data-ttu-id="ebf6b-116">有关已由 Microsoft 测试的特定于供应商的 VDI 环境和客户端硬件的信息，请参阅 [Microsoft Lync 合格的基础结构](https://go.microsoft.com/fwlink/?linkid=313435)。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-116">For information about vendor-specific VDI environments and client hardware that have been tested by Microsoft, see [Infrastructure qualified for Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span></span>

  - <span data-ttu-id="ebf6b-117">**不支持：远程桌面会话。**</span><span class="sxs-lookup"><span data-stu-id="ebf6b-117">**Not supported: Remote Desktop Sessions.**</span></span>   <span data-ttu-id="ebf6b-118">在此方案中，每个用户都登录到可自定义的常规虚拟桌面会话。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-118">In this scenario, each user logs on to a generic virtual desktop session that cannot be customized.</span></span> <span data-ttu-id="ebf6b-119">示例实施包括 Microsoft 远程桌面会话 (RDSH) 和与 Citrix Receiver 组合的 Citrix XenApp。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-119">Example implementations include Microsoft Remote Desktop Sessions (RDSH) and Citrix XenApp combined with Citrix Receiver.</span></span>

<span data-ttu-id="ebf6b-120">Lync VDI 插件不支持其他虚拟化技术（如应用程序虚拟化），它允许在不需要本地安装完整应用程序的情况下使用应用程序。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-120">The Lync VDI plug-in does not support other virtualization technologies, such as application virtualization, which allows the use of an application without requiring installation of the full application locally.</span></span> <span data-ttu-id="ebf6b-121">示例实现包括 Citrix XenApp 和 Microsoft Application Virtualization (App-v) 。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-121">Example implementations include Citrix XenApp and Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="ebf6b-122">应用程序流、应用程序远程处理和混合虚拟化模式 (例如，不支持完整桌面远程) 中的应用程序远程处理。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-122">Application streaming, application remoting, and mixed virtualization modes (for example, application remoting in full desktop remoting) are not supported.</span></span>

<span data-ttu-id="ebf6b-123">为了允许扩展性，Lync VDI 插件设计为使用名为 "动态虚拟信道" 的独立于平台的 Api (DVCs) 。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-123">To allow extensibility, the Lync VDI plug-in was designed to use platform-independent APIs called Dynamic Virtual Channels (DVCs).</span></span> <span data-ttu-id="ebf6b-124">对于不是由 Lync 明确支持的方案，请参阅来自 VDI 解决方案提供商的支持声明。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-124">For scenarios that are not explicitly supported by Lync, refer to support statements from the VDI solution provider.</span></span>

</div>

<div>

## <a name="known-feature-limitations"></a><span data-ttu-id="ebf6b-125">已知功能限制</span><span class="sxs-lookup"><span data-stu-id="ebf6b-125">Known Feature Limitations</span></span>

<span data-ttu-id="ebf6b-126">在 VDI 环境中使用 Lync 2013 时，以下是已知限制：</span><span class="sxs-lookup"><span data-stu-id="ebf6b-126">The following are known limitations when you use Lync 2013 in a VDI environment:</span></span>

  - <span data-ttu-id="ebf6b-127">对呼叫委派和响应组代理匿名化功能的支持有限。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-127">There is limited support for Call Delegation and Response Group Agent Anonymization features.</span></span>

  - <span data-ttu-id="ebf6b-128">不支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="ebf6b-128">There is no support for the following features:</span></span>
    
      - <span data-ttu-id="ebf6b-129">集成音频设备和视频设备优化页。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-129">Integrated Audio Device and Video Device tuning pages.</span></span>
    
      - <span data-ttu-id="ebf6b-130">多视图视频。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-130">Multiple-view video.</span></span>
    
      - <span data-ttu-id="ebf6b-131">录制对话。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-131">Recording of conversations.</span></span>
    
      - <span data-ttu-id="ebf6b-132"> (RDS) 的远程桌面服务。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-132">Remote Desktop Services (RDS).</span></span>
    
      - <span data-ttu-id="ebf6b-133">匿名加入会议 (也就是说，加入由不与组织) 联盟的组织托管的 Lync 会议。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-133">Joining meetings anonymously (that is, joining Lync meetings hosted by an organization that does not federate with your organization).</span></span>
    
      - <span data-ttu-id="ebf6b-134">将 Lync VDI 插件与 Lync Phone Edition 设备结合使用。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-134">Using the Lync VDI plug-in along with a Lync Phone Edition device.</span></span>
    
      - <span data-ttu-id="ebf6b-135">发生网络中断时的呼叫连续性。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-135">Call continuity in case of a network outage.</span></span>
    
      - <span data-ttu-id="ebf6b-136">自定义铃声和保持音乐功能。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-136">Customized ringtones and music-on-hold features.</span></span>

  - <span data-ttu-id="ebf6b-137">Microsoft 365 或 Office 365 环境中不支持 Lync VDI 插件。</span><span class="sxs-lookup"><span data-stu-id="ebf6b-137">The Lync VDI plug-in is not supported in a Microsoft 365 or Office 365 environment.</span></span>

<span data-ttu-id="ebf6b-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ebf6b-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

