---
title: Lync Server 2013：配置语音策略和 PSTN 用法记录以授权呼叫功能和权限
description: Lync Server 2013：配置语音策略和 PSTN 使用记录以授权呼叫功能和权限。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring voice policies and PSTN usage records to authorize calling features and privileges
ms:assetid: 63f22010-a3d7-4cbd-86e8-6fc0e13c2b84
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398450(v=OCS.15)
ms:contentKeyID: 48184307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a12c9c64c3f02effba7c7709321eda91350ebb75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432392"
---
# <a name="configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges-in-lync-server-2013"></a><span data-ttu-id="b535e-103">在 Lync Server 2013 中配置语音策略和 PSTN 用法记录以授权呼叫功能和权限</span><span class="sxs-lookup"><span data-stu-id="b535e-103">Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b535e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b535e-104">

<span> </span></span></span>

<span data-ttu-id="b535e-105">_**主题上次修改时间：** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="b535e-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="b535e-106">*语音策略* 支持一组呼叫功能，并关联一个或多个 PSTN 使用记录，以定义分配了该策略的用户的呼叫功能和权限。</span><span class="sxs-lookup"><span data-stu-id="b535e-106">A *voice policy* enables a set of calling features and associates one or more PSTN usage records to define the calling features and permissions of users who are assigned the policy.</span></span>

<span data-ttu-id="b535e-107">语音策略作用域可以是 *网站* (，它定义网络网站的默认功能和权限) 或 *用户* (，用于定义在每个用户或组基础上分配的功能和权限) 。</span><span class="sxs-lookup"><span data-stu-id="b535e-107">Voice policy scope can be either *Site* (which defines the default features and permissions for a network site) or *User* (which defines the features and permissions to be assigned on a per-user or group basis).</span></span> <span data-ttu-id="b535e-108">未分配到语音策略的用户将自动分配给全局策略，该策略是随产品一起安装的默认语音策略。</span><span class="sxs-lookup"><span data-stu-id="b535e-108">Users not assigned to a voice policy will automatically be assigned to the global policy, which is the default voice policy that is installed with the product.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b535e-109">有关详细信息，请参阅规划文档中 <A href="lync-server-2013-voice-policies.md">Lync Server 2013 中的语音策略</A> 。</span><span class="sxs-lookup"><span data-stu-id="b535e-109">For details, see <A href="lync-server-2013-voice-policies.md">Voice policies in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b535e-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="b535e-110">In This Section</span></span>

  - [<span data-ttu-id="b535e-111">在 Lync Server 2013 中创建语音策略和配置 PSTN 使用记录</span><span class="sxs-lookup"><span data-stu-id="b535e-111">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="b535e-112">在 Lync Server 2013 中修改语音策略和配置 PSTN 使用记录</span><span class="sxs-lookup"><span data-stu-id="b535e-112">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="b535e-113">在 Lync Server 2013 中配置语音邮件转义</span><span class="sxs-lookup"><span data-stu-id="b535e-113">Configuring voice mail escape in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-mail-escape.md)

<span data-ttu-id="b535e-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b535e-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

