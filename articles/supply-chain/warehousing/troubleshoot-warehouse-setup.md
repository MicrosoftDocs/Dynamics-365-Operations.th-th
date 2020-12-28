---
title: แก้ไขปัญหาการตั้งค่าคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณตั้งค่าคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2158c097fafb6c35bce7dc28a29c175f458cde1b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645852"
---
# <a name="troubleshoot-warehouse-setup"></a><span data-ttu-id="77737-103">แก้ไขปัญหาการตั้งค่าคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="77737-103">Troubleshoot warehouse setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77737-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณตั้งค่าคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="77737-104">This topic describes how to fix common issues that you might encounter while you set up warehouses in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-use-any-role-except-administrator-to-access-the-mobile-device-app-emulator"></a><span data-ttu-id="77737-105">ฉันไม่สามารถใช้บทบาทใด ๆ ยกเว้นผู้ดูแลระบบเพื่อเข้าถึงตัวเลียนแบบแอปบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="77737-105">I can't use any role except administrator to access the mobile device app emulator.</span></span>

### <a name="issue-description"></a><span data-ttu-id="77737-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="77737-106">Issue description</span></span>

<span data-ttu-id="77737-107">คุณไม่สามารถใช้บทบาทใด ๆ ยกเว้นผู้ดูแลระบบเพื่อเข้าถึงตัวเลียนแบบแอปบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="77737-107">You can't any use role except the administrator tole to access the mobile device app emulator.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="77737-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="77737-108">Issue resolution</span></span>

<span data-ttu-id="77737-109">ตัวเลียนแบบแอปบนอุปกรณ์เคลื่อนที่มีการตั้งค่าให้ทำงานกับบัญชีผู้ดูแลระบบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="77737-109">The mobile device app emulator is set to work only with the administrator account.</span></span> <span data-ttu-id="77737-110">สำหรับวัตถุประสงค์ในการทดสอบและการดำเนินการสด เราขอแนะนำให้คุณใช้แอปคลังสินค้าเอง</span><span class="sxs-lookup"><span data-stu-id="77737-110">For all testing and live process purposes, we recommend that you use the warehouse app itself.</span></span>
