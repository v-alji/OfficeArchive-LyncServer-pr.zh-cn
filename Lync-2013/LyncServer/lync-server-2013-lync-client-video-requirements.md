---
title: Lync Server 2013： Lync 客户端视频要求
description: Lync Server 2013： Lync 客户端视频要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync client video requirements
ms:assetid: 8f68f4c2-3194-487c-bd2f-fbe71ba8ad70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688132(v=OCS.15)
ms:contentKeyID: 49733731
ms.date: 01/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea1d4a993650ec8102d8b66ea5aa936ad1613f20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426436"
---
# <a name="lync-client-video-requirements-for-lync-server-2013"></a><span data-ttu-id="18b75-103">Lync Server 2013 的 lync 客户端视频要求</span><span class="sxs-lookup"><span data-stu-id="18b75-103">Lync client video requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18b75-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18b75-104">

<span> </span></span></span>

<span data-ttu-id="18b75-105">_**主题上次修改时间：** 2016-01-29_</span><span class="sxs-lookup"><span data-stu-id="18b75-105">_**Topic Last Modified:** 2016-01-29_</span></span>

<span data-ttu-id="18b75-106">本部分介绍了 Lync 2013 视频通话的视频硬件支持，并介绍如何确定各种计算机、平板电脑和移动设备配置的预期视频质量。</span><span class="sxs-lookup"><span data-stu-id="18b75-106">This section describes video hardware support for Lync 2013 video calls and describes how to determine the expected video quality for various computer, tablet, and mobile device configurations.</span></span>

<div>

## <a name="windows-desktop-and-tablet-video-requirements-and-capabilities"></a><span data-ttu-id="18b75-107">Windows 桌面和平板电脑视频要求和功能</span><span class="sxs-lookup"><span data-stu-id="18b75-107">Windows Desktop and Tablet Video Requirements and Capabilities</span></span>

<span data-ttu-id="18b75-108">Lync 2013 引入了基于 H： 264/MPEG-4 第10部分高级视频编码标准的视频编码和解码的硬件加速。</span><span class="sxs-lookup"><span data-stu-id="18b75-108">Lync 2013 introduces hardware acceleration for video encoding and decoding based on the H.264/MPEG-4 Part 10 Advanced Video Coding standard.</span></span> <span data-ttu-id="18b75-109">利用此功能，CPU 时钟速度较慢的计算机可对分辨率较高的视频进行编码和解码。</span><span class="sxs-lookup"><span data-stu-id="18b75-109">This feature allows computers with lower CPU clock speeds to encode and decode higher resolution video.</span></span> <span data-ttu-id="18b75-110">视频硬件要求随计算机配置和所需的视频分辨率的不同而不同。</span><span class="sxs-lookup"><span data-stu-id="18b75-110">Video hardware requirements vary depending on the computer configuration and the video resolution wanted.</span></span>

<div>

