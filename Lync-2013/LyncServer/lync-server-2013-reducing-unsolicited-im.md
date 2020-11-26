---
title: Lync Server 2013：减少垃圾 IM
description: Lync Server 2013：减少未经请求的 IM。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reducing unsolicited IM for Lync Server 2013
ms:assetid: d2998708-e699-4465-a918-e1d9ea4c49c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518335(v=OCS.15)
ms:contentKeyID: 62625493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 294c53a6b82b4dc345fbb9afcf9983d5bd35893a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436669"
---
# <a name="reducing-unsolicited-im-for-lync-server-2013"></a><span data-ttu-id="4294a-103">减少 Lync Server 2013 的垃圾 IM</span><span class="sxs-lookup"><span data-stu-id="4294a-103">Reducing unsolicited IM for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4294a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4294a-104">

<span> </span></span></span>

<span data-ttu-id="4294a-105">_**主题上次修改时间：** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="4294a-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="4294a-106">智能 IM 筛选器应用程序可帮助保护 Microsoft Lync Server 2013 部署，使其不会受到最常见病毒的攻击，最大程度地降低用户体验。</span><span class="sxs-lookup"><span data-stu-id="4294a-106">The Intelligent IM Filter application helps protect your Microsoft Lync Server 2013 deployment against the most common viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="4294a-107">智能 IM 筛选器提供以下内容：</span><span class="sxs-lookup"><span data-stu-id="4294a-107">The Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="4294a-108">增强的 URL 筛选</span><span class="sxs-lookup"><span data-stu-id="4294a-108">Enhanced URL filtering</span></span>

  - <span data-ttu-id="4294a-109">增强的文件传输筛选</span><span class="sxs-lookup"><span data-stu-id="4294a-109">Enhanced file transfer filtering</span></span>

<span data-ttu-id="4294a-110">使用智能 IM 筛选器配置筛选器，阻止来自公司防火墙外的未知终结点的未经请求或可能有害的即时消息。</span><span class="sxs-lookup"><span data-stu-id="4294a-110">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="4294a-111">通过指定用于确定应阻止的条件的条件（如包含超链接的即时消息和具有特定扩展名的文件）来配置筛选器。</span><span class="sxs-lookup"><span data-stu-id="4294a-111">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks and files with specific extensions.</span></span>

<span data-ttu-id="4294a-112">在部署智能 IM 消息筛选器应用程序之前，应了解当邮件从一个 Lync Server 2013 服务器路由到另一个时如何应用筛选选项。</span><span class="sxs-lookup"><span data-stu-id="4294a-112">Before you deploy the Intelligent IM Message Filter application, you should understand how filtering options are applied when messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="4294a-113">应用这些筛选选项的方式是一致的，无论服务器位于单个组织还是跨组织边界。</span><span class="sxs-lookup"><span data-stu-id="4294a-113">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="4294a-114">此一致性适用于将自定义通知和警告文本插入到邮件中并在服务器上发送的方式。</span><span class="sxs-lookup"><span data-stu-id="4294a-114">This consistency applies to the way that the customized notice, and warning texts are inserted into messages and sent across servers.</span></span>

<span data-ttu-id="4294a-115">建议的筛选选项是允许带有超链接的即时消息，但需要智能 IM 筛选器通过在其前面插入下划线来禁用链接。</span><span class="sxs-lookup"><span data-stu-id="4294a-115">The recommended filtering option is to allow instant messages with hyperlinks but require the Intelligent IM Filter to disable the link by inserting an underscore before it.</span></span> <span data-ttu-id="4294a-116">如果选择此选项，则可以选择向用户提供通知，该选项显示在包含超链接的每个即时消息的开头。</span><span class="sxs-lookup"><span data-stu-id="4294a-116">If you choose this option, you have the additional option of composing a notice to users that appears at the beginning of each instant message that contains a hyperlink.</span></span>

<span data-ttu-id="4294a-117">第二个筛选选项允许带有未修改的超链接的即时消息。</span><span class="sxs-lookup"><span data-stu-id="4294a-117">A second filtering option is to allow instant messages with unmodified hyperlinks.</span></span> <span data-ttu-id="4294a-118">如果选择此选项，则会 (建议) 向插入到每封邮件中的用户撰写警告的其他选项。</span><span class="sxs-lookup"><span data-stu-id="4294a-118">If you choose this option, you have the additional option (recommended) of composing a warning to users that is inserted in each message.</span></span>

<span data-ttu-id="4294a-119">第三个选项是阻止所有包含超链接的即时消息。</span><span class="sxs-lookup"><span data-stu-id="4294a-119">A third option is to block all instant messages that contain hyperlinks.</span></span> <span data-ttu-id="4294a-120">如果选择此选项，服务器会向用户发送警告。</span><span class="sxs-lookup"><span data-stu-id="4294a-120">If you choose this option, the server sends a warning to the user.</span></span> <span data-ttu-id="4294a-121">必须编写此警告。</span><span class="sxs-lookup"><span data-stu-id="4294a-121">You must write this warning.</span></span>

<span data-ttu-id="4294a-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4294a-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

