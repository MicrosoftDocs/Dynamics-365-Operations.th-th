---
title: กลุ่มผู้ขนส่ง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าข้อมูลสำหรับกลุ่มผู้ขนส่ง
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646442"
---
# <a name="carrier-groups"></a><span data-ttu-id="19f7e-103">กลุ่มผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="19f7e-103">Carrier groups</span></span>

<span data-ttu-id="19f7e-104">กลุ่มผู้ขนส่งเป็นชุดของผู้ขนส่งสินค้าและบริการผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="19f7e-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="19f7e-105">กลุ่มผู้ขนส่งแต่ละกลุ่มจะระบุลำดับที่ต้องการสำหรับผู้ขนส่งสินค้าและบริการของผู้ขนส่งที่เป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="19f7e-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="19f7e-106">เมื่อมีผู้ขนส่งสินค้าและบริการผู้ขนส่งหลายรายอยู่สำหรับเซ็กเมนต์กระบวนการผลิตเดียวกัน คุณสามารถระบุกลุ่มผู้ขนส่งแทนผู้ขนส่งสินค้าและบริการผู้ขนส่งที่ระบุในแผนกระบวนการผลิตหรือคู่มือกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="19f7e-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="19f7e-107">สร้างกลุ่มผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="19f7e-107">Create a carrier group</span></span>

1. <span data-ttu-id="19f7e-108">ไปที่ **การจัดการการขนส่ง &gt; การตั้งค่า &gt; ผู้ขนส่ง &gt; กลุ่มผู้ขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="19f7e-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="19f7e-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="19f7e-109">Select **New**.</span></span>
1. <span data-ttu-id="19f7e-110">ในฟิลด์ **กลุ่มผู้ขนส่ง** ให้ป้อนรหัสเฉพาะ (ID) สำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="19f7e-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="19f7e-111">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="19f7e-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="19f7e-112">บนแท็บด่วน **รายละเอียด** ให้เพิ่มแถว และเลือกผู้ขนส่งสินค้าและบริการผู้ขนส่งสำหรับผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="19f7e-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="19f7e-113">ทำซ้ำขั้นตอนนี้จนกว่าคุณจะเพิ่มผู้ขนส่งมากเท่าที่คุณต้องการสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="19f7e-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="19f7e-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="19f7e-114">Close the page.</span></span>
