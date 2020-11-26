---
title: Lync Server 2013：使用备份服务还原会议内容
description: Lync Server 2013：使用备份服务还原会议内容。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring conference contents using the Backup Service
ms:assetid: 3e0f18ec-7319-4c07-a59b-2938e7787bc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688030(v=OCS.15)
ms:contentKeyID: 49733620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3a0037af711948c008e74c5444373ed995f0e6e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442542"
---
# <a name="restoring-conference-contents-using-the-backup-service-in-lync-server-2013"></a><span data-ttu-id="0f1cf-103">在 Lync Server 2013 中使用备份服务还原会议内容</span><span class="sxs-lookup"><span data-stu-id="0f1cf-103">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0f1cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0f1cf-104">

<span> </span></span></span>

<span data-ttu-id="0f1cf-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0f1cf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0f1cf-106">如果在前端池的文件存储中存储的会议信息不可用。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-106">If the conference information stored in the file store of a Front End pool becomes unavailable.</span></span> <span data-ttu-id="0f1cf-107">您必须还原此信息，以便驻留在该池中的用户保留其会议数据。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-107">you must restore this information so that users homed on the pool retain their conference data.</span></span> <span data-ttu-id="0f1cf-108">如果已丢失会议数据的前端池与另一个前端池配对，则可以使用备份服务还原数据。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-108">If the Front End pool which has lost conference data is paired with another Front End pool, you can use the Backup Service to restore the data.</span></span>

<span data-ttu-id="0f1cf-109">如果整个池出现故障，并且你必须将其用户故障转移到备份池，还必须执行此任务。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-109">You must also perform this task if an entire pool has failed and you have to fail over its users to a backup pool.</span></span> <span data-ttu-id="0f1cf-110">当这些用户故障恢复到其原始池时，必须使用此过程将其会议内容复制回其原始池。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-110">When these users are failed back over to their original pool, you must use this procedure to copy their conference content back to their original pool as well.</span></span>

<span data-ttu-id="0f1cf-111">假设 Pool1 与 Pool2 配对，并且 Pool1 中的会议数据丢失。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-111">Assume that Pool1 is paired with Pool2, and the conference data in Pool1 is lost.</span></span> <span data-ttu-id="0f1cf-112">你可以使用以下 cmdlet 调用备份服务来还原内容：</span><span class="sxs-lookup"><span data-stu-id="0f1cf-112">You can use the following cmdlet to invoke the Backup Service to restore the contents:</span></span>

    Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="0f1cf-113">还原会议内容可能需要一些时间，具体取决于它们的大小。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-113">Restoring the conference contents may take some time, depending on their size.</span></span> <span data-ttu-id="0f1cf-114">你可以使用以下 cmdlet 检查进程状态：</span><span class="sxs-lookup"><span data-stu-id="0f1cf-114">You can use the following cmdlet to check the process status:</span></span>

    Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="0f1cf-115">当此 cmdlet 为数据会议模块返回稳定状态的值时，将执行此过程。</span><span class="sxs-lookup"><span data-stu-id="0f1cf-115">The process is done when this cmdlet returns a value of Steady State for the data conference module.</span></span>

<span data-ttu-id="0f1cf-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0f1cf-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