## <a name="video-hardware-requirements"></a><span data-ttu-id="18b75-111">视频硬件要求</span><span class="sxs-lookup"><span data-stu-id="18b75-111">Video Hardware Requirements</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18b75-112">功能</span><span class="sxs-lookup"><span data-stu-id="18b75-112">Feature</span></span></th>
<th><span data-ttu-id="18b75-113">要求</span><span class="sxs-lookup"><span data-stu-id="18b75-113">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18b75-114">使用 DirectX 视频加速 (DXVA) 的硬件加速 H.264 解码</span><span class="sxs-lookup"><span data-stu-id="18b75-114">Hardware accelerated H.264 decoding using DirectX Video Acceleration (DXVA)</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="18b75-115">显卡必须支持 DirectX 9.0 且必须公开 DXVA2_ModeH264_VLD_NoFGT 解码模式。</span><span class="sxs-lookup"><span data-stu-id="18b75-115">Graphics card must support DirectX 9.0 and must expose the DXVA2_ModeH264_VLD_NoFGT decoding mode.</span></span></p></li>
<li><p><span data-ttu-id="18b75-116">必须安装最新的显卡驱动程序。</span><span class="sxs-lookup"><span data-stu-id="18b75-116">The latest graphics card driver must be installed.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="18b75-117">有关解码模式的详细信息，请参阅 <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A> 。</span><span class="sxs-lookup"><span data-stu-id="18b75-117">For details about decoding modes, see <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A>.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-118">硬件加速 H.264 编码：芯片集要求</span><span class="sxs-lookup"><span data-stu-id="18b75-118">Hardware accelerated H.264 encoding: Chipset Requirements</span></span></p></td>
<td><p><span data-ttu-id="18b75-119">支持以下 Intel 硬件加速视频编码解决方案：</span><span class="sxs-lookup"><span data-stu-id="18b75-119">The following Intel hardware accelerated video encoding solutions are supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="18b75-120">第二和第三代英特尔高质图形2000、2500、3000和4000芯片组 (或更高版本，) 集成的硬件视频编码器。</span><span class="sxs-lookup"><span data-stu-id="18b75-120">Second and third generation Intel HD Graphics 2000, 2500, 3000, and 4000 chipsets (or later versions) with integrated hardware video encoders.</span></span> <span data-ttu-id="18b75-121">需要安装 Intel 高清显卡驱动程序 15.28.9.2884 或包含以下内容的最新驱动程序：</span><span class="sxs-lookup"><span data-stu-id="18b75-121">Installation of the Intel HD Graphics driver 15.28.9.2884 or the latest driver containing the following is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="18b75-122">显示驱动程序 9.17.10.2884 或最新驱动程序</span><span class="sxs-lookup"><span data-stu-id="18b75-122">Display driver 9.17.10.2884 or the latest driver</span></span></p></li>
<li><p><span data-ttu-id="18b75-123">硬件媒体基础转换 (HMFT) 版本 3.12.10.31 或最新 HMFT</span><span class="sxs-lookup"><span data-stu-id="18b75-123">Hardware media foundation transform (HMFT) version 3.12.10.31 or the latest HMFT</span></span></p></li>
</ul></li>
</ul>
<p><span data-ttu-id="18b75-124">支持以下 AMD 硬件加速视频编码解决方案 (需要 Lync Server 2013) 更新 CU1：</span><span class="sxs-lookup"><span data-stu-id="18b75-124">The following AMD hardware accelerated video encoding solutions are supported (requires CU1 Updates for Lync Server 2013):</span></span></p>
<ul>
<li><p><span data-ttu-id="18b75-p103">AMD 视频编解码引擎，在许多不同的显卡和 AMD A 系列加速处理器的集成加速处理单元中提供。必须安装 AMD 视频编解码引擎驱动程序 9.12.0.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="18b75-p103">AMD Video Codec Engine, which is available in several discrete graphics cards and in integrated accelerated processing units of AMD A-Series Accelerated Processors. The AMD Video Codec Engine driver 9.12.0.0 or higher must be installed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b75-127">硬件加速 H.264 编码：摄像机要求</span><span class="sxs-lookup"><span data-stu-id="18b75-127">Hardware accelerated H.264 encoding: Camera Requirements</span></span></p></td>
<td><p><span data-ttu-id="18b75-128">具有符合 USB Video Class (UVC) 规格版本 1.5 的集成 H.264 硬件编码器的 USB 视频摄像机。</span><span class="sxs-lookup"><span data-stu-id="18b75-128">USB video cameras with integrated H.264 hardware encoder that conforms to the USB Video Class (UVC) specification version 1.5.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="18b75-129">Lync 2013 支持带有 Windows 8 或 Windows 8.1 的 UVC 1.5 摄像头，其中包括对 UVC 1.5 的支持。</span><span class="sxs-lookup"><span data-stu-id="18b75-129">Lync 2013 supports UVC 1.5 cameras with Windows 8 or Windows 8.1, which includes support for UVC 1.5.</span></span> <span data-ttu-id="18b75-130">由于 Windows 7 不包括对 UVC 1.5 的支持，因此 Lync 2013 将 UVC 1.5 相机视为不支持硬件编码的常规相机。</span><span class="sxs-lookup"><span data-stu-id="18b75-130">Because Windows 7 does not include support for UVC 1.5, Lync 2013 treats UVC 1.5 cameras as regular cameras with no hardware encoding support.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="determining-h264-video-encoding-and-decoding-capabilities"></a><span data-ttu-id="18b75-131">确定 H-p 视频编码和解码功能</span><span class="sxs-lookup"><span data-stu-id="18b75-131">Determining H.264 Video Encoding and Decoding Capabilities</span></span>

