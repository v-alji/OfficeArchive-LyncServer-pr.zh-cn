---
title: 删除前端池的 SQL Server 数据库
description: 删除前端池的 SQL Server 数据库。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Front End pool
ms:assetid: 6bb932df-3ed7-49b6-ae17-61e4c6a5fe82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688084(v=OCS.15)
ms:contentKeyID: 49733681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c5d47e4c52197c5792fa3b7770da7bbd1b26cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392460"
---
# <a name="remove-the-sql-server-database-for-a-front-end-pool"></a>删除前端池的 SQL Server 数据库

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**主题上次修改时间：** 2012-10-04_

删除 Microsoft Lync Server 2010 前端池或将其重新配置为使用其他数据库后，可以删除托管了池数据的 SQL Server 数据库。 使用以下过程从拓扑生成器中删除定义，然后从数据库服务器中删除数据库和日志文件。

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a>使用拓扑生成器删除 SQL Server 数据库

1.  从 Lync Server 2013 前端服务器，打开拓扑生成器并下载现有拓扑。

2.  在拓扑生成器中，导航到 " **共享组件** "，然后导航到 " **sql server 存储**"，右键单击与删除或重新配置的前端池相关联的 SQL Server 实例，然后单击 " **删除**"。

3.  发布拓扑，然后检查复制状态。

</div>

<div>

## <a name="to-remove-user-and-application-databases-from-the-sql-server"></a>从 SQL Server 中删除用户和应用程序数据库

1.  若要删除 SQL Server 上的数据库，您必须是要删除数据库文件的 SQL Server 的 SQL Server sysadmin 组的成员。

2.  打开 Lync Server 命令行管理程序

3.  若要删除 "池用户" 存储的数据库，请键入：
    
        Uninstall-CsDataBase -DatabaseType User -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    其中 \<FQDN\> 是数据库服务器的 FQDN) 的完全限定的域名 (，并且 \<instance\> 是指定的数据库实例 (即) 定义了一个实例。

4.  若要删除池应用商店的数据库，请键入：
    
        Uninstall-CsDataBase -DatabaseType Application -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    \<FQDN\>数据库服务器的 FQDN 是数据库服务器的 FQDN，并且 \<instance\> 是指定的数据库实例 (也就是说，如果) 定义了一个实例。

5.  当 **CsDataBase** cmdlet 提示你确认操作时，请阅读该信息，然后按 **Y** (或按 enter) 以继续，或者按 N，然后按 N，然后按 N，然后按 **N** (，以防出现错误) 。

</div>

</div>

<span> </span>

</div>

</div>

</div>

