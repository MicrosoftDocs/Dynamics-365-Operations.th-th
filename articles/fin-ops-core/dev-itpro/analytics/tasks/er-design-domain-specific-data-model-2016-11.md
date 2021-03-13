---
title: ออกแบบโดเมนของแบบจำลองข้อมูลที่เฉพาะเจาะจงของ ER
description: หัวข้อนี้จะอธิบายวิธีการสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)ใหม่ ที่มีรูปแบบข้อมูลสำหรับเอกสารการชำระเงินอิเล็กทรอนิกส์
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1eb2c6e5b5f186fb6db7c32a9982807274e5ea1b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092702"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="eddfe-103">ออกแบบโดเมนของแบบจำลองข้อมูลที่เฉพาะเจาะจงของ ER</span><span class="sxs-lookup"><span data-stu-id="eddfe-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eddfe-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์สามารถสร้างอิเล็กทรอนิกส์ใหม่การตั้งค่าคอนฟิก (ER) ที่ประกอบด้วยแบบจำลองข้อมูลสำหรับเอกสารการชำระเงินทางอิเล็กทรอนิกส์ในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="eddfe-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="eddfe-105">ในภายหลังแบบจำลองข้อมูลนี้จะสามารถใช้เป็นแหล่งข้อมูลเมื่อคุณสร้างรูปแบบของเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="eddfe-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="eddfe-106">ในตัวอย่างนี้ คุณจะสร้างโครงแบบสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถดำเนินการในบริษัทใด ๆ ตามที่ตั้งค่าคอนฟิก ER ใช้ร่วมกันระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="eddfe-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="eddfe-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="eddfe-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="eddfe-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="eddfe-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="eddfe-109">เลือกผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="eddfe-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="eddfe-110">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="eddfe-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="eddfe-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="eddfe-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="eddfe-112">คุณจะสร้างการตั้งค่าคอนฟิกที่ประกอบด้วยแบบจำลองข้อมูลสำหรับเอกสารการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="eddfe-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="eddfe-113">รูปแบบข้อมูลนี้จะถูกใช้ในภายหลัง เมื่อคุณสร้างรูปแบบสำหรับเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="eddfe-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="eddfe-114">สร้างแบบจำลองการจัดโครงแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="eddfe-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="eddfe-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="eddfe-116">ในฟิลด์ชื่อ พิมพ์ 'การชำระเงิน (แบบอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="eddfe-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="eddfe-117">ในฟิลด์คำอธิบาย พิมพ์ 'การตั้งค่าคอนฟิกรูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="eddfe-118">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="eddfe-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="eddfe-119">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="eddfe-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="eddfe-120">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="eddfe-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="eddfe-121">คลิกปุ่ม 'สร้างการตั้งค่าคอนฟิก' เพื่อดำเนินงานการสร้างการตั้งค่าคอนฟิกให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="eddfe-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="eddfe-122">สร้างแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="eddfe-122">Create a data model</span></span>
<span data-ttu-id="eddfe-123">คุณกำลังสร้างแบบจำลองข้อมูลใหม่สำหรับการตั้งค่าคอนฟิกที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eddfe-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="eddfe-124">เวอร์ชันการตั้งค่าคอนฟิกนี้จะมีสถานะเป็นฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="eddfe-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="eddfe-125">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="eddfe-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="eddfe-126">กำหนดโครงสร้างของฝ่ายที่เข้าร่วมในกระบวนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="eddfe-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="eddfe-127">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="eddfe-128">ในฟิลด์ชื่อ ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="eddfe-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="eddfe-129">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-129">Click Add.</span></span>
4. <span data-ttu-id="eddfe-130">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="eddfe-131">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="eddfe-132">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="eddfe-133">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-133">Click Add.</span></span>
8. <span data-ttu-id="eddfe-134">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="eddfe-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="eddfe-135">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="eddfe-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="eddfe-136">กำหนดโครงสร้างของธนาคารสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="eddfe-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="eddfe-137">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="eddfe-138">ในฟิลด์ชื่อ พิมพ์ 'ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="eddfe-139">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="eddfe-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="eddfe-140">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-140">Click Add.</span></span>
5. <span data-ttu-id="eddfe-141">ในฟิลด์คำอธิบาย ให้ป้อน 'สถาบันการเงิน (เช่น ธนาคาร) ที่ให้บริการบัญชีสำหรับฝ่าย (ลูกหนี้/เจ้าหนี้)'</span><span class="sxs-lookup"><span data-stu-id="eddfe-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="eddfe-142">สถาบันการเงิน (เช่น ธนาคาร) ที่ให้บริการบัญชีสำหรับฝ่าย (ลูกหนี้/เจ้าหนี้)</span><span class="sxs-lookup"><span data-stu-id="eddfe-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="eddfe-143">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="eddfe-144">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="eddfe-145">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="eddfe-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-146">Click Add.</span></span>
10. <span data-ttu-id="eddfe-147">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="eddfe-148">ในฟิลด์ชื่อ พิมพ์ 'SWIFT'</span><span class="sxs-lookup"><span data-stu-id="eddfe-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="eddfe-149">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-149">Click Add.</span></span>
13. <span data-ttu-id="eddfe-150">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสการระบุของธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="eddfe-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="eddfe-151">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="eddfe-152">ในฟิลด์ชื่อ พิมพ์ 'หมายเลขการกำหนดเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="eddfe-153">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-153">Click Add.</span></span>
17. <span data-ttu-id="eddfe-154">ในฟิลด์คำอธิบาย ให้ป้อน 'หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="eddfe-155">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="eddfe-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="eddfe-156">กำหนดโครงสร้างของบัญชีสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="eddfe-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="eddfe-157">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="eddfe-158">ในฟิลด์ชื่อ ให้พิมพ์ 'บัญชี'</span><span class="sxs-lookup"><span data-stu-id="eddfe-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="eddfe-159">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="eddfe-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="eddfe-160">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-160">Click Add.</span></span>
5. <span data-ttu-id="eddfe-161">ในฟิลด์คำอธิบาย ให้ป้อน 'การระบุของบัญชีของฝ่ายในสถาบันการเงิน (เช่น ธนาคาร)'</span><span class="sxs-lookup"><span data-stu-id="eddfe-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="eddfe-162">การระบุของบัญชีของฝ่ายในสถาบันการเงิน (ตัวอย่างเช่น ธนาคาร)</span><span class="sxs-lookup"><span data-stu-id="eddfe-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="eddfe-163">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="eddfe-164">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="eddfe-165">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="eddfe-166">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-166">Click Add.</span></span>
10. <span data-ttu-id="eddfe-167">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสสกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="eddfe-168">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="eddfe-169">ในฟิลด์ชื่อ ให้พิมพ์ 'หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="eddfe-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="eddfe-170">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-170">Click Add.</span></span>
14. <span data-ttu-id="eddfe-171">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="eddfe-172">ในฟิลด์ชื่อ ให้พิมพ์ 'IBAN'</span><span class="sxs-lookup"><span data-stu-id="eddfe-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="eddfe-173">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-173">Click Add.</span></span>
17. <span data-ttu-id="eddfe-174">ในฟิลด์คำอธิบาย ให้ป้อน 'เลขที่บัญชีธนาคารระหว่างประเทศ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="eddfe-175">กำหนดโครงสร้างของข้อความการชำระเงินสำหรับชนิดการชำระเงินแบบการโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="eddfe-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="eddfe-176">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="eddfe-177">ในฟิลด์สร้างโหนดใหม่เป็น ให้ป้อน 'รากแบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="eddfe-178">ในฟิลด์ชื่อ ให้พิมพ์ 'การเริ่มต้นการโอนย้ายเครดิตของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="eddfe-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="eddfe-179">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-179">Click Add.</span></span>
5. <span data-ttu-id="eddfe-180">ในฟิลด์ค้นหา ให้พิมพ์ 'CustomerCreditTransferInitiation'</span><span class="sxs-lookup"><span data-stu-id="eddfe-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="eddfe-181">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="eddfe-181">Click Find previous.</span></span>
7. <span data-ttu-id="eddfe-182">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="eddfe-183">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="eddfe-184">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-184">Click Add.</span></span>
10. <span data-ttu-id="eddfe-185">ในฟิลด์คำอธิบาย ให้ป้อน 'การอ้างอิงแบบจุดต่อจุดตามที่กำหนดโดยฝ่ายที่ให้การแนะนำ (และส่งไปยังฝ่ายถัดไป) เพื่อระบุข้อความอย่างชัดเจน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="eddfe-186">การอ้างอิงแบบจุดต่อจุดตามที่กำหนดโดยฝ่ายที่ให้การแนะนำ (และส่งไปยังฝ่ายถัดไป) เพื่อระบุข้อความอย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="eddfe-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="eddfe-187">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="eddfe-188">ในฟิลด์ชื่อ ให้พิมพ์ 'ระยะเวลาประมวลผลข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="eddfe-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="eddfe-189">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่เวลา'</span><span class="sxs-lookup"><span data-stu-id="eddfe-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="eddfe-190">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-190">Click Add.</span></span>
15. <span data-ttu-id="eddfe-191">ในฟิลด์คำอธิบาย ให้ป้อน 'วันและเวลาที่ข้อความการชำระเงินถูกสร้างขึ้น'</span><span class="sxs-lookup"><span data-stu-id="eddfe-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="eddfe-192">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="eddfe-193">กำหนดโครงสร้างของธุรกรรมการชำระเงินสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="eddfe-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="eddfe-194">ในฟิลด์ชื่อ ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="eddfe-195">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="eddfe-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="eddfe-196">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-196">Click Add.</span></span>
20. <span data-ttu-id="eddfe-197">ในฟิลด์คำอธิบาย ให้ป้อน 'รายการการชำระเงินของเอกสารปัจจุบัน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="eddfe-198">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="eddfe-199">ในฟิลด์ชื่อ ให้พิมพ์ 'เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="eddfe-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="eddfe-200">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="eddfe-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="eddfe-201">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-201">Click Add.</span></span>
25. <span data-ttu-id="eddfe-202">ในฟิลด์คำอธิบาย ให้ป้อน 'ฝ่ายที่มียอดเงินถึงเวลาครบกำหนดชำระ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="eddfe-203">คลิก สลับการอ้างอิงรายการ</span><span class="sxs-lookup"><span data-stu-id="eddfe-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="eddfe-204">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="eddfe-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="eddfe-205">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="eddfe-205">Click Find next.</span></span>
29. <span data-ttu-id="eddfe-206">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="eddfe-206">Click OK.</span></span>
30. <span data-ttu-id="eddfe-207">ในฟิลด์ค้นหา ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="eddfe-208">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="eddfe-208">Click Find next.</span></span>
32. <span data-ttu-id="eddfe-209">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="eddfe-210">ในฟิลด์ชื่อ ให้พิมพ์ 'ลูกหนี้'</span><span class="sxs-lookup"><span data-stu-id="eddfe-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="eddfe-211">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-211">Click Add.</span></span>
35. <span data-ttu-id="eddfe-212">ในฟิลด์คำอธิบาย ให้ป้อน 'ฝ่ายที่ค้างชำระยอดเงินกับเจ้าหนี้ (ลำดับสุดท้าย)'</span><span class="sxs-lookup"><span data-stu-id="eddfe-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="eddfe-213">คลิก สลับการอ้างอิงรายการ</span><span class="sxs-lookup"><span data-stu-id="eddfe-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="eddfe-214">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="eddfe-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="eddfe-215">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="eddfe-215">Click Find next.</span></span>
39. <span data-ttu-id="eddfe-216">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="eddfe-216">Click OK.</span></span>
40. <span data-ttu-id="eddfe-217">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="eddfe-217">Click Find next.</span></span>
41. <span data-ttu-id="eddfe-218">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="eddfe-219">ในฟิลด์ชื่อ ให้พิมพ์ 'คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="eddfe-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="eddfe-220">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="eddfe-221">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-221">Click Add.</span></span>
45. <span data-ttu-id="eddfe-222">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="eddfe-223">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="eddfe-224">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-224">Click Add.</span></span>
48. <span data-ttu-id="eddfe-225">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสสกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="eddfe-226">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="eddfe-227">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="eddfe-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="eddfe-228">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="eddfe-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="eddfe-229">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-229">Click Add.</span></span>
53. <span data-ttu-id="eddfe-230">ในฟิลด์คำอธิบาย ให้ป้อน 'วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="eddfe-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="eddfe-231">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="eddfe-232">ในฟิลด์ชื่อ ให้พิมพ์ 'ยอดเงินที่แนะนำ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="eddfe-233">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนจริง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="eddfe-234">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-234">Click Add.</span></span>
58. <span data-ttu-id="eddfe-235">ในฟิลด์คำอธิบาย ให้ป้อน 'ยอดเงินที่เคลื่อนไหวระหว่างลูกหนี้กับเจ้าหนี้ ก่อนที่จะมีการหักลดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="eddfe-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="eddfe-236">ยอดเงินควรจะถูกแสดงในสกุลเงินตามที่มีการสั่งโดยฝ่ายผู้สร้างข้อความ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="eddfe-237">ยอดเงินที่เคลื่อนไหวระหว่างลูกหนี้กับเจ้าหนี้ ก่อนที่จะมีการหักลดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="eddfe-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="eddfe-238">ยอดเงินควรจะถูกแสดงในสกุลเงินตามที่มีการสั่งโดยฝ่ายผู้สร้างข้อความ</span><span class="sxs-lookup"><span data-stu-id="eddfe-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="eddfe-239">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="eddfe-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="eddfe-240">ในฟิลด์ชื่อ ให้พิมพ์'End2EndID'</span><span class="sxs-lookup"><span data-stu-id="eddfe-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="eddfe-241">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="eddfe-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="eddfe-242">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eddfe-242">Click Add.</span></span>
63. <span data-ttu-id="eddfe-243">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสแบบเฉพาะตามที่กำหนดโดยฝ่ายผู้สร้างข้อความ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="eddfe-244">การระบุรหัสนี้มีการส่งผ่านโดยไม่มีการเปลี่ยนแปลงตลอดห่วงโซ่ตั้งแต่ต้นจนจบ'</span><span class="sxs-lookup"><span data-stu-id="eddfe-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="eddfe-245">ในฟิลด์ชื่อ พิมพ์ 'รูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="eddfe-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="eddfe-246">ชื่อของ PaymentModel จัดเรียงตามอินเทอเฟสที่ถูกกำหนดไว้ก่อนหน้าของแบบชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="eddfe-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="eddfe-247">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="eddfe-247">Click Save.</span></span>
66. <span data-ttu-id="eddfe-248">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="eddfe-248">Close the page.</span></span>

