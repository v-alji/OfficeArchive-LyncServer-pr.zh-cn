---
title: Lync Server 2013：启用 Office Web Apps Server 和 Lync Server 2013
description: Lync Server 2013：启用 Office Web Apps Server 和 Lync Server 2013。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Office Web Apps Server and Lync Server 2013
ms:assetid: 3370ab55-9949-4f32-b88b-5cffed6aaad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204792(v=OCS.15)
ms:contentKeyID: 48183790
ms.date: 08/19/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a1bf4e09dc29bf344b78df50595258f0663cd731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392191"
---
# <a name="configuring-integration-with-office-web-apps-server-and-lync-server-2013"></a><span data-ttu-id="75ef3-103">配置与 Office Web Apps Server 和 Lync Server 2013 的集成</span><span class="sxs-lookup"><span data-stu-id="75ef3-103">Configuring integration with Office Web Apps Server and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75ef3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75ef3-104">

<span> </span></span></span>

<span data-ttu-id="75ef3-105">_**主题上次修改时间：** 2016-08-19_</span><span class="sxs-lookup"><span data-stu-id="75ef3-105">_**Topic Last Modified:** 2016-08-19_</span></span>

<span data-ttu-id="75ef3-106">Lync Server 2013 使用 Office Web Apps 服务器处理 PowerPoint 演示文稿。</span><span class="sxs-lookup"><span data-stu-id="75ef3-106">Lync Server 2013 employs Office Web Apps Server to handle PowerPoint presentations.</span></span> <span data-ttu-id="75ef3-107">有关此方法的优势的信息，请参阅 [Lync Server 2013 中的 web 会议概述](lync-server-2013-web-conferencing-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="75ef3-107">For information about the advantages to this approach, see [Overview of web conferencing in Lync Server 2013](lync-server-2013-web-conferencing-overview.md).</span></span>

<span data-ttu-id="75ef3-108">若要使用这些新功能，管理员必须安装 Office Web Apps 服务器，并且必须将 Lync Server 2013 配置为与 Office Web Apps 服务器通信。</span><span class="sxs-lookup"><span data-stu-id="75ef3-108">In order to use these new capabilities administrators must install Office Web Apps Server and they must configure Lync Server 2013 to communicate with Office Web Apps Server.</span></span> <span data-ttu-id="75ef3-109">本文档提供有关如何将 Lync Server 2013 配置为使用 Office Web Apps 服务器的信息。</span><span class="sxs-lookup"><span data-stu-id="75ef3-109">This documentation provides information on how to configure Lync Server 2013 to work with Office Web Apps Server.</span></span> <span data-ttu-id="75ef3-110">本文档不提供的信息是有关如何安装 Office Web Apps 服务器本身的信息;有关这些信息，请参阅 Microsoft Office Web Apps 部署网站 <https://go.microsoft.com/fwlink/p/?linkid=257525> 。</span><span class="sxs-lookup"><span data-stu-id="75ef3-110">What this documentation does not provide is information on how to install Office Web Apps Server itself; for that information, see the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span> <span data-ttu-id="75ef3-111">该指南包括 Office Web Apps 服务器的完整必备信息;请注意，Office Web Apps 服务器应安装在未运行 Lync Server、Microsoft SQL Server 或任何其他服务器应用程序的独立计算机上。</span><span class="sxs-lookup"><span data-stu-id="75ef3-111">That guide includes complete prerequisite information for Office Web Apps Server; note that Office Web Apps Server should be installed on a stand-alone computer that is not running Lync Server, Microsoft SQL Server, or any other server application.</span></span> <span data-ttu-id="75ef3-112"> (您不能在该计算机上安装任何版本的 Microsoft Office。 ) 用于运行 Office Web Apps 服务器的任何计算机还必须安装一组特定的软件， (包括 .NET Framework 4.5 和 Windows PowerShell 3.0) ;有关配置证书和 Internet 信息服务 (IIS) 的详细信息，请参阅 Microsoft Office Web Apps 部署网站中的详细讨论 <https://go.microsoft.com/fwlink/p/?linkid=257525> 。</span><span class="sxs-lookup"><span data-stu-id="75ef3-112">(You must not have any version of Microsoft Office installed on that computer.) Any computer used to run Office Web Apps Server must also have a specific set of software installed (including .NET Framework 4.5 and Windows PowerShell 3.0); these requirements, along with information on configuring certificates and Internet Information Services (IIS), are discussed in detail in the Microsoft Office Web Apps Deployment website at <https://go.microsoft.com/fwlink/p/?linkid=257525>.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="75ef3-113">Office Web Apps 服务器的最新小版本称为 "Office Online Server"，该服务器受 Lync Server 2013 支持。</span><span class="sxs-lookup"><span data-stu-id="75ef3-113">The latest iteration of Office Web Apps Server is named Office Online Server, which is supported by Lync Server 2013.</span></span> <span data-ttu-id="75ef3-114">有关更多详细信息，请参阅 <A href="https://technet.microsoft.com/library/jj219456(v=office.16).aspx">Office Online Server 文档</A>。</span><span class="sxs-lookup"><span data-stu-id="75ef3-114">For more detail, refer to the <A href="https://technet.microsoft.com/library/jj219456(v=office.16).aspx">Office Online Server documentation</A>.</span></span>



</div>

<span data-ttu-id="75ef3-115">本文档包含以下主题区域：</span><span class="sxs-lookup"><span data-stu-id="75ef3-115">This document covers the following topic areas:</span></span>

  - [<span data-ttu-id="75ef3-116">将 Lync Server 2013 配置为使用 Office Web Apps 服务器</span><span class="sxs-lookup"><span data-stu-id="75ef3-116">Configuring Lync Server 2013 to work with Office Web Apps Server</span></span>](lync-server-2013-configuring-lync-server-2013-to-work-with-office-web-apps-server.md)

  - [<span data-ttu-id="75ef3-117">使用反向代理服务器在 Lync Server 2013 中发布 Office Web Apps 服务器</span><span class="sxs-lookup"><span data-stu-id="75ef3-117">Publishing Office Web Apps Server in Lync Server 2013 using a reverse proxy server</span></span>](lync-server-2013-publishing-office-web-apps-server-using-a-reverse-proxy-server.md)

  - [<span data-ttu-id="75ef3-118">在 Lync Server 2013 中验证 Office Web Apps 服务器的配置</span><span class="sxs-lookup"><span data-stu-id="75ef3-118">Validating the configuration of Office Web Apps Server in Lync Server 2013</span></span>](lync-server-2013-validating-the-configuration-of-office-web-apps-server.md)

  - [<span data-ttu-id="75ef3-119">配置 Lync Server 2013 客户端以与 Office Web Apps 服务器配合使用</span><span class="sxs-lookup"><span data-stu-id="75ef3-119">Configuring clients of Lync Server 2013 for use with Office Web Apps Server</span></span>](lync-server-2013-configuring-clients-for-use-with-office-web-apps-server.md)

<span data-ttu-id="75ef3-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75ef3-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