<span data-ttu-id="18b75-132">通常，存在确定特定计算机配置的最大编码和解码功能的四大因素：</span><span class="sxs-lookup"><span data-stu-id="18b75-132">Generally, there are four major factors that determine the maximum encoding and decoding capability of a particular computer configuration:</span></span>

  - <span data-ttu-id="18b75-133">使用 DXVA 支持硬件加速解码</span><span class="sxs-lookup"><span data-stu-id="18b75-133">Support for hardware accelerated decoding by using DXVA</span></span>

  - <span data-ttu-id="18b75-134">支持硬件加速编码</span><span class="sxs-lookup"><span data-stu-id="18b75-134">Support for hardware accelerated encoding</span></span>

  - <span data-ttu-id="18b75-135">物理核心数</span><span class="sxs-lookup"><span data-stu-id="18b75-135">Number of physical cores</span></span>

  - <span data-ttu-id="18b75-136">Windows 体验指数 (WEI)</span><span class="sxs-lookup"><span data-stu-id="18b75-136">Windows Experience Index (WEI)</span></span>

<span data-ttu-id="18b75-137">Windows 系统评估工具 (WinSAT) 确定 WEI。</span><span class="sxs-lookup"><span data-stu-id="18b75-137">The Windows System Assessment Tool (WinSAT) determines the WEI.</span></span> <span data-ttu-id="18b75-138">当你运行 WinSAT 工具时，它会在% windir% \\ 性能 \\ WinSAT \\ 数据存储目录中的计算机上生成一个正式的评估 XML 文档。</span><span class="sxs-lookup"><span data-stu-id="18b75-138">When you run the WinSAT tool, it generates a Formal.Assessment XML document on the computer in the %windir%\\Performance\\WinSAT\\DataStore directory.</span></span> <span data-ttu-id="18b75-139">此 XML 文件包含对于确定编码功能和解码功能非常重要的以下两项分数：</span><span class="sxs-lookup"><span data-stu-id="18b75-139">This XML file contains the following two scores that are of particular importance for determining encoding and decoding capabilities:</span></span>

  - <span data-ttu-id="18b75-140">VideoEncodeScore 指示计算机的基于软件的视频编码功能。</span><span class="sxs-lookup"><span data-stu-id="18b75-140">The VideoEncodeScore indicates the software-based video encoding capability of the computer.</span></span>

  - <span data-ttu-id="18b75-141">GraphicsScore 值指示计算机的硬件加速编码功能。</span><span class="sxs-lookup"><span data-stu-id="18b75-141">The GraphicsScore value indicates the hardware accelerated encoding capability of the computer.</span></span>

<span data-ttu-id="18b75-p106">以下三个表说明了不同的 PC 类型依据其支持的硬件加速所具有的最大编码功能和解码功能。对于 640x360 和更高分辨率，最大支持帧速率为 30 帧/秒 (fps)。对于低于 640x360 的分辨率，最大支持帧速率为 15 fps。</span><span class="sxs-lookup"><span data-stu-id="18b75-p106">The following three tables explain the maximum encoding and decoding capability for different PC types depending on what hardware acceleration they support. For resolutions of 640x360 and higher, the maximum supported frame rate is 30 frames per second (fps). For resolutions lower than 640x360, the maximum supported frame rate is 15 fps.</span></span>

