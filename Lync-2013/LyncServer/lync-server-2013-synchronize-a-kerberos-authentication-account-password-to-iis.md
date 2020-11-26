---
title: 将 Kerberos 身份验证帐户密码同步到 IIS
description: 将 Kerberos 身份验证帐户密码同步到 IIS。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Synchronize a Kerberos authentication account password to IIS
ms:assetid: 05925a66-2684-4c1b-adfa-69bd0da1bf38
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398107(v=OCS.15)
ms:contentKeyID: 48183296
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59555fc25088d0d932105f77051f959b4bcebb46
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444581"
---
# <a name="synchronize-a-kerberos-authentication-account-password-to-iis-in-lync-server-2013"></a><span data-ttu-id="b50f4-103">在 Lync Server 2013 中将 Kerberos 身份验证帐户密码同步到 IIS</span><span class="sxs-lookup"><span data-stu-id="b50f4-103">Synchronize a Kerberos authentication account password to IIS in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b50f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b50f4-104">

<span> </span></span></span>

<span data-ttu-id="b50f4-105">_**主题上次修改时间：** 2010-11-08_</span><span class="sxs-lookup"><span data-stu-id="b50f4-105">_**Topic Last Modified:** 2010-11-08_</span></span>

<span data-ttu-id="b50f4-106">若要成功完成此过程，你应以 RTCUniversalServerAdmins 组成员的用户身份登录。</span><span class="sxs-lookup"><span data-stu-id="b50f4-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="b50f4-107">在网站、前端服务器、标准版服务器和控制器上，可以使用 Kerberos 身份验证帐户对 Web 服务服务请求进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="b50f4-107">In a site, Front End Servers, Standard Edition servers, and Directors can use a Kerberos authentication account for purposes of authenticating requests to the Web Services service.</span></span> <span data-ttu-id="b50f4-108">此过程将在已分配 Kerberos 帐户的网站中查找运行 Web 服务的每台服务器，并将 Internet 信息服务 (IIS) 配置设置更新为使用 Kerberos 帐户。</span><span class="sxs-lookup"><span data-stu-id="b50f4-108">This procedure locates each server running Web Services in a site that has been assigned a Kerberos account and updates the Internet Information Services (IIS) configuration settings to use the Kerberos account.</span></span> <span data-ttu-id="b50f4-109">有关详细信息，请参阅 [在 Lync server 2013 中的服务器上设置 Kerberos 身份验证帐户密码](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)。</span><span class="sxs-lookup"><span data-stu-id="b50f4-109">For details, see [Set a Kerberos authentication account password on a server in Lync Server 2013](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md).</span></span>

<div>

## <a name="to-set-and-configure-a-kerberos-authentication-account-password"></a><span data-ttu-id="b50f4-110">设置和配置 Kerberos 身份验证帐户密码</span><span class="sxs-lookup"><span data-stu-id="b50f4-110">To set and configure a Kerberos authentication account password</span></span>

1.  <span data-ttu-id="b50f4-111">以 RTCUniversalServerAdmins 组成员的身份登录源计算机 (例如 fe01.contoso.com) 。</span><span class="sxs-lookup"><span data-stu-id="b50f4-111">Log on to a source computer (such as fe01.contoso.com) as a member of RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="b50f4-112">启动 Lync Server 命令行管理程序：依次单击 " **开始**"、" **所有程序**"、" **Microsoft Lync server 2013**"，然后单击 " **Lync server Management shell**"。</span><span class="sxs-lookup"><span data-stu-id="b50f4-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="b50f4-113">在 Lync Server Management Shell 命令行中，运行以下两个命令：</span><span class="sxs-lookup"><span data-stu-id="b50f4-113">From the Lync Server Management Shell command line, run the following two commands:</span></span>
    
        Set-CsKerberosAccountPassword -FromComputer SourceComputer -ToComputer DestinationComputer
    
    <span data-ttu-id="b50f4-114">例如：</span><span class="sxs-lookup"><span data-stu-id="b50f4-114">For example:</span></span>
    
        Set-CsKerberosAccountPassword -FromComputer fe01.contoso.com -ToComputer dir01.contoso.com
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="b50f4-115">源计算机和目标计算机的名称必须是完全限定的域 (FQDN) 服务器名称。</span><span class="sxs-lookup"><span data-stu-id="b50f4-115">The name of the source computer and destination computer must be a fully qualified domain (FQDN) name of the server.</span></span> <span data-ttu-id="b50f4-116">除非池名称与用作源计算机或目标计算机的计算机的名称相同，否则不能使用池 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b50f4-116">You cannot use the pool FQDN unless the pool name is the same as the name of the computer that you are using as a source computer or destination computer.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="b50f4-117">对 Kerberos 身份验证进行任何更改（如添加帐户或删除帐户）后，必须从 Lync Server Management Shell 命令提示符运行 <STRONG>Enable-CsTopology</STRONG> 。</span><span class="sxs-lookup"><span data-stu-id="b50f4-117">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="b50f4-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b50f4-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

