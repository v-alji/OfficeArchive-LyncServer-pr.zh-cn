---
title: 安装 Lync Server 2013 core 文件和 RTCLocal 数据库
description: 安装 Lync Server 2013 core 文件和 RTCLocal 数据库。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Server 2013 core files and the RTCLocal database
ms:assetid: 206f0c1d-40f7-45b6-aa62-88aaef6cf7f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204734(v=OCS.15)
ms:contentKeyID: 48183591
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68964f8b80f6377afd859d113783d61e33afbebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426996"
---
# <a name="installing-the-lync-server-2013-core-files-and-the-rtclocal-database"></a><span data-ttu-id="e032b-103">安装 Lync Server 2013 core 文件和 RTCLocal 数据库</span><span class="sxs-lookup"><span data-stu-id="e032b-103">Installing the Lync Server 2013 core files and the RTCLocal database</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e032b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e032b-104">

<span> </span></span></span>

<span data-ttu-id="e032b-105">_**主题上次修改时间：** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="e032b-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="e032b-106">若要在计算机上安装 Lync Server 2013 core 文件，请完成以下过程。</span><span class="sxs-lookup"><span data-stu-id="e032b-106">To install the Lync Server 2013 core files on a computer, complete the following procedure.</span></span> <span data-ttu-id="e032b-107">当安装核心文件时，将自动安装 RTCLocal 数据库。</span><span class="sxs-lookup"><span data-stu-id="e032b-107">The RTCLocal database is automatically installed when you install the core files.</span></span> <span data-ttu-id="e032b-108">请注意，不需要在观察程序节点上安装 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="e032b-108">Note that you do not need to install SQL Server on the watcher nodes.</span></span> <span data-ttu-id="e032b-109">相反，系统会自动为您安装 SQL Server Express。</span><span class="sxs-lookup"><span data-stu-id="e032b-109">Instead, SQL Server Express is automatically installed for you.</span></span>

<span data-ttu-id="e032b-110">要安装 Lync Server 2013 core 文件和 RTCLocal 数据库，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="e032b-110">To install the Lync Server 2013 core files and the RTCLocal database:</span></span>

1.  <span data-ttu-id="e032b-111">在观察程序节点计算机上，单击 " **开始**"，单击 " **所有程序**"，单击 " **附件**"，右键单击 " **命令提示符**"，然后单击 "以 **管理员身份运行**"。</span><span class="sxs-lookup"><span data-stu-id="e032b-111">On the watcher node computer, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="e032b-112">在控制台窗口中，键入以下命令，然后按 ENTER，使用 Lync Server 设置文件的相应路径：</span><span class="sxs-lookup"><span data-stu-id="e032b-112">In the console window, type the following command and then press ENTER, using the appropriate path to your Lync Server setup files:</span></span>
    
        D:\Setup.exe /BootstrapLocalMgmt

<span data-ttu-id="e032b-113">若要验证是否已成功安装核心 Lync 服务器组件，请依次单击 " **开始**"、" **所有程序**"、" **lync server 2013**"，然后单击 " **lync server Management Shell**"。</span><span class="sxs-lookup"><span data-stu-id="e032b-113">To verify that the core Lync Server components were successfully installed, click **Start**, click **All Programs**, click **Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span> <span data-ttu-id="e032b-114">在 Lync Server 2013 命令行管理程序中，键入以下 Windows PowerShell 命令，然后按 ENTER：</span><span class="sxs-lookup"><span data-stu-id="e032b-114">In the Lync Server 2013 Management Shell, type the following Windows PowerShell command, and then press ENTER:</span></span>

    Get-CsWatcherNodeConfiguration

<span data-ttu-id="e032b-115">第一次运行此命令时，由于尚未配置任何观察程序节点计算机，因此不会返回任何数据。</span><span class="sxs-lookup"><span data-stu-id="e032b-115">The first time you run this command, you no data is returned because you have not configured any watcher node computers yet.</span></span> <span data-ttu-id="e032b-116">只要命令运行时不返回错误，您就可以假设 Lync Server 设置已成功完成。</span><span class="sxs-lookup"><span data-stu-id="e032b-116">As long as the command runs without returning an error, you can assume that the Lync Server setup completed successfully.</span></span>

<span data-ttu-id="e032b-117">如果你的观察程序节点计算机位于你的外围网络内，你可以运行以下命令来验证 Lync Server 2013 的安装：</span><span class="sxs-lookup"><span data-stu-id="e032b-117">If your watcher node computer is located inside your perimeter network, you can run the following command to verify the installation of Lync Server 2013:</span></span>

    Get-CsPinPolicy

<span data-ttu-id="e032b-118">你将收到如下所示的信息，具体取决于在你的组织中配置使用的 (引脚) 策略的个人识别码的数量：</span><span class="sxs-lookup"><span data-stu-id="e032b-118">You will receive information similar to the following, depending on the number of personal identification number (PIN) policies configured for use in your organization:</span></span>

    Identity             : Global
    Description          :
    MinPasswordLength    : 5
    PINHistoryCount      : 0
    AllowCommonPatterns  : False
    PINLifetime          : 0
    MaximumLogonAttempts :

<span data-ttu-id="e032b-119">如果你看到有关 PIN 策略的信息，则表示你已成功安装核心组件。</span><span class="sxs-lookup"><span data-stu-id="e032b-119">If you see information about your PIN policies, it means that you have successfully installed the core components.</span></span>

<span data-ttu-id="e032b-120"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e032b-120"></div>

<span> </span>

</div>

</div>

</span></span></div>

