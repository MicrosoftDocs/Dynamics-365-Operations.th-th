---
title: การอัปเดตตัวนับสินทรัพย์ด้วยตนเอง
description: หัวข้อนี้อธิบายการอัปเดตตัวนับสินทรัพย์ด้วยตนเองในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23a94415a662059ddbd41cc6a0ba9dab24aae44e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889444"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="18851-103">การอัปเดตตัวนับสินทรัพย์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="18851-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="18851-104">ตัวนับจะใช้ในการสร้างการลงทะเบียนในสินทรัพย์ เช่น การลงทะเบียนเกี่ยวกับจำนวนชั่วโมงที่มีการดำเนินงานสินทรัพย์หรือปริมาณที่มีการผลิต</span><span class="sxs-lookup"><span data-stu-id="18851-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="18851-105">ชนิดตัวนับที่ถูกเลือกสำหรับตัวนับอาจถูกตั้งค่าให้สืบทอดค่าตัวนับ</span><span class="sxs-lookup"><span data-stu-id="18851-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="18851-106">กล่าวคือ มีการตั้งค่าตัวเลือก **สืบทอดมูลค่าของตัวนับสินทรัพย์** เป็น **ใช่** บน FastTab **ทั่วไป** ของหน้า **ตัวนับ** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ชนิดสินทรัพย์** > **ตัวนับ**)</span><span class="sxs-lookup"><span data-stu-id="18851-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="18851-107">ในกรณีนี้ เมื่อคุณสร้างรายการตัวนับใหม่ของชนิดนั้น สินทรัพย์รองทั้งหมดที่ใช้ชนิดตัวนับเดียวกันจะถูกอัพเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="18851-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="18851-108">บนหน้า **สินทรัพย์ทั้งหมด** คุณสร้างการลงทะเบียนตัวนับชั่วโมงหรือปริมาณในสินทรัพย์ ตามการอ่านของคุณในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="18851-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="18851-109">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="18851-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="18851-110">เลือกสินทรัพย์ และจากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **สินทรัพย์** ในกลุ่ม **เชิงป้องกัน** เลือก **ตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="18851-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="18851-111">บนหน้า **ตัวนับสินทรัพย์** แสดงรายการของการลงทะเบียนตัวนับก่อนหน้านี้ทั้งหมดที่ถูกดำเนินการในสินทรัพย์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="18851-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="18851-112">เลือก **สร้าง** เพื่อสร้างการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="18851-112">Select **New** to create a registration.</span></span> <span data-ttu-id="18851-113">รหัสสินทรัพย์ถูกป้อนโดยอัตโนมัติลงในฟิลด์ **สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="18851-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="18851-114">ในฟิลด์ **ตัวนับ** เลือกตัวนับที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="18851-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="18851-115">เฉพาะตัวนับที่เกี่ยวข้องกับชนิดสินทรัพย์ที่เลือกไว้ในสินทรัพย์เท่านั้นที่พร้อมใช้งานสำหรับการเลือก</span><span class="sxs-lookup"><span data-stu-id="18851-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="18851-116">หน่วยที่เกี่ยวข้องจะถูกป้อนโดยอัตโนมัติในฟิลด์ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="18851-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="18851-117">ในฟิลด์ **ลงทะเบียน** ให้เลือกวันที่และเวลาสำหรับการลงทะเบียนตัวนับ</span><span class="sxs-lookup"><span data-stu-id="18851-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="18851-118">ในฟิลด์ **ค่า** ป้อนหมายเลขตั้งแต่การลงทะเบียนตัวนับสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="18851-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="18851-119">อีกทางหนึ่งคือ ในฟิลด์ **มูลค่ารวม** ให้ป้อนหมายเลขการตรวจนับทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="18851-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="18851-120">บันทึกคะแนนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="18851-120">Note the following points:</span></span>

- <span data-ttu-id="18851-121">ถ้าคุณได้ติดตั้งตัวนับใหม่บนสินทรัพย์ คุณต้องลงทะเบียนการเปลี่ยนแปลงบนสินทรัพย์ในหน้า **ตัวนับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="18851-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="18851-122">หลังจากนั้นคุณต้องสร้างรายการลงทะเบียนสองรายการที่มีการลงเวลาที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="18851-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="18851-123">รายการแรกต้องเป็นตัวนับที่คุณกำลังจะแทนที่</span><span class="sxs-lookup"><span data-stu-id="18851-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="18851-124">บนรายการที่เกี่ยวข้องกับตัวนับใหม่ ให้เลือกกล่องกาเครื่องหมาย **รีเซ็ตตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="18851-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="18851-125">ในฟิลด์ **รวม** หมายเลขการตรวจนับรวมคือผลรวมของตัวนับของค่าลงทะเบียนทั้งหมดบนชนิดตัวนับนั้น</span><span class="sxs-lookup"><span data-stu-id="18851-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="18851-126">ถ้ากล่องกาเครื่องหมาย **รีเซ็ตตัวนับ** ถูกเลือกบนสินทรัพย์โดยใช้เเผนการบำรุงรักษาที่มีชนิดของช่วงเวลา "หนึ่งครั้งจาก ..." หรือ "เมื่อถึง ..." ตัวนับยังคงใช้งานอยู่บนรายการตัวนับใหม่ เนื่องจากคุณสร้างรายการตัวนับที่แยกต่างหาก และเริ่มต้นด้วยตัวนับใหม่</span><span class="sxs-lookup"><span data-stu-id="18851-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="18851-127">ภาพประกอบด้านล่างแสดงตัวอย่างของหน้า **ตัวนับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="18851-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![รูปที่ 1](media/11-work-orders.png)

<span data-ttu-id="18851-129">บนหน้า **ตัวนับสินทรัพย์** (**การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **ตัวนับสินทรัพย์**) คุณสามารถทำการลงทะเบียนตัวนับในสินทรัพย์ต่างๆ ในเวลาเดียวกันได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="18851-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="18851-130">คุณสามารถตั้งค่าช่วงเพื่อกำหนดความเบี่ยงเบนในการลงทะเบียนตัวนับด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="18851-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="18851-131">นอกจากนี้ คุณยังสามารถระบุชนิดของข้อความที่จะแสดงขึ้น ถ้าการลงทะเบียนอยู่นอกช่วงที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="18851-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="18851-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าตัวนับ ให้ดูที่ [ตัวนับ](../setup-for-objects/counters.md)</span><span class="sxs-lookup"><span data-stu-id="18851-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

