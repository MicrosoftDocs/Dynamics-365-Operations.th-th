--- 
title: "สร้างลำดับของจดหมายเรียกเก็บเงิน"
description: "ใช้คำแนะนำของงานนี้เพื่อสร้างลำดับจดหมายเรียกเก็บเงิน "
author: mikefalkner
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 63f28194065821f898cc73678a9868ec9ee2c64b
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="360b5-103">สร้างลำดับของจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="360b5-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="360b5-104">ใช้คำแนะนำของงานนี้เพื่อสร้างลำดับจดหมายเรียกเก็บเงิน </span><span class="sxs-lookup"><span data-stu-id="360b5-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="360b5-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="360b5-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="360b5-106">ไปที่สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > การตั้งค่าลำดับจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="360b5-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="360b5-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="360b5-107">Click New.</span></span>
3. <span data-ttu-id="360b5-108">ในฟิลด์ลำดับจดหมายเรียกเก็บเงิน ป้อนรหัสลำดับที่จะแสดงถึงลำดับ </span><span class="sxs-lookup"><span data-stu-id="360b5-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="360b5-109">มันจะถูกใช้เมื่อคุณตั้งค่าโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="360b5-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="360b5-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="360b5-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="360b5-111">เงื่อนไขการชำระเงินไม่จำเป็นต้องระบุ </span><span class="sxs-lookup"><span data-stu-id="360b5-111">The terms of payment is optional.</span></span> <span data-ttu-id="360b5-112">ถ้าคุณป้อนค่าที่นี่ ใบแจ้งหนี้ค่าธรรมเนียมของจดหมายเรียกเก็บเงินจะใช้เงื่อนไขการชำระเงินเหล่านี้แทนเงื่อนไขการชำระเงินที่จัดเก็บไว้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="360b5-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="360b5-113">ในฟิลด์รหัสจดหมายเรียกเก็บเงิน เลือกรหัสของจดหมายเรียกเก็บเงินครั้งแรกที่คุณต้องการส่ง</span><span class="sxs-lookup"><span data-stu-id="360b5-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="360b5-114">จดหมายเรียกเก็บเงินฉบับแรกถูกสร้างตามวันครบกำหนดชำระในใบแจ้งหนี้ ค่าที่คุณป้อนสำหรับระยะเวลาผ่อนผันในฟิลด์วันที่ของบรรทัดนี้ และข้อมูลอื่นๆที่คุณป้อนในบรรทัดนี้</span><span class="sxs-lookup"><span data-stu-id="360b5-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="360b5-115">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="360b5-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="360b5-116">สกุลเงินสำหรับค่าธรรมเนียมเป็นค่าเริ่มต้นของสกุลเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="360b5-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="360b5-117">รหัสสกุลเงินนี้อาจแตกต่างจากสกุลเงินของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="360b5-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="360b5-118">คลิกเพิ่ม เพื่อเพิ่มจดหมายเรียกเก็บเงินถัดไปที่จะถูกส่งในลำดับ</span><span class="sxs-lookup"><span data-stu-id="360b5-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="360b5-119">ในหลายกรณี จดหมายเรียกเก็บเงินแรกเป็นเพียงคำเตือน </span><span class="sxs-lookup"><span data-stu-id="360b5-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="360b5-120">คุณสามารถเพิ่มค่าธรรมเนียมได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="360b5-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="360b5-121">ในฟิลด์รหัสจดหมายเรียกเก็บเงิน เลือกรหัสของจดหมายเรียกเก็บเงินถัดไปที่คุณต้องการส่งในลำดับ</span><span class="sxs-lookup"><span data-stu-id="360b5-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="360b5-122">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="360b5-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="360b5-123">ในฟิลด์บัญชีหลัก เลือกบัญชีรายได้ที่จะใช้สำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="360b5-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="360b5-124">ป้อนค่าธรรมเนียมที่จะคิดค่าธรรมเนียมเมื่อจดหมายเรียกเก็บเงินนี้ถูกการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="360b5-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="360b5-125">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="360b5-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="360b5-126">เลือกกลุ่มภาษีขายของสินค้าถ้าต้องคำนวณภาษีขายของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="360b5-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="360b5-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="360b5-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="360b5-128">ป้อนยอดดุลที่พ้นกำหนดชำระต่ำสุดที่จำเป็นก่อนการสร้างจดหมายเรียกเก็บเงินถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="360b5-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="360b5-129">ป้อนจำนวนวันปลอดหนี้ที่คุณจะอนุญาต</span><span class="sxs-lookup"><span data-stu-id="360b5-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="360b5-130">นี่คือจำนวนวันหลังจากวันครบกำหนดที่สามารถสร้างจดหมายเรียกเก็บเงินได้ </span><span class="sxs-lookup"><span data-stu-id="360b5-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="360b5-131">วันครบกำหนดที่จะใช้สำหรับการคำนวณขึ้นอยู่กับตำแหน่งของจดหมายเรียกเก็บเงินในลำดับจดหมายเรียกเก็บเงิน:   ⦁    ระยะเวลาผ่อนผันสำหรับจดหมายเรียกเก็บเงิน 1 จะสัมพันธ์กับวันครบกำหนดชำระบนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="360b5-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="360b5-132">⦁ ระยะเวลาผ่อนผันสำหรับจดหมายเรียกเก็บเงิน 2 และสูงกว่านี้จะสัมพันธ์กับวันที่จดหมายเรียกเก็บเงินก่อนหน้าถูกลงรายการบัญชีหรือพิมพ์ ขึ้นอยู่กับการเลือกในฟิลด์การอัพเดทรหัสจดหมายเรียกเก็บเงินในหน้าพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="360b5-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="360b5-133">คลิกเพิ่ม เพื่อเพิ่มจดหมายเรียกเก็บเงินล่าสุดที่จะถูกส่งในลำดับ</span><span class="sxs-lookup"><span data-stu-id="360b5-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="360b5-134">คุณสามารถเพิ่มรหัสจดหมายเรียกเก็บเงินได้มากถึง 5 รหัสสำหรับลำดับจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="360b5-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="360b5-135">ในฟิลด์รหัสจดหมายเรียกเก็บเงิน เลือกรหัสของจดหมายเรียกเก็บเงินถัดไปที่คุณต้องการส่งในลำดับ</span><span class="sxs-lookup"><span data-stu-id="360b5-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="360b5-136">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="360b5-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="360b5-137">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="360b5-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="360b5-138">ในฟิลด์ค่าธรรมเนียมในสกุลเงิน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="360b5-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="360b5-139">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="360b5-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="360b5-140">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="360b5-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="360b5-141">ในฟิลด์ยอดดุลที่พ้นกำหนดชำระต่ำสุด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="360b5-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="360b5-142">ในฟิลด์จำนวนวัน ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="360b5-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="360b5-143">เลือกกล่องกาเครื่องหมายนี้เพื่อหยุดลูกค้าไม่ให้จัดส่งและออกอินวอยซ์อีก</span><span class="sxs-lookup"><span data-stu-id="360b5-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="360b5-144">เพื่อเลิกบล็อกบัญชี เลือก ไม่ ในฟิลด์หมายเลขในการออกใบแจ้งหนี้และการจัดส่งการระงับในหน้าลูกค้า</span><span class="sxs-lookup"><span data-stu-id="360b5-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="360b5-145">ขยายแท็บด่วนของหมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="360b5-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="360b5-146">ป้อนข้อความที่จะปรากฏบนจดหมายเรียกเก็บเงินสำหรับรหัสจดหมายเรียกเก็บเงินที่เลือก</span><span class="sxs-lookup"><span data-stu-id="360b5-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="360b5-147">คุณสามารถแปลข้อความนี้ได้หลายภาษาโดยใช้เมนูแปลเหนือกล่องหมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="360b5-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


