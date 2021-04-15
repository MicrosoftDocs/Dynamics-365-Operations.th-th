---
title: กลุ่มผู้ขนส่ง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าข้อมูลสำหรับกลุ่มผู้ขนส่ง
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9fe95ee9a0b6d69544f35ac6bc9cdf3dd00db291
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809073"
---
# <a name="carrier-groups"></a><span data-ttu-id="48398-103">กลุ่มผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="48398-103">Carrier groups</span></span>

<span data-ttu-id="48398-104">กลุ่มผู้ขนส่งเป็นชุดของผู้ขนส่งสินค้าและบริการผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="48398-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="48398-105">กลุ่มผู้ขนส่งแต่ละกลุ่มจะระบุลำดับที่ต้องการสำหรับผู้ขนส่งสินค้าและบริการของผู้ขนส่งที่เป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="48398-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="48398-106">เมื่อมีผู้ขนส่งสินค้าและบริการผู้ขนส่งหลายรายอยู่สำหรับเซ็กเมนต์กระบวนการผลิตเดียวกัน คุณสามารถระบุกลุ่มผู้ขนส่งแทนผู้ขนส่งสินค้าและบริการผู้ขนส่งที่ระบุในแผนกระบวนการผลิตหรือคู่มือกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="48398-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="48398-107">สร้างกลุ่มผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="48398-107">Create a carrier group</span></span>

1. <span data-ttu-id="48398-108">ไปที่ **การจัดการการขนส่ง &gt; การตั้งค่า &gt; ผู้ขนส่ง &gt; กลุ่มผู้ขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="48398-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="48398-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="48398-109">Select **New**.</span></span>
1. <span data-ttu-id="48398-110">ในฟิลด์ **กลุ่มผู้ขนส่ง** ให้ป้อนรหัสเฉพาะ (ID) สำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="48398-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="48398-111">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="48398-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="48398-112">บนแท็บด่วน **รายละเอียด** ให้เพิ่มแถว และเลือกผู้ขนส่งสินค้าและบริการผู้ขนส่งสำหรับผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="48398-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="48398-113">ทำซ้ำขั้นตอนนี้จนกว่าคุณจะเพิ่มผู้ขนส่งมากเท่าที่คุณต้องการสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="48398-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="48398-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="48398-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]