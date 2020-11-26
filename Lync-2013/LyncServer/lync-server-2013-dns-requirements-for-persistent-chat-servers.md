---
title: Lync Server 2013：持久聊天服务器的 DNS 要求
description: Lync Server 2013：持久聊天服务器的 DNS 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Persistent Chat Servers
ms:assetid: f7531374-d7ed-4b63-ae81-02294cb4496a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205391(v=OCS.15)
ms:contentKeyID: 48185857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01bfc126ab588542ef5160a0eabe0c839dcf0e44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429054"
---
# <a name="dns-requirements-for-persistent-chat-servers-in-lync-server-2013"></a><span data-ttu-id="f10c0-103">Lync Server 2013 中持久聊天服务器的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="f10c0-103">DNS requirements for Persistent Chat Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f10c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f10c0-104">

<span> </span></span></span>

<span data-ttu-id="f10c0-105">_**主题上次修改时间：** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="f10c0-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="f10c0-106">本部分介绍了域名系统， (了部署持久聊天服务器所需的 DNS) 记录。</span><span class="sxs-lookup"><span data-stu-id="f10c0-106">This section describes the Domain Name System (DNS) records that are required for deployment of Persistent Chat Servers.</span></span>

<div>

## <a name="dns-records-for-persistent-chat-servers"></a><span data-ttu-id="f10c0-107">持久聊天服务器的 DNS 记录</span><span class="sxs-lookup"><span data-stu-id="f10c0-107">DNS Records for Persistent Chat Servers</span></span>

<span data-ttu-id="f10c0-108">下表指定持久聊天服务器部署的 DNS 要求。</span><span class="sxs-lookup"><span data-stu-id="f10c0-108">The following table specifies DNS requirements for Persistent Chat Server deployment.</span></span>

### <a name="dns-requirements-for-a-persistent-chat-server"></a><span data-ttu-id="f10c0-109">持久聊天服务器的 DNS 要求</span><span class="sxs-lookup"><span data-stu-id="f10c0-109">DNS Requirements for a Persistent Chat Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f10c0-110">部署方案</span><span class="sxs-lookup"><span data-stu-id="f10c0-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="f10c0-111">DNS 要求</span><span class="sxs-lookup"><span data-stu-id="f10c0-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f10c0-112">一个持久聊天服务器</span><span class="sxs-lookup"><span data-stu-id="f10c0-112">One Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="f10c0-113">一个内部 A 记录，用于解析服务器的完全限定的域名 (FQDN) 服务器的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="f10c0-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f10c0-114">持久聊天池</span><span class="sxs-lookup"><span data-stu-id="f10c0-114">Persistent Chat pool</span></span></p></td>
<td><p><span data-ttu-id="f10c0-115">一个内部 A 记录，用于解析服务器的完全限定的域名 (FQDN) 到其 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="f10c0-115">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="f10c0-116"><strong>示例</strong></span><span class="sxs-lookup"><span data-stu-id="f10c0-116"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="f10c0-117">PersistentChatServer01.contoso.com 10.10.10。1</span><span class="sxs-lookup"><span data-stu-id="f10c0-117">PersistentChatServer01.contoso.com     10.10.10.1</span></span></p>
<p><span data-ttu-id="f10c0-118">PersistentChatServer02.contoso.com 10.10.10。2</span><span class="sxs-lookup"><span data-stu-id="f10c0-118">PersistentChatServer02.contoso.com     10.10.10.2</span></span></p>
<p><span data-ttu-id="f10c0-119">一个内部 A 记录，用于解析服务器的完全限定的域名 (FQDN) 到其 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="f10c0-119">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="f10c0-120"><strong>示例</strong></span><span class="sxs-lookup"><span data-stu-id="f10c0-120"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="f10c0-121">PersistentChatPool.contoso.com 10.10.10。1</span><span class="sxs-lookup"><span data-stu-id="f10c0-121">PersistentChatPool.contoso.com    10.10.10.1</span></span></p>
<p><span data-ttu-id="f10c0-122">PersistentChatPool.contoso.com 10.10.10。2</span><span class="sxs-lookup"><span data-stu-id="f10c0-122">PersistentChatPool.contoso.com    10.10.10.2</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f10c0-123">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f10c0-123">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

