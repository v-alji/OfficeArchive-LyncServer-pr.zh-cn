---
title: Lync Server 2013：设置公共即时消息连接
description: Lync Server 2013：设置公共即时消息连接。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up public instant messaging connectivity
ms:assetid: 816dea2a-96fa-4a36-b6c2-a9402675868b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205041(v=OCS.15)
ms:contentKeyID: 48184661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2f11c5e01de697b97395b6bc52815fadedff5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441702"
---
# <a name="setting-up-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="ca1dd-103">在 Lync Server 2013 中设置公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="ca1dd-103">Setting up public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ca1dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ca1dd-104">

<span> </span></span></span>

<span data-ttu-id="ca1dd-105">_**主题上次修改时间：** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="ca1dd-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="ca1dd-106">如果你的组织希望支持公共即时消息 (IM) 与 AOL 的连接，则无法使用 Lync Server 部署向导请求证书。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-106">If your organization wants to support public instant messaging (IM) connectivity with AOL, you cannot use the Lync Server Deployment Wizard to request the certificate.</span></span> <span data-ttu-id="ca1dd-107">请改为执行以下过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-107">Instead, perform the steps in the following procedure.</span></span>

<div>

## <a name="setting-up-public-instant-messaging-connectivity"></a><span data-ttu-id="ca1dd-108">设置公共即时消息连接</span><span class="sxs-lookup"><span data-stu-id="ca1dd-108">Setting Up Public Instant Messaging Connectivity</span></span>

1.  <span data-ttu-id="ca1dd-109">在前端服务器上，打开拓扑生成器。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-109">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="ca1dd-110">展开 "边缘池"，然后右键单击 "边缘服务器" 或 "边缘服务器" 池。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-110">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="ca1dd-111">选择 "编辑属性"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-111">Select Edit properties.</span></span>

2.  <span data-ttu-id="ca1dd-112">在 "编辑属性" 下的 "常规" 下，选择 "为此边缘池启用联盟" (端口 5061) 。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-112">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="ca1dd-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-113">Click OK.</span></span>

3.  <span data-ttu-id="ca1dd-114">单击 "操作"，选择 "拓扑"，选择 "发布"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-114">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="ca1dd-115">当系统提示发布拓扑时，单击 "下一步"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-115">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="ca1dd-116">发布完成后，单击 "完成"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-116">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="ca1dd-117">在边缘服务器上，打开 "Lync Server 部署向导"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-117">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="ca1dd-118">单击 "安装或更新 Lync 服务器系统"，然后单击 "设置" 或 "删除 Lync Server 组件"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-118">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="ca1dd-119">再次单击 "运行"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-119">Click Run Again.</span></span>

5.  <span data-ttu-id="ca1dd-120">在 "安装 Lync 服务器组件" 中，单击 "下一步"。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-120">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="ca1dd-121">"摘要" 屏幕将显示执行时的操作。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-121">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="ca1dd-122">部署完成后，单击 "查看日志" 以查看可用的日志文件。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-122">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="ca1dd-123">单击 "完成" 以完成部署。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-123">Click Finish to complete the deployment.</span></span>

</div>

<div>

## <a name="to-create-a-certificate-request-for-the-external-interface-of-the-edge-server-to-support-public-im-connectivity-with-aol"></a><span data-ttu-id="ca1dd-124">为边缘服务器的外部接口创建证书请求以支持与 AOL 的公共 IM 连接</span><span class="sxs-lookup"><span data-stu-id="ca1dd-124">To create a certificate request for the external interface of the Edge Server to support public IM connectivity with AOL</span></span>

1.  <span data-ttu-id="ca1dd-125">当所需模板可供 CA 使用时，请从 Edge 服务器使用以下 Windows PowerShell cmdlet 来申请证书</span><span class="sxs-lookup"><span data-stu-id="ca1dd-125">When the required template is available to the CA, use the following Windows PowerShell cmdlet from at the Edge Server to request the certificate</span></span>
    
        Request-CsCertificate -New -Type AccessEdgeExternal  -Output C:\ <certfilename.txt or certfilename.csr>  -ClientEku $true -Template <template name>
    
    <span data-ttu-id="ca1dd-126">Lync Server 使用的模板的默认证书名称是 Web 服务器。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-126">The default certificate name of the template used for Lync Server is Web Server.</span></span> <span data-ttu-id="ca1dd-127">仅指定 \<template name\> 需要使用不同于默认模板的模板。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-127">Only specify the \<template name\> if you need to use a template that is different from the default template.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ca1dd-128">如果你的组织希望支持与 AOL 的公共 IM 连接，你必须使用 Windows PowerShell 而不是证书向导请求将证书分配给访问边缘服务的外部边缘。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-128">If your organization wants to support public IM connectivity with AOL, you must use Windows PowerShell instead of the Certificate Wizard to request the certificate to be assigned to the external edge for the Access Edge service.</span></span> <span data-ttu-id="ca1dd-129">这是因为证书向导用于申请证书的证书颁发机构 (CA) Web 服务器模板不支持客户端 EKU 配置。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-129">This is because the Certificate Authority (CA) Web Server template that the Certificate Wizard uses to request a certificate does not support client EKU configuration.</span></span> <span data-ttu-id="ca1dd-130">在使用 Windows PowerShell 创建证书之前，CA 管理员必须创建和部署支持客户端 EKU 的新模板。</span><span class="sxs-lookup"><span data-stu-id="ca1dd-130">Before using Windows PowerShell to create the certificate, the CA administrator must create and deploy a new template that supports client EKU.</span></span>

    
    <span data-ttu-id="ca1dd-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ca1dd-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

