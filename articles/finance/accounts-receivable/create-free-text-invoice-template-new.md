---
title: สร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ
description: กระบวนงานนี้สาธิตวิธีการสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ
author: ShivamPandey-msft
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79f969d0e63458b5327950cfed98e0f3ba2cd7ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816327"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="a83b3-103">สร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="a83b3-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a83b3-104">สำหรับการฝึกปฏิบัตินี้ ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="a83b3-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="a83b3-105">กระบวนงานนี้จัดทำขึ้นสำหรับผู้ใช้ที่รับผิดชอบการจัดการและการประมวลผลใบแจ้งหนี้ A/R</span><span class="sxs-lookup"><span data-stu-id="a83b3-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="a83b3-106">สร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a83b3-106">Create a template</span></span>

1. <span data-ttu-id="a83b3-107">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ที่เกิดซ้ำ > เท็มเพลตใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="a83b3-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="a83b3-108">ใช้แบบฟอร์มนี้เพื่อสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระที่สามารถรวมรายการใบแจ้งหนี้ ค่าธรรมเนียม เท็มเพลตการกระจายการลงบัญชี และข้อมูลบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="a83b3-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="a83b3-109">คลิก 'สร้าง' เพื่อสร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระใหม่</span><span class="sxs-lookup"><span data-stu-id="a83b3-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="a83b3-110">ในฟิลด์ชื่อเท็มเพลต ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a83b3-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="a83b3-111">'ชื่อเท็มเพลต' บ่งชี้เท็มเพลใบแจ้งหนี้ข้อความอิสระโดยเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="a83b3-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="a83b3-112">เท็มเพลตสองอันไม่สามารถมี 'ชื่อเท็มเพลต' เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a83b3-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="a83b3-113">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a83b3-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="a83b3-114">ขยายแท็บรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="a83b3-115">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="a83b3-116">ในฟิลด์บัญชีหลัก เลือกบัญชีรายได้</span><span class="sxs-lookup"><span data-stu-id="a83b3-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="a83b3-117">คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้าโพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a83b3-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="a83b3-118">ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a83b3-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a83b3-119">กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a83b3-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="a83b3-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a83b3-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a83b3-121">ในฟิลด์กลุ่มภาษีขาย เลือกกลุ่มภาษีขายของสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a83b3-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="a83b3-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a83b3-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="a83b3-123">ในฟิลด์ราคาต่อหน่วย ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="a83b3-124">ยอดเงินนี้จะถูกคูณด้วยฟิลด์ปริมาณโดยอัตโนมัติเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="a83b3-125">เพิ่มรายการใหม่สำหรับเท็มเพลตใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="a83b3-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="a83b3-126">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="a83b3-127">ในฟิลด์บัญชีหลัก เลือกบัญชีรายได้</span><span class="sxs-lookup"><span data-stu-id="a83b3-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="a83b3-128">คุณสามารถเลือกกำหนดบัญชีธุรกรรมออฟเซ็ตของเครดิตลูกค้าสำหรับยอดเงินใบแจ้งหนี้ทั้งหมดรวมในหน้าโพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a83b3-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="a83b3-129">ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a83b3-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a83b3-130">กลุ่มภาษีขายสำหรับรายการใบแจ้งหนี้ปัจจุบัน เป็นกลุ่มภาษีขายเริ่มต้นสำหรับบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a83b3-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="a83b3-131">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a83b3-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="a83b3-132">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="a83b3-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a83b3-133">กลุ่มภาษีขายตามประเภทสินค้าสำหรับรายการใบแจ้งหนี้ปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="a83b3-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="a83b3-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a83b3-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="a83b3-135">ป้อนหรือดูจำนวนหน่วยสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="a83b3-136">ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ราคาต่อหน่วยเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="a83b3-137">ป้อนหรือดูราคาต่อหน่วยสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="a83b3-138">ยอดเงินนี้จะถูกคูณด้วยค่าในฟิลด์ปริมาณเพื่อกำหนดยอดเงินรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a83b3-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="a83b3-139">ดูและแก้ไขการกระจายการลงบัญชีสำหรับแต่ละบรรทัดและรายการรองใดๆ</span><span class="sxs-lookup"><span data-stu-id="a83b3-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="a83b3-140">การกระจายการลงบัญชีกำหนดวิธีที่ยอดเงินจะถูกนำมาพิจารณา เช่น วิธีที่รายได้ ภาษี หรือค่าธรรมเนียมจะถูกนำมาพิจารณาสำหรับใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="a83b3-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="a83b3-141">อัพเดทการกระจายการลงบัญชีสำหรับรายการใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a83b3-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="a83b3-142">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="a83b3-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="a83b3-143">บันทึกใบแจ้งหนี้ข้อความอิสระเป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a83b3-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="a83b3-144">คุณยังสามารถบันทึกใบแจ้งหนี้ข้อความอิสระที่มีอยู่เป็นเท็มเพลตได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="a83b3-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="a83b3-145">เมื่อคุณเลือกบันทึกไปยังเท็มเพลตจากแท็บใบแจ้งหนี้ ใส่ชื่อและคำอธิบายสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="a83b3-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="a83b3-146">ถ้ามีเท็มเพลตที่มีชื่ออยู่แล้ว คุณจะเห็นการแจ้งเตือนว่า มีเท็มเพลตที่มีชื่อนั้นอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="a83b3-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="a83b3-147">คุณยังสามารถคลิกตกลงเพื่อแทนที่ได้</span><span class="sxs-lookup"><span data-stu-id="a83b3-147">You can still click on Ok to replace it.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]