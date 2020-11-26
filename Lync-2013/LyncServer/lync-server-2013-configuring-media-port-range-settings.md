---
title: Lync Server 2013：配置媒体端口范围设置
description: Lync Server 2013：配置媒体端口范围设置。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring media port range settings
ms:assetid: 2c4b7c0b-0dce-48f4-a489-336d6e526f7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204770(v=OCS.15)
ms:contentKeyID: 48183723
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a7670284c593197068c366f43bbb3faaaad8f63
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432910"
---
# <a name="configuring-media-port-range-settings-in-lync-server-2013"></a><span data-ttu-id="4bac6-103">在 Lync Server 2013 中配置媒体端口范围设置</span><span class="sxs-lookup"><span data-stu-id="4bac6-103">Configuring media port range settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4bac6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4bac6-104">

<span> </span></span></span>

<span data-ttu-id="4bac6-105">_**主题上次修改时间：** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="4bac6-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="4bac6-106">媒体端口范围设置会显著影响客户端性能，因此应进行配置。</span><span class="sxs-lookup"><span data-stu-id="4bac6-106">Media port range settings can significantly impact client performance and should be configured.</span></span> <span data-ttu-id="4bac6-107">你可以使用 Lync Server 命令行管理程序配置这些设置。</span><span class="sxs-lookup"><span data-stu-id="4bac6-107">You can configure these settings by using Lync Server Management Shell.</span></span>

### <a name="media-port-range-settings"></a><span data-ttu-id="4bac6-108">媒体端口范围设置</span><span class="sxs-lookup"><span data-stu-id="4bac6-108">Media Port Range Settings</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bac6-109">设置</span><span class="sxs-lookup"><span data-stu-id="4bac6-109">Setting</span></span></th>
<th><span data-ttu-id="4bac6-110">说明</span><span class="sxs-lookup"><span data-stu-id="4bac6-110">Description</span></span></th>
<th><span data-ttu-id="4bac6-111">Lync Server Management Shell cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bac6-111">Lync Server Management Shell cmdlet</span></span></th>
<th><span data-ttu-id="4bac6-112">Cmdlet 参数</span><span class="sxs-lookup"><span data-stu-id="4bac6-112">Cmdlet parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bac6-113">Portrange\Enabled</span><span class="sxs-lookup"><span data-stu-id="4bac6-113">Portrange\Enabled</span></span></p></td>
<td><p><span data-ttu-id="4bac6-114">指定服务器发送的端口范围是否应由客户端用于媒体和发送信号。</span><span class="sxs-lookup"><span data-stu-id="4bac6-114">Specifies whether the port ranges sent by the server should be used by the client for media and signaling.</span></span> <span data-ttu-id="4bac6-115">与 subvalues MinMediaPort 和 MaxMediaPort 结合使用。</span><span class="sxs-lookup"><span data-stu-id="4bac6-115">Used in conjunction with the subvalues MinMediaPort and MaxMediaPort.</span></span></p></td>
<td><p><span data-ttu-id="4bac6-116"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="4bac6-116"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac6-117">ClientMediaPortRangeEnabled</span><span class="sxs-lookup"><span data-stu-id="4bac6-117">ClientMediaPortRangeEnabled</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bac6-118">Portrange\MinMediaPort</span><span class="sxs-lookup"><span data-stu-id="4bac6-118">Portrange\MinMediaPort</span></span></p></td>
<td><p><span data-ttu-id="4bac6-119">指定要用于媒体的起始端口号。</span><span class="sxs-lookup"><span data-stu-id="4bac6-119">Specifies the starting port number to use for media.</span></span> <span data-ttu-id="4bac6-120">结合 MaxMediaPort 以指定端口的范围。</span><span class="sxs-lookup"><span data-stu-id="4bac6-120">Combines with MaxMediaPort to specify the range of ports.</span></span> <span data-ttu-id="4bac6-121">推荐的最小范围是40端口。</span><span class="sxs-lookup"><span data-stu-id="4bac6-121">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="4bac6-122"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="4bac6-122"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac6-123">ClientMediaPort (表示用于客户端媒体的起始端口号) </span><span class="sxs-lookup"><span data-stu-id="4bac6-123">ClientMediaPort (represents the starting port number to use for client media)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bac6-124">Portrange\MaxMediaPort</span><span class="sxs-lookup"><span data-stu-id="4bac6-124">Portrange\MaxMediaPort</span></span></p></td>
<td><p><span data-ttu-id="4bac6-125">指定要用于媒体的最大端口号。</span><span class="sxs-lookup"><span data-stu-id="4bac6-125">Specifies the highest port number to use for media.</span></span> <span data-ttu-id="4bac6-126">结合 MinMediaPort 以指定端口的范围。</span><span class="sxs-lookup"><span data-stu-id="4bac6-126">Combines with MinMediaPort to specify the range of ports.</span></span> <span data-ttu-id="4bac6-127">推荐的最小范围是40端口。</span><span class="sxs-lookup"><span data-stu-id="4bac6-127">The recommended minimum range is 40 ports.</span></span></p></td>
<td><p><span data-ttu-id="4bac6-128"><strong>CsConferencingConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="4bac6-128"><strong>CsConferencingConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="4bac6-129">ClientMediaPortRange (指示客户端介质的可用端口总数;默认值为 40) </span><span class="sxs-lookup"><span data-stu-id="4bac6-129">ClientMediaPortRange (indicates the total number of ports available for client media; default is 40)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-media-port-range-settings"></a><span data-ttu-id="4bac6-130">配置媒体端口范围设置</span><span class="sxs-lookup"><span data-stu-id="4bac6-130">To Configure Media Port Range Settings</span></span>

