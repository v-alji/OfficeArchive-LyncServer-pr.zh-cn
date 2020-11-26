---
title: Lync Server 2013：配置公共提供商的媒体加密
description: Lync Server 2013：为公共提供程序配置媒体加密。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media encryption for public providers
ms:assetid: a95814cf-c5a9-4652-8ffc-c469a2653153
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205149(v=OCS.15)
ms:contentKeyID: 48185036
ms.date: 12/13/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 177c19f151b67d741c7e26506f7ebc98b3ce831a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433883"
---
# <a name="configure-media-encryption-for-public-providers-in-lync-server-2013"></a><span data-ttu-id="30dc1-103">在 Lync Server 2013 中配置公共提供商的媒体加密</span><span class="sxs-lookup"><span data-stu-id="30dc1-103">Configure media encryption for public providers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30dc1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30dc1-104">

<span> </span></span></span>

<span data-ttu-id="30dc1-105">_**主题上次修改时间：** 2014-12-12_</span><span class="sxs-lookup"><span data-stu-id="30dc1-105">_**Topic Last Modified:** 2014-12-12_</span></span>

<span data-ttu-id="30dc1-106">如果你要使用 Windows Live Messenger 实现音频/视频 (A/V) 联盟，则需要修改两个参数： Lync Server 加密级别和 EnablePublicCloudAccess 策略。</span><span class="sxs-lookup"><span data-stu-id="30dc1-106">If you are implementing audio/video (A/V) federation with Windows Live Messenger, there are two parameters that you need to modify: the Lync Server encryption level and the EnablePublicCloudAccess policy.</span></span> <span data-ttu-id="30dc1-107">默认情况下，加密级别设置为 "必需"。</span><span class="sxs-lookup"><span data-stu-id="30dc1-107">By default, the encryption level is set to Required.</span></span> <span data-ttu-id="30dc1-108">必须将此设置更改为 "支持"。</span><span class="sxs-lookup"><span data-stu-id="30dc1-108">You must change this setting to Supported.</span></span> <span data-ttu-id="30dc1-109">如果 EnablePublicCloudAccess 策略设置为 false，则需要将其设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="30dc1-109">If the EnablePublicCloudAccess policy is set to false, this needs to be set to **True**.</span></span> <span data-ttu-id="30dc1-110">你可以从 Lync Server 命令行管理程序中执行此操作。</span><span class="sxs-lookup"><span data-stu-id="30dc1-110">You can do this from the Lync Server Management Shell.</span></span>

<div>

## <a name="configure-federation-for-windows-live"></a><span data-ttu-id="30dc1-111">为 Windows Live 配置联合</span><span class="sxs-lookup"><span data-stu-id="30dc1-111">Configure Federation for Windows Live</span></span>

1.  <span data-ttu-id="30dc1-112">在前端服务器上启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management Shell**"。</span><span class="sxs-lookup"><span data-stu-id="30dc1-112">Start the Lync Server Management Shell on the Front End server: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="30dc1-113">在命令提示符处，键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="30dc1-113">From the command prompt, type the following commands:</span></span>
    
       ```powershell
        Set-CsMediaConfiguration -EncryptionLevel SupportEncryption
       ```
    
       ```powershell
        Set-CsExternalAccessPolicy Global -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true
       ```
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="30dc1-114">这是必需的步骤，因为 Windows Live Messenger 不支持音频/视频加密。</span><span class="sxs-lookup"><span data-stu-id="30dc1-114">This is required step because Windows Live Messenger does not support encryption of audio/video.</span></span> <span data-ttu-id="30dc1-115">该命令将你的全局策略设置为支持加密设置，而不是需要加密音频/视频数据。</span><span class="sxs-lookup"><span data-stu-id="30dc1-115">The command sets your global policy to a support encryption setting instead of requiring encryption of the audio/video data.</span></span> <span data-ttu-id="30dc1-116">支持加密的客户仍将使用加密，如 Lync 2013。</span><span class="sxs-lookup"><span data-stu-id="30dc1-116">Clients that support encryption will still use encryption, such as Lync 2013.</span></span>

    
    <span data-ttu-id="30dc1-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30dc1-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

