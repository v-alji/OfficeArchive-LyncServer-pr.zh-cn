---
title: Lync Server 2013：（可选）验证电话拨入式会议
description: Lync Server 2013： (可选) 验证电话拨入式会议。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify dial-in conferencing
ms:assetid: 3e2b4220-8fb3-442f-98b1-78447adb321f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425905(v=OCS.15)
ms:contentKeyID: 48183941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5e8d3734e89555bf4b298ac68e1e3bd67b1d901
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424854"
---
# <a name="optional-verify-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="f0afb-103">（可选）在 Lync Server 2013 中验证电话拨入式会议</span><span class="sxs-lookup"><span data-stu-id="f0afb-103">(Optional) Verify dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0afb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0afb-104">

<span> </span></span></span>

<span data-ttu-id="f0afb-105">_**主题上次修改时间：** 2011-01-21_</span><span class="sxs-lookup"><span data-stu-id="f0afb-105">_**Topic Last Modified:** 2011-01-21_</span></span>

<span data-ttu-id="f0afb-106">要验证“电话拨入式会议设置”网页和拨入访问号码是否工作正常，您需要执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="f0afb-106">To verify that the Dial-in Conferencing Settings webpage and the dial-in access numbers work correctly, you need to do the following:</span></span>

  - <span data-ttu-id="f0afb-107">通过登录简单 URL 来测试“电话拨入式会议设置”网页。</span><span class="sxs-lookup"><span data-stu-id="f0afb-107">Test the Dial-in Conferencing Settings webpage by signing in to the simple URL.</span></span>

  - <span data-ttu-id="f0afb-p101">通过运行本主题后面的脚本来测试该访问号码在特定池中是否工作正常。此脚本模拟对访问号码的呼叫。要使用此脚本，需要提供该特定池承载的一个统一通信 (UC) 客户端的 SIP 地址和凭据。</span><span class="sxs-lookup"><span data-stu-id="f0afb-p101">Test that access numbers work correctly for a specific pool by running the script later in this topic. This script simulates calls to access numbers. You need the SIP address and credentials of one unified communications (UC) client that is hosted on the specific pool to use this script.</span></span>

<span data-ttu-id="f0afb-111">此步骤是可选的。</span><span class="sxs-lookup"><span data-stu-id="f0afb-111">This step is optional.</span></span>

<div>

## <a name="to-test-access-numbers-for-a-specific-pool"></a><span data-ttu-id="f0afb-112">测试特定池的访问号码</span><span class="sxs-lookup"><span data-stu-id="f0afb-112">To test access numbers for a specific pool</span></span>

1.  <span data-ttu-id="f0afb-113">以 RTCUniversalServerAdmins 组成员的身份登录计算机，或者作为 **Cs-ServerAdministrator** 或 **CsAdministrator** 角色的成员登录到计算机。</span><span class="sxs-lookup"><span data-stu-id="f0afb-113">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="f0afb-114">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="f0afb-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f0afb-115">在命令提示符下，运行以下内容：</span><span class="sxs-lookup"><span data-stu-id="f0afb-115">Run the following at the command prompt:</span></span>
    
        $credentials = Get-Credential
           User name:  testuser1@contoso.com
           Password:   ********
        Test-CsDialInConferencing -UserSipAddress sip:testuser1@contoso.com -UserCredential $credentials -TargetFqdn <serverName>.<domainName>.com -Verbose
    
    <span data-ttu-id="f0afb-p102">得出的报告将显示 Success 或 Failure，以及具体的诊断信息。–Verbose 标志提供有关查找到的访问号码数目及其详细信息的更多详情。</span><span class="sxs-lookup"><span data-stu-id="f0afb-p102">The resulting report shows either Success or Failure, along with specific diagnostic information. The –Verbose flag provides more detailed information about how many access numbers were found and details about them.</span></span>

<span data-ttu-id="f0afb-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0afb-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

