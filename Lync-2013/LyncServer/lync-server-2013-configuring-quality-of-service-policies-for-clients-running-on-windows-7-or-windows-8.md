---
title: Lync Server 2013：为在 Windows 7 或 Windows 8 上运行的客户端配置服务质量策略
description: Lync Server 2013：为在 Windows 7 或 Windows 8 上运行的客户端配置服务质量策略。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service policies for clients running on Windows 7 or Windows 8
ms:assetid: efff2b98-b3fb-4183-a4f0-329a9105ce2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205371(v=OCS.15)
ms:contentKeyID: 48185785
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: faba5fc54ef73bfc738f94ee7209fc46a7cdc208
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432693"
---
# <a name="configuring-quality-of-service-policies-in-lync-server-2013-for-clients-running-on-windows-7-or-windows-8"></a><span data-ttu-id="9e645-103">在 Lync Server 2013 中为在 Windows 7 或 Windows 8 上运行的客户端配置服务质量策略</span><span class="sxs-lookup"><span data-stu-id="9e645-103">Configuring Quality of Service policies in Lync Server 2013 for clients running on Windows 7 or Windows 8</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e645-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e645-104">

<span> </span></span></span>

<span data-ttu-id="9e645-105">_**主题上次修改时间：** 2016-03-29_</span><span class="sxs-lookup"><span data-stu-id="9e645-105">_**Topic Last Modified:** 2016-03-29_</span></span>

<span data-ttu-id="9e645-106">除了指定要由 Lync 客户端使用的端口范围之外，还必须创建将应用于客户端计算机的单独的服务质量策略。</span><span class="sxs-lookup"><span data-stu-id="9e645-106">In addition to specifying port ranges for use by your Lync clients you must also create separate Quality of Service policies that will be applied to client computers.</span></span> <span data-ttu-id="9e645-107"> (为会议、应用程序和中介服务器创建的服务质量策略不应应用于客户端计算机。 ) 此信息仅适用于运行 Lync 2013 客户端的计算机和 Windows 7 或 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="9e645-107">(The Quality of Service policies created for Conferencing, Application, and Mediation servers should not be applied to client computers.) This information applies only to computers running the Lync 2013 client and either Windows 7 or Windows 8.</span></span>

<span data-ttu-id="9e645-108">以下示例使用这组端口范围创建音频策略和视频策略：</span><span class="sxs-lookup"><span data-stu-id="9e645-108">The following example uses this set of port ranges to create an audio policy and a video policy:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e645-109">客户端流量类型</span><span class="sxs-lookup"><span data-stu-id="9e645-109">Client Traffic Type</span></span></th>
<th><span data-ttu-id="9e645-110">端口启动</span><span class="sxs-lookup"><span data-stu-id="9e645-110">Port Start</span></span></th>
<th><span data-ttu-id="9e645-111">端口范围</span><span class="sxs-lookup"><span data-stu-id="9e645-111">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e645-112">音频</span><span class="sxs-lookup"><span data-stu-id="9e645-112">Audio</span></span></p></td>
<td><p><span data-ttu-id="9e645-113">50020</span><span class="sxs-lookup"><span data-stu-id="9e645-113">50020</span></span></p></td>
<td><p><span data-ttu-id="9e645-114">名</span><span class="sxs-lookup"><span data-stu-id="9e645-114">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e645-115">视频</span><span class="sxs-lookup"><span data-stu-id="9e645-115">Video</span></span></p></td>
<td><p><span data-ttu-id="9e645-116">58000</span><span class="sxs-lookup"><span data-stu-id="9e645-116">58000</span></span></p></td>
<td><p><span data-ttu-id="9e645-117">名</span><span class="sxs-lookup"><span data-stu-id="9e645-117">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e645-118">应用程序共享</span><span class="sxs-lookup"><span data-stu-id="9e645-118">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="9e645-119">42000</span><span class="sxs-lookup"><span data-stu-id="9e645-119">42000</span></span></p></td>
<td><p><span data-ttu-id="9e645-120">名</span><span class="sxs-lookup"><span data-stu-id="9e645-120">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e645-121">文件传输</span><span class="sxs-lookup"><span data-stu-id="9e645-121">File transfer</span></span></p></td>
<td><p><span data-ttu-id="9e645-122">42020</span><span class="sxs-lookup"><span data-stu-id="9e645-122">42020</span></span></p></td>
<td><p><span data-ttu-id="9e645-123">名</span><span class="sxs-lookup"><span data-stu-id="9e645-123">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e645-124">若要创建适用于 Windows 7 或 Windows 8 计算机的服务质量音频策略，请首先登录到已安装组策略管理的计算机。</span><span class="sxs-lookup"><span data-stu-id="9e645-124">To create a Quality of Service audio policy for Windows 7 or Windows 8 computers, first log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="9e645-125">打开组策略管理 (单击 " **开始**"，指向 " **管理工具**"，然后单击 " **组策略管理** ") 然后完成以下过程：</span><span class="sxs-lookup"><span data-stu-id="9e645-125">Open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following procedure:</span></span>

