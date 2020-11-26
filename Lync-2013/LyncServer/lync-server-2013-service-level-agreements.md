---
title: Lync Server 2013：服务级别协议
description: Lync Server 2013：服务级别协议。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Service level agreements
ms:assetid: 10899bad-e8b0-422d-83c9-1599fb3a7d17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720321(v=OCS.15)
ms:contentKeyID: 63969580
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 817aa8e092d9d368dfd8cb920958553ee32e8600
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441828"
---
# <a name="service-level-agreements-in-lync-server-2013"></a><span data-ttu-id="c36f6-103">Lync Server 2013 中的服务级别协议</span><span class="sxs-lookup"><span data-stu-id="c36f6-103">Service level agreements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c36f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c36f6-104">

<span> </span></span></span>

<span data-ttu-id="c36f6-105">_**主题上次修改时间：** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="c36f6-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="c36f6-106">SLA 是一个文档，用于定义客户期望的服务。</span><span class="sxs-lookup"><span data-stu-id="c36f6-106">The SLA is a document that defines the services that your customer expects from you.</span></span> <span data-ttu-id="c36f6-107">此文档的复杂性和内容很大程度上取决于客户是否是) 或外部环境内的内部 (。</span><span class="sxs-lookup"><span data-stu-id="c36f6-107">The complexity and content of this document depends largely on whether customers are internal (within your environment) or external.</span></span>

<div>

## <a name="external-customers"></a><span data-ttu-id="c36f6-108">外部客户</span><span class="sxs-lookup"><span data-stu-id="c36f6-108">External Customers</span></span>

<span data-ttu-id="c36f6-109">如果您的客户是外部客户，则 SLA 可能是法律合同的一部分，其中包含财务奖励以及在规定的服务级别内部或外部的性能处罚。</span><span class="sxs-lookup"><span data-stu-id="c36f6-109">If your customer is external, the SLA may be part of a legal contract with financial incentives and penalties for performance that falls inside or outside defined levels of service.</span></span> <span data-ttu-id="c36f6-110">定义这些级别的服务应属于整个合同协商。</span><span class="sxs-lookup"><span data-stu-id="c36f6-110">Defining these levels of service should be part of the overall contract negotiation.</span></span>

<span data-ttu-id="c36f6-111">与所有合同一样，双方都能理解期望值，这一点非常重要。</span><span class="sxs-lookup"><span data-stu-id="c36f6-111">As with all contracts, it’s important that both parties understand expectations.</span></span> <span data-ttu-id="c36f6-112">SLA 定义了这些预期。</span><span class="sxs-lookup"><span data-stu-id="c36f6-112">The SLA defines these expectations.</span></span> <span data-ttu-id="c36f6-113">文档内容不会经常更改，并且只能因与客户进行协商而更改。</span><span class="sxs-lookup"><span data-stu-id="c36f6-113">The contents of the document should change infrequently and only because of negotiations with the customer.</span></span>

</div>

<div>

## <a name="internal-customers"></a><span data-ttu-id="c36f6-114">内部客户</span><span class="sxs-lookup"><span data-stu-id="c36f6-114">Internal Customers</span></span>

<span data-ttu-id="c36f6-115">如果您的客户是内部客户，您可能仍希望定义运营团队和 IT 系统预期的服务。</span><span class="sxs-lookup"><span data-stu-id="c36f6-115">If your customer is internal, you may still want to define the services that are expected of operations teams and of IT systems.</span></span> <span data-ttu-id="c36f6-116">SLA 可能由操作人员创建，并旨在用作组织内 IT 服务可用性的一组目标。</span><span class="sxs-lookup"><span data-stu-id="c36f6-116">The SLA may be created by the operations staff and intended as a set of goals for the availability of IT services within your organization.</span></span> <span data-ttu-id="c36f6-117">或者，性能级别可以由管理进行设置，并在评估员工性能时用作基准。</span><span class="sxs-lookup"><span data-stu-id="c36f6-117">Or, performance levels may be set by management and used as benchmarks when assessing staff performance.</span></span>

</div>

<div>

## <a name="typical-criteria"></a><span data-ttu-id="c36f6-118">典型条件</span><span class="sxs-lookup"><span data-stu-id="c36f6-118">Typical Criteria</span></span>

<span data-ttu-id="c36f6-119">Sla 包括定义最低级别可用性、支持和容量的条件的部分。</span><span class="sxs-lookup"><span data-stu-id="c36f6-119">SLAs include sections that define criteria of minimum levels of availability, support, and capacity.</span></span>

  - <span data-ttu-id="c36f6-120">**可用性**   定义网站和其他 Lync 服务将在其上可用的小时数和操作系统。</span><span class="sxs-lookup"><span data-stu-id="c36f6-120">**Availability**   Define the hours and the operating systems on which sites and other Lync services will be available.</span></span> <span data-ttu-id="c36f6-121">应定义影响服务可用性的任何例行维护。</span><span class="sxs-lookup"><span data-stu-id="c36f6-121">Any routine maintenance that affects service availability should be defined.</span></span> <span data-ttu-id="c36f6-122">定义影响服务的外部因素，例如，失去互联网连接。</span><span class="sxs-lookup"><span data-stu-id="c36f6-122">Define external factors that affect service, for example, the loss of Internet connectivity.</span></span>

  - <span data-ttu-id="c36f6-123">**支持**   定义将提供系统支持的小时数。</span><span class="sxs-lookup"><span data-stu-id="c36f6-123">**Support**   Define the hours when support for a system will be available.</span></span> <span data-ttu-id="c36f6-124">指定用于客户联系支持人员的方法、如何对事件进行分组以及确定响应和解决事件的目标时间。</span><span class="sxs-lookup"><span data-stu-id="c36f6-124">Specify methods for customers to contact support staff, how incidents are grouped, and target time to respond and to resolve the incident.</span></span> <span data-ttu-id="c36f6-125">定义反馈给客户的频率和内容。</span><span class="sxs-lookup"><span data-stu-id="c36f6-125">Define frequency and content of feedback to the customer.</span></span>

  - <span data-ttu-id="c36f6-126">**容量**   如果超出限制，则定义 Lync 网站的最大启用大小和要执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="c36f6-126">**Capacity**   Define the maximum enabled size of Lync sites and the steps to take if the limit is exceeded.</span></span> <span data-ttu-id="c36f6-127">定义执行标准任务（如从文档库检索文档的时间）的最大启用时间。</span><span class="sxs-lookup"><span data-stu-id="c36f6-127">Define the maximum enabled time to do standard tasks, such as the time to retrieve a document from a document library.</span></span> <span data-ttu-id="c36f6-128">定义每个 Lync 池的最大用户数，并同意在添加更多用户时增加容量的进程。</span><span class="sxs-lookup"><span data-stu-id="c36f6-128">Define the maximum number of users per Lync pool and agree to a process to increase capacity if more users are added.</span></span>

<span data-ttu-id="c36f6-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c36f6-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

