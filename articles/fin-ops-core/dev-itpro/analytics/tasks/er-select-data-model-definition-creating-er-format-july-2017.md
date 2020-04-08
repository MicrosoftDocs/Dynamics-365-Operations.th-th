---
title: เลือกข้อกำหนดแบบจำลองข้อมูล เมื่อคุณสร้างรูปแบบ
description: เพื่อทำตามขั้นตอนเหล่านี้ในกระบวนงาน อันดับแรกคุณต้องทำกระบวนงาน สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่ของ ER ให้เสร็จเรียบร้อยก่อน
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 374c31b5ea9160fba773e82f658e8de05c67cab4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143257"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="64122-103">เลือกข้อกำหนดแบบจำลองข้อมูล เมื่อคุณสร้างรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="64122-103">Select data model definitions when you create formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64122-104">เพื่อทำตามขั้นตอนเหล่านี้ในกระบวนงาน อันดับแรกคุณต้องทำกระบวนงาน สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่ของ ER ให้เสร็จเรียบร้อยก่อน</span><span class="sxs-lookup"><span data-stu-id="64122-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="64122-105">กระบวนงานนี้แสดงวิธีที่สามารถเลือกรายการรากของแบบจำลองเป็นคำนิยามแบบจำลองข้อมูลสำหรับการแทรกการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีวัตถุประสงค์เพื่อสร้างเอกสารอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="64122-105">This procedure shows how a model's root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="64122-106">ในกระบวนงานนี้ คุณจะเพิ่มการตั้งค่าคอนฟิกรูปแบบ ER ใหม่สำหรับบริษัทตัวอย่าง Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="64122-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="64122-107">กระบวนงานนี้มีไว้สำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="64122-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="64122-108">ขั้นตอนสามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูลใด ๆ</span><span class="sxs-lookup"><span data-stu-id="64122-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="64122-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="64122-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="64122-110">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="64122-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="64122-111">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงาน สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่ ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="64122-111">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="64122-112">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="64122-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="64122-113">เพิ่มการตั้งค่าคอนฟิกแบบจำลองข้อมูลของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="64122-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="64122-114">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="64122-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="64122-115">เราเพิ่มการตั้งค่าคอนฟิกแบบจำลอง ER ใหม่ที่ประกอบด้วยแบบจำลองข้อมูลที่มีวัตถุประสงค์เพื่อใช้เป็นแหล่งข้อมูลสำหรับการสร้างรายงาน ER</span><span class="sxs-lookup"><span data-stu-id="64122-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="64122-116">ในฟิลด์ชื่อ พิมพ์ 'แบบจำลองการชำระเงิน (แบบสมมติ)'</span><span class="sxs-lookup"><span data-stu-id="64122-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="64122-117">รูปแบบการชำระเงิน (แบบสมมติ)</span><span class="sxs-lookup"><span data-stu-id="64122-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="64122-118">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="64122-118">Click Create configuration.</span></span>
4. <span data-ttu-id="64122-119">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="64122-119">Click Designer.</span></span>
    * <span data-ttu-id="64122-120">เปิดโปรแกรมออกแบบ ER เพื่อระบุโครงสร้างของแบบจำลองข้อมูลของการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="64122-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="64122-121">สมมติว่าเราออกแบบแบบจำลองข้อมูลสำหรับโดเมนธุรกิจการชำระเงินเพื่อสนับสนุนวิธีการชำระเงินสองแบบ – การโอนย้ายเครดิตและการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="64122-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="64122-122">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="64122-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="64122-123">ในฟิลด์ชื่อ ให้พิมพ์ 'การชำระเงิน – การโอนย้ายเครดิต'</span><span class="sxs-lookup"><span data-stu-id="64122-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="64122-124">การชำระเงิน – การโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="64122-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="64122-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="64122-125">Click Add.</span></span>
8. <span data-ttu-id="64122-126">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="64122-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="64122-127">ในฟิลด์สร้างโหนดใหม่เป็น ให้ป้อน 'รากแบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="64122-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="64122-128">ในฟิลด์ชื่อ ให้พิมพ์ 'การชำระเงิน – การหักบัญชีเงินฝากอัตโนมัติ'</span><span class="sxs-lookup"><span data-stu-id="64122-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="64122-129">การชำระเงิน – แบบหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="64122-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="64122-130">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="64122-130">Click Add.</span></span>
12. <span data-ttu-id="64122-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="64122-131">Click Save.</span></span>
13. <span data-ttu-id="64122-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="64122-132">Close the page.</span></span>
14. <span data-ttu-id="64122-133">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="64122-133">Click Change status.</span></span>
    * <span data-ttu-id="64122-134">ดำเนินการเวอร์ชันแบบร่างของแบบจำลองให้เสร็จสมบูรณ์เพื่อให้พร้อมใช้งานในรูปแบบและการแม็ปแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="64122-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="64122-135">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="64122-135">Click Complete.</span></span>