1.  <span data-ttu-id="9e645-126">在 "组策略管理" 中，找到应在其中创建新策略的容器。</span><span class="sxs-lookup"><span data-stu-id="9e645-126">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="9e645-127">例如，如果所有客户端计算机都位于名为 "客户端" 的 OU 中，则应在客户端 OU 中创建新策略。</span><span class="sxs-lookup"><span data-stu-id="9e645-127">For example, if all your client computers are located in an OU named Clients then the new policy should be created in the Client OU.</span></span>

2.  <span data-ttu-id="9e645-128">右键单击相应的容器，然后单击 " **在此域中创建 GPO"，然后在此处链接**。</span><span class="sxs-lookup"><span data-stu-id="9e645-128">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="9e645-129">在 " **新建 GPO** " 对话框中，在 " **名称** " 框中键入新组策略对象的名称 (例如 " **Lync 音频** ") 然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="9e645-129">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="9e645-130">右键单击新创建的策略，然后单击 " **编辑**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-130">Right-click the newly-created policy and then click **Edit**.</span></span>

5.  <span data-ttu-id="9e645-131">在组策略管理编辑器中，展开 " **计算机配置**"，展开 " **策略**"，展开 " **Windows 设置**"，右键单击 " **基于策略的 QoS**"，然后单击 " **创建新策略**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-131">In the Group Policy Management Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

6.  <span data-ttu-id="9e645-132">在 "**基于策略的 QoS** " 对话框中的 "打开" 页面上，在 "**名称**" 框中键入新策略的名称 (例如 " **Lync 音频**") 。</span><span class="sxs-lookup"><span data-stu-id="9e645-132">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Audio**) in the **Name** box.</span></span> <span data-ttu-id="9e645-133">选择 " **指定 DSCP 值** " 并将值设置为 **46**。</span><span class="sxs-lookup"><span data-stu-id="9e645-133">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="9e645-134">"退出" **指定出站阻止率** 未选中，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-134">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

7. <span data-ttu-id="9e645-135">在下一页上，选择 " **仅限具有此可执行名称的应用程序** " 并输入 **Lync.exe** 的名称，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-135">On the next page, select **Only applications with this executable name** and enter the name **Lync.exe**, and then click **Next**.</span></span> <span data-ttu-id="9e645-136">此设置指示策略仅优先排列 Lync 客户端的匹配流量。</span><span class="sxs-lookup"><span data-stu-id="9e645-136">This setting instructs the policy to only prioritize matching traffic from the Lync client.</span></span>

8.  <span data-ttu-id="9e645-137">在第三页上，确保选中了 " **任何来源 ip 地址** " 和 " **任何目标 ip 地址** "，然后单击 " **下一步**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-137">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="9e645-138">这两个设置确保数据包将被管理，无论哪台计算机 (IP 地址) 发送这些数据包以及哪台计算机 (IP 地址) 将接收这些数据包。</span><span class="sxs-lookup"><span data-stu-id="9e645-138">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

9.  <span data-ttu-id="9e645-139">在第4页上，从 "**选择协议此 QoS 策略应用** 于" 下拉列表中选择 " **TCP 和 UDP** "。</span><span class="sxs-lookup"><span data-stu-id="9e645-139">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="9e645-140">TCP (传输控制协议) 和 UDP (用户数据报协议) 是 Lync Server 及其客户端应用程序最常使用的两种网络协议。</span><span class="sxs-lookup"><span data-stu-id="9e645-140">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

