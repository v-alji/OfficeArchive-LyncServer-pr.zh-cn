---
title: 重置呼叫允许控制
description: 重置呼叫许可控制。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4539cda453de6249be3a9b9b61521ecf478cb70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443620"
---
# <a name="reset-call-admission-control"></a><span data-ttu-id="12494-103">重置呼叫允许控制</span><span class="sxs-lookup"><span data-stu-id="12494-103">Reset call admission control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12494-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12494-104">

<span> </span></span></span>

<span data-ttu-id="12494-105">_**主题上次修改时间：** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="12494-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="12494-106">如果 Lync Server 2010 前端池托管呼叫许可控制 (CAC) ，则必须先将 CAC 托管托管到 Lync Server 2013 池，然后才能删除 Lync Server 2010 前端池。</span><span class="sxs-lookup"><span data-stu-id="12494-106">If a Lync Server 2010 Front End pool is hosting call admission control (CAC), you must move CAC hosting to a Lync Server 2013 pool before you can remove the Lync Server 2010 Front End pool.</span></span>

<div>

## <a name="to-reset-cac"></a><span data-ttu-id="12494-107">重置 CAC</span><span class="sxs-lookup"><span data-stu-id="12494-107">To reset CAC</span></span>

1.  <span data-ttu-id="12494-108">打开拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="12494-108">Open Topology Builder.</span></span>

2.  <span data-ttu-id="12494-109">右键单击 "网站" 节点，然后单击 " **编辑属性**"。</span><span class="sxs-lookup"><span data-stu-id="12494-109">Right-click the site node, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="12494-110">在 " **呼叫许可控制" 设置** 下，请确保已选中 " **启用呼叫许可控制** "。</span><span class="sxs-lookup"><span data-stu-id="12494-110">Under **Call Admission Control setting**, make sure **Enable Call Admission Control** is selected.</span></span>

4.  <span data-ttu-id="12494-111">在 " **前端池" 下运行呼叫许可控制 (CAC)**，选择要托管 CAC 的 Lync Server 2013 池，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="12494-111">Under **Front End pool to run call admission control (CAC)**, select the Lync Server 2013 pool that is to host CAC, and then click **OK**.</span></span>

5.  <span data-ttu-id="12494-112">发布拓扑。</span><span class="sxs-lookup"><span data-stu-id="12494-112">Publish the topology.</span></span>

<span data-ttu-id="12494-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12494-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

