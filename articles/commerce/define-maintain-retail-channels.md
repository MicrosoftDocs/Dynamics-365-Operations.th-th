---
title: การกำหนดและรักษาช่องทางการขายปลีก
description: หัวข้อนี้ให้ภาพรวมของกระบวนการสำหรับการตั้งร้านค้าแบบดั้งเดิม ซึ่งเรียกว่าร้านค้าใน Dynamics 365 Commerce รวมไปถึงข้อมูลเกี่ยวกับงานที่คุณต้องทำให้สมบูรณ์ก่อนและหลังการตั้งร้านค้า
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057925"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="fd02a-104">กำหนดและรักษาช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="fd02a-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd02a-105">หัวข้อนี้ให้ภาพรวมของกระบวนการสำหรับการตั้งร้านค้าแบบดั้งเดิม ซึ่งเรียกว่าร้านค้าใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fd02a-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="fd02a-106">รวมไปถึงข้อมูลเกี่ยวกับงานที่คุณต้องทำให้สมบูรณ์ก่อนและหลังการตั้งร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="fd02a-107">การรองรับการค้าหลายช่องทาง เช่น ร้านค้าออนไลน์ ศูนย์บริการ และร้านค้าแบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="fd02a-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="fd02a-108">เรียกร้านค้าแบบดั้งเดิมว่าร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="fd02a-109">ร้านค้าแต่ละร้านสามารถมีวิธีการชำระเงินของตัวเอง กลุ่มราคา การลงทะเบียนรวมระบบขายหน้าร้าน (POS) บัญชีรายได้และบัญชีรายจ่าย และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="fd02a-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="fd02a-110">คุณต้องตั้งค่าองค์ประกอบเหล่านี้สำหรับร้านค้าทั้งหมดก่อนคุณจึงจะสามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="fd02a-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="fd02a-111">หลังจากที่คุณสร้างร้านค้าแล้ว คุณมอบหมายผลิตภัณฑ์ที่คุณต้องการให้มีอยู่</span><span class="sxs-lookup"><span data-stu-id="fd02a-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="fd02a-112">คุณยังต้องกำหนดพนักงาน เครื่องบันทึกเงินสด และลูกค้าไปยังร้าน</span><span class="sxs-lookup"><span data-stu-id="fd02a-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="fd02a-113">ในตอนท้าย คุณจะเพิ่มร้านค้าใหม่ไปยังลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="fd02a-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="fd02a-114">ตั้งค่าร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-114">Setting up stores</span></span>

<span data-ttu-id="fd02a-115">ก่อนที่คุณจะสามารถตั้งค่าร้านค้าในคอมเมิร์ซ คุณต้องทำงานเบื้องต้นที่ต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fd02a-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="fd02a-116">จากนั้นคุณสามารถสร้างร้านค้าและเพิ่มรายละเอียดได้</span><span class="sxs-lookup"><span data-stu-id="fd02a-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fd02a-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="fd02a-117">Prerequisites</span></span>

<span data-ttu-id="fd02a-118">คุณต้องทำสิ่งเหล่านี้ให้เสร็จสมบูรณ์ก่อนตั้งค่าร้านค้า:</span><span class="sxs-lookup"><span data-stu-id="fd02a-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="fd02a-119">ตั้งค่าคอนฟิกโครงสร้างองค์กรของคุณ และตั้งค่าลำดับชั้นขององค์กรสำหรับการจัดประเภทการขายปลีก การเติมสินค้า และการรายงาน</span><span class="sxs-lookup"><span data-stu-id="fd02a-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="fd02a-120">ตั้งค่าคลังสินค้าที่แสดงถึงร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="fd02a-121">ตั้งค่าหมายเลขลำดับสำหรับร้านค้า คำชี้แจงร้านค้า และคำชี้แจงใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="fd02a-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="fd02a-122">กำหนดค่าพารามิเตอร์เพื่อการพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="fd02a-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="fd02a-123">ตั้งค่าวิธีการชำระเงินที่ร้านค้ายอมรับ</span><span class="sxs-lookup"><span data-stu-id="fd02a-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="fd02a-124">เมื่อต้องการประมวลผลธุรกรรมบัตรเครดิตที่เครื่องบันทึกเงินสด POS คุณยังสามารถตั้งค่าการบริการชำระเงินได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="fd02a-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="fd02a-125">ตั้งค่ากลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="fd02a-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="fd02a-126">ตั้งค่าผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fd02a-126">Set up products.</span></span> <span data-ttu-id="fd02a-127">ในฐานะที่เป็นส่วนหนึ่งของงานนี้ คุณยังตั้งค่าลำดับชั้นของผลิตภัณฑ์ ตัวแปรผลิตภัณฑ์ และการจัดประเภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fd02a-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="fd02a-128">ตั้งค่ากลุ่มราคาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fd02a-128">Set up product price groups.</span></span>
10. <span data-ttu-id="fd02a-129">ตั้งค่าราคาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fd02a-129">Set up product pricing.</span></span> <span data-ttu-id="fd02a-130">เนื่องจากเป็นส่วนหนึ่งของงานนี้ คุณยังตั้งค่าการปรับปรุงราคา ส่วนลด และรอบระยะเวลาส่วนลดได้</span><span class="sxs-lookup"><span data-stu-id="fd02a-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="fd02a-131">ตั้งค่าพนักงาน</span><span class="sxs-lookup"><span data-stu-id="fd02a-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd02a-132">คุณต้องมอบหมายสิทธิ์ที่เหมาะสมให้กับพนักงาน เพื่อให้พวกเขาสามารถลงชื่อเข้าใช้และทำงานโดยใช้ระบบ POS ได้</span><span class="sxs-lookup"><span data-stu-id="fd02a-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="fd02a-133">กำหนดค่าโปรไฟล์ POS เพื่อมอบหมายให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="fd02a-134">งานนี้รวมหลายงานอื่น เช่น การตั้งค่าเครื่องบันทึกเงินสด การตั้งค่าโพรไฟล์ออฟไลน์ และการตั้งค่ารูปแบบใบเสร็จและโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="fd02a-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="fd02a-135">ตรวจสอบงานทั้งหมดที่รวมอยู่ในข้อกำหนดเบื้องต้น และทำงานที่เกี่ยวข้องเฉพาะกับคุณให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="fd02a-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="fd02a-136">ตั้งค่าร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-136">Set up a store</span></span>

