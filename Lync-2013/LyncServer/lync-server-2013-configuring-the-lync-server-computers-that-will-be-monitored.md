---
title: Lync Server 2013：配置将监视的 Lync Server 计算机
description: Lync Server 2013：配置将监视的 Lync Server 计算机。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computers that will be monitored
ms:assetid: 9f1b2b91-d5af-42ad-a27d-b0815f762ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205118(v=OCS.15)
ms:contentKeyID: 48184927
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 742bd8a67eb42472e598c45619514e9407cb29cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432553"
---
# <a name="configuring-the-lync-server-computers-that-will-be-monitored-in-lync-server-2013"></a><span data-ttu-id="2e395-103">配置将在 Lync Server 2013 中监视的 Lync Server 计算机</span><span class="sxs-lookup"><span data-stu-id="2e395-103">Configuring the Lync Server computers that will be monitored in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2e395-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2e395-104">

<span> </span></span></span>

<span data-ttu-id="2e395-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="2e395-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="2e395-106">由于 Lync Server 2013 不使用在 Microsoft Lync Server 2010 中使用的中央发现过程，因此要监视的每个 Lync Server 2013 计算机必须能够自我报告它是否存在于管理服务器。</span><span class="sxs-lookup"><span data-stu-id="2e395-106">Because Lync Server 2013 does not use the central discovery process used in Microsoft Lync Server 2010, each Lync Server 2013 computer that you want to monitor must be able to self-report its existence to the management server.</span></span> <span data-ttu-id="2e395-107">若要实现此操作，必须在要监视的每台计算机上安装 Operations Manager 代理文件。</span><span class="sxs-lookup"><span data-stu-id="2e395-107">To make this possible, you must install the Operations Manager agent files on each of the computers to be monitored.</span></span> <span data-ttu-id="2e395-108">安装代理文件后，必须将计算机配置为充当 System Center proxy。</span><span class="sxs-lookup"><span data-stu-id="2e395-108">After the agent files have been installed, you must configure the computer to act as a System Center proxy.</span></span> <span data-ttu-id="2e395-109">请注意，在这些计算机上安装和配置 Lync Server 之后，应执行这些过程。</span><span class="sxs-lookup"><span data-stu-id="2e395-109">Note that these procedures should be carried out after you have installed and configured Lync Server on these computers.</span></span>

<span data-ttu-id="2e395-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2e395-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

