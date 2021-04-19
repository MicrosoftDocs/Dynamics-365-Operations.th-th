---
title: ออกแบบโดเมนของแบบจำลองข้อมูลที่เฉพาะเจาะจงของ ER
description: หัวข้อนี้จะอธิบายวิธีการสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)ใหม่ ที่มีรูปแบบข้อมูลสำหรับเอกสารการชำระเงินอิเล็กทรอนิกส์
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351c5a6624f7ee912c507a9f74324f4c8f61166b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755045"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="87a83-103">ออกแบบโดเมนของแบบจำลองข้อมูลที่เฉพาะเจาะจงของ ER</span><span class="sxs-lookup"><span data-stu-id="87a83-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87a83-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์สามารถสร้างอิเล็กทรอนิกส์ใหม่การตั้งค่าคอนฟิก (ER) ที่ประกอบด้วยแบบจำลองข้อมูลสำหรับเอกสารการชำระเงินทางอิเล็กทรอนิกส์ในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="87a83-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="87a83-105">ในภายหลังแบบจำลองข้อมูลนี้จะสามารถใช้เป็นแหล่งข้อมูลเมื่อคุณสร้างรูปแบบของเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="87a83-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="87a83-106">ในตัวอย่างนี้ คุณจะสร้างโครงแบบสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถดำเนินการในบริษัทใด ๆ ตามที่ตั้งค่าคอนฟิก ER ใช้ร่วมกันระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="87a83-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="87a83-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="87a83-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="87a83-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="87a83-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="87a83-109">เลือกผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="87a83-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="87a83-110">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="87a83-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="87a83-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="87a83-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="87a83-112">คุณจะสร้างการตั้งค่าคอนฟิกที่ประกอบด้วยแบบจำลองข้อมูลสำหรับเอกสารการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="87a83-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="87a83-113">รูปแบบข้อมูลนี้จะถูกใช้ในภายหลัง เมื่อคุณสร้างรูปแบบสำหรับเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="87a83-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="87a83-114">สร้างแบบจำลองการจัดโครงแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="87a83-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="87a83-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="87a83-116">ในฟิลด์ชื่อ พิมพ์ 'การชำระเงิน (แบบอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="87a83-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="87a83-117">ในฟิลด์คำอธิบาย พิมพ์ 'การตั้งค่าคอนฟิกรูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="87a83-118">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="87a83-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="87a83-119">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="87a83-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="87a83-120">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="87a83-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="87a83-121">คลิกปุ่ม 'สร้างการตั้งค่าคอนฟิก' เพื่อดำเนินงานการสร้างการตั้งค่าคอนฟิกให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="87a83-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="87a83-122">สร้างแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="87a83-122">Create a data model</span></span>
<span data-ttu-id="87a83-123">คุณกำลังสร้างแบบจำลองข้อมูลใหม่สำหรับการตั้งค่าคอนฟิกที่เลือก</span><span class="sxs-lookup"><span data-stu-id="87a83-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="87a83-124">เวอร์ชันการตั้งค่าคอนฟิกนี้จะมีสถานะเป็นฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="87a83-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="87a83-125">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="87a83-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="87a83-126">กำหนดโครงสร้างของฝ่ายที่เข้าร่วมในกระบวนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="87a83-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="87a83-127">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="87a83-128">ในฟิลด์ชื่อ ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="87a83-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="87a83-129">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-129">Click Add.</span></span>
4. <span data-ttu-id="87a83-130">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="87a83-131">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="87a83-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="87a83-132">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="87a83-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="87a83-133">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-133">Click Add.</span></span>
8. <span data-ttu-id="87a83-134">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="87a83-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="87a83-135">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="87a83-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="87a83-136">กำหนดโครงสร้างของธนาคารสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="87a83-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="87a83-137">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="87a83-138">ในฟิลด์ชื่อ พิมพ์ 'ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="87a83-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="87a83-139">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="87a83-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="87a83-140">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-140">Click Add.</span></span>
5. <span data-ttu-id="87a83-141">ในฟิลด์คำอธิบาย ให้ป้อน 'สถาบันการเงิน (เช่น ธนาคาร) ที่ให้บริการบัญชีสำหรับฝ่าย (ลูกหนี้/เจ้าหนี้)'</span><span class="sxs-lookup"><span data-stu-id="87a83-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="87a83-142">สถาบันการเงิน (เช่น ธนาคาร) ที่ให้บริการบัญชีสำหรับฝ่าย (ลูกหนี้/เจ้าหนี้)</span><span class="sxs-lookup"><span data-stu-id="87a83-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="87a83-143">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="87a83-144">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="87a83-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="87a83-145">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="87a83-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="87a83-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-146">Click Add.</span></span>
10. <span data-ttu-id="87a83-147">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="87a83-148">ในฟิลด์ชื่อ พิมพ์ 'SWIFT'</span><span class="sxs-lookup"><span data-stu-id="87a83-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="87a83-149">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-149">Click Add.</span></span>
13. <span data-ttu-id="87a83-150">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสการระบุของธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="87a83-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="87a83-151">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="87a83-152">ในฟิลด์ชื่อ พิมพ์ 'หมายเลขการกำหนดเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="87a83-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="87a83-153">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-153">Click Add.</span></span>
17. <span data-ttu-id="87a83-154">ในฟิลด์คำอธิบาย ให้ป้อน 'หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="87a83-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="87a83-155">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="87a83-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="87a83-156">กำหนดโครงสร้างของบัญชีสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="87a83-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="87a83-157">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="87a83-158">ในฟิลด์ชื่อ ให้พิมพ์ 'บัญชี'</span><span class="sxs-lookup"><span data-stu-id="87a83-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="87a83-159">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="87a83-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="87a83-160">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-160">Click Add.</span></span>
5. <span data-ttu-id="87a83-161">ในฟิลด์คำอธิบาย ให้ป้อน 'การระบุของบัญชีของฝ่ายในสถาบันการเงิน (เช่น ธนาคาร)'</span><span class="sxs-lookup"><span data-stu-id="87a83-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="87a83-162">การระบุของบัญชีของฝ่ายในสถาบันการเงิน (ตัวอย่างเช่น ธนาคาร)</span><span class="sxs-lookup"><span data-stu-id="87a83-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="87a83-163">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="87a83-164">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="87a83-165">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="87a83-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="87a83-166">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-166">Click Add.</span></span>
10. <span data-ttu-id="87a83-167">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสสกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="87a83-168">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="87a83-169">ในฟิลด์ชื่อ ให้พิมพ์ 'หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="87a83-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="87a83-170">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-170">Click Add.</span></span>
14. <span data-ttu-id="87a83-171">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="87a83-172">ในฟิลด์ชื่อ ให้พิมพ์ 'IBAN'</span><span class="sxs-lookup"><span data-stu-id="87a83-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="87a83-173">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-173">Click Add.</span></span>
17. <span data-ttu-id="87a83-174">ในฟิลด์คำอธิบาย ให้ป้อน 'เลขที่บัญชีธนาคารระหว่างประเทศ'</span><span class="sxs-lookup"><span data-stu-id="87a83-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="87a83-175">กำหนดโครงสร้างของข้อความการชำระเงินสำหรับชนิดการชำระเงินแบบการโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="87a83-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="87a83-176">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="87a83-177">ในฟิลด์สร้างโหนดใหม่เป็น ให้ป้อน 'รากแบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="87a83-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="87a83-178">ในฟิลด์ชื่อ ให้พิมพ์ 'การเริ่มต้นการโอนย้ายเครดิตของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="87a83-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="87a83-179">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-179">Click Add.</span></span>
5. <span data-ttu-id="87a83-180">ในฟิลด์ค้นหา ให้พิมพ์ 'CustomerCreditTransferInitiation'</span><span class="sxs-lookup"><span data-stu-id="87a83-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="87a83-181">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="87a83-181">Click Find previous.</span></span>
7. <span data-ttu-id="87a83-182">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="87a83-183">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="87a83-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="87a83-184">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-184">Click Add.</span></span>
10. <span data-ttu-id="87a83-185">ในฟิลด์คำอธิบาย ให้ป้อน 'การอ้างอิงแบบจุดต่อจุดตามที่กำหนดโดยฝ่ายที่ให้การแนะนำ (และส่งไปยังฝ่ายถัดไป) เพื่อระบุข้อความอย่างชัดเจน'</span><span class="sxs-lookup"><span data-stu-id="87a83-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="87a83-186">การอ้างอิงแบบจุดต่อจุดตามที่กำหนดโดยฝ่ายที่ให้การแนะนำ (และส่งไปยังฝ่ายถัดไป) เพื่อระบุข้อความอย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="87a83-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="87a83-187">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="87a83-188">ในฟิลด์ชื่อ ให้พิมพ์ 'ระยะเวลาประมวลผลข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="87a83-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="87a83-189">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่เวลา'</span><span class="sxs-lookup"><span data-stu-id="87a83-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="87a83-190">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-190">Click Add.</span></span>
15. <span data-ttu-id="87a83-191">ในฟิลด์คำอธิบาย ให้ป้อน 'วันและเวลาที่ข้อความการชำระเงินถูกสร้างขึ้น'</span><span class="sxs-lookup"><span data-stu-id="87a83-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="87a83-192">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="87a83-193">กำหนดโครงสร้างของธุรกรรมการชำระเงินสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="87a83-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="87a83-194">ในฟิลด์ชื่อ ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="87a83-195">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="87a83-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="87a83-196">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-196">Click Add.</span></span>
20. <span data-ttu-id="87a83-197">ในฟิลด์คำอธิบาย ให้ป้อน 'รายการการชำระเงินของเอกสารปัจจุบัน'</span><span class="sxs-lookup"><span data-stu-id="87a83-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="87a83-198">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="87a83-199">ในฟิลด์ชื่อ ให้พิมพ์ 'เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="87a83-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="87a83-200">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="87a83-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="87a83-201">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-201">Click Add.</span></span>
25. <span data-ttu-id="87a83-202">ในฟิลด์คำอธิบาย ให้ป้อน 'ฝ่ายที่มียอดเงินถึงเวลาครบกำหนดชำระ'</span><span class="sxs-lookup"><span data-stu-id="87a83-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="87a83-203">คลิก สลับการอ้างอิงรายการ</span><span class="sxs-lookup"><span data-stu-id="87a83-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="87a83-204">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="87a83-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="87a83-205">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="87a83-205">Click Find next.</span></span>
29. <span data-ttu-id="87a83-206">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="87a83-206">Click OK.</span></span>
30. <span data-ttu-id="87a83-207">ในฟิลด์ค้นหา ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="87a83-208">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="87a83-208">Click Find next.</span></span>
32. <span data-ttu-id="87a83-209">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="87a83-210">ในฟิลด์ชื่อ ให้พิมพ์ 'ลูกหนี้'</span><span class="sxs-lookup"><span data-stu-id="87a83-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="87a83-211">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-211">Click Add.</span></span>
35. <span data-ttu-id="87a83-212">ในฟิลด์คำอธิบาย ให้ป้อน 'ฝ่ายที่ค้างชำระยอดเงินกับเจ้าหนี้ (ลำดับสุดท้าย)'</span><span class="sxs-lookup"><span data-stu-id="87a83-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="87a83-213">คลิก สลับการอ้างอิงรายการ</span><span class="sxs-lookup"><span data-stu-id="87a83-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="87a83-214">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="87a83-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="87a83-215">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="87a83-215">Click Find next.</span></span>
39. <span data-ttu-id="87a83-216">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="87a83-216">Click OK.</span></span>
40. <span data-ttu-id="87a83-217">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="87a83-217">Click Find next.</span></span>
41. <span data-ttu-id="87a83-218">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="87a83-219">ในฟิลด์ชื่อ ให้พิมพ์ 'คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="87a83-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="87a83-220">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="87a83-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="87a83-221">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-221">Click Add.</span></span>
45. <span data-ttu-id="87a83-222">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="87a83-223">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="87a83-224">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-224">Click Add.</span></span>
48. <span data-ttu-id="87a83-225">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสสกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="87a83-226">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="87a83-227">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="87a83-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="87a83-228">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="87a83-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="87a83-229">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-229">Click Add.</span></span>
53. <span data-ttu-id="87a83-230">ในฟิลด์คำอธิบาย ให้ป้อน 'วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="87a83-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="87a83-231">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="87a83-232">ในฟิลด์ชื่อ ให้พิมพ์ 'ยอดเงินที่แนะนำ'</span><span class="sxs-lookup"><span data-stu-id="87a83-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="87a83-233">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนจริง'</span><span class="sxs-lookup"><span data-stu-id="87a83-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="87a83-234">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-234">Click Add.</span></span>
58. <span data-ttu-id="87a83-235">ในฟิลด์คำอธิบาย ให้ป้อน 'ยอดเงินที่เคลื่อนไหวระหว่างลูกหนี้กับเจ้าหนี้ ก่อนที่จะมีการหักลดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="87a83-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="87a83-236">ยอดเงินควรจะถูกแสดงในสกุลเงินตามที่มีการสั่งโดยฝ่ายผู้สร้างข้อความ'</span><span class="sxs-lookup"><span data-stu-id="87a83-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="87a83-237">ยอดเงินที่เคลื่อนไหวระหว่างลูกหนี้กับเจ้าหนี้ ก่อนที่จะมีการหักลดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="87a83-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="87a83-238">ยอดเงินควรจะถูกแสดงในสกุลเงินตามที่มีการสั่งโดยฝ่ายผู้สร้างข้อความ</span><span class="sxs-lookup"><span data-stu-id="87a83-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="87a83-239">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="87a83-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="87a83-240">ในฟิลด์ชื่อ ให้พิมพ์'End2EndID'</span><span class="sxs-lookup"><span data-stu-id="87a83-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="87a83-241">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="87a83-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="87a83-242">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="87a83-242">Click Add.</span></span>
63. <span data-ttu-id="87a83-243">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสแบบเฉพาะตามที่กำหนดโดยฝ่ายผู้สร้างข้อความ'</span><span class="sxs-lookup"><span data-stu-id="87a83-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="87a83-244">การระบุรหัสนี้มีการส่งผ่านโดยไม่มีการเปลี่ยนแปลงตลอดห่วงโซ่ตั้งแต่ต้นจนจบ'</span><span class="sxs-lookup"><span data-stu-id="87a83-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="87a83-245">ในฟิลด์ชื่อ พิมพ์ 'รูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="87a83-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="87a83-246">ชื่อของ PaymentModel จัดเรียงตามอินเทอเฟสที่ถูกกำหนดไว้ก่อนหน้าของแบบชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="87a83-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="87a83-247">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="87a83-247">Click Save.</span></span>
66. <span data-ttu-id="87a83-248">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="87a83-248">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]