10. <span data-ttu-id="9e645-141">在 "标题" 下， **指定源端口号**，选择 " **从此源端口或范围**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-141">Under the heading **Specify the source port number**, select **From this source port or range**.</span></span> <span data-ttu-id="9e645-142">在 "随附文本" 框中，键入为音频传输保留的端口范围。</span><span class="sxs-lookup"><span data-stu-id="9e645-142">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="9e645-143">例如，如果您通过端口50039为音频流量保留了端口50020，请输入使用以下格式的端口范围： **50020:50039**。</span><span class="sxs-lookup"><span data-stu-id="9e645-143">For example, if you reserved ports 50020 through ports 50039 for audio traffic enter the port range using this format: **50020:50039**.</span></span> <span data-ttu-id="9e645-144">单击“**完成**”。</span><span class="sxs-lookup"><span data-stu-id="9e645-144">Click **Finish**.</span></span>

<span data-ttu-id="9e645-145">为音频创建 QoS 策略后，您应该为视频创建第二个策略。</span><span class="sxs-lookup"><span data-stu-id="9e645-145">After you have created the QoS policy for audio you should then create a second policy for video.</span></span> <span data-ttu-id="9e645-146">若要创建视频的策略，请按照创建音频策略时所遵循的基本过程进行操作，进行以下替换：</span><span class="sxs-lookup"><span data-stu-id="9e645-146">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="9e645-147">使用不同的 (和唯一的) 策略名称 (例如 **Lync 视频**) 。</span><span class="sxs-lookup"><span data-stu-id="9e645-147">Use a different (and unique) policy name (for example, **Lync Video**).</span></span>

  - <span data-ttu-id="9e645-148">将 DSCP 值设置为 **34** 而不是46。</span><span class="sxs-lookup"><span data-stu-id="9e645-148">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="9e645-149">如前面所述 (，您不必使用 DSCP 值 34;你只需分配一个与用于音频的值不同的 DSCP 值。 ) </span><span class="sxs-lookup"><span data-stu-id="9e645-149">(As noted previously, you do not have to use the DSCP value 34; you simply must assign a different DSCP value than the one used for audio.)</span></span>

  - <span data-ttu-id="9e645-150">对视频流量使用以前配置的端口范围。</span><span class="sxs-lookup"><span data-stu-id="9e645-150">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="9e645-151">例如，如果您已为视频保留了58000到58019的备用端口，则将端口范围设置为： **58000:58019**。</span><span class="sxs-lookup"><span data-stu-id="9e645-151">For example, if you have reserved ports 58000 through 58019 for video, then set the port range to this: **58000:58019**.</span></span>

<span data-ttu-id="9e645-152">如果你决定创建用于管理应用程序共享流量的策略，请执行以下替换：</span><span class="sxs-lookup"><span data-stu-id="9e645-152">If you decide to create a policy for managing application sharing traffic make these substitutions:</span></span>

  - <span data-ttu-id="9e645-153">使用不同的 (和唯一的) 策略名称 (例如， **Lync Server 应用程序共享**) 。</span><span class="sxs-lookup"><span data-stu-id="9e645-153">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="9e645-154">将 DSCP 值设置为 **24** ，而不是46。</span><span class="sxs-lookup"><span data-stu-id="9e645-154">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="9e645-155"> (同样，此值不必是 24;它必须与用于音频和视频的 DSCP 值不同。 ) </span><span class="sxs-lookup"><span data-stu-id="9e645-155">(Again, this value does not have to be 24; it simply must be different than the DSCP values used for audio and for video.)</span></span>

  - <span data-ttu-id="9e645-156">对视频流量使用以前配置的端口范围。</span><span class="sxs-lookup"><span data-stu-id="9e645-156">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="9e645-157">例如，如果你已为应用程序共享保留端口42000到42019，请将端口范围设置为： **42000:42019**。</span><span class="sxs-lookup"><span data-stu-id="9e645-157">For example, if you have reserved ports 42000 through 42019 for application sharing, then set the port range to this: **42000:42019**.</span></span>

