---
title: Lync Server 2013：从另一个应用程序启动 Lync
description: Lync Server 2013：从另一个应用程序启动 Lync。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Starting Lync from another application
ms:assetid: 573b30b1-6590-4b24-8e96-a41be57cb0ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398376(v=OCS.15)
ms:contentKeyID: 48184184
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd64b8b9f335638b54a0bf6473b5d159c97a0e7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391812"
---
# <a name="starting-lync-from-another-application"></a><span data-ttu-id="11664-103">从另一个应用程序启动 Lync</span><span class="sxs-lookup"><span data-stu-id="11664-103">Starting Lync from another application</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="11664-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="11664-104">

<span> </span></span></span>

<span data-ttu-id="11664-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="11664-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="11664-106">可以使用命令行参数快速启动 Lync 2013。</span><span class="sxs-lookup"><span data-stu-id="11664-106">You can use command-line parameters to quick-start Lync 2013.</span></span> <span data-ttu-id="11664-107">例如，如果用户单击另一个应用程序中的电话号码，应用程序可以启动 Lync 2013 的一个实例，并启动对该号码的调用。</span><span class="sxs-lookup"><span data-stu-id="11664-107">For example, if a user clicks a phone number in another application, the application can start an instance of Lync 2013 and initiate a call to that number.</span></span>

<span data-ttu-id="11664-108">Lync 2013 还可以识别以分号分隔的多方会议的联系人姓名列表。</span><span class="sxs-lookup"><span data-stu-id="11664-108">Lync 2013 can also recognize a semicolon-delimited list of contact names for multiparty conferencing.</span></span>

<span data-ttu-id="11664-109">如果 Lync 2013 配置为在启动时自动登录，则通过命令行参数启动 Lync 2013 将打开 Lync 主窗口。</span><span class="sxs-lookup"><span data-stu-id="11664-109">If Lync 2013 is configured to automatically sign in when started, then starting Lync 2013 with command-line parameters will open the Lync main window.</span></span> <span data-ttu-id="11664-110">如果 Lync 未配置为在启动时自动登录，则登录窗口将打开。</span><span class="sxs-lookup"><span data-stu-id="11664-110">If Lync is not configured to automatically sign in when started, the sign-in window opens.</span></span>

<span data-ttu-id="11664-111">下表显示了可用的参数。</span><span class="sxs-lookup"><span data-stu-id="11664-111">The following table shows the available parameters.</span></span>

