---
title: Lync Server 2013： Lync PreCall 诊断工具
description: Lync Server 2013： Lync PreCall 诊断工具。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync PreCall Diagnostics Tool
ms:assetid: 0ff291ec-cfb4-43eb-b5d6-a7a325681e3f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn451255(v=OCS.15)
ms:contentKeyID: 56708404
ms.date: 11/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c2c51551fe0991eb354a628b1d4660baa1532b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426322"
---
# <a name="lync-precall-diagnostics-tool-in-lync-server-2013"></a><span data-ttu-id="ac60a-103">Lync Server 2013 中的 lync PreCall 诊断工具</span><span class="sxs-lookup"><span data-stu-id="ac60a-103">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac60a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac60a-104">

<span> </span></span></span>

<span data-ttu-id="ac60a-105">_**主题上次修改时间：** 2016-11-04_</span><span class="sxs-lookup"><span data-stu-id="ac60a-105">_**Topic Last Modified:** 2016-11-04_</span></span>

<span data-ttu-id="ac60a-106">Lync PreCall 诊断工具 (PCD) 是基于客户端的应用程序，可让你查看网络的当前状态如何影响未来的企业语音通话中的音频质量。</span><span class="sxs-lookup"><span data-stu-id="ac60a-106">The Lync PreCall Diagnostics Tool (PCD) is a client-based application that allows you to see how the current state of your network might impact the audio quality in an upcoming Enterprise Voice call.</span></span>

<span data-ttu-id="ac60a-107">PCD 在网络的最后一个跃点可能是最 (弱的情况下（例如，使用公共 WiFi 网络或家庭用户) 上的膝上型电脑）时，非常有用。</span><span class="sxs-lookup"><span data-stu-id="ac60a-107">PCD is most useful in situations where the last hop of a network is likely to be the weakest (for example, with laptops on a public WiFi network or home users).</span></span> <span data-ttu-id="ac60a-108">PCD 创建一个小型数据包流，该流遍历网络的这最后一条路。</span><span class="sxs-lookup"><span data-stu-id="ac60a-108">PCD creates a small packet stream that traverses this final leg of the network.</span></span> <span data-ttu-id="ac60a-109">然后，该工具将分析数据包流，以估计沿此段腿的抖动和损失可能会影响呼叫质量，然后提供报告。</span><span class="sxs-lookup"><span data-stu-id="ac60a-109">The tool then analyzes the packet stream to estimate how the jitter and loss along this leg might impact call quality, and then provides a report.</span></span> <span data-ttu-id="ac60a-110">你可以在客户端上持续运行 PCD，即使在通话时也是如此。</span><span class="sxs-lookup"><span data-stu-id="ac60a-110">You can run PCD continuously on the client, even while calls are being placed.</span></span> <span data-ttu-id="ac60a-111">数据包流对带宽没有显著影响。</span><span class="sxs-lookup"><span data-stu-id="ac60a-111">The packet stream does not have a significant effect on bandwidth.</span></span>

<span data-ttu-id="ac60a-112">**PCD 版本1.1 的最新版本包括以下增强功能：**</span><span class="sxs-lookup"><span data-stu-id="ac60a-112">**The latest release of the PCD, version 1.1, includes the following enhancements:**</span></span>

  - <span data-ttu-id="ac60a-113">支持较长的密码，该密码现在最多可达127个字符</span><span class="sxs-lookup"><span data-stu-id="ac60a-113">Support for longer passwords, which can now be up to 127 characters</span></span>

  - <span data-ttu-id="ac60a-114">针对身份验证登录问题的其他诊断</span><span class="sxs-lookup"><span data-stu-id="ac60a-114">Additional diagnostics for authentication sign-in issues</span></span>

  - <span data-ttu-id="ac60a-115">更好地支持 Lync 混合部署</span><span class="sxs-lookup"><span data-stu-id="ac60a-115">Better support for Lync hybrid deployments</span></span>

  - <span data-ttu-id="ac60a-116">对凭据选取器的更新</span><span class="sxs-lookup"><span data-stu-id="ac60a-116">Updates to credential picker</span></span>

  - <span data-ttu-id="ac60a-117">稳定性改进</span><span class="sxs-lookup"><span data-stu-id="ac60a-117">Stability improvements</span></span>

