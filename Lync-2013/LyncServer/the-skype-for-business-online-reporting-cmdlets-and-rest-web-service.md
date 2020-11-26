---
title: Skype for Business Online 报告 cmdlet 和 REST web 服务
description: Skype for Business Online 报告 cmdlet 和 REST web 服务。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: The Skype for Business Online reporting cmdlets and REST web service
ms:assetid: cadd73a7-c08a-4102-b73a-ccb3ad4987bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362845(v=OCS.15)
ms:contentKeyID: 56563409
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2160e0910d42f811ec8b03fa50450d5f73c59b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423405"
---
# <a name="the-skype-for-business-online-reporting-cmdlets-and-rest-web-service"></a><span data-ttu-id="595ae-103">Skype for Business Online 报告 cmdlet 和 REST web 服务</span><span class="sxs-lookup"><span data-stu-id="595ae-103">The Skype for Business Online reporting cmdlets and REST web service</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="595ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="595ae-104">

<span> </span></span></span>

<span data-ttu-id="595ae-105">_**主题上次修改时间：** 2014-09-05_</span><span class="sxs-lookup"><span data-stu-id="595ae-105">_**Topic Last Modified:** 2014-09-05_</span></span>

<span data-ttu-id="595ae-106">通过结合报告功能，Skype for Business Online 提供对五个 Windows PowerShell cmdlet 的访问权限，可帮助生成这些报告，并且管理员也可以使用这些 cmdlet 返回自定义报告数据。</span><span class="sxs-lookup"><span data-stu-id="595ae-106">In conjunction with the reporting features, Skype for Business Online provides access to five Windows PowerShell cmdlets that help generate those reports and are also can be used by administrators to return customized reporting data.</span></span> <span data-ttu-id="595ae-107">Skype for Business Online 还包括 REST (Representational 状态转移) ，可供开发人员用于检索自定义报告信息。</span><span class="sxs-lookup"><span data-stu-id="595ae-107">Skype for Business Online also includes the REST (Representational State Transfer), which can be used by developers to retrieve customized reporting information.</span></span>

