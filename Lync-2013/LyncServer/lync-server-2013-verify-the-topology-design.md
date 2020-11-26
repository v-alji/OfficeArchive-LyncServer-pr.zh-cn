---
title: Lync Server 2013：验证拓扑设计
description: Lync Server 2013：验证拓扑设计。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438909"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a><span data-ttu-id="29978-103">在 Lync Server 2013 中验证拓扑设计</span><span class="sxs-lookup"><span data-stu-id="29978-103">Verify the topology design in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29978-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29978-104">

<span> </span></span></span>

<span data-ttu-id="29978-105">_**主题上次修改时间：** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="29978-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="29978-106">拓扑生成器会自动验证拓扑。</span><span class="sxs-lookup"><span data-stu-id="29978-106">Topology Builder automatically verifies the topology.</span></span> <span data-ttu-id="29978-107">任何拓扑错误均标识为验证错误，该错误由服务器角色旁边的验证错误图标指示。</span><span class="sxs-lookup"><span data-stu-id="29978-107">Any topology error is identified as a validation error, indicated by the validation error icon next to the server role.</span></span> <span data-ttu-id="29978-108">还必须验证拓扑是否正确表示你的部署的拓扑。</span><span class="sxs-lookup"><span data-stu-id="29978-108">It is important to also verify that the topology correctly represents the topology for your deployment.</span></span>

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a><span data-ttu-id="29978-109">在发布之前验证拓扑</span><span class="sxs-lookup"><span data-stu-id="29978-109">To verify the topology prior to publication</span></span>

1.  <span data-ttu-id="29978-110">检查所有简单 URL 是否配置正确。</span><span class="sxs-lookup"><span data-stu-id="29978-110">Check that all simple URLs are configured correctly.</span></span>

2.  <span data-ttu-id="29978-111">确认基于 SQL Server 的服务器处于联机状态，并可供安装拓扑生成器（包括所有必要防火墙规则）的计算机使用。</span><span class="sxs-lookup"><span data-stu-id="29978-111">Confirm that the SQL Server-based server is online and available to the computer where Topology Builder is installed, including any necessary firewall rules.</span></span>

3.  <span data-ttu-id="29978-112">确认文件共享可用且已定义适当的权限。</span><span class="sxs-lookup"><span data-stu-id="29978-112">Confirm that the file share is available and has the proper permissions defined.</span></span>

4.  <span data-ttu-id="29978-113">确认拓扑中定义了满足部署要求的正确服务器角色。</span><span class="sxs-lookup"><span data-stu-id="29978-113">Confirm that the correct server roles that meet the deployment requirements are defined in the topology.</span></span>

5.  <span data-ttu-id="29978-114">验证服务器是否存在于 Active Directory 域服务中。</span><span class="sxs-lookup"><span data-stu-id="29978-114">Verify that the servers exist in Active Directory Domain Services.</span></span> <span data-ttu-id="29978-115">如果已将服务器加入域，则会自动发生此情况。</span><span class="sxs-lookup"><span data-stu-id="29978-115">This will happen automatically if you have joined the servers to the domain.</span></span>

<span data-ttu-id="29978-116">如果已验证拓扑并且未出现验证错误，则发布拓扑的准备工作应该已经就绪。</span><span class="sxs-lookup"><span data-stu-id="29978-116">When you have verified the topology and there are no validation errors, you should be ready to publish the topology.</span></span> <span data-ttu-id="29978-117">如果存在验证错误，则必须先更正这些错误，然后才能发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="29978-117">If there are validation errors, you must correct these before you can publish the topology.</span></span> <span data-ttu-id="29978-118">有关发布拓扑的详细信息，请参阅 [在 Lync Server 2013 中发布拓扑](lync-server-2013-publish-the-topology.md)。</span><span class="sxs-lookup"><span data-stu-id="29978-118">For details about publishing your topology, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md).</span></span>

<span data-ttu-id="29978-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29978-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

