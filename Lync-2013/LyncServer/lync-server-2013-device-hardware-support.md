---
title: Lync Server 2013 设备硬件支持
description: Lync Server 2013 设备硬件支持。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429447"
---
# <a name="device-hardware-support-in-lync-server-2013"></a><span data-ttu-id="a6e5c-103">Lync Server 2013 中的设备硬件支持</span><span class="sxs-lookup"><span data-stu-id="a6e5c-103">Device hardware support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6e5c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6e5c-104">

<span> </span></span></span>

<span data-ttu-id="a6e5c-105">_**主题上次修改时间：** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="a6e5c-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="a6e5c-106">在部署 IP 电话和模拟设备之前，必须准备好特定的硬件配置。</span><span class="sxs-lookup"><span data-stu-id="a6e5c-106">Specific hardware configurations must be in place before you deploy IP phones and analog devices.</span></span>

<span data-ttu-id="a6e5c-107">运行 Lync Phone Edition 的 IP 电话支持链接层发现 Protocol-Media 终结点发现 (LLDP-) 和以太网 (PoE) 的电源。</span><span class="sxs-lookup"><span data-stu-id="a6e5c-107">IP phones running Lync Phone Edition support Link Layer Discovery Protocol-Media Endpoint Discovery (LLDP-MED) and Power over Ethernet (PoE).</span></span> <span data-ttu-id="a6e5c-108">若要充分利用 LLDP-MED-V，交换机必须支持 IEEE 802.1 AB 和 ANSI/TIA-1057。</span><span class="sxs-lookup"><span data-stu-id="a6e5c-108">To take advantage of LLDP-MED, the switch must support IEEE802.1AB and ANSI/TIA-1057.</span></span> <span data-ttu-id="a6e5c-109">为了利用 PoE，交换机必须支持 PoE 802.3 AF 或 802.3 at。</span><span class="sxs-lookup"><span data-stu-id="a6e5c-109">To take advantage of PoE, the switch must support PoE802.3AF or 802.3at.</span></span>

<span data-ttu-id="a6e5c-110">若要启用 LLDP-MED-V，管理员必须使用切换控制台窗口启用 LLDP，并使用正确的语音 VLAN ID 设置 LLDP 网络策略。</span><span class="sxs-lookup"><span data-stu-id="a6e5c-110">To enable LLDP-MED, the administrator must enable LLDP by using the switch console window and set the LLDP-MED network policy with the correct voice VLAN ID.</span></span>

<span data-ttu-id="a6e5c-111">此外，如果你的部署包括模拟设备，则必须将模拟网关配置为使用 Lync Server，并且网关必须是以下各项之一：</span><span class="sxs-lookup"><span data-stu-id="a6e5c-111">In addition, if your deployment includes analog devices, you must configure the analog gateway to use Lync Server, and the gateway must be one of the following:</span></span>

  - <span data-ttu-id="a6e5c-112"> (ATA) 的模拟电话适配器</span><span class="sxs-lookup"><span data-stu-id="a6e5c-112">An analog telephone adapter (ATA)</span></span>

  - <span data-ttu-id="a6e5c-113">PSTN 模拟网关</span><span class="sxs-lookup"><span data-stu-id="a6e5c-113">A PSTN analog gateway</span></span>

  - <span data-ttu-id="a6e5c-114">包含 PSTN 模拟网关的 Survivable 分支装置</span><span class="sxs-lookup"><span data-stu-id="a6e5c-114">A Survivable Branch Appliance that includes a PSTN analog gateway</span></span>

  - <span data-ttu-id="a6e5c-115">包括与 ATA 通信的 PSTN 网关的 Survivable 分支装置</span><span class="sxs-lookup"><span data-stu-id="a6e5c-115">A Survivable Branch Appliance that includes a PSTN gateway that communicates with an ATA</span></span>

<span data-ttu-id="a6e5c-116">若要了解如何配置模拟网关，请参阅 [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) Lync Server 2010 TechNet 库中的 "规划以部署模拟设备"。</span><span class="sxs-lookup"><span data-stu-id="a6e5c-116">To learn how to configure an analog gateway, see "Planning to Deploy Analog Devices" at [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="a6e5c-117"> (模拟设备在 lync Server 2013 中的工作方式与在 Lync Server 2010 中相同。 ) </span><span class="sxs-lookup"><span data-stu-id="a6e5c-117">(Analog devices work the same way in Lync Server 2013 as they do in Lync Server 2010.)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a6e5c-118">如果切换器支持此功能，则可以将开关配置为增强 9-1-1 (E9-1-1) 。</span><span class="sxs-lookup"><span data-stu-id="a6e5c-118">You can configure the switch for Enhanced 9-1-1 (E9-1-1), if the switch supports this.</span></span>



<span data-ttu-id="a6e5c-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6e5c-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

