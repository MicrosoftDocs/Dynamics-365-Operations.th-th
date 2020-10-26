---
title: การตั้งค่าลายเซ็นอิเล็กทรอนิกส์
description: 'ใช้ขั้นตอนนี้เพื่อตั้งค่าลายเซ็นอิเล็กทรอนิกส์ '
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be8d2c95b95be621c81d41fd98e5857caa8bbbcb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981781"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="6296b-103">การตั้งค่าลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-103">Set up electronic signatures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6296b-104">ใช้ขั้นตอนนี้เพื่อตั้งค่าลายเซ็นอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="6296b-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="6296b-105">ลายเซ็นอิเล็กทรอนิกส์จะยืนยันลักษณะเฉพาะของบุคคลที่กำลังจะเริ่มหรืออนุมัติกระบวนการระบบคอมพิวเตอร์ </span><span class="sxs-lookup"><span data-stu-id="6296b-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="6296b-106">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างกระบวนงานนี้คือ DAT </span><span class="sxs-lookup"><span data-stu-id="6296b-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="6296b-107">เปิดการใช้งานคีย์การตั้งคอนฟิกลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="6296b-108">ไปที่การจัดการระบบ > การตั้งค่า > การตั้งค่าคอนฟิกลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="6296b-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="6296b-109">ในแผนภูมิ ขยาย 'การจัดการ'</span><span class="sxs-lookup"><span data-stu-id="6296b-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="6296b-110">ตรวจดูว่าได้เลือกกล่องกาเครื่องหมายลายเซ็นอิเล็กทรอนิกส์แล้ว</span><span class="sxs-lookup"><span data-stu-id="6296b-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="6296b-111">ถ้าไม่มีการเลือกกล่องกาเครื่องหมายลายเซ็นอิเล็กทรอนิกส์ คุณต้องเปิดใช้งานโหมดการบำรุงรักษา </span><span class="sxs-lookup"><span data-stu-id="6296b-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="6296b-112">โหมดการบำรุงรักษาสามารถเปิดใช้งานในสภาพแวดล้อมนี้ได้โดยการดำเนินงานการบำรุงรักษาจาก Lifecycle Services หรือโดยการใช้เครื่องมือ Deployment.Setup เฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="6296b-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="6296b-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6296b-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="6296b-114">การตั้งค่าพารามิเตอร์ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="6296b-115">ไปที่การจัดการองค์กร > การตั้งค่า > ลายเซ็นอิเล็กทรอนิกส์ > พารามิเตอร์ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="6296b-116">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="6296b-116">Click Edit.</span></span>
3. <span data-ttu-id="6296b-117">ในฟิลด์หนังสือแจ้ง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6296b-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="6296b-118">ป้อนข้อความแจ้งที่ผู้ลงชื่อจะได้รับเมื่อมีการร้องขอลายเซ็น </span><span class="sxs-lookup"><span data-stu-id="6296b-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="6296b-119">คุณสามารถป้อนข้อความใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="6296b-119">You can enter any text.</span></span> <span data-ttu-id="6296b-120">โดยปกติแล้ว ข้อความนี้แจ้งให้ผู้ใช้ทราบว่าการลงชื่อในเอกสารทางอิเล็กทรอนิกส์หมายถึงอะไร</span><span class="sxs-lookup"><span data-stu-id="6296b-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="6296b-121">ถ้าคุณต้องการป้อนข้อความแจ้งในภาษาเพิ่มเติม ให้คลิกปุ่มการแปล</span><span class="sxs-lookup"><span data-stu-id="6296b-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="6296b-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6296b-122">Click Save.</span></span>
5. <span data-ttu-id="6296b-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6296b-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="6296b-124">การตั้งค่ารหัสเหตุผลสำหรับลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="6296b-125">ไปที่การจัดการองค์กร > การตั้งค่า > ลายเซ็นอิเล็กทรอนิกส์ > รหัสเหตุผลลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="6296b-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6296b-126">Click New.</span></span>
    * <span data-ttu-id="6296b-127">คุณต้องตั้งค่ารหัสเหตุผลก่อนใช้ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="6296b-128">รหัสเหตุผลที่ถูกต้องเป็นสิ่งที่จำเป็นเมื่อลงชื่อในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="6296b-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="6296b-129">ผู้ลงชื่อเลือกรหัสเหตุผลเพื่อบ่งชี้วัตถุประสงค์ของลายเซ็นอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="6296b-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="6296b-130">ตัวอย่างเช่น อาจใช้รหัสเหตุผลเพื่อบ่งชี้การอนุมัติทางกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="6296b-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="6296b-131">ในฟิลด์รหัสเหตุผล ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6296b-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="6296b-132">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6296b-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6296b-133">ป้อนรหัสเหตุผลเพิ่มเติม ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="6296b-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="6296b-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6296b-134">Click Save.</span></span>
6. <span data-ttu-id="6296b-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6296b-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="6296b-136">ต้องการลายเซ็นอิเล็กทรอนิกส์สำหรับกระบวนการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6296b-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="6296b-137">ไปที่การจัดการองค์กร > การตั้งค่า > ลายเซ็นอิเล็กทรอนิกส์ > ข้อกำหนดลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="6296b-138">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6296b-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6296b-139">เลือกกระบวนการที่ต้องใช้ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="6296b-140">ให้เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายต้องมีลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="6296b-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="6296b-141">ทำซ้ำขั้นตอนเหล่านี้สำหรับแต่ละกระบวนการที่ต้องใช้ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="6296b-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6296b-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="6296b-143">ตั้งค่าข้อกำหนดที่กำหนดเองสำหรับลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="6296b-144">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6296b-144">Click New.</span></span>
2. <span data-ttu-id="6296b-145">ให้เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายต้องมีลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="6296b-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="6296b-146">ในฟิลด์ชื่อ ให้ป้อนชื่อสำหรับกระบวนการที่ต้องใช้ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6296b-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="6296b-147">ในฟิลด์ตารางชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6296b-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6296b-148">ในรายการ ให้ค้นหาและเลือกตารางที่ใช้จัดเก็บข้อมูลที่ต้องลงชื่อ</span><span class="sxs-lookup"><span data-stu-id="6296b-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="6296b-149">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6296b-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6296b-150">ในฟิลด์ชื่อฟิลด์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6296b-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6296b-151">ในรายการ ให้ค้นหาและเลือกฟิลด์ในตารางที่คุณต้องการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="6296b-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="6296b-152">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6296b-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6296b-153">ระบุว่าเมื่อใดที่ต้องใช้ลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="6296b-153">Specify when a signature is required.</span></span>     <span data-ttu-id="6296b-154">เลือก เสมอ ถ้าต้องการให้ใช้ลายเซ็นเมื่อข้อมูลในฟิลด์มีการเปลี่ยนแปลง </span><span class="sxs-lookup"><span data-stu-id="6296b-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="6296b-155">เลือก เท่านั้น ถ้าต้องการให้ใช้ลายเซ็นภายใต้เงื่อนไขบางอย่างเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="6296b-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="6296b-156">ถ้าคุณเลือก เท่านั้น คุณยังจะต้องเลือกหนึ่งในตัวเลือกต่อไปนี้ด้วย: เมื่อมีการแทรกเรกคอร์ด เมื่อมีการอัพเดตเรกคอร์ด หรือเมื่อมีการลบเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="6296b-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="6296b-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6296b-157">Click Save.</span></span>
11. <span data-ttu-id="6296b-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6296b-158">Close the page.</span></span>

