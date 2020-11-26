---
title: Lync Server 2013：删除设备更新配置设置的集合
description: Lync Server 2013：删除设备更新配置设置的集合。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a collection of Device Update configuration settings
ms:assetid: 1a649136-34a9-42a7-a5b3-a78bbfe93f36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994019(v=OCS.15)
ms:contentKeyID: 51803928
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3a03227869f68a52a30ea94db33bfb954b7e122
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430712"
---
# <a name="delete-a-collection-of-device-update-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="cc793-103">在 Lync Server 2013 中删除设备更新配置设置的集合</span><span class="sxs-lookup"><span data-stu-id="cc793-103">Delete a collection of Device Update configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc793-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc793-104">

<span> </span></span></span>

<span data-ttu-id="cc793-105">_**主题上次修改时间：** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="cc793-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="cc793-106">还可以使用 Windows PowerShell 和 **CsdeviceUpdateConfiguration** cmdlet 删除设备更新配置设置。</span><span class="sxs-lookup"><span data-stu-id="cc793-106">Device update configuration settings can also be deleted by using Windows PowerShell and the **Remove-CsdeviceUpdateConfiguration** cmdlet.</span></span> <span data-ttu-id="cc793-107">此 cmdlet 既可以从 Lync Server 2013 管理外壳运行，也可以从 Windows PowerShell 的远程会话运行。</span><span class="sxs-lookup"><span data-stu-id="cc793-107">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="cc793-108">有关使用远程 Windows PowerShell 连接到 Lync Server 的详细信息，请参阅 Lync Server Windows PowerShell 博客文章 "快速入门：使用远程 PowerShell 管理 Microsoft Lync Server 2010" [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) 。</span><span class="sxs-lookup"><span data-stu-id="cc793-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="to-remove-a-specific-collection-of-device-update-configuration-settings"></a><span data-ttu-id="cc793-109">删除设备更新配置设置的特定集合</span><span class="sxs-lookup"><span data-stu-id="cc793-109">To remove a specific collection of device update configuration settings</span></span>

  - <span data-ttu-id="cc793-110">此命令将删除应用于 Redmond 网站的设备更新配置设置：</span><span class="sxs-lookup"><span data-stu-id="cc793-110">This command deletes the device update configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsDeviceUpdateConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-device-update-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="cc793-111">删除应用到网站范围的所有设备更新配置设置</span><span class="sxs-lookup"><span data-stu-id="cc793-111">To remove all the device update configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="cc793-112">此命令将删除应用到网站范围的所有设备更新配置设置：</span><span class="sxs-lookup"><span data-stu-id="cc793-112">This command deletes all the device update configuration settings applied to the site scope:</span></span>
    
        Get-CsDeviceUpdateConfiguration -Filter "site:*" | Remove-CsDeviceUpdateConfiguration

</div>

<div>

## <a name="to-remove-device-update-configuration-settings-based-on-the-value-of-the-logcleanupinterval-property"></a><span data-ttu-id="cc793-113">若要删除基于 LogCleanUpInterval 属性值的设备更新配置设置</span><span class="sxs-lookup"><span data-stu-id="cc793-113">To remove device update configuration settings based on the value of the LogCleanUpInterval property</span></span>

  - <span data-ttu-id="cc793-114">以下命令将删除日志清除间隔大于10天 (10.00：00： 00) 的所有设备更新配置设置：</span><span class="sxs-lookup"><span data-stu-id="cc793-114">The following command deletes all the device update configuration settings where the log cleanup interval is greater than 10 days (10.00:00:00):</span></span>
    
        Get-CsDeviceUpdateConfiguration | Where-Object {$_.LogCleanUpInterval -gt "10.00:00:00" | Remove-CsDeviceUpdateConfiguration

</div>

<span data-ttu-id="cc793-115">有关详细信息，请参阅 [CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateConfiguration) Cmdlet 的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="cc793-115">For details, see the Help topic for the [Remove-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateConfiguration) cmdlet.</span></span>

<span data-ttu-id="cc793-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc793-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

