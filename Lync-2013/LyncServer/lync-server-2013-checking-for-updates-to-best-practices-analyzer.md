---
title: Lync Server 2013：检查最佳做法分析器的更新
description: Lync Server 2013：检查最佳做法分析器的更新。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking for updates to Best Practices Analyzer
ms:assetid: 06f1da8b-99a7-4871-911e-bfb7542baced
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204645(v=OCS.15)
ms:contentKeyID: 48183307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c2662f143be9fc672461715d1c3da867886e686
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434911"
---
# <a name="checking-for-updates-to-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="f8978-103">在 Lync Server 2013 中检查最佳做法分析器的更新</span><span class="sxs-lookup"><span data-stu-id="f8978-103">Checking for updates to Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8978-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8978-104">

<span> </span></span></span>

<span data-ttu-id="f8978-105">_**主题上次修改时间：** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="f8978-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="f8978-106">当您启动最佳做法分析器时，该工具会向您提供一个选项，可用于搜索该工具的最新更新。</span><span class="sxs-lookup"><span data-stu-id="f8978-106">When you start Best Practices Analyzer, the tool provides you with an option to search for the latest updates to the tool.</span></span> <span data-ttu-id="f8978-107">如果有可用更新，则可以下载更新。</span><span class="sxs-lookup"><span data-stu-id="f8978-107">If an update is available, you can download the update.</span></span> <span data-ttu-id="f8978-108">如果您选择不下载更新，或者最佳做法分析器无法访问 Internet，则可以继续使用计算机上已有的版本。</span><span class="sxs-lookup"><span data-stu-id="f8978-108">If you choose not to download updates, or if Best Practices Analyzer cannot access the Internet, you can continue to use the version that is already on the computer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f8978-109">如果需要代理身份验证才能访问 Internet，最佳做法分析器无法访问要下载的新更新。</span><span class="sxs-lookup"><span data-stu-id="f8978-109">If you need proxy authentication to access the Internet, Best Practices Analyzer cannot access new updates for you to download.</span></span> <span data-ttu-id="f8978-110">但是，您可以从 Microsoft 下载中心手动下载最新版本的 RtcBPA.msi <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A> 。</span><span class="sxs-lookup"><span data-stu-id="f8978-110">However, you can manually download the latest version of RtcBPA.msi from the Microsoft Download Center at <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A>.</span></span> <span data-ttu-id="f8978-111">下载文件后，您可以将其复制到要更新最佳做法分析器的计算机上，并使用 .msi 文件在该计算机上安装新版本的工具。</span><span class="sxs-lookup"><span data-stu-id="f8978-111">After downloading the file, you can copy it to the computer on which you want to update Best Practices Analyzer and use the .msi file to install the new version of the tool on that computer.</span></span>



</div>

<span data-ttu-id="f8978-112">若要更新最佳做法分析器规则，必须以本地计算机上的管理员身份运行该工具。</span><span class="sxs-lookup"><span data-stu-id="f8978-112">To update Best Practices Analyzer rules, you must run the tool as an Administrator on the local computer.</span></span> <span data-ttu-id="f8978-113">如果您未使用管理员组成员的帐户登录，并且检测到更新，请关闭最佳做法分析器，然后按以下步骤启动程序。</span><span class="sxs-lookup"><span data-stu-id="f8978-113">If you are not logged on using an account that is a member of the Administrators group and updates are detected, close Best Practices Analyzer, and then use the following procedure to start the program.</span></span>

<div>

## <a name="to-open-best-practices-analyzer-as-administrator-to-check-for-updates"></a><span data-ttu-id="f8978-114">以管理员身份打开最佳做法分析器以检查更新</span><span class="sxs-lookup"><span data-stu-id="f8978-114">To open Best Practices Analyzer as Administrator to check for updates</span></span>

1.  <span data-ttu-id="f8978-115">在安装了最佳做法分析器的计算机上，单击 " **开始**"，指向 " **Microsoft Lync Server 2013**"，右键单击 " **最佳做法分析器**"，然后单击 " **以管理员身份运行**"。</span><span class="sxs-lookup"><span data-stu-id="f8978-115">On a computer on which Best Practices Analyzer is installed, click **Start**, point to **Microsoft Lync Server 2013**, right-click **Best Practices Analyzer**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="f8978-116">指定属于管理员组成员的帐户的凭据。</span><span class="sxs-lookup"><span data-stu-id="f8978-116">Specify credentials of an account that is a member of the Administrators group.</span></span>

<span data-ttu-id="f8978-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8978-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

