---
title: ออกแบบโดเมนของแบบจำลองข้อมูลที่เฉพาะเจาะจงของ ER
description: ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์สามารถสร้างอิเล็กทรอนิกส์ใหม่การตั้งค่าคอนฟิก (ER) ที่ประกอบด้วยแบบจำลองข้อมูลสำหรับเอกสารการชำระเงินทางอิเล็กทรอนิกส์ในการรายงาน
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d66cc69da08478ceb931fab594da51bafcacc38
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185094"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="52bb9-103">ออกแบบโดเมนของแบบจำลองข้อมูลที่เฉพาะเจาะจงของ ER</span><span class="sxs-lookup"><span data-stu-id="52bb9-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52bb9-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์สามารถสร้างอิเล็กทรอนิกส์ใหม่การตั้งค่าคอนฟิก (ER) ที่ประกอบด้วยแบบจำลองข้อมูลสำหรับเอกสารการชำระเงินทางอิเล็กทรอนิกส์ในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="52bb9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="52bb9-105">ในภายหลังแบบจำลองข้อมูลนี้จะสามารถใช้เป็นแหล่งข้อมูลเมื่อคุณสร้างรูปแบบของเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="52bb9-106">ในตัวอย่างนี้ คุณจะสร้างโครงแบบสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถดำเนินการในบริษัทใด ๆ ตามที่ตั้งค่าคอนฟิก ER ใช้ร่วมกันระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="52bb9-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="52bb9-107">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="52bb9-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="52bb9-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="52bb9-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="52bb9-109">เลือกผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง ‘Litware, Inc.‘</span><span class="sxs-lookup"><span data-stu-id="52bb9-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="52bb9-110">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="52bb9-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="52bb9-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="52bb9-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="52bb9-112">คุณจะสร้างการตั้งค่าคอนฟิกที่ประกอบด้วยแบบจำลองข้อมูลสำหรับเอกสารการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="52bb9-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="52bb9-113">รูปแบบข้อมูลนี้จะถูกใช้ในภายหลัง เมื่อคุณสร้างรูปแบบสำหรับเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="52bb9-114">สร้างแบบจำลองการจัดโครงแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="52bb9-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="52bb9-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="52bb9-116">ในฟิลด์ชื่อ พิมพ์ 'การชำระเงิน (แบบอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="52bb9-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="52bb9-117">การชำระเงิน (แบบอย่างง่าย)</span><span class="sxs-lookup"><span data-stu-id="52bb9-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="52bb9-118">ในฟิลด์คำอธิบาย พิมพ์ 'การตั้งค่าคอนฟิกรูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="52bb9-119">การตั้งค่าคอนฟิกรูปแบบการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-119">Payment model configuration</span></span>  
    * <span data-ttu-id="52bb9-120">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="52bb9-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="52bb9-121">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="52bb9-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="52bb9-122">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="52bb9-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="52bb9-123">คลิกปุ่ม 'สร้างการตั้งค่าคอนฟลิก' เพื่อดำเนินงานการสร้างการตั้งค่าคอนฟิกให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="52bb9-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="52bb9-124">สร้างแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="52bb9-124">Create a data model</span></span>
    * <span data-ttu-id="52bb9-125">คุณกำลังสร้างแบบจำลองข้อมูลใหม่สำหรับการตั้งค่าคอนฟิกที่เลือก</span><span class="sxs-lookup"><span data-stu-id="52bb9-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="52bb9-126">เวอร์ชันการตั้งค่าคอนฟิกนี้จะมีสถานะเป็นฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="52bb9-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="52bb9-127">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="52bb9-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="52bb9-128">กำหนดโครงสร้างของฝ่ายที่เข้าร่วมในกระบวนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="52bb9-129">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="52bb9-130">ในฟิลด์ชื่อ ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="52bb9-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="52bb9-131">ฝ่าย</span><span class="sxs-lookup"><span data-stu-id="52bb9-131">Party</span></span>  