<span data-ttu-id="ac60a-118">我们非常感谢您的反馈。</span><span class="sxs-lookup"><span data-stu-id="ac60a-118">We appreciate any feedback.</span></span> <span data-ttu-id="ac60a-119">请将所有支持问题或问题发送到 [PCD 反馈](mailto:pcdfb@microsoft.com) 别名 <pcdfb@microsoft.com> 。</span><span class="sxs-lookup"><span data-stu-id="ac60a-119">Please send all support questions or issues to the [PCD Feedback](mailto:pcdfb@microsoft.com) alias at <pcdfb@microsoft.com>.</span></span>

<span data-ttu-id="ac60a-120">本主题包括以下部分：</span><span class="sxs-lookup"><span data-stu-id="ac60a-120">This topic includes the following sections:</span></span>

  - <span data-ttu-id="ac60a-121">Lync PCD 版本</span><span class="sxs-lookup"><span data-stu-id="ac60a-121">Lync PCD Versions</span></span>

  - <span data-ttu-id="ac60a-122">Lync PCD 系统要求</span><span class="sxs-lookup"><span data-stu-id="ac60a-122">Lync PCD System Requirements</span></span>

  - <span data-ttu-id="ac60a-123">Lync PCD 功能</span><span class="sxs-lookup"><span data-stu-id="ac60a-123">Lync PCD Features</span></span>

  - <span data-ttu-id="ac60a-124">运行 Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ac60a-124">Running Lync PCD</span></span>

  - <span data-ttu-id="ac60a-125">卸载 Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ac60a-125">Uninstalling Lync PCD</span></span>

<span id="Version"></span>

<div>

## <a name="lync-pcd-versions"></a><span data-ttu-id="ac60a-126">Lync PCD 版本</span><span class="sxs-lookup"><span data-stu-id="ac60a-126">Lync PCD Versions</span></span>

<span data-ttu-id="ac60a-127">本主题介绍以下版本的工具，可供免费下载：</span><span class="sxs-lookup"><span data-stu-id="ac60a-127">This topic describes the following versions of the tool, available for free download:</span></span>

  - <span data-ttu-id="ac60a-128">Windows 桌面应用 ([https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914)) </span><span class="sxs-lookup"><span data-stu-id="ac60a-128">Windows Desktop App ([https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914))</span></span>

</div>

<span id="Requirements"></span>

<div>

## <a name="lync-pcd-system-requirements"></a><span data-ttu-id="ac60a-129">Lync PCD 系统要求</span><span class="sxs-lookup"><span data-stu-id="ac60a-129">Lync PCD System Requirements</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ac60a-130">PCD 要求在 Lync Server 部署中安装和配置统一通信 Web API () UCWA 以支持移动客户端。</span><span class="sxs-lookup"><span data-stu-id="ac60a-130">PCD requires that Unified Communications Web API (UCWA) be installed and configured to support mobile clients in the Lync Server deployment.</span></span> <span data-ttu-id="ac60a-131">UCWA 与 Lync Server 一起安装。</span><span class="sxs-lookup"><span data-stu-id="ac60a-131">UCWA is installed with Lync Server.</span></span>



</div>

<div>

