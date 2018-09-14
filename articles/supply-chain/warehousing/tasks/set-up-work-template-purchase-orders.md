--- 
title: "ตั้งค่าเท็มเพลตงานสำหรับใบสั่งซื้อ"
description: "ขั้นตอนนี้มุ่งเน้นไปที่การตั้งค่าของเท็มเพลตงานอย่างง่ายที่จะใช้เมื่อย้ายสินค้าที่ได้รับออกไป "
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="ef742-103">ตั้งค่าเท็มเพลตงานสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="ef742-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef742-104">ขั้นตอนนี้มุ่งเน้นไปที่การตั้งค่าของเท็มเพลตงานอย่างง่ายที่จะใช้เมื่อย้ายสินค้าที่ได้รับออกไป </span><span class="sxs-lookup"><span data-stu-id="ef742-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="ef742-105">เท็มเพลตงานกำหนดชุดของคำแนะนำที่นำเสนอต่อผู้ปฏิบัติงานคลังสินค้าบนอุปกรณ์เคลื่อนที่เมื่อเคลื่อนย้ายสินค้าจากพื้นที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="ef742-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="ef742-106">คุณสามารถใช้กระบวนงานนี้กับข้อมูลที่กล่าวถึงในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="ef742-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="ef742-107">ก่อนที่คุณจะเริ่มคำแนะนำนี้ ให้สร้างรหัสกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="ef742-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="ef742-108">ในตัวอย่างนี้ ใช้รายการที่เรียกว่ารหัสกลุ่มงานในขาเข้า</span><span class="sxs-lookup"><span data-stu-id="ef742-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="ef742-109">ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ef742-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="ef742-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="ef742-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="ef742-111">ในฟิลด์ชนิดใบสั่งงาน เลือก 'ใบสั่งซื้อ' </span><span class="sxs-lookup"><span data-stu-id="ef742-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="ef742-112">สร้างหัวข้อเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="ef742-112">Create a work template header</span></span>
1. <span data-ttu-id="ef742-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ef742-113">Click New.</span></span>
2. <span data-ttu-id="ef742-114">ในฟิลด์หมายเลขลำดับ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ef742-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="ef742-115">นี่เป็นลำดับที่เท็มเพลตงานจะถูกประเมิน </span><span class="sxs-lookup"><span data-stu-id="ef742-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="ef742-116">คุณสามารถแก้ไขลำดับได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ef742-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="ef742-117">ในฟิลด์เท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ef742-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="ef742-118">นี่คือตัวระบุเฉพาะสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="ef742-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="ef742-119">ในฟิลด์คำอธิบายเท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ef742-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="ef742-120">ตัวเลือกที่ถูกต้องจะไม่มีการตรวจสอบจนกว่าคุณจะกรอกข้อมูลทั้งหมดที่จำเป็นโดยใช้เท็มเพลตและคลิกบันทึกแล้ว</span><span class="sxs-lookup"><span data-stu-id="ef742-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="ef742-121">ใบสั่งงานของประเภทใบสั่งซื้อไม่สามารถประมวลผลโดยอัตโนมัติ ดั้งนั้นเพื่อออกจากประมวลผลโดยอัตโนมัติตั้งค่าตัวเลือกเป็น ไม่</span><span class="sxs-lookup"><span data-stu-id="ef742-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="ef742-122">ในฟิลด์รหัสกลุ่มงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ef742-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="ef742-123">รหัสกลุ่มงานช่วยให้คุณจัดระเบียบงานในกลุ่ม </span><span class="sxs-lookup"><span data-stu-id="ef742-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="ef742-124">ค่าที่คุณตั้งไว้ที่นี่จะเป็นค่าเริ่มต้นสำหรับงานใดๆ ที่ถูกสร้างขึ้นโดยใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="ef742-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="ef742-125">ในฟิลด์ระดับความสำคัญของงาน ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="ef742-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="ef742-126">นี่แสดงให้เห็นความสำคัญของงาน และค่าที่คุณตั้งไว้ที่นี่จะเป็นค่าเริ่มต้นสำหรับงานใดๆ ที่ถูกสร้างขึ้นโดยใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="ef742-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="ef742-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ef742-127">Click Save.</span></span>
    * <span data-ttu-id="ef742-128">คุณต้องบันทึกหัวข้อเท็มเพลตงานก่อนปุ่มแก้ไขแบบสอบถามจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ef742-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="ef742-129">ติดตั้งการสอบถามสำหรับเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="ef742-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="ef742-130">(คลิกแก้ไขการสอบถาม)</span><span class="sxs-lookup"><span data-stu-id="ef742-130">Click Edit query.</span></span>
    * <span data-ttu-id="ef742-131">เราจะตั้งข้อจำกัดว่าเท็มเพลตสามารถนำมาใช้เฉพาะภายในคลังสินค้าเฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ef742-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="ef742-132">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="ef742-132">Click Add.</span></span>
3. <span data-ttu-id="ef742-133">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ef742-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ef742-134">ในฟิลด์ฟิลด์ ให้พิมพ์ 'คลังสินค้า'</span><span class="sxs-lookup"><span data-stu-id="ef742-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="ef742-135">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="ef742-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="ef742-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ef742-136">Click OK.</span></span>
7. <span data-ttu-id="ef742-137">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="ef742-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="ef742-138">ตั้งค่ารายละเอียดเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="ef742-138">Set work template details</span></span>
1. <span data-ttu-id="ef742-139">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ef742-139">Click New.</span></span>
2. <span data-ttu-id="ef742-140">ในฟิลด์ประเภทงาน ให้เลือก 'เบิกสินค้า'</span><span class="sxs-lookup"><span data-stu-id="ef742-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="ef742-141">ในฟิลด์รหัสคลาสงาน ให้พิมพ์ 'การซื้อ'</span><span class="sxs-lookup"><span data-stu-id="ef742-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="ef742-142">คลาสงานที่คุณตั้งค่าไว้ที่นี่จะเป็นค่าเริ่มต้นในรายงานทั้งหมดของประเภทการเบิกสินค้าที่ถูกสร้างขึ้นโดยใช้เท็มเพลตนี้ </span><span class="sxs-lookup"><span data-stu-id="ef742-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="ef742-143">คลาสงานไม่สามารถแทนที่จากรายการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="ef742-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="ef742-144">คลาสงานถูกจะใช้โดยตรง และ/หรือจำกัดประเภทของรายการใบสั่งงานที่ผู้ปฏิบัติงานคลังสินค้าสามารถประมวลผลบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="ef742-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="ef742-145">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ef742-145">Click New.</span></span>
5. <span data-ttu-id="ef742-146">ในฟิลด์ประเภทงาน ให้เลือก 'ส่งสินค้า'</span><span class="sxs-lookup"><span data-stu-id="ef742-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="ef742-147">ในฟิลด์รหัสคลาสงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ef742-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="ef742-148">คำแนะนำเบิกสินค้าและจัดส่งเป็นชุด </span><span class="sxs-lookup"><span data-stu-id="ef742-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="ef742-149">โดยแต่ละชุดของการเบิกสินค้า/การจัดส่งจะต้องมีคลาสงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ef742-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="ef742-150">ใช้คลาสงานเดียวกันที่คุณระบุสำหรับคำแนะนำการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="ef742-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="ef742-151">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ef742-151">Click Save.</span></span>
    * <span data-ttu-id="ef742-152">โปรดทราบว่าได้เลือกกล่องกาเครื่องหมายที่ถูกต้องแล้ว</span><span class="sxs-lookup"><span data-stu-id="ef742-152">Note that the Valid checkbox is now checked.</span></span>  


