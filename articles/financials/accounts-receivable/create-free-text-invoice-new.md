---
title: สร้างใบแจ้งหนี้ข้อความอิสระ
description: หัวข้อนี้อธิบายวิธีการสร้างใบแจ้งหนี้ข้อความอิสระ
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4498f5c9ce0e3830ffe1857c0363ca962561fc59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836783"
---
# <a name="create-free-text-invoices"></a><span data-ttu-id="0ce6c-103">สร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="0ce6c-103">Create free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ce6c-104">หัวข้อนี้อธิบายวิธีการสร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="0ce6c-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="0ce6c-105">สำหรับกระบวนงาน ใช้บริษัทสาธิต **USMF**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="0ce6c-106">สร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="0ce6c-106">Create a free text invoice</span></span>

1. <span data-ttu-id="0ce6c-107">ไปที่ **บัญชีลูกหนี้ \> ใบแจ้งหนี้ \> ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="0ce6c-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-108">Select **New**.</span></span>
3. <span data-ttu-id="0ce6c-109">ในฟิลด์ **บัญชีลูกค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0ce6c-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="0ce6c-110">โดยค่าเริ่มต้น บัญชีที่ถูกเลือกเป็นบัญชีลูกค้าจะถูกใช้เป็นบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="0ce6c-111">ถ้าไม่มีการลงรายการบัญชีใบแจ้งหนี้ สถานะการลงบัญชีเริ่มต้นด้วย **อยู่ระหว่างดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="0ce6c-112">หมายเลขใบแจ้งหนี้จะถูกกำหนดเมื่อมีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="0ce6c-113">ถ้าคุณกำลังใช้ข้อบังคับ Single Euro Payments Area (SEPA) ข้อตกลงการหักบัญชีเงินฝากอัตโนมัติจะถูกป้อนโดยอัตโนมัติ เมื่อคุณเลือกบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0ce6c-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="0ce6c-114">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="0ce6c-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="0ce6c-115">ในฟิลด์ **บัญชีหลัก** ให้ระบุหมายเลขบัญชีที่ไม่มีมิติ</span><span class="sxs-lookup"><span data-stu-id="0ce6c-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="0ce6c-116">คุณจะป้อนมิติในภายหลังในคู่มือนี้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="0ce6c-117">นอกจากนี้ คุณยังสามารถป้อนอักขระหนึ่งอักขระหรือมากกว่าสำหรับบัญชีหลัก และใช้การค้นหาเพื่อค้นหาบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="0ce6c-118">เลือก FastTab **รายละเอียดของรายการ** เพื่อเพิ่มมิติไปยังบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="0ce6c-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="0ce6c-119">เลือกแท็บ **รายการมิติทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="0ce6c-120">ค่ามิติใช้สำหรับรายการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ce6c-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="0ce6c-121">กลุ่มภาษีขายจะถูกเติมจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0ce6c-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="0ce6c-122">ถ้าลูกค้าไม่มีกลุ่มภาษีขาย จะมีการใช้กลุ่มภาษีขายจากบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="0ce6c-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="0ce6c-123">กลุ่มภาษีขายตามประเภทสินค้าถูกเติมข้อมูลจากบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="0ce6c-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="0ce6c-124">ถ้าบัญชีหลักไม่มีกลุ่มภาษีขายตามประเภทสินค้า จะมีการใช้กลุ่มภาษีขายตามประเภทสินค้าที่ระบุในพารามิเตอร์ภาษีขายในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="0ce6c-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="0ce6c-125">ไม่จำเป็นต้องระบุ: ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0ce6c-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="0ce6c-126">ไม่จำเป็นต้องระบุ: ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0ce6c-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="0ce6c-127">ยอดเงินจะถูกคำนวณจากปริมาณคูณด้วยราคาต่อหน่วย </span><span class="sxs-lookup"><span data-stu-id="0ce6c-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="0ce6c-128">อย่างไรก็ตาม คุณสามารถแทนการคำนวณนั้นได้โดยการป้อนจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="0ce6c-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="0ce6c-129">เลือก **ภาษีขาย** เพื่อดูภาษีขายที่ถูกคำนวณสำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="0ce6c-130">คุณสามารถดูยอดภาษีขายในหน้านี้ หรือคุณสามารถแทนยอดเงินบนแท็บ **การปรับปรุง** ได้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="0ce6c-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-131">Select **OK**.</span></span>
12. <span data-ttu-id="0ce6c-132">เลือก **ค่าธรรมเนียม** เพื่อเพิ่มค่าธรรมเนียมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="0ce6c-133">ในฟิลด์ **รหัสค่าธรรมเนียม** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0ce6c-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="0ce6c-134">ในฟิลด์ **มูลค่าของค่าธรรมเนียม** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0ce6c-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="0ce6c-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0ce6c-135">Close the page.</span></span>
16. <span data-ttu-id="0ce6c-136">เลือก **ผลรวม** เพื่อดูสรุปของรายละเอียดใบแจ้งหนี้และผลรวม</span><span class="sxs-lookup"><span data-stu-id="0ce6c-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="0ce6c-137">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-137">Select **Close**.</span></span>
18. <span data-ttu-id="0ce6c-138">เลือก **ลงรายการบัญชี** เพื่อลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="0ce6c-139">คุณจะยังคงมีโอกาสในการยกเลิก ก่อนที่คุณจะลงรายการบัญชีจริงๆ</span><span class="sxs-lookup"><span data-stu-id="0ce6c-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="0ce6c-140">คุณสามารถเปลี่ยนช่วงเวลาของการพิมพ์ใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="0ce6c-141">เลือก **ปัจจุบัน** เพื่อพิมพ์ใบแจ้งหนี้แต่ละฉบับเมื่อมีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="0ce6c-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="0ce6c-142">เลือก **หลังจาก** เพื่อพิมพ์เอกสารหลังจากการอัพเดตใบแจ้งหนี้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0ce6c-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="0ce6c-143">เมื่อต้องการเปลี่ยนวิธีการตรวจสอบวงเงินสินเชื่อของลูกค้า ก่อนที่จะลงรายการบัญชีใบแจ้งหนี้ เปลี่ยนค่าในฟิลด์ **ชนิดวงเงินสินเชื่อ**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="0ce6c-144">เพื่อพิมพ์ใบแจ้งหนี้ ตั้งค่าตัวเลือกนี้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="0ce6c-145">เพื่อลงรายการบัญชีใบแจ้งหนี้ ตั้งค่าตัวเลือกนี้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="0ce6c-146">คุณสามารถพิมพ์ใบแจ้งหนี้ได้โดยไม่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="0ce6c-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="0ce6c-147">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="0ce6c-148">คัดลอกรายการ</span><span class="sxs-lookup"><span data-stu-id="0ce6c-148">Copy lines</span></span>
<span data-ttu-id="0ce6c-149">ในการคัดลอกรายการในใบแจ้งหนี้ข้อความอิสระ เลือกอย่างน้อยหนึ่งรายการ แล้วจากนั้น เลือก **คัดลอกรายการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="0ce6c-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="0ce6c-150">คุณสามารถระบุจำนวนของสำเนาเพื่อสร้าง และคุณยังสามารถคัดลอกบันทึกย่อและสิ่งที่แนบมาได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="0ce6c-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="0ce6c-151">คุณสามารถคัดลอกการกระจาย หรืออนุญาตให้ถูกสร้างขึ้นใหม่ เมื่อคุณลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="0ce6c-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="0ce6c-152">หลังจากที่คุณคัดลอกรายการ คุณสามารถแก้ไขข้อมูลได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ce6c-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="0ce6c-153">สร้างใบแจ้งหนี้ข้อความอิสระจากเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="0ce6c-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="0ce6c-154">คุณสามารถสร้างใบแจ้งหนี้ข้อความอิสระจากเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="0ce6c-155">เมื่อคุณเลือก **สร้างจากเท็มเพลต** ในแท็บ **ใบแจ้งหนี้** คุณสามารถเลือกชื่อเท็มเพลตและบัญชีลูกค้าสำหรับใบแจ้งหนี้ข้อความอิสระใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="0ce6c-156">ค่าเริ่มต้น เช่น เงื่อนไขในการชำระเงิน และวิธีของการชำระเงิน สามารถถูกเติมข้อมูลโดยอัตโนมัติได้จากลูกค้า หรือคุณสามารถใช้ค่าที่ถูกบันทึกไว้ในเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="0ce6c-157">ใบแจ้งหนี้ข้อความอิสระใหม่จะถูกสร้างขึ้น และคุณสามารถแก้ไขค่าตามที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="0ce6c-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