<span data-ttu-id="fd02a-137">หลังจากที่คุณทำข้อกำหนดเบื้องต้นเสร็จสิ้นแล้ว คุณต้องทำงานเหล่านี้ให้เสร็จสมบูรณ์เพื่อตั้งค่ารายละเอียดสำหรับร้านค้า:</span><span class="sxs-lookup"><span data-stu-id="fd02a-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="fd02a-138">สร้างร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-138">Create a store.</span></span>
2. <span data-ttu-id="fd02a-139">กำหนดกลุ่มภาษีขายให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="fd02a-140">กำหนดวิธีการชำระเงินที่ยอมรับให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="fd02a-141">เพิ่มรายละเอียดลงในคำอธิบายผลิตภัณฑ์สำหรับผลิตภัณฑ์ที่คุณเสนอในร้านค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="fd02a-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="fd02a-142">ตัวอย่างเช่น คุณสามารถเพิ่มรูปแบบ rich text และรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="fd02a-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="fd02a-143">รายละเอียดผลิตภัณฑ์เหล่านี้จะปรากฏขึ้นในบริบทต่าง ๆ เช่น บนเครื่องบันทึกเงินสด POS หรือป้ายชื่อที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="fd02a-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="fd02a-144">เพิ่มร้านค้าไปยังลำดับชั้นขององค์กรค่าเริ่มต้น ที่ถูกมอบหมายไปยังวัตถุประสงค์ของ **การจัดประเภทการขายปลีก** **การเติมสินค้าขายปลีก** หรือ **รายงานการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="fd02a-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="fd02a-145">หลังจากที่คุณตั้งค่าร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-145">After you set up a store</span></span>

<span data-ttu-id="fd02a-146">หลังจากคุณป้อนรายละเอียดสำหรับร้านค้า ให้ทำงานเหล่านี้ให้เสร็จสมบูรณ์เพื่อส่งข้อมูลร้านค้าใหม่ไปยัง POS:</span><span class="sxs-lookup"><span data-stu-id="fd02a-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="fd02a-147">ตั้งค่าคอนฟิกเครื่องบันทึกเงินสดการขายหน้าร้าน (POS) สำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="fd02a-148">กำหนดการจัดประเภทผลิตภัณฑ์ให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="fd02a-149">การจัดประเภทกระบวนการเพื่อสร้างรายการผลิตภัณฑ์ที่รวมอยู่ในการจัดประเภทและเพื่อให้ผลิตภัณฑ์มีอยู่ในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fd02a-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="fd02a-150">ส่งข้อมูล เช่น ลำดับหมายเลข โปรไฟล์ฮาร์ดแวร์ และเค้าโครงหน้าจอ POS ไปยังการลงทะเบียน POS</span><span class="sxs-lookup"><span data-stu-id="fd02a-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="fd02a-151">เผยแพร่ร้านค้าเพื่อส่งข้อมูลร้านค้าไปยัง POS</span><span class="sxs-lookup"><span data-stu-id="fd02a-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="fd02a-152">รันงานเพื่อส่งข้อมูลร้านค้าไปยัง POS</span><span class="sxs-lookup"><span data-stu-id="fd02a-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="fd02a-153">ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="fd02a-153">Organization hierarchies</span></span>

<span data-ttu-id="fd02a-154">การค้าใช้ลำดับชั้นขององค์กรเพื่อจัดโครงสร้างช่องทาง</span><span class="sxs-lookup"><span data-stu-id="fd02a-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="fd02a-155">ลำดับชั้นขององค์กรแสดงความสัมพันธ์ระหว่างองค์กรที่สร้างธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="fd02a-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="fd02a-156">เมื่อคุณตั้งค่าร้านค้า คุณสามารถเพิ่มร้านเหล่านั้นเข้าไปในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="fd02a-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="fd02a-157">ร้านค้าจะแบ่งปันข้อมูลที่ใช้สำหรับการจัดประเภท การเพิ่มเติมสินค้า และการรายงาน</span><span class="sxs-lookup"><span data-stu-id="fd02a-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="fd02a-158">หากต้องการใช้ฟังก์ชันการขาย Commerce ต้องเปิดใช้งานคีย์การตั้งค่าคอนฟิกสำหรับ **ที่อยู่ที่จัดส่งหลายแห่ง**</span><span class="sxs-lookup"><span data-stu-id="fd02a-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="fd02a-159">คีย์การตั้งค่าคอนฟิกนี้สามารถพบได้ในคีย์ **การตั้งค่าคอนฟิกการค้า** ใต้ **การตั้งค่าการดูแลระบบ**\> **ตั้งค่า**\> **การตั้งค่าคอนฟิกลิขสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="fd02a-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="fd02a-160">นี่มีความจำเป็น เนื่องจากการตรวจสอบความถูกต้องต่างๆ ตามที่อยู่ที่จัดส่งที่ตั้งค่าคอนฟิกไว้ที่ระดับรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="fd02a-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

