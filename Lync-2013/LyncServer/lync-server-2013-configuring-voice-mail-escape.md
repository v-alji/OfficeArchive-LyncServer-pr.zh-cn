---
title: Lync Server 2013：配置语音邮件转义
description: Lync Server 2013：配置语音邮件转义。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring voice mail escape
ms:assetid: a1d19e6c-82ff-4768-8ae5-da981368ce40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688157(v=OCS.15)
ms:contentKeyID: 49733761
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afbb2dd10c7ff8809eb8dfbcc64e40a599aa06a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432399"
---
# <a name="configuring-voice-mail-escape-in-lync-server-2013"></a><span data-ttu-id="afbe9-103">在 Lync Server 2013 中配置语音邮件转义</span><span class="sxs-lookup"><span data-stu-id="afbe9-103">Configuring voice mail escape in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="afbe9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="afbe9-104">

<span> </span></span></span>

<span data-ttu-id="afbe9-105">_**主题上次修改时间：** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="afbe9-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="afbe9-106">如果用户为移动电话配置同时响铃，则当移动电话关机、没电或没信号时，呼叫者通常将路由到用户的个人语音邮件。</span><span class="sxs-lookup"><span data-stu-id="afbe9-106">When a user configures simultaneous ringing to a mobile phone, a caller will typically be routed to the user’s personal voice mail if the mobile phone is turned off, out of battery power, or out of range.</span></span> <span data-ttu-id="afbe9-107">使用 Lync Server 2013，用户可以选择将与业务相关的呼叫路由到其企业语音邮件系统。</span><span class="sxs-lookup"><span data-stu-id="afbe9-107">With Lync Server 2013, users can opt to have business-related calls routed to their corporate voice mail system.</span></span> <span data-ttu-id="afbe9-108">具体而言，可以配置计时器，并且如果由运营商的语音邮件在定义的时间范围内接听呼叫，则 Lync Server 将断开运营商的语音邮件系统与运营商的语音邮件系统的连接 (和用户的个人语音邮件) ，而用户在公司系统中的剩余终结点将继续拨打。</span><span class="sxs-lookup"><span data-stu-id="afbe9-108">Specifically, a timer can be configured, and if the call is answered by the carrier’s voice mail within the range of time defined, Lync Server will disconnect from the carrier’s voice mail system (and the user’s personal voice mail), while the user’s remaining endpoints in the corporate system continue to ring.</span></span> <span data-ttu-id="afbe9-109">这样以来，呼叫者将自动路由到用户的企业语音邮件。</span><span class="sxs-lookup"><span data-stu-id="afbe9-109">This way, the caller is automatically routed to the user’s corporate voice mail.</span></span>

<span data-ttu-id="afbe9-110">使用以下参数在语音策略级别上使用 Lync Server Management Shell cmdlet （ **CsVoicePolicy**）执行此配置。</span><span class="sxs-lookup"><span data-stu-id="afbe9-110">This configuration is performed using the Lync Server Management Shell cmdlet, **Set-CsVoicePolicy**, at the voice policy level, with the following parameters.</span></span>

<div>

## <a name="to-configure-voice-mail-escape"></a><span data-ttu-id="afbe9-111">配置语音邮件转义</span><span class="sxs-lookup"><span data-stu-id="afbe9-111">To configure voice mail escape</span></span>

1.  <span data-ttu-id="afbe9-112">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="afbe9-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="afbe9-113">指定 **Set-CsVoicePolicy** 的以下参数：</span><span class="sxs-lookup"><span data-stu-id="afbe9-113">Specify the following parameters to **Set-CsVoicePolicy**:</span></span>
    
      - <span data-ttu-id="afbe9-114">**EnableVoicemailEscapeTimer** - 启用或禁用转义计时器。</span><span class="sxs-lookup"><span data-stu-id="afbe9-114">**EnableVoicemailEscapeTimer** - Enables or disables the escape timer.</span></span>
    
      - <span data-ttu-id="afbe9-p102">**PSTNVoicemailEscapeTimer** - 指定超时值（以毫秒为单位）。默认值为 1500 毫秒，该值的范围可介于 0 到 8000 毫秒之间。</span><span class="sxs-lookup"><span data-stu-id="afbe9-p102">**PSTNVoicemailEscapeTimer** - Specifies the timeout value in milliseconds. The default value is 1500 milliseconds, and the value can range from 0 milliseconds to 8000 milliseconds.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="afbe9-117">示例</span><span class="sxs-lookup"><span data-stu-id="afbe9-117">Example</span></span>

    Set-CsVoicePolicy UserVoicePolicy -EnableVoiceMailEscapeTimer $true - PSTNVoicemailEscapeTimer 2000
    
    Set-CsVoicePolicy -Identity site:SitePolicy -EnableVoiceMailEscapeTimer $true -PSTNVoicemailEscapeTimer 1500

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="afbe9-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="afbe9-118">See Also</span></span>


[<span data-ttu-id="afbe9-119">在 Lync Server 2013 中配置语音策略和 PSTN 用法记录以授权呼叫功能和权限</span><span class="sxs-lookup"><span data-stu-id="afbe9-119">Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md)  
  

<span data-ttu-id="afbe9-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="afbe9-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