<span data-ttu-id="595ae-108">管理员可用的报告 cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="595ae-108">The reporting cmdlets available to administrators include:</span></span>

  - <span data-ttu-id="595ae-109">CsActiveUserReport，提供有关活动用户数的信息 (也就是说，已登录到 Skype for Business Online 并参与至少一个会议或对等通信会话的用户) 。</span><span class="sxs-lookup"><span data-stu-id="595ae-109">Get-CsActiveUserReport, which provides information about the number of active users (that is, users who have logged on to Skype for Business Online and participated in at least one conference or peer-to-peer communication session).</span></span>

  - <span data-ttu-id="595ae-110">CsAVConferenceTimeReport，它提供有关) 用户在音频/视频会议上花费的 (时间量的信息。</span><span class="sxs-lookup"><span data-stu-id="595ae-110">Get-CsAVConferenceTimeReport, which provides information about the amount of time (in minutes) users spent in audio/video conferences.</span></span>

  - <span data-ttu-id="595ae-111">CsConferenceReport，提供有关用户参与的会议的数量和类型的信息。</span><span class="sxs-lookup"><span data-stu-id="595ae-111">Get-CsConferenceReport, which provides information about the number and type of conferences that users participated in.</span></span>

  - <span data-ttu-id="595ae-112">CsP2PAVTimeReport，它提供有关在中的 (时间量的信息，) 用户在包含音频和/或视频的对等会话中花费的时间。</span><span class="sxs-lookup"><span data-stu-id="595ae-112">Get-CsP2PAVTimeReport, which provides information about the amount of time (in minutes) users spent in peer-to-peer sessions that included audio and/or video.</span></span>

  - <span data-ttu-id="595ae-113">CsP2PSessionReport，提供有关用户参与的对等会话的数量和类型的信息。</span><span class="sxs-lookup"><span data-stu-id="595ae-113">Get-CsP2PSessionReport, which provides information about the number and type of peer-to-peer sessions that users participated in.</span></span>

<span data-ttu-id="595ae-114">大多数管理员将使用 Microsoft 365 管理中心提供的报表：不仅是自动生成的报表，还提供了数据的图形表示形式，这些数据通常更容易解释报告 cmdlet 返回的原始数字值。</span><span class="sxs-lookup"><span data-stu-id="595ae-114">Most administrators will use the reports available in the Microsoft 365 admin center: not only are those reports auto-generated, but they also provide a graphical representation of the data that is often easier to interpret than the raw number values returned by the reporting cmdlets.</span></span> <span data-ttu-id="595ae-115">但是，熟悉 Windows PowerShell 的管理员可以使用报告 cmdlet 从 Lync Online 报告中返回不容易提供的数据。</span><span class="sxs-lookup"><span data-stu-id="595ae-115">However, administrators familiar with Windows PowerShell can use the reporting cmdlets to return data that is not readily available from the Lync Online reports.</span></span> <span data-ttu-id="595ae-116">例如，报告 cmdlet 返回有关会话持续时间的信息， (每个会话持续) 的时间量（以分钟为单位）。</span><span class="sxs-lookup"><span data-stu-id="595ae-116">For example, the reporting cmdlets return information about session duration (the amount of time, in minutes, that each session lasted).</span></span> <span data-ttu-id="595ae-117">使用 Lync Online 报表不提供单个会话持续时间。</span><span class="sxs-lookup"><span data-stu-id="595ae-117">Individual session durations are not available using the Lync Online reports.</span></span> <span data-ttu-id="595ae-118">同样，在 "每日" 视图中，Lync Online 报表仅显示之前14天的信息。</span><span class="sxs-lookup"><span data-stu-id="595ae-118">Likewise, in daily view the Lync Online reports display information only for the preceding 14 days.</span></span> <span data-ttu-id="595ae-119">如果想要查看其他日期的每日总计 (例如，四个月前的日期) 你可以使用报告 cmdlet 执行此操作。</span><span class="sxs-lookup"><span data-stu-id="595ae-119">If you would like to review the daily totals for a different day (for example, a date from four months ago) you can do so by using the reporting cmdlets.</span></span>

<span data-ttu-id="595ae-120">管理员还可能对 [使用 Excel 检索 Office 365 报告数据](https://msdn.microsoft.com/library/dn781442.aspx)的文章感兴趣，其中介绍了如何使用 Microsoft Excel 中的 OData 数据查询功能来创建自定义 Office 365 报表。</span><span class="sxs-lookup"><span data-stu-id="595ae-120">Administrators might also be interested in the article [Using Excel to Retrieve Office 365 Reporting Data](https://msdn.microsoft.com/library/dn781442.aspx), which explains how to use the OData data querying feature in Microsoft Excel to create custom office 365 report.</span></span> <span data-ttu-id="595ae-121">自定义报表使你能够决定 (哪些数据以及从 Office 365 报告服务中返回多少数据) 。</span><span class="sxs-lookup"><span data-stu-id="595ae-121">Custom reports give you the ability to dictate which data (and how much data) is returned from the Office 365 reporting service.</span></span> <span data-ttu-id="595ae-122">自定义报表还允许你执行如下操作：指定应如何对数据进行排序和分组，并提供对不在管理中心中显示的信息的访问权限。</span><span class="sxs-lookup"><span data-stu-id="595ae-122">Custom reports also enable you to do such things as specify how the data should be sorted and grouped, and provide access to information that is not displayed in the admin center.</span></span>

<span data-ttu-id="595ae-123">具有开发背景的管理员可以使用 REST web 服务获取未在 Skype for Business Online 管理中心中显示的信息。</span><span class="sxs-lookup"><span data-stu-id="595ae-123">Administrators with a development background can use the REST web service to obtain information not displayed in the Skype for Business Online admin center.</span></span> <span data-ttu-id="595ae-124">REST 服务类似于 SOAP 服务，因为每种技术都提供了一种在客户端和服务器之间传输 XML 数据的方法。</span><span class="sxs-lookup"><span data-stu-id="595ae-124">The REST service is similar to the SOAP service, in that each technology provides a way to transfer XML data between a client and a server.</span></span> <span data-ttu-id="595ae-125">但是，REST 服务至少具有与 SOAP 服务相比的两个优势。</span><span class="sxs-lookup"><span data-stu-id="595ae-125">However, the REST service has at least two advantages over the SOAP service.</span></span> <span data-ttu-id="595ae-126">对于一个，REST 使用称为 ATOM 供稿格式的标准化格式执行 XML 数据传输。</span><span class="sxs-lookup"><span data-stu-id="595ae-126">For one, REST performs XML data transfers using a standardized format known as the ATOM syndication format.</span></span> <span data-ttu-id="595ae-127">相比之下，传输数据时使用非标准格式的 SOAP。</span><span class="sxs-lookup"><span data-stu-id="595ae-127">By contrast, SOAP using a non-standard format when transferring data.</span></span> <span data-ttu-id="595ae-128">此外，REST 能够跨阻止 "获取" 和 "发布" 等 HTTP 谓词的网络传输数据。</span><span class="sxs-lookup"><span data-stu-id="595ae-128">In addition, REST is able to transfer data across networks that block HTTP verbs other than GET and POST.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="595ae-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="595ae-129">See Also</span></span>


<span data-ttu-id="595ae-130">[Lync Online 报告](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="595ae-130">[Lync Online reporting](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span></span>  


[<span data-ttu-id="595ae-131">Office 365 报告 Web 服务</span><span class="sxs-lookup"><span data-stu-id="595ae-131">The Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984325.aspx)  
[<span data-ttu-id="595ae-132">了解 Office 365 Reporting Web 服务</span><span class="sxs-lookup"><span data-stu-id="595ae-132">Learning About the Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984321.aspx)  
<span data-ttu-id="595ae-133">[Exchange Online 报告 Cmdlet](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span><span class="sxs-lookup"><span data-stu-id="595ae-133">[The Exchange Online Reporting Cmdlets](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span></span>  
[<span data-ttu-id="595ae-134">使用 Excel 检索 Office 365 报告数据</span><span class="sxs-lookup"><span data-stu-id="595ae-134">Using Excel to Retrieve Office 365 Reporting Data</span></span>](https://msdn.microsoft.com/library/dn781442.aspx)  
  

<span data-ttu-id="595ae-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="595ae-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