3. <span data-ttu-id="52bb9-132">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-132">Click Add.</span></span>
4. <span data-ttu-id="52bb9-133">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="52bb9-134">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="52bb9-135">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="52bb9-135">Name</span></span>  
6. <span data-ttu-id="52bb9-136">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="52bb9-137">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-137">Click Add.</span></span>
8. <span data-ttu-id="52bb9-138">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="52bb9-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="52bb9-139">ฝ่าย</span><span class="sxs-lookup"><span data-stu-id="52bb9-139">Party</span></span>  
9. <span data-ttu-id="52bb9-140">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="52bb9-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="52bb9-141">กำหนดโครงสร้างของธนาคารสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="52bb9-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="52bb9-142">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="52bb9-143">ในฟิลด์ชื่อ พิมพ์ 'ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="52bb9-144">ตัวแทน</span><span class="sxs-lookup"><span data-stu-id="52bb9-144">Agent</span></span>  
3. <span data-ttu-id="52bb9-145">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="52bb9-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="52bb9-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-146">Click Add.</span></span>
5. <span data-ttu-id="52bb9-147">ในฟิลด์คำอธิบาย ให้ป้อน 'สถาบันการเงิน (เช่น ธนาคาร) ที่ให้บริการบัญชีสำหรับฝ่าย (ลูกหนี้/เจ้าหนี้)'</span><span class="sxs-lookup"><span data-stu-id="52bb9-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="52bb9-148">สถาบันการเงิน (เช่น ธนาคาร) ที่ให้บริการบัญชีสำหรับฝ่าย (ลูกหนี้/เจ้าหนี้)</span><span class="sxs-lookup"><span data-stu-id="52bb9-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="52bb9-149">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="52bb9-150">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="52bb9-151">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="52bb9-151">Name</span></span>  
8. <span data-ttu-id="52bb9-152">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="52bb9-153">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-153">Click Add.</span></span>
10. <span data-ttu-id="52bb9-154">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="52bb9-155">ในฟิลด์ชื่อ พิมพ์ 'SWIFT'</span><span class="sxs-lookup"><span data-stu-id="52bb9-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="52bb9-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="52bb9-156">SWIFT</span></span>  
12. <span data-ttu-id="52bb9-157">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-157">Click Add.</span></span>
13. <span data-ttu-id="52bb9-158">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสการระบุของธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="52bb9-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="52bb9-159">รหัสการระบุของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="52bb9-159">Bank identification code</span></span>  
14. <span data-ttu-id="52bb9-160">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="52bb9-161">ในฟิลด์ชื่อ พิมพ์ 'หมายเลขการกำหนดเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="52bb9-162">หมายเลขการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-162">RoutingNumber</span></span>  
16. <span data-ttu-id="52bb9-163">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-163">Click Add.</span></span>
17. <span data-ttu-id="52bb9-164">ในฟิลด์คำอธิบาย ให้ป้อน 'หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="52bb9-165">หมายเลขกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="52bb9-165">Routing number</span></span>  
18. <span data-ttu-id="52bb9-166">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="52bb9-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="52bb9-167">กำหนดโครงสร้างของบัญชีสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="52bb9-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="52bb9-168">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="52bb9-169">ในฟิลด์ชื่อ ให้พิมพ์ 'บัญชี'</span><span class="sxs-lookup"><span data-stu-id="52bb9-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="52bb9-170">บัญชี</span><span class="sxs-lookup"><span data-stu-id="52bb9-170">Account</span></span>  
3. <span data-ttu-id="52bb9-171">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="52bb9-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="52bb9-172">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-172">Click Add.</span></span>
5. <span data-ttu-id="52bb9-173">ในฟิลด์คำอธิบาย ให้ป้อน 'การระบุของบัญชีของฝ่ายในสถาบันการเงิน (เช่น ธนาคาร)'</span><span class="sxs-lookup"><span data-stu-id="52bb9-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="52bb9-174">การระบุของบัญชีของฝ่ายในสถาบันการเงิน (ตัวอย่างเช่น ธนาคาร)</span><span class="sxs-lookup"><span data-stu-id="52bb9-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="52bb9-175">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="52bb9-176">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="52bb9-177">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-177">Currency</span></span>  
8. <span data-ttu-id="52bb9-178">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="52bb9-179">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-179">Click Add.</span></span>
10. <span data-ttu-id="52bb9-180">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสสกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="52bb9-181">รหัสสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-181">Currency code</span></span>  
11. <span data-ttu-id="52bb9-182">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="52bb9-183">ในฟิลด์ชื่อ ให้พิมพ์ 'หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="52bb9-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="52bb9-184">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="52bb9-184">Number</span></span>  
13. <span data-ttu-id="52bb9-185">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-185">Click Add.</span></span>
14. <span data-ttu-id="52bb9-186">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="52bb9-187">ในฟิลด์ชื่อ ให้พิมพ์ 'IBAN'</span><span class="sxs-lookup"><span data-stu-id="52bb9-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="52bb9-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="52bb9-188">IBAN</span></span>  
16. <span data-ttu-id="52bb9-189">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-189">Click Add.</span></span>
17. <span data-ttu-id="52bb9-190">ในฟิลด์คำอธิบาย ให้ป้อน 'เลขที่บัญชีธนาคารระหว่างประเทศ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="52bb9-191">หมายเลขบัญชีธนาคารระหว่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="52bb9-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="52bb9-192">กำหนดโครงสร้างของข้อความการชำระเงินสำหรับชนิดการชำระเงินแบบการโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="52bb9-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="52bb9-193">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="52bb9-194">ในฟิลด์สร้างโหนดใหม่เป็น ให้ป้อน 'รากแบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="52bb9-195">ในฟิลด์ชื่อ ให้พิมพ์ 'การเริ่มต้นการโอนย้ายเครดิตของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="52bb9-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="52bb9-196">เลือก การเริ่มต้นการโอนย้ายเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="52bb9-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="52bb9-197">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-197">Click Add.</span></span>
5. <span data-ttu-id="52bb9-198">ในฟิลด์ค้นหา ให้พิมพ์ 'CustomerCreditTransferInitiation'</span><span class="sxs-lookup"><span data-stu-id="52bb9-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="52bb9-199">เลือก การเริ่มต้นการโอนย้ายเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="52bb9-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="52bb9-200">คลิก ค้นหาก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="52bb9-200">Click Find previous.</span></span>
7. <span data-ttu-id="52bb9-201">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="52bb9-202">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="52bb9-203">รหัสข้อความ</span><span class="sxs-lookup"><span data-stu-id="52bb9-203">MessageIdentification</span></span>  
9. <span data-ttu-id="52bb9-204">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-204">Click Add.</span></span>
10. <span data-ttu-id="52bb9-205">ในฟิลด์คำอธิบาย ให้ป้อน 'การอ้างอิงแบบจุดต่อจุดตามที่กำหนดโดยฝ่ายที่ให้การแนะนำ (และส่งไปยังฝ่ายถัดไป) เพื่อระบุข้อความอย่างชัดเจน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="52bb9-206">การอ้างอิงแบบจุดต่อจุดตามที่กำหนดโดยฝ่ายที่ให้การแนะนำ (และส่งไปยังฝ่ายถัดไป) เพื่อระบุข้อความอย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="52bb9-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="52bb9-207">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="52bb9-208">ในฟิลด์ชื่อ ให้พิมพ์ 'ระยะเวลาประมวลผลข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="52bb9-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="52bb9-209">ระยะเวลาการประมวลผลข้อมูล</span><span class="sxs-lookup"><span data-stu-id="52bb9-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="52bb9-210">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่เวลา'</span><span class="sxs-lookup"><span data-stu-id="52bb9-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="52bb9-211">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-211">Click Add.</span></span>
15. <span data-ttu-id="52bb9-212">ในฟิลด์คำอธิบาย ให้ป้อน 'วันและเวลาที่ข้อความการชำระเงินถูกสร้างขึ้น'</span><span class="sxs-lookup"><span data-stu-id="52bb9-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="52bb9-213">วันที่และเวลาที่ข้อความการชำระเงินถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="52bb9-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="52bb9-214">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="52bb9-215">กำหนดโครงสร้างของธุรกรรมการชำระเงินสำหรับแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="52bb9-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="52bb9-216">ในฟิลด์ชื่อ ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="52bb9-217">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-217">Payments</span></span>  
18. <span data-ttu-id="52bb9-218">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="52bb9-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="52bb9-219">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-219">Click Add.</span></span>
20. <span data-ttu-id="52bb9-220">ในฟิลด์คำอธิบาย ให้ป้อน 'รายการการชำระเงินของเอกสารปัจจุบัน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="52bb9-221">รายการการชำระเงินของเอกสารปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="52bb9-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="52bb9-222">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="52bb9-223">ในฟิลด์ชื่อ ให้พิมพ์ 'เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="52bb9-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="52bb9-224">เจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="52bb9-224">Creditor</span></span>  
23. <span data-ttu-id="52bb9-225">ในฟิลด์ประเภทสินค้า ให้เลือก 'บันทึก'</span><span class="sxs-lookup"><span data-stu-id="52bb9-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="52bb9-226">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-226">Click Add.</span></span>
25. <span data-ttu-id="52bb9-227">ในฟิลด์คำอธิบาย ให้ป้อน 'ฝ่ายที่มียอดเงินถึงเวลาครบกำหนดชำระ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="52bb9-228">ฝ่ายที่มียอดเงินถึงเวลาครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="52bb9-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="52bb9-229">คลิก สลับการอ้างอิงรายการ</span><span class="sxs-lookup"><span data-stu-id="52bb9-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="52bb9-230">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="52bb9-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="52bb9-231">ฝ่าย</span><span class="sxs-lookup"><span data-stu-id="52bb9-231">Party</span></span>  
28. <span data-ttu-id="52bb9-232">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="52bb9-232">Click Find next.</span></span>
29. <span data-ttu-id="52bb9-233">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="52bb9-233">Click OK.</span></span>
30. <span data-ttu-id="52bb9-234">ในฟิลด์ค้นหา ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="52bb9-235">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-235">Payments</span></span>  
31. <span data-ttu-id="52bb9-236">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="52bb9-236">Click Find next.</span></span>
32. <span data-ttu-id="52bb9-237">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="52bb9-238">ในฟิลด์ชื่อ ให้พิมพ์ 'ลูกหนี้'</span><span class="sxs-lookup"><span data-stu-id="52bb9-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="52bb9-239">ลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="52bb9-239">Debtor</span></span>  
34. <span data-ttu-id="52bb9-240">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-240">Click Add.</span></span>
35. <span data-ttu-id="52bb9-241">ในฟิลด์คำอธิบาย ให้ป้อน 'ฝ่ายที่ค้างชำระยอดเงินกับเจ้าหนี้ (ลำดับสุดท้าย)'</span><span class="sxs-lookup"><span data-stu-id="52bb9-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="52bb9-242">ฝ่ายที่ค้างชำระยอดเงินกับเจ้าหนี้ (ลำดับสุดท้าย)</span><span class="sxs-lookup"><span data-stu-id="52bb9-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="52bb9-243">คลิก สลับการอ้างอิงรายการ</span><span class="sxs-lookup"><span data-stu-id="52bb9-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="52bb9-244">ในฟิลด์ค้นหา ให้พิมพ์ 'ฝ่าย'</span><span class="sxs-lookup"><span data-stu-id="52bb9-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="52bb9-245">ฝ่าย</span><span class="sxs-lookup"><span data-stu-id="52bb9-245">Party</span></span>  
38. <span data-ttu-id="52bb9-246">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="52bb9-246">Click Find next.</span></span>
39. <span data-ttu-id="52bb9-247">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="52bb9-247">Click OK.</span></span>
40. <span data-ttu-id="52bb9-248">คลิก ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="52bb9-248">Click Find next.</span></span>
41. <span data-ttu-id="52bb9-249">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="52bb9-250">ในฟิลด์ชื่อ ให้พิมพ์ 'คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="52bb9-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="52bb9-251">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="52bb9-251">Description</span></span>  
43. <span data-ttu-id="52bb9-252">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="52bb9-253">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-253">Click Add.</span></span>
45. <span data-ttu-id="52bb9-254">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="52bb9-255">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="52bb9-256">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-256">Currency</span></span>  
47. <span data-ttu-id="52bb9-257">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-257">Click Add.</span></span>
48. <span data-ttu-id="52bb9-258">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสสกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="52bb9-259">รหัสสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-259">Currency code</span></span>  
49. <span data-ttu-id="52bb9-260">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="52bb9-261">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="52bb9-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="52bb9-262">วันที่ทำธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="52bb9-262">TransactionDate</span></span>  
51. <span data-ttu-id="52bb9-263">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="52bb9-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="52bb9-264">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-264">Click Add.</span></span>
53. <span data-ttu-id="52bb9-265">ในฟิลด์คำอธิบาย ให้ป้อน 'วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="52bb9-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="52bb9-266">วันที่ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="52bb9-266">Transaction date</span></span>  
54. <span data-ttu-id="52bb9-267">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="52bb9-268">ในฟิลด์ชื่อ ให้พิมพ์ 'ยอดเงินที่แนะนำ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="52bb9-269">ยอดเงินที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="52bb9-269">InstructedAmount</span></span>  
56. <span data-ttu-id="52bb9-270">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนจริง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="52bb9-271">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-271">Click Add.</span></span>
58. <span data-ttu-id="52bb9-272">ในฟิลด์คำอธิบาย ให้ป้อน 'ยอดเงินที่เคลื่อนไหวระหว่างลูกหนี้กับเจ้าหนี้ ก่อนที่จะมีการหักลดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="52bb9-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="52bb9-273">ยอดเงินควรจะถูกแสดงในสกุลเงินตามที่มีการสั่งโดยฝ่ายผู้สร้างข้อความ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="52bb9-274">ยอดเงินที่เคลื่อนไหวระหว่างลูกหนี้กับเจ้าหนี้ ก่อนที่จะมีการหักลดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="52bb9-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="52bb9-275">ยอดเงินควรจะถูกแสดงในสกุลเงินตามที่มีการสั่งโดยฝ่ายผู้สร้างข้อความ</span><span class="sxs-lookup"><span data-stu-id="52bb9-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="52bb9-276">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="52bb9-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="52bb9-277">ในฟิลด์ชื่อ ให้พิมพ์'End2EndID'</span><span class="sxs-lookup"><span data-stu-id="52bb9-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="52bb9-278">รหัสแบบครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="52bb9-278">End2EndID</span></span>  
61. <span data-ttu-id="52bb9-279">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="52bb9-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="52bb9-280">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="52bb9-280">Click Add.</span></span>
63. <span data-ttu-id="52bb9-281">ในฟิลด์คำอธิบาย ให้ป้อน 'รหัสแบบเฉพาะตามที่กำหนดโดยฝ่ายผู้สร้างข้อความ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="52bb9-282">การระบุรหัสนี้มีการส่งผ่านโดยไม่มีการเปลี่ยนแปลงตลอดห่วงโซ่ตั้งแต่ต้นจนจบ'</span><span class="sxs-lookup"><span data-stu-id="52bb9-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="52bb9-283">การระบุรหัสแบบเฉพาะตามที่กำหนดโดยฝ่ายผู้สร้างข้อความ</span><span class="sxs-lookup"><span data-stu-id="52bb9-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="52bb9-284">การระบุรหัสนี้ถูกส่งผ่านโดยไม่มีการเปลี่ยนแปลงตลอดห่วงโซตั้งแต่ต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="52bb9-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="52bb9-285">ในฟิลด์ชื่อ พิมพ์ 'รูปแบบการชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="52bb9-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="52bb9-286">ชื่อของ PaymentModel จัดเรียงตามอินเทอเฟสที่ถูกกำหนดไว้ก่อนหน้าของแบบชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52bb9-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="52bb9-287">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="52bb9-287">Click Save.</span></span>
66. <span data-ttu-id="52bb9-288">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="52bb9-288">Close the page.</span></span>

