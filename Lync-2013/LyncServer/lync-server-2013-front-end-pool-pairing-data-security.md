---
title: Lync Server 2013：前端池配对数据安全
description: Lync Server 2013：前端池配对数据安全。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Front End pool pairing data security
ms:assetid: edb852b8-ea86-4948-b756-60fe6ee876d2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721930(v=OCS.15)
ms:contentKeyID: 49733865
ms.date: 10/07/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 32a2ce72752819392429c8407649e663494f1daf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428046"
---
# <a name="front-end-pool-pairing-data-security-in-lync-server-2013"></a><span data-ttu-id="f3a28-103">Lync Server 2013 中的前端池配对数据安全</span><span class="sxs-lookup"><span data-stu-id="f3a28-103">Front End pool pairing data security in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3a28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3a28-104">

<span> </span></span></span>

<span data-ttu-id="f3a28-105">_**主题上次修改时间：** 2014-10-07_</span><span class="sxs-lookup"><span data-stu-id="f3a28-105">_**Topic Last Modified:** 2014-10-07_</span></span>

<span data-ttu-id="f3a28-106">备份服务是 Lync Server 2013 中引入的一种数据复制机制，可在两个数据中心之间连续传输两个已配对前端池的用户数据和会议内容，以便进行灾难恢复。</span><span class="sxs-lookup"><span data-stu-id="f3a28-106">The Backup Service is a data replication mechanism introduced in Lync Server 2013 that transfers user data and conference content between two paired Front End pools continuously across two data centers for disaster recovery purposes.</span></span> <span data-ttu-id="f3a28-107">用户数据包含用户 SIP Uri 以及联系人列表和设置。</span><span class="sxs-lookup"><span data-stu-id="f3a28-107">The user data contains user SIP URIs as well as contact lists and settings.</span></span> <span data-ttu-id="f3a28-108">会议内容包括 Microsoft PowerPoint 2010 上传以及在会议中使用的白板。</span><span class="sxs-lookup"><span data-stu-id="f3a28-108">Conference content includes Microsoft PowerPoint 2010 uploads, as well as whiteboards used in conferences.</span></span> <span data-ttu-id="f3a28-109">从源池中，用户数据和会议内容从已压缩的本地存储导出到目标池，并将其解压缩并导入到本地存储。</span><span class="sxs-lookup"><span data-stu-id="f3a28-109">From the source pool, user data and conference content are exported from the local storage, zipped, transferred to the target Pool, where it is unzipped and imported to local storage.</span></span> <span data-ttu-id="f3a28-110">备份服务假定两个数据中心之间的通讯链路位于公司网络内部，并且具有 Internet 保护。</span><span class="sxs-lookup"><span data-stu-id="f3a28-110">The Backup Service assumes that the communications link between the two data centers is within the corporate network that is protected from the Internet.</span></span> <span data-ttu-id="f3a28-111">它不会在两个数据中心之间加密已传输的数据，也不会在本地封装在安全协议（如 HTTPS）中。</span><span class="sxs-lookup"><span data-stu-id="f3a28-111">It does not encrypt the transferred data between the two data centers, nor is it natively encapsulated within a secure protocol, such as HTTPS.</span></span> <span data-ttu-id="f3a28-112">因此，来自公司网络内部人员的中间人攻击是可能的。</span><span class="sxs-lookup"><span data-stu-id="f3a28-112">Therefore, man-in-the-middle attack from internal personnel within the corporate network is possible.</span></span>

<div>

## <a name="evaluating-security-risks"></a><span data-ttu-id="f3a28-113">评估安全风险</span><span class="sxs-lookup"><span data-stu-id="f3a28-113">Evaluating Security Risks</span></span>

