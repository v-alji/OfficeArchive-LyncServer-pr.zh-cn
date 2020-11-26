---
title: Lync Server 2013：配置 SNMP 应用程序
description: Lync Server 2013：配置 SNMP 应用程序。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure an SNMP application
ms:assetid: c4b4a736-3b2e-45b9-a965-19d22161ad57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412972(v=OCS.15)
ms:contentKeyID: 48185346
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7374b61ad85d7ddcb40ef1db535e17f86dea58f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434107"
---
# <a name="configure-an-snmp-application-in-lync-server-2013"></a><span data-ttu-id="bd1bd-103">在 Lync Server 2013 中配置 SNMP 应用程序</span><span class="sxs-lookup"><span data-stu-id="bd1bd-103">Configure an SNMP application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd1bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd1bd-104">

<span> </span></span></span>

<span data-ttu-id="bd1bd-105">_**主题上次修改时间：** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="bd1bd-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="bd1bd-106">Lync Server 2013 包含一个标准的 web 服务接口，可用于将 Location 信息服务连接到简单网络管理协议 (SNMP) 应用程序，这些应用程序与具有端口和交换机信息的 MAC 地址相匹配。</span><span class="sxs-lookup"><span data-stu-id="bd1bd-106">Lync Server 2013 includes a standard web service interface that you can use to connect the Location Information service to Simple Network Management Protocol (SNMP) applications that match MAC addresses with port and switch information.</span></span>

<span data-ttu-id="bd1bd-107">如果已安装 SNMP 应用程序，并且位置信息服务无法在位置数据库中找到匹配项，则位置信息服务将使用客户端提供的 MAC 地址自动查询应用程序。</span><span class="sxs-lookup"><span data-stu-id="bd1bd-107">If an SNMP application is installed and the Location Information service fails to find a match in the location database, the Location Information service automatically queries the application by using the MAC address provided by the client.</span></span> <span data-ttu-id="bd1bd-108">然后，位置信息服务使用 SNMP 应用程序返回的端口和交换信息再次查询位置数据库。</span><span class="sxs-lookup"><span data-stu-id="bd1bd-108">The Location Information service then uses the port and switch information returned by the SNMP application to query the location database again.</span></span>

<span data-ttu-id="bd1bd-109">有关详细信息，请参阅 [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)。</span><span class="sxs-lookup"><span data-stu-id="bd1bd-109">For details, see [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bd1bd-110">MAC 地址在运行 Windows 8 的计算机上不可用。</span><span class="sxs-lookup"><span data-stu-id="bd1bd-110">MAC addresses are not available on computers running Windows 8.</span></span>



</div>

<div>

## <a name="to-configure-the-snmp-application-url"></a><span data-ttu-id="bd1bd-111">配置 SNMP 应用程序 URL</span><span class="sxs-lookup"><span data-stu-id="bd1bd-111">To configure the SNMP application URL</span></span>

1.  <span data-ttu-id="bd1bd-112">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="bd1bd-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="bd1bd-113">运行以下 cmdlet 为 SNMP 应用程序配置 URL。</span><span class="sxs-lookup"><span data-stu-id="bd1bd-113">Run the following cmdlet to configure the URL for the SNMP application.</span></span>
    
        Set-CsWebServiceConfiguration -MACResolverUrl "<SNMP application url>" 

<span data-ttu-id="bd1bd-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd1bd-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

