---
title: ใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยเพื่ออัพเดตความครอบคลุมขั้นต่ำ
description: 'ขั้นตอนนี้แสดงวิธีการคำนวณข้อเสนอความครอบคลุมขั้นต่ำที่ขึ้นอยู่กับธุรกรรมที่ผ่านมา จากนั้นอัพเดตความครอบคลุมสินค้าที่มีข้อเสนอ '
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "341108"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="280bc-103">ใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยเพื่ออัพเดตความครอบคลุมขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="280bc-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="280bc-104">ขั้นตอนนี้แสดงวิธีการคำนวณข้อเสนอความครอบคลุมขั้นต่ำที่ขึ้นอยู่กับธุรกรรมที่ผ่านมา จากนั้นอัพเดตความครอบคลุมสินค้าที่มีข้อเสนอ </span><span class="sxs-lookup"><span data-stu-id="280bc-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="280bc-105">ซึ่งทำได้โดยใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย </span><span class="sxs-lookup"><span data-stu-id="280bc-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="280bc-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="280bc-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="280bc-107">งานนี้มีไว้สำหรับนักวางแผนการผลิตเพื่อช่วยรักษาความครอบคลุมขั้นต่ำ</span><span class="sxs-lookup"><span data-stu-id="280bc-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="280bc-108">สร้างชื่อสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยใหม่</span><span class="sxs-lookup"><span data-stu-id="280bc-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="280bc-109">ไปที่ ชื่อสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="280bc-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="280bc-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="280bc-110">Click New.</span></span>
3. <span data-ttu-id="280bc-111">ในฟิลด์ชือ พิมพ์ 'วัสดุ'</span><span class="sxs-lookup"><span data-stu-id="280bc-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="280bc-112">ในฟิลด์ คำอธิบาย พิมพ์ 'วัสดุ'</span><span class="sxs-lookup"><span data-stu-id="280bc-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="280bc-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="280bc-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="280bc-114">สร้างสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="280bc-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="280bc-115">ไปที่ การคำนวณปริมาณสินค้าคงคลังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="280bc-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="280bc-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="280bc-116">Click New.</span></span>
3. <span data-ttu-id="280bc-117">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="280bc-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="280bc-118">เลือกชื่อสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยที่คุณสร้างขึ้น ตัวอย่างเช่น วัสดุ</span><span class="sxs-lookup"><span data-stu-id="280bc-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="280bc-119">คลิกสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="280bc-119">Click Create lines.</span></span>
5. <span data-ttu-id="280bc-120">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="280bc-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="280bc-121">กำหนดวันที่เป็น '2015-01-02'</span><span class="sxs-lookup"><span data-stu-id="280bc-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="280bc-122">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="280bc-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="280bc-123">กำหนดวันที่เป็น '2015-12-30'</span><span class="sxs-lookup"><span data-stu-id="280bc-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="280bc-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="280bc-124">Click OK.</span></span>
    * <span data-ttu-id="280bc-125">การดำเนินการนี้จะสร้างรายการสำหรับมิติที่มีธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="280bc-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="280bc-126">คำนวณข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="280bc-126">Calculate proposal</span></span>
1. <span data-ttu-id="280bc-127">คลิก คำนวณข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="280bc-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="280bc-128">เลือกตัวเลือก ใช้การออกใช้โดยเฉลี่ยในระหว่างระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="280bc-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="280bc-129">ตั้งค่าตัวคูณเป็น '10'</span><span class="sxs-lookup"><span data-stu-id="280bc-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="280bc-130">ตัวคูณจะใช้ในการปรับปรุงในข้อเสนอ </span><span class="sxs-lookup"><span data-stu-id="280bc-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="280bc-131">เนื่องจากข้อมูลสาธิตมีธุรกรรมเพียงสองสามรายการเท่านั้น คุณจะต้องตั้งค่าตัวคูณเพื่อรับข้อเสนอที่เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="280bc-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="280bc-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="280bc-132">Click OK.</span></span>
    * <span data-ttu-id="280bc-133">เลื่อนลงเพื่อค้นหา M0002 และ M0003 </span><span class="sxs-lookup"><span data-stu-id="280bc-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="280bc-134">ดูคอลัมน์ปริมาณต่ำสุดที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="280bc-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="280bc-135">อัพเดตปริมาณต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="280bc-135">Update minimum quantity</span></span>
1. <span data-ttu-id="280bc-136">ในฟิลด์ปริมาณต่ำสุดใหม่ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="280bc-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="280bc-137">อัพเดตปริมาณต่ำสุดใหม่เพื่อให้ตรงกับค่าในปริมาณต่ำสุดที่คำนวณได้ </span><span class="sxs-lookup"><span data-stu-id="280bc-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="280bc-138">ถ้าปริมาณต่ำสุดที่คำนวณได้เป็นศูนย์ คุณสามารถป้อนค่าในอนาคตที่ต้องการ </span><span class="sxs-lookup"><span data-stu-id="280bc-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="280bc-139">ตัวอย่างเช่น คุณสามารถป้อนปริมาณต่ำสุดที่คำนวณได้ในฟิลด์นี้เป็น M0002 ที่มีคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="280bc-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="280bc-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="280bc-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="280bc-141">ตัวอย่างเช่น คุณสามารถเลือก M0002 ที่มีคลังสินค้า 12</span><span class="sxs-lookup"><span data-stu-id="280bc-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="280bc-142">ในฟิลด์ปริมาณต่ำสุดใหม่ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="280bc-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="280bc-143">อัพเดตปริมาณต่ำสุดใหม่เพื่อให้ตรงกับค่าในปริมาณต่ำสุดที่คำนวณได้ </span><span class="sxs-lookup"><span data-stu-id="280bc-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="280bc-144">ถ้าปริมาณต่ำสุดที่คำนวณได้เป็นศูนย์ คุณสามารถป้อนค่าในอนาคตที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="280bc-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="280bc-145">ลงรายการบัญชีปริมาณต่ำสุดใหม่ และตรวจสอบผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="280bc-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="280bc-146">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="280bc-146">Click Post.</span></span>
2. <span data-ttu-id="280bc-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="280bc-147">Click OK.</span></span>
3. <span data-ttu-id="280bc-148">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="280bc-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="280bc-149">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="280bc-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="280bc-150">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="280bc-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="280bc-151">คลิกความครอบคลุมสินค้า</span><span class="sxs-lookup"><span data-stu-id="280bc-151">Click Item coverage.</span></span>
    * <span data-ttu-id="280bc-152">โปรดสังเกตว่าปริมาณต่ำสุดได้รับการอัพเดตเป็นปริมาณต่ำสุดใหม่จากสมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="280bc-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

