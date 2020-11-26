---
title: Lync Server 2013：响应组的技术要求
description: Lync Server 2013：响应组的技术要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Response Group
ms:assetid: 477488bd-124f-437b-9327-732a0d7271ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204863(v=OCS.15)
ms:contentKeyID: 48184044
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f3125ed8c732960e23970229e99bf5a8487eb96a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441296"
---
# <a name="technical-requirements-for-response-group-in-lync-server-2013"></a><span data-ttu-id="f63e9-103">Lync Server 2013 中响应组的技术要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-103">Technical requirements for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f63e9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f63e9-104">

<span> </span></span></span>

<span data-ttu-id="f63e9-105">_**主题上次修改时间：** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="f63e9-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="f63e9-106">本部分介绍响应组应用程序的以下技术要求：</span><span class="sxs-lookup"><span data-stu-id="f63e9-106">This section describes the following technical requirements for the Response Group application:</span></span>

  - <span data-ttu-id="f63e9-107">硬件要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-107">Hardware requirements</span></span>

  - <span data-ttu-id="f63e9-108">软件要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-108">Software requirements</span></span>

  - <span data-ttu-id="f63e9-109">端口要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-109">Port requirements</span></span>

  - <span data-ttu-id="f63e9-110">音频文件要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-110">Audio file requirements</span></span>

  - <span data-ttu-id="f63e9-111">响应组配置工具要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-111">Response Group configuration tool requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="f63e9-112">硬件要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-112">Hardware Requirements</span></span>

<span data-ttu-id="f63e9-113">响应组应用程序具有与前端服务器相同的硬件要求。</span><span class="sxs-lookup"><span data-stu-id="f63e9-113">The Response Group application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="f63e9-114">有关硬件要求的详细信息，请参阅支持文档中的 [Lync server 2013 的服务器硬件平台](lync-server-2013-server-hardware-platforms.md) 。</span><span class="sxs-lookup"><span data-stu-id="f63e9-114">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="f63e9-115">软件要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-115">Software Requirements</span></span>

