---
title: 运行 LyncPerfTool
description: 运行 LyncPerfTool。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run LyncPerfTool
ms:assetid: f2fd1940-d744-47b5-b299-04a914039182
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945612(v=OCS.15)
ms:contentKeyID: 51541437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3278754c9154f47602c5c4f1fa95cdc4b465b228
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446400"
---
# <a name="run-lyncperftool"></a>运行 LyncPerfTool

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2013-02-24_

在运行 Lync Server 2013 应力和性能工具之前 ( # A0) 中，必须创建用户、联系人和方案。 有关使用工具执行这些操作的详细信息，请参阅 [创建用户和联系人](create-users-and-contacts.md) 和 [配置用户配置文件](configure-user-profile.md)。 运行这些工具还将生成一个文件，该文件将作为批处理文件的一部分运行 LyncPerfTool.exe，其中包括所需的参数。

<div>

## <a name="running-the-lync-server-2013-stress-and-performance-tool"></a>运行 Lync Server 2013 应力和性能工具

UserProfileGenerator.exe 工具创建批处理文件，通过注册 LyncPerfTool 性能计数器并加载 XML 配置文件，可以运行 LyncPerfTool.exe。 批处理文件运行每个配置文件 LyncPerfTool.exe 的一个实例。 若要运行批处理文件，请执行下列操作：

1.  将包含配置文件夹和文件的文件夹复制到包含每台客户端计算机上的 LyncStressTool.exe 的目录中。  (例如，如果在名为 1.28 13.16.16 的文件夹中生成配置文件 \_ ，请将该文件夹复制到每个客户端上包含 LyncPerfTool.exe 的文件夹中。 ) 

2.  导航到相应编号的客户端文件夹，并运行 RunClient 批处理脚本。 只需在 Windows 资源管理器中双击批处理文件，它就会为该客户端编号运行所有配置文件。 还可以通过使用以下语法，从相应的客户端文件夹运行脚本：

    ```Batch
        RunClient0.bat "C:\Program Files\Microsoft Lync Server 2013\LyncStressAndPerfTool\LyncStress" 
    ```
若要直接运行 LyncPerfTool.exe，请打开命令提示符，然后在命令行中键入以下命令 (当第一次执行此操作时，请确保注册性能计数器 regsvr32/i/i/i/i LyncPerfToolPerf.dll，如本主题后面的注释中所示) # A2/file：\<configXML\>
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml
```
若要让该工具显示配置文件中的值，请在前面的命令中包括/displayfile 参数，如下所示：
```Powershell
    LyncPerfTool.exe /file:IM_client0.xml /displayfile
```
若要结束进程，请按 Ctrl + C。

<div>


> [!NOTE]  
> 直接运行 LyncPerfTool 之前，必须先注册性能计数器。 输入以下命令以注册性能计数器：



</div>

```Powershell
    regsvr32 /i /n /s LyncPerfToolPerf.dll
```
<div>


> [!NOTE]  
> 你启动的每个 LyncPerfTool.exe 实例将立即开始在用户中登录，通常以每秒一个用户的速率登录。 池的最大用户登录速率为每秒12次。 这意味着你不应同时启动超过12个 LyncPerfTool 实例，而用户仍在登录。 1000用户需要20分钟才能完全登录，每秒一次。



</div>

</div>

<div>

## <a name="see-also"></a>另请参阅


[创建用户和联系人](create-users-and-contacts.md)  
[配置用户配置文件](configure-user-profile.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

