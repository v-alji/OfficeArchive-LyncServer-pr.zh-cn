---
title: Lync Server 2013：配置观察程序节点以运行合成事务
description: Lync Server 2013：配置观察程序节点以运行合成事务。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to run synthetic transactions
ms:assetid: cedda508-8881-4079-88d5-49798f342ddf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205314(v=OCS.15)
ms:contentKeyID: 48185578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd5fdb3d1a1499a6ef79e962a41d9eb3ee174c33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433464"
---
# <a name="configuring-a-watcher-node-to-run-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="ccfb3-103">将观察程序节点配置为在 Lync Server 2013 中运行合成事务</span><span class="sxs-lookup"><span data-stu-id="ccfb3-103">Configuring a watcher node to run synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ccfb3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ccfb3-104">

<span> </span></span></span>

<span data-ttu-id="ccfb3-105">_**主题上次修改时间：** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="ccfb3-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="ccfb3-106">安装 System Center agent 文件后，必须接下来配置观察程序节点本身。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-106">After the System Center agent files have been installed, you must next configure the watcher node itself.</span></span> <span data-ttu-id="ccfb3-107">配置观察程序节点所采取的步骤会有所不同，具体取决于观察程序节点计算机是在外围网络内部还是在外围网络外部。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-107">The steps you take to configure a watcher node will vary depending on whether your watcher node computer lies inside your perimeter network or outside your perimeter network.</span></span>

<span data-ttu-id="ccfb3-108">配置观察程序节点时，还必须选择该节点要采用的身份验证方法类型。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-108">When you configure a watcher node, you must also choose the type of authentication method to be employed by that node.</span></span> <span data-ttu-id="ccfb3-109">Lync Server 2013 允许你选择两种身份验证方法之一：受信任的服务器或凭据身份验证。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-109">Lync Server 2013 enables you to choose one of two authentication methods: Trusted Server or Credential Authentication.</span></span> <span data-ttu-id="ccfb3-110">下表概述了这两种方法之间的差异：</span><span class="sxs-lookup"><span data-stu-id="ccfb3-110">The differences between these two methods are outlined in the following table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccfb3-111">配置</span><span class="sxs-lookup"><span data-stu-id="ccfb3-111">Configuration</span></span></th>
<th><span data-ttu-id="ccfb3-112">说明</span><span class="sxs-lookup"><span data-stu-id="ccfb3-112">Description</span></span></th>
<th><span data-ttu-id="ccfb3-113">支持的位置</span><span class="sxs-lookup"><span data-stu-id="ccfb3-113">Locations Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccfb3-114">受信任服务器</span><span class="sxs-lookup"><span data-stu-id="ccfb3-114">Trusted Server</span></span></p></td>
<td><p><span data-ttu-id="ccfb3-115">使用证书可模拟内部服务器并绕过身份验证质询。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-115">Uses a certificate to impersonate an internal server and bypass authentication challenges.</span></span></p>
<p><span data-ttu-id="ccfb3-116">这对希望管理单个证书而不是每个观察程序节点上的多个用户密码的管理员非常有用。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-116">This is useful for administrators who would prefer to manage a single certificate instead of many user passwords on each watcher node.</span></span></p></td>
<td><p><span data-ttu-id="ccfb3-117">企业内部。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-117">Inside the enterprise.</span></span></p>
<p><span data-ttu-id="ccfb3-118">请注意，利用此方法，观察程序节点必须与受监视的池位于同一个域中。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-118">Note that, with this method, the watcher node must be in the same domain as the pools being monitored.</span></span> <span data-ttu-id="ccfb3-119">如果观察程序节点和监视的池位于不同的域中，请改用凭据身份验证。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-119">If the watcher node and the monitored pools are in different domains, use Credential Authentication instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccfb3-120">凭据身份验证</span><span class="sxs-lookup"><span data-stu-id="ccfb3-120">Credential Authentication</span></span></p></td>
<td><p><span data-ttu-id="ccfb3-121">将用户名和密码安全地存储在每个观察程序节点的 Windows 凭据管理器中。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-121">Stores user names and passwords securely in Windows Credential Manager on each watcher node.</span></span></p>
<p><span data-ttu-id="ccfb3-122">此模式需要更多的密码管理，但对于位于企业外的观察程序节点，这是唯一的选择。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-122">This mode requires more password management, but is the only option for watcher nodes located outside of the enterprise.</span></span> <span data-ttu-id="ccfb3-123">不能将这些观察程序节点视为经过身份验证的受信任终结点。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-123">These watcher nodes cannot be treated as an endpoint trusted for authentication.</span></span></p></td>
<td><p><span data-ttu-id="ccfb3-124">企业外部。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-124">Outside the enterprise.</span></span></p>
<p><span data-ttu-id="ccfb3-125">企业内部。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-125">Inside the enterprise.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccfb3-126">你还应验证你的防火墙是否具有 MonitoringHost.exe 和 PowerShell.exe 的入站规则。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-126">You should also verify that your firewall has inbound rules for both MonitoringHost.exe and PowerShell.exe.</span></span> <span data-ttu-id="ccfb3-127">如果防火墙阻止了这些进程，则你的合成事务将失败，并出现 504 (服务器超时) 错误。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-127">If these processes are blocked by the firewall then your synthetic transactions will fail with a 504 (server timeout) error.</span></span>

<span data-ttu-id="ccfb3-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ccfb3-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

