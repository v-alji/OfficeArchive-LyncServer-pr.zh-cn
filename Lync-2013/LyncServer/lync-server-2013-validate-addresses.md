---
title: Lync Server 2013：验证地址
description: Lync Server 2013：验证地址。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validate addresses
ms:assetid: aae557c9-e6f5-4d23-8af1-1d4cd7968c54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412808(v=OCS.15)
ms:contentKeyID: 48185108
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcbb8789912b3bcbcfb60dd79807f06c2957c1f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446316"
---
# <a name="validate-addresses-in-lync-server-2013"></a><span data-ttu-id="3705d-103">在 Lync Server 2013 中验证地址</span><span class="sxs-lookup"><span data-stu-id="3705d-103">Validate addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3705d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3705d-104">

<span> </span></span></span>

<span data-ttu-id="3705d-105">_**主题上次修改时间：** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="3705d-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="3705d-106">在发布位置数据库之前，必须根据您的 SIP 主干或公共交换电话网络 (PSTN) E9 服务提供商维护的主要街道地址指南 () MSAG "验证新位置。</span><span class="sxs-lookup"><span data-stu-id="3705d-106">Before publishing the location database, you must validate new locations against the Master Street Address Guide (MSAG) that is maintained by your SIP trunk or public switched telephone network (PSTN) E9-1-1 service provider.</span></span>

<span data-ttu-id="3705d-107">有关 SIP 中继 E9 服务提供商的详细信息，请参阅 [为 Lync Server 2013 选择 E9 服务提供商](lync-server-2013-choosing-an-e9-1-1-service-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3705d-107">For details about SIP trunk E9-1-1 service providers, see [Choosing an E9-1-1 service provider for Lync Server 2013](lync-server-2013-choosing-an-e9-1-1-service-provider.md).</span></span>

<span data-ttu-id="3705d-108">有关验证地址的详细信息，请参阅以下 cmdlet 的 Lync Server Management Shell 文档：</span><span class="sxs-lookup"><span data-stu-id="3705d-108">For details about validating addresses, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="3705d-109">**CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="3705d-109">**Get-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="3705d-110">**Set-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="3705d-110">**Set-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="3705d-111">**Remove-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="3705d-111">**Remove-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="3705d-112">**CsLisCivicAddress**</span><span class="sxs-lookup"><span data-stu-id="3705d-112">**Get-CsLisCivicAddress**</span></span>

  - <span data-ttu-id="3705d-113">**Test-CsLisCivicAddress**</span><span class="sxs-lookup"><span data-stu-id="3705d-113">**Test-CsLisCivicAddress**</span></span>

<div>

## <a name="to-validate-addresses-located-in-the-location-database"></a><span data-ttu-id="3705d-114">验证位于位置数据库中的地址</span><span class="sxs-lookup"><span data-stu-id="3705d-114">To validate addresses located in the location database</span></span>

1.  <span data-ttu-id="3705d-115">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="3705d-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="3705d-116">运行以下 cmdlet 配置紧急服务提供商连接。</span><span class="sxs-lookup"><span data-stu-id="3705d-116">Run the following cmdlets to configure the emergency service provider connection.</span></span>
    
        $pwd = Read-Host -AsSecureString <password>
        Set-CsLisServiceProvider -ServiceProviderName Provider1 -ValidationServiceUrl <URL provided by provider> -CertFileName <location of certificate provided by provider> -Password $pwd

3.  <span data-ttu-id="3705d-117">运行以下 cmdlet 验证位置数据库中的地址。</span><span class="sxs-lookup"><span data-stu-id="3705d-117">Run the following cmdlet to validate the addresses in the location database.</span></span>
    
        Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus
    
    <span data-ttu-id="3705d-118">还可以使用 **Test-CsLisCivicAddress** cmdlet 验证单个地址。</span><span class="sxs-lookup"><span data-stu-id="3705d-118">You can also use the **Test-CsLisCivicAddress** cmdlet to validate individual addresses.</span></span>

<span data-ttu-id="3705d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3705d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

