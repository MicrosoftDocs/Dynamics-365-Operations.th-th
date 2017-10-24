---
title: "การกำหนดและรักษาช่องทางการขายปลีก"
description: "บทความนี้แสดงภาพรวมของกระบวนการสำหรับการตั้งค่าร้านค้าที่ให้บริการจริง ซึ่งจะเรียกว่าร้านค้าปลีกใน Microsoft Dynamics 365 for Retail โดยจะมีข้อมูลเกี่ยวกับภารกิจที่คุณต้องกรอกทั้งหมดก่อน และหลังจากที่คุณตั้งค่าร้านค้าปลีก"
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 700b8868a68be7f0172202d737b4f1ae9813ecf3
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="5972e-104">การกำหนดและรักษาช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-104">Define and maintain retail channels</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5972e-105">บทความนี้แสดงภาพรวมของกระบวนการสำหรับการตั้งค่าร้านค้าที่ให้บริการจริง ซึ่งจะเรียกว่าร้านค้าปลีกใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="5972e-105">This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="5972e-106">โดยจะมีข้อมูลเกี่ยวกับภารกิจที่คุณต้องกรอกทั้งหมดก่อน และหลังจากที่คุณตั้งค่าร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="5972e-107">Retail สนับสนุนช่องทางขายปลีกหลายช่องทาง เช่น ร้านค้าออนไลน์ ศูนย์บริการ และร้านค้าจริง</span><span class="sxs-lookup"><span data-stu-id="5972e-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="5972e-108">ร้านค้าจริงจะเรียกว่าเป็น ร้านค้าปลีก </span><span class="sxs-lookup"><span data-stu-id="5972e-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="5972e-109">ร้านค้าปลีกแต่ละรายการสามารถมีวิธีการชำระเงินของตนเอง กลุ่มราคา เครื่องบันทึกเงินสดการขายหน้าร้าน (POS) บัญชีกำไรขาดทุนและบัญชีค่าใช้จ่าย และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5972e-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="5972e-110">คุณต้องตั้งค่าองค์ประกอบเหล่านี้สำหรับร้านค้าปลีกก่อนที่คุณจะสร้างร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5972e-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="5972e-111">หลังจากที่คุณสร้างร้านค้าปลีกแล้ว กำหนดผลิตภัณฑ์ที่คุณต้องการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="5972e-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="5972e-112">คุณยังต้องกำหนดพนักงาน เครื่องบันทึกเงินสด และลูกค้าไปยังร้าน</span><span class="sxs-lookup"><span data-stu-id="5972e-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="5972e-113">ในตอนท้าย คุณจะเพิ่มร้านค้าใหม่ไปยังลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="5972e-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="5972e-114">การตั้งค่าร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-114">Setting up retail stores</span></span>
<span data-ttu-id="5972e-115">ก่อนที่คุณสามารถตั้งค่าร้านค้าปลีกใน Dynamics 365 for Retail คุณต้องกระทำตามข้อกำหนดเบื้องต้นบางข้อเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="5972e-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="5972e-116">จากนั้น คุณสามารถสร้างร้านค้าปลีก และเพิ่มรายละเอียดได้</span><span class="sxs-lookup"><span data-stu-id="5972e-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5972e-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="5972e-117">Prerequisites</span></span>

<span data-ttu-id="5972e-118">คุณต้องดำเนินขั้นตอนต่อไปนี้ก่อนที่คุณจะสามารถตั้งงร้านค้าปลีกได้:</span><span class="sxs-lookup"><span data-stu-id="5972e-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="5972e-119">ตั้งค่าคอนฟิกโครงสร้างองค์กรของคุณ และตั้งค่าลำดับชั้นขององค์กรสำหรับการจัดประเภทการขายปลีก การเติมสินค้า และการรายงาน</span><span class="sxs-lookup"><span data-stu-id="5972e-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="5972e-120">ตั้งค่าคลังสินค้าที่แสดงถึงร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="5972e-121">ตั้งค่าลำดับหมายเลขสำหรับร้านค้าปลีก ใบแจ้งยอดของร้านค้า และใบสำคัญการแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="5972e-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="5972e-122">ตั้งค่าคอนฟิกพารามิเตอร์สำหรับร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="5972e-123">ตั้งค่าวิธีการชำระเงินที่ร้านค้ายอมรับ</span><span class="sxs-lookup"><span data-stu-id="5972e-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="5972e-124">เมื่อต้องการประมวลผลธุรกรรมบัตรเครดิตที่เครื่องบันทึกเงินสดการขายหน้าร้าน (POS) คุณสามารถตั้งค่าการบริการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="5972e-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="5972e-125">ตั้งค่ากลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="5972e-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="5972e-126">ตั้งค่าผลิตภัณฑ์ขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-126">Set up retail products.</span></span> <span data-ttu-id="5972e-127">เนื่องจากเป็นส่วนหนึ่งของงานนี้ คุณยังตั้งค่าลำดับชั้นของผลิตภัณฑ์ขายปลีก ผลิตภัณฑ์ย่อย และการจัดประเภทผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="5972e-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="5972e-128">ตั้งค่ากลุ่มราคาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5972e-128">Set up product price groups.</span></span>
10. <span data-ttu-id="5972e-129">ตั้งค่าการกำหนดราคาผลิตภัณฑ์ขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-129">Set up retail product pricing.</span></span> <span data-ttu-id="5972e-130">เนื่องจากเป็นส่วนหนึ่งของงานนี้ คุณยังตั้งค่าการปรับปรุงราคา ส่วนลด และรอบระยะเวลาส่วนลดได้</span><span class="sxs-lookup"><span data-stu-id="5972e-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="5972e-131">ตั้งค่าพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5972e-131">Set up staff members.</span></span> <span data-ttu-id="5972e-132">**หมายเหตุ:** คุณต้องกำหนดชนิดของสิทธิ์ที่เหมาะสมสำหรับผู้ปฏิบัติงาน เพื่อให้สามารถลงชื่อเข้าใช้และทำงาน โดยใช้ Dynamics 365 for Retail สำหรับระบบ Retail POS</span><span class="sxs-lookup"><span data-stu-id="5972e-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="5972e-133">ตั้งค่าคอนฟิกโพรไฟล์ Retail POS เพื่อกำหนดให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5972e-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="5972e-134">งานนี้รวมหลายงานอื่น เช่น การตั้งค่าเครื่องบันทึกเงินสด การตั้งค่าโพรไฟล์ออฟไลน์ และการตั้งค่ารูปแบบใบเสร็จและโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="5972e-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="5972e-135">ตรวจทานงานทั้งหมดที่รวมอยู่ในข้อกำหนดเบื้องต้น และทำงานเฉพาะที่เกี่ยวข้องกับคุณ</span><span class="sxs-lookup"><span data-stu-id="5972e-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="5972e-136">ตั้งค่าร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-136">Set up a retail store</span></span>