<span data-ttu-id="f63e9-116">响应组应用程序具有与前端服务器相同的操作系统要求和软件先决条件。</span><span class="sxs-lookup"><span data-stu-id="f63e9-116">The Response Group application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="f63e9-117">有关软件要求的详细信息，请参阅支持文档中的 [Lync server 2013 中的 "服务器和工具操作系统支持](lync-server-2013-server-and-tools-operating-system-support.md) "。</span><span class="sxs-lookup"><span data-stu-id="f63e9-117">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="f63e9-118">如果你使用 Windows Media 音频 ( .wma) 文件对于响应组音乐和通知，运行响应组应用程序的所有前端服务器或标准版服务器必须为运行 windows Server 2008 R2 的服务器安装 Windows Media Format Runtime，或者为运行 Windows Server 2012 或 Windows Server 2012 R2 的服务器安装 Microsoft Media Foundation。</span><span class="sxs-lookup"><span data-stu-id="f63e9-118">If you use Windows Media Audio (.wma) files for Response Group music and announcements, all Front End Servers or Standard Editions servers that run the Response Group application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="f63e9-119">对于 Windows Server 2008 R2，Windows Media 格式运行时作为 Windows 桌面体验的一部分进行安装。</span><span class="sxs-lookup"><span data-stu-id="f63e9-119">For Windows Server 2008 R2, Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span>

<span data-ttu-id="f63e9-120">有关音频要求的更多详细信息，请参阅本部分后面部分的 "音频文件要求"。</span><span class="sxs-lookup"><span data-stu-id="f63e9-120">For more details about audio requirements, see "Audio File Requirements" later in this section.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="f63e9-121">端口要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-121">Port Requirements</span></span>

<span data-ttu-id="f63e9-122">响应组应用程序使用以下端口：</span><span class="sxs-lookup"><span data-stu-id="f63e9-122">The Response Group application uses the following ports:</span></span>

  - <span data-ttu-id="f63e9-123">**端口 5071**  用于 SIP 侦听请求</span><span class="sxs-lookup"><span data-stu-id="f63e9-123">**Port 5071**   Used for SIP listening requests</span></span>

  - <span data-ttu-id="f63e9-124">**端口 8404** 用于在服务器之间通信</span><span class="sxs-lookup"><span data-stu-id="f63e9-124">**Port 8404**   Used for interserver communications</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f63e9-125">此端口用于匹配 "正在进行" 服务，并且当响应组应用程序部署在具有多个前端服务器的池中时，此端口是必需的。</span><span class="sxs-lookup"><span data-stu-id="f63e9-125">This port is used for the Match Making service and is required when the Response Group application is deployed in a pool that has more than one Front End Server.</span></span>

    
    </div>

<div>


> [!NOTE]  
> <span data-ttu-id="f63e9-126">这些端口是默认设置，您可以使用 <STRONG>Set-CsApplicationServer</STRONG> cmdlet 更改。</span><span class="sxs-lookup"><span data-stu-id="f63e9-126">These ports are default settings that you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="f63e9-127">有关此 cmdlet 的详细信息，请参阅 Lync Server Management Shell 文档。</span><span class="sxs-lookup"><span data-stu-id="f63e9-127">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="f63e9-128">音频文件要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-128">Audio File Requirements</span></span>

<span data-ttu-id="f63e9-129">响应组应用程序支持波形 ( .wav) 文件格式和 Windows Media 音频 ( IVR) 文件格式，用于响应组消息、保留音乐或交互式语音响应 () 问题。</span><span class="sxs-lookup"><span data-stu-id="f63e9-129">The Response Group application supports wave (.wav) file format and Windows Media audio (.wma) file format for Response Group messages, on-hold music, or interactive voice response (IVR) questions.</span></span>

<span data-ttu-id="f63e9-130">Windows Media 音频文件格式要求 Windows Media 格式运行时安装在运行 Windows Server 2008 R2 和 Windows Server 2008 的前端服务器上。</span><span class="sxs-lookup"><span data-stu-id="f63e9-130">The Windows Media audio file format requires that the Windows Media Format Runtime is installed on Front End Servers running Windows Server 2008 R2 and Windows Server 2008.</span></span> <span data-ttu-id="f63e9-131">有关详细信息，请参阅上文中的“软件要求”。</span><span class="sxs-lookup"><span data-stu-id="f63e9-131">For more details, see "Software Requirements" earlier in this section.</span></span>

<div>

## <a name="supported-wave-file-formats"></a><span data-ttu-id="f63e9-132">支持的 Wave 文件格式</span><span class="sxs-lookup"><span data-stu-id="f63e9-132">Supported Wave File Formats</span></span>

<span data-ttu-id="f63e9-133">所有 wave 文件必须符合以下要求：</span><span class="sxs-lookup"><span data-stu-id="f63e9-133">All wave files must meet the following requirements:</span></span>

  - <span data-ttu-id="f63e9-134">8 位或 16 位文件</span><span class="sxs-lookup"><span data-stu-id="f63e9-134">8-bit or 16-bit file</span></span>

  - <span data-ttu-id="f63e9-135">线性脉冲编码调制 (LPCM)，A-Law 或 mu-Law 格式</span><span class="sxs-lookup"><span data-stu-id="f63e9-135">Linear pulse code modulation (LPCM), A-Law, or mu-Law format</span></span>

  - <span data-ttu-id="f63e9-136">单声道或立体声</span><span class="sxs-lookup"><span data-stu-id="f63e9-136">Mono or stereo</span></span>

  - <span data-ttu-id="f63e9-137">4 MB 或更小</span><span class="sxs-lookup"><span data-stu-id="f63e9-137">4MB or less</span></span>

<span data-ttu-id="f63e9-138">为获得 wave 文件的最佳性能，建议使用 16 kHz、单声道、16 位的 wave 文件。</span><span class="sxs-lookup"><span data-stu-id="f63e9-138">For the best performance of wave files, a 16 kHz, mono, 16-bit Wave file is recommended.</span></span>

</div>

<div>

## <a name="supported-windows-media-audio-file-formats"></a><span data-ttu-id="f63e9-139">支持的 Windows Media 音频文件格式</span><span class="sxs-lookup"><span data-stu-id="f63e9-139">Supported Windows Media Audio File Formats</span></span>

<span data-ttu-id="f63e9-140">如果使用 Windows Media 音频文件，请考虑使用较低的比特率，并验证负载下的系统性能。</span><span class="sxs-lookup"><span data-stu-id="f63e9-140">If you use a Windows Media audio file, consider using low bit rates, and verify the performance of your system under load.</span></span>

<span data-ttu-id="f63e9-141">您可以使用 Microsoft Expression Encoder 4 将文件转换为 Windows Media 音频格式。</span><span class="sxs-lookup"><span data-stu-id="f63e9-141">You can use the Microsoft Expression Encoder 4 to convert a file to the Windows Media Audio format.</span></span> <span data-ttu-id="f63e9-142">若要下载表达式编码器4，请参阅 [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) 。</span><span class="sxs-lookup"><span data-stu-id="f63e9-142">To download Expression Encoder 4, see [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843).</span></span>

</div>

</div>

<div>

## <a name="response-group-configuration-tool-requirements"></a><span data-ttu-id="f63e9-143">响应组配置工具要求</span><span class="sxs-lookup"><span data-stu-id="f63e9-143">Response Group Configuration Tool Requirements</span></span>

<span data-ttu-id="f63e9-144">"响应组配置" 工具支持下表中所述的操作系统和 web 浏览器的组合。</span><span class="sxs-lookup"><span data-stu-id="f63e9-144">The Response Group Configuration Tool supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f63e9-p107">支持 32 位或 64 位版本的操作系统。仅支持 32 位版本的 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="f63e9-p107">32-bit or 64-bit versions of the operating systems are supported. Only 32-bit versions of Internet Explorer are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="f63e9-147">支持的操作系统和 Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="f63e9-147">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f63e9-148">操作系统</span><span class="sxs-lookup"><span data-stu-id="f63e9-148">Operating system</span></span></th>
<th><span data-ttu-id="f63e9-149">Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="f63e9-149">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f63e9-150">Windows Vista Service Pack (SP) 2</span><span class="sxs-lookup"><span data-stu-id="f63e9-150">Windows Vista with Service Pack (SP) 2</span></span></p></td>
<td><p><span data-ttu-id="f63e9-151">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="f63e9-151">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="f63e9-152">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-152">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-153">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-153">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63e9-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f63e9-154">Windows 7</span></span></p>
<p><span data-ttu-id="f63e9-155">Windows 7 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="f63e9-155">Windows 7 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="f63e9-156">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-156">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-157">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-157">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f63e9-158">Windows Server 2008 Service Pack 2</span><span class="sxs-lookup"><span data-stu-id="f63e9-158">Windows Server 2008 with Service Pack 2</span></span></p></td>
<td><p><span data-ttu-id="f63e9-159">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="f63e9-159">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="f63e9-160">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-160">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-161">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-161">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63e9-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f63e9-162">Windows Server 2008 R2</span></span></p>
<p><span data-ttu-id="f63e9-163">Windows Server 2008 R2 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="f63e9-163">Windows Server 2008 R2 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="f63e9-164">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-164">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-165">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-165">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="response-group-agent-console"></a><span data-ttu-id="f63e9-166">响应组代理控制台</span><span class="sxs-lookup"><span data-stu-id="f63e9-166">Response Group Agent Console</span></span>

<span data-ttu-id="f63e9-167">此代理控制台支持下表所述的操作系统和 Web 浏览器的组合。</span><span class="sxs-lookup"><span data-stu-id="f63e9-167">The agent console supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f63e9-p108">支持 32 位或 64 位版本的操作系统。仅支持 32 位版本的 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="f63e9-p108">32-bit or 64-bit versions of the operating systems are supported. Only 32-bit versions of Internet Explorer are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="f63e9-170">支持的操作系统和 Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="f63e9-170">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f63e9-171">操作系统</span><span class="sxs-lookup"><span data-stu-id="f63e9-171">Operating system</span></span></th>
<th><span data-ttu-id="f63e9-172">Web 浏览器</span><span class="sxs-lookup"><span data-stu-id="f63e9-172">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f63e9-173">Windows Vista Service Pack (SP) 2</span><span class="sxs-lookup"><span data-stu-id="f63e9-173">Windows Vista with Service Pack (SP) 2</span></span></p></td>
<td><p><span data-ttu-id="f63e9-174">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="f63e9-174">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="f63e9-175">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-175">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-176">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-176">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63e9-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f63e9-177">Windows 7</span></span></p>
<p><span data-ttu-id="f63e9-178">Windows 7 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="f63e9-178">Windows 7 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="f63e9-179">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-179">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-180">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-180">Internet Explorer 9 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-181">Firefox 10.0</span><span class="sxs-lookup"><span data-stu-id="f63e9-181">Firefox 10.0</span></span></p>
<p><span data-ttu-id="f63e9-182">Chrome 18.0</span><span class="sxs-lookup"><span data-stu-id="f63e9-182">Chrome 18.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f63e9-183">Windows Server 2008 Service Pack 2</span><span class="sxs-lookup"><span data-stu-id="f63e9-183">Windows Server 2008 with Service Pack 2</span></span></p></td>
<td><p><span data-ttu-id="f63e9-184">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="f63e9-184">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="f63e9-185">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-185">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-186">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-186">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63e9-187">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f63e9-187">Windows Server 2008 R2</span></span></p>
<p><span data-ttu-id="f63e9-188">Windows Server 2008 R2 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="f63e9-188">Windows Server 2008 R2 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="f63e9-189">Internet Explorer 8（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-189">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-190">Internet Explorer 9（本机模式）</span><span class="sxs-lookup"><span data-stu-id="f63e9-190">Internet Explorer 9 (native mode)</span></span></p>
<p><span data-ttu-id="f63e9-191">Firefox 10.0</span><span class="sxs-lookup"><span data-stu-id="f63e9-191">Firefox 10.0</span></span></p>
<p><span data-ttu-id="f63e9-192">Chrome 18.0</span><span class="sxs-lookup"><span data-stu-id="f63e9-192">Chrome 18.0</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="f63e9-193">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f63e9-193">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

