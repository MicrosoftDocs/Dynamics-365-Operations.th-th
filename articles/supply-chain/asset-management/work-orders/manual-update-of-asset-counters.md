---
title: การอัปเดตตัวนับสินทรัพย์ด้วยตนเอง
description: หัวข้อนี้อธิบายการอัปเดตตัวนับสินทรัพย์ด้วยตนเองในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875926"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="bb64f-103">การอัปเดตตัวนับสินทรัพย์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bb64f-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="bb64f-104">ตัวนับถูกใช้ในการสร้างการลงทะเบียนของสินทรัพย์ที่เกี่ยวข้อง ตัวอย่างเช่น จำนวนชั่วโมงในการดำเนินงาน หรือจำนวนของปริมาณที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="bb64f-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="bb64f-105">ถ้าชนิดตัวนับที่เลือกไว้สำหรับตัวนับถูกตั้งค่าให้สืบทอดค่าตัวนับ (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ชนิดสินทรัพย์** > **ตัวนับ** > **ทั่วไป** เเท็บด่วน > **สืบทอดค่าตัวนับสินทรัพย์** ตั้งค่าปุ่มสลับเป็น "ใช่") จากนั้น เมื่อคุณสร้างรายการตัวนับใหม่ของชนิดนั้น สินทรัพย์รองทั้งหมดที่ใช้ชนิดตัวนับเดียวกันจะถูกอัพเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bb64f-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="bb64f-106">ใน **สินทรัพย์ทั้งหมด** คุณสร้างการลงทะเบียนตัวนับชั่วโมงหรือปริมาณในสินทรัพย์ ตามการอ่านของคุณในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="bb64f-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="bb64f-107">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bb64f-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="bb64f-108">เลือกสินทรัพย์ในรายการ และคลิก **ตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="bb64f-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="bb64f-109">ในแบบฟอร์ม **ตัวนับสินทรัพย์** คุณสามารถดูรายการของการลงทะเบียนตัวนับก่อนหน้านี้ทั้งหมดในสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bb64f-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="bb64f-110">คลิก **สร้าง** เพื่อสร้างการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bb64f-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="bb64f-111">รหัสสินทรัพย์จะถูกแทรกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bb64f-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="bb64f-112">ในฟิลด์ **ตัวนับ** เลือกตัวนับที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="bb64f-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="bb64f-113">เฉพาะตัวนับที่เกี่ยวข้องกับชนิดสินทรัพย์ที่เลือกไว้ในสินทรัพย์เท่านั้นที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb64f-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="bb64f-114">หน่วยที่เกี่ยวข้องจะถูกเเทรกโดยอัตโนมัติในฟิลด์ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="bb64f-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="bb64f-115">เลือกวันที่และเวลาสำหรับการลงทะเบียนตัวนับ</span><span class="sxs-lookup"><span data-stu-id="bb64f-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="bb64f-116">ในฟิลด์ **ค่า** เเทรกหมายเลขนับตั้งแต่การลงทะเบียนตัวนับครั้งล่าสุด หรือ ในฟิลด์ **มูลค่ารวม** เเทรกหมายเลขการตรวจนับรวม</span><span class="sxs-lookup"><span data-stu-id="bb64f-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="bb64f-117">ถ้าคุณได้ติดตั้งตัวนับใหม่บนสินทรัพย์ คุณต้องลงทะเบียนการเปลี่ยนแปลงบนสินทรัพย์ใน **ตัวนับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="bb64f-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="bb64f-118">ถัดไป คุณต้องสร้างรายการการลงทะเบียนสองรายการที่มีการลงเวลาที่เหมือนกัน และบนรายการเกี่ยวกับตัวนับใหม่ คุณเลือกกล่องกาเครื่องหมาย **รีเซ็ตตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="bb64f-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="bb64f-119">เมื่อคุณสร้างรายการการลงทะเบียนสองรายการ รายการเเรกต้องสำหรับตัวนับที่คุณเเทนที่</span><span class="sxs-lookup"><span data-stu-id="bb64f-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="bb64f-120">ในฟิลด์ **รวม** หมายเลขการตรวจนับรวมคือผลรวมของตัวนับของค่าลงทะเบียนทั้งหมดบนชนิดตัวนับ</span><span class="sxs-lookup"><span data-stu-id="bb64f-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="bb64f-121">ถ้ากล่องกาเครื่องหมาย **รีเซ็ตตัวนับ** ถูกเลือกบนสินทรัพย์โดยใช้เเผนการบำรุงรักษา "หนึ่งครั้งจาก ..." หรือ "เมื่อถึง ..." ชนิดของช่วงเวลา ตัวนับยังคงใช้งานอยู่บนรายการตัวนับใหม่เนื่องจากคุณสร้างรายการตัวนับที่แยกต่างหาก และเริ่มต้นด้วยตัวนับใหม่</span><span class="sxs-lookup"><span data-stu-id="bb64f-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![รูปที่ 1](media/11-work-orders.png)


<span data-ttu-id="bb64f-123">ถ้าคุณจำเป็นต้องทำการลงทะเบียนตัวนับบนสินทรัพย์หลายรายการ ซึ่งสามารถทำได้ใน **การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **ตัวนับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="bb64f-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="bb64f-124">คุณสามารถตั้งค่าช่วงเพื่อกำหนดความเเตกต่างในการลงทะเบียนตัวนับด้วยตนเอง และชนิดของข้อความที่ควรแสดงถ้ามีการลงทะเบียนอยู่นอกช่วงที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="bb64f-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="bb64f-125">อ้างอิงถึง [ตัวนับ](../setup-for-objects/counters.md) หัวข้อเกี่ยวกับการตั้งค่าตัวนับ</span><span class="sxs-lookup"><span data-stu-id="bb64f-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
