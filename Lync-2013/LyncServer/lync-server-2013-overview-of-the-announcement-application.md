---
title: Lync Server 2013：公告应用程序概述
description: Lync Server 2013：公告应用程序概述。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Announcement application
ms:assetid: 2abee804-2599-48bb-90b2-15df0bae5e20
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204757(v=OCS.15)
ms:contentKeyID: 48183689
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15e9834be5edc67777f258f8d041e134287a891a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424721"
---
# <a name="overview-of-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="16c58-103">Lync Server 2013 中的公告应用程序概述</span><span class="sxs-lookup"><span data-stu-id="16c58-103">Overview of the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16c58-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16c58-104">

<span> </span></span></span>

<span data-ttu-id="16c58-105">_**主题上次修改时间：** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="16c58-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="16c58-106">部署公告应用程序时，需要配置一个未分配的数字表，用于确定当某人拨打未分配的号码时要执行的操作。</span><span class="sxs-lookup"><span data-stu-id="16c58-106">When you deploy the Announcement application, you need to configure an unassigned number table that determines the action to be taken when someone dials an unassigned number.</span></span> <span data-ttu-id="16c58-107">"未分配的号码" 表包含对组织有效的电话号码范围，并指定哪个公告应用程序处理每个范围。</span><span class="sxs-lookup"><span data-stu-id="16c58-107">The unassigned number table contains ranges of phone numbers that are valid for the organization and specifies which Announcement application handles each range.</span></span> <span data-ttu-id="16c58-108">当呼叫者拨打对您的组织有效但未分配给任何人的电话号码时，Lync Server 将在 "未分配的号码" 路由表中查找该号码，标识该号码所属的范围，并将呼叫路由到为该范围指定的公告应用程序。</span><span class="sxs-lookup"><span data-stu-id="16c58-108">When a caller dials a telephone number that is valid for your organization but is not assigned to anyone, Lync Server looks up the number in the unassigned number routing table, identifies which range the number falls in, and routes the call to the Announcement application specified for that range.</span></span> <span data-ttu-id="16c58-109">如果你将其配置为) 执行此操作，则通知应用程序会应答呼叫并播放音频消息 (，然后断开通话或将其转移到预先确定的目标（如到操作员）。</span><span class="sxs-lookup"><span data-stu-id="16c58-109">The Announcement application answers the call and plays an audio message (if you configured it to do so) and then either disconnects the call or transfers it to a predetermined destination, such as to an operator.</span></span> <span data-ttu-id="16c58-110">你可以使用 Lync Server Management Shell cmdlet 配置多条音频消息或传输目标。</span><span class="sxs-lookup"><span data-stu-id="16c58-110">You can use Lync Server Management Shell cmdlets to configure multiple audio messages or to transfer destinations.</span></span>

<span data-ttu-id="16c58-p102">配置未分配号码表的方式取决于要使用该表的方式。如果您有不再使用的特定号码并且要播放为每个号码定制的消息，则可以输入未分配号码表中的那些特定号码。例如，如果已更改客户服务台的号码，则可以输入旧的客户服务号码并将其与提供新号码的通知相关联。如果要向呼叫未分配号码的任何人（例如已离开组织的员工）播放常规消息，则可以输入组织所有可用分机的范围。每当呼叫者拨打当前未分配的号码时，系统都会调用未分配号码表。</span><span class="sxs-lookup"><span data-stu-id="16c58-p102">How you configure the unassigned number table depends on how you want to use it. If you have specific numbers that are no longer in use and you want to play messages that are tailored for each number, you can enter those specific numbers in the unassigned number table. For example, if you changed the number for your customer service desk, you can enter the old customer service number and associate it with an announcement that gives the new number. If you want to play a general message to anyone who calls a number that is not assigned, such as for employees who have left your organization, you can enter ranges for all the valid extensions in your organization. The unassigned number table is invoked whenever the caller dials a number that is not currently assigned.</span></span>

<span data-ttu-id="16c58-116">在 Lync Server 2013 中，通知应用程序将随响应组应用程序一起自动安装。</span><span class="sxs-lookup"><span data-stu-id="16c58-116">In Lync Server 2013, the Announcement application is automatically installed with the Response Group application.</span></span> <span data-ttu-id="16c58-117">"通知" 和 "响应" 组应用程序是企业语音部署的标准组件：当部署企业语音时，将自动部署这两个应用程序。</span><span class="sxs-lookup"><span data-stu-id="16c58-117">The Announcement and Response Group applications are standard components of an Enterprise Voice deployment: When you deploy Enterprise Voice, both of these applications are automatically deployed.</span></span>

<span data-ttu-id="16c58-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16c58-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