<span data-ttu-id="f3a28-114">跨多个数据中心部署 Lync Server 2013 并使用灾难恢复功能的任何企业必须确保跨数据中心流量受其公司 Intranet 的保护。</span><span class="sxs-lookup"><span data-stu-id="f3a28-114">Any enterprise which deploys Lync Server 2013 across multiple data centers and uses the disaster recovery feature must ensure that cross-data center traffic is protected by their corporate Intranet.</span></span> <span data-ttu-id="f3a28-115">负责内部攻击防护的企业必须保护数据中心之间的通信链接。</span><span class="sxs-lookup"><span data-stu-id="f3a28-115">Enterprises which care about internal attack protection must secure the communication links among the data centers.</span></span>

<span data-ttu-id="f3a28-116">假设企业的数据中心受保护在公司 Intranet 的下方是标准的。</span><span class="sxs-lookup"><span data-stu-id="f3a28-116">The assumption that data centers of an enterprise are protected behind the corporate Intranet is standard.</span></span> <span data-ttu-id="f3a28-117">在这些数据中心中传输了许多其他类型的公司敏感数据。</span><span class="sxs-lookup"><span data-stu-id="f3a28-117">There are many other types of corporate sensitive data transferred among these data centers.</span></span> <span data-ttu-id="f3a28-118">如果这些跨数据中心链接不受保护，企业的 IT 基础结构将面临可怕风险。</span><span class="sxs-lookup"><span data-stu-id="f3a28-118">The enterprise’s IT infrastructure is at dire risk if these cross-data center links are not protected.</span></span>

<span data-ttu-id="f3a28-119">当公司网络内存在中间人攻击的风险时，比较而言，它相当于包含将流量公开到 Internet。</span><span class="sxs-lookup"><span data-stu-id="f3a28-119">While the risk of man-in-the-middle attacks within the corporate network exists, it is relatively contained as compared to exposing the traffic to the Internet.</span></span> <span data-ttu-id="f3a28-120">具体地说，由备份服务 (（如 SIP Uri) ）公开的用户数据通常可通过其他方式（如 Exchange 或其他目录软件的全球通讯簿）供公司内的所有员工使用。</span><span class="sxs-lookup"><span data-stu-id="f3a28-120">Specifically, the user data exposed by Backup Service (such as SIP URIs) are generally available to all employees within the company via other means such as the Global Address Book by Exchange or other directory software.</span></span> <span data-ttu-id="f3a28-121">因此，当使用备份服务在两个配对的池之间复制数据时，重点应在保护两个数据中心之间的 WAN。</span><span class="sxs-lookup"><span data-stu-id="f3a28-121">Hence, the focus should be on securing the WAN between the two data centers when the Backup Service is used to copy data between the two paired Pools.</span></span>

</div>

<div>

## <a name="mitigating-security-risks"></a><span data-ttu-id="f3a28-122">减少安全风险</span><span class="sxs-lookup"><span data-stu-id="f3a28-122">Mitigating Security Risks</span></span>