<span data-ttu-id="9e645-158">对于文件传输策略：</span><span class="sxs-lookup"><span data-stu-id="9e645-158">For a file transfer policy:</span></span>

  - <span data-ttu-id="9e645-159">使用不同的 (和唯一的) 策略名称 (例如， **Lync Server 文件传输**) 。</span><span class="sxs-lookup"><span data-stu-id="9e645-159">Use a different (and unique) policy name (for example, **Lync Server File Transfers**).</span></span>

  - <span data-ttu-id="9e645-160">将 DSCP 值设置为 **14**。</span><span class="sxs-lookup"><span data-stu-id="9e645-160">Set the DSCP value to **14**.</span></span> <span data-ttu-id="9e645-161"> (同样，此值不必是 14;它只须是唯一的 DSCP 代码。 ) </span><span class="sxs-lookup"><span data-stu-id="9e645-161">(Again, this value does not have to be 14; it simply must be a unique DSCP code.)</span></span>

  - <span data-ttu-id="9e645-162">对应用程序使用以前配置的端口范围。</span><span class="sxs-lookup"><span data-stu-id="9e645-162">Use the previously-configured port range for application.</span></span> <span data-ttu-id="9e645-163">例如，如果你已为应用程序共享保留端口42020到42039，请将端口范围设置为： **42020:42039**。</span><span class="sxs-lookup"><span data-stu-id="9e645-163">For example, if you have reserved ports 42020 through 42039 for application sharing, then set the port range to this: **42020:42039**.</span></span>

<span data-ttu-id="9e645-164">在客户端计算机上刷新组策略之前，你创建的新策略将不会生效。</span><span class="sxs-lookup"><span data-stu-id="9e645-164">The new policies you have created will not take effect until Group Policy has been refreshed on your client computers.</span></span> <span data-ttu-id="9e645-165">尽管组策略会自己定期刷新，但你可以在需要刷新组策略的每台计算机上运行以下命令，强制立即刷新：</span><span class="sxs-lookup"><span data-stu-id="9e645-165">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="9e645-166">此命令可以从在管理员凭据下运行的任何命令窗口运行。</span><span class="sxs-lookup"><span data-stu-id="9e645-166">This command can be run from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="9e645-167">若要在管理员凭据下运行命令窗口，请单击“**开始**”，右键单击“**命令提示符**”，然后单击“**以管理员身份运行**”。</span><span class="sxs-lookup"><span data-stu-id="9e645-167">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="9e645-168">请记住，这些策略应面向客户端计算机。</span><span class="sxs-lookup"><span data-stu-id="9e645-168">Keep in mind that these policies should be targeted towards your client computers.</span></span> <span data-ttu-id="9e645-169">不应将它们应用于运行 Lync Server 的服务器。</span><span class="sxs-lookup"><span data-stu-id="9e645-169">They should not be applied to servers running Lync Server.</span></span>

<span data-ttu-id="9e645-170">为了帮助确保网络数据包使用适当的 DSCP 值进行标记，还应通过完成以下过程在每台计算机上创建一个新的注册表项：</span><span class="sxs-lookup"><span data-stu-id="9e645-170">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="9e645-171">单击 " **开始** "，然后单击 " **运行**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-171">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="9e645-172">在 " **运行** " 对话框中，键入 **regedit** ，然后按 enter。</span><span class="sxs-lookup"><span data-stu-id="9e645-172">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="9e645-173">在注册表编辑器中，展开 " **HKEY \_ 本地 \_ 计算机**"，依次展开 " **系统**"、" **CurrentControlSet**"、" **服务**"，然后展开 " **Tcpip**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-173">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="9e645-174">右键单击 " **Tcpip**"，指向 " **新建**"，然后单击 " **项**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-174">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="9e645-175">创建新的注册表项后，键入 **QoS** ，然后按 enter 重命名该项。</span><span class="sxs-lookup"><span data-stu-id="9e645-175">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="9e645-176">右键单击 " **QoS**"，指向 " **新建**"，然后单击 " **字符串值**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-176">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="9e645-177">创建新的注册表值后，键入 "不 **使用 NLA** "，然后按 enter 重命名该值。</span><span class="sxs-lookup"><span data-stu-id="9e645-177">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="9e645-178">双击 "不 **使用 NLA**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-178">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="9e645-179">在 "**编辑字符串**" 对话框中，在 "**值数据**" 框中键入 **1** ，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="9e645-179">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="9e645-180">关闭注册表编辑器，然后重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="9e645-180">Close the Registry Editor and then reboot your computer.</span></span>