### <a name="computer-without-dxva-and-without-hardware-accelerated-encoder"></a><span data-ttu-id="18b75-145">不带 DXVA 且不带硬件加速编码器的计算机</span><span class="sxs-lookup"><span data-stu-id="18b75-145">Computer Without DXVA And Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18b75-146">支持的编码器分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-146">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="18b75-147">支持的解码器分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-147">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="18b75-148">要求</span><span class="sxs-lookup"><span data-stu-id="18b75-148">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18b75-149">424x240</span><span class="sxs-lookup"><span data-stu-id="18b75-149">424x240</span></span></p></td>
<td><p><span data-ttu-id="18b75-150">424x240（对于仅接收方案，分辨率为 640x360，帧速率为15fps）</span><span class="sxs-lookup"><span data-stu-id="18b75-150">424x240 (640x360 at 15fps for receive only scenarios)</span></span></p></td>
<td><p><span data-ttu-id="18b75-151">单核且 VideoEncodeScore ≥ 4.0</span><span class="sxs-lookup"><span data-stu-id="18b75-151">1 Core and VideoEncodeScore ≥ 4.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-152">640x360</span><span class="sxs-lookup"><span data-stu-id="18b75-152">640x360</span></span></p></td>
<td><p><span data-ttu-id="18b75-153">640x360</span><span class="sxs-lookup"><span data-stu-id="18b75-153">640x360</span></span></p></td>
<td><p><span data-ttu-id="18b75-154">双核且 VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="18b75-154">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b75-155">640x360</span><span class="sxs-lookup"><span data-stu-id="18b75-155">640x360</span></span></p></td>
<td><p><span data-ttu-id="18b75-156">1280x720</span><span class="sxs-lookup"><span data-stu-id="18b75-156">1280x720</span></span></p></td>
<td><p><span data-ttu-id="18b75-157">双核且 VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="18b75-157">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-158">640x360</span><span class="sxs-lookup"><span data-stu-id="18b75-158">640x360</span></span></p></td>
<td><p><span data-ttu-id="18b75-159">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-159">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-160">四核且 VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="18b75-160">4 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b75-161">1280x720</span><span class="sxs-lookup"><span data-stu-id="18b75-161">1280x720</span></span></p></td>
<td><p><span data-ttu-id="18b75-162">1280x720</span><span class="sxs-lookup"><span data-stu-id="18b75-162">1280x720</span></span></p></td>
<td><p><span data-ttu-id="18b75-163">四核且 VideoEncodeScore ≥ 7.3</span><span class="sxs-lookup"><span data-stu-id="18b75-163">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-164">1280x720</span><span class="sxs-lookup"><span data-stu-id="18b75-164">1280x720</span></span></p></td>
<td><p><span data-ttu-id="18b75-165">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-165">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-166">四核且 VideoEncodeScore ≥ 7.3</span><span class="sxs-lookup"><span data-stu-id="18b75-166">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b75-167">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-167">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-168">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-168">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-169">不适用</span><span class="sxs-lookup"><span data-stu-id="18b75-169">N/A</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="computer-with-dxva-but-without-hardware-accelerated-encoder"></a><span data-ttu-id="18b75-170">带 DXVA 但不带硬件加速编码器的计算机</span><span class="sxs-lookup"><span data-stu-id="18b75-170">Computer With DXVA But Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18b75-171">支持的编码器分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-171">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="18b75-172">支持的解码器分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-172">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="18b75-173">要求</span><span class="sxs-lookup"><span data-stu-id="18b75-173">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18b75-174">424x240</span><span class="sxs-lookup"><span data-stu-id="18b75-174">424x240</span></span></p></td>
<td><p><span data-ttu-id="18b75-175">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-175">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-176">单核且 VideoEncodeScore ≥ 3.0</span><span class="sxs-lookup"><span data-stu-id="18b75-176">1 Core and VideoEncodeScore ≥ 3.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-177">640x360</span><span class="sxs-lookup"><span data-stu-id="18b75-177">640x360</span></span></p></td>
<td><p><span data-ttu-id="18b75-178">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-178">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-179">双核且 VideoEncodeScore ≥ 4.5</span><span class="sxs-lookup"><span data-stu-id="18b75-179">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b75-180">960x540</span><span class="sxs-lookup"><span data-stu-id="18b75-180">960x540</span></span></p></td>
<td><p><span data-ttu-id="18b75-181">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-181">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-182">双核且 VideoEncodeScore ≥ 6.0</span><span class="sxs-lookup"><span data-stu-id="18b75-182">2 Cores and VideoEncodeScore ≥ 6.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-183">1280x720</span><span class="sxs-lookup"><span data-stu-id="18b75-183">1280x720</span></span></p></td>
<td><p><span data-ttu-id="18b75-184">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-184">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-185">四核且 VideoEncodeScore ≥ 6.7</span><span class="sxs-lookup"><span data-stu-id="18b75-185">4 Cores and VideoEncodeScore ≥ 6.7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18b75-186">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-186">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-187">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-187">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-188">四核且 VideoEncodeScore ≥ 8.2</span><span class="sxs-lookup"><span data-stu-id="18b75-188">4 Cores and VideoEncodeScore ≥ 8.2</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="18b75-p107">Windows 7 上的 WinSAT 分数最高为 7.9。因此，不带硬件加速编码器的计算机的编码功能仅可在 Windows 8 或 Windows 8.1 上实现，其中最高 WinSAT 分数为 9.9。</span><span class="sxs-lookup"><span data-stu-id="18b75-p107">The WinSAT score on Windows 7 is limited to a maximum of 7.9. Therefore, the encoding capability for a computer without a hardware accelerated encoder can only be achieved on Windows 8 or Windows 8.1, where the maximum WinSAT score is 9.9.</span></span>



</div>

