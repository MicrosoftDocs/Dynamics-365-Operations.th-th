--- 
title: "สร้างใบแจ้งหนี้ข้อความอิสระ"
description: "คู่มืองานนี้แสดงการสร้างใบแจ้งหนี้ข้อความอิสระ "
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="2b3fb-103">สร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b3fb-104">คู่มืองานนี้แสดงการสร้างใบแจ้งหนี้ข้อความอิสระ </span><span class="sxs-lookup"><span data-stu-id="2b3fb-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="2b3fb-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="2b3fb-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2b3fb-106">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2b3fb-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="2b3fb-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2b3fb-107">Click New.</span></span>
3. <span data-ttu-id="2b3fb-108">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2b3fb-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="2b3fb-109">บัญชีใบแจ้งหนี้จะเป็นค่าเริ่มต้นของบัญชีเดียวกันกับที่ใช้เป็นบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2b3fb-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="2b3fb-110">สถานะการลงบัญชีเริ่มต้นด้วย อยู่ระหว่างดำเนินการ ถ้าไม่มีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2b3fb-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="2b3fb-111">หมายเลขใบแจ้งหนี้จะถูกกำหนดเมื่อมีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2b3fb-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="2b3fb-112">ถ้าคุณกำลังใช้ข้อบังคับ SEPA ข้อตกลงในการหักบัญชีเงินฝากอัตโนมัติจะมีการเติมข้อมูลโดยอัตโนมัติด้วยข้อบังคับเมื่อคุณเลือกบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2b3fb-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="2b3fb-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2b3fb-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2b3fb-114">ในฟิลด์บัญชีหลัก ให้ระบุหมายเลขบัญชีโดยไม่มีมิติ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="2b3fb-115">นอกจากนี้คุณยังสามารถป้อนอักขระหนึ่งอักขระหรือมากกว่าสำหรับบัญชีหลัก และใช้การค้นหาเพื่อค้นหาบัญชีของคุณ </span><span class="sxs-lookup"><span data-stu-id="2b3fb-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="2b3fb-116">คุณจะป้อนมิติในภายหลังในคู่มือนี้</span><span class="sxs-lookup"><span data-stu-id="2b3fb-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="2b3fb-117">ขยายแท็บด่วน รายละเอียดรายการ เพื่อให้คุณสามารถเพิ่มมิติไปยังบัญชีหลักของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="2b3fb-118">คลิกแท็บ รายการมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="2b3fb-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="2b3fb-119">ค่ามิติใช้สำหรับรายการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2b3fb-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="2b3fb-120">กลุ่มภาษีขายจะถูกเติมจากลูกค้า </span><span class="sxs-lookup"><span data-stu-id="2b3fb-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="2b3fb-121">ถ้าลูกค้าไม่มีกลุ่มภาษีขาย จะมีการใช้กลุ่มภาษีขายจากบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="2b3fb-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="2b3fb-122">กลุ่มภาษีขายตามประเภทสินค้ามีการเติมข้อมูลจากบัญชีหลัก </span><span class="sxs-lookup"><span data-stu-id="2b3fb-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="2b3fb-123">ถ้าบัญชีหลักไม่มีกลุ่มภาษีขายตามประเภทสินค้า จะมีการใช้กลุ่มภาษีขายตามประเภทสินค้าในพารามิเตอร์บัญชีแยกประเภททั่วไปภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="2b3fb-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="2b3fb-124">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="2b3fb-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2b3fb-125">ไม่จำเป็นต้องระบุปริมาณ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="2b3fb-126">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="2b3fb-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="2b3fb-127">ราคาต่อหน่วยไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="2b3fb-128">ยอดเงินจะถูกคำนวณจากปริมาณคูณด้วยราคาต่อหน่วย </span><span class="sxs-lookup"><span data-stu-id="2b3fb-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="2b3fb-129">อย่างไรก็ตาม คุณสามารถแทนการคำนวณนั้นและป้อนจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="2b3fb-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="2b3fb-130">คลิก ภาษีขาย เพื่อดูภาษีขายที่คำนวณได้สำหรับใบแจ้งหนี้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="2b3fb-131">ดูยอดภาษีขายในหน้านี้ หรือคุณสามารถแทนยอดเงินบนแท็บการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="2b3fb-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="2b3fb-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2b3fb-132">Click OK.</span></span>
12. <span data-ttu-id="2b3fb-133">คลิกที่ค่าธรรมเนียมเพื่อเพิ่มค่าธรรมเนียมในใบแจ้งหนี้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="2b3fb-134">ในฟิลด์รหัสค่าธรรมเนียม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2b3fb-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="2b3fb-135">ในฟิลด์มูลค่าของค่าธรรมเนียม ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2b3fb-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="2b3fb-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2b3fb-136">Close the page.</span></span>
16. <span data-ttu-id="2b3fb-137">คลิก ผลรวม เพื่อดูสรุปรายละเอียดใบแจ้งหนี้และผลรวม</span><span class="sxs-lookup"><span data-stu-id="2b3fb-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="2b3fb-138">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="2b3fb-138">Click Close.</span></span>
18. <span data-ttu-id="2b3fb-139">คลิกที่ลงรายการบัญชีเพื่อลงรายการบัญชีใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="2b3fb-139">Click Post to post the invoice.</span></span> <span data-ttu-id="2b3fb-140">คุณสามารถยกเลิกก่อนที่คุณจะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2b3fb-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="2b3fb-141">เมื่อต้องการเปลี่ยนช่วงเวลาของการพิมพ์ใบแจ้งหนี้: ให้เลือก ปัจจุบัน เพื่อพิมพ์ใบแจ้งหนี้แต่ละใบเมื่อมีการอัพเดต หรือเลือก หลังจาก เพื่อพิมพ์ใบแจ้งหนี้หลังจากที่ได้รับการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="2b3fb-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="2b3fb-142">ถ้าคุณต้องการเปลี่ยนวิธีการตรวจสอบวงเงินสินเชื่อของลูกค้าก่อนที่จะลงรายการบัญชี ให้เปลี่ยนชนิดวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="2b3fb-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="2b3fb-143">ถ้าคุณต้องการพิมพ์ใบแจ้งหนี้ เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="2b3fb-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="2b3fb-144">ถ้าคุณต้องการลงรายการบัญชีใบแจ้งหนี้ เลือก ใช่ </span><span class="sxs-lookup"><span data-stu-id="2b3fb-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="2b3fb-145">คุณสามารถพิมพ์ใบแจ้งหนี้โดยไม่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2b3fb-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="2b3fb-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2b3fb-146">Click OK.</span></span>


