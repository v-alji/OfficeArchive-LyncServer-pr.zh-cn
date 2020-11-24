---
title: Lync Server 2013：配置 IIS
description: Lync Server 2013：配置 IIS。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure IIS
ms:assetid: bc4ae8cc-ec0c-42f1-9034-058930e530d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412918(v=OCS.15)
ms:contentKeyID: 48185248
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cdd08e47d05f2e32f14178eaaa3a100f8c445dda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392224"
---
# <a name="configure-iis-for-lync-server-2013"></a><span data-ttu-id="a0822-103">为 Lync Server 2013 配置 IIS</span><span class="sxs-lookup"><span data-stu-id="a0822-103">Configure IIS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0822-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0822-104">

<span> </span></span></span>

<span data-ttu-id="a0822-105">_**主题上次修改时间：** 2011-12-16_</span><span class="sxs-lookup"><span data-stu-id="a0822-105">_**Topic Last Modified:** 2011-12-16_</span></span>

<span data-ttu-id="a0822-106">为 Lync Server 2013 配置 Internet 信息服务 (IIS) 需要安装正确的组件以支持 Lync Server 2013 所需的 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="a0822-106">Configuring Internet Information Services (IIS) for Lync Server 2013 involves installing the correct components to support the Web Services needed by Lync Server 2013.</span></span> <span data-ttu-id="a0822-107">有关安装 IIS 的详细信息，请参阅 [Lync Server 2013 中的 IIS 配置](lync-server-2013-iis-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="a0822-107">For details about installing IIS, see [IIS configuration in Lync Server 2013](lync-server-2013-iis-configuration.md).</span></span> <span data-ttu-id="a0822-108">如果你有策略在服务器上运行安全配置向导，然后再将其投入服务或维护的典型部分，请参阅 [在安全配置向导关闭服务器后，在 iis 中关闭端口](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) ，以便在 Lync SERVER 2013 IIS 配置中关闭端口的相关信息。</span><span class="sxs-lookup"><span data-stu-id="a0822-108">If you have a policy to run the Security Configuration Wizard on servers before putting them into service or as a typical part of your maintenance, see [Re-activate server after Security Configuration Wizard closes ports in IIS](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) for information about a side effect of running the wizard that will close ports on a Lync Server 2013 IIS configuration.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a0822-109">本节内容</span><span class="sxs-lookup"><span data-stu-id="a0822-109">In This Section</span></span>

  - [<span data-ttu-id="a0822-110">Lync Server 2013 中的 IIS 配置</span><span class="sxs-lookup"><span data-stu-id="a0822-110">IIS configuration in Lync Server 2013</span></span>](lync-server-2013-iis-configuration.md)

  - [<span data-ttu-id="a0822-111">使用安全配置向导在 IIS 中关闭端口后重新激活服务器</span><span class="sxs-lookup"><span data-stu-id="a0822-111">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md)

<span data-ttu-id="a0822-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0822-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