1.  <span data-ttu-id="4bac6-131">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="4bac6-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4bac6-132">运行以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="4bac6-132">Run the following cmdlet:</span></span>
    
        Get-CsConferencingConfiguration
    
    <span data-ttu-id="4bac6-133">此 cmdlet 返回会议配置设置。</span><span class="sxs-lookup"><span data-stu-id="4bac6-133">This cmdlet returns the conferencing configuration settings.</span></span>

3.  <span data-ttu-id="4bac6-134">运行以下 cmdlet，其中包含要更改的参数和值 (有关此 cmdlet 的参数的详细信息，请参阅 Lync Server Management Shell 文档) ：</span><span class="sxs-lookup"><span data-stu-id="4bac6-134">Run the following cmdlet with the parameters and values you want to change (for details about the parameters for this cmdlet, see the Lync Server Management Shell documentation):</span></span>
    
        Set-CsConferencingConfiguration
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4bac6-135">你可以为特定网站创建其他会议配置设置集。</span><span class="sxs-lookup"><span data-stu-id="4bac6-135">You can create additional sets of conferencing configuration settings for specific sites.</span></span> <span data-ttu-id="4bac6-136">将 <STRONG>CsConferencingConfiguration</STRONG> cmdlet 与网站标识结合使用。</span><span class="sxs-lookup"><span data-stu-id="4bac6-136">Use the <STRONG>New- CsConferencingConfiguration</STRONG> cmdlet with a site identity.</span></span> <span data-ttu-id="4bac6-137">为网站创建新的会议配置设置时，网站设置优先于全局设置。</span><span class="sxs-lookup"><span data-stu-id="4bac6-137">When you create new conferencing configuration settings for sites, the site settings take precedence over the global settings.</span></span> <span data-ttu-id="4bac6-138">有关详细信息，请参阅 Lync Server Management Shell 文档。</span><span class="sxs-lookup"><span data-stu-id="4bac6-138">For details, see the Lync Server Management Shell documentation.</span></span>

    
    <span data-ttu-id="4bac6-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4bac6-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

