---
title: ตั้งค่าเท็มเพลตงานสำหรับใบสั่งซื้อ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าของเท็มเพลตงานอย่างง่ายที่จะใช้ เมื่อสำรองสินค้าที่ได้รับ
author: ShylaThompson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79c4e1810cf095a342a370018190fd0d587c15
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817304"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="fa184-103">ตั้งค่าเท็มเพลตงานสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fa184-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa184-104">หัวข้อนี้อธิบายวิธีการตั้งค่าของเท็มเพลตงานอย่างง่ายที่จะใช้ เมื่อสำรองสินค้าที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="fa184-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="fa184-105">เท็มเพลตงานกำหนดชุดของคำแนะนำที่นำเสนอต่อผู้ปฏิบัติงานคลังสินค้าบนอุปกรณ์เคลื่อนที่เมื่อเคลื่อนย้ายสินค้าจากพื้นที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fa184-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="fa184-106">คุณสามารถใช้กระบวนงานนี้กับข้อมูลที่กล่าวถึงในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="fa184-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="fa184-107">ก่อนที่คุณจะเริ่มคำแนะนำนี้ ให้สร้างรหัสกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="fa184-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="fa184-108">ในตัวอย่างนี้ ใช้รายการที่เรียกว่ารหัสกลุ่มงานในขาเข้า</span><span class="sxs-lookup"><span data-stu-id="fa184-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="fa184-109">ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fa184-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="fa184-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="fa184-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="fa184-111">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก **ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="fa184-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="fa184-112">สร้างหัวข้อเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="fa184-112">Create a work template header</span></span>
1. <span data-ttu-id="fa184-113">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="fa184-113">Select **New**.</span></span>
2. <span data-ttu-id="fa184-114">ในฟิลด์ **หมายเลขลำดับ** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="fa184-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="fa184-115">นี่เป็นลำดับที่เท็มเพลตงานจะถูกประเมิน </span><span class="sxs-lookup"><span data-stu-id="fa184-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="fa184-116">คุณสามารถแก้ไขลำดับได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="fa184-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="fa184-117">ในฟิลด์ **เท็มเพลตงาน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fa184-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="fa184-118">นี่คือตัวระบุเฉพาะสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fa184-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="fa184-119">ในฟิลด์ **คำอธิบายเท็มเพลตงาน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fa184-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="fa184-120">ตัวเลือก **มีผลบังคับใช้** จะไม่ถูกทำเครื่องหมาย จนกว่าคุณจะได้กรอกข้อมูลทั้งหมดที่จำเป็นโดยเท็มเพลตเสร็จสมบูรณ์ และจากนั้น เลือก **บันทึก** แล้ว</span><span class="sxs-lookup"><span data-stu-id="fa184-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="fa184-121">ใบสั่งงานของชนิด **ใบสั่งซื้อ** ไม่สามารถประมวลผลได้โดยอัตโนมัติ ดั้งนั้น ปล่อยให้ตัวเลือก **ประมวลผลโดยอัตโนมัติ** ถูกตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="fa184-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="fa184-122">ในฟิลด์ **รหัสกลุ่มงาน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fa184-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="fa184-123">รหัสกลุ่มงานช่วยให้คุณจัดระเบียบงานในกลุ่ม </span><span class="sxs-lookup"><span data-stu-id="fa184-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="fa184-124">ค่าที่คุณตั้งไว้ที่นี่จะเป็นค่าเริ่มต้นสำหรับงานใดๆ ที่ถูกสร้างขึ้นโดยใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="fa184-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="fa184-125">ในฟิลด์ **ระดับความสำคัญของงาน** ให้ป้อน `1`</span><span class="sxs-lookup"><span data-stu-id="fa184-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="fa184-126">นี่แสดงให้เห็นความสำคัญของงาน และค่าที่คุณตั้งไว้ที่นี่จะเป็นค่าเริ่มต้นสำหรับงานใดๆ ที่ถูกสร้างขึ้นโดยใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="fa184-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="fa184-127">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fa184-127">Select **Save**.</span></span> <span data-ttu-id="fa184-128">คุณต้องบันทึกส่วนหัวของเท็มเพลตงาน ก่อนปุ่ม **แก้ไขแบบสอบถาม** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fa184-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="fa184-129">ติดตั้งการสอบถามสำหรับเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="fa184-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="fa184-130">เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="fa184-130">Select **Edit query**.</span></span> <span data-ttu-id="fa184-131">เราจะตั้งข้อจำกัดว่าสามารถใช้เท็มเพลตได้เฉพาะภายในคลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="fa184-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="fa184-132">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="fa184-132">Select **Add**.</span></span>
3. <span data-ttu-id="fa184-133">ในฟิลด์ **ฟิลด์** ของแถวใหม่ ให้พิมพ์ `warehouse`</span><span class="sxs-lookup"><span data-stu-id="fa184-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="fa184-134">ในฟิลด์ **เงื่อนไข** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fa184-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="fa184-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fa184-135">Select **OK**.</span></span>
6. <span data-ttu-id="fa184-136">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="fa184-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="fa184-137">ตั้งค่ารายละเอียดเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="fa184-137">Set work template details</span></span>
1. <span data-ttu-id="fa184-138">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="fa184-138">Select **New**.</span></span>
2. <span data-ttu-id="fa184-139">ในฟิลด์ **ชนิดงาน** ให้เลือก **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="fa184-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="fa184-140">ในฟิลด์ **รหัสคลาสงาน** ให้พิมพ์ `purchase`</span><span class="sxs-lookup"><span data-stu-id="fa184-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="fa184-141">คลาสงานที่คุณตั้งค่าไว้ที่นี่จะเป็นค่าเริ่มต้นในรายงานทั้งหมดของประเภทการเบิกสินค้าที่ถูกสร้างขึ้นโดยใช้เท็มเพลตนี้ </span><span class="sxs-lookup"><span data-stu-id="fa184-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="fa184-142">คลาสงานไม่สามารถแทนที่จากรายการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="fa184-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="fa184-143">คลาสงานถูกจะใช้โดยตรง และ/หรือจำกัดประเภทของรายการใบสั่งงานที่ผู้ปฏิบัติงานคลังสินค้าสามารถประมวลผลบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="fa184-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="fa184-144">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="fa184-144">Select **New**.</span></span>
5. <span data-ttu-id="fa184-145">ในฟิลด์ **ประเภทงาน** ให้เลือก **ส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="fa184-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="fa184-146">ในฟิลด์ **รหัสคลาสงาน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fa184-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="fa184-147">คำแนะนำเบิกสินค้าและจัดส่งเป็นชุด </span><span class="sxs-lookup"><span data-stu-id="fa184-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="fa184-148">โดยแต่ละชุดของการเบิกสินค้า/การจัดส่งจะต้องมีคลาสงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="fa184-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="fa184-149">ใช้คลาสงานเดียวกันที่คุณระบุสำหรับคำแนะนำการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="fa184-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="fa184-150">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fa184-150">Select **Save**.</span></span> <span data-ttu-id="fa184-151">โปรดทราบว่า ขณะนี้มีการเลือกกล่องกาเครื่องหมาย **มีผลบังคับใช้** แล้ว</span><span class="sxs-lookup"><span data-stu-id="fa184-151">Note that the **Valid** checkbox is now checked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]