### <a name="computer-with-dxva-and-with-intel-hd-graphics-hardware-accelerated-encoder"></a><span data-ttu-id="18b75-191">带 DXVA 且带 Intel 高清显卡硬件加速编码器的计算机</span><span class="sxs-lookup"><span data-stu-id="18b75-191">Computer With DXVA And With Intel HD Graphics Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18b75-192">支持的编码器分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-192">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="18b75-193">支持的解码器分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-193">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="18b75-194">要求</span><span class="sxs-lookup"><span data-stu-id="18b75-194">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18b75-195">1280x720</span><span class="sxs-lookup"><span data-stu-id="18b75-195">1280x720</span></span></p></td>
<td><p><span data-ttu-id="18b75-196">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-196">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-197">所有第 2 代和第 3 代 Intel 高清显卡</span><span class="sxs-lookup"><span data-stu-id="18b75-197">All 2nd and 3rd generation Intel HD Graphics</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-198">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-198">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-199">1920x1080</span><span class="sxs-lookup"><span data-stu-id="18b75-199">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="18b75-200">第 2 代和第 3 代 Intel 高清显卡且 GraphicsScore ≥ 5.0</span><span class="sxs-lookup"><span data-stu-id="18b75-200">2nd and 3rd generation Intel HD Graphics and GraphicsScore ≥ 5.0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="mobile-device-video-capabilities"></a><span data-ttu-id="18b75-201">移动设备视频功能</span><span class="sxs-lookup"><span data-stu-id="18b75-201">Mobile Device Video Capabilities</span></span>

<span data-ttu-id="18b75-202">下表介绍了支持的移动设备的最大视频功能。</span><span class="sxs-lookup"><span data-stu-id="18b75-202">The following table describes the maximum video capabilities for supported mobile devices.</span></span> <span data-ttu-id="18b75-203">有关移动设备支持的详细信息，请参阅 [在 Lync Server 2013 中规划移动客户端](lync-server-2013-planning-for-mobile-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="18b75-203">For more information about mobile device support, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18b75-204">功能</span><span class="sxs-lookup"><span data-stu-id="18b75-204">Feature</span></span></th>
<th><span data-ttu-id="18b75-205">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="18b75-205">Windows Phone</span></span></th>
<th><span data-ttu-id="18b75-206">iPhone</span><span class="sxs-lookup"><span data-stu-id="18b75-206">iPhone</span></span></th>
<th><span data-ttu-id="18b75-207">iPad</span><span class="sxs-lookup"><span data-stu-id="18b75-207">iPad</span></span></th>
<th><span data-ttu-id="18b75-208">Android</span><span class="sxs-lookup"><span data-stu-id="18b75-208">Android</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18b75-209">H.264 编码最大分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-209">H.264 encoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="18b75-210">VGA</span><span class="sxs-lookup"><span data-stu-id="18b75-210">VGA</span></span></p></td>
<td><p><span data-ttu-id="18b75-211">QVGA：iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="18b75-211">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="18b75-212">VGA：iPhone 5</span><span class="sxs-lookup"><span data-stu-id="18b75-212">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="18b75-213">720p：iPhone 5S 和更高版本</span><span class="sxs-lookup"><span data-stu-id="18b75-213">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="18b75-214">VGA：iPad 2 和更高版本/iPad mini 1 和更高版本</span><span class="sxs-lookup"><span data-stu-id="18b75-214">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="18b75-215">720p：iPad Air/iPad mini 2/iPad Pro 和更高版本</span><span class="sxs-lookup"><span data-stu-id="18b75-215">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="18b75-216">最高可 VGA，具体取决于设备型号</span><span class="sxs-lookup"><span data-stu-id="18b75-216">Up to VGA depending on device model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18b75-217">H.264 解码最大分辨率</span><span class="sxs-lookup"><span data-stu-id="18b75-217">H.264 decoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="18b75-218">VGA</span><span class="sxs-lookup"><span data-stu-id="18b75-218">VGA</span></span></p></td>
<td><p><span data-ttu-id="18b75-219">QVGA：iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="18b75-219">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="18b75-220">VGA：iPhone 5</span><span class="sxs-lookup"><span data-stu-id="18b75-220">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="18b75-221">720p：iPhone 5S 和更高版本</span><span class="sxs-lookup"><span data-stu-id="18b75-221">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="18b75-222">VGA：iPad 2 和更高版本/iPad mini 1 和更高版本</span><span class="sxs-lookup"><span data-stu-id="18b75-222">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="18b75-223">720p：iPad Air/iPad mini 2/iPad Pro 和更高版本</span><span class="sxs-lookup"><span data-stu-id="18b75-223">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="18b75-224">最高可 VGA，具体取决于设备型号</span><span class="sxs-lookup"><span data-stu-id="18b75-224">Up to VGA depending on device model</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="18b75-225">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18b75-225">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

