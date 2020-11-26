---
title: Lync Server 2013：有关 Lync 的 Lync-Skype 连接的说明
description: Lync Server 2013：注意关于 Lync 的 Lync-Skype 连接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Note about Lync-Skype connectivity for Lync On
ms:assetid: 1d0f5c1a-74c6-468f-9877-ad2b1ddf355f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440169(v=OCS.15)
ms:contentKeyID: 57793359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f7d9758f277f2f987677c2c0ffa0a4447ba31d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424973"
---
# <a name="note-about-lync-skype-connectivity-in-lync-server-2013-for-lync-online-customers"></a><span data-ttu-id="73ed0-103">有关 Lync Server 2013 for Lync Online 客户的 Lync-Skype 连接的说明</span><span class="sxs-lookup"><span data-stu-id="73ed0-103">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73ed0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73ed0-104">

<span> </span></span></span>

<span data-ttu-id="73ed0-105">_**主题上次修改时间：** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="73ed0-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="73ed0-106">本文档旨在帮助 Lync Server 内部部署管理员设置 Lync-Skype 连接。</span><span class="sxs-lookup"><span data-stu-id="73ed0-106">This document was written to help Lync Server on-premise administrators set up Lync-Skype connectivity.</span></span>  <span data-ttu-id="73ed0-107">Lync-Skype 连接也是 Lync Online 的一项功能，它是 Office 365 和 Microsoft 365 的一部分。</span><span class="sxs-lookup"><span data-stu-id="73ed0-107">Lync-Skype connectivity is also a feature of Lync Online, which is part of Office 365 and Microsoft 365.</span></span> <span data-ttu-id="73ed0-108">你可以从管理中心内的 Lync 管理中心启用 Lync-Skype 连接功能。</span><span class="sxs-lookup"><span data-stu-id="73ed0-108">You can enable the Lync-Skype connectivity feature from the Lync Administration Center within the admin center.</span></span>

<span data-ttu-id="73ed0-109">对于 Microsoft 365 中型企业版、Office 365 企业版、Microsoft 365 教育版和 Office 365 for 政府：登录到 Office 365 门户或 Microsoft 365 管理中心，然后导航到 **Lync 管理中心**。</span><span class="sxs-lookup"><span data-stu-id="73ed0-109">For Microsoft 365 Midsize Business, Office 365 Enterprise, Microsoft 365 Education, and Office 365 for Government: Sign in to the Office 365 portal or Microsoft 365 admin center and navigate to the **Lync Administration Center**.</span></span> <span data-ttu-id="73ed0-110">转到 " **外部通信**"。</span><span class="sxs-lookup"><span data-stu-id="73ed0-110">Go to **External Communications**.</span></span> <span data-ttu-id="73ed0-111">在 " **公用 IM 服务提供商**" 下，单击 " **启用**"。</span><span class="sxs-lookup"><span data-stu-id="73ed0-111">Under **Public IM Service Providers**, click **Enable**.</span></span> <span data-ttu-id="73ed0-112">如果要控制单个用户对 Lync-Skype 连接的访问权限，您可以通过编辑单个用户的外部通信设置来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="73ed0-112">If you want to control individual user access to Lync-Skype Connectivity, you can do so by editing individual users’ External Communications settings.</span></span>

<span data-ttu-id="73ed0-113">对于 Microsoft 365 小型企业高级版：登录到 Microsoft 365，然后转到 " **管理员 \> 服务设置" \> 即时消息、会议和会议**。</span><span class="sxs-lookup"><span data-stu-id="73ed0-113">For Microsoft 365 Small Business Premium: Sign in to Microsoft 365, and go to **Admin \> Service Settings \> Instant messaging, meetings and conferencing**.</span></span> <span data-ttu-id="73ed0-114">打开“外部通信”。</span><span class="sxs-lookup"><span data-stu-id="73ed0-114">Turn on External communications.</span></span> <span data-ttu-id="73ed0-115">外部通信开关可同时打开 Lync-Skype 连接和与使用 Lync 的其他组织进行通信。</span><span class="sxs-lookup"><span data-stu-id="73ed0-115">The External communications switch turns on both Lync-Skype connectivity and communications with other organizations that use Lync.</span></span> <span data-ttu-id="73ed0-116">根据开始使用 Lync Online 的时间，"打开" 状态的外部通信开关最初可能仅指示已激活其他 Lync 组织的通信。</span><span class="sxs-lookup"><span data-stu-id="73ed0-116">Depending on when you started using Lync Online, the External communications switch in an "on" state may initially indicate only that communications with other Lync organizations is activated.</span></span> <span data-ttu-id="73ed0-117">若要打开 Lync-Skype 连接，只需关闭交换机，然后再重新打开。</span><span class="sxs-lookup"><span data-stu-id="73ed0-117">To turn on Lync-Skype Connectivity, simply toggle the switch off and then back on again.</span></span>

<span data-ttu-id="73ed0-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73ed0-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

