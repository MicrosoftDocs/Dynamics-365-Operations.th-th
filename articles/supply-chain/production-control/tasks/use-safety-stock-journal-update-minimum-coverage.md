---
title: ใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยเพื่ออัพเดตความครอบคลุมขั้นต่ำ
description: 'ขั้นตอนนี้แสดงวิธีการคำนวณข้อเสนอความครอบคลุมขั้นต่ำที่ขึ้นอยู่กับธุรกรรมที่ผ่านมา จากนั้นอัพเดตความครอบคลุมสินค้าที่มีข้อเสนอ '
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438713"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="f70d0-103">ใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยเพื่ออัพเดตความครอบคลุมขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f70d0-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f70d0-104">ขั้นตอนนี้แสดงวิธีการคำนวณข้อเสนอความครอบคลุมขั้นต่ำที่ขึ้นอยู่กับธุรกรรมที่ผ่านมา จากนั้นอัพเดตความครอบคลุมสินค้าที่มีข้อเสนอ </span><span class="sxs-lookup"><span data-stu-id="f70d0-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="f70d0-105">ซึ่งทำได้โดยใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย </span><span class="sxs-lookup"><span data-stu-id="f70d0-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="f70d0-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="f70d0-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f70d0-107">งานนี้มีไว้สำหรับนักวางแผนการผลิตเพื่อช่วยรักษาความครอบคลุมขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="f70d0-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="f70d0-108">สร้างชื่อสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยใหม่</span><span class="sxs-lookup"><span data-stu-id="f70d0-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="f70d0-109">ใน **บานหน้าต่างนำทาง** ไปที่ **การวางแผนหลัก > การตั้งค่า > ชื่อสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="f70d0-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="f70d0-110">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f70d0-110">Click **New**.</span></span>
3. <span data-ttu-id="f70d0-111">ในฟิลด์ **ชือ** พิมพ์ 'วัสดุ'</span><span class="sxs-lookup"><span data-stu-id="f70d0-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="f70d0-112">ในฟิลด์ **คำอธิบาย** พิมพ์ 'วัสดุ'</span><span class="sxs-lookup"><span data-stu-id="f70d0-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="f70d0-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f70d0-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="f70d0-114">สร้างสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="f70d0-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="f70d0-115">ใน **บานหน้าต่างนำทาง** ให้ไปที่ **การวางแผนหลัก > การวางแผนหลัก > รัน >การคำนวณปริมาณสินค้าคงคลังที่ปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="f70d0-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="f70d0-116">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f70d0-116">Click **New**.</span></span>
3. <span data-ttu-id="f70d0-117">ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f70d0-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="f70d0-118">เลือกชื่อสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยที่คุณสร้างขึ้น ตัวอย่างเช่น วัสดุ</span><span class="sxs-lookup"><span data-stu-id="f70d0-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="f70d0-119">คลิก **สร้างรายการ**</span><span class="sxs-lookup"><span data-stu-id="f70d0-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="f70d0-120">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f70d0-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="f70d0-121">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f70d0-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="f70d0-122">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f70d0-122">Click **OK**.</span></span> <span data-ttu-id="f70d0-123">การดำเนินการนี้จะสร้างรายการสำหรับมิติที่มีธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f70d0-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="f70d0-124">คำนวณข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="f70d0-124">Calculate proposal</span></span>
1. <span data-ttu-id="f70d0-125">คลิก **คำนวณข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="f70d0-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="f70d0-126">เลือกตัวเลือก **ใช้การออกใช้โดยเฉลี่ยในระหว่างระยะเวลารอคอยสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f70d0-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="f70d0-127">ตั้งค่า **ตัวคูณ** เป็น '10'</span><span class="sxs-lookup"><span data-stu-id="f70d0-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="f70d0-128">ตัวคูณจะใช้ในการปรับปรุงในข้อเสนอ </span><span class="sxs-lookup"><span data-stu-id="f70d0-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="f70d0-129">เนื่องจากข้อมูลสาธิตมีธุรกรรมเพียงสองสามรายการเท่านั้น คุณจะต้องตั้งค่าตัวคูณเพื่อรับข้อเสนอที่เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="f70d0-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="f70d0-130">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f70d0-130">Click **OK**.</span></span> <span data-ttu-id="f70d0-131">เลื่อนลงเพื่อค้นหา M0002 และ M0003 </span><span class="sxs-lookup"><span data-stu-id="f70d0-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="f70d0-132">ดูคอลัมน์ปริมาณ **ต่ำสุดที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="f70d0-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="f70d0-133">อัพเดตปริมาณต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="f70d0-133">Update minimum quantity</span></span>
1. <span data-ttu-id="f70d0-134">ในฟิลด์ **ปริมาณต่ำสุดใหม่** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f70d0-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="f70d0-135">อัพเดตปริมาณต่ำสุดใหม่เพื่อให้ตรงกับค่าในปริมาณต่ำสุดที่คำนวณได้ </span><span class="sxs-lookup"><span data-stu-id="f70d0-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="f70d0-136">ถ้าปริมาณต่ำสุดที่คำนวณได้เป็นศูนย์ คุณสามารถป้อนค่าในอนาคตที่ต้องการ </span><span class="sxs-lookup"><span data-stu-id="f70d0-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="f70d0-137">ตัวอย่างเช่น คุณสามารถป้อนปริมาณต่ำสุดที่คำนวณได้ในฟิลด์นี้เป็น M0002 ที่มีคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="f70d0-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="f70d0-138">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f70d0-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="f70d0-139">ตัวอย่างเช่น คุณสามารถเลือก M0002 ที่มีคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="f70d0-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="f70d0-140">ในฟิลด์ **ปริมาณต่ำสุดใหม่** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f70d0-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="f70d0-141">อัพเดตปริมาณต่ำสุดใหม่เพื่อให้ตรงกับค่าในปริมาณต่ำสุดที่คำนวณได้ </span><span class="sxs-lookup"><span data-stu-id="f70d0-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="f70d0-142">ถ้าปริมาณต่ำสุดที่คำนวณได้เป็นศูนย์ คุณสามารถป้อนค่าในอนาคตที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f70d0-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="f70d0-143">ลงรายการบัญชีปริมาณต่ำสุดใหม่ และตรวจสอบผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f70d0-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="f70d0-144">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="f70d0-144">Click **Post**.</span></span>
2. <span data-ttu-id="f70d0-145">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f70d0-145">Click **OK**.</span></span>
3. <span data-ttu-id="f70d0-146">คลิกเพื่อติดตามลิงค์ในฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f70d0-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="f70d0-147">คลิกเพื่อติดตามลิงค์ในฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f70d0-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="f70d0-148">ใน **บานหน้าต่างการดำเนินการ** คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="f70d0-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="f70d0-149">คลิก **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="f70d0-149">Click **Item coverage**.</span></span> <span data-ttu-id="f70d0-150">โปรดสังเกตว่า **ปริมาณต่ำสุด** ได้รับการปรับปรุงด้วยปริมาณต่ำสุดใหม่จากสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="f70d0-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

