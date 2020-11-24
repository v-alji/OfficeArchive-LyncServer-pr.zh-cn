---
title: Lync Server 2013：将 XmlAdapter 替换为自定义的持久聊天服务器合规性适配器
description: Lync Server 2013：将 XmlAdapter 替换为自定义的持久聊天服务器合规性适配器。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter
ms:assetid: 2cb70db2-663f-40a6-abcf-89ea7d4a8b65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ680106(v=OCS.15)
ms:contentKeyID: 49558152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a90b4df7df42ffdc6c55e9b551b0eb53d07ab1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "49392094"
---
# <a name="replacing-the-xmladapter-with-a-customized-persistent-chat-server-compliance-adapter-in-lync-server-2013"></a><span data-ttu-id="8cd5e-103">在 Lync Server 2013 中将 XmlAdapter 替换为自定义的持久聊天服务器合规性适配器</span><span class="sxs-lookup"><span data-stu-id="8cd5e-103">Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8cd5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8cd5e-104">

<span> </span></span></span>

<span data-ttu-id="8cd5e-105">_**主题上次修改时间：** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8cd5e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8cd5e-106">你可以编写自定义适配器，而不是使用随永久聊天服务器一起安装的 XmlAdapter。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-106">You can write a custom adapter instead of using the XmlAdapter that is installed with Persistent Chat Server.</span></span> <span data-ttu-id="8cd5e-107">若要实现此目的，您必须提供包含实现 **IComplianceAdapter** 接口的公共类的 .NET Framework 程序集。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-107">To accomplish this, you must provide a .NET Framework assembly that contains a public class that implements the **IComplianceAdapter** interface.</span></span> <span data-ttu-id="8cd5e-108">必须将此程序集放在持久聊天服务器池中每台服务器的持久聊天服务器安装文件夹中。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-108">You must place this assembly in the Persistent Chat Server installation folder of each server in your Persistent Chat Server pool.</span></span> <span data-ttu-id="8cd5e-109">任一合规性服务器都可以为您的适配器提供合规性数据，但合规性服务器不会为您的适配器的多个实例提供重复的合规性数据。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-109">Any one of the Compliance servers can provide compliance data to your adapter, but the compliance servers will not provide duplicate compliance data to multiple instances of your adapter.</span></span>

<div>

## <a name="implementing-the-icomplianceadapter-interface"></a><span data-ttu-id="8cd5e-110">实现 IComplianceAdapter 接口</span><span class="sxs-lookup"><span data-stu-id="8cd5e-110">Implementing the IComplianceAdapter interface</span></span>

<span data-ttu-id="8cd5e-111">该接口在命名空间中的 Compliance.dll 程序集中定义 `Microsoft.Rtc.Internal.Chat.Server.Compliance` 。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-111">The interface is defined in the Compliance.dll assembly in the namespace `Microsoft.Rtc.Internal.Chat.Server.Compliance`.</span></span> <span data-ttu-id="8cd5e-112">该接口定义您的自定义适配器必须实现的两种方法。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-112">The interface defines two methods that your custom adapter must implement.</span></span>

    void SetConfig(AdapterConfig config)

<span data-ttu-id="8cd5e-113">在适配器首次加载时，持久聊天合规性服务器将调用此方法。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-113">The Persistent Chat Compliance server will call this method when the adapter first loads.</span></span> <span data-ttu-id="8cd5e-114">`AdapterConfig`包含与合规性适配器相关的持久聊天合规性配置。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-114">The `AdapterConfig` contains the Persistent Chat compliance configuration that is relevant to the compliance adapter.</span></span>

    void Translate(ConversationCollection conversations)

<span data-ttu-id="8cd5e-115">只要存在要翻译的新数据，永久聊天合规性服务器将按定期时间间隔调用此方法。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-115">The Persistent Chat Compliance server calls this method at periodic intervals as long as there is new data to translate.</span></span> <span data-ttu-id="8cd5e-116">此时间间隔等于 `RunInterval` 持久聊天合规性配置中的设置。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-116">This time interval is equal to the `RunInterval` as set in the Persistent Chat Compliance configuration.</span></span>

<span data-ttu-id="8cd5e-117">`ConversationCollection`包含上次调用此方法时收集的对话信息。</span><span class="sxs-lookup"><span data-stu-id="8cd5e-117">The `ConversationCollection` contains the conversation information that was collected from the last time this method was called.</span></span>

<span data-ttu-id="8cd5e-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8cd5e-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

