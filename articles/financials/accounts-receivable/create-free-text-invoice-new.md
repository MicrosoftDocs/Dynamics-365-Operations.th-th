--- 
title: "สร้างใบแจ้งหนี้ข้อความอิสระ"
description: "บทความนี้สาธิตวิธีการสร้างใบแจ้งหนี้ข้อความอิสระ"
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="33949-103">สร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="33949-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33949-104">บทความนี้สาธิตวิธีการสร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="33949-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="33949-105">สำหรับกระบวนงานนี้ ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="33949-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="33949-106">สร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="33949-106">Create a free text invoice</span></span>

1. <span data-ttu-id="33949-107">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="33949-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="33949-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="33949-108">Click New.</span></span>
3. <span data-ttu-id="33949-109">ในฟิลด์บัญชีลูกค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="33949-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="33949-110">บัญชีใบแจ้งหนี้จะเป็นค่าเริ่มต้นของบัญชีเดียวกันกับที่ใช้เป็นบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="33949-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="33949-111">สถานะการลงบัญชีเริ่มต้นด้วย อยู่ระหว่างดำเนินการ ถ้าไม่มีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="33949-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="33949-112">หมายเลขใบแจ้งหนี้จะถูกกำหนดเมื่อมีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="33949-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="33949-113">ถ้าคุณกำลังใช้ข้อบังคับ SEPA ข้อตกลงในการหักบัญชีเงินฝากอัตโนมัติจะมีการเติมข้อมูลโดยอัตโนมัติด้วยข้อบังคับเมื่อคุณเลือกบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="33949-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="33949-114">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="33949-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="33949-115">ในฟิลด์บัญชีหลัก ให้ระบุหมายเลขบัญชีโดยไม่มีมิติ</span><span class="sxs-lookup"><span data-stu-id="33949-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="33949-116">นอกจากนี้คุณยังสามารถป้อนอักขระหนึ่งอักขระหรือมากกว่าสำหรับบัญชีหลัก และใช้การค้นหาเพื่อค้นหาบัญชีของคุณ </span><span class="sxs-lookup"><span data-stu-id="33949-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="33949-117">คุณจะป้อนมิติในภายหลังในคู่มือนี้</span><span class="sxs-lookup"><span data-stu-id="33949-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="33949-118">ขยายแท็บด่วน รายละเอียดรายการ เพื่อให้คุณสามารถเพิ่มมิติไปยังบัญชีหลักของคุณ</span><span class="sxs-lookup"><span data-stu-id="33949-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="33949-119">คลิกแท็บ รายการมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="33949-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="33949-120">ค่ามิติใช้สำหรับรายการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="33949-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="33949-121">กลุ่มภาษีขายจะถูกเติมจากลูกค้า </span><span class="sxs-lookup"><span data-stu-id="33949-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="33949-122">ถ้าลูกค้าไม่มีกลุ่มภาษีขาย จะมีการใช้กลุ่มภาษีขายจากบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="33949-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="33949-123">กลุ่มภาษีขายตามประเภทสินค้ามีการเติมข้อมูลจากบัญชีหลัก </span><span class="sxs-lookup"><span data-stu-id="33949-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="33949-124">ถ้าบัญชีหลักไม่มีกลุ่มภาษีขายตามประเภทสินค้า จะมีการใช้กลุ่มภาษีขายตามประเภทสินค้าในพารามิเตอร์ภาษีขายของบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="33949-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="33949-125">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="33949-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="33949-126">ไม่จำเป็นต้องระบุปริมาณ</span><span class="sxs-lookup"><span data-stu-id="33949-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="33949-127">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="33949-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="33949-128">ราคาต่อหน่วยไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="33949-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="33949-129">ยอดเงินจะถูกคำนวณจากปริมาณคูณด้วยราคาต่อหน่วย </span><span class="sxs-lookup"><span data-stu-id="33949-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="33949-130">อย่างไรก็ตาม คุณสามารถแทนการคำนวณนั้นและป้อนจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="33949-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="33949-131">คลิก ภาษีขาย เพื่อดูภาษีขายที่คำนวณได้สำหรับใบแจ้งหนี้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="33949-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="33949-132">ดูยอดภาษีขายในหน้านี้ หรือคุณสามารถแทนยอดเงินบนแท็บการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="33949-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="33949-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="33949-133">Click OK.</span></span>
12. <span data-ttu-id="33949-134">คลิกที่ค่าธรรมเนียมเพื่อเพิ่มค่าธรรมเนียมในใบแจ้งหนี้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="33949-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="33949-135">ในฟิลด์รหัสค่าธรรมเนียม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="33949-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="33949-136">ในฟิลด์มูลค่าของค่าธรรมเนียม ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="33949-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="33949-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="33949-137">Close the page.</span></span>
16. <span data-ttu-id="33949-138">คลิก ผลรวม เพื่อดูสรุปรายละเอียดใบแจ้งหนี้และผลรวม</span><span class="sxs-lookup"><span data-stu-id="33949-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="33949-139">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="33949-139">Click Close.</span></span>
18. <span data-ttu-id="33949-140">คลิกที่ลงรายการบัญชีเพื่อลงรายการบัญชีใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="33949-140">Click Post to post the invoice.</span></span> <span data-ttu-id="33949-141">คุณสามารถยกเลิกก่อนที่คุณจะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="33949-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="33949-142">เมื่อต้องการเปลี่ยนช่วงเวลาของการพิมพ์ใบแจ้งหนี้: ให้เลือก ปัจจุบัน เพื่อพิมพ์ใบแจ้งหนี้แต่ละใบเมื่อมีการอัพเดต หรือเลือก หลังจาก เพื่อพิมพ์ใบแจ้งหนี้หลังจากที่ได้รับการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="33949-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="33949-143">ถ้าคุณต้องการเปลี่ยนวิธีการตรวจสอบวงเงินสินเชื่อของลูกค้าก่อนที่จะลงรายการบัญชี ให้เปลี่ยนชนิดวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="33949-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="33949-144">ถ้าคุณต้องการพิมพ์ใบแจ้งหนี้ เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="33949-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="33949-145">ถ้าคุณต้องการลงรายการบัญชีใบแจ้งหนี้ เลือก ใช่ </span><span class="sxs-lookup"><span data-stu-id="33949-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="33949-146">คุณสามารถพิมพ์ใบแจ้งหนี้โดยไม่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="33949-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="33949-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="33949-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="33949-148">คัดลอกรายการ</span><span class="sxs-lookup"><span data-stu-id="33949-148">Copy lines</span></span>
<span data-ttu-id="33949-149">ในการคัดลอกรายการในใบแจ้งหนี้ข้อความอิสระ เลือกอย่างน้อยหนึ่งรายการ แล้วคลิกคัดลอกรายการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="33949-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="33949-150">คุณสามารถระบุจำนวนของสำเนาที่คุณต้องการสร้าง และคุณยังสามารถคัดลอกบันทึกย่อและสิ่งที่แนบมาได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="33949-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="33949-151">คุณสามารถคัดลอกการกระจาย หรืออนุญาตให้ถูกสร้างขึ้นใหม่ เมื่อคุณลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="33949-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="33949-152">เมื่อคุณคัดลอกรายการ คุณสามารถแก้ไขข้อมูลได้ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="33949-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="33949-153">สร้างใบแจ้งหนี้ข้อความอิสระจากเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="33949-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="33949-154">คุณสามารถสร้างใบแจ้งหนี้ข้อความอิสระจากเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="33949-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="33949-155">เมื่อคุณเลือกสร้างจากเท็มเพลตจากแท็บใบแจ้งหนี้ คุณสามารถเลือกชื่อเท็มเพลตและบัญชีลูกค้าสำหรับใบแจ้งหนี้ข้อความอิสระใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="33949-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="33949-156">นอกจากนี้ คุณยังสามารถเลือกเป็นค่าเริ่มต้นได้ เช่น เงื่อนไขการชำระเงิน และวิธีการชำระเงินจากลูกค้า หรือใช้ค่าที่ได้รับการบันทึกด้วยเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="33949-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="33949-157">ใบแจ้งหนี้ข้อความอิสระใหม่จะถูกสร้างขึ้น และคุณสามารถแก้ไขค่าในใบแจ้งหนี้นั้นได้</span><span class="sxs-lookup"><span data-stu-id="33949-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