<span data-ttu-id="f3a28-123">有多种方法可增强备份服务流量的安全保护，范围从限制对数据中心的访问，到保护两个数据中心之间的 WAN 传输。</span><span class="sxs-lookup"><span data-stu-id="f3a28-123">There are many ways to enhance security protection for the Backup Service traffic, ranging from restricting access to the data centers to securing the WAN transport between the two data centers.</span></span> <span data-ttu-id="f3a28-124">在大多数情况下，部署 Lync Server 2013 的企业可能已经有了所需的安全基础结构。</span><span class="sxs-lookup"><span data-stu-id="f3a28-124">In most cases, enterprises deploying Lync Server 2013 might already have the required security infrastructure in place.</span></span> <span data-ttu-id="f3a28-125">对于寻求指导的企业，Microsoft 提供解决方案作为如何构建安全 IT 基础结构的示例。</span><span class="sxs-lookup"><span data-stu-id="f3a28-125">For enterprises looking for guidance, Microsoft provides solution as an example of how to build a secure IT infrastructure.</span></span> <span data-ttu-id="f3a28-126">但是，这并不意味着它是唯一的解决方案，也不意味着它是 Lync Server 的首选解决方案。</span><span class="sxs-lookup"><span data-stu-id="f3a28-126">However, this does not imply that it is the only solution, nor does it imply that it is the preferred solution for Lync Server.</span></span> <span data-ttu-id="f3a28-127">我们建议，企业客户根据其 IT 安全基础结构和要求选择解决方案满足其特定需求。Microsoft 解决方案示例使用 IPSec 和组策略进行服务器和域隔离。</span><span class="sxs-lookup"><span data-stu-id="f3a28-127">We recommend that enterprise customers choose the solution suits their specific needs, based on their IT security infrastructure and requirements.The example Microsoft solution employs IPSec and Group Policy for Server and Domain Isolation.</span></span> <span data-ttu-id="f3a28-128">有关详细信息，请参阅 [https://go.microsoft.com/fwlink/p/?LinkId=268544](https://go.microsoft.com/fwlink/p/?linkid=268544) 。</span><span class="sxs-lookup"><span data-stu-id="f3a28-128">For details, see [https://go.microsoft.com/fwlink/p/?LinkId=268544](https://go.microsoft.com/fwlink/p/?linkid=268544).</span></span> <span data-ttu-id="f3a28-129">有关问题和评论，请联系 secwish@microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="f3a28-129">For questions and comments, contact secwish@microsoft.com.</span></span>

<span data-ttu-id="f3a28-130">另一个可能的解决方案是仅使用 IPSec 来帮助保护由备份服务本身发送的数据。</span><span class="sxs-lookup"><span data-stu-id="f3a28-130">Another possible solution is to use IPSec just to help secure the data sent by the Backup Service itself.</span></span> <span data-ttu-id="f3a28-131">如果选择此方法，您应该为以下服务器配置 SMB 协议的 IPSec 规则，其中，池 A 和池 B 是两个配对前端池。</span><span class="sxs-lookup"><span data-stu-id="f3a28-131">If you choose this method, you should configure the IPSec rules for the SMB protocol for the following servers, where Pool A and Pool B are two paired Front End pools.</span></span>

  - <span data-ttu-id="f3a28-132">SMB 服务 (TCP/445) 从池 A 中的每个前端服务器到由池 B 使用的文件存储。</span><span class="sxs-lookup"><span data-stu-id="f3a28-132">The SMB Service (TCP/445) from each Front End Server in Pool A to the File Store used by Pool B.</span></span>

  - <span data-ttu-id="f3a28-133">SMB 服务 (TCP/445) 从池 B 中的每个前端服务器到由池 A 使用的文件存储。</span><span class="sxs-lookup"><span data-stu-id="f3a28-133">The SMB Service (TCP/445) from each Front End Server in Pool B to the File Store used by Pool A.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="f3a28-134">IPsec 不专门用于代替应用程序级别的安全，例如，SSL/TLS。</span><span class="sxs-lookup"><span data-stu-id="f3a28-134">IPsec is not intended as a replacement for application-level security, such as SSL/TLS.</span></span> <span data-ttu-id="f3a28-135">使用 IPsec 的一个优势是，可为现有应用程序提供网络流量安全，但无需更改它们。</span><span class="sxs-lookup"><span data-stu-id="f3a28-135">One advantage of using IPsec is that it can provide network traffic security for existing applications without having to change them.</span></span> <span data-ttu-id="f3a28-136">只想在两个数据中心之间提供传输保护的企业应该咨询其相应的网络硬件供应商，以了解有关通过使用供应商的设备建立安全 WAN 连接的方法。</span><span class="sxs-lookup"><span data-stu-id="f3a28-136">Enterprises that want to just secure the transport between the two data centers should consult their respective networking hardware vendors about ways to set up secure WAN connections by using the vendor’s equipment.</span></span>



<span data-ttu-id="f3a28-137"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3a28-137"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

