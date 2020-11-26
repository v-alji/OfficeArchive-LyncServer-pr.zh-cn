---
title: Lync Server 2013：故障排除和关键运行状况指示器
description: Lync Server 2013：故障排除和关键运行状况指示器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting and Key Health Indicators
ms:assetid: 14ec9e21-aa2b-4d65-9be4-ef2adfbe9a8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720322(v=OCS.15)
ms:contentKeyID: 63969585
ms.date: 05/18/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8fdb214d4ce8472800272a05e81b0402d3bf820e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436214"
---
# <a name="troubleshooting-and-key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="9d8ce-103">Lync Server 2013 中的故障排除和关键运行状况指示器</span><span class="sxs-lookup"><span data-stu-id="9d8ce-103">Troubleshooting and Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d8ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d8ce-104">

<span> </span></span></span>

<span data-ttu-id="9d8ce-105">_**主题上次修改时间：** 2015-05-18_</span><span class="sxs-lookup"><span data-stu-id="9d8ce-105">_**Topic Last Modified:** 2015-05-18_</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9d8ce-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="9d8ce-106">In This Section</span></span>

<span data-ttu-id="9d8ce-107">为了满足参考体系结构 Sla 要求并确保顺利过渡到我们的支持团队，一般的故障排除方法必须与 Lync Server [网络指南](https://go.microsoft.com/fwlink/p/?linkid=390677) 中定义的一组必需的疑难解答工具和方法一起定义。</span><span class="sxs-lookup"><span data-stu-id="9d8ce-107">To meet the Reference Architecture SLAs and to ensure a smooth transition to our support teams, a common troubleshooting approach must be defined together with a required set of troubleshooting tools and approaches as defined in the Lync Server [Networking guide](https://go.microsoft.com/fwlink/p/?linkid=390677) .</span></span>

<span data-ttu-id="9d8ce-108">强烈建议使用 System Center Operations Manager 监视 Lync Server 2013 系统的运行状况。</span><span class="sxs-lookup"><span data-stu-id="9d8ce-108">We strongly recommend that System Center Operations Manager be used to monitor the health of the Lync Server 2013 system.</span></span> <span data-ttu-id="9d8ce-109">另外，请参阅 Lync Server 2013 [网络指南](https://go.microsoft.com/fwlink/p/?linkid=390677) 中的 KHIs 和 Excel 电子表格中与 lync 2013 一起使用的讨论。</span><span class="sxs-lookup"><span data-stu-id="9d8ce-109">Also, refer to the discussion of KHIs in the Lync Server 2013 [Networking guide](https://go.microsoft.com/fwlink/p/?linkid=390677) and the Excel spreadsheet for use with Lync 2013.</span></span>

</div>

<div>

## <a name="reference"></a><span data-ttu-id="9d8ce-110">参考</span><span class="sxs-lookup"><span data-stu-id="9d8ce-110">Reference</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="9d8ce-111">相关部分</span><span class="sxs-lookup"><span data-stu-id="9d8ce-111">Related Sections</span></span>

<span data-ttu-id="9d8ce-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d8ce-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

