---
title: Lync Server 2013：还原持久聊天数据
description: Lync Server 2013：还原持久聊天数据。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442507"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a><span data-ttu-id="a8456-103">在 Lync Server 2013 中还原永久聊天数据</span><span class="sxs-lookup"><span data-stu-id="a8456-103">Restoring Persistent Chat data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8456-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8456-104">

<span> </span></span></span>

<span data-ttu-id="a8456-105">_**主题上次修改时间：** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="a8456-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="a8456-106">持久聊天室内容存储在持久聊天数据库 (mgc) 中。</span><span class="sxs-lookup"><span data-stu-id="a8456-106">Persistent Chat room content is stored in the Persistent Chat database (mgc.mdf).</span></span> <span data-ttu-id="a8456-107">这是应定期备份的业务关键型数据。</span><span class="sxs-lookup"><span data-stu-id="a8456-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="a8456-108">除了聊天室内容之外，主体 (（如用户和组) 以及他们拥有的用于聊天聊天室和聊天室内容的角色和访问）也存储在持久聊天数据库中。</span><span class="sxs-lookup"><span data-stu-id="a8456-108">In addition to the chat room content, principals (such as users and groups) and the roles and access that they have to chat rooms and chat room content, is also stored in the Persistent Chat database.</span></span>

<span data-ttu-id="a8456-109">还原持久聊天数据的方式取决于用于备份的方法。</span><span class="sxs-lookup"><span data-stu-id="a8456-109">How you restore your Persistent Chat data depends on the method that you used to back it up.</span></span>

  - <span data-ttu-id="a8456-110">如果您使用 SQL Server 备份过程，则必须使用 SQL Server 还原过程。</span><span class="sxs-lookup"><span data-stu-id="a8456-110">If you used SQL Server backup procedures, you must use SQL Server restore procedures.</span></span>

  - <span data-ttu-id="a8456-111">如果你使用 **Export CsPersistentChatData** Cmdlet 备份持久聊天数据，则必须使用 **CsPersistentChatData** cmdlet 来还原数据。</span><span class="sxs-lookup"><span data-stu-id="a8456-111">If you used the **Export-CsPersistentChatData** cmdlet to back up Persistent Chat data, then you must use the **Import-CsPersistentChatData** cmdlet to restore the data.</span></span>

<span data-ttu-id="a8456-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8456-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

