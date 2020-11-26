---
title: Lync Server 2013： Lync for Android 要求
description: Lync Server 2013： Lync for Android 要求。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync for Android requirements
ms:assetid: 4ff53e03-0c1f-4a2b-9cec-1131c2a48563
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690980(v=OCS.15)
ms:contentKeyID: 53312965
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d3d3aa6e428c3a73f1b9263fe9cf13e5aa9fff0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426415"
---
# <a name="lync-for-android-requirements-in-lync-server-2013"></a><span data-ttu-id="9c80d-103">Lync Server 2013 中的 Lync for Android 要求</span><span class="sxs-lookup"><span data-stu-id="9c80d-103">Lync for Android requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c80d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c80d-104">

<span> </span></span></span>

<span data-ttu-id="9c80d-105">_**主题上次修改时间：** 2014-04-24_</span><span class="sxs-lookup"><span data-stu-id="9c80d-105">_**Topic Last Modified:** 2014-04-24_</span></span>

<span data-ttu-id="9c80d-106">Microsoft Lync 2013 Microsoft Lync 2013 for Android 为组织中从 Android 设备连接的用户提供即时消息 (IM) 、增强状态和 Lync 会议加入功能。</span><span class="sxs-lookup"><span data-stu-id="9c80d-106">Microsoft Lync 2013 Microsoft Lync 2013 for Android provides instant messaging (IM), enhanced presence, and Lync meeting join capabilities for users in your organization who are connecting from an Android device.</span></span> <span data-ttu-id="9c80d-107">本主题介绍了适用于 Android 的 Lync 2013 的注意事项，包括先决条件、技术要求和必备组件。</span><span class="sxs-lookup"><span data-stu-id="9c80d-107">This topic describes considerations for Lync 2013 for Android, including prerequisites, technical requirements, and required components.</span></span>

<div>

## <a name="lync-for-android-prerequisite"></a><span data-ttu-id="9c80d-108">Lync for Android 先决条件</span><span class="sxs-lookup"><span data-stu-id="9c80d-108">Lync for Android Prerequisite</span></span>

<span data-ttu-id="9c80d-109">若要支持适用于 Android 的 Lync 2013，Android 设备必须满足以下要求：</span><span class="sxs-lookup"><span data-stu-id="9c80d-109">To support Lync 2013 for Android, the Android device must meet the following requirements:</span></span>

  - <span data-ttu-id="9c80d-110">Android 设备必须运行 Android 4.0 或更高版本的手机或平板电脑（包括平板电脑），但带有 Tegra2 芯片的设备除外。</span><span class="sxs-lookup"><span data-stu-id="9c80d-110">The Android device must be running Android 4.0 or a later phone- or tablet-oriented operating system, including tablets, except those with the Tegra2 chip.</span></span>

  - <span data-ttu-id="9c80d-111">设备必须具有 1.2 GHz 双核或更高的 CPU。</span><span class="sxs-lookup"><span data-stu-id="9c80d-111">The device must have a 1.2 GHz dual core or higher CPU.</span></span>

  - <span data-ttu-id="9c80d-112">设备摄像头 (前置/后) 分辨率应为 VGA 或更高。</span><span class="sxs-lookup"><span data-stu-id="9c80d-112">The device camera (front/rear) resolution should be VGA or higher.</span></span>

  - <span data-ttu-id="9c80d-113">其他硬件要求应与 Android 4.0 兼容性定义文档相一致。</span><span class="sxs-lookup"><span data-stu-id="9c80d-113">Other hardware requirements should be aligned with Android 4.0 Compatibility Definition Document.</span></span>

</div>

<div>

## <a name="other-technical-considerations"></a><span data-ttu-id="9c80d-114">其他技术注意事项</span><span class="sxs-lookup"><span data-stu-id="9c80d-114">Other Technical Considerations</span></span>

<span data-ttu-id="9c80d-115">在 Android 设备平台上，Lync 应用程序可以在后台运行。</span><span class="sxs-lookup"><span data-stu-id="9c80d-115">On the Android device platform, the Lync application can run in the background.</span></span> <span data-ttu-id="9c80d-116">因此，与其他移动设备平台不同，Android 设备不需要推送通知。</span><span class="sxs-lookup"><span data-stu-id="9c80d-116">Therefore, unlike other mobile device platforms, push notifications are not required for Android devices.</span></span> <span data-ttu-id="9c80d-117">在 Android 设备上退出 Lync 应用程序的唯一方法是显式注销 Lync。</span><span class="sxs-lookup"><span data-stu-id="9c80d-117">The only way to exit the Lync application on an Android device is to explicitly sign out of Lync.</span></span> <span data-ttu-id="9c80d-118">Tegra 2 芯片组的设备不支持此版本的 Lync 应用程序。</span><span class="sxs-lookup"><span data-stu-id="9c80d-118">This version of the Lync application is not supported on devices with Tegra 2 chipsets.</span></span>

<span data-ttu-id="9c80d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c80d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

