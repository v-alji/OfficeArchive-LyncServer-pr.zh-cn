---
title: Lync Server 2013：文档
description: Lync Server 2013：文档。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Documentation
ms:assetid: 5a69c0a2-0986-49c3-809c-89bc175a34ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720335(v=OCS.15)
ms:contentKeyID: 63969609
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f128daa7941db8ae461b4bb12bcc9b97bbb5876e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49391746"
---
# <a name="documentation-in-lync-server-2013"></a><span data-ttu-id="a5b18-103">Lync Server 2013 中的文档</span><span class="sxs-lookup"><span data-stu-id="a5b18-103">Documentation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5b18-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5b18-104">

<span> </span></span></span>

<span data-ttu-id="a5b18-105">_**主题上次修改时间：** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="a5b18-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="a5b18-106">MOF 模型由许多服务管理功能组成。</span><span class="sxs-lookup"><span data-stu-id="a5b18-106">The MOF model is composed of many service management functions.</span></span> <span data-ttu-id="a5b18-107">有关任务执行方式和时间的文档可与同一团队的成员或与其他团队共享。</span><span class="sxs-lookup"><span data-stu-id="a5b18-107">Documentation about how and when tasks are performed can be shared with members of the same team or with other teams.</span></span> <span data-ttu-id="a5b18-108">存储和共享文档的方法可能会根据函数的类型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="a5b18-108">The method of storing and sharing documentation can vary according to the type of function.</span></span> <span data-ttu-id="a5b18-109">例如，系统管理过程可能存储为 Word 文档，因为它们很可能会经常打印和引用。</span><span class="sxs-lookup"><span data-stu-id="a5b18-109">For example, the procedures for system administration may be stored as Word documents because they are likely to be printed and referenced frequently.</span></span> <span data-ttu-id="a5b18-110">配置管理信息可能会自动生成并存储在数据库中，以便轻松进行搜索和编制索引。</span><span class="sxs-lookup"><span data-stu-id="a5b18-110">Configuration management information may be automatically generated and stored in a database for easy searching and indexing.</span></span> <span data-ttu-id="a5b18-111">某些文档可能是敏感的，应该受到限制。</span><span class="sxs-lookup"><span data-stu-id="a5b18-111">Some documentation may be sensitive and should be restricted.</span></span>

<div>

## <a name="document-management-systems"></a><span data-ttu-id="a5b18-112">文档管理系统</span><span class="sxs-lookup"><span data-stu-id="a5b18-112">Document management systems</span></span>

<span data-ttu-id="a5b18-113">文档管理系统充当文档的中央存储库，可帮助确保仅提供文档的最新修订版本。</span><span class="sxs-lookup"><span data-stu-id="a5b18-113">A documentation management system acts as a central repository for documents and helps ensure that only the latest revision of a document is available.</span></span> <span data-ttu-id="a5b18-114">您还可以考虑存档文档的旧版本以供参考。</span><span class="sxs-lookup"><span data-stu-id="a5b18-114">You can also consider archiving the older version of the document for reference.</span></span> <span data-ttu-id="a5b18-115">Lync 服务器提供适用于此任务的功能。</span><span class="sxs-lookup"><span data-stu-id="a5b18-115">Lync Server provides functionality suitable to this task.</span></span>

</div>

<div>

## <a name="databases"></a><span data-ttu-id="a5b18-116">数据库</span><span class="sxs-lookup"><span data-stu-id="a5b18-116">Databases</span></span>

<span data-ttu-id="a5b18-117">讨论了一些适用于使用数据库的工具和管理功能。</span><span class="sxs-lookup"><span data-stu-id="a5b18-117">Several tools and management functions were discussed that are suited to using databases.</span></span> <span data-ttu-id="a5b18-118">配置管理过程可能使用存储大量需要索引和搜索的数据的自动流程。</span><span class="sxs-lookup"><span data-stu-id="a5b18-118">The configuration management process is likely to use automated processes that store large amounts of data that require indexing and searching.</span></span> <span data-ttu-id="a5b18-119">支持人员可以在解决新问题时搜索过去问题和解决方法的数据库。</span><span class="sxs-lookup"><span data-stu-id="a5b18-119">Support staff may search a database of past issues and resolutions when troubleshooting new issues.</span></span>

<span data-ttu-id="a5b18-120">可能会有不同的数据库被用于不同的用途。</span><span class="sxs-lookup"><span data-stu-id="a5b18-120">It is likely that there will be different databases being used for different purposes.</span></span> <span data-ttu-id="a5b18-121">确定是否应链接或合并这些数据库。</span><span class="sxs-lookup"><span data-stu-id="a5b18-121">Decide if these databases should be linked or combined.</span></span> <span data-ttu-id="a5b18-122">例如，如果服务台发现一个常见主题 (的多个问题（例如新软件导致特定网络) 适配器出现问题），则支持人员可以查询配置数据库以预测可能受到影响的计算机数。</span><span class="sxs-lookup"><span data-stu-id="a5b18-122">For example, if the service desk identifies several issues with a common theme (such as new software causing an issue with a particular network adapter), the support staff can query the configuration database to predict how many computers might be affected.</span></span>

<span data-ttu-id="a5b18-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5b18-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