<div>

## <a name="configuring-quality-of-service-on-computers-with-multiple-network-adapters"></a><span data-ttu-id="9e645-181">在具有多个网络适配器的计算机上配置服务质量</span><span class="sxs-lookup"><span data-stu-id="9e645-181">Configuring Quality of Service on Computers with Multiple Network Adapters</span></span>

<span data-ttu-id="9e645-182">如果你有具有多个网络适配器的计算机，有时可能会遇到一些问题，即 DSCP 值显示为0x00 而不是配置值。</span><span class="sxs-lookup"><span data-stu-id="9e645-182">If you have a computer that has multiple network adapters you might occasionally run into issues where DSCP values are shown as 0x00 rather than the configured value.</span></span> <span data-ttu-id="9e645-183">这通常会在计算机上出现：一个或多个网络适配器无法访问你的 Active Directory 域 (例如，如果这些适配器用于专用网络) 。</span><span class="sxs-lookup"><span data-stu-id="9e645-183">This will typically occur on computers where one or more of the network adapters are not able to access your Active Directory domain (for example, if these adapters are used for a private network).</span></span> <span data-ttu-id="9e645-184">在此类情况下，将为可以访问域的适配器标记 DSCP 值，但不会为无法访问域的适配器标记 DSCP 值。</span><span class="sxs-lookup"><span data-stu-id="9e645-184">In cases like that, DSCP values will be tagged for the adapters that can access the domain, but will not be tagged for adapters that cannot access the domain.</span></span>

<span data-ttu-id="9e645-185">如果你想要为计算机中的所有网络适配器标记 DSCP 值（包括对你的域没有访问权限的适配器），则需要向注册表添加和配置值。</span><span class="sxs-lookup"><span data-stu-id="9e645-185">If you would like to tag DSCP values for all the network adapters in a computer, including adapters that do not have access to your domain, then you will need to add and configure a value to the registry.</span></span> <span data-ttu-id="9e645-186">可通过完成以下过程来执行此操作：</span><span class="sxs-lookup"><span data-stu-id="9e645-186">That can be done by completing the following procedure:</span></span>

1.  <span data-ttu-id="9e645-187">单击 " **开始** "，然后单击 " **运行**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-187">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="9e645-188">在 " **运行** " 对话框中，键入 **regedit** ，然后按 enter。</span><span class="sxs-lookup"><span data-stu-id="9e645-188">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="9e645-189">在注册表编辑器中，展开 " **HKEY \_ 本地 \_ 计算机**"，依次展开 " **系统**"、" **CurrentControlSet**"、" **服务**"，然后展开 " **Tcpip**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-189">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="9e645-190">如果看不到标记为 " **QoS** " 的注册表项，请右键单击 " **Tcpip**"，指向 " **新建**"，然后单击 " **项**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-190">If you do not see a registry key labeled **QoS** then right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="9e645-191">创建新密钥后，键入 **QoS** ，然后按 enter 重命名该键。</span><span class="sxs-lookup"><span data-stu-id="9e645-191">After the new key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="9e645-192">右键单击 " **QoS**"，指向 " **新建**"，然后单击 " **字符串值**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-192">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="9e645-193">创建新的注册表值后，键入 "不 **使用 NLA** "，然后按 enter 重命名该值。</span><span class="sxs-lookup"><span data-stu-id="9e645-193">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="9e645-194">双击 "不 **使用 NLA**"。</span><span class="sxs-lookup"><span data-stu-id="9e645-194">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="9e645-195">在 "**编辑字符串**" 对话框中，在 "**值数据**" 框中键入 **1** ，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="9e645-195">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

<span data-ttu-id="9e645-196">在创建和配置新的注册表值后，您需要重新启动计算机才能使更改生效。</span><span class="sxs-lookup"><span data-stu-id="9e645-196">After creating and configuring the new registry value you will need to reboot your computer in order for the changes to take effect.</span></span>

<span data-ttu-id="9e645-197"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e645-197"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

