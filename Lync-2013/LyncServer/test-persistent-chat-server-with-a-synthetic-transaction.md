---
title: 使用综合事务测试持久聊天服务器
description: 使用综合事务测试持久聊天服务器。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Test Persistent Chat Server with a synthetic transaction
ms:assetid: 414e43f3-0074-4ecf-a232-398de972cb24
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204837(v=OCS.15)
ms:contentKeyID: 48183968
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7aad6960baa4873b5992b0b51799d46ea59fddf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446575"
---
# <a name="test-persistent-chat-server-with-a-synthetic-transaction"></a><span data-ttu-id="598dd-103">使用综合事务测试持久聊天服务器</span><span class="sxs-lookup"><span data-stu-id="598dd-103">Test Persistent Chat Server with a synthetic transaction</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="598dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="598dd-104">

<span> </span></span></span>

<span data-ttu-id="598dd-105">_**主题上次修改时间：** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="598dd-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="598dd-106">测试持久聊天服务器以在两个用户之间的聊天室中发送和接收消息</span><span class="sxs-lookup"><span data-stu-id="598dd-106">To test Persistent Chat Server for sending and receiving messages in a chat room between two users</span></span>

    Test-CsPersistentChatMessage [-Authentication <TrustedServer | Negotiate | ClientCertificate | 
        LiveID>] [-ReceiverSipAddress <String>] [-RegistrarPort <Int32>] [-SenderSipAddress <String>] -TargetFqdn <String> [-Force <SwitchParameter>] [-OutLoggerVariable <String>] 
        [-OutVerboseVariable <String>] [<CommonParameters>]

<span data-ttu-id="598dd-107">或者</span><span class="sxs-lookup"><span data-stu-id="598dd-107">or</span></span>

    Test-CsPersistentChatMessage [-Authentication <TrustedServer | Negotiate | ClientCertificate | 
        LiveID>] -ReceiverCredential <PSCredential> -ReceiverSipAddress <String> [-RegistrarPort 
        <Int32>] -SenderCredential <PSCredential> -SenderSipAddress <String> [-TargetFqdn <String>] [-Force <SwitchParameter>] [-OutLoggerVariable <String>] [-OutVerboseVariable <String>] [<CommonParameters>]

<span data-ttu-id="598dd-108">或者</span><span class="sxs-lookup"><span data-stu-id="598dd-108">or</span></span>

    Test-CsPersistentChatMessage [-Authentication <TrustedServer | Negotiate | ClientCertificate | 
        LiveID>] [-Force <SwitchParameter>] [-OutLoggerVariable <String>] [-OutVerboseVariable 
        <String>] [<CommonParameters>]

<span data-ttu-id="598dd-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="598dd-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