## <a name="windows-desktop-app-requirements"></a><span data-ttu-id="ac60a-132">Windows 桌面应用要求</span><span class="sxs-lookup"><span data-stu-id="ac60a-132">Windows Desktop App Requirements</span></span>

  - <span data-ttu-id="ac60a-133">Windows 7 或 Windows 8 操作系统的任何版本</span><span class="sxs-lookup"><span data-stu-id="ac60a-133">Any edition of the Windows 7 or Windows 8 operating system</span></span>

  - <span data-ttu-id="ac60a-134">Microsoft .NET Framework 4.5 可在 [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span><span class="sxs-lookup"><span data-stu-id="ac60a-134">Microsoft .NET Framework 4.5 available at [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span></span>

</div>

</div>

<span id="features"></span>

<div>

## <a name="lync-pcd-features"></a><span data-ttu-id="ac60a-135">Lync PCD 功能</span><span class="sxs-lookup"><span data-stu-id="ac60a-135">Lync PCD Features</span></span>

<span data-ttu-id="ac60a-136">Lync PCD 包括以下功能：</span><span class="sxs-lookup"><span data-stu-id="ac60a-136">Lync PCD includes the following features:</span></span>

  - <span data-ttu-id="ac60a-137">默认按需运行 (2 分钟的猝发) </span><span class="sxs-lookup"><span data-stu-id="ac60a-137">Run in default On Demand (2 minute bursts)</span></span>

  - <span data-ttu-id="ac60a-138">在 "已对齐" 视图) 模式下运行的始终 (最多24小时</span><span class="sxs-lookup"><span data-stu-id="ac60a-138">Run in Always On (up to 24 hours in snapped view) mode</span></span>

  - <span data-ttu-id="ac60a-139">测试运行的历史视图</span><span class="sxs-lookup"><span data-stu-id="ac60a-139">Historical view of your test runs</span></span>

  - <span data-ttu-id="ac60a-140">仅诊断 (Lync PCD for Windows 8 的登录失败) </span><span class="sxs-lookup"><span data-stu-id="ac60a-140">Diagnose sign-in failures (Lync PCD for Windows 8 only)</span></span>

<span data-ttu-id="ac60a-141">![Lync PCD 功能登录进度屏幕截图](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Lync PCD 功能登录进度屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="ac60a-141">![Lync PCD features Sign in progress screen shot](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Lync PCD features Sign in progress screen shot")</span></span>

  - <span data-ttu-id="ac60a-142">网络指标的图形化视图-以全屏和贴靠视图显示网络 MOS、数据包丢失和 Interarrival 抖动。</span><span class="sxs-lookup"><span data-stu-id="ac60a-142">Graphical view of network metrics – Network MOS, Packet Loss and Interarrival Jitter in full screen and snapped view.</span></span>

<span data-ttu-id="ac60a-143">**全屏视图**</span><span class="sxs-lookup"><span data-stu-id="ac60a-143">**Full screen view**</span></span>

<span data-ttu-id="ac60a-144">![PreCall Diagnostic 工具测试结果图](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "PreCall Diagnostic 工具测试结果图")</span><span class="sxs-lookup"><span data-stu-id="ac60a-144">![PreCall Diagnostic Tool test result graphs](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "PreCall Diagnostic Tool test result graphs")</span></span>

<span data-ttu-id="ac60a-145">**贴靠视图**</span><span class="sxs-lookup"><span data-stu-id="ac60a-145">**Snapped view**</span></span>

<span data-ttu-id="ac60a-146">![PreCall Diagnostic 工具利用率测试结果](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "PreCall Diagnostic 工具利用率测试结果")</span><span class="sxs-lookup"><span data-stu-id="ac60a-146">![PreCall Diagnostic Tool Utilization test results](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "PreCall Diagnostic Tool Utilization test results")</span></span>

</div>

<span id="running"></span>

<div>

## <a name="running-lync-pcd"></a><span data-ttu-id="ac60a-147">运行 Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ac60a-147">Running Lync PCD</span></span>

<div>

## <a name="running-windows-desktop-app"></a><span data-ttu-id="ac60a-148">运行 Windows 桌面应用</span><span class="sxs-lookup"><span data-stu-id="ac60a-148">Running Windows Desktop App</span></span>

1.  <span data-ttu-id="ac60a-149">若要在 Windows 7 系统上启动 PCD，请从 "**开始**" 菜单中选择 " **PreCall 诊断**"。</span><span class="sxs-lookup"><span data-stu-id="ac60a-149">To start the PCD on a Windows 7 system, select **PreCall Diagnostics** from the **Start** menu.</span></span>
    
    <span data-ttu-id="ac60a-150">若要在 Windows 8 系统上启动 PCD，请在 "开始" 屏幕上选择该图标，或搜索 "PreCall Diagnostics"。</span><span class="sxs-lookup"><span data-stu-id="ac60a-150">To start the PCD on a Windows 8 system, select the icon on your Start screen, or search for “PreCall Diagnostics.”</span></span>
    
    <span data-ttu-id="ac60a-151">![PreCall Diagnostic 工具图标](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "PreCall Diagnostic 工具图标")</span><span class="sxs-lookup"><span data-stu-id="ac60a-151">![PreCall Diagnostic tool icon](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "PreCall Diagnostic tool icon")</span></span>

2.  <span data-ttu-id="ac60a-152">当工具启动时，选择提供凭据的首选方法，然后在 " **PreCall 诊断工具选项** " 对话框中选择 "网络操作模式"，然后选择 **"确定"**：</span><span class="sxs-lookup"><span data-stu-id="ac60a-152">When the tool starts, select your preferred method of providing credentials and select the network operating mode in the **PreCall Diagnostics Tool Options** dialog box, then select **OK**:</span></span>

3.  <span data-ttu-id="ac60a-153">选择 " **开始测试** " 按钮以开始运行诊断。</span><span class="sxs-lookup"><span data-stu-id="ac60a-153">Select the **Start Test** button to start running diagnostics.</span></span>
    
    <span data-ttu-id="ac60a-154">如果选择 " **使用网络凭据** " 选项，测试将立即开始。</span><span class="sxs-lookup"><span data-stu-id="ac60a-154">If you selected the **Use network credentials** option, the test begins immediately.</span></span>
    
    <span data-ttu-id="ac60a-155">如果选择 " **让我输入我的凭据** " 选项，则会打开 " **Windows 安全** " 对话框。</span><span class="sxs-lookup"><span data-stu-id="ac60a-155">If you selected the **Let me enter my credentials** option, the **Windows Security** dialog box opens.</span></span> <span data-ttu-id="ac60a-156">输入凭据后，测试开始。</span><span class="sxs-lookup"><span data-stu-id="ac60a-156">After you enter your credentials, the test starts.</span></span>

</div>

</div>

<span id="uninstall"></span>

<div>

## <a name="uninstalling-lync-pcd"></a><span data-ttu-id="ac60a-157">卸载 Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ac60a-157">Uninstalling Lync PCD</span></span>

<span data-ttu-id="ac60a-158">若要删除 Lync PCD，请按照操作系统的步骤进行操作：</span><span class="sxs-lookup"><span data-stu-id="ac60a-158">To remove Lync PCD, follow the procedure for your operating system:</span></span>

  - <span data-ttu-id="ac60a-159">在 Windows 7 系统上，打开 " **控制面板**"，选择 " **程序和功能**"，然后双击 " **Lync 2013 PreCall 诊断**"。</span><span class="sxs-lookup"><span data-stu-id="ac60a-159">On a Windows 7 system, open the **Control Panel**, select **Programs and Features**, and double-click **Lync 2013 PreCall Diagnostics**.</span></span>

  - <span data-ttu-id="ac60a-160">在 Windows 8 系统上，右键单击 "PCD" 磁贴，然后单击 "开始" 屏幕底部的应用栏中的 " **卸载** "。</span><span class="sxs-lookup"><span data-stu-id="ac60a-160">On a Windows 8 system, right-click on the PCD tile and click **Uninstall** from the app bar at the bottom of the start screen.</span></span>

<span data-ttu-id="ac60a-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac60a-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

