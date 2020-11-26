---
title: Lync Server 2013：设备更新 Web 服务
description: Lync Server 2013：设备更新 Web 服务。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update Web service
ms:assetid: 036f473d-a131-431f-8051-76ccadc5cfba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994015(v=OCS.15)
ms:contentKeyID: 51803921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45511d34ab99f295481472f2a3c14bf21da32ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429365"
---
# <a name="device-update-web-service-in-lync-server-2013"></a><span data-ttu-id="0be80-103">Lync Server 2013 中的设备更新 Web 服务</span><span class="sxs-lookup"><span data-stu-id="0be80-103">Device Update Web service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0be80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0be80-104">

<span> </span></span></span>

<span data-ttu-id="0be80-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="0be80-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="0be80-106">Lync 服务器包括 "设备更新" Web 服务，该服务将作为 Web 服务角色的一部分自动安装。</span><span class="sxs-lookup"><span data-stu-id="0be80-106">Lync Server includes the Device Update Web service, which is automatically installed as part of the Web Services role.</span></span> <span data-ttu-id="0be80-107">此服务允许你从 Microsoft 下载更新，测试这些更新，然后将更新部署到你的组织中的 IP 电话。</span><span class="sxs-lookup"><span data-stu-id="0be80-107">This service lets you download updates from Microsoft, test them, and then deploy the updates to IP phones in your organization.</span></span> <span data-ttu-id="0be80-108">你还可以使用 "设备更新" Web 服务将设备回退到以前的软件版本。</span><span class="sxs-lookup"><span data-stu-id="0be80-108">You can also use Device Update Web service to roll back devices to previous software versions.</span></span>

<span data-ttu-id="0be80-109">本节提供有关如何使用设备更新日志管理设备更新 Web 服务和部署更新的详细信息， (Lync Phone Edition 的规则使用 *规则* 将固件版本更新与硬件设备关联) 和配置设置。</span><span class="sxs-lookup"><span data-stu-id="0be80-109">This section provides details about how to manage the Device Update Web service and deployed updates by using device update logs, rules (Lync Phone Edition uses *rules* to associate firmware version updates with hardware devices), and configuration settings.</span></span>

<span data-ttu-id="0be80-110">有关设备更新 Web 服务流程和功能的详细信息，请参阅在 Lync Server 2010 中 [更新设备](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) TechNet 库。</span><span class="sxs-lookup"><span data-stu-id="0be80-110">For details about the Device Update Web service process and features, see [Updating Devices](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="0be80-111"> (请注意，设备更新 Web 服务（如所有 Lync Phone 版组件）的工作方式与 lync server 2013 相同，与 Lync Server 2010 相同。 ) </span><span class="sxs-lookup"><span data-stu-id="0be80-111">(Note that the Device Update Web service, like all Lync Phone Edition components, works the same way with Lync Server 2013 as it does with Lync Server 2010.)</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0be80-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="0be80-112">In This Section</span></span>

  - [<span data-ttu-id="0be80-113">Lync Server 2013 中的设备更新日志和文件</span><span class="sxs-lookup"><span data-stu-id="0be80-113">Device Update logs and files in Lync Server 2013</span></span>](lync-server-2013-device-update-logs-and-files.md)

  - [<span data-ttu-id="0be80-114">Lync Server 2013 中的设备更新规则</span><span class="sxs-lookup"><span data-stu-id="0be80-114">Device Update rules in Lync Server 2013</span></span>](lync-server-2013-device-update-rules.md)

  - [<span data-ttu-id="0be80-115">Lync Server 2013 中的设备更新配置设置</span><span class="sxs-lookup"><span data-stu-id="0be80-115">Device Update configuration settings in Lync Server 2013</span></span>](lync-server-2013-device-update-configuration-settings.md)

  - [<span data-ttu-id="0be80-116">在 Lync Server 2013 中查看设备的软件更新</span><span class="sxs-lookup"><span data-stu-id="0be80-116">View software updates for devices in Lync Server 2013</span></span>](lync-server-2013-view-software-updates-for-devices-in-your-organization.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0be80-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0be80-117">See Also</span></span>


<span data-ttu-id="0be80-118">[用于管理设备和排除设备故障的工具和服务](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span><span class="sxs-lookup"><span data-stu-id="0be80-118">[Tools and Services for Managing and Troubleshooting Devices](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span></span>  
  

<span data-ttu-id="0be80-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0be80-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

