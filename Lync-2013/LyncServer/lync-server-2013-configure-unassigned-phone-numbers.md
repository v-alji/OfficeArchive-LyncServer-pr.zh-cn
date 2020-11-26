---
title: Lync Server 2013：配置未分配的电话号码
description: Lync Server 2013：配置未分配的电话号码。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure unassigned phone numbers
ms:assetid: a0650659-dce7-455f-8977-02454bbfa400
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182559(v=OCS.15)
ms:contentKeyID: 48185009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 702f297ea0a77d5e81be8b650a514ea4fa939d32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433582"
---
# <a name="configure-unassigned-phone-numbers-in-lync-server-2013"></a><span data-ttu-id="09629-103">在 Lync Server 2013 中配置未分配的电话号码</span><span class="sxs-lookup"><span data-stu-id="09629-103">Configure unassigned phone numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09629-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09629-104">

<span> </span></span></span>

<span data-ttu-id="09629-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="09629-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="09629-106">Lync Server 允许您配置对您的组织有效但未分配给用户或电话的电话号码所发生的传入呼叫。</span><span class="sxs-lookup"><span data-stu-id="09629-106">Lync Server lets you configure what happens to incoming calls to phone numbers that are valid for your organization, but are not assigned to a user or a phone.</span></span> <span data-ttu-id="09629-107">若要配置此类通话的处理，请设置未分配的号码表。</span><span class="sxs-lookup"><span data-stu-id="09629-107">To configure the handling of such calls, you set up an unassigned number table.</span></span> <span data-ttu-id="09629-108">可以使用表将呼叫路由到公告应用程序或 Exchange UM 服务器。</span><span class="sxs-lookup"><span data-stu-id="09629-108">You can use the table to route the calls to an Announcement application or to an Exchange UM server.</span></span>

<span data-ttu-id="09629-p102">配置未分配号码表的方式取决于要使用该表的方式。可以使用组织的所有有效分机、仅使用未分配的分机或使用这两类号码的组合来配置该表。未分配号码表可以同时包含已分配和未分配的号码，但仅当呼叫者拨打当前未分配号码时，才会调用该表。如果在未分配号码表中包含所有有效分机，则可以指定某人离开组织时所执行的操作，而无需重新配置该表。如果在该表中包含未分配的分机，则可以为特定号码定制所执行的操作。例如，如果更改客户服务台的分机，则可以在该表中包含旧的客户服务号码并将其分配给提供新号码的通知。</span><span class="sxs-lookup"><span data-stu-id="09629-p102">How you configure the unassigned number table depends on how you want to use it. You can configure the table with all the valid extensions for your organization, with only unassigned extensions, or with a combination of both types of numbers. The unassigned number table can include both assigned and unassigned numbers, but it is invoked only when a caller dials a number that is not currently assigned. If you include all the valid extensions in the unassigned number table, you can specify the action that occurs whenever someone leaves your organization, without needing to reconfigure the table. If you include unassigned extensions in the table, you can tailor the action that occurs for specific numbers. For example, if you change the extension for your customer service desk, you can include the old customer service number in the table and assign it to an announcement that provides the new number.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="09629-115">在配置 "未分配的号码" 表之前，必须已定义一个或多个公告，或者设置了 Exchange UM 自动助理。</span><span class="sxs-lookup"><span data-stu-id="09629-115">Before you configure the unassigned number table, you must already have either one or more announcements defined or an Exchange UM Auto Attendant set up.</span></span> <span data-ttu-id="09629-116">有关创建公告的详细信息，请参阅 <A href="lync-server-2013-create-an-announcement.md">在 Lync Server 2013 中创建公告</A>。</span><span class="sxs-lookup"><span data-stu-id="09629-116">For details about creating announcements, see <A href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</A>.</span></span> <span data-ttu-id="09629-117">若要查看是否已配置 Exchange UM 设置，请运行 <STRONG>CsExUmContact</STRONG> cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09629-117">To see if you have configured Exchange UM settings, run the <STRONG>Get-CsExUmContact</STRONG> cmdlet.</span></span> <span data-ttu-id="09629-118">有关详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact">CsExUmContact</A>。</span><span class="sxs-lookup"><span data-stu-id="09629-118">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact">Get-CsExUmContact</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="09629-119">本节内容</span><span class="sxs-lookup"><span data-stu-id="09629-119">In This Section</span></span>

  - [<span data-ttu-id="09629-120">在 Lync Server 2013 中创建或修改未分配的号码范围</span><span class="sxs-lookup"><span data-stu-id="09629-120">Create or modify an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-unassigned-number-range.md)

  - [<span data-ttu-id="09629-121">在 Lync Server 2013 中删除未分配的号码范围</span><span class="sxs-lookup"><span data-stu-id="09629-121">Delete an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-delete-an-unassigned-number-range.md)

<span data-ttu-id="09629-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09629-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