<span data-ttu-id="5972e-137">หลังจากที่คุณทำงานที่เป็นข้อกำหนดเบื้องต้นเสร็จสมบูรณ์แล้ว ให้ดำเนินงานเหล่านี้เพื่อตั้งค่ารายละเอียดสำหรับร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="5972e-138">สร้างร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-138">Create a retail store.</span></span>
2.  <span data-ttu-id="5972e-139">กำหนดกลุ่มภาษีขายให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5972e-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="5972e-140">กำหนดวิธีการชำระเงินที่ยอมรับให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5972e-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="5972e-141">เพิ่มรายละเอียดที่คำอธิบายผลิตภัณฑ์สำหรับผลิตภัณฑ์ที่คุณเสนอในร้านค้าปลีกของคุณ</span><span class="sxs-lookup"><span data-stu-id="5972e-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="5972e-142">ตัวอย่างเช่น คุณสามารถเพิ่มรูปแบบ rich text และรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="5972e-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="5972e-143">รายละเอียดผลิตภัณฑ์เหล่านี้จะปรากฏขึ้นในบริบทต่าง ๆ เช่น บนเครื่องบันทึกเงินสด POS หรือป้ายชื่อที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="5972e-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="5972e-144">เพิ่มร้านค้าไปยังลำดับชั้นเริ่มต้นขององค์กรที่กำหนดตถุประสงค์ของ **การจัดประเภทการขายปลีก** , **การเติมสินค้าขายปลีก** หรือ **รายงานการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="5972e-144">Add the store to an the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="5972e-145">หลังจากที่คุณตั้งค่าร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-145">After you set up a retail store</span></span>

<span data-ttu-id="5972e-146">หลังจากที่คุณป้อนรายละเอียดสำหรับร้านค้าปลีก ให้ดำเนินงานเหล่านี้เพื่อส่งข้อมูลร้านค้าปลีกใหม่ไปยัง Retail POS:</span><span class="sxs-lookup"><span data-stu-id="5972e-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="5972e-147">ตั้งค่าคอนฟิกเครื่องบันทึกเงินสดการขายหน้าร้าน (POS) สำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5972e-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="5972e-148">กำหนดการจัดประเภทผลิตภัณฑ์ให้กับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5972e-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="5972e-149">ประมวลผลการจัดประเภทเพื่อสร้างรายการผลิตภัณฑ์ที่รวมอยู่ในการจัดประเภท และทำให้ผลิตภัณฑ์พร้อมใช้งานในร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="5972e-150">ส่งข้อมูล เช่น ลำดับหมายเลข โพรไฟล์ฮาร์ดแวร์ และโครงร่างหน้าจอ POS ไปยังเครื่องบันทึกเงินสดสำหรับร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="5972e-151">เผยแพร่ร้านค้าปลีกเพื่อส่งข้อมูลร้านค้าไปยัง Retail POS</span><span class="sxs-lookup"><span data-stu-id="5972e-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="5972e-152">รันงานเพื่อส่งข้อมูลร้านค้าไปยัง Retail POS</span><span class="sxs-lookup"><span data-stu-id="5972e-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="5972e-153">ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="5972e-153">Organization hierarchies</span></span>
<span data-ttu-id="5972e-154">Retail จะใช้ลำดับชั้นขององค์กรเพื่อกำหนดโครงสร้างช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5972e-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="5972e-155">ลำดับชั้นขององค์กรแสดงความสัมพันธ์ระหว่างองค์กรที่สร้างธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="5972e-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="5972e-156">เมื่อคุณตั้งค่าร้านค้า คุณสามารถเพิ่มร้านเหล่านั้นเข้าไปในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="5972e-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="5972e-157">ร้านค้าจะแบ่งปันข้อมูลที่ใช้สำหรับการจัดประเภท การเพิ่มเติมสินค้า และการรายงาน</span><span class="sxs-lookup"><span data-stu-id="5972e-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




