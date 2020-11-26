---
title: 预配要运行加载的拓扑
description: 预配要运行加载的拓扑。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Provisioning the Topology to Run Load
ms:assetid: 6fba03df-3914-4d2a-8208-e252ad993aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945598(v=OCS.15)
ms:contentKeyID: 51541424
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da482fde949675acc1722305433b95b7a6a6b523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446421"
---
# <a name="provisioning-the-topology-to-run-load"></a><span data-ttu-id="51fb7-103">预配要运行加载的拓扑</span><span class="sxs-lookup"><span data-stu-id="51fb7-103">Provisioning the Topology to Run Load</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51fb7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51fb7-104">

<span> </span></span></span>

<span data-ttu-id="51fb7-105">_**主题上次修改时间：** 2013-02-04_</span><span class="sxs-lookup"><span data-stu-id="51fb7-105">_**Topic Last Modified:** 2013-02-04_</span></span>

<div>

<span data-ttu-id="51fb7-106">你可能需要在你的环境中进行以下更改，具体取决于 Lync Server 2013 的现有设置和配置：</span><span class="sxs-lookup"><span data-stu-id="51fb7-106">Depending on your existing settings and configuration of Lync Server 2013, you may need to make the following changes in your environment:</span></span>

1.  <span data-ttu-id="51fb7-107">将 Windows PowerShell 执行策略设置为 "无限制"。</span><span class="sxs-lookup"><span data-stu-id="51fb7-107">Set the Windows PowerShell execution policy to Unrestricted.</span></span> <span data-ttu-id="51fb7-108">若要检查执行策略设置，请打开 Lync Server 命令行管理程序，然后运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="51fb7-108">To check your execution policy settings, open the Lync Server Management Shell and run the following command:</span></span>

    ``` powershell
        Get-ExecutionPolicy
    ```        

    <span data-ttu-id="51fb7-109">如果此命令不会返回不受限制的值，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="51fb7-109">If this command does not return the value Unrestricted, run this command:</span></span>

    ``` powershell
        Set-ExecutionPolicy -Unrestricted
    ```

2.  <span data-ttu-id="51fb7-110">若要有效配置 Lync Server 2013，您需要：</span><span class="sxs-lookup"><span data-stu-id="51fb7-110">To effectively configure Lync Server 2013, you will need to:</span></span>
    
      - <span data-ttu-id="51fb7-111">熟悉 Lync Server 2013 拓扑 (例如，计算机名称、服务实例、站点名称和策略) 。</span><span class="sxs-lookup"><span data-stu-id="51fb7-111">Be familiar with Lync Server 2013 topology (for example, computer names, service instances, site names, and policies).</span></span>
    
      - <span data-ttu-id="51fb7-112">将已创建的某些用户分配给组，例如 "响应组查寻组" (例如，SIP Uri) 。</span><span class="sxs-lookup"><span data-stu-id="51fb7-112">Assign some of the users that were created to groups, such as Response Group hunt groups (for example, SIP URIs).</span></span>

3.  <span data-ttu-id="51fb7-113">若要从命令行运行脚本，您可以使用：</span><span class="sxs-lookup"><span data-stu-id="51fb7-113">To run the script from the command line, you may use:</span></span>

    ``` powershell
        Powershell.exe -file <path to the file>
    ```
    
4.  <span data-ttu-id="51fb7-114">通常，在此程序包中的某个脚本运行后，脚本中生成的跟踪将存储在一个文件中，该文件位于调用脚本的同一路径中，名为 \<scriptname\> $h $ m $s.txt。</span><span class="sxs-lookup"><span data-stu-id="51fb7-114">Typically, after one of the scripts in this package runs, the resulting traces from the script will be stored in a file in the same path from which the script was invoked, named \<scriptname\>$h$m$s.txt.</span></span> <span data-ttu-id="51fb7-115">例如，在 12:15 P.M. 运行 ArchivingPolicy.ps1。</span><span class="sxs-lookup"><span data-stu-id="51fb7-115">For example, running ArchivingPolicy.ps1 at 12:15 P.M.</span></span> <span data-ttu-id="51fb7-116">将生成一个日志文件，如 ArchivingPolicy121500.txt。</span><span class="sxs-lookup"><span data-stu-id="51fb7-116">will generate a log file such as ArchivingPolicy121500.txt.</span></span>

5.  <span data-ttu-id="51fb7-117">最后，请注意，虽然我们提供了配置服务器的示例，但你负责在运行完加载后修改或删除配置。</span><span class="sxs-lookup"><span data-stu-id="51fb7-117">Finally, note that although we have provided examples to configure the server, you are responsible for modifying or deleting the configuration after you have finished running the load.</span></span>

<span data-ttu-id="51fb7-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51fb7-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