16. <span data-ttu-id="64122-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="64122-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="64122-137">เริ่มต้นการป้อนการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="64122-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="64122-138">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="64122-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="64122-139">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองการชำระเงินแบบจำลองข้อมูล (แบบสมมติ)'</span><span class="sxs-lookup"><span data-stu-id="64122-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="64122-140">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="64122-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="64122-141">หมายเหตุว่าในปัจจุบันทุกรายการรากของแบบจำลองข้อมูลที่เลือกพร้อมใช้งานแล้วสำหรับการเลือกเป็นคำนิยามแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="64122-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="64122-142">คุณสามารถดำเนินต่อเพื่อออกแบบรูปแบบของคุณโดยใช้รายการรากที่จำเป็นของแบบจำลองข้อมูลใด ๆ</span><span class="sxs-lookup"><span data-stu-id="64122-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="64122-143">การแม็ปแบบจำลองที่ขาดหายไปสำหรับรายการรากที่เลือกไม่ได้ทำให้คุณไม่สามารถดำเนินต่อ</span><span class="sxs-lookup"><span data-stu-id="64122-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="64122-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="64122-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="64122-145">เพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="64122-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="64122-146">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="64122-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="64122-147">ในฟิลด์ใหม่ ป้อน 'การแม็ปแบบจำลองตามแบบจำลองการชำระเงินแบบจำลองข้อมูล (แบบสมมติ)'</span><span class="sxs-lookup"><span data-stu-id="64122-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="64122-148">ในฟิลด์ชื่อ พิมพ์ 'การแม็ปแบบจำลองการชำระเงิน (แบบสมมติ)'</span><span class="sxs-lookup"><span data-stu-id="64122-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="64122-149">การแม็ปแบบจำลองการชำระเงิน (แบบสมมติ)</span><span class="sxs-lookup"><span data-stu-id="64122-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="64122-150">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="64122-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="64122-151">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="64122-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="64122-152">ออกแบบการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="64122-152">Design ER model mappings</span></span>
1. <span data-ttu-id="64122-153">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="64122-153">Click Designer.</span></span>
    * <span data-ttu-id="64122-154">ใช้โปรแกรมออกแบบ ER เพื่อระบุการแม็ปแบบจำลองสำหรับรายการรากที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="64122-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="64122-155">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="64122-155">Click Designer.</span></span>
    * <span data-ttu-id="64122-156">จำลองการตั้งค่าของการแม็ปแบบจำลองที่เลือกสำหรับรายการรากของแบบจำลองที่เลือก</span><span class="sxs-lookup"><span data-stu-id="64122-156">Simulate setting of selected model mapping for the selected model's root item.</span></span>  
3. <span data-ttu-id="64122-157">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\เรกคอร์ดตาราง'</span><span class="sxs-lookup"><span data-stu-id="64122-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="64122-158">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="64122-158">Click Add root.</span></span>
5. <span data-ttu-id="64122-159">ในฟิลด์ชื่อ ให้พิมพ์ 'บัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="64122-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="64122-160">ในฟิลด์ตาราง พิมพ์ 'LedgerJournalTrans'</span><span class="sxs-lookup"><span data-stu-id="64122-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="64122-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="64122-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="64122-162">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="64122-162">Click OK.</span></span>
8. <span data-ttu-id="64122-163">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="64122-163">Click Save.</span></span>
9. <span data-ttu-id="64122-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="64122-164">Close the page.</span></span>
10. <span data-ttu-id="64122-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="64122-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="64122-166">เริ่มต้นการป้อนการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่อื่น</span><span class="sxs-lookup"><span data-stu-id="64122-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="64122-167">ในแผนภูมิ ให้เลือก 'แบบจำลองการชำระเงิน (แบบสมมติ)'</span><span class="sxs-lookup"><span data-stu-id="64122-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="64122-168">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="64122-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="64122-169">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองการชำระเงินแบบจำลองข้อมูล (แบบสมมติ)'</span><span class="sxs-lookup"><span data-stu-id="64122-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="64122-170">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="64122-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="64122-171">หมายเหตุว่าในขณะนี้มีรายการรากเดียวเท่านั้นที่พร้อมใช้งานในการแม็ปกับแหล่งข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="64122-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="64122-172">เมื่อมีการนำการแม็ปแบบจำลองอย่างน้อยหนึ่งรายการมาใช้เป็นครั้งแรก คุณสามารถเลือกได้เฉพาะรายการรากของแบบจำลองที่ได้รับการแม็ปไปยังแหล่งข้อมูลแอพลิเคชันเป็นคำนิยามแบบจำลอง ในขณะที่มีการเพิ่มรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="64122-172">When at least one model mapping is introduced, only the model's root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="64122-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="64122-173">Close the page.</span></span>

