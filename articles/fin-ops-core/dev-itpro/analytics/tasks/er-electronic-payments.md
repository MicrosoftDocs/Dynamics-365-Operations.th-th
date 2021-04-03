---
title: ER สร้างเอกสารทางอิเล็กทรอนิกส์ สำหรับการชำระเงินโดยใช้การตั้งค่าคอนฟิกรูปแบบ
description: หัวข้อนี้อธิบายวิธีการใช้การตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ เพื่อสร้างเอกสารอิเล็กทรอนิกสำหรับการประมวลผลการชำระเงิน
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dd39b3faba90b38b837cd5167b216f9faa31d82
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570227"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="78334-103">ER สร้างเอกสารทางอิเล็กทรอนิกส์ สำหรับการชำระเงินโดยใช้การตั้งค่าคอนฟิกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="78334-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78334-104">ขั้นตอนต่อไปนี้อธิบายถึง วิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถใช้การตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ เพื่อสร้างเอกสารทางอิเล็กทรอนิกส์สำหรับการประมวลผลการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="78334-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="78334-105">ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทตัวอย่าง GBSI </span><span class="sxs-lookup"><span data-stu-id="78334-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="78334-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำให้ขั้นตอนในกระบวนงาน "สร้างการตั้งค่าคอนฟิกด้วยรูปแบบของเอกสารการชำระเงิน" เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="78334-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="78334-107">เปลี่ยนการตั้งค่าคอนฟิกของวิธีการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="78334-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="78334-108">ไปที่บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="78334-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="78334-109">สลับส่วนรูปแบบไฟล์เพื่อขยาย ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="78334-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="78334-110">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="78334-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="78334-111">ตัวอย่างเช่น กรองข้อมูลในฟิลด์วิธีการชำระเงินด้วยค่า 'Electronic'</span><span class="sxs-lookup"><span data-stu-id="78334-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="78334-112">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="78334-112">Click Edit.</span></span>
5. <span data-ttu-id="78334-113">ตั้งค่าฟิลด์การรายงานทางอิเล็กทรอนิกส์ทั่วไปเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="78334-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="78334-114">เลือก ใช่ เพื่อใช้รูปแบบการรายงานทางอิเล็กทรอนิกส์ทั่วไป สำหรับการสร้างไฟล์การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="78334-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="78334-115">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="78334-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="78334-116">เลือกการตั้งค่าคอนฟิกรูปแบบ BACS (แบบสมมติ UK)</span><span class="sxs-lookup"><span data-stu-id="78334-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="78334-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="78334-117">Click Save.</span></span>
9. <span data-ttu-id="78334-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="78334-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="78334-119">ทดสอบรูปแบบของไฟล์การชำระเงินที่สร้างไว้</span><span class="sxs-lookup"><span data-stu-id="78334-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="78334-120">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="78334-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="78334-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="78334-121">Click New.</span></span>
3. <span data-ttu-id="78334-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78334-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="78334-123">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="78334-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="78334-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78334-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78334-125">เลือก VendPay</span><span class="sxs-lookup"><span data-stu-id="78334-125">Select VendPay.</span></span>  
6. <span data-ttu-id="78334-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="78334-126">Click Save.</span></span>
7. <span data-ttu-id="78334-127">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="78334-127">Click Lines.</span></span>
8. <span data-ttu-id="78334-128">ในฟิลด์บริษัท ให้พิมพ์ 'DEMF'</span><span class="sxs-lookup"><span data-stu-id="78334-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="78334-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="78334-129">DEMF</span></span>  
9. <span data-ttu-id="78334-130">ในฟิลด์บัญชี ให้ระบุค่า 'DE-01001'</span><span class="sxs-lookup"><span data-stu-id="78334-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="78334-131">DE-01001</span><span class="sxs-lookup"><span data-stu-id="78334-131">DE-01001</span></span>  
10. <span data-ttu-id="78334-132">ในฟิลด์คำอธิบาย ให้พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="78334-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="78334-133">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="78334-133">Payment</span></span>  
11. <span data-ttu-id="78334-134">ในฟิลด์เดบิต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="78334-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="78334-135">1000</span><span class="sxs-lookup"><span data-stu-id="78334-135">1000</span></span>  
12. <span data-ttu-id="78334-136">คลิกแท็บการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="78334-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="78334-137">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="78334-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="78334-138">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="78334-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78334-139">เลือกค่าอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="78334-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="78334-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78334-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="78334-141">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="78334-141">Click Save.</span></span>
17. <span data-ttu-id="78334-142">คลิกสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="78334-142">Click Generate payments.</span></span>
18. <span data-ttu-id="78334-143">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="78334-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="78334-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="78334-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78334-145">เลือกค่าอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="78334-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="78334-146">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78334-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78334-147">เลือกค่าอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="78334-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="78334-148">ในฟิลด์ชื่อไฟล์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="78334-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="78334-149">ตัวอย่างเช่น พิมพ์ 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="78334-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="78334-150">ในฟิลด์บัญชีธนาคาร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="78334-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="78334-151">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78334-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78334-152">เลือกค่า GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="78334-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="78334-153">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="78334-153">Click OK.</span></span>
25. <span data-ttu-id="78334-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="78334-154">Click OK.</span></span>
    * <span data-ttu-id="78334-155">วิเคราะห์ไฟล์การชำระเงินที่สร้างในรูปแบบ XML </span><span class="sxs-lookup"><span data-stu-id="78334-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="78334-156">เปรียบเทียบกับโครงร่างเอกสารที่ออกแบบไว้ และแอททริบิวต์ธุรกรรมการชำระเงินที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="78334-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]