### <a name="lync-2013-command-line-parameters"></a><span data-ttu-id="11664-112">Lync 2013 Command-Line 参数</span><span class="sxs-lookup"><span data-stu-id="11664-112">Lync 2013 Command-Line Parameters</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11664-113">线</span><span class="sxs-lookup"><span data-stu-id="11664-113">Extension</span></span></th>
<th><span data-ttu-id="11664-114">数据的格式</span><span class="sxs-lookup"><span data-stu-id="11664-114">Format of Data</span></span></th>
<th><span data-ttu-id="11664-115">Action</span><span class="sxs-lookup"><span data-stu-id="11664-115">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11664-116">tel</span><span class="sxs-lookup"><span data-stu-id="11664-116">tel:</span></span></p></td>
<td><p><span data-ttu-id="11664-117">电话 URI</span><span class="sxs-lookup"><span data-stu-id="11664-117">tel URI</span></span></p></td>
<td><p><span data-ttu-id="11664-118">为音频呼叫打开对话窗口，但不拨打指定号码。</span><span class="sxs-lookup"><span data-stu-id="11664-118">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11664-119">callto</span><span class="sxs-lookup"><span data-stu-id="11664-119">callto:</span></span></p></td>
<td><p><span data-ttu-id="11664-120">电话：、sip：或 typeable 电话 URI</span><span class="sxs-lookup"><span data-stu-id="11664-120">tel:, sip:, or typeable tel URI</span></span></p></td>
<td><p><span data-ttu-id="11664-121">为音频呼叫打开对话窗口，但不拨打指定号码。</span><span class="sxs-lookup"><span data-stu-id="11664-121">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11664-122">sip</span><span class="sxs-lookup"><span data-stu-id="11664-122">sip:</span></span></p></td>
<td><p><span data-ttu-id="11664-123">SIP URI</span><span class="sxs-lookup"><span data-stu-id="11664-123">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="11664-124">在参与者列表中打开具有指定 SIP 统一资源标识符 (URI) 的对话窗口。</span><span class="sxs-lookup"><span data-stu-id="11664-124">Opens the Conversation window with the specified SIP Uniform Resource Identifier (URI) in the participant list.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11664-125">那些</span><span class="sxs-lookup"><span data-stu-id="11664-125">Sips:</span></span></p></td>
<td><p><span data-ttu-id="11664-126">SIP URI</span><span class="sxs-lookup"><span data-stu-id="11664-126">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="11664-127">如果 Lync 2013 配置为使用 (TLS) 协议的传输层安全，则功能与 sip 完全一样：。</span><span class="sxs-lookup"><span data-stu-id="11664-127">If Lync 2013 is configured to use the Transport Layer Security (TLS) protocol, functions exactly like sip:.</span></span> <span data-ttu-id="11664-128">如果未使用 TLS，则会显示一个对话框，通知用户需要更高的安全级别。</span><span class="sxs-lookup"><span data-stu-id="11664-128">If TLS is not being used, displays a dialog box informing the user that a higher level of security is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11664-129">会议</span><span class="sxs-lookup"><span data-stu-id="11664-129">conf:</span></span></p></td>
<td><p><span data-ttu-id="11664-130">要加入的会议的 SIP URI</span><span class="sxs-lookup"><span data-stu-id="11664-130">SIP URI of conference to join</span></span></p></td>
<td><p><span data-ttu-id="11664-131">如果 URI 为 self，则实例化焦点并显示仅限名单的视图。</span><span class="sxs-lookup"><span data-stu-id="11664-131">If URI is self, instantiates the focus and brings up roster-only view.</span></span> <span data-ttu-id="11664-132">否则，调出名单视图，但不发送邀请。</span><span class="sxs-lookup"><span data-stu-id="11664-132">Otherwise, brings up roster view but does not send INVITE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11664-133">im</span><span class="sxs-lookup"><span data-stu-id="11664-133">im:</span></span></p></td>
<td><p><span data-ttu-id="11664-134">SIP URI</span><span class="sxs-lookup"><span data-stu-id="11664-134">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="11664-135">显示即时消息 (IM) 仅使用 SIP URI 的对话窗口。</span><span class="sxs-lookup"><span data-stu-id="11664-135">Displays an instant messaging (IM)-only Conversation window with the SIP URI.</span></span> <span data-ttu-id="11664-136">接受尖括号中指定的多个 SIP Uri (&lt; &gt; 不带任何分隔符的) 。</span><span class="sxs-lookup"><span data-stu-id="11664-136">Accepts multiple SIP URIs specified inside angle brackets (&lt;&gt;) without any separator.</span></span></p>
<pre><code>im:&lt;sip:user1@host&gt;&lt;sip:user2@host&gt;</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="11664-137">下表提供了这些命令行参数的示例。</span><span class="sxs-lookup"><span data-stu-id="11664-137">The following table provides examples of these command-line parameters.</span></span>

### <a name="command-line-parameter-examples"></a><span data-ttu-id="11664-138">Command-Line 参数示例</span><span class="sxs-lookup"><span data-stu-id="11664-138">Command-Line Parameter Examples</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11664-139">示例</span><span class="sxs-lookup"><span data-stu-id="11664-139">Instance</span></span></th>
<th><span data-ttu-id="11664-140">结果</span><span class="sxs-lookup"><span data-stu-id="11664-140">Results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11664-141">电话： + 14255550101</span><span class="sxs-lookup"><span data-stu-id="11664-141">Tel:+14255550101</span></span></p></td>
<td><p><span data-ttu-id="11664-142">打开具有 + 14255550101 的仅手机视图。</span><span class="sxs-lookup"><span data-stu-id="11664-142">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11664-143">Callto：电话： + 14255550101</span><span class="sxs-lookup"><span data-stu-id="11664-143">Callto:tel:+ 14255550101</span></span></p></td>
<td><p><span data-ttu-id="11664-144">打开具有 + 14255550101 的仅手机视图。</span><span class="sxs-lookup"><span data-stu-id="11664-144">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11664-145">Callto:sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="11664-145">Callto:sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="11664-146">打开一个仅限手机的视图，kazuto@litwareinc.com。</span><span class="sxs-lookup"><span data-stu-id="11664-146">Opens a phone-only view with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11664-147">sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="11664-147">sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="11664-148">打开一个带 kazuto@litwareinc.com 的对话窗口。</span><span class="sxs-lookup"><span data-stu-id="11664-148">Opens a Conversation window with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11664-149">会议： sip：https://meet.contoso.com/kazuto/7322994</span><span class="sxs-lookup"><span data-stu-id="11664-149">conf:sip:https://meet.contoso.com/kazuto/7322994</span></span></p></td>
<td><p><span data-ttu-id="11664-150">打开对话窗口，并显示会议音频联接选项。</span><span class="sxs-lookup"><span data-stu-id="11664-150">Opens a Conversation window and displays meeting audio join options.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="11664-151">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="11664-151">


</div>

<span> </span>

</div>

</div>

</span></span></div>

