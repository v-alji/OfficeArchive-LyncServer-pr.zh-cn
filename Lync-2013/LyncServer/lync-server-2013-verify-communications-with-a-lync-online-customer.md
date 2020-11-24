---
title: Lync Server 2013：验证与 Lync Online 客户的通信
description: Lync Server 2013：验证与 Lync Online 客户的通信。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify communications with a Lync Online customer
ms:assetid: c8287b15-e1bb-4b26-8354-0ec90b2fcfe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202189(v=OCS.15)
ms:contentKeyID: 48185378
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 867b0f7ffffd563c869b9bcd5443a3cb91b156af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392369"
---
# <a name="verify-communications-with-a-lync-online-customer-in-lync-server-2013"></a><span data-ttu-id="8dfbc-103">在 Lync Server 2013 中验证与 Lync Online 客户的通信</span><span class="sxs-lookup"><span data-stu-id="8dfbc-103">Verify communications with a Lync Online customer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8dfbc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8dfbc-104">

<span> </span></span></span>

<span data-ttu-id="8dfbc-105">_**主题上次修改时间：** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="8dfbc-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="8dfbc-106">若要使你的组织中的 Lync 用户能够与 Microsoft Lync Online 2010 客户的用户进行通信，你必须已完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="8dfbc-106">To enable Lync users in your organization to communicate with users of a Microsoft Lync Online 2010 customer, you must have completed the following steps:</span></span>

  - <span data-ttu-id="8dfbc-107">满足所有先决条件。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-107">Met all prerequisites.</span></span> <span data-ttu-id="8dfbc-108">这包括部署内部和边缘服务器、为你的组织启用联合身份验证支持以及设置用户帐户。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-108">This includes deploying your internal and edge servers, enabling federation support for your organization, and setting up user accounts.</span></span> <span data-ttu-id="8dfbc-109">有关详细信息，请参阅 [在 Lync Server 2013 中与 Lync Online 客户进行联盟的先决条件](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md)。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-109">For details, see [Prerequisites for federating with a Lync Online customer in Lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md).</span></span>

  - <span data-ttu-id="8dfbc-110">在内部部署中配置了域访问支持。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-110">Configured domain access support in your internal deployment.</span></span> <span data-ttu-id="8dfbc-111">这包括创建主机提供程序条目和配置你的部署，以允许从 Lync Online 客户的域访问。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-111">This includes creating a host provider entry and configuring your deployment to allow access from the Lync Online customer’s domain.</span></span> <span data-ttu-id="8dfbc-112">有关详细信息，请参阅 [在 Lync Server 2013 中配置 Lync Online 域的联合身份验证支持](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md)。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-112">For details, see [Configure federation support for a Lync Online domain in Lync Server 2013](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md).</span></span>

  - <span data-ttu-id="8dfbc-113">已配置你的用户帐户以支持联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-113">Configured your user accounts to support federation.</span></span> <span data-ttu-id="8dfbc-114">有关详细信息，请参阅 [在 Lync Server 2013 中配置与 Lync Online 客户的联盟的用户访问权限](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md)。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-114">For details, see [Configure user access for federation with a Lync Online customer in Lync Server 2013](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md).</span></span>

<span data-ttu-id="8dfbc-115">完成所有这些步骤以及 Lync Online 2010 客户的管理员完成其在线服务的所有配置以支持与你的组织的联盟，请通过测试组织内部用户与 Lync Online 客户之间的通信来验证通信。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-115">After you complete all of these steps and the administrator of the Lync Online 2010 customer completes all configuration of their online services to support federation with your organization, verify communications by testing communications between an internal user in your organization and a user of the Lync Online customer.</span></span> <span data-ttu-id="8dfbc-116">如果通信不成功，请使用边缘服务器中的日志记录工具捕获日志和跟踪文件，以便对问题进行故障排除。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-116">If communication is not successful, use the Logging Tool from your Edge Server to capture log and trace files in order to troubleshoot the problem.</span></span> <span data-ttu-id="8dfbc-117">有关使用日志记录工具的详细信息，请参阅在操作文档中 [打开 Lync Server 2013 管理工具](lync-server-2013-open-lync-server-administrative-tools.md) 。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-117">For details about using the Logging Tool, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md) in the Operations documentation.</span></span> <span data-ttu-id="8dfbc-118">有关日志记录工具的详细信息，请参阅 TechNet 库中的 Lync Server 2010 日志记录工具文档 [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265) 。</span><span class="sxs-lookup"><span data-stu-id="8dfbc-118">For details about the Logging Tool, see the Lync Server 2010 Logging Tool documentation on the TechNet Library at [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265).</span></span>

<span data-ttu-id="8dfbc-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8dfbc-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

