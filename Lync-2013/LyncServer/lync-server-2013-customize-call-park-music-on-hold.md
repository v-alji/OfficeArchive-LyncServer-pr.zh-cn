---
title: Lync Server 2013：自定义呼叫寄存音乐暂候
description: Lync Server 2013：自定义呼叫寄存音乐处于暂候状态。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Customize Call Park music on hold
ms:assetid: 3d78e6f9-a4ae-49f4-a89f-4515acb49dac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688031(v=OCS.15)
ms:contentKeyID: 49733621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19219e4a77d4be4a18a43255e142339a4af6f463
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431377"
---
# <a name="customize-call-park-music-on-hold-in-lync-server-2013"></a><span data-ttu-id="0c798-103">在 Lync Server 2013 中自定义呼叫寄存音乐处于暂停状态</span><span class="sxs-lookup"><span data-stu-id="0c798-103">Customize Call Park music on hold in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c798-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c798-104">

<span> </span></span></span>

<span data-ttu-id="0c798-105">_**主题上次修改时间：** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="0c798-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="0c798-106">你可以指定自己的音乐文件用于保留音乐，而不是 Lync Server 2013 附带的默认音乐文件。</span><span class="sxs-lookup"><span data-stu-id="0c798-106">You can specify your own music file to use for music on hold, instead of the default music file that ships with Lync Server 2013.</span></span> <span data-ttu-id="0c798-107">若要自定义保留音乐，请使用 **Set-CsCallParkServiceMusicOnHoldFile** cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c798-107">To customize music on hold, use the **Set-CsCallParkServiceMusicOnHoldFile** cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0c798-108">如果你自定义暂停的音乐并希望同一音乐用于多个网站，则必须为运行呼叫驻留应用程序的每个网站配置音乐文件。</span><span class="sxs-lookup"><span data-stu-id="0c798-108">If you customize music on hold and want the same music for multiple sites, you must configure the music file for each site that runs the Call Park application.</span></span>



</div>

<div>

## <a name="to-customize-the-music-file"></a><span data-ttu-id="0c798-109">自定义音乐文件</span><span class="sxs-lookup"><span data-stu-id="0c798-109">To customize the music file</span></span>

1.  <span data-ttu-id="0c798-110">以 RTCUniversalServerAdmins 组成员的身份或必要的用户权限登录到安装了 Lync Server 管理外壳的计算机，如在 [Lync Server 2013 中的 "委派设置权限](lync-server-2013-delegate-setup-permissions.md)" 中所述。</span><span class="sxs-lookup"><span data-stu-id="0c798-110">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="0c798-111">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="0c798-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="0c798-112">运行：</span><span class="sxs-lookup"><span data-stu-id="0c798-112">Run:</span></span>
    
        Set-CsCallParkServiceMusicOnHoldFile -Service <ServiceID where the Call Park application resides> -Content <Byte[]>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="0c798-113">使用 <STRONG>Get-CsService</STRONG> cmdlet 可标识服务。</span><span class="sxs-lookup"><span data-stu-id="0c798-113">Use the <STRONG>Get-CsService</STRONG> cmdlet to identify the service.</span></span> <span data-ttu-id="0c798-114">有关详细信息，请参阅 <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsService">CsService</A>。</span><span class="sxs-lookup"><span data-stu-id="0c798-114">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsService">Get-CsService</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="0c798-115">以下示例说明了如何以字节数组的形式获取文件 soothingmusic.wma 的内容并将其分配给变量。</span><span class="sxs-lookup"><span data-stu-id="0c798-115">The following example shows how to obtain the contents of a file, soothingmusic.wma, as a byte array and assign it to a variable.</span></span> <span data-ttu-id="0c798-116">然后，将音频文件指定为呼叫寄存的保留音乐文件。</span><span class="sxs-lookup"><span data-stu-id="0c798-116">Then the audio file is assigned as the music-on-hold file for Call Park.</span></span> <span data-ttu-id="0c798-117">有关详细信息，请参阅 [Set-CsCallParkServiceMusicOnHoldFile](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkServiceMusicOnHoldFile)。</span><span class="sxs-lookup"><span data-stu-id="0c798-117">For details, see [Set-CsCallParkServiceMusicOnHoldFile](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkServiceMusicOnHoldFile).</span></span>
    
        $a = Get-Content -ReadCount 0 -Encoding byte "C:\MoHFiles\soothingmusic.wma"
        Set-CsCallParkServiceMusicOnHoldFile -Service Redmond1-applicationserver-1 -Content $a

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0c798-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c798-118">See Also</span></span>


[<span data-ttu-id="0c798-119">Set-CsCallParkServiceMusicOnHoldFile</span><span class="sxs-lookup"><span data-stu-id="0c798-119">Set-CsCallParkServiceMusicOnHoldFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkServiceMusicOnHoldFile)  
[<span data-ttu-id="0c798-120">CsService</span><span class="sxs-lookup"><span data-stu-id="0c798-120">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="0c798-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c798-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

